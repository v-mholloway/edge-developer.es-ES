---
description: Inicializa el `VARIANT` valor que se pasa como proyección de un valor de JavaScript.
title: Función JsValueToVariant | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573396"
---
# <span data-ttu-id="49733-103">Función JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="49733-103">JsValueToVariant Function</span></span>
<span data-ttu-id="49733-104">Inicializa el `VARIANT` valor que se pasa como proyección de un valor de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="49733-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="49733-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49733-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="49733-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49733-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="49733-107">Un valor de JavaScript para proyectar como un `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="49733-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="49733-108">Puntero a una `VARIANT` estructura que se inicializará como una proyección.</span><span class="sxs-lookup"><span data-stu-id="49733-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="49733-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49733-109">Return Value</span></span>  
  
## <span data-ttu-id="49733-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49733-110">Remarks</span></span>  
 <span data-ttu-id="49733-111">Los `VARIANT` clientes de automatización com pueden usar la proyección para llamar al objeto de JavaScript proyectado.</span><span class="sxs-lookup"><span data-stu-id="49733-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="49733-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="49733-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="49733-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49733-113">Requirements</span></span>  
 <span data-ttu-id="49733-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="49733-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="49733-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="49733-115">See Also</span></span>  
 [<span data-ttu-id="49733-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="49733-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)