---
description: Navegación
title: Navegación
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, edge html
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314800"
---
# <span data-ttu-id="20b68-104">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="20b68-104">Navigation events</span></span>  

<span data-ttu-id="20b68-105">La secuencia normal de eventos de navegación `NavigationStarting` es `SourceChanged` , , `ContentLoading` `HistoryChanged` y, a `NavigationCompleted` continuación, .</span><span class="sxs-lookup"><span data-stu-id="20b68-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="20b68-106">Los siguientes eventos describen el estado de WebView2 durante cada navegación.</span><span class="sxs-lookup"><span data-stu-id="20b68-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="20b68-107">Secuencia</span><span class="sxs-lookup"><span data-stu-id="20b68-107">Sequence</span></span> | <span data-ttu-id="20b68-108">Nombre del evento</span><span class="sxs-lookup"><span data-stu-id="20b68-108">Event name</span></span> | <span data-ttu-id="20b68-109">Detalles</span><span class="sxs-lookup"><span data-stu-id="20b68-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="20b68-110">1</span><span class="sxs-lookup"><span data-stu-id="20b68-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="20b68-111">WebView2 comienza a navegar y la navegación da como resultado una solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="20b68-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="20b68-112">El host puede no permitir la solicitud durante el evento.</span><span class="sxs-lookup"><span data-stu-id="20b68-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="20b68-113">2</span><span class="sxs-lookup"><span data-stu-id="20b68-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="20b68-114">El origen de WebView2 cambia a una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="20b68-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="20b68-115">El evento puede ser el resultado de una navegación que no provoca una solicitud de red, como una navegación por fragmentos.</span><span class="sxs-lookup"><span data-stu-id="20b68-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="20b68-116">3</span><span class="sxs-lookup"><span data-stu-id="20b68-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="20b68-117">El historial de actualizaciones de WebView2 como resultado de la navegación.</span><span class="sxs-lookup"><span data-stu-id="20b68-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="20b68-118">4</span><span class="sxs-lookup"><span data-stu-id="20b68-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="20b68-119">WebView2 comienza a cargar contenido para la nueva página.</span><span class="sxs-lookup"><span data-stu-id="20b68-119">WebView2 starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="20b68-120">5</span><span class="sxs-lookup"><span data-stu-id="20b68-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="20b68-121">WebView2 completa la carga de contenido en la nueva página.</span><span class="sxs-lookup"><span data-stu-id="20b68-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="20b68-122">Realiza `navigations` un seguimiento de cada nuevo documento con el identificador de navegación \( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="20b68-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="20b68-123">El `NavigationId` elemento WebView cambia cada vez que hay una navegación correcta a un nuevo documento.</span><span class="sxs-lookup"><span data-stu-id="20b68-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="Eventos de navegación de Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="20b68-125">Eventos de navegación de Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="20b68-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="20b68-126">La figura anterior representa los eventos de navegación con la misma `NavigationId` propiedad en el argumento de evento respectivo.</span><span class="sxs-lookup"><span data-stu-id="20b68-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="20b68-127">los eventos con diferentes instancias de `NavigationId` evento pueden superponerse.</span><span class="sxs-lookup"><span data-stu-id="20b68-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="20b68-128">Por ejemplo, al iniciar una navegación, debe esperar al evento `NavigationStarting` relacionado.</span><span class="sxs-lookup"><span data-stu-id="20b68-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="20b68-129">Si, a continuación, inicia otra navegación, debería ver el evento de la primera navegación seguido del evento para la segunda navegación, seguido del evento para la primera navegación y, a continuación, todos los demás eventos de navegación adecuados para la segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegación.</span><span class="sxs-lookup"><span data-stu-id="20b68-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="20b68-130">En los casos de error puede haber o no un evento dependiendo de si la `ContentLoading` navegación continúa a una página de error.</span><span class="sxs-lookup"><span data-stu-id="20b68-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="20b68-131">En el caso de un redireccionamiento HTTP, hay varios eventos en una fila, donde los argumentos de eventos posteriores tienen la propiedad establecida, pero el `NavigationStarting` `IsRedirect` resto permanece `NavigationId` igual.</span><span class="sxs-lookup"><span data-stu-id="20b68-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="20b68-132">El mismo documento, como navegar a un fragmento, no produce el `navigations` evento y no incrementa el archivo `NavigationStarting` `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="20b68-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="20b68-133">Para supervisar o cancelar dentro de subframes en webView, usa los eventos que actúan igual que los eventos equivalentes que no son `navigations` `FrameNavigationStarting` `FrameNavigationCompleted` equivalentes a fotogramas.</span><span class="sxs-lookup"><span data-stu-id="20b68-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  
