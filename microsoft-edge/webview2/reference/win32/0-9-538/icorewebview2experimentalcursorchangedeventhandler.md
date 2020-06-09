---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b44bd47f5352179abcc06ef5fd5b8f613bde455e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699352"
---
# <span data-ttu-id="20049-104">interfaz ICoreWebView2ExperimentalCursorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="20049-104">interface ICoreWebView2ExperimentalCursorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="20049-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="20049-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="20049-106">La persona que llama implementa esta interfaz para recibir eventos CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="20049-106">The caller implements this interface to receive CursorChanged events.</span></span>

## <span data-ttu-id="20049-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="20049-107">Summary</span></span>

 <span data-ttu-id="20049-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="20049-108">Members</span></span>                        | <span data-ttu-id="20049-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="20049-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="20049-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="20049-110">Invoke</span></span>](#invoke) | <span data-ttu-id="20049-111">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="20049-111">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="20049-112">Use la propiedad cursor para obtener el nuevo cursor.</span><span class="sxs-lookup"><span data-stu-id="20049-112">Use the Cursor property to get the new cursor.</span></span>

## <span data-ttu-id="20049-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="20049-113">Members</span></span>

#### <span data-ttu-id="20049-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="20049-114">Invoke</span></span> 

<span data-ttu-id="20049-115">Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="20049-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="20049-116">invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* Sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="20049-116">public HRESULT [Invoke](#invoke)([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="20049-117">No hay argumentos de evento y el parámetro args será null.</span><span class="sxs-lookup"><span data-stu-id="20049-117">There are no event args and the args parameter will be null.</span></span>

