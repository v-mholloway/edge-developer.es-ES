---
description: Las herramientas de desarrollo notifican errores de JavaScript y depuran cada uno en la consola
title: Seguimiento de errores con la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ebd12f8932332b3e63162ab6952577bdb43bbccd
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483658"
---
# <a name="debug-errors-reported-in-console"></a>Errores de depuración notificados en la consola  

La primera experiencia que tiene con **la consola es** probablemente un error en un script.  Para probarlo, vaya a [Error de JavaScript notificado en la herramienta consola][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml].  

Si abre DevTools en el explorador, un botón de la parte superior derecha muestra un error para la página web.  
Elija el botón para llevarle a la **consola** y darle más información sobre el error.  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools proporciona información detallada sobre el error en la consola" lightbox="../media/console-debug-displays-error.msft.png":::
   DevTools proporciona información detallada sobre el error en la **consola**  
:::image-end:::  

A partir de la información, puede recopilar que el error está en la línea 16 del `error.html` archivo.  Si elige el vínculo a la derecha de la consola, le llevará a la herramienta Orígenes y resaltará la `error.html:16` línea de código con el error. **** ****  

:::image type="complex" source="../media/console-debug-displays-in-sources.msft.png" alt-text="La herramienta Orígenes resalta la línea de código que provoca el error" lightbox="../media/console-debug-displays-in-sources.msft.png":::
   La **herramienta Orígenes** resalta la línea de código que provoca el error  
:::image-end:::  

El script intenta obtener el primer `h2` elemento del documento y pintar un borde rojo alrededor de él.  Pero no `h2` existe ningún elemento, por lo que se produce un error en el script.  

## <a name="find-and-debug-network-issues"></a>Buscar y depurar problemas de red  

Otros errores que los informes **de consola** son errores de red.  Para mostrarlo en acción, vaya al [error de red notificado en consola][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml].  

:::image type="complex" source="../media/console-debug-network-error.msft.png" alt-text="La consola muestra una red y un error de JavaScript" lightbox="../media/console-debug-network-error.msft.png":::
   **La** consola muestra una red y un error de JavaScript  
:::image-end:::  

La tabla muestra , pero nada cambia en la página `loading` web porque los datos nunca se recuperan.  En la **consola,** se produjeron los dos errores siguientes.  

*   Error de red que comienza con el `GET` método HTTP seguido de un URI.  
*   `Uncaught (in promise) TypeError: data.forEach is not a function`Error.  
    
Si elige el vínculo `network-error.html:40` en la **consola**, DevTools le llevará a la **herramienta** Orígenes.  La línea de código problemática está resaltada y seguida de un `error` botón \( `x` \).  Para mostrar el `Failed to load resource: the server responded with a status of 404 ()` mensaje de error, elija el **botón error** \( `x` \).  


:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-code-line.msft.png" alt-text="Elegir el vínculo a la página web y el código donde se produce el error se abre la herramienta Orígenes" lightbox="../media/console-debug-network-error-code-line.msft.png":::
         Elegir el vínculo a la página web y el código donde se produce el error se abre la **herramienta** Orígenes  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-sources.msft.png" alt-text="Para encontrar el error en JavaScript, use la herramienta Orígenes" lightbox="../media/console-debug-network-error-sources.msft.png":::
         Para encontrar el error en JavaScript, use la **herramienta Orígenes**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

En el ejemplo, el error le informa de que no se encuentra la dirección URL solicitada.  Después, complete las siguientes acciones para abrir la **herramienta Red.**  

1.  Abra la **consola**.  
1.  Elija el URI asociado al error.  
    
:::image type="complex" source="../media/console-debug-network-error-url.msft.png" alt-text="La consola muestra un código de estado HTTP del error después de no cargar un recurso" lightbox="../media/console-debug-network-error-url.msft.png":::
   **La** consola muestra un código de estado HTTP del error después de no cargar un recurso  
:::image-end:::  

:::row:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network.msft.png" alt-text="La herramienta Red muestra más información sobre la solicitud con errores" lightbox="../media/console-debug-network-error-network.msft.png":::
           La **herramienta Red** muestra más información sobre la solicitud con errores  
        :::image-end:::  
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network-detail.msft.png" alt-text="Inspeccionar los encabezados de la herramienta Red puede dar más información" lightbox="../media/console-debug-network-error-network-detail.msft.png":::
           Inspeccionar los encabezados de la **herramienta Red** puede dar más información  
        :::image-end:::  
    :::column-end:::
:::row-end:::  

¿Cuál fue el problema?  Dos caracteres de barra diagonal `//` \( \) se producen en el URI solicitado después de la palabra `repos` .  Abra la **herramienta Orígenes** e inspeccione la línea 26.  Un carácter de barra diagonal final \( `/` \) se produce al final del URI base.  

:::image type="complex" source="../media/console-debug-network-error-code-error.msft.png" alt-text="La herramienta Orígenes muestra la línea de código con el error" lightbox="../media/console-debug-network-error-code-error.msft.png":::
   La **herramienta Orígenes** muestra la línea de código con el error  
:::image-end:::  

Para revisar ningún error en la **consola,** vaya a [Error de red fijo notificado en consola][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].  

