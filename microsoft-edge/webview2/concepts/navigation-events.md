---
description: Navegación
title: Navegación | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: d133bfb99808d0e036c4b46be9ef82039aee49eb
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535709"
---
# <a name="navigation-events"></a><span data-ttu-id="da742-104">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="da742-104">Navigation events</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="da742-105">Plataformas compatibles:</span><span class="sxs-lookup"><span data-stu-id="da742-105">Supported platforms:</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="da742-106">Win32, Windows Forms, WinUi, WPF</span><span class="sxs-lookup"><span data-stu-id="da742-106">Win32, Windows Forms, WinUi, WPF</span></span>
   :::column-end:::
:::row-end:::  

<span data-ttu-id="da742-107">Los eventos de navegación se ejecutan cuando se producen acciones asincrónicas específicas al contenido mostrado en una instancia webView2.</span><span class="sxs-lookup"><span data-stu-id="da742-107">Navigation events run when specific asynchronous actions occur to the content displayed in a WebView2 instance.</span></span>  <span data-ttu-id="da742-108">Por ejemplo, cuando un usuario de WebView2 navega a un nuevo sitio web, el contenido nativo escucha el evento change `NavigationStarting` using.</span><span class="sxs-lookup"><span data-stu-id="da742-108">For example, when a WebView2 user navigates to a new website, the native content listens for the change using `NavigationStarting` event.</span></span>  <span data-ttu-id="da742-109">Cuando se completa la acción de navegación, `NavigationCompleted` se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="da742-109">When the navigation action completes, `NavigationCompleted` runs.</span></span>  <span data-ttu-id="da742-110">Para obtener un buen ejemplo de eventos de navegación, vaya a [WebView2 Introducción guía][Webview2IndexGetStarted].</span><span class="sxs-lookup"><span data-stu-id="da742-110">For a good example of navigation events, navigate to [WebView2 Get Started guide][Webview2IndexGetStarted].</span></span>  

<!--todo:  Move the relevant information out of the get started guide to better focus the content and leave the most concise elements in the get started guide.  -->   

