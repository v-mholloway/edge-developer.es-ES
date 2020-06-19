---
description: Realiza la `instanceof` prueba de operador de JavaScript.
title: Función JsInstanceOf | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4d9bf2e4c3da9f83fdf7c0ef4e2c31df04670420
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751978"
---
# <span data-ttu-id="4ee1a-103">Función JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="4ee1a-103">JsInstanceOf Function</span></span>
<span data-ttu-id="4ee1a-104">Realiza la `instanceof` prueba de operador de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="4ee1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ee1a-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="4ee1a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ee1a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="4ee1a-107">Objeto que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="4ee1a-108">Función constructora con la que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="4ee1a-109">Si el "constructor de instancia de objeto" es verdadero.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="4ee1a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ee1a-110">Return Value</span></span>  
 <span data-ttu-id="4ee1a-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4ee1a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ee1a-112">Remarks</span></span>  
 <span data-ttu-id="4ee1a-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="4ee1a-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4ee1a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee1a-114">Requirements</span></span>  
 <span data-ttu-id="4ee1a-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4ee1a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4ee1a-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="4ee1a-116">See Also</span></span>  
 [<span data-ttu-id="4ee1a-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4ee1a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)