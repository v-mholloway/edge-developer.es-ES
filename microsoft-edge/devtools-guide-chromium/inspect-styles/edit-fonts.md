---
description: Obtenga información sobre cómo cambiar los estilos y la configuración de fuentes CSS mediante el panel Estilos en Microsoft Edge DevTools.
title: Editar estilos y opciones de fuente CSS en el panel Estilos de DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
no-loc:
- Enable new font editor tool within the Styles pane
ms.openlocfilehash: 5d9074ca65f9cb98662a1bc181f70ead4c4232e1
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439496"
---
# <a name="edit-css-font-styles-and-settings-in-the-styles-pane"></a>Editar estilos y opciones de fuente CSS en el panel Estilos  

:::image type="icon" source="../media/experimental-tag-14px.msft.png":::

La tipografía en la web es una parte importante de la experiencia del usuario.  Quieres asegurarte de que cumples las directrices de marca corporativa y que el contenido se muestra según lo esperado en varios dispositivos.  El texto debe ser fácil de leer con el tamaño y el alto de línea.  Los usuarios pueden cambiar el tamaño de las fuentes para satisfacer las necesidades individuales.  Para situaciones en las que fuentes específicas no están disponibles en un dispositivo de usuario, debes proporcionar opciones de fuente de reserva.  

CSS proporciona una mejor compatibilidad con la tipografía en los últimos años.  Hay decenas de unidades CSS diferentes disponibles para definir el tamaño del texto.  También tiene varias propiedades CSS que afectan al tamaño de fuente, el espaciado, el alto de línea y otras características tipográficas.  

Para facilitar el trabajo con tipografía, un **Editor** de fuentes visual está ahora en el **panel Estilos.**  Puede cambiar la configuración de fuente y los cambios se representan inmediatamente en el explorador.  Todo ello sin conocimientos profundos de CSS.  

Actualmente, **Enable new font editor tool within the Styles pane** la característica es experimental y debe [activarla para Microsoft Edge Developer Tools][DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures].  

Cualquier CSS del panel **Estilos,** ya sea definiciones de fuente o estilos en línea, muestra automáticamente un icono que abre el **Editor de fuentes visual.**  Para abrir el **Editor de fuentes visual,** elija el icono **Editor de** fuentes.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-icon.msft.png" alt-text="Icono del panel Estilos para editar la configuración de fuente" lightbox="../media/font-editor-icon.msft.png":::
         Icono del panel **Estilos para** editar la configuración de fuente  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Editor de fuentes abierto en la parte superior del panel Estilos" lightbox="../media/font-editor-open.msft.png":::
         Editor **de fuentes** abierto en la parte superior del panel **Estilos**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Todos los campos del **Editor de fuentes visuales** se rellenan a partir de los valores del CSS en el panel **Estilos.**  Por ejemplo, la definición se establece en en el panel Estilos, por lo que se muestra el campo de texto alto de línea y se muestra `line-height` `160%` el desplegable de **** `160` unidades `%` .  Además, el control deslizante se establece automáticamente para que coincida con los valores del campo de texto.  

El **Editor de** fuentes consta de dos partes: el selector de familia de fuentes y el editor de propiedades CSS.  

## <a name="the-font-family-selector"></a>Selector de familia de fuentes  

El selector de familia de fuentes es la parte superior del Editor **de fuentes visual.**  Para elegir las fuentes de la regla CSS, en el editor CSS, use el selector **familia de** fuentes.  Puede elegir fuentes principales y de reserva para cada regla CSS.  

:::image type="complex" source="../media/font-editor-font-family.msft.png" alt-text="El Editor de fuentes se abre en la parte superior del panel Estilos con el selector familia de fuentes resaltado" lightbox="../media/font-editor-font-family.msft.png":::
   El **Editor de fuentes** se abre en la parte superior del panel **Estilos** con el selector **familia** de fuentes resaltado  
:::image-end:::  

Usa el **desplegable Familia de** fuentes para elegir entre una lista de fuentes.  Las fuentes se organizan en cuatro grupos.  

