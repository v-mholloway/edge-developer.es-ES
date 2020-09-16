---
description: Emular las deficiencias de la visión del color, acoplar a la izquierda en el menú de comandos y mucho más.
title: Novedades de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f9eb306ab7b30495c91ff4a70797898459d7e722
ms.sourcegitcommit: b337717957529239434b4e8e1e167aebf0543518
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015485"
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

# <span data-ttu-id="fc038-104">Novedades de DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="fc038-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="fc038-105">Después de la programación de cromo actualizada, estamos ajustando nuestra programación para las próximas versiones de Microsoft Edge y cancelando la versión 82 de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fc038-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="fc038-106">Para obtener más información, consulta nuestra [entrada de blog][WindowsBlogStableRelease] .</span><span class="sxs-lookup"><span data-stu-id="fc038-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="fc038-107">Estas son las nuevas características disponibles en el DevTools en Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="fc038-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <span data-ttu-id="fc038-108">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fc038-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="fc038-109">Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fc038-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="fc038-110">Compruébelos para probar nuevas características en DevTools, Visual Studio Code Extensions y mucho más.</span><span class="sxs-lookup"><span data-stu-id="fc038-110">Check them out to try new features in the DevTools, Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="fc038-111">Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="fc038-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="fc038-112">Depurar Microsoft Edge de forma remota en dispositivos con Windows 10</span><span class="sxs-lookup"><span data-stu-id="fc038-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="fc038-113">La aplicación [de herramientas remotas para Microsoft Edge \ (beta \)][RemoteTools] ya está disponible en [Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="fc038-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="fc038-114">Con esta aplicación, que extiende [Windows Device portal][WindowsUwpDebugTestPerfDevicePortal], podrás conectarte desde la instancia de Microsoft Edge que se ejecuta en el equipo de desarrollo a un dispositivo de Windows 10 remoto, ver una lista de destinos \ (todas las pestañas de Microsoft Edge y [PWAs][PprgressiveWebAppsChromiumIndex] abiertas en el dispositivo Windows 10) y usar el DevTools en el equipo de desarrollo con un destino que se ejecute en el dispositivo remoto</span><span class="sxs-lookup"><span data-stu-id="fc038-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, see a list of targets \(all tabs in Microsoft Edge and [PWAs][PprgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="La aplicación de herramientas remotas para Microsoft Edge (beta) disponible en Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="fc038-116">La aplicación de [herramientas remotas para Microsoft Edge (beta)][RemoteTools] disponible en [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="fc038-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-117">[Lea nuestra guía para configurar su dispositivo Windows 10 y su equipo de desarrollo para la depuración remota][DevtoolsRemoteDebuggingWindows].</span><span class="sxs-lookup"><span data-stu-id="fc038-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="fc038-118">Para informarnos sobre la experiencia de depuración remota, haga [clic en el][PostTweetEdgeDevTools] icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="fc038-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <span data-ttu-id="fc038-119">Nuevas formas de obtener acceso a la configuración</span><span class="sxs-lookup"><span data-stu-id="fc038-119">New ways to access Settings</span></span>  

