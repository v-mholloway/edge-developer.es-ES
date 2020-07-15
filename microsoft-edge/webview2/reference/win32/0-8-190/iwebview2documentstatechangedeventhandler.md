---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: b669d04ba46b1670610e1efb00b552b2b6b1a4fc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878571"
---
# <span data-ttu-id="a5c50-104">0.8.355: IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a5c50-104">0.8.355 - interface IWebView2DocumentStateChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a5c50-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a5c50-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a5c50-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a5c50-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="a5c50-107">La persona que llama implementa esta interfaz para recibir el evento DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="a5c50-107">The caller implements this interface to receive the DocumentStateChanged event.</span></span>

## <span data-ttu-id="a5c50-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a5c50-108">Summary</span></span>

 <span data-ttu-id="a5c50-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5c50-109">Members</span></span>                        | <span data-ttu-id="a5c50-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a5c50-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a5c50-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a5c50-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a5c50-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a5c50-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a5c50-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5c50-113">Members</span></span>

#### <span data-ttu-id="a5c50-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="a5c50-114">Invoke</span></span> 

<span data-ttu-id="a5c50-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a5c50-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a5c50-116">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a5c50-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span></span>

