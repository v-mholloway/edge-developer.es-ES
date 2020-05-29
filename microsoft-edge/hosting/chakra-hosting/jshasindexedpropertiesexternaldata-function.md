---
description: Determina si un objeto tiene sus propiedades indizadas en datos externos.
title: Función JsHasIndexedPropertiesExternalData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7f9f87b19016b3d837b637219eec936a11211e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574567"
---
# <span data-ttu-id="2538c-103">Función JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="2538c-103">JsHasIndexedPropertiesExternalData Function</span></span>
<span data-ttu-id="2538c-104">Determina si un objeto tiene sus propiedades indizadas en datos externos.</span><span class="sxs-lookup"><span data-stu-id="2538c-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="2538c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2538c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="2538c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2538c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="2538c-107">El objeto.</span><span class="sxs-lookup"><span data-stu-id="2538c-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="2538c-108">Si el objeto tiene sus propiedades indizadas en datos externos.</span><span class="sxs-lookup"><span data-stu-id="2538c-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="2538c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2538c-109">Return Value</span></span>  
 <span data-ttu-id="2538c-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="2538c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2538c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2538c-111">Remarks</span></span>  
 <span data-ttu-id="2538c-112">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2538c-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="2538c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2538c-113">Requirements</span></span>  
 <span data-ttu-id="2538c-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2538c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2538c-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="2538c-115">See Also</span></span>  
 [<span data-ttu-id="2538c-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2538c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)