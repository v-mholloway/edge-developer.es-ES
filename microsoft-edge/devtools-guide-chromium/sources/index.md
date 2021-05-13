---
description: Use la herramienta Orígenes para ver, modificar y depurar JavaScript devuelto por el servidor e inspeccionar los recursos que conste la página web actual.  Para usar la herramienta Orígenes como entorno de desarrollo, agregue archivos de origen a un área de trabajo.
title: Información general sobre la herramienta Orígenes
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d3ef49bf986d8827216bd0bc183e45806aa0a2c3
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564717"
---
# <a name="sources-tool-overview"></a><span data-ttu-id="7781a-105">Información general sobre la herramienta Orígenes</span><span class="sxs-lookup"><span data-stu-id="7781a-105">Sources tool overview</span></span>  

<span data-ttu-id="7781a-106">Use la **herramienta Orígenes** para ver, modificar y depurar código JavaScript front-end e inspeccionar los recursos que formaban la página web actual.</span><span class="sxs-lookup"><span data-stu-id="7781a-106">Use the **Sources** tool to view, modify, and debug front-end JavaScript code, and to inspect the resources that make up the current webpage.</span></span>  <span data-ttu-id="7781a-107">La **herramienta Orígenes** tiene tres paneles:</span><span class="sxs-lookup"><span data-stu-id="7781a-107">The **Sources** tool has three panes:</span></span>  

| <span data-ttu-id="7781a-108">Panel</span><span class="sxs-lookup"><span data-stu-id="7781a-108">Pane</span></span> | <span data-ttu-id="7781a-109">Acciones</span><span class="sxs-lookup"><span data-stu-id="7781a-109">Actions</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="7781a-110">**Panel Navegador**</span><span class="sxs-lookup"><span data-stu-id="7781a-110">**Navigator** pane</span></span> | <span data-ttu-id="7781a-111">Navegue entre los recursos que se devuelven desde el servidor para crear la página web actual.</span><span class="sxs-lookup"><span data-stu-id="7781a-111">Navigate among the resources that are returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="7781a-112">Seleccione archivos, imágenes y otros recursos y vea sus rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="7781a-112">Select files, images, and other resources, and view their paths.</span></span>  <span data-ttu-id="7781a-113">Opcionalmente, configure un área de trabajo local para guardar los cambios directamente en los archivos de origen.</span><span class="sxs-lookup"><span data-stu-id="7781a-113">Optionally, set up a local Workspace to save changes directly to source files.</span></span>  |  
| <span data-ttu-id="7781a-114">**Panel editor**</span><span class="sxs-lookup"><span data-stu-id="7781a-114">**Editor** pane</span></span> | <span data-ttu-id="7781a-115">Ver JavaScript, HTML, CSS y otros archivos que se devuelven desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="7781a-115">View JavaScript, HTML, CSS, and other files that are returned from the server.</span></span>  <span data-ttu-id="7781a-116">Realice ediciones experimentales en JavaScript o CSS.</span><span class="sxs-lookup"><span data-stu-id="7781a-116">Make experimental edits to JavaScript or CSS.</span></span>  <span data-ttu-id="7781a-117">Los cambios se conservan hasta actualizar la página o se conservan después de la actualización de la página si se guarda en un archivo local con áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="7781a-117">Your changes are preserved until you refresh the page, or are preserved after page refresh if you save to a local file with Workspaces.</span></span>  <span data-ttu-id="7781a-118">Al usar áreas de trabajo o invalidaciones, también puede editar archivos HTML.</span><span class="sxs-lookup"><span data-stu-id="7781a-118">When you use Workspaces or Overrides, you can edit HTML files as well.</span></span>  |  
| <span data-ttu-id="7781a-119">**Panel depurador**</span><span class="sxs-lookup"><span data-stu-id="7781a-119">**Debugger** pane</span></span> | <span data-ttu-id="7781a-120">Use el depurador de JavaScript para establecer puntos de interrupción, pausar la ejecución de JavaScript y realizar un paso por el código, incluidas las modificaciones que haya realizado, mientras observa las expresiones de JavaScript que especifique.</span><span class="sxs-lookup"><span data-stu-id="7781a-120">Use the JavaScript Debugger to set breakpoints, pause running JavaScript, and step through the code, including any edits you have made, while watching any JavaScript expressions you specify.</span></span>  <span data-ttu-id="7781a-121">Observe y cambie manualmente los valores de las variables que están dentro del ámbito de la línea de código actual.</span><span class="sxs-lookup"><span data-stu-id="7781a-121">Watch and manually change the values of variables that are in-scope for the current line of code.</span></span>  |  

<span data-ttu-id="7781a-122">En la siguiente \*\*\*\* figura se muestra el panel Navegador resaltado con un cuadro rojo en la esquina superior \*\*\*\* izquierda de DevTools, el **panel Editor** resaltado en la parte superior derecha y el panel Depurador resaltado en la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="7781a-122">The following figure shows the **Navigator** pane highlighted with a red box in the upper left corner of DevTools, the **Editor** pane highlighted in the upper right, and the **Debugger** pane highlighted on the bottom.</span></span>  <span data-ttu-id="7781a-123">En el lado izquierdo se encuentra la parte principal de la ventana del explorador, que muestra la página web en gris porque el depurador está pausado en un punto de interrupción:</span><span class="sxs-lookup"><span data-stu-id="7781a-123">On the far left side is the main part of the browser window, showing the rendered webpage grayed-out because the debugger is paused on a breakpoint:</span></span>

:::image type="complex" source="../media/sources-panes-narrow-layout.msft.png" alt-text="Los paneles de la herramienta Orígenes, en diseño estrecho" lightbox="../media/sources-panes-narrow-layout.msft.png":::
   <span data-ttu-id="7781a-125">Los paneles de la herramienta Orígenes, en diseño estrecho</span><span class="sxs-lookup"><span data-stu-id="7781a-125">The panes of the Sources tool, in narrow layout</span></span>  
:::image-end:::  

<span data-ttu-id="7781a-126">Cuando DevTools es ancho, el panel **Depurador** se coloca a la derecha e incluye **Scope** y **Watch:**</span><span class="sxs-lookup"><span data-stu-id="7781a-126">When DevTools is wide, the **Debugger** pane is placed on the right, and includes **Scope** and **Watch**:</span></span>  

:::image type="complex" source="../media/sources-panes-wide-layout.msft.png" alt-text="Navegar, ver, editar y depurar JavaScript devuelto por el servidor" lightbox="../media/sources-panes-wide-layout.msft.png":::
   <span data-ttu-id="7781a-128">Navegar, ver, editar y depurar JavaScript devuelto por el servidor</span><span class="sxs-lookup"><span data-stu-id="7781a-128">Navigate, view, edit, and debug JavaScript returned by the server</span></span>  
:::image-end:::  

