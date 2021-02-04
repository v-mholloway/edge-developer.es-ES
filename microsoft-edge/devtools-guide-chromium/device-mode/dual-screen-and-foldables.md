---
description: Usa dispositivos virtuales en Microsoft Edge para mejorar tu sitio web para dispositivos de doble pantalla y plegados.
title: Emular dispositivos de doble pantalla y plegado en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, emulación, dispositivo, simulación, móvil, pantalla doble, plegado, Surface Duo, Retenido de Samsung
ms.openlocfilehash: bc91c0b7c917d82f169dc7d47e047a587d505353
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313368"
---
# Emular dispositivos de doble pantalla y plegado en Microsoft Edge DevTools  

En Microsoft Edge versión 89 o posterior, puedes emular los siguientes dispositivos de doble pantalla y plegados.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Redoblón Desdeso][SamsungMobileGalaxyFold]  
    
Emula los dispositivos y alterna entre las siguientes posturas.  

*   Posición de una sola pantalla o plegado  
*   Posición de pantalla doble o desdoblada  
    
Activa las API [experimentales](#turn-on-experimental-apis) de la plataforma web y usa la característica de pantalla multimedia [CSS][DualScreenDocsCssMedia] y la [API getWindowSegments][DualScreenDocsJSAPI] de JavaScript para mejorar tu sitio web \(o app\) para dispositivos de doble pantalla y plegados.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Emular Surface Duo en Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Emular Surface Duo en Microsoft Edge  
:::image-end:::  

## Activar las API experimentales  

Para usar la característica [de pantalla][DualScreenDocsCssMedia] multimedia CSS y la [API getWindowSegments de JavaScript,][DualScreenDocsJSAPI]activa la marca en Microsoft `Experimental Web Platform features` Edge.  Complete los pasos siguientes.  

1.  Vaya a `edge://flags` .  
1.  En el **cuadro de texto Marcas de** búsqueda, escriba , elija la marca de características de la plataforma web `Experimental Web Platform features` **experimental** y cambie **Deshabilitado** a **Habilitado.**  
1.  Reiniciar MicrosoftEdge.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activar la marca de características de la plataforma web experimental" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Activar la marca **de características de la plataforma web** experimental  
:::image-end:::  

> [!NOTE]
> Si usas consultas multimedia [CSS][DualScreenDocsCssMedia] o la API de enumeración de segmentos de Windows de [JavaScript][DualScreenDocsJSAPI] para mejorar tu sitio web o aplicación para [Surface Duo,][SurfaceDevicesDuo]también debes activar la marca de características de la plataforma **web experimental** en la aplicación De Microsoft Edge para [Android][GooglePlayMicrosoftEdge] en el dispositivo [Surface Duo.][SurfaceDevicesDuo]  
> 
> Si la marca de características de la plataforma **web experimental** está activada en el escritorio de [Microsoft Edge][MicrosoftEdge] y desactivada en la aplicación De Microsoft Edge para [Android,][GooglePlayMicrosoftEdge]el comportamiento de tu sitio web o aplicación en el emulador de Surface Duo en el escritorio de Microsoft Edge no coincide con la aplicación [De Microsoft Edge][GooglePlayMicrosoftEdge] para Android en [Surface Duo.][SurfaceDevicesDuo]  Asegúrate de que las marcas coincidan en Microsoft Edge de escritorio y Android para usar correctamente el emulador de Surface Duo en el escritorio [de Microsoft Edge.][MicrosoftEdge]  

## Prueba en dispositivos de doble pantalla y plegados  

Cuando emulas [Surface Duo][SurfaceDevicesDuo] en una posición de pantalla doble en Microsoft Edge, la forma \(el espacio entre las dos pantallas\) se dibuja a través de tu sitio web o aplicación.  

La pantalla emulada coincide con la forma en que tu sitio web \(o app\) se representa en la aplicación [Microsoft Edge para Android][GooglePlayMicrosoftEdge] mientras se ejecuta en Surface [Duo.][SurfaceDevicesDuo]  Es posible que tenga que actualizar su sitio web \(o app\) para que se muestre mejor a lo largo de la seam.  Para obtener más información acerca de la adaptación de tu sitio web \(o app\) a la seam, ve a Cómo trabajar [con la seam][DualScreenIntroductionHowWorkSeam].  

La [barra de herramientas del][DevtoolsDeviceModeIndexSimulateMobileViewport] dispositivo tiene características adicionales que te ayudarán a probar tu sitio web o aplicación en varias posturas y orientaciones.  Elige **Girar** \( Girar \) para girar la ventanilla ![ a orientación ](../media/rotate-dark-icon.msft.png) horizontal. Combina la característica con **Span** \( Span \) para alternar entre una sola pantalla o con una pantalla doble o ![ ](../media/span-dark-icon.msft.png) posturas desenvolvadas.  Juntas, las características te permiten probar tu sitio web o aplicación en las cuatro posibles posturas y orientaciones.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matriz de posturas y orientaciones para dispositivos de doble pantalla y plegados" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matriz de posturas y orientaciones para dispositivos de doble pantalla y plegados  
:::image-end:::  

El **icono características de la plataforma** web experimental \( ExperimentalApis \) muestra el estado de la marca de características de ![ la plataforma web ](../media/experimental-apis-dark-icon.msft.png) **experimental.**  Si la marca está activada, se resalta el icono.  Si la marca está desactivada, el icono no se resalta.  Para activar \(o desactivar\) la marca, elige el icono o navega a `edge://flags` y alterna la marca.  

> [!NOTE]
> A continuación se muestra una lista de problemas conocidos actuales.  
> 
> *   Cuando usas un cliente de Escritorio remoto de [Microsoft][RemoteDesktopClientDocs] para conectarte a un equipo remoto y emular [Surface Duo][SurfaceDevicesDuo] o El plegado [Desconsudada de Samsung ,][SamsungMobileGalaxyFold]el puntero puede estremezárselo o estremezz.  Si tiene problemas con el problema, [envíe comentarios.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## Recursos adicionales  

Estos son recursos adicionales que pueden ayudarte a mejorar tu sitio web \(o app\) para dispositivos de pantalla doble.  

*   Para obtener más información sobre el desarrollo web en dispositivos de pantalla doble, vaya a [experiencias web de doble pantalla.][DualScreenWebIndex]  
*   Instala el [emulador de Surface Duo.][DualScreenAndroidUseEmulator]  El emulador de Surface Duo es diferente del emulador de Microsoft Edge, ejecuta Android y se integra con [Android Studio.][AndroidDeveloperStudio]  Para obtener más información, ve [a Obtener el SDK de Surface Duo.][DualScreenAndroidGetDuoSdk]  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias web de pantalla doble | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el emulador de Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la seam: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de pantalla multimedia CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Escritorio remoto | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
