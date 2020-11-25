---
description: Nuevas herramientas de depuración de cuadrícula CSS, herramienta webauthn, herramientas móviles y panel de barra lateral calculado.
title: Novedades de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b972468ad21f3a64985a00aecbe29836032b3334
ms.sourcegitcommit: 080759f68a0a158f10dc20d20c14e222ace1be84
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/24/2020
ms.locfileid: "11190008"
---
# <span data-ttu-id="10410-104">Novedades de DevTools (Microsoft Edge 87)</span><span class="sxs-lookup"><span data-stu-id="10410-104">What's New In DevTools (Microsoft Edge 87)</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <span data-ttu-id="10410-105">Mejorar la localización de DevTools</span><span class="sxs-lookup"><span data-stu-id="10410-105">Improving DevTools localization</span></span>  

<span data-ttu-id="10410-106">Para satisfacer sus necesidades de traducción, el equipo de Microsoft Edge DevTools se centró en mejorar la calidad de la traducción.</span><span class="sxs-lookup"><span data-stu-id="10410-106">To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.</span></span>  <span data-ttu-id="10410-107">A partir de la versión 87 de Microsoft Edge, varias cadenas y términos están bloqueados y no cambian incluso cuando el resto de las DevTools se muestran en otros idiomas.</span><span class="sxs-lookup"><span data-stu-id="10410-107">Starting in Microsoft Edge version 87, several strings and terms are locked and do not change even when the rest of the DevTools are displayed in other languages.</span></span>  <span data-ttu-id="10410-108">La lista de cadenas y términos afectados incluye lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="10410-108">The list of affected strings and terms include the following.</span></span>  

*   <span data-ttu-id="10410-109">Las cadenas de la herramienta **Lighthouse** .</span><span class="sxs-lookup"><span data-stu-id="10410-109">The strings in the **Lighthouse** tool.</span></span>  
*   <span data-ttu-id="10410-110">El término `service worker` .</span><span class="sxs-lookup"><span data-stu-id="10410-110">The term `service worker`.</span></span>  
*   <span data-ttu-id="10410-111">Algunos de los filtros de herramientas de **red** , como `URL` ,, `XHR` `JS` y `CSS` .</span><span class="sxs-lookup"><span data-stu-id="10410-111">Some of the **Network** tool filters such as `URL`, `XHR`, `JS`, and `CSS`.</span></span>  
*   <span data-ttu-id="10410-112">La API de utilidades de consola de [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] .</span><span class="sxs-lookup"><span data-stu-id="10410-112">The [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] Console Utilities API.</span></span>  
    
<span data-ttu-id="10410-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] está disponible en la [consola](/microsoft-edge/devtools-guide-chromium/console/index.md) para los usuarios de versiones localizadas de la DevTools.</span><span class="sxs-lookup"><span data-stu-id="10410-113">[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] is now available in the [Console](/microsoft-edge/devtools-guide-chromium/console/index.md) for users on localized versions of the DevTools.</span></span>   <span data-ttu-id="10410-114">Gracias por ayudar a la comunidad de programadores de la globalización de mejorar la localización de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="10410-114">Thank you to the global developer community for helping improve localization of the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="10410-115">Sigue [enviando comentarios sobre la calidad de la localización](#getting-in-touch-with-microsoft-edge-devtools-team) para mejorar la compatibilidad con DevTools en todas las configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="10410-115">Continue to [send feedback on localization quality](#getting-in-touch-with-microsoft-edge-devtools-team) to improve support for DevTools in all locales.</span></span>  <span data-ttu-id="10410-116">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1136655][CR1136655]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-116">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1136655][CR1136655].</span></span>  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   <span data-ttu-id="10410-118">Panel de **red** con filtros no localizados</span><span class="sxs-lookup"><span data-stu-id="10410-118">**Network** pane with non-localized filters</span></span>  
:::image-end:::  

## <span data-ttu-id="10410-119">Mover herramientas entre los paneles superior e inferior</span><span class="sxs-lookup"><span data-stu-id="10410-119">Move tools between top and bottom panels</span></span>  

