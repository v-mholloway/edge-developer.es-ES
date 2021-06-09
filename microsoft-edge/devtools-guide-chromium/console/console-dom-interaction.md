---
description: Información general sobre cómo interactuar con la página web actual en el explorador mediante la herramienta Consola
title: Usar la consola para interactuar con el DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 56ce6b1d8f1ad98eeb9c141c2e9b002e7679d7de
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597019"
---
# <a name="use-the-console-to-interact-with-the-dom"></a>Usar la consola para interactuar con el DOM

La **herramienta Consola** no es solo para la información de [registro][DevtoolsConsoleConsoleLog] o para [ejecutar JavaScript arbitrario.][DevtoolsConsoleConsoleJavascript]  También es una excelente manera de interactuar con la página web en el explorador.  Conste que es una versión de entorno de script de **la herramienta Inspeccionar.**  

## <a name="read-from-the-dom"></a>Leer desde el DOM

Para hacer referencia al encabezado de la página web, realice las siguientes acciones.  

1.  Abra la **consola**.
    *   Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  
1.  Escriba o copie y pegue el siguiente fragmento de código en la **consola**.  
    
    ```javascript
    document.querySelector('header')
    ```  
    
:::image type="complex" source="../media/console-dom-get-reference.msft.png" alt-text="Para obtener una referencia al encabezado en la consola, use document.querySelector" lightbox="../media/console-dom-get-reference.msft.png":::
    Para obtener una referencia al encabezado en la consola, use `document.querySelector`  
:::image-end:::  

Si selecciona o `Shift` + `Tab` mueve el cursor del mouse sobre el resultado HTML, DevTools resalta el encabezado.  

:::image type="complex" source="../media/console-dom-highlight-element.msft.png" alt-text="DevTools resalta la sección que elija en la consola" lightbox="../media/console-dom-highlight-element.msft.png":::
    DevTools resalta la sección que elija en la **consola**  
:::image-end:::  

## <a name="manipulate-the-dom"></a>Manipular el DOM

También puede manipular la página web.  Por ejemplo, si copia y pega o escribe lo siguiente en la **Consola,** se muestra un borde verde alrededor del encabezado.

```javascript
document.querySelector('header').style.border = '2em solid green'
```  

:::image type="complex" source="../media/console-dom-add-border.msft.png" alt-text="Para agregar un borde a un elemento, use la consola" lightbox="../media/console-dom-add-border.msft.png":::
    Para agregar un borde a un elemento, use la **consola**  
:::image-end:::  

Según la complejidad de la página web, puede resultar desalentador encontrar el elemento adecuado para manipular.  Pero puede usar la herramienta **Inspeccionar** para ayudarle.  Diga que desea manipular la `Documentation` parte del encabezado.

:::image type="complex" source="../media/console-dom-highlight-documentation.msft.png" alt-text="Mostrar el elemento que inspecciona en la pantalla" lightbox="../media/console-dom-highlight-documentation.msft.png":::
    Mostrar el elemento que inspecciona en la pantalla  
:::image-end:::  

Para obtener una referencia directa al elemento que se debe manipular, complete las siguientes acciones.  

1.  Use la **herramienta Inspeccionar** para elegir el elemento.  

    :::image type="complex" source="../media/console-dom-use-inspector-to-get-element.msft.png" alt-text="Para elegir un elemento, use la herramienta Inspeccionar" lightbox="../media/console-dom-use-inspector-to-get-element.msft.png":::
        Para elegir un elemento, use la **herramienta Inspeccionar**  
    :::image-end:::  
    
1.  Seleccióne y DevTools saltará a la **herramienta** Elementos.  
1.  Elija el `...` menú situado junto al elemento del árbol DOM.  
    
    :::image type="complex" source="../media/console-dom-overflow-menu-in-elements.msft.png" alt-text="El elemento elegido se muestra en el árbol DOM de la herramienta Elementos, elija el menú desbordamiento para obtener más características" lightbox="../media/console-dom-overflow-menu-in-elements.msft.png":::
        El elemento elegido se muestra en el árbol DOM de la **herramienta Elementos,** elija el menú desbordamiento para obtener más características  
    :::image-end:::  
    
