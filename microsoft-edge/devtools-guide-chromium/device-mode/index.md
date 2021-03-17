---
description: Usa dispositivos virtuales en Microsoft Edge para crear sitios web móviles.
title: Emular dispositivos móviles en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, emulación, dispositivo, simulación, móvil
ms.openlocfilehash: bb081ddd5f773e5e9ae6a1b83b5fcb13408df6cb
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439454"
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

# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a><span data-ttu-id="ea9cd-104">Emular dispositivos móviles en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ea9cd-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="ea9cd-105">Usa **la emulación de dispositivo para** aproximar el aspecto de la página y cómo responde en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="ea9cd-106">Microsoft Edge DevTools proporciona una colección de características que le ayudarán a emular dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="ea9cd-107">La colección incluye las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="ea9cd-108">Simular una ventanilla móvil</span><span class="sxs-lookup"><span data-stu-id="ea9cd-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="ea9cd-109">Limitar la red</span><span class="sxs-lookup"><span data-stu-id="ea9cd-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="ea9cd-110">Limitar la CPU</span><span class="sxs-lookup"><span data-stu-id="ea9cd-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="ea9cd-111">Simular geolocalización</span><span class="sxs-lookup"><span data-stu-id="ea9cd-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="ea9cd-112">Establecer orientación</span><span class="sxs-lookup"><span data-stu-id="ea9cd-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="ea9cd-113">Establecer la cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="ea9cd-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <a name="limitations"></a><span data-ttu-id="ea9cd-114">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="ea9cd-114">Limitations</span></span>  

<span data-ttu-id="ea9cd-115">**La emulación de dispositivo** [es][WikiApproximation] una aproximación de primer orden de la apariencia de la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="ea9cd-116">**La emulación de** dispositivos no ejecuta realmente el código en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="ea9cd-117">En su lugar, simulas la experiencia del usuario móvil desde tu portátil o escritorio.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="ea9cd-118">Algunos aspectos de los dispositivos móviles nunca se emulan en DevTools.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="ea9cd-119">Por ejemplo, la arquitectura de las CPU móviles es diferente de la arquitectura de las CPU de equipos portátiles o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="ea9cd-120">Cuando hay dudas, la mejor opción es ejecutar la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="ea9cd-121">Use [Depuración remota][DevToolsRemoteDebugging] para interactuar con el código de una página desde el equipo mientras la página se ejecuta realmente en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="ea9cd-122">Puede ver, cambiar, depurar, perfil o los cuatro mientras interactúa con el código.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="ea9cd-123">El equipo puede ser un bloc de notas o un equipo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-123">Your machine may be a notebook or desktop computer.</span></span>  

## <a name="simulate-a-mobile-viewport"></a><span data-ttu-id="ea9cd-124">Simular una ventanilla móvil</span><span class="sxs-lookup"><span data-stu-id="ea9cd-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="ea9cd-125">Elija **Alternar emulación** de dispositivo \( Alternar barra de herramientas del dispositivo \) o elija Personalizar y ![ controlar ](../media/toggle-device-toolbar-dark-icon.msft.png) **DevTools** \( `...` \) \*\*\*\* emulación de dispositivo > para abrir la interfaz de usuario que permite simular una ventanilla móvil.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar](../media/toggle-device-toolbar-dark-icon.msft.png)\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="ea9cd-127">La barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ea9cd-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="ea9cd-128">De forma predeterminada, la barra de herramientas del dispositivo se abre en modo de ventanilla dinámica.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <a name="responsive-viewport-mode"></a><span data-ttu-id="ea9cd-129">Modo de ventanilla dinámica</span><span class="sxs-lookup"><span data-stu-id="ea9cd-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="ea9cd-130">Para probar rápidamente el aspecto de la página en varios tamaños de pantalla, arrastre los controladores para cambiar el tamaño de la ventanilla a las dimensiones necesarias.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="ea9cd-131">También puede especificar valores específicos en los cuadros de ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="ea9cd-132">En la figura siguiente, el ancho se establece en `626` y el alto se establece en `516` .</span><span class="sxs-lookup"><span data-stu-id="ea9cd-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Los controladores para cambiar las dimensiones de la ventanilla cuando se encuentra en modo de ventanilla dinámica" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="ea9cd-134">Los controladores para cambiar las dimensiones de la ventanilla cuando se encuentra en modo de ventanilla dinámica</span><span class="sxs-lookup"><span data-stu-id="ea9cd-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <a name="show-media-queries"></a><span data-ttu-id="ea9cd-135">Mostrar consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="ea9cd-135">Show media queries</span></span>  

