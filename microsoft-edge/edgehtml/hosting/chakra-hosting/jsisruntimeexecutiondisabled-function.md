---
description: Devuelve un valor que indica si la ejecución de scripts está deshabilitada en tiempo de ejecución.
title: Función JsIsRuntimeExecutionDisabled | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ce59c77525abdb2dd6cac71dde1378264395e79
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235902"
---
# <span data-ttu-id="47262-103">Función JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="47262-103">JsIsRuntimeExecutionDisabled Function</span></span>

<span data-ttu-id="47262-104">Devuelve un valor que indica si la ejecución de scripts está deshabilitada en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="47262-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="47262-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47262-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="47262-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47262-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="47262-107">Especifica el motor en tiempo de ejecución para comprobar si la ejecución está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="47262-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="47262-108">Si la ejecución está deshabilitada, de `false` lo contrario.</span><span class="sxs-lookup"><span data-stu-id="47262-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="47262-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47262-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="47262-110">Si la operación se realizó correctamente, un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="47262-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="47262-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47262-111">Requirements</span></span>  
 <span data-ttu-id="47262-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="47262-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="47262-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="47262-113">See Also</span></span>  
 [<span data-ttu-id="47262-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="47262-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
