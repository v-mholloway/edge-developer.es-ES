---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: fe84f29798b01aed2787559c717f2893c9eda7f9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885943"
---
# <span data-ttu-id="69c09-104">0.8.355: IWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="69c09-104">0.8.355 - interface IWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="69c09-105">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="69c09-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="69c09-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="69c09-106">Summary</span></span>

 <span data-ttu-id="69c09-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="69c09-107">Members</span></span>                        | <span data-ttu-id="69c09-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="69c09-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="69c09-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="69c09-109">Invoke</span></span>](#invoke) | <span data-ttu-id="69c09-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="69c09-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="69c09-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="69c09-111">Members</span></span>

#### <span data-ttu-id="69c09-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="69c09-112">Invoke</span></span> 

<span data-ttu-id="69c09-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="69c09-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="69c09-114">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="69c09-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

