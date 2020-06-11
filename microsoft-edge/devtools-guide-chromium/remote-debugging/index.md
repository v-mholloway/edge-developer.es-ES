---
title: Introducción a la depuración remota dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c77633c4844f0e576b7dff6574000a78c8c083da
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708539"
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

# <span data-ttu-id="a1775-103">Introducción a la depuración remota dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="a1775-103">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="a1775-104">Depure de forma remota contenido en vivo en un dispositivo Android desde su equipo con Windows o macOS.</span><span class="sxs-lookup"><span data-stu-id="a1775-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="a1775-105">La siguiente página del tutorial le enseña a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="a1775-105">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="a1775-106">Configure su dispositivo Android para la depuración remota y descárguelo desde el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a1775-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="a1775-107">Inspeccione y depure contenido en vivo en su dispositivo Android desde su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a1775-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="a1775-108">Contenido de screencast de su dispositivo Android en una instancia de DevTools en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a1775-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="a1775-109">La depuración remota de la aplicación Microsoft Edge en dispositivos iOS no es compatible actualmente.</span><span class="sxs-lookup"><span data-stu-id="a1775-109">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="a1775-110">La siguiente guía está específicamente centrada en la depuración remota de Microsoft Edge en dispositivos con Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-110">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="a1775-111">Si tiene un dispositivo macOS, siga la [Guía de depuración Brightcove][BrightcoveSupportDebuggingMobileDevices] para depurar Microsoft Edge de forma remota en un dispositivo iOS con Safari.</span><span class="sxs-lookup"><span data-stu-id="a1775-111">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="a1775-112">Para obtener más información sobre la herramienta Web Inspector de Safari, vea [herramientas de desarrollo web de Safari][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="a1775-112">For more information about the Web Inspector tool in Safari, see [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <span data-ttu-id="a1775-113">Paso 1: descubrir su dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="a1775-113">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="a1775-114">El flujo de trabajo siguiente funciona para la mayoría de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a1775-114">The workflow below works for most users.</span></span>  <span data-ttu-id="a1775-115">Para obtener más ayuda, consulte la [solución de problemas: DevTools no detecta la sección del dispositivo Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="a1775-115">For more help, see the [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="a1775-116">Abra la pantalla **Opciones del desarrollador** en Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-116">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="a1775-117">Para obtener más información, vea [configurar las opciones de Desarrollador en dispositivos][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="a1775-117">For more information, see [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="a1775-118">Seleccione **Habilitar depuración USB**.</span><span class="sxs-lookup"><span data-stu-id="a1775-118">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="a1775-119">En tu equipo de desarrollo, abre Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a1775-119">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="a1775-120">Vaya a la `edge://inspect` Página de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a1775-120">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="La página edge://inspect en Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="a1775-122">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="a1775-122">Figure 1.</span></span>  <span data-ttu-id="a1775-123">La `edge://inspect` página en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a1775-123">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a1775-124">Conecta el dispositivo Android directamente a tu equipo de desarrollo con un cable USB.</span><span class="sxs-lookup"><span data-stu-id="a1775-124">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="a1775-125">La primera vez que intentes conectarte, normalmente verás pregunta sobre DevTools detectando un dispositivo desconocido.</span><span class="sxs-lookup"><span data-stu-id="a1775-125">The first time you try to connect, you usually see prompt about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="a1775-126">Acepte la solicitud de permiso de **depuración USB** en su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-126">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="La solicitud de permiso de depuración USB en un dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="a1775-128">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="a1775-128">Figure 2.</span></span>  <span data-ttu-id="a1775-129">La solicitud de permiso de **depuración USB** en un dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="a1775-129">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a1775-130">Si ve el nombre del modelo de su dispositivo Android, Microsoft Edge ha establecido correctamente la conexión con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1775-130">If you see the model name of your Android device, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="a1775-131">Continúe con la sección [paso 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .</span><span class="sxs-lookup"><span data-stu-id="a1775-131">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="a1775-132">Solución de problemas: DevTools no detecta el dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="a1775-132">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="a1775-133">Use las siguientes sugerencias para solucionar problemas relacionados con la configuración correcta de su hardware.</span><span class="sxs-lookup"><span data-stu-id="a1775-133">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="a1775-134">Si está usando un concentrador USB, intente conectar el dispositivo Android directamente a su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a1775-134">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="a1775-135">Intenta desconectar el cable USB entre el dispositivo Android y el equipo de desarrollo y, a continuación, vuelve a conectar tu cable USB.</span><span class="sxs-lookup"><span data-stu-id="a1775-135">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="a1775-136">Complete la tarea mientras las pantallas de Android y de equipo de desarrollo estén desbloqueadas.</span><span class="sxs-lookup"><span data-stu-id="a1775-136">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="a1775-137">Asegúrate de que tu cable USB funcione.</span><span class="sxs-lookup"><span data-stu-id="a1775-137">Make sure that your USB cable works.</span></span>  <span data-ttu-id="a1775-138">Debería poder inspeccionar los archivos de su dispositivo Android desde su equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="a1775-138">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="a1775-139">Use las siguientes sugerencias para comprobar que el software está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a1775-139">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="a1775-140">Si tu equipo de desarrollo ejecuta Windows, intenta instalar manualmente los drivers USB para tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-140">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="a1775-141">Para obtener más información, consulte [instalar controladores de OEM USB][AndroidDeveloperToolsOemUsb].</span><span class="sxs-lookup"><span data-stu-id="a1775-141">For more information, see [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="a1775-142">Algunas combinaciones de Windows y dispositivos Android \ (especialmente Samsung \) requieren configuración adicional.</span><span class="sxs-lookup"><span data-stu-id="a1775-142">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="a1775-143">Para obtener más información, consulte los [dispositivos de DevTools no detectan el dispositivo cuando está conectado][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="a1775-143">For more information, see [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="a1775-144">Use las siguientes sugerencias para evitar que se vea el aviso de **depuración USB** en su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-144">Use the following tips to help you troubleshoot not seeing the **Allow USB Debugging** prompt on your Android device.</span></span>  

