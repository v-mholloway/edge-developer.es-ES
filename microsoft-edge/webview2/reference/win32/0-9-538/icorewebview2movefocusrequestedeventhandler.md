---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2MoveFocusRequestedEventHandler
ms.openlocfilehash: bd07256203944b4d640d859451fa000cbc1fcd46
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011326"
---
# <span data-ttu-id="04e97-104">0.9.579: ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="04e97-104">0.9.579 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="04e97-105">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="04e97-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="04e97-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="04e97-106">Summary</span></span>

 <span data-ttu-id="04e97-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="04e97-107">Members</span></span>                        | <span data-ttu-id="04e97-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="04e97-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04e97-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="04e97-109">Invoke</span></span>](#invoke) | <span data-ttu-id="04e97-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="04e97-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="04e97-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="04e97-111">Members</span></span>

#### <span data-ttu-id="04e97-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="04e97-112">Invoke</span></span> 

<span data-ttu-id="04e97-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="04e97-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="04e97-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* Sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="04e97-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

