---
description: Establece las propiedades indizadas de un objeto en datos externos. Los datos externos se usarán como almacén posterior para las propiedades indizadas del objeto y se puede obtener acceso a ellos como una matriz con tipo.
title: Función JsSetIndexedPropertiesToExternalData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fa0eba3659c20066913cd42a0a18dd5ffe5f857f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236064"
---
# <span data-ttu-id="6a758-104">Función JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="6a758-104">JsSetIndexedPropertiesToExternalData Function</span></span>

<span data-ttu-id="6a758-105">Establece las propiedades indizadas de un objeto en datos externos.</span><span class="sxs-lookup"><span data-stu-id="6a758-105">Sets an object's indexed properties to external data.</span></span> <span data-ttu-id="6a758-106">Los datos externos se usarán como almacén posterior para las propiedades indizadas del objeto y se puede obtener acceso a ellos como una matriz con tipo.</span><span class="sxs-lookup"><span data-stu-id="6a758-106">The external data will be used as back store for the object's indexed properties and accessed like a typed array.</span></span>  
  
## <span data-ttu-id="6a758-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a758-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### <span data-ttu-id="6a758-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a758-108">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6a758-109">Objeto en el que se va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="6a758-109">The object to operate on.</span></span>  
  
 `data`  
 <span data-ttu-id="6a758-110">Datos externos que se usarán como almacén trasero para las propiedades indizadas del objeto.</span><span class="sxs-lookup"><span data-stu-id="6a758-110">The external data to be used as back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="6a758-111">El tipo de elemento de matriz en datos externos.</span><span class="sxs-lookup"><span data-stu-id="6a758-111">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="6a758-112">El número de elementos de matriz de datos externos.</span><span class="sxs-lookup"><span data-stu-id="6a758-112">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="6a758-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a758-113">Return Value</span></span>  
 <span data-ttu-id="6a758-114">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="6a758-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6a758-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a758-115">Remarks</span></span>  
 <span data-ttu-id="6a758-116">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="6a758-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="6a758-117">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="6a758-117">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="6a758-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a758-118">Requirements</span></span>  
 <span data-ttu-id="6a758-119">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6a758-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6a758-120">Consulta también</span><span class="sxs-lookup"><span data-stu-id="6a758-120">See Also</span></span>  
 [<span data-ttu-id="6a758-121">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6a758-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
