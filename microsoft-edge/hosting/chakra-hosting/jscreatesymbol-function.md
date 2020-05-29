---
description: Crea un símbolo de JavaScript.
title: Función JsCreateSymbol | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a4e634e6f0726ca32ad1056129186ce941edb77b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573486"
---
# <span data-ttu-id="2fd55-103">Función JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="2fd55-103">JsCreateSymbol Function</span></span>
<span data-ttu-id="2fd55-104">Crea un símbolo de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2fd55-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="2fd55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fd55-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="2fd55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fd55-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="2fd55-107">La descripción de la cadena del símbolo.</span><span class="sxs-lookup"><span data-stu-id="2fd55-107">The string description of the symbol.</span></span> <span data-ttu-id="2fd55-108">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="2fd55-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="2fd55-109">El nuevo símbolo.</span><span class="sxs-lookup"><span data-stu-id="2fd55-109">The new symbol.</span></span>  
  
## <span data-ttu-id="2fd55-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fd55-110">Return Value</span></span>  
 <span data-ttu-id="2fd55-111">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="2fd55-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2fd55-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fd55-112">Remarks</span></span>  
 <span data-ttu-id="2fd55-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="2fd55-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="2fd55-114">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2fd55-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="2fd55-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fd55-115">Requirements</span></span>  
 <span data-ttu-id="2fd55-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2fd55-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2fd55-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="2fd55-117">See Also</span></span>  
 [<span data-ttu-id="2fd55-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2fd55-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)