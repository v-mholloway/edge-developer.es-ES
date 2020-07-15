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
# interfaz ICoreWebView2DevToolsProtocolEventReceiver 

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

Se crea un receptor para un evento de protocolo DevTools en particular y le permite suscribirse y anular la suscripción de ese evento.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | Suscribirse a un evento de DevToolsProtocol.
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.

Obtenido del objeto WebView a través de GetDevToolsProtocolEventReceiver.

## Miembros

#### add_DevToolsProtocolEventReceived 

Suscribirse a un evento de DevToolsProtocol.

> [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)pública HRESULT (controlador[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) *, EventRegistrationToken * token)

Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente. Se llamará a Invoke con un objeto de argumentos de evento que contenga el objeto de parámetro del protocolo DevTools como una cadena JSON.

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

#### remove_DevToolsProtocolEventReceived 

Quitar un controlador de eventos agregado previamente con add_DevToolsProtocolEventReceived.

> [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)de HRESULT público (token EventRegistrationToken)

