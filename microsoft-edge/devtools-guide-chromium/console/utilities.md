---
description: Una referencia de comandos de comodidad disponibles en la consola de Microsoft Edge DevTools.
title: Referencia de la API de utilidades de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e7253bf5402a03d1659f56ba083bb87e93b3af38
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398829"
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

# <a name="console-utilities-api-reference"></a>Referencia de la API de utilidades de consola  

La API de utilidades de consola contiene una colección de comandos de comodidad para realizar tareas comunes: seleccionar e inspeccionar elementos DOM, mostrar datos en formato legible, detener e iniciar el perfilador y supervisar eventos DOM.  

> [!WARNING]
> Los siguientes comandos solo funcionan en la consola de Microsoft Edge DevTools.  Los comandos no funcionan si se ejecutan desde los scripts.  

Para los `console.log()` métodos and `console.error()` del resto de los `console.*` métodos, vaya a [Console API Reference][DevToolsConsoleApi].  

## <a name="recently-evaluated-expression"></a>Expresión recientemente evaluada  

```console
$_
```  

Devuelve el valor de la expresión evaluada más recientemente.  

En la siguiente figura, se evalúa una expresión sencilla \( `2 + 2` \).  A `$_` continuación, se evalúa la propiedad, que contiene el mismo valor.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ es la expresión evaluada más recientemente" lightbox="../media/console-arithmatic.msft.png":::
   Figura 1:  `$_` es la expresión evaluada más recientemente  
:::image-end:::  

En la siguiente figura, la expresión evaluada contiene inicialmente una matriz de nombres.  Al evaluar para encontrar la longitud de la matriz, el valor almacenado en los cambios para convertirse en `$_.length` `$_` la última expresión evaluada, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ cambia cuando se evalúan nuevos comandos" lightbox="../media/console-array-length.msft.png":::
   Figura 2:  `$_` cambios cuando se evalúan nuevos comandos  
:::image-end:::  

## <a name="recently-chosen-element-or-javascript-object"></a>Elemento elegido recientemente o objeto JavaScript  

```console
$0
```  

Devuelve el elemento seleccionado más recientemente o el objeto JavaScript.  `$1` devuelve el segundo seleccionado más recientemente, y así sucesivamente.  Los comandos , , y funcionan como una referencia histórica a los últimos cinco elementos DOM inspeccionados dentro de la herramienta Elementos o los últimos cinco objetos de `$0` `$1` montón de `$2` `$3` `$4` JavaScript seleccionados **** **** en la herramienta Memoria.  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

En la siguiente figura, se `img` selecciona un elemento en la **herramienta** Elementos.  En el **cajón** de consola, `$0` se ha evaluado y muestra el mismo elemento.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Los $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Figura 3: La `$0`  
:::image-end:::  

En la siguiente figura, la imagen muestra un elemento diferente seleccionado en la misma página.  Ahora `$0` hace referencia al elemento recién seleccionado, mientras que devuelve el seleccionado `$1` anteriormente.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="El $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Figura 4: La `$1`  
:::image-end:::  

## <a name="query-selector"></a>Selector de consultas  

```console
$(selector, [startNode])
```  

Devuelve la referencia al primer elemento DOM con el selector CSS especificado.  Este método es un alias para el [método document.querySelector().][MDNDocumentQuerySelector]  

En la figura siguiente, se devuelve una referencia al primer `<img>` elemento del documento.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="El $('img')" lightbox="../media/console-element-selector-image.msft.png":::
   Figura 5: La `$('img')`  
:::image-end:::  

Mantenga el mouse sobre el resultado devuelto, abra el menú contextual \(hacer clic con **** el botón secundario\) y elija Mostrar en el **Panel** de elementos para encontrarlo en el DOM o Desplazarse hasta Ver para mostrarlo en la página.  

En la siguiente figura, se devuelve una referencia al elemento seleccionado actualmente y se muestra la propiedad src.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="El $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   Figura 6: La `$('img').src`  
:::image-end:::  

Este método también admite un segundo parámetro, startNode, que especifica un "elemento" o Node desde el que buscar elementos.  El valor predeterminado del parámetro es `document` .  

En la siguiente figura, se encuentra el primer elemento después de que se devuelve el elemento `img` `title--image` y muestra el `src` correcto.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="El $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Figura 7: La `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Si usa una biblioteca como jQuery que usa , la funcionalidad se sobrescribe y corresponde a la implementación `$` `$` de esa biblioteca.  

