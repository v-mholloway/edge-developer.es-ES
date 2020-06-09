---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: a38d451f4ee99e4ab1392f4685a66abf1f274ddb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698067"
---
# <span data-ttu-id="0d9f6-104">interfaz ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0d9f6-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0d9f6-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="0d9f6-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="0d9f6-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="0d9f6-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="0d9f6-107">La persona que llama implementa esta interfaz para recibir eventos DevToolsProtocolEventReceived de la vista en WebView.</span><span class="sxs-lookup"><span data-stu-id="0d9f6-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="0d9f6-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="0d9f6-108">Summary</span></span>

 <span data-ttu-id="0d9f6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d9f6-109">Members</span></span>                        | <span data-ttu-id="0d9f6-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0d9f6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0d9f6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="0d9f6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0d9f6-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0d9f6-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0d9f6-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d9f6-113">Members</span></span>

#### <span data-ttu-id="0d9f6-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="0d9f6-114">Invoke</span></span> 

<span data-ttu-id="0d9f6-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0d9f6-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0d9f6-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0d9f6-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

