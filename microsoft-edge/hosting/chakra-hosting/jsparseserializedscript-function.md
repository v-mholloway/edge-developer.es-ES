---
description: Analiza una secuencia de comandos serializada y devuelve una función que representa el script.
title: Función JsParseSerializedScript | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a778a007e69f15063d23cc55f999144ab55a306c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574551"
---
# <span data-ttu-id="ffc0b-103">Función JsParseSerializedScript</span><span class="sxs-lookup"><span data-stu-id="ffc0b-103">JsParseSerializedScript Function</span></span>
<span data-ttu-id="ffc0b-104">Analiza una secuencia de comandos serializada y devuelve una función que representa el script.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-104">Parses a serialized script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="ffc0b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffc0b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="ffc0b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffc0b-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="ffc0b-107">Script que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-107">The script to parse.</span></span>  
  
 `buffer`  
 <span data-ttu-id="ffc0b-108">El script serializado.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="ffc0b-109">Una cookie que identifica el script que puede ser usado por contextos de scripts depurables.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="ffc0b-110">La ubicación de la que procede la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="ffc0b-111">Una función que representa el código de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-111">A function representing the script code.</span></span>  
  
## <span data-ttu-id="ffc0b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffc0b-112">Return Value</span></span>  
 <span data-ttu-id="ffc0b-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ffc0b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffc0b-114">Remarks</span></span>  
 <span data-ttu-id="ffc0b-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="ffc0b-116">El motor de scripting no conserva el búfer en la memoria, por lo que el código debe mantenerlo activo durante el tiempo que pueda usarse para ejecutar scripts.</span><span class="sxs-lookup"><span data-stu-id="ffc0b-116">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="ffc0b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffc0b-117">Requirements</span></span>  
 <span data-ttu-id="ffc0b-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ffc0b-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ffc0b-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ffc0b-119">See Also</span></span>  
 [<span data-ttu-id="ffc0b-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ffc0b-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)