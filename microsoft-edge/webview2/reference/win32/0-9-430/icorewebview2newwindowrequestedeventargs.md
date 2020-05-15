---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 2ea3500c5e230b543f75241c47c58163276942da
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655309"
---
# <span data-ttu-id="038dc-104">interfaz ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="038dc-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="038dc-105">Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="038dc-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="038dc-106">Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.</span><span class="sxs-lookup"><span data-stu-id="038dc-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="038dc-107">Argumentos de evento para el evento NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="038dc-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="038dc-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="038dc-108">Summary</span></span>

 <span data-ttu-id="038dc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="038dc-109">Members</span></span>                        | <span data-ttu-id="038dc-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="038dc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="038dc-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="038dc-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="038dc-112">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="038dc-112">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="038dc-113">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="038dc-113">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="038dc-114">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="038dc-114">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="038dc-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="038dc-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="038dc-116">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="038dc-116">Gets the new window.</span></span>
[<span data-ttu-id="038dc-117">put_Handled</span><span class="sxs-lookup"><span data-stu-id="038dc-117">put_Handled</span></span>](#put_handled) | <span data-ttu-id="038dc-118">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="038dc-118">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="038dc-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="038dc-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="038dc-120">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="038dc-120">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="038dc-121">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="038dc-121">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="038dc-122">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="038dc-122">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="038dc-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="038dc-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="038dc-124">Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="038dc-124">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="038dc-125">El evento se desencadena cuando el contenido de la vista previa solicita a un abrir una nueva ventana (a través de window. Open () etc.).</span><span class="sxs-lookup"><span data-stu-id="038dc-125">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="038dc-126">Miembros</span><span class="sxs-lookup"><span data-stu-id="038dc-126">Members</span></span>

#### <span data-ttu-id="038dc-127">get_Uri</span><span class="sxs-lookup"><span data-stu-id="038dc-127">get_Uri</span></span> 

<span data-ttu-id="038dc-128">El URI de destino de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="038dc-128">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="038dc-129">[get_Uri](#get_uri)de HRESULT público (URI LPWStr \*)</span><span class="sxs-lookup"><span data-stu-id="038dc-129">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="038dc-130">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="038dc-130">put_NewWindow</span></span> 

<span data-ttu-id="038dc-131">Establece una vista previa como resultado de la NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="038dc-131">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="038dc-132">[put_NewWindow](#put_newwindow)(HRESULT) público ([ICoreWebView2](ICoreWebView2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="038dc-132">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="038dc-133">No se debe navegar por la WebView de destino.</span><span class="sxs-lookup"><span data-stu-id="038dc-133">The target webview should not be navigated.</span></span> <span data-ttu-id="038dc-134">Si se establece NewWindow, la ventana de nivel superior volverá como la WindowProxy abierta.</span><span class="sxs-lookup"><span data-stu-id="038dc-134">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="038dc-135">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="038dc-135">get_NewWindow</span></span> 

<span data-ttu-id="038dc-136">Obtiene la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="038dc-136">Gets the new window.</span></span>

> <span data-ttu-id="038dc-137">[get_NewWindow](#get_newwindow)de HRESULT público ([ICoreWebView2](ICoreWebView2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="038dc-137">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="038dc-138">put_Handled</span><span class="sxs-lookup"><span data-stu-id="038dc-138">put_Handled</span></span> 

<span data-ttu-id="038dc-139">Establece si el NewWindowRequestedEvent es manejado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="038dc-139">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="038dc-140">[put_Handled](#put_handled)de HRESULT público (bool controlado)</span><span class="sxs-lookup"><span data-stu-id="038dc-140">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="038dc-141">Si es falso y no se establece NewWindow, WebView abrirá una ventana emergente y se devolverá como WindowProxy abierto.</span><span class="sxs-lookup"><span data-stu-id="038dc-141">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="038dc-142">Si se establece en true y no se establece NewWindow para una Window. Open Call, el WindowProxy abierto será para un objeto de ventana ficticio y no se cargará ninguna ventana.</span><span class="sxs-lookup"><span data-stu-id="038dc-142">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="038dc-143">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="038dc-143">Default is false.</span></span>

#### <span data-ttu-id="038dc-144">get_Handled</span><span class="sxs-lookup"><span data-stu-id="038dc-144">get_Handled</span></span> 

<span data-ttu-id="038dc-145">Obtiene si el NewWindowRequestedEvent es controlado por el hospedador.</span><span class="sxs-lookup"><span data-stu-id="038dc-145">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="038dc-146">[get_Handled](#get_handled)de HRESULT público (bool \* Handled)</span><span class="sxs-lookup"><span data-stu-id="038dc-146">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="038dc-147">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="038dc-147">get_IsUserInitiated</span></span> 

<span data-ttu-id="038dc-148">IsUserInitiated es verdadero cuando se inició la solicitud de la nueva ventana mediante un gesto de usuario, por ejemplo, haciendo clic en una etiqueta de delimitador con destino.</span><span class="sxs-lookup"><span data-stu-id="038dc-148">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="038dc-149">[get_IsUserInitiated](#get_isuserinitiated)de HRESULT público (bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="038dc-149">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="038dc-150">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="038dc-150">GetDeferral</span></span> 

<span data-ttu-id="038dc-151">Obtén un objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) y coloca el evento en un estado diferido.</span><span class="sxs-lookup"><span data-stu-id="038dc-151">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="038dc-152">[GETDEFERRAL](#getdeferral)HRESULT ([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* aplazamiento)</span><span class="sxs-lookup"><span data-stu-id="038dc-152">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="038dc-153">Puedes usar el objeto [ICoreWebView2Deferral](ICoreWebView2Deferral.md) para completar la solicitud de apertura de ventana más adelante.</span><span class="sxs-lookup"><span data-stu-id="038dc-153">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="038dc-154">Mientras se difiere este evento, se devolverá la ventana de apertura de WindowProxy a una ventana no navegada, que se desplazará cuando se complete el aplazamiento.</span><span class="sxs-lookup"><span data-stu-id="038dc-154">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

