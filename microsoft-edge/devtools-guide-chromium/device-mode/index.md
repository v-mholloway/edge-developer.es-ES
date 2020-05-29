---
title: Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607429"
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





# <span data-ttu-id="f164f-103">Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f164f-103">Simulate Mobile Devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="f164f-104">Use el modo de dispositivo para aproximar el aspecto y el rendimiento de la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="f164f-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="f164f-105">El modo de dispositivo es el nombre de la colección floja de características de Microsoft Edge DevTools que le ayudan a simular dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="f164f-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="f164f-106">Entre estas funciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="f164f-106">These features include:</span></span>  

*   [<span data-ttu-id="f164f-107">Simular un área de visualización móvil</span><span class="sxs-lookup"><span data-stu-id="f164f-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="f164f-108">Limitación de la red</span><span class="sxs-lookup"><span data-stu-id="f164f-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="f164f-109">Limitación de la CPU</span><span class="sxs-lookup"><span data-stu-id="f164f-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="f164f-110">Simulando geolocalización</span><span class="sxs-lookup"><span data-stu-id="f164f-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="f164f-111">Establecer la orientación</span><span class="sxs-lookup"><span data-stu-id="f164f-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="f164f-112">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="f164f-112">Limitations</span></span>   

<span data-ttu-id="f164f-113">Considere el modo de dispositivo como una [aproximación de primer orden][WikiApproximation] de la apariencia y el aspecto de su página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="f164f-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="f164f-114">Con el modo de dispositivo, no ejecutas el código en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="f164f-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="f164f-115">Simula la experiencia de usuario móvil desde su equipo portátil o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="f164f-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="f164f-116">Hay algunos aspectos de los dispositivos móviles que DevTools nunca podrá simular.</span><span class="sxs-lookup"><span data-stu-id="f164f-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="f164f-117">Por ejemplo, la arquitectura de las CPU móviles es muy diferente de la arquitectura de las CPU de equipos portátiles o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="f164f-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="f164f-118">Cuando tenga dudas, la mejor opción es ejecutar la página en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="f164f-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="f164f-119">Use [depuración remota] [DevToolsRemoteDebugging] para ver, cambiar, depurar y perfilar el código de una página desde su equipo portátil o de escritorio mientras se ejecuta en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="f164f-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="f164f-120">Simular un área de visualización móvil</span><span class="sxs-lookup"><span data-stu-id="f164f-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="f164f-121">Haga clic en **activar o** desactivar la barra de herramientas dispositivo ![ ][ImageDeviceToolbarIcon] para abrir la interfaz de usuario que le permite simular un área de visualización móvil.</span><span class="sxs-lookup"><span data-stu-id="f164f-121">Click **Toggle Device Toolbar** ![Toggle Device Toolbar][ImageDeviceToolbarIcon] to open the UI that enables you to simulate a mobile viewport.</span></span>  

> ##### <span data-ttu-id="f164f-122">Figura 1</span><span class="sxs-lookup"><span data-stu-id="f164f-122">Figure 1</span></span>  
> <span data-ttu-id="f164f-123">La barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f164f-123">The Device Toolbar</span></span>  
> ![La barra de herramientas del dispositivo][ImageDeviceToolbar]  

<span data-ttu-id="f164f-125">De forma predeterminada, la barra de herramientas del dispositivo se abre en modo de ventanilla eficaz.</span><span class="sxs-lookup"><span data-stu-id="f164f-125">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="f164f-126">Modo de ventanilla receptiva</span><span class="sxs-lookup"><span data-stu-id="f164f-126">Responsive Viewport Mode</span></span>   

<span data-ttu-id="f164f-127">Arrastre los controladores para cambiar el tamaño de la ventanilla a cualquier dimensión que necesite.</span><span class="sxs-lookup"><span data-stu-id="f164f-127">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="f164f-128">O bien, escriba valores específicos en los cuadros ancho y alto.</span><span class="sxs-lookup"><span data-stu-id="f164f-128">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="f164f-129">En la [ilustración 2](#figure-2), el ancho se establece en `626` y el alto se establece en `516` .</span><span class="sxs-lookup"><span data-stu-id="f164f-129">In [Figure 2](#figure-2), the width is set to `626` and the height is set to `516`.</span></span>  

> ##### <span data-ttu-id="f164f-130">Figura 2</span><span class="sxs-lookup"><span data-stu-id="f164f-130">Figure 2</span></span>  
> <span data-ttu-id="f164f-131">Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica</span><span class="sxs-lookup"><span data-stu-id="f164f-131">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
> ![Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica][ImageResponsiveHandles]  

#### <span data-ttu-id="f164f-133">Mostrar consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="f164f-133">Show media queries</span></span>   

<span data-ttu-id="f164f-134">Para mostrar los puntos de interrupción de la consulta multimedia encima de su ventanilla, haga clic en **más opciones** y seleccione **Mostrar consultas multimedia**.</span><span class="sxs-lookup"><span data-stu-id="f164f-134">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

> ##### <span data-ttu-id="f164f-135">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="f164f-135">Figure 3</span></span>  
> <span data-ttu-id="f164f-136">Mostrar consultas multimedia</span><span class="sxs-lookup"><span data-stu-id="f164f-136">Show media queries</span></span>  
> ![Mostrar consultas multimedia][ImageShowMediaQueries]  

<span data-ttu-id="f164f-138">Haga clic en un punto de interrupción para cambiar el ancho de la ventanilla de modo que se desencadene el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="f164f-138">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

> ##### <span data-ttu-id="f164f-139">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="f164f-139">Figure 4</span></span>  
> <span data-ttu-id="f164f-140">Hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="f164f-140">Click a breakpoint to change the width of the viewport</span></span>  
> ![Hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla][ImageBreakpoint]  

#### <span data-ttu-id="f164f-142">Establecer el tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f164f-142">Set the device type</span></span>   

<span data-ttu-id="f164f-143">Use la lista **tipo de dispositivo** para simular un dispositivo móvil o un dispositivo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="f164f-143">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

> ##### <span data-ttu-id="f164f-144">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="f164f-144">Figure 5</span></span>  
> <span data-ttu-id="f164f-145">Lista **tipo de dispositivo**</span><span class="sxs-lookup"><span data-stu-id="f164f-145">The **Device Type** list</span></span>  
> ![Lista tipo de dispositivo][ImageDeviceType]  

<span data-ttu-id="f164f-147">En la tabla siguiente se describen las diferencias entre las opciones.</span><span class="sxs-lookup"><span data-stu-id="f164f-147">The table below describes the differences between the options.</span></span>  <span data-ttu-id="f164f-148">**Método de representación** hace referencia a si Microsoft Edge representa la página como un área de visualización de escritorio o móvil.</span><span class="sxs-lookup"><span data-stu-id="f164f-148">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="f164f-149">El **icono cursor** hace referencia al tipo de cursor que se ve al pasar el puntero por la página.</span><span class="sxs-lookup"><span data-stu-id="f164f-149">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="f164f-150">**Eventos desencadenados** hace referencia a si la página `touch` se desencadena o se produce un `click` evento al interactuar con la página.</span><span class="sxs-lookup"><span data-stu-id="f164f-150">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="f164f-151">Opción</span><span class="sxs-lookup"><span data-stu-id="f164f-151">Option</span></span> | <span data-ttu-id="f164f-152">Método de representación</span><span class="sxs-lookup"><span data-stu-id="f164f-152">Rendering method</span></span> | <span data-ttu-id="f164f-153">Icono cursor</span><span class="sxs-lookup"><span data-stu-id="f164f-153">Cursor icon</span></span> | <span data-ttu-id="f164f-154">Eventos desencadenados</span><span class="sxs-lookup"><span data-stu-id="f164f-154">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="f164f-155">Móvil</span><span class="sxs-lookup"><span data-stu-id="f164f-155">Mobile</span></span> | <span data-ttu-id="f164f-156">Móvil</span><span class="sxs-lookup"><span data-stu-id="f164f-156">Mobile</span></span> | <span data-ttu-id="f164f-157">Círculo</span><span class="sxs-lookup"><span data-stu-id="f164f-157">Circle</span></span> | <span data-ttu-id="f164f-158">Función táctil</span><span class="sxs-lookup"><span data-stu-id="f164f-158">touch</span></span> |  
| <span data-ttu-id="f164f-159">Móvil \ (sin contacto \)</span><span class="sxs-lookup"><span data-stu-id="f164f-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="f164f-160">Móvil</span><span class="sxs-lookup"><span data-stu-id="f164f-160">Mobile</span></span> | <span data-ttu-id="f164f-161">Normal</span><span class="sxs-lookup"><span data-stu-id="f164f-161">Normal</span></span> | <span data-ttu-id="f164f-162"> haz clic en </span><span class="sxs-lookup"><span data-stu-id="f164f-162">click</span></span> |  
| <span data-ttu-id="f164f-163">Escritorio</span><span class="sxs-lookup"><span data-stu-id="f164f-163">Desktop</span></span> | <span data-ttu-id="f164f-164">Escritorio</span><span class="sxs-lookup"><span data-stu-id="f164f-164">Desktop</span></span> | <span data-ttu-id="f164f-165">Normal</span><span class="sxs-lookup"><span data-stu-id="f164f-165">Normal</span></span> | <span data-ttu-id="f164f-166"> haz clic en </span><span class="sxs-lookup"><span data-stu-id="f164f-166">click</span></span> |  
| <span data-ttu-id="f164f-167">Escritorio \ (Touch \)</span><span class="sxs-lookup"><span data-stu-id="f164f-167">Desktop \(touch\)</span></span> | <span data-ttu-id="f164f-168">Escritorio</span><span class="sxs-lookup"><span data-stu-id="f164f-168">Desktop</span></span> | <span data-ttu-id="f164f-169">Círculo</span><span class="sxs-lookup"><span data-stu-id="f164f-169">Circle</span></span> | <span data-ttu-id="f164f-170">Función táctil</span><span class="sxs-lookup"><span data-stu-id="f164f-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="f164f-171">Si no ve la lista **tipo de dispositivo** , haga clic en **más opciones** y seleccione **Agregar tipo de dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="f164f-171">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="f164f-172">Modo de ventanilla de dispositivos móviles</span><span class="sxs-lookup"><span data-stu-id="f164f-172">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="f164f-173">Para simular las dimensiones de un dispositivo móvil específico, seleccione el dispositivo en la lista de **dispositivos** .</span><span class="sxs-lookup"><span data-stu-id="f164f-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

> ##### <span data-ttu-id="f164f-174">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="f164f-174">Figure 6</span></span>  
> <span data-ttu-id="f164f-175">La lista de dispositivos</span><span class="sxs-lookup"><span data-stu-id="f164f-175">The Device list</span></span>  
> ![La lista de dispositivos][ImageDeviceList]  

#### <span data-ttu-id="f164f-177">Girar la ventanilla a la orientación horizontal</span><span class="sxs-lookup"><span data-stu-id="f164f-177">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="f164f-178">Haga clic en **girar** ![ girar ][ImageRotateIcon] para girar la ventanilla a orientación horizontal.</span><span class="sxs-lookup"><span data-stu-id="f164f-178">Click **Rotate** ![Rotate][ImageRotateIcon] to rotate the viewport to landscape orientation.</span></span>  

> ##### <span data-ttu-id="f164f-179">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="f164f-179">Figure 7</span></span>  
> <span data-ttu-id="f164f-180">Orientación horizontal</span><span class="sxs-lookup"><span data-stu-id="f164f-180">Landscape orientation</span></span>  
> ![Orientación horizontal][ImageLandscape]  

> [!NOTE]
> <span data-ttu-id="f164f-182">El botón **girar** desaparecerá si la **barra de herramientas del dispositivo** es estrecha.</span><span class="sxs-lookup"><span data-stu-id="f164f-182">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="f164f-183">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="f164f-183">Figure 8</span></span>  
> <span data-ttu-id="f164f-184">La barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f164f-184">The Device Toolbar</span></span>  
> ![La barra de herramientas del dispositivo][ImageDeviceToolbar2]  

<span data-ttu-id="f164f-186">Consulte también [establecer orientación](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="f164f-186">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="f164f-187">Mostrar marco del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f164f-187">Show device frame</span></span>   

<span data-ttu-id="f164f-188">Al simular las dimensiones de un dispositivo móvil específico, como un iPhone 6, Abra **más opciones** y, a continuación, seleccione **Mostrar marco del dispositivo** para mostrar el marco del dispositivo físico en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="f164f-188">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="f164f-189">Si no ve un marco de dispositivo para un dispositivo en particular, significa que es probable que DevTools simplemente no tenga imágenes para esa opción específica.</span><span class="sxs-lookup"><span data-stu-id="f164f-189">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

> ##### <span data-ttu-id="f164f-190">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="f164f-190">Figure 9</span></span>  
> <span data-ttu-id="f164f-191">Mostrar marco del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f164f-191">Show device frame</span></span>  
> ![Mostrar marco del dispositivo][ImageShowDeviceFrame]  

> ##### <span data-ttu-id="f164f-193">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="f164f-193">Figure 10</span></span>  
> <span data-ttu-id="f164f-194">El marco del dispositivo para el iPhone 6</span><span class="sxs-lookup"><span data-stu-id="f164f-194">The device frame for the iPhone 6</span></span>  
> ![El marco del dispositivo para el iPhone 6][ImageIphoneFrame]  

#### <span data-ttu-id="f164f-196">Agregar un dispositivo móvil personalizado</span><span class="sxs-lookup"><span data-stu-id="f164f-196">Add a custom mobile device</span></span>   

<span data-ttu-id="f164f-197">Para agregar un dispositivo personalizado:</span><span class="sxs-lookup"><span data-stu-id="f164f-197">To add a custom device:</span></span>  

1.  <span data-ttu-id="f164f-198">Haga clic en la lista de **dispositivos** y seleccione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="f164f-198">Click the **Device** list and then select **Edit**.</span></span>  

> ##### <span data-ttu-id="f164f-199">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="f164f-199">Figure 11</span></span>  
> <span data-ttu-id="f164f-200">Selección de **Editar**, 
> ![ selección de edición][ImageEdit]</span><span class="sxs-lookup"><span data-stu-id="f164f-200">Selecting **Edit**
![Selecting Edit][ImageEdit]</span></span>  

1.  <span data-ttu-id="f164f-201">Haga clic en **Agregar dispositivo personalizado**.</span><span class="sxs-lookup"><span data-stu-id="f164f-201">Click **Add custom device**.</span></span>  

1.  <span data-ttu-id="f164f-202">Escriba un nombre, una anchura y un alto para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f164f-202">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="f164f-203">La [relación de píxeles del dispositivo][MDNWindowDevicePixelRatio], la [cadena de agente de usuario][MDNUserAgent]y los campos de tipo de [dispositivo](#set-the-device-type) son opcionales.</span><span class="sxs-lookup"><span data-stu-id="f164f-203">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="f164f-204">El campo tipo de dispositivo es la lista que se establece en **móvil** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f164f-204">The device type field is the list that is set to **Mobile** by default.</span></span>  

> ##### <span data-ttu-id="f164f-205">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="f164f-205">Figure 12</span></span>  
> <span data-ttu-id="f164f-206">Crear un dispositivo personalizado</span><span class="sxs-lookup"><span data-stu-id="f164f-206">Creating a custom device</span></span>  
> ![Crear un dispositivo personalizado][ImageAddCustomDevice]  

### <span data-ttu-id="f164f-208">Mostrar reglas</span><span class="sxs-lookup"><span data-stu-id="f164f-208">Show rulers</span></span>   

<span data-ttu-id="f164f-209">Haga clic en **más opciones** y, a continuación, seleccione **Mostrar reglas** para ver las reglas por encima y a la izquierda de su ventanilla.</span><span class="sxs-lookup"><span data-stu-id="f164f-209">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="f164f-210">La unidad de tamaño de las reglas es píxeles.</span><span class="sxs-lookup"><span data-stu-id="f164f-210">The sizing unit of the rulers is pixels.</span></span>  

> ##### <span data-ttu-id="f164f-211">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="f164f-211">Figure 13</span></span>  
> <span data-ttu-id="f164f-212">Mostrar reglas</span><span class="sxs-lookup"><span data-stu-id="f164f-212">Show rulers</span></span>  
> ![Mostrar reglas][ImageShowRulers]  

> ##### <span data-ttu-id="f164f-214">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="f164f-214">Figure 14</span></span>  
> <span data-ttu-id="f164f-215">Reglas por encima y a la izquierda de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="f164f-215">Rulers above and to the left of the viewport</span></span>  
> ![Reglas por encima y a la izquierda de la ventanilla][ImageRulers]  

### <span data-ttu-id="f164f-217">Acercar la ventanilla</span><span class="sxs-lookup"><span data-stu-id="f164f-217">Zoom the viewport</span></span>   

<span data-ttu-id="f164f-218">Use la lista de **zoom** para acercar o alejar.</span><span class="sxs-lookup"><span data-stu-id="f164f-218">Use the **Zoom** list to zoom in or out.</span></span>  

> ##### <span data-ttu-id="f164f-219">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="f164f-219">Figure 15</span></span>  
> <span data-ttu-id="f164f-220">Zoom</span><span class="sxs-lookup"><span data-stu-id="f164f-220">Zoom</span></span>  
> ![Zoom][ImageZoomViewport]  

## <span data-ttu-id="f164f-222">Limitar la red y la CPU</span><span class="sxs-lookup"><span data-stu-id="f164f-222">Throttle the network and CPU</span></span>   

<span data-ttu-id="f164f-223">Para limitar la red y la CPU, seleccione teléfono móvil de **nivel intermedio** o **móvil de gama baja** de la lista **acelerador** .</span><span class="sxs-lookup"><span data-stu-id="f164f-223">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="f164f-224">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="f164f-224">Figure 16</span></span>  
> <span data-ttu-id="f164f-225">La lista de aceleración</span><span class="sxs-lookup"><span data-stu-id="f164f-225">The Throttle list</span></span>  
> ![La lista de aceleración][ImageThrottling]  

<span data-ttu-id="f164f-227">El **teléfono móvil de nivel intermedio** simula una 3G rápida y acelera tu CPU para que sea 4 veces más lenta de lo normal.</span><span class="sxs-lookup"><span data-stu-id="f164f-227">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="f164f-228">Los **teléfonos móviles de low-end** simulan una 3G lenta y aceleran la CPU 6 veces más despacio de lo normal.</span><span class="sxs-lookup"><span data-stu-id="f164f-228">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="f164f-229">Tenga en cuenta que el límite es relativo a la capacidad normal de su equipo portátil o de escritorio.</span><span class="sxs-lookup"><span data-stu-id="f164f-229">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="f164f-230">La lista de **aceleradores** se ocultará si la **barra de herramientas del dispositivo** es estrecha.</span><span class="sxs-lookup"><span data-stu-id="f164f-230">The **Throttle** list will be hidden if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="f164f-231">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="f164f-231">Figure 17</span></span>  
> <span data-ttu-id="f164f-232">La barra de herramientas del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f164f-232">The Device Toolbar</span></span>  
> ![La barra de herramientas del dispositivo][ImageDeviceToolbar3]  

### <span data-ttu-id="f164f-234">Limitar solo la CPU</span><span class="sxs-lookup"><span data-stu-id="f164f-234">Throttle the CPU only</span></span>   

<span data-ttu-id="f164f-235">Para limitar solo la CPU y no la red, vaya al panel **rendimiento** , haga clic en **capturar** ajustes de ![ captura configuración ][ImageCaptureIcon] y, a continuación, seleccione velocidad **lenta** o velocidad **6. disminución** de la lista de **CPU** .</span><span class="sxs-lookup"><span data-stu-id="f164f-235">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** ![Capture Settings][ImageCaptureIcon], and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

> ##### <span data-ttu-id="f164f-236">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="f164f-236">Figure 18</span></span>  
> <span data-ttu-id="f164f-237">Lista de CPU</span><span class="sxs-lookup"><span data-stu-id="f164f-237">The CPU list</span></span>  
> ![Lista de CPU][ImageCPU]  

### <span data-ttu-id="f164f-239">Limitar la velocidad de la red</span><span class="sxs-lookup"><span data-stu-id="f164f-239">Throttle the network only</span></span>   

<span data-ttu-id="f164f-240">Para limitar solo la red y no la CPU, vaya al panel **red** y seleccione **3G rápido** o **3G lento** de la lista **acelerador** .</span><span class="sxs-lookup"><span data-stu-id="f164f-240">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="f164f-241">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="f164f-241">Figure 19</span></span>  
> <span data-ttu-id="f164f-242">La lista de aceleración</span><span class="sxs-lookup"><span data-stu-id="f164f-242">The Throttle list</span></span>  
> ![La lista de aceleración][ImageNetwork]  

<span data-ttu-id="f164f-244">O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `3G` y seleccione **Habilitar aceleración 3G rápida** o **Habilitar limitación 3G lento**.</span><span class="sxs-lookup"><span data-stu-id="f164f-244">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

> ##### <span data-ttu-id="f164f-245">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="f164f-245">Figure 20</span></span>  
> <span data-ttu-id="f164f-246">El menú de comandos</span><span class="sxs-lookup"><span data-stu-id="f164f-246">The Command Menu</span></span>  
> ![El menú de comandos][ImageCommandMenu]  

<span data-ttu-id="f164f-248">También puede establecer el límite de red en el panel **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="f164f-248">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="f164f-249">Haga clic en **capturar** ![ configuración ][ImageCaptureIcon] de captura y, a continuación, seleccione **3G rápido** o **3G lento** de la lista de **redes** .</span><span class="sxs-lookup"><span data-stu-id="f164f-249">Click **Capture Settings** ![Capture Settings][ImageCaptureIcon] and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

> ##### <span data-ttu-id="f164f-250">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="f164f-250">Figure 21</span></span>  
> <span data-ttu-id="f164f-251">Configurar el límite de red en el panel rendimiento</span><span class="sxs-lookup"><span data-stu-id="f164f-251">Setting network throttling from the Performance panel</span></span>  
> ![Configurar el límite de red en el panel rendimiento][ImageNetwork2]  

## <span data-ttu-id="f164f-253">Invalidar geolocalización</span><span class="sxs-lookup"><span data-stu-id="f164f-253">Override geolocation</span></span>   

<span data-ttu-id="f164f-254">Para abrir la interfaz de usuario de reemplazo de ubicaciones, haga clic en **personalizar y controle DevTools** `...` y, a continuación, seleccione **más**  >  **sensores**de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f164f-254">To open the geolocation overriding UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="f164f-255">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="f164f-255">Figure 22</span></span>  
> <span data-ttu-id="f164f-256">Sensores</span><span class="sxs-lookup"><span data-stu-id="f164f-256">Sensors</span></span>  
> ![Sensores][ImageSensors]  

<span data-ttu-id="f164f-258">O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `Sensors` y, a continuación, seleccione **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="f164f-258">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="f164f-259">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="f164f-259">Figure 23</span></span>  
> <span data-ttu-id="f164f-260">Mostrar sensores</span><span class="sxs-lookup"><span data-stu-id="f164f-260">Show Sensors</span></span>  
> ![Mostrar sensores][ImageShowSensors]  

<span data-ttu-id="f164f-262">Seleccione uno de los valores preestablecidos de la lista **ubicación geográfica** o seleccione **ubicación personalizada** para escribir sus propias coordenadas o seleccione **ubicación no disponible** para probar cómo se comporta la página cuando la geolocalización está en un estado de error.</span><span class="sxs-lookup"><span data-stu-id="f164f-262">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

> ##### <span data-ttu-id="f164f-263">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="f164f-263">Figure 24</span></span>  
> <span data-ttu-id="f164f-264">Geolocalización</span><span class="sxs-lookup"><span data-stu-id="f164f-264">Geolocation</span></span>  
> ![Geolocalización][ImageGeolocation]  

## <span data-ttu-id="f164f-266">Establecer orientación</span><span class="sxs-lookup"><span data-stu-id="f164f-266">Set orientation</span></span>   

<span data-ttu-id="f164f-267">Para abrir la interfaz de usuario de orientación, haga clic en **personalizar y controle DevTools** `...` y, a continuación, seleccione **más**  >  **sensores**de herramientas.</span><span class="sxs-lookup"><span data-stu-id="f164f-267">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="f164f-268">Ilustración 25</span><span class="sxs-lookup"><span data-stu-id="f164f-268">Figure 25</span></span>  
> <span data-ttu-id="f164f-269">Sensores</span><span class="sxs-lookup"><span data-stu-id="f164f-269">Sensors</span></span>  
> ![Sensores][ImageSensors2]  

<span data-ttu-id="f164f-271">O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `Sensors` y, a continuación, seleccione **Mostrar sensores**.</span><span class="sxs-lookup"><span data-stu-id="f164f-271">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="f164f-272">Ilustración 26</span><span class="sxs-lookup"><span data-stu-id="f164f-272">Figure 26</span></span>  
> <span data-ttu-id="f164f-273">Mostrar sensores</span><span class="sxs-lookup"><span data-stu-id="f164f-273">Show Sensors</span></span>  
> ![Mostrar sensores][ImageShowSensors2]  

<span data-ttu-id="f164f-275">Seleccione uno de los valores preestablecidos de la lista **orientación** o seleccione **orientación personalizada** para establecer sus propios valores alfa, beta y gamma.</span><span class="sxs-lookup"><span data-stu-id="f164f-275">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

> ##### <span data-ttu-id="f164f-276">Ilustración 27</span><span class="sxs-lookup"><span data-stu-id="f164f-276">Figure 27</span></span>  
> <span data-ttu-id="f164f-277">Orientación</span><span class="sxs-lookup"><span data-stu-id="f164f-277">Orientation</span></span>  
> ![Orientación][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Ilustración 1: la barra de herramientas del dispositivo"  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Ilustración 2: los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla con capacidad de respuesta"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Ilustración 3: mostrar las consultas multimedia"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Ilustración 4: hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla"  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Ilustración 5: lista tipo de dispositivo"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Ilustración 6: la lista de dispositivos"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Ilustración 7: orientación horizontal"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Ilustración 8: la barra de herramientas del dispositivo"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Ilustración 9: Mostrar marco del dispositivo"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Ilustración 10: el marco del dispositivo para iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Ilustración 11: selección de edición"  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Ilustración 12: crear un dispositivo personalizado"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Ilustración 13: mostrar las reglas"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Ilustración 14: reglas por encima y a la izquierda de la ventanilla"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Ilustración 15: zoom"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Ilustración 16: la lista de aceleración"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Ilustración 17: la barra de herramientas del dispositivo"  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Ilustración 18: la lista de CPU"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "Ilustración 19: la lista de aceleración"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Ilustración 20: el menú de comandos"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Ilustración 21: configuración del límite de red en el panel rendimiento"  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Ilustración 22: sensores"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Ilustración 23: Mostrar sensores"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Ilustración 24: geolocalización"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Ilustración 25: sensores"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Ilustración 26: Mostrar sensores"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Ilustración 27: orientación"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/DevTools-Guide-Chromium/Remote-Debugging/index "Introducción a la depuración remota de dispositivos Android"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Orden de aproximación-primer orden-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="f164f-310">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f164f-310">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f164f-311">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f164f-311">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f164f-313">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f164f-313">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
