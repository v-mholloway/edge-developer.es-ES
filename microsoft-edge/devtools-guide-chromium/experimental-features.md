---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/21/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, experimento
ms.openlocfilehash: 6b3e1c06d6b8ed79054c28df483fcca93e5751d6
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902857"
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
| [Habilitar la pestaña de configuración personalizada de métodos abreviados de teclado](#enable-custom-keyboard-shortcuts-settings-tab) | 84 o posterior |
| [Habilitar nuevas características de depuración de cuadrícula CSS](#enable-new-css-grid-debugging-features) | 85 o posterior |  
| [Habilitar la compatibilidad para mover pestañas entre paneles](#enable-support-to-move-tabs-between-panels) | 85 o posterior |  
| [Habilitar webhint](#enable-webhint) | 85 o posterior | 
| [Habilitar la consola de red](#enable-network-console) | 85 o posterior |

### Habilitar la pestaña de configuración personalizada de métodos abreviados de teclado

Proporciona una nueva página de **accesos directos** en la [configuración de DevTools][DevToolsCustomizeSettings] que permite que los [métodos abreviados de teclado][DevToolsShortcuts] coincidentes en el DevTools de [vs][VisualstudioCode].  

Una vez que hayas habilitado el experimento, vuelve a abrir la [configuración de DevTools][DevToolsCustomizeSettings] con seleccionar `Shift` + `?` .  Vaya a la nueva página de **accesos directos** .  Seleccione **DevTools (valor predeterminado)** en la lista desplegable **coincidir con métodos abreviados preestablecidos** y seleccione **código de Visual Studio**.  Los métodos abreviados de teclado de la DevTools ahora coinciden con los métodos abreviados para acciones equivalentes en VS Code.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a VS" lightbox="./media/experiments-keyboard-shortcut.png":::
   Hacer coincidir los métodos abreviados de teclado en el código de DevTools a VS
:::image-end:::  

Por ejemplo, en Windows, el método abreviado de teclado para pausar o seguir ejecutando un script en [vs Code][VisualstudioCodeShortcutsKeyboardWindows] es `F5` .  Con el ajuste preestablecido **DevTools (predeterminado)** , el mismo método abreviado de DevTools es `F8` .  Con el ajuste preestablecido de **Visual Studio** , también está el método abreviado `F5` .  

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
   Comentarios sobre webhint en el panel problemas  
:::image-end:::      

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar la consola de red

La **consola de red** es el título de trabajo de un experimento para hacer solicitudes de red sintéticas a través de http.  Puede usar el experimento **consola de red** para enviar solicitudes de API Web.  

Después de habilitar el experimento, asegúrate de reiniciar el DevTools. Para usar la consola de red:
1.  Abra el panel **red** .
1.  Busque la solicitud de red que desea cambiar y reenviar.
1.  Abra el menú contextual \ (haga clic con el botón derecho \) y elija **Editar y reproducir**. 
1.  Cuando se abra la **consola de red** , edite la información de solicitud de red.
1.  Seleccione **Enviar**.  

:::image type="complex" source="./media/network-network-console.png" alt-text="Consola de red en el cajón de consola" lightbox="./media/network-network-console.png":::
Consola de red en el cajón de consola
:::image-end::: 

<!--Available in Microsoft Edge version 85 and later.  --> 

## Características experimentales anteriores  

*   la [vista 3D][Devtools3dViewIndex] ahora está disponible y activada de forma predeterminada en Microsoft Edge versión 83 o posterior.  

## Proporcionar comentarios sobre características experimentales  

Para proporcionar comentarios sobre experimentos con Microsoft Edge DevTools o sobre cualquier otro tema relacionado con DevTools.  

*   Envíe sus comentarios con el icono de comentarios en el DevTools  
*   Tweet a [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/devtools-feedback.png" alt-text="Icono de comentarios en el DevTools de Microsoft Edge" lightbox="./media/devtools-feedback.png":::
   Icono de comentarios en el DevTools de Microsoft Edge  
:::image-end:::  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Vista 3D | Microsoft docs"  
[DevtoolsIssues]: ./issues/index.md "Buscar y solucionar problemas con la herramienta de problemas de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsOpen]: ./open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Métodos abreviados de teclado de código de Visual Studio para Windows | Código de Visual Studio"  

[WebhintMain]: https://webhint.io "sugerencia" 
