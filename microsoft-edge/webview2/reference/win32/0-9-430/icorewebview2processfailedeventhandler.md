---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 9dbf6ee630db1e99a74506f377fb4e01018c340f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877598"
---
# <span data-ttu-id="a2ee0-104">0.9.430: ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a2ee0-104">0.9.430 - interface ICoreWebView2ProcessFailedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a2ee0-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a2ee0-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="a2ee0-107">La persona que llama implementa esta interfaz para recibir eventos ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-107">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="a2ee0-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a2ee0-108">Summary</span></span>

 <span data-ttu-id="a2ee0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2ee0-109">Members</span></span>                        | <span data-ttu-id="a2ee0-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a2ee0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a2ee0-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a2ee0-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a2ee0-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a2ee0-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a2ee0-113">Members</span></span>

#### <span data-ttu-id="a2ee0-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="a2ee0-114">Invoke</span></span> 

<span data-ttu-id="a2ee0-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a2ee0-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2ProcessFailedEventArgs](ICoreWebView2ProcessFailedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a2ee0-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ProcessFailedEventArgs](ICoreWebView2ProcessFailedEventArgs.md) \* args)</span></span>

