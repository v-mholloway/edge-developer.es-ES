---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b3eb56101c6e69bab018cbb549339fd5deb2eb3e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885194"
---
# <span data-ttu-id="8e3fe-104">0.9.515: ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8e3fe-104">0.9.515 - interface ICoreWebView2SourceChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="8e3fe-105">La persona que llama implementa esta interfaz para recibir el evento SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="8e3fe-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="8e3fe-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="8e3fe-106">Summary</span></span>

 <span data-ttu-id="8e3fe-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e3fe-107">Members</span></span>                        | <span data-ttu-id="8e3fe-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="8e3fe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8e3fe-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8e3fe-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8e3fe-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8e3fe-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8e3fe-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e3fe-111">Members</span></span>

#### <span data-ttu-id="8e3fe-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="8e3fe-112">Invoke</span></span> 

<span data-ttu-id="8e3fe-113">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="8e3fe-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8e3fe-114">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8e3fe-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>

