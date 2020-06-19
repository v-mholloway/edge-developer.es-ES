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
# Objeto FocusNavigationEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

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

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### Valor de propiedad  

Escriba: **NavigationReason**  

### originHeight  

La ubicación de origen del elemento al que se va a asignar el foco.  

Esta propiedad es de solo lectura.  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### Valor de propiedad  

Tipo: **float**  

### originLeft  

Origen izquierdo del elemento al que se va a asignar el foco.  

Esta propiedad es de solo lectura.  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### Valor de propiedad  

Tipo: **float**  

### originTop  

Ubicación de origen superior del elemento al que se va a asignar el foco.  

Esta propiedad es de solo lectura.  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### Valor de propiedad  

Tipo: **float**  

### originWidth  

La ubicación del ancho de origen del elemento al que se va a asignar el foco.  

Esta propiedad es de solo lectura.  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### Valor de propiedad  

Tipo: **float**  
