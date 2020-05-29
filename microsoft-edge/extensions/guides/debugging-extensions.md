---
description: Con las herramientas de desarrollo F12, aprenda a depurar el script de fondo de una extensión, los scripts de contenido y las páginas de extensión.
title: Extensiones-depuración
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, JavaScript, desarrollador, depuración, depuración
ms.custom: seodec18
ms.openlocfilehash: 34488870cb4e4a92a9d57859509ce7d1176cf284
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573636"
---
# <span data-ttu-id="332db-104">Extensiones de depuración</span><span class="sxs-lookup"><span data-stu-id="332db-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="332db-105">Puede depurar las extensiones en Microsoft Edge con las herramientas de desarrollo F12.</span><span class="sxs-lookup"><span data-stu-id="332db-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>

<span data-ttu-id="332db-106">El siguiente vídeo pasa por una extensión de Microsoft Edge con errores, caminar a través de cada escenario de depuración y corregirlo a lo largo del camino.</span><span class="sxs-lookup"><span data-stu-id="332db-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span> <span data-ttu-id="332db-107">Para obtener más información, consulta las instrucciones paso a paso más adelante.</span><span class="sxs-lookup"><span data-stu-id="332db-107">See the step-by-step instructions below for more info.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> <span data-ttu-id="332db-108">Para aprovechar las ventajas de la depuración de la extensión con F12, primero debe activar las características para desarrolladores en about: Flags.</span><span class="sxs-lookup"><span data-stu-id="332db-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span> <span data-ttu-id="332db-109">Consulte [Agregar y quitar extensiones](./adding-and-removing-extensions.md) para obtener más información sobre cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="332db-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>


## <span data-ttu-id="332db-110">Depuración de script de fondo</span><span class="sxs-lookup"><span data-stu-id="332db-110">Background script debugging</span></span>
<span data-ttu-id="332db-111">Para empezar a depurar el script de fondo de su extensión:</span><span class="sxs-lookup"><span data-stu-id="332db-111">To start debugging the background script of your extension:</span></span>

1. <span data-ttu-id="332db-112">Haga clic en **más (...)** seguido de **extensiones** para ir al panel de extensiones.</span><span class="sxs-lookup"><span data-stu-id="332db-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
 ![botón más](./../media/morebutton.png)
2. <span data-ttu-id="332db-114">Haga clic en la extensión que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="332db-114">Click on the extension that you want to debug.</span></span>
3. <span data-ttu-id="332db-115">Haga clic en el vínculo de la **Página de fondo** para que se muestre F12 para el proceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="332db-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
 ![vista de extensión seleccionada de las opciones con el vínculo de inspección](./../media/debug-inspect.png)
4. <span data-ttu-id="332db-117">Seleccione la pestaña **depurador** en F12.</span><span class="sxs-lookup"><span data-stu-id="332db-117">Select the **Debugger** tab in F12.</span></span>
5. <span data-ttu-id="332db-118">Navegue hasta el script de fondo de la extensión y selecciónelo.</span><span class="sxs-lookup"><span data-stu-id="332db-118">Navigate to and select your extension's background script.</span></span>
6. <span data-ttu-id="332db-119">Coloque puntos de interrupción para la depuración haciendo clic a la izquierda del número de línea del código de origen.</span><span class="sxs-lookup"><span data-stu-id="332db-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![consola F12 que muestra el script de fondo con puntos de interrupción](./../media/debug-f12-background.png)
7. <span data-ttu-id="332db-121">Seleccione la ficha **Console (consola** ) y ejecute el comando " `location.reload()` ".</span><span class="sxs-lookup"><span data-stu-id="332db-121">Select the **Console** tab and execute the command "`location.reload()`".</span></span> <span data-ttu-id="332db-122">Esto volverá a ejecutar el script de fondo, lo que le permitirá recorrer el código.</span><span class="sxs-lookup"><span data-stu-id="332db-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
 ![consola con ubicación. recarga introducida](./../media/debug-f12-background-console.png)


## <span data-ttu-id="332db-124">Depuración de script de contenido</span><span class="sxs-lookup"><span data-stu-id="332db-124">Content script debugging</span></span>
<span data-ttu-id="332db-125">Para empezar a depurar el script de contenido de la extensión:</span><span class="sxs-lookup"><span data-stu-id="332db-125">To start debugging the content script of your extension:</span></span>

