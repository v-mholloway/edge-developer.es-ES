---
description: Realiza la `instanceof` prueba de operador de JavaScript.
title: Función JsInstanceOf | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 3a7e2397abe5dcb25346e583a0fdab301b8b45f4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573432"
---
# <span data-ttu-id="add04-103">Función JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="add04-103">JsInstanceOf Function</span></span>
<span data-ttu-id="add04-104">Realiza la `instanceof` prueba de operador de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="add04-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="add04-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="add04-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="add04-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="add04-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="add04-107">Objeto que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="add04-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="add04-108">Función constructora con la que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="add04-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="add04-109">Si el "constructor de instancia de objeto" es verdadero.</span><span class="sxs-lookup"><span data-stu-id="add04-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="add04-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="add04-110">Return Value</span></span>  
 <span data-ttu-id="add04-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="add04-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="add04-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="add04-112">Remarks</span></span>  
 <span data-ttu-id="add04-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="add04-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="add04-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="add04-114">Requirements</span></span>  
 <span data-ttu-id="add04-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="add04-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="add04-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="add04-116">See Also</span></span>  
 [<span data-ttu-id="add04-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="add04-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)