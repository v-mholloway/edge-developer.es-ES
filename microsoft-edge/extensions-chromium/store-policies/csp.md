---
description: Directiva de seguridad de contenido para extensiones perimetrales (Chromium).
title: Directiva de seguridad de contenido (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: db4a1595bf9ee691a141435a374ed8874cdd272ce1a1b928fe72348f38922fc7
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11803590"
---
# <a name="content-security-policy-csp"></a>Directiva de seguridad de contenido \(CSP\)  

Para mitigar una gran clase de posibles problemas de scripting entre sitios, el sistema de extensión de Microsoft Edge ha incorporado el concepto general de directiva de seguridad de contenido [\(CSP\)][W3CContentSecurityPolicy].  Esto presenta algunas directivas bastante estrictas que hacen que las extensiones sean más seguras de forma predeterminada y le proporciona la capacidad de crear y aplicar reglas que rigen los tipos de contenido que pueden cargarse y ejecutarse por las extensiones y las aplicaciones.  

En general, CSP funciona como un mecanismo de bloqueo/lista de permitidos para los recursos cargados o ejecutados por las extensiones.  La definición de una directiva razonable para su extensión le permite tener en cuenta cuidadosamente los recursos que necesita la extensión y solicitar al explorador que se asegure de que esos son los únicos recursos a los que tiene acceso la Extensión.  Las directivas proporcionan seguridad por encima de los permisos de host que solicita la extensión; son una capa adicional de protección, no un reemplazo.  

En la web, dicha directiva se define a través de un elemento o encabezado `meta` HTTP.  Dentro del Microsoft Edge extension, ninguno de los dos es un mecanismo adecuado.  En su lugar, se define una directiva de extensión con `manifest.json` el archivo de la extensión de la siguiente manera:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Para obtener información completa acerca de la [][W3CContentSecurityPolicy] sintaxis de CSP, consulte la especificación de directiva de seguridad de contenido y el artículo "Introducción a la directiva de seguridad de [contenido"][HTML5RocksIntroductionContentSecurityPolicy] en HTML5Rocks.  

## <a name="default-policy-restrictions"></a>Restricciones de directiva predeterminadas  

Los paquetes que no definen una `manifest_version` no tienen una directiva de seguridad de contenido predeterminada.  Los paquetes que `manifest_version` elijan 2 tienen la siguiente directiva de seguridad de contenido predeterminada.  

```javascript
script-src 'self'; object-src 'self'
```  

La directiva agrega seguridad limitando las extensiones y las aplicaciones de tres maneras:  

**Las funciones Eval y relacionadas están deshabilitadas**  

El código como el siguiente no funciona:  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

Evaluar cadenas de JavaScript como esta es un vector de ataque XSS común.  En su lugar, debe escribir código como:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**JavaScript en línea no se ejecuta**  

JavaScript en línea no se ejecuta.  Esta restricción prohíbe tanto los bloques en línea como los controladores de eventos en `<script>` línea, como `<button onclick="...">` .

La primera restricción elimina una gran clase de ataques de scripting entre sitios al hacer que sea imposible ejecutar accidentalmente el script proporcionado por un tercero malintencionado.  Sin embargo, requiere que escriba el código con una separación limpia entre el contenido y el comportamiento \(que, por supuesto, debe hacer de todos modos, ¿no?\).  Un ejemplo puede hacerlo más claro.  Puede intentar escribir una ventana emergente Acción del explorador como una sola `pop-up.html` que contenga:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script>
            function awesome() {
                // do something awesome!
            }
            
            function totallyAwesome() {
                // do something TOTALLY awesome!
            }
            
            function clickHandler(element) {
                setTimeout("awesome(); totallyAwesome()", 1000);
            }
            
            function main() {
                // Initialization work goes here.
            }
        </script>
    </head>
    <body onload="main();">
        <button onclick="clickHandler(this)">
            Click for awesomeness!
        </button>
    </body>
