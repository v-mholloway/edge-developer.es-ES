---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: d2b1aa9bbfc15aa44023a43425bb2fc939165cae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880160"
---
# <span data-ttu-id="439f6-104">0.9.430: ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="439f6-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="439f6-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="439f6-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="439f6-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="439f6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="439f6-107">Se desencadena cuando se realiza una solicitud HTTP en la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="439f6-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="439f6-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="439f6-108">Summary</span></span>

 <span data-ttu-id="439f6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="439f6-109">Members</span></span>                        | <span data-ttu-id="439f6-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="439f6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="439f6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="439f6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="439f6-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="439f6-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="439f6-113">El host puede invalidar los encabezados de solicitud y respuesta y el contenido de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="439f6-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="439f6-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="439f6-114">Members</span></span>

#### <span data-ttu-id="439f6-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="439f6-115">Invoke</span></span> 

<span data-ttu-id="439f6-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="439f6-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="439f6-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="439f6-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

