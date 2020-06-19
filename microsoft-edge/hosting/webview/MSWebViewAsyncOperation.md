---
description: Expone si la operación se completó correctamente o se produjo un error
title: Objeto MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: d6e03af2a0205938f19120076aa0ad622539d7e5
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752131"
---
# <span data-ttu-id="050d8-104">Objeto MSWebViewAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="050d8-104">MSWebViewAsyncOperation object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="050d8-105">Expone si la operación se completó correctamente o falló.</span><span class="sxs-lookup"><span data-stu-id="050d8-105">Exposes whether the operation completed successfully or failed.</span></span>  

## <span data-ttu-id="050d8-106">Eventos</span><span class="sxs-lookup"><span data-stu-id="050d8-106">Events</span></span>  

### <span data-ttu-id="050d8-107">completado</span><span class="sxs-lookup"><span data-stu-id="050d8-107">complete</span></span>  

<span data-ttu-id="050d8-108">Indica que se completó la operación.</span><span class="sxs-lookup"><span data-stu-id="050d8-108">Indicates that the operation completed.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### <span data-ttu-id="050d8-109">Información del evento</span><span class="sxs-lookup"><span data-stu-id="050d8-109">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="050d8-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="050d8-110">Interface</span></span>** | **<span data-ttu-id="050d8-111">Evento</span><span class="sxs-lookup"><span data-stu-id="050d8-111">Event</span></span>** |  
| **<span data-ttu-id="050d8-112">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="050d8-112">Synchronous</span></span>** |<span data-ttu-id="050d8-113">Sí</span><span class="sxs-lookup"><span data-stu-id="050d8-113">Yes</span></span> |  
| **<span data-ttu-id="050d8-114">Pase</span><span class="sxs-lookup"><span data-stu-id="050d8-114">Bubbles</span></span>** |<span data-ttu-id="050d8-115">No</span><span class="sxs-lookup"><span data-stu-id="050d8-115">No</span></span> |   
| **<span data-ttu-id="050d8-116">Cancelable</span><span class="sxs-lookup"><span data-stu-id="050d8-116">Cancelable</span></span>** |<span data-ttu-id="050d8-117">No</span><span class="sxs-lookup"><span data-stu-id="050d8-117">No</span></span> |  

### <span data-ttu-id="050d8-118">error</span><span class="sxs-lookup"><span data-stu-id="050d8-118">error</span></span>  

<span data-ttu-id="050d8-119">Indica que se ha producido un error con la operación.</span><span class="sxs-lookup"><span data-stu-id="050d8-119">Indicates that there was an error with the operation.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### <span data-ttu-id="050d8-120">Información del evento</span><span class="sxs-lookup"><span data-stu-id="050d8-120">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="050d8-121">Interfaz</span><span class="sxs-lookup"><span data-stu-id="050d8-121">Interface</span></span>** | **<span data-ttu-id="050d8-122">Evento</span><span class="sxs-lookup"><span data-stu-id="050d8-122">Event</span></span>** |  
| **<span data-ttu-id="050d8-123">Sincrónico</span><span class="sxs-lookup"><span data-stu-id="050d8-123">Synchronous</span></span>** | <span data-ttu-id="050d8-124">Sí</span><span class="sxs-lookup"><span data-stu-id="050d8-124">Yes</span></span> |  
| **<span data-ttu-id="050d8-125">Pase</span><span class="sxs-lookup"><span data-stu-id="050d8-125">Bubbles</span></span>** | <span data-ttu-id="050d8-126">No</span><span class="sxs-lookup"><span data-stu-id="050d8-126">No</span></span> |  
| **<span data-ttu-id="050d8-127">Cancelable</span><span class="sxs-lookup"><span data-stu-id="050d8-127">Cancelable</span></span>** | <span data-ttu-id="050d8-128">No</span><span class="sxs-lookup"><span data-stu-id="050d8-128">No</span></span> |  

## <span data-ttu-id="050d8-129">Métodos</span><span class="sxs-lookup"><span data-stu-id="050d8-129">Methods</span></span>  

### <span data-ttu-id="050d8-130">start</span><span class="sxs-lookup"><span data-stu-id="050d8-130">start</span></span>  

<span data-ttu-id="050d8-131">Se llama para iniciar la tarea asincrónica.</span><span class="sxs-lookup"><span data-stu-id="050d8-131">Called to start the async task.</span></span>  

```javascript
MSWebViewAsyncOperation.start();
```  

### <span data-ttu-id="050d8-132">Parameters</span><span class="sxs-lookup"><span data-stu-id="050d8-132">Parameters</span></span>  

<span data-ttu-id="050d8-133">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="050d8-133">This method does not have parameters.</span></span>  

