---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, experimento
ms.openlocfilehash: f885201ddfb7553a2b9c58a07dd52b7a77c4137a
ms.sourcegitcommit: 0326a4082064e9cdfa602736f3f9ce7d8d294604
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "11094937"
---
# Características experimentales  

Microsoft Edge DevTools proporcionar acceso a las características experimentales que aún están en desarrollo.  Puede probar y [Enviar comentarios](#providing-feedback-on-experimental-features) antes de que se publique cada característica.  

Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, es posible que obtengas las últimas características experimentales con el canal Canarias de Microsoft Edge.  

## Activar características experimentales  

Para activar las características experimentales \ (o desactivada \) en Microsoft Edge, siga estos pasos.  

1.  [Abra DevTools][DevtoolsOpen].  
     *   Seleccione `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \).  Para obtener más información, vaya a [métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  
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
| [Emulación: modo de pantalla dual](#emulation-support-dual-screen-mode) | 84 o posterior |  
| [Habilitar nuevas características de depuración de cuadrícula CSS](#enable-new-css-grid-debugging-features) | 85 o posterior |  
| [Habilitar la compatibilidad para mover pestañas entre paneles](#enable-support-to-move-tabs-between-panels) | 85 o posterior |  
| [Habilitar webhint](#enable-webhint) | 85 o posterior |  
| [Habilitar la consola de red](#enable-network-console) | 85 o posterior |  
| [Visor de pedido de origen](#source-order-viewer) | 86 o posterior |  

### Emulación: modo de pantalla dual  

Proporciona características adicionales para emular dos nuevos dispositivos de pantalla dual y plegable en Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Doblado de Samsung Galaxy][SamsungMobileGalaxyFold]  

Emular los dispositivos y alternar entre las siguientes posturas.  

*   postura de pantalla única o plegada  
*   postura de pantalla doble o desdoblada  
    
[Habilita las API experimentales de la plataforma web](#enable-experimental-apis) y usa la [característica de expansión de pantalla multimedia de CSS][DualScreenDocsCssMedia] y la API de getWindowSegments de [JavaScript][DualScreenDocsJSAPI] para mejorar tu sitio web \ (o aplicación \) para dispositivos de doble pantalla y plegable.  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   Emula Surface Duo en Microsoft Edge  
:::image-end:::  

#### Habilitar las API experimentales  

Para usar la [característica de expansión de pantalla multimedia de CSS][DualScreenDocsCssMedia] y la [API de getWindowSegments de JavaScript][DualScreenDocsJSAPI], activa la `Experimental Web Platform features` bandera en Microsoft Edge.  Complete los siguientes pasos.  

1.  Vaya a `edge://flags` .  
1.  En el cuadro de texto **marcas de búsqueda** , escriba `Experimental Web Platform features` , elija el marcador de **características de plataforma web experimentales** y cambie **deshabilitado** a **habilitado**.  
1.  Reiniciar MicrosoftEdge.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Habilitar la marca experimental de características de plataforma web  
:::image-end:::  

> [!NOTE]
> Si está usando [consultas multimedia de CSS][DualScreenDocsCssMedia] o la [API de enumeración de segmentos de Windows de JavaScript][DualScreenDocsJSAPI] para mejorar su sitio web o aplicación para [Surface Duo][SurfaceDevicesDuo], también debe habilitar el marcador **experimental características de plataforma web** en la [aplicación Android Microsoft Edge][GooglePlayMicrosoftEdge] en su dispositivo [Surface Duo][SurfaceDevicesDuo] .  
> 
> Si el marcador **experimental características de plataforma web** está habilitado en el [escritorio Microsoft Edge][MicrosoftEdge] y deshabilitado en la [aplicación Android Microsoft Edge][GooglePlayMicrosoftEdge], el comportamiento de su sitio web o aplicación en el emulador Surface Duo en el escritorio Microsoft Edge no coincide con la [aplicación Android de Microsoft Edge][GooglePlayMicrosoftEdge] de [Surface Duo][SurfaceDevicesDuo].  Asegúrate de que los indicadores coincidan en Microsoft Edge y Android para usar correctamente el emulador Surface Duo en [Microsoft Edge para escritorio][MicrosoftEdge].  

#### Probar en dispositivos de plegable y de doble pantalla  

Cuando se emula la [Surface Duo][SurfaceDevicesDuo] en una postura de pantalla doble en Microsoft Edge, los marinos \ (el espacio entre las dos pantallas \) se dibuja sobre el sitio web o la aplicación.  

La pantalla emulada coincide con el modo en que tu sitio web \ (o aplicación \) se representa en la [aplicación Microsoft Edge Android][GooglePlayMicrosoftEdge] en [Surface Duo][SurfaceDevicesDuo].  Es posible que tengas que actualizar tu sitio web \ (o aplicación \) para que se muestre mejor a lo largo de la costura.  Para obtener más información sobre cómo adaptar su sitio web \ (o aplicación \) a la costura, desplácese hasta [Cómo trabajar con las costuras][DualScreenIntroductionHowWorkSeam] en la documentación de Surface Duo.  

La [barra de herramientas del dispositivo][DevtoolsDeviceModeIndexSimulateMobileViewport] tiene características adicionales que te ayudan a probar el sitio web o la aplicación en varias posturas y orientaciones.  Elija **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar la ventanilla a orientación horizontal. Combine la función con **span** \ ( ![ span ][ImageSpanIcon] \) para alternar entre las posturas de una pantalla o de doble cara o sin plegar.  Juntas, las características permiten probar el sitio web o la aplicación en las cuatro posturas y orientaciones posibles.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matriz de posturas y orientaciones para dispositivos de doble pantalla y plegable  
:::image-end:::  

El icono de **características de plataforma web experimental** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) muestra el estado del marcador de **características de plataforma web experimental** .  Si la bandera está activada, el icono está resaltado.  Si la marca está desactivada, el icono no está resaltado.  Para activar \ (o desactivar \) la bandera, navegue hasta `edge://flags` la bandera y vuelva a activarla.  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

