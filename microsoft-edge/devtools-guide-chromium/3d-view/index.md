---
description: Todo acerca de la vista 3D y cómo usarla.
title: Vista 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 5e218b24fb21fcfa9c82b99f17373fed1ba5a21c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "11203973"
---
# <a name="3d-view"></a>Vista 3D  

Use la **vista 3D** para depurar la aplicación web navegando por el modelo de objetos de documento [(DOM)][MDNDocumentObjectModel] o el contexto de apilamiento [de índice z.][MDNZIndex]  Con él, puede completar las siguientes tareas.  

*   [Explorar la página web traducida a una perspectiva 3D](#3d-dom)  
*   [Depuración basada en el contexto de apilamiento de índice z](#z-index)  
*   [Acceder a la funcionalidad de la herramienta Capas desde la vista 3D con capas compuestas](#composited-layers)  
*   [Borrar parte del desorden en el panel DOM](#changing-your-view) o en el panel de índice [z](#change-the-scope-of-your-exploration)  
*   [Elegir la combinación de colores para depurar mejor los problemas dom o](#dom-color-type) los problemas de índice [z](#z-index-color-type)  

Si desea explorar un prototipo anticipado del proyecto de vista 3D y ejecutar el código usted mismo, vaya a [Muestra de vista 3D][GithubMicrosoftedgeDevtoolssamples3dview].  

En el lado izquierdo, hay tres paneles que puede usar para la experiencia de depuración.  

*   Panel [de índice Z.](#z-index)  Navegue por los diferentes elementos de la aplicación web con el contexto de índice z en mente.  El **panel de índice Z** es el panel predeterminado.  
*   Panel [DOM 3D.](#3d-dom)  Explore el DOM en su conjunto con todos los elementos fácilmente accesibles.  Para obtener acceso al panel, elija el panel **DOM** junto al panel **de índice Z.**  
*   Panel [Capas compuestas.](#composited-layers)  Agregue otro elemento 3D para crear una experiencia más completa desde una perspectiva de capas.  Para obtener acceso al panel, elija el panel **Capas compuestas** junto al **panel DOM.**  
    
En el lado derecho, el lienzo muestra las selecciones de las capas [Z-index](#z-index), [3D DOM](#3d-dom)o [Composited .](#composited-layers)  

## <a name="navigating-the-canvas"></a>Navegar por el lienzo  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Lienzo de vista 3D" lightbox="../media/3d-view-canvas.msft.png":::
   Lienzo de vista 3D  
:::image-end:::  

### <a name="keyboard-shortcuts"></a>Accesos rápidos de teclado  

*   Girar el DOM: para girar horizontalmente, seleccione las `left-arrow` teclas `right-arrow` y.  Para girar verticalmente, seleccione las `up-arrow` teclas `down-arrow` y.  
*   Navegar por el DOM: para desplazarse por los elementos adyacentes, elija un elemento y seleccione las `up-arrow` teclas `down-arrow` y.  

### <a name="mouse-controls"></a>Controles de mouse  

*   Girar el DOM: elija y arrastre alrededor del espacio del lienzo.  
*   Desplazarse por el DOM: abra el menú contextual \(hacer clic con el botón secundario\) y arrastre en la dirección en la que desea que se mueva el DOM.  
*   Zoom: arrastre dos dedos a través del panel táctil o use la rueda de desplazamiento del mouse.  

### <a name="on-screen-controls"></a>Controles en pantalla  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Controles en pantalla" lightbox="../media/3d-view-controls-small.msft.png":::
   Controles en pantalla  
:::image-end:::  

*   Restablecer la vista de lienzo a **** la vista original: elija el botón Restablecer cámara o elija el botón Restablecer elementos en la vista y vuelva a centrar la cámara **\(icono** de actualización lateral\).  
*   Actualice el lienzo \(por ejemplo, si el explorador cambió o cambió a una vista **** del emulador de dispositivo\): Elija el botón **Recaptación** de instantáneas o elija el botón Tomar nueva instantánea \(icono de actualización\).  

## <a name="z-index"></a>Índice Z  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Vista de índice Z" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Vista de índice Z  
:::image-end:::  

Aunque el **panel de índice Z** tiene características compartidas con el panel DOM **3D,** los paneles aún tienen elementos que son únicos para el panel.  

### <a name="highlight-elements-with-stacking-context"></a>Resaltar elementos con contexto de apilamiento  

La **configuración Resaltar elementos** con contexto de apilamiento permite activar \(y desactivar\) las etiquetas de índice z para los elementos del lienzo.  La casilla se elige de forma predeterminada.  

### <a name="change-the-scope-of-your-exploration"></a>Cambiar el ámbito de la exploración  

El **botón Mostrar todos los** elementos es la forma más rápida de mostrar todos los elementos del DOM después de cambiar la configuración debajo de él.  

El **botón Mostrar solo elementos con** contexto de apilamiento quita los elementos sin apilar el contexto y aplana el DOM para facilitar la navegación.  

El **botón Aislar elemento seleccionado** es básicamente tres botones en uno.  Hay dos casillas de verificación debajo **** del botón **Aislar** elemento seleccionado: la casilla Mostrar todos los elementos primarios y Mantener solo los elementos primarios con nuevo contexto **de apilamiento.**  

La **casilla Mostrar todos los padres** está activada de forma predeterminada.  Para mostrar el elemento y los elementos primarios en el lienzo, elija un elemento y elija el **botón Aislar elemento** seleccionado.  

Para mostrar el elemento y los elementos primarios que tienen **** un nuevo contexto de apilamiento en el lienzo, active la opción Mantener solo los elementos primarios con nuevo contexto de apilamiento y elija el botón Aislar elemento **seleccionado.**  

Para mostrar el elemento que eligió en el lienzo, desactive la configuración y elija **Aislar botón del elemento** seleccionado.  

En la parte inferior del panel **DOM 3D,** busque la casilla Ocultar elementos con el mismo orden de **pintura que su elemento** primario.  Al elegir y anular la selección de la casilla, se actualizan los elementos en función de su elección.  Si se elige, los elementos que comparten el orden de pintura se aplana al elemento primario.  

Las opciones están pensadas para borrar parte del desorden que las páginas web más complejas crean en el lienzo.  

### <a name="z-index-color-type"></a>Tipo de color de índice Z  

Son las diferentes visualizaciones que puede usar para el DOM en el lienzo.  Tanto si lo usas para la diversión como porque las visualizaciones te ayudan a visualizar mejor el DOM, las DevTools tienen diferentes colores y una **opción Usar color de fondo.**  El **panel de índice Z** comparte el color púrpura a **blanco** y el color **de fondo** con el panel **DOM 3D.**  Dado el elemento visual agregado de las etiquetas de índice z, los comentarios que llevaron a una reducción en el número de opciones de color.  La nueva simplicidad mejora la experiencia de depuración de índice z.  Los botones de radio permiten alternar entre las opciones y elegir el tipo de color.  El tipo de color es el más adecuado para el proyecto o el que más te gusta.  

## <a name="3d-dom"></a>DOM 3D  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="Vista DOM" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   Vista DOM  
:::image-end:::  

Si desea tener más de una vista de depuración general, en lugar de la experiencia de índice z, el **DOM 3D** ofrece una apariencia general del DOM.  Dado que se quita el contexto de índice z, el DOM se apila de forma más estrecha y limpia.  El **panel DOM 3D** tiene una funcionalidad similar, pero hay algunos matices.  

### <a name="changing-your-view"></a>Cambiar la vista  

En el **panel DOM 3D,** el botón **Aislar** elemento seleccionado tiene las casillas Incluir **elementos** secundarios e Incluir **elementos primarios.**  Ambas casillas están activadas de forma predeterminada.  Esto significa que si elige el botón **Aislar** elemento seleccionado después de elegir un elemento, el lienzo muestra el elemento elegido, los elementos primarios del elemento y los elementos secundarios del elemento.  Desactive la opción Incluir elementos **** **secundarios** y vuelva a elegir el botón Aislar elemento seleccionado para mostrar el elemento elegido y los elementos primarios del elemento.  Si activa la opción Incluir elementos **** secundarios y desactiva la **** opción Incluir elementos primarios y, a continuación, elige el botón Aislar elemento seleccionado, el lienzo muestra el elemento y los elementos secundarios. ****  Si desactivas ambas opciones y eliges el botón **Aislar** elemento seleccionado, el lienzo solo muestra el elemento que has elegido anteriormente.  

Un control deslizante en el panel de control denominado **Nivel de anidamiento para la** página con un número junto a él.  El número indica el número de capas del documento.  Al arrastrar el control deslizante hacia la izquierda, las capas más externas se pelan hasta que se deja un nivel de anidamiento establecido en , que muestra solo el elemento posterior más alejado del `1` DOM.  Para quitar parte del desorden, arrastre el control deslizante.  Te ayuda a conocer más de cerca lo que está sucediendo en los niveles inferiores.  

### <a name="dom-color-type"></a>Tipo de color DOM  

El **panel DOM 3D** muestra las siguientes opciones.  

*   Tres colores diferentes.  
    *   **Mapa de calor: púrpura a blanco**  
    *   **Mapa de calor: azul a amarillo**  
    *   **Mapa de calor: arco iris**  
*   **Usar color de fondo**  
*   **Usar textura de pantalla**  
    
La **opción Usar textura de** pantalla agrega contexto a la experiencia de depuración.  Muestra directamente el contenido de la página web en los elementos.  

## <a name="composited-layers"></a>Capas compuestas

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel de capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   Panel **Capas compuestas**
:::image-end:::  

El **panel Capas compuestas** abre los elementos de la **herramienta Capas** sin cambiar contextos.  Es posible que aún tenga acceso a **** los detalles de cada una de las capas y tenga los retrocesos de desplazamiento lento **y Paint**.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

El Microsoft Edge de Devtools está trabajando en la interfaz de usuario y agregando más funcionalidad a la vista 3D en función de los comentarios.  Envíe sus comentarios para ayudar a mejorar el Microsoft Edge DevTools.  Elija el **icono Enviar** comentarios en DevTools o seleccione en Windows/Linux o en macOS e introduzca los comentarios o solicitudes de características que tenga para `Alt` + `Shift` + `I` `Option` + `Shift` + `I` DevTools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Microsoft Edge Vista 3D de DevTools: MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Modelo de objetos de documento (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "Z-index | MDN"  
