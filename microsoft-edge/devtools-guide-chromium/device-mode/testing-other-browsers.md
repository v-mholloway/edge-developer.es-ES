---
description: El trabajo no termina asegurando que el sitio se ejecute bien en Microsoft Edge y Android.  Aunque el modo dispositivo es capaz de simular una variedad de otros dispositivos como iPhones, te recomendamos que consultes las soluciones de emulación proporcionadas por otros exploradores.
title: Emular y probar otros exploradores
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f2ca56c2e15f578a970e6ceb84b1554bfda53862
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564283"
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
# <a name="emulate-and-test-other-browsers"></a><span data-ttu-id="ffb56-105">Emular y probar otros exploradores</span><span class="sxs-lookup"><span data-stu-id="ffb56-105">Emulate and test other browsers</span></span>  

<span data-ttu-id="ffb56-106">El trabajo no termina asegurando que el sitio se ejecute bien en Microsoft Edge y Android.</span><span class="sxs-lookup"><span data-stu-id="ffb56-106">Your job does not end with ensuring your site runs great across Microsoft Edge and Android.</span></span>  <span data-ttu-id="ffb56-107">Aunque el modo dispositivo es capaz de simular una variedad de otros dispositivos como iPhones, te recomendamos que consultes las soluciones de emulación proporcionadas por otros exploradores.</span><span class="sxs-lookup"><span data-stu-id="ffb56-107">Even though Device Mode is able to simulate a range of other devices like iPhones, we encourage you to check out solutions for emulation provided by other browsers.</span></span>  

### <a name="summary"></a><span data-ttu-id="ffb56-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="ffb56-108">Summary</span></span>  

*   <span data-ttu-id="ffb56-109">Cuando no tienes un dispositivo en particular o quieres hacer una comprobación de puntos en algo, la mejor opción es emular el dispositivo directamente dentro del explorador.</span><span class="sxs-lookup"><span data-stu-id="ffb56-109">When you do not have a particular device, or want to do a spot check on something, the best option is to emulate the device right inside your browser.</span></span>  
*   <span data-ttu-id="ffb56-110">Los emuladores y simuladores de dispositivos te permiten imitar el sitio de desarrollo en una amplia variedad de dispositivos de la estación de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ffb56-110">Device emulators and simulators enable you to mimic your development site on a range of devices from your workstation.</span></span>  
*   <span data-ttu-id="ffb56-111">Los emuladores basados en la nube permiten automatizar las pruebas unitarias de su sitio en diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="ffb56-111">Cloud-based emulators enable you to automate unit tests for your site across different platforms.</span></span>  

## <a name="browser-emulators"></a><span data-ttu-id="ffb56-112">Emuladores de explorador</span><span class="sxs-lookup"><span data-stu-id="ffb56-112">Browser emulators</span></span>  

<span data-ttu-id="ffb56-113">Los emuladores de explorador son excelentes para probar la capacidad de respuesta de un sitio, pero cada uno no emula las diferencias en api, compatibilidad con CSS y determinados comportamientos que se muestran en un explorador móvil.</span><span class="sxs-lookup"><span data-stu-id="ffb56-113">Browser emulators are great for testing the responsiveness of a site, but each does not emulate differences in API, CSS support, and certain behaviors that is displayed on a mobile browser.</span></span>  <span data-ttu-id="ffb56-114">Pruebe el sitio en exploradores que se ejecutan en dispositivos reales para que todo se comporte como se esperaba.</span><span class="sxs-lookup"><span data-stu-id="ffb56-114">Test your site on browsers running on real devices to be certain everything behaves as expected.</span></span>  

### <a name="firefox-responsive-design-view"></a><span data-ttu-id="ffb56-115">Vista Diseño dinámico de Firefox</span><span class="sxs-lookup"><span data-stu-id="ffb56-115">Firefox Responsive Design View</span></span>  

<span data-ttu-id="ffb56-116">Firefox tiene una [vista de][MDNResponsiveDesignMode] diseño adaptable que te anima a dejar de pensar en términos de dispositivos específicos y, en su lugar, explorar cómo cambia el diseño en tamaños de pantalla comunes o tu propio tamaño arrastrando los bordes.</span><span class="sxs-lookup"><span data-stu-id="ffb56-116">Firefox has a [responsive design view][MDNResponsiveDesignMode] that encourages you to stop thinking in terms of specific devices and instead explore how your design changes at common screen sizes or your own size by dragging the edges.</span></span>  

### <a name="edgehtml-emulation"></a><span data-ttu-id="ffb56-117">Emulación edgeHTML</span><span class="sxs-lookup"><span data-stu-id="ffb56-117">EdgeHTML emulation</span></span>  