Estos son otros recursos adicionales que pueden ayudarte a mejorar tu sitio web \ (o aplicación \) para dispositivos de dos pantallas:
*   Para obtener más información sobre el desarrollo web en dispositivos de doble pantalla, vaya a [experiencias Web en dos pantallas][DualScreenWebIndex].  
*   Instala el [emulador Surface Duo][DualScreenAndroidUseEmulator].  Es diferente al emulador en Microsoft Edge, emula la Surface Duo con Android y se integra con [Android Studio][AndroidDeveloperStudio].  Para obtener más información, vaya a [obtener el SDK Surface Duo][DualScreenAndroidGetDuoSdk].  

> [!NOTE]
> A continuación se muestra una lista de los problemas conocidos actuales.  
> 
> *   Cuando se usa un [cliente de escritorio remoto de Microsoft][RemoteDesktopClientDocs] para conectarse a un equipo remoto y emular el plegado de [Surface Duo][SurfaceDevicesDuo] o [Samsung Galaxy][SamsungMobileGalaxyFold], el puntero puede vibrar o reproducirse.  Si tiene el problema, [envíe sus comentarios](#providing-feedback-on-experimental-features).  

### Habilitar nuevas características de depuración de cuadrícula CSS  

Esta característica experimental ofrece una serie de nuevas visualizaciones que te ayudarán a depurar diseños de cuadrícula CSS.  Para obtener una vista previa de las últimas características experimentales, [habilita este experimento](#turn-on-experimental-features) y recarga DevTools.  Este experimento está activado de forma predeterminada en Edge 87 y versiones posteriores.  

#### Visualización de superposiciones de cuadrículas activadas con la herramienta inspeccionar  

La herramienta **inspeccionar** ofrece una manera rápida de identificar y visualizar diseños de cuadrícula CSS en un sitio web al desplazarse por ellos con el mouse.  Elija el icono de **inspeccionar** \ ( ![ inspeccionar ](./media/inspect-icon.msft.png) \) en la esquina superior izquierda de DevTools.  A continuación, mantenga el mouse sobre un elemento de cuadrícula en el sitio web que está depurando.  Los contornos se muestran en torno a la cuadrícula y el sombreado indica la ubicación de los huecos de la cuadrícula si están presentes.  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/grid-inspect.msft.png":::
   Visualización de cuadrículas con la herramienta inspeccionar  
:::image-end:::  

#### Visualización de superposiciones de cuadrícula persistentes  

En Edge 86 y versiones posteriores, la característica de cuadrícula de CSS experimental también ofrece la opción de habilitar las superposiciones de cuadrícula persistentes.  Las superposiciones persistentes ofrecen varias ventajas.  

*   Las superposiciones persistentes permanecen visibles en la página mientras se desplaza, mueve el mouse y usan otras características de la DevTools.  
*   Se pueden habilitar varias superposiciones persistentes al mismo tiempo, lo que le permite revisar numerosos diseños de cuadrícula a la vez.  
*   Las superposiciones persistentes ofrecen muchas opciones de configuración, como ocultar o mostrar nombres de área de cuadrícula, espacios de la cuadrícula, tamaños de pista y más.  

Las dos formas de alternar una superposición de cuadrícula persistente.  

*   Elija el rombo de **cuadrícula** junto a cualquier elemento de la cuadrícula que se muestra en el árbol DOM de la herramienta **elementos** .  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/grid-adorner.msft.png":::
       Rombo de cuadrícula en la herramienta elementos  
    :::image-end:::  
    
*   Abra el nuevo panel de **diseño** que se encuentra en la herramienta elementos y seleccione la casilla junto a cada elemento de la cuadrícula que desee resaltar.  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/grid-layout-zoom.msft.png":::
       Panel de diseño  
    :::image-end:::  
    
#### Configurar superposiciones persistentes  

El nuevo panel de **diseño** , ubicado en la herramienta **elementos** , junto a los **estilos** y las pestañas **calculadas** en Edge 86 y versiones posteriores, opciones de configuración de superficies para las superposiciones persistentes.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-grid.msft.png":::
   Característica de depuración de cuadrícula CSS  
:::image-end:::  

### Habilitar la compatibilidad para mover pestañas entre paneles  

Normalmente, las herramientas, como **los elementos** y la **red** , solo se pueden abrir en el panel principal que se encuentra en la parte superior de la DevTools.  Herramientas como la **vista 3D** y **problemas** que normalmente solo se abren en el panel de **cajón** , que se encuentra en la parte inferior de la DevTools.  Después de elegir el experimento, puede mover herramientas entre los paneles superior e inferior.  Para mover una herramienta, desplace el puntero en la pestaña, abra el menú contextual \ (haga clic con el botón derecho \) y elija **mover a la parte superior** o **mover a la parte inferior**.   Este experimento te permite personalizar el diseño de tu DevTools.  Para mostrar u ocultar el panel de **cajón** , seleccione `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-move-panels.msft.png":::
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

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-webhint.msft.png":::
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

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/network-network-console.msft.png":::
   **Consola de red** en el cajón de **consola**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Visor de pedido de origen  

El **visor de pedidos de origen** es un experimento que muestra el orden de los elementos en el origen de la página.  El orden de visualización en pantalla puede ser diferente del orden de origen, lo que confunde a los usuarios del lector de pantalla y del teclado.  Use el experimento del **visor de pedidos de origen** para encontrar las diferencias entre el orden de visualización en pantalla y el orden de origen.  

Después de habilitar el experimento, asegúrate de reiniciar el DevTools.  Para usar el **visor de órdenes de origen**, siga estos pasos.  

1.  Abra el panel **elementos** .  
1.  Abra el panel **accesibilidad** en el panel cajón \ (inferior \).  
1.  En la sección **visor de pedido de origen** , active la casilla Mostrar el pedido de **origen** .  
1.  Resalte cualquier elemento HTML para mostrar una superposición que sea el orden en el origen de la página.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/experiments-source-order-viewer.msft.png":::
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

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Lista de experimentos en la configuración de DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
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
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Personalizar los métodos abreviados de teclado en Microsoft Edge DevTools | Microsoft docs"

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias Web en pantalla dual | Microsoft docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtén el emulador Surface Duo | Microsoft docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con las costuras-Introducción a los dispositivos de doble pantalla | Microsoft docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usar el emulador Surface Duo | Microsoft docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de expansión de pantalla multimedia CSS para detección de pantalla doble | Microsoft docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript de getWindowSegments para dispositivos de doble pantalla | Microsoft docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de escritorio remoto | Microsoft docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Plegado de Galaxy | Fantástico"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "sugerencia"  
