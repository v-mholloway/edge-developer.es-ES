---
description: LongRunningScriptDetectedEvent (objeto)
title: LongRunningScriptDetectedEvent (objeto)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: webview, aplicaciones de Windows 10, uwp, edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f5eb3230e46ee2cd7926b21f6526e512a7a0322
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397947"
---
# <a name="longrunningscriptdetectedevent-object"></a>LongRunningScriptDetectedEvent (objeto)  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Proporciona información para [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).  

## <a name="properties"></a>Propiedades  

### <a name="executiontime"></a>executionTime  

Obtiene el número de milisegundos que el [elemento webview](../webview/index.md) ha estado ejecutando un script de larga ejecución.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a>Valor de la propiedad  

Tipo: **long**  

### <a name="stoppagescriptexecution"></a>stopPageScriptExecution  

Detiene la ejecución de un script de larga ejecución en el [elemento webview.](../webview/index.md)  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a>Valor de la propiedad  

Tipo: **Boolean**  
