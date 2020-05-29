---
title: Novedades de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 17dab9120535ae11ea5a5456552d47dbd7f9e236
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684723"
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







# <span data-ttu-id="b85d4-103">Novedades de DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="b85d4-103">What's New In DevTools (Microsoft Edge 83)</span></span>   

  

<span data-ttu-id="b85d4-104">Después de la programación de cromo actualizada, estamos ajustando nuestra programación para las próximas versiones de Microsoft Edge y cancelando la versión 82 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b85d4-104">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="b85d4-105">Para obtener más información, consulta nuestra [entrada de blog][WindowsBlogStableRelease] .</span><span class="sxs-lookup"><span data-stu-id="b85d4-105">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>

<span data-ttu-id="b85d4-106">Estas son las nuevas características disponibles en el DevTools en Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="b85d4-106">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>

## <span data-ttu-id="b85d4-107">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b85d4-107">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="b85d4-108">Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b85d4-108">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="b85d4-109">Compruébelos para probar las nuevas características de la DevTools, las extensiones de código de VS y mucho más.</span><span class="sxs-lookup"><span data-stu-id="b85d4-109">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="b85d4-110">Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="b85d4-110">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="b85d4-111">Depurar Microsoft Edge de forma remota en dispositivos con Windows 10</span><span class="sxs-lookup"><span data-stu-id="b85d4-111">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="b85d4-112">La aplicación [de herramientas remotas para Microsoft Edge \ (beta \)][RemoteTools] ya está disponible en [Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="b85d4-112">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="b85d4-113">Con esta aplicación, que extiende [Windows Device portal][WindowsDevicePortal], podrás conectarte desde la instancia de Microsoft Edge que se ejecuta en el equipo de desarrollo a un dispositivo de Windows 10 remoto, ver una lista de destinos \ (todas las pestañas de Microsoft Edge y [PWAs][PWADoc] abiertas en el dispositivo Windows 10) y usar el DevTools en el equipo de desarrollo con un destino que se ejecute en el dispositivo remoto</span><span class="sxs-lookup"><span data-stu-id="b85d4-113">Using this app, which extends the [Windows Device Portal][WindowsDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PWADoc] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

