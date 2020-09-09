---
description: Use dispositivos virtuales en Microsoft Edge para crear sitios web móviles.
title: Emular dispositivos móviles en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, emulación, dispositivo, simulación, móvil
ms.openlocfilehash: c70b81eabb145461eac7d1b9a8f438d6a18fbc89
ms.sourcegitcommit: cc96ada9679b23feb841e46f19d8077251c4a4df
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "10997173"
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

# <span data-ttu-id="3c392-104">Emular dispositivos móviles en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3c392-104">Emulate mobile devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="3c392-105">Use la **emulación de dispositivos** para aproximar el aspecto y la respuesta de la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="3c392-105">Use **Device emulation** to approximate how your page looks and responds on a mobile device.</span></span>  <span data-ttu-id="3c392-106">El DevTools de Microsoft Edge proporciona una colección de características que te ayudan a emular dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="3c392-106">The Microsoft Edge DevTools provide a collection of features to help you emulate mobile devices.</span></span>  <span data-ttu-id="3c392-107">La colección incluye las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="3c392-107">The collection includes the following features.</span></span>  

*   [<span data-ttu-id="3c392-108">Simular un área de visualización móvil</span><span class="sxs-lookup"><span data-stu-id="3c392-108">Simulate a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="3c392-109">Limitar la red</span><span class="sxs-lookup"><span data-stu-id="3c392-109">Throttle the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="3c392-110">Limitar la CPU</span><span class="sxs-lookup"><span data-stu-id="3c392-110">Throttle the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="3c392-111">Simular geolocalización</span><span class="sxs-lookup"><span data-stu-id="3c392-111">Simulate geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="3c392-112">Establecer orientación</span><span class="sxs-lookup"><span data-stu-id="3c392-112">Set orientation</span></span>](#set-orientation)  
*   [<span data-ttu-id="3c392-113">Establecer la cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="3c392-113">Set the user agent string</span></span>](#set-user-agent-string)  

## <span data-ttu-id="3c392-114">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="3c392-114">Limitations</span></span>  

<span data-ttu-id="3c392-115">La **emulación de dispositivos** es una [aproximación de primer orden][WikiApproximation] de la apariencia de la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="3c392-115">**Device emulation** is a [first-order approximation][WikiApproximation] of the look and feel of your page on a mobile device.</span></span>  <span data-ttu-id="3c392-116">La **emulación de dispositivos** realmente no ejecuta el código en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="3c392-116">**Device emulation** does not actually run your code on a mobile device.</span></span>  <span data-ttu-id="3c392-117">En su lugar, simula la experiencia de usuario móvil desde su equipo portátil o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="3c392-117">Instead you simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="3c392-118">Algunos aspectos de los dispositivos móviles nunca se emulan en DevTools.</span><span class="sxs-lookup"><span data-stu-id="3c392-118">Some aspects of mobile devices are never emulated in DevTools.</span></span>  <span data-ttu-id="3c392-119">Por ejemplo, la arquitectura de las CPU móviles es diferente de la arquitectura de las CPU de equipos portátiles o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="3c392-119">For example, the architecture of mobile CPUs is different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="3c392-120">Cuando tenga dudas, la mejor opción es ejecutar la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="3c392-120">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="3c392-121">Use [depuración remota] [DevToolsRemoteDebugging] para interactuar con el código de una página de su equipo mientras la página se ejecuta en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="3c392-121">Use [Remote Debugging][DevToolsRemoteDebugging] to interact with the code of a page from your machine while your page actually runs on a mobile device.</span></span>  <span data-ttu-id="3c392-122">Puede ver, cambiar, depurar, perfil o los cuatro mientras interactúa con el código.</span><span class="sxs-lookup"><span data-stu-id="3c392-122">You may view, change, debug, profile, or all four while you interact with the code.</span></span>  <span data-ttu-id="3c392-123">Su equipo puede ser un portátil o un equipo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="3c392-123">Your machine may be a notebook or desktop computer.</span></span>  

## <span data-ttu-id="3c392-124">Simular un área de visualización móvil</span><span class="sxs-lookup"><span data-stu-id="3c392-124">Simulate a mobile viewport</span></span>  

<span data-ttu-id="3c392-125">Elija **alternar emulación de dispositivo**  \ ( ![ Alternar barra de herramientas de dispositivo ][ImageDeviceToolbarIcon] \) o elegir **personalizar y controlar DevTools** \ ( `...` \) > **emulación de dispositivo** para abrir la interfaz de usuario que le permite simular un área de visualización móvil.</span><span class="sxs-lookup"><span data-stu-id="3c392-125">Choose **Toggle device emulation**  \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) or choose **Customize and control DevTools** \(`...`\) > **Device emulation** to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    <span data-ttu-id="3c392-127">La barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c392-127">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="3c392-128">De forma predeterminada, la barra de herramientas del dispositivo se abre en modo de ventanilla eficaz.</span><span class="sxs-lookup"><span data-stu-id="3c392-128">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="3c392-129">Modo de ventanilla receptiva</span><span class="sxs-lookup"><span data-stu-id="3c392-129">Responsive Viewport Mode</span></span>  

<span data-ttu-id="3c392-130">Para probar rápidamente la apariencia de la página en varios tamaños de pantalla, arrastre los controladores para cambiar el tamaño de la ventanilla a las dimensiones necesarias.</span><span class="sxs-lookup"><span data-stu-id="3c392-130">To quickly test the look and feel of your page across multiple screen sizes, drag the handles to resize the viewport to your required dimensions.</span></span>  <span data-ttu-id="3c392-131">También puede especificar valores específicos en los cuadros ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="3c392-131">You may also enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="3c392-132">En la siguiente ilustración, el ancho se establece en `626` y el alto se establece en `516` .</span><span class="sxs-lookup"><span data-stu-id="3c392-132">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    <span data-ttu-id="3c392-134">Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica</span><span class="sxs-lookup"><span data-stu-id="3c392-134">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="3c392-135">Mostrar consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="3c392-135">Show media queries</span></span>  

<span data-ttu-id="3c392-136">Si ha definido consultas multimedia en la página, vaya a las dimensiones de la ventanilla donde las consultas de medios surten efecto mostrando puntos de interrupción de consulta multimedia encima de su ventanilla.</span><span class="sxs-lookup"><span data-stu-id="3c392-136">If you have defined media queries on your page, jump to the viewport dimensions where those media queries take effect by showing media query breakpoints above your viewport.</span></span>  <span data-ttu-id="3c392-137">Elija **más opciones**para  >  **Mostrar las consultas de medios**.</span><span class="sxs-lookup"><span data-stu-id="3c392-137">Choose **More options** > **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas multimedia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="3c392-139">Mostrar consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="3c392-139">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="3c392-140">Elija un punto de interrupción para cambiar el ancho de la ventanilla de modo que se desencadene la consulta multimedia.</span><span class="sxs-lookup"><span data-stu-id="3c392-140">Choose a breakpoint to change the width of the viewport so that the media query gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Elegir un punto de interrupción para cambiar el ancho de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="3c392-142">Elegir un punto de interrupción para cambiar el ancho de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="3c392-142">Choose a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="3c392-143">Establecer el tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c392-143">Set the device type</span></span>  

<span data-ttu-id="3c392-144">Use la lista **tipo de dispositivo** para simular un dispositivo móvil o un dispositivo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="3c392-144">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Lista tipo de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="3c392-146">Lista **tipo de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="3c392-146">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="3c392-147">En la siguiente tabla se describen las diferencias entre las opciones de tipo de dispositivo disponibles.</span><span class="sxs-lookup"><span data-stu-id="3c392-147">The following table describes the differences between the available device type options.</span></span>  <span data-ttu-id="3c392-148">La columna método de representación hace referencia a si Microsoft Edge representa la página como un área de visualización de escritorio o móvil.</span><span class="sxs-lookup"><span data-stu-id="3c392-148">The Rendering method column refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="3c392-149">La columna icono del cursor hace referencia al tipo de cursor que se ve al pasar el puntero por la página.</span><span class="sxs-lookup"><span data-stu-id="3c392-149">The Cursor icon column refers to what type of cursor you see when you hover on the page.</span></span>  <span data-ttu-id="3c392-150">La columna eventos desencadenados hace referencia a si la página `touch` se desencadena o `click` se desencadena cuando se interactúa con la página.</span><span class="sxs-lookup"><span data-stu-id="3c392-150">The Events triggered column refers to whether the page triggers `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="3c392-151">Opción</span><span class="sxs-lookup"><span data-stu-id="3c392-151">Option</span></span> | <span data-ttu-id="3c392-152">Método de representación</span><span class="sxs-lookup"><span data-stu-id="3c392-152">Rendering method</span></span> | <span data-ttu-id="3c392-153">Icono cursor</span><span class="sxs-lookup"><span data-stu-id="3c392-153">Cursor icon</span></span> | <span data-ttu-id="3c392-154">Eventos desencadenados</span><span class="sxs-lookup"><span data-stu-id="3c392-154">Events triggered</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="3c392-155">Móvil</span><span class="sxs-lookup"><span data-stu-id="3c392-155">Mobile</span></span> | <span data-ttu-id="3c392-156">Móvil</span><span class="sxs-lookup"><span data-stu-id="3c392-156">Mobile</span></span> | <span data-ttu-id="3c392-157">Círculo</span><span class="sxs-lookup"><span data-stu-id="3c392-157">Circle</span></span> | <span data-ttu-id="3c392-158">Función táctil</span><span class="sxs-lookup"><span data-stu-id="3c392-158">touch</span></span> |  
| <span data-ttu-id="3c392-159">Móvil \ (sin contacto \)</span><span class="sxs-lookup"><span data-stu-id="3c392-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="3c392-160">Móvil</span><span class="sxs-lookup"><span data-stu-id="3c392-160">Mobile</span></span> | <span data-ttu-id="3c392-161">Normal</span><span class="sxs-lookup"><span data-stu-id="3c392-161">Normal</span></span> | <span data-ttu-id="3c392-162"> haz clic en </span><span class="sxs-lookup"><span data-stu-id="3c392-162">click</span></span> |  
| <span data-ttu-id="3c392-163">Escritorio</span><span class="sxs-lookup"><span data-stu-id="3c392-163">Desktop</span></span> | <span data-ttu-id="3c392-164">Escritorio</span><span class="sxs-lookup"><span data-stu-id="3c392-164">Desktop</span></span> | <span data-ttu-id="3c392-165">Normal</span><span class="sxs-lookup"><span data-stu-id="3c392-165">Normal</span></span> | <span data-ttu-id="3c392-166"> haz clic en </span><span class="sxs-lookup"><span data-stu-id="3c392-166">click</span></span> |  
| <span data-ttu-id="3c392-167">Escritorio \ (Touch \)</span><span class="sxs-lookup"><span data-stu-id="3c392-167">Desktop \(touch\)</span></span> | <span data-ttu-id="3c392-168">Escritorio</span><span class="sxs-lookup"><span data-stu-id="3c392-168">Desktop</span></span> | <span data-ttu-id="3c392-169">Círculo</span><span class="sxs-lookup"><span data-stu-id="3c392-169">Circle</span></span> | <span data-ttu-id="3c392-170">Función táctil</span><span class="sxs-lookup"><span data-stu-id="3c392-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="3c392-171">Si no se muestra la lista **tipo de dispositivo** , elija **más opciones**  >  **Agregar tipo de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="3c392-171">If the **Device Type** list is not displayed, choose **More options** > **Add device type**.</span></span>  

### <span data-ttu-id="3c392-172">Modo de ventanilla de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="3c392-172">Mobile Device Viewport Mode</span></span>  

<span data-ttu-id="3c392-173">Para simular las dimensiones de un dispositivo móvil específico, seleccione el dispositivo en la lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="3c392-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="La lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="3c392-175">La lista de **dispositivos**</span><span class="sxs-lookup"><span data-stu-id="3c392-175">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="3c392-176">Girar la ventanilla a la orientación horizontal</span><span class="sxs-lookup"><span data-stu-id="3c392-176">Rotate the viewport to landscape orientation</span></span>  

<span data-ttu-id="3c392-177">Pruebe la página web con orientación horizontal.</span><span class="sxs-lookup"><span data-stu-id="3c392-177">Test your webpage in landscape orientation.</span></span>  

*   <span data-ttu-id="3c392-178">Para girar la ventanilla a orientación horizontal, elija **girar** \ ( ![ girar ][ImageRotateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3c392-178">To rotate the viewport to landscape orientation, choose **Rotate** \(![Rotate][ImageRotateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Página mostrada en orientación horizontal" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       <span data-ttu-id="3c392-180">Página mostrada en orientación horizontal</span><span class="sxs-lookup"><span data-stu-id="3c392-180">Page displayed in landscape orientation</span></span>  
    :::image-end:::  
    
> [!NOTE]
> <span data-ttu-id="3c392-181">El botón **girar** desaparecerá si la **barra de herramientas del dispositivo** es estrecha.</span><span class="sxs-lookup"><span data-stu-id="3c392-181">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="3c392-183">La **barra de herramientas del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="3c392-183">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="3c392-184">Para obtener más información, vaya a [establecer orientación](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="3c392-184">For more information, go to [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="3c392-185">Mostrar marco del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c392-185">Show device frame</span></span>  

<span data-ttu-id="3c392-186">Mostrar el marco del dispositivo físico en el área de visualización al simular las dimensiones de un dispositivo móvil específico, como un iPhone 6.</span><span class="sxs-lookup"><span data-stu-id="3c392-186">Display the physical device frame around the viewport when you simulate the dimensions of a specific mobile device such as an iPhone 6.</span></span>  

1.  <span data-ttu-id="3c392-187">Abra **más opciones**.</span><span class="sxs-lookup"><span data-stu-id="3c392-187">Open **More options**.</span></span>  
1.  <span data-ttu-id="3c392-188">Elija **Mostrar marco del dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="3c392-188">Choose **Show device frame**.</span></span>  

> [!NOTE]
> <span data-ttu-id="3c392-189">Si no ve un marco de dispositivo para un dispositivo en particular, significa que DevTools no tiene arte para esa opción.</span><span class="sxs-lookup"><span data-stu-id="3c392-189">If you do not see a device frame for a particular device, it means that DevTools does not have art for that option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar marco del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="3c392-191">Mostrar marco del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c392-191">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="El marco del dispositivo para el iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="3c392-193">El marco del dispositivo para el iPhone 6</span><span class="sxs-lookup"><span data-stu-id="3c392-193">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="3c392-194">Agregar un dispositivo móvil personalizado</span><span class="sxs-lookup"><span data-stu-id="3c392-194">Add a custom mobile device</span></span>  

<span data-ttu-id="3c392-195">Si la opción de dispositivo móvil que necesita no está incluida en la lista predeterminada, puede Agregar un dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="3c392-195">If the mobile device option that you need is not included on the default list, you may add a custom device.</span></span>  <span data-ttu-id="3c392-196">Para agregar un dispositivo personalizado, siga los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="3c392-196">To add a custom device, complete the following steps.</span></span>  

1.  <span data-ttu-id="3c392-197">Elija la lista de **dispositivos** > **Editar**.</span><span class="sxs-lookup"><span data-stu-id="3c392-197">Choose the **Device** list > **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Seleccione Editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="3c392-199">Seleccione **Editar**</span><span class="sxs-lookup"><span data-stu-id="3c392-199">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="3c392-200">Elija **Agregar dispositivo personalizado**.</span><span class="sxs-lookup"><span data-stu-id="3c392-200">Choose **Add custom device**.</span></span>  
1.  <span data-ttu-id="3c392-201">En **dispositivos emulados**, escriba un nombre de dispositivo, un ancho de pantalla y un alto de pantalla para el dispositivo personalizado.</span><span class="sxs-lookup"><span data-stu-id="3c392-201">On **Emulated Devices**, enter a device name, screen width, and screen height for the custom device.</span></span>  <span data-ttu-id="3c392-202">La [relación de píxeles del dispositivo][MDNWindowDevicePixelRatio], la [cadena de agente de usuario][MDNUserAgent]y los campos de tipo de [dispositivo](#set-the-device-type) son opcionales.</span><span class="sxs-lookup"><span data-stu-id="3c392-202">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="3c392-203">El valor predeterminado del campo tipo de dispositivo es **móvil**.</span><span class="sxs-lookup"><span data-stu-id="3c392-203">The device type field defaults to **Mobile**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Crear un dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="3c392-205">Crear un dispositivo personalizado</span><span class="sxs-lookup"><span data-stu-id="3c392-205">Create a custom device</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3c392-206">Mostrar reglas</span><span class="sxs-lookup"><span data-stu-id="3c392-206">Show rulers</span></span>  

<span data-ttu-id="3c392-207">Si necesita medir las dimensiones de la pantalla, puede usar las reglas para medir el tamaño de la pantalla en píxeles.</span><span class="sxs-lookup"><span data-stu-id="3c392-207">If you need to measure screen dimensions, you may use rulers to measure the screen size in pixels.</span></span>  <span data-ttu-id="3c392-208">Elija **más opciones**  >  para**Mostrar** las reglas para mostrar las reglas por encima y a la izquierda de su ventanilla.</span><span class="sxs-lookup"><span data-stu-id="3c392-208">Choose **More options** > **Show rulers** to display rulers above and to the left of your viewport.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Elemento de menú para mostrar las reglas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         <span data-ttu-id="3c392-210">Elemento de menú para mostrar las reglas</span><span class="sxs-lookup"><span data-stu-id="3c392-210">Menu item to display rulers</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Reglas por encima y a la izquierda de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="3c392-212">Reglas por encima y a la izquierda de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="3c392-212">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="3c392-213">Acercar la ventanilla</span><span class="sxs-lookup"><span data-stu-id="3c392-213">Zoom the viewport</span></span>  

<span data-ttu-id="3c392-214">Para probar la apariencia de la página en varios niveles de zoom, use la lista de **zoom** para acercar o alejar.</span><span class="sxs-lookup"><span data-stu-id="3c392-214">To test the look and feel of your page at multiple zoom levels, use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="3c392-216">Zoom</span><span class="sxs-lookup"><span data-stu-id="3c392-216">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="3c392-217">Limitar la red y la CPU</span><span class="sxs-lookup"><span data-stu-id="3c392-217">Throttle the network and CPU</span></span>  

<span data-ttu-id="3c392-218">Los dispositivos móviles suelen tener restricciones de red y de CPU.</span><span class="sxs-lookup"><span data-stu-id="3c392-218">Mobile devices often have network and CPU constraints.</span></span>  <span data-ttu-id="3c392-219">Asegúrese de probar la rapidez con la que se carga la página y cómo responde a diferentes velocidades de Internet y de CPU.</span><span class="sxs-lookup"><span data-stu-id="3c392-219">Ensure you test how quickly your page loads and how it responds at different internet and CPU speeds.</span></span>  

<span data-ttu-id="3c392-220">Limite la red y la CPU.</span><span class="sxs-lookup"><span data-stu-id="3c392-220">Throttle the network and CPU.</span></span>  

1.  <span data-ttu-id="3c392-221">Elige la lista de **aceleración** y cambia el ajuste preestablecido a móvil **de nivel intermedio** o **móvil de low-end**.</span><span class="sxs-lookup"><span data-stu-id="3c392-221">Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.</span></span>  
    *   <span data-ttu-id="3c392-222">El **teléfono móvil de nivel intermedio** simula `fast 3G` y acelera su CPU.</span><span class="sxs-lookup"><span data-stu-id="3c392-222">**Mid-tier mobile** simulates `fast 3G` and throttles your CPU.</span></span>  <span data-ttu-id="3c392-223">Es cuatro veces más lentas de lo normal.</span><span class="sxs-lookup"><span data-stu-id="3c392-223">It is four times slower than normal.</span></span>  
    *   <span data-ttu-id="3c392-224">La **tecnología móvil de gama baja** simula `slow 3G` y acelera su CPU.</span><span class="sxs-lookup"><span data-stu-id="3c392-224">**Low-end mobile** simulates `slow 3G` and throttles your CPU.</span></span>  <span data-ttu-id="3c392-225">Es seis veces más lento de lo normal.</span><span class="sxs-lookup"><span data-stu-id="3c392-225">It is six times slower than normal.</span></span>  
    
<span data-ttu-id="3c392-226">Todo el límite se basa en la capacidad normal de su equipo portátil o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="3c392-226">All of the throttling is based upon the normal capability of your laptop or desktop.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Lista de aceleradores de la barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="3c392-228">Lista de **aceleradores** de la barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c392-228">The **Throttle** list in the Device Toolbar</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="3c392-229">Si la **lista acelerador** está oculta, la **barra de herramientas del dispositivo** es demasiado estrecha.</span><span class="sxs-lookup"><span data-stu-id="3c392-229">If the **Throttle list** is hidden, your **Device Toolbar** is too narrow.</span></span>  <span data-ttu-id="3c392-230">Para obtener acceso a la **lista aceleradora**, aumente el ancho de la **barra de herramientas del dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="3c392-230">To access the **Throttle list**, increase the width of the **Device Toolbar**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="3c392-232">La **barra de herramientas del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="3c392-232">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="3c392-233">Limitar solo la CPU</span><span class="sxs-lookup"><span data-stu-id="3c392-233">Throttle the CPU only</span></span>  

<span data-ttu-id="3c392-234">Para limitar solo la CPU y no la red, complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="3c392-234">To throttle the CPU only and not the network, complete the following steps.</span></span>

1.  <span data-ttu-id="3c392-235">Elija el panel **rendimiento** y elija **configuración de captura** \ ( ![ configuración de captura ][ImageCaptureIcon] \).</span><span class="sxs-lookup"><span data-stu-id="3c392-235">Choose the **Performance** panel, and choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\).</span></span>
1.  <span data-ttu-id="3c392-236">Elija **CPU**  >  **4x lentitud** o **ralentización 6**.</span><span class="sxs-lookup"><span data-stu-id="3c392-236">Choose **CPU** > **4x slowdown** or **6x slowdown**.</span></span>
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Lista de CPU en el panel rendimiento" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       <span data-ttu-id="3c392-238">Lista de **CPU** en el panel **rendimiento**</span><span class="sxs-lookup"><span data-stu-id="3c392-238">The **CPU** list in the **Performance** panel</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="3c392-239">Limitar la velocidad de la red</span><span class="sxs-lookup"><span data-stu-id="3c392-239">Throttle the network only</span></span>  

<span data-ttu-id="3c392-240">Para limitar solo la red, siga los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="3c392-240">To throttle the network only, complete the following steps.</span></span>

1.  <span data-ttu-id="3c392-241">Elija el panel **red** .</span><span class="sxs-lookup"><span data-stu-id="3c392-241">Choose the **Network** panel.</span></span>
1.  <span data-ttu-id="3c392-242">Elige 3G rápido **en línea**  >  **Fast 3G** o **3G lento**.</span><span class="sxs-lookup"><span data-stu-id="3c392-242">Choose **Online** > **Fast 3G** or **Slow 3G**.</span></span>
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="La lista de aceleradores en el panel red" lightbox="../media/device-mode-network-throttle.msft.png":::
       <span data-ttu-id="3c392-244">La lista de **aceleradores** en el panel red</span><span class="sxs-lookup"><span data-stu-id="3c392-244">The **Throttle** list in the Network panel</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="3c392-245">O seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**, escriba `3G` y elija **Habilitar la limitación rápida de 3G** o habilitar la limitación de **3G**.</span><span class="sxs-lookup"><span data-stu-id="3c392-245">Or select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and choose **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="El menú de comandos" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       <span data-ttu-id="3c392-247">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="3c392-247">The **Command Menu**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="3c392-248">También puede establecer el límite de red en el panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="3c392-248">You may also set network throttling from the **Performance** panel.</span></span>  

1.  <span data-ttu-id="3c392-249">Elija **configuración de captura** \ ( ![ configuración de captura ][ImageCaptureIcon] \) y seleccione la lista de **redes** y cambie el ajuste preestablecido a **3G rápido** o **3G lento**.</span><span class="sxs-lookup"><span data-stu-id="3c392-249">Choose **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and choose the **Network** list and change the preset to **Fast 3G** or **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Configurar el límite de red en el panel rendimiento" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       <span data-ttu-id="3c392-251">Configurar el límite de red en el panel **rendimiento**</span><span class="sxs-lookup"><span data-stu-id="3c392-251">Set network throttling from the **Performance** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="3c392-252">Invalidar geolocalización</span><span class="sxs-lookup"><span data-stu-id="3c392-252">Override geolocation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3c392-253">Si su página depende de la información de geolocalización de un dispositivo móvil para representarse correctamente, proporcione geolocalización diferentes mediante la interfaz de usuario de reemplazo de geolocal.</span><span class="sxs-lookup"><span data-stu-id="3c392-253">If your page depends on geolocation information from a mobile device to render properly, provide different geolocations using the geolocation overriding UI.</span></span>  

      1.  <span data-ttu-id="3c392-254">Elija **personalizar y controlar DevTools** \ ( `...` \) > **más**  >  **sensores**de herramientas.</span><span class="sxs-lookup"><span data-stu-id="3c392-254">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores de geolocalización" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="3c392-256">**Sensores** de geolocalización</span><span class="sxs-lookup"><span data-stu-id="3c392-256">**Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="3c392-257">Abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="3c392-257">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="3c392-258">Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="3c392-258">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="3c392-259">Escriba `Sensors` y elija **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="3c392-259">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores de geolocalización" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="3c392-261">**Mostrar sensores** de geolocalización</span><span class="sxs-lookup"><span data-stu-id="3c392-261">**Show Sensors** for geolocation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="3c392-262">En el panel **sensores** , puede seleccionar una de las ubicaciones preestablecidas incluidas en DevTools con el menú desplegable **Ubicación** .</span><span class="sxs-lookup"><span data-stu-id="3c392-262">On the **Sensors** panel, you may select one of the preset locations included in DevTools using the **Location** drop-down menu.</span></span>  <span data-ttu-id="3c392-263">Para escribir una ubicación personalizada, elija **otro...**</span><span class="sxs-lookup"><span data-stu-id="3c392-263">To enter a custom location, choose **Other…**</span></span> <span data-ttu-id="3c392-264">e introduzca las coordenadas de la ubicación personalizada.</span><span class="sxs-lookup"><span data-stu-id="3c392-264">and enter the coordinates of your custom location.</span></span>  <span data-ttu-id="3c392-265">Para probar la página en estado de error cuando la información de ubicación no está disponible, elija **ubicación no disponible**.</span><span class="sxs-lookup"><span data-stu-id="3c392-265">To test your page in an error state when location information is unavailable, choose **Location unavailable**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Panel sensores con una ubicación preestablecida seleccionada" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    <span data-ttu-id="3c392-267">Panel **sensores** con una ubicación preestablecida seleccionada.</span><span class="sxs-lookup"><span data-stu-id="3c392-267">**Sensors** panel with a preset location selected.</span></span>  
:::image-end:::

## <span data-ttu-id="3c392-268">Establecer orientación</span><span class="sxs-lookup"><span data-stu-id="3c392-268">Set orientation</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3c392-269">Si tu página depende de la información de orientación de un dispositivo móvil para representarla correctamente, abre la interfaz de usuario de orientación.</span><span class="sxs-lookup"><span data-stu-id="3c392-269">If your page depends on orientation information from a mobile device to render properly, open the orientation UI.</span></span>  

      1.  <span data-ttu-id="3c392-270">Elija **personalizar y controlar DevTools** \ ( `...` \) > **más**  >  **sensores**de herramientas.</span><span class="sxs-lookup"><span data-stu-id="3c392-270">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores para orientación" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         <span data-ttu-id="3c392-272">**Sensores** para orientación</span><span class="sxs-lookup"><span data-stu-id="3c392-272">**Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="3c392-273">Abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="3c392-273">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="3c392-274">Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="3c392-274">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="3c392-275">Escriba `Sensors` y elija **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="3c392-275">Type `Sensors`, and choose **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores para la orientación" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         <span data-ttu-id="3c392-277">**Mostrar sensores** para la orientación</span><span class="sxs-lookup"><span data-stu-id="3c392-277">**Show Sensors** for orientation</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="3c392-278">En el panel **sensores** , puede seleccionar una orientación preestablecida en el menú desplegable **orientación** .</span><span class="sxs-lookup"><span data-stu-id="3c392-278">On the **Sensors** panel, you may select a preset orientation from the **Orientation** drop-down menu.</span></span>  <span data-ttu-id="3c392-279">Para escribir su propia orientación, elija **orientación personalizada**y escriba sus propios valores de [alfa][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta]y [gamma][MDNDeviceOrientaitonGamma] .</span><span class="sxs-lookup"><span data-stu-id="3c392-279">To enter your own orientation, choose **Custom orientation**, and enter your own [alpha][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta], and [gamma][MDNDeviceOrientaitonGamma] values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Opciones de orientación en el panel sensores" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    <span data-ttu-id="3c392-281">Opciones de **orientación** en el panel **sensores**</span><span class="sxs-lookup"><span data-stu-id="3c392-281">**Orientation** options on the **Sensors** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="3c392-282">Establecer cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="3c392-282">Set user agent string</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="3c392-283">Si la página depende de la cadena de agente de usuario de un dispositivo móvil para representarla correctamente, use el panel **condiciones de red** para proporcionar diferentes cadenas de agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="3c392-283">If your page depends on the user agent string from a mobile device to render properly, use the **Network conditions** panel to provide different user agent strings.</span></span>  
      
      1.  <span data-ttu-id="3c392-284">Elija **personalizar y controlar DevTools** \ ( `...` \) > **más herramientas**  >  **condiciones de red**.</span><span class="sxs-lookup"><span data-stu-id="3c392-284">Choose **Customize and control DevTools** \(`...`\) > **More tools** > **Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrada de condiciones de red en el menú más herramientas" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         <span data-ttu-id="3c392-286">Entrada de **condiciones de red** en el menú **más herramientas**</span><span class="sxs-lookup"><span data-stu-id="3c392-286">**Network conditions** entry in the **More tools** menu</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  <span data-ttu-id="3c392-287">Abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="3c392-287">Open the Command Menu.</span></span>  
          *   <span data-ttu-id="3c392-288">Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="3c392-288">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
      1. <span data-ttu-id="3c392-289">Escriba `Network conditions` y elija **Mostrar condiciones de red**.</span><span class="sxs-lookup"><span data-stu-id="3c392-289">Type `Network conditions`, and choose **Show Network conditions**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Mostrar condiciones de red" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **<span data-ttu-id="3c392-291">Mostrar condiciones de red</span><span class="sxs-lookup"><span data-stu-id="3c392-291">Show Network conditions</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="3c392-292">Junto a **agente de usuario**, desactive la casilla **seleccionar automáticamente** .</span><span class="sxs-lookup"><span data-stu-id="3c392-292">Next to **User agent**, clear the **Select automatically** checkbox.</span></span>  <span data-ttu-id="3c392-293">Después, seleccione **personalizado...** para seleccionar en una lista de cadenas de agente de usuario predefinidas.</span><span class="sxs-lookup"><span data-stu-id="3c392-293">Then, select **Custom...** to select from a list of predefined user agent strings.</span></span>  <span data-ttu-id="3c392-294">Para introducir su propia cadena de agente de usuario, escriba la cadena en **Escriba un agente de usuario personalizado**.</span><span class="sxs-lookup"><span data-stu-id="3c392-294">To enter your own user agent string, enter the string in **Enter a custom user agent**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Establecer la cadena de agente de usuario en Microsoft Edge en macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    <span data-ttu-id="3c392-296">Establecer la cadena de agente de usuario en Microsoft Edge en macOS</span><span class="sxs-lookup"><span data-stu-id="3c392-296">Set the user agent string to Microsoft Edge on macOS</span></span>  
:::image-end:::  

## <span data-ttu-id="3c392-297">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3c392-297">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "Introducción a la depuración remota de dispositivos Android | Microsoft docs "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. Alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Orden de aproximación-primer orden-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="3c392-305">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3c392-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3c392-306">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3c392-306">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3c392-308">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3c392-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
