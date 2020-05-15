---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 7c5aece49cf2a3e8e6a65eba3fbb4d46f0ff2997
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655246"
---
# <span data-ttu-id="92958-104">interfaz ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="92958-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="92958-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="92958-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="92958-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="92958-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="92958-107">La persona que llama implementa este método para recibir los eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="92958-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="92958-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="92958-108">Summary</span></span>

 <span data-ttu-id="92958-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="92958-109">Members</span></span>                        | <span data-ttu-id="92958-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="92958-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="92958-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="92958-111">Invoke</span></span>](#invoke) | <span data-ttu-id="92958-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="92958-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="92958-113">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="92958-113">There are no event args for this event.</span></span>

## <span data-ttu-id="92958-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="92958-114">Members</span></span>

#### <span data-ttu-id="92958-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="92958-115">Invoke</span></span> 

<span data-ttu-id="92958-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="92958-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="92958-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="92958-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="92958-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="92958-118">There are no event args and the args parameter will be null.</span></span>

