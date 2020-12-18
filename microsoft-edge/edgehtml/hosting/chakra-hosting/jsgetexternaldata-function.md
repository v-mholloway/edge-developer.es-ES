---
description: Recupera los datos de un objeto externo.
title: Función JsGetExternalData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d046b5c515b1a688cd527fdc0eb9cd173eb47570
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236324"
---
# <span data-ttu-id="e5221-103">Función JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="e5221-103">JsGetExternalData Function</span></span>

<span data-ttu-id="e5221-104">Recupera los datos de un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e5221-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="e5221-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5221-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="e5221-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5221-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e5221-107">Objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e5221-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="e5221-108">Los datos externos almacenados en el objeto.</span><span class="sxs-lookup"><span data-stu-id="e5221-108">The external data stored in the object.</span></span> <span data-ttu-id="e5221-109">Puede ser null si no hay datos externos almacenados en el objeto.</span><span class="sxs-lookup"><span data-stu-id="e5221-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="e5221-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5221-110">Return Value</span></span>  
 <span data-ttu-id="e5221-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="e5221-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e5221-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5221-112">Remarks</span></span>  
 <span data-ttu-id="e5221-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="e5221-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e5221-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5221-114">Requirements</span></span>  
 <span data-ttu-id="e5221-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e5221-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e5221-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="e5221-116">See Also</span></span>  
 [<span data-ttu-id="e5221-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e5221-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
