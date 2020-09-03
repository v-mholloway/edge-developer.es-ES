---
description: Una referencia de los comandos de comodidad disponibles en la consola de Microsoft Edge DevTools.
title: Referencia de API de utilidades de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2882d980e6da45072cab4b028ceb1838a9078064
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993110"
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

En la siguiente ilustración, se evalúa una expresión simple \ ( `2 + 2` \).  `$_`A continuación, se evalúa la propiedad, que contiene el mismo valor.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ es la expresión evaluada más recientemente" lightbox="../media/console-arithmatic.msft.png":::
   Ilustración 1:  `$_` es la expresión evaluada más reciente  
:::image-end:::  

En la siguiente ilustración, la expresión evaluada inicialmente contiene una matriz de nombres.  Si se evalúa `$_.length` para encontrar la longitud de la matriz, el valor almacenado en `$_` los cambios se convertirá en la última expresión evaluada, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ cambios cuando se evalúan nuevos comandos" lightbox="../media/console-array-length.msft.png":::
   Ilustración 2:  `$_` cambios cuando se evalúan nuevos comandos  
:::image-end:::  

## Elemento o objeto JavaScript recientemente seleccionados  

```console
$0
```  

Devuelve el último elemento o objeto JavaScript seleccionado.  `$1` Devuelve la segunda versión seleccionada recientemente, y así sucesivamente.  Los `$0` comandos,,, `$1` `$2` `$3` y `$4` funcionan como referencia histórica a los últimos cinco elementos DOM inspeccionados en el panel **elementos** o los últimos cinco objetos del montón de JavaScript seleccionados en el panel **memoria** .  

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

En la siguiente ilustración, `img` se selecciona un elemento en el panel **elementos** .  En el cajón de **consola** , se ha `$0` evaluado y muestra el mismo elemento.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="El $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   Ilustración 3: el `$0`  
:::image-end:::  

En la siguiente ilustración, la imagen muestra un elemento diferente seleccionado en la misma página.  `$0`Ahora hace referencia al elemento que acaba de seleccionarse, mientras `$1` devuelve la selección.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="El $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   Ilustración 4: el `$1`  
:::image-end:::  

## Selector de consultas  

```console
$(selector, [startNode])
```  

Devuelve la referencia al primer elemento DOM con el selector CSS especificado.  Este método es un alias para el método [Document. querySelector ()][MDNDocumentQuerySelector] .  

En la siguiente ilustración, se devuelve una referencia al primer `<img>` elemento en el documento.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ (' IMG ')" lightbox="../media/console-element-selector-image.msft.png":::
   Ilustración 5: el `$('img')`  
:::image-end:::  

Mantenga el puntero sobre el resultado devuelto, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **Mostrar en el panel de elementos** para encontrarlo en el Dom o **Desplácese hasta la vista** para mostrarlo en la página.  

En la siguiente ilustración, se devuelve una referencia al elemento que está seleccionado y se muestra la propiedad src.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="El $ (' IMG '). src" lightbox="../media/console-element-selector-image-source.msft.png":::
   Ilustración 6: el `$('img').src`  
:::image-end:::  

Este método también admite un segundo parámetro, startNode, que especifica un "elemento" o un nodo desde el que buscar elementos.  El valor predeterminado del parámetro es `document` .  

