---
description: Directiva de seguridad de contenido para las extensiones de Edge (cromo).
title: Directiva de seguridad de contenido (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: f3769639465d048c42ad0705f74598fbd1db8a20
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015719"
---
# Directiva de seguridad de contenido \ (CSP \)  

Para mitigar una gran clase de posibles problemas de scripting entre sitios, el sistema de extensiones Microsoft Edge ha incorporado el concepto general de [Directiva de seguridad de contenido \ (CSP \)][W3CContentSecurityPolicy].  Esto presenta directivas muy estrictas que hacen que las extensiones sean más seguras de forma predeterminada y le proporcionan la capacidad de crear y aplicar reglas que rijan los tipos de contenido que las extensiones y aplicaciones pueden cargar y ejecutar.  

En general, CSP funciona como un mecanismo de bloqueo/allowlisting para los recursos cargados o ejecutados por las extensiones.  La definición de una directiva razonable para su extensión le permite considerar cuidadosamente los recursos que la extensión necesita y pedir al explorador que asegúrese de que son los únicos recursos a los que tiene acceso la extensión.  Estas directivas proporcionan seguridad y una mayor parte de los permisos de host y las solicitudes de extensión; son una capa adicional de protección, no un sustituto.  

En la web, tal directiva se define a través de un elemento o encabezado HTTP `meta` .  En el sistema de extensión Microsoft Edge, ninguno de los mecanismos es adecuado.  En su lugar, se define una política de extensión a través del `manifest.json` archivo para la extensión de la siguiente manera:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Para obtener información completa sobre la sintaxis de CSP, eche un vistazo a la especificación de la [política de seguridad de contenido][W3CContentSecurityPolicy] y el artículo ["una introducción a la Directiva de seguridad de contenido"][HTML5RocksIntroductionContentSecurityPolicy] en HTML5Rocks.  

## Restricciones de directiva predeterminadas  

Los paquetes que no definen una no `manifest_version` tienen una directiva de seguridad de contenido predeterminada.  Los que seleccionan `manifest_version` 2, tienen una directiva de seguridad de contenido predeterminada de:  

```javascript
script-src 'self'; object-src 'self'
```  

Esta directiva agrega seguridad limitando las extensiones y aplicaciones de tres maneras:  

**Eval y las funciones relacionadas están deshabilitadas**  

El código como el siguiente no funciona:  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

La evaluación de cadenas de JavaScript como esta es un vector de ataques XSS común.  En su lugar, debe escribir código como el siguiente:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**No se ejecutan JavaScript en línea**  

No se ejecutan los JavaScripts en línea.  Esta restricción prohíbe tanto los bloques alineados como los `<script>` controladores de eventos alineados, como `<button onclick="...">` .

La primera restricción elimina una enorme clase de ataques de scripting entre sitios, lo que le impide ejecutar accidentalmente la secuencia de comandos proporcionada por un tercero malintencionado.  Sin embargo, le pedirá que escriba su código con una separación clara entre el contenido y el comportamiento \ (¿qué debe hacer? de todos modos, ¿bien? \).  Un ejemplo puede hacer que sea más claro.  Puede intentar escribir un elemento emergente de acción del explorador como un único `pop-up.html` contenedor:  

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

Deben cambiarse tres cosas para que este funcione de la manera esperada:  

*   La `clickHandler` definición se debe mover a un archivo JavaScript externo \ ( `popup.js` puede ser un buen objetivo).  
*   Las definiciones de los controladores de eventos en línea se deben volver a escribir en términos de `addEventListener` y extraer en `popup.js` .  
    Si actualmente inicia su programa con un código como `<body onload="main();">` , considere la posibilidad de reemplazarlo enlazando el `DOMContentLoaded` evento del documento o el `load` evento de la ventana, en función de sus necesidades.  Use el antiguo, ya que generalmente se desencadena más rápidamente.  

*   La `setTimeout` llamada se debe volver a escribir para evitar convertir la cadena `"awesome(); totallyAwesome()"` en JavaScript para ejecutarla.  
    Esos cambios pueden tener un aspecto similar al siguiente:  

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

**Solo se cargan los recursos de objetos y scripts locales**  

Los recursos de scripts y objetos solo se pueden cargar desde el paquete de extensión, no desde la web en general.  Esto garantiza que su extensión solo ejecutará el código que haya aprobado específicamente, evitando que un atacante de red activa redirija su solicitud de un recurso por error.  

En lugar de escribir código que depende de jQuery \ (o cualquier otra biblioteca \) que se cargue desde una red CDN externa, considere la posibilidad de incluir la versión específica de jQuery en el paquete de extensión.  Es decir, en lugar de:  

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

Descargar el archivo, incluirlo en el paquete y escribir:  

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

## Cómo relajar la directiva predeterminada  

**Script en línea**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Los scripts en línea pueden permitirse especificando el hash codificado en base64 del código fuente de la Directiva.  Este hash debe ir precedido por el algoritmo hash usado \ (SHA256, SHA384 o SHA512 \).  Consulta el [uso de hash de \<script\> los elementos][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] para obtener un ejemplo.  

**Script remoto**  

Si necesita algunos recursos de JavaScript o de objeto externo, puede relajar la Directiva en una medida limitada por allowlisting los orígenes seguros de los que se deben aceptar las secuencias de comandos.  Compruebe que los recursos en tiempo de ejecución cargados con permisos elevados de una extensión son exactamente los recursos que espera y no son reemplazados por un atacante de red activo.  Dado que los [ataques de intermediario][WikiManMiddleAttacks] son sencillos y no detectables a través de http, no se aceptan esos orígenes.  

En la actualidad, los desarrolladores pueden lista denegados origen con los siguientes esquemas: `blob` ,, `filesystem` `https` , y `extension` .  La parte del host del origen debe especificarse explícitamente para `https` los `extension` esquemas y.  Los caracteres comodín genéricos, como https:, `https://*` y `https://*.com` no están permitidos; se permiten los caracteres comodín de subdominio, como por ejemplo `https://*.example.com` .  Los dominios de la [lista de sufijos públicos][PublicSuffixList] también se visualizan como dominios genéricos de nivel superior.  Para cargar un recurso desde estos dominios, el subdominio debe mostrarse explícitamente.  Por ejemplo, `https://*.cloudfront.net` no es válido, pero `https://XXXX.cloudfront.net` y `https://*.XXXX.cloudfront.net` puede ser allowlisted.  

Por facilidad de desarrollo, los recursos cargados por HTTP desde los servidores en el equipo local pueden allowlisted.  Puede lista denegados los orígenes de scripts y objetos en cualquier puerto de `http://127.0.0.1` o `http://localhost` .  

> [!NOTE]
> La restricción de los recursos cargados por HTTP solo se aplica a los recursos que se ejecutan directamente.  Sigue siendo gratis, por ejemplo, hacer conexiones de XMLHTTPRequest a cualquier origen que desee; la directiva predeterminada no se restringe `connect-src` de ninguna manera a las demás directivas de CSP ni ninguna de ellas.  

Una definición de directiva relajada que permite que los recursos de script se carguen desde example.com a través de HTTPS puede tener el siguiente aspecto:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Ambos `script-src` y `object-src` los define la Directiva.  Microsoft Edge no acepta una directiva que no limite cada uno de estos valores a \ (por lo menos \) ' `self` '.  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**JavaScript evaluado**  

La Directiva en relación con las `eval()` funciones relacionadas como `setTimeout(String)` , `setInterval(String)` y que se pueden `new Function(String)` relajar agregando `unsafe-eval` a la Directiva:  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

Sin embargo, le recomendamos especialmente que lo haga.  Estas funciones son vectores de ataque XSS.  

## Ajustar la directiva predeterminada  

Por supuesto, puede ajustar esta directiva a cualquier medida que su extensión permita para aumentar la seguridad a costa de comodidad.  Para especificar que la extensión solo puede cargar recursos de cualquier tipo \ (imágenes, etc.) del paquete de extensión asociado, por ejemplo, una directiva de `default-src 'self'` puede ser adecuada.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## Scripts de contenido  

La Directiva que se está discutiendo se aplica a las páginas de fondo y a las páginas de evento de la extensión.  La forma en que los scripts de contenido se aplican a los scripts de contenido es más complicado.  

Los scripts de contenido generalmente no están sujetos al CSP de la extensión.  Dado que los scripts de contenido no son HTML, la principal repercusión de esto es que pueden usarse `eval` incluso si el CSP de la extensión no especifica `unsafe-eval` , aunque no se recomienda.  Además, el CSP de la página no se aplica a los scripts de contenido.  Más complicadas son las `<script>` etiquetas que los scripts de contenido crean y se colocan en el Dom de la página en la que se están ejecutando.  Se hace referencia a estos como scripts inyectados en DOM hacia adelante.  

DOM inyectado los scripts que se ejecutan inmediatamente después de la inserción en la página se ejecuta como cabría esperar.  Imagínese un script de contenido con el código siguiente como un ejemplo simple:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Esta secuencia de comandos de contenido provoca una `alert` inmediata `document.write()` .  Ten en cuenta que esto se ejecuta independientemente de la Directiva que una página puede especificar.
Sin embargo, el comportamiento es más complicado tanto dentro de la secuencia de comandos inyectada de DOM como en cualquier secuencia de comandos que no se ejecuta inmediatamente después de la inserción.  Suponga que su extensión se está ejecutando en una página que proporciona un CSP asociado que especifica `script-src 'self'` .  Ahora Imagine que el script de contenido ejecuta el siguiente código:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Si un usuario hace clic en el botón, el `onclick` script no se ejecuta.  Esto se debe a que el script no se ejecutó inmediatamente y el código no se interpreta hasta que el evento click no se considera parte del script de contenido, por lo que el CSP de la página \ (no la extensión \) restringe el comportamiento.  Y como ese CSP no lo especifica `unsafe-inline` , el controlador de eventos inline se bloquea.  
La manera correcta de implementar el comportamiento deseado en este caso puede ser agregar el `onclick` controlador como una función de la secuencia de comandos de contenido de la siguiente manera:  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Otro problema similar se produce si el script de contenido ejecuta lo siguiente:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

En este caso, se ejecutará la secuencia de comandos y aparecerá la alerta.  Sin embargo, tomemos este caso:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

Mientras se ejecuta el script inicial, la llamada a `eval` está bloqueada.  Es decir, mientras se permite el tiempo de ejecución de los scripts iniciales, el comportamiento dentro del script se regula por el CSP de la página.  
Por lo tanto, según el modo en que se escriben las secuencias de comandos inyectadas de DOM en la extensión, los cambios en el CSP de la página pueden afectar al comportamiento de la extensión.  Dado que los scripts de contenido no se ven afectados por el CSP de la página, esta es una excelente razón para poner el mayor comportamiento posible de la extensión en el script de contenido en lugar de las secuencias de comandos inyectadas en DOM.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Introducción a la Directiva de seguridad de contenido: Rock HTML5"  
[PublicSuffixList]: https://publicsuffix.org/list "VER LA LISTA DE SUFIJOS PÚBLICOS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Uso de hash para \ <scripts \ > elementos-nivel 2 de directiva de seguridad de contenido"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Nivel 3 de directiva de seguridad de contenido"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Ataque de hombre en el medio: Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/extensions/contentSecurityPolicy).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