<span data-ttu-id="7781a-129">Para maximizar el tamaño de la herramienta Orígenes, desasoye DevTools en una ventana independiente y, opcionalmente, mueva la ventana DevTools a un monitor independiente.</span><span class="sxs-lookup"><span data-stu-id="7781a-129">To maximize the size of the Sources tool, undock DevTools into a separate window, and optionally move the DevTools window to a separate monitor.</span></span>  <span data-ttu-id="7781a-130">Vea [Cambiar Microsoft Edge ubicación de DevTools (Undock, Dock to bottom, Dock to left).][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="7781a-130">See [Change Microsoft Edge DevTools placement (Undock, Dock to bottom, Dock to left)][DevToolsCustomizePlacement].</span></span>

<span data-ttu-id="7781a-131">Para cargar la página web de demostración de depuración que se muestra anteriormente, consulta [El enfoque básico para usar un depurador](#the-basic-approach-to-using-a-debugger), a continuación.</span><span class="sxs-lookup"><span data-stu-id="7781a-131">To load the debugging demo webpage that's shown above, see [The basic approach to using a debugger](#the-basic-approach-to-using-a-debugger), below.</span></span>

## <a name="using-the-navigator-pane-to-select-files"></a><span data-ttu-id="7781a-132">Uso del panel Navegador para seleccionar archivos</span><span class="sxs-lookup"><span data-stu-id="7781a-132">Using the Navigator pane to select files</span></span>

<span data-ttu-id="7781a-133">Use el **panel** Navegador \(a la izquierda\) para navegar entre los recursos que se devuelven desde el servidor para construir la página web actual.</span><span class="sxs-lookup"><span data-stu-id="7781a-133">Use the **Navigator** pane \(on the left\) to navigate among the resources that are returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="7781a-134">Seleccione archivos, imágenes y otros recursos y vea sus rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="7781a-134">Select files, images, and other resources, and view their paths.</span></span>  

:::image type="complex" source="../media/navigator-pane.msft.png" alt-text="Panel Navegador" lightbox="../media/navigator-pane.msft.png":::
   <span data-ttu-id="7781a-136">Panel **Navegador**</span><span class="sxs-lookup"><span data-stu-id="7781a-136">The **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="7781a-137">Para obtener acceso a las pestañas ocultas del panel Navegador, seleccione ![ Más fichas ](../media/more-tabs-icon.msft.png) \(**Más pestañas**\).</span><span class="sxs-lookup"><span data-stu-id="7781a-137">To access any hidden tabs of the Navigator pane, select ![More tabs](../media/more-tabs-icon.msft.png) \(**More tabs**\).</span></span>

<span data-ttu-id="7781a-138">Las siguientes subsecciones abarcan el panel Navegador:</span><span class="sxs-lookup"><span data-stu-id="7781a-138">The following subsections cover the Navigator pane:</span></span>  

*   [<span data-ttu-id="7781a-139">Uso de la pestaña Página para explorar los recursos que crean la página web actual</span><span class="sxs-lookup"><span data-stu-id="7781a-139">Using the Page tab to explore resources that construct the current webpage</span></span>](#using-the-page-tab-to-explore-resources-that-construct-the-current-webpage)  
*   [<span data-ttu-id="7781a-140">Uso de la pestaña Sistema de archivos para definir un área de trabajo local</span><span class="sxs-lookup"><span data-stu-id="7781a-140">Using the Filesystem tab to define a local Workspace</span></span>](#using-the-filesystem-tab-to-define-a-local-workspace)  
*   [<span data-ttu-id="7781a-141">Uso de la pestaña Invalidaciones para invalidar archivos de servidor con archivos locales</span><span class="sxs-lookup"><span data-stu-id="7781a-141">Using the Overrides tab to override server files with local files</span></span>](#using-the-overrides-tab-to-override-server-files-with-local-files)  
*   [<span data-ttu-id="7781a-142">Uso de la pestaña Scripts de contenido para Microsoft Edge extensiones</span><span class="sxs-lookup"><span data-stu-id="7781a-142">Using the Content scripts tab for Microsoft Edge extensions</span></span>](#using-the-content-scripts-tab-for-microsoft-edge-extensions)  
*   [<span data-ttu-id="7781a-143">Uso de la pestaña Fragmentos de código para ejecutar fragmentos de código JavaScript en cualquier página</span><span class="sxs-lookup"><span data-stu-id="7781a-143">Using the Snippets tab to run JavaScript code snippets on any page</span></span>](#using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage)  
*   [<span data-ttu-id="7781a-144">Uso del menú comando para abrir archivos</span><span class="sxs-lookup"><span data-stu-id="7781a-144">Using the Command Menu to open files</span></span>](#using-the-command-menu-to-open-files)  
    
### <a name="using-the-page-tab-to-explore-resources-that-construct-the-current-webpage"></a><span data-ttu-id="7781a-145">Uso de la pestaña Página para explorar los recursos que crean la página web actual</span><span class="sxs-lookup"><span data-stu-id="7781a-145">Using the Page tab to explore resources that construct the current webpage</span></span>

<span data-ttu-id="7781a-146">Use la **pestaña Página** **del** panel Navegador para explorar el sistema de archivos que se devuelve desde el servidor para crear la página web actual.</span><span class="sxs-lookup"><span data-stu-id="7781a-146">Use the **Page** tab of the **Navigator** pane to explore the file system that's returned from the server to construct the current webpage.</span></span>  <span data-ttu-id="7781a-147">Seleccione un archivo JavaScript para verlo, editarlo y depurarlo.</span><span class="sxs-lookup"><span data-stu-id="7781a-147">Select a JavaScript file to view, edit, and debug it.</span></span>  <span data-ttu-id="7781a-148">La **pestaña** Página enumera todos los recursos que la página ha cargado.</span><span class="sxs-lookup"><span data-stu-id="7781a-148">The **Page** tab lists all of the resources that the page has loaded.</span></span>

:::image type="complex" source="../media/sources-page-tab.msft.png" alt-text="La pestaña Página del panel Navegador de la herramienta Orígenes" lightbox="../media/sources-page-tab.msft.png":::
   <span data-ttu-id="7781a-150">La **pestaña Página** del panel **Navegador** de la herramienta **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="7781a-150">The **Page** tab in the **Navigator** pane of the **Sources** tool</span></span>
:::image-end:::  

<span data-ttu-id="7781a-151">Para mostrar un archivo en el **panel Editor,** seleccione un archivo en la **pestaña** Página.  Para una imagen, se muestra una vista previa de la imagen.</span><span class="sxs-lookup"><span data-stu-id="7781a-151">To display a file in the **Editor** pane, select a file in the **Page** tab.  For an image, a preview of the image is displayed.</span></span>  
<span data-ttu-id="7781a-152">Para mostrar la dirección URL o la ruta de acceso de un recurso, mantenga el puntero sobre el recurso.</span><span class="sxs-lookup"><span data-stu-id="7781a-152">To display the URL or path for a resource, hover over the resource.</span></span>  
<span data-ttu-id="7781a-153">Para cargar un archivo en una nueva pestaña del explorador o para mostrar otras acciones, haga clic con el botón secundario en el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="7781a-153">To load a file into a new tab of the browser, or to display other actions, right-click on the file name.</span></span>  

#### <a name="icons-in-the-page-tab"></a><span data-ttu-id="7781a-154">Iconos en la pestaña Página</span><span class="sxs-lookup"><span data-stu-id="7781a-154">Icons in the Page tab</span></span>

<span data-ttu-id="7781a-155">La **pestaña** Página usa los siguientes iconos:</span><span class="sxs-lookup"><span data-stu-id="7781a-155">The **Page** tab uses the following icons:</span></span>  

*   <span data-ttu-id="7781a-156">El **icono de** ventana, junto con la etiqueta , representa el marco del documento `top` principal, que es un marco [HTML][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="7781a-156">The **window** icon, along with the label `top`, represents the main document frame, which is an [HTML frame][W3CHtml4Frames].</span></span>  
*   <span data-ttu-id="7781a-157">El **icono de** nube representa un [origen][WhatwgHtmlSpecMulitpageOriginHtmlOrigin].</span><span class="sxs-lookup"><span data-stu-id="7781a-157">The **cloud** icon represents an [origin][WhatwgHtmlSpecMulitpageOriginHtmlOrigin].</span></span>  
*   <span data-ttu-id="7781a-158">El **icono de** carpeta representa un directorio.</span><span class="sxs-lookup"><span data-stu-id="7781a-158">The **folder** icon represents a directory.</span></span>  
*   <span data-ttu-id="7781a-159">El **icono de** página representa un recurso.</span><span class="sxs-lookup"><span data-stu-id="7781a-159">The **page** icon represents a resource.</span></span>  
    
#### <a name="group-files-by-folder-or-as-a-flat-list"></a><span data-ttu-id="7781a-160">Agrupar archivos por carpeta o como una lista plana</span><span class="sxs-lookup"><span data-stu-id="7781a-160">Group files by folder or as a flat list</span></span>

<span data-ttu-id="7781a-161">La **pestaña** Página muestra archivos o recursos agrupados por servidor y directorio, o como una lista plana.</span><span class="sxs-lookup"><span data-stu-id="7781a-161">The **Page** tab displays files or resources grouped by server and directory, or as a flat list.</span></span>

<span data-ttu-id="7781a-162">Para cambiar la forma en que se agrupan los recursos:</span><span class="sxs-lookup"><span data-stu-id="7781a-162">To change how resources are grouped:</span></span>

1.  <span data-ttu-id="7781a-163">Junto a las pestañas del panel Navegador \(a la izquierda\), seleccione **el botón ...** \( Más**opciones**\).</span><span class="sxs-lookup"><span data-stu-id="7781a-163">Next to the tabs on the Navigator pane \(on the left\), select the **...** \(**More options**\) button.</span></span>  <span data-ttu-id="7781a-164">Aparece un menú.</span><span class="sxs-lookup"><span data-stu-id="7781a-164">A menu appears.</span></span>  
1.  <span data-ttu-id="7781a-165">Seleccione o desactive la **opción Agrupar por** carpeta.</span><span class="sxs-lookup"><span data-stu-id="7781a-165">Select or clear the **Group by folder** option.</span></span>  
    
### <a name="using-the-filesystem-tab-to-define-a-local-workspace"></a><span data-ttu-id="7781a-166">Uso de la pestaña Sistema de archivos para definir un área de trabajo local</span><span class="sxs-lookup"><span data-stu-id="7781a-166">Using the Filesystem tab to define a local Workspace</span></span>

<span data-ttu-id="7781a-167">Use la pestaña Sistema \*\*\*\* **de** archivos del panel Navegador para agregar archivos a un área de trabajo, de modo que los cambios realizados en DevTools se guarden en el sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="7781a-167">Use the **Filesystem** tab of the **Navigator** pane to add files to a Workspace, so that changes you make in DevTools get saved to your local file system.</span></span>  
<span data-ttu-id="7781a-168">Un archivo que está en un área de trabajo se indica mediante un punto verde junto al nombre del archivo, en DevTools.</span><span class="sxs-lookup"><span data-stu-id="7781a-168">A file that's in a Workspace is indicated by a green dot next to the file name, throughout DevTools.</span></span>  

:::image type="complex" source="../media/sources-filesystem-tab.msft.png" alt-text="Ficha Sistema de archivos para un área de trabajo" lightbox="../media/sources-filesystem-tab.msft.png":::
   <span data-ttu-id="7781a-170">Ficha **Sistema de** archivos para un área de trabajo</span><span class="sxs-lookup"><span data-stu-id="7781a-170">The **Filesystem** tab, for a Workspace</span></span>
:::image-end:::  

<span data-ttu-id="7781a-171">De forma predeterminada, al editar un archivo en la **herramienta Orígenes,** los cambios se descartan al actualizar la página web.</span><span class="sxs-lookup"><span data-stu-id="7781a-171">By default, when you edit a file in the **Sources** tool, your changes are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="7781a-172">La **herramienta Orígenes** funciona con una copia de los recursos front-end devueltos por el servidor web.</span><span class="sxs-lookup"><span data-stu-id="7781a-172">The **Sources** tool works with a copy of the front-end resources that are returned by the web server.</span></span>  <span data-ttu-id="7781a-173">Al modificar estos archivos front-end devueltos por el servidor, los cambios no persisten, ya que no ha cambiado los archivos de origen.</span><span class="sxs-lookup"><span data-stu-id="7781a-173">When you modify these front-end files that are returned by the server, the changes don't persist, because you didn't change the source files.</span></span>  <span data-ttu-id="7781a-174">También debe aplicar las ediciones en el código fuente real y, a continuación, volver a implementar en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7781a-174">You need to also apply your edits in your actual source code, and then re-deploy to the server.</span></span>  
<span data-ttu-id="7781a-175">En cambio, al usar un área de trabajo, los cambios realizados en el código front-end se conservan al actualizar la página web.</span><span class="sxs-lookup"><span data-stu-id="7781a-175">In contrast, when you use a Workspace, changes that you make to your front-end code are preserved when you refresh the webpage.</span></span>  <span data-ttu-id="7781a-176">Con un área de trabajo, al editar el código front-end devuelto por el servidor, la herramienta Orígenes también aplica las ediciones al código fuente local.</span><span class="sxs-lookup"><span data-stu-id="7781a-176">With a Workspace, when you edit the front-end code that's returned by the server, the Sources tool also applies your edits to your local source code.</span></span>  <span data-ttu-id="7781a-177">A continuación, para que otros usuarios vean los cambios, solo necesita volver a implementar los archivos de origen cambiados en el servidor.</span><span class="sxs-lookup"><span data-stu-id="7781a-177">Then for other users to see your changes, you only need to redeploy your changed source files to the server.</span></span>  
<span data-ttu-id="7781a-178">Las áreas de trabajo funcionan bien cuando el código JavaScript devuelto por el servidor es el mismo que el código fuente de JavaScript local.</span><span class="sxs-lookup"><span data-stu-id="7781a-178">Workspaces work well when the JavaScript code that's returned by the server is the same as your local JavaScript source code.</span></span>  <span data-ttu-id="7781a-179">Las áreas de trabajo no funcionan tan bien cuando el flujo de trabajo implica transformaciones en el código fuente, como la minificación o la compilación [de TypeScript.][TypescriptlangMain]</span><span class="sxs-lookup"><span data-stu-id="7781a-179">Workspaces don't work as well when your workflow involves transformations on your source code, such as minification or [TypeScript][TypescriptlangMain] compilation.</span></span>  

<span data-ttu-id="7781a-180">Para obtener más información, vea el tutorial [Editar archivos con áreas de trabajo.][DevtoolsGuideChromiumWorkspacesIndex]</span><span class="sxs-lookup"><span data-stu-id="7781a-180">For more information, see the tutorial [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span></span>

### <a name="using-the-overrides-tab-to-override-server-files-with-local-files"></a><span data-ttu-id="7781a-181">Uso de la pestaña Invalidaciones para invalidar archivos de servidor con archivos locales</span><span class="sxs-lookup"><span data-stu-id="7781a-181">Using the Overrides tab to override server files with local files</span></span>

<span data-ttu-id="7781a-182">Use la **pestaña Invalidaciones** del panel **Navegador** para invalidar los activos de página \(como imágenes\) con archivos de una carpeta local.</span><span class="sxs-lookup"><span data-stu-id="7781a-182">Use the **Overrides** tab of the **Navigator** pane to override page assets \(such as images\) with files from a local folder.</span></span>  
<span data-ttu-id="7781a-183">Los elementos de esta pestaña invalidan lo que el servidor envía al explorador, incluso después de que el servidor haya enviado los activos.</span><span class="sxs-lookup"><span data-stu-id="7781a-183">Items in this tab override what the server sends to the browser, even after the server has sent the assets.</span></span>  

:::image type="complex" source="../media/overrides-tab.msft.png" alt-text="La pestaña Invalidaciones del panel Navegador" lightbox="../media/overrides-tab.msft.png":::
   <span data-ttu-id="7781a-185">La **pestaña Invalidaciones** del **panel** Navegador</span><span class="sxs-lookup"><span data-stu-id="7781a-185">The **Overrides** tab of the **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="7781a-186">La **característica Invalidaciones** es similar a Workspaces.</span><span class="sxs-lookup"><span data-stu-id="7781a-186">The **Overrides** feature is similar to Workspaces.</span></span>  <span data-ttu-id="7781a-187">Usa Invalidaciones cuando quieras experimentar con los cambios en una página web y debes mantener los cambios después de actualizar la página web, pero no te importa asignar los cambios al código fuente de la página web.</span><span class="sxs-lookup"><span data-stu-id="7781a-187">Use Overrides when you want to experiment with changes to a webpage, and you need to keep the changes after you refresh the webpage, but you don't care about mapping your changes to the source code of the webpage.</span></span>  

<span data-ttu-id="7781a-188">Un archivo que reemplaza un archivo devuelto por el servidor se indica mediante un punto púrpura junto al nombre del archivo, en DevTools.</span><span class="sxs-lookup"><span data-stu-id="7781a-188">A file that overrides a file that is returned by the server is indicated by a purple dot next to the file name, throughout DevTools.</span></span>

#### <a name="see-also"></a><span data-ttu-id="7781a-189">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7781a-189">See also</span></span>

*   [<span data-ttu-id="7781a-190">Invalidar recursos de página web con copias locales mediante Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7781a-190">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>][DevtoolsJavascriptOverrides]  
*   [<span data-ttu-id="7781a-191">Asignar código preprocesado al código fuente</span><span class="sxs-lookup"><span data-stu-id="7781a-191">Map preprocessed code to source code</span></span>][DevToolsJavaScriptSourceMaps]  
    
### <a name="using-the-content-scripts-tab-for-microsoft-edge-extensions"></a><span data-ttu-id="7781a-192">Uso de la pestaña Scripts de contenido para Microsoft Edge extensiones</span><span class="sxs-lookup"><span data-stu-id="7781a-192">Using the Content scripts tab for Microsoft Edge extensions</span></span>

<span data-ttu-id="7781a-193">Use la pestaña Scripts \*\*\*\* **de** contenido del panel Navegador para ver los scripts de contenido cargados por una Microsoft Edge de contenido que haya instalado.</span><span class="sxs-lookup"><span data-stu-id="7781a-193">Use the **Content scripts** tab of the **Navigator** pane to view any content scripts that were loaded by a Microsoft Edge extension that you installed.</span></span>  

:::image type="complex" source="../media/content-scripts-tab.msft.png" alt-text="La pestaña Scripts de contenido del panel Navegador" lightbox="../media/content-scripts-tab.msft.png":::
   <span data-ttu-id="7781a-195">La **pestaña Scripts de contenido** del **panel** Navegador</span><span class="sxs-lookup"><span data-stu-id="7781a-195">The **Content scripts** tab of the **Navigator** pane</span></span>
:::image-end:::  

<span data-ttu-id="7781a-196">Cuando el depurador entra en el código que no reconoce, es posible que desee marcar ese código como código de biblioteca, para evitar entrar en ese código.</span><span class="sxs-lookup"><span data-stu-id="7781a-196">When the debugger steps into code that you don't recognize, you might want to mark that code as Library code, to avoid stepping into that code.</span></span>  <span data-ttu-id="7781a-197">Vea [Marcar scripts de contenido como código de biblioteca][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].</span><span class="sxs-lookup"><span data-stu-id="7781a-197">See [Mark content scripts as Library code][DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode].</span></span>

#### <a name="see-also"></a><span data-ttu-id="7781a-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7781a-198">See also</span></span>

*   [<span data-ttu-id="7781a-199">Scripts de contenido</span><span class="sxs-lookup"><span data-stu-id="7781a-199">Content scripts</span></span>][MdnAddOnsWebextensionsContentScripts]  
*   [<span data-ttu-id="7781a-200">Crear un tutorial de extensión, parte 2</span><span class="sxs-lookup"><span data-stu-id="7781a-200">Create an extension tutorial Part 2</span></span>][ExtensionsChromiumGetstartPart2ContentScripts]  
    
### <a name="using-the-snippets-tab-to-run-javascript-code-snippets-on-any-webpage"></a><span data-ttu-id="7781a-201">Uso de la pestaña Fragmentos de código para ejecutar fragmentos de código JavaScript en cualquier página web</span><span class="sxs-lookup"><span data-stu-id="7781a-201">Using the Snippets tab to run JavaScript code snippets on any webpage</span></span>

<span data-ttu-id="7781a-202">Use la **pestaña Fragmentos** de código del panel **Navegador** para crear y guardar fragmentos de código javaScript, de modo que pueda ejecutar fácilmente estos fragmentos de código en cualquier página web.</span><span class="sxs-lookup"><span data-stu-id="7781a-202">Use the **Snippets** tab of the **Navigator** pane to create and save JavaScript code snippets, so that you can easily run these snippets on any webpage.</span></span>

:::image type="complex" source="../media/snippet.msft.png" alt-text="Fragmento de código que inserta la biblioteca jQuery en una página web" lightbox="../media/snippet.msft.png":::
   <span data-ttu-id="7781a-204">Fragmento de código que inserta la biblioteca jQuery en una página web</span><span class="sxs-lookup"><span data-stu-id="7781a-204">A Snippet that inserts the jQuery library into a webpage</span></span>  
:::image-end:::  

<span data-ttu-id="7781a-205">Por ejemplo, supongamos que escribe con frecuencia el siguiente código en la consola **,** para insertar la biblioteca jQuery en una página para que pueda ejecutar comandos jQuery desde la **consola**:</span><span class="sxs-lookup"><span data-stu-id="7781a-205">For example, suppose you frequently enter the following code in the **Console**, to insert the jQuery library into a page so that you can run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="7781a-206">En su lugar, puede guardar este código en un **fragmento** de código y, a continuación, ejecutarlo fácilmente siempre que lo necesite.</span><span class="sxs-lookup"><span data-stu-id="7781a-206">Instead, you can save this code in a **Snippet** and then easily run it whenever you need to.</span></span>  <span data-ttu-id="7781a-207">Al seleccionar `Ctrl` + `S` \(Windows/Linux\) o `Command` + `S` \(macOS\), DevTools \*\*\*\* guarda el fragmento de código en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="7781a-207">When you select `Ctrl`+`S` \(Windows/Linux\) or `Command`+`S` \(macOS\), DevTools saves the **Snippet** to your file system.</span></span>  

<span data-ttu-id="7781a-208">Hay varias maneras de ejecutar un fragmento de código:</span><span class="sxs-lookup"><span data-stu-id="7781a-208">There are multiple ways to run a Snippet:</span></span>  

*   <span data-ttu-id="7781a-209">En el **panel Navegador,** seleccione la pestaña **Fragmentos** de código y, a continuación, seleccione el archivo de fragmentos de código para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="7781a-209">In the **Navigator** pane, select the **Snippets** tab, and then select the snippets file to open it.</span></span>  <span data-ttu-id="7781a-210">A continuación, en la parte inferior del panel Editor, seleccione **Ejecutar** \( ![ El botón Ejecutar ](../media/run-snippet-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="7781a-210">Then at the bottom of the Editor pane, select **Run** \(![The Run button](../media/run-snippet-icon.msft.png)\).</span></span>  
*   <span data-ttu-id="7781a-211">Cuando DevTools tenga el foco, seleccione `Ctrl` + `P` \(Windows/Linux\) o `Command` + `P` [][DevToolsCommandMenuIndex]\(macOS\) `!` para abrir el menú comando y, a continuación, escriba .</span><span class="sxs-lookup"><span data-stu-id="7781a-211">When DevTools has focus, select `Ctrl`+`P` \(Windows/Linux\) or `Command`+`P` \(macOS\) to open the [Command Menu][DevToolsCommandMenuIndex], and then type `!`.</span></span>  
    
<span data-ttu-id="7781a-212">Los fragmentos de código son similares a los bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="7781a-212">Snippets are similar to bookmarklets.</span></span>

#### <a name="see-also"></a><span data-ttu-id="7781a-213">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7781a-213">See also</span></span>

*   [<span data-ttu-id="7781a-214">Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7781a-214">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>][DevtoolsGuideChromiumJavascriptSnippets]  
    
### <a name="using-the-command-menu-to-open-files"></a><span data-ttu-id="7781a-215">Uso del menú comando para abrir archivos</span><span class="sxs-lookup"><span data-stu-id="7781a-215">Using the Command Menu to open files</span></span>

<span data-ttu-id="7781a-216">Para abrir un archivo, además \*\*\*\* de usar el panel Navegador de la herramienta **Orígenes,** puede usar el menú comando desde cualquier lugar dentro de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7781a-216">To open a file, in addition to using the **Navigator** pane within the **Sources** tool, you can use the Command Menu from anywhere within DevTools.</span></span>

*   <span data-ttu-id="7781a-217">Desde cualquier lugar de DevTools, seleccione `Ctrl` + `P` en Windows/Linux o `Command` + `P` en macOS.</span><span class="sxs-lookup"><span data-stu-id="7781a-217">From anywhere in DevTools, select `Ctrl`+`P` on Windows/Linux or `Command`+`P` on macOS.</span></span>  <span data-ttu-id="7781a-218">Aparece el menú Comando y enumera todos los recursos que se encuentran en las pestañas del **panel** Navegador de la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="7781a-218">The Command Menu appears, and lists all the resources that are in the tabs of the **Navigator** pane of the **Sources** tool.</span></span>  
*   <span data-ttu-id="7781a-219">O bien, junto a \*\*\*\* las pestañas del panel Navegador de la herramienta **Orígenes,** seleccione **el botón ...** **\(** Más opciones \) y, a continuación, seleccione **Abrir archivo**.</span><span class="sxs-lookup"><span data-stu-id="7781a-219">Or, next to the tabs of the **Navigator** pane in the **Sources** tool, select the **...** \(**More options**\) button, and then select **Open File**.</span></span>  

<span data-ttu-id="7781a-220">Para mostrar y seleccionar de una lista de todos .js archivos, escriba `.js` .</span><span class="sxs-lookup"><span data-stu-id="7781a-220">To display and pick from a list of all .js files, type `.js`.</span></span>

:::image type="complex" source="../media/sources-command-menu-to-open-file.msft.png" alt-text="Abrir un archivo mediante el menú comando" lightbox="../media/sources-command-menu-to-open-file.msft.png":::
   <span data-ttu-id="7781a-222">Abrir un archivo mediante el menú comando</span><span class="sxs-lookup"><span data-stu-id="7781a-222">Opening a file by using the Command Menu</span></span>
:::image-end:::

<span data-ttu-id="7781a-223">Si escribe `?` , el menú de comandos muestra varios comandos, incluidos **...  Abrir archivo**.</span><span class="sxs-lookup"><span data-stu-id="7781a-223">If you type `?`, the Command Menu shows several commands, including **...  Open file**.</span></span>  <span data-ttu-id="7781a-224">Si selecciona borrar `Backspace` el menú comando, se muestra una lista de archivos.</span><span class="sxs-lookup"><span data-stu-id="7781a-224">If you select `Backspace` to clear the Command Menu, a list of files is shown.</span></span>

<span data-ttu-id="7781a-225">Para obtener más información, vea [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="7781a-225">For more information, see [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span></span>

## <a name="using-the-editor-pane-to-view-or-edit-files"></a><span data-ttu-id="7781a-226">Uso del panel Editor para ver o editar archivos</span><span class="sxs-lookup"><span data-stu-id="7781a-226">Using the Editor pane to view or edit files</span></span>

<span data-ttu-id="7781a-227">Use el **panel Editor** para ver los archivos front-end que se devuelven desde el servidor para redactar la página web actual, incluidos los archivos JavaScript, HTML, CSS e imagen.</span><span class="sxs-lookup"><span data-stu-id="7781a-227">Use the **Editor** pane to view the front-end files that are returned from the server to compose the current webpage, including JavaScript, HTML, CSS, and image files.</span></span>  <span data-ttu-id="7781a-228">Al editar los archivos front-end en el **panel Editor,** DevTools actualiza la página web para ejecutar el código modificado.</span><span class="sxs-lookup"><span data-stu-id="7781a-228">When you edit the front-end files in the **Editor** pane, DevTools updates the webpage to run the modified code.</span></span>  

:::image type="complex" source="../media/editor-pane.msft.png" alt-text="El panel Editor de la herramienta Orígenes" lightbox="../media/editor-pane.msft.png":::
   <span data-ttu-id="7781a-230">El **panel Editor** de la herramienta **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="7781a-230">The **Editor** pane in the **Sources** tool</span></span>  
:::image-end:::

<span data-ttu-id="7781a-231">El **panel Editor** tiene el siguiente nivel de compatibilidad para varios tipos de archivo:</span><span class="sxs-lookup"><span data-stu-id="7781a-231">The **Editor** pane has the following level of support for various file types:</span></span>  

| <span data-ttu-id="7781a-232">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="7781a-232">File Type</span></span> | <span data-ttu-id="7781a-233">Acciones admitidas</span><span class="sxs-lookup"><span data-stu-id="7781a-233">Supported Actions</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="7781a-234">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7781a-234">JavaScript</span></span> | <span data-ttu-id="7781a-235">Ver, editar y depurar.</span><span class="sxs-lookup"><span data-stu-id="7781a-235">View, edit, and debug.</span></span>  |  
| <span data-ttu-id="7781a-236">CSS</span><span class="sxs-lookup"><span data-stu-id="7781a-236">CSS</span></span> | <span data-ttu-id="7781a-237">Ver y editar.</span><span class="sxs-lookup"><span data-stu-id="7781a-237">View and edit.</span></span>  |  
| <span data-ttu-id="7781a-238">HTML</span><span class="sxs-lookup"><span data-stu-id="7781a-238">HTML</span></span> | <span data-ttu-id="7781a-239">Ver y editar.</span><span class="sxs-lookup"><span data-stu-id="7781a-239">View and edit.</span></span>  |  
| <span data-ttu-id="7781a-240">Imágenes</span><span class="sxs-lookup"><span data-stu-id="7781a-240">Images</span></span> | <span data-ttu-id="7781a-241">Ver.</span><span class="sxs-lookup"><span data-stu-id="7781a-241">View.</span></span>  |  

<span data-ttu-id="7781a-242">De forma predeterminada, las ediciones se descartan al actualizar la página web.</span><span class="sxs-lookup"><span data-stu-id="7781a-242">By default, edits are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="7781a-243">Para obtener información sobre cómo guardar los cambios en el sistema de archivos, consulte [Using the Filesystem tab to define a local Workspace](#using-the-filesystem-tab-to-define-a-local-workspace), arriba.</span><span class="sxs-lookup"><span data-stu-id="7781a-243">For information about how to save the changes to your file system, see [Using the Filesystem tab to define a local Workspace](#using-the-filesystem-tab-to-define-a-local-workspace), above.</span></span>

<span data-ttu-id="7781a-244">Las siguientes subsecciones abarcan el panel Editor:</span><span class="sxs-lookup"><span data-stu-id="7781a-244">The following subsections cover the Editor pane:</span></span>  

*   [<span data-ttu-id="7781a-245">Edición de un archivo JavaScript</span><span class="sxs-lookup"><span data-stu-id="7781a-245">Editing a JavaScript file</span></span>](#editing-a-javascript-file)  
*   [<span data-ttu-id="7781a-246">Reformatear un archivo JavaScript minificado con pretty-print</span><span class="sxs-lookup"><span data-stu-id="7781a-246">Reformatting a minified JavaScript file with pretty-print</span></span>](#reformatting-a-minified-javascript-file-with-pretty-print)  
*   [<span data-ttu-id="7781a-247">Asignación de código minificado al código fuente para mostrar código legible</span><span class="sxs-lookup"><span data-stu-id="7781a-247">Mapping minified code to your source code to show readable code</span></span>](#mapping-minified-code-to-your-source-code-to-show-readable-code)  
*   [<span data-ttu-id="7781a-248">Transformaciones del código fuente al código front-end compilado</span><span class="sxs-lookup"><span data-stu-id="7781a-248">Transformations from source code to compiled front-end code</span></span>](#transformations-from-source-code-to-compiled-front-end-code)  
*   [<span data-ttu-id="7781a-249">Edición de un archivo CSS</span><span class="sxs-lookup"><span data-stu-id="7781a-249">Editing a CSS file</span></span>](#editing-a-css-file)  
*   [<span data-ttu-id="7781a-250">Edición de un archivo HTML</span><span class="sxs-lookup"><span data-stu-id="7781a-250">Editing an HTML file</span></span>](#editing-an-html-file)  
*   [<span data-ttu-id="7781a-251">Ir a una función o número de línea</span><span class="sxs-lookup"><span data-stu-id="7781a-251">Going to a line number or function</span></span>](#going-to-a-line-number-or-function)  
*   [<span data-ttu-id="7781a-252">Mostrar archivos de origen al usar una herramienta diferente</span><span class="sxs-lookup"><span data-stu-id="7781a-252">Displaying source files when using a different tool</span></span>](#displaying-source-files-when-using-a-different-tool)  
    
### <a name="editing-a-javascript-file"></a><span data-ttu-id="7781a-253">Edición de un archivo JavaScript</span><span class="sxs-lookup"><span data-stu-id="7781a-253">Editing a JavaScript file</span></span>

<span data-ttu-id="7781a-254">Para editar un archivo JavaScript en DevTools, use el **panel Editor,** dentro de la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="7781a-254">To edit a JavaScript file in DevTools, use the **Editor** pane, within the **Sources** tool.</span></span>

:::image type="complex" source="../media/editing-js-in-editor-pane.msft.png" alt-text="Edición de JavaScript en el panel Editor" lightbox="../media/editing-js-in-editor-pane.msft.png":::
   <span data-ttu-id="7781a-256">Edición de JavaScript en el **panel Editor**</span><span class="sxs-lookup"><span data-stu-id="7781a-256">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::

<span data-ttu-id="7781a-257">Para cargar un archivo en el panel Editor, use la pestaña **Página** en el **panel** Navegador \(a la izquierda\).</span><span class="sxs-lookup"><span data-stu-id="7781a-257">To load a file into the Editor pane, use the **Page** tab in the **Navigator** pane \(on the left\).</span></span>  <span data-ttu-id="7781a-258">O bien, use el **menú comando**, como se muestra a continuación: en la parte superior derecha de DevTools, seleccione Personalizar y **controlar DevTools** \( \) y, a continuación, `...` seleccione Abrir **archivo**.</span><span class="sxs-lookup"><span data-stu-id="7781a-258">Or use the **Command Menu**, as follows: in the upper right of DevTools, select **Customize and control DevTools** \(`...`\) and then select **Open File**.</span></span>

#### <a name="save-and-undo"></a><span data-ttu-id="7781a-259">Guardar y deshacer</span><span class="sxs-lookup"><span data-stu-id="7781a-259">Save and Undo</span></span>

<span data-ttu-id="7781a-260">Para que los cambios de JavaScript entren en vigor, seleccione `Ctrl` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="7781a-260">For JavaScript changes to take effect, select `Ctrl`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  

<span data-ttu-id="7781a-261">Si cambia un archivo, aparecerá un asterisco junto al nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="7781a-261">If you change a file, an asterisk appears next to the file name.</span></span>  

*   <span data-ttu-id="7781a-262">Para guardar los cambios, `Ctrl` + `S` seleccione en Windows/Linux o `Command` + `S` en macOS.</span><span class="sxs-lookup"><span data-stu-id="7781a-262">To save changes, select `Ctrl`+`S` on Windows/Linux or `Command`+`S` on macOS.</span></span>  
*   <span data-ttu-id="7781a-263">Para deshacer un cambio, seleccione `Ctrl` + `Z` en Windows/Linux o `Command` + `Z` en macOS.</span><span class="sxs-lookup"><span data-stu-id="7781a-263">To undo a change, select `Ctrl`+`Z` on Windows/Linux or `Command`+`Z` on macOS.</span></span>  
    
<span data-ttu-id="7781a-264">De forma predeterminada, las ediciones se descartan al actualizar la página web.</span><span class="sxs-lookup"><span data-stu-id="7781a-264">By default, your edits are discarded when you refresh the webpage.</span></span>  <span data-ttu-id="7781a-265">Para obtener más información acerca de cómo guardar los cambios en el sistema de archivos local, vea [Editar archivos con áreas de trabajo.][DevtoolsGuideChromiumWorkspacesIndex]</span><span class="sxs-lookup"><span data-stu-id="7781a-265">For more information about how to save the changes in your local file system, see [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex].</span></span>

#### <a name="find-and-replace"></a><span data-ttu-id="7781a-266">Buscar y reemplazar</span><span class="sxs-lookup"><span data-stu-id="7781a-266">Find and Replace</span></span>

<span data-ttu-id="7781a-267">Para buscar texto en el archivo actual, seleccione el **panel Editor** para darle el foco y, a continuación, seleccione `Ctrl` + `F` en Windows/Linux o `Command` + `F` en macOS.</span><span class="sxs-lookup"><span data-stu-id="7781a-267">To find text in the current file, select the **Editor** pane to give it focus, and then select `Ctrl`+`F` on Windows/Linux, or `Command`+`F` on macOS.</span></span>  

:::image type="complex" source="../media/find-replace.msft.png" alt-text="Buscar y reemplazar, en el panel Editor de la herramienta Orígenes" lightbox="../media/find-replace.msft.png":::
   <span data-ttu-id="7781a-269">**Buscar** y **reemplazar**, en el **panel Editor** de la **herramienta** Orígenes</span><span class="sxs-lookup"><span data-stu-id="7781a-269">**Find** and **Replace**, in the **Editor** pane of the **Sources** tool</span></span>
:::image-end:::

<span data-ttu-id="7781a-270">Para buscar y reemplazar texto, seleccione el botón **Reemplazar** \(**A-\>B**\) a la izquierda del cuadro **de** texto Buscar.</span><span class="sxs-lookup"><span data-stu-id="7781a-270">To find and replace text, select the **Replace** \(**A-\>B**\) button to the left of the **Find** textbox.</span></span>  <span data-ttu-id="7781a-271">El **botón** Reemplazar \(**A-\>B**\) aparece al ver un archivo editable.</span><span class="sxs-lookup"><span data-stu-id="7781a-271">The **Replace** \(**A-\>B**\) button appears when viewing an editable file.</span></span>

#### <a name="showing-the-changes-you-made"></a><span data-ttu-id="7781a-272">Mostrar los cambios realizados</span><span class="sxs-lookup"><span data-stu-id="7781a-272">Showing the changes you made</span></span>

<span data-ttu-id="7781a-273">Para revisar los cambios realizados en un archivo, haga clic con el botón secundario en el **panel Editor** y, a continuación, seleccione **Modificaciones locales**.</span><span class="sxs-lookup"><span data-stu-id="7781a-273">To review the changes you made to a file, right-click in the **Editor** pane and then select **Local Modifications**.</span></span>

<span data-ttu-id="7781a-274">El **cajón** se abre en la parte inferior de DevTools y muestra los cambios en la **pestaña** Cambios.</span><span class="sxs-lookup"><span data-stu-id="7781a-274">The **Drawer** opens at the bottom of DevTools, showing your changes within the **Changes** tab.</span></span>

:::image type="complex" source="../media/local-modifications.msft.png" alt-text="Mostrar modificaciones locales, en la pestaña Cambios del cajón" lightbox="../media/local-modifications.msft.png":::
   <span data-ttu-id="7781a-276">Mostrar **modificaciones locales**, en la pestaña **Cambios** del **cajón**</span><span class="sxs-lookup"><span data-stu-id="7781a-276">Showing **Local Modifications**, in the **Changes** tab of the **Drawer**</span></span>
:::image-end:::

#### <a name="changes-inside-a-function-take-effect"></a><span data-ttu-id="7781a-277">Los cambios dentro de una función tienen efecto</span><span class="sxs-lookup"><span data-stu-id="7781a-277">Changes inside a function take effect</span></span>

<span data-ttu-id="7781a-278">DevTools no vuelve a ejecutar un script, por lo que los únicos cambios de JavaScript que tienen efecto son los cambios que se realicen dentro de las funciones.</span><span class="sxs-lookup"><span data-stu-id="7781a-278">DevTools doesn't re-run a script, so the only JavaScript changes that take effect are changes that you make within functions.</span></span>  <span data-ttu-id="7781a-279">Por ejemplo, en la siguiente figura, agregamos el siguiente código al JavaScript que devuelve el servidor:</span><span class="sxs-lookup"><span data-stu-id="7781a-279">For example, in the following figure, we added the following code to the JavaScript that is returned by the server:</span></span>  
*   <span data-ttu-id="7781a-280">Se agregó la instrucción `console.log('A')` fuera de cualquier función.</span><span class="sxs-lookup"><span data-stu-id="7781a-280">We added the statement `console.log('A')` outside of any function.</span></span>  
*   <span data-ttu-id="7781a-281">Se agregó la instrucción `console.log('B')` dentro de una `onClick` función.</span><span class="sxs-lookup"><span data-stu-id="7781a-281">We added the statement `console.log('B')` inside an `onClick` function.</span></span>  
<span data-ttu-id="7781a-282">A continuación, guardamos los cambios, introdujmos números en el formulario y, a continuación, seleccionamos el botón de formulario para enviar el formulario.</span><span class="sxs-lookup"><span data-stu-id="7781a-282">We then saved the changes, entered numbers into the form, and then selected the form button to send the form.</span></span>  

<span data-ttu-id="7781a-283">Después de enviar el formulario, , que está en el ámbito global, no se ejecuta, pero , dentro de una función, se ejecuta, lo que da como resultado `console.log('A')` `console.log('B')` a la `onClick` `B` consola:</span><span class="sxs-lookup"><span data-stu-id="7781a-283">After submitting the form, `console.log('A')`, which is at global scope, doesn't run, but `console.log('B')`, inside an `onClick` function, does run, outputting `B` to the Console:</span></span>

:::image type="complex" source="../media/edit-js.msft.png" alt-text="JavaScript de ámbito global no se vuelve a ejecutar" lightbox="../media/edit-js.msft.png":::
   <span data-ttu-id="7781a-285">JavaScript de ámbito global no se vuelve a ejecutar</span><span class="sxs-lookup"><span data-stu-id="7781a-285">Global-scope JavaScript is not re-run</span></span>  
:::image-end:::

### <a name="reformatting-a-minified-javascript-file-with-pretty-print"></a><span data-ttu-id="7781a-286">Reformatear un archivo JavaScript minificado con pretty-print</span><span class="sxs-lookup"><span data-stu-id="7781a-286">Reformatting a minified JavaScript file with pretty-print</span></span>

<span data-ttu-id="7781a-287">Para usar pretty-print para volver a formatear un \*\*\*\* archivo para que sea legible, seleccione el botón De impresión bastante \( Formato \), que se muestra como llaves, en la parte inferior del ![ ](../media/format-icon.msft.png) panel Editor.</span><span class="sxs-lookup"><span data-stu-id="7781a-287">To use pretty-print to reformat a file to make it readable, select the **Pretty print** button \(![Format](../media/format-icon.msft.png)\), which is shown as braces, at the bottom of the Editor pane.</span></span>  <span data-ttu-id="7781a-288">O bien, si **aparece un botón De impresión** bastante en la parte superior del panel Editor, puede seleccionar ese botón.</span><span class="sxs-lookup"><span data-stu-id="7781a-288">Or, if a **Pretty-print** button appears at the top of the Editor pane, you can select that button.</span></span>

:::image type="complex" source="../media/minified.msft.png" alt-text="El botón De impresión bastante" lightbox="../media/minified.msft.png":::
   <span data-ttu-id="7781a-290">El **botón De impresión** bastante</span><span class="sxs-lookup"><span data-stu-id="7781a-290">The **Pretty print** button</span></span>  
:::image-end:::  

<span data-ttu-id="7781a-291">El archivo reformateado aparece en una pestaña nueva, con `:formatted` anexado al nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="7781a-291">The reformatted file appears in a new tab, with `:formatted` appended to the file name.</span></span>  <span data-ttu-id="7781a-292">El código reformateado es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7781a-292">The reformatted code is read-only.</span></span>  

:::image type="complex" source="../media/pretty-printed.msft.png" alt-text="Un archivo JavaScript bastante impreso (reformateado)" lightbox="../media/pretty-printed.msft.png":::
   <span data-ttu-id="7781a-294">Un archivo JavaScript bastante impreso \(reformatted\)</span><span class="sxs-lookup"><span data-stu-id="7781a-294">A pretty-printed \(reformatted\) JavaScript file</span></span>  
:::image-end:::  

<span data-ttu-id="7781a-295">Para hacer que el archivo reformateado se desplace al código que seleccione en el archivo minificado:</span><span class="sxs-lookup"><span data-stu-id="7781a-295">To make the reformatted file scroll to the code that you select in the minified file:</span></span>  

1.  <span data-ttu-id="7781a-296">Si la pestaña de archivo reformateado está abierta, cierre.</span><span class="sxs-lookup"><span data-stu-id="7781a-296">If the reformatted file tab is open, close it.</span></span>  
1.  <span data-ttu-id="7781a-297">Seleccione algún código en el archivo minificado en el panel Editor.</span><span class="sxs-lookup"><span data-stu-id="7781a-297">Select some code in the minified file in the Editor pane.</span></span>
1.  <span data-ttu-id="7781a-298">Seleccione el **botón Imprimir** bastante.</span><span class="sxs-lookup"><span data-stu-id="7781a-298">Select the **Pretty print** button.</span></span>  
     
<span data-ttu-id="7781a-299">El código con formato aparece en una pestaña nueva y se desplaza hasta el código seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7781a-299">The formatted code appears in a new tab, scrolled to the code that you selected.</span></span>

<span data-ttu-id="7781a-300">Para obtener más información, [vea Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].</span><span class="sxs-lookup"><span data-stu-id="7781a-300">For more information, see [Reformat a minified JavaScript file with pretty-print][DevToolsJavaScriptReferenceReformat].</span></span>  

### <a name="mapping-minified-code-to-your-source-code-to-show-readable-code"></a><span data-ttu-id="7781a-301">Asignación de código minificado al código fuente para mostrar código legible</span><span class="sxs-lookup"><span data-stu-id="7781a-301">Mapping minified code to your source code to show readable code</span></span>

<span data-ttu-id="7781a-302">Los mapas de origen de los preprocesadores hacen que DevTools cargue los archivos de origen de JavaScript originales, además de los archivos JavaScript minificados y transformados que devuelve el servidor.</span><span class="sxs-lookup"><span data-stu-id="7781a-302">Source maps from preprocessors cause DevTools to load your original JavaScript source files in addition to your minified, transformed JavaScript files that are returned by the server.</span></span>  <span data-ttu-id="7781a-303">A continuación, puede ver los archivos de origen originales mientras establece puntos de interrupción y atraviesa el código.</span><span class="sxs-lookup"><span data-stu-id="7781a-303">You then view your original source files while you set breakpoints and step through code.</span></span>  <span data-ttu-id="7781a-304">Mientras tanto, Microsoft Edge está ejecutando el código minificado.</span><span class="sxs-lookup"><span data-stu-id="7781a-304">Meanwhile, Microsoft Edge is actually running your minified code.</span></span>  

<span data-ttu-id="7781a-305">En el **panel Editor,** si hace clic con el botón secundario en un archivo JavaScript y luego selecciona Agregar mapa de **origen,** aparecerá un cuadro emergente, con un cuadro de texto Dirección **URL** de mapa de origen y un **botón** Agregar.</span><span class="sxs-lookup"><span data-stu-id="7781a-305">In the **Editor** pane, if you right-click a JavaScript file and then select **Add source map**, a popup box appears, with a **Source map URL** textbox and an **Add** button.</span></span>

<span data-ttu-id="7781a-306">El enfoque de asignación de origen mantiene el código front-end legible y depurable incluso después de combinarlo, minificarlo o compilarlo.</span><span class="sxs-lookup"><span data-stu-id="7781a-306">The source-mapping approach keeps your front-end code human-readable and debuggable even after you combine, minify, or compile it.</span></span>
<span data-ttu-id="7781a-307">Para obtener más información, vea [Map preprocessed code to source code][DevToolsJavaScriptSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="7781a-307">For more information, see [Map preprocessed code to source code][DevToolsJavaScriptSourceMaps].</span></span>

### <a name="transformations-from-source-code-to-compiled-front-end-code"></a><span data-ttu-id="7781a-308">Transformaciones del código fuente al código front-end compilado</span><span class="sxs-lookup"><span data-stu-id="7781a-308">Transformations from source code to compiled front-end code</span></span>

<span data-ttu-id="7781a-309">Si usa un marco que transforma los archivos JavaScript, como React, el Código JavaScript de origen local puede ser diferente del JavaScript front-end devuelto por el servidor.</span><span class="sxs-lookup"><span data-stu-id="7781a-309">If you use a framework that transforms your JavaScript files, such as React, your local source JavaScript might be different than the front-end JavaScript that's returned by the server.</span></span>  <span data-ttu-id="7781a-310">En este escenario no se admiten áreas de trabajo, pero en este escenario se admite la asignación de código fuente.</span><span class="sxs-lookup"><span data-stu-id="7781a-310">Workspaces aren't supported in this scenario, but source code mapping is supported in this scenario.</span></span>  

<span data-ttu-id="7781a-311">En un entorno de desarrollo, el servidor puede incluir los mapas de origen y el original `.ts` o los archivos para `.jsx` React.</span><span class="sxs-lookup"><span data-stu-id="7781a-311">In a development environment, your server might include your source maps and your original `.ts` or `.jsx` files for React.</span></span>  <span data-ttu-id="7781a-312">La **herramienta Orígenes** muestra estos archivos, pero no permite editar estos archivos.</span><span class="sxs-lookup"><span data-stu-id="7781a-312">The **Sources** tool displays these files, but doesn't allow you to edit these files.</span></span>  <span data-ttu-id="7781a-313">Cuando se establecen puntos de interrupción y se usa el depurador, DevTools muestra el original o los archivos, pero en realidad se hace un paso a través de la versión minificada de los `.ts` `.jsx` archivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7781a-313">When you set breakpoints and use the debugger, DevTools displays your original `.ts` or `.jsx` files, but actually steps-through the minified version of your JavaScript files.</span></span>

<span data-ttu-id="7781a-314">En este escenario, la herramienta **Orígenes** es útil para inspeccionar y realizar un paso a través del JavaScript front-end transformado que se devuelve desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="7781a-314">In this scenario, the **Sources** tool is useful for inspecting and stepping-through the transformed, front-end JavaScript that's returned from the server.</span></span>  <span data-ttu-id="7781a-315">Use el depurador para definir expresiones Watch y use la Consola para escribir expresiones de JavaScript para manipular datos que están dentro del ámbito.</span><span class="sxs-lookup"><span data-stu-id="7781a-315">Use the debugger to define Watch expressions, and use the Console to enter JavaScript expressions to manipulate data that's in-scope.</span></span>

### <a name="editing-a-css-file"></a><span data-ttu-id="7781a-316">Edición de un archivo CSS</span><span class="sxs-lookup"><span data-stu-id="7781a-316">Editing a CSS file</span></span>

<span data-ttu-id="7781a-317">Hay dos formas de editar CSS en DevTools:</span><span class="sxs-lookup"><span data-stu-id="7781a-317">There are two ways to edit CSS in DevTools:</span></span>  

*   <span data-ttu-id="7781a-318">En la **herramienta Elementos,** se trabaja con una configuración CSS a la vez, a través de controles de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7781a-318">In the **Elements** tool, you work with one CSS setting at a time, through user interface controls.</span></span>  <span data-ttu-id="7781a-319">Este enfoque se recomienda en la mayoría de los casos.</span><span class="sxs-lookup"><span data-stu-id="7781a-319">This approach is recommended in most cases.</span></span>  <span data-ttu-id="7781a-320">Para obtener más información, vea [Edit CSS font styles and settings in the Styles pane][DevToolsInspectStylesEditFonts].</span><span class="sxs-lookup"><span data-stu-id="7781a-320">For more information, see [Edit CSS font styles and settings in the Styles pane][DevToolsInspectStylesEditFonts].</span></span>  
*   <span data-ttu-id="7781a-321">En la **herramienta Orígenes,** se usa un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="7781a-321">In the **Sources** tool, you use a text editor.</span></span>  
    
<span data-ttu-id="7781a-322">La herramienta Orígenes admite la edición directa de un archivo CSS.</span><span class="sxs-lookup"><span data-stu-id="7781a-322">The Sources tool supports directly editing a CSS file.</span></span>  <span data-ttu-id="7781a-323">Por ejemplo, si edita el archivo CSS desde el tutorial Editar archivos con áreas de [trabajo][DevtoolsGuideChromiumWorkspacesIndex] para que coincidan con la regla de estilo siguiente, el elemento de la parte superior izquierda de la página web representado `H1` cambia a verde:</span><span class="sxs-lookup"><span data-stu-id="7781a-323">For example, if you edit the CSS file from the tutorial [Edit files with Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to match the style rule below, the `H1` element in the upper left of the rendered webpage changes to green:</span></span>

```css
h1 {
  color: green;
}  
```  

:::image type="complex" source="../media/edit-css.msft.png" alt-text="Editar CSS en el panel Editor para cambiar el color del texto del encabezado H1 a verde" lightbox="../media/edit-css.msft.png":::
   <span data-ttu-id="7781a-325">Editar CSS en el **panel Editor** para cambiar el color del texto del encabezado `H1` a verde</span><span class="sxs-lookup"><span data-stu-id="7781a-325">Edit CSS in the **Editor** pane to change the text color of the `H1` heading to green</span></span>  
:::image-end:::  

<span data-ttu-id="7781a-326">Los cambios CSS se llevan a efecto inmediatamente; no es necesario guardar manualmente los cambios.</span><span class="sxs-lookup"><span data-stu-id="7781a-326">CSS changes take effect immediately; you don't need to manually save the changes.</span></span>

#### <a name="see-also"></a><span data-ttu-id="7781a-327">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7781a-327">See also</span></span>  

*   [<span data-ttu-id="7781a-328">Editar estilos y opciones de fuente CSS en el panel Estilos</span><span class="sxs-lookup"><span data-stu-id="7781a-328">Edit CSS font styles and settings in the Styles pane</span></span>][DevToolsInspectStylesEditFonts]  
*   <span data-ttu-id="7781a-329">[DevTools para principiantes: Introducción a CSS][DevToolsBeginnersCss] - tutorial</span><span class="sxs-lookup"><span data-stu-id="7781a-329">[DevTools for beginners: Get started with CSS][DevToolsBeginnersCss] - tutorial</span></span>  
    
### <a name="editing-an-html-file"></a><span data-ttu-id="7781a-330">Edición de un archivo HTML</span><span class="sxs-lookup"><span data-stu-id="7781a-330">Editing an HTML file</span></span>

<span data-ttu-id="7781a-331">Hay dos formas de editar HTML en DevTools:</span><span class="sxs-lookup"><span data-stu-id="7781a-331">There are two ways to edit HTML in DevTools:</span></span>  

*   <span data-ttu-id="7781a-332">En la **herramienta Elementos,** se trabaja con un elemento HTML a la vez, a través de controles de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7781a-332">In the **Elements** tool, you work with one HTML element at a time, through user interface controls.</span></span>  
*   <span data-ttu-id="7781a-333">En la **herramienta Orígenes,** se usa un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="7781a-333">In the **Sources** tool, you use a text editor.</span></span>  
    
:::image type="complex" source="../media/sources-html-editor.msft.png" alt-text="El editor HTML de la herramienta Orígenes" lightbox="../media/sources-html-editor.msft.png":::
   <span data-ttu-id="7781a-335">El editor HTML de la **herramienta Orígenes**</span><span class="sxs-lookup"><span data-stu-id="7781a-335">The HTML editor of the **Sources** tool</span></span>
:::image-end:::  

<span data-ttu-id="7781a-336">A diferencia de un archivo JavaScript o CSS, un archivo HTML devuelto por el servidor web no se puede editar directamente en la herramienta Orígenes.</span><span class="sxs-lookup"><span data-stu-id="7781a-336">Unlike a JavaScript or CSS file, an HTML file that is returned by the web server cannot be directly edited in the Sources tool.</span></span>  <span data-ttu-id="7781a-337">Para editar un archivo HTML con el Editor de la herramienta Orígenes, el archivo HTML debe estar en un área de trabajo o en la pestaña **Invalidaciones.**  Vea estas subsecciones del artículo actual:</span><span class="sxs-lookup"><span data-stu-id="7781a-337">To edit an HTML file using the Editor of the Sources tool, the HTML file must be in a Workspace or on the **Overrides** tab.  See these subsections of the current article:</span></span>  

*   [<span data-ttu-id="7781a-338">Uso de la pestaña Sistema de archivos para definir un área de trabajo local</span><span class="sxs-lookup"><span data-stu-id="7781a-338">Using the Filesystem tab to define a local Workspace</span></span>](#using-the-filesystem-tab-to-define-a-local-workspace)  
*   [<span data-ttu-id="7781a-339">Uso de la pestaña Invalidaciones para invalidar archivos de servidor con archivos locales</span><span class="sxs-lookup"><span data-stu-id="7781a-339">Using the Overrides tab to override server files with local files</span></span>](#using-the-overrides-tab-to-override-server-files-with-local-files)  
   
<span data-ttu-id="7781a-340">Para guardar los cambios, `Ctrl` + `S` seleccione en Windows/Linux o `Command` + `S` en macOS.</span><span class="sxs-lookup"><span data-stu-id="7781a-340">To save changes, select `Ctrl`+`S` on Windows/Linux or `Command`+`S` on macOS.</span></span>  <span data-ttu-id="7781a-341">Un archivo editado está marcado por un asterisco.</span><span class="sxs-lookup"><span data-stu-id="7781a-341">An edited file is marked by an asterisk.</span></span>  
<span data-ttu-id="7781a-342">Para buscar texto, seleccione `Ctrl` + `F` en Windows/Linux o `Command` + `F` en macOS.</span><span class="sxs-lookup"><span data-stu-id="7781a-342">To find text, select `Ctrl`+`F` on Windows/Linux or `Command`+`F` on macOS.</span></span>  
<span data-ttu-id="7781a-343">Para deshacer una edición, seleccione `Ctrl` + `Z` en Windows/Linux o `Command` + `Z` en macOS.</span><span class="sxs-lookup"><span data-stu-id="7781a-343">To undo an edit, select `Ctrl`+`Z` on Windows/Linux or `Command`+`Z` on macOS.</span></span>  
<span data-ttu-id="7781a-344">Para ver otros comandos al editar un archivo HTML, en el panel Editor, haga clic con el botón secundario en el archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="7781a-344">To view other commands while editing an HTML file, in the Editor pane, right-click the HTML file.</span></span>  
<span data-ttu-id="7781a-345">También puede editar HTML mediante un editor HTML, en lugar de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7781a-345">You can also edit HTML by using an HTML editor, rather than DevTools.</span></span>  <span data-ttu-id="7781a-346">Por ejemplo, el artículo [DevTools para principiantes:][DevToolsBeginnersHtml] Introducción a HTML y dom usa un sitio web que permite la edición HTML dentro de la página web.</span><span class="sxs-lookup"><span data-stu-id="7781a-346">For example, the article [DevTools for beginners: Get started with HTML and the DOM][DevToolsBeginnersHtml] uses a website that enables HTML editing within the webpage.</span></span>  

### <a name="going-to-a-line-number-or-function"></a><span data-ttu-id="7781a-347">Ir a una función o número de línea</span><span class="sxs-lookup"><span data-stu-id="7781a-347">Going to a line number or function</span></span>

<span data-ttu-id="7781a-348">Para ir a un número de línea o símbolo \(como un nombre de función\) en el archivo que está abierto en el panel Editor, puede usar el menú comando, en lugar de desplazarse por el archivo.</span><span class="sxs-lookup"><span data-stu-id="7781a-348">To go to a line number or symbol \(such as a function name\) in the file which is open in the Editor pane, you can use the Command Menu, rather than scrolling through the file.</span></span>

1.  <span data-ttu-id="7781a-349">En el **panel** Navegador, seleccione los puntos suspensivos \( `...` \) \(**Más opciones**\) y, a continuación, seleccione Abrir **archivo**.</span><span class="sxs-lookup"><span data-stu-id="7781a-349">In the **Navigator** pane, select the ellipses \(`...`\) \(**More options**\), and then select **Open File**.</span></span>  <span data-ttu-id="7781a-350">Aparece el menú comando.</span><span class="sxs-lookup"><span data-stu-id="7781a-350">The Command Menu appears.</span></span>  
1.  <span data-ttu-id="7781a-351">Escriba uno de los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="7781a-351">Type one of the following characters:</span></span>  
     
| <span data-ttu-id="7781a-352">Carácter</span><span class="sxs-lookup"><span data-stu-id="7781a-352">Character</span></span> | <span data-ttu-id="7781a-353">Nombre del comando</span><span class="sxs-lookup"><span data-stu-id="7781a-353">Command name</span></span> | <span data-ttu-id="7781a-354">Propósito</span><span class="sxs-lookup"><span data-stu-id="7781a-354">Purpose</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="7781a-355">\:</span><span class="sxs-lookup"><span data-stu-id="7781a-355">\:</span></span> | **<span data-ttu-id="7781a-356">Ir a la línea</span><span class="sxs-lookup"><span data-stu-id="7781a-356">Go to line</span></span>** | <span data-ttu-id="7781a-357">Vaya a un número de línea.</span><span class="sxs-lookup"><span data-stu-id="7781a-357">Go to a line number.</span></span>  |  
| \@ | **<span data-ttu-id="7781a-358">Ir al símbolo</span><span class="sxs-lookup"><span data-stu-id="7781a-358">Go to symbol</span></span>** | <span data-ttu-id="7781a-359">Vaya a una función.</span><span class="sxs-lookup"><span data-stu-id="7781a-359">Go to a function.</span></span>  <span data-ttu-id="7781a-360">Al escribir , el menú comando enumera las funciones que se encuentran en el archivo JavaScript que `@` está abierto en el panel Editor.</span><span class="sxs-lookup"><span data-stu-id="7781a-360">When you type `@`, the Command Menu lists the functions that are found in the JavaScript file which is open in the Editor pane.</span></span>  |  
   
<span data-ttu-id="7781a-361">Para obtener más información, vea [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span><span class="sxs-lookup"><span data-stu-id="7781a-361">For more information, see [Run commands with the Microsoft Edge DevTools Command Menu][DevToolsCommandMenuIndex].</span></span>

### <a name="displaying-source-files-when-using-a-different-tool"></a><span data-ttu-id="7781a-362">Mostrar archivos de origen al usar una herramienta diferente</span><span class="sxs-lookup"><span data-stu-id="7781a-362">Displaying source files when using a different tool</span></span>

<span data-ttu-id="7781a-363">El lugar principal para ver los archivos de origen en DevTools está dentro de la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="7781a-363">The main place to view source files in the DevTools is within the **Sources** tool.</span></span>  <span data-ttu-id="7781a-364">Pero a veces es necesario tener acceso a otras herramientas, como **Elementos** o **Consola,** mientras se ven o editan los archivos de origen.</span><span class="sxs-lookup"><span data-stu-id="7781a-364">But sometimes you need to access other tools, such as **Elements** or **Console**, while viewing or editing your source files.</span></span>  <span data-ttu-id="7781a-365">Use la **herramienta Orígenes rápidos** en el [cajón][DevtoolsCustomizeIndexDrawer].</span><span class="sxs-lookup"><span data-stu-id="7781a-365">Use the **Quick Sources** tool in the [Drawer][DevtoolsCustomizeIndexDrawer].</span></span>  

1.  <span data-ttu-id="7781a-366">Seleccione una herramienta que no sea **la herramienta Orígenes,** como la **herramienta Elementos.**</span><span class="sxs-lookup"><span data-stu-id="7781a-366">Select a tool other than the **Sources** tool, such as the **Elements** tool.</span></span>  
1.  <span data-ttu-id="7781a-367">Seleccione `Ctrl` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="7781a-367">Select `Ctrl`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="7781a-368">Se abre el menú comando.</span><span class="sxs-lookup"><span data-stu-id="7781a-368">The Command Menu opens.</span></span>  
1.  <span data-ttu-id="7781a-369">Escriba `Quick Source` y, a continuación, **seleccione Mostrar origen rápido**.</span><span class="sxs-lookup"><span data-stu-id="7781a-369">Type `Quick Source`, and then select **Show Quick Source**.</span></span>  <span data-ttu-id="7781a-370">En la parte inferior de la ventana DevTools, aparece el cajón, con el panel **Origen rápido** seleccionado.</span><span class="sxs-lookup"><span data-stu-id="7781a-370">At the bottom of the DevTools window, the Drawer appears, with the **Quick Source** panel selected.</span></span>  <span data-ttu-id="7781a-371">El **panel Origen rápido** contiene el último archivo que editó en la herramienta **Orígenes,** dentro de una versión compacta del editor de código DevTools.</span><span class="sxs-lookup"><span data-stu-id="7781a-371">The **Quick Source** panel contains the last file you edited in the **Sources** tool, within a compact version of the DevTools code editor.</span></span>  
1.  <span data-ttu-id="7781a-372">Seleccione `Ctrl` + `P` \(Windows, Linux\) o `Command` + `P` \(macOS\) para \*\*\*\* abrir el cuadro de diálogo Abrir archivo.</span><span class="sxs-lookup"><span data-stu-id="7781a-372">Select `Ctrl`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  
    
## <a name="using-the-debugger-pane-to-debug-javascript-code"></a><span data-ttu-id="7781a-373">Uso del panel Depurador para depurar código JavaScript</span><span class="sxs-lookup"><span data-stu-id="7781a-373">Using the Debugger pane to debug JavaScript code</span></span>

<span data-ttu-id="7781a-374">Use el depurador de JavaScript para pasar por el código JavaScript devuelto por el servidor.</span><span class="sxs-lookup"><span data-stu-id="7781a-374">Use the JavaScript debugger to step through the JavaScript code that's returned by the server.</span></span>  
<span data-ttu-id="7781a-375">El depurador incluye el **panel Depurador,** junto con los puntos de interrupción que se establecen en líneas de código en el **panel Editor.**</span><span class="sxs-lookup"><span data-stu-id="7781a-375">The debugger includes the **Debugger** pane, along with breakpoints that you set on lines of code in the **Editor** pane.</span></span>

<span data-ttu-id="7781a-376">Con el depurador, se pasa por el código mientras se observan las expresiones de JavaScript especificadas.</span><span class="sxs-lookup"><span data-stu-id="7781a-376">With the debugger, you step through the code, while watching any JavaScript expressions you specify.</span></span>  <span data-ttu-id="7781a-377">Observe y cambie manualmente los valores de las variables y muestre automáticamente qué variables están en el ámbito de la instrucción actual.</span><span class="sxs-lookup"><span data-stu-id="7781a-377">Watch and manually change variable values, and automatically show which variables are in-scope for the current statement.</span></span>

:::image type="complex" source="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png" alt-text="El panel Depurador de la herramienta Orígenes  " lightbox="../media/sources-paused-breakpoint-highlight-debug-pane.msft.png":::
   <span data-ttu-id="7781a-379">El **panel Depurador** de la herramienta **Orígenes**</span><span class="sxs-lookup"><span data-stu-id="7781a-379">The **Debugger** pane of the **Sources** tool</span></span>  
:::image-end:::  

<span data-ttu-id="7781a-380">El depurador admite acciones de depuración estándar, como:</span><span class="sxs-lookup"><span data-stu-id="7781a-380">The debugger supports standard debugging actions, such as:</span></span>  

*   <span data-ttu-id="7781a-381">Establecer puntos de interrupción para pausar el código.</span><span class="sxs-lookup"><span data-stu-id="7781a-381">Setting breakpoints, to pause code.</span></span>  
*   <span data-ttu-id="7781a-382">Paso a paso por el código.</span><span class="sxs-lookup"><span data-stu-id="7781a-382">Stepping through code.</span></span>  
*   <span data-ttu-id="7781a-383">Visualización y edición de propiedades y variables.</span><span class="sxs-lookup"><span data-stu-id="7781a-383">Viewing and editing properties and variables.</span></span>  
*   <span data-ttu-id="7781a-384">Ver los valores de las expresiones de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7781a-384">Watching the values of JavaScript expressions.</span></span>  
*   <span data-ttu-id="7781a-385">Visualización de la pila de llamadas\ (la secuencia de llamadas de función hasta ahora\).</span><span class="sxs-lookup"><span data-stu-id="7781a-385">Viewing the call stack\ (the sequence of function calls so far\).</span></span>  
    
<span data-ttu-id="7781a-386">El depurador de DevTools está diseñado para que se vea, se sienta y funcione como el depurador de [Visual Studio Code][VisualStudioCodeDocsEditorDebugging] y el [depurador de Visual Studio][VisualStudioDebuggerNavigatingThroughCodeWithTheDebugger].</span><span class="sxs-lookup"><span data-stu-id="7781a-386">The debugger in DevTools is designed to look, feel, and work like [the debugger in Visual Studio Code][VisualStudioCodeDocsEditorDebugging] and [the debugger in Visual Studio][VisualStudioDebuggerNavigatingThroughCodeWithTheDebugger].</span></span>

<span data-ttu-id="7781a-387">Las subsecciones siguientes cubren la depuración:</span><span class="sxs-lookup"><span data-stu-id="7781a-387">The following subsections cover debugging:</span></span>  

*   [<span data-ttu-id="7781a-388">El enfoque básico para usar un depurador</span><span class="sxs-lookup"><span data-stu-id="7781a-388">The basic approach to using a debugger</span></span>](#the-basic-approach-to-using-a-debugger)  
*   [<span data-ttu-id="7781a-389">Ventajas de watch y scope sobre console.log del depurador</span><span class="sxs-lookup"><span data-stu-id="7781a-389">Advantages of the debugger's Watch and Scope over console.log</span></span>](#advantages-of-the-debuggers-watch-and-scope-over-consolelog)  
*   [<span data-ttu-id="7781a-390">Depurar desde Visual Studio Code directamente</span><span class="sxs-lookup"><span data-stu-id="7781a-390">Debug from Visual Studio Code directly</span></span>](#debug-from-visual-studio-code-directly)  
*   [<span data-ttu-id="7781a-391">Artículos sobre depuración</span><span class="sxs-lookup"><span data-stu-id="7781a-391">Articles about debugging</span></span>](#articles-about-debugging)  
    
### <a name="the-basic-approach-to-using-a-debugger"></a><span data-ttu-id="7781a-392">El enfoque básico para usar un depurador</span><span class="sxs-lookup"><span data-stu-id="7781a-392">The basic approach to using a debugger</span></span>

<span data-ttu-id="7781a-393">Para solucionar problemas de código JavaScript, puede insertar `console.log()` instrucciones en el panel **Editor.**</span><span class="sxs-lookup"><span data-stu-id="7781a-393">To troubleshoot JavaScript code, you can insert `console.log()` statements in the **Editor** pane.</span></span>  <span data-ttu-id="7781a-394">Otro enfoque más eficaz es usar el depurador de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="7781a-394">Another, more powerful approach is to use the debugger of Microsoft Edge DevTools.</span></span>  <span data-ttu-id="7781a-395">En realidad, el uso de un depurador puede ser más sencillo que , una vez que estés `console.log()` familiarizado con el enfoque del depurador.</span><span class="sxs-lookup"><span data-stu-id="7781a-395">Using a debugger can actually be simpler than `console.log()`, once you're familiar with the debugger approach.</span></span>

<span data-ttu-id="7781a-396">Para usar un depurador en una página web, normalmente se establece un punto de interrupción y, a continuación, se envía un formulario desde la página web, de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="7781a-396">To use a debugger on a webpage, you typically set a breakpoint and then send a form from the webpage, as follows:</span></span>

1.  <span data-ttu-id="7781a-397">Abra la página web en una nueva pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="7781a-397">Open the webpage in a new tab of the browser.</span></span>  <span data-ttu-id="7781a-398">Por ejemplo, abra esta página web de formulario en una pestaña [nueva: Demo: Introducción Debugging JavaScript with Microsoft Edge (Chromium) DevTools][GlitchMicrosoftEdgeChromiumDevtoolsDebugJsGetStarted].</span><span class="sxs-lookup"><span data-stu-id="7781a-398">For example, open this form webpage in a new tab: [Demo: Get Started Debugging JavaScript with Microsoft Edge (Chromium) DevTools][GlitchMicrosoftEdgeChromiumDevtoolsDebugJsGetStarted].</span></span>  
1.  <span data-ttu-id="7781a-399">Seleccione `F12` para abrir la ventana **DevTools** y, a continuación, seleccione la **pestaña** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="7781a-399">Select `F12` to open the **DevTools** window, and then select the **Sources** tab.</span></span>  
1.  <span data-ttu-id="7781a-400">En el **panel Navegador** \(a la izquierda\), seleccione la pestaña **Página** y, a continuación, seleccione el archivo JavaScript, como `get-started.js` .</span><span class="sxs-lookup"><span data-stu-id="7781a-400">In the **Navigator** pane \(on the left\), select the **Page** tab, and then select the JavaScript file, such as `get-started.js`.</span></span>  
1.  <span data-ttu-id="7781a-401">En el **panel Editor,** seleccione un número de línea cerca de una línea de código sospechosa para establecer un punto de interrupción en esa línea.</span><span class="sxs-lookup"><span data-stu-id="7781a-401">In the **Editor** pane, select a line number near a suspect line of code, to set a breakpoint on that line.</span></span>  <span data-ttu-id="7781a-402">En la figura siguiente, se establece un punto de interrupción en la línea `var sum = addend1 + addend2;` .</span><span class="sxs-lookup"><span data-stu-id="7781a-402">In the figure below, a breakpoint is set on the line `var sum = addend1 + addend2;`.</span></span>  
1.  <span data-ttu-id="7781a-403">En la página web, escriba valores y envíe el formulario.</span><span class="sxs-lookup"><span data-stu-id="7781a-403">In the webpage, enter values and submit the form.</span></span>  <span data-ttu-id="7781a-404">Por ejemplo, escriba números, como y, a continuación, seleccione el botón `5` `1` Agregar número **1 y Número 2**.</span><span class="sxs-lookup"><span data-stu-id="7781a-404">For example, enter numbers, such as `5` and `1`, then select the button **Add Number 1 and Number 2**.</span></span>  
    
    <span data-ttu-id="7781a-405">El depurador ejecuta el código JavaScript y, a continuación, se pausa en el punto de interrupción.</span><span class="sxs-lookup"><span data-stu-id="7781a-405">The debugger runs the JavaScript code and then pauses at the breakpoint.</span></span>  <span data-ttu-id="7781a-406">El depurador está ahora en modo pausado, por lo que puede inspeccionar los valores de las propiedades que están en el ámbito y pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="7781a-406">The debugger is now in Paused mode, so you can inspect the values of the properties that are in-scope, and step through the code.</span></span>  
    
    :::image type="complex" source="../media/sources-paused-breakpoint-highlights.msft.png" alt-text="Introducción al modo pausado del depurador" lightbox="../media/sources-paused-breakpoint-highlights.msft.png":::
        <span data-ttu-id="7781a-408">Introducción al modo pausado del depurador</span><span class="sxs-lookup"><span data-stu-id="7781a-408">Entering Paused mode of the debugger</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="7781a-409">En la figura anterior, agregamos las expresiones Watch y , y hemos pasado dos `sum` líneas más allá del punto de `typeof sum` interrupción.</span><span class="sxs-lookup"><span data-stu-id="7781a-409">In the above figure, we added the Watch expressions `sum` and `typeof sum`, and stepped two lines past the breakpoint.</span></span>  
    
1.  <span data-ttu-id="7781a-410">Examine los valores del **panel Ámbito,** que muestra todas las variables o propiedades que están dentro del ámbito del punto de interrupción actual y sus valores.</span><span class="sxs-lookup"><span data-stu-id="7781a-410">Examine the values in the **Scope** pane, which shows all variables or properties that are in-scope for the current breakpoint, and their values.</span></span>  <span data-ttu-id="7781a-411">O bien, agregue expresiones en el **panel** Ver.</span><span class="sxs-lookup"><span data-stu-id="7781a-411">Or, add expressions in the **Watch** pane.</span></span>  <span data-ttu-id="7781a-412">Estas expresiones son las mismas expresiones que escribiría en una `console.log` instrucción para depurar el código.</span><span class="sxs-lookup"><span data-stu-id="7781a-412">These expressions are the same expressions that you would write within a `console.log` statement to debug your code.</span></span>  <span data-ttu-id="7781a-413">Para ejecutar comandos de JavaScript para manipular datos en el contexto actual, use la **consola**.</span><span class="sxs-lookup"><span data-stu-id="7781a-413">To run JavaScript commands to manipulate data in the current context, use the **Console**.</span></span>  <span data-ttu-id="7781a-414">Para abrir la consola, seleccione `Esc` .</span><span class="sxs-lookup"><span data-stu-id="7781a-414">To open the console, select `Esc`.</span></span>  
1.  <span data-ttu-id="7781a-415">Pase por el código mediante los controles de la parte superior del panel **Depurador,** como **Step** \( `F9` \).</span><span class="sxs-lookup"><span data-stu-id="7781a-415">Step through the code by using the controls at the top of the **Debugger** pane, such as **Step** \(`F9`\).</span></span>
    
#### <a name="see-also"></a><span data-ttu-id="7781a-416">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7781a-416">See also</span></span>

*   <span data-ttu-id="7781a-417">[Introducción a la depuración de JavaScript:][DevtoolsGuideChromiumJavascriptIndex] un tutorial con una página web sencilla y existente que contiene algunos controles de formulario.</span><span class="sxs-lookup"><span data-stu-id="7781a-417">[Get started with debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] - a tutorial using an existing, simple webpage that contains a few form controls.</span></span>
    
### <a name="advantages-of-the-debuggers-watch-and-scope-over-consolelog"></a><span data-ttu-id="7781a-418">Ventajas del depurador \'s Watch and Scope over console\.log</span><span class="sxs-lookup"><span data-stu-id="7781a-418">Advantages of the debugger\'s Watch and Scope over console\.log</span></span>  

<span data-ttu-id="7781a-419">Estos tres enfoques son equivalentes:</span><span class="sxs-lookup"><span data-stu-id="7781a-419">These three approaches are equivalent:</span></span>

*   <span data-ttu-id="7781a-420">Agregar temporalmente las instrucciones `console.log(sum)` y `console.log(typeof sum)` en el código, donde está en `sum` el ámbito.</span><span class="sxs-lookup"><span data-stu-id="7781a-420">Temporarily adding the statements `console.log(sum)` and `console.log(typeof sum)` in the code, where `sum` is in-scope.</span></span>  
*   <span data-ttu-id="7781a-421">Emitir las instrucciones y en el panel Consola de DevTools, cuando el depurador se pausa `sum` donde está en el `console.log(typeof sum)` \*\*\*\* `sum` ámbito.</span><span class="sxs-lookup"><span data-stu-id="7781a-421">Issuing the statements `sum` and `console.log(typeof sum)` in the **Console** pane of the DevTools, when the debugger is paused where `sum` is in-scope.</span></span>  
*   <span data-ttu-id="7781a-422">Establecer las **expresiones** Watch `sum` y en el panel `typeof sum` **Depurador.**</span><span class="sxs-lookup"><span data-stu-id="7781a-422">Setting the **Watch** expressions `sum` and `typeof sum` in the **Debugger** pane.</span></span>  
    
<span data-ttu-id="7781a-423">Cuando la variable está en el ámbito y su valor se muestra automáticamente en la sección Ámbito del panel Depurador, y también se sobrelada en el panel Editor donde `sum` `sum` se \*\*\*\* \*\*\*\* `sum` calcula.</span><span class="sxs-lookup"><span data-stu-id="7781a-423">When the variable `sum` is in-scope, `sum` and its value are automatically shown in the **Scope** section of the **Debugger** pane, and are also overlaid in the Editor pane where `sum` is calculated.</span></span>  <span data-ttu-id="7781a-424">Por lo tanto, probablemente no tendría que definir una expresión Watch para `sum` .</span><span class="sxs-lookup"><span data-stu-id="7781a-424">So you probably wouldn't need to define a Watch expression for `sum`.</span></span>

<span data-ttu-id="7781a-425">El depurador proporciona una pantalla y un entorno más enriquecidos y flexibles que una `console.log` instrucción.</span><span class="sxs-lookup"><span data-stu-id="7781a-425">The debugger gives a richer, more flexible display and environment than a `console.log` statement.</span></span>  <span data-ttu-id="7781a-426">Por ejemplo, en el depurador, al pasar por el código, puede mostrar y cambiar los valores de todas las propiedades y variables definidas actualmente.</span><span class="sxs-lookup"><span data-stu-id="7781a-426">For example, in the debugger, as you step through the code, you can display and change the values of all currently defined properties and variables.</span></span>  <span data-ttu-id="7781a-427">También puede emitir instrucciones JavaScript en **la consola,** como cambiar los valores de una matriz que está dentro del ámbito.</span><span class="sxs-lookup"><span data-stu-id="7781a-427">You can also issue JavaScript statements in the **Console**, such as to change values in an array that's in-scope.</span></span>  <span data-ttu-id="7781a-428">\(Para mostrar la consola, **seleccione Esc**.\)</span><span class="sxs-lookup"><span data-stu-id="7781a-428">\(To display the Console, select **Esc**.\)</span></span>

<span data-ttu-id="7781a-429">Los puntos de interrupción y las expresiones watch se conservan al actualizar la página web.</span><span class="sxs-lookup"><span data-stu-id="7781a-429">Breakpoints and Watch expressions are preserved when you refresh the webpage.</span></span>

### <a name="debug-from-visual-studio-code-directly"></a><span data-ttu-id="7781a-430">Depurar desde Visual Studio Code directamente</span><span class="sxs-lookup"><span data-stu-id="7781a-430">Debug from Visual Studio Code directly</span></span>

<span data-ttu-id="7781a-431">Para usar el depurador más completo de Visual Studio Code en lugar del depurador DevTools, use la extensión herramientas de Microsoft Edge **para** VS Code para Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="7781a-431">To use the more full-featured debugger of Visual Studio Code instead of the DevTools debugger, use the **Microsoft Edge Tools for VS Code** extension for Visual Studio Code.</span></span>

:::image type="complex" source="../media/microsoft-edge-tools-for-vs-code-extension.msft.png" alt-text="La Microsoft Edge herramientas de VS Code para Visual Studio Code" lightbox="../media/microsoft-edge-tools-for-vs-code-extension.msft.png":::
   <span data-ttu-id="7781a-433">La **Microsoft Edge herramientas de VS Code** para Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="7781a-433">The **Microsoft Edge Tools for VS Code** extension for Visual Studio Code</span></span>  
:::image-end:::  

<span data-ttu-id="7781a-434">Esta extensión proporciona acceso \*\*\*\* a los **elementos** y herramientas de red de Microsoft Edge DevTools, desde dentro Microsoft Visual Studio código.</span><span class="sxs-lookup"><span data-stu-id="7781a-434">This extension provides access to the **Elements** and **Network** tools of Microsoft Edge DevTools, from within Microsoft Visual Studio Code.</span></span>  

<span data-ttu-id="7781a-435">Para obtener más información, [Visual Studio Code información general][VisualStudioCodeIndex] y la GitHub Léame, Microsoft Edge Developer Tools for [Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="7781a-435">For more information, see [Visual Studio Code overview][VisualStudioCodeIndex] and the GitHub Readme page, [Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools].</span></span>

### <a name="articles-about-debugging"></a><span data-ttu-id="7781a-436">Artículos sobre depuración</span><span class="sxs-lookup"><span data-stu-id="7781a-436">Articles about debugging</span></span>

<span data-ttu-id="7781a-437">Los siguientes artículos abarcan el **panel Depurador** y los puntos de interrupción:</span><span class="sxs-lookup"><span data-stu-id="7781a-437">The following articles cover the **Debugger** pane and breakpoints:</span></span>

*   <span data-ttu-id="7781a-438">[Introducción a la depuración de JavaScript en Microsoft Edge DevTools:][DevtoolsGuideChromiumJavascriptIndex] un tutorial \(con capturas de pantalla\), mediante un proyecto simple y existente.</span><span class="sxs-lookup"><span data-stu-id="7781a-438">[Get started with debugging JavaScript in Microsoft Edge DevTools][DevtoolsGuideChromiumJavascriptIndex] - A tutorial \(with screen captures\), using an existing, simple project.</span></span>  
*   <span data-ttu-id="7781a-439">[Usar las características][DevToolsJavaScriptReference] del depurador: cómo usar el depurador para establecer puntos de interrupción, pasar por el código, ver y modificar valores de variables, ver expresiones de JavaScript y ver la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="7781a-439">[Use the debugger features][DevToolsJavaScriptReference] - How to use the debugger to set breakpoints, step through code, view and modify variable values, watch JavaScript expressions, and view the call stack.</span></span>  
*   <span data-ttu-id="7781a-440">[Pausar el código con puntos de interrupción:][DevToolsJavaScriptBreakpoints] cómo establecer puntos de interrupción básicos y especializados en el depurador.</span><span class="sxs-lookup"><span data-stu-id="7781a-440">[Pause your code with breakpoints][DevToolsJavaScriptBreakpoints] - How to set basic and specialized breakpoints in the debugger.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="7781a-441">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7781a-441">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsBeginnersCss]: ../beginners/css.md "DevTools para principiantes: Introducción a CSS | Microsoft Docs"  
[DevToolsBeginnersHtml]: ../beginners/html.md "DevTools para principiantes: Introducción a HTML y el dom | Microsoft Docs"  
[DevToolsCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"   
[DevtoolsCustomizeIndexDrawer]: ../customize/index.md#drawer "Drawer: personalice Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar Microsoft Edge ubicación de DevTools (Undock, Dock to bottom, Dock to left) | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptIndex]: ../javascript/index.md "Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumJavascriptSnippets]: ../javascript/snippets.md "Ejecutar fragmentos de código de JavaScript en cualquier página web con Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumWorkspacesIndex]: ../workspaces/index.md "Editar archivos con áreas de trabajo | Microsoft Docs"  
[DevToolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos y opciones de fuente CSS en el panel Estilos | Microsoft Docs"  
[DevToolsJavaScriptBreakpoints]: ../javascript/breakpoints.md "Pausa el código con puntos de interrupción | Microsoft Docs"  
[DevToolsJavaScriptGuidesMarkContentScriptsLibraryCode]: ../javascript/guides/mark-content-scripts-library-code.md "Marcar scripts de contenido como código de biblioteca | Microsoft Docs"  
[DevtoolsJavascriptOverrides]: ../javascript/overrides.md "Invalidar recursos de página web con copias locales mediante Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsJavaScriptReference]: ../javascript/reference.md "Usar las características del depurador | Microsoft Docs"  
[DevToolsJavaScriptReferenceReformat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Volver a formatear un archivo JavaScript minificado con pretty-print: use las características del depurador | Microsoft Docs"  
[DevToolsJavaScriptSourceMaps]: ../javascript/source-maps.md "Asignar código preprocesado al código fuente | Microsoft Docs"  
[VisualStudioCodeIndex]: ../../visual-studio-code/index.md "Visual Studio Code información general | Microsoft Docs"  
[ExtensionsChromiumGetstartPart2ContentScripts]: ../../extensions-chromium/getting-started/part2-content-scripts.md "Crear un tutorial de extensión Parte 2 | Microsoft Docs"  

[VisualStudioDebuggerNavigatingThroughCodeWithTheDebugger]: /visualstudio/debugger/navigating-through-code-with-the-debugger "Navegue por el código con el Visual Studio de | Microsoft Docs"  

[VisualStudioCodeDocsEditorDebugging]: https://code.visualstudio.com/docs/editor/debugging "Depuración | Visual Studio Code"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "Microsoft Edge Herramientas de desarrollador para Visual Studio Code | GitHub"  

[GlitchMicrosoftEdgeChromiumDevtoolsDebugJsGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/debug-js/get-started.html "Demostración: Introducción Depuración de JavaScript con Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[WhatwgHtmlSpecMulitpageOriginHtmlOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origen | Estándar HTML"  

[MdnAddOnsWebextensionsContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de contenido | MDN"  

[TypescriptlangMain]: https://www.typescriptlang.org "TypeScript"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Fotogramas | W3C"  

> [!NOTE]
> <span data-ttu-id="7781a-467">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7781a-467">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7781a-468">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/sources) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="7781a-468">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7781a-470">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7781a-470">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  

<!--todo: needs an accessibility review to replace "view", "see", and "look" with "display", exception is "see also" headings -->  

<!--todo: need a consistency review to replace all UI interactions with "choose" and all keyboard interactions with "select" -->  
