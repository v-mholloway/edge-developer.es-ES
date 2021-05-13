---
description: Una referencia de comandos de comodidad disponibles en la Microsoft Edge DevTools Console.
title: Referencia de API de utilidades de consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 436f2807c5fab1723ca6cc93fddc68d9ecf12db7
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564535"
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
# <a name="console-utilities-api-reference"></a>Referencia de API de utilidades de consola  

La API de utilidades de consola contiene una colección de comandos de comodidad para completar las siguientes tareas comunes.  

*   Elegir e inspeccionar elementos DOM  
*   Mostrar datos en formato legible  
*   Detener e iniciar el perfilador  
*   Supervisar eventos DOM  
    
> [!WARNING]
> Los siguientes comandos solo funcionan en la Microsoft Edge DevTools **Console**.  Los comandos no funcionan si se ejecutan desde los scripts.  

Para obtener más información sobre los `console.log()` métodos and `console.error()` y el resto de los `console.*` métodos, vaya a [Console API Reference][DevToolsConsoleApi].  

## <a name="recently-evaluated-expression"></a>Expresión recientemente evaluada  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
$_
```  

Este comando devuelve el valor de la expresión evaluada más recientemente.  

### <a name="console-example"></a>Ejemplo de consola  

En la siguiente figura, se evalúa una expresión sencilla \( `2 + 2` \).  A `$_` continuación, se evalúa la propiedad, que contiene el mismo valor.  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$_ es la expresión evaluada más recientemente" lightbox="../media/console-arithmatic.msft.png":::
   `$_` es la expresión evaluada más recientemente  
:::image-end:::  

En la siguiente figura, la expresión evaluada contiene inicialmente una matriz de nombres.  Al evaluar para encontrar la longitud de la matriz, el valor almacenado en se convierte en `$_.length` la última expresión `$_` evaluada, `4` .  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$_ cambia cuando se evalúan nuevos comandos" lightbox="../media/console-array-length.msft.png":::
   `$_` cambios cuando se evalúan los nuevos comandos  
:::image-end:::  

---  

## <a name="recently-chosen-element-or-javascript-object"></a>Elemento elegido recientemente o objeto JavaScript  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
$0
```  

Este comando devuelve el elemento elegido más recientemente o el objeto JavaScript.  `$1` devuelve el segundo elegido más recientemente, y así sucesivamente.  Los comandos , , y funcionan como una referencia histórica a los últimos cinco elementos DOM inspeccionados dentro de la herramienta Elementos o los últimos cinco objetos de montón de `$0` `$1` `$2` `$3` `$4` JavaScript elegidos **** **** en la herramienta Memoria.  

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
      &nbsp;
   :::column-end:::
:::row-end:::  

### <a name="console-example"></a>Ejemplo de consola  

En la siguiente figura, se `img` elige un elemento en la **herramienta** Elementos.  En el **cajón** de consola, `$0` se ha evaluado y muestra el mismo elemento.  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="Los $0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   El `$0`  
:::image-end:::  

En la siguiente figura, la imagen muestra un elemento diferente elegido en la misma página web.  Ahora `$0` hace referencia al elemento recién elegido, mientras que devuelve el elegido `$1` anteriormente.  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="El $1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   El `$1`  
:::image-end:::  

---  

