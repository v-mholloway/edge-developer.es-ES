---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Experimental
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2Experimental
ms.openlocfilehash: 98f13193e73781f9f7371db05ed3ca99ca93c128
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886572"
---
# <span data-ttu-id="e8450-104">interfaz ICoreWebView2Experimental</span><span class="sxs-lookup"><span data-stu-id="e8450-104">interface ICoreWebView2Experimental</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2Experimental
  : public IUnknown
```

## <span data-ttu-id="e8450-105">Resumen</span><span class="sxs-lookup"><span data-stu-id="e8450-105">Summary</span></span>

 <span data-ttu-id="e8450-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e8450-106">Members</span></span>                        | <span data-ttu-id="e8450-107">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e8450-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e8450-108">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="e8450-108">add_WebResourceResponseReceived</span></span>](#add_webresourceresponsereceived) | <span data-ttu-id="e8450-109">Agregue un controlador de eventos para el evento WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="e8450-109">Add an event handler for the WebResourceResponseReceived event.</span></span>
[<span data-ttu-id="e8450-110">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="e8450-110">remove_WebResourceResponseReceived</span></span>](#remove_webresourceresponsereceived) | <span data-ttu-id="e8450-111">Quita el controlador de eventos WebResourceResponseReceived agregado anteriormente con add_WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="e8450-111">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

## <span data-ttu-id="e8450-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="e8450-112">Members</span></span>

#### <span data-ttu-id="e8450-113">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="e8450-113">add_WebResourceResponseReceived</span></span> 

<span data-ttu-id="e8450-114">Agregue un controlador de eventos para el evento WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="e8450-114">Add an event handler for the WebResourceResponseReceived event.</span></span>

> <span data-ttu-id="e8450-115">[add_WebResourceResponseReceived](#add_webresourceresponsereceived)de HRESULT público ([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* EventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="e8450-115">public HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e8450-116">El evento WebResourceResponseReceived se desencadena después de que la vista previa reciba y procese la respuesta de una solicitud de recursos de WebResource.</span><span class="sxs-lookup"><span data-stu-id="e8450-116">WebResourceResponseReceived event fires after the WebView has received and processed the response for a WebResource request.</span></span> <span data-ttu-id="e8450-117">Los argumentos del evento incluyen los WebResourceRequest enviados por el cable y WebResourceResponse recibidos, incluidos los encabezados adicionales agregados por la pila de red que no se incluyeron como parte del evento WebResourceRequested asociado, como los encabezados de autenticación.</span><span class="sxs-lookup"><span data-stu-id="e8450-117">The event args include the WebResourceRequest as sent by the wire and WebResourceResponse received, including any additional headers added by the network stack that were not be included as part of the associated WebResourceRequested event, such as Authentication headers.</span></span> 
```cpp
    wil::com_ptr<ICoreWebView2Experimental> webviewExperimental;
    CHECK_FAILURE(m_appWindow->GetWebView()->QueryInterface(IID_PPV_ARGS(&webviewExperimental)));
    CHECK_FAILURE(webviewExperimental->add_WebResourceResponseReceived(
        Callback<ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler>(
            [this](
                ICoreWebView2Experimental* sender,
                ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs* args) {           
                wil::com_ptr<ICoreWebView2WebResourceRequest> request;
                CHECK_FAILURE(args->get_Request(&request));
                wil::unique_cotaskmem_string uri;
                CHECK_FAILURE(request->get_Uri(&uri));
                if (wcscmp(uri.get(), L"https://authenticationtest.com/HTTPAuth/") == 0)
                {
                    wil::com_ptr<ICoreWebView2HttpRequestHeaders> requestHeaders;
                    CHECK_FAILURE(request->get_Headers(&requestHeaders));

                    wil::unique_cotaskmem_string authHeaderValue;
                    if (requestHeaders->GetHeader(L"Authorization", &authHeaderValue) == S_OK)
                    {
                        std::wstring message(L"Authorization: ");
                        message += authHeaderValue.get();
                        MessageBox(nullptr, message.c_str(), nullptr, MB_OK);
                        m_appWindow->DeleteComponent(this);
                    }
                }
                
                return S_OK;
            })
            .Get(),
        &m_webResourceResponseReceivedToken));
```

#### <span data-ttu-id="e8450-118">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="e8450-118">remove_WebResourceResponseReceived</span></span> 

<span data-ttu-id="e8450-119">Quita el controlador de eventos WebResourceResponseReceived agregado anteriormente con add_WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="e8450-119">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

> <span data-ttu-id="e8450-120">[remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="e8450-120">public HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(EventRegistrationToken token)</span></span>

