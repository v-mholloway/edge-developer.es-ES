---
description: Microsoft Edge (Chromium) y Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, vs, visual studio, depurador
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387274"
---
# <a name="visual-studio"></a><span data-ttu-id="8eafa-104">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eafa-104">Visual Studio</span></span>  

<span data-ttu-id="8eafa-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] es un entorno de desarrollo integrado \(IDE\).</span><span class="sxs-lookup"><span data-stu-id="8eafa-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] is an integrated development environment \(IDE\).</span></span>   <span data-ttu-id="8eafa-106">Úselo para editar, depurar, compilar y publicar sus aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="8eafa-106">Use it to edit, debug, build, and publish your web apps.</span></span>  <span data-ttu-id="8eafa-107">Es un programa completo de características que puede usarse para muchos aspectos del desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="8eafa-107">It is a feature-rich program that may be used for many aspects of your web development.</span></span>  <span data-ttu-id="8eafa-108">Más allá del editor y depurador estándar que proporcionan la mayoría de los identificadores, Visual Studio incluye las siguientes características para facilitar el proceso de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="8eafa-108">Over and above the standard editor and debugger that most IDEs provide, Visual Studio includes the following features to ease your development process.</span></span>  

*   <span data-ttu-id="8eafa-109">compiladores</span><span class="sxs-lookup"><span data-stu-id="8eafa-109">compilers</span></span>  
*   <span data-ttu-id="8eafa-110">herramientas de finalización de código</span><span class="sxs-lookup"><span data-stu-id="8eafa-110">code completion tools</span></span>  
*   <span data-ttu-id="8eafa-111">diseñadores gráficos</span><span class="sxs-lookup"><span data-stu-id="8eafa-111">graphical designers</span></span>  
*   <span data-ttu-id="8eafa-112">muchos más</span><span class="sxs-lookup"><span data-stu-id="8eafa-112">many more</span></span>  
    
<span data-ttu-id="8eafa-113">Si aún no está usando Visual Studio, vaya [a Descargar Visual Studio][MicrosoftVisualstudioDownloads] para descargarlo.</span><span class="sxs-lookup"><span data-stu-id="8eafa-113">If you are not already using Visual Studio, navigate to [Download Visual Studio][MicrosoftVisualstudioDownloads] to download it.</span></span>  

<span data-ttu-id="8eafa-114">Actualmente, Visual Studio 2019 admite la depuración de JavaScript en Microsoft Edge para su ASP.NET Framework y ASP.NET Core aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8eafa-114">Currently, Visual Studio 2019 supports debugging JavaScript in Microsoft Edge for your ASP.NET Framework and ASP.NET Core apps.</span></span>  <span data-ttu-id="8eafa-115">Complete los siguientes pasos para usar Visual Studio para depurar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8eafa-115">Complete the following steps to use Visual Studio to debug Microsoft Edge.</span></span>  

## <a name="launch-microsoft-edge"></a><span data-ttu-id="8eafa-116">Iniciar Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8eafa-116">Launch Microsoft Edge</span></span>  

<span data-ttu-id="8eafa-117">Visual Studio completa el siguiente flujo de trabajo con un solo botón.</span><span class="sxs-lookup"><span data-stu-id="8eafa-117">Visual Studio completes the following workflow using a single button.</span></span>  

1.  <span data-ttu-id="8eafa-118">Crea la aplicación ASP.NET y ASP.NET Core aplicación.</span><span class="sxs-lookup"><span data-stu-id="8eafa-118">Builds your ASP.NET and ASP.NET Core app.</span></span>  
1.  <span data-ttu-id="8eafa-119">Inicia el servidor web.</span><span class="sxs-lookup"><span data-stu-id="8eafa-119">Starts your web server.</span></span>  
1.  <span data-ttu-id="8eafa-120">Inicia Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8eafa-120">Launches Microsoft Edge.</span></span>  
1.  <span data-ttu-id="8eafa-121">Conecta el depurador Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8eafa-121">Connects the Visual Studio debugger.</span></span>  
    
