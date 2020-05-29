---
description: 'Habilita la ejecución de scripts en tiempo de ejecución. '
title: Función JsEnableRuntimeExecution | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8071fd3c120d1c2029a3c7a3d9c39e68c4cfd2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574608"
---
# <span data-ttu-id="12d07-103">Función JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="12d07-103">JsEnableRuntimeExecution Function</span></span>
<span data-ttu-id="12d07-104">Habilita la ejecución de scripts en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="12d07-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="12d07-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12d07-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="12d07-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12d07-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="12d07-107">El Runtime que se va a habilitar.</span><span class="sxs-lookup"><span data-stu-id="12d07-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="12d07-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12d07-108">Return Value</span></span>  
 <span data-ttu-id="12d07-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="12d07-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="12d07-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12d07-110">Remarks</span></span>  
 <span data-ttu-id="12d07-111">La habilitación de la ejecución de scripts en tiempo de ejecución que ya tiene habilitada la ejecución de scripts es no operativo.</span><span class="sxs-lookup"><span data-stu-id="12d07-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="12d07-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12d07-112">Requirements</span></span>  
 <span data-ttu-id="12d07-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="12d07-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="12d07-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="12d07-114">See Also</span></span>  
 [<span data-ttu-id="12d07-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="12d07-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)