1. <span data-ttu-id="332db-126">Para iniciar F12, navegue hasta el botón **más (...)** y seleccione **"herramientas para desarrolladores F12"** o presione F12 en el teclado.</span><span class="sxs-lookup"><span data-stu-id="332db-126">Launch F12 by either navigating to the **More (...)** button and selecting **"F12 Developer Tools"** or by pressing F12 on your keyboard.</span></span>
2. <span data-ttu-id="332db-127">Desplácese hasta el script de contenido de la extensión y selecciónelo.</span><span class="sxs-lookup"><span data-stu-id="332db-127">Navigate to and select your extension's content script.</span></span> <span data-ttu-id="332db-128">Los scripts de contenido para las extensiones que se están ejecutando se representarán mediante una carpeta diferente para cada extensión.</span><span class="sxs-lookup"><span data-stu-id="332db-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>

    > [!NOTE]
    > <span data-ttu-id="332db-129">Solo aparecerán los scripts de contenido en ejecución.</span><span class="sxs-lookup"><span data-stu-id="332db-129">Only running content scripts will appear.</span></span>

3. <span data-ttu-id="332db-130">Coloque puntos de interrupción para la depuración haciendo clic a la izquierda del número de línea del código de origen.</span><span class="sxs-lookup"><span data-stu-id="332db-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![F12 con secuencia de comandos de contenido en proceso de depuración](./../media/debug-content-f12.png)
4. <span data-ttu-id="332db-132">Actualice la pestaña del explorador para empezar a desplazarse por el código.</span><span class="sxs-lookup"><span data-stu-id="332db-132">Refresh the browser tab to begin stepping though your code.</span></span>




## <span data-ttu-id="332db-133">Depuración de la página de extensión</span><span class="sxs-lookup"><span data-stu-id="332db-133">Extension page debugging</span></span>

<span data-ttu-id="332db-134">Hay dos métodos que se pueden usar para obtener acceso al código fuente de la página de extensión para la depuración.</span><span class="sxs-lookup"><span data-stu-id="332db-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span> <span data-ttu-id="332db-135">Un método se aplica a varias páginas, mientras que la otra solo funciona con páginas emergentes.</span><span class="sxs-lookup"><span data-stu-id="332db-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>

### <span data-ttu-id="332db-136">Depurar cualquier página de extensión</span><span class="sxs-lookup"><span data-stu-id="332db-136">Debugging any extension page</span></span>
<span data-ttu-id="332db-137">El siguiente método funciona para todas las páginas de extensión como la página de opciones y los elementos emergentes:</span><span class="sxs-lookup"><span data-stu-id="332db-137">The following method works for all extension pages like the options page and popups:</span></span>


1. <span data-ttu-id="332db-138">Haga clic con el botón derecho en el fondo de la página.</span><span class="sxs-lookup"><span data-stu-id="332db-138">Right-click on the background of your page.</span></span>
2. <span data-ttu-id="332db-139">Seleccione **"ver origen"**.</span><span class="sxs-lookup"><span data-stu-id="332db-139">Select **"View source"**.</span></span>

   ![depuración de elementos emergentes con F12](./../media/debug-popup-select.png)

3. <span data-ttu-id="332db-141">Una vez que se abra F12, coloque puntos de interrupción dentro del archivo que quiera depurar.</span><span class="sxs-lookup"><span data-stu-id="332db-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>

   ![depuración de elementos emergentes con F12](./../media/debug-popup-f12.png)
4. <span data-ttu-id="332db-143">Seleccione la ficha **Console (consola** ) y ejecute el comando `location.reload()` .</span><span class="sxs-lookup"><span data-stu-id="332db-143">Select the **Console** tab and execute the command `location.reload()`.</span></span> <span data-ttu-id="332db-144">Esto volverá a ejecutar la secuencia de comandos de la página, lo que le permitirá recorrer el código.</span><span class="sxs-lookup"><span data-stu-id="332db-144">This will re-execute the page script, allowing you to step through your code.</span></span>  

   ![consola con ubicación. recarga introducida](./../media/debug-f12-background-console.png)

### <span data-ttu-id="332db-146">Depurar una página de extensión emergente</span><span class="sxs-lookup"><span data-stu-id="332db-146">Debugging a popup extension page</span></span>
<span data-ttu-id="332db-147">Aunque el método para la depuración de páginas de extensión también se aplica a las páginas de extensión emergentes, los pasos siguientes describen otra manera de depurar el elemento emergente:</span><span class="sxs-lookup"><span data-stu-id="332db-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>

1. <span data-ttu-id="332db-148">Haga clic con el botón secundario en el icono de la extensión.</span><span class="sxs-lookup"><span data-stu-id="332db-148">Right-click your extension's icon.</span></span>
2. <span data-ttu-id="332db-149">Seleccione **"Inspeccionar mensaje emergente"**.</span><span class="sxs-lookup"><span data-stu-id="332db-149">Select **"Inspect popup"**.</span></span>

   ![inspección de depuración de popup](./../media/debug-popup-inspect.png)
3. <span data-ttu-id="332db-151">Siga los pasos 3 y 4 anteriores para colocar puntos de interrupción y volver a cargar el elemento emergente.</span><span class="sxs-lookup"><span data-stu-id="332db-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>
