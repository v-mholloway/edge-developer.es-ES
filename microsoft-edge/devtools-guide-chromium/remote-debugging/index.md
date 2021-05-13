---
description: Depuración remota de contenido en directo en un dispositivo Android desde un Windows o un equipo macOS.
title: Introducción a la depuración remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d5a5ea8faef40925fb0fb986eb984ac9ae4f051b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565109"
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
# <a name="get-started-with-remote-debugging-android-devices"></a><span data-ttu-id="b2afb-104">Introducción a la depuración remota de dispositivos Android</span><span class="sxs-lookup"><span data-stu-id="b2afb-104">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="b2afb-105">Depuración remota de contenido en directo en un dispositivo Android desde Windows o equipo macOS.</span><span class="sxs-lookup"><span data-stu-id="b2afb-105">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="b2afb-106">La siguiente página de tutorial le enseña a completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b2afb-106">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="b2afb-107">Configura tu dispositivo Android para la depuración remota y descóyralo desde el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-107">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="b2afb-108">Inspecciona y depura contenido en directo en tu dispositivo Android desde el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-108">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="b2afb-109">Difusión de contenido desde el dispositivo Android a una instancia de DevTools en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-109">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="b2afb-110">Actualmente no se admite la depuración Microsoft Edge la aplicación en dispositivos iOS.</span><span class="sxs-lookup"><span data-stu-id="b2afb-110">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="b2afb-111">La siguiente guía se centra específicamente en la depuración remota Microsoft Edge dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-111">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="b2afb-112">Si tienes un dispositivo macOS, sigue la guía de depuración de [Brightcove][BrightcoveSupportDebuggingMobileDevices] para depurar de forma remota Microsoft Edge en un dispositivo iOS con Safari.</span><span class="sxs-lookup"><span data-stu-id="b2afb-112">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="b2afb-113">Para obtener más información acerca de la herramienta Inspector web en Safari, vaya a [Safari Web Development Tools][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="b2afb-113">For more information about the Web Inspector tool in Safari, navigate to [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <a name="step-1-discover-your-android-device"></a><span data-ttu-id="b2afb-114">Paso 1: Descubrir el dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="b2afb-114">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="b2afb-115">El flujo de trabajo siguiente funciona para la mayoría de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b2afb-115">The workflow below works for most users.</span></span>  <span data-ttu-id="b2afb-116">Para obtener más ayuda, vaya [a Solución de problemas: DevTools no detecta la sección dispositivo Android.](#troubleshooting-devtools-is-not-detecting-the-android-device)</span><span class="sxs-lookup"><span data-stu-id="b2afb-116">For more help, navigate to [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="b2afb-117">Abre la **pantalla Opciones de** desarrollador en tu Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-117">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="b2afb-118">Para obtener más información, vaya a [Configurar opciones de desarrollador en el dispositivo][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="b2afb-118">For more information, navigate to [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="b2afb-119">Elija **Habilitar depuración USB**.</span><span class="sxs-lookup"><span data-stu-id="b2afb-119">Choose **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="b2afb-120">En el equipo de desarrollo, abra Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b2afb-120">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="b2afb-121">Vaya a la `edge://inspect` página en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b2afb-121">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="La edge://inspect en Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="b2afb-123">Figura 1.</span><span class="sxs-lookup"><span data-stu-id="b2afb-123">Figure 1.</span></span>  <span data-ttu-id="b2afb-124">La `edge://inspect` página de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b2afb-124">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b2afb-125">Conectar el dispositivo Android directamente a la máquina de desarrollo mediante un cable USB.</span><span class="sxs-lookup"><span data-stu-id="b2afb-125">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="b2afb-126">La primera vez que intentes conectarte, debería mostrarse un mensaje sobre DevTools que detecta un dispositivo desconocido.</span><span class="sxs-lookup"><span data-stu-id="b2afb-126">The first time you try to connect, a prompt should be displayed about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="b2afb-127">Acepta el **símbolo del permiso Permitir depuración USB** en tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-127">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="El símbolo del sistema de permiso Permitir depuración USB en un dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="b2afb-129">Figura 2.</span><span class="sxs-lookup"><span data-stu-id="b2afb-129">Figure 2.</span></span>  <span data-ttu-id="b2afb-130">El **símbolo del sistema de permiso Permitir depuración USB** en un dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="b2afb-130">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b2afb-131">Si se muestra el nombre del modelo del dispositivo Android, Microsoft Edge ha establecido correctamente la conexión con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-131">If the model name of your Android device is displayed, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="b2afb-132">Continúe con la [sección Paso 2.](#step-2-debug-content-on-your-android-device-from-your-development-machine)</span><span class="sxs-lookup"><span data-stu-id="b2afb-132">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a><span data-ttu-id="b2afb-133">Solución de problemas: DevTools no detecta el dispositivo Android</span><span class="sxs-lookup"><span data-stu-id="b2afb-133">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="b2afb-134">Use las siguientes sugerencias para ayudarle a solucionar problemas con la configuración correcta del hardware.</span><span class="sxs-lookup"><span data-stu-id="b2afb-134">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="b2afb-135">Si usas un concentrador USB, prueba a conectar el dispositivo Android directamente a la máquina de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-135">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="b2afb-136">Prueba a desconectar el cable USB entre el dispositivo Android y la máquina de desarrollo y, a continuación, vuelve a conectar el cable USB.</span><span class="sxs-lookup"><span data-stu-id="b2afb-136">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="b2afb-137">Completa la tarea mientras se desbloquean las pantallas de la máquina de desarrollo y Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-137">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="b2afb-138">Asegúrese de que el cable USB funciona.</span><span class="sxs-lookup"><span data-stu-id="b2afb-138">Make sure that your USB cable works.</span></span>  <span data-ttu-id="b2afb-139">Debes poder inspeccionar los archivos del dispositivo Android desde el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-139">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="b2afb-140">Use las siguientes sugerencias para comprobar que el software está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="b2afb-140">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="b2afb-141">Si el equipo de desarrollo se Windows, intenta instalar manualmente los controladores USB para tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-141">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="b2afb-142">Para obtener más información, vaya a [Instalar controladores USB OEM.][AndroidDeveloperToolsOemUsb]</span><span class="sxs-lookup"><span data-stu-id="b2afb-142">For more information, navigate to [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="b2afb-143">Algunas combinaciones de Windows dispositivos Android \(especialmente Samsung\) requieren configuraciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="b2afb-143">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="b2afb-144">Para obtener más información, vaya [a DevTools Devices no detecta el dispositivo cuando está conectado][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="b2afb-144">For more information, navigate to [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="b2afb-145">Usa las siguientes sugerencias para ayudarte a solucionar problemas si el mensaje Permitir **depuración USB** no se muestra en tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-145">Use the following tips to help you troubleshoot if the **Allow USB Debugging** prompt is not displayed on your Android device.</span></span>  

