---
description: Todo sobre la vista 3D y cómo usarla.
title: Vista 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 5e218b24fb21fcfa9c82b99f17373fed1ba5a21c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "11203973"
---
# <a name="3d-view"></a>Vista 3D  

Use la **Vista 3D** para depurar la aplicación web navegando por el [Document Object Model (DOM)][MDNDocumentObjectModel] o el contexto de apilamiento [índice z][MDNZIndex].  Con ella, puede completar las siguientes tareas.  

*   [Explorar la página web traducida a una perspectiva 3D](#3d-dom)  
*   [Depuración basada en el contexto de apilamiento índice z](#z-index)  
*   [Acceso a la funcionalidad de la herramienta Capas desde la Vista 3D con capas compuestas](#composited-layers)  
*   [Borrar parte del desorden en el panel del DOM](#changing-your-view) o el [panel de índice z](#change-the-scope-of-your-exploration)  
*   [Elija la combinación de colores para depurar mejor los problemas de DOM](#dom-color-type) o [problemas de índice Z](#z-index-color-type)  

Si desea explorar un prototipo inicial del proyecto de Vista 3D y ejecutar el código usted mismo, vaya a [Ejemplo de Vista 3D][GithubMicrosoftedgeDevtoolssamples3dview].  

En el lado izquierdo, hay tres paneles que puede usar para la experiencia de depuración.  

*   El panel de [índice Z](#z-index).  Navegue por los distintos elementos de la aplicación web teniendo en cuenta el contexto de índice z.  El panel de **índice z** es el panel predeterminado.  
*   El panel de [DOM 3D](#3d-dom).  Explore el DOM como un todo con todos los elementos fácilmente accesibles.  Para acceder al panel, elija el panel **DOM** situado junto al panel de **índice Z**.  
*   El panel [Capas compuestas](#composited-layers).  Agregue otro elemento 3D para crear una experiencia más completa desde una perspectiva de capas.  Para acceder al panel, elija el panel **Capas compuestas** junto al panel **DOM**.  
    
En el lado derecho, el lienzo muestra las selecciones de [índice Z](#z-index), [DOM 3D](#3d-dom) o [Capas compuestas](#composited-layers).  

## <a name="navigating-the-canvas"></a>Navegar por el lienzo  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Lienzo de vista 3D" lightbox="../media/3d-view-canvas.msft.png":::
   Lienzo de vista 3D  
:::image-end:::  

### <a name="keyboard-shortcuts"></a>Accesos rápidos de teclado  

*   Girar el DOM:  para girar horizontalmente, seleccione las teclas `left-arrow` y `right-arrow`.  Para girar verticalmente, seleccione las teclas `up-arrow` y `down-arrow`.  
*   Navegar por el DOM:  para desplazarse por los elementos adyacentes, elija un elemento y seleccione las teclas `up-arrow` y `down-arrow`.  

### <a name="mouse-controls"></a>Controles del mouse  

*   Girar el DOM:  elija y arrastre alrededor del espacio de lienzo.  
*   Desplazarse por el DOM:  abra el menú contextual \(clic con el botón derecho\) y arrástrelo en la dirección en la que desea que se mueva el DOM.  
*   Zoom:  arrastre dos dedos por el panel táctil o use la rueda de desplazamiento del mouse.  

### <a name="on-screen-controls"></a>Controles en pantalla  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Controles en pantalla" lightbox="../media/3d-view-controls-small.msft.png":::
   Controles en pantalla  
:::image-end:::  

*   Restablecer la vista de lienzo a la vista original:  elija el botón **Restablecer cámara** o elija el botón **Restablecer elementos en la vista y volver a centrar la cámara** \(icono de actualización lateral\).  
*   Actualice el lienzo \(por ejemplo, si el explorador cambió o usted está en una vista del emulador de dispositivo\): elija el botón **Repetir instantánea** o elija el botón **Tomar nueva instantánea** \(icono actualizar\).  

## <a name="z-index"></a>Índice Z  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Vista de índice Z" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Vista de índice Z  
:::image-end:::  

Aunque el panel de **índice Z** tiene características compartidas con el panel **DOM 3D**, los paneles siguen teniendo elementos únicos para sí mismos.  

### <a name="highlight-elements-with-stacking-context"></a>Resaltar elementos con contexto de apilamiento  

La configuración **Resaltar elementos con contexto de apilamiento** permite activar \(y desactivar\) las etiquetas de índice z para los elementos del lienzo.  La casilla está establecida de manera predeterminada  

### <a name="change-the-scope-of-your-exploration"></a>Cambiar el ámbito de la exploración  

El botón **Mostrar todos los elementos** es la forma más rápida de mostrar todos los elementos del DOM después de cambiar la configuración debajo de él.  

El botón **Mostrar solo los elementos con contexto de apilamiento** quita los elementos sin contexto de apilamiento y aplana el DOM para facilitar la navegación.  

El botón **Aislar el elemento seleccionado** es básicamente tres botones en uno.  Hay dos casillas debajo del botón **Aislar el elemento seleccionado**:  la casilla **Mostrar todos los elementos primarios** y la casilla **Mantener solo los elementos primarios con nuevo contexto de apilamiento**.  

La casilla **Mostrar todos los elementos primarios** está activada de manera predeterminada.  Para mostrar el elemento y otros elementos primarios en el lienzo, elija un elemento y el botón **Aislar el elemento seleccionado**.  

Para mostrar el elemento y los elementos primarios que tienen un nuevo contexto de apilamiento en el lienzo, active la opción **Mantener solo los elementos primarios con nuevo contexto de apilamiento** y elija el botón **Aislar el elemento seleccionado**.  

Para mostrar el elemento que eligió en el lienzo, desactive la configuración y elija el botón **Aislar el elemento seleccionado**.  

En la parte inferior del panel **DOM 3D**, busque la casilla **Ocultar elementos con el mismo orden de pintura que su elemento primario**.  Al elegir y anular la selección de la casilla, se actualizarán los elementos en función de su elección.  Si se elige, los elementos que comparten el orden de pintura se aplanan al elemento primario.  

Las opciones están diseñadas para borrar parte del desorden que crean las páginas web más complejas en el lienzo.  

### <a name="z-index-color-type"></a>Tipo de color de índice Z  

Estas son las distintas visualizaciones que puede usar para el DOM en el lienzo.  Tanto si lo usa para diversión o porque las visualizaciones le ayudan a observar mejor el DOM, las DevTools tiene diferentes colores y una opción de **Usar el color de fondo**.  El panel **índice Z** comparte el de **Púrpura a blanco** y el de **Color de fondo** con el panel **DOM 3D**.  Dado el elemento visual agregado de las etiquetas de índice z, sus comentarios han llevado a reducir el número de opciones de color.  La nueva simplicidad mejora la experiencia de depuración del índice Z.  Los botones de radio le permiten alternar entre las opciones y elegir el tipo de color.  El tipo de color es el más adecuado para el proyecto o uno que más le guste.  

## <a name="3d-dom"></a>DOM 3D  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="Vista DOM" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   Vista DOM  
:::image-end:::  

Si desea obtener más de una vista de depuración general, en lugar de la experiencia de índice z, el **DOM 3D** proporciona un aspecto general del DOM.  Al eliminar contexto de índice z, el DOM se apila de forma más estrecha y limpia.  El panel **DOM 3D** tiene una funcionalidad similar, pero hay algunos matices.  

### <a name="changing-your-view"></a>Cambiar la vista  

En el panel **DOM 3D**, el botón **Aislar el elemento seleccionado** tiene las casillas **Incluir elementos secundarios** e **Incluir elementos primarios**.  Ambas casillas están activadas de manera predeterminada.  Esto significa que si elige el botón **Aislar elemento seleccionado** después de elegir un elemento, el lienzo muestra el elemento elegido, los elementos primarios y los elementos secundarios del elemento.  Desactive la opción **Incluir elementos secundarios** y elija de nuevo el botón **Aislar el elemento seleccionado** para mostrar el elemento elegido y sus elementos primarios.  Si activa la opción **Incluir elementos secundarios**, y desactiva la opción **Incluir elementos primarios** y, a continuación, elige el botón **Aislar el elemento seleccionado**, el lienzo muestra el elemento y sus elementos secundarios.  Si desactiva ambas opciones y elige el botón **Aislar el elemento seleccionado**, el lienzo solo muestra el elemento que eligió anteriormente.  

Un control deslizante en el panel de control denominado **Nivel de anidamiento para la página** con un número junto a él.  El número indica el número de capas del documento.  Si arrastra el control deslizante a la izquierda, las capas más externas se despegarán hasta que quede con un nivel de anidamiento establecido en `1`, que muestra solo el elemento posterior más alejado del DOM.  Para quitar parte del desorden, arrastre el control deslizante.  Esto le ayudará a ver más de cerca lo que sucede en los niveles inferiores.  

### <a name="dom-color-type"></a>Tipo de color DOM  

El panel **DOM 3D** muestra las siguientes opciones.  

*   Tres colores diferentes.  
    *   **Mapa térmico: púrpura a blanco**  
    *   **Mapa térmico: azul a amarillo**  
    *   **Mapa térmico: arco iris**  
*   **Usar color de fondo**  
*   **Usar textura de pantalla**  
    
La opción **Usar textura de pantalla** agrega contexto a su experiencia de depuración.  Muestra directamente el contenido de la página web en los elementos.  

## <a name="composited-layers"></a>Capas compuestas

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   Panel **Capas compuestas**
:::image-end:::  

El panel **Capas compuestas** abre los elementos de la herramienta **Capas** sin cambiar los contextos.  Puede seguir teniendo acceso a los detalles de cada una de las capas y tener **Rectángulos de desplazamiento lento** y **Paint**.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

El equipo de Microsoft Edge Devtools está trabajando en la interfaz de usuario y agregando más funcionalidad a la vista 3D de acuerdo a sus comentarios.  Envíe sus comentarios para ayudar a mejorar las DevTools de Microsoft Edge.  Elija el icono **Enviar comentarios** en DevTools o seleccione `Alt`+`Shift`+`I` en Windows/Linux o `Option`+`Shift`+`I` en macOS y escriba los comentarios o solicitudes de características que tenga para las DevTools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Vista 3D de DevTools de Microsoft Edge: MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-index | MDN"  