1.  Abra el menú contextual y elija `Copy`  >  `Copy JS Path` .  
    
    :::image type="complex" source="../media/console-dom-copy-JS-path.msft.png" alt-text="Copiar la ruta de acceso de JavaScript desde un elemento en el árbol DOM de la herramienta Elementos" lightbox="../media/console-dom-copy-JS-path.msft.png":::
        Copiar la ruta de acceso de JavaScript desde un elemento en el árbol DOM de la **herramienta** Elementos  
    :::image-end:::  
    
1.  Vuelva a la **consola y** pegue el comando.  
    
Para cambiar el texto del vínculo a `My Playground` , agregue al comando que ha `.textContent = "My Playground"` pegado anteriormente.  

:::image type="complex" source="../media/console-dom-change-content.msft.png" alt-text="Usar la consola para cambiar el contenido de un elemento" lightbox="../media/console-dom-change-content.msft.png":::
    Usar la **consola** para cambiar el contenido de un elemento  
:::image-end:::  

Use las manipulaciones dom de JavaScript que desee hacer en la **consola**.  Para que sea más conveniente, **la consola** viene con algunos métodos auxiliares.  

## <a name="helpful-console-utility-methods"></a>Métodos de utilidad de consola útiles  

Hay muchos métodos de comodidad y accesos directos disponibles como [Utilidades de consola.][DevtoolsConsoleUtilities]  Algunos de los métodos son increíblemente eficaces y son cosas que probablemente escribiste como una serie `console.log()` de instrucciones en el pasado.

### <a name="the-power-to-the-"></a>La potencia de $

El `$` tiene poderes especiales en **la consola** y puede recordarlo desde jQuery.

*   `$_` almacena el resultado del último comando.  Por lo tanto, si escribe `2 + 2` y selecciona `Enter` y, a continuación, escribe `$_` , la **consola** le muestra `4` .
*   `$0` to `$4` es una pila de los últimos elementos inspeccionados es siempre la más `$0` reciente.  Por lo tanto, en el ejemplo anterior, simplemente eligió el elemento de la herramienta **Inspeccionar** y escriba `$0.textContent = "My Playground"` para obtener el mismo efecto.
*   `$x()` permite elegir elementos DOM con XPATH.
*   `$()` y `$$()` son versiones más cortas de for y `document.querySelector()` `document.querySelectorAll()` .  
    
Por ejemplo, el siguiente fragmento de código recupera todos los vínculos de la página web \(as is short for \) y muestra los vínculos como una tabla ordenable para copiar y pegar, por ejemplo, en `$$('a')` `document.querySelectorAll('a')` Excel.

```javascript
console.table($$('a'),['href','text']);
```  

:::image type="complex" source="../media/console-dom-get-all-links.msft.png" alt-text="Obtener todos los vínculos de la página web y mostrar el resultado como una tabla" lightbox="../media/console-dom-get-all-links.msft.png":::
    Obtener todos los vínculos de la página web y mostrar el resultado como una tabla  
:::image-end:::  

Sin embargo, si no desea mostrar la información, pero desea tomarla como datos.  El `$$('a')` acceso directo proporciona los vínculos de delimitador y todas las propiedades de cada uno.  El problema es que solo desea los vínculos y el texto relacionado.  

:::image type="complex" source="../media/console-dom-too-much-link-information.msft.png" alt-text="El método abreviado $$ devuelve demasiada información" lightbox="../media/console-dom-too-much-link-information.msft.png":::
    El `$$` acceso directo devuelve demasiada información  
:::image-end:::  

El `$$` acceso directo tiene una característica adicional interesante.  En lugar de devolver un `NodeList` tipo `document.querySelectorAll()` puro, el `$$` acceso directo le ofrece todos los `Array` métodos.  Use `map()` el método para reducir la información a lo que necesita.  

