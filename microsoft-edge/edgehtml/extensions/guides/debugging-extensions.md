---
description: Con F12 Developer Tools, aprenda a depurar el script en segundo plano, los scripts de contenido y las páginas de extensión de una extensión.
title: Depuración | Extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, javascript, developer, debug, debugging
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399368"
---
# <a name="debugging-extensions"></a><span data-ttu-id="2cc18-104">Depuración de extensiones</span><span class="sxs-lookup"><span data-stu-id="2cc18-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="2cc18-105">Puede depurar las extensiones en Microsoft Edge mediante F12 Developer Tools.</span><span class="sxs-lookup"><span data-stu-id="2cc18-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>  

<span data-ttu-id="2cc18-106">El siguiente vídeo pasa por una extensión de Microsoft Edge con errores, paseando por cada escenario de depuración y corrigiendo el camino.</span><span class="sxs-lookup"><span data-stu-id="2cc18-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span>  <span data-ttu-id="2cc18-107">Consulta las instrucciones paso a paso que aparecen a continuación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="2cc18-107">See the step-by-step instructions below for more info.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> <span data-ttu-id="2cc18-108">Para aprovechar la depuración de extensiones con F12, primero debe activar las características del desarrollador en about:flags.</span><span class="sxs-lookup"><span data-stu-id="2cc18-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span>  <span data-ttu-id="2cc18-109">Consulte [Agregar y quitar extensiones para](./adding-and-removing-extensions.md) obtener más información sobre cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="2cc18-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>  

## <a name="background-script-debugging"></a><span data-ttu-id="2cc18-110">Depuración de scripts en segundo plano</span><span class="sxs-lookup"><span data-stu-id="2cc18-110">Background script debugging</span></span>  

<span data-ttu-id="2cc18-111">Para empezar a depurar el script en segundo plano de la extensión:</span><span class="sxs-lookup"><span data-stu-id="2cc18-111">To start debugging the background script of your extension:</span></span>  

1.  <span data-ttu-id="2cc18-112">Haga clic **en Más (...)** seguido de **Extensiones** para ir al panel de extensiones.</span><span class="sxs-lookup"><span data-stu-id="2cc18-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
    
    ![botón más](../media/morebutton.png)  
    
1.  <span data-ttu-id="2cc18-114">Haga clic en la extensión que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="2cc18-114">Click on the extension that you want to debug.</span></span>  
1.  <span data-ttu-id="2cc18-115">Haga clic en **el vínculo Página en** segundo plano para mostrar F12 para el proceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="2cc18-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
    
    ![vista de extensión seleccionada de las opciones con vínculo inspeccionar](../media/debug-inspect.png)  
    
1.  <span data-ttu-id="2cc18-117">Seleccione la **pestaña Depurador** en F12.</span><span class="sxs-lookup"><span data-stu-id="2cc18-117">Select the **Debugger** tab in F12.</span></span>  
1.  <span data-ttu-id="2cc18-118">Vaya a y seleccione el script en segundo plano de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2cc18-118">Navigate to and select your extension's background script.</span></span>  
1.  <span data-ttu-id="2cc18-119">Coloque puntos de interrupción para la depuración haciendo clic a la izquierda del número de línea de código fuente.</span><span class="sxs-lookup"><span data-stu-id="2cc18-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![Consola f12 que muestra script en segundo plano con puntos de interrupción](../media/debug-f12-background.png)  
    