## <a name="query-selector-all"></a>Selector de consultas todo  

```console
$$(selector, [startNode])
```  

Devuelve una matriz de elementos que coinciden con el selector CSS especificado.  Este método equivale a ejecutar el [método document.querySelectorAll().][MDNDocumentQuerySelectorAll]  

En el siguiente ejemplo de código y figura, se usa para crear una matriz de todos los elementos del documento actual y mostrar el valor de la propiedad `$$()` `<img>` para cada `src` elemento.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Uso de $$() para seleccionar todas las imágenes del documento y mostrar los orígenes" lightbox="../media/console-element-selector-image-all.msft.png":::
   Figura 8: Usar `$$()` para seleccionar todas las imágenes del documento y mostrar los orígenes  
:::image-end:::  

Este método también admite un segundo parámetro, startNode, que especifica un elemento o Node desde el que buscar elementos.  El valor predeterminado del parámetro es `document` .  

En la siguiente ilustración y ejemplo de código, se usa una versión modificada del ejemplo de código y la figura anteriores para crear una matriz de todos los elementos que aparecen en el documento actual después del `$$()` `<img>` nodo seleccionado.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Uso de $$() para seleccionar todas las imágenes que aparecen después del elemento div <div> especificado en el documento y mostrar los orígenes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Figura 9: Usar para seleccionar todas las imágenes que aparecen después del elemento especificado en el documento y `$$()` `<div>` mostrar los orígenes  
:::image-end:::  

> [!NOTE]
> Seleccione `Shift` + `Enter` en la consola para iniciar una nueva línea sin ejecutar el script.  

## <a name="xpath"></a>XPath  

```console
$x(path, [startNode])
```  

Devuelve una matriz de elementos DOM que coinciden con la expresión XPath especificada.  

En el siguiente ejemplo de código y figura, se devuelven todos los `<p>` elementos de la página.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Uso de un selector XPath" lightbox="../media/console-array-xpath.msft.png":::
   Figura 10: Uso de un selector XPath  
:::image-end:::  

En el siguiente ejemplo de código y figura, se devuelven todos los `<p>` elementos que contienen `<a>` elementos.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Uso de un selector XPath más complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Figura 11: Uso de un selector XPath más complicado  
:::image-end:::  

Al igual que los demás comandos de selector, tiene un segundo parámetro opcional, , que especifica un elemento o Node desde el que buscar `$x(path)` `startNode` elementos.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Uso de un selector XPath con startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Figura 12: Uso de un selector XPath con `startNode`  
:::image-end:::  

## <a name="clear"></a>clear  

```console
clear()
```  

Borra la consola del historial.  

```console
clear()
```  

## <a name="copy"></a>copy  

```console
copy(object)
```  

El `copy(object)` método copia una representación de cadena del objeto especificado en el Portapapeles.  

```console
copy($0)
```  

## <a name="debug"></a>depurar  

```console
debug(method)
```  

