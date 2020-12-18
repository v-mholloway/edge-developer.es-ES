---
description: Eliminar el valor en el índice especificado de un objeto.
title: Función JsDeleteIndexedProperty | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1340b0204d3845d4a9bd3f18a58ec125a82d2bc0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236425"
---
# <span data-ttu-id="90bee-103">Función JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="90bee-103">JsDeleteIndexedProperty Function</span></span>

<span data-ttu-id="90bee-104">Eliminar el valor en el índice especificado de un objeto.</span><span class="sxs-lookup"><span data-stu-id="90bee-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="90bee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90bee-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="90bee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90bee-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="90bee-107">Objeto en el que se va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="90bee-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="90bee-108">Índice que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="90bee-108">The index to delete.</span></span>  
  
## <span data-ttu-id="90bee-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90bee-109">Return Value</span></span>  
 <span data-ttu-id="90bee-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="90bee-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="90bee-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90bee-111">Remarks</span></span>  
 <span data-ttu-id="90bee-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="90bee-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="90bee-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90bee-113">Requirements</span></span>  
 <span data-ttu-id="90bee-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="90bee-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="90bee-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="90bee-115">See Also</span></span>  
 [<span data-ttu-id="90bee-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="90bee-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
