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
# Objeto MSWebViewAsyncOperation

Expone si la operación se completó correctamente o falló. 

## Eventos

### completado

Indica que se completó la operación. 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### Información del evento

|            |      |
|------------|------|
|**Interfaz** | **Evento**
|**Sincrónico** |Sí |    
|**Pase**     |No |   
|**Cancelable**  |No |        


### error

Indica que se ha producido un error con la operación.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### Información del evento

|            |      |
|------------|------|
|**Interfaz** | **Evento**
|**Sincrónico** |Sí |    
|**Pase**     |No |   
|**Cancelable**  |No |            


## Métodos

### start

Se llama para iniciar la tarea asincrónica. 

```js
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

```js
var error = MSWebViewAsyncOperation.error;
```

#### Valor de propiedad
Escriba: **DOMError**

### finalizar

El controlador de eventos **completo** . 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### Valor de propiedad
Escriba: **EventHandler**

### OnError

El controlador de eventos de **error** . 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### Valor de propiedad
Escriba: **EventHandler**

### readyState

Describe el estado de lista del objeto.

Esta propiedad es de solo lectura.

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### Valor de propiedad
Tipo: **corto sin signo**

### resultado

Resultado de la operación.

Esta propiedad es de solo lectura.

```js
var result = MSWebViewAsyncOperation.result;
```

#### Valor de propiedad
Escriba lo siguiente: cualquiera

### target

El destino de la operación. 

Esta propiedad es de solo lectura.

```js
var target = MSWebViewAsyncOperation.target;
```

#### Valor de propiedad
Escriba: [ **MSHTMLWebViewElement**](../webview.md)

### tipo

El tipo de la operación.

Esta propiedad es de solo lectura.

```js
var type = MSWebViewAsyncOperation.type;
```

#### Valor de propiedad
Tipo: **corto sin signo**