<span data-ttu-id="10410-120">DevTools ahora es compatible con las herramientas de movimiento entre los paneles superior e inferior.</span><span class="sxs-lookup"><span data-stu-id="10410-120">DevTools now supports moving tools between the top and bottom panels.</span></span>  <span data-ttu-id="10410-121">Personalice su DevTools y mejore su productividad viendo cualquier combinación de dos herramientas al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="10410-121">Customize your DevTools and improve your productivity by viewing any combination of two tools at the same time.</span></span>  <span data-ttu-id="10410-122">Por ejemplo, vea los **elementos** y las herramientas de **orígenes** al mismo tiempo \ (para ello, mueva la herramienta de **fuentes** al final \).</span><span class="sxs-lookup"><span data-stu-id="10410-122">For example, view the **Elements** and the **Sources** tools at the same time \(by moving the **Sources** tool to the bottom\).</span></span>  <span data-ttu-id="10410-123">Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el [#1075732][CR1075732]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-123">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1075732][CR1075732].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="10410-124">Para mover cualquier herramienta superior a la parte inferior, desplace el puntero sobre una pestaña, abra el menú contextual \ (haga clic con el botón derecho \) y elija **mover a la parte inferior**.</span><span class="sxs-lookup"><span data-stu-id="10410-124">To move any top tool to the bottom, hover on a tab, open the contextual menu \(right-click\), and choose **Move to bottom**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Mover a la parte inferior" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         <span data-ttu-id="10410-126">Mover a la parte inferior</span><span class="sxs-lookup"><span data-stu-id="10410-126">Move to bottom</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="10410-127">Para mover cualquier herramienta inferior a la parte superior, desplace el puntero sobre una pestaña, abra el menú contextual \ (haga clic con el botón derecho \) y elija **mover a la parte superior**.</span><span class="sxs-lookup"><span data-stu-id="10410-127">To move any bottom tool to the top, hover on a tab, open the contextual menu \(right-click\), and choose **Move to top**.</span></span>  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Mover al principio" lightbox="../../media/2020/10/move-to-top.msft.png":::
         <span data-ttu-id="10410-129">Mover al principio</span><span class="sxs-lookup"><span data-stu-id="10410-129">Move to top</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="10410-130">Guardar y exportar con la consola de red</span><span class="sxs-lookup"><span data-stu-id="10410-130">Save and export using the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="10410-132">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="10410-132">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="10410-133">La herramienta de **consola de red** ahora tiene mayor compatibilidad con los esquemas [v 2.1][PostmanSchemaJsonCollectionv210Index] y [OpenAPI V2][SwaggerSpecificationV2] .</span><span class="sxs-lookup"><span data-stu-id="10410-133">The **Network Console** tool now has improved compatibility with the [Postman v2.1][PostmanSchemaJsonCollectionv210Index] and [OpenAPI v2][SwaggerSpecificationV2] schemas.</span></span>  <span data-ttu-id="10410-134">Para habilitar el experimento, navegue para [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla que se encuentra junto a **Habilitar consola de red**.</span><span class="sxs-lookup"><span data-stu-id="10410-134">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable Network Console**.</span></span>  <span data-ttu-id="10410-135">Para obtener más información sobre la **consola de red**, vaya a habilitar la [característica experimental consola de red][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span><span class="sxs-lookup"><span data-stu-id="10410-135">For more information about the **Network Console**, navigate to [Enable Network Console Experimental feature][DevtoolsExperimentalFeaturesEnableNetworkConsole].</span></span>  <span data-ttu-id="10410-136">Este experimento ahora es compatible con las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="10410-136">This experiment now supports the following actions.</span></span>  

*   <span data-ttu-id="10410-137">Guardar y exportar colecciones y entornos.</span><span class="sxs-lookup"><span data-stu-id="10410-137">Save and export Collections and Environments.</span></span>  
*   <span data-ttu-id="10410-138">Edite y exporte conjuntos de variables de entorno dentro de la herramienta de **consola de red** .</span><span class="sxs-lookup"><span data-stu-id="10410-138">Edit and export sets of environment variables within the **Network Console** tool.</span></span>  
    
<span data-ttu-id="10410-139">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1093687][CR1093687]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-139">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1093687][CR1093687].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Escriba un nombre para el nuevo entorno" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         <span data-ttu-id="10410-141">Escriba un nombre para el nuevo entorno</span><span class="sxs-lookup"><span data-stu-id="10410-141">Enter name for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Elegir formato para el nuevo entorno" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         <span data-ttu-id="10410-143">Elegir formato para el nuevo entorno</span><span class="sxs-lookup"><span data-stu-id="10410-143">Choose format for the new environment</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="10410-144">Herramientas de cuadrícula CSS mejoradas</span><span class="sxs-lookup"><span data-stu-id="10410-144">Improved CSS Grid tooling</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="10410-146">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="10410-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="10410-147">Ahora, Microsoft Edge DevTools es compatible con las siguientes características para inspeccionar, visualizar y depurar las cuadrículas de CSS.</span><span class="sxs-lookup"><span data-stu-id="10410-147">The Microsoft Edge DevTools now support the following features for inspecting, viewing, and debugging your CSS grids.</span></span>  

*   <span data-ttu-id="10410-148">Mostrar una superposición de cuadrícula simplificada con la herramienta **inspeccionar** , u obtener información más detallada con las superposiciones persistentes.</span><span class="sxs-lookup"><span data-stu-id="10410-148">Display a simplified grid overlay using the **Inspect** tool, or get more detailed information with persistent overlays.</span></span>  
*   <span data-ttu-id="10410-149">Para habilitar las superposiciones de cuadrícula persistentes, elija el icono de cuadrícula junto a un elemento de contenedor de cuadrícula en la herramienta **elementos** o elija la cuadrícula en la herramienta de **diseño** .</span><span class="sxs-lookup"><span data-stu-id="10410-149">To enable persistent grid overlays, choose the grid icon next to a grid container element in the **Elements** tool or choose the grid in the **Layout** tool.</span></span>  
*   <span data-ttu-id="10410-150">Puede habilitar superposiciones persistentes para varias cuadrículas.</span><span class="sxs-lookup"><span data-stu-id="10410-150">You may enable persistent overlays for multiple grids.</span></span>  
*   <span data-ttu-id="10410-151">La nueva herramienta de **diseño** le permite alternar fácilmente las superposiciones de cuadrícula y configurar la apariencia y el contenido de cada una de ellas.</span><span class="sxs-lookup"><span data-stu-id="10410-151">The new **Layout** tool allows you to easily toggle grid overlays and configure the appearance and the content for each.</span></span>  
    
<span data-ttu-id="10410-152">Las características están activadas de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="10410-152">The features are turned on by default.</span></span>  <span data-ttu-id="10410-153">Para obtener más información sobre las características, vaya a [cuadrículas de CSS][DevtoolsCssGrid].</span><span class="sxs-lookup"><span data-stu-id="10410-153">For more information about the features, navigate to [CSS grids][DevtoolsCssGrid].</span></span>  <span data-ttu-id="10410-154">Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el [#1047356][CR1047356]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-154">To review the history of this feature in the Chromium open-source project, navigate to Issue [#1047356][CR1047356].</span></span>  <span data-ttu-id="10410-155">Además, el equipo de Microsoft Edge DevTools está colaborando con el equipo de Chrome DevTools y la comunidad de cromo para agregar nuevas características de herramientas de Flexbox a DevTools.</span><span class="sxs-lookup"><span data-stu-id="10410-155">Additionally, the Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new flexbox tooling features to DevTools.</span></span>  <span data-ttu-id="10410-156">Para obtener las actualizaciones de las herramientas de Flexbox en el proyecto de origen abierto de cromo, navegue hasta el [#1136394][CR1136394]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-156">For updates on flexbox tooling in the Chromium open-source project, navigate to Issue [#1136394][CR1136394].</span></span>  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Herramienta de diseño con cuadrículas" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   <span data-ttu-id="10410-158">Herramienta de **diseño** con cuadrículas</span><span class="sxs-lookup"><span data-stu-id="10410-158">**Layout** tool with grids</span></span>  
:::image-end:::  

## <span data-ttu-id="10410-159">Personalizar métodos abreviados de teclado en la configuración</span><span class="sxs-lookup"><span data-stu-id="10410-159">Customize keyboard shortcuts in Settings</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="10410-161">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="10410-161">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="10410-162">Ahora puede personalizar el método abreviado de teclado para cualquier acción en el DevTools.</span><span class="sxs-lookup"><span data-stu-id="10410-162">You are now able to customize the keyboard shortcut for any action in the DevTools.</span></span>  <span data-ttu-id="10410-163">Desde Microsoft Edge versión 84, puede elegir entre los valores preestablecidos de **Visual Studio Code** y **DevTools (predeterminado)** para los [métodos abreviados de teclado][DevtoolsCustomizeShortcuts].</span><span class="sxs-lookup"><span data-stu-id="10410-163">Since Microsoft Edge version 84, you are able to choose between **Visual Studio Code** and **DevTools (default)** presets for [keyboard shortcuts][DevtoolsCustomizeShortcuts].</span></span>  <span data-ttu-id="10410-164">A partir de la versión 87 de Microsoft Edge, puede activar el experimento **Habilitar editor de método abreviado de teclado** para personalizar aún más los [métodos abreviados de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="10410-164">Starting in Microsoft Edge version 87, you may turn on the **Enable keyboard shortcut editor** experiment to further [customize keyboard shortcuts][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  

<span data-ttu-id="10410-165">Para habilitar el experimento, navegue para [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a **Habilitar el editor de métodos abreviados de teclado**.</span><span class="sxs-lookup"><span data-stu-id="10410-165">To enable the experiment, navigate to [Turn on Experimental features][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] and choose the checkbox next to **Enable keyboard shortcut editor**.</span></span>  <span data-ttu-id="10410-166">Para obtener más información sobre la personalización y la edición de accesos directos, vaya a [Habilitar la característica experimental editor de método abreviado de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span><span class="sxs-lookup"><span data-stu-id="10410-166">For more information about customizing and editing shortcuts, navigate to [Enable keyboard shortcut editor Experimental feature][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].</span></span>  <span data-ttu-id="10410-167">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#174309][CR174309]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-167">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#174309][CR174309].</span></span>  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Acceso directo personalizado para pausar un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   <span data-ttu-id="10410-169">Acceso directo personalizado para pausar un script</span><span class="sxs-lookup"><span data-stu-id="10410-169">Custom shortcut for pausing a script</span></span>  
:::image-end:::  

## <span data-ttu-id="10410-170">Presentamos la extensión de código de las herramientas de Microsoft Edge para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="10410-170">Introducing the Microsoft Edge Tools for Visual Studio Code extension</span></span>  

<span data-ttu-id="10410-171">Los **elementos para Visual Studio Code** y las extensiones **de código de Visual Studio** ahora se combinan en la nueva extensión [de código de las herramientas de desarrollo de Microsoft Edge para Visual Studio][VisualStudioCodeMarketplaceMsEdgedevtools] .</span><span class="sxs-lookup"><span data-stu-id="10410-171">The **Elements for Visual Studio Code** and **Network for Visual Studio Code** extensions are now merged into the new [Microsoft Edge Developer Tools for Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extension.</span></span>  <span data-ttu-id="10410-172">Usa el DevTools de Microsoft Edge para las siguientes actividades sin salir de Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="10410-172">Use the Microsoft Edge DevTools for the following activities without leaving Visual Studio Code.</span></span>  

*   <span data-ttu-id="10410-173">Depurar DOM</span><span class="sxs-lookup"><span data-stu-id="10410-173">Debug the DOM</span></span>  
*   <span data-ttu-id="10410-174">Editar CSS</span><span class="sxs-lookup"><span data-stu-id="10410-174">Edit CSS</span></span>  
*   <span data-ttu-id="10410-175">Inspeccionar el tráfico de red</span><span class="sxs-lookup"><span data-stu-id="10410-175">Inspect network traffic</span></span>  

<span data-ttu-id="10410-176">Con la extensión, Inicie Microsoft Edge, conéctese a una instancia existente del explorador o use un explorador sin cabeza directamente desde el editor.</span><span class="sxs-lookup"><span data-stu-id="10410-176">With the extension, launch Microsoft Edge, connect to an existing instance of the browser, or use a headless browser directly from your editor.</span></span>  <span data-ttu-id="10410-177">Para empezar a colaborar y archivar problemas con sus comentarios sobre esta extensión, navegue hasta el repositorio [de código de las herramientas de desarrollo de Microsoft Edge para Visual Studio][GithubMicrosoftVscodeEdgeDevtools] en github.</span><span class="sxs-lookup"><span data-stu-id="10410-177">To start contributing and filing issues with your feedback about this extension, navigate to the [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Uso de la extensión en el modo de navegador completo" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         <span data-ttu-id="10410-179">Uso de la extensión en el modo de navegador completo</span><span class="sxs-lookup"><span data-stu-id="10410-179">Using the extension in full browser mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Uso de la extensión en modo de pantalla desatendida" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         <span data-ttu-id="10410-181">Uso de la extensión en modo de pantalla desatendida</span><span class="sxs-lookup"><span data-stu-id="10410-181">Using the extension in headless mode screenshot</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="10410-182">Anuncios del proyecto de cromo</span><span class="sxs-lookup"><span data-stu-id="10410-182">Announcements from the Chromium project</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <span data-ttu-id="10410-183">Nueva herramienta webauthn</span><span class="sxs-lookup"><span data-stu-id="10410-183">New WebAuthn tool</span></span>  

<span data-ttu-id="10410-184">En versiones anteriores de Microsoft Edge, no había ninguna compatibilidad nativa de depuración de webauthr.</span><span class="sxs-lookup"><span data-stu-id="10410-184">In earlier versions of Microsoft Edge, there was no native WebAuthn debugging support.</span></span>  <span data-ttu-id="10410-185">Necesitaba autenticadores físicos para probar la aplicación web con la [API de autenticación Web][GithubW3cWebauthn].</span><span class="sxs-lookup"><span data-stu-id="10410-185">You needed physical authenticators to test your web application with the [Web Authentication API][GithubW3cWebauthn].</span></span>  <span data-ttu-id="10410-186">Con la nueva herramienta **Webauthn** , podrá realizar las siguientes acciones sin usar ningún autenticador físico.</span><span class="sxs-lookup"><span data-stu-id="10410-186">With the new **WebAuthn** tool, you are able to do the following actions without the use of any physical authenticators.</span></span>

*   <span data-ttu-id="10410-187">Emular autenticadores</span><span class="sxs-lookup"><span data-stu-id="10410-187">Emulate authenticators</span></span>
*   <span data-ttu-id="10410-188">Personalizar atributos de autenticadores</span><span class="sxs-lookup"><span data-stu-id="10410-188">Customize attributes of authenticators</span></span>
*   <span data-ttu-id="10410-189">Inspeccionar Estados de autenticadores</span><span class="sxs-lookup"><span data-stu-id="10410-189">Inspect states of authenticators</span></span>
    
<span data-ttu-id="10410-190">Para obtener más información sobre la característica **Webauthn** , vaya a [emular autenticadores y depurar webauthn en Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span><span class="sxs-lookup"><span data-stu-id="10410-190">For more information about the **WebAuthn** feature, navigate to [Emulate authenticators and debug WebAuthn in Microsoft Edge DevTools][DevtoolsWebauthnIndex].</span></span>  

<span data-ttu-id="10410-191">Puede emular autenticadores y depurar la [API de autenticación Web][GithubW3cWebauthn] con la nueva herramienta [webauthn][DevtoolsWebauthnIndex] .</span><span class="sxs-lookup"><span data-stu-id="10410-191">You are able to emulate authenticators and debug the [Web Authentication API][GithubW3cWebauthn] with the new [WebAuthn][DevtoolsWebauthnIndex] tool.</span></span>  <span data-ttu-id="10410-192">Para abrir la herramienta **webauthn** , elija **el icono personalizar y controlar DevTools** \ ( `...` \) > **más herramientas**  >  **webauthn**.</span><span class="sxs-lookup"><span data-stu-id="10410-192">To open the **WebAuthn** tool, choose **the Customize and control DevTools** \(`...`\) icon > **More tools** > **WebAuthn**.</span></span>  <span data-ttu-id="10410-193">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1034663][CR1034663]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-193">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1034663][CR1034663].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Abrir la herramienta webauthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         <span data-ttu-id="10410-195">Abrir la herramienta **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="10410-195">Open the **WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Herramienta webauthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         <span data-ttu-id="10410-197">Herramienta **Webauthn**</span><span class="sxs-lookup"><span data-stu-id="10410-197">**WebAuthn** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="10410-198">Actualizaciones de la herramienta elementos</span><span class="sxs-lookup"><span data-stu-id="10410-198">Elements tool updates</span></span>  

#### <span data-ttu-id="10410-199">Ver el panel de la barra lateral calculado en el panel estilos</span><span class="sxs-lookup"><span data-stu-id="10410-199">View the Computed sidebar pane in the Styles pane</span></span>  

<span data-ttu-id="10410-200">Activar o desactivar el panel **calculado** en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="10410-200">Toggle the **Computed** pane in the **Styles** pane.</span></span>  <span data-ttu-id="10410-201">El panel **calculado** del panel **estilos** está contraído de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="10410-201">The **Computed** pane in the **Styles** pane is collapsed by default.</span></span>  <span data-ttu-id="10410-202">Para activarla, elija el botón.</span><span class="sxs-lookup"><span data-stu-id="10410-202">To toggle it, choose the button.</span></span>  <span data-ttu-id="10410-203">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1073899][CR1073899]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-203">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1073899][CR1073899].</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Abrir el panel de la barra lateral calculado" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         <span data-ttu-id="10410-205">Abrir el panel de la **barra lateral calculado**</span><span class="sxs-lookup"><span data-stu-id="10410-205">Open the **Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Panel de barra lateral calculado" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         <span data-ttu-id="10410-207">Panel de **barra lateral calculado**</span><span class="sxs-lookup"><span data-stu-id="10410-207">**Computed sidebar** pane</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <span data-ttu-id="10410-208">Agrupar las propiedades de CSS en el panel calculado</span><span class="sxs-lookup"><span data-stu-id="10410-208">Grouping CSS properties in the Computed panel</span></span>  

<span data-ttu-id="10410-209">Para ver la CSS aplicada con menos desplazamiento, Agrupe las propiedades de CSS por categorías en el panel **calculado** .</span><span class="sxs-lookup"><span data-stu-id="10410-209">To view your applied CSS with less scrolling, group the CSS properties by categories in the **Computed** pane.</span></span>  <span data-ttu-id="10410-210">También puede concentrarse selectivamente en un conjunto de propiedades relacionadas mientras inspecciona su CSS.</span><span class="sxs-lookup"><span data-stu-id="10410-210">You may also selectively focus on a set of related properties while you inspect your CSS.</span></span>  <span data-ttu-id="10410-211">Desde la herramienta **elementos** , elija un elemento.</span><span class="sxs-lookup"><span data-stu-id="10410-211">From the **Elements** tool, choose an element.</span></span>  <span data-ttu-id="10410-212">Para agrupar \ (o desagrupar \) las propiedades de CSS, marque la casilla de verificación de **Grupo** .</span><span class="sxs-lookup"><span data-stu-id="10410-212">To group \(or ungroup\) the CSS properties, toggle the **Group** checkbox.</span></span>  <span data-ttu-id="10410-213">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a problemas [#1096230][CR1096230], [#1084673][CR1084673]y [#1106251][CR1106251].</span><span class="sxs-lookup"><span data-stu-id="10410-213">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1096230][CR1096230], [#1084673][CR1084673], and [#1106251][CR1106251].</span></span>  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Agrupar propiedades CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   <span data-ttu-id="10410-215">Agrupar propiedades CSS</span><span class="sxs-lookup"><span data-stu-id="10410-215">Grouping CSS properties</span></span>  
:::image-end:::  

### <span data-ttu-id="10410-216">Lighthouse 6,4 en la herramienta Lighthouse</span><span class="sxs-lookup"><span data-stu-id="10410-216">Lighthouse 6.4 in the Lighthouse tool</span></span>  

<span data-ttu-id="10410-217">La herramienta **Lighthouse** se ejecuta ahora Lighthouse 6,4.</span><span class="sxs-lookup"><span data-stu-id="10410-217">The **Lighthouse** tool is now running Lighthouse 6.4.</span></span>  <span data-ttu-id="10410-218">Para obtener una lista completa de los cambios, vaya a las notas de la [versión de Lighthouse][GithubGoogleChromeLighthouseReleasesV641].</span><span class="sxs-lookup"><span data-stu-id="10410-218">For a full list of changes, navigate to the [Lighthouse release notes][GithubGoogleChromeLighthouseReleasesV641].</span></span>  <span data-ttu-id="10410-219">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#772558][CR772558]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-219">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#772558][CR772558].</span></span>  

### <span data-ttu-id="10410-220">eventos performance. Mark () en la sección intervalos</span><span class="sxs-lookup"><span data-stu-id="10410-220">performance.mark() events in the Timings section</span></span>  

<span data-ttu-id="10410-221">La **sección intervalos** de una grabación en la herramienta [rendimiento][DevtoolsGuideChromiumEvaluatePerformanceReference] marca ahora los `performance.mark()` eventos.</span><span class="sxs-lookup"><span data-stu-id="10410-221">The **Timings section** of a recording in the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool now marks `performance.mark()` events.</span></span>  <span data-ttu-id="10410-222">Para probar esta característica y medir el rendimiento de su código de JavaScript, agregue `performance.mark()` eventos al código.</span><span class="sxs-lookup"><span data-stu-id="10410-222">To try this feature and measure the performance of your JavaScript code, add `performance.mark()` events to your code.</span></span>  <span data-ttu-id="10410-223">Por ejemplo, el siguiente fragmento de código agrega marcadores antes y después de un `for` bucle que itera de 0 a 1000 con incrementos de 7.</span><span class="sxs-lookup"><span data-stu-id="10410-223">For example, the following code snippet adds markers before and after a `for` loop that iterates from 0 to 1000 using increments of 7.</span></span>  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

<span data-ttu-id="10410-224">Después, abra la herramienta [rendimiento][DevtoolsGuideChromiumEvaluatePerformanceReference] y vaya a la **sección intervalos** para grabar el código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10410-224">Then, open the [Performance][DevtoolsGuideChromiumEvaluatePerformanceReference] tool and navigate to the **Timings section** to record your JavaScript code.</span></span>  <span data-ttu-id="10410-225">Los `performance.mark()` eventos que ha agregado se muestran ahora en la grabación.</span><span class="sxs-lookup"><span data-stu-id="10410-225">The `performance.mark()` events you added are now displayed in the recording.</span></span>  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Rendimiento. marcar eventos" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` <span data-ttu-id="10410-227">ceso</span><span class="sxs-lookup"><span data-stu-id="10410-227">events</span></span>  
:::image-end:::  

### <span data-ttu-id="10410-228">Nuevos filtros de recursos URL y tipos de recursos en la herramienta red</span><span class="sxs-lookup"><span data-stu-id="10410-228">New resource-type and url filters in the Network tool</span></span>  

<span data-ttu-id="10410-229">Use las `resource-type` `url` palabras clave New y keyword de la herramienta **red** para filtrar solicitudes de red.</span><span class="sxs-lookup"><span data-stu-id="10410-229">Use the new `resource-type` and `url` keywords in the **Network** tool to filter network requests.</span></span>  <span data-ttu-id="10410-230">Por ejemplo, use `resource-type:image` para centrarse en las solicitudes de red que son imágenes.</span><span class="sxs-lookup"><span data-stu-id="10410-230">For example, use `resource-type:image` to focus on the network requests that are images.</span></span>  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtro de tipo de recurso" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   <span data-ttu-id="10410-232">filtro de tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="10410-232">resource-type filter</span></span>  
:::image-end:::  

<span data-ttu-id="10410-233">Para descubrir más palabras clave especiales como `resource-type` y `url` , vaya a [filtrar las solicitudes por propiedades][DevtoolsNetworkReferenceFilterRequestsProperties].</span><span class="sxs-lookup"><span data-stu-id="10410-233">To discover more special keywords such as `resource-type` and `url`, navigate to [filter requests by properties][DevtoolsNetworkReferenceFilterRequestsProperties].</span></span>  <span data-ttu-id="10410-234">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a problemas [#1121141][CR1121141] y [#1104188][CR1104188].</span><span class="sxs-lookup"><span data-stu-id="10410-234">To review real-time updates on this feature in the Chromium open-source project, navigate to Issues [#1121141][CR1121141] and [#1104188][CR1104188].</span></span>  

### <span data-ttu-id="10410-235">Actualización de la vista de detalles del marco</span><span class="sxs-lookup"><span data-stu-id="10410-235">Frame details view updates</span></span>  

#### <span data-ttu-id="10410-236">Mostrar informes de COEP y de COOP al punto final</span><span class="sxs-lookup"><span data-stu-id="10410-236">Display COEP and COOP reporting to endpoint</span></span>  

<span data-ttu-id="10410-237">Ver la Directiva de Embedder de origen cruzado \ (COEP \) y la Directiva de apertura cruzada de origen \ (COOP \) `reporting to` en la sección **aislamiento del & de seguridad** .</span><span class="sxs-lookup"><span data-stu-id="10410-237">View the Cross-Origin Embedder Policy \(COEP\) and Cross-Origin Opener Policy \(COOP\) `reporting to` endpoint under the **Security & Isolation** section.</span></span>  <span data-ttu-id="10410-238">La [API de informes][MdnReportingApi] define `Report-To` , un nuevo encabezado HTTP, que le ofrece una manera de especificar los puntos de conexión de servidor para que el explorador envíe advertencias y errores.</span><span class="sxs-lookup"><span data-stu-id="10410-238">The [Reporting API][MdnReportingApi] defines `Report-To`, a new HTTP header, that gives you a way to specify the server endpoints for the browser to send warnings and errors.</span></span>  <span data-ttu-id="10410-239">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1051466][CR1051466]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-239">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="El reporting al punto de conexión" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   <span data-ttu-id="10410-241">El `reporting to` punto final</span><span class="sxs-lookup"><span data-stu-id="10410-241">The `reporting to` endpoint</span></span>  
:::image-end:::  

#### <span data-ttu-id="10410-242">Modo de solo informe de COEP y de COOP</span><span class="sxs-lookup"><span data-stu-id="10410-242">Display COEP and COOP report-only mode</span></span>  

<span data-ttu-id="10410-243">DevTools ahora Mostrar la `report-only` etiqueta de COEP y Coop que están establecidas en `report-only` mode.</span><span class="sxs-lookup"><span data-stu-id="10410-243">DevTools now display the `report-only` label for COEP and COOP that are set to `report-only` mode.</span></span>  <span data-ttu-id="10410-244">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1051466][CR1051466]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-244">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1051466][CR1051466].</span></span>  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Etiqueta de modo de solo informe" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   <span data-ttu-id="10410-246">La `report-only` etiqueta de modo</span><span class="sxs-lookup"><span data-stu-id="10410-246">The `report-only` mode label</span></span>  
:::image-end:::  

### <span data-ttu-id="10410-247">Ver y corregir problemas de contraste de color en la herramienta de información general de CSS</span><span class="sxs-lookup"><span data-stu-id="10410-247">View and fix color contrast issues in the CSS Overview tool</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   <span data-ttu-id="10410-249">Característica experimental</span><span class="sxs-lookup"><span data-stu-id="10410-249">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="10410-250">La herramienta de **información general de CSS** ahora muestra una lista de elementos en la página que tienen problemas de contraste de color.</span><span class="sxs-lookup"><span data-stu-id="10410-250">The **CSS Overview** tool now displays a list of elements on your page that have color contrast issues.</span></span>  <span data-ttu-id="10410-251">La siguiente página de demostración tiene un ejemplo de un problema de contraste de color.</span><span class="sxs-lookup"><span data-stu-id="10410-251">The following demo page has an example of a color contrast issue.</span></span>  

[<span data-ttu-id="10410-252">Demostración de colores accesibles de CSS</span><span class="sxs-lookup"><span data-stu-id="10410-252">CSS Overview Accessible Colors Demo</span></span>][GlitchCssOverviewAccessibleColorsDemo]  

<span data-ttu-id="10410-253">Para habilitar este experimento, en **Settings**  >  **experimentos**de configuración, seleccione la casilla de verificación **Descripción general de CSS** .</span><span class="sxs-lookup"><span data-stu-id="10410-253">To enable this experiment, under **Settings** > **Experiments**, choose the **CSS Overview** checkbox.</span></span>  <span data-ttu-id="10410-254">Para ver una lista de elementos que tienen un problema de contraste de color, en **problemas de contraste**, elija **texto**.</span><span class="sxs-lookup"><span data-stu-id="10410-254">To view a list of elements that have a color contrast issue, on **Contrast issues**, choose **Text**.</span></span>  <span data-ttu-id="10410-255">Para abrir el elemento en la herramienta **elementos** , elija un elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="10410-255">To open the element in the **Elements** tool, choose an element in the list.</span></span>  <span data-ttu-id="10410-256">Para ayudar a solucionar los problemas de contraste, Microsoft Edge DevTools [ofrece automáticamente sugerencias de color][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span><span class="sxs-lookup"><span data-stu-id="10410-256">To help fix contrast issues, the Microsoft Edge DevTools [automatically provide color suggestions][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].</span></span>  <span data-ttu-id="10410-257">Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1120316][CR1120316]de problemas.</span><span class="sxs-lookup"><span data-stu-id="10410-257">To review real-time updates on this feature in the Chromium open-source project, navigate to Issue [#1120316][CR1120316].</span></span>  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problemas de contraste de color bajo" lightbox="../../media/2020/10/css-overview.msft.png":::
   <span data-ttu-id="10410-259">Problemas de contraste de color bajo</span><span class="sxs-lookup"><span data-stu-id="10410-259">Low color contrast issues</span></span>  
:::image-end:::  

## <span data-ttu-id="10410-260">Descargar los canales de Microsoft Edge Preview</span><span class="sxs-lookup"><span data-stu-id="10410-260">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="10410-261">Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="10410-261">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="10410-262">Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="10410-262">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="10410-263">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="10410-263">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Desuso del panel de propiedades en la herramienta elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de la cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugerencia de color accesible en el panel Estilos: novedades de DevTools (Microsoft Edge 86) | Microsoft docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento seleccionado recientemente o objeto de JavaScript: referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar los métodos abreviados de teclado en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referencia del análisis de rendimiento | Microsoft docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulación: compatibilidad con el modo de pantalla dual-características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar las API experimentales: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar el editor de métodos abreviados de teclado: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulación: compatibilidad con el modo de pantalla dual-características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Habilitar la consola de red: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar visor de pedidos de origen-características experimentales | Microsoft docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos de plegable y dos pantallas: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabla-referencia de API de consola | Microsoft docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspeccionar CSS cuadrícula | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de la representación con la pestaña representación, referencia de análisis de rendimiento | Microsoft docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Ver y depurar información de reproductores multimedia | Microsoft docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtrar solicitudes por propiedades-referencia de análisis de red | Microsoft docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emular autenticadores y depurar webauthn en Microsoft Edge DevTools | Microsoft docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de Microsoft Edge Preview"  

[VisualStudioCode]: https://code.visualstudio.com "Código de Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Código de Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar métodos abreviados de teclado o enlaces de clave | Errores de cromo"
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la última versión de Lighthouse | Errores de cromo"  
[CR1034663]: https://crbug.com/1034663 "Crear un front-end para la API de pruebas de webauthn | Errores de cromo"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS/Flexbox/tables de CSS | Errores de cromo"  
[CR1051466]: https://crbug.com/1051466 "Compatibilidad con COOP/depuración COEP en DevTools | Errores de cromo"  
[CR1073899]: https://crbug.com/1073899 "La pestaña de estilo calculado desaparece en modo de respuesta | Errores de cromo"  
[CR1075732]: https://crbug.com/1075732 "Personalización de DevTools: pestañas móviles | Errores de cromo"  
[CR1084673]: https://crbug.com/1084673 "DevTools: mejora la manera en que presentamos las propiedades personalizadas de CSS ((aka). Variables de CSS) y sus valores | Errores de cromo"  
[CR1093687]: https://crbug.com/1093687 "Herramienta crear y reproducir solicitudes de red sintéticas | Errores de cromo"  
[CR1096230]: https://crbug.com/1096230 "Agrupar propiedades CSS por categorías en el panel Estilos calculados | Errores de cromo"  
[CR1104188]: https://crbug.com/1104188 "La búsqueda de herramientas de red no encuentra resultados al buscar la dirección URL completa | Errores de cromo"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: mejorar la pestaña estilos calculados | Errores de cromo"  
[CR1120316]: https://crbug.com/1120316 "Resalte mala parte del contraste en CSS Descripción > colores | Errores de cromo"  
[CR1121141]: https://crbug.com/1121141 "Permitir filtrar por tipo de recurso en el registro de red | Errores de cromo"  
[CR1121312]: https://crbug.com/1121312 "La configuración debe quitarse del menú herramientas | Errores de cromo"  
[CR1136394]: https://crbug.com/1136394 "Herramientas de Flexbox | Errores de cromo"  
[CR1136655]: https://crbug.com/1136655 "DevTools: localización V2 | Errores de cromo"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "API de informes | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-DevTools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/Lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "¡ Hola! | Intento"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato de colección Postman de v 2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Especificación de OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> <span data-ttu-id="10410-316">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="10410-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="10410-317">La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/10/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).</span><span class="sxs-lookup"><span data-stu-id="10410-317">The original page is found [here](https://developers.google.com/web/updates/2020/10/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="10410-319">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="10410-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  