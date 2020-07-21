---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: d18ccc91d16213cf0a915420b406b65823b3f9d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886454"
---
# <span data-ttu-id="ac95b-104">interfaz ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ac95b-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="ac95b-105">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="ac95b-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="ac95b-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="ac95b-106">Summary</span></span>

 <span data-ttu-id="ac95b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac95b-107">Members</span></span>                        | <span data-ttu-id="ac95b-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ac95b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac95b-109">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="ac95b-109">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="ac95b-110">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="ac95b-110">Window features specified by the window.open call.</span></span>

<span data-ttu-id="ac95b-111">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="ac95b-111">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="ac95b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac95b-112">Members</span></span>

#### <span data-ttu-id="ac95b-113">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="ac95b-113">get_WindowFeatures</span></span> 

<span data-ttu-id="ac95b-114">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="ac95b-114">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="ac95b-115">[get_WindowFeatures](#get_windowfeatures)(HRESULT) público ([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="ac95b-115">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="ac95b-116">Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.</span><span class="sxs-lookup"><span data-stu-id="ac95b-116">These features can be considered for positioning and sizing of new webview windows.</span></span>

