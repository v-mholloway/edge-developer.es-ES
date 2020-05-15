---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 8ca8de3c430eda3bde089ca53501d880f4d8e35e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655297"
---
# <span data-ttu-id="89886-104">interfaz ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="89886-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="89886-105">Argumentos de evento para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="89886-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="89886-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="89886-106">Summary</span></span>

 <span data-ttu-id="89886-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="89886-107">Members</span></span>                        | <span data-ttu-id="89886-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="89886-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="89886-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="89886-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="89886-110">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="89886-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="89886-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="89886-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="89886-112">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="89886-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="89886-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="89886-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="89886-114">Establecer la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="89886-114">Set the Handled property.</span></span>

## <span data-ttu-id="89886-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="89886-115">Members</span></span>

#### <span data-ttu-id="89886-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="89886-116">get_Handled</span></span> 

<span data-ttu-id="89886-117">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="89886-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="89886-118">[get_Handled](#get_handled)de HRESULT público (bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="89886-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="89886-119">Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE.</span><span class="sxs-lookup"><span data-stu-id="89886-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="89886-120">Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="89886-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="89886-121">La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="89886-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="89886-122">Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="89886-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="89886-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="89886-123">get_Reason</span></span> 

<span data-ttu-id="89886-124">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="89886-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="89886-125">[get_Reason](#get_reason)de HRESULT público (valor COREWEBVIEW2_MOVE_FOCUS_REASON \*)</span><span class="sxs-lookup"><span data-stu-id="89886-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="89886-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="89886-126">put_Handled</span></span> 

<span data-ttu-id="89886-127">Establecer la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="89886-127">Set the Handled property.</span></span>

> <span data-ttu-id="89886-128">[put_Handled](#put_handled)de HRESULT público (valor bool)</span><span class="sxs-lookup"><span data-stu-id="89886-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

