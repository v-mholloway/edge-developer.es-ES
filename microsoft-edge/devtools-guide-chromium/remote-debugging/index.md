---
title: Introducción a la depuración remota dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a9002ca82e6e0dcaf7f174b336e5c640929a561b
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611822"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  




<!--
<style>
.devtools-inline {
  max-height: 1em;
  vertical-align: middle;
}
</style>
-->  
# <span data-ttu-id="270cd-103">Introducción a la depuración remota dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="270cd-103">Get Started with Remote Debugging Android Devices</span></span>   



<span data-ttu-id="270cd-104">Depure de forma remota contenido en vivo en un dispositivo Android desde su equipo con Windows o macOS.</span><span class="sxs-lookup"><span data-stu-id="270cd-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="270cd-105">Este tutorial le enseña a:</span><span class="sxs-lookup"><span data-stu-id="270cd-105">This tutorial teaches you how to:</span></span>  

*   <span data-ttu-id="270cd-106">Configure su dispositivo Android para la depuración remota y descárguelo desde el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="270cd-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="270cd-107">Inspeccione y depure contenido en vivo en su dispositivo Android desde su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="270cd-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="270cd-108">Contenido de screencast de su dispositivo Android en una instancia de DevTools en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="270cd-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## <span data-ttu-id="270cd-109">Paso 1: descubrir su dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="270cd-109">Step 1: Discover your Android device</span></span>   

