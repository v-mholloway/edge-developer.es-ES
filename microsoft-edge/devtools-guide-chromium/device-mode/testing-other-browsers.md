---
description: El trabajo no termina asegurando que el sitio se ejecute bien en Microsoft Edge y Android.  Aunque el modo dispositivo es capaz de simular una variedad de otros dispositivos como iPhones, te recomendamos que consultes las soluciones de emulación proporcionadas por otros exploradores.
title: Emular y probar otros exploradores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 22153a54df7c5b92236a745be8e3bbac9a52d247
ms.sourcegitcommit: fa8bedfc83fbd1c4ce7bda8c69586c4f24007beb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "11481369"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="emulate-and-test-other-browsers"></a>Emular y probar otros exploradores  

El trabajo no termina asegurando que el sitio se ejecute bien en Microsoft Edge y Android.  Aunque el modo dispositivo es capaz de simular una variedad de otros dispositivos como iPhones, te recomendamos que consultes las soluciones de emulación proporcionadas por otros exploradores.  

### <a name="summary"></a>Resumen  

*   Cuando no tienes un dispositivo en particular o quieres hacer una comprobación de puntos en algo, la mejor opción es emular el dispositivo directamente dentro del explorador.  
*   Los emuladores y simuladores de dispositivos te permiten imitar el sitio de desarrollo en una amplia variedad de dispositivos de la estación de trabajo.  
*   Los emuladores basados en la nube permiten automatizar las pruebas unitarias de su sitio en diferentes plataformas.  

## <a name="browser-emulators"></a>Emuladores de explorador  

Los emuladores de explorador son excelentes para probar la capacidad de respuesta de un sitio, pero cada uno no emula las diferencias en api, compatibilidad con CSS y determinados comportamientos que se muestran en un explorador móvil.  Pruebe el sitio en exploradores que se ejecutan en dispositivos reales para que todo se comporte como se esperaba.  

### <a name="firefox-responsive-design-view"></a>Vista Diseño dinámico de Firefox  

Firefox tiene una [vista de][MDNResponsiveDesignMode] diseño adaptable que te anima a dejar de pensar en términos de dispositivos específicos y, en su lugar, explorar cómo cambia el diseño en tamaños de pantalla comunes o tu propio tamaño arrastrando los bordes.  

### <a name="edgehtml-emulation"></a>Emulación edgeHTML  

Para emular Windows Phones, usa la [emulación][ArchiveMicrosoftEdgeDevtoolsEmulation]integrada de Microsoft Edge \(EdgeHTML\).  

Usa [la emulación de IE 11][Ie11DevToolsEmulation] para simular el aspecto de tu página en versiones anteriores de Internet Explorer.  

## <a name="device-emulators-and-simulators"></a>Emuladores y simuladores de dispositivos  

Los simuladores y emuladores de dispositivo simulan no solo el entorno del explorador, sino todo el dispositivo.  Cada uno es útil para probar cosas que requieren la integración del sistema operativo, por ejemplo, la entrada de formulario con teclados virtuales.  

### <a name="android-emulator"></a>Emulador de Android  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

Por el momento, no hay forma de instalar Microsoft Edge en un emulador de Android.  Sin embargo, puede usar el Explorador de Android, el Shell de contenido chromium y Firefox para Android que revisaremos más adelante en esta guía.  Chromium Content Shell ejecuta el mismo motor de representación de Chromium que Microsoft Edge, pero viene sin ninguna de las características específicas del explorador.  

El emulador de Android viene con el SDK de Android que necesitas descargar como parte de [Android Studio][AndroidStudioDownload].  A continuación, siga [las instrucciones para configurar un dispositivo virtual e][AndroidStudioCreateManageVirtualDevices] iniciar el [emulador][AndroidStudioRunAppsAndroidEmulator].  
Una vez que se inicie el emulador, elija en el icono Explorador y pruebe el sitio en el antiguo Explorador de acciones para Android.  

#### <a name="chromium-content-shell-on-android"></a>Shell de contenido chromium en Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Para instalar el Shell de contenido de Chromium para Android, deje el emulador en ejecución y ejecute el siguiente comando.  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Ahora puede probar su sitio con el Shell de contenido de Chromium.  

