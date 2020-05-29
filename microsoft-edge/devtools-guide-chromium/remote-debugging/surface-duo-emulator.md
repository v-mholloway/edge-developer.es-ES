---
title: Introducción a los emuladores de superficies de depuración remota Duo
author: zoherghadyali
ms.author: zoghadya
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, depuración remota, Android, Surface Duo
ms.openlocfilehash: af6fa6433b0bc6bba0599e6e9a805235504caadd
ms.sourcegitcommit: 966bfc60040acc794b6ee20eb2084bc8264a4852
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/05/2020
ms.locfileid: "10621505"
---
# Introducción a los emuladores de superficies de depuración remota Duo

En este artículo, encontrarás el proceso de depuración remota de contenido web en la [aplicación Microsoft Edge][AndroidEdge] en un emulador [Surface Duo][SurfaceDuo] desde una instancia de escritorio de [Microsoft Edge][DesktopEdge]. Para obtener información sobre la depuración en un dispositivo Surface Duo, siga nuestra guía para la [depuración remota de dispositivos Android][RemoteDebuggingAndroid].

## Antes de empezar

Instala el [SDK Surface Duo][DuoSdk] antes de ejecutar el [emulador Surface Duo][DuoEmulator]. Para obtener más información, vea [obtener el SDK de Surface Duo][DuoSdkdocs].

## Paso 1: vaya a edge://inspect

Abra una instancia de escritorio de [Microsoft Edge][DesktopEdge]y vaya a `edge://inspect` .

> ##### Figura 1  
> La `edge://inspect` Página de Microsoft Edge en el escritorio ![ la página Edge://Inspect de Microsoft Edge en el escritorio][ImageEdgeInspect]

> [!NOTE]
> Si la `edge://inspect` Página no reconoce el [emulador Surface Duo][DuoEmulator], reinicie el emulador.

## Paso 2: iniciar el emulador Surface Duo

Inicia el [emulador Surface Duo][DuoEmulator]. Observe que el emulador muestra dos pantallas diferentes ejecutándose en el emulador.

> ##### Figura 2
> Emulador Surface Duo, ![ el emulador Surface Duo][ImageDuoEmulator]  

## Paso 3: cargar el contenido web en Microsoft Edge en el emulador Surface Duo

En cualquiera de las dos pantallas, deslice el dedo hacia arriba en la bandeja favoritos del [emulador Surface Duo][DuoEmulator] para mostrar el cajón de aplicaciones. Elija **borde** para iniciar la [aplicación Microsoft Edge][AndroidEdge].

> ##### Imagen 3
> La aplicación Microsoft Edge en el emulador Surface Duo, ![ la aplicación Microsoft Edge en el emulador Surface Duo][ImageDuoEmulatorEdge]  

Navegue hasta el sitio web o la aplicación que quiera depurar en la [aplicación Microsoft Edge][AndroidEdge].

## Paso 4: Depure su contenido web desde el emulador Surface Duo 

Vuelva a la instancia de escritorio de [Microsoft Edge][DesktopEdge]. La `edge://inspect` página ahora muestra la **SurfaceDuoEmulator** con una lista de las pestañas abiertas o de [PWAs][PwaDocs] que se ejecutan en el [emulador Surface Duo][DuoEmulator].

> ##### Imagen 4
> La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador ![ la página Edge://Inspect muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador][ImageEdgeInspectTargets]  

> [!NOTE]
> Si no ve **SurfaceDuoEmulator** en la `edge://inspect` página, intente abrir o cerrar las pestañas en la [aplicación Microsoft Edge][AndroidEdge] en el [emulador Surface Duo][DuoEmulator]. Para obtener instrucciones adicionales para la solución de problemas, consulte la [sección solución de problemas para dispositivos Android][TroubleshootingAndroid].

En la lista de las pestañas abiertas que se ejecutan en el emulador, elija **inspeccionar** en la pestaña que tiene el contenido web que se va a depurar. El [DevTools de Microsoft Edge][DevToolsDocs] se abrirá en una ventana nueva. Elija **activar o desactivar** screencast de la demostración ![ ][ImageToggleScreencastIcon] para ver el contenido web desde el [emulador Surface Duo][DuoEmulator] en la ventana DevTools. Ahora puede usar el DevTools de Microsoft Edge para depurar su contenido web en el [emulador Surface Duo][DuoEmulator].

> ##### Imagen 5
> Usar el DevTools de Microsoft Edge para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo con el emulador de ![ Microsoft Edge DevTools para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo][ImageDevTools]  

> [!NOTE]
> Si abarca la [aplicación Microsoft Edge][AndroidEdge] en las dos pantallas del emulador, el screencast reflejará el nuevo tamaño de la aplicación, pero no la articulación. Para comprender cómo la bisagra afecta al diseño de su contenido Web, use el [emulador Surface Duo][DuoEmulator] en lugar del screencast.

## Recursos adicionales

La web es una excelente plataforma para la nueva clase de plegable y dispositivos de pantalla dual porque puedes escribir una vez HTML, CSS y JavaScript y hacer que tenga un aspecto excelente en los dispositivos de pantalla única, dual y plegable. Para obtener más información, vea estos recursos adicionales para empezar a crear contenido web para estos dispositivos nuevos.

- [Documentación para crear aplicaciones en dispositivos de doble pantalla][DualScreenDocs]
- [El explicación de la plataforma web Microsoft Edge para nuevas API para crear experiencias Web en dispositivos de plegable y de doble pantalla][WebPlatformExplainer]
- [Grabación de la sesión del día del desarrollador de 365 de Microsoft: Cómo crear experiencias en dos pantallas para sitios web y aplicaciones Web][DeveloperDay]

<!-- image links -->  
[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page.msft.png "Ilustración 1: la página edge://inspect en Microsoft Edge en el escritorio"
[ImageDuoEmulator]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator.msft.png "Ilustración 2: el emulador Surface Duo"
[ImageDuoEmulatorEdge]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator-edge.msft.png "Ilustración 3: la aplicación Microsoft Edge en el emulador Surface Duo"
[ImageEdgeInspectTargets]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png "Ilustración 4: la página edge://inspect muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador"
[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png
[ImageDevTools]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-devtools.msft.png "Ilustración 5: usar el DevTools de Microsoft Edge para depurar Bing en la aplicación Microsoft Edge en el emulador Surface Duo"

<!-- links -->  
[RemoteDebuggingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introducción a la depuración remota dispositivos Android"
[PwaDocs]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows"
[DevToolsDocs]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"
[TroubleshootingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index#troubleshooting-devtools-is-not-detecting-the-android-device "Solución de problemas: DevTools no detecta el dispositivo Android"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicación Microsoft Edge Android"
[SurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Presentamos Surface Duo"
[DesktopEdge]: https://www.microsoft.com/edge/ "Presentamos el nuevo Microsoft Edge"
[DuoEmulator]: https://docs.microsoft.com/dual-screen/android/use-emulator "Usar el emulador Surface DUo"
[DuoSdk]: https://www.microsoft.com/download/details.aspx?id=100847 "Versión preliminar del SDK de Surface Duo"
[DuoSdkDocs]: https://docs.microsoft.com/dual-screen/android/get-duo-sdk "Obtener el SDK Surface Duo"
[DualScreenDocs]: https://docs.microsoft.com/dual-screen/ "Crear aplicaciones para dispositivos de doble pantalla"
[WebPlatformExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitivas de plataforma web para experiencias habilitadas en dispositivos plegable"
[DeveloperDay]: https://youtu.be/DXrZWsqXPVc "Cómo crear experiencias en pantalla dual para el sitio web y las aplicaciones Web"
