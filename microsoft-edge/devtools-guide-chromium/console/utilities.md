---
title: Referencia de API de utilidades de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601799"
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





# Referencia de API de utilidades de consola   



La API de utilidades de consola contiene una colección de comandos útiles para realizar tareas comunes: seleccionar e inspeccionar elementos de DOM, Mostrar datos en formato legible, detener e iniciar el generador de perfiles y supervisar eventos de DOM.  

> [!WARNING]
> Los siguientes comandos solo funcionan en la consola de Microsoft Edge DevTools.  Los comandos no funcionan si se ejecutan desde las secuencias de comandos.  

¿Busca `console.log()` , `console.error()` y el resto de los `console.*` métodos?  Consulte [referencia][DevToolsConsoleApi]de la API de consola.  

## Expresión evaluada recientemente  

```console
$_
```  

Devuelve el valor de la expresión evaluada más reciente.  

En la [Ilustración 1](#figure-1), se evalúa una expresión simple \ ( `2 + 2` \).  `$_`A continuación, se evalúa la propiedad, que contiene el mismo valor.  

> ##### Figura 1  
> `$_` es la expresión evaluada más reciente  
> ![$ _ es la expresión evaluada más recientemente][ImageRecentExpression]  

En la [ilustración 2](#figure-2), la expresión evaluada inicialmente contiene una matriz de nombres.  Si se evalúa `$_.length` para encontrar la longitud de la matriz, el valor almacenado en `$_` los cambios se convertirá en la última expresión evaluada, `4` .  

> ##### Figura 2  
> `$_` cambios cuando se evalúan nuevos comandos  
> ![$ _ cambios cuando se evalúan nuevos comandos][ImageChangedRecentExpression]  

## Elemento o objeto JavaScript recientemente seleccionados  

```console
$0
```  

Devuelve el último elemento o objeto JavaScript seleccionado.  `$1` Devuelve la segunda versión seleccionada recientemente, y así sucesivamente.  Los `$0` comandos,,, `$1` `$2` `$3` y `$4` funcionan como referencia histórica a los últimos cinco elementos DOM inspeccionados en el panel **elementos** o los últimos cinco objetos del montón de JavaScript seleccionados en el panel **memoria** .  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

En la [figura 3](#figure-3), `img` se selecciona un elemento en el panel **elementos** .  En el cajón de **consola** , se ha `$0` evaluado y muestra el mismo elemento.  

> ##### Imagen 3  
> El `$0`  
> ![El $0][ImageElement0]  

En la [figura 4](#figure-4), la imagen muestra un elemento diferente seleccionado en la misma página.  `$0`Ahora hace referencia al elemento que acaba de seleccionarse, mientras `$1` devuelve la selección.  

> ##### Imagen 4  
> El `$1`  
> ![El $1][ImageElement1]  

## Selector de consultas  

```console
$(selector, [startNode])
```  

Devuelve la referencia al primer elemento DOM con el selector CSS especificado.  Este método es un alias para el método [Document. querySelector ()][MDNDocumentQuerySelector] .  

En la [figura 5](#figure-5), se devuelve una referencia al primer `<img>` elemento en el documento.  

> ##### Imagen 5  
> El `$('img')`  
> ![$ (' IMG ')][ImageElementImg]  

Haga clic con el botón derecho en el resultado devuelto y seleccione **Mostrar en el panel de elementos** para encontrarlo en el Dom, o **Desplácese hasta la vista** para mostrarlo en la página.  

En la [figura 6](#figure-6), se devuelve una referencia al elemento seleccionado actualmente y se muestra la propiedad src.  

> ##### Imagen 6  
> El `$('img').src`  
> ![El $ (' IMG '). src][ImageElementImgSource]  

Este método también admite un segundo parámetro, startNode, que especifica un "elemento" o un nodo desde el que buscar elementos.  El valor predeterminado de este parámetro es `document` .  

En la [figura 7](#figure-7), el primer `img` elemento se encuentra después de `title--image` y muestra que `src` se devuelve correctamente.  

> ##### Imagen 7  
> $ (' IMG ', Document. querySelector (' title--Image ')). src  
> ![$ (' IMG ', Document. querySelector (' title--Image ')). src][ImageElementImgNodeSource]  

> [!NOTE]
> Si está usando una biblioteca, como jQuery, que usa `$` , esta funcionalidad se sobrescribe y se `$` corresponde con la implementación de esa biblioteca.  

## Selector de consulta todo  

```console
$$(selector, [startNode])
```  

Devuelve una matriz de elementos que coincide con el selector CSS especificado.  Este método es equivalente a llamar al método [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .  

En la [ilustración 8](#figure-8), `$$()` se usa para crear una matriz de todos los `<img>` elementos en el documento actual y mostrar el valor de la `src` propiedad para cada elemento.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### Imagen 8  
> Usar `$$()` para seleccionar todas las imágenes del documento y mostrar las fuentes  
> ![Uso de $ $ () para seleccionar todas las imágenes del documento y mostrar las fuentes][ImageArrayElementImgSource]  

Este método también admite un segundo parámetro, startNode, que especifica un nodo o elemento desde el que buscar elementos.  El valor predeterminado de este parámetro es `document` .  

En la [figura 9](#figure-9), una versión modificada de la [figura 8](#figure-8) usa `$$()` para crear una matriz de todos los `<img>` elementos que aparecen en el documento actual después del nodo seleccionado.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### Imagen 9  
> Usar `$$()` para seleccionar todas las imágenes que aparecen después del `<div>` elemento especificado en el documento y mostrar los orígenes  
> ![Usar $ $ () para seleccionar todas las imágenes que aparecen después del elemento <div> especificado en el documento y mostrar los orígenes][ImageArrayElementImgNodeSource]  

> [!NOTE]
> Pulse `Shift` + `Enter` en la consola para iniciar una nueva línea sin ejecutar el script.  

## Instrucción  

```console
$x(path, [startNode])
```  

Devuelve una matriz de elementos DOM que coinciden con la expresión XPath especificada.  

En la [figura 10](#figure-10), `<p>` se devuelven todos los elementos de la página.  

```console
$x("//p")
```  

> ##### Imagen 10  
> Usar un selector XPath  
> ![Usar un selector XPath][ImageArrayXpath]  

En la [ilustración 11](#figure-11), `<p>` `<a>` se devuelven todos los elementos que contienen elementos.  

```console
$x("//p[a]")
```  

> ##### Imagen 11  
> Usar un selector de XPath más complicado  
> ![Usar un selector de XPath más complicado][ImageArrayXpathChild]  

Es similar a los otros comandos del selector, `$x(path)` tiene un segundo parámetro opcional, `startNode` que especifica un elemento o nodo desde el que buscar elementos.  

> ##### Imagen 12  
> Usar un selector XPath con `startNode`  
> ![Usar un selector XPath con startNode][ImageArrayXpathNode]  

## Libere  

```console
clear()
```  

Borra la consola del historial.  

```console
clear()
```  

## copy  

```console
copy(object)
```  

El `copy(object)` método copia una representación de cadena del objeto especificado en el portapapeles.  

```console
copy($0)
```  

## depurar  

```console
debug(method)
```  

>[!NOTE]
> El [#1050237 de problemas de cromo][MonorailIssue1050237] está realizando un seguimiento de un error con la `debug()` función.  Si se produce este problema, pruebe a [usar puntos de interrupción][DevtoolsJavascriptBreakpoints] en su lugar.  

Cuando se solicita el método especificado, se invoca el depurador y se interrumpe dentro del método en el panel de **fuentes** , lo que permite recorrer el código y depurarlo.  

```console
debug("debug");
```  

> ##### Imagen 13  
> Interrumpir un método con `debug()`  
> ![Interrumpir dentro de un método con debug ()][ImageDebugMethod]  

Use `undebug(method)` este modo para detener la ruptura en el método o use la interfaz de usuario para deshabilitar todos los puntos de interrupción.  

Para obtener más información sobre puntos de interrupción, vea [pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Muestra una lista de estilo de objeto de todas las propiedades del objeto especificado.  Este método es un alias para el método [Console. dir ()][MDNConsoleDir] .  

Evalúe `document.head` en la consola para mostrar el código HTML entre `<head>` las `</head>` etiquetas y.  En la [figura 14](#figure-14), se muestra una lista de estilo de objeto después `console.dir()` de usar en la consola.  

```console
document.head;
dir(document.head);
```  

> ##### Imagen 14  
> Registrar `document.head` con el `dir()` método  
> ![Registro de documento. Head con el método DIR ()][ImageLogObject]  

Para obtener más información, consulte la [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entrada en la API de consola.  

## dirxml  

```console
dirxml(object)
```  

Imprime una representación XML del objeto especificado, como se muestra en la pestaña **elementos** .  Este método es equivalente al método [Console. dirxml ()][MDNConsoleDirxml] .  

## controlados  

```console
inspect(object/method)
```  

Abre y selecciona el elemento u objeto especificado en el panel correspondiente: el panel **elementos** de los elementos DOM o el panel **memoria** para los objetos del montón JavaScript.  

En la [figura 15](#figure-15), `document.body` se abre el panel **elementos** .  

```console
inspect(document.body);
```  

> ##### Imagen 15  
> Inspeccionar un elemento con `inspect()`  
> ![Inspeccionar un elemento con inspeccionar ()][ImageInspectElement]  

Al pasar un método para inspeccionar, el método abre el documento en el panel **orígenes** para que usted lo examine.  

## getEventListeners  

```console
getEventListeners(object)
```  

Devuelve los agentes de escucha de eventos registrados en el objeto especificado.  El valor devuelto es un objeto que contiene una matriz para cada tipo de evento registrado \ (como `click` o `keydown` \).  Los miembros de cada matriz son objetos que describen el agente de escucha registrado para cada tipo.  En la [figura 16](#figure-16), se muestran todas las escuchas de eventos registradas en el objeto de documento.  

```console
getEventListeners(document);
```  

> ##### Imagen 16  
> Resultado de usar `getEventListeners(document)`  
> ![Resultado de usar getEventListeners (Document)][ImageGetListeners]  

Si hay más de un agente de escucha registrado en el objeto especificado, la matriz contendrá un miembro para cada agente de escucha.  En la [figura 16](#figure-16), hay dos escuchas de eventos registradas en el elemento de documento para el `click` evento.  

> ##### Imagen 17  
> Varios agentes de escucha  
> ![Varios agentes de escucha][ImageMultipleListeners]  

Puede expandir aún más cada uno de los siguientes objetos para explorar las propiedades.  

> ##### Ilustración 18  
> Vista expandida del objeto Listener  
> ![Vista expandida del objeto Listener][ImageListenersExpanded]  

## teclas  

```console
keys(object)
```  

Devuelve una matriz que contiene los nombres de las propiedades que pertenecen al objeto especificado.  Para obtener los valores asociados de las mismas propiedades, use `values()` .  

Por ejemplo, supongamos que su aplicación ha definido el siguiente objeto.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

En la [figura 19](#figure-19), el resultado `player1` es el que se definió en el espacio de nombres global \ (para simplificar \) antes de escribir `keys(player1)` y `values(player1)` en la consola.  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### Ilustración 19  
> Los `keys()` `values()` comandos y  
> ![Los comandos Keys () y Values ()][ImageConsoleKeysValues]  

## monitor  

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

> ##### Ilustración 20  
> El `monitor()` método  
> ![El método monitor ()][ImageConsoleMonitorSum]  

Usar `unmonitor(method)` para cesar la supervisión.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Cuando se produce uno de los eventos especificados en el objeto especificado, el objeto de evento se registra en la consola.  Puede especificar un solo evento para supervisar, una matriz de eventos o uno de los tipos de eventos genéricos que se asignan a una colección predefinida de eventos.  Consulte la [figura 21](#figure-21).  

El siguiente monitor supervisa todos los eventos de cambiar tamaño en el objeto Window.  

```console
monitorEvents(window, "resize");
```  

> ##### Ilustración 21  
> Supervisión de eventos de la ventana de supervisión  
> ![Supervisión de eventos de la ventana de supervisión][ImageMonitorResize]  

En el procedimiento siguiente se define una matriz para supervisar ambos `resize` `scroll` eventos y eventos en el objeto de ventana.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

También puede especificar uno de los tipos de eventos disponibles, cadenas que se asignan a conjuntos de eventos predefinidos.  En la tabla siguiente se muestran los tipos de eventos disponibles y las asignaciones de eventos asociadas.  

| Tipo de evento | Eventos asignados correspondientes |  
|:--- |:--- |  
| `mouse` | "click", "DblClick", "MouseDown", "MouseMove", "mouseout", "mouseover", "MouseUp", "MouseWheel" |  
| `key` | "KeyDown", "KeyPress", "KeyUp", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "desenfocar", "cambiar", "foco", "restablecer", "cambiar tamaño", "desplazar", "seleccionar", "enviar", "hacer zoom" |  

En la [figura 22](#figure-22), el `key` tipo de evento que corresponde a `key` los eventos en un campo de texto de entrada está actualmente seleccionado en el panel **elementos** .  

```console
monitorEvents($0, "key");
```  

En la [figura 22](#figure-22) , se muestra el resultado de ejemplo después de escribir un carácter en el campo de texto.  

> ##### Ilustración 22  
> Supervisión de eventos clave  
> ![Supervisión de eventos clave][ImageMonitorKey]  

## profile  

```console
profile([name])
```  

Inicia una sesión de generación de perfiles de CPU de JavaScript con un nombre opcional.  El método [profileEnd ()](#profileend) completa el perfil y muestra los resultados en el panel **memoria** .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Ejecute el `profile()` método para iniciar la generación de perfiles.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Ejecuta el método [profileEnd ()](#profileend) para detener la generación de perfiles y mostrar los resultados en el panel **memoria** .  

Los perfiles también pueden estar anidados.  En la [Figura 23](#figure-23) , el resultado es el mismo, independientemente del orden.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Varios perfiles de CPU pueden funcionar al mismo tiempo y no es necesario cerrar cada uno de ellos en el orden de creación.  

## profileEnd  

```console
profileEnd([name])
```  

Completa una sesión de generación de perfiles de CPU de JavaScript y muestra los resultados en el panel **memoria** .  Debes estar ejecutando el método [Profile ()](#profile) .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Ejecuta el método [Profile ()](#profile) para iniciar la generación de perfiles.  
1.  Ejecute el `profileEnd()` método para detener la generación de perfiles y mostrar los resultados en el panel **memoria** .  
    
    ```console
    profileEnd("My profile")
    ```  

Los perfiles también pueden estar anidados.  En la [Figura 23](#figure-23) , el resultado es el mismo, independientemente del orden.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

El resultado aparece como una instantánea de montones en el panel **memoria** .  

> ##### Ilustración 23  
> Perfiles agrupados  
> ![Perfiles agrupados][ImageGroupedProfiles]  

> [!NOTE]
> Varios perfiles de CPU pueden funcionar al mismo tiempo y no es necesario cerrar cada uno de ellos en el orden de creación.  

## Table  

```console
table(data[, columns])
```  

Registra datos de objeto con formato de tabla basado en el objeto de datos en con encabezados de columna opcionales.  En la [figura 24](#figure-24), se muestra una lista de nombres que usan una tabla en la consola.  

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

> ##### Ilustración 24  
> El `table()` método  
> ![El método Table ()][ImageConsoleTable]  

## despurar  

```console
undebug(method)
```  

Detiene la depuración del método especificado para que cuando se llame al método se deje de llamar al depurador.  

```console
undebug(getData);
```  

## dessupervisar  

```console
unmonitor(method)
```  

Detiene la supervisión del método especificado.  Se usa en conjunto con el método [monitor ()](#monitor) .  

```console
unmonitor(getData);
```  

## unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Detiene la supervisión de eventos para el objeto y los eventos especificados.  Por ejemplo, a continuación se detiene toda la supervisión de eventos en el objeto Window.  

```console
unmonitorEvents(window);
```  

También puede dejar de supervisar selectivamente los eventos específicos de un objeto.  Por ejemplo, el siguiente código comienza a supervisar todos los `mouse` eventos del elemento seleccionado actualmente y, a continuación, detiene `mousemove` la supervisión de eventos \ (quizás para reducir el ruido en el resultado de la consola \).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## los  

```console
values(object)
```  

Devuelve una matriz que contiene todos los valores de todas las propiedades que pertenecen al objeto especificado.  

```console
values(object);
```  

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Ilustración 1: $ _ es la expresión evaluada más recientemente"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Ilustración 2: $ _ cambios cuando se evalúan nuevos comandos"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Ilustración 3: $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Ilustración 4: $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Ilustración 5: $ (' IMG ')"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Ilustración 6: el $ (' IMG '). src"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Ilustración 7: $ (' IMG ', Document. querySelector (' title--Image ')). src"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Ilustración 8: uso de $ $ () para seleccionar todas las imágenes del documento y mostrar las fuentes"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "Ilustración 9: uso de $ $ () para seleccionar todas las imágenes que aparecen después de la <especificada div> en el documento y mostrar los orígenes"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Ilustración 10: uso de un selector XPath"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Ilustración 11: usar un selector de XPath más complicado"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Ilustración 12: uso de un selector XPath con startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Ilustración 13: interrumpir un método con debug ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Ilustración 14: registro de Document. Body con el método DIR ()"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Ilustración 15: inspeccionar un elemento con inspeccionar ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Ilustración 16: resultado de usar getEventListeners (Document)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Ilustración 17: varios agentes de escucha"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Ilustración 18: vista ampliada del objeto Listener"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Ilustración 19: los comandos Keys () y Values ()"  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Ilustración 20: el método monitor ()"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Ilustración 21: supervisión de los eventos de la ventana de supervisión"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Ilustración 22: supervisión de eventos clave"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Ilustración 23: perfiles agrupados"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Ilustración 24: el método Table ()"  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de la API de consola"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "DIR-consola de referencia de API"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Acelerar el tiempo de ejecución de JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. dirxml () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Problema 1050237: debug (función) no funciona | Monorail"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/utilities) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
