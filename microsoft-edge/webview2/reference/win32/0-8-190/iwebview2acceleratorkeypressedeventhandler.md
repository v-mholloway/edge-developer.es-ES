---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 6b5cf77e8091d79b582907b4cbfe7c9aa415de9c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879068"
---
# <span data-ttu-id="7eba0-104">0.8.355: IWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7eba0-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7eba0-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="7eba0-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="7eba0-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="7eba0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="7eba0-107">La persona que llama implementa esta interfaz para recibir el evento AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7eba0-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="7eba0-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="7eba0-108">Summary</span></span>

 <span data-ttu-id="7eba0-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="7eba0-109">Members</span></span>                        | <span data-ttu-id="7eba0-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7eba0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7eba0-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="7eba0-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7eba0-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7eba0-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="7eba0-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="7eba0-113">Members</span></span>

#### <span data-ttu-id="7eba0-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="7eba0-114">Invoke</span></span> 

<span data-ttu-id="7eba0-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7eba0-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7eba0-116">invocación [Invoke](#invoke)pública de HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7eba0-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

