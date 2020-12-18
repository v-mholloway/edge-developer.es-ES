---
description: Crea un valor de JavaScript que es una proyección del valor que se ha pasado `VARIANT` .
title: Función JsVariantToValue | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 58c928b519b5a9a678b6cd6ad367e1db2332f021
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236227"
---
# <span data-ttu-id="95148-103">Función JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="95148-103">JsVariantToValue Function</span></span>

<span data-ttu-id="95148-104">Crea un valor de JavaScript que es una proyección del valor que se ha pasado `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="95148-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="95148-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95148-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="95148-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95148-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="95148-107">`VARIANT`A para que se proyecte.</span><span class="sxs-lookup"><span data-stu-id="95148-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="95148-108">Un valor de JavaScript que es una proyección del `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="95148-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="95148-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95148-109">Return Value</span></span>  
 <span data-ttu-id="95148-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="95148-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="95148-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95148-111">Remarks</span></span>  
 <span data-ttu-id="95148-112">El script puede utilizar el valor proyectado para llamar a un objeto de automatización COM desde un script.</span><span class="sxs-lookup"><span data-stu-id="95148-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="95148-113">Los hosts son responsables de exigir reglas de subprocesamiento COM.</span><span class="sxs-lookup"><span data-stu-id="95148-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="95148-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="95148-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="95148-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95148-115">Requirements</span></span>  
 <span data-ttu-id="95148-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="95148-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="95148-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="95148-117">See Also</span></span>  
 [<span data-ttu-id="95148-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="95148-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
