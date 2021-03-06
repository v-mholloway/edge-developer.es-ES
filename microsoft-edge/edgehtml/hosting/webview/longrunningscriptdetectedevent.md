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
# <a name="longrunningscriptdetectedevent-object"></a><span data-ttu-id="5943e-104">LongRunningScriptDetectedEvent (objeto)</span><span class="sxs-lookup"><span data-stu-id="5943e-104">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="5943e-105">Proporciona información para [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="5943e-105">Provides information for [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span></span>  

## <a name="properties"></a><span data-ttu-id="5943e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5943e-106">Properties</span></span>  

### <a name="executiontime"></a><span data-ttu-id="5943e-107">executionTime</span><span class="sxs-lookup"><span data-stu-id="5943e-107">executionTime</span></span>  

<span data-ttu-id="5943e-108">Obtiene el número de milisegundos que el [elemento webview](../webview/index.md) ha estado ejecutando un script de larga ejecución.</span><span class="sxs-lookup"><span data-stu-id="5943e-108">Gets the number of milliseconds that the [webview](../webview/index.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a><span data-ttu-id="5943e-109">Valor de la propiedad</span><span class="sxs-lookup"><span data-stu-id="5943e-109">Property value</span></span>  

<span data-ttu-id="5943e-110">Tipo: **long**</span><span class="sxs-lookup"><span data-stu-id="5943e-110">Type: **long**</span></span>  

### <a name="stoppagescriptexecution"></a><span data-ttu-id="5943e-111">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="5943e-111">stopPageScriptExecution</span></span>  

<span data-ttu-id="5943e-112">Detiene la ejecución de un script de larga ejecución en el [elemento webview.](../webview/index.md)</span><span class="sxs-lookup"><span data-stu-id="5943e-112">Stops a long-running script executing in the [webview](../webview/index.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a><span data-ttu-id="5943e-113">Valor de la propiedad</span><span class="sxs-lookup"><span data-stu-id="5943e-113">Property value</span></span>  

<span data-ttu-id="5943e-114">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5943e-114">Type: **Boolean**</span></span>  
