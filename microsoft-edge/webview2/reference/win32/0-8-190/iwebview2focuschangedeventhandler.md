---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 8b7a588122b93cf56f7ce4473db87a0df16522b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885999"
---
# <span data-ttu-id="6c33e-104">0.8.355: IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6c33e-104">0.8.355 - interface IWebView2FocusChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6c33e-105">La persona que llama implementa este método para recibir los eventos GotFocus y LostFocus.</span><span class="sxs-lookup"><span data-stu-id="6c33e-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="6c33e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="6c33e-106">Summary</span></span>

 <span data-ttu-id="6c33e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c33e-107">Members</span></span>                        | <span data-ttu-id="6c33e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6c33e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c33e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6c33e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6c33e-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6c33e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6c33e-111">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="6c33e-111">There are no event args for this event.</span></span>

## <span data-ttu-id="6c33e-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="6c33e-112">Members</span></span>

#### <span data-ttu-id="6c33e-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="6c33e-113">Invoke</span></span> 

<span data-ttu-id="6c33e-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6c33e-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6c33e-115">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6c33e-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="6c33e-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="6c33e-116">There are no event args and the args parameter will be null.</span></span>

