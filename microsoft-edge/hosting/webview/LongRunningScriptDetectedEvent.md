---
description: ''
title: Objeto LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573377"
---
# <span data-ttu-id="3d793-103">Objeto LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="3d793-103">LongRunningScriptDetectedEvent object</span></span>

<span data-ttu-id="3d793-104">Proporciona información para [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="3d793-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>

## <span data-ttu-id="3d793-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d793-105">Properties</span></span>

### <span data-ttu-id="3d793-106">executionTime</span><span class="sxs-lookup"><span data-stu-id="3d793-106">executionTime</span></span>

<span data-ttu-id="3d793-107">Obtiene el número de milisegundos que el elemento [WebView](../webview.md) ha estado ejecutando un script de ejecución prolongada.</span><span class="sxs-lookup"><span data-stu-id="3d793-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### <span data-ttu-id="3d793-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3d793-108">Property value</span></span>
<span data-ttu-id="3d793-109">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="3d793-109">Type: **long**</span></span>

### <span data-ttu-id="3d793-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="3d793-110">stopPageScriptExecution</span></span>
<span data-ttu-id="3d793-111">Detiene un script de ejecución larga que se ejecuta en el elemento [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="3d793-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### <span data-ttu-id="3d793-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3d793-112">Property value</span></span>
<span data-ttu-id="3d793-113">Tipo: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="3d793-113">Type: **Boolean**</span></span>