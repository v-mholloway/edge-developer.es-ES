---
description: Eliminar el valor en el índice especificado de un objeto.
title: Función JsDeleteIndexedProperty | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6148a9c59105749a78ece73578d4b840501c6ecc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573474"
---
# <span data-ttu-id="628e3-103">Función JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="628e3-103">JsDeleteIndexedProperty Function</span></span>
<span data-ttu-id="628e3-104">Eliminar el valor en el índice especificado de un objeto.</span><span class="sxs-lookup"><span data-stu-id="628e3-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="628e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="628e3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="628e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="628e3-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="628e3-107">Objeto en el que se va a trabajar.</span><span class="sxs-lookup"><span data-stu-id="628e3-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="628e3-108">Índice que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="628e3-108">The index to delete.</span></span>  
  
## <span data-ttu-id="628e3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="628e3-109">Return Value</span></span>  
 <span data-ttu-id="628e3-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="628e3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="628e3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="628e3-111">Remarks</span></span>  
 <span data-ttu-id="628e3-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="628e3-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="628e3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="628e3-113">Requirements</span></span>  
 <span data-ttu-id="628e3-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="628e3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="628e3-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="628e3-115">See Also</span></span>  
 [<span data-ttu-id="628e3-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="628e3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)