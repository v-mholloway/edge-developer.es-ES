---
description: Lo llama el motor en tiempo de ejecución para cargar el código fuente de la secuencia de comandos serializada. El autor de la llamada debe mantener el búfer de script válido hasta el `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2bb30befc61003d20cdeaa293fd1fdfdc95b36f7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236639"
---
# <span data-ttu-id="29098-104">Definición de tipo JsSerializedScriptLoadSourceCallback</span><span class="sxs-lookup"><span data-stu-id="29098-104">JsSerializedScriptLoadSourceCallback Typedef</span></span>

<span data-ttu-id="29098-105">Lo llama el motor en tiempo de ejecución para cargar el código fuente de la secuencia de comandos serializada.</span><span class="sxs-lookup"><span data-stu-id="29098-105">Called by the runtime to load the source code of the serialized script.</span></span> <span data-ttu-id="29098-106">El autor de la llamada debe mantener el búfer de script válido hasta el `JsSerializedScriptUnloadCallback` .</span><span class="sxs-lookup"><span data-stu-id="29098-106">The caller must keep the script buffer valid until the `JsSerializedScriptUnloadCallback`.</span></span>  
  
## <span data-ttu-id="29098-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29098-107">Syntax</span></span>  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### <span data-ttu-id="29098-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29098-108">Parameters</span></span>  
 `sourceContext`  
 <span data-ttu-id="29098-109">El contexto pasado a `JsParseSerializedScriptWithCallback` o `JsRunSerializedScriptWithCallback` .</span><span class="sxs-lookup"><span data-stu-id="29098-109">The context passed to `JsParseSerializedScriptWithCallback` or `JsRunSerializedScriptWithCallback`.</span></span>  
  
 `scriptBuffer`  
 <span data-ttu-id="29098-110">El script devuelto.</span><span class="sxs-lookup"><span data-stu-id="29098-110">The script returned.</span></span>  
  
## <span data-ttu-id="29098-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29098-111">Remarks</span></span>  
  
> [!WARNING]
## <span data-ttu-id="29098-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29098-112">Requirements</span></span>  
 <span data-ttu-id="29098-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="29098-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="29098-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="29098-114">See Also</span></span>  
 [<span data-ttu-id="29098-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="29098-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
