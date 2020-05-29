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
# Objeto FocusNavigationEvent

El objeto distribuido de [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) que contiene la [**NavigationReason**](#navigationreason) y la ubicación. 

## Métodos

### requestFocus

Se llama para mover el foco de la aplicación a la vista de.

### Parameters

Este método no tiene parámetros.

### Valor devuelto

Este método no devuelve un valor.

## Propiedades
    
### navigationReason

Tipo enumerado **NavigationReason**, ya sea "left", "up", "Right" o "Down". 

Esta propiedad es de solo lectura.

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### Valor de propiedad
Escriba: **NavigationReason**

### originHeight

La ubicación de origen del elemento al que se va a asignar el foco.

Esta propiedad es de solo lectura.

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### Valor de propiedad
Tipo: **float**

### originLeft

Origen izquierdo del elemento al que se va a asignar el foco.

Esta propiedad es de solo lectura.

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### Valor de propiedad
Tipo: **float**

### originTop

Ubicación de origen superior del elemento al que se va a asignar el foco.

Esta propiedad es de solo lectura.

```js
var originTop = FocusNavigationEvent.originTop;
```

#### Valor de propiedad
Tipo: **float**

### originWidth

La ubicación del ancho de origen del elemento al que se va a asignar el foco.

Esta propiedad es de solo lectura.

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### Valor de propiedad
Tipo: **float**

