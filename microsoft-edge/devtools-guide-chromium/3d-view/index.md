---
description: Todo sobre la vista 3D y cómo usarla.
title: Vista 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203973"
---
# Vista 3D  

Use la **vista 3D** para depurar la aplicación web desplazándose por el [modelo de objetos de documento (dom)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z][MDNZIndex] .  Con ella, puede completar las siguientes tareas.  

*   [Explorar la Página Web traducida a una perspectiva 3D](#3d-dom)  
*   [Depuración basada en el contexto de apilamiento de índice z](#z-index)  
*   [Obtener acceso a la funcionalidad de la herramienta capas desde la vista 3D con capas compuestas](#composited-layers)  
*   [Borrar parte del desorden en el panel Dom o en](#changing-your-view) el [Panel de índice z](#change-the-scope-of-your-exploration)  
*   [Elegir la combinación de colores para la mejor depuración de problemas de Dom](#dom-color-type) o [de índice z](#z-index-color-type)  

Si desea explorar un prototipo temprano de proyecto de vista 3D y ejecutar el código usted mismo, vaya a [muestra de vista 3D][GithubMicrosoftedgeDevtoolssamples3dview].  

En el lado izquierdo, hay tres paneles que puede usar para su experiencia de depuración.  

*   El panel [Índice Z](#z-index) .  Navegue por los diferentes elementos de la aplicación web con el contexto de índice z en mente.  El panel **Índice Z** es el panel predeterminado.  
*   El panel [3D Dom](#3d-dom) .  Explore el DOM como un todo con todos los elementos accesibles fácilmente.  Para obtener acceso al panel, elija el panel **Dom** situado junto al panel **Índice Z** .  
*   Panel [capas compuestas](#composited-layers) .  Agregue otro elemento 3D para crear una experiencia más completa desde una perspectiva de capas.  Para obtener acceso al panel, seleccione el panel **capas compuestas** junto al panel **Dom** .  
    
En la parte derecha, el lienzo muestra las selecciones del [Índice Z](#z-index), del [Dom 3D](#3d-dom)o de las [capas compuestas](#composited-layers).  

## Navegar por el lienzo  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Lienzo de vista 3D" lightbox="../media/3d-view-canvas.msft.png":::
   Lienzo de vista 3D  
:::image-end:::  

### Accesos rápidos de teclado  

*   Girar el DOM: para girar horizontalmente, seleccione las `left-arrow` `right-arrow` teclas y.  Para girar verticalmente, seleccione las `up-arrow` `down-arrow` teclas y.  
*   Navegar por el DOM: para desplazarse por los elementos adyacentes, seleccione un elemento y seleccione las `up-arrow` `down-arrow` teclas y.  

### Controles del ratón  

*   Girar el DOM: elija y arrastre alrededor del espacio del lienzo.  
*   Desplácese por el DOM: Abra el menú contextual \ (haga clic con el botón secundario del ratón) y arrastre en la dirección en la que desea que se mueva el DOM.  
*   Zoom: arrastre dos dedos por el panel táctil o use la rueda de desplazamiento del mouse.  

### Controles en pantalla  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Controles en pantalla" lightbox="../media/3d-view-controls-small.msft.png":::
   Controles en pantalla  
:::image-end:::  

*   Restablezca la vista de lienzo a la vista original: seleccione el botón **restablecer cámara** o elija el botón **restablecer elementos en la vista y volver a centrar la cámara** \ (en el icono de actualización de un lado).  
*   Actualice el lienzo \ (por ejemplo, si el explorador cambió o cambió a una vista emulador de dispositivos \): elija el botón volver a **tomar instantánea** o elija el botón **tomar nueva instantánea** \ (icono Actualizar \).  

## Índice Z  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Vista de índice Z" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Vista de índice Z  
:::image-end:::  

Mientras que el panel **Índice Z** tiene características compartidas con el panel **3D Dom** , los paneles siguen teniendo elementos que son únicos para el panel.  

### Resaltar elementos con contexto de apilamiento  

La configuración **resaltar elementos con el contexto de apilamiento** permite activar las etiquetas de índice z de los elementos del lienzo \ (y desactivar \).  La casilla de verificación está seleccionada de forma predeterminada.  

### Cambiar el ámbito de exploración  

El botón **Mostrar todos los elementos** es la manera más rápida de Mostrar todos los elementos del DOM después de cambiar la configuración que está debajo.  

El botón **Mostrar solo los elementos con el contexto de apilamiento** quita elementos sin contexto de apilamiento y alisa el Dom para facilitar la navegación.  

El botón **aislar elemento seleccionado** es esencialmente tres botones en uno.  Hay dos casillas debajo del botón **aislar elemento seleccionado** : la casilla **Mostrar todos los padres** y **mantener solo los padres con la casilla de verificación de nuevo contexto de apilamiento** .  

La casilla **Mostrar todos los padres** está activada de forma predeterminada.  Para mostrar el elemento y los elementos primarios en el lienzo, seleccione un elemento y elija el botón **aislar elemento seleccionado** .  

Para mostrar el elemento y los padres que tienen un nuevo contexto de apilamiento en el lienzo, active la opción **conservar solo los padres con el nuevo contexto de apilamiento** y seleccione el botón **aislar elemento seleccionado** .  

Para mostrar el elemento que ha elegido en el lienzo, desactive la configuración y elija el botón **aislar elemento seleccionado** .  

En la parte inferior del panel **3D Dom** , ubique los **elementos ocultos con el mismo orden de pintura que** la casilla principal.  Al seleccionar y anular la selección de la casilla, se renuevan los elementos según su elección.  Si se elige, los elementos que comparten el orden de pintura se acoplan al elemento primario.  

Las opciones pretenden borrar algunos de los desordens que las páginas web más complejas crean en el lienzo.  

### Tipo de color de índice Z  

Las son las diferentes visualizaciones que puede usar para el DOM de su lienzo.  Independientemente de si lo usas para divertirse o porque las visualizaciones te ayudan a visualizar mejor el DOM, el DevTools tiene colorways diferentes y una opción **usar color de fondo** .  El panel **Índice Z** comparte el **púrpura** con el blanco y el **color de fondo** con el panel **3D Dom** .  Dado el elemento visual agregado de las etiquetas de índice z, los comentarios que llevaron a una reducción del número de opciones de color.  La nueva simplicidad mejora la experiencia de depuración de índice z.  Los botones de radio permiten alternar entre las opciones y seleccionar el tipo de color.  El tipo de color es el más adecuado para el proyecto o uno que le guste más.  

## DOM 3D  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="Vista DOM" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   Vista DOM  
:::image-end:::  

Si desea tomar más de una vista de depuración general, en lugar de la experiencia de índice z, el **Dom 3D** ofrece un aspecto general del DOM.  Dado que el contexto de índice z se elimina, DOM se apila de forma más estrecha y clara.  El panel **3D Dom** tiene una funcionalidad similar, pero hay algunos matices.  

### Cambiar la vista  

En el panel **3D Dom** , el botón **aislar elemento seleccionado** tiene las casillas de verificación incluir **elementos secundarios** e **incluir padres** .  Ambas casillas están activadas de forma predeterminada.  Esto significa que si elige el botón **aislar elemento seleccionado** después de elegir un elemento, el lienzo muestra el elemento elegido, los elementos primarios del elemento y los elementos secundarios del elemento.  Desactive la opción **incluir elementos secundarios** y seleccione de nuevo el botón **aislar elemento seleccionado** para mostrar el elemento elegido y los elementos primarios del elemento.  Si activa la opción **incluir elementos secundarios** y desactiva la opción **incluir padres** y, a continuación, elige el botón **aislar elemento seleccionado** , el lienzo muestra el elemento y los elementos secundarios.  Si desactiva la configuración y elige el botón **aislar elemento seleccionado** , el lienzo solo muestra el elemento que haya elegido previamente.  

Control deslizante en el panel de control denominado **nivel de anidamiento de la página** con un número al lado.  El número indica el número de capas del documento.  Si arrastra el control deslizante hacia la izquierda, las capas exteriores desaparecerán hasta que quede con un nivel de anidamiento establecido en `1` , que solo muestra el elemento posterior más lejano en el Dom.  Para quitar parte del desorden, arrastre el control deslizante.  Le ayuda a tener una visión más detallada de lo que sucede en los niveles inferiores.  

### Tipo de color DOM  

En el panel **3D Dom** se muestran las siguientes opciones.  

*   Tres colorways diferentes.  
    *   **Calor-púrpura a blanco**  
    *   **Calor: azul a amarillo**  
    *   **Calor: arco iris**  
*   **Usar color de fondo**  
*   **Usar textura de pantalla**  
    
La opción **usar textura de pantalla** agrega el contexto a la experiencia de depuración.  Muestra directamente el contenido de la página web en los elementos.  

## Capas compuestas

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   Panel **capas compuestas**
:::image-end:::  

El panel **capas compuestas** abre los elementos de la herramienta **capas** sin cambiar los contextos.  Aún puede acceder a los detalles de cada una de las capas y tener las **imágenes o los** **rects de desplazamiento lentos** .

## Contactar al equipo de Microsoft Edge DevTools  

El equipo de Microsoft Edge DevTools está trabajando en la interfaz de usuario y agregando más funciones a la vista 3D en función de los comentarios.  Envíe sus comentarios para ayudar a mejorar el DevTools de Microsoft Edge.  Seleccione el icono **Enviar comentarios** en la DevTools o seleccione `Alt` + `Shift` + `I` en Windows/Linux o `Option` + `Shift` + `I` en MacOS y escriba las solicitudes de comentarios o características que tenga para el DevTools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Vista 3D de Microsoft Edge DevTools-MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "índice z | MDN"  