*   <span data-ttu-id="b2afb-146">Desconectar y volver a conectar el cable USB mientras DevTools se centra en la máquina de desarrollo y se muestra la pantalla principal de Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-146">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b2afb-147">El mensaje se muestra si las pantallas de la máquina de desarrollo o Android están bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="b2afb-147">The prompt is displayed if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="b2afb-148">Actualizar la configuración de pantalla para el dispositivo Android y la máquina de desarrollo para que cada uno nunca entre en suspensión.</span><span class="sxs-lookup"><span data-stu-id="b2afb-148">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="b2afb-149">Establecer el modo USB para Android en PTP.</span><span class="sxs-lookup"><span data-stu-id="b2afb-149">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="b2afb-150">Para obtener más información, vaya [a Galaxy S4 no muestra el cuadro de diálogo Autorizar depuración USB][StackexchangeAndroid101933].</span><span class="sxs-lookup"><span data-stu-id="b2afb-150">For more information, navigate to [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="b2afb-151">Elige **Revocar autorizaciones de depuración USB** en la pantalla Opciones de desarrollador del dispositivo Android para restablecerla a un estado nuevo. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b2afb-151">Choose **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="b2afb-152">Si encuentras una solución que no se menciona en esta página o en [DevTools Devices][Stackoverflow21925992] no detecta el dispositivo cuando está conectado a Stack Overflow, agrega la solución a la pregunta Stack Overflow</span><span class="sxs-lookup"><span data-stu-id="b2afb-152">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="b2afb-153">.</span><span class="sxs-lookup"><span data-stu-id="b2afb-153">.</span></span>  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a><span data-ttu-id="b2afb-154">Paso 2: Depurar contenido en el dispositivo Android desde el equipo de desarrollo</span><span class="sxs-lookup"><span data-stu-id="b2afb-154">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="b2afb-155">Abre Microsoft Edge en tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-155">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="b2afb-156">Navegue hasta , se muestra el nombre del modelo del dispositivo `edge://inspect` Android, seguido del número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-156">Navigate to `edge://inspect`, the model name of your Android device is displayed, followed by the device serial number.</span></span>  <span data-ttu-id="b2afb-157">A continuación, se debe mostrar la versión Microsoft Edge que se ejecuta en el dispositivo, con el número de versión entre paréntesis.</span><span class="sxs-lookup"><span data-stu-id="b2afb-157">Below that, the version of Microsoft Edge running on the device should be displayed, with the version number in parentheses.</span></span>  <span data-ttu-id="b2afb-158">Cada pestaña Microsoft Edge obtiene una sección única.</span><span class="sxs-lookup"><span data-stu-id="b2afb-158">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="b2afb-159">Puede interactuar con esa pestaña desde una sección.</span><span class="sxs-lookup"><span data-stu-id="b2afb-159">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="b2afb-161">Figura 3.</span><span class="sxs-lookup"><span data-stu-id="b2afb-161">Figure 3.</span></span>  <span data-ttu-id="b2afb-162">Un dispositivo remoto conectado</span><span class="sxs-lookup"><span data-stu-id="b2afb-162">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b2afb-163">En el **cuadro de texto Abrir pestaña con dirección URL,** escriba una dirección URL y, a continuación, elija **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="b2afb-163">In the **Open tab with url** text box, enter a URL and then choose **Open**.</span></span>  <span data-ttu-id="b2afb-164">La página se abre en una nueva pestaña en el dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-164">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="b2afb-165">Elija **inspeccionar** junto a la dirección URL que acaba de abrir.</span><span class="sxs-lookup"><span data-stu-id="b2afb-165">Choose **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="b2afb-166">Se abre una nueva instancia de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b2afb-166">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a><span data-ttu-id="b2afb-167">Más acciones: enfocar, actualizar o cerrar una pestaña</span><span class="sxs-lookup"><span data-stu-id="b2afb-167">More actions: focus, refresh, or close a tab</span></span>  

<span data-ttu-id="b2afb-168">Elija **la pestaña foco,** **volver**a cargar o **cerrar** junto a la pestaña que desea enfocar, actualizar o cerrar.</span><span class="sxs-lookup"><span data-stu-id="b2afb-168">Choose **focus tab**, **reload**, or **close** next to the tab that you want to focus, refresh, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Botones para enfocar, actualizar o cerrar una pestaña" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="b2afb-170">Figura 4.</span><span class="sxs-lookup"><span data-stu-id="b2afb-170">Figure 4.</span></span>  <span data-ttu-id="b2afb-171">Botones para enfocar, actualizar o cerrar una pestaña</span><span class="sxs-lookup"><span data-stu-id="b2afb-171">The buttons for focusing, refreshing, or closing a tab</span></span>  
:::image-end:::  

### <a name="inspect-elements"></a><span data-ttu-id="b2afb-172">Inspeccionar elementos</span><span class="sxs-lookup"><span data-stu-id="b2afb-172">Inspect elements</span></span>  

<span data-ttu-id="b2afb-173">Vaya a la **herramienta Elementos** de la instancia de DevTools y mantenga el mouse sobre un elemento para resaltarlo en la ventanilla del dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-173">Navigate to the **Elements** tool of your DevTools instance, and hover on an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="b2afb-174">También puedes seleccionar un elemento en la pantalla del dispositivo Android para seleccionarlo en la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="b2afb-174">You may also select an element on your Android device screen to select it in the **Elements** tool.</span></span>  <span data-ttu-id="b2afb-175">Elija **Seleccionar elemento** \( Seleccionar elemento \) icono en la instancia de ![ DevTools y, a continuación, seleccione ](../media/select-element-icon.msft.png) el elemento en la pantalla del dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="b2afb-175">Choose **Select Element** \(![Select Element](../media/select-element-icon.msft.png)\) icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="b2afb-176">**Select Element** está deshabilitado después de la primera selección, por lo que debes volver a habilitarlo cada vez que quieras usar la característica.</span><span class="sxs-lookup"><span data-stu-id="b2afb-176">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <a name="screencast-your-android-screen-to-your-development-machine"></a><span data-ttu-id="b2afb-177">Difusión en pantalla de la pantalla de Android a la máquina de desarrollo</span><span class="sxs-lookup"><span data-stu-id="b2afb-177">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="b2afb-178">Elija **Alternar difusión** de pantalla \( Alternar difusión por pantalla \) icono para ver el contenido de su dispositivo ![ Android en la instancia de ](../media/toggle-screencast-icon.msft.png) DevTools.</span><span class="sxs-lookup"><span data-stu-id="b2afb-178">Choose **Toggle Screencast** \(![Toggle Screencast](../media/toggle-screencast-icon.msft.png)\) icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="b2afb-179">Puede interactuar con la difusión en pantalla de las siguientes maneras.</span><span class="sxs-lookup"><span data-stu-id="b2afb-179">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="b2afb-180">Las opciones se traducen en pulsaciones, lo que dispara los eventos táctiles adecuados en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-180">Chooses are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="b2afb-181">Las pulsaciones de teclas del equipo se envían al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b2afb-181">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="b2afb-182">Para simular un gesto de pellizco, mantén `Shift` presionado mientras arrastras.</span><span class="sxs-lookup"><span data-stu-id="b2afb-182">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="b2afb-183">Para desplazarse, use el trackpad o la rueda del mouse o fling con el puntero del mouse.</span><span class="sxs-lookup"><span data-stu-id="b2afb-183">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="b2afb-184">Usa las siguientes sugerencias para ayudarte a la difusión en pantalla.</span><span class="sxs-lookup"><span data-stu-id="b2afb-184">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="b2afb-185">Los difusión en pantalla solo muestran el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="b2afb-185">Screencasts only display page content.</span></span>  <span data-ttu-id="b2afb-186">Las partes transparentes de la difusión en pantalla representan interfaces de dispositivo, como la barra de direcciones Microsoft Edge, la barra de estado de Android o el teclado androide.</span><span class="sxs-lookup"><span data-stu-id="b2afb-186">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="b2afb-187">Las difusión en pantalla afectan negativamente a las tasas de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b2afb-187">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="b2afb-188">Deshabilite la difusión por pantalla al medir desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.</span><span class="sxs-lookup"><span data-stu-id="b2afb-188">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="b2afb-189">Si la pantalla del dispositivo Android se bloquea, el contenido de la difusión en pantalla desaparece.</span><span class="sxs-lookup"><span data-stu-id="b2afb-189">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="b2afb-190">Desbloquea la pantalla del dispositivo Android para reanudar automáticamente la difusión por pantalla.</span><span class="sxs-lookup"><span data-stu-id="b2afb-190">Unlock your Android device screen to automatically resume the screencast.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b2afb-191">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b2afb-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurar opciones de desarrollador en el dispositivo | Desarrollador de Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Instalar controladores USB OEM | Desarrolladores de Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Herramientas de desarrollo web de Safari | Desarrollador de Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://general.support.brightcove.com/developer/debugging-mobile-devices.html "Depuración en dispositivos móviles | Compatibilidad con Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb: pila de entusiastas de Android Exchange"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Dispositivos DevTools no detecta el dispositivo cuando está conectado: desbordamiento de pila"  

> [!NOTE]
> <span data-ttu-id="b2afb-198">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b2afb-198">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b2afb-199">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b2afb-199">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b2afb-201">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b2afb-201">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