*   <span data-ttu-id="a1775-145">Desconectar y volver a conectar el cable USB mientras DevTools está en el equipo de desarrollo y se muestra el pantalla Android de Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-145">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a1775-146">Es posible que no vea el mensaje si su pantalla de Android o de equipo de desarrollo está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="a1775-146">You may not see the prompt if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="a1775-147">Actualización de la configuración de pantalla de su dispositivo Android y de la máquina de desarrollo para que cada uno nunca vaya al modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="a1775-147">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="a1775-148">Configuración del modo USB para Android en PTP.</span><span class="sxs-lookup"><span data-stu-id="a1775-148">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="a1775-149">Para obtener más información, consulte [Galaxy S4 no muestra el cuadro de diálogo autorizar depuración USB][StackexchangeAndroid101933].</span><span class="sxs-lookup"><span data-stu-id="a1775-149">For more information, see [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="a1775-150">Seleccione **revocar las autorizaciones de depuración USB** en la pantalla de **Opciones del desarrollador** de su dispositivo Android para restablecerla a un estado actualizado.</span><span class="sxs-lookup"><span data-stu-id="a1775-150">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="a1775-151">Si encuentra una solución que no está mencionada en esta página o en [DevTools dispositivos no detecta el dispositivo cuando está conectado][Stackoverflow21925992] al desbordamiento de la pila, agregue la solución a la pregunta de desbordamiento de pila.</span><span class="sxs-lookup"><span data-stu-id="a1775-151">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="a1775-152">!</span><span class="sxs-lookup"><span data-stu-id="a1775-152">!</span></span>  

## <span data-ttu-id="a1775-153">Paso 2: depure contenido en su dispositivo Android desde su equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="a1775-153">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="a1775-154">Abre Microsoft Edge en tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-154">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="a1775-155">En la `edge://inspect` página, verá el nombre del modelo de su dispositivo Android, seguido del número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1775-155">From the `edge://inspect` page, you see the model name of your Android device, followed by the device serial number.</span></span>  <span data-ttu-id="a1775-156">Debajo de eso, debería ver la versión de Microsoft Edge que se ejecuta en el dispositivo, con el número de versión entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="a1775-156">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="a1775-157">Cada pestaña abierta de Microsoft Edge obtiene una sección única.</span><span class="sxs-lookup"><span data-stu-id="a1775-157">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="a1775-158">Puede interactuar con esa pestaña en una sección.</span><span class="sxs-lookup"><span data-stu-id="a1775-158">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="a1775-160">Figura 3.</span><span class="sxs-lookup"><span data-stu-id="a1775-160">Figure 3.</span></span>  <span data-ttu-id="a1775-161">Un dispositivo remoto conectado</span><span class="sxs-lookup"><span data-stu-id="a1775-161">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a1775-162">En el cuadro de texto **pestaña abrir con dirección URL** , escriba una dirección URL y, a continuación, seleccione **abrir**.</span><span class="sxs-lookup"><span data-stu-id="a1775-162">In the **Open tab with url** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="a1775-163">La página se abre en una nueva pestaña en su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-163">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="a1775-164">Seleccione **inspeccionar** junto a la dirección URL que acaba de abrir.</span><span class="sxs-lookup"><span data-stu-id="a1775-164">Select **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="a1775-165">Se abrirá una nueva instancia de DevTools.</span><span class="sxs-lookup"><span data-stu-id="a1775-165">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="a1775-166">Más acciones: foco, volver a cargar o cerrar una pestaña</span><span class="sxs-lookup"><span data-stu-id="a1775-166">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="a1775-167">Seleccione la **pestaña foco**, **volver a cargar**o **cerca** de la pestaña que desea centrar, volver a cargar o cerrar.</span><span class="sxs-lookup"><span data-stu-id="a1775-167">Select **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Botones para centrar, volver a cargar o cerrar una pestaña" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="a1775-169">Figura 4.</span><span class="sxs-lookup"><span data-stu-id="a1775-169">Figure 4.</span></span>  <span data-ttu-id="a1775-170">Botones para centrar, volver a cargar o cerrar una pestaña</span><span class="sxs-lookup"><span data-stu-id="a1775-170">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="a1775-171">Inspeccionar elementos</span><span class="sxs-lookup"><span data-stu-id="a1775-171">Inspect elements</span></span>  

<span data-ttu-id="a1775-172">Vaya al panel **elementos** de la instancia de DevTools y mantenga el mouse sobre un elemento para resaltarlo en el área de visualización de su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-172">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="a1775-173">También puede seleccionar un elemento de la pantalla de su dispositivo Android para seleccionarlo en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="a1775-173">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="a1775-174">Seleccione **Select Element** ![ ][ImageSelectElementIcon] el icono de elemento seleccionar elemento en la instancia de DevTools y, a continuación, seleccione el elemento en la pantalla de su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-174">Select **Select Element** ![Select Element][ImageSelectElementIcon] icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="a1775-175">**Seleccionar elemento** está deshabilitado después de la primera selección, por lo que debe volver a habilitarlo cada vez que desee usar la característica.</span><span class="sxs-lookup"><span data-stu-id="a1775-175">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="a1775-176">Screencasts la pantalla de Android a su equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="a1775-176">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="a1775-177">Seleccione **activar o desactivar** ![ ][ImageToggleScreencastIcon] el icono del screencast para ver el contenido de su dispositivo Android en la instancia de DevTools.</span><span class="sxs-lookup"><span data-stu-id="a1775-177">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="a1775-178">Puede interactuar con el screencast de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="a1775-178">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="a1775-179">Los clics se traducen en pulsaciones, lo que desencadena eventos táctiles adecuados en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1775-179">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="a1775-180">Las pulsaciones de tecla de tu equipo se envían al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1775-180">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="a1775-181">Para simular un gesto de reducir, espera `Shift` mientras arrastra.</span><span class="sxs-lookup"><span data-stu-id="a1775-181">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="a1775-182">Para desplazarse, use el panel táctil o la rueda del mouse, o Fling con el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="a1775-182">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="a1775-183">Use las siguientes sugerencias para ayudarle con el screencast.</span><span class="sxs-lookup"><span data-stu-id="a1775-183">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="a1775-184">Los screencasts solo muestran el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="a1775-184">Screencasts only display page content.</span></span>  <span data-ttu-id="a1775-185">Partes transparentes del screencast representan interfaces de dispositivo, como la barra de direcciones de Microsoft Edge, la barra de estado de Android o el teclado Android.</span><span class="sxs-lookup"><span data-stu-id="a1775-185">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="a1775-186">Los screencasts afectan negativamente a las tarifas de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="a1775-186">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="a1775-187">Deshabilite el screencasts y mida los desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="a1775-187">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="a1775-188">Si su dispositivo Android bloquea la pantalla, el contenido del screencast desaparecerá.</span><span class="sxs-lookup"><span data-stu-id="a1775-188">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="a1775-189">Desbloquear la pantalla de su dispositivo Android para reanudar automáticamente el screencast.</span><span class="sxs-lookup"><span data-stu-id="a1775-189">Unlock your Android device screen to automatically resume the screencast.</span></span>  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurar opciones de Desarrollador en el dispositivo | Desarrollador de Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Instalar controladores USB para OEM | Desarrolladores de Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Herramientas de desarrollo web de Safari | Desarrollador de Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Depurar en dispositivos móviles | Soporte técnico de Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "ADB-intercambio de pila de entusiastas de Android"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Los dispositivos DevTools no detectan el dispositivo cuando está conectado el desbordamiento de pila"  

> [!NOTE]
> <span data-ttu-id="a1775-196">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a1775-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a1775-197">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a1775-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a1775-199">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a1775-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
