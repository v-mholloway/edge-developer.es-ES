---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 855425e5cbdd594c7a4bca12efe1827035ca2f3a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011107"
---
# <span data-ttu-id="5cc01-104">0.9.579: ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5cc01-104">0.9.579 - interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="5cc01-105">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="5cc01-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="5cc01-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="5cc01-106">Summary</span></span>

 <span data-ttu-id="5cc01-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5cc01-107">Members</span></span>                        | <span data-ttu-id="5cc01-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="5cc01-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5cc01-109">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="5cc01-109">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="5cc01-110">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="5cc01-110">Window features specified by the window.open call.</span></span>

<span data-ttu-id="5cc01-111">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="5cc01-111">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="5cc01-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5cc01-112">Members</span></span>

#### <span data-ttu-id="5cc01-113">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="5cc01-113">get_WindowFeatures</span></span> 

<span data-ttu-id="5cc01-114">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="5cc01-114">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="5cc01-115">[get_WindowFeatures](#get_windowfeatures)(HRESULT) público ([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="5cc01-115">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="5cc01-116">Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.</span><span class="sxs-lookup"><span data-stu-id="5cc01-116">These features can be considered for positioning and sizing of new webview windows.</span></span>

