---
description: Cómo ver nodos, buscar nodos, editar nodos, hacer referencia a nodos de la consola, interrumpir cambios de nodo y mucho más.
title: Introducción a la visualización y el cambio de DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 8c0b544f2c4717a01d09c287f1167c81456a97f3
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125030"
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

# Introducción a la visualización y el cambio de DOM  

Complete estos tutoriales interactivos para obtener información básica sobre cómo ver y cambiar el DOM de una página con Microsoft Edge DevTools.  

En este tutorial se supone que conoce la diferencia entre DOM y HTML.  Consulta [el apéndice: HTML en comparación con Dom](#appendix-html-versus-the-dom) para obtener una explicación.  

## Ejemplos de Open DOM  

1.  Espera `Control` \ (Windows, Linux \) o `Command` \ (MacOS \) y elige **ejemplos de Dom** para abrir en una nueva pestaña.  
    
    [Ejemplos de DOM][GlitchDomExamples]  
    
## Ver nodos DOM  

El árbol DOM del panel elementos es el lugar donde se realizan todas las actividades relacionadas con DOM en DevTools.  

### Inspeccionar un nodo  

Cuando esté interesado en un nodo DOM determinado, **inspeccionar** es una forma rápida de abrir DevTools e investigar ese nodo.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **inspeccionar un nodo**, seleccione **Michelangelo** y elija **inspeccionar**.  
    
    :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-glitch-dom-examples-michelangelo-inspect.msft.png":::
       Inspeccionar un nodo  
    :::image-end:::  
    
    1.  Se abre el panel **elementos** de DevTools.  `<li>Michelangelo</li>` está resaltado en el **árbol DOM**.  
        
        :::image type="complex" source="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png":::
           Resaltar el `Michelangelo` nodo  
        :::image-end:::  
        
        1.  Haga clic en el icono de **inspeccionar** \ ( ![ inspeccionar ][ImageInspectIcon] \) en la esquina superior izquierda de DevTools.  
            
            :::image type="complex" source="../media/dom-elements-highlighted-select-element-page-inspect.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-select-element-page-inspect.msft.png":::
               Icono de **inspección**  
            :::image-end:::  
            
1.  En **inspeccionar un nodo**, haga clic en el texto de **Tokio** .  Ahora, `<li>Tokyo</li>` está resaltado en el árbol DOM.  

Inspeccionar un nodo también es el primer paso para ver y cambiar los estilos de un nodo.  Consulte Introducción [a la visualización y el cambio de CSS][DevToolsCssGetStarted].  

### Navegar por el árbol DOM con un teclado  

Una vez que haya seleccionado un nodo en el árbol DOM, puede desplazarse por el árbol DOM con el teclado.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **navegar por el árbol DOM con un teclado**, haga clic con el botón derecho en **Ringo** y elija **inspeccionar**.  `<li>Ringo</li>` está seleccionado en el árbol DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png":::
       Inspeccionar el `Ringo` nodo  
    :::image-end:::  
    
    1.  Presione la `Up` tecla de dirección dos veces.  `<ul>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png":::
           Inspeccionar el `ul` nodo  
        :::image-end:::  
        
    1.  Presione la `Left` tecla de dirección.  La `<ul>` lista se contraerá.  
    1.  `Left`Vuelva a presionar la tecla de dirección.  Se selecciona el elemento primario del `<ul>` nodo.  En este caso, es el `<div>` con el identificador `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Presione la `Down` tecla de dirección dos veces para que se vuelva a seleccionar la `<ul>` lista que acaba de contraer.  Debe tener el siguiente aspecto: `<ul>... </ul>`  
    1.  Presione la `Right` tecla de dirección.  Se expande la lista.  

### Desplazarse en la vista  

Al ver el árbol DOM, es posible que te encuentres interesado en un nodo DOM que actualmente no está en la ventanilla.  Por ejemplo, supongamos que se ha desplazado a la parte inferior de la página y está interesado en el `<h1>` nodo de la parte superior de la página.  **Desplazarse hacia la vista** le permite cambiar rápidamente la posición de la ventanilla para poder ver el nodo.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **desplazarse a la vista**, seleccione **Magritte** y elija **inspeccionar**.  
1.  Desplácese hasta la parte inferior de la página de ejemplos de DOM.  
1.  El `<li>Magritte</li>` nodo debe seguir estando seleccionado en el árbol DOM.  Si no es así, vuelva a [desplazarse](#scroll-into-view) hacia la vista y volver a empezar.  
1.  Haga clic con el botón derecho en el `<li>Magritte</li>` nodo y seleccione **desplazarse a la vista**.  Su ventanilla se desplaza hacia arriba para que pueda ver el nodo **Magritte** .  Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver la opción **desplazarse a la vista** .
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       **Desplazarse en la vista**  
    :::image-end:::  

### Buscar nodos  

Puede buscar en el árbol DOM por cadena, selector de CSS o selector XPath.  

1.  Centre el cursor en el panel **elementos** .  
1.  Seleccione `Control` + `F` \ (Windows, Linux \) o `Command` + `F` \ (MacOS \).  La barra de búsqueda se abre en la parte inferior del árbol DOM.  
1.  Escribe `The Moon is a Harsh Mistress`.  La última oración se resalta en el árbol DOM.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-search-nodes-highlight.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-search-nodes-highlight.msft.png":::
       Resaltar la consulta en la barra de búsqueda  
    :::image-end:::  
    
Como se mencionó anteriormente, la barra de búsqueda también admite los selectores CSS y CSS.  

## Editar el DOM  

Puede editar el DOM sobre la marcha y ver cómo afectan esos cambios a la página.  

### Editar contenido  

Para editar el contenido de un nodo, haga doble clic en el contenido del árbol DOM.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **editar contenido**, haga clic con el botón derecho en **Michelle** y elija **inspeccionar**.  
    1.  En el árbol DOM, haga doble clic `Michelle` .  En otras palabras, haga doble clic en el texto entre `<li>` y `</li>` .  El texto se resalta para indicar que está seleccionado.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-content.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-edit-content.msft.png":::
           Editar el texto  
        :::image-end:::  
        
    1.  Eliminar `Michelle` , escriba `Leela` y, a continuación, seleccione `Enter` para confirmar el cambio.  El texto del DOM cambia de **Michelle** a **Leela**.  

### Editar atributos  

Para editar atributos, haga doble clic en el nombre o valor del atributo.  Siga las instrucciones para obtener información sobre cómo agregar atributos a un nodo.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **Editar atributos**, elija **Howard** y elija **inspeccionar**.  
1.  Haga doble clic `<li>` .  El texto se resalta para indicar que el nodo está seleccionado.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-edit-attributes-highlighted.msft.png":::
       Editar el nodo  
    :::image-end:::  
    
1.  Presione la `Right` tecla de dirección, agregue un espacio, escriba `style="background-color:gold"` y, a continuación, seleccione `Enter` .  El color de fondo del nodo cambia a oro.  
    
    :::image type="complex" source="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-edit-attributes-inline-css.msft.png":::
       Agregar un `style` atributo al nodo  
    :::image-end:::  
    
### Editar tipo de nodo  

Para editar el tipo de un nodo, haga doble clic en el tipo y, a continuación, escriba el nuevo tipo.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **Editar tipo de nodo**, haga clic con el botón derecho en **Hank** y elija **inspeccionar**.  
    1.  Haga doble clic `<li>` .  `li`Se resalta el texto.  
    1.  Eliminar `li` , escriba `button` y, a continuación, seleccione `Enter` .  El `<li>` nodo cambia a un `<button>` nodo.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-edit-node-type-button.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-edit-node-type-button.msft.png":::
           Cambiar el tipo de nodo a `button`  
        :::image-end:::  
        
### Reordenar los nodos DOM  

Arrastre los nodos para reordenarlos.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **Reordenar los nodos DOM**, haga clic con el botón derecho en **Elvis Presley** y elija **inspeccionar**.  
    
    > [!NOTE]
    > Es el último elemento de la lista.  
    
    1.  En el árbol DOM, arrastre `<li>Elvis Presley</li>` hasta la parte superior de la lista.  
        
        :::image type="complex" source="../media/dom-elements-reorder-dom-nodes.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-reorder-dom-nodes.msft.png":::
           Arrastre el nodo a la parte superior de la lista  
        :::image-end:::  
        
### Estado de fuerza  

Puede obligar a que los nodos permanezcan en Estados incluidos `:active` ,, `:hover` `:focus` , `:visited` y `:focus-within` .  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **Estado de fuerza**, desplace el puntero sobre **el Señor de la vuela**.  El color de fondo se convierte en naranja.  
    1.  Haga clic con el botón derecho en **el Señor de la vuela** y elija **inspeccionar**.  
    1.  Haga clic con el botón derecho `<li class="demo--hover">The Lord of the Flies</li>` y elija **Estado de fuerza**  >  **: mantener**el mouse.  Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no ve esta opción.  El color de fondo sigue siendo naranja aunque no se esté colocando el puntero sobre el nodo.  

### Ocultar un nodo  

Seleccione esta opción `H` para ocultar un nodo.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **ocultar un nodo**, elija **las estrellas mi destino** y elija **inspeccionar**.  
    1.  Presione la `H` tecla.  El nodo está oculto.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-hide-a-node.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-hide-a-node.msft.png":::
           El aspecto del nodo en el árbol DOM después de ocultarlo  
        :::image-end:::  
        
    1.  `H`Vuelva a presionar la tecla.  Se vuelve a mostrar el nodo.  

### Eliminar un nodo  

Seleccione esta `Delete` para eliminar un nodo.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **eliminar un nodo**, elija **Fundación** y elija **inspeccionar**.  
    1.  Presione la `Delete` tecla.  Se elimina el nodo.  
    1.  Seleccione `Control` + `Z` \ (Windows, Linux \) o `Command` + `Z` \ (MacOS \).  La última acción se deshará y el nodo reaparecerá.  

## Nodos de acceso en la consola  

DevTools proporciona algunos métodos abreviados para acceder a los nodos DOM desde la consola o para obtener referencias de JavaScript a cada uno de ellos.  

### Hacer referencia al nodo actualmente seleccionado con $0  

Al inspeccionar un nodo, el `== $0` texto que se encuentra junto al nodo significa que puede hacer referencia a este nodo en la consola con la variable `$0` .  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **referencia el nodo seleccionado actualmente con $0**, seleccione con el botón derecho **la oscuridad hacia la izquierda** y elija **inspeccionar**.  
    1.  Presione la `Escape` tecla para abrir el cajón de consola.  
    1.  Escriba `$0` y presione la `Enter` tecla.  El resultado de la expresión muestra que `$0` se evalúa `<li>The Left Hand of Darkness</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png":::
            El resultado de la primera `$0` expresión en la **consola**  
        :::image-end:::  
        
    1.  Desplace el puntero sobre el resultado.  El nodo se resalta en la ventanilla.  
    1.  Haga clic `<li>Dune</li>` en el árbol DOM, escriba `$0` la consola de nuevo y, a continuación, vuelva a seleccionar `Enter` .  Ahora, `$0` evalúa a `<li>Dune</li>` .  
        
        :::image type="complex" source="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png":::
           Resultado de la segunda `$0` expresión en la **consola**  
        :::image-end:::  
        
### Almacenar como variable global  

Si necesita hacer referencia a un nodo varias veces, almacénelo como una variable global.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **almacenar como variable global**, elija la opción **suspender** y elija **inspeccionar**.  
    1.  Haga clic con el botón derecho `<li>The Big Sleep</li>` en el árbol DOM y elija **almacenar como variable global**.  Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no ve esta opción.  
    1.  Escriba `temp1` la consola y, a continuación, seleccione `Enter` .  El resultado de la expresión muestra que la variable se evalúa en el nodo.  
        
        :::image type="complex" source="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png":::
           El resultado de la `temp1` expresión  
        :::image-end:::  
        
### Copiar ruta JS  

Copie la ruta de acceso de JavaScript en un nodo cuando necesite hacer referencia a él en una prueba automatizada.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **copiar JS path**, haga clic con el botón derecho en **el Karamazov de Brothers** y elija **inspeccionar**.  
    1.  Haga clic con el botón derecho `<li>The Brothers Karamazov</li>` en el árbol DOM y elija **copiar**  >  **ruta JS**.  Una `document.querySelector()` expresión que se resuelve en el nodo se ha copiado en el portapapeles.  
    1.  Seleccione `Control` + `V` \ (Windows, Linux \) o `Command` + `V` \ (MacOS \) para pegar la expresión en la consola.  
    1.  Seleccione `Enter` para evaluar la expresión.
        
        :::image type="complex" source="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png":::
           Resultado de la expresión de **ruta de copia JS**  
        :::image-end:::  
        
## Interrupción en cambios de DOM  

DevTools le permite pausar el JavaScript de una página cuando el JavaScript modifica el DOM.  

### Interrupciones en las modificaciones de atributos  

Use puntos de interrupción de modificación de atributos cuando desee pausar el código JavaScript que hace que los atributos de un nodo cambien.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **interrupción en las modificaciones de atributos**, elija **sauerkraut** y elija **inspeccionar**.  
    1.  En el árbol DOM, haga clic con el botón derecho `<li id="target">Sauerkraut</li>` y elija **interrumpir en**las  >  **modificaciones de atributos**.  Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.
        
        :::image type="complex" source="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png":::
           **Interrupciones en las modificaciones de atributos**  
        :::image-end:::  
        
    1.  En el siguiente paso, se le indicará que haga clic en un botón que pausa el código de la página.  Una vez que la página se haya pausado, ya no podrás desplazarse por la página.  Debe elegir **reanudar script** \ ( ![ resume script ][ImageResumeScriptIcon] \) para que la página se vuelva a desplazar.
        
        :::image type="complex" source="../media/dom-break-attribute-modifications-sources-paused-on.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-break-attribute-modifications-sources-paused-on.msft.png":::
           Dónde reanudar la secuencia de comandos que se ejecuta  
        :::image-end:::  
        
    1.  Haga clic en el botón **establecer fondo** de arriba.  Esto establece el `style` atributo del nodo en `background-color:thistle` .  DevTools pausa la página y resalta el código que hizo que el atributo cambie.  
    1.  Elija **reanudar script** \ ( ![ resume script ][ImageResumeScriptIcon] \), como se mencionó anteriormente.  
    
### Interrupción en eliminación de nodo  

Si desea hacer una pausa cuando se quita un nodo en particular, use los puntos de interrupción de eliminación de nodos.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **interrumpir en la eliminación del nodo**, seleccione **Neuromancer** y elija **inspeccionar**.  
    1.  En el árbol DOM, haga clic con el botón derecho `<li id="target">Neuromancer</li>` y elija **interrumpir**  >  **eliminación de nodo**.  Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.  
    1.  Haga clic en el botón **eliminar** .  DevTools pausa la página y resalta el código que ha provocado la eliminación del nodo.  
    1.  Elija **resume script** \ ( ![ resume script ][ImageResumeScriptIcon] \).  
    
### Saltos en las modificaciones del subárbol  

Después de poner un punto de interrupción de modificación de un subárbol en un nodo, DevTools hace una pausa en la página cuando se agrega o se quita cualquiera de los descendientes del nodo.  

1.  [Abra ejemplos de Dom](#open-dom-examples).  
1.  En **interrupciones en las modificaciones de subárbol**, elija la opción de **incendio** y elija **inspeccionar**.  
    1.  En el árbol DOM, haga clic con el botón derecho `<ul id="target">` , que es el nodo de arriba `<li>A Fire Upon the Deep</li>` y elija **interrumpir en**las  >  **modificaciones del subárbol**.  Consulte el [Apéndice: opciones que faltan](#appendix-missing-options) si no puede ver esta opción.  
    1.  Elija **Agregar hijo**.  El código se detiene porque `<li>` se ha agregado un nodo a la lista.  
    1.  Elija **resume script** \ ( ![ resume script ][ImageResumeScriptIcon] \).  
    
## Pasos siguientes  

Que cubre la mayoría de las características relacionadas con DOM de DevTools.  Puede descubrir el resto de ellos haciendo clic con el botón secundario en los nodos del árbol DOM y experimentando con las otras opciones que no se han descrito en este tutorial.  Consulte también [métodos abreviados de teclado del panel elementos][DevToolsShortcutsElements].  

Visite la [Página principal de Microsoft Edge DevTools][MicrosoftEdgeDevTools] para descubrir todo lo que pueda hacer con DevTools.  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  

## Apéndice: HTML frente a DOM  

En la siguiente sección se explica rápidamente la diferencia entre HTML y DOM.  

:::row:::
   :::column span="":::
      Cuando se usa un explorador Web para solicitar una página, el servidor devuelve HTML como el siguiente fragmento de código.  

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
      El explorador analiza el código HTML y crea un árbol de objetos como la siguiente lista.  
      
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

Este árbol de objetos, o nodos, que representa el contenido de la página, se denomina DOM.  

:::row:::
   :::column span="":::
      Ahora es lo mismo que el código HTML, pero Supongamos que la secuencia de comandos a la que se hace referencia en la parte inferior del HTML ejecuta el siguiente fragmento de código.  
      
      ```javascript
      const h1 = document.querySelector('h1');
      h1.parentElement.removeChild(h1);
      const p = document.createElement('p');
      p.textContent = 'Wildcard!';
      document.body.appendChild(p);
      ```  
   :::column-end:::
   :::column span="":::
      Ese código quita el `h1` nodo y agrega otro `p` nodo al Dom.  El DOM completo ahora muestra la siguiente lista.  
      
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

El código HTML de la página es ahora diferente al del DOM.  En otras palabras, HTML representa el contenido inicial de la página y DOM representa el contenido de la página actual.  Cuando JavaScript agrega, quita o modifica nodos, el DOM es diferente del HTML.  

Para obtener más información, consulta [Introducción al Dom][MDNIntroductionToDOM] .  

<!--
## Appendix: Scroll into view  

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and choose **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    :::image type="complex" source="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png":::
       Scroll into view  
    :::image-end:::  
    -->  

## Apéndice: opciones perdidas  

Muchas de las instrucciones de este tutorial le indican que debe hacer clic con el botón secundario del mouse en un nodo del árbol DOM y, a continuación, seleccionar una opción en el menú contextual que aparece.  Si no ve la opción especificada en el menú contextual, intente hacer clic con el botón secundario del ratón fuera del texto del nodo.  

:::image type="complex" source="../media/dom-elements-highlighted-right-click-right-side.msft.png" alt-text="Inspeccionar un nodo" lightbox="../media/dom-elements-highlighted-right-click-right-side.msft.png":::
   Dónde hacer clic si no ve todas las opciones  
:::image-end:::  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageInspectIcon]: ../media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: ../media/resume-script-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas de desarrollador de Microsoft Edge \ (cromo \) | Microsoft docs"  
[DevToolsCssGetStarted]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevToolsShortcutsElements]: ../shortcuts.md#elements-panel-keyboard-shortcuts "Métodos abreviados de teclado del panel elementos-métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft docs"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Ejemplo de DOM de DevTools Microsoft Edge (cromo) | Intento"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/dom/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
