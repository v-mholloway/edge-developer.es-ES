---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8a826b5693bce0970c4360fb40c7e13ccacc1f01
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880979"
---
# <span data-ttu-id="a1357-104">0.9.430: ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a1357-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a1357-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="a1357-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a1357-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="a1357-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="a1357-107">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="a1357-107">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="a1357-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="a1357-108">Summary</span></span>

 <span data-ttu-id="a1357-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1357-109">Members</span></span>                        | <span data-ttu-id="a1357-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a1357-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a1357-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a1357-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a1357-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a1357-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a1357-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1357-113">Members</span></span>

#### <span data-ttu-id="a1357-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="a1357-114">Invoke</span></span> 

<span data-ttu-id="a1357-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a1357-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a1357-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a1357-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

