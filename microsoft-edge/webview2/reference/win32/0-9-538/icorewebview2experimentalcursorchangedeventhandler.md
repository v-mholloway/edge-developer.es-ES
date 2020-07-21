---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: 67d0e6e05fb3640e141ec1ae7193746a1200bbd0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884886"
---
# <span data-ttu-id="fe495-104">interfaz ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fe495-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="fe495-105">La persona que llama implementa esta interfaz para recibir eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="fe495-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="fe495-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="fe495-106">Summary</span></span>

 <span data-ttu-id="fe495-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe495-107">Members</span></span>                        | <span data-ttu-id="fe495-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="fe495-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fe495-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fe495-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fe495-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fe495-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="fe495-111">Use la propiedad cursor para obtener el nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="fe495-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="fe495-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe495-112">Members</span></span>

#### <span data-ttu-id="fe495-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="fe495-113">Invoke</span></span> 

<span data-ttu-id="fe495-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="fe495-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fe495-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="fe495-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="fe495-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="fe495-116">There are no event args and the args parameter will be null.</span></span>

