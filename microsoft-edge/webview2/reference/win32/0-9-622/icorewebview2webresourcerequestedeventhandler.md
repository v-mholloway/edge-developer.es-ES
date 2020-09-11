---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 6aa36c8b28a3e47a796324987687ab23179aae10
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012591"
---
# <span data-ttu-id="599c1-104">interfaz ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="599c1-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="599c1-105">Se desencadena cuando se realiza una solicitud de dirección URL (a través de red, archivo, etc.) en la vista Web para un filtro de contexto de recursos y una dirección URL especificados en AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="599c1-105">Fires when a URL request (through network, file etc.) is made in the webview for a Web resource matching resource context filter and URL specified in AddWebResourceRequestedFilter.</span></span>

## <span data-ttu-id="599c1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="599c1-106">Summary</span></span>

 <span data-ttu-id="599c1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="599c1-107">Members</span></span>                        | <span data-ttu-id="599c1-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="599c1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="599c1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="599c1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="599c1-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="599c1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="599c1-111">El anfitrión puede ver y modificar la solicitud o proporcionar una respuesta de un patrón similar a HTTP, en cuyo caso la solicitud se completa inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="599c1-111">The host can view and modify the request or provide a response in a similar pattern to HTTP, in which case the request immediately completed.</span></span> <span data-ttu-id="599c1-112">Es posible que no contenga encabezados de solicitud agregados por la pila de red, como encabezados de autorización.</span><span class="sxs-lookup"><span data-stu-id="599c1-112">This may not contain any request headers that are added by the network stack, such as Authorization headers.</span></span>

## <span data-ttu-id="599c1-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="599c1-113">Members</span></span>

#### <span data-ttu-id="599c1-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="599c1-114">Invoke</span></span> 

<span data-ttu-id="599c1-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="599c1-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="599c1-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="599c1-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

