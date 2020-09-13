---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalCursorChangedEventHandler
ms.openlocfilehash: 246fc6d23a003a346a20055fbf083421a6fb1b26
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012665"
---
# <span data-ttu-id="382c1-104">interfaz ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="382c1-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="382c1-105">La persona que llama implementa esta interfaz para recibir eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="382c1-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="382c1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="382c1-106">Summary</span></span>

 <span data-ttu-id="382c1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="382c1-107">Members</span></span>                        | <span data-ttu-id="382c1-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="382c1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="382c1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="382c1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="382c1-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="382c1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="382c1-111">Use la propiedad cursor para obtener el nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="382c1-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="382c1-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="382c1-112">Members</span></span>

#### <span data-ttu-id="382c1-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="382c1-113">Invoke</span></span> 

<span data-ttu-id="382c1-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="382c1-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="382c1-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="382c1-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="382c1-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="382c1-116">There are no event args and the args parameter will be null.</span></span>
