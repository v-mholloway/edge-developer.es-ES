---
description: Expone si la operación se completó correctamente o se produjo un error
title: Objeto MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: ebb89c0fc645ebcd97357af10af2be650d8218b9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573371"
---
# <span data-ttu-id="e9c42-104">Objeto MSWebViewAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="e9c42-104">MSWebViewAsyncOperation object</span></span>

<span data-ttu-id="e9c42-105">Expone si la operación se completó correctamente o falló.</span><span class="sxs-lookup"><span data-stu-id="e9c42-105">Exposes whether the operation completed successfully or failed.</span></span> 

## <span data-ttu-id="e9c42-106">Eventos</span><span class="sxs-lookup"><span data-stu-id="e9c42-106">Events</span></span>

### <span data-ttu-id="e9c42-107">completado</span><span class="sxs-lookup"><span data-stu-id="e9c42-107">complete</span></span>

<span data-ttu-id="e9c42-108">Indica que se completó la operación.</span><span class="sxs-lookup"><span data-stu-id="e9c42-108">Indicates that the operation completed.</span></span> 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### <span data-ttu-id="e9c42-109">Información del evento</span><span class="sxs-lookup"><span data-stu-id="e9c42-109">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="e9c42-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="e9c42-110">Interface</span></span>** | **<span data-ttu-id="e9c42-111">Evento</span><span class="sxs-lookup"><span data-stu-id="e9c42-111">Event</span></span>**
|**<span data-ttu-id="e9c42-112">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="e9c42-112">Synchronous</span></span>** |<span data-ttu-id="e9c42-113">Sí</span><span class="sxs-lookup"><span data-stu-id="e9c42-113">Yes</span></span> |    
|**<span data-ttu-id="e9c42-114">Pase</span><span class="sxs-lookup"><span data-stu-id="e9c42-114">Bubbles</span></span>**     |<span data-ttu-id="e9c42-115">No</span><span class="sxs-lookup"><span data-stu-id="e9c42-115">No</span></span> |   
|**<span data-ttu-id="e9c42-116">Cancelable</span><span class="sxs-lookup"><span data-stu-id="e9c42-116">Cancelable</span></span>**  |<span data-ttu-id="e9c42-117">No</span><span class="sxs-lookup"><span data-stu-id="e9c42-117">No</span></span> |        


### <span data-ttu-id="e9c42-118">error</span><span class="sxs-lookup"><span data-stu-id="e9c42-118">error</span></span>

<span data-ttu-id="e9c42-119">Indica que se ha producido un error con la operación.</span><span class="sxs-lookup"><span data-stu-id="e9c42-119">Indicates that there was an error with the operation.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### <span data-ttu-id="e9c42-120">Información del evento</span><span class="sxs-lookup"><span data-stu-id="e9c42-120">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="e9c42-121">Interfaz</span><span class="sxs-lookup"><span data-stu-id="e9c42-121">Interface</span></span>** | **<span data-ttu-id="e9c42-122">Evento</span><span class="sxs-lookup"><span data-stu-id="e9c42-122">Event</span></span>**
|**<span data-ttu-id="e9c42-123">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="e9c42-123">Synchronous</span></span>** |<span data-ttu-id="e9c42-124">Sí</span><span class="sxs-lookup"><span data-stu-id="e9c42-124">Yes</span></span> |    
|**<span data-ttu-id="e9c42-125">Pase</span><span class="sxs-lookup"><span data-stu-id="e9c42-125">Bubbles</span></span>**     |<span data-ttu-id="e9c42-126">No</span><span class="sxs-lookup"><span data-stu-id="e9c42-126">No</span></span> |   
|**<span data-ttu-id="e9c42-127">Cancelable</span><span class="sxs-lookup"><span data-stu-id="e9c42-127">Cancelable</span></span>**  |<span data-ttu-id="e9c42-128">No</span><span class="sxs-lookup"><span data-stu-id="e9c42-128">No</span></span> |            


## <span data-ttu-id="e9c42-129">Métodos</span><span class="sxs-lookup"><span data-stu-id="e9c42-129">Methods</span></span>

### <span data-ttu-id="e9c42-130">start</span><span class="sxs-lookup"><span data-stu-id="e9c42-130">start</span></span>

<span data-ttu-id="e9c42-131">Se llama para iniciar la tarea asincrónica.</span><span class="sxs-lookup"><span data-stu-id="e9c42-131">Called to start the async task.</span></span> 

```js
MSWebViewAsyncOperation.start();
```

### <span data-ttu-id="e9c42-132">Parameters</span><span class="sxs-lookup"><span data-stu-id="e9c42-132">Parameters</span></span>

<span data-ttu-id="e9c42-133">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e9c42-133">This method does not have parameters.</span></span>

### <span data-ttu-id="e9c42-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9c42-134">Return value</span></span>

