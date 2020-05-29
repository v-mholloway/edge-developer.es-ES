---
description: Objeto distribuido de un evento de foco que contiene la causa y la ubicación de navegación.
title: Objeto FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: b988bcd7ff252b9972bef9a31339a34b4b58d9ee
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573378"
---
# <span data-ttu-id="e8c96-104">Objeto FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="e8c96-104">FocusNavigationEvent object</span></span>

<span data-ttu-id="e8c96-105">El objeto distribuido de [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) que contiene la [**NavigationReason**](#navigationreason) y la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e8c96-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span> 

## <span data-ttu-id="e8c96-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e8c96-106">Methods</span></span>

### <span data-ttu-id="e8c96-107">requestFocus</span><span class="sxs-lookup"><span data-stu-id="e8c96-107">requestFocus</span></span>

<span data-ttu-id="e8c96-108">Se llama para mover el foco de la aplicación a la vista de.</span><span class="sxs-lookup"><span data-stu-id="e8c96-108">Called to move focus from the app to the webview.</span></span>

### <span data-ttu-id="e8c96-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="e8c96-109">Parameters</span></span>

<span data-ttu-id="e8c96-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e8c96-110">This method does not have parameters.</span></span>

### <span data-ttu-id="e8c96-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8c96-111">Return value</span></span>

<span data-ttu-id="e8c96-112">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e8c96-112">This method does not return a value.</span></span>

## <span data-ttu-id="e8c96-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8c96-113">Properties</span></span>
    
### <span data-ttu-id="e8c96-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="e8c96-114">navigationReason</span></span>

<span data-ttu-id="e8c96-115">Tipo enumerado **NavigationReason**, ya sea "left", "up", "Right" o "Down".</span><span class="sxs-lookup"><span data-stu-id="e8c96-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span> 

<span data-ttu-id="e8c96-116">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8c96-116">This property is read-only.</span></span>

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### <span data-ttu-id="e8c96-117">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8c96-117">Property value</span></span>
<span data-ttu-id="e8c96-118">Escriba: **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="e8c96-118">Type: **NavigationReason**</span></span>

### <span data-ttu-id="e8c96-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="e8c96-119">originHeight</span></span>

<span data-ttu-id="e8c96-120">La ubicación de origen del elemento al que se va a asignar el foco.</span><span class="sxs-lookup"><span data-stu-id="e8c96-120">The origin height location of the element to be given focus.</span></span>

<span data-ttu-id="e8c96-121">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8c96-121">This property is read-only.</span></span>

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### <span data-ttu-id="e8c96-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8c96-122">Property value</span></span>
<span data-ttu-id="e8c96-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e8c96-123">Type: **float**</span></span>

### <span data-ttu-id="e8c96-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="e8c96-124">originLeft</span></span>

<span data-ttu-id="e8c96-125">Origen izquierdo del elemento al que se va a asignar el foco.</span><span class="sxs-lookup"><span data-stu-id="e8c96-125">The origin left location of the element to be given focus.</span></span>

<span data-ttu-id="e8c96-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8c96-126">This property is read-only.</span></span>

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### <span data-ttu-id="e8c96-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8c96-127">Property value</span></span>
<span data-ttu-id="e8c96-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e8c96-128">Type: **float**</span></span>

### <span data-ttu-id="e8c96-129">originTop</span><span class="sxs-lookup"><span data-stu-id="e8c96-129">originTop</span></span>

<span data-ttu-id="e8c96-130">Ubicación de origen superior del elemento al que se va a asignar el foco.</span><span class="sxs-lookup"><span data-stu-id="e8c96-130">The origin top location of the element to be given focus.</span></span>

<span data-ttu-id="e8c96-131">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8c96-131">This property is read-only.</span></span>

```js
var originTop = FocusNavigationEvent.originTop;
```

#### <span data-ttu-id="e8c96-132">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8c96-132">Property value</span></span>
<span data-ttu-id="e8c96-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e8c96-133">Type: **float**</span></span>

### <span data-ttu-id="e8c96-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="e8c96-134">originWidth</span></span>

<span data-ttu-id="e8c96-135">La ubicación del ancho de origen del elemento al que se va a asignar el foco.</span><span class="sxs-lookup"><span data-stu-id="e8c96-135">The origin width location of the element to be given focus.</span></span>

<span data-ttu-id="e8c96-136">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8c96-136">This property is read-only.</span></span>

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### <span data-ttu-id="e8c96-137">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8c96-137">Property value</span></span>
<span data-ttu-id="e8c96-138">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e8c96-138">Type: **float**</span></span>

