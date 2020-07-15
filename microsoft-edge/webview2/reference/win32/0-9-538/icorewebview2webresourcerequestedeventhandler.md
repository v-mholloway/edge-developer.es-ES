---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 9cd221ac1b528b0be52201daa0c15217534944a6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879229"
---
# <span data-ttu-id="12f85-104">interfaz ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="12f85-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="12f85-105">Se desencadena cuando se realiza una solicitud HTTP en la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="12f85-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="12f85-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="12f85-106">Summary</span></span>

 <span data-ttu-id="12f85-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="12f85-107">Members</span></span>                        | <span data-ttu-id="12f85-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="12f85-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="12f85-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="12f85-109">Invoke</span></span>](#invoke) | <span data-ttu-id="12f85-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="12f85-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="12f85-111">El host puede invalidar los encabezados de solicitud y respuesta y el contenido de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="12f85-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="12f85-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="12f85-112">Members</span></span>

#### <span data-ttu-id="12f85-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="12f85-113">Invoke</span></span> 

<span data-ttu-id="12f85-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="12f85-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="12f85-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="12f85-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