```javascript
$$('a').map(a => {
    return {url: a.href, text: a.innerText}
})
```  

El fragmento de código devuelve una matriz de todos los vínculos como objetos `url` con y `text` propiedades.  

:::image type="complex" source="../media/console-dom-filter-link-data.msft.png" alt-text="Usar la asignación en $$ para filtrar la información al mínimo mínimo" lightbox="../media/console-dom-filter-link-data.msft.png":::
    Usar la asignación `$$` para filtrar la información al mínimo mínimo  
:::image-end:::  

Aún no ha terminado, varios vínculos son vínculos internos a la página web o tienen texto vacío.  Use el método filter para deshacerse de los vínculos internos.  

```javascript
$$('a').map(a => {
    return {text: a.innerText, url: a.href}
}).filter(a => {
    return a.text !== '' && !a.url.match('docs.microsoft.com')
})
```  

:::image type="complex" source="../media/console-dom-filter-out-empty-links.msft.png" alt-text="Obtener los vínculos que no están vacíos y son externos" lightbox="../media/console-dom-filter-out-empty-links.msft.png":::
    Obtener los vínculos que no están vacíos y son externos  
:::image-end:::  

Como se muestra al principio de la página web, también puede cambiar estos elementos.  Por ejemplo, el siguiente fragmento de código crea un borde verde alrededor de todos los vínculos externos:

```javascript
$$('a[href^="https://"]').forEach(
  a => a.style.border = '1px solid green'
)
```  

:::image type="complex" source="../media/console-dom-highlight-links.msft.png" alt-text="Para resaltar todos los vínculos externos, agregue un borde verde alrededor de cada uno" lightbox="../media/console-dom-highlight-links.msft.png":::
    Para resaltar todos los vínculos externos, agregue un borde verde alrededor de cada uno  
:::image-end:::  

En lugar de escribir JavaScript complejo para filtrar resultados, usa la potencia de los selectores CSS.  

Para crear una tabla de la información y para todas las imágenes de la página web que no son imágenes en `src` `alt` línea, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Escriba o copie y pegue el siguiente fragmento de código.  

```javascript
console.table($$('img:not([src^=data])'), ['src','alt'])
```  

:::image type="complex" source="../media/console-dom-complex-CSS-selector.msft.png" alt-text="Para elegir elementos, use un selector CSS complejo" lightbox="../media/console-dom-complex-CSS-selector.msft.png":::
    Para elegir elementos, use un selector CSS complejo  
:::image-end:::  

¿Listo para un ejemplo aún más complejo?  Las páginas web HTML generadas a partir de markdown como este artículo tienen valores de id. automáticos para cada encabezado que le permiten vincular profundamente a esa sección.  Por ejemplo, un `# New features` cambio en `<h1 id="new-features">New features</h1>` .  

Para enumerar todos los encabezados automáticos que se van a copiar y pegar, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Escriba o copie y pegue el siguiente fragmento de código.  

```javascript
let out = '';
$$('#main [id]').filter(
    elm => {return elm.nodeName.startsWith('H')}
).forEach(elm => {
   out += elm.innerText + "\n" + 
          document.location.href + '#' +
          elm.id + "\n";
});
console.log(out);
```  

El resultado es texto que contiene contenido para cada encabezado seguido de la dirección URL completa que apunta a él.  

:::image type="complex" source="../media/console-dom-get-generated-headings.msft.png" alt-text="Obtener todos los encabezados y las direcciones URL generadas de la página web" lightbox="../media/console-dom-get-generated-headings.msft.png":::
    Obtener todos los encabezados y las direcciones URL generadas de la página web  
:::image-end:::  

### <a name="clean-up-with-clear-and-copy"></a>Limpiar con borrar y copiar

Cuando se desarrolla en la **consola,** las cosas pueden resultar desordenas.  Puede resultar frustrante intentar elegir resultados mientras copia y pega.  Los dos métodos de utilidad siguientes le ayudan.  