## <a name="query-selector"></a>Selector de consultas  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
$(selector, [startNode])
```  

Este comando devuelve la referencia al primer elemento DOM con el selector CSS especificado.  Este método es un alias para el [método document.querySelector().][MdnDocsWebApiDocumentQueryselector]  

### <a name="console-example"></a>Ejemplo de consola  

En la siguiente figura, se devuelve una referencia al primer `<img>` elemento de la página web.  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="El $('img')" lightbox="../media/console-element-selector-image.msft.png":::
   El `$('img')`  
:::image-end:::  

Para buscar el primer elemento en el DOM o para buscarlo y mostrarlo en la página web, realice las siguientes acciones.  

1.  Mantenga el mouse sobre el resultado devuelto.  
1.  Abra el menú contextual \(haga clic con el botón derecho\).  
1.  Elija **Mostrar en el Panel de elementos**.  

En la siguiente figura, se devuelve una referencia al elemento seleccionado actualmente y se `src` muestra la propiedad.  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="El $('img').src" lightbox="../media/console-element-selector-image-source.msft.png":::
   El `$('img').src`  
:::image-end:::  

Este método también admite un segundo parámetro, , que especifica un elemento o nodo desde el que `startNode` buscar elementos.  El valor predeterminado del parámetro es `document` .  

En la siguiente figura, se devuelve el primer elemento después de que se encuentra el elemento y se devuelve la propiedad `img` `title--image` del `src` `img` elemento.  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="El $('img', document.querySelector('title--image')).src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   El `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> Si usa una biblioteca como jQuery que usa , la funcionalidad se sobrescribe y corresponde a la implementación `$` `$` de esa biblioteca.  

---  

## <a name="query-selector-all"></a>Selector de consultas todos  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
$$(selector, [startNode])
```  

Este comando devuelve una matriz de elementos que coinciden con el selector CSS especificado.  Este método equivale a ejecutar el [método document.querySelectorAll().][MdnDocsWebApiDocumentQueryselectorall]  

### <a name="console-example"></a>Ejemplo de consola  

En el siguiente ejemplo de código y figura, se usa para crear una matriz de todos los elementos de la página web actual y mostrar el valor de la propiedad `$$()` `<img>` para cada `src` elemento.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Usar $$() para elegir todas las imágenes de la página web y mostrar los orígenes" lightbox="../media/console-element-selector-image-all.msft.png":::
   Usar `$$()` para elegir todas las imágenes de la página web y mostrar los orígenes  
:::image-end:::  

Este método también admite un segundo parámetro, , que especifica un elemento o nodo desde el que `startNode` buscar elementos.  El valor predeterminado del parámetro es `document` .  

En la siguiente ilustración y ejemplo de código, una versión modificada del ejemplo de código y la figura anteriores se usa para crear una matriz de todos los elementos que aparecen en la página web actual después del `$$()` `<img>` nodo elegido.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Usar $$() para elegir todas las imágenes que aparecen después del elemento div <div> en la página web y mostrar los orígenes" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   Usar para elegir todas las imágenes que aparecen después del elemento especificado en la página `$$()` web y mostrar los `<div>` orígenes  
:::image-end:::  

> [!NOTE]
> Seleccione `Shift` + `Enter` en la **Consola para** iniciar una nueva línea sin ejecutar el script.  

---  

## <a name="xpath"></a>XPath  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
$x(path, [startNode])
```  

Este comando devuelve una matriz de elementos DOM que coinciden con la expresión XPath especificada.  

### <a name="console-example"></a>Ejemplo de consola  

En el siguiente ejemplo de código y figura, se devuelven todos los `<p>` elementos de la página web.  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Uso de un selector XPath" lightbox="../media/console-array-xpath.msft.png":::
   Uso de un selector XPath  
:::image-end:::  

En el siguiente ejemplo de código y figura, se devuelven todos los `<p>` elementos que contienen `<a>` elementos.  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Uso de un selector XPath más complicado" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   Uso de un selector XPath más complicado  
:::image-end:::  

Al igual que los demás comandos de selector, tiene un segundo parámetro opcional, , que especifica un elemento o nodo desde el que buscar `$x(path)` `startNode` elementos.  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Uso de un selector XPath con startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   Uso de un selector XPath con `startNode`  
:::image-end:::  

---  

## <a name="clear"></a>clear  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
clear()
```  

Este commnad borra la consola del historial.  

### <a name="console-example"></a>Ejemplo de consola  

```console
clear()
```  

## <a name="copy"></a>copy  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
copy(object)
```  

Este método copia una representación de cadena del objeto especificado en el portapapeles.  

### <a name="console-example"></a>Ejemplo de consola  

