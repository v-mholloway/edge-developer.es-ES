---
description: Use la herramienta de consola para la depuración interactiva y las pruebas ad hoc.
title: DevTools-consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, consola
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 472aafa9e6c6fd98ea952804f0e92ed0b774f59c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236164"
---
# <span data-ttu-id="f0771-104">Consola</span><span class="sxs-lookup"><span data-stu-id="f0771-104">Console</span></span>

<span data-ttu-id="f0771-105">La herramienta de desarrollador de consola de Microsoft Edge registra información que está asociada a una página web, como JavaScript, solicitudes de red y errores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f0771-105">The Console developer tool in Microsoft Edge logs information that's associated with a webpage, such as JavaScript, network requests, and security errors.</span></span> <span data-ttu-id="f0771-106">Puede usar la consola para la depuración interactiva y las pruebas ad hoc.</span><span class="sxs-lookup"><span data-stu-id="f0771-106">You can use the Console for interactive debugging and ad hoc testing.</span></span> 

<span data-ttu-id="f0771-107">Para abrir la herramienta de consola en Microsoft Edge, presione la tecla F12 para acceder a la ventana de la herramienta de desarrollador (o haga clic con el botón derecho en la página y, a continuación, seleccione **Inspeccionar elemento**).</span><span class="sxs-lookup"><span data-stu-id="f0771-107">To open the Console tool in Microsoft Edge, press the F12 key to access the developer tool window (or right-click on the page, and then select **Inspect Element**).</span></span> <span data-ttu-id="f0771-108">Después, seleccione la pestaña de **consola** en la parte superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f0771-108">Then, select the **Console** tab at the top of the window.</span></span> 

<span data-ttu-id="f0771-109">También puede usar la herramienta de consola para comunicarse con una página web en ejecución y desde ella.</span><span class="sxs-lookup"><span data-stu-id="f0771-109">You can also use the Console tool to communicate to and from a running webpage.</span></span> <span data-ttu-id="f0771-110">Puede usar la consola para:</span><span class="sxs-lookup"><span data-stu-id="f0771-110">You can use the Console to:</span></span>

- <span data-ttu-id="f0771-111">Publique [códigos de estado y errores](./console/error-and-status-codes.md) estándar y mensajes informativos mientras se ejecuta el código.</span><span class="sxs-lookup"><span data-stu-id="f0771-111">Post standard [error and status codes](./console/error-and-status-codes.md) and informational messages as your code runs.</span></span>
- <span data-ttu-id="f0771-112">Genera registros de depuración personalizados de las llamadas [API de consola](./console/console-api.md) que incluyas en el código.</span><span class="sxs-lookup"><span data-stu-id="f0771-112">Generate custom debug logs from the [Console API](./console/console-api.md) calls you include in your code.</span></span>
- <span data-ttu-id="f0771-113">Proporciona una [línea de comandos](./console/command-line.md) y una vista de árbol interactiva para inspeccionar los valores devueltos actuales de las variables y funciones clave.</span><span class="sxs-lookup"><span data-stu-id="f0771-113">Provide a [command line](./console/command-line.md) and interactive tree view for inspecting current return values of key variables and functions.</span></span>

## <span data-ttu-id="f0771-114">Partes de la consola</span><span class="sxs-lookup"><span data-stu-id="f0771-114">Parts of the Console</span></span>

<span data-ttu-id="f0771-115">La imagen siguiente muestra las partes principales de la consola:</span><span class="sxs-lookup"><span data-stu-id="f0771-115">The following image shows the key parts of the Console:</span></span>

![La consola de Microsoft Edge DevTools](./media/console.png)

