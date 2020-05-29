---
description: Recupera los datos de un objeto externo.
title: Función JsGetExternalData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 469d28d47f89b06897e4b72d081baad34eb92a6c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573460"
---
# <span data-ttu-id="c1efe-103">Función JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="c1efe-103">JsGetExternalData Function</span></span>
<span data-ttu-id="c1efe-104">Recupera los datos de un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="c1efe-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="c1efe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1efe-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="c1efe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1efe-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="c1efe-107">Objeto externo.</span><span class="sxs-lookup"><span data-stu-id="c1efe-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="c1efe-108">Los datos externos almacenados en el objeto.</span><span class="sxs-lookup"><span data-stu-id="c1efe-108">The external data stored in the object.</span></span> <span data-ttu-id="c1efe-109">Puede ser null si no hay datos externos almacenados en el objeto.</span><span class="sxs-lookup"><span data-stu-id="c1efe-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="c1efe-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1efe-110">Return Value</span></span>  
 <span data-ttu-id="c1efe-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c1efe-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c1efe-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1efe-112">Remarks</span></span>  
 <span data-ttu-id="c1efe-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="c1efe-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c1efe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1efe-114">Requirements</span></span>  
 <span data-ttu-id="c1efe-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c1efe-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c1efe-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c1efe-116">See Also</span></span>  
 [<span data-ttu-id="c1efe-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c1efe-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)