---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: cbcac385546c44e776ed48b8ae4d3ab754b614e0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885896"
---
# <span data-ttu-id="7608e-104">0.8.355: IWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7608e-104">0.8.355 - interface IWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="7608e-105">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="7608e-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="7608e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="7608e-106">Summary</span></span>

 <span data-ttu-id="7608e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7608e-107">Members</span></span>                        | <span data-ttu-id="7608e-108">Descripciones</span><span class="sxs-lookup"><span data-stu-id="7608e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7608e-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7608e-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="7608e-110">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7608e-110">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="7608e-111">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="7608e-111">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="7608e-112">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7608e-112">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="7608e-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="7608e-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="7608e-114">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="7608e-114">Gets the new window.</span></span>
[<span data-ttu-id="7608e-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="7608e-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="7608e-116">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="7608e-116">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="7608e-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="7608e-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="7608e-118">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="7608e-118">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="7608e-119">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7608e-119">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="7608e-120">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="7608e-120">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="7608e-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7608e-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="7608e-122">Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="7608e-122">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="7608e-123">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () etc.).</span><span class="sxs-lookup"><span data-stu-id="7608e-123">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="7608e-124">Miembros</span><span class="sxs-lookup"><span data-stu-id="7608e-124">Members</span></span>

#### <span data-ttu-id="7608e-125">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7608e-125">get_Uri</span></span> 

<span data-ttu-id="7608e-126">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7608e-126">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="7608e-127">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="7608e-127">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="7608e-128">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="7608e-128">put_NewWindow</span></span> 

<span data-ttu-id="7608e-129">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7608e-129">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="7608e-130">[put_NewWindow](#put_newwindow)(HRESULT) público ([IWebView2WebView](IWebView2WebView.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="7608e-130">public HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* newWindow)</span></span>

<span data-ttu-id="7608e-131">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="7608e-131">The target webview should not be navigated.</span></span> <span data-ttu-id="7608e-132">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="7608e-132">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="7608e-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="7608e-133">get_NewWindow</span></span> 

<span data-ttu-id="7608e-134">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="7608e-134">Gets the new window.</span></span>

> <span data-ttu-id="7608e-135">[get_NewWindow](#get_newwindow)de HRESULT público ([IWebView2WebView](IWebView2WebView.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="7608e-135">public HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="7608e-136">put_Handled</span><span class="sxs-lookup"><span data-stu-id="7608e-136">put_Handled</span></span> 

<span data-ttu-id="7608e-137">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="7608e-137">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="7608e-138">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="7608e-138">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="7608e-139">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="7608e-139">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="7608e-140">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="7608e-140">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="7608e-141">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="7608e-141">Default is false.</span></span>

#### <span data-ttu-id="7608e-142">get_Handled</span><span class="sxs-lookup"><span data-stu-id="7608e-142">get_Handled</span></span> 

<span data-ttu-id="7608e-143">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="7608e-143">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="7608e-144">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="7608e-144">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="7608e-145">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7608e-145">get_IsUserInitiated</span></span> 

<span data-ttu-id="7608e-146">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="7608e-146">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="7608e-147">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="7608e-147">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="7608e-148">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7608e-148">GetDeferral</span></span> 

<span data-ttu-id="7608e-149">Obtén un objeto [IWebView2Deferral](IWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="7608e-149">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="7608e-150">[GETDEFERRAL](#getdeferral)HRESULT ([IWebView2Deferral](IWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="7608e-150">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="7608e-151">Puedes usar el objeto [IWebView2Deferral](IWebView2Deferral.md) para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="7608e-151">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="7608e-152">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="7608e-152">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

