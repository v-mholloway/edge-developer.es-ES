---
description: 'Habilita la ejecución de scripts en tiempo de ejecución. '
title: Función JsEnableRuntimeExecution | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e87191197f70898b2f69d138026edd4e75cd5114
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236278"
---
# <span data-ttu-id="ac573-103">Función JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="ac573-103">JsEnableRuntimeExecution Function</span></span>

<span data-ttu-id="ac573-104">Habilita la ejecución de scripts en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ac573-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="ac573-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac573-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="ac573-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac573-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="ac573-107">El Runtime que se va a habilitar.</span><span class="sxs-lookup"><span data-stu-id="ac573-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="ac573-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac573-108">Return Value</span></span>  
 <span data-ttu-id="ac573-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="ac573-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ac573-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac573-110">Remarks</span></span>  
 <span data-ttu-id="ac573-111">La habilitación de la ejecución de scripts en tiempo de ejecución que ya tiene habilitada la ejecución de scripts es no operativo.</span><span class="sxs-lookup"><span data-stu-id="ac573-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="ac573-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac573-112">Requirements</span></span>  
 <span data-ttu-id="ac573-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ac573-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ac573-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ac573-114">See Also</span></span>  
 [<span data-ttu-id="ac573-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ac573-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
