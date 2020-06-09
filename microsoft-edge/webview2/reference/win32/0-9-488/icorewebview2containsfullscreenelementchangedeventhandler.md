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
ms.openlocfilehash: d48baec759174d9dcecc236a685db12c5de03db1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697059"
---
# <span data-ttu-id="7f39d-104">interfaz ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7f39d-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7f39d-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7f39d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7f39d-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="7f39d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="7f39d-107">La persona que llama implementa este método para recibir los eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="7f39d-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="7f39d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="7f39d-108">Summary</span></span>

 <span data-ttu-id="7f39d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f39d-109">Members</span></span>                        | <span data-ttu-id="7f39d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7f39d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f39d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="7f39d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7f39d-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7f39d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="7f39d-113">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="7f39d-113">There are no event args for this event.</span></span>

## <span data-ttu-id="7f39d-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="7f39d-114">Members</span></span>

#### <span data-ttu-id="7f39d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="7f39d-115">Invoke</span></span> 

<span data-ttu-id="7f39d-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7f39d-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7f39d-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="7f39d-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="7f39d-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="7f39d-118">There are no event args and the args parameter will be null.</span></span>

