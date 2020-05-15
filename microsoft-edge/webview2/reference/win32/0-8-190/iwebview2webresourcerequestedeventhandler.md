---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 602c00258e9ff3362269ebe90de8306ecbd7503e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655129"
---
# <span data-ttu-id="584e5-104">interfaz IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="584e5-104">interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="584e5-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="584e5-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="584e5-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="584e5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="584e5-107">Se desencadena cuando se realiza una solicitud HTTP en la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="584e5-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="584e5-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="584e5-108">Summary</span></span>

 <span data-ttu-id="584e5-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="584e5-109">Members</span></span>                        | <span data-ttu-id="584e5-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="584e5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="584e5-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="584e5-111">Invoke</span></span>](#invoke) | <span data-ttu-id="584e5-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="584e5-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="584e5-113">El host puede invalidar los encabezados de solicitud y respuesta y el contenido de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="584e5-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="584e5-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="584e5-114">Members</span></span>

#### <span data-ttu-id="584e5-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="584e5-115">Invoke</span></span> 

<span data-ttu-id="584e5-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="584e5-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="584e5-117">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="584e5-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

