---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: d50f84edeb532d90a1268f553b38e4cbf256556a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884090"
---
# <span data-ttu-id="e1122-104">0.9.430: ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e1122-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e1122-105">La persona que llama implementa este método para recibir el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="e1122-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="e1122-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="e1122-106">Summary</span></span>

 <span data-ttu-id="e1122-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1122-107">Members</span></span>                        | <span data-ttu-id="e1122-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="e1122-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1122-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1122-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e1122-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e1122-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e1122-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1122-111">Members</span></span>

#### <span data-ttu-id="e1122-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1122-112">Invoke</span></span> 

<span data-ttu-id="e1122-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e1122-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e1122-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* Sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e1122-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