En la siguiente ilustración, el primer `img` elemento se encuentra después de `title--image` y muestra que `src` se devuelve correctamente.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$ (' IMG ', Document. querySelector (' title--Image ')). src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   Ilustración 7: el `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Si está usando una biblioteca, como jQuery, que usa `$` , la funcionalidad se sobrescribe y se `$` corresponde con la implementación de esa biblioteca.  

## Selector de consulta todo  

```console
$$(selector, [startNode])
```  

Devuelve una matriz de elementos que coincide con el selector CSS especificado.  Este método es equivalente a llamar al método [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .  

En el siguiente ejemplo de código y Ilustración, use `$$()` para crear una matriz de todos los `<img>` elementos en el documento actual y mostrar el valor de la `src` propiedad para cada elemento.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Uso de $ $ () para seleccionar todas las imágenes del documento y mostrar las fuentes" lightbox="../media/console-element-selector-image-all.msft.png":::
   Ilustración 8: usar `$$()` para seleccionar todas las imágenes del documento y mostrar las fuentes  
:::image-end:::  

Este método también admite un segundo parámetro, startNode, que especifica un nodo o elemento desde el que buscar elementos.  El valor predeterminado del parámetro es `document` .  

En el siguiente ejemplo de código y figura, una versión modificada de la muestra de código anterior y la ilustración usa `$$()` para crear una matriz de todos los `<img>` elementos que aparecen en el documento actual después del nodo seleccionado.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usar $ $ () para seleccionar todas las imágenes que aparecen después del elemento <div> especificado en el documento y mostrar los orígenes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Ilustración 9: usar `$$()` para seleccionar todas las imágenes que aparecen después del `<div>` elemento especificado en el documento y mostrar los orígenes  
:::image-end:::  

> [!NOTE]
> Pulse `Shift` + `Enter` en la consola para iniciar una nueva línea sin ejecutar el script.  

## Instrucción  

```console
$x(path, [startNode])
```  

Devuelve una matriz de elementos DOM que coinciden con la expresión XPath especificada.  

En el siguiente ejemplo de código y figura, `<p>` se devuelven todos los elementos de la página.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Usar un selector XPath" lightbox="../media/console-array-xpath.msft.png":::
   Ilustración 10: uso de un selector XPath  
:::image-end:::  

En el siguiente ejemplo de código y figura, `<p>` se devuelven todos los elementos que contienen `<a>` elementos.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Usar un selector de XPath más complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Ilustración 11: usar un selector de XPath más complicado  
:::image-end:::  

Es similar a los otros comandos del selector, `$x(path)` tiene un segundo parámetro opcional, `startNode` que especifica un elemento o nodo desde el que buscar elementos.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Usar un selector XPath con startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Ilustración 12: uso de un selector XPath con `startNode`  
:::image-end:::  

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
> El [#1050237 de problemas de cromo][MonorailIssue1050237] está realizando un seguimiento de un error con la `debug()` función.  Si encuentra el problema, pruebe a [usar puntos de interrupción][DevtoolsJavascriptBreakpoints] en su lugar.  

Cuando se solicita el método especificado, se invoca el depurador y se interrumpe dentro del método en el panel de **fuentes** , lo que permite recorrer el código y depurarlo.  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Interrumpir dentro de un método con debug ()" lightbox="../media/console-debug-text.msft.png":::
   Ilustración 13: interrumpir un método con `debug()`  
:::image-end:::  

Use `undebug(method)` este modo para detener la ruptura en el método o use la interfaz de usuario para deshabilitar todos los puntos de interrupción.  

Para obtener más información sobre puntos de interrupción, vea [pausar el código con puntos de interrupción][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Muestra una lista de estilo de objeto de todas las propiedades del objeto especificado.  Este método es un alias para el método [Console. dir ()][MDNConsoleDir] .  

Evalúe `document.head` en la consola para mostrar el código HTML entre `<head>` las `</head>` etiquetas y.  En el siguiente ejemplo de código y figura, se muestra una lista de estilo de objeto después `console.dir()` de usar en la consola.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Registro de documento. Head con el método DIR ()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Ilustración 14: registrar `document.head` con el `dir()` método  
:::image-end:::  

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

En el siguiente ejemplo de código y figura, el `document.body` se abre en el panel **elementos** .  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspeccionar un elemento con inspeccionar ()" lightbox="../media/console-inspect-document-body.msft.png":::
   Ilustración 15: inspeccionar un elemento con `inspect()`  
:::image-end:::  

Cuando pase un método para inspeccionar, el método abrirá el documento en el panel **orígenes** para que lo inspeccione.  

## getEventListeners  

```console
getEventListeners(object)
```  

Devuelve los agentes de escucha de eventos registrados en el objeto especificado.  El valor devuelto es un objeto que contiene una matriz para cada tipo de evento registrado \ (como `click` o `keydown` \).  Los miembros de cada matriz son objetos que describen el agente de escucha registrado para cada tipo.  En la siguiente ilustración de ejemplo de código, se enumeran todos los agentes de escucha de eventos registrados en el objeto de documento.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Resultado de usar getEventListeners (Document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   Ilustración 16: el resultado de usar `getEventListeners(document)`  
:::image-end:::  

Si hay más de un agente de escucha registrado en el objeto especificado, la matriz contendrá un miembro para cada agente de escucha.  En la siguiente ilustración, hay dos escuchas de eventos registradas en el elemento de documento para el `click` evento.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Varios agentes de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Ilustración 17: varios agentes de escucha  
:::image-end:::  

Puede expandir aún más cada uno de los siguientes objetos para explorar las propiedades.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vista expandida del objeto Listener" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Ilustración 18: vista ampliada del objeto Listener  
:::image-end:::  

## teclas  

```console
keys(object)
```  

Devuelve una matriz que contiene los nombres de las propiedades que pertenecen al objeto especificado.  Para obtener los valores asociados de las mismas propiedades, use `values()` .  

Por ejemplo, supongamos que su aplicación ha definido el siguiente objeto.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

En los siguientes ejemplos de código y la figura, el resultado se ha dado por sentado que `player1` se definió en el espacio de nombres global \ (para simplificar \) antes de escribir `keys(player1)` y `values(player1)` en la consola.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Los comandos Keys () y Values ()" lightbox="../media/console-keys-values.msft.png":::
   Ilustración 19: `keys()` comandos y `values()`  
:::image-end:::  

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

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="El método monitor ()" lightbox="../media/console-function-monitor-sum.msft.png":::
   Ilustración 20: el `monitor()` método  
:::image-end:::  

Usar `unmonitor(method)` para cesar la supervisión.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Cuando se produce uno de los eventos especificados en el objeto especificado, el objeto de evento se registra en la consola.  Puede especificar un solo evento para supervisar, una matriz de eventos o uno de los tipos de eventos genéricos que se asignan a una colección predefinida de eventos.  Consulta la siguiente muestra de código y la figura.  

El siguiente monitor supervisa todos los eventos de cambiar tamaño en el objeto Window.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Supervisión de eventos de la ventana de supervisión" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Ilustración 21: supervisión de los eventos de la ventana de supervisión  
:::image-end:::  

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

En el siguiente ejemplo de código, el `key` tipo de evento correspondiente a `key` los eventos de un campo de texto de entrada está actualmente seleccionado en el panel **elementos** .  

```console
monitorEvents($0, "key");
```  

En la siguiente ilustración, se muestra el resultado de ejemplo después de escribir un carácter en el campo de texto.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Supervisión de eventos clave" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Ilustración 22: supervisión de eventos clave  
:::image-end:::  

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

Los perfiles también pueden estar anidados.  En los siguientes ejemplos de código y figura el resultado es el mismo, independientemente del orden.  

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

Los perfiles también pueden estar anidados.  En el siguiente ejemplo de código y figura el resultado es el mismo, independientemente del orden.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

El resultado aparece como una instantánea de montones en el panel **memoria** .  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfiles agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Ilustración 23: perfiles agrupados  
:::image-end:::  

> [!NOTE]
> Varios perfiles de CPU pueden funcionar al mismo tiempo y no es necesario cerrar cada uno de ellos en el orden de creación.  

## queryObjects  

```console
queryObjects(Constructor)
```  

Devuelve una matriz de objetos creados con el constructor especificado.  El ámbito de `queryObjects()` es el contexto en tiempo de ejecución actualmente seleccionado en la consola.

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      Devuelve All `Promises` .  
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
      
      Devuelve todos los objetos de los que se crearon instancias mediante `new functionName()` .  
   :::column-end:::
:::row-end:::  

---  

## Table  

```console
table(data[, columns])
```  

Registra datos de objeto con formato de tabla basado en el objeto de datos en con encabezados de columna opcionales.  En el siguiente ejemplo de código y figura, se muestra una lista de nombres que usan una tabla de la consola.  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="El resultado del método Table ()" lightbox="../media/console-table-display.msft.png":::
   Ilustración 24: el resultado del `table()` método  
:::image-end:::  

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

Detiene la supervisión del método especificado.  Este método se usa en conjunto con el método [monitor ()](#monitor) .  

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
