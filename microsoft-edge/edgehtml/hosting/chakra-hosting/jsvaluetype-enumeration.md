---
description: El tipo de JavaScript de un JsValueRef.
title: JsValueType (enumeración) | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236228"
---
# <span data-ttu-id="b1545-103">Enumeración de JsValueType</span><span class="sxs-lookup"><span data-stu-id="b1545-103">JsValueType Enumeration</span></span>

<span data-ttu-id="b1545-104">El tipo de JavaScript de un JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="b1545-104">The JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="b1545-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1545-105">Syntax</span></span>  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## <span data-ttu-id="b1545-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1545-106">Members</span></span>  
  
### <span data-ttu-id="b1545-107">Los</span><span class="sxs-lookup"><span data-stu-id="b1545-107">Values</span></span>  
  
|<span data-ttu-id="b1545-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b1545-108">Name</span></span>|<span data-ttu-id="b1545-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1545-109">Description</span></span>|  
|----------|-----------------|  
|`JsUndefined`|<span data-ttu-id="b1545-110">El valor es el `undefined` valor.</span><span class="sxs-lookup"><span data-stu-id="b1545-110">The value is the `undefined` value.</span></span>|  
|`JsNull`|<span data-ttu-id="b1545-111">El valor es el `null` valor.</span><span class="sxs-lookup"><span data-stu-id="b1545-111">The value is the `null` value.</span></span>|  
|`JsNumber`|<span data-ttu-id="b1545-112">El valor es un valor de número de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-112">The value is a JavaScript number value.</span></span>|  
|`JsString`|<span data-ttu-id="b1545-113">El valor es un valor de cadena de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-113">The value is a JavaScript string value.</span></span>|  
|`JsBoolean`|<span data-ttu-id="b1545-114">El valor es un valor booleano de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-114">The value is a JavaScript Boolean value.</span></span>|  
|`JsObject`|<span data-ttu-id="b1545-115">El valor es un valor de objeto de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-115">The value is a JavaScript object value.</span></span>|  
|`JsFunction`|<span data-ttu-id="b1545-116">El valor es un valor de objeto de función de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-116">The value is a JavaScript function object value.</span></span>|  
|`JsError`|<span data-ttu-id="b1545-117">El valor es un valor de objeto de error de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-117">The value is a JavaScript error object value.</span></span>|  
|`JsArray`|<span data-ttu-id="b1545-118">El valor es un valor de objeto de matriz de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-118">The value is a JavaScript array object value.</span></span>|  
|`JsSymbol`|<span data-ttu-id="b1545-119">El valor es un valor de símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-119">The value is a JavaScript symbol value.</span></span><br /><br /> <span data-ttu-id="b1545-120">Este valor de enumeración solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b1545-120">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsArrayBuffer`|<span data-ttu-id="b1545-121">El valor es un valor de objeto de JavaScript `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="b1545-121">The value is a JavaScript `ArrayBuffer` object value.</span></span><br /><br /> <span data-ttu-id="b1545-122">Este valor de enumeración solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b1545-122">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsTypedArray`|<span data-ttu-id="b1545-123">El valor es un valor de objeto de matriz con tipo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b1545-123">The value is a JavaScript typed array object value.</span></span><br /><br /> <span data-ttu-id="b1545-124">Este valor de enumeración solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b1545-124">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsDataView`|<span data-ttu-id="b1545-125">El valor es un valor de objeto de JavaScript `DataView` .</span><span class="sxs-lookup"><span data-stu-id="b1545-125">The value is a JavaScript `DataView` object value.</span></span><br /><br /> <span data-ttu-id="b1545-126">Este valor de enumeración solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b1545-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
  
## <span data-ttu-id="b1545-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1545-127">Requirements</span></span>  
 <span data-ttu-id="b1545-128">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b1545-128">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b1545-129">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b1545-129">See Also</span></span>  
 [<span data-ttu-id="b1545-130">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b1545-130">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