<span data-ttu-id="ffb56-118">Para emular Windows teléfonos, use la [emulación][ArchiveMicrosoftEdgeDevtoolsEmulation]Microsoft Edge \(EdgeHTML\) integrada .</span><span class="sxs-lookup"><span data-stu-id="ffb56-118">To emulate Windows Phones, use the Microsoft Edge \(EdgeHTML\) [built-in emulation][ArchiveMicrosoftEdgeDevtoolsEmulation].</span></span>  

<span data-ttu-id="ffb56-119">Usa [la emulación de IE 11][Ie11DevToolsEmulation] para simular el aspecto de tu página en versiones anteriores de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ffb56-119">Use [IE 11 Emulation][Ie11DevToolsEmulation] to simulate how your page may look in older versions of Internet Explorer.</span></span>  

## <a name="device-emulators-and-simulators"></a><span data-ttu-id="ffb56-120">Emuladores y simuladores de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ffb56-120">Device emulators and simulators</span></span>  

<span data-ttu-id="ffb56-121">Los simuladores y emuladores de dispositivo simulan no solo el entorno del explorador, sino todo el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ffb56-121">Device simulators and emulators simulate not just the browser environment but the entire device.</span></span>  <span data-ttu-id="ffb56-122">Cada uno es útil para probar cosas que requieren la integración del sistema operativo, por ejemplo, la entrada de formulario con teclados virtuales.</span><span class="sxs-lookup"><span data-stu-id="ffb56-122">Each are useful to test things that require OS integration, for example form input with virtual keyboards.</span></span>  

### <a name="android-emulator"></a><span data-ttu-id="ffb56-123">Emulador de Android</span><span class="sxs-lookup"><span data-stu-id="ffb56-123">Android emulator</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-emulator-stock-browser.msft.png" alt-text="Stock Browser in Android Emulator" lightbox="../media/device-mode-android-emulator-stock-browser.msft.png":::
   Stock Browser in Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="ffb56-124">Por el momento, no hay ninguna forma de instalar Microsoft Edge en un emulador de Android.</span><span class="sxs-lookup"><span data-stu-id="ffb56-124">At the moment, there is no way to install Microsoft Edge on an Android emulator.</span></span>  <span data-ttu-id="ffb56-125">Sin embargo, puede usar el Explorador de Android, el Shell de contenido Chromium y Firefox para Android que revisaremos más adelante en esta guía.</span><span class="sxs-lookup"><span data-stu-id="ffb56-125">However, you may use the Android Browser, the Chromium Content Shell, and Firefox for Android which we review later in this guide.</span></span>  <span data-ttu-id="ffb56-126">Chromium El Shell de contenido ejecuta el mismo Chromium de representación que Microsoft Edge, pero viene sin ninguna de las características específicas del explorador.</span><span class="sxs-lookup"><span data-stu-id="ffb56-126">Chromium Content Shell runs the same Chromium rendering engine as Microsoft Edge, but comes without any of the browser specific features.</span></span>  

<span data-ttu-id="ffb56-127">El emulador de Android viene con el SDK de Android que necesitas descargar como parte de [Android Studio][AndroidStudioDownload].</span><span class="sxs-lookup"><span data-stu-id="ffb56-127">The Android emulator comes with the Android SDK which you need to download as part of [Android Studio][AndroidStudioDownload].</span></span>  <span data-ttu-id="ffb56-128">A continuación, siga [las instrucciones para configurar un dispositivo virtual e][AndroidStudioCreateManageVirtualDevices] iniciar el [emulador][AndroidStudioRunAppsAndroidEmulator].</span><span class="sxs-lookup"><span data-stu-id="ffb56-128">Then follow the instructions to [set up a virtual device][AndroidStudioCreateManageVirtualDevices] and [start the emulator][AndroidStudioRunAppsAndroidEmulator].</span></span>  
<span data-ttu-id="ffb56-129">Una vez que se inicie el emulador, elija en el icono Explorador y pruebe el sitio en el antiguo Explorador de acciones para Android.</span><span class="sxs-lookup"><span data-stu-id="ffb56-129">Once your emulator is booted, choose on the Browser icon, and test your site on the old Stock Browser for Android.</span></span>  

#### <a name="chromium-content-shell-on-android"></a><span data-ttu-id="ffb56-130">Chromium shell de contenido en Android</span><span class="sxs-lookup"><span data-stu-id="ffb56-130">Chromium content shell on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-android-avd-contentshell.msft.png" alt-text="Android Emulator Content Shell" lightbox="../media/device-mode-android-avd-contentshell.msft.png":::
   Android Emulator Content Shell  
:::image-end:::  
-->  

