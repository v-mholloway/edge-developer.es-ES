---
description: Convierte un objeto en no extensible.
title: Función JsPreventExtension | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1904756a932bd581e05ec474004af7107da3f64b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236408"
---
# <span data-ttu-id="fa2ef-103">Función JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="fa2ef-103">JsPreventExtension Function</span></span>

<span data-ttu-id="fa2ef-104">Convierte un objeto en no extensible.</span><span class="sxs-lookup"><span data-stu-id="fa2ef-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="fa2ef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa2ef-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="fa2ef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fa2ef-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="fa2ef-107">Objeto que se va a hacer no extensible.</span><span class="sxs-lookup"><span data-stu-id="fa2ef-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="fa2ef-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fa2ef-108">Return Value</span></span>  
 <span data-ttu-id="fa2ef-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="fa2ef-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fa2ef-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa2ef-110">Remarks</span></span>  
 <span data-ttu-id="fa2ef-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="fa2ef-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="fa2ef-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa2ef-112">Requirements</span></span>  
 <span data-ttu-id="fa2ef-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fa2ef-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fa2ef-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="fa2ef-114">See Also</span></span>  
 [<span data-ttu-id="fa2ef-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fa2ef-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
