---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 5d8d447bced6bbbb51ae33220e74ebcf47f11ce5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885930"
---
# <span data-ttu-id="a8e18-104">0.8.355: IWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a8e18-104">0.8.355 - interface IWebView2MoveFocusRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="a8e18-105">Argumentos de evento para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="a8e18-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="a8e18-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="a8e18-106">Summary</span></span>

 <span data-ttu-id="a8e18-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8e18-107">Members</span></span>                        | <span data-ttu-id="a8e18-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="a8e18-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a8e18-109">get_Reason</span><span class="sxs-lookup"><span data-stu-id="a8e18-109">get_Reason</span></span>](#get_reason) | <span data-ttu-id="a8e18-110">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="a8e18-110">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="a8e18-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a8e18-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="a8e18-112">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="a8e18-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="a8e18-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a8e18-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="a8e18-114">Establecer la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="a8e18-114">Set the Handled property.</span></span>

## <span data-ttu-id="a8e18-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8e18-115">Members</span></span>

#### <span data-ttu-id="a8e18-116">get_Reason</span><span class="sxs-lookup"><span data-stu-id="a8e18-116">get_Reason</span></span> 

<span data-ttu-id="a8e18-117">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="a8e18-117">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="a8e18-118">[get_Reason](#get_reason)de HRESULT público (valor WEBVIEW2_MOVE_FOCUS_REASON \*)</span><span class="sxs-lookup"><span data-stu-id="a8e18-118">public HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="a8e18-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a8e18-119">get_Handled</span></span> 

<span data-ttu-id="a8e18-120">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="a8e18-120">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="a8e18-121">[get_Handled](#get_handled)de HRESULT público (bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="a8e18-121">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="a8e18-122">Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE.</span><span class="sxs-lookup"><span data-stu-id="a8e18-122">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="a8e18-123">Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a8e18-123">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="a8e18-124">La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="a8e18-124">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="a8e18-125">Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="a8e18-125">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="a8e18-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a8e18-126">put_Handled</span></span> 

<span data-ttu-id="a8e18-127">Establecer la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="a8e18-127">Set the Handled property.</span></span>

> <span data-ttu-id="a8e18-128">[put_Handled](#put_handled)de HRESULT público (valor bool)</span><span class="sxs-lookup"><span data-stu-id="a8e18-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

