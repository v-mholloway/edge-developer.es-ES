---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 7f710b4da71a4a4e61869f06e5d2a4a95a2d0891
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885712"
---
# <span data-ttu-id="a2799-104">0.8.355: IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="a2799-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="a2799-105">Argumentos de evento para el evento WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="a2799-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="a2799-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="a2799-106">Summary</span></span>

 <span data-ttu-id="a2799-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2799-107">Members</span></span>                        | <span data-ttu-id="a2799-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a2799-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a2799-109">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="a2799-109">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="a2799-110">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="a2799-110">The web resource request contexts.</span></span>

## <span data-ttu-id="a2799-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2799-111">Members</span></span>

#### <span data-ttu-id="a2799-112">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="a2799-112">get_ResourceContext</span></span> 

<span data-ttu-id="a2799-113">Los contextos de solicitud de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="a2799-113">The web resource request contexts.</span></span>

> <span data-ttu-id="a2799-114">[get_ResourceContext](#get_resourcecontext)de HRESULT público (WEBVIEW2_WEB_RESOURCE_CONTEXT \*)</span><span class="sxs-lookup"><span data-stu-id="a2799-114">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

