---
description: Determina si un objeto tiene sus propiedades indizadas en datos externos.
title: Función JsHasIndexedPropertiesExternalData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e6395bacb15904bc3f2e74d22959844e8e0af373
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236578"
---
# <span data-ttu-id="449a5-103">Función JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="449a5-103">JsHasIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="449a5-104">Determina si un objeto tiene sus propiedades indizadas en datos externos.</span><span class="sxs-lookup"><span data-stu-id="449a5-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="449a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="449a5-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="449a5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="449a5-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="449a5-107">El objeto.</span><span class="sxs-lookup"><span data-stu-id="449a5-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="449a5-108">Si el objeto tiene sus propiedades indizadas en datos externos.</span><span class="sxs-lookup"><span data-stu-id="449a5-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="449a5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="449a5-109">Return Value</span></span>  
 <span data-ttu-id="449a5-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="449a5-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="449a5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="449a5-111">Remarks</span></span>  
 <span data-ttu-id="449a5-112">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="449a5-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="449a5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="449a5-113">Requirements</span></span>  
 <span data-ttu-id="449a5-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="449a5-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="449a5-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="449a5-115">See Also</span></span>  
 [<span data-ttu-id="449a5-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="449a5-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