>[!NOTE]
> El [problema chromium #1050237][MonorailIssue1050237] está rastreando un error con la `debug()` función.  Si encuentra el problema, intente [usar puntos de interrupción en][DevtoolsJavascriptBreakpoints] su lugar.  

Cuando se solicita el método especificado, se invoca al depurador y se interrumpe dentro del método en la herramienta **Orígenes,** lo que le permite pasar por el código y depurarlo.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Irrumpir dentro de un método con debug()" lightbox="../media/console-debug-text.msft.png":::
   Figura 13: Dividir dentro de un método con `debug()`  
:::image-end:::  

Se `undebug(method)` usa para detener la interrupción del método o usar la interfaz de usuario para deshabilitar todos los puntos de interrupción.  

Para obtener más información sobre los puntos de interrupción, vaya [a Pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints].  

## <a name="dir"></a>dir  

```console
dir(object)
```  

Muestra una lista de estilo de objeto de todas las propiedades del objeto especificado.  Este método es un alias para el [método console.dir().][MDNConsoleDir]  

Evalúe `document.head` en la consola para mostrar el HTML entre las `<head>` `</head>` etiquetas y.  En el siguiente ejemplo de código y figura, se muestra una descripción de estilo de objeto después de usar `console.dir()` en la consola.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Registro de document.head con el método dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Figura 14: Registro `document.head` con `dir()` método  
:::image-end:::  

Para obtener más información, vaya a [`console.dir()`][DevToolsConsoleApiConsoleDirObject] la entrada en la API de consola.  

## <a name="dirxml"></a>dirxml  

```console
dirxml(object)
```  

Imprime una representación XML del objeto especificado, tal como se muestra en la **herramienta** Elementos.  Este método es equivalente al [método console.dirxml().][MDNConsoleDirxml]  

## <a name="inspect"></a>inspeccionar  

```console
inspect(object/method)
```  

Abre y selecciona el elemento u objeto especificado en el panel correspondiente: **** la herramienta **Elementos** para elementos DOM o la herramienta Memoria para objetos de montón de JavaScript.  

En el siguiente ejemplo de código y figura, se `document.body` abre en la **herramienta** Elementos.  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspeccionar un elemento con inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   Figura 15: Inspeccionar un elemento con `inspect()`  
:::image-end:::  

Al pasar un método para inspeccionar, el método abre el documento en la **herramienta Orígenes** para que lo examine.  

## <a name="geteventlisteners"></a>getEventListeners  

```console
getEventListeners(object)
```  

Devuelve los agentes de escucha de eventos registrados en el objeto especificado.  El valor devuelto es un objeto que contiene una matriz para cada tipo de evento registrado \(como `click` o `keydown` \).  Los miembros de cada matriz son objetos que describen el agente de escucha registrado para cada tipo.  En la siguiente figura de ejemplo de código, se enumeran todos los agentes de escucha de eventos registrados en el objeto de documento.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Resultado del uso de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Figura 16: El resultado del uso `getEventListeners(document)`  
:::image-end:::  

Si se registra más de un agente de escucha en el objeto especificado, la matriz contiene un miembro para cada escucha.  En la siguiente figura, hay dos agentes de escucha de eventos registrados en el elemento de documento para el `click` evento.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Varios agentes de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Figura 17: Varios agentes de escucha  
:::image-end:::  

Puede expandir cada uno de los siguientes objetos para explorar las propiedades.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vista expandida del objeto de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Figura 18: Vista expandida del objeto de escucha  
:::image-end:::  

## <a name="keys"></a>teclas  

```console
keys(object)
```  

Devuelve una matriz que contiene los nombres de las propiedades que pertenecen al objeto especificado.  Para obtener los valores asociados de las mismas propiedades, use `values()` .  

Por ejemplo, supongamos que la aplicación definió el siguiente objeto.  

```console
var player1 =   
```  

En los siguientes ejemplos de código y figura, se supone que el resultado se definió en el espacio de nombres global \(por simplicidad\) antes de escribir y `player1` `keys(player1)` en la `values(player1)` consola.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Los comandos keys() y values()" lightbox="../media/console-keys-values.msft.png":::
   Figura 19: Los `keys()` comandos y `values()`  
:::image-end:::  

## <a name="monitor"></a>monitor  

```console
monitor(method)
```  

Registra un mensaje en la consola que indica el nombre del método junto con los argumentos que se pasan al método cuando se llamó.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="El método monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   Figura 20: El `monitor()` método  
:::image-end:::  

Se `unmonitor(method)` usa para dejar de supervisar.  

## <a name="monitorevents"></a>monitorEvents  

```console
monitorEvents(object[, events])
```  

Cuando se produce uno de los eventos especificados en el objeto especificado, el objeto de evento se registra en la consola.  Puede especificar un único evento para supervisar, una matriz de eventos o uno de los tipos de eventos genéricos que se asignan a una colección predefinida de eventos.  Revise el siguiente ejemplo de código y figura.  

A continuación se supervisan todos los eventos de cambio de tamaño del objeto de ventana.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Eventos de cambio de tamaño de ventana de supervisión" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Figura 21: Eventos de cambio de tamaño de ventana de supervisión  
:::image-end:::  

A continuación se define una matriz para supervisar tanto `resize` los eventos como los del objeto `scroll` window.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

También puede especificar uno de los tipos de eventos disponibles, cadenas que se asignan a conjuntos predefinidos de eventos.  En la tabla siguiente se muestran los tipos de eventos disponibles y las asignaciones de eventos asociadas.  

| Tipo de evento | Eventos asignados correspondientes |  
|:--- |:--- |  
| `mouse` | "click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel" |  
| `key` | "keydown", "keypress", "keyup", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom" |  

En el siguiente ejemplo de código, el tipo de evento correspondiente a los eventos de un campo de texto de entrada se selecciona actualmente `key` `key` en la **herramienta** Elementos.  

```console
monitorEvents($0, "key");
```  

En la siguiente figura se muestra el resultado de ejemplo después de escribir un carácter en el campo de texto.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Supervisión de eventos clave" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Figura 22: Eventos clave de supervisión  
:::image-end:::  

## <a name="profile"></a>profile  

```console
profile([name])
```  

Inicia una sesión de generación de perfiles de CPU de JavaScript con un nombre opcional.  El [método profileEnd()](#profileend) completa el perfil y muestra los resultados en la **herramienta Memoria.**  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Ejecute el `profile()` método para iniciar la generación de perfiles.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Ejecute el [método profileEnd()](#profileend) para detener la generación de perfiles y mostrar los resultados en la **herramienta Memoria.**  

Los perfiles también pueden estar anidados.  En los siguientes ejemplos de código y figura, el resultado es el mismo independientemente del orden.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Es posible que varios perfiles de CPU funcionen al mismo tiempo y no es necesario cerrar cada uno en orden de creación.  

## <a name="profileend"></a>profileEnd  

```console
profileEnd([name])
```  

Completa una sesión de generación de perfiles de CPU de JavaScript y muestra los resultados en la **herramienta Memoria.**  Debe ejecutar el método [profile().](#profile)  <!--Navigate to [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Ejecute el [método profile()](#profile) para iniciar la generación de perfiles.  
1.  Ejecute el `profileEnd()` método para detener la generación de perfiles y mostrar los resultados en la herramienta **Memoria.**  
    
    ```console
    profileEnd("My profile")
    ```  

Los perfiles también pueden estar anidados.  En el siguiente ejemplo de código y figura, el resultado es el mismo independientemente del orden.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

El resultado aparece como una instantánea de montón en la **herramienta Memoria.**  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfiles agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Figura 23: Perfiles agrupados  
:::image-end:::  

> [!NOTE]
> Es posible que varios perfiles de CPU funcionen al mismo tiempo y no es necesario cerrar cada uno en orden de creación.  

## <a name="queryobjects"></a>queryObjects  

```console
queryObjects(Constructor)
```  

Devuelve una matriz de objetos creados con el constructor especificado.  El ámbito de `queryObjects()` es el contexto de tiempo de ejecución seleccionado actualmente en la consola.

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Devuelve todo `Promises` .  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      Devuelve todos los elementos HTML.  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      Devuelve todos los objetos que se crearon instancias mediante `new functionName()` .  
   :::column-end:::
:::row-end:::  

---  

## <a name="table"></a>tabla  

```console
table(data[, columns])
```  

Registra los datos del objeto con formato de tabla en función del objeto de datos con encabezados de columna opcionales.  En el siguiente ejemplo de código y figura, se muestra una lista de nombres que usan una tabla en la consola.  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="El resultado del método table()" lightbox="../media/console-table-display.msft.png":::
   Figura 24: El resultado del `table()` método  
:::image-end:::  

## <a name="undebug"></a>undebug  

```console
undebug(method)
```  

Detiene la depuración del método especificado de modo que, cuando se llama al método, ya no se invoca al depurador.  

```console
undebug(getData);
```  

## <a name="unmonitor"></a>unmonitor  

```console
unmonitor(method)
```  

Detiene la supervisión del método especificado.  Este método se usa en función del [método monitor().](#monitor)  

```console
unmonitor(getData);
```  

## <a name="unmonitorevents"></a>unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Detiene la supervisión de eventos para el objeto y los eventos especificados.  Por ejemplo, lo siguiente detiene toda la supervisión de eventos en el objeto de ventana.  

```console
unmonitorEvents(window);
```  

También puede detener selectivamente la supervisión de eventos específicos en un objeto.  Por ejemplo, el siguiente código inicia la supervisión de todos los eventos del elemento seleccionado actualmente y, a continuación, detiene la supervisión de eventos \(quizás para reducir el ruido en la salida de la `mouse` `mousemove` consola\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <a name="values"></a>valores  

```console
values(object)
```  

Devuelve una matriz que contiene los valores de todas las propiedades que pertenecen al objeto especificado.  

```console
values(object);
```  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de api de consola"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir: referencia de api de consola"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar el tiempo de ejecución de JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problema 1050237: debug(function) no funciona | Monorraíl"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/utilities) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
