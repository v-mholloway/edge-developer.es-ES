---
description: Una devolución de llamada que se llama antes de recopilar un objeto.
title: JsObjectBeforeCollectCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 27bbd1aed72cc751397ac4e6734f107612653b66
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573415"
---
# <span data-ttu-id="8ae99-103">JsObjectBeforeCollectCallback typedef</span><span class="sxs-lookup"><span data-stu-id="8ae99-103">JsObjectBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="8ae99-104">Una devolución de llamada que se llama antes de recopilar un objeto.</span><span class="sxs-lookup"><span data-stu-id="8ae99-104">A callback called before collecting an object.</span></span>  
  
## <span data-ttu-id="8ae99-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ae99-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="8ae99-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ae99-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="8ae99-107">Objeto que se va a recopilar.</span><span class="sxs-lookup"><span data-stu-id="8ae99-107">The object to be collected.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="8ae99-108">El estado que se ha pasado a `JsSetObjectBeforeCollectCallback` .</span><span class="sxs-lookup"><span data-stu-id="8ae99-108">The state passed to `JsSetObjectBeforeCollectCallback`.</span></span>  
  
## <span data-ttu-id="8ae99-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ae99-109">Remarks</span></span>  
 <span data-ttu-id="8ae99-110">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="8ae99-110">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="8ae99-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ae99-111">Requirements</span></span>  
 <span data-ttu-id="8ae99-112">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8ae99-112">jsrt.h</span></span>  
  
## <span data-ttu-id="8ae99-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="8ae99-113">See Also</span></span>  
 [<span data-ttu-id="8ae99-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8ae99-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)