#### <a name="firefox-on-android"></a>Firefox en Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

Al igual que el Shell de contenido de Chromium, puedes obtener un APK para instalar Firefox en el emulador.  

[Descargue el archivo .apk correcto.][MozillaFirefoxDownload]  

Para instalar el archivo en un emulador abierto o un dispositivo Android conectado, ejecute el siguiente comando.  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a>Simulador de iOS  

El simulador de iOS para Mac OS X viene con Xcode, que se [instala desde la Tienda de aplicaciones.][MacAppStoreXcode]  

Cuando haya terminado, obtenga información sobre cómo trabajar con el simulador a través de la [documentación del desarrollador de Apple][AppleSimulatorHelp].  

> [!NOTE]
> Para evitar tener que abrir Xcode cada vez que quiera usar el simulador de iOS, ábralo, mantenga el mouse en el icono simulador de iOS en el dock, abra el menú contextual \(haga clic con el botón secundario\) y elija Mantener en **dock**.  Ahora solo tienes que elegir el icono siempre que lo necesites.  

###  <a name="microsoft-edge-edgehtml"></a>Microsoft Edge (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Máquina virtual IE moderna" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   Máquina virtual IE moderna  
:::image-end:::  

Las máquinas virtuales \(VM\) de Microsoft Edge \(EdgeHTML\) permiten tener acceso a diferentes versiones de EdgeHTML e IE en el equipo a través de VirtualBox \(o VMWare\).  Elija una [máquina virtual en la página de descarga][MicrosoftDeveloperEdgeVms].  

## <a name="cloud-based-emulators-and-simulators"></a>Emuladores y simuladores basados en la nube  

Si no puedes usar los emuladores y no tienes acceso a dispositivos reales, los emuladores basados en la nube son lo siguiente mejor.  Una gran ventaja de los emuladores basados en la nube sobre dispositivos reales y emuladores locales es que puede automatizar las pruebas unitarias de su sitio en diferentes plataformas.  

*   [BrowserStack (comercial)][|::ref1::|] es el más fácil de usar para pruebas manuales.  Seleccionas un sistema operativo, seleccionas la versión del explorador y el tipo de dispositivo, seleccionas una dirección URL para examinar y gira hacia arriba una máquina virtual hospedada con la que puedes interactuar.  También puedes ejecutar varios emuladores en la misma pantalla, lo que te permite probar la apariencia de la aplicación en varios dispositivos al mismo tiempo.  
*   [SauceLabs (comercial)][SauceLabs] permite ejecutar pruebas unitarias dentro de un emulador, lo que puede ser realmente útil para secuencias de comandos de un flujo a través del sitio y ver la grabación de vídeo de esto después en varios dispositivos.  También puede realizar pruebas manuales con su sitio.  
*   [Device Anywhere (comercial)][AppExperience] no usa emuladores, sino dispositivos reales que puedes controlar de forma remota.  Esto es muy útil en caso de que necesites reproducir un problema en un dispositivo específico y puede que no muestres el error con ninguna de las opciones de las guías anteriores.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[ArchiveMicrosoftEdgeDevtoolsEmulation]: /archive/microsoft-edge/legacy/developer/devtools-guide/emulation "Emulación | Microsoft Docs"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Emular exploradores, tamaños de pantalla y ubicaciones DE GPS | Microsoft Docs"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Descargar máquinas virtuales"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Crear y administrar dispositivos virtuales | Desarrolladores de Android"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Descargar herramientas de Android Studio y SDK | Desarrolladores de Android"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Ejecutar aplicaciones en el emulador de Android | Desarrolladores de Android"  

[AppExperience]: https://www.sigos.com/app-experience/ "Experiencia de la aplicación"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Ayuda del simulador: configuración | manzana"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode en la Mac App Store"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Modo de diseño dinámico | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Descargar el explorador Firefox"  
[SauceLabs]: https://saucelabs.com "Laboratorios de salsa"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original [](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) se encuentra aquí y es creado por [Meggin Kearney][MegginKearney] \(Tech Writer\) y [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate en Google | Herramientas, Rendimiento, Animación, UX\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de una [Licencia internacional de Atribución de Creative Commons 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
