---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: 7e02fb9480f70dbffe6d33cfd7fb436c26c97da3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011366"
---
# <span data-ttu-id="16537-104">0.9.579: ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="16537-104">0.9.579 - interface ICoreWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="16537-105">La persona que llama implementa este método para recibir los eventos GotFocus y LostFocus.</span><span class="sxs-lookup"><span data-stu-id="16537-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="16537-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="16537-106">Summary</span></span>

 <span data-ttu-id="16537-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="16537-107">Members</span></span>                        | <span data-ttu-id="16537-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="16537-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="16537-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="16537-109">Invoke</span></span>](#invoke) | <span data-ttu-id="16537-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="16537-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="16537-111">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="16537-111">There are no event args for this event.</span></span>

## <span data-ttu-id="16537-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="16537-112">Members</span></span>

#### <span data-ttu-id="16537-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="16537-113">Invoke</span></span> 

<span data-ttu-id="16537-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="16537-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="16537-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="16537-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="16537-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="16537-116">There are no event args and the args parameter will be null.</span></span>