<span data-ttu-id="e9c42-135">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="e9c42-135">This method does not return a value.</span></span>

## <span data-ttu-id="e9c42-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9c42-136">Properties</span></span>

### <span data-ttu-id="e9c42-137">error</span><span class="sxs-lookup"><span data-stu-id="e9c42-137">error</span></span>

<span data-ttu-id="e9c42-138">El error que se produjo.</span><span class="sxs-lookup"><span data-stu-id="e9c42-138">The error that occured.</span></span>

<span data-ttu-id="e9c42-139">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9c42-139">This property is read-only.</span></span>

```js
var error = MSWebViewAsyncOperation.error;
```

#### <span data-ttu-id="e9c42-140">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e9c42-140">Property value</span></span>
<span data-ttu-id="e9c42-141">Escriba: **DOMError**</span><span class="sxs-lookup"><span data-stu-id="e9c42-141">Type: **DOMError**</span></span>

### <span data-ttu-id="e9c42-142">finalizar</span><span class="sxs-lookup"><span data-stu-id="e9c42-142">oncomplete</span></span>

<span data-ttu-id="e9c42-143">El controlador de eventos **completo** .</span><span class="sxs-lookup"><span data-stu-id="e9c42-143">The **complete** event handler.</span></span> 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### <span data-ttu-id="e9c42-144">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e9c42-144">Property value</span></span>
<span data-ttu-id="e9c42-145">Escriba: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="e9c42-145">Type: **EventHandler**</span></span>

### <span data-ttu-id="e9c42-146">OnError</span><span class="sxs-lookup"><span data-stu-id="e9c42-146">onerror</span></span>

<span data-ttu-id="e9c42-147">El controlador de eventos de **error** .</span><span class="sxs-lookup"><span data-stu-id="e9c42-147">The **error** event handler.</span></span> 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### <span data-ttu-id="e9c42-148">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e9c42-148">Property value</span></span>
<span data-ttu-id="e9c42-149">Escriba: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="e9c42-149">Type: **EventHandler**</span></span>

### <span data-ttu-id="e9c42-150">readyState</span><span class="sxs-lookup"><span data-stu-id="e9c42-150">readyState</span></span>

<span data-ttu-id="e9c42-151">Describe el estado de lista del objeto.</span><span class="sxs-lookup"><span data-stu-id="e9c42-151">Describes the ready state of the object.</span></span>

<span data-ttu-id="e9c42-152">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9c42-152">This property is read-only.</span></span>

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### <span data-ttu-id="e9c42-153">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e9c42-153">Property value</span></span>
<span data-ttu-id="e9c42-154">Tipo: **corto sin signo**</span><span class="sxs-lookup"><span data-stu-id="e9c42-154">Type: **unsigned short**</span></span>

### <span data-ttu-id="e9c42-155">resultado</span><span class="sxs-lookup"><span data-stu-id="e9c42-155">result</span></span>

<span data-ttu-id="e9c42-156">Resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e9c42-156">The result of the operation.</span></span>

<span data-ttu-id="e9c42-157">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9c42-157">This property is read-only.</span></span>

```js
var result = MSWebViewAsyncOperation.result;
```

#### <span data-ttu-id="e9c42-158">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e9c42-158">Property value</span></span>
<span data-ttu-id="e9c42-159">Escriba lo siguiente: cualquiera</span><span class="sxs-lookup"><span data-stu-id="e9c42-159">Type: any</span></span>

### <span data-ttu-id="e9c42-160">target</span><span class="sxs-lookup"><span data-stu-id="e9c42-160">target</span></span>

<span data-ttu-id="e9c42-161">El destino de la operación.</span><span class="sxs-lookup"><span data-stu-id="e9c42-161">The target of the operation.</span></span> 

<span data-ttu-id="e9c42-162">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9c42-162">This property is read-only.</span></span>

```js
var target = MSWebViewAsyncOperation.target;
```

#### <span data-ttu-id="e9c42-163">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e9c42-163">Property value</span></span>
<span data-ttu-id="e9c42-164">Escriba: [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="e9c42-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>

### <span data-ttu-id="e9c42-165">tipo</span><span class="sxs-lookup"><span data-stu-id="e9c42-165">type</span></span>

<span data-ttu-id="e9c42-166">El tipo de la operación.</span><span class="sxs-lookup"><span data-stu-id="e9c42-166">The type of the operation.</span></span>

<span data-ttu-id="e9c42-167">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9c42-167">This property is read-only.</span></span>

```js
var type = MSWebViewAsyncOperation.type;
```

#### <span data-ttu-id="e9c42-168">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e9c42-168">Property value</span></span>
<span data-ttu-id="e9c42-169">Tipo: **corto sin signo**</span><span class="sxs-lookup"><span data-stu-id="e9c42-169">Type: **unsigned short**</span></span>
