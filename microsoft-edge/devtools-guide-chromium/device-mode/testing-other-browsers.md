---
title: Emular y probar otros exploradores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 65ad10ff89d3e4c27abc97cea0eb18b15853dd2e
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607312"
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





# <span data-ttu-id="3eae1-103">Emular y probar otros exploradores</span><span class="sxs-lookup"><span data-stu-id="3eae1-103">Emulate and Test Other Browsers</span></span>   




<span data-ttu-id="3eae1-104">Su trabajo no finaliza con la garantía de que su sitio funciona de forma excelente en Microsoft Edge y Android.</span><span class="sxs-lookup"><span data-stu-id="3eae1-104">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="3eae1-105">Aunque el modo de dispositivo pueda simular una variedad de dispositivos como iPhone, le recomendamos que consulte las soluciones para la emulación proporcionadas por otros exploradores.</span><span class="sxs-lookup"><span data-stu-id="3eae1-105">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <span data-ttu-id="3eae1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="3eae1-106">Summary</span></span>  

*   <span data-ttu-id="3eae1-107">Si no tiene un dispositivo en particular o desea realizar una comprobación puntual en algo, la mejor opción es emular el dispositivo directamente en el explorador.</span><span class="sxs-lookup"><span data-stu-id="3eae1-107">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="3eae1-108">Los emuladores y simuladores de dispositivos le permiten imitar su sitio de desarrollo en un intervalo de dispositivos de su estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="3eae1-108">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="3eae1-109">Los emuladores basados en la nube permiten automatizar las pruebas unitarias de su sitio a través de diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="3eae1-109">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <span data-ttu-id="3eae1-110">Emuladores del explorador</span><span class="sxs-lookup"><span data-stu-id="3eae1-110">Browser emulators</span></span>  

<span data-ttu-id="3eae1-111">Los emuladores de explorador son ideales para probar la capacidad de respuesta de un sitio, pero cada uno de ellos no emula las diferencias en la API, la compatibilidad con CSS y determinados comportamientos que se pueden ver en un explorador móvil.</span><span class="sxs-lookup"><span data-stu-id="3eae1-111">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that you see on a mobile browser.</span></span>  <span data-ttu-id="3eae1-112">Pruebe su sitio en exploradores que se ejecutan en dispositivos reales para asegurarse de que todo funciona como se espera.</span><span class="sxs-lookup"><span data-stu-id="3eae1-112">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <span data-ttu-id="3eae1-113">Vista diseño dinámico de Firefox</span><span class="sxs-lookup"><span data-stu-id="3eae1-113">Firefox Responsive Design View</span></span>  

<span data-ttu-id="3eae1-114">Firefox tiene una [vista de diseño con capacidad de respuesta][MDNResponsiveDesignMode] que le anima a dejar de pensar en términos de dispositivos específicos y, en su lugar, explorar cómo cambia el diseño en tamaños de pantalla comunes o su propio tamaño arrastrando los bordes.</span><span class="sxs-lookup"><span data-stu-id="3eae1-114">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <span data-ttu-id="3eae1-115">Emulación de EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="3eae1-115">EdgeHTML Emulation</span></span>  

<span data-ttu-id="3eae1-116">Para emular teléfonos con Windows, use la [emulación integrada][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="3eae1-116">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][DevToolsEdgeHtmlEmulation].</span></span>  

<span data-ttu-id="3eae1-117">Use la [emulación de IE 11][Ie11DevToolsEmulation] para simular el aspecto que tendrá la página en versiones anteriores de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3eae1-117">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <span data-ttu-id="3eae1-118">Emuladores y simuladores de dispositivos</span><span class="sxs-lookup"><span data-stu-id="3eae1-118">Device emulators and simulators</span></span>  

<span data-ttu-id="3eae1-119">Los simuladores y simuladores de dispositivos simulan no solo el entorno del explorador, sino el dispositivo completo.</span><span class="sxs-lookup"><span data-stu-id="3eae1-119">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="3eae1-120">Cada uno es útil para probar las cosas que requieren integración del sistema operativo, por ejemplo, la entrada de datos con teclados virtuales.</span><span class="sxs-lookup"><span data-stu-id="3eae1-120">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <span data-ttu-id="3eae1-121">Emulador de Android</span><span class="sxs-lookup"><span data-stu-id="3eae1-121">Android Emulator</span></span>  

<!--
> ##### Figure old 1  
> Stock Browser in Android Emulator  
> ![Stock Browser in Android Emulator][ImageAndroidEmulatorStockBrowser]  
-->

