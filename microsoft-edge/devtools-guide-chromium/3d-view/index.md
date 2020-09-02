---
description: Todo sobre la vista 3D y cómo usarla.
title: Vista 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ba1125654c46be6ef4da99efc9ba027ba5e40672
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986083"
---
# Vista 3D  

Use la **vista 3D** para depurar la aplicación web desplazándose por el [modelo de objetos de documento (dom)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z][MDNZIndex] .  Con él podrás realizar las siguientes tareas:  

*   [Explorar la Página Web traducida a una perspectiva 3D](#3d-dom)  
*   [Depuración basada en el contexto de apilamiento de índice z](#z-index)  
*   [Borrar parte del desorden en el panel Dom o en](#changing-your-view) el [Panel de índice z](#change-the-scope-of-your-exploration)  
*   [Elegir la combinación de colores para la mejor depuración de problemas de Dom](#dom-color-type) o [de índice z](#z-index-color-type)  

Si desea explorar un prototipo temprano de proyecto de vista 3D y ejecutar el código usted mismo, consulte [muestra de vista 3D][GithubMicrosoftedgeDevtoolssamples3dview].   

En el lado izquierdo, hay dos paneles que puede usar para su experiencia de depuración.  

1.  El panel [Índice Z](#z-index) .  Desplácese por los distintos elementos de la aplicación web con el contexto de índice z en mente.  El panel **Índice Z** es el panel predeterminado.  
1.  El panel [3D Dom](#3d-dom) .  Explore el DOM como un todo con todos los elementos a su alcance.  Para obtener acceso al panel, seleccione en el panel **Dom** situado junto al panel **Índice Z** .  
    
En la parte derecha, el lienzo muestra las selecciones del [Índice Z](#z-index) o del [Dom 3D](#3d-dom).  

## Navegar por el lienzo  

:::image type="complex" source="../media/canvas.png" alt-text="Lienzo de vista 3D" lightbox="../media/canvas.png":::
   Lienzo de vista 3D  
:::image-end:::  

### Métodos abreviados de teclado  

*   Girar el DOM: para girar horizontalmente, presione las `left-arrow` `right-arrow` teclas y.  Para girar verticalmente, presione las `up-arrow` `down-arrow` teclas y.  
*   Navegar por el DOM: para desplazarse por los elementos adyacentes, seleccione un elemento y presione las `up-arrow` `down-arrow` teclas y.  

### Controles del ratón  

*   Girar el DOM: seleccione y arrastre alrededor del espacio del lienzo.  
*   Desplácese por el DOM: Abra el menú contextual \ (haga clic con el botón secundario del ratón) y arrastre en la dirección en la que desea que se mueva el DOM.  
*   Zoom: arrastre dos dedos por el panel táctil o use la rueda de desplazamiento del mouse.  

### Controles en pantalla  

:::image type="complex" source="../media/controls-small.png" alt-text="Controles en pantalla" lightbox="../media/controls-small.png":::
   Controles en pantalla  
:::image-end:::  

*   Restablezca la vista original en la vista de lienzo: seleccione el botón **restablecer la cámara** , o bien, seleccione el botón **restablecer elementos en la vista y vuelva a centrar la cámara** \ (en el icono de actualización lateral \).  
*   Actualice el lienzo \ (por ejemplo, si el explorador cambió o cambió a una vista emulador de dispositivos \): seleccione el botón volver a **tomar instantánea** o seleccione el botón **tomar nueva instantánea** \ (icono Actualizar \).  

## Índice Z  

:::image type="complex" source="../media/z-index-view-box.png" alt-text="Vista de índice Z" lightbox="../media/z-index-view-box.png":::
   Vista de índice Z  
:::image-end:::  

Mientras que el panel **Índice Z** tiene características compartidas con el panel **3D Dom** , los paneles siguen teniendo elementos que son únicos para el panel.  

### Resaltar elementos con contexto de apilamiento  

La configuración **resaltar elementos con el contexto de apilamiento** permite activar las etiquetas de índice z de los elementos del lienzo \ (y desactivar \).  La casilla está seleccionada de forma predeterminada.  

### Cambiar el ámbito de exploración  

El botón **Mostrar todos los elementos** es la forma más rápida de Mostrar todos los elementos del DOM después de cambiar la configuración a continuación.  

El botón **Mostrar solo los elementos con el contexto de apilamiento** quita elementos sin contexto de apilamiento y alisa el Dom para facilitar la navegación.  

El botón **aislar elemento seleccionado** es esencialmente tres botones en uno.  Hay dos casillas debajo del botón **aislar elemento seleccionado** : la casilla **Mostrar todos los padres** y **mantener solo los padres con la casilla de verificación de nuevo contexto de apilamiento** .  

La casilla **Mostrar todos los padres** está seleccionada de forma predeterminada.  Si selecciona un elemento en el panel de lienzo y selecciona el botón de **elemento seleccionado** , el lienzo solo muestra el elemento y los elementos primarios.  

Si selecciona la casilla **mantener solo los padres con el nuevo contexto de apilamiento** y selecciona el botón **aislar elemento seleccionado** , el lienzo solo muestra el elemento y los elementos primarios que tienen un nuevo contexto de apilamiento.  

Si anula la selección de las casillas de verificación y selecciona el botón de **elemento seleccionado** , el lienzo solo muestra el elemento que haya elegido en primer lugar.  

En la parte inferior del panel **Dom 3D** , ubique los **elementos ocultos con el mismo orden de pintura que** la casilla principal.  Al seleccionar y anular la selección de la casilla, se actualizan los elementos en función de la selección.  Si se selecciona, los elementos que comparten el orden de pintura se acoplan al elemento primario.  

Las opciones pretenden borrar algunos de los desordens que las páginas web más complejas crean en el lienzo.  

### Tipo de color de índice Z  

Las son las diferentes visualizaciones que puede usar para el DOM de su lienzo.  Independientemente de si lo usas para divertirse o porque las visualizaciones te ayudan a visualizar mejor el DOM, la DevTools tiene tres colorways diferentes, así como una configuración de **color de fondo** .  Los botones de radio le permiten alternar entre las opciones y seleccionar el tipo de color más adecuado para el proyecto \ (o que le gusten más).  

## DOM 3D  

:::image type="complex" source="../media/dom-purple-box.png" alt-text="Vista DOM" lightbox="../media/dom-purple-box.png":::
   Vista DOM  
:::image-end:::  

Si desea tomar más de una vista de depuración general, en lugar de la experiencia de índice z, el **Dom 3D** ofrece un aspecto general del DOM.  Dado que el contexto de índice z se elimina, DOM se apila de forma más estrecha y clara.  El panel **3D Dom** tiene una funcionalidad similar, pero hay algunos matices.  

### Cambiar la vista  

En el panel **3D Dom** , el botón **aislar elemento seleccionado** tiene las casillas de verificación incluir **elementos secundarios** e **incluir padres** .  De forma predeterminada, se seleccionan las dos casillas, lo que significa que al seleccionar el botón **aislar elemento seleccionado** después de seleccionar un elemento en el lienzo, se mostrará el elemento elegido, los elementos primarios del elemento y los elementos secundarios del elemento.  Si se anula la selección de la casilla de verificación **incluir hijos** y se vuelve a seleccionar el botón **aislar elemento seleccionado** , se mostrará el elemento seleccionado y los elementos primarios del elemento.  Si selecciona la casilla **incluir hijos** y desmarca la casilla **incluir padres** antes de seleccionar el botón **aislar elemento seleccionado** , el lienzo muestra el elemento y los elementos secundarios.  Si desmarca las casillas de verificación y selecciona el botón **aislar elemento seleccionado** , el lienzo solo muestra el elemento que seleccionó previamente.  

Un control deslizante en el panel de control titulado **nivel de anidamiento para la página** con un número al lado.  El número indica el número de capas del documento.  Si arrastra el control deslizante hacia la izquierda, las capas exteriores desaparecerán hasta que quede con un nivel de anidamiento establecido en 1, que solo muestra el elemento posterior más lejano en el DOM.  Arrastrar el control deslizante le permite quitar algunos de los desorden si está intentando obtener más información sobre lo que sucede en los niveles inferiores.  

### Tipo de color DOM  

Además de los botones de **calor-púrpura a blanco**, **calor-azul a amarillo**, **calor-arco iris**y **usar color de fondo** , se **usa la textura**de la pantalla.  La textura de la pantalla agrega el contexto a la experiencia de depuración mostrando el contenido de la página web directamente en los elementos.  En el panel **Dom 3D** , la configuración de  **tipo de color** sigue siendo un trabajo en curso, ya que algunos sitios web tienen una textura de pantalla de procesamiento de tiempo más difícil en la vista 3D.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools

El equipo de Microsoft Edge DevTools está trabajando en la interfaz de usuario y agregando más funciones a la vista 3D basándose en las preguntas de los usuarios como usted.  Envíanos tus comentarios para ayudar a mejorar la DevTools de Microsoft Edge.  Simplemente selecciona el icono de comentarios en la DevTools o pulsa `Alt` + `Shift` + `I` \ (Windows \) o pulsa `Option` + `Shift` + `I` \ (MacOS \) e introduce las solicitudes de comentarios o características para el DevTools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Vista 3D de Microsoft Edge DevTools-MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "índice z | MDN"  
