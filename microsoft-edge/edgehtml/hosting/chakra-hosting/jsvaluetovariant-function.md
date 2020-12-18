---
description: Inicializa el `VARIANT` valor que se pasa como proyección de un valor de JavaScript.
title: Función JsValueToVariant | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f383f2d8bc3aab70b4a361b370698cd71cb714d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236230"
---
# <span data-ttu-id="dcdcf-103">Función JsValueToVariant</span><span class="sxs-lookup"><span data-stu-id="dcdcf-103">JsValueToVariant Function</span></span>

<span data-ttu-id="dcdcf-104">Inicializa el `VARIANT` valor que se pasa como proyección de un valor de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-104">Initializes the passed in `VARIANT` as a projection of a JavaScript value.</span></span>  
  
## <span data-ttu-id="dcdcf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcdcf-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### <span data-ttu-id="dcdcf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcdcf-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="dcdcf-107">Un valor de JavaScript para proyectar como un `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="dcdcf-107">A JavaScript value to project as a `VARIANT`.</span></span>  
  
 `variant`  
 <span data-ttu-id="dcdcf-108">Puntero a una `VARIANT` estructura que se inicializará como una proyección.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-108">A pointer to a `VARIANT` struct that will be initialized as a projection.</span></span>  
  
## <span data-ttu-id="dcdcf-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcdcf-109">Return Value</span></span>  
  
## <span data-ttu-id="dcdcf-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcdcf-110">Remarks</span></span>  
 <span data-ttu-id="dcdcf-111">Los `VARIANT` clientes de automatización com pueden usar la proyección para llamar al objeto de JavaScript proyectado.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-111">The projection `VARIANT` can be used by COM automation clients to call into the projected JavaScript object.</span></span>  
  
 <span data-ttu-id="dcdcf-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="dcdcf-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dcdcf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcdcf-113">Requirements</span></span>  
 <span data-ttu-id="dcdcf-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dcdcf-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dcdcf-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="dcdcf-115">See Also</span></span>  
 [<span data-ttu-id="dcdcf-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dcdcf-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
