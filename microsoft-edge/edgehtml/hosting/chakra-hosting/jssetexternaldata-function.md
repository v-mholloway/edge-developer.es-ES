---
description: Establece los datos externos en un objeto externo.
title: Función JsSetExternalData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f2ebdce4448a14f145ce5aafe6ba412f7db26c17
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236394"
---
# <span data-ttu-id="7bd57-103">Función JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="7bd57-103">JsSetExternalData Function</span></span>

<span data-ttu-id="7bd57-104">Establece los datos externos en un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="7bd57-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="7bd57-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bd57-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="7bd57-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7bd57-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="7bd57-107">Objeto externo.</span><span class="sxs-lookup"><span data-stu-id="7bd57-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="7bd57-108">Los datos externos almacenados en el objeto.</span><span class="sxs-lookup"><span data-stu-id="7bd57-108">The external data stored in the object.</span></span> <span data-ttu-id="7bd57-109">Puede ser null si no hay datos externos almacenados en el objeto.</span><span class="sxs-lookup"><span data-stu-id="7bd57-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="7bd57-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bd57-110">Return Value</span></span>  
 <span data-ttu-id="7bd57-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7bd57-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7bd57-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bd57-112">Remarks</span></span>  
 <span data-ttu-id="7bd57-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="7bd57-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7bd57-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bd57-114">Requirements</span></span>  
 <span data-ttu-id="7bd57-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7bd57-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7bd57-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7bd57-116">See Also</span></span>  
 [<span data-ttu-id="7bd57-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7bd57-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
