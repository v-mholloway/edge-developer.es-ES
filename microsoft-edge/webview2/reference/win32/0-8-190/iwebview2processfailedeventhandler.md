---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 97a0d8f2afda5f6391a574e6ad62fbd2e17abcc1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884942"
---
# <span data-ttu-id="ebf9d-104">0.8.355: IWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ebf9d-104">0.8.355 - interface IWebView2ProcessFailedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="ebf9d-105">La persona que llama implementa esta interfaz para recibir eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="ebf9d-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ebf9d-106">Summary</span></span>

 <span data-ttu-id="ebf9d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ebf9d-107">Members</span></span>                        | <span data-ttu-id="ebf9d-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ebf9d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ebf9d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ebf9d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ebf9d-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ebf9d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ebf9d-111">Members</span></span>

#### <span data-ttu-id="ebf9d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ebf9d-112">Invoke</span></span> 

<span data-ttu-id="ebf9d-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ebf9d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ebf9d-114">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ebf9d-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ProcessFailedEventArgs](IWebView2ProcessFailedEventArgs.md) \* args)</span></span>

