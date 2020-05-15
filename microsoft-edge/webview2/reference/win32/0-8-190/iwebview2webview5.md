---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 3c32cd59e75eb81bf69661d01f6044a0628ba35d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655067"
---
# <span data-ttu-id="bcfab-104">interfaz IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="bcfab-104">interface IWebView2WebView5</span></span> 

> [!NOTE]
> <span data-ttu-id="bcfab-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="bcfab-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="bcfab-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="bcfab-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="bcfab-107">Funcionalidad adicional implementada por el objeto WebView principal.</span><span class="sxs-lookup"><span data-stu-id="bcfab-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="bcfab-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="bcfab-108">Summary</span></span>

 <span data-ttu-id="bcfab-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bcfab-109">Members</span></span>                        | <span data-ttu-id="bcfab-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="bcfab-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bcfab-111">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="bcfab-111">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="bcfab-112">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="bcfab-112">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="bcfab-113">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="bcfab-113">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="bcfab-114">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bcfab-114">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="bcfab-115">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="bcfab-115">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="bcfab-116">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="bcfab-116">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="bcfab-117">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="bcfab-117">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="bcfab-118">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="bcfab-118">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="bcfab-119">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="bcfab-119">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="bcfab-120">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="bcfab-120">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="bcfab-121">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="bcfab-121">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="bcfab-122">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="bcfab-122">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="bcfab-123">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="bcfab-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="bcfab-124">Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="bcfab-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="bcfab-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="bcfab-125">Members</span></span>

#### <span data-ttu-id="bcfab-126">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="bcfab-126">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="bcfab-127">Notifica cuando cambia la propiedad ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="bcfab-127">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="bcfab-128">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)de HRESULT público ([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="bcfab-128">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="bcfab-129">Esto significa que un elemento HTML dentro de la vista de WebView está escribiendo Fullscreen en el tamaño de WebView o saliendo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="bcfab-129">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="bcfab-130">Este evento es útil cuando, por ejemplo, un elemento de vídeo solicita la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="bcfab-130">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="bcfab-131">El agente de escucha de ContainsFullScreenElementChanged puede cambiar el tamaño de la vista en WebView en respuesta.</span><span class="sxs-lookup"><span data-stu-id="bcfab-131">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="bcfab-132">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="bcfab-132">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="bcfab-133">Quitar un controlador de eventos agregado previamente con el método de evento add_ correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bcfab-133">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="bcfab-134">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="bcfab-134">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="bcfab-135">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="bcfab-135">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="bcfab-136">Indica si WebView contiene un elemento HTML de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="bcfab-136">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="bcfab-137">[get_ContainsFullScreenElement](#get_containsfullscreenelement)de HRESULT público (bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="bcfab-137">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="bcfab-138">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="bcfab-138">add_WebResourceRequested</span></span> 

<span data-ttu-id="bcfab-139">Agregue un controlador de eventos para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="bcfab-139">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="bcfab-140">[add_WebResourceRequested](#add_webresourcerequested)de HRESULT público ([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="bcfab-140">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="bcfab-141">Se desencadena cuando WebView realiza una solicitud HTTP a una dirección URL y un filtro de contexto de recursos coincidentes que se agregaron con AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="bcfab-141">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="bcfab-142">Debe agregar al menos un filtro para que se active el evento.</span><span class="sxs-lookup"><span data-stu-id="bcfab-142">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="bcfab-143">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="bcfab-143">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="bcfab-144">Agrega un URI y un filtro de contexto de recursos al evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="bcfab-144">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="bcfab-145">[ADDWEBRESOURCEREQUESTEDFILTER](#addwebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="bcfab-145">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="bcfab-146">El parámetro URI puede ser una cadena comodín (' ': cero o más, '? ': exactamente uno).</span><span class="sxs-lookup"><span data-stu-id="bcfab-146">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="bcfab-147">nullptr es equivalente a L "".</span><span class="sxs-lookup"><span data-stu-id="bcfab-147">nullptr is equivalent to L"".</span></span> <span data-ttu-id="bcfab-148">Consulta WEBVIEW2_WEB_RESOURCE_CONTEXT enum para obtener una descripción de los filtros de contexto de recursos.</span><span class="sxs-lookup"><span data-stu-id="bcfab-148">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="bcfab-149">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="bcfab-149">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="bcfab-150">Quita un filtro de recursos Webque coincide con el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="bcfab-150">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="bcfab-151">[REMOVEWEBRESOURCEREQUESTEDFILTER](#removewebresourcerequestedfilter)HRESULT público (LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span><span class="sxs-lookup"><span data-stu-id="bcfab-151">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="bcfab-152">Si se agregó el mismo filtro varias veces, tendrá que quitarlo tantas veces como se agregara para que la eliminación sea efectiva.</span><span class="sxs-lookup"><span data-stu-id="bcfab-152">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="bcfab-153">Devuelve E_INVALIDARG para un filtro que nunca se ha agregado.</span><span class="sxs-lookup"><span data-stu-id="bcfab-153">Returns E_INVALIDARG for a filter that was never added.</span></span>

