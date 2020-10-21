---
description: Su trabajo no finaliza con la garantía de que su sitio funciona de forma excelente en Microsoft Edge y Android.  Aunque el modo de dispositivo pueda simular una variedad de dispositivos como iPhone, le recomendamos que consulte las soluciones para la emulación proporcionadas por otros exploradores.
title: Emular y probar otros exploradores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1a7cc1c7e0a49760f30afdc16921824372b3a1aa
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124946"
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

# <span data-ttu-id="e65a8-105">Emular y probar otros exploradores</span><span class="sxs-lookup"><span data-stu-id="e65a8-105">Emulate and test other browsers</span></span>  

<span data-ttu-id="e65a8-106">Su trabajo no finaliza con la garantía de que su sitio funciona de forma excelente en Microsoft Edge y Android.</span><span class="sxs-lookup"><span data-stu-id="e65a8-106">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="e65a8-107">Aunque el modo de dispositivo pueda simular una variedad de dispositivos como iPhone, le recomendamos que consulte las soluciones para la emulación proporcionadas por otros exploradores.</span><span class="sxs-lookup"><span data-stu-id="e65a8-107">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <span data-ttu-id="e65a8-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="e65a8-108">Summary</span></span>  

*   <span data-ttu-id="e65a8-109">Si no tiene un dispositivo en particular o desea realizar una comprobación puntual en algo, la mejor opción es emular el dispositivo directamente en el explorador.</span><span class="sxs-lookup"><span data-stu-id="e65a8-109">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="e65a8-110">Los emuladores y simuladores de dispositivos le permiten imitar su sitio de desarrollo en un intervalo de dispositivos de su estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="e65a8-110">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="e65a8-111">Los emuladores basados en la nube permiten automatizar las pruebas unitarias de su sitio a través de diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="e65a8-111">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <span data-ttu-id="e65a8-112">Emuladores del explorador</span><span class="sxs-lookup"><span data-stu-id="e65a8-112">Browser emulators</span></span>  

<span data-ttu-id="e65a8-113">Los emuladores de explorador son ideales para probar la capacidad de respuesta de un sitio, pero cada uno de ellos no emula las diferencias en la API, la compatibilidad con CSS y determinados comportamientos que se pueden ver en un explorador móvil.</span><span class="sxs-lookup"><span data-stu-id="e65a8-113">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that you see on a mobile browser.</span></span>  <span data-ttu-id="e65a8-114">Pruebe su sitio en exploradores que se ejecutan en dispositivos reales para asegurarse de que todo funciona como se espera.</span><span class="sxs-lookup"><span data-stu-id="e65a8-114">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <span data-ttu-id="e65a8-115">Vista diseño dinámico de Firefox</span><span class="sxs-lookup"><span data-stu-id="e65a8-115">Firefox Responsive Design View</span></span>  

<span data-ttu-id="e65a8-116">Firefox tiene una [vista de diseño con capacidad de respuesta][MDNResponsiveDesignMode] que le anima a dejar de pensar en términos de dispositivos específicos y, en su lugar, explorar cómo cambia el diseño en tamaños de pantalla comunes o su propio tamaño arrastrando los bordes.</span><span class="sxs-lookup"><span data-stu-id="e65a8-116">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <span data-ttu-id="e65a8-117">Emulación de EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="e65a8-117">EdgeHTML emulation</span></span>  

<span data-ttu-id="e65a8-118">Para emular teléfonos con Windows, use la [emulación integrada][DevToolsEdgeHtmlEmulation]Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="e65a8-118">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][DevToolsEdgeHtmlEmulation].</span></span>  

<span data-ttu-id="e65a8-119">Use la [emulación de IE 11][Ie11DevToolsEmulation] para simular el aspecto que tendrá la página en versiones anteriores de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e65a8-119">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <span data-ttu-id="e65a8-120">Emuladores y simuladores de dispositivos</span><span class="sxs-lookup"><span data-stu-id="e65a8-120">Device emulators and simulators</span></span>  

