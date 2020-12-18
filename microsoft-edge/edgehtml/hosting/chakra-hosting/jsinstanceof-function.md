---
description: Realiza la `instanceof` prueba de operador de JavaScript.
title: Función JsInstanceOf | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d8aec1d4512fe937d1fd48aa6f3e88294bf9850c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236460"
---
# <span data-ttu-id="89708-103">Función JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="89708-103">JsInstanceOf Function</span></span>

<span data-ttu-id="89708-104">Realiza la `instanceof` prueba de operador de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="89708-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="89708-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89708-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="89708-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89708-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="89708-107">Objeto que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="89708-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="89708-108">Función constructora con la que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="89708-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="89708-109">Si el "constructor de instancia de objeto" es verdadero.</span><span class="sxs-lookup"><span data-stu-id="89708-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="89708-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89708-110">Return Value</span></span>  
 <span data-ttu-id="89708-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="89708-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="89708-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89708-112">Remarks</span></span>  
 <span data-ttu-id="89708-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="89708-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="89708-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89708-114">Requirements</span></span>  
 <span data-ttu-id="89708-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="89708-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="89708-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="89708-116">See Also</span></span>  
 [<span data-ttu-id="89708-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="89708-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