<span data-ttu-id="fc038-120">Hay toneladas de opciones de configuración para el DevTools que puede personalizar para DevTools la apariencia y el funcionamiento de la manera que necesita.</span><span class="sxs-lookup"><span data-stu-id="fc038-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="fc038-121">En Microsoft Edge 83, obtener acceso a la [configuración][DevtoolsCustomizeIndexSettings] de la DevTools es ahora mucho más fácil.</span><span class="sxs-lookup"><span data-stu-id="fc038-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span> <span data-ttu-id="fc038-122">Abra configuración con el icono de engranaje junto a alertas de consola y el menú principal.</span><span class="sxs-lookup"><span data-stu-id="fc038-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="El icono de engranaje abre la configuración en el DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="fc038-124">El icono de engranaje abre la **configuración** en el DevTools</span><span class="sxs-lookup"><span data-stu-id="fc038-124">The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-125">También puede abrir la [configuración][DevtoolsCustomizeIndexSettings] desde el **menú principal** , en **más herramientas**.</span><span class="sxs-lookup"><span data-stu-id="fc038-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menú principal > más herramientas > configuración" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="fc038-127">**Menú principal**  >  **Más herramientas**  >  **Configuración**</span><span class="sxs-lookup"><span data-stu-id="fc038-127">**Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-128">[#1050855][CR1050855] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-128">Chromium issue [#1050855][CR1050855]</span></span>

### <span data-ttu-id="fc038-129">Infobars nuevos y mejorados</span><span class="sxs-lookup"><span data-stu-id="fc038-129">New and improved infobars</span></span>

<span data-ttu-id="fc038-130">Las barras de notificación informativas \ (infobars \) en DevTools ahora tienen un aspecto mejorado y una mayor funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fc038-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="fc038-131">En Microsoft Edge 83, infobars son más fáciles de leer y proporcionan botones para que puedas llevar a cabo la acción pertinente de inmediato.</span><span class="sxs-lookup"><span data-stu-id="fc038-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barra de barra para imprimir un archivo minified en Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="fc038-133">Barra de barra para imprimir un archivo minified en Microsoft Edge versión 83</span><span class="sxs-lookup"><span data-stu-id="fc038-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-134">[#1056348][CR1056348] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-134">Chromium issue [#1056348][CR1056348]</span></span>

### <span data-ttu-id="fc038-135">Navegar por el selector de colores con el teclado</span><span class="sxs-lookup"><span data-stu-id="fc038-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="fc038-136">El [selector de colores][DevtoolsCssReferenceColorPicker] es una GUI en el [Panel elementos][DevtoolsCssIndex] para el cambio `color` y las `background-color` declaraciones.</span><span class="sxs-lookup"><span data-stu-id="fc038-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="fc038-137">En versiones anteriores de Microsoft Edge, no se podía navegar por la sección **sombras** del selector de [colores][DevtoolsCssReferenceColorPicker] con el teclado.</span><span class="sxs-lookup"><span data-stu-id="fc038-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Ahora puede usar el teclado para mover el selector en la sección sombras del selector de colores." lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="fc038-139">Ahora puede usar el teclado para mover el selector en la sección **sombras** del [selector de colores][DevtoolsCssReferenceColorPicker] .</span><span class="sxs-lookup"><span data-stu-id="fc038-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-140">En Microsoft Edge 83, ahora puede usar el teclado para mover el selector en la sección **sombras** del selector de colores.</span><span class="sxs-lookup"><span data-stu-id="fc038-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="fc038-141">[#963183][CR963183] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-141">Chromium issue [#963183][CR963183]</span></span>  

### <span data-ttu-id="fc038-142">La pestaña propiedades ahora se rellena después de actualizar una página</span><span class="sxs-lookup"><span data-stu-id="fc038-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="fc038-143">En Microsoft Edge 81 y versiones anteriores, la **pestaña propiedades** del [Panel elementos][DevtoolsCssIndex] se interrumpió por actualizaciones de página.</span><span class="sxs-lookup"><span data-stu-id="fc038-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="fc038-144">Cuando ha actualizado la página, la **pestaña propiedades** no ha rellenado las propiedades del elemento seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="fc038-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="En Microsoft Edge 81 y versiones anteriores, la pestaña propiedades estaba en blanco después de actualizar una página" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="fc038-146">En Microsoft Edge 81 y versiones anteriores, la **pestaña propiedades** estaba en blanco después de actualizar una página</span><span class="sxs-lookup"><span data-stu-id="fc038-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-147">En Microsoft Edge 83, ahora puede ver las propiedades del elemento seleccionado en ese momento después de actualizar una página en la **pestaña propiedades**.</span><span class="sxs-lookup"><span data-stu-id="fc038-147">In Microsoft Edge 83, you are now able to see the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="En Microsoft Edge 83, la pestaña propiedades muestra las propiedades del elemento seleccionado actualmente después de actualizar una página." lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="fc038-149">En Microsoft Edge 83, la **pestaña propiedades** muestra las propiedades del elemento seleccionado actualmente después de actualizar una página.</span><span class="sxs-lookup"><span data-stu-id="fc038-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-150">[#1050999][CR1050999] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <span data-ttu-id="fc038-151">Use las teclas de dirección para desplazarse por la herramienta de cambios</span><span class="sxs-lookup"><span data-stu-id="fc038-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="fc038-152">La **herramienta cambios** realiza un seguimiento de los cambios realizados en CSS o JavaScript en el DevTools.</span><span class="sxs-lookup"><span data-stu-id="fc038-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="fc038-153">Puede usar la **herramienta cambios** para ver rápidamente todos los cambios y recuperarlos en el editor o IDE.</span><span class="sxs-lookup"><span data-stu-id="fc038-153">You are able to use the **Changes tool** to quickly see all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="fc038-154">Para abrir la **herramienta de cambios** , pulsa `Ctrl` + `Shift` + `P` en el DevTools para abrir el menú de [comandos][DevToolsCommandMenuIndex] y escribir `changes` .</span><span class="sxs-lookup"><span data-stu-id="fc038-154">Open the **Changes tool** by pressing `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and typing `changes`.</span></span>  <span data-ttu-id="fc038-155">Seleccione y ejecute el comando **Mostrar cambios** para abrir la **herramienta de cambios** del alimentador de DevTools.</span><span class="sxs-lookup"><span data-stu-id="fc038-155">Select and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="fc038-156">Una vez que haya realizado un cambio en un archivo minified, la **herramienta cambios** le permitirá desplazarse horizontalmente para ver todo el código minified.</span><span class="sxs-lookup"><span data-stu-id="fc038-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to see all of your minified code.</span></span>  <span data-ttu-id="fc038-157">A partir de Microsoft Edge 83, ahora puede desplazarse horizontalmente con las teclas de dirección del teclado.</span><span class="sxs-lookup"><span data-stu-id="fc038-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de dirección para ver el código de minified en la herramienta de cambios" lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="fc038-159">En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de dirección para ver los cambios que realizó en el código de minified en la **herramienta de cambios**</span><span class="sxs-lookup"><span data-stu-id="fc038-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to see the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-160">Si usa lectores de pantalla o el teclado para desplazarse por la DevTools, envíenos sus comentarios con un [Tweet][PostTweetEdgeDevTools] o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="fc038-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="fc038-161">[#963183][CR963183] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-161">Chromium issue [#963183][CR963183]</span></span>  

## <span data-ttu-id="fc038-162">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="fc038-163">En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 83 que se han contribuido al proyecto de código abierto.</span><span class="sxs-lookup"><span data-stu-id="fc038-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="fc038-164">Emular deficiencias de la visión</span><span class="sxs-lookup"><span data-stu-id="fc038-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="fc038-165">Abra la [pestaña representación][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] y use la nueva característica **emular deficiencias de Vision** para obtener una mejor idea de cómo las personas con diferentes tipos de deficiencias visuales experimentan su sitio.</span><span class="sxs-lookup"><span data-stu-id="fc038-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emular visión borrosa" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="fc038-167">Emular visión borrosa</span><span class="sxs-lookup"><span data-stu-id="fc038-167">Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-168">DevTools es capaz de emular una visión borrosa y los siguientes [tipos de deficiencias de la visión del color][ColorBlindnessTypes].</span><span class="sxs-lookup"><span data-stu-id="fc038-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="fc038-169">Deficiencia de la visión del color</span><span class="sxs-lookup"><span data-stu-id="fc038-169">Color Vision Deficiency</span></span> | <span data-ttu-id="fc038-170">Detalles</span><span class="sxs-lookup"><span data-stu-id="fc038-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="fc038-171">Protanopia</span><span class="sxs-lookup"><span data-stu-id="fc038-171">Protanopia</span></span> | <span data-ttu-id="fc038-172">La incapacidad de percibir cualquier luz roja.</span><span class="sxs-lookup"><span data-stu-id="fc038-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="fc038-173">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="fc038-173">Deuteranopia</span></span> | <span data-ttu-id="fc038-174">La incapacidad de percibir cualquier luz verde.</span><span class="sxs-lookup"><span data-stu-id="fc038-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="fc038-175">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="fc038-175">Tritanopia</span></span> | <span data-ttu-id="fc038-176">La incapacidad de percibir cualquier luz azul.</span><span class="sxs-lookup"><span data-stu-id="fc038-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="fc038-177">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="fc038-177">Achromatopsia</span></span> | <span data-ttu-id="fc038-178">La incapacidad de percibir cualquier color, excepto tonos de gris \ (muy raro \).</span><span class="sxs-lookup"><span data-stu-id="fc038-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="fc038-179">Existen versiones menos extremas de estas deficiencias de la visión del color y, de hecho, son más comunes.</span><span class="sxs-lookup"><span data-stu-id="fc038-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="fc038-180">Por ejemplo, protanomaly es una sensibilidad reducida a la luz roja (a diferencia de Protanopia, que es la incapacidad completa de percibir la luz roja).</span><span class="sxs-lookup"><span data-stu-id="fc038-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="fc038-181">Sin embargo, estas deficiencias visuales de Omaly no están claramente definidas: todas las personas con dicha deficiencia visual son diferentes y pueden ver de manera diferente (pueden percibir más/menos los colores pertinentes).</span><span class="sxs-lookup"><span data-stu-id="fc038-181">However, these -omaly vision deficiencies are not as clearly defined: every person with such a vision deficiency is different and might see things differently (being able to perceive more/less of the relevant colors).</span></span>  

<span data-ttu-id="fc038-182">Al diseñar las simulaciones más extremas en DevTools, se garantiza que las aplicaciones web estarán accesibles para las personas con protanomaly, deuteranomaly, tritanomaly y achromatomaly también.</span><span class="sxs-lookup"><span data-stu-id="fc038-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="fc038-183">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="fc038-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="fc038-184">[#1003700][CR1003700] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <span data-ttu-id="fc038-185">Emular configuraciones regionales</span><span class="sxs-lookup"><span data-stu-id="fc038-185">Emulate locales</span></span>  

<span data-ttu-id="fc038-186">Para emular configuraciones regionales, configura una ubicación en la ubicación de los **sensores**  >  **Location**.</span><span class="sxs-lookup"><span data-stu-id="fc038-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="fc038-187">[Abrir el **menú de comandos** ][DevToolsCommandMenuIndex] y escribir `Sensors` para acceder a la ficha **sensores** .  Después de realizar estas acciones, DevTools modifica la configuración regional predeterminada actual, lo que afecta al siguiente código.</span><span class="sxs-lookup"><span data-stu-id="fc038-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="fc038-188">API, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fc038-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="fc038-189">Otras API de JavaScript que reconocen la configuración regional, como `String.prototype.localeCompare` y `*.prototype.toLocaleString` , por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fc038-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="fc038-190">Las API de DOM, como `navigator.language` y</span><span class="sxs-lookup"><span data-stu-id="fc038-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="fc038-191">Encabezado [de solicitud HTTP Accept-Language][MDNAcceptLanguage]</span><span class="sxs-lookup"><span data-stu-id="fc038-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="fc038-192">Actualizaciones de `navigator.language` y `navigator.languages` no visibles inmediatamente, pero solo después de la siguiente navegación o actualización de la página.</span><span class="sxs-lookup"><span data-stu-id="fc038-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="fc038-193">Los cambios en el `Accept-Language` encabezado HTTP solo se reflejan en solicitudes posteriores.</span><span class="sxs-lookup"><span data-stu-id="fc038-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emular una configuración regional" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="fc038-195">Emular una configuración regional</span><span class="sxs-lookup"><span data-stu-id="fc038-195">Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-196">Para probar una demostración, consulta [ejemplo de código dependiente de la configuración regional][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="fc038-196">To try a demo, see [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="fc038-197">[#1051822][CR1051822] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-197">Chromium issue [#1051822][CR1051822]</span></span>

### <span data-ttu-id="fc038-198">Depuración de directivas de Embedder entre orígenes (COEP)</span><span class="sxs-lookup"><span data-stu-id="fc038-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="fc038-199">El panel red ahora proporciona información de depuración de [directivas de Embedder entre orígenes][COEP] .</span><span class="sxs-lookup"><span data-stu-id="fc038-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="fc038-200">La columna **Estado** ahora ofrece una explicación rápida del motivo por el que se bloqueó una solicitud, así como un vínculo para ver los encabezados de la solicitud para una mayor depuración:</span><span class="sxs-lookup"><span data-stu-id="fc038-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Solicitudes bloqueadas en la columna \* \* Estado \* \*" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="fc038-202">Solicitudes bloqueadas en la columna **Estado**</span><span class="sxs-lookup"><span data-stu-id="fc038-202">Blocked requests in the **Status** column</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-203">La sección de **encabezados de respuesta** de la pestaña **encabezados** proporciona más información sobre cómo resolver los problemas:</span><span class="sxs-lookup"><span data-stu-id="fc038-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Más información en la sección de encabezados de respuesta" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="fc038-205">Más información en la sección de **encabezados de respuesta**</span><span class="sxs-lookup"><span data-stu-id="fc038-205">More guidance in the **Response Headers** section</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-206">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="fc038-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="fc038-207">[#1051466][CR1051466] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <span data-ttu-id="fc038-208">Nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y logpoints</span><span class="sxs-lookup"><span data-stu-id="fc038-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="fc038-209">El panel orígenes tiene nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y logpoints:</span><span class="sxs-lookup"><span data-stu-id="fc038-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="fc038-210">Puntos de interrupción \ (</span><span class="sxs-lookup"><span data-stu-id="fc038-210">Breakpoints \(</span></span>![Punto](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="fc038-212">\) se representan mediante círculos rojos.</span><span class="sxs-lookup"><span data-stu-id="fc038-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="fc038-213">Puntos de interrupción condicionales \ (</span><span class="sxs-lookup"><span data-stu-id="fc038-213">Conditional Breakpoints \(</span></span>![Punto de interrupción condicional](../../media/2020/03/conditional.msft.png)<span data-ttu-id="fc038-215">\) se representan mediante círculos de doble cara de color rojo.</span><span class="sxs-lookup"><span data-stu-id="fc038-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="fc038-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="fc038-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="fc038-218">\) se representan mediante círculos rojos con iconos de consola.</span><span class="sxs-lookup"><span data-stu-id="fc038-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="fc038-219">El motivo por el que los nuevos iconos era hacer que la interfaz de usuario sea más coherente con otras herramientas de depuración de GUI \ (que suelen tener puntos de interrupción de color rojo \) y para que sea más fácil distinguir las tres características de un vistazo.</span><span class="sxs-lookup"><span data-stu-id="fc038-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="fc038-220">[#1041830][CR1041830] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <span data-ttu-id="fc038-221">Ver las solicitudes de red que establecen una ruta de cookie específica</span><span class="sxs-lookup"><span data-stu-id="fc038-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="fc038-222">Use la nueva `cookie-path` palabra clave de filtro en el panel **red** para centrarse en las solicitudes de red que establecen una [ruta de cookie][MDNCookiePath]específica.</span><span class="sxs-lookup"><span data-stu-id="fc038-222">Use the new `cookie-path` filter keyword in the **Network** panel to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="fc038-223">Desproteja las [solicitudes de filtro por propiedades][DevtoolsNetworkReferenceFilterRequestsProperties] para descubrir más palabras clave como `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="fc038-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <span data-ttu-id="fc038-224">Acoplar a la izquierda desde el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="fc038-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="fc038-225">Abra el [menú de comandos][DevToolsCommandMenuIndex] y ejecute el `Dock to left` comando para mover DevTools a la izquierda de su ventanilla.</span><span class="sxs-lookup"><span data-stu-id="fc038-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools acoplado a la izquierda de la ventanilla" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="fc038-227">DevTools acoplado a la izquierda de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="fc038-227">DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="fc038-228">La característica **acoplar a la izquierda** está disponible desde el 75 de Microsoft Edge, pero anteriormente solo era posible acceder a ella desde el [menú principal][DevtoolsCustomizePlacementsChangeMainMenu].</span><span class="sxs-lookup"><span data-stu-id="fc038-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="fc038-229">La nueva característica de Microsoft Edge 83 es que ahora puede acceder a esta característica desde el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="fc038-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="fc038-230">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="fc038-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="fc038-231">[#1011679][CR1011679] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <span data-ttu-id="fc038-232">El panel auditorías es ahora el panel de Lighthouse</span><span class="sxs-lookup"><span data-stu-id="fc038-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="fc038-233">El equipo DevTools con frecuencia recibe comentarios de los programadores de Internet que, aunque fuera posible ejecutar [Lighthouse][GithubGoogleChromeLighthouse] desde DevTools, cuando lo intentaron no podían encontrar el panel de la Lighthouse, por lo que el panel **auditorías** es ahora el panel de **Lighthouse** .</span><span class="sxs-lookup"><span data-stu-id="fc038-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="El panel de Lighthouse" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="fc038-235">El panel de Lighthouse</span><span class="sxs-lookup"><span data-stu-id="fc038-235">The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="fc038-236">El panel de **Lighthouse** proporciona vínculos a contenido hospedado en sitios web de terceros.</span><span class="sxs-lookup"><span data-stu-id="fc038-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="fc038-237">Microsoft no se responsabiliza y no tiene ningún control sobre el contenido de estos sitios y los datos que pueden recopilar.</span><span class="sxs-lookup"><span data-stu-id="fc038-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <span data-ttu-id="fc038-238">Eliminar todos los reemplazos locales de una carpeta</span><span class="sxs-lookup"><span data-stu-id="fc038-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="fc038-239">Después de configurar los **reemplazos locales** , puede hacer clic con el botón secundario del mouse en una carpeta y seleccionar la nueva opción **eliminar todas las sustituciones** para eliminar todos los reemplazos locales de esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="fc038-239">After setting up **Local Overrides** you may right-click a folder and select the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Eliminar todas las invalidaciones" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="fc038-241">Eliminar todas las invalidaciones</span><span class="sxs-lookup"><span data-stu-id="fc038-241">Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-242">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="fc038-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="fc038-243">[#1016501][CR1016501] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <span data-ttu-id="fc038-244">Interfaz de usuario de tareas largas actualizada</span><span class="sxs-lookup"><span data-stu-id="fc038-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="fc038-245">Una **tarea larga** es código JavaScript que monopoliza el subproceso principal durante mucho tiempo, lo que provoca la inmovilización de una página web.</span><span class="sxs-lookup"><span data-stu-id="fc038-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="fc038-246">Ya ha podido [visualizar tareas largas en el panel rendimiento][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] por un momento, pero en Microsoft Edge 83 se ha actualizado la interfaz de usuario de visualización de tareas largas en el panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="fc038-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="fc038-247">La parte de tarea larga de una tarea ahora está coloreada con un fondo con bandas de color rojo.</span><span class="sxs-lookup"><span data-stu-id="fc038-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="La nueva interfaz de usuario de tareas largas" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="fc038-249">La nueva interfaz de usuario de tareas largas</span><span class="sxs-lookup"><span data-stu-id="fc038-249">The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="fc038-250">Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="fc038-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="fc038-251">[#1054447][CR1054447] de problemas de cromo</span><span class="sxs-lookup"><span data-stu-id="fc038-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <span data-ttu-id="fc038-252">Compatibilidad con el icono enmascarable en el panel manifiesto</span><span class="sxs-lookup"><span data-stu-id="fc038-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="fc038-253">Android Oreo presentó iconos adaptables, que muestran los iconos de la aplicación en una variedad de formas en diferentes modelos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fc038-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="fc038-254">Los **iconos Enmascarables** son un nuevo formato de icono que admite iconos adaptables, que le permiten asegurarse de que el icono de [PWA][PprgressiveWebAppsChromiumIndex] se ve bien en los dispositivos que admiten el estándar de iconos Enmascarables.</span><span class="sxs-lookup"><span data-stu-id="fc038-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][PprgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="fc038-255">Active la casilla nuevo **Mostrar solo el área mínima segura para los iconos Enmascarables** en el panel **manifiesto** para comprobar que el icono enmascarable es adecuado en dispositivos Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="fc038-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Casilla Mostrar solo el área de seguridad mínima para los iconos Enmascarables" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="fc038-257">La casilla **Mostrar solo el área de seguridad mínima para iconos Enmascarables**</span><span class="sxs-lookup"><span data-stu-id="fc038-257">The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="fc038-258">Esta característica se inició en Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="fc038-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="fc038-259">Las actualizaciones descritas aquí en Microsoft Edge 83 no se cubren en [novedades de DevTools (Microsoft edge 81)][WhatsNew81].</span><span class="sxs-lookup"><span data-stu-id="fc038-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <span data-ttu-id="fc038-260">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="fc038-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="fc038-261">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fc038-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="fc038-262">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="fc038-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="fc038-263">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fc038-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Novedades de DevTools (Microsoft Edge 81) | Microsoft docs"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambiar colores con el selector de colores | Microsoft docs"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Cambiar la ubicación desde el menú principal | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Ver actividad de subproceso principal | Microsoft docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de la representación con la ficha representación | Microsoft docs"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft docs"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota dispositivos con Windows 10 | Microsoft docs"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Puntos de interrupción de línea de código: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft docs"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrar solicitudes por propiedades-referencia de análisis de red | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Información general de Windows Device portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Herramientas remotas para Microsoft Edge (beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de Microsoft Edge Preview"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Actualizar en las versiones de canal estable para Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/Edge-Developer-GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  
[TheWebWeWant]: https://webwewant.fyi "La web que queremos"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Tipos de daltonismo"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Aceptar-idioma | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Ejemplo de código dependiente de la configuración regional"  

[CR963183]: https://crbug.com/963183 "Problema 963183: DevTools no son compatibles con WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problema 1003700: agregar compatibilidad DevTools para simulación de deficiencias de la visión del color"  
[CR1011679]: https://crbug.com/1011679 "Problema 1011679: presentar ' acoplar a la izquierda ' con el menú de comandos"  
[CR1016501]: https://crbug.com/1016501 "Problema 1016501: solicitud de característica: botón para eliminar todos los reemplazos locales"  
[CR1050999]: https://crbug.com/1050999 "Problema 1050999: ficha Propiedades"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: compatibilidad con COOP/depuración de COEP en DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problema 1054447: actualizar las métricas de rendimiento en la escala de tiempo de DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: agregar una interfaz de usuario para emular la configuración regional"
[CR1041830]: https://crbug.com/1041830 "Problema 1041830: mejorar los colores de los puntos de interrupción"
[CR1050855]: https://crbug.com/1050855 "Problema 1050855: la vista de configuración es difícil de detectar"
[CR1056348]: https://crbug.com/1056348 "Problema 1056348: actualización de componentes de barra de error"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Explicación de COOP y COEP explicado: política de apertura entre orígenes cruzados"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Normas de COOP y COEP explicadas: política de Embedder de origen cruzado"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Lighthouse | GitHub"  

> [!NOTE]
> <span data-ttu-id="fc038-305">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fc038-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fc038-306">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/03/devtools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="fc038-306">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fc038-308">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fc038-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