1.  <span data-ttu-id="2cc18-121">Seleccione la **pestaña Consola** y ejecute el `location.reload()` comando.</span><span class="sxs-lookup"><span data-stu-id="2cc18-121">Select the **Console** tab and execute the `location.reload()` command.</span></span>  <span data-ttu-id="2cc18-122">Esto volverá a ejecutar el script en segundo plano, lo que le permitirá pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="2cc18-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
    
    ![consola con location.reload escrito](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a><span data-ttu-id="2cc18-124">Depuración de scripts de contenido</span><span class="sxs-lookup"><span data-stu-id="2cc18-124">Content script debugging</span></span>  

<span data-ttu-id="2cc18-125">Para empezar a depurar el script de contenido de la extensión:</span><span class="sxs-lookup"><span data-stu-id="2cc18-125">To start debugging the content script of your extension:</span></span>  

1.  <span data-ttu-id="2cc18-126">Inicie F12 navegando al botón **Más (...)** y **seleccionando F12 Developer Tools** o presionando en el `F12` teclado.</span><span class="sxs-lookup"><span data-stu-id="2cc18-126">Launch F12 by either navigating to the **More (...)** button and selecting **F12 Developer Tools** or by pressing `F12` on your keyboard.</span></span>  
1.  <span data-ttu-id="2cc18-127">Vaya a y seleccione el script de contenido de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2cc18-127">Navigate to and select your extension's content script.</span></span>  <span data-ttu-id="2cc18-128">Los scripts de contenido de las extensiones que se están ejecutando actualmente se representarán en una carpeta diferente para cada extensión.</span><span class="sxs-lookup"><span data-stu-id="2cc18-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="2cc18-129">Solo aparecerán scripts de contenido en ejecución.</span><span class="sxs-lookup"><span data-stu-id="2cc18-129">Only running content scripts will appear.</span></span>  
    
1.  <span data-ttu-id="2cc18-130">Coloque puntos de interrupción para la depuración haciendo clic a la izquierda del número de línea de código fuente.</span><span class="sxs-lookup"><span data-stu-id="2cc18-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
    
    ![f12 con script de contenido que se está depurando](../media/debug-content-f12.png)  
    
1.  <span data-ttu-id="2cc18-132">Actualice la pestaña del explorador para empezar a pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="2cc18-132">Refresh the browser tab to begin stepping though your code.</span></span>  
    
## <a name="extension-page-debugging"></a><span data-ttu-id="2cc18-133">Depuración de páginas de extensión</span><span class="sxs-lookup"><span data-stu-id="2cc18-133">Extension page debugging</span></span>  

<span data-ttu-id="2cc18-134">Existen dos métodos que se pueden usar para obtener acceso al código fuente de la página de extensión para la depuración.</span><span class="sxs-lookup"><span data-stu-id="2cc18-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span>  <span data-ttu-id="2cc18-135">Un método se aplica a una variedad de páginas mientras que el otro solo funciona para páginas emergentes.</span><span class="sxs-lookup"><span data-stu-id="2cc18-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>  

### <a name="debugging-any-extension-page"></a><span data-ttu-id="2cc18-136">Depurar cualquier página de extensión</span><span class="sxs-lookup"><span data-stu-id="2cc18-136">Debugging any extension page</span></span>  

<span data-ttu-id="2cc18-137">El siguiente método funciona para todas las páginas de extensión, como la página de opciones y los elementos emergentes:</span><span class="sxs-lookup"><span data-stu-id="2cc18-137">The following method works for all extension pages like the options page and popups:</span></span>  

1.  <span data-ttu-id="2cc18-138">Haga clic con el botón secundario en el fondo de la página.</span><span class="sxs-lookup"><span data-stu-id="2cc18-138">Right-click on the background of your page.</span></span>  
1.  <span data-ttu-id="2cc18-139">Seleccione **Ver origen**.</span><span class="sxs-lookup"><span data-stu-id="2cc18-139">Select **View source**.</span></span>  
    
    ![Abrir depuración emergente con f12](../media/debug-popup-select.png)  
    
1.  <span data-ttu-id="2cc18-141">Una vez que se abra F12, coloque los puntos de interrupción en el archivo que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="2cc18-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>  
    
    ![depuración emergente con f12](../media/debug-popup-f12.png)  
    
1.  <span data-ttu-id="2cc18-143">Seleccione la **pestaña Consola** y ejecute el comando `location.reload()` .</span><span class="sxs-lookup"><span data-stu-id="2cc18-143">Select the **Console** tab and execute the command `location.reload()`.</span></span>  <span data-ttu-id="2cc18-144">Esto volverá a ejecutar el script de página, lo que le permitirá pasar por el código.</span><span class="sxs-lookup"><span data-stu-id="2cc18-144">This will re-execute the page script, allowing you to step through your code.</span></span>  
    
    ![consola con location.reload escrito](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a><span data-ttu-id="2cc18-146">Depurar una página de extensión emergente</span><span class="sxs-lookup"><span data-stu-id="2cc18-146">Debugging a popup extension page</span></span>  

<span data-ttu-id="2cc18-147">Aunque el método para depurar páginas de extensión también se aplica a las páginas de extensión emergentes, los pasos siguientes describen otra forma de depurar el elemento emergente:</span><span class="sxs-lookup"><span data-stu-id="2cc18-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>  

1.  <span data-ttu-id="2cc18-148">Haga clic con el botón secundario en el icono de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2cc18-148">Right-click your extension's icon.</span></span>  
1.  <span data-ttu-id="2cc18-149">Seleccione **Inspeccionar elemento emergente**.</span><span class="sxs-lookup"><span data-stu-id="2cc18-149">Select **Inspect popup**.</span></span>  
    
    ![inspección de depuración emergente](../media/debug-popup-inspect.png)  
    
1.  <span data-ttu-id="2cc18-151">Siga los pasos 3 y 4 anteriores para colocar puntos de interrupción y volver a cargar el elemento emergente.</span><span class="sxs-lookup"><span data-stu-id="2cc18-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>  
    