<span data-ttu-id="8eafa-122">El flujo de trabajo simplificado permite depurar JavaScript que se ejecutan en Microsoft Edge directamente desde el IDE.</span><span class="sxs-lookup"><span data-stu-id="8eafa-122">The simplified workflow allows you to debug JavaScript that run in Microsoft Edge directly from your IDE.</span></span>  

### <a name="create-a-new-aspnet-core-web-app"></a><span data-ttu-id="8eafa-123">Crear una nueva aplicación ASP.NET Core web</span><span class="sxs-lookup"><span data-stu-id="8eafa-123">Create a new ASP.NET Core web app</span></span>  

<span data-ttu-id="8eafa-124">Abra Visual Studio 2019 y elija **Crear un nuevo proyecto**.</span><span class="sxs-lookup"><span data-stu-id="8eafa-124">Open Visual Studio 2019 and choose **Create a new project**.</span></span>  <span data-ttu-id="8eafa-125">En la siguiente pantalla, elija **ASP.NET Core aplicación web**  >  **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="8eafa-125">On the next screen, choose **ASP.NET Core Web app** > **Next**.</span></span>  

:::image type="complex" source="./media/create-new-project.png" alt-text="Crear una nueva ASP.NET Core web" lightbox="./media/create-new-project.png":::
   <span data-ttu-id="8eafa-127">Crear una nueva ASP.NET Core web</span><span class="sxs-lookup"><span data-stu-id="8eafa-127">Create a new ASP.NET Core Web app</span></span>  
:::image-end:::  

<span data-ttu-id="8eafa-128">Proporcione un **Project nombre para** el nuevo proyecto y elija **Crear**.</span><span class="sxs-lookup"><span data-stu-id="8eafa-128">Provide a **Project name** for your new project and choose **Create**.</span></span>  <span data-ttu-id="8eafa-129">Para los fines del ejemplo, elijaReact.js\*\* como \*\* plantilla y elija **Crear**.</span><span class="sxs-lookup"><span data-stu-id="8eafa-129">For the purposes of the example, choose **React.js** as the template, and choose **Create**.</span></span>  <span data-ttu-id="8eafa-130">La **React.js** especifica cómo integrar React.js con una ASP.NET Core aplicación.</span><span class="sxs-lookup"><span data-stu-id="8eafa-130">The **React.js** template specifies how to integrate React.js with an ASP.NET Core app.</span></span>  

### <a name="launch-microsoft-edge-from-visual-studio"></a><span data-ttu-id="8eafa-131">Inicie Microsoft Edge desde Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eafa-131">Launch Microsoft Edge from Visual Studio</span></span>  

<span data-ttu-id="8eafa-132">Después de crear el proyecto, abra `ClientApp/src/components/Counter.js` .</span><span class="sxs-lookup"><span data-stu-id="8eafa-132">After you create your project, open `ClientApp/src/components/Counter.js`.</span></span>  <span data-ttu-id="8eafa-133">Ahora, para usar Visual Studio para depurar JavaScript, elija el desplegable junto al botón **verde Reproducir** y **IIS Express**.</span><span class="sxs-lookup"><span data-stu-id="8eafa-133">Now, to use Visual Studio to debug JavaScript, choose the dropdown next to the green **Play** button and **IIS Express**.</span></span>  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="La lista desplegable junto al botón verde Reproducir y IIS Express" lightbox="./media/vs-dropdown.png":::
   <span data-ttu-id="8eafa-135">La lista desplegable junto al botón **verde Reproducir** y **IIS Express**</span><span class="sxs-lookup"><span data-stu-id="8eafa-135">The dropdown next to the green **Play** button and **IIS Express**</span></span>  
:::image-end:::  