<span data-ttu-id="ffb56-131">Para instalar el shell Chromium contenido para Android, deje el emulador en ejecución y ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="ffb56-131">To install the Chromium Content Shell for Android, leave your emulator running and run the following command.</span></span>  

```shell
git clone https://github.com/PaulKinlan/chromium-android-installer.git
chmod u+x ./chromium-android-installer/*.sh
./chromium-android-installer/install-chromeandroid.sh
```  

<span data-ttu-id="ffb56-132">Ahora puede probar su sitio con el Shell Chromium contenido.</span><span class="sxs-lookup"><span data-stu-id="ffb56-132">Now you are able to test your site with the Chromium Content Shell.</span></span>  

#### <a name="firefox-on-android"></a><span data-ttu-id="ffb56-133">Firefox en Android</span><span class="sxs-lookup"><span data-stu-id="ffb56-133">Firefox on Android</span></span>  

<!--  
:::image type="complex" source="../media/device-mode-ff-on-android-emulator.msft.png" alt-text="Firefox Icon on Android Emulator" lightbox="../media/device-mode-ff-on-android-emulator.msft.png":::
   Firefox Icon on Android Emulator  
:::image-end:::  
-->  

<span data-ttu-id="ffb56-134">Al igual que Chromium Shell de contenido, puedes obtener un APK para instalar Firefox en el emulador.</span><span class="sxs-lookup"><span data-stu-id="ffb56-134">Similar to the Chromium Content Shell, you are able to get an APK to install Firefox onto the emulator.</span></span>  

<span data-ttu-id="ffb56-135">[Descargue el archivo .apk correcto.][MozillaFirefoxDownload]</span><span class="sxs-lookup"><span data-stu-id="ffb56-135">[Download the correct .apk file][MozillaFirefoxDownload].</span></span>  

<span data-ttu-id="ffb56-136">Para instalar el archivo en un emulador abierto o un dispositivo Android conectado, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="ffb56-136">To install the file onto an open emulator or connected Android device, run the following command.</span></span>  

```shell
adb install <path_to_APK>/fennec-XX.X.XX.android-arm.apk
```  

### <a name="ios-simulator"></a><span data-ttu-id="ffb56-137">Simulador de iOS</span><span class="sxs-lookup"><span data-stu-id="ffb56-137">iOS simulator</span></span>  

<span data-ttu-id="ffb56-138">El simulador de iOS para Mac OS X viene con Xcode, que se [instala desde la Tienda de aplicaciones.][MacAppStoreXcode]</span><span class="sxs-lookup"><span data-stu-id="ffb56-138">The iOS simulator for Mac OS X comes with Xcode, which you [install from the App Store][MacAppStoreXcode].</span></span>  

<span data-ttu-id="ffb56-139">Cuando haya terminado, obtenga información sobre cómo trabajar con el simulador a través de la [documentación del desarrollador de Apple][AppleSimulatorHelp].</span><span class="sxs-lookup"><span data-stu-id="ffb56-139">When you are done, learn how to work with the simulator through [Apple Developer documentation][AppleSimulatorHelp].</span></span>  

> [!NOTE]
> <span data-ttu-id="ffb56-140">Para evitar tener que abrir Xcode cada vez que quiera usar el simulador de iOS, ábralo, mantenga el mouse en el icono simulador de iOS en el dock, abra el menú contextual \(haga clic con el botón secundario\) y elija Mantener en **dock**.</span><span class="sxs-lookup"><span data-stu-id="ffb56-140">To avoid having to open Xcode every time you want to use the iOS Simulator, open it, hover on the iOS Simulator icon in your dock, open the contextual menu \(right-click\), and choose **Keep in Dock**.</span></span>  <span data-ttu-id="ffb56-141">Ahora solo tienes que elegir el icono siempre que lo necesites.</span><span class="sxs-lookup"><span data-stu-id="ffb56-141">Now just choose the icon whenever you need it.</span></span>  

###  <a name="microsoft-edge-edgehtml"></a><span data-ttu-id="ffb56-142">Microsoft Edge (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="ffb56-142">Microsoft Edge (EdgeHTML)</span></span>  

:::image type="complex" source="../media/device-mode-modern-ie-vm.msft.png" alt-text="Máquina virtual IE moderna" lightbox="../media/device-mode-modern-ie-vm.msft.png":::
   <span data-ttu-id="ffb56-144">Máquina virtual IE moderna</span><span class="sxs-lookup"><span data-stu-id="ffb56-144">Modern IE VM</span></span>  
:::image-end:::  