1. <span data-ttu-id="f0771-117">**Errores**  /  **Advertencias**  /  **Información**  /  Botones de **registro** : filtrar la salida de consola por el tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="f0771-117">**Errors** / **Warnings** / **Info** / **Logs** buttons: Filter console output by the specified type.</span></span> <span data-ttu-id="f0771-118">Puede seleccionar varios botones manteniendo presionada la tecla **Ctrl** .</span><span class="sxs-lookup"><span data-stu-id="f0771-118">You can multi-select buttons by holding down the **Ctrl** key.</span></span> <span data-ttu-id="f0771-119">El botón **todo** borra todos los filtros.</span><span class="sxs-lookup"><span data-stu-id="f0771-119">The **All** button clears all filters.</span></span>

2. <span data-ttu-id="f0771-120">Botón **Borrar** (**Ctrl + L**): el botón **Borrar** borra la pantalla actual de la consola.</span><span class="sxs-lookup"><span data-stu-id="f0771-120">**Clear** button (**Ctrl+L**): The **Clear** button clears the current console display.</span></span>

3. <span data-ttu-id="f0771-121">Casilla de verificación **conservar registro** : al seleccionar la casilla de verificación **conservar registro** , se conserva la salida de la consola en las actualizaciones de página y se cierra y vuelve a abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="f0771-121">**Preserve Log** check box: Selecting the **Preserve Log** check box persists your console output across page refreshes and closing and reopening DevTools.</span></span> <span data-ttu-id="f0771-122">El historial de consola se borra solo cuando se cierra la pestaña o cuando se borra manualmente la consola.</span><span class="sxs-lookup"><span data-stu-id="f0771-122">The Console history clears only when the tab is closed or you manually clear the Console.</span></span>

4. <span data-ttu-id="f0771-123">**Destino**: Use el menú desplegable de **destino** para cambiar a un contexto de ejecución diferente, como un `<iframe>` en la página o una extensión en curso.</span><span class="sxs-lookup"><span data-stu-id="f0771-123">**Target**: Use the **Target** drop-down menu to switch to a different execution context, such as an `<iframe>` in your page or a running extension.</span></span> <span data-ttu-id="f0771-124">De forma predeterminada, se selecciona el marco de nivel superior de la página.</span><span class="sxs-lookup"><span data-stu-id="f0771-124">By default, the top-level frame of your page is selected.</span></span> <span data-ttu-id="f0771-125">Al mantener el puntero sobre un marco seleccionado, se muestra la información sobre herramientas que muestra la dirección URL completa de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="f0771-125">Hovering over a selected frame displays a tooltip that shows the full URL for that resource.</span></span>

5. <span data-ttu-id="f0771-126">**Mostrar consola**  /  **Ocultar** botón de consola (**Ctrl** +  **&grave;** ): además del panel de consola, puede usar la consola desde la parte inferior de cualquier otro panel de DevTools pulsando el   /  botón**ocultar** consola de la consola.</span><span class="sxs-lookup"><span data-stu-id="f0771-126">**Show Console** / **Hide Console** button (**Ctrl**+ **&grave;** ): In addition to the Console panel, you can use the console from the bottom of any other DevTools panel by pressing the **Show Console** / **Hide Console** button.</span></span> <span data-ttu-id="f0771-127">El botón no surte efecto cuando DevTools está abierto en el panel de consola.</span><span class="sxs-lookup"><span data-stu-id="f0771-127">The button has no effect when DevTools is open to the Console panel.</span></span>
 
6. <span data-ttu-id="f0771-128">**Filtrar registros** (**Ctrl + b**): también puede filtrar los registros mediante una cadena de texto específica en el cuadro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f0771-128">**Filter logs** (**Ctrl+F**) : You can also filter logs by using a specific text string in the search box.</span></span>

7. <span data-ttu-id="f0771-129">**Depurador**: Seleccione cualquier vínculo de origen azul para abrir el depurador de DevTools a esa línea de código en particular para su posterior inspección.</span><span class="sxs-lookup"><span data-stu-id="f0771-129">**Debugger**: Select any blue source link to open the DevTools Debugger to that particular line of code for further inspection.</span></span>

## <span data-ttu-id="f0771-130">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="f0771-130">Shortcuts</span></span>

