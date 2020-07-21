---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8b29e3a4262afc708608de20d81e3463718a50c2
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884228"
---
# <span data-ttu-id="618c2-104">0.9.430: ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="618c2-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="618c2-105">Se crea un receptor para un evento de protocolo DevTools en particular y le permite suscribirse y unsubsribe de ese evento.</span><span class="sxs-lookup"><span data-stu-id="618c2-105">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubsribe from that event.</span></span>

## <span data-ttu-id="618c2-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="618c2-106">Summary</span></span>

 <span data-ttu-id="618c2-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="618c2-107">Members</span></span>                        | <span data-ttu-id="618c2-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="618c2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="618c2-109">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="618c2-109">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="618c2-110">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="618c2-110">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="618c2-111">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="618c2-111">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="618c2-112">Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="618c2-112">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="618c2-113">Obtenido del objeto WebView a través de GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="618c2-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="618c2-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="618c2-114">Members</span></span>

#### <span data-ttu-id="618c2-115">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="618c2-115">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="618c2-116">Suscribirse a un evento de DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="618c2-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="618c2-117">[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)pública HRESULT (controlador[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="618c2-117">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="618c2-118">Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente.</span><span class="sxs-lookup"><span data-stu-id="618c2-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="618c2-119">Se llamará a Invoke con el objeto de parámetro de un evento que contiene el objeto de parámetro del protocolo DevTools como una cadena JSON.</span><span class="sxs-lookup"><span data-stu-id="618c2-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

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

#### <span data-ttu-id="618c2-120">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="618c2-120">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="618c2-121">Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="618c2-121">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="618c2-122">[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)de HRESULT público (token EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="618c2-122">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