*   `copy()` copia lo que le des al Portapapeles.  El `copy()` método es especialmente útil cuando se mezcla con que copia el último `$_` resultado.
*   `clear()` borra la **consola**.

### <a name="read-and-monitor-events"></a>Leer y supervisar eventos

Otros dos métodos de utilidad interesantes de **la consola tratan** el control de eventos.

*   `getEventListeners(node)` enumera todos los agentes de escucha de eventos de un nodo.
*   `monitorEvents(node, events)` supervisa y registra los eventos que ocurren en un nodo.

Para enumerar todo el agente de escucha de eventos asignado al primer formulario de la página web, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Escriba o copie y pegue el siguiente fragmento de código.  
    
    ```javascript
    getEventListeners($('form')); 
    ```  

:::image type="complex" source="../media/console-dom-get-form-events.msft.png" alt-text="Obtener todos los agentes de escucha de eventos para el primer formulario de la página web" lightbox="../media/console-dom-get-form-events.msft.png":::
    Obtener todos los agentes de escucha de eventos para el primer formulario de la página web  
:::image-end:::  

Al supervisar, se obtiene una notificación en la **consola** cada vez que algo cambia en los elementos especificados.  Defina los eventos que desea escuchar como un segundo parámetro.  Es importante que defina los eventos que desea supervisar, de lo contrario, se notifica cualquier evento que se produce en el elemento.

Para obtener una notificación en la **Consola** cada vez que se desplaza, cambie el tamaño de la ventana o cuando el usuario los tipos en el formulario de búsqueda, complete las siguientes acciones.  

1.  Abra la **consola**.  
1.  Escriba o copie y pegue el siguiente fragmento de código.  
    
    ```javascript
    monitorEvents(window, ['resize', 'scroll']);
    monitorEvents($0, 'keyup');
    ```  
    
:::image type="complex" source="../media/console-dom-monitor-events.msft.png" alt-text="La consola muestra todos los eventos de desplazamiento que se produce en la ventana" lightbox="../media/console-dom-monitor-events.msft.png":::
    **La** consola muestra todos los eventos de desplazamiento que se produce en la ventana  
:::image-end:::  

Para registrar cualquier acción clave en el elemento seleccionado actualmente, céntrate en el formulario de búsqueda en el encabezado y selecciona algunas claves.  

:::image type="complex" source="../media/console-dom-monitor-key-events.msft.png" alt-text="La consola muestra los eventos keyup que se suceden en el formulario" lightbox="../media/console-dom-monitor-key-events.msft.png":::
    **La** consola muestra `keyup` los eventos que ocurren en el formulario  
:::image-end:::  

Para detenerlo, quite la supervisión que estableció con el siguiente fragmento de código.  

```javascript
unmonitorEvents(window, ['resize', 'scroll']);
unmonitorEvents($0, 'key');
```  

## <a name="reuse-dom-manipulation-scripts"></a>Reutilizar scripts de manipulación dom

Puede resultar útil manipular el DOM desde la **consola**.  Pronto puede encontrarse con las limitaciones de la **consola como** plataforma de desarrollo.  La buena noticia es que la [herramienta Orígenes][DevtoolsSourcesIndex] de DevTools ofrece un entorno de desarrollo totalmente destacado.  En la **herramienta Orígenes,** puede completar las siguientes acciones.  

*   Almacene los scripts de la **consola como** [fragmentos de código][DevToolsJavascriptSnippets].  
*   Ejecute los scripts en una página web con un método abreviado de teclado o el editor.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleConsoleJavascript]: ./console-javascript.md "Consola como entorno de JavaScript | Microsoft Docs"  
[DevtoolsConsoleConsoleLog]: ./console-log.md "Inicia sesión en la herramienta consola | Microsoft Docs"  
[DevtoolsConsoleUtilities]: ./utilities.md "Referencia de api de utilidades de consola | Microsoft Docs"  

[DevToolsJavascriptSnippets]: ../javascript/snippets.md "Ejecute fragmentos de código de JavaScript en cualquier página con Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsSourcesIndex]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