<span data-ttu-id="ffb56-145">Microsoft Edge \(EdgeHTML\) Máquinas virtuales \(VM\) permiten tener acceso a diferentes versiones de EdgeHTML e IE en el equipo a través de VirtualBox \(o VMWare\).</span><span class="sxs-lookup"><span data-stu-id="ffb56-145">Microsoft Edge \(EdgeHTML\) Virtual Machines \(VMs\) enable you to access different versions of EdgeHTML and IE on your computer via VirtualBox \(or VMWare\).</span></span>  <span data-ttu-id="ffb56-146">Elija una [máquina virtual en la página de descarga][MicrosoftDeveloperEdgeVms].</span><span class="sxs-lookup"><span data-stu-id="ffb56-146">Choose a [virtual machine on the download page][MicrosoftDeveloperEdgeVms].</span></span>  

## <a name="cloud-based-emulators-and-simulators"></a><span data-ttu-id="ffb56-147">Emuladores y simuladores basados en la nube</span><span class="sxs-lookup"><span data-stu-id="ffb56-147">Cloud-based emulators and simulators</span></span>  

<span data-ttu-id="ffb56-148">Si no puedes usar los emuladores y no tienes acceso a dispositivos reales, los emuladores basados en la nube son lo siguiente mejor.</span><span class="sxs-lookup"><span data-stu-id="ffb56-148">If you are not able to use the emulators and do not have access to real devices, then cloud-based emulators are the next best thing.</span></span>  <span data-ttu-id="ffb56-149">Una gran ventaja de los emuladores basados en la nube sobre dispositivos reales y emuladores locales es que puede automatizar las pruebas unitarias de su sitio en diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="ffb56-149">A big advantage of cloud-based emulators over real devices and local emulators is that you are able to automate unit tests for your site across different platforms.</span></span>  

*   <span data-ttu-id="ffb56-150">[BrowserStack (comercial)][|::ref1::|] es el más fácil de usar para pruebas manuales.</span><span class="sxs-lookup"><span data-stu-id="ffb56-150">[BrowserStack (commercial)][|::ref1::|] is the easiest to use for manual testing.</span></span>  <span data-ttu-id="ffb56-151">Seleccionas un sistema operativo, seleccionas la versión del explorador y el tipo de dispositivo, seleccionas una dirección URL para examinar y gira hacia arriba una máquina virtual hospedada con la que puedes interactuar.</span><span class="sxs-lookup"><span data-stu-id="ffb56-151">You select an operating system, select your browser version and device type, select a URL to browse, and it spins up a hosted virtual machine with which you may interact.</span></span>  <span data-ttu-id="ffb56-152">También puedes ejecutar varios emuladores en la misma pantalla, lo que te permite probar la apariencia de la aplicación en varios dispositivos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ffb56-152">You are able to also run multiple emulators in the same screen, enabling you to test the look and feel of your app across multiple devices at the same time.</span></span>  
*   <span data-ttu-id="ffb56-153">[SauceLabs (comercial)][SauceLabs] permite ejecutar pruebas unitarias dentro de un emulador, lo que puede ser realmente útil para secuencias de comandos de un flujo a través del sitio y ver la grabación de vídeo de esto después en varios dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ffb56-153">[SauceLabs (commercial)][SauceLabs] enables you to run unit tests inside of an emulator, which may be really useful for scripting a flow through your site and watching the video recording of this afterwards on various devices.</span></span>  <span data-ttu-id="ffb56-154">También puede realizar pruebas manuales con su sitio.</span><span class="sxs-lookup"><span data-stu-id="ffb56-154">You are also able to do manual testing with your site.</span></span>  
*   <span data-ttu-id="ffb56-155">[Device Anywhere (comercial)][AppExperience] no usa emuladores, sino dispositivos reales que puedes controlar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="ffb56-155">[Device Anywhere (commercial)][AppExperience] does not use emulators but real devices which you are able to control remotely.</span></span>  <span data-ttu-id="ffb56-156">Esto es muy útil en caso de que necesites reproducir un problema en un dispositivo específico y puede que no muestres el error con ninguna de las opciones de las guías anteriores.</span><span class="sxs-lookup"><span data-stu-id="ffb56-156">This is very useful in the event where you need to reproduce a problem on a specific device and may not display the bug using any of the options in the previous guides.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ffb56-157">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ffb56-157">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="ffb56-171">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ffb56-171">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ffb56-172">La página original [](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) se encuentra aquí y es creado por [Meggin Kearney][MegginKearney] \(Tech Writer\) y [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate en Google | Herramientas, Rendimiento, Animación, UX\).</span><span class="sxs-lookup"><span data-stu-id="ffb56-172">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/testing-other-browsers) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate at Google | Tools, Performance, Animation, UX\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ffb56-174">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ffb56-174">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors#paul-bakaus  