<span data-ttu-id="8eafa-136">Elija **Depuración de scripts**  >  **habilitada**.</span><span class="sxs-lookup"><span data-stu-id="8eafa-136">Choose **Script Debugging** > **Enabled**.</span></span>  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Activar la depuración de scripts en Visual Studio" lightbox="./media/enable-script-debugging.png":::
   <span data-ttu-id="8eafa-138">Activar la depuración de scripts en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eafa-138">Turn on script debugging in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="8eafa-139">En el mismo desplegable, elija **Explorador web** > el canal de vista previa de Microsoft Edge que desea que Visual Studio inicie, como Microsoft Edge Canary, Dev o Beta.</span><span class="sxs-lookup"><span data-stu-id="8eafa-139">In the same dropdown, choose **Web Browser** > the preview channel of Microsoft Edge that you want Visual Studio to launch, such as Microsoft Edge Canary, Dev, or Beta.</span></span>  <span data-ttu-id="8eafa-140">Si aún no usa uno de los canales de vista Microsoft Edge, vaya a Descargar [Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] para descargar uno.</span><span class="sxs-lookup"><span data-stu-id="8eafa-140">If you are not already using one of the Microsoft Edge preview channels, navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] to download one.</span></span>  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Elija el canal de vista previa Microsoft Edge que desea que Visual Studio inicie" lightbox="./media/set-web-browser.png":::
   <span data-ttu-id="8eafa-142">Elija el canal de vista previa Microsoft Edge que desea que Visual Studio inicie</span><span class="sxs-lookup"><span data-stu-id="8eafa-142">Choose the preview channel of Microsoft Edge that you want Visual Studio to launch</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="8eafa-143">Si elige Microsoft Edge \(EdgeHTML\), Visual Studio la inicia en lugar de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="8eafa-143">If you choose Microsoft Edge \(EdgeHTML\), Visual Studio launches it instead of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="8eafa-144">[Instale uno][MicrosoftedgeinsiderDownload] de los canales de vista previa de Microsoft Edge o asegúrese de que la versión de Microsoft Edge instalada en el equipo sea Microsoft Edge \(Chromium\) y no Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="8eafa-144">[Install the one of the preview channels of Microsoft Edge][MicrosoftedgeinsiderDownload] or ensure that the version of Microsoft Edge installed on your machine is Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  

<span data-ttu-id="8eafa-145">Ahora que Visual Studio está configurado correctamente, elija el botón **verde Reproducir.**</span><span class="sxs-lookup"><span data-stu-id="8eafa-145">Now that Visual Studio is correctly configured, choose the green **Play** button.</span></span>  <span data-ttu-id="8eafa-146">Visual Studio compila la aplicación, inicia el servidor web, inicia Microsoft Edge y navega al puerto especificado en `https://localhost:44362/` `launchSettings.json` .</span><span class="sxs-lookup"><span data-stu-id="8eafa-146">Visual Studio builds your app, start the web server, launch Microsoft Edge, and navigate to `https://localhost:44362/` or whatever port is specified in `launchSettings.json`.</span></span>  

:::image type="complex" source="./media/edge-launch.png" alt-text="Microsoft Edge inicia desde Visual Studio" lightbox="./media/edge-launch.png":::
   <span data-ttu-id="8eafa-148">Microsoft Edge inicia desde Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eafa-148">Microsoft Edge launches from Visual Studio</span></span>  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a><span data-ttu-id="8eafa-149">Depurar JavaScript que se ejecuta en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8eafa-149">Debug JavaScript running in Microsoft Edge</span></span>  

<span data-ttu-id="8eafa-150">Vuelva a Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8eafa-150">Switch back to Visual Studio.</span></span>  <span data-ttu-id="8eafa-151">In `Counter.js` , to set a breakpoint on Line 13, choose the gutter next to the line.</span><span class="sxs-lookup"><span data-stu-id="8eafa-151">In `Counter.js`, to set a breakpoint on Line 13, choose the gutter next to the line.</span></span>  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Elija el canal situado junto a la línea 13 en Counter.js para establecer un punto de interrupción en Visual Studio" lightbox="./media/set-breakpoint.png":::
   <span data-ttu-id="8eafa-153">Elija el canal situado junto a la línea 13 para establecer un punto de `Counter.js` interrupción en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eafa-153">Choose the gutter next to Line 13 in `Counter.js` to set a breakpoint in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="8eafa-154">Ahora vuelva a la instancia de Microsoft Edge que Visual Studio iniciado.</span><span class="sxs-lookup"><span data-stu-id="8eafa-154">Now switch back to the instance of Microsoft Edge that Visual Studio launched.</span></span>  <span data-ttu-id="8eafa-155">Elija en **Contador** en navmenu a la izquierda de la página web.</span><span class="sxs-lookup"><span data-stu-id="8eafa-155">Choose on **Counter** in the NavMenu on the left of the webpage.</span></span>  <span data-ttu-id="8eafa-156">Ahora elija **Increment**.</span><span class="sxs-lookup"><span data-stu-id="8eafa-156">Now choose **Increment**.</span></span>  

