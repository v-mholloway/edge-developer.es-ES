---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: f4976cc5077f211970a953cebe7f2c3647879861
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880603"
---
# <span data-ttu-id="245c6-104">0.9.515: ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="245c6-104">0.9.515 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="245c6-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="245c6-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="245c6-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="245c6-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="245c6-107">La persona que llama implementa este método para recibir los eventos GotFocus y LostFocus.</span><span class="sxs-lookup"><span data-stu-id="245c6-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="245c6-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="245c6-108">Summary</span></span>

 <span data-ttu-id="245c6-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="245c6-109">Members</span></span>                        | <span data-ttu-id="245c6-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="245c6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="245c6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="245c6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="245c6-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="245c6-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="245c6-113">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="245c6-113">There are no event args for this event.</span></span>

## <span data-ttu-id="245c6-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="245c6-114">Members</span></span>

#### <span data-ttu-id="245c6-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="245c6-115">Invoke</span></span> 

<span data-ttu-id="245c6-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="245c6-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="245c6-117">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="245c6-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="245c6-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="245c6-118">There are no event args and the args parameter will be null.</span></span>

