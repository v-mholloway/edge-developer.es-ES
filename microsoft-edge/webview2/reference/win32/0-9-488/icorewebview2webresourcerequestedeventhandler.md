---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 715af5cbf2bbaf8301e39dce1516019102b61ab1
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877332"
---
# <span data-ttu-id="77f82-104">0.9.515: ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="77f82-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="77f82-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="77f82-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="77f82-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="77f82-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="77f82-107">Se desencadena cuando se realiza una solicitud HTTP en la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="77f82-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="77f82-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="77f82-108">Summary</span></span>

 <span data-ttu-id="77f82-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="77f82-109">Members</span></span>                        | <span data-ttu-id="77f82-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="77f82-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="77f82-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="77f82-111">Invoke</span></span>](#invoke) | <span data-ttu-id="77f82-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="77f82-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="77f82-113">El host puede invalidar los encabezados de solicitud y respuesta y el contenido de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="77f82-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="77f82-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="77f82-114">Members</span></span>

#### <span data-ttu-id="77f82-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="77f82-115">Invoke</span></span> 

<span data-ttu-id="77f82-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="77f82-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="77f82-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="77f82-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