<span data-ttu-id="270cd-110">El flujo de trabajo siguiente funciona para la mayoría de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="270cd-110">The workflow below works for most users.</span></span>  <span data-ttu-id="270cd-111">Consulte [solución de problemas: DevTools no detecta el dispositivo Android](#troubleshooting-devtools-is-not-detecting-the-android-device) para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="270cd-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="270cd-112">Abra la pantalla **Opciones del desarrollador** en Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="270cd-113">Consulte [configurar las opciones de Desarrollador en dispositivos](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="270cd-113">See [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="270cd-114">Seleccione **Habilitar depuración USB**.</span><span class="sxs-lookup"><span data-stu-id="270cd-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="270cd-115">En tu equipo de desarrollo, abre Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="270cd-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="270cd-116">[Abra DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="270cd-116">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="270cd-117">En DevTools, seleccione el **menú principal** `...` y, a continuación, seleccione **más herramientas**  >  **dispositivos remotos**.</span><span class="sxs-lookup"><span data-stu-id="270cd-117">In DevTools, select the **Main Menu** `...` then select **More tools** > **Remote devices**.</span></span>  
    
    > ##### <span data-ttu-id="270cd-118">Figura 1</span><span class="sxs-lookup"><span data-stu-id="270cd-118">Figure 1</span></span>  
    > <span data-ttu-id="270cd-119">Abrir la ficha **dispositivos remotos** a través del **menú principal**</span><span class="sxs-lookup"><span data-stu-id="270cd-119">Opening the **Remote Devices** tab via the **Main Menu**</span></span>  
    > <span data-ttu-id="270cd-120">! [Abriendo la ficha dispositivos remotos a través del menú principal] [ImageOpenRemoteDevices]</span><span class="sxs-lookup"><span data-stu-id="270cd-120">![Opening the Remote Devices tab via the Main Menu][ImageOpenRemoteDevices]</span></span>  

1.  <span data-ttu-id="270cd-121">En DevTools, abra la pestaña **configuración** .</span><span class="sxs-lookup"><span data-stu-id="270cd-121">In DevTools, open the **Settings** tab.</span></span>  

1.  <span data-ttu-id="270cd-122">Asegúrese de que la casilla **descubrir dispositivos USB** esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="270cd-122">Make sure that the **Discover USB devices** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="270cd-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="270cd-123">Figure 2</span></span>  
    > <span data-ttu-id="270cd-124">La casilla **descubrir dispositivos USB** está habilitada</span><span class="sxs-lookup"><span data-stu-id="270cd-124">The **Discover USB Devices** checkbox is enabled</span></span>  
    > <span data-ttu-id="270cd-125">! [La casilla descubrir dispositivos USB está habilitada] [ImageDiscoverUSBDevices]</span><span class="sxs-lookup"><span data-stu-id="270cd-125">![The Discover USB Devices checkbox is enabled][ImageDiscoverUSBDevices]</span></span>  

1.  <span data-ttu-id="270cd-126">Conecta el dispositivo Android directamente a tu equipo de desarrollo con un cable USB.</span><span class="sxs-lookup"><span data-stu-id="270cd-126">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="270cd-127">La primera vez que lo haces, verás que DevTools ha detectado un dispositivo desconocido.</span><span class="sxs-lookup"><span data-stu-id="270cd-127">The first time you do this, you usually see that DevTools has detected an unknown device.</span></span>  <span data-ttu-id="270cd-128">Si ve un punto verde y el texto **conectado** debajo del nombre del modelo de su dispositivo Android, DevTools ha establecido correctamente la conexión con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="270cd-128">If you see a green dot and the text **Connected** below the model name of your Android device, then DevTools has successfully established the connection to your device.</span></span>  <span data-ttu-id="270cd-129">Continúe con el [paso 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span><span class="sxs-lookup"><span data-stu-id="270cd-129">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  <span data-ttu-id="270cd-130">Si el dispositivo se muestra como **desconocido**, acepte el aviso de permiso de **depuración USB** en tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-130">If your device is showing up as **Unknown**, accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  

### <span data-ttu-id="270cd-131">Solución de problemas: DevTools no detecta el dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="270cd-131">Troubleshooting: DevTools is not detecting the Android device</span></span>   

<span data-ttu-id="270cd-132">Asegúrese de que el hardware esté configurado correctamente:</span><span class="sxs-lookup"><span data-stu-id="270cd-132">Make sure that your hardware is set up correctly:</span></span>  

*   <span data-ttu-id="270cd-133">Si está usando un concentrador USB, intente conectar el dispositivo Android directamente a su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="270cd-133">If you are using a USB hub, try connecting your Android device directly to your development machine instead.</span></span>  
*   <span data-ttu-id="270cd-134">Intente desconectar el cable USB entre su dispositivo Android y su equipo de desarrollo y, a continuación, conéctelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="270cd-134">Try unplugging the USB cable between your Android device and development machine, and then plugging it back in.</span></span>  <span data-ttu-id="270cd-135">Hágalo mientras las pantallas de Android y de equipo de desarrollo estén desbloqueadas.</span><span class="sxs-lookup"><span data-stu-id="270cd-135">Do it while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="270cd-136">Asegúrate de que tu cable USB funcione.</span><span class="sxs-lookup"><span data-stu-id="270cd-136">Make sure that your USB cable works.</span></span>  <span data-ttu-id="270cd-137">Debería poder inspeccionar los archivos de su dispositivo Android desde su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="270cd-137">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="270cd-138">Asegúrese de que el software esté configurado correctamente:</span><span class="sxs-lookup"><span data-stu-id="270cd-138">Make sure that your software is set up correctly:</span></span>  

*   <span data-ttu-id="270cd-139">Si tu equipo de desarrollo ejecuta Windows, intenta instalar manualmente los drivers USB para tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-139">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="270cd-140">Consulte [Instalar drivers OEM USB][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="270cd-140">See [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
    
*   <span data-ttu-id="270cd-141">Algunas combinaciones de dispositivos Windows y Android (especialmente Samsung) requieren una configuración adicional.</span><span class="sxs-lookup"><span data-stu-id="270cd-141">Some combinations of Windows and Android devices (especially Samsung) require extra set up.</span></span>  <span data-ttu-id="270cd-142">Consulte [DevTools dispositivos no detectan el dispositivo cuando está conectado] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="270cd-142">See [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  
    
<span data-ttu-id="270cd-143">Si no ve el mensaje **permitir la depuración de USB** en su dispositivo Android, pruebe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="270cd-143">If you do not see the **Allow USB Debugging** prompt on your Android device try:</span></span>  

*   <span data-ttu-id="270cd-144">Desconectar y volver a conectar el cable USB mientras DevTools está en el equipo de desarrollo y se muestra el pantalla Android de Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-144">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  <span data-ttu-id="270cd-145">En otras palabras, a veces el mensaje no se muestra cuando las pantallas de Android o de equipo de desarrollo están bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="270cd-145">In other words, sometimes the prompt does not show up when your Android or development machine screens are locked.</span></span>
*   <span data-ttu-id="270cd-146">Actualización de la configuración de pantalla de su dispositivo Android y equipo de desarrollo para que nunca pasen al modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="270cd-146">Updating the display settings for your Android device and development machine so that they never go to sleep.</span></span>  
*   <span data-ttu-id="270cd-147">Configuración del modo USB para Android en PTP.</span><span class="sxs-lookup"><span data-stu-id="270cd-147">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="270cd-148">Consulte [Galaxy S4 no muestra el cuadro de diálogo autorizar depuración USB][StackExchangeGalaxyS4DoesNotShowDialogBox].</span><span class="sxs-lookup"><span data-stu-id="270cd-148">See [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="270cd-149">Seleccione **revocar las autorizaciones de depuración USB** en la pantalla de **Opciones del desarrollador** de su dispositivo Android para restablecerla a un estado actualizado.</span><span class="sxs-lookup"><span data-stu-id="270cd-149">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="270cd-150">Si encuentra una solución que no se menciona en esta sección o en [los dispositivos DevTools no detectan el dispositivo cuando está conectado] [StackOverflowDevicesNotDetected] o agrega una respuesta a esa pregunta de desbordamiento de pila</span><span class="sxs-lookup"><span data-stu-id="270cd-150">If you find a solution that is not mentioned in this section or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] or please add an answer to that Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="270cd-151">!</span><span class="sxs-lookup"><span data-stu-id="270cd-151">!</span></span>  

## <span data-ttu-id="270cd-152">Paso 2: depure contenido en su dispositivo Android desde su equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="270cd-152">Step 2: Debug content on your Android device from your development machine</span></span>   

1.  <span data-ttu-id="270cd-153">Abre Microsoft Edge en tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-153">Open Microsoft Edge on your Android device.</span></span>  

1.  <span data-ttu-id="270cd-154">En la pestaña **dispositivos remotos** , seleccione la pestaña que coincida con el nombre de su modelo de dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-154">In the **Remote Devices** tab, select the tab that matches your Android device model name.</span></span>  
    <span data-ttu-id="270cd-155">En la parte superior de esta página, verá el nombre del modelo de su dispositivo Android, seguido de su número de serie.</span><span class="sxs-lookup"><span data-stu-id="270cd-155">At the top of this page, you see the model name of your Android device, followed by its serial number.</span></span>  <span data-ttu-id="270cd-156">Debajo de eso, debería ver la versión de Microsoft Edge que se ejecuta en el dispositivo, con el número de versión entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="270cd-156">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="270cd-157">Cada pestaña abierta de Microsoft Edge obtiene su propia sección.</span><span class="sxs-lookup"><span data-stu-id="270cd-157">Each open Microsoft Edge tab gets its own section.</span></span>  <span data-ttu-id="270cd-158">Puede interactuar con esa pestaña de esta sección.</span><span class="sxs-lookup"><span data-stu-id="270cd-158">You may interact with that tab from this section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  <span data-ttu-id="270cd-159">En el cuadro de texto **nueva pestaña** , escriba una dirección URL y, después, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="270cd-159">In the **New tab** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="270cd-160">La página se abre en una nueva pestaña en su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-160">The page opens in a new tab on your Android device.</span></span>  

1.  <span data-ttu-id="270cd-161">Seleccione **inspeccionar** junto a la dirección URL que acaba de abrir.</span><span class="sxs-lookup"><span data-stu-id="270cd-161">Select **Inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="270cd-162">Se abrirá una nueva instancia de DevTools.</span><span class="sxs-lookup"><span data-stu-id="270cd-162">A new DevTools instance opens.</span></span>  <span data-ttu-id="270cd-163">La versión de Microsoft Edge que se ejecuta en su dispositivo Android determina la versión de DevTools que se abre en su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="270cd-163">The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.</span></span>  
    <span data-ttu-id="270cd-164">Por lo tanto, si su dispositivo Android está ejecutando una versión muy antigua de Microsoft Edge, la instancia de DevTools puede tener un aspecto muy diferente al que está acostumbrado.</span><span class="sxs-lookup"><span data-stu-id="270cd-164">So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.</span></span>  

### <span data-ttu-id="270cd-165">Más acciones: volver a cargar, enfocar o cerrar una pestaña</span><span class="sxs-lookup"><span data-stu-id="270cd-165">More actions: reload, focus, or close a tab</span></span>   

<span data-ttu-id="270cd-166">Seleccione **más opciones** `...` junto a la pestaña que desea volver a cargar, enfocar o cerrar.</span><span class="sxs-lookup"><span data-stu-id="270cd-166">Select **More Options** `...` next to the tab that you want to reload, focus, or close.</span></span>  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### <span data-ttu-id="270cd-167">Inspeccionar elementos</span><span class="sxs-lookup"><span data-stu-id="270cd-167">Inspect elements</span></span>   

<span data-ttu-id="270cd-168">Vaya al panel **elementos** de la instancia de DevTools y mantenga el mouse sobre un elemento para resaltarlo en el área de visualización de su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="270cd-169">También puede seleccionar un elemento de la pantalla de su dispositivo Android para seleccionarlo en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="270cd-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="270cd-170">Seleccione el elemento **Seleccionar elemento** ![ ][ImageSelectElementIcon] de la instancia de DevTools y, a continuación, seleccione el elemento en la pantalla de su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="270cd-171">**Seleccionar elemento** está deshabilitado después de la primera selección, por lo que debe volver a habilitarlo cada vez que desee usar esta característica.</span><span class="sxs-lookup"><span data-stu-id="270cd-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use this feature.</span></span>  

### <span data-ttu-id="270cd-172">Screencasts la pantalla de Android a su equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="270cd-172">Screencast your Android screen to your development machine</span></span>   

<span data-ttu-id="270cd-173">Seleccione **activar o** desactivar ![ la demostración de alternancia ][ImageToggleScreencastIcon] para ver el contenido de su dispositivo Android en la instancia de DevTools.</span><span class="sxs-lookup"><span data-stu-id="270cd-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="270cd-174">Puede interactuar con el screencast de varias maneras:</span><span class="sxs-lookup"><span data-stu-id="270cd-174">You are able to interact with the screencast in multiple ways:</span></span>  

*   <span data-ttu-id="270cd-175">Los clics se traducen en pulsaciones, lo que desencadena eventos táctiles adecuados en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="270cd-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="270cd-176">Las pulsaciones de tecla de tu equipo se envían al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="270cd-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="270cd-177">Para simular un gesto de reducir, espera `Shift` mientras arrastra.</span><span class="sxs-lookup"><span data-stu-id="270cd-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="270cd-178">Para desplazarse, use el panel táctil o la rueda del mouse, o Fling con el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="270cd-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

<span data-ttu-id="270cd-179">Algunas notas en los screencasts:</span><span class="sxs-lookup"><span data-stu-id="270cd-179">Some notes on screencasts:</span></span>  

*   <span data-ttu-id="270cd-180">Los screencasts solo muestran el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="270cd-180">Screencasts only display page content.</span></span>  <span data-ttu-id="270cd-181">Partes transparentes del screencast representan interfaces de dispositivo, como la barra de direcciones de Microsoft Edge, la barra de estado de Android o el teclado Android.</span><span class="sxs-lookup"><span data-stu-id="270cd-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
*   <span data-ttu-id="270cd-182">Los screencasts afectan negativamente a las tarifas de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="270cd-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="270cd-183">Deshabilite el screencasts y mida los desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="270cd-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
*   <span data-ttu-id="270cd-184">Si su dispositivo Android bloquea la pantalla, el contenido del screencast desaparecerá.</span><span class="sxs-lookup"><span data-stu-id="270cd-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="270cd-185">Desbloquear la pantalla de su dispositivo Android para reanudar automáticamente el screencast.</span><span class="sxs-lookup"><span data-stu-id="270cd-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  





<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
[ImageOpenRemoteDevices]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Remote-Debugging-More-Tools-Remote-Devices.msft.png "Ilustración 1: abrir la pestaña dispositivos remotos a través del menú principal"  
[ImageDiscoverUSBDevices]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Remote-Debugging-Remote-Devices-Tab.msft.png "Ilustración 2: la casilla descubrir dispositivos USB está habilitada"  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--connected-remote-device.msft.png "old Figure 5:  A connected remote device"  -->
<!--[ImageReload]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--reload.msft.png "old Figure 6: The menu for reloading, focusing, or closing a tab"  -->

<!-- links -->  

[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Instalar controladores USB para OEM | Desarrolladores de Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 "los dispositivos DevTools no detectan el dispositivo cuando el desbordamiento de pila está conectado"  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB-intercambio de pila de entusiastas de Android"  

> [!NOTE]
> <span data-ttu-id="270cd-192">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="270cd-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="270cd-193">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="270cd-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="270cd-195">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="270cd-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