### <span data-ttu-id="050d8-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="050d8-134">Return value</span></span>  

<span data-ttu-id="050d8-135">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="050d8-135">This method does not return a value.</span></span>  

## <span data-ttu-id="050d8-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="050d8-136">Properties</span></span>  

### <span data-ttu-id="050d8-137">error</span><span class="sxs-lookup"><span data-stu-id="050d8-137">error</span></span>  

<span data-ttu-id="050d8-138">El error que se produjo.</span><span class="sxs-lookup"><span data-stu-id="050d8-138">The error that occurred.</span></span>  

<span data-ttu-id="050d8-139">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="050d8-139">This property is read-only.</span></span>  

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### <span data-ttu-id="050d8-140">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="050d8-140">Property value</span></span>  

<span data-ttu-id="050d8-141">Escriba: **DOMError**</span><span class="sxs-lookup"><span data-stu-id="050d8-141">Type: **DOMError**</span></span>  

### <span data-ttu-id="050d8-142">finalizar</span><span class="sxs-lookup"><span data-stu-id="050d8-142">oncomplete</span></span>  

<span data-ttu-id="050d8-143">El controlador de eventos **completo** .</span><span class="sxs-lookup"><span data-stu-id="050d8-143">The **complete** event handler.</span></span>  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### <span data-ttu-id="050d8-144">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="050d8-144">Property value</span></span>  

<span data-ttu-id="050d8-145">Escriba: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="050d8-145">Type: **EventHandler**</span></span>  

### <span data-ttu-id="050d8-146">OnError</span><span class="sxs-lookup"><span data-stu-id="050d8-146">onerror</span></span>  

<span data-ttu-id="050d8-147">El controlador de eventos de **error** .</span><span class="sxs-lookup"><span data-stu-id="050d8-147">The **error** event handler.</span></span>  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### <span data-ttu-id="050d8-148">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="050d8-148">Property value</span></span>  

<span data-ttu-id="050d8-149">Escriba: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="050d8-149">Type: **EventHandler**</span></span>  

### <span data-ttu-id="050d8-150">readyState</span><span class="sxs-lookup"><span data-stu-id="050d8-150">readyState</span></span>  

<span data-ttu-id="050d8-151">Describe el estado de lista del objeto.</span><span class="sxs-lookup"><span data-stu-id="050d8-151">Describes the ready state of the object.</span></span>  

<span data-ttu-id="050d8-152">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="050d8-152">This property is read-only.</span></span>  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### <span data-ttu-id="050d8-153">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="050d8-153">Property value</span></span>  

<span data-ttu-id="050d8-154">Tipo: **corto sin signo**</span><span class="sxs-lookup"><span data-stu-id="050d8-154">Type: **unsigned short**</span></span>  

### <span data-ttu-id="050d8-155">resultado</span><span class="sxs-lookup"><span data-stu-id="050d8-155">result</span></span>  

<span data-ttu-id="050d8-156">Resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="050d8-156">The result of the operation.</span></span>  

<span data-ttu-id="050d8-157">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="050d8-157">This property is read-only.</span></span>  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### <span data-ttu-id="050d8-158">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="050d8-158">Property value</span></span>  

<span data-ttu-id="050d8-159">Escriba lo siguiente: cualquiera</span><span class="sxs-lookup"><span data-stu-id="050d8-159">Type: any</span></span>  

### <span data-ttu-id="050d8-160">target</span><span class="sxs-lookup"><span data-stu-id="050d8-160">target</span></span>  

<span data-ttu-id="050d8-161">El destino de la operación.</span><span class="sxs-lookup"><span data-stu-id="050d8-161">The target of the operation.</span></span>  

<span data-ttu-id="050d8-162">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="050d8-162">This property is read-only.</span></span>  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### <span data-ttu-id="050d8-163">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="050d8-163">Property value</span></span>  

<span data-ttu-id="050d8-164">Escriba: [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="050d8-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>  

### <span data-ttu-id="050d8-165">tipo</span><span class="sxs-lookup"><span data-stu-id="050d8-165">type</span></span>  

<span data-ttu-id="050d8-166">El tipo de la operación.</span><span class="sxs-lookup"><span data-stu-id="050d8-166">The type of the operation.</span></span>  

<span data-ttu-id="050d8-167">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="050d8-167">This property is read-only.</span></span>  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### <span data-ttu-id="050d8-168">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="050d8-168">Property value</span></span>  

<span data-ttu-id="050d8-169">Tipo: **corto sin signo**</span><span class="sxs-lookup"><span data-stu-id="050d8-169">Type: **unsigned short**</span></span>  