:::image type="complex" source="./media/edge-counter.png" alt-text="La página Contador de nuestra aplicación ASP.NET Core web" lightbox="./media/edge-counter.png":::
   <span data-ttu-id="8eafa-158">La página Contador de nuestra aplicación ASP.NET Core web</span><span class="sxs-lookup"><span data-stu-id="8eafa-158">The Counter page in our ASP.NET Core web app</span></span>  
:::image-end:::  

<span data-ttu-id="8eafa-159">El depurador de JavaScript de Visual Studio alcanza el punto de interrupción establecido en `Counter.js` .</span><span class="sxs-lookup"><span data-stu-id="8eafa-159">The JavaScript debugger in Visual Studio hits the breakpoint you set in `Counter.js`.</span></span>  <span data-ttu-id="8eafa-160">Visual Studio pausa el tiempo de ejecución del JavaScript que se ejecuta en Microsoft Edge y puede pasar por el script línea por línea.</span><span class="sxs-lookup"><span data-stu-id="8eafa-160">Visual Studio now pauses the runtime of the JavaScript running in Microsoft Edge and you may step through the script line-by-line.</span></span>  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio pausa la ejecución de JavaScript en Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
   <span data-ttu-id="8eafa-162">Visual Studio pausa la ejecución de JavaScript en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8eafa-162">Visual Studio pauses JavaScript running in Microsoft Edge</span></span>  
:::image-end:::  

<span data-ttu-id="8eafa-163">El ejemplo era solo una pequeña demostración de la funcionalidad disponible en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8eafa-163">The example was just a minor demonstration of the functionality available in Visual Studio.</span></span>  <span data-ttu-id="8eafa-164">Para obtener más información acerca de la funcionalidad de Visual Studio 2019, vaya [a Visual Studio documentación][VisualStudioWindowsIndex].</span><span class="sxs-lookup"><span data-stu-id="8eafa-164">For more information about the functionality in Visual Studio 2019, navigate to [Visual Studio documentation][VisualStudioWindowsIndex].</span></span>  

## <a name="attach-to-microsoft-edge"></a><span data-ttu-id="8eafa-165">Adjuntar a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8eafa-165">Attach to Microsoft Edge</span></span>  

<span data-ttu-id="8eafa-166">Anteriormente, tenías que iniciar Microsoft Edge desde Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8eafa-166">Previously, you had to launch Microsoft Edge from Visual Studio.</span></span>  <span data-ttu-id="8eafa-167">Ahora, puede adjuntar el depurador de Visual Studio a una instancia de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8eafa-167">Now, you are able to attach the Visual Studio debugger to an already running instance of Microsoft Edge.</span></span>  

<span data-ttu-id="8eafa-168">En primer lugar, asegúrese de que no hay instancias en ejecución de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8eafa-168">First, ensure that there are no running instances of Microsoft Edge.</span></span>  <span data-ttu-id="8eafa-169">Ahora, desde la línea de comandos, ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="8eafa-169">Now, from your command line, run the following command.</span></span>  

```console
start msedge –remote-debugging-port=9222
```  

