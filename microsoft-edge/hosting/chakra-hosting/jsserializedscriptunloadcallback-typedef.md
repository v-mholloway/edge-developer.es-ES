---
description: Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos. La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.
title: JsSerializedScriptUnloadCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574522"
---
# <span data-ttu-id="2f77b-104">JsSerializedScriptUnloadCallback typedef</span><span class="sxs-lookup"><span data-stu-id="2f77b-104">JsSerializedScriptUnloadCallback typedef</span></span>
<span data-ttu-id="2f77b-105">Lo llama el motor en tiempo de ejecución cuando termina con todos los recursos relacionados con la ejecución de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="2f77b-105">Called by the runtime when it is finished with all resources related to the script execution.</span></span> <span data-ttu-id="2f77b-106">La persona que llama debe liberar el origen si está cargado, el código de byte y el contexto en este momento.</span><span class="sxs-lookup"><span data-stu-id="2f77b-106">The caller should free the source if loaded, the byte code, and the context at this time.</span></span>  
  
## <span data-ttu-id="2f77b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f77b-107">Syntax</span></span>  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### <span data-ttu-id="2f77b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f77b-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="2f77b-109">El contexto pasado a `JsParseSerializedScriptWithCallback` o `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="2f77b-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
## <span data-ttu-id="2f77b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f77b-110">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="2f77b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f77b-111">Requirements</span></span>  
 <span data-ttu-id="2f77b-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2f77b-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2f77b-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="2f77b-113">See Also</span></span>  
 [<span data-ttu-id="2f77b-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2f77b-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)