---
description: Establecer el valor en el índice especificado de un objeto.
title: Función JsSetIndexedProperty | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetIndexedProperty
helpviewer_keywords:
- JsSetIndexedProperty function
ms.assetid: ccbc5bf4-d99b-485c-ab25-d2bd1ed2142e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 893849c42d9cbf0de160846d3397fcd5d7c77b7b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574509"
---
# <span data-ttu-id="2dcad-103">Función JsSetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="2dcad-103">JsSetIndexedProperty Function</span></span>
<span data-ttu-id="2dcad-104">Establecer el valor en el índice especificado de un objeto.</span><span class="sxs-lookup"><span data-stu-id="2dcad-104">Set the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="2dcad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2dcad-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _In_ JsValueRef value  
);  
```  
  
#### <span data-ttu-id="2dcad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dcad-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="2dcad-107">Objeto en el que se va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="2dcad-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="2dcad-108">Índice que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="2dcad-108">The index to set.</span></span>  
  
 `value`  
 <span data-ttu-id="2dcad-109">Valor que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="2dcad-109">The value to set.</span></span>  
  
## <span data-ttu-id="2dcad-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2dcad-110">Return Value</span></span>  
 <span data-ttu-id="2dcad-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="2dcad-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2dcad-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dcad-112">Remarks</span></span>  
 <span data-ttu-id="2dcad-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="2dcad-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="2dcad-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dcad-114">Requirements</span></span>  
 <span data-ttu-id="2dcad-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2dcad-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2dcad-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="2dcad-116">See Also</span></span>  
 [<span data-ttu-id="2dcad-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2dcad-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)