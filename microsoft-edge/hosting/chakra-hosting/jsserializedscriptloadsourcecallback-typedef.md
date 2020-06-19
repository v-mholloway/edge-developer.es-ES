---
description: Lo llama el motor en tiempo de ejecución para cargar el código fuente de la secuencia de comandos serializada. El autor de la llamada debe mantener el búfer de script válido hasta el `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 571314145cc19513f04174a9a1c93822a5795b29
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752202"
---
# <span data-ttu-id="5ca6b-104">Definición de tipo JsSerializedScriptLoadSourceCallback</span><span class="sxs-lookup"><span data-stu-id="5ca6b-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>
<span data-ttu-id="5ca6b-105">Lo llama el motor en tiempo de ejecución para cargar el código fuente de la secuencia de comandos serializada.</span><span class="sxs-lookup"><span data-stu-id="5ca6b-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="5ca6b-106">El autor de la llamada debe mantener el búfer de script válido hasta el `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="5ca6b-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="5ca6b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ca6b-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="5ca6b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ca6b-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="5ca6b-109">El contexto pasado a `JsParseSerializedScriptWithCallback` o `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="5ca6b-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="5ca6b-110">El script devuelto.</span><span class="sxs-lookup"><span data-stu-id="5ca6b-110">The script returned.</span></span>  
  
## <span data-ttu-id="5ca6b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ca6b-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="5ca6b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ca6b-112">Requirements</span></span>  
 <span data-ttu-id="5ca6b-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5ca6b-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5ca6b-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="5ca6b-114">See Also</span></span>  
 [<span data-ttu-id="5ca6b-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5ca6b-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)