> ##### <span data-ttu-id="b85d4-114">Figura 1</span><span class="sxs-lookup"><span data-stu-id="b85d4-114">Figure 1</span></span>  
> <span data-ttu-id="b85d4-115">La aplicación de [herramientas remotas para Microsoft Edge (beta)][RemoteTools] disponible en [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="b85d4-115">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
> ![La aplicación de herramientas remotas para Microsoft Edge (beta) disponible en Microsoft Store][ImageRemoteTools]  

<span data-ttu-id="b85d4-117">[Lea nuestra guía para configurar su dispositivo Windows 10 y su equipo de desarrollo para la depuración remota][RemoteDebuggingWin10].</span><span class="sxs-lookup"><span data-stu-id="b85d4-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][RemoteDebuggingWin10].</span></span>  <span data-ttu-id="b85d4-118">Infórmenos sobre su experiencia de depuración remota mediante la función de [Tweet][PostTweetEdgeDevTools] o haciendo clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b85d4-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

### <span data-ttu-id="b85d4-119">Nuevas formas de obtener acceso a la configuración</span><span class="sxs-lookup"><span data-stu-id="b85d4-119">New ways to access Settings</span></span> 

<span data-ttu-id="b85d4-120">Hay toneladas de opciones de configuración para el DevTools que puede personalizar para DevTools la apariencia y el funcionamiento de la manera que necesita.</span><span class="sxs-lookup"><span data-stu-id="b85d4-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="b85d4-121">En Microsoft Edge 83, obtener acceso a la [configuración][OverviewSettings] de la DevTools es ahora mucho más fácil.</span><span class="sxs-lookup"><span data-stu-id="b85d4-121">In Microsoft Edge 83, accessing [Settings][OverviewSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="b85d4-122">Abra configuración con el icono de engranaje junto a alertas de consola y el menú principal.</span><span class="sxs-lookup"><span data-stu-id="b85d4-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>

> ##### <span data-ttu-id="b85d4-123">Figura 2</span><span class="sxs-lookup"><span data-stu-id="b85d4-123">Figure 2</span></span> 
> <span data-ttu-id="b85d4-124">El icono de engranaje abre la configuración en la DevTools ![ el icono de engranaje abre la configuración de la DevTools][ImageSettingsGearIcon]</span><span class="sxs-lookup"><span data-stu-id="b85d4-124">The gear icon opens Settings in the DevTools ![The gear icon opens Settings in the DevTools][ImageSettingsGearIcon]</span></span>  

<span data-ttu-id="b85d4-125">También puede abrir la [configuración][OverviewSettings] desde el **menú principal** , en **más herramientas**.</span><span class="sxs-lookup"><span data-stu-id="b85d4-125">You are also able to open [Settings][OverviewSettings] from the **Main Menu** under **More tools**.</span></span>

> ##### <span data-ttu-id="b85d4-126">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="b85d4-126">Figure 3</span></span> 
> <span data-ttu-id="b85d4-127">Menú principal > más herramientas > configuración del ![ menú principal > más herramientas > configuración][ImageSettingsMainMenu]</span><span class="sxs-lookup"><span data-stu-id="b85d4-127">Main Menu > More tools > Settings ![Main Menu > More tools > Settings][ImageSettingsMainMenu]</span></span>  

<span data-ttu-id="b85d4-128">[#1050855][crbug1050855] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-128">Chromium issue [#1050855][crbug1050855]</span></span>

### <span data-ttu-id="b85d4-129">Infobars nuevos y mejorados</span><span class="sxs-lookup"><span data-stu-id="b85d4-129">New and improved infobars</span></span>

<span data-ttu-id="b85d4-130">Las barras de notificación informativas \ (infobars \) en DevTools ahora tienen un aspecto mejorado y una mayor funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="b85d4-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="b85d4-131">En Microsoft Edge 83, infobars son más fáciles de leer y proporcionan botones para que puedas llevar a cabo la acción pertinente de inmediato.</span><span class="sxs-lookup"><span data-stu-id="b85d4-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>

> ##### <span data-ttu-id="b85d4-132">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="b85d4-132">Figure 4</span></span>
> <span data-ttu-id="b85d4-133">Barra de barra para imprimir un archivo minified en Microsoft Edge 83 ![ barra de tiempo para imprimir un archivo de minified en Microsoft edge 83][ImageInfobar]</span><span class="sxs-lookup"><span data-stu-id="b85d4-133">Infobar for pretty-printing a minified file in Microsoft Edge 83 ![Infobar for pretty-printing a minified file in Microsoft Edge 83][ImageInfobar]</span></span>  

<span data-ttu-id="b85d4-134">[#1056348][crbug1056348] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-134">Chromium issue [#1056348][crbug1056348]</span></span>

### <span data-ttu-id="b85d4-135">Navegar por el selector de colores con el teclado</span><span class="sxs-lookup"><span data-stu-id="b85d4-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="b85d4-136">El [selector de colores][ColorPicker] es una GUI en el [Panel elementos][ElementsDoc] para el cambio `color` y las `background-color` declaraciones.</span><span class="sxs-lookup"><span data-stu-id="b85d4-136">The [Color Picker][ColorPicker] is a GUI in the [Elements panel][ElementsDoc] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="b85d4-137">En versiones anteriores de Microsoft Edge, no se podía navegar por la sección **sombras** del selector de [colores][ColorPicker] con el teclado.</span><span class="sxs-lookup"><span data-stu-id="b85d4-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][ColorPicker] with the keyboard.</span></span>  

> ##### <span data-ttu-id="b85d4-138">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="b85d4-138">Figure 5</span></span>  
> <span data-ttu-id="b85d4-139">Ahora puede usar el teclado para mover el selector en la sección **sombras** del [selector de colores][ColorPicker] .</span><span class="sxs-lookup"><span data-stu-id="b85d4-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][ColorPicker]</span></span>  
> ![Ahora puede usar el teclado para mover el selector en la sección sombras del selector de colores.][ImageColorPicker]  

<span data-ttu-id="b85d4-141">En Microsoft Edge 83, ahora puede usar el teclado para mover el selector en la sección **sombras** del selector de colores.</span><span class="sxs-lookup"><span data-stu-id="b85d4-141">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="b85d4-142">[#963183][crbug963183] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-142">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="b85d4-143">La pestaña propiedades ahora se rellena después de actualizar una página</span><span class="sxs-lookup"><span data-stu-id="b85d4-143">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="b85d4-144">En Microsoft Edge 81 y versiones anteriores, la **pestaña propiedades** del [Panel elementos][ElementsDoc] se interrumpió por actualizaciones de página.</span><span class="sxs-lookup"><span data-stu-id="b85d4-144">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][ElementsDoc] was broken by page refreshes.</span></span>  <span data-ttu-id="b85d4-145">Cuando ha actualizado la página, la **pestaña propiedades** no ha rellenado las propiedades del elemento seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b85d4-145">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

> ##### <span data-ttu-id="b85d4-146">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="b85d4-146">Figure 6</span></span>  
> <span data-ttu-id="b85d4-147">En Microsoft Edge 81 y versiones anteriores, la **pestaña propiedades** estaba en blanco después de actualizar una página</span><span class="sxs-lookup"><span data-stu-id="b85d4-147">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
> ![En Microsoft Edge 81 y versiones anteriores, la pestaña propiedades estaba en blanco después de actualizar una página][ImagePropertiesIn81]  

<span data-ttu-id="b85d4-149">En Microsoft Edge 83, ahora puede ver las propiedades del elemento seleccionado en ese momento después de actualizar una página en la **pestaña propiedades**.</span><span class="sxs-lookup"><span data-stu-id="b85d4-149">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

> ##### <span data-ttu-id="b85d4-150">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="b85d4-150">Figure 7</span></span>  
> <span data-ttu-id="b85d4-151">En Microsoft Edge 83, la **pestaña propiedades** muestra las propiedades del elemento seleccionado actualmente después de actualizar una página.</span><span class="sxs-lookup"><span data-stu-id="b85d4-151">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
> ![En Microsoft Edge 83, la pestaña propiedades muestra las propiedades del elemento seleccionado actualmente después de actualizar una página.][ImagePropertiesIn82]  

<span data-ttu-id="b85d4-153">[#1050999][crbug1050999] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-153">Chromium issue [#1050999][crbug1050999]</span></span>  

### <span data-ttu-id="b85d4-154">Use las teclas de dirección para desplazarse por la herramienta de cambios</span><span class="sxs-lookup"><span data-stu-id="b85d4-154">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="b85d4-155">La **herramienta cambios** realiza un seguimiento de los cambios realizados en CSS o JavaScript en el DevTools.</span><span class="sxs-lookup"><span data-stu-id="b85d4-155">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="b85d4-156">Puede usar la **herramienta cambios** para ver rápidamente todos los cambios y recuperarlos en el editor o IDE.</span><span class="sxs-lookup"><span data-stu-id="b85d4-156">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="b85d4-157">Para abrir la **herramienta de cambios** , pulsa `Ctrl` + `Shift` + `P` en el DevTools para abrir el menú de [comandos][DevToolsCommandMenuIndex] y escribir `changes` .</span><span class="sxs-lookup"><span data-stu-id="b85d4-157">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="b85d4-158">Seleccione y ejecute el comando **Mostrar cambios** para abrir la **herramienta de cambios** del alimentador de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b85d4-158">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="b85d4-159">Una vez que haya realizado un cambio en un archivo minified, la **herramienta cambios** le permitirá desplazarse horizontalmente para ver todo el código minified.</span><span class="sxs-lookup"><span data-stu-id="b85d4-159">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="b85d4-160">A partir de Microsoft Edge 83, ahora puede desplazarse horizontalmente con las teclas de dirección del teclado.</span><span class="sxs-lookup"><span data-stu-id="b85d4-160">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

> ##### <span data-ttu-id="b85d4-161">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="b85d4-161">Figure 8</span></span>  
> <span data-ttu-id="b85d4-162">En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de dirección para ver los cambios que realizó en el código de minified en la **herramienta de cambios**</span><span class="sxs-lookup"><span data-stu-id="b85d4-162">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
> ![En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de dirección para ver el código de minified en la herramienta de cambios][ImageChanges]  

<span data-ttu-id="b85d4-164">Si usa lectores de pantalla o el teclado para desplazarse por la DevTools, envíenos sus comentarios con un [Tweet][PostTweetEdgeDevTools] o haga clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b85d4-164">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="b85d4-165">[#963183][crbug963183] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-165">Chromium issue [#963183][crbug963183]</span></span>  

## <span data-ttu-id="b85d4-166">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-166">Announcements from the Chromium project</span></span>  

<span data-ttu-id="b85d4-167">En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 83 que se han contribuido al proyecto de código abierto.</span><span class="sxs-lookup"><span data-stu-id="b85d4-167">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="b85d4-168">Emular deficiencias de la visión</span><span class="sxs-lookup"><span data-stu-id="b85d4-168">Emulate vision deficiencies</span></span>   

<span data-ttu-id="b85d4-169">Abra la [pestaña representación][RenderingDoc] y use la nueva característica **emular deficiencias de Vision** para obtener una mejor idea de cómo las personas con diferentes tipos de deficiencias visuales experimentan su sitio.</span><span class="sxs-lookup"><span data-stu-id="b85d4-169">Open the [Rendering tab][RenderingDoc] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

> ##### <span data-ttu-id="b85d4-170">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="b85d4-170">Figure 9</span></span>  
> <span data-ttu-id="b85d4-171">Emular visión borrosa</span><span class="sxs-lookup"><span data-stu-id="b85d4-171">Emulating blurred vision</span></span>  
> ![Emular visión borrosa][ImageEmulatingBlurredVision]  

<span data-ttu-id="b85d4-173">DevTools es capaz de emular una visión borrosa y los siguientes [tipos de deficiencias de la visión del color][ColorBlindnessTypes].</span><span class="sxs-lookup"><span data-stu-id="b85d4-173">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="b85d4-174">Deficiencia de la visión del color</span><span class="sxs-lookup"><span data-stu-id="b85d4-174">Color Vision Deficiency</span></span> | <span data-ttu-id="b85d4-175">Detalles</span><span class="sxs-lookup"><span data-stu-id="b85d4-175">Details</span></span> |  
|:--- |:--- | 
| <span data-ttu-id="b85d4-176">Protanopia</span><span class="sxs-lookup"><span data-stu-id="b85d4-176">Protanopia</span></span> | <span data-ttu-id="b85d4-177">La incapacidad de percibir cualquier luz roja.</span><span class="sxs-lookup"><span data-stu-id="b85d4-177">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="b85d4-178">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="b85d4-178">Deuteranopia</span></span> | <span data-ttu-id="b85d4-179">La incapacidad de percibir cualquier luz verde.</span><span class="sxs-lookup"><span data-stu-id="b85d4-179">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="b85d4-180">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="b85d4-180">Tritanopia</span></span> | <span data-ttu-id="b85d4-181">La incapacidad de percibir cualquier luz azul.</span><span class="sxs-lookup"><span data-stu-id="b85d4-181">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="b85d4-182">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="b85d4-182">Achromatopsia</span></span> | <span data-ttu-id="b85d4-183">La incapacidad de percibir cualquier color, excepto tonos de gris \ (muy raro \).</span><span class="sxs-lookup"><span data-stu-id="b85d4-183">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> | 

<span data-ttu-id="b85d4-184">Existen versiones menos extremas de estas deficiencias de la visión del color y, de hecho, son más comunes.</span><span class="sxs-lookup"><span data-stu-id="b85d4-184">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>
<span data-ttu-id="b85d4-185">Por ejemplo, protanomaly es una sensibilidad reducida a la luz roja (a diferencia de Protanopia, que es la incapacidad completa de percibir la luz roja).</span><span class="sxs-lookup"><span data-stu-id="b85d4-185">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="b85d4-186">Sin embargo, estas deficiencias visuales de Omaly no están claramente definidas: todas las personas con dicha deficiencia visual son diferentes y pueden ver de manera diferente (pueden percibir más/menos los colores pertinentes).</span><span class="sxs-lookup"><span data-stu-id="b85d4-186">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>

<span data-ttu-id="b85d4-187">Al diseñar las simulaciones más extremas en DevTools, se garantiza que las aplicaciones web estarán accesibles para las personas con protanomaly, deuteranomaly, tritanomaly y achromatomaly también.</span><span class="sxs-lookup"><span data-stu-id="b85d4-187">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>

<span data-ttu-id="b85d4-188">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b85d4-188">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="b85d4-189">[#1003700][crbug1003700] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-189">Chromium issue [#1003700][crbug1003700]</span></span>  

### <span data-ttu-id="b85d4-190">Emular configuraciones regionales</span><span class="sxs-lookup"><span data-stu-id="b85d4-190">Emulate locales</span></span> 

<span data-ttu-id="b85d4-191">Para emular configuraciones regionales, configura una ubicación en la ubicación de los **sensores**  >  **Location**.</span><span class="sxs-lookup"><span data-stu-id="b85d4-191">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="b85d4-192">[Abrir el **menú de comandos** ][DevToolsCommandMenuIndex] y escribir `Sensors` para acceder a la ficha **sensores** . Después de realizar estas acciones, DevTools modifica la configuración regional predeterminada actual, lo que afecta a lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b85d4-192">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab. After performing these actions, DevTools modifies the current default locale, affecting the following:</span></span>

- `Intl.*` <span data-ttu-id="b85d4-193">API, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b85d4-193">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`
- <span data-ttu-id="b85d4-194">otras API de JavaScript que reconocen la configuración regional, como `String.prototype.localeCompare` y `*.prototype.toLocaleString` , por ejemplo:`123_456..toLocaleString()`</span><span class="sxs-lookup"><span data-stu-id="b85d4-194">other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example: `123_456..toLocaleString()`</span></span>
- <span data-ttu-id="b85d4-195">Las API de DOM, como `navigator.language` y</span><span class="sxs-lookup"><span data-stu-id="b85d4-195">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`
- <span data-ttu-id="b85d4-196">el [`Accept-Language`][MDNAcceptLanguage] encabezado de la solicitud http</span><span class="sxs-lookup"><span data-stu-id="b85d4-196">the [`Accept-Language`][MDNAcceptLanguage] HTTP request header</span></span>

> ##### <span data-ttu-id="b85d4-197">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="b85d4-197">Figure 10</span></span>  
> <span data-ttu-id="b85d4-198">Emular una configuración regional</span><span class="sxs-lookup"><span data-stu-id="b85d4-198">Emulating a locale</span></span>  
> ![Emular una configuración regional][ImageEmulatingLocales]  

<span data-ttu-id="b85d4-200">Para probar una demostración, consulta [ejemplo de código dependiente de la configuración regional][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="b85d4-200">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="b85d4-201">[#1051822][crbug1051822] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-201">Chromium issue [#1051822][crbug1051822]</span></span>

### <span data-ttu-id="b85d4-202">Política de Embedder entre orígenes \ (COEP \) depuración</span><span class="sxs-lookup"><span data-stu-id="b85d4-202">Cross-Origin Embedder Policy \(COEP\) debugging</span></span>   

<span data-ttu-id="b85d4-203">El panel red ahora proporciona información de depuración de [directivas de Embedder entre orígenes][COEP] .</span><span class="sxs-lookup"><span data-stu-id="b85d4-203">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="b85d4-204">La columna **Estado** ahora ofrece una explicación rápida del motivo por el que se bloqueó una solicitud, así como un vínculo para ver los encabezados de la solicitud para una mayor depuración:</span><span class="sxs-lookup"><span data-stu-id="b85d4-204">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

> ##### <span data-ttu-id="b85d4-205">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="b85d4-205">Figure 11</span></span>  
> <span data-ttu-id="b85d4-206">Solicitudes bloqueadas en la columna **Estado**</span><span class="sxs-lookup"><span data-stu-id="b85d4-206">Blocked requests in the **Status** column</span></span>  
> ![Solicitudes bloqueadas en la columna Estado][ImageNetworkStatus]  

<span data-ttu-id="b85d4-208">La sección de **encabezados de respuesta** de la pestaña **encabezados** proporciona más información sobre cómo resolver los problemas:</span><span class="sxs-lookup"><span data-stu-id="b85d4-208">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

> ##### <span data-ttu-id="b85d4-209">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="b85d4-209">Figure 12</span></span>  
> <span data-ttu-id="b85d4-210">Más información en la sección de encabezados de respuesta</span><span class="sxs-lookup"><span data-stu-id="b85d4-210">More guidance in the Response Headers section</span></span>  
> ![Más información en la sección de encabezados de respuesta][ImageNetworkGuidance]  

<span data-ttu-id="b85d4-212">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b85d4-212">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="b85d4-213">[#1051466][crbug1051466] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-213">Chromium issue [#1051466][crbug1051466]</span></span>  

### <span data-ttu-id="b85d4-214">Ver las solicitudes de red que establecen una ruta de cookie específica</span><span class="sxs-lookup"><span data-stu-id="b85d4-214">View network requests that set a specific cookie path</span></span> 

<span data-ttu-id="b85d4-215">Use la nueva `cookie-path` palabra clave de filtro en el panel **red** para centrarse en las solicitudes de red que establecen una [ruta de cookie][MDNCookiePath]específica.</span><span class="sxs-lookup"><span data-stu-id="b85d4-215">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>

<span data-ttu-id="b85d4-216">Desproteja las [solicitudes de filtro por propiedades][NetworkProperties] para descubrir más palabras clave como `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="b85d4-216">Check out [Filter requests by properties][NetworkProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="b85d4-217">**Acoplar a la izquierda** desde el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="b85d4-217">**Dock to left** from the Command Menu</span></span>   

<span data-ttu-id="b85d4-218">Abra el [menú de comandos][DevToolsCommandMenuIndex] y ejecute el `Dock to left` comando para mover DevTools a la izquierda de su ventanilla.</span><span class="sxs-lookup"><span data-stu-id="b85d4-218">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

> ##### <span data-ttu-id="b85d4-219">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="b85d4-219">Figure 13</span></span>  
> <span data-ttu-id="b85d4-220">DevTools acoplado a la izquierda de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="b85d4-220">DevTools docked to the left of the viewport</span></span>  
> ![DevTools acoplado a la izquierda de la ventanilla][ImageDockToLeft]  

> [!NOTE]
> <span data-ttu-id="b85d4-222">La característica **acoplar a la izquierda** ya está disponible desde Microsoft Edge 75, pero anteriormente solo se tenía acceso desde el [**menú principal**][MainMenuDoc].</span><span class="sxs-lookup"><span data-stu-id="b85d4-222">The **Dock to left** feature has been available since Microsoft Edge 75 but it was previously only accessible from the [**Main Menu**][MainMenuDoc].</span></span>  <span data-ttu-id="b85d4-223">La nueva característica de Microsoft Edge 83 es que ahora puede acceder a esta característica desde el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="b85d4-223">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="b85d4-224">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b85d4-224">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="b85d4-225">[#1011679][crbug1011679] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-225">Chromium issue [#1011679][crbug1011679]</span></span>  

### <span data-ttu-id="b85d4-226">El panel **auditorías** es ahora el panel de **Lighthouse**</span><span class="sxs-lookup"><span data-stu-id="b85d4-226">The **Audits** panel is now the **Lighthouse** panel</span></span>   

<span data-ttu-id="b85d4-227">El equipo DevTools con frecuencia recibe comentarios de los programadores de Internet que, aunque fuera posible ejecutar [Lighthouse][GithubGoogleChromeLighthouse] desde DevTools, cuando lo intentaron no podían encontrar el panel de la Lighthouse, por lo que el panel **auditorías** es ahora el panel de **Lighthouse** .</span><span class="sxs-lookup"><span data-stu-id="b85d4-227">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

> ##### <span data-ttu-id="b85d4-228">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="b85d4-228">Figure 14</span></span>  
> <span data-ttu-id="b85d4-229">El panel de Lighthouse</span><span class="sxs-lookup"><span data-stu-id="b85d4-229">The Lighthouse panel</span></span>  
> ![El panel de Lighthouse][ImageLighthouse]  

> [!NOTE]
> <span data-ttu-id="b85d4-231">El panel de **Lighthouse** proporciona vínculos a contenido hospedado en sitios web de terceros.</span><span class="sxs-lookup"><span data-stu-id="b85d4-231">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="b85d4-232">Microsoft no se responsabiliza y no tiene ningún control sobre el contenido de estos sitios y los datos que pueden recopilar.</span><span class="sxs-lookup"><span data-stu-id="b85d4-232">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="b85d4-233">Eliminar todos los reemplazos locales de una carpeta</span><span class="sxs-lookup"><span data-stu-id="b85d4-233">Delete all Local Overrides in a folder</span></span>   

<span data-ttu-id="b85d4-234">Después de configurar los **reemplazos locales** , puede hacer clic con el botón secundario del mouse en una carpeta y seleccionar la nueva opción **eliminar todas las sustituciones** para eliminar todos los reemplazos locales de esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="b85d4-234">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

> ##### <span data-ttu-id="b85d4-235">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="b85d4-235">Figure 15</span></span>  
> <span data-ttu-id="b85d4-236">Eliminar todas las invalidaciones</span><span class="sxs-lookup"><span data-stu-id="b85d4-236">Delete all overrides</span></span>  
> ![Eliminar todas las invalidaciones][ImageDeleteOverrides]  

<span data-ttu-id="b85d4-238">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b85d4-238">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="b85d4-239">[#1016501][crbug1016501] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-239">Chromium issue [#1016501][crbug1016501]</span></span>  

### <span data-ttu-id="b85d4-240">Interfaz de usuario de tareas largas actualizada</span><span class="sxs-lookup"><span data-stu-id="b85d4-240">Updated Long tasks UI</span></span>   

<span data-ttu-id="b85d4-241">Una **tarea larga** es código JavaScript que monopoliza el subproceso principal durante mucho tiempo, lo que provoca la inmovilización de una página web.</span><span class="sxs-lookup"><span data-stu-id="b85d4-241">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="b85d4-242">Ya ha podido [visualizar tareas largas en el panel rendimiento][LongTasksInPerformancePanel] por un momento, pero en Microsoft Edge 83 se ha actualizado la interfaz de usuario de visualización de tareas largas en el panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b85d4-242">You have been able to [visualize Long Tasks in the Performance panel][LongTasksInPerformancePanel] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="b85d4-243">La parte de tarea larga de una tarea ahora está coloreada con un fondo con bandas de color rojo.</span><span class="sxs-lookup"><span data-stu-id="b85d4-243">The Long Task portion of a task is now colored with a striped red background.</span></span>  

> ##### <span data-ttu-id="b85d4-244">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="b85d4-244">Figure 16</span></span>  
> <span data-ttu-id="b85d4-245">La nueva interfaz de usuario de tareas largas</span><span class="sxs-lookup"><span data-stu-id="b85d4-245">The new Long Task UI</span></span>  
> ![La nueva interfaz de usuario de tareas largas][ImageLongTask]  

<span data-ttu-id="b85d4-247">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono de [comentarios](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="b85d4-247">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="b85d4-248">[#1054447][crbug1054447] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="b85d4-248">Chromium issue [#1054447][crbug1054447]</span></span>  

### <span data-ttu-id="b85d4-249">Compatibilidad con el icono enmascarable en el panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="b85d4-249">Maskable icon support in the Manifest pane</span></span>   

<span data-ttu-id="b85d4-250">Android Oreo presentó iconos adaptables, que muestran los iconos de la aplicación en una variedad de formas en diferentes modelos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="b85d4-250">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="b85d4-251">Los **iconos Enmascarables** son un nuevo formato de icono que admite iconos adaptables, que le permiten asegurarse de que el icono de [PWA][PWADoc] se ve bien en los dispositivos que admiten el estándar de iconos Enmascarables.</span><span class="sxs-lookup"><span data-stu-id="b85d4-251">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PWADoc] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="b85d4-252">Active la casilla nuevo **Mostrar solo el área mínima segura para los iconos Enmascarables** en el panel **manifiesto** para comprobar que el icono enmascarable es adecuado en dispositivos Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="b85d4-252">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

> ##### <span data-ttu-id="b85d4-253">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="b85d4-253">Figure 17</span></span>  
> <span data-ttu-id="b85d4-254">La casilla "Mostrar solo el área mínima segura para los iconos Enmascarables"</span><span class="sxs-lookup"><span data-stu-id="b85d4-254">The "Show only the minimum safe area for maskable icons" checkbox</span></span>  
> ![La casilla "Mostrar solo el área mínima segura para los iconos Enmascarables"][ImageMaskableIcons]  

> [!NOTE]
> <span data-ttu-id="b85d4-256">Esta característica se inició en Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="b85d4-256">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="b85d4-257">Las actualizaciones descritas aquí en Microsoft Edge 83 no se cubren en [novedades de DevTools (Microsoft edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="b85d4-257">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="b85d4-258">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b85d4-258">Feedback</span></span>   

  

<span data-ttu-id="b85d4-259">Para comentar las nuevas características y cambios de esta publicación, o cualquier otro tema relacionado con DevTools:</span><span class="sxs-lookup"><span data-stu-id="b85d4-259">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="b85d4-260">Envíe sus comentarios con el icono de **comentarios** en el DevTools</span><span class="sxs-lookup"><span data-stu-id="b85d4-260">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
*   <span data-ttu-id="b85d4-261">Tweet a [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="b85d4-261">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="b85d4-262">Enviar una sugerencia a [la web][TheWebWeWant] que queremos</span><span class="sxs-lookup"><span data-stu-id="b85d4-262">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="b85d4-263">Archivar errores en este documento en el repositorio [Edge-desarrollador][GitHubMicrosoftDocsEdgeDeveloperNewIssue]</span><span class="sxs-lookup"><span data-stu-id="b85d4-263">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

> ##### <span data-ttu-id="b85d4-264">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="b85d4-264">Figure 18</span></span>  
> <span data-ttu-id="b85d4-265">El icono de **comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b85d4-265">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![El icono \* \* comentarios \* \* en Microsoft Edge DevTools][ImageFeedbackIcon]  

## <span data-ttu-id="b85d4-267">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="b85d4-267">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="b85d4-268">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b85d4-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="b85d4-269">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b85d4-269">The preview channels give you access to the latest DevTools features.</span></span>  

<!-- <<../../_shared/devtools-feedback.md>>

<<../../_shared/canary.md>>

<<../../_shared/discover.md>> -->

  

<!-- image links -->  

[ImageRemoteTools]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/remote-tools.msft.png "Ilustración 1: aplicación de herramientas remotas para Microsoft Edge (beta) disponible en Microsoft Store"  
[ImageSettingsGearIcon]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/settings.msft.png "Ilustración 2: el icono de engranaje abre la configuración en el DevTools"
[ImageSettingsMainMenu]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/settings2.msft.png "Ilustración 3: menú principal > más herramientas > configuración"
[ImageInfobar]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/infobar.msft.png "Ilustración 4: barra de barra para imprimir un archivo minified en Microsoft Edge 83"
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/color-picker.msft.png "Ilustración 5: ahora puede usar el teclado para mover el selector en la sección sombras del selector de colores."  
[ImagePropertiesIn81]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/properties-in-81.msft.png "Ilustración 6: en Microsoft Edge 81 y versiones anteriores, la pestaña propiedades estaba en blanco después de actualizar una página"  
[ImagePropertiesIn82]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/properties-in-82.msft.png "Ilustración 7: en Microsoft Edge 83, la pestaña propiedades muestra las propiedades del elemento seleccionado actualmente después de actualizar una página."  
[ImageChanges]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/changes.msft.png "Ilustración 8: en Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de dirección para ver el código de minified en la herramienta de cambios"  
[ImageEmulatingBlurredVision]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/vision.msft.png "Ilustración 9: emular una visión borrosa"  
[ImageEmulatingLocales]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/locale.msft.png "Ilustración 10: emular una configuración regional"
[ImageNetworkStatus]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/status.msft.png "Ilustración 11: solicitudes bloqueadas en la columna Estado"  
[ImageNetworkGuidance]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/guidance.msft.png "Ilustración 12: más instrucciones en la sección de encabezados de respuesta"  
[ImageDockToLeft]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/dock-to-left.msft.png "Ilustración 13: DevTools acoplado a la izquierda de la ventanilla"  
[ImageLighthouse]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/lighthouse.msft.png "Ilustración 14: el panel de Lighthouse"  
[ImageDeleteOverrides]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/overrides.msft.png "Ilustración 15: eliminar todas las invalidaciones"  
[ImageLongTask]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/long-task.msft.png "Ilustración 16: la nueva interfaz de usuario de tareas largas"  
[ImageMaskableIcons]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/maskable-icons.msft.png "Ilustración 17: la casilla Mostrar solo el área mínima segura para los iconos Enmascarables"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/feedback-icon.msft.png "Ilustración 18: el icono de comentarios en el Microsoft Edge DevTools"  

[ImageLineOfCodeBreakpoint]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/breakpoint.msft.png
[ImageLogpoint]: /microsoft-edge/devtools-guide-chromium/whats-new/images/2020/03/logpoint.msft.png

<!-- links -->  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de Microsoft Edge Preview"  
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"  

[WhatsNew81]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/01/devtools "Novedades de DevTools (Microsoft Edge 81)"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[ColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambiar los colores con el selector de colores"  
[ElementsDoc]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS"  
[MainMenuDoc]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Cambiar la ubicación desde el menú principal"  
[LongTasksInPerformancePanel]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Ver actividad de subproceso principal"  
[RenderingDoc]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de la representación con la pestaña representación"  
[PWADoc]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows"  
[RemoteDebuggingWin10]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota dispositivos con Windows 10"  
[LineOfCodeBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Puntos de interrupción de línea de código"
[NetworkProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties
[OverviewSettings]: /microsoft-edge/devtools-guide-chromium/customize/#settings

[WindowsDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Información general de Windows Device portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Herramientas remotas para Microsoft Edge (beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  
[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/ "Actualizar en las versiones de canal estable para Microsoft Edge"

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness/ "Tipos de daltonismo"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Ejemplo de código dependiente de la configuración regional"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[crbug963183]: https://crbug.com/963183 "Problema 963183: DevTools no son compatibles con WCAG"  
[crbug1003700]: https://crbug.com/1003700 "Problema 1003700: agregar compatibilidad DevTools para simulación de deficiencias de la visión del color"  
[crbug1011679]: https://crbug.com/1011679 "Problema 1011679: presentar ' acoplar a la izquierda ' con el menú de comandos"  
[crbug1016501]: https://crbug.com/1016501 "Problema 1016501: solicitud de característica: botón para eliminar todos los reemplazos locales"  
[crbug1050999]: https://crbug.com/1050999 "Problema 1050999: ficha Propiedades"  
[crbug1051466]: https://crbug.com/1051466 "Problema 1051466: compatibilidad con COOP/depuración de COEP en DevTools"  
[crbug1054447]: https://crbug.com/1054447 "Problema 1054447: actualizar las métricas de rendimiento en la escala de tiempo de DevTools"  
[crbug1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: agregar una interfaz de usuario para emular la configuración regional"
[crbug1041830]: https://crbug.com/1041830 "Problema 1041830: mejorar los colores de los puntos de interrupción"
[crbug1050855]: https://crbug.com/1050855 "Problema 1050855: la vista de configuración es difícil de detectar"
[crbug1056348]: https://crbug.com/1056348 "Problema 1056348: actualización de componentes de barra de error"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Explicación de COOP y COEP explicado: política de apertura entre orígenes cruzados"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Normas de COOP y COEP explicadas: política de Embedder de origen cruzado"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Repositorio de GitHub Lighthouse"  

> [!NOTE]
> <span data-ttu-id="b85d4-324">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b85d4-324">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b85d4-325">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/03/devtools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b85d4-325">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b85d4-327">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b85d4-327">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