```console
copy($0)
```  

---  

## <a name="debug"></a>depurar  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
debug(method)
```  

>[!NOTE]
> El [Chromium problema #1050237][CR1050237] está rastreando un error con la `debug()` función.  Si encuentra el problema, intente usar [puntos de interrupción en][DevtoolsJavascriptBreakpoints] su lugar.  

Cuando se solicita el método especificado, el depurador invoca y rompe dentro del método en la **herramienta Orígenes.**  Le permite realizar un paso a través y depurar el código.  

### <a name="console-example"></a>Ejemplo de consola  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Irrumpir dentro de un método con debug()" lightbox="../media/console-debug-text.msft.png":::
   Dividir dentro de un método con `debug()`  
:::image-end:::  

Se `undebug(method)` usa para detener la interrupción del método o usar la interfaz de usuario para desactivar todos los puntos de interrupción.  

Para obtener más información sobre los puntos de interrupción, vaya a Cómo pausar el código con puntos de interrupción [en Microsoft Edge DevTools][DevtoolsJavascriptBreakpoints].  

---  

## <a name="dir"></a>dir  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
dir(object)
```  

Este comando muestra una lista de estilo de objeto de todas las propiedades del objeto especificado.  Este método es un alias para el [método console.dir().][MdnDocsWebApiConsoleDir]  

Evalúe `document.head` en la consola **para** mostrar el HTML entre las `<head>` `</head>` etiquetas y.  

### <a name="console-example"></a>Ejemplo de consola  

En el siguiente ejemplo de código y figura, se muestra una descripción de estilo de objeto después de usar `console.dir()` en la **consola**.  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Registro de document.head con el método dir()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   Registro `document.head` con `dir()` método  
:::image-end:::  

Para obtener más información, vaya a [console.dir()][DevToolsConsoleApiConsoleDirObject] en la API de consola.  

---  

## <a name="dirxml"></a>dirxml  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
dirxml(object)
```  

Este comando imprime una representación XML del objeto especificado, tal como se muestra en la **herramienta** Elementos.  Este método es equivalente al [método console.dirxml().][MdnDocsWebApiConsoleDirxml]  

---  

## <a name="inspect"></a>inspeccionar  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
inspect(object/method)
```  

Este comando se abre y elige el elemento u objeto especificado en el **** panel correspondiente: la herramienta **Elementos** para elementos DOM o la herramienta Memoria para objetos de montón de JavaScript.  

### <a name="console-example"></a>Ejemplo de consola  

En el siguiente ejemplo de código y figura, se `document.body` abre en la **herramienta** Elementos.  

### <a name="console-example"></a>Ejemplo de consola  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Inspeccionar un elemento con inspect()" lightbox="../media/console-inspect-document-body.msft.png":::
   Inspeccionar un elemento con `inspect()`  
:::image-end:::  

Al pasar un método para inspeccionar, el método abre la página web en la **herramienta Orígenes** para que la examine.  

---  

## <a name="geteventlisteners"></a>getEventListeners  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
getEventListeners(object)
```  

Este comando devuelve los agentes de escucha de eventos registrados en el objeto especificado.  El valor devuelto es un objeto que contiene una matriz para cada tipo de evento registrado \(como `click` o `keydown` \).  Los miembros de cada matriz son objetos que describen el agente de escucha registrado para cada tipo.  

### <a name="console-example"></a>Ejemplo de consola  

En el siguiente fragmento de código y figura, se enumeran todos los agentes de escucha de eventos registrados `document` en el objeto.  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Resultado del uso de getEventListeners(document)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   El resultado de usar `getEventListeners(document)`  
:::image-end:::  

Si se registra más de un agente de escucha en el objeto especificado, la matriz contiene un miembro para cada escucha.  En la siguiente figura, se registran dos agentes de escucha de eventos en el `document` elemento para el `click` evento.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Varios agentes de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   Varios agentes de escucha  
:::image-end:::  

Puede expandir cada uno de los siguientes objetos para explorar las propiedades.  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Vista expandida del objeto de escucha" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   Vista expandida del objeto de escucha  
:::image-end:::  

---  

## <a name="keys"></a>teclas  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
keys(object)
```  

