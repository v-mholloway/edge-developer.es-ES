---
description: Obtenga información sobre todas las formas en que puede pausar el código en Microsoft Edge DevTools.
title: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 9734841a9994625bfbaa97a84781581415ed883ed92f8ca914b81cea277d8fac
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11800542"
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
# <a name="how-to-pause-your-code-with-breakpoints-in-microsoft-edge-devtools"></a>Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools  

Use puntos de interrupción para pausar el código JavaScript.  En este artículo se explica cada tipo de punto de interrupción disponible en DevTools, así como cuándo usar y cómo establecer cada tipo.

Para obtener un tutorial introductorio con una página web existente, vaya a Introducción a la [depuración de JavaScript en Microsoft Edge DevTools][DevtoolsJavascriptIndex].

## <a name="overview-of-when-to-use-each-breakpoint-type"></a>Información general sobre cuándo usar cada tipo de punto de interrupción  

El tipo de punto de interrupción más conocido es la línea de código.  Pero los puntos de interrupción de línea de código pueden ser ineficientes para establecer, especialmente si no sabe exactamente dónde buscar o si está trabajando con una base de código grande.  Puede ahorrar tiempo al depurar al saber cómo y cuándo usar los otros tipos de puntos de interrupción.  

| Tipo de punto de interrupción | Úsalo cuando quieras pausar... |  
|:--- |:--- |  
| [Línea de código](#line-of-code-breakpoints) | En una región exacta del código.  |  
| [Línea de código condicional](#conditional-line-of-code-breakpoints) | En una región exacta del código, pero solo cuando alguna otra condición es true.  |  
| [DOM](#dom-change-breakpoints) | En el código que cambia o quita un nodo DOM específico o los elementos secundarios.  |  
| [XHR](#xhrfetch-breakpoints) | Cuando una dirección URL XHR contiene un patrón de cadena.  |  
| [Escucha de eventos](#event-listener-breakpoints) | En el código que se ejecuta después de que se ejecute un evento, como `click` , .  |  
| [Excepción](#exception-breakpoints) | En la línea de código que está generando una excepción capturada o no capturada.  |  
| [Función](#function-breakpoints) | Siempre que se ejecute un comando, una función o un método específicos.  |  

## <a name="line-of-code-breakpoints"></a>Puntos de interrupción de línea de código  

Use un punto de interrupción de línea de código cuando sepa la región exacta del código que necesita investigar.  DevTools siempre se pausa antes de que se ejecute esta línea de código.  

Para establecer un punto de interrupción de línea de código en DevTools:  

1.  Elija la **herramienta Orígenes.**  
1.  Abra el archivo que contiene la línea de código en la que desea interrumpir.  
1.  Vaya a la línea de código.  
1.  A la izquierda de la línea de código se encuentra la columna de número de línea.  Elija.  Aparece un icono rojo junto a la columna de número de línea.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoint-30.msft.png" alt-text="Punto de interrupción de línea de código" lightbox="../media/javascript-sources-page-js-breakpoint-30.msft.png":::
       Punto de interrupción de línea de código  
    :::image-end:::  
    
### <a name="line-of-code-breakpoints-in-your-code"></a>Puntos de interrupción de línea de código en el código  

Ejecute el `debugger` método desde el código para pausar en esa línea.  Esto equivale a un [punto de](#line-of-code-breakpoints)interrupción de línea de código , excepto que el punto de interrupción se establece en el código, no en la interfaz de usuario de DevTools.  

```javascript
console.log('a');
console.log('b');
debugger;
console.log('c');
```  

### <a name="conditional-line-of-code-breakpoints"></a>Puntos de interrupción de línea de código condicionales  

Use un punto de interrupción de línea de código condicional cuando sepa la región exacta del código que necesita investigar, pero desea pausar solo cuando se cumple alguna otra condición.  

Para establecer un punto de interrupción de línea de código condicional:  

1.  Elija la **herramienta Orígenes.**  
1.  Abra el archivo que contiene la línea de código en la que desea interrumpir.  
1.  Vaya a la línea de código.  
1.  A la izquierda de la línea de código se encuentra la columna de número de línea.  Mantenga el mouse en el número de línea y abra el menú contextual \(haga clic con el botón secundario\).  
1.  Elija **Agregar punto de interrupción condicional**.  Se muestra un cuadro de diálogo debajo de la línea de código.  
1.  Escriba la condición en el cuadro de diálogo.  
1.  Seleccione `Enter` para activar el punto de interrupción.  Icono junto a la columna de número de línea.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-conditional-breakpoint.msft.png" alt-text="Punto de interrupción de línea de código condicional" lightbox="../media/javascript-sources-page-js-conditional-breakpoint.msft.png":::
       Punto de interrupción de línea de código condicional  
    :::image-end:::  
    
### <a name="manage-line-of-code-breakpoints"></a>Administrar puntos de interrupción de línea de código  

Use el **panel Puntos de interrupción** para deshabilitar o quitar puntos de interrupción de línea de código de una única ubicación.  

:::image type="complex" source="../media/javascript-sources-page-js-breakpoints-16-33.msft.png" alt-text="Panel Puntos de interrupción" lightbox="../media/javascript-sources-page-js-breakpoints-16-33.msft.png":::
   Panel **Puntos de interrupción**  
:::image-end:::  

*   Active la casilla junto a una entrada para deshabilitar ese punto de interrupción.  
*   Mantenga el mouse sobre una entrada y abra el menú contextual \(clic con el botón secundario\) para quitar ese punto de interrupción.  
*   Mantenga el mouse en cualquier lugar del panel **Puntos** de interrupción y abra el menú contextual \(clic con el botón secundario\) para desactivar todos los puntos de interrupción, deshabilitar todos los puntos de interrupción o quitar todos los puntos de interrupción.  Deshabilitar todos los puntos de interrupción equivale a desactivar cada uno.  La desactivación de todos los puntos de interrupción indica a DevTools que ignore todos los puntos de interrupción de línea de código, pero que también mantenga el estado habilitado para que cada uno esté en el mismo estado que antes al reactivar cada uno.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png" alt-text="Puntos de interrupción desactivados en el panel Puntos de interrupción" lightbox="../media/javascript-sources-page-js-breakpoints-deactivate-breakpoints.msft.png":::
       Puntos de interrupción desactivados en el **panel Puntos de** interrupción  
    :::image-end:::  
    
## <a name="dom-change-breakpoints"></a>Puntos de interrupción de cambios dom  

Use un punto de interrupción de cambio dom cuando desee pausar el código que cambia un nodo DOM o los elementos secundarios.  

Para establecer un punto de interrupción de cambio dom:  

1.  Elija la **herramienta** Elementos.  
1.  Vaya al elemento en el que desea establecer el punto de interrupción.  
1.  Mantenga el mouse en el elemento y abra el menú contextual \(clic con el botón secundario\).  
1.  Mantenga el **mouse en Interrumpir ,** luego elija Modificaciones de **subárbol,** **Modificaciones de atributo**o **Eliminación de nodos.**  
    
    :::image type="complex" source="../media/javascript-elements-break-on-subtree-modifications.msft.png" alt-text="Menú contextual para crear un punto de interrupción de cambio dom" lightbox="../media/javascript-elements-break-on-subtree-modifications.msft.png":::
       Menú contextual para crear un punto de interrupción de cambio dom  
    :::image-end:::  
    
### <a name="types-of-dom-change-breakpoints"></a>Tipos de puntos de interrupción de cambios dom  

*   **Modificaciones de subárbol**.  Se desencadena cuando se quita o se agrega un elemento secundario del nodo seleccionado actualmente, o cuando se cambia el contenido de un elemento secundario.  No se desencadena en los cambios de atributo de nodo secundario ni en los cambios realizados en el nodo seleccionado actualmente.  
*   **Modificaciones de atributos:** se desencadenan cuando se agrega o quita un atributo en el nodo seleccionado actualmente, o cuando cambia un valor de atributo.  
*   **Eliminación de nodos:** se desencadena cuando se quita el nodo seleccionado actualmente.  
    
## <a name="xhrfetch-breakpoints"></a>Puntos de interrupción XHR/Fetch  

Use un punto de interrupción XHR cuando desee interrumpir cuando la dirección URL de solicitud de un XHR contenga una cadena especificada.  DevTools se detiene en la línea de código donde XHR ejecuta el `send()` método.  

> [!NOTE]
> Esta característica también funciona con [solicitudes de API de Fetch.][MDNFetchApi]  

Un ejemplo de cuándo esto es útil es cuando la página web solicita una dirección URL incorrecta y desea encontrar rápidamente el código fuente AJAX o Fetch que está provocando la solicitud incorrecta.  

Para establecer un punto de interrupción XHR:  

1.  Elija la **herramienta Orígenes.**  
1.  Expanda el **panel Puntos de interrupción XHR.**  
1.  Elija **Agregar punto de interrupción**.  
1.  Escriba la cadena en la que desea romper.  DevTools se detiene cuando esta cadena está presente en cualquier lugar de una dirección URL de solicitud XHR.  
1.  Seleccione `Enter` para confirmar.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png" alt-text="Crear un punto de interrupción XHR" lightbox="../media/javascript-sources-page-js-xhr-fetch-breakpoints-org.msft.png":::
       Crear un punto de interrupción XHR  
    :::image-end:::  
    
## <a name="event-listener-breakpoints"></a>Puntos de interrupción de escucha de eventos  

Use puntos de interrupción de escucha de eventos cuando desee pausar el código de escucha de eventos que se ejecuta después de que se desencadena un evento.  Puede seleccionar eventos específicos, como , o `click` categorías de eventos, como todos los eventos del mouse.  

1.  Elija la **herramienta Orígenes.**  
1.  Expanda el **panel Puntos de interrupción de escucha de eventos.**  DevTools muestra una lista de categorías de eventos, como **Animation**.  
1.  Comprueba una de estas categorías para pausar cada vez que se desencadena cualquier evento de esa categoría, o expande la categoría y comprueba un evento específico.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png" alt-text="Crear un punto de interrupción de escucha de eventos" lightbox="../media/javascript-sources-page-js-event-listener-breakpoints-device-deviceorientation.msft.png":::
       Crear un punto de interrupción de escucha de eventos  
    :::image-end:::  
    
## <a name="exception-breakpoints"></a>Puntos de interrupción de excepción  

Use puntos de interrupción de excepción cuando desee pausar en la línea de código que inicia una excepción capturada o no capturada.  

1.  Elija la **herramienta Orígenes.**  
1.  Elija **Pausar en excepciones** \( ![ Pausar en excepciones ](../media/pause-on-exceptions-icon.msft.png) \).  El icono se vuelve azul cuando está habilitado.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-pause-on-exceptions.msft.png" alt-text="Botón Pausar en excepciones" lightbox="../media/javascript-sources-page-js-pause-on-exceptions.msft.png":::
       Botón **Pausar en excepciones**  
    :::image-end:::  
    
1.  **Opcional**.  Active la **casilla Pausar en** excepciones capturadas si también desea pausar las excepciones capturadas, además de las no capturadas.  
    
    :::image type="complex" source="../media/javascript-sources-page-js-paused-on-exception.msft.png" alt-text="Pausada en una excepción no detectada" lightbox="../media/javascript-sources-page-js-paused-on-exception.msft.png":::
       Pausada en una excepción no detectada  
    :::image-end:::  
    
## <a name="function-breakpoints"></a>Puntos de interrupción de funciones  

Ejecute el método, donde está el comando, la función o el método que desea depurar, cuando desee pausar cada vez que se ejecute `debug(method)` `method` una función específica.  Puede insertar en `debug()` el código (como una `console.log()` instrucción) o ejecutar el método desde la consola de DevTools.  `debug()` equivale a establecer un [punto de interrupción de](#line-of-code-breakpoints) línea de código en la primera línea de la función.  

```javascript
function sum(a, b) {
    let result = a + b; // DevTools pauses on this line.
    return result;
}
debug(sum); // Pass the function object, not a string.
sum();
```  

### <a name="make-sure-the-target-function-is-in-scope"></a>Asegúrese de que la función de destino está en el ámbito  

DevTools inicia un `ReferenceError` si la función que desea depurar no está en el ámbito.  

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

Asegurarse de que la función de destino está en el ámbito es complicado si está ejecutando el `debug()` método desde la consola de DevTools.  Esta es una estrategia:  

1.  Establezca un [punto de interrupción de línea de código en](#line-of-code-breakpoints) algún lugar donde la función esté en el ámbito.
1.  Desencadene el punto de interrupción.  
1.  Ejecute el `debug()` método en la Consola de DevTools mientras el código aún está en pausa en el punto de interrupción de línea de código.  
    
## <a name="related-articles"></a>Artículos relacionados

*   [Usar las características del depurador:][DevtoolsJavascriptReference] usar la interfaz de usuario del depurador en la **herramienta** Orígenes.
*   [Introducción a la depuración de JavaScript en Microsoft Edge DevTools:][DevtoolsJavascriptIndex] un tutorial introductorio con una página web existente.
*   [Introducción a la][DevtoolsSourcesIndex] herramienta Sources: el depurador forma parte de **la herramienta Orígenes,** que incluye un editor de JavaScript.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsJavascriptReference]: ./reference.md "Usar las características del depurador | Microsoft Docs"  

[DevtoolsJavascriptIndex]: index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsSourcesIndex]: ../sources/index.md "Información general sobre la herramienta Orígenes | Microsoft Docs"  

[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Recuperación de api | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/breakpoints) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
