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
ms.openlocfilehash: 436e0e33180c65afcce0487fffeff5f168dceab7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655072"
---
# <span data-ttu-id="34409-104">interfaz IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="34409-104">interface IWebView2WebView3</span></span> 

> [!NOTE]
> <span data-ttu-id="34409-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="34409-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="34409-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="34409-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="34409-107">Funcionalidad adicional implementada por el objeto WebView principal.</span><span class="sxs-lookup"><span data-stu-id="34409-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="34409-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="34409-108">Summary</span></span>

 <span data-ttu-id="34409-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="34409-109">Members</span></span>                        | <span data-ttu-id="34409-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="34409-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="34409-111">Detener</span><span class="sxs-lookup"><span data-stu-id="34409-111">Stop</span></span>](#stop) | <span data-ttu-id="34409-112">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="34409-112">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="34409-113">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="34409-113">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="34409-114">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="34409-114">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="34409-115">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="34409-115">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="34409-116">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="34409-116">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="34409-117">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="34409-117">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="34409-118">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="34409-118">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="34409-119">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="34409-119">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="34409-120">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="34409-120">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="34409-121">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="34409-121">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="34409-122">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="34409-122">The title for the current top level document.</span></span>

<span data-ttu-id="34409-123">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="34409-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="34409-124">Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="34409-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="34409-125">Miembros</span><span class="sxs-lookup"><span data-stu-id="34409-125">Members</span></span>

#### <span data-ttu-id="34409-126">Detener</span><span class="sxs-lookup"><span data-stu-id="34409-126">Stop</span></span> 

<span data-ttu-id="34409-127">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="34409-127">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="34409-128">[HRESULT público](#stop)()</span><span class="sxs-lookup"><span data-stu-id="34409-128">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="34409-129">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="34409-129">add_NewWindowRequested</span></span> 

<span data-ttu-id="34409-130">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="34409-130">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="34409-131">[add_NewWindowRequested](#add_newwindowrequested)de HRESULT público ([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="34409-131">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="34409-132">Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open.</span><span class="sxs-lookup"><span data-stu-id="34409-132">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="34409-133">La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.</span><span class="sxs-lookup"><span data-stu-id="34409-133">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<IWebView2NewWindowRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<IWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="34409-134">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="34409-134">remove_NewWindowRequested</span></span> 

<span data-ttu-id="34409-135">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="34409-135">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="34409-136">[remove_NewWindowRequested](#remove_newwindowrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="34409-136">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="34409-137">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="34409-137">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="34409-138">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="34409-138">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="34409-139">[add_DocumentTitleChanged](#add_documenttitlechanged)de HRESULT público ([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="34409-139">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="34409-140">El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="34409-140">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<IWebView2DocumentTitleChangedEventHandler>(
            [this](IWebView2WebView3* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="34409-141">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="34409-141">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="34409-142">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="34409-142">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="34409-143">[remove_DocumentTitleChanged](#remove_documenttitlechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="34409-143">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="34409-144">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="34409-144">get_DocumentTitle</span></span> 

<span data-ttu-id="34409-145">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="34409-145">The title for the current top level document.</span></span>

> <span data-ttu-id="34409-146">[get_DocumentTitleción](#get_documenttitle)HRESULT pública (título LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="34409-146">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="34409-147">Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.</span><span class="sxs-lookup"><span data-stu-id="34409-147">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

