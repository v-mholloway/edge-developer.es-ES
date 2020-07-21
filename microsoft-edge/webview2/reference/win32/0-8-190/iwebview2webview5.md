---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: bc48c5d495c2182ba39b867fdb46ce7af503f5ba
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884690"
---
# <span data-ttu-id="82604-104">0.8.355: IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="82604-104">0.8.355 - interface IWebView2WebView5</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="82604-105">Funcionalidad adicional implementada por el objeto WebView principal.</span><span class="sxs-lookup"><span data-stu-id="82604-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="82604-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="82604-106">Summary</span></span>

 <span data-ttu-id="82604-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="82604-107">Members</span></span>                        | <span data-ttu-id="82604-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="82604-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82604-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="82604-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="82604-110">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="82604-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="82604-111">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="82604-111">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="82604-112">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="82604-112">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="82604-113">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="82604-113">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="82604-114">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="82604-114">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="82604-115">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="82604-115">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="82604-116">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="82604-116">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="82604-117">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="82604-117">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="82604-118">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="82604-118">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="82604-119">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="82604-119">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="82604-120">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="82604-120">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="82604-121">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="82604-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="82604-122">Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="82604-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="82604-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="82604-123">Members</span></span>

#### <span data-ttu-id="82604-124">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="82604-124">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="82604-125">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="82604-125">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="82604-126">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)de HRESULT público ([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="82604-126">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="82604-127">Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="82604-127">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="82604-128">Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="82604-128">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="82604-129">El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.</span><span class="sxs-lookup"><span data-stu-id="82604-129">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<IWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](IWebView2WebView5* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="82604-130">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="82604-130">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="82604-131">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="82604-131">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="82604-132">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="82604-132">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="82604-133">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="82604-133">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="82604-134">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="82604-134">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="82604-135">[get_ContainsFullScreenElement](#get_containsfullscreenelement)de HRESULT público (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="82604-135">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="82604-136">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="82604-136">add_WebResourceRequested</span></span> 

<span data-ttu-id="82604-137">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="82604-137">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="82604-138">[add_WebResourceRequested](#add_webresourcerequested)de HRESULT público ([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="82604-138">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="82604-139">Se desencadena cuando WebView realiza una solicitud HTTP a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="82604-139">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="82604-140">Debe agregar al menos un filtro para que se active el evento.</span><span class="sxs-lookup"><span data-stu-id="82604-140">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="82604-141">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="82604-141">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="82604-142">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="82604-142">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="82604-143">[ADDWEBRESOURCEREQUESTEDFILTER](#addwebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="82604-143">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="82604-144">El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno).</span><span class="sxs-lookup"><span data-stu-id="82604-144">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="82604-145">nullptr es equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="82604-145">nullptr is equivalent to L"".</span></span> <span data-ttu-id="82604-146">Consulta WEBVIEW2_WEB_RESOURCE_CONTEXT enum para obtener una descripción de los filtros de contexto de recursos.</span><span class="sxs-lookup"><span data-stu-id="82604-146">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="82604-147">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="82604-147">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="82604-148">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="82604-148">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="82604-149">[REMOVEWEBRESOURCEREQUESTEDFILTER](#removewebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="82604-149">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="82604-150">Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva.</span><span class="sxs-lookup"><span data-stu-id="82604-150">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="82604-151">Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="82604-151">Returns E_INVALIDARG for a filter that was never added.</span></span>

