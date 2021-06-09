---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, experiment
no-loc:
- Enable webhint
- Enable Network Console
- Source Order Viewer
- Enable Composited Layers in 3D View
- Enable new Font Editor tool within the Styles pane
- Enable new CSS Flexbox debugging features
- Enable + button tab menus to open more tools
- Enable Welcome tab
- 3D View
- Turn on support to move tabs between panels
- Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code
- Edit keyboard shortcuts for any action in the DevTools
- Turn on new CSS grid debugging features
- 'Emulation: Support dual screen mode'
ms.openlocfilehash: 82d547c8c1ed0606bda9ade27d0dbddbfa2ca800
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11596995"
---
# <a name="experimental-features"></a>Características experimentales  

Microsoft Edge DevTools proporciona acceso a características experimentales que aún están en desarrollo.  Puede probar y [proporcionar comentarios antes](#providing-feedback-on-experimental-features) de publicar cada característica.  

Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, puede obtener las características experimentales más recientes mediante el canal Microsoft Edge Canary.  

## <a name="turn-on-experimental-features"></a>Activar características experimentales  

Para activar las características experimentales \(or off\) en Microsoft Edge, siga estos pasos.  

1.  [Abra DevTools][DevtoolsOpenIndex].  
    *   Seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).  Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  
1.  Abra el [Configuración][DevToolsCustomizeIndexSettings] panel.  
    *   Seleccione `Shift` + `?` .  Para obtener más información, vaya [a Microsoft Edge métodos abreviados de teclado de DevTools][DevtoolsShortcutsIndex].  
1.  En el lado izquierdo del **panel Configuración,** elija la **sección** Experimentos.  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="La página Experimentos de Configuración" lightbox="../media/experiments-devtools.msft.png":::
       La **página Experimentos** de **Configuración**  
    :::image-end:::  
    
1.  En la **página Experimentos,** desplácese por la lista de todas las características experimentales disponibles y elija la casilla junto a cada característica que desee probar.  
1.  Cierre y vuelva a abrir Microsoft Edge DevTools.  
    
> [!NOTE]
> Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.  Para desactivar una característica experimental, abra la página **Experimentos** y desactive la casilla de la característica experimental que desea desactivar.  

## <a name="highlighted-experimental-features"></a>Características experimentales resaltadas  

En las secciones siguientes se describen las nuevas características experimentales que están disponibles en Microsoft Edge.  

