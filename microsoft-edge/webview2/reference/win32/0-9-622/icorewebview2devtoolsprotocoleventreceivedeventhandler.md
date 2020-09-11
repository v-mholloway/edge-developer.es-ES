---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 4b280a16c18c84641f91efd39407f93db968f69d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012760"
---
# <span data-ttu-id="71e09-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="71e09-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="71e09-105">La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="71e09-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="71e09-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="71e09-106">Summary</span></span>

 <span data-ttu-id="71e09-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="71e09-107">Members</span></span>                        | <span data-ttu-id="71e09-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="71e09-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="71e09-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="71e09-109">Invoke</span></span>](#invoke) | <span data-ttu-id="71e09-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="71e09-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="71e09-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="71e09-111">Members</span></span>

#### <span data-ttu-id="71e09-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="71e09-112">Invoke</span></span> 

<span data-ttu-id="71e09-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="71e09-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="71e09-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="71e09-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

