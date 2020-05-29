---
description: Una devolución de llamada llamada antes de la colección.
title: JsBeforeCollectCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 17f279c2d2ffcc8d02819994dddebfc22baa4cab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573534"
---
# <span data-ttu-id="04ee0-103">JsBeforeCollectCallback typedef</span><span class="sxs-lookup"><span data-stu-id="04ee0-103">JsBeforeCollectCallback Typedef</span></span>
<span data-ttu-id="04ee0-104">Una devolución de llamada llamada antes de la colección.</span><span class="sxs-lookup"><span data-stu-id="04ee0-104">A callback called before collection.</span></span>  
  
## <span data-ttu-id="04ee0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04ee0-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### <span data-ttu-id="04ee0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04ee0-106">Parameters</span></span>  
 <span data-ttu-id="04ee0-107">callbackState</span><span class="sxs-lookup"><span data-stu-id="04ee0-107">callbackState</span></span>  
 <span data-ttu-id="04ee0-108">El estado pasado a JsSetBeforeCollectCallback.</span><span class="sxs-lookup"><span data-stu-id="04ee0-108">The state passed to JsSetBeforeCollectCallback.</span></span>  
  
## <span data-ttu-id="04ee0-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04ee0-109">Remarks</span></span>  
 <span data-ttu-id="04ee0-110">Usa JsSetBeforeCollectCallback para registrar esta devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="04ee0-110">Use JsSetBeforeCollectCallback to register this callback.</span></span>  
  
## <span data-ttu-id="04ee0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04ee0-111">Requirements</span></span>  
 <span data-ttu-id="04ee0-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="04ee0-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="04ee0-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="04ee0-113">See Also</span></span>  
 [<span data-ttu-id="04ee0-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="04ee0-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)