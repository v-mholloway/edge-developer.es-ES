---
description: Ejecuta una secuencia de comandos serializada.
title: Función JsRunSerializedScript | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1e2fb7fdc5df52fde3b7cc59cf9173d658782a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574537"
---
# <span data-ttu-id="7e7ca-103">Función JsRunSerializedScript</span><span class="sxs-lookup"><span data-stu-id="7e7ca-103">JsRunSerializedScript Function</span></span>
<span data-ttu-id="7e7ca-104">Ejecuta una secuencia de comandos serializada.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-104">Runs a serialized script.</span></span>  
  
## <span data-ttu-id="7e7ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e7ca-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="7e7ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e7ca-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="7e7ca-107">El código fuente de la secuencia de comandos serializada.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-107">The source code of the serialized script.</span></span>  
  
 `buffer`  
 <span data-ttu-id="7e7ca-108">El script serializado.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="7e7ca-109">Una cookie que identifica el script que puede ser usado por contextos de scripts depurables.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="7e7ca-110">La ubicación de la que procede la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="7e7ca-111">El resultado de ejecutar el script, si existe.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-111">The result of running the script, if any.</span></span> <span data-ttu-id="7e7ca-112">Este parámetro puede ser null.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-112">This parameter can be null.</span></span>  
  
## <span data-ttu-id="7e7ca-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e7ca-113">Return Value</span></span>  
 <span data-ttu-id="7e7ca-114">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7e7ca-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e7ca-115">Remarks</span></span>  
 <span data-ttu-id="7e7ca-116">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="7e7ca-117">El motor de scripting no conserva el búfer en la memoria, por lo que el código debe mantenerlo activo durante el tiempo que pueda usarse para ejecutar scripts.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-117">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="7e7ca-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7ca-118">Requirements</span></span>  
 <span data-ttu-id="7e7ca-119">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7e7ca-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7e7ca-120">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7e7ca-120">See Also</span></span>  
 [<span data-ttu-id="7e7ca-121">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7e7ca-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)