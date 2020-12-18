---
description: Crea un símbolo de JavaScript.
title: Función JsCreateSymbol | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 6a2f77f477aeebac150635d93cbd0cd043357256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236295"
---
# <span data-ttu-id="82b5c-103">Función JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="82b5c-103">JsCreateSymbol Function</span></span>

<span data-ttu-id="82b5c-104">Crea un símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="82b5c-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="82b5c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82b5c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="82b5c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82b5c-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="82b5c-107">La descripción de la cadena del símbolo.</span><span class="sxs-lookup"><span data-stu-id="82b5c-107">The string description of the symbol.</span></span> <span data-ttu-id="82b5c-108">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="82b5c-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="82b5c-109">El nuevo símbolo.</span><span class="sxs-lookup"><span data-stu-id="82b5c-109">The new symbol.</span></span>  
  
## <span data-ttu-id="82b5c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82b5c-110">Return Value</span></span>  
 <span data-ttu-id="82b5c-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="82b5c-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="82b5c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82b5c-112">Remarks</span></span>  
 <span data-ttu-id="82b5c-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="82b5c-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="82b5c-114">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="82b5c-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="82b5c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82b5c-115">Requirements</span></span>  
 <span data-ttu-id="82b5c-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="82b5c-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="82b5c-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="82b5c-117">See Also</span></span>  
 [<span data-ttu-id="82b5c-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="82b5c-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
