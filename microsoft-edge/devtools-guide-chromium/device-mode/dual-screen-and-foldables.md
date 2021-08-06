---
description: Usa dispositivos virtuales en Microsoft Edge para mejorar tu sitio web para dispositivos de doble pantalla y plegables.
title: Emular dispositivos de pantalla doble y plegado en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, emulación, dispositivo, simulación, móvil, pantalla doble, plegado, Surface Duo, Samsung Galaxy Fold
ms.openlocfilehash: 22a83e242027ca2e4b3e9c0072cf8c0624ec2cd16497dc7a38b2de6460e9be4c
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11800622"
---
# <a name="emulate-dual-screen-and-foldable-devices-in-microsoft-edge-devtools"></a>Emular dispositivos de pantalla doble y plegado en Microsoft Edge DevTools  

En Microsoft Edge versión 89 o posterior, puedes emular los siguientes dispositivos de doble pantalla y plegados.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy Fold][SamsungMobileGalaxyFold]  
    
Emula los dispositivos y alterna entre las siguientes posturas.  

*   Postura de pantalla única o doblada  
*   Postura de pantalla doble o desdoblada  
    
Activa las API [experimentales](#turn-on-experimental-apis) de plataforma web y usa la característica de pantalla multimedia [CSS][DualScreenDocsCssMedia] y la [API getWindowSegments][DualScreenDocsJSAPI] de JavaScript para mejorar tu sitio web \(o aplicación\) para dispositivos de pantalla doble y plegables.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emular Surface Duo en Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Emular Surface Duo en Microsoft Edge  
:::image-end:::  

## <a name="turn-on-experimental-apis"></a>Activar API experimentales  

Para usar la característica de pantalla de medios [CSS][DualScreenDocsCssMedia] y la [API getWindowSegments de JavaScript,][DualScreenDocsJSAPI]active la marca en `Experimental Web Platform features` Microsoft Edge.  Complete los pasos siguientes.  

1.  Vaya a `edge://flags`.  
1.  En el **cuadro de texto** Marcas de búsqueda, escriba , elija la marca características de plataforma web `Experimental Web Platform features` **experimental** y cambie **Deshabilitado** a **Habilitado**.  
1.  Reiniciar Microsoft Edge.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activar la marca de características de la plataforma web experimental" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Activar la marca **de características de la plataforma web** experimental  
:::image-end:::  

> [!NOTE]
> Si usas consultas multimedia [CSS][DualScreenDocsCssMedia] o la API de enumeración de segmentos de [JavaScript Windows][DualScreenDocsJSAPI] para mejorar tu sitio web o aplicación para [Surface Duo,][SurfaceDevicesDuo]también debes activar la marca de características de plataforma **web experimental** en la aplicación [Android Microsoft Edge][GooglePlayMicrosoftEdge] en tu dispositivo [Surface Duo.][SurfaceDevicesDuo]  
> 
> Si la marca de características de [][MicrosoftEdge] la Plataforma web experimental está activada en Microsoft Edge de escritorio y desactivada en la aplicación [Android Microsoft Edge][GooglePlayMicrosoftEdge], el comportamiento de tu sitio **web** o aplicación en el emulador de Surface Duo en el Microsoft Edge de escritorio no coincide con la aplicación de Android [Microsoft Edge en][GooglePlayMicrosoftEdge] Surface [Duo][SurfaceDevicesDuo].  Asegúrate de que las marcas coincidan en android y Microsoft Edge para usar correctamente el emulador de Surface Duo en el equipo de [Microsoft Edge][MicrosoftEdge].  

## <a name="test-on-foldable-and-dual-screen-devices"></a>Probar en dispositivos de doble pantalla y plegados  

Cuando emulas Surface [Duo][SurfaceDevicesDuo] en una posición de pantalla doble en Microsoft Edge, la costura \(el espacio entre las dos pantallas\) se dibuja sobre tu sitio web o aplicación.  

La pantalla emulada coincide con la forma en que el sitio web \(o aplicación\) se representa en la [aplicación android][GooglePlayMicrosoftEdge] Microsoft Edge mientras se ejecuta en [Surface Duo][SurfaceDevicesDuo].  Es posible que deba actualizar su sitio web \(o app\) para mostrarse mejor a lo largo de la costura.  Para obtener más información acerca de cómo adaptar el sitio web \(o aplicación\) a la costura, vaya a Cómo trabajar [con la costura][DualScreenIntroductionHowWorkSeam].  

La [barra de herramientas del][DevtoolsDeviceModeIndexSimulateMobileViewport] dispositivo tiene características adicionales que te ayudarán a probar tu sitio web o aplicación en varias posturas y orientaciones.  Elija **Girar** \( ![ Girar ](../media/rotate-dark-icon.msft.png) \) para girar la ventanilla a orientación horizontal. Combina la característica con **Span** \( Span \) para alternar entre posturas de pantalla única o doblada y de doble ![ pantalla o ](../media/span-dark-icon.msft.png) desdobladas.  Juntos, las características te permiten probar tu sitio web o aplicación en las cuatro posturas y orientaciones posibles.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas y orientaciones para dispositivos de pantalla doble y plegables" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matriz de posturas y orientaciones para dispositivos de pantalla doble y plegables  
:::image-end:::  

El **icono Características de la plataforma web** experimental \( ![ ExperimentalApis \) muestra el estado de la marca de características de la ](../media/experimental-apis-dark-icon.msft.png) Plataforma **web** experimental.  Si la marca está activada, se resalta el icono.  Si la marca está desactivada, el icono no se resalta.  Para activar \(o desactivar\) la marca, elija el icono o vaya a `edge://flags` y cambie la marca.  

> [!NOTE]
> A continuación se muestra una lista de problemas conocidos actuales.  
> 
> *   Cuando usas un [cliente Escritorio remoto de Microsoft para][RemoteDesktopClientDocs] conectarte a un equipo remoto y emular Surface [Duo][SurfaceDevicesDuo] o Samsung [Galaxy Fold,][SamsungMobileGalaxyFold]el puntero puede agitarse o tartamudear.  Si se ejecuta con el problema, [envíe comentarios](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## <a name="additional-resources"></a>Recursos adicionales  

Estos son recursos adicionales que pueden ayudarle a mejorar su sitio web \(o aplicación\) para dispositivos de pantalla doble.  

*   Para obtener más información sobre el desarrollo web en dispositivos de pantalla doble, vaya a [Experiencias web de pantalla dual.][DualScreenWebIndex]  
*   Instalar el [emulador de Surface Duo][DualScreenAndroidUseEmulator].  El emulador de Surface Duo es diferente del emulador de Microsoft Edge, ejecuta Android e se integra con [Android Studio][AndroidDeveloperStudio].  Para obtener más información, ve [a Obtener el SDK de Surface Duo][DualScreenAndroidGetDuoSdk].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias web de pantalla doble | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el emulador de Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la unión: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de pantalla expandida para medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API de JavaScript de getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Escritorio remoto | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/global/galaxy/galaxy-fold "Galaxy Fold | Samsung"  
