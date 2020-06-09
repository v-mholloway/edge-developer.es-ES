---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2908ad851a7899d2ea053bfa50616c8b244bca6c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699362"
---
# <span data-ttu-id="bb5f3-104">interfaz ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="bb5f3-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="bb5f3-105">La persona que llama implementa esta interfaz para recibir eventos DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="bb5f3-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="bb5f3-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="bb5f3-106">Summary</span></span>

 <span data-ttu-id="bb5f3-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bb5f3-107">Members</span></span>                        | <span data-ttu-id="bb5f3-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="bb5f3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bb5f3-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="bb5f3-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bb5f3-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bb5f3-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="bb5f3-111">Use la propiedad DocumentTitle para obtener el título modificado.</span><span class="sxs-lookup"><span data-stu-id="bb5f3-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="bb5f3-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="bb5f3-112">Members</span></span>

#### <span data-ttu-id="bb5f3-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="bb5f3-113">Invoke</span></span> 

<span data-ttu-id="bb5f3-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bb5f3-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bb5f3-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="bb5f3-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="bb5f3-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="bb5f3-116">There are no event args and the args parameter will be null.</span></span>

