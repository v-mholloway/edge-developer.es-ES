---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 4f2bb4e5077fea7583f7d9f9886923ea1867e1ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883685"
---
# <span data-ttu-id="2b097-104">0.9.515: ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2b097-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="2b097-105">Se desencadena cuando se realiza una solicitud HTTP en la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="2b097-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="2b097-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="2b097-106">Summary</span></span>

 <span data-ttu-id="2b097-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b097-107">Members</span></span>                        | <span data-ttu-id="2b097-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2b097-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2b097-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2b097-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2b097-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2b097-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2b097-111">El host puede invalidar los encabezados de solicitud y respuesta y el contenido de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2b097-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="2b097-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b097-112">Members</span></span>

#### <span data-ttu-id="2b097-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="2b097-113">Invoke</span></span> 

<span data-ttu-id="2b097-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2b097-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2b097-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2b097-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

