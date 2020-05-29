---
description: Devuelve un valor que indica si la ejecución de scripts está deshabilitada en tiempo de ejecución.
title: Función JsIsRuntimeExecutionDisabled | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573424"
---
# <span data-ttu-id="d951b-103">Función JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="d951b-103">JsIsRuntimeExecutionDisabled Function</span></span>
<span data-ttu-id="d951b-104">Devuelve un valor que indica si la ejecución de scripts está deshabilitada en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d951b-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="d951b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d951b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="d951b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d951b-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="d951b-107">Especifica el motor en tiempo de ejecución para comprobar si la ejecución está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="d951b-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="d951b-108">Si la ejecución está deshabilitada, de `false` lo contrario.</span><span class="sxs-lookup"><span data-stu-id="d951b-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="d951b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d951b-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="d951b-110">Si la operación se realizó correctamente, un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d951b-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d951b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d951b-111">Requirements</span></span>  
 <span data-ttu-id="d951b-112">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d951b-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d951b-113">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d951b-113">See Also</span></span>  
 [<span data-ttu-id="d951b-114">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d951b-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)