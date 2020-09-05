---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, experimento
ms.openlocfilehash: a5793b6f4b67add313958ad4b8cee01cb7b09dbf
ms.sourcegitcommit: 7e3644e6b1d568ab795168e421c013814efa0073
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/04/2020
ms.locfileid: "10996162"
---
# Características experimentales  

Puede usar las características experimentales que aún están en desarrollo en el Microsoft Edge DevTools para probar y [proporcionar comentarios](#providing-feedback-on-experimental-features) antes de que se publiquen de manera generalizada.  

Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, es posible que obtengas las últimas características experimentales con el canal Canarias de Microsoft Edge.  

## Activar características experimentales  

Siga estos pasos para activar las características experimentales \ (o desactivada \) en Microsoft Edge.  

1.  [Abra DevTools][DevtoolsOpen].  
     *   Seleccione `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \).  Para obtener más información, vea [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  
1.  Abra el panel [configuración][DevToolsCustomizeSettings] .  
    *   Seleccione `Shift` + `?` .  Para obtener más información, vea [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  
1.  En el lado izquierdo del panel **configuración** , seleccione la sección **experimentos** .  
    
    :::image type="complex" source="./media/experiments-devtools.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-devtools.png":::
       Lista de experimentos en la configuración de DevTools  
    :::image-end:::  
    
1.  En la página **experimentos** , desplácese por la lista de todas las características experimentales disponibles y seleccione la casilla junto a las características que quiera probar.  
1.  Cierre y vuelva a abrir Microsoft Edge DevTools.  

> [!NOTE]
> Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.  Para desactivar una característica experimental, abra la página **experimentos** y desmarque la casilla de verificación de la característica experimental que desea desactivar.  

## Características experimentales resaltadas  

En las siguientes secciones, se describen las nuevas características experimentales que están disponibles en Microsoft Edge.  

| Característica experimental | Versión de Microsoft Edge |  
|:--- |:--- |  
| [Habilitar nuevas características de depuración de cuadrícula CSS](#enable-new-css-grid-debugging-features) | 85 o posterior |  
| [Habilitar la compatibilidad para mover pestañas entre paneles](#enable-support-to-move-tabs-between-panels) | 85 o posterior |  
| [Habilitar webhint](#enable-webhint) | 85 o posterior |  
| [Habilitar la consola de red](#enable-network-console) | 85 o posterior |  
| [Habilitar el visor de pedido de origen](#enable-source-order-viewer) | 86 o posterior |  

### Habilitar nuevas características de depuración de cuadrícula CSS  

Mejora las visualizaciones en la página al depurar sitios web que tienen diseños de cuadrícula CSS.  Puede personalizar aún más las superposiciones en configuración de DevTools.  

:::image type="complex" source="./media/experiments-grid.png" alt-text="Característica de depuración de cuadrícula CSS" lightbox="./media/experiments-grid.png":::
   Característica de depuración de cuadrícula CSS  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar la compatibilidad para mover pestañas entre paneles  

Normalmente, las herramientas, como **los elementos** y la **red** , solo se pueden abrir en el panel \ (parte superior \) de DevTools.  De forma similar, las herramientas, como la **vista 3D** y los **problemas** , solo se pueden abrir en el panel del cajón \ (inferior \) de DevTools.  Si elige el experimento, puede mover herramientas entre los paneles superior e inferior activando la pestaña, abriendo el menú contextual \ (con el botón secundario del mouse \) y seleccionando **mover a la parte superior** o **mover a la parte inferior**.   Este experimento te permite personalizar el diseño de tu DevTools.  Para mostrar u ocultar el panel inferior, seleccione `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.png" alt-text="Mover pestañas entre paneles" lightbox="./media/experiments-move-panels.png":::
   Mover pestañas entre paneles  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar webhint  

[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real sobre accesibilidad, compatibilidad entre exploradores, seguridad, rendimiento, PWAs y otros problemas comunes de desarrollo web de los sitios Web.  El experimento de [webhint][WebhintMain] lleva los comentarios de webhint en DevTools en el panel [problemas][DevtoolsIssues] .  Puede seleccionar el problema para ver documentación sobre cómo solucionar el problema y una lista de los recursos afectados de su sitio Web.  Seleccione un vínculo de recursos para abrir el panel de **redes**, **orígenes**o **elementos** correspondiente en DevTools.  

:::image type="complex" source="./media/experiments-webhint.png" alt-text="Comentarios sobre webhint en el panel problemas" lightbox="./media/experiments-webhint.png":::
   Comentarios sobre webhint en el panel **problemas**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar la consola de red  

La **consola de red** es el título de trabajo de un experimento para hacer solicitudes de red sintéticas a través de http.  Puede usar el experimento **consola de red** para enviar solicitudes de API Web.  

Después de habilitar el experimento, asegúrate de reiniciar el DevTools.  Para usar la consola de red:  

1.  Abra el panel **red** .  
1.  Busque la solicitud de red que desea cambiar y reenviar.  
1.  Abra el menú contextual \ (haga clic con el botón derecho \) y elija **Editar y reproducir**.  
1.  Cuando se abra la **consola de red** , edite la información de solicitud de red.  
1.  Seleccione **Enviar**.  

:::image type="complex" source="./media/network-network-console.png" alt-text="Consola de red en el cajón de consola" lightbox="./media/network-network-console.png":::
   **Consola de red** en el cajón de **consola**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  --> 

### Habilitar el visor de pedido de origen  

El **visor de pedidos de origen** es el título de trabajo de un experimento para mostrar el orden de los elementos en el origen de la página.  Puede usar el experimento de **visor de pedidos de origen** para encontrar problemas de accesibilidad en las páginas, ya que el orden de visualización en pantalla puede ser diferente del orden de origen, lo que confunde a los usuarios del lector de pantalla.  

Después de habilitar el experimento, asegúrate de reiniciar el DevTools.  Para usar el visor de órdenes de origen:  

1.  Abra el panel **elementos** .  
1.  Abra el panel **accesibilidad** en el panel cajón \ (inferior \).  
1.  En la sección **visor de pedido de origen** , active la casilla Mostrar el pedido de **origen** .  
1.  Resalte cualquier elemento HTML para mostrar una superposición que sea el orden en el origen de la página.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visor de pedidos de origen en el panel Accesibilidad" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Visor de pedidos de origen** en el panel **accesibilidad**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## Características experimentales anteriores  

*   la [vista 3D][Devtools3dViewIndex] ahora está disponible y activada de forma predeterminada en Microsoft Edge versión 83 o posterior.  
*   [Personalizar los métodos abreviados de teclado][DevtoolsCustomKeyboardShortcuts] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 86 o posterior.
## Proporcionar comentarios sobre características experimentales  

Para proporcionar comentarios sobre experimentos con Microsoft Edge DevTools o sobre cualquier otro tema relacionado con DevTools.  

*   Envíe sus comentarios con el icono para **Enviar comentarios** en la DevTools  
*   Tweet a [@EdgeDevTools][TwitterEdgedevtools]   

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="El icono enviar comentarios en el DevTools de Microsoft Edge" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   El icono **Enviar comentarios** en Microsoft Edge DevTools  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Vista 3D | Microsoft docs"  
[DevtoolsIssues]: ./issues/index.md "Buscar y solucionar problemas con la herramienta de problemas de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsOpen]: ./open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Personalizar los métodos abreviados de teclado en Microsoft Edge DevTools | Microsoft docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "sugerencia" 
