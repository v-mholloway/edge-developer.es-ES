---
description: Crea un nuevo Runtime.
title: Función JsCreateRuntime | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3b893bd75725d6d9da56417ba83adfce18d77bac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236299"
---
# <span data-ttu-id="c6716-103">Función JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="c6716-103">JsCreateRuntime Function</span></span>

<span data-ttu-id="c6716-104">Crea un nuevo Runtime.</span><span class="sxs-lookup"><span data-stu-id="c6716-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="c6716-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6716-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="c6716-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6716-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="c6716-107">Atributos del motor en tiempo de ejecución que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c6716-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="c6716-108">Versión del motor en tiempo de ejecución que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c6716-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="c6716-109">El servicio de subprocesos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c6716-109">The thread service for the runtime.</span></span> <span data-ttu-id="c6716-110">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="c6716-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="c6716-111">El motor en tiempo de ejecución creado.</span><span class="sxs-lookup"><span data-stu-id="c6716-111">The runtime created.</span></span>  
  
## <span data-ttu-id="c6716-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6716-112">Return Value</span></span>  
 <span data-ttu-id="c6716-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c6716-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c6716-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6716-114">Remarks</span></span>  
 <span data-ttu-id="c6716-115">El `version` parámetro no es compatible con el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6716-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="c6716-116">Para obtener más información sobre el uso de esta API en el modo Microsoft Edge, consulta [dirigirse a Microsoft Edge frente a motores heredados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="c6716-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="c6716-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6716-117">Requirements</span></span>  
 <span data-ttu-id="c6716-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c6716-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c6716-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c6716-119">See Also</span></span>  
 [<span data-ttu-id="c6716-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c6716-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
