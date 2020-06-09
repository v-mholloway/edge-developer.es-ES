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
ms.openlocfilehash: de0319060b6e618c30fc685815bcbcc41e8c3005
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697850"
---
# <span data-ttu-id="29d2e-104">interfaz ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="29d2e-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="29d2e-105">Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="29d2e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="29d2e-106">Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.</span><span class="sxs-lookup"><span data-stu-id="29d2e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="29d2e-107">Argumentos de evento para el evento MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="29d2e-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="29d2e-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="29d2e-108">Summary</span></span>

 <span data-ttu-id="29d2e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="29d2e-109">Members</span></span>                        | <span data-ttu-id="29d2e-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="29d2e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="29d2e-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="29d2e-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="29d2e-112">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="29d2e-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="29d2e-113">get_Reason</span><span class="sxs-lookup"><span data-stu-id="29d2e-113">get_Reason</span></span>](#get_reason) | <span data-ttu-id="29d2e-114">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="29d2e-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="29d2e-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="29d2e-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="29d2e-116">Establecer la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="29d2e-116">Set the Handled property.</span></span>

## <span data-ttu-id="29d2e-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="29d2e-117">Members</span></span>

#### <span data-ttu-id="29d2e-118">get_Handled</span><span class="sxs-lookup"><span data-stu-id="29d2e-118">get_Handled</span></span> 

<span data-ttu-id="29d2e-119">Indicar si la aplicación ha controlado el evento.</span><span class="sxs-lookup"><span data-stu-id="29d2e-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="29d2e-120">[get_Handled](#get_handled)de HRESULT público (bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="29d2e-120">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="29d2e-121">Si la aplicación ha movido el foco a la ubicación deseada, debe establecer la propiedad Handled en TRUE.</span><span class="sxs-lookup"><span data-stu-id="29d2e-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="29d2e-122">Cuando la propiedad Handled es false después de que el controlador de eventos devuelva, se realiza una acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="29d2e-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="29d2e-123">La acción predeterminada es intentar buscar la siguiente ventana secundaria de la pestaña detener en la aplicación e intentar mover el foco a esa ventana.</span><span class="sxs-lookup"><span data-stu-id="29d2e-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="29d2e-124">Si no hay ninguna otra ventana de este tipo para mover el foco, el foco se reactivará dentro del contenido Web de WebView.</span><span class="sxs-lookup"><span data-stu-id="29d2e-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="29d2e-125">get_Reason</span><span class="sxs-lookup"><span data-stu-id="29d2e-125">get_Reason</span></span> 

<span data-ttu-id="29d2e-126">El motivo de la vista en WebView para activar el evento solicitado MoveFocus.</span><span class="sxs-lookup"><span data-stu-id="29d2e-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="29d2e-127">[get_Reason](#get_reason)de HRESULT público (valor COREWEBVIEW2_MOVE_FOCUS_REASON \*)</span><span class="sxs-lookup"><span data-stu-id="29d2e-127">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="29d2e-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="29d2e-128">put_Handled</span></span> 

<span data-ttu-id="29d2e-129">Establecer la propiedad Handled.</span><span class="sxs-lookup"><span data-stu-id="29d2e-129">Set the Handled property.</span></span>

> <span data-ttu-id="29d2e-130">[put_Handled](#put_handled)de HRESULT público (valor bool)</span><span class="sxs-lookup"><span data-stu-id="29d2e-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

