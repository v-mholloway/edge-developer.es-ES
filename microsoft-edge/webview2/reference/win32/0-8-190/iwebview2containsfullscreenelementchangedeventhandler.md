---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 70e9ad7782fe495ffd366664ecb132edd0c57df5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878655"
---
# <span data-ttu-id="17f8d-104">0.8.355: IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="17f8d-104">0.8.355 - interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="17f8d-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="17f8d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="17f8d-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="17f8d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="17f8d-107">La persona que llama implementa este método para recibir los eventos ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="17f8d-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="17f8d-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="17f8d-108">Summary</span></span>

 <span data-ttu-id="17f8d-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="17f8d-109">Members</span></span>                        | <span data-ttu-id="17f8d-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="17f8d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17f8d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="17f8d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="17f8d-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17f8d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="17f8d-113">No hay argumentos de evento para este evento.</span><span class="sxs-lookup"><span data-stu-id="17f8d-113">There are no event args for this event.</span></span>

## <span data-ttu-id="17f8d-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="17f8d-114">Members</span></span>

#### <span data-ttu-id="17f8d-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="17f8d-115">Invoke</span></span> 

<span data-ttu-id="17f8d-116">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17f8d-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="17f8d-117">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="17f8d-117">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="17f8d-118">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="17f8d-118">There are no event args and the args parameter will be null.</span></span>