</html>
```  

Tres cosas deben cambiar para que esto funcione de la manera que espera:  

*   La `clickHandler` definición debe moverse a un archivo JavaScript externo \( `popup.js` puede ser un buen destino).  
*   Las definiciones del controlador de eventos en línea deben reescribirse en términos de y `addEventListener` extraerse en `popup.js` .  
    Si está iniciando el programa con código como , considere la posibilidad de reemplazarlo conectando al evento del documento o al evento de la ventana, según `<body onload="main();">` `DOMContentLoaded` sus `load` requisitos.  Use el primero, ya que generalmente se desencadena más rápidamente.  

*   La `setTimeout` llamada debe reescribirse para evitar convertir la cadena `"awesome(); totallyAwesome()"` en JavaScript para que se ejecute.  
    Estos cambios pueden tener un aspecto parecido al siguiente:  

```javascript
function awesome() {
    // Do something awesome!
}

function totallyAwesome() {
    // do something TOTALLY awesome!
}

function awesomeTask() {
    awesome();
    totallyAwesome();
}

function clickHandler(e) {
    setTimeout(awesomeTask, 1000);
}

function main() {
    // Initialization work goes here.
}

// Add event listeners once the DOM has fully loaded by listening for the
// `DOMContentLoaded` event on the document, and adding your listeners to
// specific elements when it triggers.
document.addEventListener('DOMContentLoaded', function () {
    document.querySelector('button').addEventListener('click', clickHandler);
    main();
});
```  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="popup.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

**Solo se cargan los recursos de script y objeto locales**  

Los recursos de script y objeto solo se pueden cargar desde el paquete de extensión, no desde la web en general.  Esto garantiza que la extensión solo ejecute el código que aprobó específicamente, lo que impide que un atacante de red activo redirija malintencionadamente la solicitud de un recurso.  

En lugar de escribir código que dependa de la carga de jQuery \(o cualquier otra biblioteca\) desde un CDN externo, considere la posibilidad de incluir la versión específica de jQuery en el paquete de extensión.  Es decir, en lugar de:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

Descargue el archivo, inscríbalo en el paquete y escriba:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

## <a name="relaxing-the-default-policy"></a>Relajación de la directiva predeterminada  

**Script en línea**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Los scripts en línea pueden permitirse especificando el hash codificado en base64 del código fuente en la directiva.  Este hash debe ir precedido por el algoritmo hash usado \(sha256, sha384 o sha512\).  Para obtener un ejemplo, vaya a [Uso hash de los \<script\> elementos][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].  

**Script remoto**  

Si necesita algunos recursos de objeto u JavaScript externos, puede que relaje la directiva en una medida limitada al permitir la lista de orígenes seguros desde los que se deben aceptar scripts.  Compruebe que los recursos en tiempo de ejecución cargados con permisos elevados de una extensión son exactamente los recursos que espera y que no se reemplazan por un atacante de red activo.  Como los ataques de tipo [man-in-the-middle][WikiManMiddleAttacks] son triviales e indetectables a través de HTTP, esos orígenes no se aceptan.  

Actualmente, los desarrolladores pueden permitir orígenes de lista con los siguientes esquemas: `blob` , `filesystem` , y `https` `extension` .  La parte host del origen debe especificarse explícitamente para los `https` esquemas `extension` y.  Caracteres comodín genéricos como https:, y no están permitidos; se permiten caracteres `https://*` `https://*.com` comodín de subdominio `https://*.example.com` como.  Los dominios de la [lista Sufijo público][PublicSuffixList] también se ven como dominios genéricos de nivel superior.  Para cargar un recurso desde estos dominios, el subdominio debe aparecer explícitamente.  Por ejemplo, `https://*.cloudfront.net` no es válido, pero `https://XXXX.cloudfront.net` puede `https://*.XXXX.cloudfront.net` ser `allowlisted` .  

Para facilitar el desarrollo, los recursos cargados a través de HTTP desde los servidores de la máquina local pueden ser `allowlisted` .  Puede permitir el script de lista y los orígenes de objetos en cualquier puerto de cualquiera `http://127.0.0.1` o `http://localhost` .  

> [!NOTE]
> La restricción de los recursos cargados a través de HTTP solo se aplica a los recursos que se ejecutan directamente.  Sigue siendo libre, por ejemplo, para realizar conexiones a cualquier origen que quiera; la directiva predeterminada no restringe ni ninguna de las otras directivas `XMLHTTPRequest` CSP de ninguna `connect-src` manera.  

