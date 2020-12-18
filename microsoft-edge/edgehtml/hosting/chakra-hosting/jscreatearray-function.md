---
description: Crea un objeto de matriz de JavaScript.
title: Función JsCreateArray | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34ce07055fa3d4d24188d7edbcedc3f08973e233
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236081"
---
# <span data-ttu-id="08908-103">Función JsCreateArray</span><span class="sxs-lookup"><span data-stu-id="08908-103">JsCreateArray Function</span></span>

<span data-ttu-id="08908-104">Crea un objeto de matriz de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="08908-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="08908-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08908-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="08908-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08908-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="08908-107">La longitud inicial de la matriz.</span><span class="sxs-lookup"><span data-stu-id="08908-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="08908-108">El nuevo objeto de matriz.</span><span class="sxs-lookup"><span data-stu-id="08908-108">The new array object.</span></span>  
  
## <span data-ttu-id="08908-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08908-109">Return Value</span></span>  
 <span data-ttu-id="08908-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="08908-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="08908-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08908-111">Remarks</span></span>  
 <span data-ttu-id="08908-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="08908-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="08908-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08908-113">Requirements</span></span>  
 <span data-ttu-id="08908-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="08908-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="08908-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="08908-115">See Also</span></span>  
 [<span data-ttu-id="08908-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="08908-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
