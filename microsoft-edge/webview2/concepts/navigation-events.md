---
description: Navegación
title: Navegación
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895598"
---
# <span data-ttu-id="b5ccb-104">Eventos de navegación</span><span class="sxs-lookup"><span data-stu-id="b5ccb-104">Navigation events</span></span>  

<span data-ttu-id="b5ccb-105">La secuencia normal de eventos de navegación es `NavigationStarting` , `SourceChanged` ,, `ContentLoading` `HistoryChanged` y, a continuación, `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="b5ccb-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="b5ccb-106">Los siguientes eventos describen el estado de WebView2 durante cada navegación.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="b5ccb-107">Serie</span><span class="sxs-lookup"><span data-stu-id="b5ccb-107">Sequence</span></span> | <span data-ttu-id="b5ccb-108">Nombre del evento</span><span class="sxs-lookup"><span data-stu-id="b5ccb-108">Event name</span></span> | <span data-ttu-id="b5ccb-109">Detalles</span><span class="sxs-lookup"><span data-stu-id="b5ccb-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b5ccb-110">uno</span><span class="sxs-lookup"><span data-stu-id="b5ccb-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="b5ccb-111">WebView2 comienza a navegar y el resultado de la navegación es una solicitud de red.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="b5ccb-112">El anfitrión puede impedir la solicitud durante el evento.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="b5ccb-113">1</span><span class="sxs-lookup"><span data-stu-id="b5ccb-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="b5ccb-114">El origen de WebView2 cambia a una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="b5ccb-115">El evento puede ser el resultado de una navegación que no produce una solicitud de red, como la navegación de fragmentos.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="b5ccb-116">2</span><span class="sxs-lookup"><span data-stu-id="b5ccb-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="b5ccb-117">El historial de las actualizaciones de WebView2 como resultado de la navegación.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="b5ccb-118">cuatro</span><span class="sxs-lookup"><span data-stu-id="b5ccb-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="b5ccb-119">La vista Web comienza a cargar el contenido de la página nueva.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-119">WebView starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="b5ccb-120">4</span><span class="sxs-lookup"><span data-stu-id="b5ccb-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="b5ccb-121">WebView2 completa la carga de contenido en la página nueva.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="b5ccb-122">Realice un seguimiento `navigations` de cada nuevo documento con el identificador de navegación \ ( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="b5ccb-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="b5ccb-123">El `NavigationId` de WebView cambia cada vez que se produce una navegación correcta a un documento nuevo.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="Los eventos de navegación de Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="b5ccb-125">Los eventos de navegación de Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="b5ccb-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="b5ccb-126">La figura anterior representa los eventos de navegación con la misma `NavigationId` propiedad en el respectivo argumento de evento.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="b5ccb-127">se pueden superponer eventos con diferentes instancias de `NavigationId` evento.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="b5ccb-128">Por ejemplo, cuando inicias una navegación, debes esperar el `NavigationStarting` evento relacionado.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="b5ccb-129">Si después inicia otra navegación, debería ver el evento del `NavigationStarting` primer Navigate seguido por el `NavigationStarting` evento para el segundo Navigate, seguido del `NavigationCompleted` evento de la primera navegación y, a continuación, el resto de los eventos de navegación correspondientes de la segunda navegación.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="b5ccb-130">En casos de error puede o no ser un `ContentLoading` evento dependiendo de si la navegación continúa o no en una página de error.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="b5ccb-131">En el caso de una redirección HTTP, hay varios `NavigationStarting` eventos en una fila, donde los argumentos de evento posteriores tienen la `IsRedirect` propiedad establecida; sin embargo, el `NavigationId` sigue siendo el mismo.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="b5ccb-132">El mismo documento `navigations` , como navegar hasta un fragmento, no produce el `NavigationStarting` evento y no incrementa el `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="b5ccb-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="b5ccb-133">Para supervisar o cancelar `navigations` dentro de los submarcos en la vista de vistas de contenido, use el `FrameNavigationStarting` y los `FrameNavigationCompleted` eventos que actúan del mismo modo que los eventos equivalentes sin marcos.</span><span class="sxs-lookup"><span data-stu-id="b5ccb-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  
