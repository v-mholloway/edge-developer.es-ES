---
description: Todo sobre la vista 3D y cómo usarla.
title: Vista 3D
author: erdraud
ms.author: erdraud
ms.date: 11/27/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f2ae80426da71797d4bee4060d33965f04047e19
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573275"
---
# Vista 3D

Use la **vista 3D** para depurar la aplicación web desplazándose por el [modelo de objetos de documento](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) (dom) o el contexto de apilamiento [de índice z](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index) . Con ella, puedes hacer lo siguiente: 

- [Explorar la Página Web traducida a un 3D perspevtive](#3d-dom)
- [Depuración basada en el contexto de apilamiento de índice z](#z-index)
- [Borrar parte del desorden en el panel Dom o en](#changing-your-view) el [Panel de índice z](#change-the-scope-of-your-exploration)
- [Elegir la combinación de colores para la mejor depuración de problemas de Dom](#dom-color-type) o [de índice z](#z-index-color-type)

Hay dos paneles que puede usar para su experiencia de depuración.

1. **Índice Z** Desplácese por los distintos elementos de la aplicación web con el contexto de índice z en mente. Este es el panel predeterminado.
2. **Dom 3D** Explore el DOM como un todo con todos los elementos a su alcance. Para obtener acceso a este panel, haga clic en el panel "DOM" junto al panel "índice Z".

![lienzo de vista 3D](./media/canvas.png)

## Navegar por el lienzo

### Métodos abreviados de teclado
- Girar el DOM: Use las teclas de flecha izquierda y derecha para girar horizontalmente y use las teclas de flecha arriba y abajo para girar verticalmente.
- Navegar por el DOM: si se selecciona un elemento, puede usar las teclas de flecha arriba y abajo para desplazarse por los elementos adyacentes

### Controles del ratón
- Girar el DOM: haga clic con el botón izquierdo y arrastre alrededor del espacio del lienzo.
- Desplácese por el DOM: haga clic con el botón secundario y arrastre en la dirección en la que desea mover el DOM.
- Zoom: arrastre dos dedos por el panel táctil o use la rueda de desplazamiento del mouse.

![controles en pantalla](./media/controls-small.png)
### Controles en pantalla
- Restablezca la vista de lienzo a la vista original: haga clic en el botón con la etiqueta "restablecer cámara" o haga clic en el icono que se parezca a un botón de actualización de un lado y tendrá "restablecer elementos en la vista y volver a centrar la cámara".
- Actualice el lienzo (por ejemplo, si el explorador cambió o ha cambiado a la vista emulador de dispositivos): haga clic en el botón que dice "volver a tomar instantánea" o haga clic en el botón que tiene el aspecto de un icono de actualización y tiene "tomar instantánea nueva" como el texto activable.

![Vista de índice Z](./media/z-index-view-box.png)

## Índice Z

Aunque el panel Índice Z tiene características compartidas con el panel DOM, aún tienen elementos que son únicos para el panel.

### Resaltar elementos con contexto de apilamiento

Esta configuración le permite activar y desactivar las etiquetas de índice z de los elementos del lienzo. La casilla de verificación estará seleccionada de forma predeterminada.

### Cambiar el ámbito de exploración

El botón **Mostrar todos los elementos** es la manera más rápida de Mostrar todos los elementos del DOM después de cambiar la configuración a continuación.

**Mostrar solo los elementos con el contexto de apilamiento** quita los elementos sin contexto de apilamiento y alisa el Dom para facilitar la navegación.

El filtro de **elemento seleccionado aislar** es esencialmente tres botones en uno. Hay dos casillas debajo de este botón: una es "Mostrar todos los padres" y "mantener solo los padres con el nuevo contexto de apilamiento". 

La casilla "Mostrar todos los padres" se activará de forma predeterminada. Si selecciona un elemento en el panel de lienzo y hace clic en **aislar elemento seleccionado**, el lienzo solo mostrará el elemento y sus elementos primarios.

Si selecciona la "conservar solo los padres con el nuevo contexto de apilamiento" y hace clic en **aislar elemento seleccionado**, el lienzo solo mostrará el elemento y los elementos primarios que tienen un nuevo contexto de apilamiento.

Si anula la selección de las casillas de verificación y hace clic en **aislar elemento seleccionado**, el lienzo solo mostrará el elemento que haya elegido en primer lugar.

En la parte inferior del panel controles, hay **elementos ocultos con el mismo orden de pintura que su control parental** . Al seleccionar y anular la selección de la casilla, se volverán a cargar los elementos en función de la selección. Si está seleccionado, los elementos que compartan el orden de pintura se acoplarán al elemento primario.

Estas opciones pretenden borrar algunos de los desordens que crean páginas web más complejas en el lienzo.

### Tipo de color de índice Z

Estas son las diferentes visualizaciones que puede usar para el DOM en el lienzo. Tanto si lo usas por diversión como si te ayudan a visualizar mejor el DOM, tenemos tres colorways diferentes, así como una configuración de "color de fondo". Los botones de radio le permiten alternar entre las opciones y seleccionar el tipo de color más adecuado para el proyecto (o que le gusten).

![Vista DOM](./media/dom-purple-box.png)

## DOM 3D

Si desea tomar más de una vista de depuración general, en lugar de la experiencia de índice z, el DOM 3D ofrece un aspecto general del DOM. Dado que el contexto de índice z se elimina, DOM se apila de forma más estrecha y clara. Este panel tiene una funcionalidad similar, pero hay algunos matices.

### Cambiar la vista

En el panel **3D Dom** , el filtro del **elemento seleccionado aislar** tiene "incluir hijos" y "incluir padres". De forma predeterminada, se seleccionan las dos casillas, lo que significa que al hacer clic en el botón **aislar elemento seleccionado** después de seleccionar un elemento en el lienzo, se muestra el elemento elegido, los elementos primarios del elemento y los elementos secundarios del elemento. Si anula la selección de la casilla "incluir hijos" y hace clic de nuevo en el botón **aislar elemento seleccionado** , se mostrará el elemento seleccionado y los elementos primarios del elemento. Si selecciona la casilla "incluir hijos" y anula la selección de la casilla "incluir padres" antes de hacer clic en **aislar elemento seleccionado**, el lienzo mostrará el elemento y sus elementos secundarios. Si anula la selección de ambas casillas y hace clic en **aislar elemento seleccionado**, el lienzo solo mostrará el elemento que seleccionó previamente.

Verá un control deslizante en el panel de control titulado **nivel de anidamiento** con un número al lado. El número indica el número de capas en el documento. Si arrastra el control deslizante hacia la izquierda, las capas exteriores desaparecerán hasta que se quede con un nivel de anidamiento de 1, lo que muestra únicamente el elemento posterior más lejano del DOM. Esto le permite quitar algunos de los desorden si está intentando obtener más información sobre lo que sucede en los niveles inferiores.

### Tipo de color DOM

Verá que, además de las opciones de color de fondo *a blanco*, *azul a amarillo*, *arco iris*y *usar color de fondo* , se *usa la textura*de la pantalla. La textura de la pantalla agrega el contexto a la experiencia de depuración mostrando el contenido de la página web directamente en los elementos. Esto sigue siendo un trabajo en curso, ya que algunos sitios web tienen un tiempo más difícil que representa la textura de la pantalla en la vista 3D. 

## Pasos siguientes

Trabajamos en la interfaz de usuario y agregamos más funcionalidad a la vista 3D según las preguntas de los usuarios como usted. Envíanos tus comentarios para que podamos seguir mejorando el DevTools de Microsoft Edge para ti. Simplemente haz clic en el icono de comentarios de la DevTools o pulsa `Alt`  +  `Shift`  +  `I` en Windows ( `Option`  +  `Shift`  +  `I` en Mac) y escribe las solicitudes de comentarios o características de la DevTools.