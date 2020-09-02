---
title: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 8eefea3fad894af6b66a6d7f595c5b663c03a0dc
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991184"
---
<!-- Copyright Kayce Basques 
   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at
       https://www.apache.org/licenses/LICENSE-2.0
   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  







# Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools   



Usa puntos de interrupción para pausar el código de JavaScript.  En esta guía se explica cada tipo de punto de interrupción que está disponible en DevTools, así como Cuándo usar y cómo establecer cada tipo.  Para obtener un tutorial práctico del proceso de depuración, consulte Introducción [a la depuración de JavaScript en Microsoft Edge DevTools][DevtoolsJavascriptIndex].  

## Información general sobre Cuándo usar cada tipo de punto de interrupción   

El tipo de punto de interrupción más conocido es la línea de código.  Pero los puntos de interrupción de línea de código pueden resultar ineficaces para establecerlos, sobre todo si no sabe exactamente dónde mirar o si está trabajando con un código base grande.  Puede ahorrar tiempo al depurar si conoce cómo y Cuándo usar los otros tipos de puntos de interrupción.  

| Tipo de punto de interrupción | Use esto cuando quiera hacer una pausa...  |  
|:--- |:--- |  
| [Línea de código](#line-of-code-breakpoints) | En una región exacta del código.  |  
| [Línea de código condicional](#conditional-line-of-code-breakpoints) | En una región exacta de código, pero solo cuando alguna otra condición sea verdadera.  |  
| [DOM](#dom-change-breakpoints) | En el código que cambia o quita un nodo DOM específico o los elementos secundarios.  |  
| [XHR](#xhrfetch-breakpoints) | Cuando una dirección URL de XHR contiene un patrón de cadena.  |  
| [Detector de eventos](#event-listener-breakpoints) | En el código que se ejecuta después de que se ejecute un evento, como, por ejemplo `click` ,.  |  
| [Excepción](#exception-breakpoints) | En la línea de código que produce una excepción detectada o no detectada.  |  
| [Función](#function-breakpoints) | Siempre que se ejecute un comando, una función o un método específico.  |  

## Puntos de interrupción de línea de código   

Use un punto de interrupción de línea de código cuando Conozca la región exacta de código que necesita investigar.  DevTools siempre se pausa antes de que se ejecute esta línea de código.  

Para establecer un punto de interrupción de línea de código en DevTools:  

1.  Haga clic en la pestaña **orígenes** .  
1.  Abra el archivo que contiene la línea de código en la que desea interrumpir.  
1.  Ir a la línea de código.  
1.  A la izquierda de la línea de código se encuentra la columna de número de línea.  Haz clic en él.  Aparece un icono rojo junto a la columna número de línea.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Un punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Un punto de interrupción de línea de código  
    :::image-end:::  
    
### Puntos de interrupción de línea de código en el código   

Ejecuta el `debugger` método desde tu código para hacer una pausa en esa línea.  Es equivalente a un [punto de interrupción de línea de código](#line-of-code-breakpoints), excepto en que el punto de interrupción se establece en el código, no en la interfaz de usuario de DevTools.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### Puntos de interrupción de línea de código condicional   

Use un punto de interrupción de línea de código condicional cuando Conozca la región exacta de código que necesita investigar, pero solo desea pausarla cuando se cumpla otra condición.  

Para establecer un punto de interrupción de línea de código condicional:  

1.  Haga clic en la pestaña **orígenes** .  
1.  Abra el archivo que contiene la línea de código en la que desea interrumpir.  
1.  Ir a la línea de código.  
1.  A la izquierda de la línea de código se encuentra la columna de número de línea.  Haga clic con el botón secundario en el número de línea.  
1.  Seleccione **Agregar punto de interrupción condicional**.  Aparece un cuadro de diálogo debajo de la línea de código.  
1.  Escriba la condición en el cuadro de diálogo.  
1.  Pulse `Enter` para activar el punto de interrupción.  Un icono junto a la columna de números de línea.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Punto de interrupción de línea de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Punto de interrupción de línea de código condicional  
    :::image-end:::  
    
### Administrar puntos de interrupción de línea de código   

Use el panel **puntos de interrupción** para deshabilitar o quitar puntos de interrupción de línea de código de una sola ubicación.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Panel puntos de interrupción" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   Panel **puntos de interrupción**  
:::image-end:::  

*   Active la casilla situada junto a una entrada para deshabilitar el punto de interrupción.  
*   Haga clic con el botón secundario en una entrada para quitar ese punto de interrupción.  
*   Haga clic con el botón secundario en cualquier parte del panel **puntos de interrupción** para desactivar todos los puntos de interrupción, deshabilitar todos los puntos de interrupción o quitar todos los puntos de interrupción.  Deshabilitar todos los puntos de interrupción es equivalente a desactivarlo.  Desactivar todos los puntos de interrupción indica a DevTools que pase por alto todos los puntos de interrupción de línea de código, pero también debe mantener el estado habilitado para que cada uno esté en el mismo estado que antes cuando reactive cada uno.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Puntos de interrupción desactivados en el panel de puntos de interrupción" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Puntos de interrupción desactivados en el panel de **puntos de interrupción**  
    :::image-end:::  
    
## DOM cambiar puntos de interrupción   

Use un punto de interrupción de cambio de DOM cuando desee pausar el código que cambia un nodo DOM o los elementos secundarios.  

Para establecer un punto de interrupción de cambio de DOM:  

1.  Haga clic en la pestaña **elementos** .  
1.  Desplazarse por el elemento en el que desea establecer el punto de interrupción.  
1.  Haga clic con el botón secundario en el elemento.  
1.  Mantenga el mouse sobre **break on**y, a continuación, seleccione **modificaciones de subárbol**, **modificaciones de atributos**o eliminación de **nodos**.  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Menú contextual para crear un punto de interrupción de cambio de DOM" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       Menú contextual para crear un punto de interrupción de cambio de DOM  
    :::image-end:::  
    
### Tipos de puntos de interrupción de cambio de DOM   

*   **Modificaciones en el subárbol**.  Se desencadena cuando se quita o agrega un elemento secundario del nodo que se encuentra seleccionado, o se cambia el contenido de un elemento secundario.  No se desencadena en cambios en los atributos del nodo secundario o en los cambios realizados en el nodo seleccionado actualmente.  
*   **Modificaciones de atributos**: se desencadena cuando se agrega o se quita un atributo en el nodo seleccionado actualmente o cuando cambia un valor de atributo.  
*   **Eliminación de nodos**: se desencadena cuando se quita el nodo seleccionado actualmente.  
    
## XHR/capturar puntos de interrupción   

Use un punto de interrupción de XHR cuando desee interrumpir cuando la dirección URL de la solicitud de un XHR contiene una cadena especificada.  DevTools se detiene en la línea de código donde el XHR ejecuta el `send()` método.  

> [!NOTE]
> Esta característica también funciona con las solicitudes de [API de captura][MDNFetchApi] .  

Un ejemplo de cuándo resulta útil es cuando ve que la página está solicitando una dirección URL incorrecta y desea buscar rápidamente los códigos de origen de AJAX o fetch que causan la solicitud incorrecta.  

Para establecer un punto de interrupción de XHR:  

1.  Haga clic en la pestaña **orígenes** .  
1.  Expanda el panel de **puntos de interrupción XHR** .  
1.  Haga clic en **Agregar punto de interrupción**.  
1.  Escriba la cadena en la que desea interrumpir.  DevTools se detiene cuando esta cadena está presente en cualquier lugar de una dirección URL de solicitud de XHR.  
1.  Pulse `Enter` para confirmar.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Crear un punto de interrupción de XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Crear un punto de interrupción de XHR  
    :::image-end:::  
    
## Puntos de interrupción de escucha de eventos 

Use puntos de interrupción de escucha de eventos cuando desee pausar el código del agente de escucha de eventos que se ejecuta después de desencadenar un evento.  Puede seleccionar eventos específicos, como `click` o categorías de eventos, como todos los eventos del mouse.  

1.  Haga clic en la pestaña **orígenes** .  
1.  Expanda el panel de **puntos de interrupción de escucha de eventos** .  DevTools muestra una lista de categorías de eventos, como la **animación**.  
1.  Active una de estas categorías para pausar cada vez que se desencadene un evento de la categoría o expanda la categoría y compruebe un evento específico.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Crear un punto de interrupción de detector de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Crear un punto de interrupción de detector de eventos  
    :::image-end:::  
    
## Puntos de interrupción de excepción   

Use puntos de interrupción de excepción cuando desee hacer una pausa en la línea de código que produce una excepción detectada o no detectada.  

1.  Haga clic en la pestaña **orígenes** .  
1.  Haga clic en **pausar en excepciones** \ ( ![ pausar en excepciones ][ImagePauseOnExceptionsIcon] \).  El icono se vuelve azul al habilitarlo.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="El botón pausar en las excepciones" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       El botón **pausar en las excepciones**  
    :::image-end:::  
    
1.  **Opcional**.  Active la casilla **pausar las excepciones capturadas** si también desea pausar las excepciones detectadas, además de las no capturadas.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausado en una excepción no detectada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Pausado en una excepción no detectada  
    :::image-end:::  
    
## Puntos de interrupción de función   

Ejecute el `debug(method)` método, donde `method` es el comando, la función o el método que desea depurar, cuando desee pausarlo siempre que se ejecute una función específica.  Puede insertar `debug()` el código (como una `console.log()` instrucción) o ejecutar el método desde la consola de DevTools.  `debug()` es equivalente a establecer un [punto de interrupción de línea de código](#line-of-code-breakpoints) en la primera línea de la función.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### Asegurarse de que la función de destino está en el ámbito   

DevTools inicia una `ReferenceError` si la función que desea depurar no está en el ámbito.  

```javascript
(function () {
    function hey() {
        console.log('hey');
    }
    function yo() {
        console.log('yo');
    }
    debug(yo); // This works.
    yo();
})();
debug(hey); // This does not work.  hey() is out of scope.
```  

Garantizar que la función de destino esté dentro del ámbito es complicada si está ejecutando el `debug()` método desde la consola de DevTools.  Esta es una estrategia:  

1.  Establezca un [punto de interrupción de línea de código](#line-of-code-breakpoints) en el lugar donde se encuentra la función en el ámbito.
1.  Desencadenar el punto de interrupción.  
1.  Ejecuta el `debug()` método en la consola de DevTools mientras el código está en pausa en el punto de interrupción de línea de código.  
    
<!---  
 


-->  

<!-- image links -->  

[ImagePauseOnExceptionsIcon]: ../media/pause-on-exceptions-icon.msft.png  

<!-- links -->  

[DevtoolsJavascriptIndex]: index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Fetch API | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
