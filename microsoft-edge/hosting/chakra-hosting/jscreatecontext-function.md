---
description: Crea un contexto de script para ejecutar scripts.
title: Función JsCreateContext | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 06bd4c4780a8c7610ebc95cfc0da058306ce5b78
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573510"
---
# <span data-ttu-id="693a5-103">Función JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="693a5-103">JsCreateContext Function</span></span>
<span data-ttu-id="693a5-104">Crea un contexto de script para ejecutar scripts.</span><span class="sxs-lookup"><span data-stu-id="693a5-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="693a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="693a5-105">Syntax</span></span>  
  
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
  
#### <span data-ttu-id="693a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="693a5-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="693a5-107">El motor en tiempo de ejecución en el que se crea el script.</span><span class="sxs-lookup"><span data-stu-id="693a5-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="693a5-108">Aplicación de depuración que se va a usar para la depuración.</span><span class="sxs-lookup"><span data-stu-id="693a5-108">The debug application to use for debugging.</span></span> <span data-ttu-id="693a5-109">Este parámetro puede ser null, en cuyo caso la depuración no está habilitada para el contexto.</span><span class="sxs-lookup"><span data-stu-id="693a5-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="693a5-110">El contexto de script creado.</span><span class="sxs-lookup"><span data-stu-id="693a5-110">The created script context.</span></span>  
  
## <span data-ttu-id="693a5-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="693a5-111">Return Value</span></span>  
 <span data-ttu-id="693a5-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="693a5-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="693a5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="693a5-113">Remarks</span></span>  
 <span data-ttu-id="693a5-114">Cada contexto de script tiene su propio objeto global que se aísla del resto de contextos de script.</span><span class="sxs-lookup"><span data-stu-id="693a5-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="693a5-115">El `debugApplication` parámetro no es compatible con el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="693a5-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="693a5-116">Para obtener más información sobre el uso de esta API en el modo Microsoft Edge, consulta [dirigirse a Microsoft Edge frente a motores heredados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="693a5-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="693a5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="693a5-117">Requirements</span></span>  
 <span data-ttu-id="693a5-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="693a5-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="693a5-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="693a5-119">See Also</span></span>  
 [<span data-ttu-id="693a5-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="693a5-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)