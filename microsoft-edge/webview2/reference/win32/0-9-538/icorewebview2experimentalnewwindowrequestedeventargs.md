---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 39d52b1231e767739b63b3759cdd08e4c9b26be3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879992"
---
# <span data-ttu-id="011d4-104">interfaz ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="011d4-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="011d4-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="011d4-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="011d4-106">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="011d4-106">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="011d4-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="011d4-107">Summary</span></span>

 <span data-ttu-id="011d4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="011d4-108">Members</span></span>                        | <span data-ttu-id="011d4-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="011d4-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="011d4-110">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="011d4-110">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="011d4-111">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="011d4-111">Window features specified by the window.open call.</span></span>

<span data-ttu-id="011d4-112">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="011d4-112">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="011d4-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="011d4-113">Members</span></span>

#### <span data-ttu-id="011d4-114">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="011d4-114">get_WindowFeatures</span></span> 

<span data-ttu-id="011d4-115">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="011d4-115">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="011d4-116">[get_WindowFeatures](#get_windowfeatures)(HRESULT) público ([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="011d4-116">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="011d4-117">Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.</span><span class="sxs-lookup"><span data-stu-id="011d4-117">These features can be considered for positioning and sizing of new webview windows.</span></span>

