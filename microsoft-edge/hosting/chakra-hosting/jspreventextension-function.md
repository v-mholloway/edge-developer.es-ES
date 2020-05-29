---
description: Convierte un objeto en no extensible.
title: Función JsPreventExtension | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: baa001b2fd26133ef3a20c88213ac6aaf34a2e0d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574543"
---
# <span data-ttu-id="60f56-103">Función JsPreventExtension</span><span class="sxs-lookup"><span data-stu-id="60f56-103">JsPreventExtension Function</span></span>
<span data-ttu-id="60f56-104">Convierte un objeto en no extensible.</span><span class="sxs-lookup"><span data-stu-id="60f56-104">Makes an object non-extensible.</span></span>  
  
## <span data-ttu-id="60f56-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60f56-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### <span data-ttu-id="60f56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60f56-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="60f56-107">Objeto que se va a hacer no extensible.</span><span class="sxs-lookup"><span data-stu-id="60f56-107">The object to make non-extensible.</span></span>  
  
## <span data-ttu-id="60f56-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60f56-108">Return Value</span></span>  
 <span data-ttu-id="60f56-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="60f56-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="60f56-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60f56-110">Remarks</span></span>  
 <span data-ttu-id="60f56-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="60f56-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="60f56-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60f56-112">Requirements</span></span>  
 <span data-ttu-id="60f56-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="60f56-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="60f56-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="60f56-114">See Also</span></span>  
 [<span data-ttu-id="60f56-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="60f56-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)