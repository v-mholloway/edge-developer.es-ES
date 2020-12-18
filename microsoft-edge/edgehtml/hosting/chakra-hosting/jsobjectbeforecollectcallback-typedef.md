---
description: Una devolución de llamada que se llama antes de recopilar un objeto.
title: JsObjectBeforeCollectCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4c24385ec5e15919719ffb0ae71c8adf39c1724c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236417"
---
# <span data-ttu-id="de926-103">Definición de tipo JsObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="de926-103">JsObjectBeforeCollectCallback Typedef</span></span>

<span data-ttu-id="de926-104">Una devolución de llamada que se llama antes de recopilar un objeto.</span><span class="sxs-lookup"><span data-stu-id="de926-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="de926-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de926-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="de926-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de926-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="de926-107">Objeto que se va a recopilar.</span><span class="sxs-lookup"><span data-stu-id="de926-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="de926-108">El estado que se ha pasado a `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="de926-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="de926-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de926-109">Remarks</span></span>  
 <span data-ttu-id="de926-110">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="de926-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="de926-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de926-111">Requirements</span></span>  
 <span data-ttu-id="de926-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="de926-112">jsrt.h</span></span>  
  
## <span data-ttu-id="de926-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="de926-113">See Also</span></span>  
 [<span data-ttu-id="de926-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="de926-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