<span data-ttu-id="da742-111">La secuencia normal de eventos de navegación es `NavigationStarting` `SourceChanged` , , , `ContentLoading` `HistoryChanged` y, a continuación, `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="da742-111">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="da742-112">Los siguientes eventos describen el estado de WebView2 durante cada navegación.</span><span class="sxs-lookup"><span data-stu-id="da742-112">The following events describe the state of WebView2 during each navigation.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Eventos de navegación Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
         <span data-ttu-id="da742-114">Eventos de navegación Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="da742-114">The Microsoft Edge WebView2 Navigation Events</span></span>  
      :::image-end:::  
      
      > [!NOTE]
      > <span data-ttu-id="da742-115">La figura representa eventos de navegación con la misma `NavigationId` propiedad en el argumento de evento respectivo.</span><span class="sxs-lookup"><span data-stu-id="da742-115">The figure represents navigation events with the same `NavigationId` property on the respective event argument.</span></span>  
   :::column-end:::
   :::column span="2":::
      | <span data-ttu-id="da742-116">Secuencia</span><span class="sxs-lookup"><span data-stu-id="da742-116">Sequence</span></span> | <span data-ttu-id="da742-117">Nombre del evento</span><span class="sxs-lookup"><span data-stu-id="da742-117">Event name</span></span> | <span data-ttu-id="da742-118">Detalles</span><span class="sxs-lookup"><span data-stu-id="da742-118">Details</span></span> |  
      |:--- |:--- |:--- |  
      | <span data-ttu-id="da742-119">1</span><span class="sxs-lookup"><span data-stu-id="da742-119">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="da742-120">WebView2 comienza a navegar y la navegación da como resultado una solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="da742-120">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="da742-121">El host puede no permitir la solicitud durante el evento.</span><span class="sxs-lookup"><span data-stu-id="da742-121">The host may disallow the request during the event.</span></span>  |  
      | <span data-ttu-id="da742-122">2</span><span class="sxs-lookup"><span data-stu-id="da742-122">2</span></span> | `SourceChanged`  |  <span data-ttu-id="da742-123">El origen de WebView2 cambia a una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="da742-123">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="da742-124">El evento puede ser el resultado de una acción de navegación que no provoca una solicitud de red, como una navegación por fragmentos.</span><span class="sxs-lookup"><span data-stu-id="da742-124">The event may result from a navigation action that does not cause a network request such as a fragment navigation.</span></span>  |  
      | <span data-ttu-id="da742-125">3</span><span class="sxs-lookup"><span data-stu-id="da742-125">3</span></span> | `ContentLoading`  |  <span data-ttu-id="da742-126">WebView inicia la carga de contenido de la nueva página.</span><span class="sxs-lookup"><span data-stu-id="da742-126">WebView starts loading content for the new page.</span></span>  |  
      | <span data-ttu-id="da742-127">4</span><span class="sxs-lookup"><span data-stu-id="da742-127">4</span></span> | `HistoryChanged`  |  <span data-ttu-id="da742-128">La navegación hace que se actualice el historial de WebView2.</span><span class="sxs-lookup"><span data-stu-id="da742-128">The navigation causes the history of WebView2 to update.</span></span>  |  
      | <span data-ttu-id="da742-129">5</span><span class="sxs-lookup"><span data-stu-id="da742-129">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="da742-130">WebView2 completa la carga de contenido en la nueva página.</span><span class="sxs-lookup"><span data-stu-id="da742-130">WebView2 completes loading content on the new page.</span></span>  |  
   :::column-end:::
:::row-end:::

<span data-ttu-id="da742-131">Realice un seguimiento de los eventos de navegación a cada nuevo documento mediante el identificador de navegación \( `NavigationId` event\).</span><span class="sxs-lookup"><span data-stu-id="da742-131">Track navigation events to each new document using the navigation ID \(`NavigationId` event\).</span></span>  <span data-ttu-id="da742-132">El evento WebView cambia cada vez que se completa una navegación `NavigationId` correcta a un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="da742-132">The `NavigationId` event of WebView changes every time a successful navigation to a new document completes.</span></span>  

 <span data-ttu-id="da742-133">Los eventos de navegación con diferentes instancias de `NavigationId` evento pueden superponerse.</span><span class="sxs-lookup"><span data-stu-id="da742-133">Navigation events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="da742-134">Por ejemplo, al iniciar un evento de navegación, debe esperar al evento `NavigationStarting` relacionado.</span><span class="sxs-lookup"><span data-stu-id="da742-134">For instance, when you start a navigation event, you must wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="da742-135">Si, a continuación, inicia otra navegación, debería ver el evento de la primera navegación seguido del evento de la segunda navegación, seguido del evento para la primera navegación y, a continuación, todos los demás eventos de navegación adecuados para la segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegación.</span><span class="sxs-lookup"><span data-stu-id="da742-135">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="da742-136">En casos de error, puede haber o no un evento en función de si la `ContentLoading` navegación continúa en una página de error.</span><span class="sxs-lookup"><span data-stu-id="da742-136">In error cases, there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="da742-137">Si se produce un redireccionamiento HTTP, hay varios eventos en una fila, donde los argumentos de evento posteriores tienen la propiedad establecida, pero el `NavigationStarting` `IsRedirect` evento permanece `NavigationId` igual.</span><span class="sxs-lookup"><span data-stu-id="da742-137">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row, where later event arguments have the `IsRedirect` property set, however the `NavigationId` event remains the same.</span></span>  
 
 <span data-ttu-id="da742-138">Los mismos eventos de navegación de documentos, como navegar a un fragmento, no resultan en el evento y no `NavigationStarting` incrementan el `NavigationId` evento.</span><span class="sxs-lookup"><span data-stu-id="da742-138">Same document navigation events, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId` event.</span></span>  

<span data-ttu-id="da742-139">Para supervisar o cancelar eventos de navegación dentro de subframes en una instancia WebView2, use los eventos y que actúan igual que los eventos equivalentes que no son `FrameNavigationStarting` `FrameNavigationCompleted` de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="da742-139">To monitor or cancel navigation events inside subframes in a WebView2 instance, use the `FrameNavigationStarting` and `FrameNavigationCompleted` events that act just like the equivalent non-frame counterpart events.</span></span>  

## <a name="see-also"></a><span data-ttu-id="da742-140">Consulta también</span><span class="sxs-lookup"><span data-stu-id="da742-140">See also</span></span>  

*   <span data-ttu-id="da742-141">Para empezar a usar WebView2, vaya a Guías de Introducción [WebView2.][Webview2IndexGetStarted]</span><span class="sxs-lookup"><span data-stu-id="da742-141">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2IndexGetStarted] guides.</span></span>  
*   <span data-ttu-id="da742-142">Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] en GitHub.</span><span class="sxs-lookup"><span data-stu-id="da742-142">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>  
*   <span data-ttu-id="da742-143">Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].</span><span class="sxs-lookup"><span data-stu-id="da742-143">For more detailed information about WebView2 APIs, navigate to [API reference][DotnetApiMicrosoftWebWebview2WpfWebview2].</span></span>  
*   <span data-ttu-id="da742-144">Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].</span><span class="sxs-lookup"><span data-stu-id="da742-144">For more information about WebView2, navigate to [WebView2 Resources][Webview2IndexNextSteps].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="da742-145">Getting in touch with the Microsoft Edge WebView team</span><span class="sxs-lookup"><span data-stu-id="da742-145">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introducción: introducción a Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
