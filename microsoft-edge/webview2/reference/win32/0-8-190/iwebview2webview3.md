---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: a095b1ed085cd49a597195e01da21cde53b9095d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884746"
---
# <span data-ttu-id="89500-104">0.8.355: IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="89500-104">0.8.355 - interface IWebView2WebView3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="89500-105">Funcionalidad adicional implementada por el objeto WebView principal.</span><span class="sxs-lookup"><span data-stu-id="89500-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="89500-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="89500-106">Summary</span></span>

 <span data-ttu-id="89500-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="89500-107">Members</span></span>                        | <span data-ttu-id="89500-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="89500-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="89500-109">Detener</span><span class="sxs-lookup"><span data-stu-id="89500-109">Stop</span></span>](#stop) | <span data-ttu-id="89500-110">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="89500-110">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="89500-111">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="89500-111">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="89500-112">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="89500-112">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="89500-113">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="89500-113">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="89500-114">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="89500-114">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="89500-115">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="89500-115">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="89500-116">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="89500-116">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="89500-117">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="89500-117">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="89500-118">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="89500-118">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="89500-119">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="89500-119">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="89500-120">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="89500-120">The title for the current top level document.</span></span>

<span data-ttu-id="89500-121">Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="89500-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="89500-122">Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="89500-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="89500-123">Miembros</span><span class="sxs-lookup"><span data-stu-id="89500-123">Members</span></span>

#### <span data-ttu-id="89500-124">Detener</span><span class="sxs-lookup"><span data-stu-id="89500-124">Stop</span></span> 

<span data-ttu-id="89500-125">Detenga todas las navegaciones y las búsquedas de recursos pendientes.</span><span class="sxs-lookup"><span data-stu-id="89500-125">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="89500-126">[HRESULT público](#stop)()</span><span class="sxs-lookup"><span data-stu-id="89500-126">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="89500-127">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="89500-127">add_NewWindowRequested</span></span> 

<span data-ttu-id="89500-128">Agregue un controlador de eventos para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="89500-128">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="89500-129">[add_NewWindowRequested](#add_newwindowrequested)de HRESULT público ([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="89500-129">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="89500-130">Se desencadena cuando el contenido de la vista en WebView solicita abrir una nueva ventana, por ejemplo, a través de window. Open.</span><span class="sxs-lookup"><span data-stu-id="89500-130">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="89500-131">La aplicación puede pasar una vista previa de destino que se considerará la ventana abierta.</span><span class="sxs-lookup"><span data-stu-id="89500-131">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="89500-132">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="89500-132">remove_NewWindowRequested</span></span> 

<span data-ttu-id="89500-133">Quitar un controlador de eventos agregado previamente con add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="89500-133">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="89500-134">[remove_NewWindowRequested](#remove_newwindowrequested)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="89500-134">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="89500-135">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="89500-135">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="89500-136">Agregue un controlador de eventos para el evento DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="89500-136">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="89500-137">[add_DocumentTitleChanged](#add_documenttitlechanged)de HRESULT público ([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="89500-137">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="89500-138">El evento se desencadena cuando la propiedad DocumentTitle de WebView cambia y se puede activar antes o después del evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="89500-138">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="89500-139">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="89500-139">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="89500-140">Quitar un controlador de eventos agregado previamente con add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="89500-140">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="89500-141">[remove_DocumentTitleChanged](#remove_documenttitlechanged)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="89500-141">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="89500-142">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="89500-142">get_DocumentTitle</span></span> 

<span data-ttu-id="89500-143">Título del documento de nivel superior actual.</span><span class="sxs-lookup"><span data-stu-id="89500-143">The title for the current top level document.</span></span>

> <span data-ttu-id="89500-144">[get_DocumentTitleción](#get_documenttitle)HRESULT pública (título LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="89500-144">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="89500-145">Si el documento no tiene un título explícito o no está vacío, de lo contrario, se usará un valor predeterminado que puede o no coincidir con el URI del documento.</span><span class="sxs-lookup"><span data-stu-id="89500-145">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

