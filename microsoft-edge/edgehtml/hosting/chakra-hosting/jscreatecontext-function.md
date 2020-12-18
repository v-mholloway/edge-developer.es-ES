---
description: Crea un contexto de script para ejecutar scripts.
title: Función JsCreateContext | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5d6c8149b8a5e5fee7cbc8dac821713b1d9649ee
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236080"
---
# <span data-ttu-id="d535a-103">Función JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="d535a-103">JsCreateContext Function</span></span>

<span data-ttu-id="d535a-104">Crea un contexto de script para ejecutar scripts.</span><span class="sxs-lookup"><span data-stu-id="d535a-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="d535a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d535a-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### <span data-ttu-id="d535a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d535a-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="d535a-107">El motor en tiempo de ejecución en el que se crea el script.</span><span class="sxs-lookup"><span data-stu-id="d535a-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="d535a-108">Aplicación de depuración que se va a usar para la depuración.</span><span class="sxs-lookup"><span data-stu-id="d535a-108">The debug application to use for debugging.</span></span> <span data-ttu-id="d535a-109">Este parámetro puede ser null, en cuyo caso la depuración no está habilitada para el contexto.</span><span class="sxs-lookup"><span data-stu-id="d535a-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="d535a-110">El contexto de script creado.</span><span class="sxs-lookup"><span data-stu-id="d535a-110">The created script context.</span></span>  
  
## <span data-ttu-id="d535a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d535a-111">Return Value</span></span>  
 <span data-ttu-id="d535a-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d535a-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d535a-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d535a-113">Remarks</span></span>  
 <span data-ttu-id="d535a-114">Cada contexto de script tiene su propio objeto global que se aísla del resto de contextos de script.</span><span class="sxs-lookup"><span data-stu-id="d535a-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="d535a-115">El `debugApplication` parámetro no es compatible con el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d535a-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="d535a-116">Para obtener más información sobre el uso de esta API en el modo Microsoft Edge, consulta [dirigirse a Microsoft Edge frente a motores heredados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="d535a-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="d535a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d535a-117">Requirements</span></span>  
 <span data-ttu-id="d535a-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d535a-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d535a-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d535a-119">See Also</span></span>  
 [<span data-ttu-id="d535a-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d535a-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
