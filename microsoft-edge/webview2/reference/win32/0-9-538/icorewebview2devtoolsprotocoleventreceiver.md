---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: cc2203e698947702cd4f3e39f95f2371519c9a25
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880104"
---
# <span data-ttu-id="7a4cd-104">interfaz ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="7a4cd-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="7a4cd-105">Se crea un receptor para un evento de protocolo DevTools en particular y le permite suscribirse y anular la suscripción de ese evento.</span><span class="sxs-lookup"><span data-stu-id="7a4cd-105">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="7a4cd-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7a4cd-106">Summary</span></span>

 <span data-ttu-id="7a4cd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a4cd-107">Members</span></span>                        | <span data-ttu-id="7a4cd-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7a4cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a4cd-109">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7a4cd-109">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="7a4cd-110">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7a4cd-110">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="7a4cd-111">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7a4cd-111">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="7a4cd-112">Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="7a4cd-112">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="7a4cd-113">Obtenido del objeto WebView a través de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="7a4cd-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="7a4cd-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a4cd-114">Members</span></span>

#### <span data-ttu-id="7a4cd-115">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7a4cd-115">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="7a4cd-116">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7a4cd-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="7a4cd-117">[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)pública HRESULT (controlador[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7a4cd-117">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7a4cd-118">Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7a4cd-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="7a4cd-119">Se llamará a Invoke con un objeto de argumentos de evento que contenga el objeto de parámetro del protocolo DevTools como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="7a4cd-119">Invoke will be called with an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="7a4cd-120">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7a4cd-120">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="7a4cd-121">Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="7a4cd-121">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="7a4cd-122">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7a4cd-122">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

