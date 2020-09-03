---
description: Usa dispositivos virtuales en modo de dispositivo para que Microsoft Edge compile sitios web móviles.
title: Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: eababe8112b5d888671a8955e16f0fe1c89564fb
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993019"
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





# <span data-ttu-id="abccb-104">Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="abccb-104">Simulate mobile devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="abccb-105">Use el modo de dispositivo para aproximar el aspecto y el rendimiento de la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="abccb-105">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="abccb-106">El modo de dispositivo es el nombre de la colección floja de características de Microsoft Edge DevTools que le ayudan a simular dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="abccb-106">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="abccb-107">Entre estas funciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="abccb-107">These features include:</span></span>  

*   [<span data-ttu-id="abccb-108">Simular un área de visualización móvil</span><span class="sxs-lookup"><span data-stu-id="abccb-108">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="abccb-109">Limitación de la red</span><span class="sxs-lookup"><span data-stu-id="abccb-109">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="abccb-110">Limitación de la CPU</span><span class="sxs-lookup"><span data-stu-id="abccb-110">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="abccb-111">Simulando geolocalización</span><span class="sxs-lookup"><span data-stu-id="abccb-111">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="abccb-112">Establecer la orientación</span><span class="sxs-lookup"><span data-stu-id="abccb-112">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="abccb-113">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="abccb-113">Limitations</span></span>   

<span data-ttu-id="abccb-114">Considere el modo de dispositivo como una [aproximación de primer orden][WikiApproximation] de la apariencia y el aspecto de su página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="abccb-114">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="abccb-115">Con el modo de dispositivo, no ejecutas el código en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="abccb-115">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="abccb-116">Simula la experiencia de usuario móvil desde su equipo portátil o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="abccb-116">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="abccb-117">Hay algunos aspectos de los dispositivos móviles que DevTools nunca podrá simular.</span><span class="sxs-lookup"><span data-stu-id="abccb-117">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="abccb-118">Por ejemplo, la arquitectura de las CPU móviles es muy diferente de la arquitectura de las CPU de equipos portátiles o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="abccb-118">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="abccb-119">Cuando tenga dudas, la mejor opción es ejecutar la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="abccb-119">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="abccb-120">Use [depuración remota] [DevToolsRemoteDebugging] para ver, cambiar, depurar y perfilar el código de una página desde su equipo portátil o de escritorio mientras se ejecuta en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="abccb-120">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="abccb-121">Simular un área de visualización móvil</span><span class="sxs-lookup"><span data-stu-id="abccb-121">Simulate a mobile viewport</span></span>   

<span data-ttu-id="abccb-122">Haga clic en **Alternar barra de herramientas dispositivo** \ ( ![ Alternar barra de herramientas dispositivo ][ImageDeviceToolbarIcon] \) para abrir la interfaz de usuario que le permite simular un área de visualización móvil.</span><span class="sxs-lookup"><span data-stu-id="abccb-122">Click **Toggle Device Toolbar** \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="abccb-124">La barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="abccb-124">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="abccb-125">De forma predeterminada, la barra de herramientas del dispositivo se abre en modo de ventanilla eficaz.</span><span class="sxs-lookup"><span data-stu-id="abccb-125">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="abccb-126">Modo de ventanilla receptiva</span><span class="sxs-lookup"><span data-stu-id="abccb-126">Responsive Viewport Mode</span></span>   

<span data-ttu-id="abccb-127">Arrastre los controladores para cambiar el tamaño de la ventanilla a cualquier dimensión que necesite.</span><span class="sxs-lookup"><span data-stu-id="abccb-127">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="abccb-128">O bien, escriba valores específicos en los cuadros ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="abccb-128">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="abccb-129">En la siguiente ilustración, el ancho se establece en `626` y el alto se establece en `516` .</span><span class="sxs-lookup"><span data-stu-id="abccb-129">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   <span data-ttu-id="abccb-131">Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica</span><span class="sxs-lookup"><span data-stu-id="abccb-131">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="abccb-132">Mostrar consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="abccb-132">Show media queries</span></span>   

<span data-ttu-id="abccb-133">Para mostrar los puntos de interrupción de la consulta multimedia encima de su ventanilla, haga clic en **más opciones** y seleccione **Mostrar consultas multimedia**.</span><span class="sxs-lookup"><span data-stu-id="abccb-133">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas multimedia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="abccb-135">Mostrar consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="abccb-135">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="abccb-136">Haga clic en un punto de interrupción para cambiar el ancho de la ventanilla de modo que se desencadene el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="abccb-136">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="abccb-138">Hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="abccb-138">Click a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="abccb-139">Establecer el tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="abccb-139">Set the device type</span></span>   

<span data-ttu-id="abccb-140">Use la lista **tipo de dispositivo** para simular un dispositivo móvil o un dispositivo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="abccb-140">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Lista tipo de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="abccb-142">Lista **tipo de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="abccb-142">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="abccb-143">En la tabla siguiente se describen las diferencias entre las opciones.</span><span class="sxs-lookup"><span data-stu-id="abccb-143">The table below describes the differences between the options.</span></span>  <span data-ttu-id="abccb-144">**Método de representación** hace referencia a si Microsoft Edge representa la página como un área de visualización de escritorio o móvil.</span><span class="sxs-lookup"><span data-stu-id="abccb-144">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="abccb-145">El **icono cursor** hace referencia al tipo de cursor que se ve al pasar el puntero por la página.</span><span class="sxs-lookup"><span data-stu-id="abccb-145">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="abccb-146">**Eventos desencadenados** hace referencia a si la página `touch` se desencadena o se produce un `click` evento al interactuar con la página.</span><span class="sxs-lookup"><span data-stu-id="abccb-146">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="abccb-147">Opción</span><span class="sxs-lookup"><span data-stu-id="abccb-147">Option</span></span> | <span data-ttu-id="abccb-148">Método de representación</span><span class="sxs-lookup"><span data-stu-id="abccb-148">Rendering method</span></span> | <span data-ttu-id="abccb-149">Icono cursor</span><span class="sxs-lookup"><span data-stu-id="abccb-149">Cursor icon</span></span> | <span data-ttu-id="abccb-150">Eventos desencadenados</span><span class="sxs-lookup"><span data-stu-id="abccb-150">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="abccb-151">Móvil</span><span class="sxs-lookup"><span data-stu-id="abccb-151">Mobile</span></span> | <span data-ttu-id="abccb-152">Móvil</span><span class="sxs-lookup"><span data-stu-id="abccb-152">Mobile</span></span> | <span data-ttu-id="abccb-153">Círculo</span><span class="sxs-lookup"><span data-stu-id="abccb-153">Circle</span></span> | <span data-ttu-id="abccb-154">Función táctil</span><span class="sxs-lookup"><span data-stu-id="abccb-154">touch</span></span> |  
| <span data-ttu-id="abccb-155">Móvil \ (sin contacto \)</span><span class="sxs-lookup"><span data-stu-id="abccb-155">Mobile \(no touch\)</span></span> | <span data-ttu-id="abccb-156">Móvil</span><span class="sxs-lookup"><span data-stu-id="abccb-156">Mobile</span></span> | <span data-ttu-id="abccb-157">Normal</span><span class="sxs-lookup"><span data-stu-id="abccb-157">Normal</span></span> | <span data-ttu-id="abccb-158"> haz clic en </span><span class="sxs-lookup"><span data-stu-id="abccb-158">click</span></span> |  
| <span data-ttu-id="abccb-159">Escritorio</span><span class="sxs-lookup"><span data-stu-id="abccb-159">Desktop</span></span> | <span data-ttu-id="abccb-160">Escritorio</span><span class="sxs-lookup"><span data-stu-id="abccb-160">Desktop</span></span> | <span data-ttu-id="abccb-161">Normal</span><span class="sxs-lookup"><span data-stu-id="abccb-161">Normal</span></span> | <span data-ttu-id="abccb-162"> haz clic en </span><span class="sxs-lookup"><span data-stu-id="abccb-162">click</span></span> |  
| <span data-ttu-id="abccb-163">Escritorio \ (Touch \)</span><span class="sxs-lookup"><span data-stu-id="abccb-163">Desktop \(touch\)</span></span> | <span data-ttu-id="abccb-164">Escritorio</span><span class="sxs-lookup"><span data-stu-id="abccb-164">Desktop</span></span> | <span data-ttu-id="abccb-165">Círculo</span><span class="sxs-lookup"><span data-stu-id="abccb-165">Circle</span></span> | <span data-ttu-id="abccb-166">Función táctil</span><span class="sxs-lookup"><span data-stu-id="abccb-166">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="abccb-167">Si no ve la lista **tipo de dispositivo** , haga clic en **más opciones** y seleccione **Agregar tipo de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="abccb-167">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="abccb-168">Modo de ventanilla de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="abccb-168">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="abccb-169">Para simular las dimensiones de un dispositivo móvil específico, seleccione el dispositivo en la lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="abccb-169">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="La lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="abccb-171">La lista de **dispositivos**</span><span class="sxs-lookup"><span data-stu-id="abccb-171">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="abccb-172">Girar la ventanilla a la orientación horizontal</span><span class="sxs-lookup"><span data-stu-id="abccb-172">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="abccb-173">Haga clic en **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar la ventanilla a orientación horizontal.</span><span class="sxs-lookup"><span data-stu-id="abccb-173">Click **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Orientación horizontal" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   <span data-ttu-id="abccb-175">Orientación horizontal</span><span class="sxs-lookup"><span data-stu-id="abccb-175">Landscape orientation</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="abccb-176">El botón **girar** desaparecerá si la **barra de herramientas del dispositivo** es estrecha.</span><span class="sxs-lookup"><span data-stu-id="abccb-176">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="abccb-178">La **barra de herramientas del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="abccb-178">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="abccb-179">Consulte también [establecer orientación](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="abccb-179">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="abccb-180">Mostrar marco del dispositivo</span><span class="sxs-lookup"><span data-stu-id="abccb-180">Show device frame</span></span>   

<span data-ttu-id="abccb-181">Al simular las dimensiones de un dispositivo móvil específico, como un iPhone 6, Abra **más opciones** y, a continuación, seleccione **Mostrar marco del dispositivo** para mostrar el marco del dispositivo físico en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="abccb-181">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="abccb-182">Si no ve un marco de dispositivo para un dispositivo en particular, significa que es probable que DevTools simplemente no tenga imágenes para esa opción específica.</span><span class="sxs-lookup"><span data-stu-id="abccb-182">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar marco del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="abccb-184">Mostrar marco del dispositivo</span><span class="sxs-lookup"><span data-stu-id="abccb-184">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="El marco del dispositivo para el iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="abccb-186">El marco del dispositivo para el iPhone 6</span><span class="sxs-lookup"><span data-stu-id="abccb-186">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="abccb-187">Agregar un dispositivo móvil personalizado</span><span class="sxs-lookup"><span data-stu-id="abccb-187">Add a custom mobile device</span></span>   

<span data-ttu-id="abccb-188">Para agregar un dispositivo personalizado:</span><span class="sxs-lookup"><span data-stu-id="abccb-188">To add a custom device:</span></span>  

1.  <span data-ttu-id="abccb-189">Haga clic en la lista de **dispositivos** y seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="abccb-189">Click the **Device** list and then select **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Seleccione Editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="abccb-191">Seleccione **Editar**</span><span class="sxs-lookup"><span data-stu-id="abccb-191">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="abccb-192">Haga clic en **Agregar dispositivo personalizado**.</span><span class="sxs-lookup"><span data-stu-id="abccb-192">Click **Add custom device**.</span></span>  
1.  <span data-ttu-id="abccb-193">Escriba un nombre, una anchura y un alto para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="abccb-193">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="abccb-194">La [relación de píxeles del dispositivo][MDNWindowDevicePixelRatio], la [cadena de agente de usuario][MDNUserAgent]y los campos de tipo de [dispositivo](#set-the-device-type) son opcionales.</span><span class="sxs-lookup"><span data-stu-id="abccb-194">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="abccb-195">El campo tipo de dispositivo es la lista que se establece en **móvil** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="abccb-195">The device type field is the list that is set to **Mobile** by default.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Crear un dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="abccb-197">Crear un dispositivo personalizado</span><span class="sxs-lookup"><span data-stu-id="abccb-197">Createa custom device</span></span>  
    :::image-end:::  

### <span data-ttu-id="abccb-198">Mostrar reglas</span><span class="sxs-lookup"><span data-stu-id="abccb-198">Show rulers</span></span>   

<span data-ttu-id="abccb-199">Haga clic en **más opciones** y, a continuación, seleccione **Mostrar reglas** para ver las reglas por encima y a la izquierda de su ventanilla.</span><span class="sxs-lookup"><span data-stu-id="abccb-199">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="abccb-200">La unidad de tamaño de las reglas es píxeles.</span><span class="sxs-lookup"><span data-stu-id="abccb-200">The sizing unit of the rulers is pixels.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Mostrar reglas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **<span data-ttu-id="abccb-202">Mostrar reglas</span><span class="sxs-lookup"><span data-stu-id="abccb-202">Show rulers</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Reglas por encima y a la izquierda de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="abccb-204">Reglas por encima y a la izquierda de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="abccb-204">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="abccb-205">Acercar la ventanilla</span><span class="sxs-lookup"><span data-stu-id="abccb-205">Zoom the viewport</span></span>   

<span data-ttu-id="abccb-206">Use la lista de **zoom** para acercar o alejar.</span><span class="sxs-lookup"><span data-stu-id="abccb-206">Use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="abccb-208">Zoom</span><span class="sxs-lookup"><span data-stu-id="abccb-208">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="abccb-209">Limitar la red y la CPU</span><span class="sxs-lookup"><span data-stu-id="abccb-209">Throttle the network and CPU</span></span>   

<span data-ttu-id="abccb-210">Para limitar la red y la CPU, seleccione teléfono móvil de **nivel intermedio** o **móvil de gama baja** de la lista **acelerador** .</span><span class="sxs-lookup"><span data-stu-id="abccb-210">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="La lista de aceleración" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="abccb-212">La lista de **aceleración**</span><span class="sxs-lookup"><span data-stu-id="abccb-212">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="abccb-213">El **teléfono móvil de nivel intermedio** simula una 3G rápida y acelera tu CPU para que sea 4 veces más lenta de lo normal.</span><span class="sxs-lookup"><span data-stu-id="abccb-213">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="abccb-214">Los **teléfonos móviles de low-end** simulan una 3G lenta y aceleran la CPU 6 veces más despacio de lo normal.</span><span class="sxs-lookup"><span data-stu-id="abccb-214">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="abccb-215">Tenga en cuenta que el límite es relativo a la capacidad normal de su equipo portátil o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="abccb-215">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="abccb-216">La lista de **aceleradores** se oculta si la **barra de herramientas del dispositivo** es estrecha.</span><span class="sxs-lookup"><span data-stu-id="abccb-216">The **Throttle** list is hidden if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="abccb-218">La **barra de herramientas del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="abccb-218">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="abccb-219">Limitar solo la CPU</span><span class="sxs-lookup"><span data-stu-id="abccb-219">Throttle the CPU only</span></span>   

<span data-ttu-id="abccb-220">Para limitar solo la CPU y no la red, vaya al panel **rendimiento** , haga clic en **configuración de captura** \ ![ (capturar configuración ][ImageCaptureIcon] \) y, a continuación, seleccione velocidad **lenta** o velocidad **6X** en la lista de **CPU** .</span><span class="sxs-lookup"><span data-stu-id="abccb-220">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\), and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Lista de CPU" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   <span data-ttu-id="abccb-222">Lista de **CPU**</span><span class="sxs-lookup"><span data-stu-id="abccb-222">The **CPU** list</span></span>  
:::image-end:::  

### <span data-ttu-id="abccb-223">Limitar la velocidad de la red</span><span class="sxs-lookup"><span data-stu-id="abccb-223">Throttle the network only</span></span>   

<span data-ttu-id="abccb-224">Para limitar solo la red y no la CPU, vaya al panel **red** y seleccione **3G rápido** o **3G lento** de la lista **acelerador** .</span><span class="sxs-lookup"><span data-stu-id="abccb-224">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="La lista de aceleración" lightbox="../media/device-mode-network-throttle.msft.png":::
   <span data-ttu-id="abccb-226">La lista de **aceleración**</span><span class="sxs-lookup"><span data-stu-id="abccb-226">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="abccb-227">O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**, escriba `3G` y seleccione **Habilitar aceleración 3G rápida** o **Habilitar limitación 3G lento**.</span><span class="sxs-lookup"><span data-stu-id="abccb-227">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="El menú de comandos" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   <span data-ttu-id="abccb-229">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="abccb-229">The **Command Menu**</span></span>  
:::image-end:::  

<span data-ttu-id="abccb-230">También puede establecer el límite de red en el panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="abccb-230">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="abccb-231">Haga clic en **configuración de captura** \ ( ![ capturar configuración ][ImageCaptureIcon] \) y, a continuación, seleccione **3G rápido** o **3G lento** de la lista de **redes** .</span><span class="sxs-lookup"><span data-stu-id="abccb-231">Click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Configurar el límite de red en el panel rendimiento" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   <span data-ttu-id="abccb-233">Configurar el límite de red en el panel **rendimiento**</span><span class="sxs-lookup"><span data-stu-id="abccb-233">Set network throttling from the **Performance** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="abccb-234">Invalidar geolocalización</span><span class="sxs-lookup"><span data-stu-id="abccb-234">Override geolocation</span></span>   

<span data-ttu-id="abccb-235">Para abrir la interfaz de usuario de reemplazo de ubicaciones, haga clic en **personalizar y control DevTools** \ ( `...` \) y, a continuación, seleccione **más**  >  **sensores**de herramientas.</span><span class="sxs-lookup"><span data-stu-id="abccb-235">To open the geolocation overriding UI click **Customize and control DevTools** \(`...`\) and then select **More tools** > **Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **<span data-ttu-id="abccb-237">Sensores</span><span class="sxs-lookup"><span data-stu-id="abccb-237">Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="abccb-238">O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `Sensors` y, a continuación, seleccione **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="abccb-238">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **<span data-ttu-id="abccb-240">Mostrar sensores</span><span class="sxs-lookup"><span data-stu-id="abccb-240">Show Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="abccb-241">Seleccione uno de los valores preestablecidos de la lista **ubicación geográfica** o seleccione **ubicación personalizada** para escribir sus propias coordenadas o seleccione **ubicación no disponible** para probar cómo se comporta la página cuando la geolocalización está en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="abccb-241">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Geolocalización" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **<span data-ttu-id="abccb-243">Geolocalización</span><span class="sxs-lookup"><span data-stu-id="abccb-243">Geolocation</span></span>**  
:::image-end:::  

## <span data-ttu-id="abccb-244">Establecer orientación</span><span class="sxs-lookup"><span data-stu-id="abccb-244">Set orientation</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="abccb-245">Para abrir la interfaz de usuario de orientación, haga clic en **personalizar y controle DevTools** `...` y, a continuación, seleccione **más**  >  **sensores**de herramientas.</span><span class="sxs-lookup"><span data-stu-id="abccb-245">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **<span data-ttu-id="abccb-247">Sensores</span><span class="sxs-lookup"><span data-stu-id="abccb-247">Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="abccb-248">O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `Sensors` y, a continuación, seleccione **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="abccb-248">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **<span data-ttu-id="abccb-250">Mostrar sensores</span><span class="sxs-lookup"><span data-stu-id="abccb-250">Show Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="abccb-251">Seleccione uno de los valores preestablecidos de la lista **orientación** o seleccione **orientación personalizada** para establecer sus propios valores alfa, beta y gamma.</span><span class="sxs-lookup"><span data-stu-id="abccb-251">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Orientación" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **<span data-ttu-id="abccb-253">Orientación</span><span class="sxs-lookup"><span data-stu-id="abccb-253">Orientation</span></span>**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "Introducción a la depuración remota de dispositivos Android | Microsoft docs "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Orden de aproximación-primer orden-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="abccb-258">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="abccb-258">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="abccb-259">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="abccb-259">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="abccb-261">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="abccb-261">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