Este comando devuelve una matriz que contiene los nombres de las propiedades que pertenecen al objeto especificado.  Para obtener los valores asociados de las mismas propiedades, use `values()` .  

### <a name="console-example"></a>Ejemplo de consola  

Por ejemplo, supongamos que la aplicación definió el siguiente objeto.  

```console
var player1 = {"name": "Ted", "level": 42}
```  

En los siguientes ejemplos de código y figura, se supone que el resultado se definió en el espacio de nombres `player1` global \(por simplicidad\) antes de escribir y `keys(player1)` en la `values(player1)` consola.  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Los comandos keys() y values()" lightbox="../media/console-keys-values.msft.png":::
   Los `keys()` comandos y `values()`  
:::image-end:::  

---  

## <a name="monitor"></a>monitor  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
monitor(method)
```  

Este comando registra un mensaje en la consola que indica el nombre del método junto con los argumentos pasados al método como parte de una solicitud.  

### <a name="console-example"></a>Ejemplo de consola  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="El método monitor()" lightbox="../media/console-function-monitor-sum.msft.png":::
   El `monitor()` método  
:::image-end:::  

Se `unmonitor(method)` usa para finalizar la supervisión.  

---  

## <a name="monitorevents"></a>monitorEvents  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
monitorEvents(object[, events])
```  

Cuando se produce uno de los eventos especificados en el objeto especificado, el objeto de evento se registra en la consola.  Puede especificar un único evento para supervisar, una matriz de eventos o uno de los tipos de eventos genéricos que se asignan a una colección predefinida de eventos.  

### <a name="console-example"></a>Ejemplo de consola  

Revise el siguiente ejemplo de código y figura.  

A continuación se supervisan todos los eventos de cambio de tamaño del objeto de ventana.  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Eventos de cambio de tamaño de ventana de supervisión" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   Eventos de cambio de tamaño de ventana de supervisión  
:::image-end:::  

El siguiente fragmento de código define una matriz para supervisar los eventos `resize` y ambos en el objeto `scroll` window.  

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

En el siguiente ejemplo de código, el tipo de evento correspondiente a los eventos de un campo de texto de entrada se elige `key` actualmente en la `key` **herramienta** Elementos.  

```console
monitorEvents($0, "key");
```  

En la siguiente figura, se muestra el resultado de ejemplo después de escribir un carácter en el campo de texto.  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Supervisión de eventos clave" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   Supervisión de eventos clave  
:::image-end:::  

---  

## <a name="profile"></a>profile  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
profile([name])
```  

Este comando inicia una sesión de generación de perfiles de CPU de JavaScript con un nombre opcional.  El [método profileEnd()](#profileend) completa el perfil y muestra los resultados en la **herramienta Memoria.**  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a>Ejemplo de consola  

1.  Ejecute el `profile()` método para iniciar la generación de perfiles.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Ejecute el [método profileEnd()](#profileend) para detener la generación de perfiles y mostrar los resultados en la **herramienta Memoria.**  

Los perfiles también pueden estar anidados.  En los siguientes ejemplos de código y figura, el resultado es el mismo sea cual sea el orden.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Es posible que varios perfiles de CPU funcionen al mismo tiempo y no es necesario cerrar cada uno en orden de creación.  

---  

## <a name="profileend"></a>profileEnd  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
profileEnd([name])
```  

