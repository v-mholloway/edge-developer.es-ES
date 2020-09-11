---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 7cadbfddca9c05c8649b79503de3ce4f3695ea4c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011275"
---
# <span data-ttu-id="0ae05-104">0.9.579: ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="0ae05-104">0.9.579 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="0ae05-105">La persona que llama implementa esta interfaz para recibir eventos NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="0ae05-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="0ae05-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="0ae05-106">Summary</span></span>

 <span data-ttu-id="0ae05-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ae05-107">Members</span></span>                        | <span data-ttu-id="0ae05-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="0ae05-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0ae05-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0ae05-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0ae05-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0ae05-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0ae05-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ae05-111">Members</span></span>

#### <span data-ttu-id="0ae05-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="0ae05-112">Invoke</span></span> 

<span data-ttu-id="0ae05-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0ae05-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0ae05-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="0ae05-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

