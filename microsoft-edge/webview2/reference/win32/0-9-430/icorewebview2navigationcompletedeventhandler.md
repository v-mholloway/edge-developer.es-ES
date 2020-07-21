---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 57a0b844181c7c1ea14a56e87cc11dc008773a28
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886307"
---
# <span data-ttu-id="2ba69-104">0.9.430: ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2ba69-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="2ba69-105">La persona que llama implementa esta interfaz para recibir el evento NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2ba69-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="2ba69-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="2ba69-106">Summary</span></span>

 <span data-ttu-id="2ba69-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ba69-107">Members</span></span>                        | <span data-ttu-id="2ba69-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2ba69-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2ba69-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2ba69-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2ba69-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2ba69-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2ba69-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2ba69-111">Members</span></span>

#### <span data-ttu-id="2ba69-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2ba69-112">Invoke</span></span> 

<span data-ttu-id="2ba69-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="2ba69-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2ba69-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](ICoreWebView2.md) \* Sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2ba69-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span></span>

