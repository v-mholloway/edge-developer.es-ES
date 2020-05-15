---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2f3effd612303d1532c7220d566791a800753b37
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655112"
---
# <span data-ttu-id="b74c3-104">interfaz ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b74c3-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="b74c3-105">Se desencadena cuando se realiza una solicitud HTTP en la vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="b74c3-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="b74c3-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="b74c3-106">Summary</span></span>

 <span data-ttu-id="b74c3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b74c3-107">Members</span></span>                        | <span data-ttu-id="b74c3-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="b74c3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b74c3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b74c3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b74c3-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b74c3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b74c3-111">El host puede invalidar los encabezados de solicitud y respuesta y el contenido de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b74c3-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="b74c3-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="b74c3-112">Members</span></span>

#### <span data-ttu-id="b74c3-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="b74c3-113">Invoke</span></span> 

<span data-ttu-id="b74c3-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b74c3-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b74c3-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b74c3-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

