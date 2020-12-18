---
description: Crea un objeto nuevo.
title: Función JsCreateObject | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateObject
helpviewer_keywords:
- JsCreateObject function
ms.assetid: 6c1d01a4-9254-443e-b974-6f0b0c861ca2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d5effe7ade1679392fcad7f2bb5cea880712ef7f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236219"
---
# <span data-ttu-id="393e6-103">Función JsCreateObject</span><span class="sxs-lookup"><span data-stu-id="393e6-103">JsCreateObject Function</span></span>

<span data-ttu-id="393e6-104">Crea un objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="393e6-104">Creates a new object.</span></span>
  
## <span data-ttu-id="393e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="393e6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateObject(  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="393e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="393e6-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="393e6-107">El objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="393e6-107">The new object.</span></span>  
  
## <span data-ttu-id="393e6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="393e6-108">Return Value</span></span>  
 <span data-ttu-id="393e6-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="393e6-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="393e6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="393e6-110">Remarks</span></span>  
 <span data-ttu-id="393e6-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="393e6-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="393e6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="393e6-112">Requirements</span></span>  
 <span data-ttu-id="393e6-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="393e6-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="393e6-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="393e6-114">See Also</span></span>  
 [<span data-ttu-id="393e6-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="393e6-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