1.  Fuentes calculadas, que son las fuentes disponibles en la hoja de estilos en el **panel Estilos.**  
1.  Fuentes del sistema, que son las fuentes que están disponibles en el sistema operativo actual.  
1.  Familias de fuentes genéricas, como `serif` o `sans-serif` .  
1.  Valores globales, como `inherit` , `initial` y `unset` .  
    
:::image type="complex" source="../media/font-editor-font-family-list.msft.png" alt-text="El editor de fuentes se abre en la parte superior del panel Estilos con el selector familia de fuentes resaltado" lightbox="../media/font-editor-font-family-list.msft.png":::
   El **Editor de fuentes** se abre en la parte superior del panel **Estilos** con el selector **familia** de fuentes resaltado  
:::image-end:::  

Después de elegir una fuente, se muestra otro menú desplegable para que elija fuentes de reserva.  Puede elegir hasta ocho fuentes de reserva.  Para quitar una fuente, elija el **icono Eliminar familia de** fuentes.  

<!--:::image type="complex" source="../media/font-editor-defining-fonts.msft.png" alt-text="The font editor with a defined list of fonts and fallback fonts" lightbox="../media/font-editor-defining-fonts.msft.png":::
   The **Font Editor** with a defined list of fonts and fallback fonts highlighted
:::image-end:::  -->

> [!NOTE]
> Si eliges un valor global para la familia de fuentes, no obtienes otro desplegable ya que no hay reserva para él en CSS.  

## <a name="the-css-properties-editor"></a>Editor de propiedades CSS  

Puede cambiar las propiedades de fuente CSS en la parte inferior del Editor **de fuentes visual.**  Puedes cambiar el tamaño de fuente, el alto de línea, el grosor de fuente y el espaciado entre letras mediante cualquiera de los controles de la interfaz de usuario.  Los cambios se aplican inmediatamente en el explorador.  

:::image type="complex" source="../media/font-editor-css-properties.msft.png" alt-text="El editor de fuentes se abre en la parte superior del panel Estilos con las propiedades CSS resaltadas" lightbox="../media/font-editor-css-properties.msft.png":::
   El **Editor de fuentes** se abre en la parte superior del panel **Estilos** con las propiedades CSS resaltadas  
:::image-end:::  

También puede convertir unidades CSS mediante el **Editor de fuentes visual**.  Por ejemplo, puede usar la herramienta en una regla CSS donde el control deslizante Tamaño **de** fuente está establecido inicialmente en `16 pixels` .  Ahora, use el desplegable de unidades y elija el valor `em` .  El `1 em` valor mostrado es igual a `16 pixels` .  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-setting-to-16px.msft.png" alt-text="Cambiar el tamaño de fuente a 16 píxeles" lightbox="../media/font-editor-setting-to-16px.msft.png":::
         Cambiar el tamaño de fuente a `16 pixels`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/font-editor-converted-to-em.msft.png" alt-text="Abrir la lista desplegable de unidades para convertir a em" lightbox="../media/font-editor-converted-to-em.msft.png":::
         Abrir la lista desplegable de unidades a la que convertir `em`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

El desplegable de unidades proporciona todas las unidades CSS numéricas que están disponibles.  El tamaño de fuente, el alto de línea, el grosor de fuente y el espaciado usan unidades diferentes.  Cuando los cuadros de texto tengan el foco, puede seleccionar las `arrow up` teclas y para ajustar la `arrow down` configuración.  Para usar los controles deslizantes con un teclado, seleccione las `arrow left` teclas `arrow down` y.  

El editor de propiedades CSS también incluye palabras clave preestablecidas.  Para usar las palabras clave preestablecidas, en el lado derecho, elija el `Toggle Input Type` icono.  La interfaz de usuario cambia y se muestra un desplegable de palabras clave preestablecidas.  Para volver a la interfaz de usuario con el control deslizante y otros controles de la interfaz de usuario, vuelve a `Toggle Input Type` elegir el icono.  

:::image type="complex" source="../media/font-editor-preset-font-sizes.msft.png" alt-text="Abrir la interfaz de palabras clave preestablecidas" lightbox="../media/font-editor-preset-font-sizes.msft.png":::
   Abrir la interfaz de palabras clave preestablecidas  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndex]: ../experimental-features/index.md "Características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesIndexTurnOnExperimentalFeatures]: ../experimental-features/index.md#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
