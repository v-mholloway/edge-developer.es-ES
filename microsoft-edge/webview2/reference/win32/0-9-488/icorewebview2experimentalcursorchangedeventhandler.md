---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalCursorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: ee6de606d6ed8a9e00dbdacee9bb07b341a6d04e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886489"
---
# <span data-ttu-id="ee62d-104">0.9.515: ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ee62d-104">0.9.515 - interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ee62d-105">La persona que llama implementa esta interfaz para recibir eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="ee62d-105">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="ee62d-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ee62d-106">Summary</span></span>

 <span data-ttu-id="ee62d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee62d-107">Members</span></span>                        | <span data-ttu-id="ee62d-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ee62d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ee62d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ee62d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ee62d-110">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ee62d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ee62d-111">Use la propiedad cursor para obtener el nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="ee62d-111">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="ee62d-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee62d-112">Members</span></span>

#### <span data-ttu-id="ee62d-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="ee62d-113">Invoke</span></span> 

<span data-ttu-id="ee62d-114">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ee62d-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ee62d-115">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ee62d-115">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="ee62d-116">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="ee62d-116">There are no event args and the args parameter will be null.</span></span>

