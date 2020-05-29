---
description: Crea un nuevo Runtime.
title: Función JsCreateRuntime | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d25c1b46354be1fda0ce906dc68c3643989fe2c6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573490"
---
# <span data-ttu-id="15626-103">Función JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="15626-103">JsCreateRuntime Function</span></span>
<span data-ttu-id="15626-104">Crea un nuevo Runtime.</span><span class="sxs-lookup"><span data-stu-id="15626-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="15626-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15626-105">Syntax</span></span>  
  
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
  
#### <span data-ttu-id="15626-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15626-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="15626-107">Atributos del motor en tiempo de ejecución que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="15626-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="15626-108">Versión del motor en tiempo de ejecución que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="15626-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="15626-109">El servicio de subprocesos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="15626-109">The thread service for the runtime.</span></span> <span data-ttu-id="15626-110">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="15626-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="15626-111">El motor en tiempo de ejecución creado.</span><span class="sxs-lookup"><span data-stu-id="15626-111">The runtime created.</span></span>  
  
## <span data-ttu-id="15626-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15626-112">Return Value</span></span>  
 <span data-ttu-id="15626-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="15626-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="15626-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15626-114">Remarks</span></span>  
 <span data-ttu-id="15626-115">El `version` parámetro no es compatible con el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="15626-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="15626-116">Para obtener más información sobre el uso de esta API en el modo Microsoft Edge, consulta [dirigirse a Microsoft Edge frente a motores heredados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="15626-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="15626-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15626-117">Requirements</span></span>  
 <span data-ttu-id="15626-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="15626-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="15626-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="15626-119">See Also</span></span>  
 [<span data-ttu-id="15626-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="15626-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)