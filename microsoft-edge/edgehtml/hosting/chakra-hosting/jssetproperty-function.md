---
description: Coloca la propiedad de un objeto.
title: Función JsSetProperty | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 29c3e04fc240bd63fc755c6727752d053b94484d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236290"
---
# <span data-ttu-id="deb75-103">Función JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="deb75-103">JsSetProperty Function</span></span>

<span data-ttu-id="deb75-104">Coloca la propiedad de un objeto.</span><span class="sxs-lookup"><span data-stu-id="deb75-104">Puts an object's property.</span></span>  
  
## <span data-ttu-id="deb75-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="deb75-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### <span data-ttu-id="deb75-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="deb75-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="deb75-107">Objeto que contiene la propiedad.</span><span class="sxs-lookup"><span data-stu-id="deb75-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="deb75-108">IDENTIFICADOR de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="deb75-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="deb75-109">Nuevo valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="deb75-109">The new value of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="deb75-110">El conjunto de propiedades debe seguir las reglas de modo estricto.</span><span class="sxs-lookup"><span data-stu-id="deb75-110">The property set should follow strict mode rules.</span></span>  
  
## <span data-ttu-id="deb75-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="deb75-111">Return Value</span></span>  
 <span data-ttu-id="deb75-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="deb75-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="deb75-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="deb75-113">Remarks</span></span>  
 <span data-ttu-id="deb75-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="deb75-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="deb75-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deb75-115">Requirements</span></span>  
 <span data-ttu-id="deb75-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="deb75-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="deb75-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="deb75-117">See Also</span></span>  
 [<span data-ttu-id="deb75-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="deb75-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