<span data-ttu-id="e65a8-121">Los simuladores y simuladores de dispositivos simulan no solo el entorno del explorador, sino el dispositivo completo.</span><span class="sxs-lookup"><span data-stu-id="e65a8-121">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="e65a8-122">Cada uno es útil para probar las cosas que requieren integración del sistema operativo, por ejemplo, la entrada de datos con teclados virtuales.</span><span class="sxs-lookup"><span data-stu-id="e65a8-122">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <span data-ttu-id="e65a8-123">Emulador de Android</span><span class="sxs-lookup"><span data-stu-id="e65a8-123">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="e65a8-124">Por el momento, no hay ninguna forma de instalar Microsoft Edge en un emulador Android.</span><span class="sxs-lookup"><span data-stu-id="e65a8-124">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="e65a8-125">Sin embargo, puede usar el explorador Android, el shell de contenido de cromo y Firefox para Android que revisamos más adelante en esta guía.</span><span class="sxs-lookup"><span data-stu-id="e65a8-125">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="e65a8-126">El shell de contenido de cromo ejecuta el mismo motor de procesamiento de cromo que Microsoft Edge, pero sin ninguna de las características específicas del explorador.</span><span class="sxs-lookup"><span data-stu-id="e65a8-126">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="e65a8-127">El emulador de Android viene con el SDK de Android que necesita descargar como parte de [Android Studio][AndroidStudioDownload].</span><span class="sxs-lookup"><span data-stu-id="e65a8-127">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="e65a8-128">A continuación, siga las instrucciones para [configurar un dispositivo virtual][AndroidStudioCreateManageVirtualDevices] e [iniciar el emulador][AndroidStudioRunAppsAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="e65a8-128">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="e65a8-129">Una vez que se haya arrancado el emulador, haga clic en el icono del explorador y pruebe su sitio en el antiguo explorador de cotizaciones para Android.</span><span class="sxs-lookup"><span data-stu-id="e65a8-129">Once your emulator is booted, click on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <span data-ttu-id="e65a8-130">Shell de contenido de cromo en Android</span><span class="sxs-lookup"><span data-stu-id="e65a8-130">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="e65a8-131">Para instalar el shell de contenido de cromo para Android, deje el emulador ejecutándose y ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="e65a8-131">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="e65a8-132">Ahora puede probar su sitio con el shell de contenido de cromo.</span><span class="sxs-lookup"><span data-stu-id="e65a8-132">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <span data-ttu-id="e65a8-133">Firefox en Android</span><span class="sxs-lookup"><span data-stu-id="e65a8-133">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="e65a8-134">Al igual que el shell de contenido de cromo, puede obtener una APK para instalar Firefox en el emulador.</span><span class="sxs-lookup"><span data-stu-id="e65a8-134">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="e65a8-135">[Descargue el archivo. apk correcto][MozillaFirefoxDownload].</span><span class="sxs-lookup"><span data-stu-id="e65a8-135">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="e65a8-136">Para instalar el archivo en un emulador abierto o en un dispositivo Android conectado, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="e65a8-136">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <span data-ttu-id="e65a8-137">simulador iOS</span><span class="sxs-lookup"><span data-stu-id="e65a8-137">iOS simulator</span></span>  

<span data-ttu-id="e65a8-138">El simulador iOS para Mac OS X viene con Xcode, que se [instala desde la App Store][MacAppStoreXcode].</span><span class="sxs-lookup"><span data-stu-id="e65a8-138">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="e65a8-139">Cuando haya terminado, obtenga información sobre cómo trabajar con el simulador a través de la [documentación para desarrolladores de Apple][AppleSimulatorHelp].</span><span class="sxs-lookup"><span data-stu-id="e65a8-139">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="e65a8-140">Para evitar tener que abrir Xcode cada vez que desee usar el simulador iOS, ábralo y, a continuación, haga clic con el botón derecho en el icono del simulador iOS en el Dock y seleccione **mantener en Dock**.</span><span class="sxs-lookup"><span data-stu-id="e65a8-140">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, then right-click the iOS Simulator icon in your dock and choose **Keep in Dock**.</span></span>  <span data-ttu-id="e65a8-141">Ahora solo tienes que hacer clic en este icono cuando lo necesites.</span><span class="sxs-lookup"><span data-stu-id="e65a8-141">Now just click this icon whenever you need it.</span></span>  

###  <span data-ttu-id="e65a8-142">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="e65a8-142">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="e65a8-144">VM moderna de IE</span><span class="sxs-lookup"><span data-stu-id="e65a8-144">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="e65a8-145">Microsoft Edge \ (EdgeHTML \) las máquinas virtuales \ (VMs \) te permiten acceder a diferentes versiones de EdgeHTML e IE en tu equipo a través de VirtualBox \ (o VMWare \).</span><span class="sxs-lookup"><span data-stu-id="e65a8-145">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="e65a8-146">Elija una [máquina virtual en la página de descarga][MicrosoftDeveloperEdgeVms].</span><span class="sxs-lookup"><span data-stu-id="e65a8-146">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <span data-ttu-id="e65a8-147">Emuladores y simuladores basados en la nube</span><span class="sxs-lookup"><span data-stu-id="e65a8-147">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="e65a8-148">Si no puede usar los emuladores y no tiene acceso a dispositivos reales, los emuladores basados en la nube son la mejor opción.</span><span class="sxs-lookup"><span data-stu-id="e65a8-148">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="e65a8-149">Una gran ventaja de los emuladores basados en la nube en los dispositivos reales y en los emuladores locales es que puede automatizar las pruebas unitarias de su sitio a través de distintas plataformas.</span><span class="sxs-lookup"><span data-stu-id="e65a8-149">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="e65a8-150">[BrowserStack (comercial)][|::ref1::|] es el más fácil de usar para pruebas manuales.</span><span class="sxs-lookup"><span data-stu-id="e65a8-150">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="e65a8-151">Seleccione un sistema operativo, seleccione la versión del explorador y el tipo de dispositivo, seleccione una dirección URL para explorar y una máquina virtual hospedada con la que pueda interactuar.</span><span class="sxs-lookup"><span data-stu-id="e65a8-151">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="e65a8-152">También puedes ejecutar varios emuladores en la misma pantalla, lo que te permite probar la apariencia de la aplicación en varios dispositivos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e65a8-152">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="e65a8-153">[SauceLabs (Commercial)][SauceLabs] le permite ejecutar pruebas unitarias dentro de un emulador, que pueden ser muy útiles para crear secuencias de comandos en su sitio y observar la grabación de vídeo de este después en varios dispositivos.</span><span class="sxs-lookup"><span data-stu-id="e65a8-153">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="e65a8-154">También puede realizar pruebas manuales con su sitio.</span><span class="sxs-lookup"><span data-stu-id="e65a8-154">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="e65a8-155">El [dispositivo en cualquier lugar (comercial)][AppExperience] no usa emuladores pero dispositivos reales que puedas controlar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="e65a8-155">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="e65a8-156">Esto es muy útil en el caso de que necesite reproducir un problema en un dispositivo específico y no pueda ver el error utilizando cualquiera de las opciones de las guías anteriores.</span><span class="sxs-lookup"><span data-stu-id="e65a8-156">This is very useful in the event where you need to reproduce a problem on a specific device and are not able to see the bug using any of the options in the previous guides.</span></span>  

## <span data-ttu-id="e65a8-157">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e65a8-157">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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
> <span data-ttu-id="e65a8-171">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e65a8-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e65a8-172">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Paul Bakaus][PaulBakaus] \ (abrir el sitio web para desarrolladores de Google | Herramientas, rendimiento, animación, UX \).</span><span class="sxs-lookup"><span data-stu-id="e65a8-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="e65a8-174">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e65a8-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