<span data-ttu-id="ea9cd-136">Si ha definido consultas multimedia en la página, vaya a las dimensiones de ventanilla donde esas consultas multimedia tengan efecto mostrando puntos de interrupción de consulta multimedia encima de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="ea9cd-137">Elija **Más opciones Mostrar**consultas  >  **multimedia**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas multimedia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="ea9cd-139">Mostrar consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="ea9cd-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="ea9cd-140">Elija un punto de interrupción para cambiar el ancho de la ventanilla para que se desencadene la consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Elegir un punto de interrupción para cambiar el ancho de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="ea9cd-142">Elegir un punto de interrupción para cambiar el ancho de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="ea9cd-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <a name="set-the-device-type"></a><span data-ttu-id="ea9cd-143">Establecer el tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="ea9cd-143">Set the device type</span></span>  

<span data-ttu-id="ea9cd-144">Usa la **lista Tipo de** dispositivo para simular un dispositivo móvil o dispositivo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="La lista Tipo de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="ea9cd-146">La **lista Tipo de** dispositivo</span><span class="sxs-lookup"><span data-stu-id="ea9cd-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="ea9cd-147">En la tabla siguiente se describen las diferencias entre las opciones de tipo de dispositivo disponibles.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="ea9cd-148">La columna Rendering method hace referencia a si Microsoft Edge representa la página como una ventanilla móvil o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="ea9cd-149">La columna de icono cursor hace referencia al tipo de cursor que se muestra al pasar el mouse en la página.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-149">The Cursor icon column refers to what type of cursor is displayed when you hover on the page.</span></span>  <span data-ttu-id="ea9cd-150">La columna Eventos desencadenados hace referencia a si la página desencadena `touch` o eventos al interactuar con la `click` página.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="ea9cd-151">Opción</span><span class="sxs-lookup"><span data-stu-id="ea9cd-151">Option</span></span> | <span data-ttu-id="ea9cd-152">Método rendering</span><span class="sxs-lookup"><span data-stu-id="ea9cd-152">Rendering method</span></span> | <span data-ttu-id="ea9cd-153">Icono de cursor</span><span class="sxs-lookup"><span data-stu-id="ea9cd-153">Cursor icon</span></span> | <span data-ttu-id="ea9cd-154">Eventos desencadenados</span><span class="sxs-lookup"><span data-stu-id="ea9cd-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="ea9cd-155">Móvil</span><span class="sxs-lookup"><span data-stu-id="ea9cd-155">Mobile</span></span> | <span data-ttu-id="ea9cd-156">Móvil</span><span class="sxs-lookup"><span data-stu-id="ea9cd-156">Mobile</span></span> | <span data-ttu-id="ea9cd-157">Círculo</span><span class="sxs-lookup"><span data-stu-id="ea9cd-157">Circle</span></span> | <span data-ttu-id="ea9cd-158">Función táctil</span><span class="sxs-lookup"><span data-stu-id="ea9cd-158">touch</span></span> |  
| <span data-ttu-id="ea9cd-159">Mobile \(no touch\)</span><span class="sxs-lookup"><span data-stu-id="ea9cd-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="ea9cd-160">Móvil</span><span class="sxs-lookup"><span data-stu-id="ea9cd-160">Mobile</span></span> | <span data-ttu-id="ea9cd-161">Normal</span><span class="sxs-lookup"><span data-stu-id="ea9cd-161">Normal</span></span> | <span data-ttu-id="ea9cd-162"> elige </span><span class="sxs-lookup"><span data-stu-id="ea9cd-162">choose</span></span> |  
| <span data-ttu-id="ea9cd-163">Escritorio</span><span class="sxs-lookup"><span data-stu-id="ea9cd-163">Desktop</span></span> | <span data-ttu-id="ea9cd-164">Escritorio</span><span class="sxs-lookup"><span data-stu-id="ea9cd-164">Desktop</span></span> | <span data-ttu-id="ea9cd-165">Normal</span><span class="sxs-lookup"><span data-stu-id="ea9cd-165">Normal</span></span> | <span data-ttu-id="ea9cd-166"> elige </span><span class="sxs-lookup"><span data-stu-id="ea9cd-166">choose</span></span> |  
| <span data-ttu-id="ea9cd-167">Escritorio \(touch\)</span><span class="sxs-lookup"><span data-stu-id="ea9cd-167">Desktop \(touch\)</span></span> | <span data-ttu-id="ea9cd-168">Escritorio</span><span class="sxs-lookup"><span data-stu-id="ea9cd-168">Desktop</span></span> | <span data-ttu-id="ea9cd-169">Círculo</span><span class="sxs-lookup"><span data-stu-id="ea9cd-169">Circle</span></span> | <span data-ttu-id="ea9cd-170">Función táctil</span><span class="sxs-lookup"><span data-stu-id="ea9cd-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="ea9cd-171">Si no **se muestra la** lista Tipo de dispositivo, elija Más **opciones**Agregar tipo  >  **de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <a name="mobile-device-viewport-mode"></a><span data-ttu-id="ea9cd-172">Modo de ventanilla de dispositivo móvil</span><span class="sxs-lookup"><span data-stu-id="ea9cd-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="ea9cd-173">Para simular las dimensiones de un dispositivo móvil específico, selecciona el dispositivo en la **lista** Dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="ea9cd-175">Lista **de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-175">The **Device** list</span></span>  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a><span data-ttu-id="ea9cd-176">Girar la ventanilla a orientación horizontal</span><span class="sxs-lookup"><span data-stu-id="ea9cd-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="ea9cd-177">Pruebe la página web en orientación horizontal.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="ea9cd-178">Para girar la ventanilla a orientación horizontal, **elija Girar** \( ![ Girar ](../media/rotate-dark-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="ea9cd-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Página mostrada en orientación horizontal" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="ea9cd-180">Página mostrada en orientación horizontal</span><span class="sxs-lookup"><span data-stu-id="ea9cd-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="ea9cd-181">El **botón** Girar desaparece si la barra **de herramientas del** dispositivo es estrecha.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="ea9cd-183">La **barra de herramientas del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="ea9cd-184">Para obtener más información, vaya a [Establecer orientación](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="ea9cd-184">For more information, navigate to [Set orientation](#set-orientation).</span></span>  

#### <a name="show-device-frame"></a><span data-ttu-id="ea9cd-185">Mostrar fotograma del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ea9cd-185">Show device frame</span></span>  

<span data-ttu-id="ea9cd-186">Muestra el marco del dispositivo físico alrededor de la ventanilla cuando simulas las dimensiones de un dispositivo móvil específico, como un iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="ea9cd-187">Abra **Más opciones**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="ea9cd-188">Elija **Mostrar marco de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="ea9cd-189">Si no se muestra un marco de dispositivo para un dispositivo determinado, significa que DevTools no tiene arte para la opción.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-189">If a device frame for a particular device is not displayed, it means that DevTools does not have art for the option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar fotograma del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="ea9cd-191">Mostrar fotograma del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ea9cd-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Marco del dispositivo para el iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="ea9cd-193">Marco del dispositivo para el iPhone 6</span><span class="sxs-lookup"><span data-stu-id="ea9cd-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a><span data-ttu-id="ea9cd-194">Agregar un dispositivo móvil personalizado</span><span class="sxs-lookup"><span data-stu-id="ea9cd-194">Add a custom mobile device</span></span>  

<span data-ttu-id="ea9cd-195">Si la opción de dispositivo móvil que necesitas no está incluida en la lista predeterminada, puedes agregar un dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="ea9cd-196">Para agregar un dispositivo personalizado, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="ea9cd-197">Elija la **lista** Dispositivo > **Editar**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Elegir editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="ea9cd-199">Elegir **editar**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-199">Choose **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ea9cd-200">Elija **Agregar dispositivo personalizado**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="ea9cd-201">En **Dispositivos emulados,** escriba un nombre de dispositivo, ancho de pantalla y alto de pantalla para el dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="ea9cd-202">La [relación de píxeles del dispositivo,][MDNWindowDevicePixelRatio] [la cadena de agente de usuario][MDNUserAgent]y los campos de [tipo de](#set-the-device-type) dispositivo son opcionales.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="ea9cd-203">El campo de tipo de dispositivo tiene el valor **predeterminado Mobile**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Crear un dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="ea9cd-205">Crear un dispositivo personalizado</span><span class="sxs-lookup"><span data-stu-id="ea9cd-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <a name="show-rulers"></a><span data-ttu-id="ea9cd-206">Mostrar reglas</span><span class="sxs-lookup"><span data-stu-id="ea9cd-206">Show rulers</span></span>  

<span data-ttu-id="ea9cd-207">Si necesita medir las dimensiones de pantalla, puede usar reglas para medir el tamaño de pantalla en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="ea9cd-208">Elija **Más opciones**Mostrar reglas para mostrar las reglas arriba y a la izquierda de la  >  \*\*\*\* ventanilla.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Elemento de menú para mostrar reglas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="ea9cd-210">Elemento de menú para mostrar reglas</span><span class="sxs-lookup"><span data-stu-id="ea9cd-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Reglas arriba y a la izquierda de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="ea9cd-212">Reglas arriba y a la izquierda de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="ea9cd-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a><span data-ttu-id="ea9cd-213">Acercar la ventanilla</span><span class="sxs-lookup"><span data-stu-id="ea9cd-213">Zoom the viewport</span></span>  

<span data-ttu-id="ea9cd-214">Para probar la apariencia de la página en varios niveles de zoom, usa la **lista Zoom** para acercar o alejar.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="ea9cd-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="ea9cd-216">Zoom</span></span>**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a><span data-ttu-id="ea9cd-217">Limitar la red y la CPU</span><span class="sxs-lookup"><span data-stu-id="ea9cd-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="ea9cd-218">Los dispositivos móviles suelen tener restricciones de red y CPU.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="ea9cd-219">Asegúrate de probar la rapidez con la que se carga la página y cómo responde a diferentes velocidades de Internet y CPU.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="ea9cd-220">Limita la red y la CPU.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="ea9cd-221">Elija **Lista de** limitaciones y cambie el valor preestablecido a Móvil de **nivel** intermedio o Móvil de **gama baja.**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="ea9cd-222">**El móvil de nivel intermedio** simula y limita la `fast 3G` CPU.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="ea9cd-223">Es cuatro veces más lento de lo normal.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="ea9cd-224">**El móvil de gama baja** simula y limita la `slow 3G` CPU.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="ea9cd-225">Es seis veces más lento de lo normal.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="ea9cd-226">Toda la limitación se basa en la funcionalidad normal de su portátil o escritorio.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="La lista De limitación de la barra de herramientas de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="ea9cd-228">La **lista De limitación** de la barra de herramientas de dispositivos</span><span class="sxs-lookup"><span data-stu-id="ea9cd-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="ea9cd-229">Si la **lista de limitaciones** está oculta, la **barra de herramientas del** dispositivo es demasiado estrecha.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="ea9cd-230">Para obtener acceso a **la lista de limitaciones,** aumente el ancho de la barra de herramientas **del dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="ea9cd-232">La **barra de herramientas del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a><span data-ttu-id="ea9cd-233">Limitar solo la CPU</span><span class="sxs-lookup"><span data-stu-id="ea9cd-233">Throttle the CPU only</span></span>  

<span data-ttu-id="ea9cd-234">Para limitar la CPU solo y no la red, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="ea9cd-235">Elija el panel **Rendimiento** y elija **Configuración de captura** \( Configuración de captura ![ ](../media/capture-settings-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="ea9cd-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\).</span></span>
1.  <span data-ttu-id="ea9cd-236">Elija **CPU**  >  **4x slowdown** o **6x slowdown**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="La lista de CPU del panel Rendimiento" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="ea9cd-238">La **lista de CPU** del panel **Rendimiento**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a><span data-ttu-id="ea9cd-239">Limitar solo la red</span><span class="sxs-lookup"><span data-stu-id="ea9cd-239">Throttle the network only</span></span>  

<span data-ttu-id="ea9cd-240">Para limitar solo la red, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="ea9cd-241">Elija la **herramienta Red.**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-241">Choose the **Network** tool.</span></span>
1.  <span data-ttu-id="ea9cd-242">Elija **Online**  >  **Fast 3G** o Slow **3G**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Lista de limitaciones en el panel Red" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="ea9cd-244">Lista **de limitaciones** en el panel Red</span><span class="sxs-lookup"><span data-stu-id="ea9cd-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="ea9cd-245">O seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) \*\*\*\* `3G` \*\*\*\* \*\*\*\* para abrir el menú comando , escriba y elija Habilitar la limitación rápida de 3G o Habilitar la limitación 3G lenta .</span><span class="sxs-lookup"><span data-stu-id="ea9cd-245">Or select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Menú comando" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="ea9cd-247">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="ea9cd-248">También puede establecer la limitación de red desde **el** panel Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="ea9cd-249">Elija **Configuración de** captura \( Configuración de captura \) y elija la lista Red y cambie el valor preestablecido ![ a Fast ](../media/capture-settings-icon.msft.png) **3G** o **Slow 3G**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ea9cd-249">Choose **Capture Settings** \(![Capture Settings](../media/capture-settings-icon.msft.png)\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Establecer limitación de red desde el panel Rendimiento" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="ea9cd-251">Establecer limitación de red desde **el** panel Rendimiento</span><span class="sxs-lookup"><span data-stu-id="ea9cd-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <a name="override-geolocation"></a><span data-ttu-id="ea9cd-252">Reemplazar geolocalización</span><span class="sxs-lookup"><span data-stu-id="ea9cd-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ea9cd-253">Si la página depende de la información de geolocalización de un dispositivo móvil para representarse correctamente, proporcione distintas geolocalizaciones mediante la interfaz de usuario de reemplazo de geolocalización.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="ea9cd-254">Elija **Personalizar y controlar DevTools** \( `...` \) > Más herramientas \*\*\*\*  >  **Sensores**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores de geolocalización" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="ea9cd-256">**Sensores** de geolocalización</span><span class="sxs-lookup"><span data-stu-id="ea9cd-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="ea9cd-257">Abra el menú comando.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="ea9cd-258">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ea9cd-258">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="ea9cd-259">Escriba `Sensors` y elija Mostrar **sensores**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores para geolocalización" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="ea9cd-261">**Mostrar sensores** para geolocalización</span><span class="sxs-lookup"><span data-stu-id="ea9cd-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="ea9cd-262">En **el** panel Sensores, puede seleccionar una de las \*\*\*\* ubicaciones preestablecidas incluidas en DevTools mediante el menú desplegable Ubicación.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="ea9cd-263">Para especificar una ubicación personalizada, elija **Otros...**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="ea9cd-264">e introduzca las coordenadas de la ubicación personalizada.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="ea9cd-265">Para probar la página en un estado de error cuando la información de ubicación no está disponible, elija **Ubicación no disponible.**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Panel de sensores con una ubicación preestablecida seleccionada" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="ea9cd-267">**Panel** de sensores con una ubicación preestablecida seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <a name="set-orientation"></a><span data-ttu-id="ea9cd-268">Establecer orientación</span><span class="sxs-lookup"><span data-stu-id="ea9cd-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ea9cd-269">Si la página depende de la información de orientación de un dispositivo móvil para que se represente correctamente, abra la interfaz de usuario de orientación.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="ea9cd-270">Elija **Personalizar y controlar DevTools** \( `...` \) > Más herramientas \*\*\*\*  >  **Sensores**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores de orientación" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="ea9cd-272">**Sensores** de orientación</span><span class="sxs-lookup"><span data-stu-id="ea9cd-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="ea9cd-273">Abra el menú comando.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="ea9cd-274">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ea9cd-274">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="ea9cd-275">Escriba `Sensors` y elija Mostrar **sensores**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores para orientación" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="ea9cd-277">**Mostrar sensores** para orientación</span><span class="sxs-lookup"><span data-stu-id="ea9cd-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="ea9cd-278">En **el** panel Sensores, puede seleccionar una orientación preestablecida en **el** menú desplegable Orientación.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="ea9cd-279">Para escribir su propia orientación, elija **Orientación personalizada**e introduzca sus propios [valores alfa,][MDNDeviceOrientaitonAlpha] [beta][MDNDeviceOrientaitonBeta]y [gamma.][MDNDeviceOrientaitonGamma]</span><span class="sxs-lookup"><span data-stu-id="ea9cd-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Opciones de orientación en el panel Sensores" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="ea9cd-281">**Opciones de** orientación en el panel **Sensores**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <a name="set-user-agent-string"></a><span data-ttu-id="ea9cd-282">Establecer cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="ea9cd-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="ea9cd-283">Si la página depende de la cadena de agente de usuario de un dispositivo móvil para representarse correctamente, use el panel **Condiciones** de red para proporcionar distintas cadenas de agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="ea9cd-284">Elija **Personalizar y controlar DevTools** \( `...` \) > Más herramientas **Condiciones**  >  **de red**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrada condiciones de red en el menú Más herramientas" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="ea9cd-286">**Entrada condiciones de** red en el **menú Más** herramientas</span><span class="sxs-lookup"><span data-stu-id="ea9cd-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="ea9cd-287">Abra el menú comando.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="ea9cd-288">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="ea9cd-288">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="ea9cd-289">Escriba `Network conditions` y elija Mostrar condiciones de **red**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Mostrar condiciones de red" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="ea9cd-291">Mostrar condiciones de red</span><span class="sxs-lookup"><span data-stu-id="ea9cd-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="ea9cd-292">Junto al **agente de usuario,** desactive la **casilla Seleccionar automáticamente.**</span><span class="sxs-lookup"><span data-stu-id="ea9cd-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="ea9cd-293">A continuación, **elija Personalizado...** para seleccionar de una lista de cadenas de agente de usuario predefinidas.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-293">Then, choose **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="ea9cd-294">Para escribir su propia cadena de agente de usuario, escriba la cadena **en Entrar en un agente de usuario personalizado**.</span><span class="sxs-lookup"><span data-stu-id="ea9cd-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Establecer la cadena de agente de usuario en Microsoft Edge en macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="ea9cd-296">Establecer la cadena de agente de usuario en Microsoft Edge en macOS</span><span class="sxs-lookup"><span data-stu-id="ea9cd-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ea9cd-297">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ea9cd-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Orden de aproximación - Primer orden - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="ea9cd-305">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ea9cd-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ea9cd-306">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="ea9cd-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ea9cd-308">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ea9cd-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
