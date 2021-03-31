---
description: Modelo de proceso
title: Modelo de proceso
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895593"
---
# <span data-ttu-id="41ee7-104">Modelo de proceso</span><span class="sxs-lookup"><span data-stu-id="41ee7-104">Process model</span></span>  

<span data-ttu-id="41ee7-105">WebView2 usa el mismo modelo de proceso que el explorador Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="41ee7-105">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="41ee7-106">Para obtener más información sobre el modelo de proceso del explorador, vea [arquitectura del explorador en el explorador web moderno][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span><span class="sxs-lookup"><span data-stu-id="41ee7-106">For more information about the browser process model, see [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span> 

<span data-ttu-id="41ee7-107">Un proceso del explorador está asociado con los procesos de representación y otros procesos de utilidades, tal y como se describe en este artículo.</span><span class="sxs-lookup"><span data-stu-id="41ee7-107">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="41ee7-108">Además, en el caso de WebView2, hay aplicaciones de hospedaje que solicitan procesos mediante WebView2.</span><span class="sxs-lookup"><span data-stu-id="41ee7-108">Additionally, in the case of WebView2, there are host app requesting processes using WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Proceso 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="41ee7-110">Proceso 1</span><span class="sxs-lookup"><span data-stu-id="41ee7-110">Process 1</span></span>  
:::image-end:::  

<span data-ttu-id="41ee7-111">Se especifica un proceso de explorador por carpeta de datos de usuario en una sesión de usuario que ofrece servicio a cualquier proceso de solicitud de WebView2 que especifique la carpeta de datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="41ee7-111">One browser process is specified per user data folder in a user session that serve any WebView2 requesting process that specifies that user data folder.</span></span>  <span data-ttu-id="41ee7-112">Esto significa que un proceso del explorador puede estar atendiendo a varios procesos de solicitud y un proceso de solicitud puede estar usando varios procesos de explorador.</span><span class="sxs-lookup"><span data-stu-id="41ee7-112">This means one browser process may be serving multiple requesting processes and one requesting process may be using multiple browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Proceso 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="41ee7-114">Proceso 2</span><span class="sxs-lookup"><span data-stu-id="41ee7-114">Process 2</span></span>  
:::image-end:::  

<span data-ttu-id="41ee7-115">Un proceso de explorador tiene varios procesos de representación asociados.</span><span class="sxs-lookup"><span data-stu-id="41ee7-115">A browser process has some number of associated renderer processes.</span></span>  <span data-ttu-id="41ee7-116">Los procesos del explorador se crean según sea necesario para dar servicio a varios fotogramas en diferentes instancias de WebView2.</span><span class="sxs-lookup"><span data-stu-id="41ee7-116">The browser processes are created as required to service potentially multiple frames in different instances of WebView2.</span></span>  <span data-ttu-id="41ee7-117">La cantidad de procesos de representación varía según la característica de explorador de aislamiento del sitio y el número de orígenes distintos desconectados representados en instancias asociadas de WebView2.</span><span class="sxs-lookup"><span data-stu-id="41ee7-117">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  <span data-ttu-id="41ee7-118">La característica explorador de aislamiento del sitio se describe en el contenido anterior.</span><span class="sxs-lookup"><span data-stu-id="41ee7-118">The site isolation browser feature is described in the previous content.</span></span>  

<span data-ttu-id="41ee7-119">`CoreWebView2Environment`Representa una carpeta de datos de usuario y el proceso del explorador.</span><span class="sxs-lookup"><span data-stu-id="41ee7-119">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="41ee7-120">El `CoreWebView2` no se corresponde directamente con ningún conjunto de procesos, ya que un WebView2 usa varios procesos de representación, en función del aislamiento del sitio, como se ha descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="41ee7-120">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on site isolation as previously described.</span></span>  

<span data-ttu-id="41ee7-121">Puede reaccionar ante los bloqueos y bloqueos en estos procesos del explorador y el representador con el `ProcessFailed` evento de `CoreWebView2` .</span><span class="sxs-lookup"><span data-stu-id="41ee7-121">You are able to react to crashes and hangs in these browser and renderer processes using the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="41ee7-122">Puede apagar de forma segura los procesos del explorador y el representador asociados con el `Close` método de `CoreWebView2Controller` .</span><span class="sxs-lookup"><span data-stu-id="41ee7-122">You are able to safely shutdown associated browser and renderer processes using the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="41ee7-123">Para abrir la ventana del administrador de tareas del explorador desde la ventana **DevTools** de una instancia de WebView2, puede seleccionar `Shift` + `Escape` o mantener el mouse en la barra de título de la ventana de DevTools, abrir el menú contextual \(haga clic con el botón secundario del mouse \) y elija `Browser task manager` .</span><span class="sxs-lookup"><span data-stu-id="41ee7-123">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, you are able to select `Shift`+`Escape` or hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  <span data-ttu-id="41ee7-124">Se muestran todos los procesos asociados con el proceso del explorador de su WebView2, incluidos los propósitos relacionados.</span><span class="sxs-lookup"><span data-stu-id="41ee7-124">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Arquitectura del navegador-en el explorador web moderno (parte 1)"  
