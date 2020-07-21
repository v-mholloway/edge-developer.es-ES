---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 70ecc1898f9a72656f12b912d103116c381d4218
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885677"
---
# <span data-ttu-id="8a77b-104">0.8.355: IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8a77b-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="8a77b-105">Se desencadena cuando se realiza una solicitud HTTP en la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="8a77b-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="8a77b-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="8a77b-106">Summary</span></span>

 <span data-ttu-id="8a77b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a77b-107">Members</span></span>                        | <span data-ttu-id="8a77b-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8a77b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8a77b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8a77b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8a77b-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8a77b-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="8a77b-111">El host puede invalidar los encabezados de solicitud y respuesta y el contenido de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a77b-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="8a77b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a77b-112">Members</span></span>

#### <span data-ttu-id="8a77b-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="8a77b-113">Invoke</span></span> 

<span data-ttu-id="8a77b-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8a77b-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8a77b-115">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8a77b-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

