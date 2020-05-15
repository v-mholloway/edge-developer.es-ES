---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: cd60598e220f4cf474a288a5120b7e75c2b5f0a3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655481"
---
# <span data-ttu-id="2292c-104">interfaz ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2292c-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="2292c-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="2292c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="2292c-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="2292c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2292c-107">Argumentos de evento para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="2292c-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="2292c-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="2292c-108">Summary</span></span>

 <span data-ttu-id="2292c-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="2292c-109">Members</span></span>                        | <span data-ttu-id="2292c-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="2292c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2292c-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="2292c-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="2292c-112">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="2292c-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="2292c-113">get_Handled</span><span class="sxs-lookup"><span data-stu-id="2292c-113">get_Handled</span></span>](#get_handled) | <span data-ttu-id="2292c-114">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="2292c-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="2292c-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="2292c-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="2292c-116">Establecer la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="2292c-116">Set the Handled property.</span></span>

## <span data-ttu-id="2292c-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="2292c-117">Members</span></span>

#### <span data-ttu-id="2292c-118">get_Reason</span><span class="sxs-lookup"><span data-stu-id="2292c-118">get_Reason</span></span> 

<span data-ttu-id="2292c-119">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="2292c-119">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="2292c-120">[get_Reason](#get_reason)de HRESULT público (valor CORE_WEBVIEW2_MOVE_FOCUS_REASON \*)</span><span class="sxs-lookup"><span data-stu-id="2292c-120">public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="2292c-121">get_Handled</span><span class="sxs-lookup"><span data-stu-id="2292c-121">get_Handled</span></span> 

<span data-ttu-id="2292c-122">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="2292c-122">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="2292c-123">[get_Handled](#get_handled)de HRESULT público (bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="2292c-123">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="2292c-124">Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE.</span><span class="sxs-lookup"><span data-stu-id="2292c-124">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="2292c-125">Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2292c-125">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="2292c-126">La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="2292c-126">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="2292c-127">Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="2292c-127">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="2292c-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="2292c-128">put_Handled</span></span> 

<span data-ttu-id="2292c-129">Establecer la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="2292c-129">Set the Handled property.</span></span>

> <span data-ttu-id="2292c-130">[put_Handled](#put_handled)de HRESULT público (valor bool)</span><span class="sxs-lookup"><span data-stu-id="2292c-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

