---
description: Emular las deficiencias de la visión de color, acoplar a la izquierda en el menú de comandos y mucho más.
title: Novedades de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f97155b12a679f630ce80c007e7f0ca693e19876
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408356"
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
# <a name="whats-new-in-devtools-microsoft-edge-83"></a><span data-ttu-id="18081-104">Novedades de DevTools (Microsoft Edge 83)</span><span class="sxs-lookup"><span data-stu-id="18081-104">What's New In DevTools (Microsoft Edge 83)</span></span>  

<span data-ttu-id="18081-105">Siguiendo la programación de Chromium actualizada, estamos ajustando nuestra programación para las próximas versiones de Microsoft Edge y cancelando la versión de Microsoft Edge 82.</span><span class="sxs-lookup"><span data-stu-id="18081-105">Following the updated Chromium schedule, we are adjusting our schedule for upcoming Microsoft Edge releases and cancelling the Microsoft Edge 82 release.</span></span> <span data-ttu-id="18081-106">Consulta nuestra [entrada de blog][WindowsBlogStableRelease] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="18081-106">Check out our [blog post][WindowsBlogStableRelease] for more info.</span></span>  

<span data-ttu-id="18081-107">Estas son las nuevas características disponibles en DevTools en Microsoft Edge 83.</span><span class="sxs-lookup"><span data-stu-id="18081-107">Here are the new features available in the DevTools in Microsoft Edge 83.</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="18081-108">Anuncios del equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="18081-108">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="18081-109">Las siguientes secciones son una lista de anuncios que puede que falte del equipo de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="18081-109">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="18081-110">Echa un vistazo a los anuncios para probar nuevas características en DevTools, microsoft Visual Studio code extensions y mucho más.</span><span class="sxs-lookup"><span data-stu-id="18081-110">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="18081-111">Para mantenerse al día de todas las características más recientes y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] y [síganos en Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="18081-111">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a><span data-ttu-id="18081-112">Depuración remota de Microsoft Edge en dispositivos Windows 10</span><span class="sxs-lookup"><span data-stu-id="18081-112">Remotely debug Microsoft Edge on Windows 10 Devices</span></span>  

<span data-ttu-id="18081-113">La [aplicación Herramientas remotas para Microsoft Edge \(Beta\)][RemoteTools] ya está disponible en [la Microsoft Store][MicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="18081-113">The [Remote Tools for Microsoft Edge \(Beta\)][RemoteTools] app is now available in the [Microsoft Store][MicrosoftStore].</span></span>  <span data-ttu-id="18081-114">Con esta aplicación, que amplía el Portal de dispositivos [de Windows,][WindowsUwpDebugTestPerfDevicePortal]puedes conectarte desde la instancia de Microsoft Edge que se ejecuta en el equipo de desarrollo a un dispositivo remoto de Windows 10, mostrar una lista de destinos \(todas las pestañas de Microsoft Edge y [PWAs][ProgressiveWebAppsChromiumIndex] abiertas en el dispositivo Windows 10\) y usar DevTools en el equipo de desarrollo en un destino que se ejecuta en el dispositivo remoto de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="18081-114">Using this app, which extends the [Windows Device Portal][WindowsUwpDebugTestPerfDevicePortal], you are able to connect from the instance of Microsoft Edge running on your development machine to a remote Windows 10 device, display a list of targets \(all tabs in Microsoft Edge and [PWAs][ProgressiveWebAppsChromiumIndex] open on the Windows 10 device\), and use the DevTools on your development machine against a target running on the remote Windows 10 device.</span></span>  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="La aplicación Herramientas remotas para Microsoft Edge (Beta) disponible en Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   <span data-ttu-id="18081-116">La [aplicación Herramientas remotas para Microsoft Edge (Beta)][RemoteTools] disponible en [Microsoft Store][MicrosoftStore]</span><span class="sxs-lookup"><span data-stu-id="18081-116">The [Remote Tools for Microsoft Edge (Beta)][RemoteTools] app available in the [Microsoft Store][MicrosoftStore]</span></span>  
:::image-end:::  

<span data-ttu-id="18081-117">[Lee nuestra guía para configurar el dispositivo Windows 10 y la máquina de desarrollo para la depuración remota.][DevtoolsRemoteDebuggingWindows]</span><span class="sxs-lookup"><span data-stu-id="18081-117">[Read our guide for setting up your Windows 10 device and your development machine for remote debugging][DevtoolsRemoteDebuggingWindows].</span></span>  <span data-ttu-id="18081-118">Háganos saber acerca de su experiencia de depuración remota [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="18081-118">Let us know about your remote debugging experience by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

### <a name="new-ways-to-access-settings"></a><span data-ttu-id="18081-119">Nuevas formas de acceder a la configuración</span><span class="sxs-lookup"><span data-stu-id="18081-119">New ways to access Settings</span></span>  

<span data-ttu-id="18081-120">Hay un montón de opciones de configuración para DevTools que puedes personalizar para que DevTools se vea, se sienta y funcione de la forma que necesita.</span><span class="sxs-lookup"><span data-stu-id="18081-120">There are tons of settings for the DevTools that you are able to customize to make the DevTools look, feel, and work the way you need.</span></span> <span data-ttu-id="18081-121">En Microsoft Edge 83, ahora es mucho más fácil obtener acceso a [Configuración][DevtoolsCustomizeIndexSettings] en DevTools.</span><span class="sxs-lookup"><span data-stu-id="18081-121">In Microsoft Edge 83, accessing [Settings][DevtoolsCustomizeIndexSettings] in the DevTools is now much easier.</span></span>  <span data-ttu-id="18081-122">Abre Configuración con el icono de engranaje junto a Alertas de consola y el menú principal.</span><span class="sxs-lookup"><span data-stu-id="18081-122">Open Settings with the gear icon next to Console alerts and the main menu.</span></span>  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="El icono de engranaje abre Configuración en DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   <span data-ttu-id="18081-124">El icono de engranaje abre **Configuración** en DevTools</span><span class="sxs-lookup"><span data-stu-id="18081-124">The gear icon opens **Settings** in the DevTools</span></span>  
:::image-end:::  

<span data-ttu-id="18081-125">También puede abrir Configuración desde [el][DevtoolsCustomizeIndexSettings] menú **principal en** **Más herramientas.**</span><span class="sxs-lookup"><span data-stu-id="18081-125">You are also able to open [Settings][DevtoolsCustomizeIndexSettings] from the **Main Menu** under **More tools**.</span></span>

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menú principal > Más herramientas > configuración" lightbox="../../media/2020/03/settings2.msft.png":::
   <span data-ttu-id="18081-127">**Menú principal**  >  **Más herramientas**  >  **Configuración**</span><span class="sxs-lookup"><span data-stu-id="18081-127">**Main Menu** > **More tools** > **Settings**</span></span>  
:::image-end:::  

<span data-ttu-id="18081-128">Problema de [chromium #1050855][CR1050855]</span><span class="sxs-lookup"><span data-stu-id="18081-128">Chromium issue [#1050855][CR1050855]</span></span>

### <a name="new-and-improved-infobars"></a><span data-ttu-id="18081-129">Infobars nuevas y mejoradas</span><span class="sxs-lookup"><span data-stu-id="18081-129">New and improved infobars</span></span>

<span data-ttu-id="18081-130">Las barras de notificación informativos \(infobars\) de DevTools ahora tienen una apariencia mejorada y más funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="18081-130">Informational notification bars \(infobars\) in DevTools now have an improved look and more functionality.</span></span> <span data-ttu-id="18081-131">En Microsoft Edge 83, las barras de información son más fáciles de leer y proporcionar botones para que puedas realizar la acción pertinente de inmediato.</span><span class="sxs-lookup"><span data-stu-id="18081-131">In Microsoft Edge 83, infobars are easier to read and provide buttons so you are able to take the relevant action right away.</span></span>  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Infobar para imprimir un archivo minificado en Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   <span data-ttu-id="18081-133">Infobar para imprimir un archivo minificado en Microsoft Edge versión 83</span><span class="sxs-lookup"><span data-stu-id="18081-133">Infobar for pretty-printing a minified file in Microsoft Edge Version 83</span></span>  
:::image-end:::  

<span data-ttu-id="18081-134">Problema de [chromium #1056348][CR1056348]</span><span class="sxs-lookup"><span data-stu-id="18081-134">Chromium issue [#1056348][CR1056348]</span></span>

### <a name="navigate-the-color-picker-with-your-keyboard"></a><span data-ttu-id="18081-135">Navegar por el Selector de colores con el teclado</span><span class="sxs-lookup"><span data-stu-id="18081-135">Navigate the Color Picker with your keyboard</span></span>  

<span data-ttu-id="18081-136">El [Selector de colores][DevtoolsCssReferenceColorPicker] es una GUI en el panel [Elementos][DevtoolsCssIndex] para cambiar `color` y `background-color` declaraciones.</span><span class="sxs-lookup"><span data-stu-id="18081-136">The [Color Picker][DevtoolsCssReferenceColorPicker] is a GUI in the [Elements panel][DevtoolsCssIndex] for changing `color` and `background-color` declarations.</span></span>  <span data-ttu-id="18081-137">En versiones anteriores de Microsoft Edge, no podía navegar por la sección **Sombras** del Selector de [colores][DevtoolsCssReferenceColorPicker] con el teclado.</span><span class="sxs-lookup"><span data-stu-id="18081-137">In previous versions of Microsoft Edge, you were not able to navigate the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker] with the keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Ahora puedes usar el teclado para mover el selector en la sección Sombras del Selector de colores" lightbox="../../media/2020/03/color-picker.msft.png":::
   <span data-ttu-id="18081-139">Ahora puedes usar el teclado para mover el selector en la sección **Sombras** del [Selector de colores][DevtoolsCssReferenceColorPicker]</span><span class="sxs-lookup"><span data-stu-id="18081-139">You are now able to use your keyboard to move the selector in the **Shades** section of the [Color Picker][DevtoolsCssReferenceColorPicker]</span></span>  
:::image-end:::  

<span data-ttu-id="18081-140">En Microsoft Edge 83, ahora puedes usar el teclado para mover el selector en la sección **Sombras** del Selector de colores.</span><span class="sxs-lookup"><span data-stu-id="18081-140">In Microsoft Edge 83, you are now able to use the keyboard to move the selector in the **Shades** section of the Color Picker.</span></span>  

<span data-ttu-id="18081-141">Problema de [chromium #963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="18081-141">Chromium issue [#963183][CR963183]</span></span>  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a><span data-ttu-id="18081-142">La pestaña Propiedades se rellena ahora después de una actualización de página</span><span class="sxs-lookup"><span data-stu-id="18081-142">Properties tab now populates after a page refresh</span></span>  

<span data-ttu-id="18081-143">En Microsoft Edge 81  y versiones anteriores, las actualizaciones de página han roto la pestaña Propiedades del [panel][DevtoolsCssIndex] Elementos.</span><span class="sxs-lookup"><span data-stu-id="18081-143">In Microsoft Edge 81 and earlier, the **Properties tab** in the [Elements panel][DevtoolsCssIndex] was broken by page refreshes.</span></span>  <span data-ttu-id="18081-144">Al actualizar la página, la pestaña **Propiedades** no rellenaba las propiedades del elemento seleccionado actualmente.</span><span class="sxs-lookup"><span data-stu-id="18081-144">When you refreshed the page, the **Properties tab** did not populate the properties of the currently-selected element.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="En Microsoft Edge 81 y versiones anteriores, la pestaña Propiedades estaba en blanco después de una actualización de página" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   <span data-ttu-id="18081-146">En Microsoft Edge 81 y versiones anteriores, la **pestaña Propiedades** estaba en blanco después de una actualización de página</span><span class="sxs-lookup"><span data-stu-id="18081-146">In Microsoft Edge 81 and earlier, the **Properties tab** was blank after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="18081-147">En Microsoft Edge 83, ahora puede mostrar las propiedades del elemento seleccionado actualmente después de una actualización de página en la **pestaña Propiedades**.</span><span class="sxs-lookup"><span data-stu-id="18081-147">In Microsoft Edge 83, you are now able to display the properties of the currently-selected element after a page refresh in the **Properties tab**.</span></span>  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="En Microsoft Edge 83, la pestaña Propiedades muestra las propiedades del elemento seleccionado actualmente después de una actualización de página" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   <span data-ttu-id="18081-149">En Microsoft Edge 83, la pestaña **Propiedades** muestra las propiedades del elemento seleccionado actualmente después de una actualización de página</span><span class="sxs-lookup"><span data-stu-id="18081-149">In Microsoft Edge 83, the **Properties tab** displays the properties of the currently-selected element after a page refresh</span></span>  
:::image-end:::  

<span data-ttu-id="18081-150">Problema de [chromium #1050999][CR1050999]</span><span class="sxs-lookup"><span data-stu-id="18081-150">Chromium issue [#1050999][CR1050999]</span></span>  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a><span data-ttu-id="18081-151">Usar las teclas de flecha para desplazarse en la herramienta Cambios</span><span class="sxs-lookup"><span data-stu-id="18081-151">Use the arrow keys to scroll in the Changes tool</span></span>  

<span data-ttu-id="18081-152">La **herramienta Cambios realiza** un seguimiento de los cambios realizados en CSS o JavaScript en DevTools.</span><span class="sxs-lookup"><span data-stu-id="18081-152">The **Changes tool** tracks any changes you have made to CSS or JavaScript in the DevTools.</span></span>  <span data-ttu-id="18081-153">Puede usar la herramienta **Cambios** para mostrar rápidamente todos los cambios y volver a usarlos en el editor/IDE.</span><span class="sxs-lookup"><span data-stu-id="18081-153">You are able to use the **Changes tool** to quickly display all your changes and take those back to your editor/IDE.</span></span>  

<span data-ttu-id="18081-154">Para abrir la **herramienta Cambios,** seleccione `Ctrl` + `Shift` + `P` en DevTools para abrir el [menú comando][DevToolsCommandMenuIndex] y escriba `changes` .</span><span class="sxs-lookup"><span data-stu-id="18081-154">To open the **Changes tool**, select `Ctrl`+`Shift`+`P` in the DevTools to open the [Command Menu][DevToolsCommandMenuIndex] and type `changes`.</span></span>  <span data-ttu-id="18081-155">elija y ejecute el **comando Mostrar cambios** para abrir la herramienta **Cambios** en el cajón DevTools.</span><span class="sxs-lookup"><span data-stu-id="18081-155">choose and run the **Show Changes** command to open the **Changes tool** in the DevTools drawer.</span></span>  

<span data-ttu-id="18081-156">Cuando haya realizado un cambio en un archivo minificado, la herramienta **Cambios** permite desplazarse horizontalmente para mostrar todo el código minificado.</span><span class="sxs-lookup"><span data-stu-id="18081-156">When you have made a change to a minified file, the **Changes tool** enables you to scroll horizontally to display all of your minified code.</span></span>  <span data-ttu-id="18081-157">A partir de Microsoft Edge 83, ahora puede desplazarse horizontalmente con las teclas de flecha del teclado.</span><span class="sxs-lookup"><span data-stu-id="18081-157">Starting in Microsoft Edge 83, you may now scroll horizontally using the arrow keys on your keyboard.</span></span>  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de flecha para mostrar el código minificado en la herramienta Cambios" lightbox="../../media/2020/03/changes.msft.png":::
   <span data-ttu-id="18081-159">En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de flecha para mostrar los cambios realizados en el código **minificado** en la herramienta Cambios</span><span class="sxs-lookup"><span data-stu-id="18081-159">In Microsoft Edge 83, you may scroll horizontally with the arrow keys to display the changes you made to your minified code in the **Changes tool**</span></span>  
:::image-end:::  

<span data-ttu-id="18081-160">Si usas lectores de pantalla o el teclado para navegar [][PostTweetEdgeDevTools] por DevTools, envíanos tus comentarios tuiteando o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="18081-160">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="18081-161">Problema de [chromium #963183][CR963183]</span><span class="sxs-lookup"><span data-stu-id="18081-161">Chromium issue [#963183][CR963183]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="18081-162">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="18081-162">Announcements from the Chromium project</span></span>  

<span data-ttu-id="18081-163">En las secciones siguientes se anuncian características adicionales disponibles en Microsoft Edge 83 que se contribuyeron al proyecto chromium de código abierto.</span><span class="sxs-lookup"><span data-stu-id="18081-163">The following sections announce additional features available in Microsoft Edge 83 that were contributed to the open source Chromium project.</span></span>  

### <a name="emulate-vision-deficiencies"></a><span data-ttu-id="18081-164">Emular deficiencias visuales</span><span class="sxs-lookup"><span data-stu-id="18081-164">Emulate vision deficiencies</span></span>  

<span data-ttu-id="18081-165">Abra la [pestaña Representación][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] y use la nueva característica **Emular** deficiencias de visión para obtener una mejor idea de cómo las personas con diferentes tipos de deficiencias de visión experimentan su sitio.</span><span class="sxs-lookup"><span data-stu-id="18081-165">Open the [Rendering tab][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] and use the new **Emulate vision deficiencies** feature to get a better idea of how people with different types of vision deficiencies experience your site.</span></span>  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emular la visión borrosa" lightbox="../../media/2020/03/vision.msft.png":::
   <span data-ttu-id="18081-167">Emular la visión borrosa</span><span class="sxs-lookup"><span data-stu-id="18081-167">Emulating blurred vision</span></span>  
:::image-end:::  

<span data-ttu-id="18081-168">DevTools es capaz de emular la visión borrosa y los siguientes [tipos de deficiencias de la visión de color.][ColorBlindnessTypes]</span><span class="sxs-lookup"><span data-stu-id="18081-168">DevTools is able to emulate blurred vision and the following [types of color vision deficiencies][ColorBlindnessTypes].</span></span>  

| <span data-ttu-id="18081-169">Deficiencia de la visión de color</span><span class="sxs-lookup"><span data-stu-id="18081-169">Color Vision Deficiency</span></span> | <span data-ttu-id="18081-170">Detalles</span><span class="sxs-lookup"><span data-stu-id="18081-170">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="18081-171">Protanopia</span><span class="sxs-lookup"><span data-stu-id="18081-171">Protanopia</span></span> | <span data-ttu-id="18081-172">La incapacidad de percibir cualquier luz roja.</span><span class="sxs-lookup"><span data-stu-id="18081-172">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="18081-173">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="18081-173">Deuteranopia</span></span> | <span data-ttu-id="18081-174">La incapacidad de percibir cualquier luz verde.</span><span class="sxs-lookup"><span data-stu-id="18081-174">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="18081-175">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="18081-175">Tritanopia</span></span> | <span data-ttu-id="18081-176">La incapacidad de percibir cualquier luz azul.</span><span class="sxs-lookup"><span data-stu-id="18081-176">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="18081-177">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="18081-177">Achromatopsia</span></span> | <span data-ttu-id="18081-178">La incapacidad de percibir cualquier color, excepto para las sombras de gris \(extremadamente rara\).</span><span class="sxs-lookup"><span data-stu-id="18081-178">The inability to perceive any color, except for shades of grey \(extremely rare\).</span></span> |  

<span data-ttu-id="18081-179">Existen versiones menos extremas de estas deficiencias de visión de color y, de hecho, son más comunes.</span><span class="sxs-lookup"><span data-stu-id="18081-179">Less extreme versions of these color vision deficiencies exist, and in fact they are more common.</span></span>  
<span data-ttu-id="18081-180">Por ejemplo, protanomaly es una sensibilidad reducida a la luz roja (a diferencia de la protanopia, que es la incapacidad completa para percibir la luz roja).</span><span class="sxs-lookup"><span data-stu-id="18081-180">For example, protanomaly is a reduced sensitivity to red light (as opposed to protanopia, which is the complete inability to perceive red light).</span></span> <span data-ttu-id="18081-181">Sin embargo, estas deficiencias de visión **-omaly** no están tan claramente definidas: cada persona con una deficiencia de visión de este tipo es diferente y puede ver las cosas de forma diferente \(ser capaz de percibir más o menos de los colores relevantes\).</span><span class="sxs-lookup"><span data-stu-id="18081-181">However, these **-omaly** vision deficiencies are not as clearly defined:  every person with such a vision deficiency is different and may see things differently \(being able to perceive more/less of the relevant colors\).</span></span>  

<span data-ttu-id="18081-182">Al diseñar para las simulaciones más extremas en DevTools, se garantiza que las aplicaciones web sean accesibles para las personas con protanomaly, deuteranomaly, tritanomaly y achromatomaly también.</span><span class="sxs-lookup"><span data-stu-id="18081-182">By designing for the more extreme simulations in DevTools, your web apps are guaranteed to be accessible to people with protanomaly, deuteranomaly, tritanomaly, and achromatomaly as well.</span></span>  

<span data-ttu-id="18081-183">Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="18081-183">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="18081-184">Problema de [chromium #1003700][CR1003700]</span><span class="sxs-lookup"><span data-stu-id="18081-184">Chromium issue [#1003700][CR1003700]</span></span>  

### <a name="emulate-locales"></a><span data-ttu-id="18081-185">Emular configuraciones regionales</span><span class="sxs-lookup"><span data-stu-id="18081-185">Emulate locales</span></span>  

<span data-ttu-id="18081-186">Emular configuraciones regionales estableciendo una ubicación en **Ubicación de**  >  **sensores**.</span><span class="sxs-lookup"><span data-stu-id="18081-186">Emulate locales by setting a location in **Sensors** > **Location**.</span></span> <span data-ttu-id="18081-187">[Abra el **menú comando y** ][DevToolsCommandMenuIndex] escriba para obtener acceso a la pestaña `Sensors` **Sensores.**  Después de realizar estas acciones, DevTools modifica la configuración regional predeterminada actual, lo que afecta al código siguiente.</span><span class="sxs-lookup"><span data-stu-id="18081-187">[Open the **Command Menu**][DevToolsCommandMenuIndex] and type `Sensors` to access the **Sensors** tab.  After performing these actions, DevTools modifies the current default locale, affecting the following code.</span></span>  

*   `Intl.*` <span data-ttu-id="18081-188">API, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="18081-188">APIs, for example:</span></span> `new Intl.NumberFormat().resolvedOptions().locale`  
*   <span data-ttu-id="18081-189">Otras API de JavaScript con configuración regional, `String.prototype.localeCompare` como y , por `*.prototype.toLocaleString` ejemplo:</span><span class="sxs-lookup"><span data-stu-id="18081-189">Other locale-aware JavaScript APIs such as `String.prototype.localeCompare` and `*.prototype.toLocaleString`, for example:</span></span> `123_456..toLocaleString()`  
*   <span data-ttu-id="18081-190">API de DOM como `navigator.language` y</span><span class="sxs-lookup"><span data-stu-id="18081-190">DOM APIs such as `navigator.language` and</span></span> `navigator.languages`  
*   <span data-ttu-id="18081-191">Encabezado de solicitud HTTP [Accept-Language][MDNAcceptLanguage]</span><span class="sxs-lookup"><span data-stu-id="18081-191">The [Accept-Language][MDNAcceptLanguage] HTTP request header</span></span>  

> [!NOTE]
> <span data-ttu-id="18081-192">Las actualizaciones `navigator.language` a y no son `navigator.languages` visibles inmediatamente, pero solo después de la siguiente navegación o actualización de página.</span><span class="sxs-lookup"><span data-stu-id="18081-192">Updates to `navigator.language` and `navigator.languages` are not visible immediately, but only after the next navigation or page refresh.</span></span>  <span data-ttu-id="18081-193">Los cambios en el `Accept-Language` encabezado HTTP solo se reflejan para las solicitudes posteriores.</span><span class="sxs-lookup"><span data-stu-id="18081-193">Changes to the `Accept-Language` HTTP header are only reflected for subsequent requests.</span></span>  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emular una configuración regional" lightbox="../../media/2020/03/locale.msft.png":::
   <span data-ttu-id="18081-195">Emular una configuración regional</span><span class="sxs-lookup"><span data-stu-id="18081-195">Emulating a locale</span></span>  
:::image-end:::  

<span data-ttu-id="18081-196">Para probar una demostración, vaya al [ejemplo de código dependiente de la configuración regional][MathiasByensLocaleDemo].</span><span class="sxs-lookup"><span data-stu-id="18081-196">To try a demo, navigate to [Locale-dependent code example][MathiasByensLocaleDemo].</span></span>

<span data-ttu-id="18081-197">Problema de [chromium #1051822][CR1051822]</span><span class="sxs-lookup"><span data-stu-id="18081-197">Chromium issue [#1051822][CR1051822]</span></span>

### <a name="cross-origin-embedder-policy-coep-debugging"></a><span data-ttu-id="18081-198">Depuración de directiva de incrustación entre orígenes (COEP)</span><span class="sxs-lookup"><span data-stu-id="18081-198">Cross-Origin Embedder Policy (COEP) debugging</span></span>  

<span data-ttu-id="18081-199">El panel Red ahora proporciona información de depuración de directivas [de incrustación entre][COEP] orígenes.</span><span class="sxs-lookup"><span data-stu-id="18081-199">The Network panel now provides [Cross-Origin Embedder Policy][COEP] debugging information.</span></span>  

<span data-ttu-id="18081-200">La **columna** Estado ahora proporciona una explicación rápida de por qué se bloqueó una solicitud, así como un vínculo para ver los encabezados de esa solicitud para su posterior depuración:</span><span class="sxs-lookup"><span data-stu-id="18081-200">The **Status** column now provides a quick explanation of why a request was blocked as well as a link to view the headers of that request for further debugging:</span></span>  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Solicitudes bloqueadas en la columna **Status**" lightbox="../../media/2020/03/status.msft.png":::
   <span data-ttu-id="18081-202">Solicitudes bloqueadas en la **columna** Estado</span><span class="sxs-lookup"><span data-stu-id="18081-202">Blocked requests in the **Status** column</span></span>  
:::image-end:::  

<span data-ttu-id="18081-203">La **sección Encabezados de** respuesta de la pestaña **Encabezados** proporciona más instrucciones sobre cómo resolver los problemas:</span><span class="sxs-lookup"><span data-stu-id="18081-203">The **Response Headers** section of the **Headers** tab provides more guidance on how to resolve the issues:</span></span>  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Más instrucciones en la sección Encabezados de respuesta" lightbox="../../media/2020/03/guidance.msft.png":::
   <span data-ttu-id="18081-205">Más instrucciones en la sección **Encabezados de** respuesta</span><span class="sxs-lookup"><span data-stu-id="18081-205">More guidance in the **Response Headers** section</span></span>  
:::image-end:::  

<span data-ttu-id="18081-206">Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="18081-206">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="18081-207">Problema de [chromium #1051466][CR1051466]</span><span class="sxs-lookup"><span data-stu-id="18081-207">Chromium issue [#1051466][CR1051466]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="18081-208">Nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y puntos de registro</span><span class="sxs-lookup"><span data-stu-id="18081-208">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="18081-209">El panel Orígenes tiene nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y puntos de registro:</span><span class="sxs-lookup"><span data-stu-id="18081-209">The Sources panel has new icons for breakpoints, conditional breakpoints, and logpoints:</span></span>  

*   <span data-ttu-id="18081-210">Puntos de interrupción \(</span><span class="sxs-lookup"><span data-stu-id="18081-210">Breakpoints \(</span></span>![Punto de interrupción](../../media/2020/03/breakpoint.msft.png)<span data-ttu-id="18081-212">\) se representan mediante círculos rojos.</span><span class="sxs-lookup"><span data-stu-id="18081-212">\) are represented by red circles.</span></span>  
*   <span data-ttu-id="18081-213">Puntos de interrupción condicionales \(</span><span class="sxs-lookup"><span data-stu-id="18081-213">Conditional Breakpoints \(</span></span>![Punto de interrupción condicional](../../media/2020/03/conditional.msft.png)<span data-ttu-id="18081-215">\) están representados por círculos semi-rojos de medio blanco.</span><span class="sxs-lookup"><span data-stu-id="18081-215">\) are represented by half-red half-white circles.</span></span>  
*   <span data-ttu-id="18081-216">Logpoints \(</span><span class="sxs-lookup"><span data-stu-id="18081-216">Logpoints \(</span></span>![Logpoint](../../media/2020/03/logpoint.msft.png)<span data-ttu-id="18081-218">\) se representan mediante círculos rojos con iconos de consola.</span><span class="sxs-lookup"><span data-stu-id="18081-218">\) are represented by red circles with Console icons.</span></span>  

<span data-ttu-id="18081-219">La motivación de los nuevos iconos era hacer que la interfaz de usuario fuera más coherente con otras herramientas de depuración DE GUI \(que normalmente colorean puntos de interrupción rojo\) y hacer que sea más fácil distinguir entre las 3 características de un vistazo.</span><span class="sxs-lookup"><span data-stu-id="18081-219">The motivation for the new icons was to make the UI more consistent with other GUI debugging tools \(which usually color breakpoints red\) and to make it easier to distinguish between the 3 features at a glance.</span></span>  

<span data-ttu-id="18081-220">Problema de [chromium #1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="18081-220">Chromium issue [#1041830][CR1041830]</span></span>  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a><span data-ttu-id="18081-221">Ver solicitudes de red que establecen una ruta de acceso de cookie específica</span><span class="sxs-lookup"><span data-stu-id="18081-221">View network requests that set a specific cookie path</span></span>  

<span data-ttu-id="18081-222">Use la palabra clave de filtro nueva de la herramienta Red para centrarse en las solicitudes de red `cookie-path` que establecen una ruta de acceso de cookie [específica.][MDNCookiePath] </span><span class="sxs-lookup"><span data-stu-id="18081-222">Use the new `cookie-path` filter keyword in the **Network** tool to focus on the network requests that set a specific [cookie path][MDNCookiePath].</span></span>  

<span data-ttu-id="18081-223">Consulte [Filtrar solicitudes por propiedades para][DevtoolsNetworkReferenceFilterRequestsProperties] detectar más palabras clave como `cookie-path` .</span><span class="sxs-lookup"><span data-stu-id="18081-223">Check out [Filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties] to discover more keywords like `cookie-path`.</span></span>

### <a name="dock-to-left-from-the-command-menu"></a><span data-ttu-id="18081-224">Acoplar a la izquierda desde el menú comando</span><span class="sxs-lookup"><span data-stu-id="18081-224">Dock to left from the Command Menu</span></span>  

<span data-ttu-id="18081-225">Abra el [menú comando][DevToolsCommandMenuIndex] y ejecute el comando para `Dock to left` mover DevTools a la izquierda de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="18081-225">Open the [Command Menu][DevToolsCommandMenuIndex] and run the `Dock to left` command to move DevTools to the left of your viewport.</span></span>  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools acoplada a la izquierda de la ventanilla" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   <span data-ttu-id="18081-227">DevTools acoplada a la izquierda de la ventanilla</span><span class="sxs-lookup"><span data-stu-id="18081-227">DevTools docked to the left of the viewport</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="18081-228">La **característica Acoplar a la** izquierda ha estado disponible desde Microsoft Edge 75, pero anteriormente solo era accesible desde el menú [principal][DevtoolsCustomizePlacementsChangeMainMenu].</span><span class="sxs-lookup"><span data-stu-id="18081-228">The **Dock to left** feature has been available since Microsoft Edge 75, but it was previously only accessible from the [Main Menu][DevtoolsCustomizePlacementsChangeMainMenu].</span></span>  <span data-ttu-id="18081-229">La nueva característica de Microsoft Edge 83 es que ahora puede tener acceso a esta característica desde el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="18081-229">The new feature in Microsoft Edge 83 is that you may now access this feature from the Command Menu.</span></span>  

<span data-ttu-id="18081-230">Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="18081-230">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="18081-231">Problema de [chromium #1011679][CR1011679]</span><span class="sxs-lookup"><span data-stu-id="18081-231">Chromium issue [#1011679][CR1011679]</span></span>  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a><span data-ttu-id="18081-232">El panel Auditorías es ahora el panel Faro</span><span class="sxs-lookup"><span data-stu-id="18081-232">The Audits panel is now the Lighthouse panel</span></span>  

<span data-ttu-id="18081-233">El equipo de DevTools recibió con frecuencia comentarios de desarrolladores web que, aunque era posible ejecutar [Lighthouse][GithubGoogleChromeLighthouse] desde DevTools, cuando lo intentaron no pudieron encontrar el panel "Faro", por lo que el panel **Auditorías** ahora es el **panel** Faro.</span><span class="sxs-lookup"><span data-stu-id="18081-233">The DevTools team frequently got feedback from web developers that while it was possible to run [Lighthouse][GithubGoogleChromeLighthouse] from DevTools, when they tried it out they were not able to find the "Lighthouse" panel, so the **Audits** panel is now the **Lighthouse** panel.</span></span>  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Panel De faro" lightbox="../../media/2020/03/lighthouse.msft.png":::
   <span data-ttu-id="18081-235">Panel De faro</span><span class="sxs-lookup"><span data-stu-id="18081-235">The Lighthouse panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="18081-236">El panel **Faro** proporciona vínculos al contenido hospedado en sitios web de terceros.</span><span class="sxs-lookup"><span data-stu-id="18081-236">The **Lighthouse** panel provides links to content hosted on third-party websites.</span></span>  <span data-ttu-id="18081-237">Microsoft no es responsable y no tiene control sobre el contenido de estos sitios ni sobre los datos que puedan recopilar.</span><span class="sxs-lookup"><span data-stu-id="18081-237">Microsoft is not responsible for and has no control over the content of these sites and any data they may collect.</span></span>  

### <a name="delete-all-local-overrides-in-a-folder"></a><span data-ttu-id="18081-238">Eliminar todas las invalidaciones locales de una carpeta</span><span class="sxs-lookup"><span data-stu-id="18081-238">Delete all Local Overrides in a folder</span></span>  

<span data-ttu-id="18081-239">Después de configurar **Invalidaciones** locales, puede mantener el mouse en un directorio, abrir el menú contextual \(hacer clic con el botón secundario\) y elegir la nueva opción **Eliminar** todas las invalidaciones para eliminar todas las invalidaciones locales de esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="18081-239">After setting up **Local Overrides** you may hover on a directory, open the contextual menu \(right-click\), and choose the new **Delete all overrides** option to delete all Local Overrides in that folder.</span></span>  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Eliminar todas las invalidaciones" lightbox="../../media/2020/03/overrides.msft.png":::
   <span data-ttu-id="18081-241">Eliminar todas las invalidaciones</span><span class="sxs-lookup"><span data-stu-id="18081-241">Delete all overrides</span></span>  
:::image-end:::  

<span data-ttu-id="18081-242">Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="18081-242">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="18081-243">Problema de [chromium #1016501][CR1016501]</span><span class="sxs-lookup"><span data-stu-id="18081-243">Chromium issue [#1016501][CR1016501]</span></span>  

### <a name="updated-long-tasks-ui"></a><span data-ttu-id="18081-244">Interfaz de usuario de tareas largas actualizada</span><span class="sxs-lookup"><span data-stu-id="18081-244">Updated Long tasks UI</span></span>  

<span data-ttu-id="18081-245">Una **tarea larga** es código JavaScript que monopoliza el subproceso principal durante mucho tiempo, lo que hace que una página web se congele.</span><span class="sxs-lookup"><span data-stu-id="18081-245">A **Long Task** is JavaScript code that monopolizes the main thread for a long time, causing a web page to freeze.</span></span>  

<span data-ttu-id="18081-246">Has podido visualizar tareas largas en el [panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] Rendimiento desde hace tiempo, pero en Microsoft Edge 83 se ha actualizado la interfaz de usuario de visualización de tareas largas en el panel Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="18081-246">You have been able to [visualize Long Tasks in the Performance panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] for a while now, but in Microsoft Edge 83 the Long Task visualization UI in the Performance panel has been updated.</span></span>  <span data-ttu-id="18081-247">La parte tarea larga de una tarea ahora se coloreó con un fondo rojo a rayas.</span><span class="sxs-lookup"><span data-stu-id="18081-247">The Long Task portion of a task is now colored with a striped red background.</span></span>  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="La nueva interfaz de usuario de tarea larga" lightbox="../../media/2020/03/long-task.msft.png":::
   <span data-ttu-id="18081-249">La nueva interfaz de usuario de tarea larga</span><span class="sxs-lookup"><span data-stu-id="18081-249">The new Long Task UI</span></span>  
:::image-end:::  

<span data-ttu-id="18081-250">Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.</span><span class="sxs-lookup"><span data-stu-id="18081-250">Send your feedback by [tweeting][PostTweetEdgeDevTools] orchoosing the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="18081-251">Problema de [chromium #1054447][CR1054447]</span><span class="sxs-lookup"><span data-stu-id="18081-251">Chromium issue [#1054447][CR1054447]</span></span>  

### <a name="maskable-icon-support-in-the-manifest-pane"></a><span data-ttu-id="18081-252">Compatibilidad con iconos enmascarables en el panel Manifiesto</span><span class="sxs-lookup"><span data-stu-id="18081-252">Maskable icon support in the Manifest pane</span></span>  

<span data-ttu-id="18081-253">Android Oreo introdujo iconos adaptables, que muestran iconos de aplicaciones en una variedad de formas en diferentes modelos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="18081-253">Android Oreo introduced adaptive icons, which display app icons in a variety of shapes across different device models.</span></span>  <span data-ttu-id="18081-254">**Los iconos enmascarables** son un nuevo formato de icono que admite iconos adaptables, que te permiten asegurarte de que el icono [de PWA][ProgressiveWebAppsChromiumIndex] se vea bien en dispositivos que admitan el estándar de iconos enmascarables.</span><span class="sxs-lookup"><span data-stu-id="18081-254">**Maskable icons** are a new icon format that support adaptive icons, which enable you to ensure that your [PWA][ProgressiveWebAppsChromiumIndex] icon looks good on devices that support the maskable icons standard.</span></span>  

<span data-ttu-id="18081-255">Habilita la nueva **casilla Mostrar solo** el área  mínima segura para iconos enmascarables en el panel Manifiesto para comprobar que el icono enmascarable se ve bien en dispositivos Android Oreo.</span><span class="sxs-lookup"><span data-stu-id="18081-255">Enable the new **Show only the minimum safe area for maskable icons** checkbox in the **Manifest** pane to check that your maskable icon looks good on Android Oreo devices.</span></span>  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Mostrar solo el área segura mínima para iconos enmascarables" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   <span data-ttu-id="18081-257">La **casilla Mostrar solo el área segura mínima para iconos enmascarables**</span><span class="sxs-lookup"><span data-stu-id="18081-257">The **Show only the minimum safe area for maskable icons** checkbox</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="18081-258">Esta característica se inicia en Microsoft Edge 81.</span><span class="sxs-lookup"><span data-stu-id="18081-258">This feature launched in Microsoft Edge 81.</span></span>  <span data-ttu-id="18081-259">Las actualizaciones que se tratan aquí en Microsoft Edge 83 no se han cubierto en [What's New In DevTools (Microsoft Edge 81).][WhatsNew81]</span><span class="sxs-lookup"><span data-stu-id="18081-259">The updates covered here in Microsoft Edge 83 were not covered in [What's New In DevTools (Microsoft Edge 81)][WhatsNew81].</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="18081-260">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="18081-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="18081-261">Si estás en Windows o macOS, considera usar los canales de vista [previa de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="18081-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="18081-262">Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="18081-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="18081-263">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="18081-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Novedades de DevTools (Microsoft Edge 81) | Microsoft Docs"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambie los colores con el selector de | Microsoft Docs"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y cambio de css | Microsoft Docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Cambiar la ubicación desde el menú principal | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Ver la actividad del subproceso | Microsoft Docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de representación con la pestaña Representación | Microsoft Docs"  
[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota de dispositivos Windows 10 | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Puntos de interrupción de línea de código: cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrar solicitudes por propiedades: referencia de análisis de red | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalización de Microsoft Edge DevTools | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Introducción al Portal de dispositivos windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Herramientas remotas para Microsoft Edge (Beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Actualización de versiones de canal estables para Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema : MicrosoftDocs/edge-developer - GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  
[TheWebWeWant]: https://webwewant.fyi "La web que queremos"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Tipos de ceguera de color"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Ejemplo de código dependiente de la configuración regional"  

[CR963183]: https://crbug.com/963183 "Problema 963183: DevTools no son compatibles con WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problema 1003700: Agregar compatibilidad con DevTools para la simulación de deficiencia de visión de color"  
[CR1011679]: https://crbug.com/1011679 "Problema 1011679: Introducir "Acoplar a la izquierda" mediante el menú de comandos"  
[CR1016501]: https://crbug.com/1016501 "Problema 1016501: Solicitud de característica: botón para eliminar todas las invalidaciones locales"  
[CR1050999]: https://crbug.com/1050999 "Problema 1050999: Pestaña Propiedades"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: Compatibilidad con la depuración DE COOP/COEP en DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problema 1054447: Actualizar métricas de rendimiento en la escala de tiempo de DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: agregar interfaz de usuario para emular la configuración regional"
[CR1041830]: https://crbug.com/1041830 "Problema 1041830: Mejorar los colores de los puntos de interrupción"
[CR1050855]: https://crbug.com/1050855 "Problema 1050855: La vista Configuración es difícil de detectar"
[CR1056348]: https://crbug.com/1056348 "Problema 1056348: Actualización de componentes de infobar"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP y COEP explicados: directiva de abridor entre orígenes"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "COOP y COEP explicados: directiva de incrustación entre orígenes"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "| GitHub"  

> [!NOTE]
> <span data-ttu-id="18081-305">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18081-305">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="18081-306">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/03/devtools/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="18081-306">The original page is found [here](https://developers.google.com/web/updates/2020/03/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="18081-308">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18081-308">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
