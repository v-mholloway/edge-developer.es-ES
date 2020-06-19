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
# Objeto MSWebViewAsyncOperation  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Expone si la operación se completó correctamente o falló.  

## Eventos  

### completado  

Indica que se completó la operación.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | **Evento** |  
| **Sincrónico** |Sí |  
| **Pase** |No |   
| **Cancelable** |No |  

### error  

Indica que se ha producido un error con la operación.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### Información del evento  

|  |  |  
|:--- |:--- |  
| **Interfaz** | **Evento** |  
| **Sincrónico** | Sí |  
| **Pase** | No |  
| **Cancelable** | No |  

## Métodos  

### start  

Se llama para iniciar la tarea asincrónica.  

```javascript
MSWebViewAsyncOperation.start();
```  

### Parameters  

Este método no tiene parámetros.  

### Valor devuelto  

Este método no devuelve un valor.  

## Propiedades  

### error  

El error que se produjo.  

Esta propiedad es de solo lectura.  

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### Valor de propiedad  

Escriba: **DOMError**  

### finalizar  

El controlador de eventos **completo** .  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### Valor de propiedad  

Escriba: **EventHandler**  

### OnError  

El controlador de eventos de **error** .  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### Valor de propiedad  

Escriba: **EventHandler**  

### readyState  

Describe el estado de lista del objeto.  

Esta propiedad es de solo lectura.  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### Valor de propiedad  

Tipo: **corto sin signo**  

### resultado  

Resultado de la operación.  

Esta propiedad es de solo lectura.  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### Valor de propiedad  

Escriba lo siguiente: cualquiera  

### target  

El destino de la operación.  

Esta propiedad es de solo lectura.  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### Valor de propiedad  

Escriba: [ **MSHTMLWebViewElement**](../webview.md)  

### tipo  

El tipo de la operación.  

Esta propiedad es de solo lectura.  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### Valor de propiedad  

Tipo: **corto sin signo**  
