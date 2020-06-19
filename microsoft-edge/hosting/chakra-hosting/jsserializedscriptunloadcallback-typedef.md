---
description: Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos. La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3da27af18ebc7a1913980a865d926bac6a29d11
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751943"
---
# <span data-ttu-id="0172f-104">Definición de tipo JsSerializedScriptUnloadCallback</span><span class="sxs-lookup"><span data-stu-id="0172f-104">JsSerializedScriptUnloadCallback typedef</span></span>
<span data-ttu-id="0172f-105">Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="0172f-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="0172f-106">La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.</span><span class="sxs-lookup"><span data-stu-id="0172f-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="0172f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0172f-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="0172f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0172f-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="0172f-109">El contexto pasado a `JsParseSerializedScriptWithCallback` o `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="0172f-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="0172f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0172f-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="0172f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0172f-111">Requirements</span></span>  
 <span data-ttu-id="0172f-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0172f-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0172f-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0172f-113">See Also</span></span>  
 [<span data-ttu-id="0172f-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0172f-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)