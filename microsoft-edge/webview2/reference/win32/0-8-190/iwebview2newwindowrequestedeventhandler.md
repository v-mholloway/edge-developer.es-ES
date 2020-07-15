---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: bacd1cff4406caffd4d7c3e1ca4c3e320c051443
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878326"
---
# <span data-ttu-id="2d479-104">0.8.355: IWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2d479-104">0.8.355 - interface IWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="2d479-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="2d479-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="2d479-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2d479-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="2d479-107">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="2d479-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="2d479-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2d479-108">Summary</span></span>

 <span data-ttu-id="2d479-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d479-109">Members</span></span>                        | <span data-ttu-id="2d479-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2d479-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2d479-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="2d479-111">Invoke</span></span>](#invoke) | <span data-ttu-id="2d479-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2d479-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2d479-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="2d479-113">Members</span></span>

#### <span data-ttu-id="2d479-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="2d479-114">Invoke</span></span> 

<span data-ttu-id="2d479-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2d479-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2d479-116">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2d479-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>