<span data-ttu-id="8eafa-170">Desde Visual Studio, abra el menú **Depurar** y elija **Adjuntar al proceso** o seleccione `Ctrl` + `Alt` + `P` .</span><span class="sxs-lookup"><span data-stu-id="8eafa-170">From Visual Studio, open the **Debug** menu and choose **Attach to Process** or select `Ctrl`+`Alt`+`P`.</span></span>  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Elija Adjuntar al proceso en Visual Studio" lightbox="./media/attach-to-process.png":::
   <span data-ttu-id="8eafa-172">Elija **Adjuntar al proceso** en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eafa-172">Choose **Attach to Process** in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="8eafa-173">En el **cuadro de diálogo** Adjuntar a proceso, establezca Tipo de **conexión** en **Websocket del protocolo de devtools de Chrome (sin autenticación).**</span><span class="sxs-lookup"><span data-stu-id="8eafa-173">From the **Attach to Process** dialog, set **Connection type** to **Chrome devtools protocol websocket (no authentication)**.</span></span>  <span data-ttu-id="8eafa-174">En el **cuadro de texto Conexión de** destino, escriba y seleccione `http://localhost:9222/` `Enter` .</span><span class="sxs-lookup"><span data-stu-id="8eafa-174">In the **Connecting target** textbox, type `http://localhost:9222/` and select `Enter`.</span></span>  <span data-ttu-id="8eafa-175">Revise la lista de pestañas abiertas que tiene en Microsoft Edge en el cuadro de diálogo Adjuntar **al** proceso.</span><span class="sxs-lookup"><span data-stu-id="8eafa-175">Review the list of open tabs you have in Microsoft Edge listed out in the **Attach to Process** dialog.</span></span>  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Configurar el cuadro de diálogo Adjuntar al proceso en Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   <span data-ttu-id="8eafa-177">Configurar el **cuadro de diálogo Adjuntar** al proceso en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eafa-177">Configure the **Attach to Process** dialog in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="8eafa-178">Elija **Seleccionar...** > la casilla situada junto a **JavaScript (Microsoft Edge – Chromium).**</span><span class="sxs-lookup"><span data-stu-id="8eafa-178">Choose **Select...** > the checkbox next to **JavaScript (Microsoft Edge – Chromium)**.</span></span>  <span data-ttu-id="8eafa-179">Para agregar pestañas, vaya a nuevas pestañas, cierre pestañas \*\*\*\* y muestre los cambios reflejados en el cuadro de diálogo Adjuntar al proceso, elija el **botón** Actualizar.</span><span class="sxs-lookup"><span data-stu-id="8eafa-179">To add tabs, navigate to new tabs, and close tabs and display the changes reflected in the **Attach to Process** dialog, choose the **Refresh** button.</span></span>  <span data-ttu-id="8eafa-180">Elija la pestaña que desea depurar y elija **Adjuntar**.</span><span class="sxs-lookup"><span data-stu-id="8eafa-180">Choose the tab you want to debug and choose **Attach**.</span></span>  

<span data-ttu-id="8eafa-181">El Visual Studio está conectado a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8eafa-181">The Visual Studio debugger is now attached to Microsoft Edge.</span></span>  <span data-ttu-id="8eafa-182">Puede pausar la ejecución de JavaScript, establecer puntos de interrupción y revisar instrucciones directamente en la ventana `console.log()` Depurar salida en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8eafa-182">You may pause the running of JavaScript, set breakpoints, and review `console.log()` statements directly in the Debug Output window in Visual Studio.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a><span data-ttu-id="8eafa-183">Getting in touch with the Microsoft Visual Studio team</span><span class="sxs-lookup"><span data-stu-id="8eafa-183">Getting in touch with the Microsoft Visual Studio team</span></span>  

<span data-ttu-id="8eafa-184">Los Microsoft Visual Studio y Microsoft Edge quieren obtener más información sobre cómo trabajar con JavaScript en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8eafa-184">The Microsoft Visual Studio and Microsoft Edge teams wants to learn more about how you work with JavaScript in Visual Studio.</span></span>  <span data-ttu-id="8eafa-185">Para enviar sus comentarios, elija el icono **Enviar** comentarios en Visual Studio o @VisualStudio [y @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span><span class="sxs-lookup"><span data-stu-id="8eafa-185">To send your feedback, choose the **Send Feedback** icon in Visual Studio or tweet [@VisualStudio and @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span></span>  

:::image type="complex" source="./media/feedback-icon.png" alt-text="El icono Enviar comentarios en Visual Studio" lightbox="./media/feedback-icon.png":::
   <span data-ttu-id="8eafa-187">El **icono Enviar comentarios** en Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8eafa-187">The **Send Feedback** icon in Visual Studio</span></span>  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio documentación | Microsoft Docs"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Descargar Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet to @VisualStudio and @EdgeDevTools | Twitter"  