Una definición de directiva relajada que permite cargar recursos de script desde `example.com` https puede tener el siguiente aspecto:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Ambos `script-src` y `object-src` están definidos por la directiva.  Microsoft Edge no acepta una directiva que no limite cada uno de estos valores a \(al menos\) ' `self` '.  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**JavaScript evaluado**  

La directiva y las funciones relacionadas como , y pueden ser `eval()` `setTimeout(String)` `setInterval(String)` `new Function(String)` relajadas agregando `unsafe-eval` a la directiva:  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

Sin embargo, debe evitar las directivas de relajación.  Las funciones son vectores de ataque XSS notorios.  

## <a name="tightening-the-default-policy"></a>Ajustar la directiva predeterminada  

Por supuesto, puede ajustar esta directiva en la medida en que la extensión lo permita para aumentar la seguridad a expensas de la comodidad.  Para especificar que la extensión solo puede cargar recursos de cualquier tipo \(imágenes, y así sucesivamente\) del paquete de extensión asociado, por ejemplo, una directiva de puede `default-src 'self'` ser adecuada.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a>Scripts de contenido  

La directiva que se está analizando se aplica a las páginas en segundo plano y a las páginas de eventos de la extensión.  El modo en que los scripts de contenido se aplican a los scripts de contenido de la extensión es más complicado.  

Por lo general, los scripts de contenido no están sujetos al CSP de la extensión.  Dado que los scripts de contenido no son HTML, el impacto principal de esto es que pueden usar incluso si el CSP de la extensión no especifica , aunque esto `eval` `unsafe-eval` no se recomienda.  Además, el CSP de la página no se aplica a los scripts de contenido.  Más complicadas son las etiquetas que los scripts de contenido crean `<script>` y ponen en el DOM de la página en la que se ejecutan.  A estos se les hace referencia como scripts inyectados por DOM en el futuro.  

Los scripts inyectados por DOM que se ejecutan inmediatamente después de la inyección en la página se ejecutan como puede esperar.  Imagine un script de contenido con el siguiente código como un ejemplo sencillo:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Este script de contenido provoca `alert` una inmediatamente después de `document.write()` .  Tenga en cuenta que esto se ejecuta independientemente de la directiva que pueda especificar una página.
Sin embargo, el comportamiento se vuelve más complicado tanto dentro de ese script inyectado por DOM como para cualquier script que no se ejecute inmediatamente después de la inyección.  Imagine que la extensión se ejecuta en una página que proporciona un CSP asociado que especifica `script-src 'self'` .  Ahora imagine que el script de contenido ejecuta el siguiente código:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Si un usuario elige ese botón, el `onclick` script no se ejecuta.  Esto se debe a que el script no se ha ejecutado inmediatamente y el código no se interpreta hasta que el evento se produce no se considera parte del script de contenido, por lo que el CSP de la página \(no de extension\) restringe el `click` comportamiento.  Y como ese CSP no especifica , se bloquea el controlador de `unsafe-inline` eventos en línea.  
La forma correcta de implementar el comportamiento deseado en este caso puede ser agregar el controlador como una función del script de contenido de la `onclick` siguiente manera:  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Se produce otro problema similar si el script de contenido ejecuta lo siguiente:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

En este caso, se ejecuta el script y se muestra la alerta.  Sin embargo, tome este caso:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

Mientras se ejecuta el script inicial, se bloquea `eval` la llamada a.  Es decir, mientras se permite el tiempo de ejecución del script inicial, el comportamiento dentro del script está regulado por el CSP de la página.  
Por lo tanto, en función de cómo escriba los scripts inyectados de DOM en la extensión, los cambios en el CSP de la página pueden afectar al comportamiento de la extensión.  Dado que los scripts de contenido no se ven afectados por el CSP de la página, este es un gran motivo para colocar el mayor comportamiento posible de la extensión en el script de contenido en lugar de scripts inyectados por DOM.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Una introducción a la directiva de seguridad de contenido | Rocas de HTML5"  
[PublicSuffixList]: https://publicsuffix.org/list "VER LA LISTA DE SUFIJOS PÚBLICOS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Uso de hash para elementos \<script\>: nivel 2 de directiva de seguridad de contenido | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Directiva de seguridad de contenido nivel 3 | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Ataque man-in-the-middle | Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí.](https://developer.chrome.com/extensions/contentSecurityPolicy)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