<span data-ttu-id="3eae1-122">Por el momento, no hay ninguna forma de instalar Microsoft Edge en un emulador Android.</span><span class="sxs-lookup"><span data-stu-id="3eae1-122">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="3eae1-123">Sin embargo, puede usar el explorador Android, el shell de contenido de cromo y Firefox para Android que revisamos más adelante en esta guía.</span><span class="sxs-lookup"><span data-stu-id="3eae1-123">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="3eae1-124">El shell de contenido de cromo ejecuta el mismo motor de procesamiento de cromo que Microsoft Edge, pero sin ninguna de las características específicas del explorador.</span><span class="sxs-lookup"><span data-stu-id="3eae1-124">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="3eae1-125">El emulador de Android viene con el SDK de Android que necesita descargar como parte de [Android Studio][AndroidStudioDownload].</span><span class="sxs-lookup"><span data-stu-id="3eae1-125">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="3eae1-126">A continuación, siga las instrucciones para [configurar un dispositivo virtual][AndroidStudioCreateManageVirtualDevices] e [iniciar el emulador][AndroidStudioRunAppsAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="3eae1-126">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="3eae1-127">Una vez que se haya arrancado el emulador, haga clic en el icono del explorador y pruebe su sitio en el antiguo explorador de cotizaciones para Android.</span><span class="sxs-lookup"><span data-stu-id="3eae1-127">Once your emulator is booted, click on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <span data-ttu-id="3eae1-128">Shell de contenido de cromo en Android</span><span class="sxs-lookup"><span data-stu-id="3eae1-128">Chromium Content Shell on Android</span></span>  

<!--
> ##### Figure old 2  
> Android Emulator Content Shell  
> ![Android Emulator Content Shell][ImageAndroidEmulatorContentShell]  
-->

<span data-ttu-id="3eae1-129">Para instalar el shell de contenido de cromo para Android, deje el emulador ejecutándose y ejecute los siguientes comandos en un símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="3eae1-129">To install the Chromium Content Shell for Android, leave your emulator running and run the following commands at a command prompt:</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="3eae1-130">Ahora puede probar su sitio con el shell de contenido de cromo.</span><span class="sxs-lookup"><span data-stu-id="3eae1-130">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <span data-ttu-id="3eae1-131">Firefox en Android</span><span class="sxs-lookup"><span data-stu-id="3eae1-131">Firefox on Android</span></span>  

<!--
> ##### Figure old 3  
> Firefox Icon on Android Emulator  
> ![Firefox Icon on Android Emulator][ImageAndroidEmulatorFirefoxBrowser]  
-->

<span data-ttu-id="3eae1-132">Al igual que el shell de contenido de cromo, puede obtener una APK para instalar Firefox en el emulador.</span><span class="sxs-lookup"><span data-stu-id="3eae1-132">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="3eae1-133">[Descargue el archivo. apk correcto][MozillaFirefoxDownload].</span><span class="sxs-lookup"><span data-stu-id="3eae1-133">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="3eae1-134">Desde aquí, podrás instalar el archivo en un emulador abierto o en un dispositivo Android conectado con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="3eae1-134">From here, you are able to install the file onto an open emulator or connected Android device with the following command:</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <span data-ttu-id="3eae1-135">Simulador iOS</span><span class="sxs-lookup"><span data-stu-id="3eae1-135">iOS Simulator</span></span>  

<span data-ttu-id="3eae1-136">El simulador iOS para Mac OS X viene con Xcode, que se [instala desde la App Store][MacAppStoreXcode].</span><span class="sxs-lookup"><span data-stu-id="3eae1-136">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="3eae1-137">Cuando haya terminado, obtenga información sobre cómo trabajar con el simulador a través de la [documentación para desarrolladores de Apple][AppleSimulatorHelp].</span><span class="sxs-lookup"><span data-stu-id="3eae1-137">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="3eae1-138">Para evitar tener que abrir Xcode cada vez que desee usar el simulador iOS, ábralo, luego haga clic con el botón derecho en el icono del simulador iOS en el Dock y seleccione **mantener en Dock**.</span><span class="sxs-lookup"><span data-stu-id="3eae1-138">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, then right-click the iOS Simulator icon in your dock and select **Keep in Dock**.</span></span>  <span data-ttu-id="3eae1-139">Ahora solo tienes que hacer clic en este icono cuando lo necesites.</span><span class="sxs-lookup"><span data-stu-id="3eae1-139">Now just click this icon whenever you need it.</span></span>  

###  <span data-ttu-id="3eae1-140">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="3eae1-140">Microsoft Edge (EdgeHTML)</span></span>  

> ##### <span data-ttu-id="3eae1-141">Figura 1</span><span class="sxs-lookup"><span data-stu-id="3eae1-141">Figure 1</span></span>  
> <span data-ttu-id="3eae1-142">VM moderna de IE</span><span class="sxs-lookup"><span data-stu-id="3eae1-142">Modern IE VM</span></span>  
> <span data-ttu-id="3eae1-143">! [VM moderna de IE] [ImageVMModernIe]</span><span class="sxs-lookup"><span data-stu-id="3eae1-143">![Modern IE VM][ImageVMModernIe]</span></span>  

<span data-ttu-id="3eae1-144">Microsoft Edge \ (EdgeHTML \) las máquinas virtuales \ (VMs \) te permiten acceder a diferentes versiones de EdgeHTML e IE en tu equipo a través de VirtualBox \ (o VMWare \).</span><span class="sxs-lookup"><span data-stu-id="3eae1-144">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="3eae1-145">Elija una [máquina virtual en la página de descarga][MicrosoftDeveloperEdgeVms].</span><span class="sxs-lookup"><span data-stu-id="3eae1-145">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <span data-ttu-id="3eae1-146">Emuladores y simuladores basados en la nube</span><span class="sxs-lookup"><span data-stu-id="3eae1-146">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="3eae1-147">Si no puede usar los emuladores y no tiene acceso a dispositivos reales, los emuladores basados en la nube son la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="3eae1-147">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="3eae1-148">Una gran ventaja de los emuladores basados en la nube en los dispositivos reales y en los emuladores locales es que puede automatizar las pruebas unitarias de su sitio a través de distintas plataformas.</span><span class="sxs-lookup"><span data-stu-id="3eae1-148">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="3eae1-149">[BrowserStack (comercial)][|::ref1::|] es el más fácil de usar para pruebas manuales.</span><span class="sxs-lookup"><span data-stu-id="3eae1-149">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="3eae1-150">Seleccione un sistema operativo, seleccione la versión del explorador y el tipo de dispositivo, seleccione una dirección URL para explorar y una máquina virtual hospedada con la que pueda interactuar.</span><span class="sxs-lookup"><span data-stu-id="3eae1-150">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="3eae1-151">También puedes ejecutar varios emuladores en la misma pantalla, lo que te permite probar la apariencia de la aplicación en varios dispositivos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="3eae1-151">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="3eae1-152">[SauceLabs (Commercial)][SauceLabs] le permite ejecutar pruebas unitarias dentro de un emulador, que pueden ser muy útiles para crear secuencias de comandos en su sitio y observar la grabación de vídeo de este después en varios dispositivos.</span><span class="sxs-lookup"><span data-stu-id="3eae1-152">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="3eae1-153">También puede realizar pruebas manuales con su sitio.</span><span class="sxs-lookup"><span data-stu-id="3eae1-153">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="3eae1-154">El [dispositivo en cualquier lugar (comercial)][AppExperience] no usa emuladores pero dispositivos reales que puedas controlar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="3eae1-154">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="3eae1-155">Esto es muy útil en el caso de que necesite reproducir un problema en un dispositivo específico y no pueda ver el error utilizando cualquiera de las opciones de las guías anteriores.</span><span class="sxs-lookup"><span data-stu-id="3eae1-155">This is very useful in the event where you need to reproduce a problem on a specific device and are not able to see the bug using any of the options in the previous guides.</span></span>  

 



<!-- image links -->  

<!--[ImageAndroidEmulatorStockBrowser]: /microsoft-edge/devtools-guide-chromium/media/device-mode-android-emulator-stock-browser.msft.png "Figure old 1: Stock Browser in Android Emulator"  -->  
<!--[ImageAndroidEmulatorContentShell]: /microsoft-edge/devtools-guide-chromium/media/device-mode-android-avd-contentshell.msft.png "Figure old 2: Android Emulator Content Shell"  -->  
<!--[ImageAndroidEmulatorFirefoxBrowser]: /microsoft-edge/devtools-guide-chromium/media/device-mode-ff-on-android-emulator.msft.png "Figure old 3: Firefox Icon on Android Emulator"  -->  
[ImageVMModernIe]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Device-Mode-Modern-IE-VM.msft.png "Ilustración 1: VM moderna de IE"  

<!-- links -->  

[DevToolsEdgeHtmlEmulation]: /microsoft-edge/devtools-guide/emulation "DevTools (EdgeHTML): emulación"  

[Ie11DevToolsEmulation]: /previous-versions/windows/internet-explorer/ie-developer/samples/dn255001(v=vs.85) "Emular exploradores, tamaños de pantalla y ubicaciones GPS"  

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
> <span data-ttu-id="3eae1-170">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3eae1-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3eae1-171">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Paul Bakaus][PaulBakaus] \ (abrir el sitio web para desarrolladores de Google | Herramientas, rendimiento, animación, UX \).</span><span class="sxs-lookup"><span data-stu-id="3eae1-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3eae1-173">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3eae1-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
