---
description: Establece los datos externos en un objeto externo.
title: Función JsSetExternalData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cc638905786a1baa0a3d5f79bfa3792a764f358f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574513"
---
# <span data-ttu-id="3a408-103">Función JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="3a408-103">JsSetExternalData Function</span></span>
<span data-ttu-id="3a408-104">Establece los datos externos en un objeto externo.</span><span class="sxs-lookup"><span data-stu-id="3a408-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="3a408-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a408-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="3a408-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a408-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="3a408-107">Objeto externo.</span><span class="sxs-lookup"><span data-stu-id="3a408-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="3a408-108">Los datos externos almacenados en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3a408-108">The external data stored in the object.</span></span> <span data-ttu-id="3a408-109">Puede ser null si no hay datos externos almacenados en el objeto.</span><span class="sxs-lookup"><span data-stu-id="3a408-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="3a408-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a408-110">Return Value</span></span>  
 <span data-ttu-id="3a408-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="3a408-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3a408-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a408-112">Remarks</span></span>  
 <span data-ttu-id="3a408-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="3a408-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3a408-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a408-114">Requirements</span></span>  
 <span data-ttu-id="3a408-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3a408-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3a408-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="3a408-116">See Also</span></span>  
 [<span data-ttu-id="3a408-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3a408-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)