Este comando completa una sesión de generación de perfiles de CPU de JavaScript y muestra los resultados en la **herramienta Memoria.**  Debe ejecutar el método [profile().](#profile)  <!--Navigate to [Speed Up JavaScript Runtime][DevtoolsRenderingToolsJsRuntime].  -->  

### <a name="console-example"></a>Ejemplo de consola  

1.  Ejecute el [método profile()](#profile) para iniciar la generación de perfiles.  
1.  Ejecute el `profileEnd()` método para detener la generación de perfiles y mostrar los resultados en la herramienta **Memoria.**  
    
    ```console
    profileEnd("My profile")
    ```  

Los perfiles también pueden estar anidados.  En el siguiente ejemplo de código y figura, el resultado es el mismo sea cual sea el orden.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

El resultado aparece como una instantánea de montón en la **herramienta Memoria.**  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Perfiles agrupados" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   Perfiles agrupados  
:::image-end:::  

> [!NOTE]
> Es posible que varios perfiles de CPU funcionen al mismo tiempo y no es necesario cerrar cada uno en orden de creación.  

---  

## <a name="queryobjects"></a>queryObjects  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
queryObjects(Constructor)
```  

Este comando devuelve una matriz de objetos creados con el constructor especificado.  El ámbito de `queryObjects()` es el contexto de tiempo de ejecución elegido actualmente en la **consola**.  

### <a name="console-example"></a>Ejemplo de consola  

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

### <a name="console-syntax"></a>Sintaxis de consola  

```console
table(data[, columns])
```  

Este comando registra los datos del objeto con formato de tabla basado en el objeto de datos con encabezados de columna opcionales.  

### <a name="console-example"></a>Ejemplo de consola  

En el siguiente ejemplo de código y figura, se muestra una lista de nombres que usan una tabla en la consola.  

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
   El resultado del `table()` método  
:::image-end:::  

---  

## <a name="undebug"></a>undebug  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
undebug(method)
```  

Este comando detiene la depuración del método especificado. Por lo tanto, cuando se solicita el método, el depurador ya no se invoca.  

### <a name="console-example"></a>Ejemplo de consola  

```console
undebug(getData);
```  

---  

## <a name="unmonitor"></a>unmonitor  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
unmonitor(method)
```  

Este comando detiene la supervisión del método especificado.  Este método se usa en función del [método monitor().](#monitor)  

### <a name="console-example"></a>Ejemplo de consola  

```console
unmonitor(getData);
```  

---  

## <a name="unmonitorevents"></a>unmonitorEvents  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
unmonitorEvents(object[, events])
```  

Este comando detiene la supervisión de eventos para el objeto y los eventos especificados.  

### <a name="console-example"></a>Ejemplo de consola  

Por ejemplo, el siguiente fragmento de código detiene toda la supervisión de eventos en el objeto de ventana.  

```console
unmonitorEvents(window);
```  

También puede detener selectivamente la supervisión de eventos específicos en un objeto.  Por ejemplo, el siguiente código inicia la supervisión de todos los eventos del elemento seleccionado actualmente y, a continuación, detiene la supervisión de eventos \(quizás para reducir el ruido en la salida de la `mouse` `mousemove` consola\).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

---  

## <a name="values"></a>valores  

### <a name="console-syntax"></a>Sintaxis de consola  

```console
values(object)
```  

Este comando devuelve una matriz que contiene los valores de todas las propiedades que pertenecen al objeto especificado.  

### <a name="console-example"></a>Ejemplo de consola  

```console
values(object);
```  

---  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevToolsConsoleApiConsoleDirObject]: ./api.md#dir "dir: referencia de api de consola | Microsoft Docs"  

[DevtoolsJavascriptBreakpoints]: ../javascript/breakpoints.md "Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"  

[DevtoolsRenderingToolsJsRuntime]: ../rendering-tools/js-runtime.md "Acelerar el tiempo de ejecución de JavaScript | Microsoft Docs"  

[CR1050237]: https://crbug.com/1050237 "Problema 1050237: debug(function) no funciona | Chromium errores"  

[MdnDocsWebApiConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console.dir() | MDN"  
[MdnDocsWebApiConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console.dirxml() | MDN"  
[MdnDocsWebApiDocumentQueryselector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document.querySelector() | MDN"  
[MdnDocsWebApiDocumentQueryselectorall]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document.querySelectorAll() | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/utilities) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
