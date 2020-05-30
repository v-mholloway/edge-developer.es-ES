---
title: Introducción a la depuración remota dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fc7450ba2b088eee8f4005216374980096cbb067
ms.sourcegitcommit: ba9f0ed77e84174b03262b17e62c6a7e26cfeb3d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/30/2020
ms.locfileid: "10688170"
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

# <span data-ttu-id="c0a14-103">Introducción a la depuración remota dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="c0a14-103">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="c0a14-104">Depure de forma remota contenido en vivo en un dispositivo Android desde su equipo con Windows o macOS.</span><span class="sxs-lookup"><span data-stu-id="c0a14-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="c0a14-105">Esta página del tutorial le enseña a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="c0a14-105">This tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="c0a14-106">Configure su dispositivo Android para la depuración remota y descárguelo desde el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="c0a14-107">Inspeccione y depure contenido en vivo en su dispositivo Android desde su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="c0a14-108">Contenido de screencast de su dispositivo Android en una instancia de DevTools en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

## <span data-ttu-id="c0a14-109">Paso 1: descubrir su dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="c0a14-109">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="c0a14-110">El flujo de trabajo siguiente funciona para la mayoría de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c0a14-110">The workflow below works for most users.</span></span>  <span data-ttu-id="c0a14-111">Consulte [solución de problemas: DevTools no detecta el dispositivo Android](#troubleshooting-devtools-is-not-detecting-the-android-device) para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="c0a14-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="c0a14-112">Abra la pantalla **Opciones del desarrollador** en Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="c0a14-113">Para obtener más información, vea [configurar las opciones de Desarrollador en dispositivos](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="c0a14-113">For more information, see [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="c0a14-114">Seleccione **Habilitar depuración USB**.</span><span class="sxs-lookup"><span data-stu-id="c0a14-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="c0a14-115">En tu equipo de desarrollo, abre Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c0a14-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="c0a14-116">Vaya a la `edge://inspect` Página de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c0a14-116">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="La página edge://inspect en Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="c0a14-118">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="c0a14-118">Figure 1.</span></span>  <span data-ttu-id="c0a14-119">La `edge://inspect` página en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c0a14-119">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c0a14-120">Conecta el dispositivo Android directamente a tu equipo de desarrollo con un cable USB.</span><span class="sxs-lookup"><span data-stu-id="c0a14-120">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="c0a14-121">La primera vez que intentes conectarte, normalmente verás pregunta sobre DevTools detectando un dispositivo desconocido.</span><span class="sxs-lookup"><span data-stu-id="c0a14-121">The first time you try to connect, you usually see prompt about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="c0a14-122">Acepte la solicitud de permiso de **depuración USB** en su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-122">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="La solicitud de permiso de depuración USB en un dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="c0a14-124">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="c0a14-124">Figure 2.</span></span>  <span data-ttu-id="c0a14-125">La solicitud de permiso de **depuración USB** en un dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="c0a14-125">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c0a14-126">Si ve el nombre del modelo de su dispositivo Android, Microsoft Edge ha establecido correctamente la conexión con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-126">If you see the model name of your Android device, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="c0a14-127">Continúe con el [paso 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span><span class="sxs-lookup"><span data-stu-id="c0a14-127">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="c0a14-128">Solución de problemas: DevTools no detecta el dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="c0a14-128">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="c0a14-129">Use las siguientes sugerencias para solucionar problemas relacionados con la configuración correcta de su hardware.</span><span class="sxs-lookup"><span data-stu-id="c0a14-129">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="c0a14-130">Si está usando un concentrador USB, intente conectar el dispositivo Android directamente a su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-130">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="c0a14-131">Intenta desconectar el cable USB entre el dispositivo Android y el equipo de desarrollo y, a continuación, vuelve a conectar tu cable USB.</span><span class="sxs-lookup"><span data-stu-id="c0a14-131">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="c0a14-132">Complete la tarea mientras las pantallas de Android y de equipo de desarrollo estén desbloqueadas.</span><span class="sxs-lookup"><span data-stu-id="c0a14-132">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="c0a14-133">Asegúrate de que tu cable USB funcione.</span><span class="sxs-lookup"><span data-stu-id="c0a14-133">Make sure that your USB cable works.</span></span>  <span data-ttu-id="c0a14-134">Debería poder inspeccionar los archivos de su dispositivo Android desde su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-134">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="c0a14-135">Use las siguientes sugerencias para comprobar que el software está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c0a14-135">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="c0a14-136">Si tu equipo de desarrollo ejecuta Windows, intenta instalar manualmente los drivers USB para tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-136">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="c0a14-137">Para obtener más información, consulte [instalar controladores de OEM USB][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="c0a14-137">For more information, see [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
*   <span data-ttu-id="c0a14-138">Algunas combinaciones de Windows y dispositivos Android \ (especialmente Samsung \) requieren configuración adicional.</span><span class="sxs-lookup"><span data-stu-id="c0a14-138">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="c0a14-139">Para obtener más información, consulte [DevTools los dispositivos no detectan el dispositivo cuando está conectado] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="c0a14-139">For more information, see [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  

<span data-ttu-id="c0a14-140">Use las siguientes sugerencias para evitar que se vea el aviso de **depuración USB** en su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-140">Use the following tips to help you troubleshoot not seeing the **Allow USB Debugging** prompt on your Android device.</span></span>  

*   <span data-ttu-id="c0a14-141">Desconectar y volver a conectar el cable USB mientras DevTools está en el equipo de desarrollo y se muestra el pantalla Android de Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-141">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c0a14-142">Es posible que no vea el mensaje si su pantalla de Android o de equipo de desarrollo está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="c0a14-142">You may not see the prompt if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="c0a14-143">Actualización de la configuración de pantalla de su dispositivo Android y de la máquina de desarrollo para que cada uno nunca vaya al modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="c0a14-143">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="c0a14-144">Configuración del modo USB para Android en PTP.</span><span class="sxs-lookup"><span data-stu-id="c0a14-144">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="c0a14-145">Para obtener más información, consulte [Galaxy S4 no muestra el cuadro de diálogo autorizar depuración USB][StackExchangeGalaxyS4DoesNotShowDialogBox].</span><span class="sxs-lookup"><span data-stu-id="c0a14-145">For more information, see [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="c0a14-146">Seleccione **revocar las autorizaciones de depuración USB** en la pantalla de **Opciones del desarrollador** de su dispositivo Android para restablecerla a un estado actualizado.</span><span class="sxs-lookup"><span data-stu-id="c0a14-146">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="c0a14-147">Si encuentra una solución que no se menciona en esta página o [los dispositivos DevTools no detectan el dispositivo cuando está conectado] [StackOverflowDevicesNotDetected] en desbordamiento de pila, agregue la solución a la pregunta de desbordamiento de pila.</span><span class="sxs-lookup"><span data-stu-id="c0a14-147">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="c0a14-148">!</span><span class="sxs-lookup"><span data-stu-id="c0a14-148">!</span></span>  

## <span data-ttu-id="c0a14-149">Paso 2: depure contenido en su dispositivo Android desde su equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="c0a14-149">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="c0a14-150">Abre Microsoft Edge en tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-150">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="c0a14-151">En la `edge://inspect` página, verá el nombre del modelo de su dispositivo Android, seguido del número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-151">From the `edge://inspect` page, you see the model name of your Android device, followed by the device serial number.</span></span>  <span data-ttu-id="c0a14-152">Debajo de eso, debería ver la versión de Microsoft Edge que se ejecuta en el dispositivo, con el número de versión entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="c0a14-152">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="c0a14-153">Cada pestaña abierta de Microsoft Edge obtiene una sección única.</span><span class="sxs-lookup"><span data-stu-id="c0a14-153">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="c0a14-154">Puede interactuar con esa pestaña en una sección.</span><span class="sxs-lookup"><span data-stu-id="c0a14-154">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="c0a14-156">Figura 3.</span><span class="sxs-lookup"><span data-stu-id="c0a14-156">Figure 3.</span></span>  <span data-ttu-id="c0a14-157">Un dispositivo remoto conectado</span><span class="sxs-lookup"><span data-stu-id="c0a14-157">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c0a14-158">En el cuadro de texto **pestaña abrir con dirección URL** , escriba una dirección URL y, a continuación, seleccione **abrir**.</span><span class="sxs-lookup"><span data-stu-id="c0a14-158">In the **Open tab with url** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="c0a14-159">La página se abre en una nueva pestaña en su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-159">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="c0a14-160">Seleccione **inspeccionar** junto a la dirección URL que acaba de abrir.</span><span class="sxs-lookup"><span data-stu-id="c0a14-160">Select **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="c0a14-161">Se abrirá una nueva instancia de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c0a14-161">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="c0a14-162">Más acciones: foco, volver a cargar o cerrar una pestaña</span><span class="sxs-lookup"><span data-stu-id="c0a14-162">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="c0a14-163">Seleccione la **pestaña foco**, **volver a cargar**o **cerca** de la pestaña que desea centrar, volver a cargar o cerrar.</span><span class="sxs-lookup"><span data-stu-id="c0a14-163">Select **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Botones para centrar, volver a cargar o cerrar una pestaña" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="c0a14-165">Figura 4.</span><span class="sxs-lookup"><span data-stu-id="c0a14-165">Figure 4.</span></span>  <span data-ttu-id="c0a14-166">Botones para centrar, volver a cargar o cerrar una pestaña</span><span class="sxs-lookup"><span data-stu-id="c0a14-166">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="c0a14-167">Inspeccionar elementos</span><span class="sxs-lookup"><span data-stu-id="c0a14-167">Inspect elements</span></span>  

<span data-ttu-id="c0a14-168">Vaya al panel **elementos** de la instancia de DevTools y mantenga el mouse sobre un elemento para resaltarlo en el área de visualización de su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="c0a14-169">También puede seleccionar un elemento de la pantalla de su dispositivo Android para seleccionarlo en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="c0a14-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="c0a14-170">Seleccione **Select Element** ![ ][ImageSelectElementIcon] el icono de elemento seleccionar elemento en la instancia de DevTools y, a continuación, seleccione el elemento en la pantalla de su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="c0a14-171">**Seleccionar elemento** está deshabilitado después de la primera selección, por lo que debe volver a habilitarlo cada vez que desee usar la característica.</span><span class="sxs-lookup"><span data-stu-id="c0a14-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="c0a14-172">Screencasts la pantalla de Android a su equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="c0a14-172">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="c0a14-173">Seleccione **activar o desactivar** ![ ][ImageToggleScreencastIcon] el icono del screencast para ver el contenido de su dispositivo Android en la instancia de DevTools.</span><span class="sxs-lookup"><span data-stu-id="c0a14-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="c0a14-174">Puede interactuar con el screencast de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="c0a14-174">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="c0a14-175">Los clics se traducen en pulsaciones, lo que desencadena eventos táctiles adecuados en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="c0a14-176">Las pulsaciones de tecla de tu equipo se envían al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0a14-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="c0a14-177">Para simular un gesto de reducir, espera `Shift` mientras arrastra.</span><span class="sxs-lookup"><span data-stu-id="c0a14-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="c0a14-178">Para desplazarse, use el panel táctil o la rueda del mouse, o Fling con el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="c0a14-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="c0a14-179">Use las siguientes sugerencias para ayudarle con el screencast.</span><span class="sxs-lookup"><span data-stu-id="c0a14-179">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="c0a14-180">Los screencasts solo muestran el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="c0a14-180">Screencasts only display page content.</span></span>  <span data-ttu-id="c0a14-181">Partes transparentes del screencast representan interfaces de dispositivo, como la barra de direcciones de Microsoft Edge, la barra de estado de Android o el teclado Android.</span><span class="sxs-lookup"><span data-stu-id="c0a14-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="c0a14-182">Los screencasts afectan negativamente a las tarifas de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="c0a14-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="c0a14-183">Deshabilite el screencasts y mida los desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="c0a14-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="c0a14-184">Si su dispositivo Android bloquea la pantalla, el contenido del screencast desaparecerá.</span><span class="sxs-lookup"><span data-stu-id="c0a14-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="c0a14-185">Desbloquear la pantalla de su dispositivo Android para reanudar automáticamente el screencast.</span><span class="sxs-lookup"><span data-stu-id="c0a14-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
<!--[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-no-targets.msft.png "Figure 1: The edge://inspect page in Microsoft Edge"  -->  
<!--[ImageAndroidPermissionPrompt]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-android-permissions-prompt.msft.png "Figure 2: The Allow USB Debugging permission prompt on an Android device"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-with-targets.msft.png "Figure 3: A connected remote device"  -->  
<!-- [ImageReload]:  /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-with-targets-buttons.msft.png "Figure 4: The buttons for focusing, reloading, or closing a tab"  -->  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  

<!-- links -->  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Instalar controladores USB para OEM | Desarrolladores de Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 "los dispositivos DevTools no detectan el dispositivo cuando el desbordamiento de pila está conectado"  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB-intercambio de pila de entusiastas de Android"  

> [!NOTE]
> <span data-ttu-id="c0a14-189">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c0a14-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c0a14-190">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c0a14-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c0a14-192">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c0a14-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
