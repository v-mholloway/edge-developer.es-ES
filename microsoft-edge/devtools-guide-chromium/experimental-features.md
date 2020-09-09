---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, experimento
ms.openlocfilehash: c78e9aa5e0b4d808dd67d607a954b185ddcf54e7
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004055"
---
# Características experimentales  

Microsoft Edge DevTools proporcionar acceso a las características experimentales que aún están en desarrollo.  Puede probar y p[Enviar comentarios](#providing-feedback-on-experimental-features) antes de que se publique cada característica.  

Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, es posible que obtengas las últimas características experimentales con el canal Canarias de Microsoft Edge.  

## Activar características experimentales  

Siga estos pasos para activar las características experimentales \ (o desactivada \) en Microsoft Edge.  

1.  [Abra DevTools][DevtoolsOpen].  
     *   Seleccione `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \).  Para obtener más información, vea [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  
1.  Abra el panel [configuración][DevToolsCustomizeSettings] .  
    *   Seleccione `Shift` + `?` .  Para obtener más información, vaya a [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  
1.  En el lado izquierdo del panel **configuración** , elija la sección **experimentos** .  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-devtools.msft.png":::
       Lista de experimentos en la configuración de DevTools  
    :::image-end:::  
    
1.  En la página **experimentos** , desplácese por la lista de todas las características experimentales disponibles y seleccione la casilla junto a cada característica que quiera probar.  
1.  Cierre y vuelva a abrir Microsoft Edge DevTools.  

> [!NOTE]
> Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.  Para desactivar una característica experimental, abra la página **experimentos** y desmarque la casilla de verificación de la característica experimental que desea desactivar.  

## Características experimentales resaltadas  

En las siguientes secciones, se describen las nuevas características experimentales que están disponibles en Microsoft Edge.  

| Característica experimental | Versión de Microsoft Edge |  
|:--- |:--- |  
| [Habilitar la pestaña de configuración personalizada de métodos abreviados de teclado](#enable-custom-keyboard-shortcuts-settings-tab) | 84 o posterior |
| [Emulación: modo de pantalla dual](#emulation-support-dual-screen-mode) | 84 o posterior |  
| [Habilitar nuevas características de depuración de cuadrícula CSS](#enable-new-css-grid-debugging-features) | 85 o posterior |  
| [Habilitar la compatibilidad para mover pestañas entre paneles](#enable-support-to-move-tabs-between-panels) | 85 o posterior |  
| [Habilitar webhint](#enable-webhint) | 85 o posterior |  
| [Habilitar la consola de red](#enable-network-console) | 85 o posterior |  
| [Habilitar el visor de pedido de origen](#enable-source-order-viewer) | 86 o posterior |  

### Habilitar la pestaña de configuración personalizada de métodos abreviados de teclado  

Proporciona una nueva página de **accesos directos** en [configuración de DevTools][DevToolsCustomizeSettings] para que coincidan los [métodos abreviados de teclado][DevToolsShortcuts] del DevTools con el código de [Microsoft Visual Studio][VisualstudioCode].  

Después de habilitar el experimento, vuelve a abrir la [configuración de DevTools][DevToolsCustomizeSettings] con seleccionar `Shift` + `?` .  Vaya a la nueva página de **accesos directos** .  Seleccione **DevTools (valor predeterminado)** en la lista desplegable **coincidir con métodos abreviados preestablecidos** y seleccione **código de Visual Studio**.  Los métodos abreviados de teclado de la DevTools ahora coinciden con los métodos abreviados para acciones equivalentes en el código de Visual Studio.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="./media/experiments-keyboard-shortcut.msft.png":::
   Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio  
:::image-end:::  

Por ejemplo, en Windows, el método abreviado de teclado para pausar o seguir ejecutando un script en [Visual Studio Code][VisualstudioCodeShortcutsKeyboardWindows] es `F5` .  Con el ajuste preestablecido **DevTools (predeterminado)** , el mismo método abreviado de DevTools es `F8` .  Con el ajuste preestablecido de **Visual Studio** , también está el método abreviado `F5` .  

### Emulación: modo de pantalla dual  

Proporciona características adicionales para emular dos nuevos dispositivos de pantalla dual y plegable en Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Doblado de Samsung Galaxy][SamsungMobileGalaxyFold]  

Emular los dispositivos y alternar entre las siguientes posturas.  

*   postura de pantalla única o plegada  
*   postura de pantalla doble o desdoblada  

Use la opción [habilitar las API experimentales](#enable-experimental-apis) para mejorar su sitio web \ (o aplicación \) para un dispositivo.  También puede usar las [consultas de multimedia de CSS y la API de enumeración de segmentos de Windows de JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].  

<!-- This image was taken in Chromium Canary since we don't yet have an Edge Canary that has Stan's changes -->  

:::image type="complex" source="./media/experiments-dual-screen-emulation.msft.png" alt-text="Emula Surface Duo en Microsoft Edge" lightbox="./media/experiments-dual-screen-emulation.msft.png":::  
   Emula Surface Duo en Microsoft Edge  
:::image-end:::  

#### Habilitar las API experimentales  

Para [habilitar este experimento](#turn-on-experimental-features) en Microsoft Edge DevTools, siga los pasos que se indican a continuación.  

1.  Vaya a `edge://flags` .  
1.  En el cuadro de texto **marcas de búsqueda** , escriba `Experimental Web Platform features` , elija el marcador de **características de plataforma web experimentales** y cambie **deshabilitado** a **habilitado**.  
1.  Reiniciar MicrosoftEdge.  

Para mejorar el sitio web o la aplicación para dispositivos de plegable y pantalla doble, navegue hasta las [consultas de multimedia CSS y la API de enumeración de segmentos de Windows de JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].

[Activa este experimento](#turn-on-experimental-features) en el DevTools de Microsoft Edge.  

1.  Abra una nueva pestaña en Microsoft Edge y vaya a `edge://flags` .  
1.  En el cuadro de texto **marcas de búsqueda** , escriba `Experimental Web Platform features` , elija **características experimentales de plataforma web**y cambiar **deshabilitado** a **habilitado**.  
1.  Reiniciar MicrosoftEdge.  

Para obtener más información sobre cómo mejorar el sitio web \ (o la aplicación \) para dispositivos de dos pantallas y plegable, navegue hasta las [consultas de multimedia CSS y la API de enumeración de segmentos de Windows de JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Habilitar la marca experimental de características de plataforma web" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Habilitar la marca experimental de características de plataforma web  
:::image-end:::  

> [!NOTE]
> Si está usando [consultas multimedia de CSS o la API de enumeración de segmentos de Windows de JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables] para mejorar su sitio web o aplicación para [Surface Duo][SurfaceDevicesDuo], también debe habilitar el marcador **experimental características de plataforma web** en la [aplicación Android Microsoft Edge][GooglePlayMicrosoftEdge] en su dispositivo [Surface Duo][SurfaceDevicesDuo] .
> 
> Si el marcador **experimental características de plataforma web** está habilitado en el [escritorio Microsoft Edge][MicrosoftEdge] y deshabilitado en la [aplicación Android Microsoft Edge][GooglePlayMicrosoftEdge], el comportamiento de su sitio web o aplicación en el emulador Surface Duo no coincidirá con la [aplicación Android de Microsoft Edge][GooglePlayMicrosoftEdge] de [Surface Duo][SurfaceDevicesDuo].  Asegúrate de que los indicadores coincidan en Microsoft Edge y Android para usar correctamente el emulador Surface Duo en [Microsoft Edge para escritorio][MicrosoftEdge].  

#### Probar en dispositivos de plegable y de doble pantalla  

Al emular la [Surface Duo][SurfaceDevicesDuo] en una postura de pantalla doble en Microsoft Edge, las **costuras** se dibujan sobre el sitio web o la aplicación.  

> [!NOTE]
> La **costura** es el espacio entre las dos pantallas.  

La visualización emulada de tu sitio web \ (o de la aplicación \) es una representación correcta.  Coincide con la pantalla de la [aplicación Microsoft Edge Android][GooglePlayMicrosoftEdge] en [Surface Duo][SurfaceDevicesDuo].  Actualiza el contenido para que se muestre mejor a lo largo de la **costura**.  Para obtener más información sobre cómo adaptar su sitio web \ (o aplicación \) a la **costura**, desplácese hasta [Cómo trabajar con las costuras][DualScreenIntroductionHowWorkSeam] en la documentación de Surface Duo.  

La [barra de herramientas del dispositivo][DevtoolsDeviceModeIndexSimulateMobileViewport] tiene características adicionales que te ayudan a probar el sitio web o la aplicación en varias posturas y orientaciones.  Elija **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar la ventanilla a orientación horizontal. Combine la función con **span** \ ( ![ span ][ImageSpanIcon] \) para alternar entre las posturas de una pantalla o de doble cara o sin plegar.  Juntas, las características permiten probar el sitio web o la aplicación en las cuatro posturas y orientaciones posibles.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas y orientaciones para dispositivos de doble pantalla y plegable" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matriz de posturas y orientaciones para dispositivos de doble pantalla y plegable  
:::image-end:::  

El icono de **características de plataforma web experimental** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) muestra el estado del marcador de **características de plataforma web experimental** .  Si la bandera está activada, el icono está resaltado.  Si la marca está desactivada, el icono no está resaltado.  Para activar \ (o desactivar \) la bandera, elija el icono o desplácese hasta ella y, a continuación, `edge://flags` alterne la bandera.  

#### Recursos adicionales  
*   Para obtener más información sobre cómo desarrollar, vaya a [experiencias Web de pantalla doble][DualScreenWebIndex].  
*   Instala el emulador Surface Duo].  Es diferente del emulador en Microsoft Edge.  Emula la Surface Duo con Android y se integra con [Android Studio][AndroidDeveloperStudio].  Para obtener más información, vaya a [obtener el SDK Surface Duo][DualScreenAndroidGetDuoSdk].  

### Habilitar nuevas características de depuración de cuadrícula CSS  

Mejora las visualizaciones en la página al depurar sitios web que tienen diseños de cuadrícula CSS.  Puede personalizar aún más las superposiciones en configuración de DevTools.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Característica de depuración de cuadrícula CSS" lightbox="./media/experiments-grid.msft.png":::
   Característica de depuración de cuadrícula CSS  
:::image-end:::  

Para obtener una vista previa de las últimas características experimentales, complete las siguientes acciones.  

1.  En la sección **experimentos** , seleccione la casilla **Habilitar nuevas características de depuración de la cuadrícula CSS (opciones de configuración disponibles en el panel de la barra lateral diseño en elementos después de reiniciar)** .  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar la compatibilidad para mover pestañas entre paneles  

Normalmente, las herramientas, como **los elementos** y la **red** , solo se pueden abrir en el panel principal que se encuentra en la parte superior de la DevTools.  Herramientas como la **vista 3D** y **problemas** que normalmente solo se abren en el panel de **cajón** , que se encuentra en la parte inferior de la DevTools.  Después de elegir el experimento, puede mover herramientas entre los paneles superior e inferior.  Para mover una herramienta, desplace el puntero en la pestaña, abra el menú contextual \ (haga clic con el botón derecho \) y elija **mover a la parte superior** o **mover a la parte inferior**.   Este experimento te permite personalizar el diseño de tu DevTools.  Para mostrar u ocultar el panel de **cajón** , seleccione `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Mover pestañas entre paneles" lightbox="./media/experiments-move-panels.msft.png":::
   Mover pestañas entre paneles  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar webhint  

[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real para sitios web y páginas web locales.  El tipo de comentarios proporcionados por [webhint][WebhintMain].  

*   accesibilidad  
*   compatibilidad entre exploradores  
*   seguridad  
*   comportamiento  
*   PWA  
*   otros problemas comunes de desarrollo web  

El experimento [webhint][WebhintMain] muestra los comentarios de webhint en el panel [problemas][DevtoolsIssues] .  Seleccione un problema para mostrar la documentación de la solución y una lista de los recursos afectados de su sitio Web.  Seleccione un vínculo de recursos para abrir el panel de **redes**, **orígenes**o **elementos** correspondiente en DevTools.  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Comentarios sobre webhint en el panel problemas" lightbox="./media/experiments-webhint.msft.png":::
   Comentarios sobre webhint en el panel **problemas**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar la consola de red  

La **consola de red** es el título de trabajo de un experimento para hacer solicitudes de red sintéticas a través de http.  Puede usar el experimento **consola de red** para enviar solicitudes de API Web.  

Después de habilitar el experimento, asegúrate de reiniciar el DevTools.  Para usar la **consola de red**, siga estos pasos.    

1.  Abra el panel **red** .  
1.  Busque la solicitud de red que desea cambiar y reenviar.  
1.  Abra el menú contextual \ (haga clic con el botón derecho \) y elija **Editar y reproducir**.  
1.  Cuando se abra la **consola de red** , edite la información de solicitud de red.  
1.  Seleccione **Enviar**.  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Consola de red en el cajón de consola" lightbox="./media/network-network-console.msft.png":::
   **Consola de red** en el cajón de **consola**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar el visor de pedido de origen  

El **visor de pedidos de origen** es un experimento que muestra el orden de los elementos en el origen de la página.  El orden de visualización en pantalla puede ser diferente del orden de origen, lo que confunde a los usuarios del lector de pantalla y del teclado.  Use el experimento del **visor de pedidos de origen** para encontrar las diferencias entre el orden de visualización en pantalla y el orden de origen.  

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

## Proporcionar comentarios sobre características experimentales  

Para proporcionar comentarios sobre experimentos con Microsoft Edge DevTools o sobre cualquier otro tema relacionado con DevTools.  

*   Envíe sus comentarios con el icono para **Enviar comentarios** en la DevTools  
*   Tweet a [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="El icono enviar comentarios en Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   El icono **Enviar comentarios** en Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Vista 3D | Microsoft docs"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Buscar y solucionar problemas con la herramienta de problemas de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsShortcuts]: ./shortcuts.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsOpen]: ./open.md "Abrir Microsoft Edge DevTools | Microsoft docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias Web en pantalla dual | Microsoft docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtén el emulador Surface Duo | Microsoft docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con las costuras-Introducción a los dispositivos de doble pantalla | Microsoft docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[VisualstudioCode]: https://code.visualstudio.com "Código de Microsoft Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Métodos abreviados de teclado de código de Visual Studio para Windows | Código de Microsoft Visual Studio"  

[GitHubMicrosoftedgeMsedgeexplainerFoldables]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma web para experiencias habilitadas en dispositivos plegable | GitHub"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Plegado de Galaxy | Fantástico"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "sugerencia"  
