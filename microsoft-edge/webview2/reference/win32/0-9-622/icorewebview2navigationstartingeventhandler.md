---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2NavigationStartingEventHandler
ms.openlocfilehash: ab4181d8a334ae4263665d964448f67cca965ff5
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012729"
---
# <span data-ttu-id="32f39-104">interfaz ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="32f39-104">interface ICoreWebView2NavigationStartingEventHandler</span></span> 

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="32f39-105">La persona que llama implementa esta interfaz para recibir el evento NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="32f39-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="32f39-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="32f39-106">Summary</span></span>

 <span data-ttu-id="32f39-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="32f39-107">Members</span></span>                        | <span data-ttu-id="32f39-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="32f39-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="32f39-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="32f39-109">Invoke</span></span>](#invoke) | <span data-ttu-id="32f39-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="32f39-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="32f39-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="32f39-111">Members</span></span>

#### <span data-ttu-id="32f39-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="32f39-112">Invoke</span></span> 

<span data-ttu-id="32f39-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="32f39-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="32f39-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="32f39-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>

