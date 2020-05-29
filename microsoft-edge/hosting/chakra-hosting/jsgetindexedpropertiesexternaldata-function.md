---
description: Recupera la información de datos externos de las propiedades indizadas de un objeto.
title: Función JsGetIndexedPropertiesExternalData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 96fdcd4b6fe29ffc20a796983cc1de692c80a3f1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573454"
---
# <span data-ttu-id="dc043-103">Función JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="dc043-103">JsGetIndexedPropertiesExternalData Function</span></span>
<span data-ttu-id="dc043-104">Recupera la información de datos externos de las propiedades indizadas de un objeto.</span><span class="sxs-lookup"><span data-stu-id="dc043-104">Retrieves an object's indexed properties external data information.</span></span>  
  
## <span data-ttu-id="dc043-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc043-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### <span data-ttu-id="dc043-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc043-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="dc043-107">El objeto.</span><span class="sxs-lookup"><span data-stu-id="dc043-107">The object.</span></span>  
  
 `data`  
 <span data-ttu-id="dc043-108">El almacén de datos externos para las propiedades indizadas del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc043-108">The external data back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="dc043-109">El tipo de elemento de matriz en datos externos.</span><span class="sxs-lookup"><span data-stu-id="dc043-109">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="dc043-110">El número de elementos de matriz de datos externos.</span><span class="sxs-lookup"><span data-stu-id="dc043-110">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="dc043-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc043-111">Return Value</span></span>  
 <span data-ttu-id="dc043-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="dc043-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dc043-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc043-113">Remarks</span></span>  
 <span data-ttu-id="dc043-114">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dc043-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="dc043-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc043-115">Requirements</span></span>  
 <span data-ttu-id="dc043-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dc043-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dc043-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="dc043-117">See Also</span></span>  
 [<span data-ttu-id="dc043-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dc043-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)