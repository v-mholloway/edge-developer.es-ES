---
description: Objeto distribuido de un evento de foco que contiene la causa y la ubicación de navegación.
title: Objeto FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 88f0a4ef8834c6e851f81ee10bf4202a0429f969
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752167"
---
# <span data-ttu-id="e6f83-104">Objeto FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="e6f83-104">FocusNavigationEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="e6f83-105">El objeto distribuido de [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) que contiene la [**NavigationReason**](#navigationreason) y la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e6f83-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span>  

## <span data-ttu-id="e6f83-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="e6f83-106">Methods</span></span>  

### <span data-ttu-id="e6f83-107">requestFocus</span><span class="sxs-lookup"><span data-stu-id="e6f83-107">requestFocus</span></span>  

<span data-ttu-id="e6f83-108">Se llama para mover el foco de la aplicación a la vista de.</span><span class="sxs-lookup"><span data-stu-id="e6f83-108">Called to move focus from the app to the webview.</span></span>  

### <span data-ttu-id="e6f83-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="e6f83-109">Parameters</span></span>  

<span data-ttu-id="e6f83-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e6f83-110">This method does not have parameters.</span></span>  

### <span data-ttu-id="e6f83-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6f83-111">Return value</span></span>  

<span data-ttu-id="e6f83-112">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e6f83-112">This method does not return a value.</span></span>  

## <span data-ttu-id="e6f83-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6f83-113">Properties</span></span>  

### <span data-ttu-id="e6f83-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="e6f83-114">navigationReason</span></span>  

<span data-ttu-id="e6f83-115">Tipo enumerado **NavigationReason**, ya sea "left", "up", "Right" o "Down".</span><span class="sxs-lookup"><span data-stu-id="e6f83-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span>  

<span data-ttu-id="e6f83-116">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6f83-116">This property is read-only.</span></span>  

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### <span data-ttu-id="e6f83-117">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6f83-117">Property value</span></span>  

<span data-ttu-id="e6f83-118">Escriba: **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="e6f83-118">Type: **NavigationReason**</span></span>  

### <span data-ttu-id="e6f83-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="e6f83-119">originHeight</span></span>  

<span data-ttu-id="e6f83-120">La ubicación de origen del elemento al que se va a asignar el foco.</span><span class="sxs-lookup"><span data-stu-id="e6f83-120">The origin height location of the element to be given focus.</span></span>  

<span data-ttu-id="e6f83-121">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6f83-121">This property is read-only.</span></span>  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### <span data-ttu-id="e6f83-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6f83-122">Property value</span></span>  

<span data-ttu-id="e6f83-123">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e6f83-123">Type: **float**</span></span>  

### <span data-ttu-id="e6f83-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="e6f83-124">originLeft</span></span>  

<span data-ttu-id="e6f83-125">Origen izquierdo del elemento al que se va a asignar el foco.</span><span class="sxs-lookup"><span data-stu-id="e6f83-125">The origin left location of the element to be given focus.</span></span>  

<span data-ttu-id="e6f83-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6f83-126">This property is read-only.</span></span>  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### <span data-ttu-id="e6f83-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6f83-127">Property value</span></span>  

<span data-ttu-id="e6f83-128">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e6f83-128">Type: **float**</span></span>  

### <span data-ttu-id="e6f83-129">originTop</span><span class="sxs-lookup"><span data-stu-id="e6f83-129">originTop</span></span>  

<span data-ttu-id="e6f83-130">Ubicación de origen superior del elemento al que se va a asignar el foco.</span><span class="sxs-lookup"><span data-stu-id="e6f83-130">The origin top location of the element to be given focus.</span></span>  

<span data-ttu-id="e6f83-131">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6f83-131">This property is read-only.</span></span>  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### <span data-ttu-id="e6f83-132">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6f83-132">Property value</span></span>  

<span data-ttu-id="e6f83-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e6f83-133">Type: **float**</span></span>  

### <span data-ttu-id="e6f83-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="e6f83-134">originWidth</span></span>  

<span data-ttu-id="e6f83-135">La ubicación del ancho de origen del elemento al que se va a asignar el foco.</span><span class="sxs-lookup"><span data-stu-id="e6f83-135">The origin width location of the element to be given focus.</span></span>  

<span data-ttu-id="e6f83-136">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e6f83-136">This property is read-only.</span></span>  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### <span data-ttu-id="e6f83-137">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e6f83-137">Property value</span></span>  

<span data-ttu-id="e6f83-138">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="e6f83-138">Type: **float**</span></span>  
