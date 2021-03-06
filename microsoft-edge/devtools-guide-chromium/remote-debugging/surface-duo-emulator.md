---
description: Introducción a los emuladores de Surface Duo de depuración remota.
title: Introducción a los emuladores de Surface Duo de depuración remota
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, depuración remota, android, surface duo
ms.openlocfilehash: a9696e63528a674d349b78fbdec2a1b804f61c49
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398017"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a>Introducción a los emuladores de Surface Duo de depuración remota  

En este artículo, describes el proceso de depuración remota del contenido web en la aplicación [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en un emulador de [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] desde una instancia de escritorio de Microsoft [Edge][MicrosoftEdge].  Para obtener información sobre la depuración en un dispositivo Surface Duo, sigue nuestra guía para la depuración remota [de dispositivos Android.][DevtoolsRemoteDebuggingMain]  

## <a name="before-you-begin"></a>Antes de comenzar

Instala el [SDK de Surface Duo][MicrosoftDownload100847] antes de ejecutar el emulador de Surface [Duo][DualScreenAndroidUseEmulator].  Para obtener más información, ve [a Obtener el SDK de Surface Duo][DualScreenAndroidGetDuoSdk].  

## <a name="step-1-navigate-to-edgeinspect"></a>Paso 1: Vaya a edge://inspect  

Abra una instancia de escritorio de [Microsoft Edge][MicrosoftEdge]y vaya a `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="La edge://inspect de Microsoft Edge en el escritorio" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   La `edge://inspect` página de Microsoft Edge en el escritorio  
:::image-end:::

> [!NOTE]
> Si la `edge://inspect` página no reconoce el emulador de Surface [Duo,][DualScreenAndroidUseEmulator]reinicia el emulador.  

## <a name="step-2-launch-the-surface-duo-emulator"></a>Paso 2: Iniciar el emulador de Surface Duo  

Inicia el [emulador de Surface Duo][DualScreenAndroidUseEmulator].  Observe que el emulador muestra 2 pantallas diferentes que se ejecutan en el emulador.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Emulador de Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   Emulador de Surface Duo  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a>Paso 3: Cargar el contenido web en Microsoft Edge en el emulador de Surface Duo  

En cualquier pantalla, desliza el dedo hacia arriba en la Bandeja de favoritos del emulador [de Surface Duo][DualScreenAndroidUseEmulator] para mostrar el cajón de aplicaciones.  Elija **Edge** para iniciar la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="La aplicación Microsoft Edge en el emulador de Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   La aplicación Microsoft Edge en el emulador de Surface Duo  
:::image-end:::  

Navegue hasta el sitio web o la aplicación que desea depurar en la [aplicación de Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a>Paso 4: Depurar el contenido web desde el emulador de Surface Duo  

Vuelva a la instancia de escritorio de [Microsoft Edge][MicrosoftEdge].  La `edge://inspect` página ahora muestra **SurfaceDuoEmulator** con una lista de las pestañas abiertas o [pwas][ProgressiveWebAppsIndex] que se ejecutan en el emulador [de Surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La edge://inspect muestra una lista de las pestañas abiertas en la aplicación de Microsoft Edge que se ejecuta en el emulador" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación microsoft edge que se ejecuta en el emulador  
:::image-end:::  

> [!NOTE]
> Si **SurfaceDuoEmulator** no se muestra en la página, intenta abrir o cerrar pestañas en la aplicación Microsoft Edge en `edge://inspect` el emulador de Surface [Duo][DualScreenAndroidUseEmulator]. [][GooglePlayStoreAppsComMicrosoftEmmx]  Para obtener pasos adicionales de solución de problemas, vaya a la sección [de solución de problemas para dispositivos Android][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].  

En la lista de pestañas abiertas que se ejecutan en el emulador, elija **Inspeccionar** en la pestaña que tiene el contenido web que se va a depurar.  Microsoft [Edge DevTools][DevtoolsIndex] se abrirá en una nueva ventana.  Elige **Alternar difusión** de pantalla \( Alternar difusión por pantalla \) para ver el contenido web desde el emulador ![ de Surface ][ImageToggleScreencastIcon] [Duo][DualScreenAndroidUseEmulator] en la ventana DevTools.  Ahora puedes usar Microsoft Edge DevTools para depurar el contenido web en el emulador [de Surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Uso de Microsoft Edge DevTools para depurar Bing en la aplicación Microsoft Edge en el emulador de Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Uso de Microsoft Edge DevTools para depurar Bing en la aplicación Microsoft Edge en el emulador de Surface Duo  
:::image-end:::  

> [!NOTE]
> Si abarcas la [aplicación de Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en ambas pantallas del emulador, la difusión en pantalla reflejará el nuevo tamaño de la aplicación, pero no la bisagra.  Para comprender cómo afecta la bisagra al diseño del contenido web, usa el [emulador de Surface Duo][DualScreenAndroidUseEmulator] en lugar de la difusión por pantalla.  

## <a name="additional-resources"></a>Recursos adicionales  

La web es una excelente plataforma para la nueva clase de dispositivos de doble pantalla y plegados, ya que puede escribir html, CSS y JavaScript una vez y tener un aspecto excelente en dispositivos de pantalla única, doble pantalla y plegados.  Para obtener más información, vaya a los siguientes recursos adicionales para empezar a crear contenido web para estos nuevos dispositivos.  

*   [Documentación para crear aplicaciones en dispositivos de pantalla doble][DualScreenIndex]  
*   [El explicador de la plataforma web de Microsoft Edge para nuevas API para crear experiencias web en dispositivos de doble pantalla y plegados][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Grabación de la sesión del Día del desarrollador de Microsoft 365: cómo crear experiencias de pantalla doble para sitios web y aplicaciones web][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Aplicaciones web progresivas en Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Solución de problemas: DevTools no detecta el dispositivo Android: introducción a la depuración remota de dispositivos Android | Microsoft Docs"  

[DualScreenIndex]: /dual-screen/index "Crear aplicaciones para dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface DUo | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el SDK de Surface Duo | Microsoft Docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Presentación del nuevo Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "El nuevo surface duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Descargar Surface Duo SDK Preview Release | Centro de descarga de Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: Explorador web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivos de plataforma web para experiencias ilustradas en dispositivos plegables: MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Cómo crear experiencias de pantalla doble para el sitio web y las aplicaciones web | YouTube"  
