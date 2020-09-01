---
title: Emular y probar otros exploradores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d5eb33ea4cd1224930e91898d2c711310202cfc0
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984986"
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





# Emular y probar otros exploradores   




Su trabajo no finaliza con la garantía de que su sitio funciona de forma excelente en Microsoft Edge y Android.  Aunque el modo de dispositivo pueda simular una variedad de dispositivos como iPhone, le recomendamos que consulte las soluciones para la emulación proporcionadas por otros exploradores.  

### Resumen  

*   Si no tiene un dispositivo en particular o desea realizar una comprobación puntual en algo, la mejor opción es emular el dispositivo directamente en el explorador.  
*   Los emuladores y simuladores de dispositivos le permiten imitar su sitio de desarrollo en un intervalo de dispositivos de su estación de trabajo.  
*   Los emuladores basados en la nube permiten automatizar las pruebas unitarias de su sitio a través de diferentes plataformas.  

## Emuladores del explorador  

Los emuladores de explorador son ideales para probar la capacidad de respuesta de un sitio, pero cada uno de ellos no emula las diferencias en la API, la compatibilidad con CSS y determinados comportamientos que se pueden ver en un explorador móvil.  Pruebe su sitio en exploradores que se ejecutan en dispositivos reales para asegurarse de que todo funciona como se espera.  

### Vista diseño dinámico de Firefox  

Firefox tiene una [vista de diseño con capacidad de respuesta][MDNResponsiveDesignMode] que le anima a dejar de pensar en términos de dispositivos específicos y, en su lugar, explorar cómo cambia el diseño en tamaños de pantalla comunes o su propio tamaño arrastrando los bordes.  

### Emulación de EdgeHTML  

Para emular teléfonos con Windows, use la [emulación integrada][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).  

Use la [emulación de IE 11][Ie11DevToolsEmulation] para simular el aspecto que tendrá la página en versiones anteriores de Internet Explorer.  

## Emuladores y simuladores de dispositivos  

Los simuladores y simuladores de dispositivos simulan no solo el entorno del explorador, sino el dispositivo completo.  Cada uno es útil para probar las cosas que requieren integración del sistema operativo, por ejemplo, la entrada de datos con teclados virtuales.  

### Emulador de Android  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

Por el momento, no hay ninguna forma de instalar Microsoft Edge en un emulador Android.  Sin embargo, puede usar el explorador Android, el shell de contenido de cromo y Firefox para Android que revisamos más adelante en esta guía.  El shell de contenido de cromo ejecuta el mismo motor de procesamiento de cromo que Microsoft Edge, pero sin ninguna de las características específicas del explorador.  

El emulador de Android viene con el SDK de Android que necesita descargar como parte de [Android Studio][AndroidStudioDownload].  A continuación, siga las instrucciones para [configurar un dispositivo virtual][AndroidStudioCreateManageVirtualDevices] e [iniciar el emulador][AndroidStudioRunAppsAndroidEmulator].  
Una vez que se haya arrancado el emulador, haga clic en el icono del explorador y pruebe su sitio en el antiguo explorador de cotizaciones para Android.  

#### Shell de contenido de cromo en Android  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

Para instalar el shell de contenido de cromo para Android, deje el emulador ejecutándose y ejecute el siguiente comando.  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

Ahora puede probar su sitio con el shell de contenido de cromo.  

#### Firefox en Android  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

Al igual que el shell de contenido de cromo, puede obtener una APK para instalar Firefox en el emulador.  

[Descargue el archivo. apk correcto][MozillaFirefoxDownload].  

Para instalar el archivo en un emulador abierto o en un dispositivo Android conectado, ejecute el siguiente comando.  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### simulador iOS  

El simulador iOS para Mac OS X viene con Xcode, que se [instala desde la App Store][MacAppStoreXcode].  

Cuando haya terminado, obtenga información sobre cómo trabajar con el simulador a través de la [documentación para desarrolladores de Apple][AppleSimulatorHelp].  

