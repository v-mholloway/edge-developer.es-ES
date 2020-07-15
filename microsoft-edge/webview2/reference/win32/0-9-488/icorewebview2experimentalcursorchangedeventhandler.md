---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 6fbcc82409791bc3d2da3bb2f7985732cb344a97
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880629"
---
# <span data-ttu-id="6fec7-104">0.9.515: ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6fec7-104">0.9.515 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="6fec7-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="6fec7-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6fec7-106">La persona que llama implementa esta interfaz para recibir eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="6fec7-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="6fec7-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="6fec7-107">Summary</span></span>

 <span data-ttu-id="6fec7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6fec7-108">Members</span></span>                        | <span data-ttu-id="6fec7-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="6fec7-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6fec7-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="6fec7-110">Invoke</span></span>](#invoke) | <span data-ttu-id="6fec7-111">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6fec7-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="6fec7-112">Use la propiedad cursor para obtener el nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="6fec7-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="6fec7-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="6fec7-113">Members</span></span>

#### <span data-ttu-id="6fec7-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="6fec7-114">Invoke</span></span> 

<span data-ttu-id="6fec7-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6fec7-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6fec7-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="6fec7-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="6fec7-117">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="6fec7-117">There are no event args and the args parameter will be null.</span></span>

