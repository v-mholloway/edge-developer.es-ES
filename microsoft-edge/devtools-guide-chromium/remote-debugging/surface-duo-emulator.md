---
description: Introducción a los emuladores de superficies de depuración remota Duo.
title: Introducción a los emuladores de superficies de depuración remota Duo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, depuración remota, Android, Surface Duo
ms.openlocfilehash: f44c85c468de3bdd7727695e3f33269584966231
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230659"
---
# Introducción a los emuladores de superficies de depuración remota Duo  

En este artículo, encontrarás el proceso de depuración remota de contenido web en la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en un emulador [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] desde una instancia de escritorio de [Microsoft Edge][MicrosoftEdge].  Para obtener información sobre la depuración en un dispositivo Surface Duo, siga nuestra guía para la [depuración remota de dispositivos Android][DevtoolsRemoteDebuggingMain].  

## Antes de empezar

Instala el [SDK Surface Duo][MicrosoftDownload100847] antes de ejecutar el [emulador Surface Duo][DualScreenAndroidUseEmulator].  Para obtener más información, vea [obtener el SDK de Surface Duo][DualScreenAndroidGetDuoSdk].  

## Paso 1: vaya a edge://inspect  

Abra una instancia de escritorio de [Microsoft Edge][MicrosoftEdge]y vaya a `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="La página edge://inspect en Microsoft Edge en el escritorio" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   La `edge://inspect` página en Microsoft Edge en el escritorio  
:::image-end:::

> [!NOTE]
> Si la `edge://inspect` Página no reconoce el [emulador Surface Duo][DualScreenAndroidUseEmulator], reinicie el emulador.  

## Paso 2: iniciar el emulador Surface Duo  

Inicia el [emulador Surface Duo][DualScreenAndroidUseEmulator].  Observe que el emulador muestra dos pantallas diferentes ejecutándose en el emulador.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   Emulador Surface Duo  
:::image-end:::  

## Paso 3: cargar el contenido web en Microsoft Edge en el emulador Surface Duo  

En cualquiera de las dos pantallas, deslice el dedo hacia arriba en la bandeja favoritos del [emulador Surface Duo][DualScreenAndroidUseEmulator] para mostrar el cajón de aplicaciones.  Elija **borde** para iniciar la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="La aplicación Microsoft Edge en el emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   La aplicación Microsoft Edge en el emulador Surface Duo  
:::image-end:::  

Navegue hasta el sitio web o la aplicación que quiera depurar en la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].  

## Paso 4: Depure su contenido web desde el emulador Surface Duo  

Vuelva a la instancia de escritorio de [Microsoft Edge][MicrosoftEdge].  La `edge://inspect` página ahora muestra la **SurfaceDuoEmulator** con una lista de las pestañas abiertas o de [PWAs][ProgressiveWebAppsIndex] que se ejecutan en el [emulador Surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La página edge://inspect muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador  
:::image-end:::  

> [!NOTE]
> Si no ve **SurfaceDuoEmulator** en la `edge://inspect` página, intente abrir o cerrar las pestañas en la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en el [emulador Surface Duo][DualScreenAndroidUseEmulator].  Para obtener instrucciones adicionales para la solución de problemas, consulte la [sección solución de problemas para dispositivos Android][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].  

En la lista de las pestañas abiertas que se ejecutan en el emulador, elija **inspeccionar** en la pestaña que tiene el contenido web que se va a depurar.  El [DevTools de Microsoft Edge][DevtoolsIndex] se abrirá en una ventana nueva.  Elija **alternar screencast** \ ( ![ alternar screencast ][ImageToggleScreencastIcon] \) para ver el contenido web desde el [emulador Surface Duo][DualScreenAndroidUseEmulator] en la ventana DevTools.  Ahora puede usar el DevTools de Microsoft Edge para depurar su contenido web en el [emulador Surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Usar el DevTools de Microsoft Edge para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Usar el DevTools de Microsoft Edge para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo  
:::image-end:::  

> [!NOTE]
> Si abarca la [aplicación Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] en las dos pantallas del emulador, el screencast reflejará el nuevo tamaño de la aplicación, pero no la articulación.  Para comprender cómo la bisagra afecta al diseño de su contenido Web, use el [emulador Surface Duo][DualScreenAndroidUseEmulator] en lugar del screencast.  

## Recursos adicionales  

La web es una excelente plataforma para la nueva clase de plegable y dispositivos de pantalla dual porque puedes escribir una vez HTML, CSS y JavaScript y hacer que tenga un aspecto excelente en los dispositivos de pantalla única, dual y plegable.  Para obtener más información, vea estos recursos adicionales para empezar a crear contenido web para estos dispositivos nuevos.  

*   [Documentación para crear aplicaciones en dispositivos de doble pantalla][DualScreenIndex]  
*   [El explicación de la plataforma web Microsoft Edge para nuevas API para crear experiencias Web en dispositivos de plegable y de doble pantalla][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Grabación de la sesión del día del desarrollador de 365 de Microsoft: Cómo crear experiencias en dos pantallas para sitios web y aplicaciones Web][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Aplicaciones web progresivas en Windows | Microsoft docs"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Introducción a la depuración remota dispositivos Android | Microsoft docs"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Solución de problemas: DevTools no detecta el dispositivo Android: Introducción a la depuración remota dispositivos Android | Microsoft docs"  

[DualScreenIndex]: /dual-screen/index "Crear aplicaciones para dispositivos de doble pantalla | Microsoft docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usar el emulador Surface DUo | Microsoft docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el SDK Surface Duo | Microsoft docs"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Presentamos el nuevo Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "La nueva superficie | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Descargar Surface Duo SDK Preview versión | Centro de descarga de Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: explorador Web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma web para experiencias habilitadas en dispositivos plegable: MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Cómo crear experiencias en dos pantallas para el sitio web y aplicaciones Web | YouTube"  
