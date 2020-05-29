---
description: Recuperar el valor en el índice especificado de un objeto.
title: Función JsGetIndexedProperty | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7bb048b841462e27604ab169c69e4c051209a67d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574587"
---
# <span data-ttu-id="72793-103">Función JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="72793-103">JsGetIndexedProperty Function</span></span>
<span data-ttu-id="72793-104">Recuperar el valor en el índice especificado de un objeto.</span><span class="sxs-lookup"><span data-stu-id="72793-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="72793-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72793-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="72793-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72793-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="72793-107">Objeto en el que se va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="72793-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="72793-108">Índice que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="72793-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="72793-109">El valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="72793-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="72793-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72793-110">Return Value</span></span>  
 <span data-ttu-id="72793-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="72793-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="72793-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72793-112">Remarks</span></span>  
 <span data-ttu-id="72793-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="72793-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="72793-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72793-114">Requirements</span></span>  
 <span data-ttu-id="72793-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="72793-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="72793-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="72793-116">See Also</span></span>  
 [<span data-ttu-id="72793-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="72793-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)