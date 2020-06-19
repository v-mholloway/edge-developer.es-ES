---
description: ''
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752159"
---
# <span data-ttu-id="3ea42-103">Objeto LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="3ea42-103">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="3ea42-104">Proporciona información para [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="3ea42-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>  

## <span data-ttu-id="3ea42-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ea42-105">Properties</span></span>  

### <span data-ttu-id="3ea42-106">executionTime</span><span class="sxs-lookup"><span data-stu-id="3ea42-106">executionTime</span></span>  

<span data-ttu-id="3ea42-107">Obtiene el número de milisegundos que el elemento [WebView](../webview.md) ha estado ejecutando un script de ejecución prolongada.</span><span class="sxs-lookup"><span data-stu-id="3ea42-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <span data-ttu-id="3ea42-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3ea42-108">Property value</span></span>  

<span data-ttu-id="3ea42-109">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="3ea42-109">Type: **long**</span></span>  

### <span data-ttu-id="3ea42-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="3ea42-110">stopPageScriptExecution</span></span>  

<span data-ttu-id="3ea42-111">Detiene un script de ejecución larga que se ejecuta en el elemento [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="3ea42-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <span data-ttu-id="3ea42-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3ea42-112">Property value</span></span>  

<span data-ttu-id="3ea42-113">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3ea42-113">Type: **Boolean**</span></span>  
