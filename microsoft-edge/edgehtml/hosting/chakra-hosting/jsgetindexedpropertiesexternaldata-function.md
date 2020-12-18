---
description: Recupera la información de datos externos de las propiedades indizadas de un objeto.
title: Función JsGetIndexedPropertiesExternalData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627aaef48def2e042927467e1cbb6d6b7c06a525
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235910"
---
# <span data-ttu-id="0790b-103">Función JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="0790b-103">JsGetIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="0790b-104">Recupera la información de datos externos de las propiedades indizadas de un objeto.</span><span class="sxs-lookup"><span data-stu-id="0790b-104">Retrieves an object's indexed properties external data information.</span></span>  
  
## <span data-ttu-id="0790b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0790b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### <span data-ttu-id="0790b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0790b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="0790b-107">El objeto.</span><span class="sxs-lookup"><span data-stu-id="0790b-107">The object.</span></span>  
  
 `data`  
 <span data-ttu-id="0790b-108">El almacén de datos externos para las propiedades indizadas del objeto.</span><span class="sxs-lookup"><span data-stu-id="0790b-108">The external data back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="0790b-109">El tipo de elemento de matriz en datos externos.</span><span class="sxs-lookup"><span data-stu-id="0790b-109">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="0790b-110">El número de elementos de matriz de datos externos.</span><span class="sxs-lookup"><span data-stu-id="0790b-110">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="0790b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0790b-111">Return Value</span></span>  
 <span data-ttu-id="0790b-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="0790b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0790b-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0790b-113">Remarks</span></span>  
 <span data-ttu-id="0790b-114">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0790b-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="0790b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0790b-115">Requirements</span></span>  
 <span data-ttu-id="0790b-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0790b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0790b-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0790b-117">See Also</span></span>  
 [<span data-ttu-id="0790b-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0790b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
