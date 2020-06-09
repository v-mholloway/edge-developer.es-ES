---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: df43e9cb1d036482a73e1ff92446a5a74b921d5d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698158"
---
# <span data-ttu-id="c4319-104">interfaz ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c4319-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c4319-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c4319-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c4319-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="c4319-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="c4319-107">La persona que llama implementa esta interfaz para recibir eventos NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="c4319-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="c4319-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="c4319-108">Summary</span></span>

 <span data-ttu-id="c4319-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4319-109">Members</span></span>                        | <span data-ttu-id="c4319-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c4319-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4319-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4319-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c4319-112">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c4319-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c4319-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4319-113">Members</span></span>

#### <span data-ttu-id="c4319-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4319-114">Invoke</span></span> 

<span data-ttu-id="c4319-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c4319-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c4319-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2](icorewebview2.md) \* Sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="c4319-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