<span data-ttu-id="f0771-131">Acción</span><span class="sxs-lookup"><span data-stu-id="f0771-131">Action</span></span>                                            | <span data-ttu-id="f0771-132">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="f0771-132">Shortcut</span></span>               
:-------------------------------------------------| :----------------------
<span data-ttu-id="f0771-133">Iniciar DevTools con la consola en el foco</span><span class="sxs-lookup"><span data-stu-id="f0771-133">Launch DevTools with Console in focus</span></span>             | <span data-ttu-id="f0771-134">**Ctrl**  +  **MAYÚS**  +  **J**</span><span class="sxs-lookup"><span data-stu-id="f0771-134">**Ctrl** + **Shift** + **J**</span></span> 
<span data-ttu-id="f0771-135">Cambiar a la consola</span><span class="sxs-lookup"><span data-stu-id="f0771-135">Switch to the Console</span></span>                                 | <span data-ttu-id="f0771-136">**Ctrl**  +  **2**</span><span class="sxs-lookup"><span data-stu-id="f0771-136">**Ctrl** + **2**</span></span>           
<span data-ttu-id="f0771-137">Mostrar u ocultar la consola de otra ficha de DevTools</span><span class="sxs-lookup"><span data-stu-id="f0771-137">Show/hide the Console from another DevTools tab</span></span>       | <span data-ttu-id="f0771-138">  +  Ctrl **&grave;** (marca atrás)</span><span class="sxs-lookup"><span data-stu-id="f0771-138">**Ctrl** + **&grave;** (back tick)</span></span>  
<span data-ttu-id="f0771-139">Ejecutar (comando de una sola línea)</span><span class="sxs-lookup"><span data-stu-id="f0771-139">Execute (single-line command)</span></span>                     | **<span data-ttu-id="f0771-140">Entrar</span><span class="sxs-lookup"><span data-stu-id="f0771-140">Enter</span></span>**                
<span data-ttu-id="f0771-141">Salto de línea sin ejecutar (comando de varias líneas)</span><span class="sxs-lookup"><span data-stu-id="f0771-141">Line break without executing (multi-line command)</span></span> | <span data-ttu-id="f0771-142">**MAYÚS**  +  **Entrar** o **Ctrl +**  +  **entrar**</span><span class="sxs-lookup"><span data-stu-id="f0771-142">**Shift** + **Enter** or **Ctrl** + **Enter**</span></span>      
<span data-ttu-id="f0771-143">Borrar la consola de todos los mensajes</span><span class="sxs-lookup"><span data-stu-id="f0771-143">Clear the Console of all messages</span></span>                 | <span data-ttu-id="f0771-144">**Ctrl**  +  **L**</span><span class="sxs-lookup"><span data-stu-id="f0771-144">**Ctrl** + **L**</span></span>           
<span data-ttu-id="f0771-145">Filtrar registros (establecer el foco en el cuadro de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="f0771-145">Filter logs (set focus to search box)</span></span>             | <span data-ttu-id="f0771-146">**Ctrl**  +  **F**</span><span class="sxs-lookup"><span data-stu-id="f0771-146">**Ctrl** + **F**</span></span>           
<span data-ttu-id="f0771-147">Aceptar la sugerencia de finalización automática (cuando está en el foco)</span><span class="sxs-lookup"><span data-stu-id="f0771-147">Accept auto-completion suggestion (when in focus)</span></span> | <span data-ttu-id="f0771-148">**Entrar** o **Tab**</span><span class="sxs-lookup"><span data-stu-id="f0771-148">**Enter** or **Tab**</span></span>       
<span data-ttu-id="f0771-149">Sugerencia de finalización automática anterior o siguiente</span><span class="sxs-lookup"><span data-stu-id="f0771-149">Previous/next auto-completion suggestion</span></span>          | <span data-ttu-id="f0771-150">Tecla de flecha **arriba** / **Tecla de dirección abajo**</span><span class="sxs-lookup"><span data-stu-id="f0771-150">**Up arrow key**/**Down arrow key**</span></span>   
