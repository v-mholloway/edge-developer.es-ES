---
description: Obtiene el tipo de JavaScript de un JsValueRef.
title: Función JsGetValueType | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85dc6644e26017c6085ab64d914a86196cca8080
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574566"
---
# <span data-ttu-id="ee70d-103">Función JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="ee70d-103">JsGetValueType Function</span></span>
<span data-ttu-id="ee70d-104">Obtiene el tipo de JavaScript de un JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="ee70d-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="ee70d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee70d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="ee70d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee70d-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="ee70d-107">El valor cuyo tipo se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="ee70d-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="ee70d-108">Tipo del valor.</span><span class="sxs-lookup"><span data-stu-id="ee70d-108">The type of the value.</span></span>  
  
## <span data-ttu-id="ee70d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee70d-109">Return Value</span></span>  
 <span data-ttu-id="ee70d-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="ee70d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ee70d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee70d-111">Remarks</span></span>  
 <span data-ttu-id="ee70d-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="ee70d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ee70d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee70d-113">Requirements</span></span>  
 <span data-ttu-id="ee70d-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ee70d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ee70d-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ee70d-115">See Also</span></span>  
 [<span data-ttu-id="ee70d-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ee70d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)