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
ms.openlocfilehash: 1d91bb767045179a5d8de3700f86ff6d92a9ef36
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699473"
---
# <span data-ttu-id="311ba-104">interfaz ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="311ba-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="311ba-105">Esta es una API experimental que se incluye con nuestra versión preliminar SDK versión 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="311ba-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="311ba-106">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="311ba-106">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="311ba-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="311ba-107">Summary</span></span>

 <span data-ttu-id="311ba-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="311ba-108">Members</span></span>                        | <span data-ttu-id="311ba-109">Descripciones</span><span class="sxs-lookup"><span data-stu-id="311ba-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="311ba-110">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="311ba-110">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="311ba-111">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="311ba-111">Window features specified by the window.open call.</span></span>

<span data-ttu-id="311ba-112">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () y así sucesivamente).</span><span class="sxs-lookup"><span data-stu-id="311ba-112">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="311ba-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="311ba-113">Members</span></span>

#### <span data-ttu-id="311ba-114">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="311ba-114">get_WindowFeatures</span></span> 

<span data-ttu-id="311ba-115">Características de la ventana especificadas por la llamada Window. Open.</span><span class="sxs-lookup"><span data-stu-id="311ba-115">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="311ba-116">[get_WindowFeatures](#get_windowfeatures)(HRESULT) público ([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="311ba-116">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="311ba-117">Estas características se pueden considerar para posicionar y cambiar el tamaño de nuevas ventanas de WebView.</span><span class="sxs-lookup"><span data-stu-id="311ba-117">These features can be considered for positioning and sizing of new webview windows.</span></span>

