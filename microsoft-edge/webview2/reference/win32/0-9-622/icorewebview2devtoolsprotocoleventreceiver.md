---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: 6b3d6170d84f5e968121f90e1eebe5daf532f03d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012594"
---
# <span data-ttu-id="d99d6-104">interfaz ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="d99d6-104">interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="d99d6-105">Se crea un receptor para un evento de protocolo DevTools en particular y le permite suscribirse y anular la suscripción de ese evento.</span><span class="sxs-lookup"><span data-stu-id="d99d6-105">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="d99d6-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="d99d6-106">Summary</span></span>

 <span data-ttu-id="d99d6-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d99d6-107">Members</span></span>                        | <span data-ttu-id="d99d6-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="d99d6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d99d6-109">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="d99d6-109">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="d99d6-110">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="d99d6-110">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="d99d6-111">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="d99d6-111">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="d99d6-112">Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="d99d6-112">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="d99d6-113">Obtenido del objeto WebView a través de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="d99d6-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="d99d6-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="d99d6-114">Members</span></span>

#### <span data-ttu-id="d99d6-115">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="d99d6-115">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="d99d6-116">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="d99d6-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="d99d6-117">[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)pública HRESULT (controlador[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d99d6-117">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d99d6-118">Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente.</span><span class="sxs-lookup"><span data-stu-id="d99d6-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="d99d6-119">Se llamará a Invoke con un objeto de argumentos de evento que contenga el objeto de parámetro del protocolo DevTools como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="d99d6-119">Invoke will be called with an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

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

#### <span data-ttu-id="d99d6-120">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="d99d6-120">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="d99d6-121">Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="d99d6-121">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="d99d6-122">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d99d6-122">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

