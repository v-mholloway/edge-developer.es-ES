---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 5a0c15cf56283c9d2ba71b9f8261288977c6ef39
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885474"
---
# <span data-ttu-id="95eaf-104">0.9.515: ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="95eaf-104">0.9.515 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="95eaf-105">La persona que llama implementa este método para recibir los eventos GotFocus y LostFocus.</span><span class="sxs-lookup"><span data-stu-id="95eaf-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="95eaf-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="95eaf-106">Summary</span></span>

 <span data-ttu-id="95eaf-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="95eaf-107">Members</span></span>                        | <span data-ttu-id="95eaf-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="95eaf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95eaf-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="95eaf-109">Invoke</span></span>](#invoke) | <span data-ttu-id="95eaf-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="95eaf-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="95eaf-111">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="95eaf-111">There are no event args for this event.</span></span>

## <span data-ttu-id="95eaf-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="95eaf-112">Members</span></span>

#### <span data-ttu-id="95eaf-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="95eaf-113">Invoke</span></span> 

<span data-ttu-id="95eaf-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="95eaf-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="95eaf-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="95eaf-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="95eaf-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="95eaf-116">There are no event args and the args parameter will be null.</span></span>

