---
description: Nuevas herramientas de depuración de cuadrícula CSS, herramienta Webauthn, herramientas movebles y panel lateral calculado.
title: Novedades de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c7859631327fc031909cd25736fddb8cff3cff45
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564899"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-87"></a><span data-ttu-id="168ef-104">Novedades de DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="168ef-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a><span data-ttu-id="168ef-105">Mejorar la localización de DevTools</span><span class="sxs-lookup"><span data-stu-id="168ef-105">Improving DevTools localization</span></span>  

<span data-ttu-id="168ef-106">Para satisfacer sus necesidades de traducción, el Microsoft Edge de DevTools se centra en mejorar la calidad de la traducción.</span><span class="sxs-lookup"><span data-stu-id="168ef-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="168ef-107">A partir Microsoft Edge versión 87, varias cadenas y términos están bloqueados y no cambian incluso cuando el resto de DevTools se muestran en otros idiomas.</span><span class="sxs-lookup"><span data-stu-id="168ef-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="168ef-108">La lista de cadenas y términos afectados incluye lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="168ef-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="168ef-109">Las cadenas de la **herramienta Faro.**</span><span class="sxs-lookup"><span data-stu-id="168ef-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="168ef-110">El término `service worker` .</span><span class="sxs-lookup"><span data-stu-id="168ef-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="168ef-111">Algunos de los **filtros de** herramientas de red como , , `URL` y `XHR` `JS` `CSS` .</span><span class="sxs-lookup"><span data-stu-id="168ef-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="168ef-112">LA API de utilidades de consola [$0.][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]</span><span class="sxs-lookup"><span data-stu-id="168ef-112">The [$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="168ef-113">[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] ahora está disponible en la [consola para][DevtoolsConsoleIndex] los usuarios en versiones localizadas de DevTools.</span><span class="sxs-lookup"><span data-stu-id="168ef-113">[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] is now available in the [Console][DevtoolsConsoleIndex] for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="168ef-114">Gracias a la comunidad de desarrolladores global por ayudar a mejorar la localización del Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="168ef-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="168ef-115">Continúe con [el envío de comentarios sobre la calidad de localización](#getting-in-touch-with-microsoft-edge-devtools-team) para mejorar la compatibilidad con DevTools en todas las configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="168ef-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="168ef-116">Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya a Problema [#1136655][CR1136655].</span><span class="sxs-lookup"><span data-stu-id="168ef-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  


:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="168ef-118">**Panel de** red con filtros no localizados</span><span class="sxs-lookup"><span data-stu-id="168ef-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a><span data-ttu-id="168ef-119">Mover herramientas entre paneles superior e inferior</span><span class="sxs-lookup"><span data-stu-id="168ef-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="168ef-120">DevTools ahora admite mover herramientas entre los paneles superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="168ef-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="168ef-121">Personalice sus DevTools y mejore su productividad viendo cualquier combinación de dos herramientas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="168ef-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="168ef-122">Por ejemplo, vea las \*\*\*\* **herramientas Elementos** y Orígenes al mismo tiempo \(moviendo la herramienta **Orígenes** a la parte inferior\).</span><span class="sxs-lookup"><span data-stu-id="168ef-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="168ef-123">Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#1075732][CR1075732].</span><span class="sxs-lookup"><span data-stu-id="168ef-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="168ef-124">Para mover cualquier herramienta superior a la parte inferior, mantenga el mouse en una pestaña, abra el menú contextual \(haga clic con el botón secundario\) y elija **Mover a la parte inferior**.</span><span class="sxs-lookup"><span data-stu-id="168ef-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Desplazarse a la parte inferior" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="168ef-126">Desplazarse a la parte inferior</span><span class="sxs-lookup"><span data-stu-id="168ef-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="168ef-127">Para mover cualquier herramienta inferior a la parte superior, mantenga el mouse en una pestaña, abra el menú contextual \(hacer clic con el botón derecho\) y elija **Mover a la parte superior**.</span><span class="sxs-lookup"><span data-stu-id="168ef-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Desplazarse a la parte superior" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="168ef-129">Desplazarse a la parte superior</span><span class="sxs-lookup"><span data-stu-id="168ef-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a><span data-ttu-id="168ef-130">Guardar y exportar con la consola de red</span><span class="sxs-lookup"><span data-stu-id="168ef-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="168ef-132">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="168ef-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="168ef-133">La **herramienta Consola de** red ahora ha mejorado la compatibilidad con los esquemas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] y [OpenAPI v2.][SwaggerSpecificationV2]</span><span class="sxs-lookup"><span data-stu-id="168ef-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="168ef-134">Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y elija la casilla situada junto a **Habilitar**consola de red .</span><span class="sxs-lookup"><span data-stu-id="168ef-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="168ef-135">Para obtener más información acerca de **la**consola de red, vaya a [Habilitar la característica experimental de consola de red][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="168ef-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="168ef-136">Este experimento ahora admite las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="168ef-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="168ef-137">Guardar y exportar colecciones y entornos.</span><span class="sxs-lookup"><span data-stu-id="168ef-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="168ef-138">Edite y exporte conjuntos de variables de entorno dentro de la **herramienta Consola de** red.</span><span class="sxs-lookup"><span data-stu-id="168ef-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="168ef-139">Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya a Problema [#1093687][CR1093687].</span><span class="sxs-lookup"><span data-stu-id="168ef-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Escriba el nombre del nuevo entorno" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="168ef-141">Escriba el nombre del nuevo entorno</span><span class="sxs-lookup"><span data-stu-id="168ef-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Elegir formato para el nuevo entorno" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="168ef-143">Elegir formato para el nuevo entorno</span><span class="sxs-lookup"><span data-stu-id="168ef-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a><span data-ttu-id="168ef-144">Herramientas de cuadrícula CSS mejoradas</span><span class="sxs-lookup"><span data-stu-id="168ef-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="168ef-146">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="168ef-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="168ef-147">Las Microsoft Edge DevTools ahora admiten las siguientes características para inspeccionar, ver y depurar las cuadrículas CSS.</span><span class="sxs-lookup"><span data-stu-id="168ef-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="168ef-148">Muestra una superposición de cuadrícula simplificada con **la herramienta Inspeccionar** u obtén información más detallada con superposiciones persistentes.</span><span class="sxs-lookup"><span data-stu-id="168ef-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="168ef-149">Para habilitar las superposiciones de cuadrícula persistentes, elija el icono de cuadrícula junto a un elemento contenedor de cuadrícula en la herramienta **Elementos** o elija la cuadrícula en la **herramienta** Diseño.</span><span class="sxs-lookup"><span data-stu-id="168ef-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="168ef-150">Puede habilitar las superposiciones persistentes para varias cuadrículas.</span><span class="sxs-lookup"><span data-stu-id="168ef-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="168ef-151">La nueva **herramienta Diseño** te permite alternar fácilmente las superposiciones de cuadrícula y configurar la apariencia y el contenido de cada una.</span><span class="sxs-lookup"><span data-stu-id="168ef-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="168ef-152">Las características están activadas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="168ef-152">The features are turned on by default.</span></span>  <span data-ttu-id="168ef-153">Para obtener más información acerca de las características, vaya a [cuadrículas CSS][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="168ef-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="168ef-154">Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [#1047356][CR1047356].</span><span class="sxs-lookup"><span data-stu-id="168ef-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="168ef-155">Además, el equipo Microsoft Edge DevTools colabora con el equipo de Chrome DevTools y la comunidad de Chromium para agregar nuevas características de herramientas de flexbox a DevTools.</span><span class="sxs-lookup"><span data-stu-id="168ef-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="168ef-156">Para obtener actualizaciones sobre las herramientas de flexbox Chromium proyecto de código abierto, vaya a Problema [#1136394][CR1136394].</span><span class="sxs-lookup"><span data-stu-id="168ef-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Herramienta de diseño con cuadrículas" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="168ef-158">**Herramienta de** diseño con cuadrículas</span><span class="sxs-lookup"><span data-stu-id="168ef-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a><span data-ttu-id="168ef-159">Personalizar accesos rápidos de teclado en Configuración</span><span class="sxs-lookup"><span data-stu-id="168ef-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="168ef-161">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="168ef-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="168ef-162">Ahora puedes personalizar el método abreviado de teclado para cualquier acción en DevTools.</span><span class="sxs-lookup"><span data-stu-id="168ef-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="168ef-163">Desde Microsoft Edge versión 84, puede elegir \*\*\*\* entre los ajustes preestablecidos Visual Studio Code **y DevTools (predeterminado)** para los [métodos abreviados de teclado.][DevtoolsCustomizeShortcuts]</span><span class="sxs-lookup"><span data-stu-id="168ef-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="168ef-164">A partir Microsoft Edge versión 87, puede activar el experimento Habilitar **editor** de métodos abreviados de teclado para personalizar aún más [los métodos abreviados de teclado.][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]</span><span class="sxs-lookup"><span data-stu-id="168ef-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span></span>  

<span data-ttu-id="168ef-165">Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a Habilitar editor de métodos abreviados de **teclado**.</span><span class="sxs-lookup"><span data-stu-id="168ef-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="168ef-166">Para obtener más información acerca de la personalización y edición de accesos directos, vaya a [Editar métodos abreviados de teclado para cualquier acción en DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span><span class="sxs-lookup"><span data-stu-id="168ef-166">For more information about customizing and editing shortcuts, navigate to [Edit keyboard shortcuts for any action in the DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].</span></span>  <span data-ttu-id="168ef-167">Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya a Problema [#174309][CR174309].</span><span class="sxs-lookup"><span data-stu-id="168ef-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Acceso directo personalizado para pausar un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="168ef-169">Acceso directo personalizado para pausar un script</span><span class="sxs-lookup"><span data-stu-id="168ef-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a><span data-ttu-id="168ef-170">Presentación de la Microsoft Edge herramientas de Visual Studio Code extensión</span><span class="sxs-lookup"><span data-stu-id="168ef-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="168ef-171">Los **elementos para Visual Studio Code** **y red** para extensiones Visual Studio Code ahora se combinan en la nueva [Microsoft Edge Developer Tools para Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extensión.</span><span class="sxs-lookup"><span data-stu-id="168ef-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="168ef-172">Use el Microsoft Edge DevTools para las siguientes actividades sin salir de Microsoft Visual Studio code.</span><span class="sxs-lookup"><span data-stu-id="168ef-172">Use the Microsoft Edge DevTools for the following activities without leaving Microsoft Visual Studio Code.</span></span>  

*   <span data-ttu-id="168ef-173">Depurar el DOM</span><span class="sxs-lookup"><span data-stu-id="168ef-173">Debug the DOM</span></span>  
*   <span data-ttu-id="168ef-174">Editar CSS</span><span class="sxs-lookup"><span data-stu-id="168ef-174">Edit CSS</span></span>  
*   <span data-ttu-id="168ef-175">Inspeccionar el tráfico de red</span><span class="sxs-lookup"><span data-stu-id="168ef-175">Inspect network traffic</span></span>  

<span data-ttu-id="168ef-176">Con la extensión, inicie Microsoft Edge, conéctese a una instancia existente del explorador o use un explorador sin cabeza directamente desde el editor.</span><span class="sxs-lookup"><span data-stu-id="168ef-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="168ef-177">Para empezar a contribuir y archivar problemas con sus comentarios sobre esta extensión, vaya a Microsoft Edge [Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span><span class="sxs-lookup"><span data-stu-id="168ef-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Uso de la extensión en la captura de pantalla del modo de explorador completo" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="168ef-179">Uso de la extensión en la captura de pantalla del modo de explorador completo</span><span class="sxs-lookup"><span data-stu-id="168ef-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Uso de la extensión en la captura de pantalla del modo sin cabeza" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="168ef-181">Uso de la extensión en la captura de pantalla del modo sin cabeza</span><span class="sxs-lookup"><span data-stu-id="168ef-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="168ef-182">Anuncios del proyecto de Chromium</span><span class="sxs-lookup"><span data-stu-id="168ef-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a><span data-ttu-id="168ef-183">Nueva herramienta WebAuthn</span><span class="sxs-lookup"><span data-stu-id="168ef-183">New WebAuthn tool</span></span>  

<span data-ttu-id="168ef-184">En versiones anteriores de Microsoft Edge, no había compatibilidad de depuración nativa de WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="168ef-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="168ef-185">Necesitaba autenticadores físicos para probar la aplicación web con la [API de autenticación web.][GithubW3cWebauthn]</span><span class="sxs-lookup"><span data-stu-id="168ef-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="168ef-186">Con la nueva **herramienta WebAuthn,** puede realizar las siguientes acciones sin el uso de autenticadores físicos.</span><span class="sxs-lookup"><span data-stu-id="168ef-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="168ef-187">Emular autenticadores</span><span class="sxs-lookup"><span data-stu-id="168ef-187">Emulate authenticators</span></span>
*   <span data-ttu-id="168ef-188">Personalizar atributos de autenticadores</span><span class="sxs-lookup"><span data-stu-id="168ef-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="168ef-189">Inspeccionar estados de autenticadores</span><span class="sxs-lookup"><span data-stu-id="168ef-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="168ef-190">Para obtener más información acerca de la característica **WebAuthn,** vaya a [Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="168ef-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="168ef-191">Puede emular autenticadores y depurar la API de autenticación [web][GithubW3cWebauthn] con la nueva herramienta [WebAuthn][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="168ef-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="168ef-192">Para abrir la **herramienta WebAuthn,** elija el icono Personalizar y **controlar DevTools** \( \) > `...` Más **herramientas**  >  **WebAuthn**.</span><span class="sxs-lookup"><span data-stu-id="168ef-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="168ef-193">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#1034663][CR1034663].</span><span class="sxs-lookup"><span data-stu-id="168ef-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Abrir la herramienta WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="168ef-195">Abrir la **herramienta WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="168ef-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Herramienta WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="168ef-197">**Herramienta WebAuthn**</span><span class="sxs-lookup"><span data-stu-id="168ef-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a><span data-ttu-id="168ef-198">Actualizaciones de la herramienta Elementos</span><span class="sxs-lookup"><span data-stu-id="168ef-198">Elements tool updates</span></span>  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a><span data-ttu-id="168ef-199">Ver el panel lateral calculado en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="168ef-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="168ef-200">Alterna el **panel Calculado** en el **panel Estilos.**</span><span class="sxs-lookup"><span data-stu-id="168ef-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="168ef-201">El **panel Calculado** del panel **Estilos** se contrae de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="168ef-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="168ef-202">Para alternar, elija el botón.</span><span class="sxs-lookup"><span data-stu-id="168ef-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="168ef-203">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#1073899][CR1073899].</span><span class="sxs-lookup"><span data-stu-id="168ef-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Abrir el panel de la barra lateral calculada" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="168ef-205">Abrir el **panel de la barra lateral calculada**</span><span class="sxs-lookup"><span data-stu-id="168ef-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Panel de barra lateral computada" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="168ef-207">**Panel de barra lateral** computada</span><span class="sxs-lookup"><span data-stu-id="168ef-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a><span data-ttu-id="168ef-208">Agrupación de propiedades CSS en el panel Calculado</span><span class="sxs-lookup"><span data-stu-id="168ef-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="168ef-209">Para ver el CSS aplicado con menos desplazamiento, agrupa las propiedades CSS por categorías en **el panel Calculado.**</span><span class="sxs-lookup"><span data-stu-id="168ef-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="168ef-210">También puede centrarse selectivamente en un conjunto de propiedades relacionadas mientras inspecciona su CSS.</span><span class="sxs-lookup"><span data-stu-id="168ef-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="168ef-211">En la **herramienta Elementos,** elija un elemento.</span><span class="sxs-lookup"><span data-stu-id="168ef-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="168ef-212">Para agrupar \(o desagrupar\) las propiedades CSS, active la **casilla Grupo.**</span><span class="sxs-lookup"><span data-stu-id="168ef-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="168ef-213">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya a Problemas [#1096230][CR1096230], [#1084673][CR1084673]y [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="168ef-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Agrupación de propiedades CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="168ef-215">Agrupación de propiedades CSS</span><span class="sxs-lookup"><span data-stu-id="168ef-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a><span data-ttu-id="168ef-216">Faro 6.4 en la herramienta Faro</span><span class="sxs-lookup"><span data-stu-id="168ef-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="168ef-217">La **herramienta Lighthouse** ahora ejecuta Lighthouse 6.4.</span><span class="sxs-lookup"><span data-stu-id="168ef-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="168ef-218">Para obtener una lista completa de los cambios, vaya a las notas [de la versión de Lighthouse][GithubGoogleChromeLighthouseReleasesV641].</span><span class="sxs-lookup"><span data-stu-id="168ef-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="168ef-219">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#772558][CR772558].</span><span class="sxs-lookup"><span data-stu-id="168ef-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <a name="performancemark-events-in-the-timings-section"></a><span data-ttu-id="168ef-220">eventos performance.mark() en la sección Timings</span><span class="sxs-lookup"><span data-stu-id="168ef-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="168ef-221">La **sección Timings de** una grabación de la herramienta [Performance][DevtoolsEvaluatePerformanceReference] marca ahora los `performance.mark()` eventos.</span><span class="sxs-lookup"><span data-stu-id="168ef-221">The **Timings section** of a recording in the [Performance][DevtoolsEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="168ef-222">Para probar esta característica y medir el rendimiento del código JavaScript, agregue `performance.mark()` eventos al código.</span><span class="sxs-lookup"><span data-stu-id="168ef-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="168ef-223">Por ejemplo, el siguiente fragmento de código agrega marcadores antes y después de un bucle que itera de 0 a `for` 1000 mediante incrementos de 7.</span><span class="sxs-lookup"><span data-stu-id="168ef-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="168ef-224">A continuación, abra la [herramienta][DevtoolsEvaluatePerformanceReference] Rendimiento y vaya a la **sección Timings** para registrar el código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="168ef-224">Then, open the [Performance][DevtoolsEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="168ef-225">Los `performance.mark()` eventos que agregó ahora se muestran en la grabación.</span><span class="sxs-lookup"><span data-stu-id="168ef-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Eventos Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="168ef-227">eventos</span><span class="sxs-lookup"><span data-stu-id="168ef-227">events</span></span>  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a><span data-ttu-id="168ef-228">Nuevos filtros de tipo de recurso y url en la herramienta Red</span><span class="sxs-lookup"><span data-stu-id="168ef-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="168ef-229">Use las palabras `resource-type` clave y nuevas de la herramienta `url` **Red** para filtrar las solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="168ef-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="168ef-230">Por ejemplo, se `resource-type:image` usa para centrarse en las solicitudes de red que son imágenes.</span><span class="sxs-lookup"><span data-stu-id="168ef-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtro de tipo de recurso" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="168ef-232">filtro de tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="168ef-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="168ef-233">Para descubrir palabras clave más especiales como y , vaya a [solicitudes de filtro por `resource-type` `url` propiedades][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="168ef-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="168ef-234">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problemas [#1121141][CR1121141] y [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="168ef-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <a name="frame-details-view-updates"></a><span data-ttu-id="168ef-235">Actualización de la vista de detalles del marco</span><span class="sxs-lookup"><span data-stu-id="168ef-235">Frame details view updates</span></span>  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a><span data-ttu-id="168ef-236">Mostrar informes de COEP y COOP en el punto de conexión</span><span class="sxs-lookup"><span data-stu-id="168ef-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="168ef-237">Vea el extremo Directiva de incrustación entre orígenes \(COEP\) y Directiva de apertura entre orígenes \(COOP\) en la sección Seguridad `reporting to` **& aislamiento.**</span><span class="sxs-lookup"><span data-stu-id="168ef-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="168ef-238">La [API de informes][MdnReportingApi] define , un nuevo encabezado HTTP, que le permite especificar los puntos de conexión del servidor para que el explorador envíe `Report-To` advertencias y errores.</span><span class="sxs-lookup"><span data-stu-id="168ef-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="168ef-239">Para revisar las actualizaciones en tiempo real de esta característica en el Chromium de código abierto, vaya a Problema [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="168ef-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="El punto de conexión de informes" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="168ef-241">El `reporting to` extremo</span><span class="sxs-lookup"><span data-stu-id="168ef-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a><span data-ttu-id="168ef-242">Mostrar el modo de solo informe DE COEP y COOP</span><span class="sxs-lookup"><span data-stu-id="168ef-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="168ef-243">DevTools ahora muestra la `report-only` etiqueta de COEP y COOP que están establecidas en `report-only` modo.</span><span class="sxs-lookup"><span data-stu-id="168ef-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="168ef-244">Para revisar las actualizaciones en tiempo real de esta característica en el Chromium de código abierto, vaya a Problema [#1051466][CR1051466].</span><span class="sxs-lookup"><span data-stu-id="168ef-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="La etiqueta de modo de solo informe" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="168ef-246">La `report-only` etiqueta de modo</span><span class="sxs-lookup"><span data-stu-id="168ef-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a><span data-ttu-id="168ef-247">Ver y corregir problemas de contraste de color en la herramienta Información general de CSS</span><span class="sxs-lookup"><span data-stu-id="168ef-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="168ef-249">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="168ef-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="168ef-250">Ahora, **la herramienta** Información general de CSS muestra una lista de elementos de la página que tienen problemas de contraste de color.</span><span class="sxs-lookup"><span data-stu-id="168ef-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="168ef-251">La siguiente página de demostración tiene un ejemplo de un problema de contraste de color.</span><span class="sxs-lookup"><span data-stu-id="168ef-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="168ef-252">CSS Overview Accessible Colors Demo</span><span class="sxs-lookup"><span data-stu-id="168ef-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="168ef-253">Para habilitar este \*\*\*\* experimento, en  >  **Configuración,** seleccione la casilla **Información general de CSS.**</span><span class="sxs-lookup"><span data-stu-id="168ef-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="168ef-254">Para ver una lista de elementos que tienen un problema de contraste de color, en **Problemas de contraste**, elija **Texto**.</span><span class="sxs-lookup"><span data-stu-id="168ef-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="168ef-255">Para abrir el elemento en la **herramienta Elementos,** elija un elemento en la lista.</span><span class="sxs-lookup"><span data-stu-id="168ef-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="168ef-256">Para ayudar a solucionar problemas de contraste, el Microsoft Edge DevTools [proporciona automáticamente sugerencias de color.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]</span><span class="sxs-lookup"><span data-stu-id="168ef-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="168ef-257">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#1120316][CR1120316].</span><span class="sxs-lookup"><span data-stu-id="168ef-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problemas de contraste de color bajo" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="168ef-259">Problemas de contraste de color bajo</span><span class="sxs-lookup"><span data-stu-id="168ef-259">Low color contrast issues</span></span>  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="168ef-260">Descargar los canales de vista previa de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="168ef-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="168ef-261">Si está en Windows o macOS, considere la posibilidad de usar los canales [Microsoft Edge vista previa][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="168ef-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="168ef-262">Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="168ef-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="168ef-263">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="168ef-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsTool]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Desuso del panel Propiedades en la herramienta Elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugerencia de color accesible en el panel Estilos: novedades de DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsConsoleIndex]: ../../../console/index.md "Use la consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]:  ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Elemento o objeto JavaScript elegido recientemente: referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalización de accesos rápidos de teclado en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Edite los métodos abreviados de teclado para cualquier acción en el archivo DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReference]: ../../../evaluate-performance/reference.md "Referencia de análisis de rendimiento | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: ../../../experimental-features/index.md#emulation-support-dual-screen-mode "Emulación: admite el modo de pantalla dual: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features.md#enable-experimental-apis "Habilitar API experimentales: características experimentales | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: .. /.. /.. /experimental-features/index.md#enable-new-css-grid-debugging-features "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: .. /.. /.. /experimental-features/index.md#enable-network-console "Enable Network Console - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#enable-source-order-viewer "Enable Source Order Viewer - Experimental features | Microsoft Docs&quot; [DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: .. /.. /.. /experimental-features/index.md#testing-on-foldable-and-dual-screen-devices &quot;Testing on foldable and dual-screen devices - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsConsoleApiTable]: .. /.. /.. /console/api.md#table "table- Console API reference | Microsoft Docs"  
[DevtoolsCoverageIndex]: .. /.. /.. /coverage/index.md "Buscar código JavaScript y CSS sin usar con la pestaña Cobertura en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: .. /.. /.. /css/grid.md "Inspect CSS Grid | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: .. /.. /.. /customize/index.md#drawer "Drawer- Customize Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: .. /.. /.. /customize/index.md#settings "Configuración: Personalizar Microsoft Edge devTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: .. /.. /.. /evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tab "Analyze rendering performance with the Rendering tab - Performance Analysis Reference | Microsoft Docs"  
[DevtoolsMediaIndex]: .. /.. /.. /media/index.md "Ver y depurar la información de los reproductores multimedia | Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: .. /.. /.. /network/reference.md#filter-requests-by-properties "Filter requests by properties - Network Analysis reference | Microsoft Docs"  
[DevtoolsWebauthnIndex]: .. /.. /.. /webauthn/index.md "Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Herramientas para Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar los métodos abreviados de teclado o los enlaces de teclas | Chromium errores"
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la versión más reciente de | Chromium errores"  
[CR1034663]: https://crbug.com/1034663 "Crear un front-end para la API de prueba de WebAuthn | Chromium errores"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS Grid/Flexbox/Table | Chromium errores"  
[CR1051466]: https://crbug.com/1051466 "Admite la depuración de COOP/COEP en DevTools | Chromium errores"  
[CR1073899]: https://crbug.com/1073899 "La pestaña Estilo calculado desaparece en modo de respuesta | Chromium errores"  
[CR1075732]: https://crbug.com/1075732 "Personalización de DevTools: pestañas móviles | Chromium errores"  
[CR1084673]: https://crbug.com/1084673 "DevTools: mejore la forma en que presentamos propiedades personalizadas css ((aka). variables CSS) y sus valores | Chromium errores"  
[CR1093687]: https://crbug.com/1093687 "Crear herramienta para crear y reproducir solicitudes de red sintéticas | Chromium errores"  
[CR1096230]: https://crbug.com/1096230 "Agrupar propiedades CSS por categorías en el panel Estilos calculados | Chromium errores"  
[CR1104188]: https://crbug.com/1104188 "La búsqueda de herramientas de red no encuentra resultados al buscar direcciones URL | Chromium errores"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: mejorar la pestaña Estilos calculados | Chromium errores"  
[CR1120316]: https://crbug.com/1120316 "Resalte el contraste malo en Información general de CSS > colores | Chromium Errores"  
[CR1121141]: https://crbug.com/1121141 "Permitir el filtrado por tipo de recurso en el registro de red | Chromium errores"  
[CR1121312]: https://crbug.com/1121312 "Configuración debe quitarse del menú Más herramientas | Chromium errores"  
[CR1136394]: https://crbug.com/1136394 "Herramientas flexbox | Chromium Errores"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Localización V2 | Chromium errores"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Api de informes | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1: GoogleChrome/lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Hola! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato de colección postman v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "OpenAPI Specification | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="168ef-316">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="168ef-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="168ef-317">La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-87) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).</span><span class="sxs-lookup"><span data-stu-id="168ef-317">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-87) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="168ef-319">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="168ef-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