:::image type="complex" source="../media/console-debug-network-error-fixed.msft.png" alt-text="El ejemplo sin errores carga información de GitHub y la muestra" lightbox="../media/console-debug-network-error-fixed.msft.png":::
   El ejemplo sin errores carga información de GitHub y la muestra  
:::image-end:::  

Asegúrese de proporcionar técnicas de codificación defensivas para evitar las experiencias anteriores del usuario.  Además, asegúrate de que el código detecta errores y muestra cada uno en la **consola**.  Vaya a [Informes de errores de red en consola e interfaz de][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] usuario y revise los siguientes elementos.  

*   Proporcionar interfaz de usuario al usuario que algo salió mal.  
*   En la **consola,** proporcione información útil sobre el error de red del código.  
    
:::image type="complex" source="../media/console-debug-network-error-report.msft.png" alt-text="Un ejemplo que detecta e informa de errores" lightbox="../media/console-debug-network-error-report.msft.png":::
   Un ejemplo que detecta e informa de errores  
:::image-end:::  

El siguiente fragmento de código detecta e informa de errores mediante el `handleErrors` método, específicamente la `throw Error` línea.  

```javascript
const handleErrors = (response) => {
    if (!response.ok) {
        let message = 'Could not load the information'
        document.querySelector('tbody').innerHTML = `
        <tr><td colspan=3>Error ${message}</td></tr>
        `;
        throw Error(response.status + ' ' + response.statusText);
    }
    return response;
};
```  

## <a name="create-errors-and-traces-in-the-console"></a>Crear errores y seguimientos en la consola

Además del ejemplo de la sección anterior, también puede crear diferentes errores y problemas de `throw Error` seguimiento en la **consola**.  
Para mostrar dos mensajes de error creados en la **consola,** vaya a Crear informes [de error y aserciones en consola][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml].  

:::image type="complex" source="../media/console-debug-error-assert.msft.png" alt-text="Mensajes de error creados desde la consola" lightbox="../media/console-debug-error-assert.msft.png":::
   Mensajes de error creados desde la **consola**  
:::image-end:::  

El siguiente fragmento de código se usó en el ejemplo anterior.  

```javascript
function first(name) { second(name); }
function second(name) { third(name); }
function third(name) {
    if (!name) {
        console.error(`Name isn't defined :(`)
    } else {
        console.assert(
            name.length <= 8, 
            `"${name} is not less than eight letters"`
        );
    }
}
first();
first('Console');
first('Microsoft Edge Canary');
```  

Tiene tres funciones que se solicitan mutuamente sucesivamente.  

*   `first()`  
*   `second()`  
*   `third()`  
    
Cada uno envía un `name` argumento al otro.  En la función, se comprueba si el argumento existe y, si no lo hace, se registra un error que no `third()` `name` se define ese nombre.  Si `name` está definido, se usa el método para comprobar si el argumento tiene menos de ocho letras de `assert()` `name` longitud.  La función se `first()` solicita tres veces, con los siguientes parámetros.  

*   Ningún argumento que desencadena `console.error()` el método en la `third()` función.  
*   El término como parámetro de la función no provoca un error porque el argumento existe y `Console` es inferior a ocho `first()` `name` letras.  
*   La frase como parámetro para funcionar hace que el método informe de un error, ya que `Microsoft Edge Canary` el parámetro tiene más de ocho `first()` `console.assert()` letras.  
    
Use el `console.assert()` método para crear informes de errores condicionales.  Los dos ejemplos siguientes tienen el mismo resultado, pero se necesita una instrucción `if{}` adicional.  

```javascript
let x = 20;
if (x < 40) { console.error(`${x} is too small`) };
console.assert(x >= 40, `${x} is too small`) 
```  

> [!IMPORTANT]
> La segunda y tercera líneas del código realizan la misma prueba.  Dado que la aserción debe registrar un resultado negativo, debe probar en `x < 40` el caso y para la `if` `x >= 40` aserción.  

Si no está seguro de qué función solicita otra función, use el método para realizar un seguimiento de las funciones que se solicitan para llegar a `console.trace()` la función actual.  Para mostrar el seguimiento en la **consola,** vaya [a Crear seguimientos en consola][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml].  

```javascript
function here() {there()}
function there() {everywhere()}
function everywhere() {
    console.trace();
}
here();
there();
```  

El resultado es un seguimiento para mostrar que se denomina y, a continuación, y en el `here()` segundo ejemplo que se denomina `there()` `everywhere()` `everywhere()` .  

:::image type="complex" source="../media/console-debug-trace.msft.png" alt-text="Seguimiento creado desde la consola" lightbox="../media/console-debug-trace.msft.png":::
   Seguimiento creado desde la **consola**  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error.html "Error de JavaScript notificado en la herramienta consola | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error-assert.html "Creación de informes de error y aserciones en consola | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error.html "Error de red notificado en la consola | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-fixed.html "Se ha corregido un error de red notificado en la consola | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-reported.html "Informes de errores de red en consola e interfaz de usuario | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]: https://microsoftedge.github.io/DevToolsSamples/console/trace.html "Creación de seguimientos en la consola | GitHub"  
