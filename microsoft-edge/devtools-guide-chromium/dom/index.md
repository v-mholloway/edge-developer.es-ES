---
description: Cómo ver nodos, buscar nodos, editar nodos, nodos de referencia en la consola, interrumpir los cambios de nodo y mucho más.
title: Introducción a la visualización y cambio del DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e4c08fb2fd5f360f037502c04edabaabb873ba16
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439243"
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

# <a name="get-started-with-viewing-and-changing-the-dom"></a>Introducción a la visualización y cambio del DOM  

Complete estos tutoriales interactivos para aprender los conceptos básicos de ver y cambiar el DOM de una página mediante Microsoft Edge DevTools.  

En este tutorial se supone que conoce la diferencia entre DOM y HTML.  Vaya a [Apéndice: HTML frente al DOM](#appendix-html-versus-the-dom) para obtener una explicación.  

## <a name="open-dom-examples"></a>Ejemplos de OPEN DOM  

1.  Mantenga `Control` presionada \(Windows, Linux\) o `Command` \(macOS\) y elija **Ejemplos de DOM** para abrir en una nueva pestaña.  
    
    [Ejemplos de DOM][GlitchDomExamples]  
    
## <a name="view-dom-nodes"></a>Ver nodos DOM  

El árbol DOM del panel Elementos es donde se hacen todas las actividades relacionadas con DOM en DevTools.  

### <a name="inspect-a-node"></a>Inspeccionar un nodo  

Cuando está interesado en un nodo DOM determinado, **Inspect** es una forma rápida de abrir DevTools e investigar ese nodo.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Inspeccionar un nodo,** elija **Miguel Ángel** con el botón secundario y elija **Inspeccionar**.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Inspeccionar un nodo  
    :::image-end:::  
    
    1.  Se **abre** la herramienta Elementos de DevTools.  `<li>Michelangelo</li>` se resalta en el **árbol DOM**.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Resaltar el nodo Miguel Ángel" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Resaltar el `Michelangelo` nodo  
        :::image-end:::  
        
        1.  Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="El icono Inspeccionar" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               El **icono Inspeccionar**  
            :::image-end:::  
            
1.  En **Inspeccionar un nodo,** elija el **texto de** Tokio.  Ahora, `<li>Tokyo</li>` se resalta en el árbol DOM.  

Inspeccionar un nodo también es el primer paso para ver y cambiar los estilos de un nodo.  Vaya a [Introducción a Ver y cambiar CSS][DevToolsCssGetStarted].  

### <a name="navigate-the-dom-tree-with-a-keyboard"></a>Navegar por el árbol DOM con un teclado  

Una vez que haya seleccionado un nodo en el árbol DOM, puede navegar por el árbol DOM con el teclado.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Navegar por el árbol DOM con un teclado**, elija Anillo con el botón **derecho** y elija **Inspeccionar**.  `<li>Ringo</li>` se selecciona en el árbol DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspeccionar el nodo Ringo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Inspeccionar el `Ringo` nodo  
    :::image-end:::  
    
    1.  Seleccione la `Up` tecla de flecha 2 veces.  `<ul>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspeccionar el nodo ul" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Inspeccionar el `ul` nodo  
        :::image-end:::  
        
    1.  Seleccione la `Left` tecla de flecha.  La `<ul>` lista se contrae.  
    1.  Vuelva a `Left` seleccionar la tecla de flecha.  Se selecciona el elemento `<ul>` primario del nodo.  En este caso, es el `<div>` con el identificador `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Seleccione la tecla de flecha 2 veces para volver a seleccionar `Down` la lista que acaba de `<ul>` contraer.  Debe tener el siguiente aspecto: `<ul>... </ul>`  
    1.  Seleccione la `Right` tecla de flecha.  La lista se expande.  

### <a name="scroll-into-view"></a>Desplazarse a la vista  

Al ver el árbol DOM, es posible que te interese un nodo DOM que no esté actualmente en la ventanilla.  Por ejemplo, supongamos que se desplazó hasta la parte inferior de la página y que le interesa el nodo situado en `<h1>` la parte superior de la página.  **Desplazarse a la** vista le permite cambiar rápidamente la posición de la ventanilla para que pueda revisar el nodo.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Desplazarse a la vista**, elija **Magritte con** el botón derecho y elija **Inspeccionar**.  
1.  Desplácese hasta la parte inferior de la página Ejemplos de DOM.  
1.  El `<li>Magritte</li>` nodo todavía debe estar seleccionado en el árbol DOM.  Si no es así, vuelva a [Desplazarse a la vista](#scroll-into-view) y vuelva a empezar.  
1.  Mantenga el mouse en `<li>Magritte</li>` el nodo, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Desplazarse a la vista**.  La ventanilla se desplaza hacia arriba para que pueda revisar el **nodo Magritte.**  Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no puede revisar la **opción Desplazarse a la** vista.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Desplazarse a la vista" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Desplazarse a la vista**  
    :::image-end:::  

### <a name="search-for-nodes"></a>Buscar nodos  

Puede buscar en el árbol DOM por cadena, selector CSS o selector XPath.  

1.  Centra el cursor en la **herramienta** Elementos.  
1.  Seleccione `Control` + `F` \(Windows, Linux\) o `Command` + `F` \(macOS\).  La barra de búsqueda se abre en la parte inferior del árbol DOM.  
1.  Escribe `The Moon is a Harsh Mistress`.  La última oración se resalta en el árbol DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Resaltar la consulta en la barra de búsqueda" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Resaltar la consulta en la barra de búsqueda  
    :::image-end:::  
    
Como se mencionó anteriormente, la barra de búsqueda también admite selectores CSS y XPath.  

## <a name="edit-the-dom"></a>Editar el DOM  

Puede editar el DOM al instante y revisar cómo afectan los cambios a la página.  

### <a name="edit-content"></a>Editar contenido  

Para editar el contenido de un nodo, haga doble clic en el contenido del árbol DOM.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Editar contenido,** elija **Michelle** con el botón derecho y elija **Inspeccionar**.  
    1.  En el árbol DOM, haga doble clic en `Michelle` .  En otras palabras, haga doble clic en el texto entre `<li>` y `</li>` .  El texto se resalta para indicar que está seleccionado.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Editar el texto" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Editar el texto  
        :::image-end:::  
        
    1.  Eliminar `Michelle` , escriba `Leela` y, a continuación, `Enter` seleccione para confirmar el cambio.  El texto del DOM cambia de **Michelle** a **Leela**.  

### <a name="edit-attributes"></a>Editar atributos  

Para editar atributos, haga doble clic en el nombre o el valor del atributo.  Siga las instrucciones para obtener información sobre cómo agregar atributos a un nodo.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Editar atributos**, elija Howard con el botón **derecho** y elija **Inspeccionar**.  
1.  Haga doble clic `<li>` en .  El texto se resalta para indicar que el nodo está seleccionado.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Editar el nodo" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Editar el nodo  
    :::image-end:::  
    
1.  Seleccione la `Right` tecla de flecha, agregue un espacio, escriba y, a `style="background-color:gold"` continuación, seleccione `Enter` .  El color de fondo del nodo cambia a oro.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Agregar un atributo style al nodo" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Agregar un `style` atributo al nodo  
    :::image-end:::  
    
### <a name="edit-node-type"></a>Editar tipo de nodo  

Para editar el tipo de un nodo, haga doble clic en el tipo y, a continuación, escriba el nuevo tipo.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Editar tipo de nodo**, elija Hank con el botón **secundario** y elija **Inspeccionar**.  
    1.  Haga doble clic `<li>` en .  El texto `li` está resaltado.  
    1.  Eliminar `li` , escribir `button` y, a continuación, seleccionar `Enter` .  El `<li>` nodo cambia a un `<button>` nodo.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Cambiar el tipo de nodo a botón" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Cambiar el tipo de nodo a `button`  
        :::image-end:::  
        
### <a name="reorder-dom-nodes"></a>Reordenar nodos DOM  

Arrastre nodos para volver a ordenarlos.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Reordenar nodos DOM,** elija **Elvis Presley con** el botón derecho y elija **Inspeccionar**.  
    
    > [!NOTE]
    > Es el último elemento de la lista.  
    
    1.  En el árbol DOM, arrastre `<li>Elvis Presley</li>` hasta la parte superior de la lista.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Arrastre el nodo a la parte superior de la lista" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Arrastre el nodo a la parte superior de la lista  
        :::image-end:::  
        
### <a name="force-state"></a>Estado de fuerza  

Puede forzar a los nodos a permanecer en estados como `:active` , , , y `:hover` `:focus` `:visited` `:focus-within` .  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Estado de fuerza**, mantenga el mouse en El señor de las **moscas**.  El color de fondo se convierte en naranja.  
    1.  Mantenga el **mouse en El señor de las moscas**, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
    1.  Mantenga el `<li class="demo--hover">The Lord of the Flies</li>` mouse sobre , abra el menú contextual \(haga clic con el botón secundario\) y elija Forzar **estado**  >  **:hover**.  Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no se muestra la opción.  El color de fondo permanece naranja aunque no se mantenga el puntero sobre el nodo.  

### <a name="hide-a-node"></a>Ocultar un nodo  

Seleccione `H` para ocultar un nodo.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Ocultar un nodo,** elija **Las estrellas mi destino y** elija **Inspeccionar**.  
    1.  Seleccione la `H` clave.  El nodo está oculto.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Cómo es el nodo en el árbol DOM después de que esté oculto" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           Cómo es el nodo en el árbol DOM después de que esté oculto  
        :::image-end:::  
        
    1.  Vuelva a `H` seleccionar la clave.  El nodo se muestra de nuevo.  

### <a name="delete-a-node"></a>Eliminar un nodo  

Seleccione `Delete` para eliminar un nodo.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Eliminar un nodo,** elija **Foundation** con el botón secundario y elija **Inspeccionar**.  
    1.  Seleccione la `Delete` clave.  El nodo se elimina.  
    1.  Seleccione `Control` + `Z` \(Windows, Linux\) o `Command` + `Z` \(macOS\).  La última acción es deshacer y el nodo vuelve a aparecer.  

## <a name="access-nodes-in-the-console"></a>Nodos de acceso en la consola  

DevTools proporciona algunos accesos directos para obtener acceso a los nodos DOM desde la consola o para obtener referencias de JavaScript a cada uno.  

### <a name="reference-the-currently-selected-node-with-0"></a>Hacer referencia al nodo seleccionado actualmente con $0  

Al inspeccionar un nodo, el texto junto al nodo significa que puede hacer referencia a este nodo en la `== $0` consola con la variable `$0` .  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Referencia al nodo seleccionado actualmente con $0**, elija La mano izquierda de **la** oscuridad y elija **Inspeccionar**.  
    1.  Seleccione la `Escape` tecla para abrir el cajón de consola.  
    1.  Escriba `$0` y seleccione la `Enter` clave.  El resultado de la expresión muestra que `$0` se evalúa como `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="El resultado de la primera expresión $0 en la consola" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            El resultado de la primera `$0` expresión de la **consola**  
        :::image-end:::  
        
    1.  Mantenga el mouse sobre el resultado.  El nodo se resalta en la ventanilla.  
    1.  Elija en el árbol DOM, escriba de nuevo en la consola y, a `<li>Dune</li>` `$0` continuación, vuelva a `Enter` seleccionar.  Ahora, `$0` se evalúa como `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="El resultado de la segunda expresión $0 en la consola" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           El resultado de la segunda `$0` expresión en la **consola**  
        :::image-end:::  
        
### <a name="store-as-global-variable"></a>Almacenar como variable global  

Si necesita volver a hacer referencia a un nodo muchas veces, guárdalo como una variable global.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Almacenar como variable global**, mantenga el mouse en **El**gran reposo , abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
    1.  Mantenga el mouse en el árbol DOM, abra el menú contextual \(hacer clic con el `<li>The Big Sleep</li>` botón secundario\) y elija Almacenar como variable **global**.  Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no se muestra la opción.  
    1.  Escriba `temp1` la consola y, a continuación, seleccione `Enter` .  El resultado de la expresión muestra que la variable evalúa el nodo.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="El resultado de la expresión temp1" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           El resultado de la `temp1` expresión  
        :::image-end:::  
        
### <a name="copy-js-path"></a>Copiar ruta de acceso DE JS  

Copie la ruta de acceso de JavaScript en un nodo cuando necesite hacer referencia a ella en una prueba automatizada.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Copiar ruta de acceso JS**, mantenga el mouse en Los **hermanos Karamazov**, abra el menú contextual \(haga clic con el botón secundario\) y elija **Inspeccionar**.  
    1.  Mantenga el mouse en el árbol DOM, abra el menú contextual \(hacer clic con el `<li>The Brothers Karamazov</li>` botón secundario\) y elija **Copiar**  >  **ruta js**.  Una `document.querySelector()` expresión que se resuelve en el nodo se ha copiado en el portapapeles.  
    1.  Seleccione `Control` + `V` \(Windows, Linux\) o `Command` + `V` \(macOS\) para pegar la expresión en la consola.  
    1.  Seleccione `Enter` esta opción para evaluar la expresión.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="El resultado de la expresión Copy JS Path" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           El resultado de la **expresión Copy JS Path**  
        :::image-end:::  
        
## <a name="break-on-dom-changes"></a>Interrupción de los cambios dom  

DevTools permite pausar el JavaScript de una página cuando JavaScript modifica el DOM.  

### <a name="break-on-attribute-modifications"></a>Interrupción en las modificaciones de atributos  

Use puntos de interrupción de modificación de atributos cuando desee pausar JavaScript que haga que cambie cualquier atributo de un nodo.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Interrumpir las modificaciones de atributo,** elija **Sauerkraut con el botón** derecho y elija **Inspeccionar**.  
    1.  En el árbol DOM, mantenga el mouse sobre , abra el menú contextual \(haga clic con el `<li id="target">Sauerkraut</li>` botón secundario\) y elija Interrumpir las modificaciones **de**  >  **atributo**.  Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no se muestra la opción.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Interrupción en las modificaciones de atributos" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Interrupción en las modificaciones de atributos**  
        :::image-end:::  
        
    1.  En el siguiente paso, se le indicará que elija un botón que detenga el código de la página.  Después de pausar la página, ya no podrá desplazarse por la página.  Debe elegir **Reanudar script** \( Reanudar script \) para que la página se pueda desplazar de ![ ](../media/resume-script-icon.msft.png) nuevo.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Dónde reanudar la ejecución de scripts" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Dónde reanudar la ejecución de scripts  
        :::image-end:::  
        
    1.  Elija el **botón Establecer fondo** anterior.  Esto establece el `style` atributo del nodo en `background-color:thistle` .  DevTools pausa la página y resalta el código que hizo que el atributo cambiara.  
    1.  Elija **Resume Script** \( Resume Script ![ ](../media/resume-script-icon.msft.png) \), como se mencionó anteriormente.  
    
### <a name="break-on-node-removal"></a>Interrupción en la eliminación de nodos  

Si desea pausar cuando se quita un nodo determinado, use puntos de interrupción de eliminación de nodos.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Interrumpir la eliminación de nodos,** elija **Neuromancer con** el botón secundario y elija **Inspeccionar**.  
    1.  En el árbol DOM, mantenga el mouse sobre , abra el menú contextual \(haga clic con el botón `<li id="target">Neuromancer</li>` secundario\) y elija Interrumpir al **quitar**  >  **nodo**.  Vaya a [Apéndice: faltan opciones](#appendix-missing-options) si no se muestra la opción.  
    1.  Elija el **botón Eliminar** anterior.  DevTools pausa la página y resalta el código que hizo que se quitara el nodo.  
    1.  Elija **Reanudar script** \( Reanudar script ![ ](../media/resume-script-icon.msft.png) \).  
    
### <a name="break-on-subtree-modifications"></a>Interrupción de las modificaciones del subárbol  

Después de colocar un punto de interrupción de modificación de subárbol en un nodo, DevTools pausa la página cuando se agrega o quita cualquiera de los descendientes del nodo.  

1.  [Abra ejemplos de DOM](#open-dom-examples).  
1.  En **Interrumpir las modificaciones del subárbol,** elija A Fire Upon The **Deep** y elija **Inspect**.  
    1.  En el árbol DOM, mantenga el mouse sobre , que es el nodo anterior , abra el menú contextual \(haga clic con el botón secundario\) y elija `<ul id="target">` `<li>A Fire Upon the Deep</li>` Interrumpir en **modificaciones**  >  **del subárbol**.  Si no se muestra la opción, vaya a [Apéndice: Falta opciones](#appendix-missing-options).  
    1.  Elija **Agregar elemento**secundario .  El código se detiene porque se `<li>` agregó un nodo a la lista.  
    1.  Elija **Reanudar script** \( Reanudar script ![ ](../media/resume-script-icon.msft.png) \).  
    
## <a name="next-steps"></a>Pasos siguientes  

Eso cubre la mayoría de las características relacionadas con DOM en DevTools.  Para descubrir el resto de las características, mantenga el mouse en los nodos del árbol DOM, abra el menú contextual \(haga clic con el botón secundario\) y experimente con las otras opciones que no se han cubierto en este tutorial.  Vaya a [Métodos abreviados de teclado del panel Elementos][DevToolsShortcutsElements].  

Consulte la página [principal de Microsoft Edge DevTools][MicrosoftEdgeDevTools] para descubrir todo lo que puede hacer con DevTools.  

<!--Navigate to [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## <a name="appendix-html-versus-the-dom"></a>Apéndice: HTML frente al DOM  

En la siguiente sección se explica rápidamente la diferencia entre HTML y DOM.  

:::row:::
   :::column span="":::
      Cuando se usa un explorador web para solicitar una página, el servidor devuelve HTML como el siguiente fragmento de código  

      ```html
      <!doctype html>
      <html>
          <head>
              <title>Hello, world!</title>
          </head>
          <body>
              <h1>Hello, world!</h1>
              <p>This is a hypertext document on the World Wide Web.</p>
              <script src="/script.js" async></script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      El explorador analiza el HTML y crea un árbol de objetos como la siguiente lista.  
      
      ```dom
      html
          head
              title
          body
              h1
              p
              script
      ```  
   :::column-end:::
:::row-end:::  

Este árbol de objetos o nodos que representa el contenido de la página se denomina DOM.  

:::row:::
   :::column span="":::
      Ahora mismo tiene el mismo aspecto que el HTML, pero supongamos que el script al que se hace referencia en la parte inferior del HTML ejecuta el siguiente fragmento de código.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Ese código quita el `h1` nodo y agrega otro nodo al `p` DOM.  El DOM completo ahora muestra la siguiente lista.  
      
      ```dom
      html
          head
              title
          body
              p
              script
              p
      ```  
   :::column-end:::
:::row-end:::  

El CÓDIGO HTML de la página ahora es diferente del DOM.  En otras palabras, HTML representa el contenido inicial de la página y el DOM representa el contenido actual de la página.  Cuando JavaScript agrega, quita o edita nodos, el DOM se convierte en diferente que el HTML.  

Vaya a [Introducción al DOM][MDNIntroductionToDOM] para obtener más información.  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Hover on the `<li>Magritte</li>` node, open the contextual menu \(right-click\), and choose **Scroll into view**.  Your viewport scrolls back up so that the **Magritte** node is displayed.  If you the **Scroll into view** option is not displayed, navigate to [Appendix: Missing options](#appendix-missing-options).
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Scroll into view" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## <a name="appendix-missing-options"></a>Apéndice: Faltan opciones  

Muchas de las instrucciones de este tutorial le indican que mantenga el mouse en un nodo del árbol DOM, abra el menú contextual \(hacer clic con el botón secundario\) y, a continuación, elija una opción en el menú contextual que aparece.  Si no se muestra la opción especificada en el menú contextual, intente alejarse del texto del nodo y abrir el menú contextual \(hacer clic con el botón secundario\).  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Dónde elegir si no se muestran todas las opciones" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Dónde elegir si no se muestran todas las opciones  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge \(Chromium\) Developer Tools | Microsoft Docs"  
[DevToolsCssGetStarted]: ../css/index.md "Introducción a la visualización y cambio de css | Microsoft Docs"  
[DevToolsShortcutsElements]: ../shortcuts/index.md#elements-tool-keyboard-shortcuts "Métodos abreviados de teclado de la herramienta Elements: métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Ejemplo de Microsoft Edge (Chromium) DevTools DOM | Glitch"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción al dom | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/dom/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