> [!NOTE]
> Para evitar tener que abrir Xcode cada vez que desee usar el simulador iOS, ábralo, luego haga clic con el botón derecho en el icono del simulador iOS en el Dock y seleccione **mantener en Dock**.  Ahora solo tienes que hacer clic en este icono cuando lo necesites.  

###  Microsoft Edge (EdgeHTML)  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="VM moderna de IE" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   VM moderna de IE  
:::image-end:::  

Microsoft Edge \ (EdgeHTML \) las máquinas virtuales \ (VMs \) te permiten acceder a diferentes versiones de EdgeHTML e IE en tu equipo a través de VirtualBox \ (o VMWare \).  Elija una [máquina virtual en la página de descarga][MicrosoftDeveloperEdgeVms].  

## Emuladores y simuladores basados en la nube  

Si no puede usar los emuladores y no tiene acceso a dispositivos reales, los emuladores basados en la nube son la mejor opción.  Una gran ventaja de los emuladores basados en la nube en los dispositivos reales y en los emuladores locales es que puede automatizar las pruebas unitarias de su sitio a través de distintas plataformas.  

*   [BrowserStack (comercial)][|::ref1::|] es el más fácil de usar para pruebas manuales.  Seleccione un sistema operativo, seleccione la versión del explorador y el tipo de dispositivo, seleccione una dirección URL para explorar y una máquina virtual hospedada con la que pueda interactuar.  También puedes ejecutar varios emuladores en la misma pantalla, lo que te permite probar la apariencia de la aplicación en varios dispositivos al mismo tiempo.  
*   [SauceLabs (Commercial)][SauceLabs] le permite ejecutar pruebas unitarias dentro de un emulador, que pueden ser muy útiles para crear secuencias de comandos en su sitio y observar la grabación de vídeo de este después en varios dispositivos.  También puede realizar pruebas manuales con su sitio.  
*   El [dispositivo en cualquier lugar (comercial)][AppExperience] no usa emuladores pero dispositivos reales que puedas controlar de forma remota.  Esto es muy útil en el caso de que necesite reproducir un problema en un dispositivo específico y no pueda ver el error utilizando cualquiera de las opciones de las guías anteriores.  

<!--  
 


-->  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML): emulación | Microsoft docs"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Emular exploradores, tamaños de pantalla y ubicaciones GPS | Microsoft docs"  

[MicrosoftDeveloperEdgeVms]: https://developer.microsoft.com/microsoft-edge/tools/vms "Descargar máquinas virtuales"  

[AndroidStudioCreateManageVirtualDevices]: https://developer.android.com/tools/devices/managing-avds.html "Crear y administrar dispositivos virtuales | Desarrolladores de Android"  
[AndroidStudioDownload]:  https://developer.android.com/sdk/installing/studio.html "Descargar herramientas de Android Studio y SDK | Desarrolladores de Android"  
[AndroidStudioRunAppsAndroidEmulator]: https://developer.android.com/tools/devices/emulator.html "Ejecutar aplicaciones en el emulador de Android | Desarrolladores de Android"  

[AppExperience]: https://www.sigos.com/app-experience/ "Experiencia de la aplicación"  
[AppleSimulatorHelp]: https://help.apple.com/simulator/mac/current "Ayuda del simulador: actual | Apple"  
[BrowserStack]: https://www.browserstack.com/automate "BrowserStack"  
[MacAppStoreXcode]: https://itunes.apple.com/app/xcode/id497799835 "Xcode en la tienda de aplicaciones para Mac"  
[MDNResponsiveDesignMode]: https://developer.mozilla.org/docs/Tools/Responsive_Design_View "Modo de diseño dinámico | MDN"  
[MozillaFirefoxDownload]: https://www.mozilla.org/firefox/all/#product-android-beta "Descargar el explorador Firefox"  
[SauceLabs]: https://saucelabs.com "Prácticas de salsa"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Paul Bakaus][PaulBakaus] \ (abrir el sitio web para desarrolladores de Google | Herramientas, rendimiento, animación, UX \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
