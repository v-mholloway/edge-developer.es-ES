---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 44e24ef8e0e4b41968835ff7cd70fd9904482c6c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878452"
---
# <span data-ttu-id="9adbe-104">0.8.355: IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9adbe-104">0.8.355 - interface IWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="9adbe-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="9adbe-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="9adbe-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="9adbe-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9adbe-107">La persona que llama implementa este método para recibir los eventos GotFocus y LostFocus.</span><span class="sxs-lookup"><span data-stu-id="9adbe-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="9adbe-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="9adbe-108">Summary</span></span>

 <span data-ttu-id="9adbe-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="9adbe-109">Members</span></span>                        | <span data-ttu-id="9adbe-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="9adbe-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9adbe-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="9adbe-111">Invoke</span></span>](#invoke) | <span data-ttu-id="9adbe-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9adbe-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="9adbe-113">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="9adbe-113">There are no event args for this event.</span></span>

## <span data-ttu-id="9adbe-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="9adbe-114">Members</span></span>

#### <span data-ttu-id="9adbe-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="9adbe-115">Invoke</span></span> 

<span data-ttu-id="9adbe-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9adbe-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9adbe-117">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9adbe-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="9adbe-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="9adbe-118">There are no event args and the args parameter will be null.</span></span>

