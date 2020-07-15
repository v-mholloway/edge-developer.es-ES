---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: c0980f26ef06497cded81e2f9c7c00162af18d9b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878095"
---
# <span data-ttu-id="2c55d-104">0.8.355: IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2c55d-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="2c55d-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="2c55d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="2c55d-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2c55d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="2c55d-107">Se desencadena cuando se realiza una solicitud HTTP en la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="2c55d-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="2c55d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2c55d-108">Summary</span></span>

 <span data-ttu-id="2c55d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2c55d-109">Members</span></span>                        | <span data-ttu-id="2c55d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2c55d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2c55d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="2c55d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="2c55d-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2c55d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2c55d-113">El host puede invalidar los encabezados de solicitud y respuesta y el contenido de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c55d-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="2c55d-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="2c55d-114">Members</span></span>

#### <span data-ttu-id="2c55d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="2c55d-115">Invoke</span></span> 

<span data-ttu-id="2c55d-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2c55d-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2c55d-117">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2c55d-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