| Característica experimental | Microsoft Edge versión |  
|:--- |:--- |  
| [Enable webhint](#enable-webhint) | 85 o posterior |  
| [Enable Network Console](#enable-network-console) | 85 o posterior |  
| [Source Order Viewer](#source-order-viewer) | 86 o posterior |  
| [Enable Composited Layers in 3D View](#enable-composited-layers-in-3d-view) | 87 o posterior |  
| [Enable new Font Editor tool within the Styles pane](#enable-new-font-editor-tool-within-the-styles-pane) | 89 o posterior |  
| [Enable new CSS Flexbox debugging features](#enable-new-css-flexbox-debugging-features) | 89 o posterior |  
| [Enable + button tab menus to open more tools](#enable--button-tab-menus-to-open-more-tools) | 89 o posterior |  
| [Enable Welcome tab](#enable-welcome-tab) | 89 o posterior |  

### Enable webhint  

[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real para sitios web y páginas web locales.  El tipo de comentarios proporcionados [por webhint][WebhintMain].  

*   accesibilidad  
*   compatibilidad entre exploradores  
*   seguridad  
*   rendimiento  
*   Aplicaciones web progresivas (PWA)  
*   otros problemas comunes de desarrollo web  
    
El [experimento webhint][WebhintMain] muestra los comentarios de webhint en el panel [Problemas.][DevtoolsIssuesIndex]  Elija un problema para mostrar la documentación de la solución y una lista de los recursos afectados en su sitio web.  Elija un vínculo de recurso para abrir el panel **Network**, **Sources**o **Elements** relevante en DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   comentarios de webhint en el panel **Problemas**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Enable Network Console  

**Consola de** red es el título de trabajo de un experimento para realizar solicitudes de red sintéticas a través de HTTP.  Puede usar el experimento **consola de** red para enviar solicitudes de API web.  

Después de activar el experimento, asegúrese de reiniciar DevTools.  Para usar la **consola de red,** siga estos pasos.  

1.  Abra el **panel** Red.  
1.  Busque la solicitud de red que desea cambiar y reenviar.  
1.  Abra el menú contextual \(right-click\) y elija **Editar y reproducir**.  
1.  Cuando se **abra la consola de** red, edite la información de solicitud de red.  
1.  Elija **Enviar**.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Consola de red en el cajón de la consola" lightbox="../media/network-network-console.msft.png":::
   **Consola de red** en el **cajón de la** consola  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Source Order Viewer  

**Source Order Viewer** es un experimento que muestra el orden de los elementos en el origen de la página web.  El orden de visualización en pantalla puede diferir del orden del origen, lo que confunde el lector de pantalla y los usuarios de teclado.  Use el experimento para encontrar las diferencias entre el orden de visualización en pantalla **Source Order Viewer** y el orden del origen.  

Después de activar el experimento, asegúrese de reiniciar DevTools.  Para usar **Source Order Viewer** , complete los pasos siguientes.  

1.  Abra la **herramienta** Elementos.  
1.  A la derecha de la **pestaña Estilos,** seleccione la **pestaña Accesibilidad.**  
1.  En la **Source Order Viewer** sección, seleccione la casilla **Mostrar orden de origen.**  
1.  Resalte cualquier elemento HTML para mostrar una superposición que el orden en el origen de la página web.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Source Order Viewer en el panel Accesibilidad" lightbox=".. /media/experiments-source-order-viewer.msft.png":: **Source Order Viewer** en el panel **Accesibilidad**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Enable Composited Layers in 3D View  

Ahora puede visualizar capas junto con índices z y el modelo de objetos de documento \(DOM\).  Esta característica le ayuda a depurar sin cambiar de contexto con tanta frecuencia.  Identificó que la reducción del cambio de contexto era un punto de dolor importante.  No siempre está claro cómo el código que escribe afecta a la aplicación web.  Para una experiencia de depuración visual completa, ahora se combinan las capas 3D View compuestas y las capas compuestas.  

Después de activar el experimento, asegúrese de reiniciar DevTools.  Para usar **capas compuestas,** siga estos pasos.  

1.  En el cajón, elija la **3D View** herramienta.  
1.  Abra el **panel Capas compuestas.**  
1.  Se muestran todas las capas pintadas de la aplicación.  Pruebe esta característica con sus propias aplicaciones web.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   Panel **Capas compuestas**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Enable new Font Editor tool within the Styles pane  

Ahora puede usar el nuevo Editor de [fuentes][DevtoolsInspectStylesEditFonts] visual para editar fuentes.  Úselo para definir fuentes y características de fuente.  El Editor **de fuentes visual** le ayuda a completar las siguientes acciones.  

*   Cambiar entre unidades para las diferentes propiedades de la fuente  
*   Cambiar entre palabras clave para las diferentes propiedades de la fuente  
*   Convertir unidades  
*   Generar código CSS preciso  
    
Después de activar el experimento, asegúrese de reiniciar DevTools.  Para usar el nuevo Editor de **fuentes visuales,** siga estos pasos.  

1.  Abra la **herramienta** Elementos.  
1.  Abra el **panel Estilos.**  
1.  Elija el **icono Editor de** fuentes.  
    
Para obtener más información sobre el nuevo **Editor**de fuentes visual, vaya a Editar estilos y configuraciones de fuentes CSS en el panel Estilos [en DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Se resalta el panel Editor de fuentes visuales" lightbox="../media/font-editor-open.msft.png":::
   Se resalta **el panel Editor de** fuentes visuales  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable new CSS Flexbox debugging features  

Esta característica experimental proporciona muchas visualizaciones nuevas que le ayudarán a depurar diseños de CSS Flexbox.  Para obtener una vista previa de las características experimentales más recientes, [activa este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a>Mostrar superposiciones persistentes en diseños de Flexbox con la herramienta Inspeccionar  

La **herramienta Inspeccionar** proporciona una forma rápida de identificar y visualizar diseños de CSS Flexbox en un sitio web activando el mouse sobre ellos.  Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.  A continuación, mientras depura el sitio web, mantenga el mouse en un contenedor flexible para mostrar los contornos alrededor del contenedor flexible.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Mostrar contenedores de Flexbox con la herramienta Inspeccionar" lightbox="../media/flexbox-hover.msft.png":::
   Mostrar contenedores de Flexbox con **la herramienta Inspeccionar**  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a>Mostrar superposiciones persistentes en diseños de Flexbox  

En Microsoft Edge versión 89 o posterior, la característica experimental CSS Flexbox también ofrece la opción de activar superposiciones persistentes en diseños de Flexbox.  Las superposiciones persistentes proporcionan las siguientes ventajas.  

*   Las superposiciones persistentes permanecen visibles en la página web a medida que se desplaza, mueve el mouse y usa otras características de DevTools.
*   Se pueden usar varias superposiciones persistentes al mismo tiempo, para permitirle revisar varios diseños de Flexbox a la vez.  
*   Las superposiciones persistentes ofrecen opciones de configuración de color.  
    
Para alternar las superposiciones persistentes en el diseño de Flexbox, use una de las siguientes acciones.  

*   Elija el **icono oval de Flexbox** junto a cualquier contenedor de Flexbox que se muestre en el árbol DOM de la **herramienta** Elementos.  
*   Abra el nuevo panel **Diseño** ubicado en la **herramienta Elementos** y seleccione la casilla situada junto a cada contenedor de Flexbox que desee resaltar.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Iconos de Flex y panel Diseño en DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Iconos de Flex y panel **Diseño** en DevTools  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a>Configurar superposiciones persistentes  

Para configurar opciones para superposiciones persistentes para cuadrículas CSS o diseños de Flexbox, use el **panel** Diseño.  El **panel** Diseño se encuentra en la **herramienta Elementos** junto a los paneles **Estilos** **y** Calculados.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panel Diseño" lightbox="../media/flexbox-layout.msft.png":::
   Panel Diseño  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable + button tab menus to open more tools  

Ahora puede abrir más herramientas con el nuevo icono **Más herramientas** \( `+` \).  Después de activar el experimento y volver a cargar DevTools, se muestra un signo más \( \) a la derecha del grupo de pestañas en la parte superior **Enable + button tab menus to open more tools** `+` de DevTools.  Para mostrar una lista de otras herramientas que puede agregar a la barra de pestañas, elija el nuevo icono **Más** herramientas \( `+` \).  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Más herramientas en el panel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Más herramientas** en el panel superior
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Enable Welcome tab

Este experimento reemplaza la herramienta **Novedades** por la nueva **herramienta De** bienvenida.  Muestra un diseño actualizado para el siguiente contenido.  

*   Vínculos a documentos para desarrolladores  
*   las características más recientes  
*   notas de la versión  
*   Opción para ponerse en contacto con el Microsoft Edge de DevTools  
    
La **herramienta De** bienvenida se abre automáticamente después de cada actualización a Microsoft Edge.  Para evitar que se muestre la herramienta **de** bienvenida después de cada actualización, desactive la casilla situada junto a la pestaña Abrir después de cada **actualización** en el **título de** la herramienta de bienvenida.  

Si prefiere la herramienta original **Novedades,** vaya [a Configuración][DevtoolsCustomizeIndexSettings]  >  **Experiments** y quite la casilla situada junto a **Enable Welcome tab** .  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Herramienta de bienvenida" lightbox="../media/experiments-welcome.msft.png":::
   **Herramienta de** bienvenida  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Características experimentales anteriores  

*   [3D View][Devtools3dViewIndex]ahora está disponible y activado de forma predeterminada Microsoft Edge versión 83 o posterior.  
*   [Turn on support to move tabs between panels][DevtoolsCustomizeIndex]ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 85 o posterior.  
*   [Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code][DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 86 o posterior.  
*   [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]ahora está disponible y activado de forma predeterminada Microsoft Edge versión 89 o posterior.  
*   [Turn on new CSS grid debugging features][DevtoolsCssGrid]ahora está disponible y activado de forma predeterminada Microsoft Edge versión 89 o posterior.  
*   [Emulation: Support dual screen mode][DevtoolsDeviceModeDualScreenAndFoldables]ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 90 o posterior.  

## <a name="providing-feedback-on-experimental-features"></a>Proporcionar comentarios sobre características experimentales  

Para proporcionar comentarios sobre Microsoft Edge experimentos de DevTools o cualquier otra cosa relacionada con DevTools.  

*   Enviar sus comentarios con el icono **Enviar comentarios** en DevTools  
*   Tweet en [@EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en devTools de Microsoft Edge" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   El icono **Enviar comentarios en** devTools de Microsoft Edge  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Vista 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspeccionar css grid en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndex]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Edit keyboard shortcuts for any action in the DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsMatchKeyboardShortcutsDevtoolsMicrosoftVisualStudioCode]: ../customize/shortcuts.md#match-keyboard-shortcuts-in-the-devtools-to-microsoft-visual-studio-code "Match keyboard shortcuts in the DevTools to Microsoft Visual Studio Code | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar la configuración y los estilos de fuente CSS en el panel Estilos en DevTools | Microsoft Docs"  
[DevtoolsIssuesIndex]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsOpenIndex]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsShortcutsIndex]: ../shortcuts/index.md "Microsoft Edge Métodos abreviados de teclado de DevTools | Microsoft Docs"  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
