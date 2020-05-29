---
description: Crea un valor de JavaScript que es una proyección del valor que se ha pasado `VARIANT` .
title: Función JsVariantToValue | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 01796bc38548cf56b500731d899541ef214ec4e3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573392"
---
# <span data-ttu-id="4ff01-103">Función JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="4ff01-103">JsVariantToValue Function</span></span>
<span data-ttu-id="4ff01-104">Crea un valor de JavaScript que es una proyección del valor que se ha pasado `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="4ff01-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="4ff01-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ff01-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="4ff01-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ff01-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="4ff01-107">`VARIANT`A para que se proyecte.</span><span class="sxs-lookup"><span data-stu-id="4ff01-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="4ff01-108">Un valor de JavaScript que es una proyección del `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="4ff01-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="4ff01-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ff01-109">Return Value</span></span>  
 <span data-ttu-id="4ff01-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="4ff01-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4ff01-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ff01-111">Remarks</span></span>  
 <span data-ttu-id="4ff01-112">El script puede utilizar el valor proyectado para llamar a un objeto de automatización COM desde un script.</span><span class="sxs-lookup"><span data-stu-id="4ff01-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="4ff01-113">Los hosts son responsables de exigir reglas de subprocesamiento COM.</span><span class="sxs-lookup"><span data-stu-id="4ff01-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="4ff01-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="4ff01-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4ff01-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ff01-115">Requirements</span></span>  
 <span data-ttu-id="4ff01-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4ff01-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4ff01-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="4ff01-117">See Also</span></span>  
 [<span data-ttu-id="4ff01-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4ff01-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)