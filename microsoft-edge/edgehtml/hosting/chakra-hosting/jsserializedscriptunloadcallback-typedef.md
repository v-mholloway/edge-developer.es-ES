---
description: Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos. La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5c63f2ff3faf21a19e31f2f6fd1692e21d59fc0b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236589"
---
# <span data-ttu-id="bdc37-104">Definición de tipo JsSerializedScriptUnloadCallback</span><span class="sxs-lookup"><span data-stu-id="bdc37-104">JsSerializedScriptUnloadCallback typedef</span></span>

<span data-ttu-id="bdc37-105">Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="bdc37-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="bdc37-106">La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.</span><span class="sxs-lookup"><span data-stu-id="bdc37-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="bdc37-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdc37-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="bdc37-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdc37-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="bdc37-109">El contexto pasado a `JsParseSerializedScriptWithCallback` o `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="bdc37-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="bdc37-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdc37-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="bdc37-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdc37-111">Requirements</span></span>  
 <span data-ttu-id="bdc37-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bdc37-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bdc37-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="bdc37-113">See Also</span></span>  
 [<span data-ttu-id="bdc37-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bdc37-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
