---
description: Devolución de llamada de función.
title: JsNativeFunction typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573421"
---
# <span data-ttu-id="a6030-103">JsNativeFunction typedef</span><span class="sxs-lookup"><span data-stu-id="a6030-103">JsNativeFunction Typedef</span></span>
<span data-ttu-id="a6030-104">Devolución de llamada de función.</span><span class="sxs-lookup"><span data-stu-id="a6030-104">A function callback.</span></span>  
  
## <span data-ttu-id="a6030-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6030-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="a6030-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6030-106">Parameters</span></span>  
 <span data-ttu-id="a6030-107">destinatario</span><span class="sxs-lookup"><span data-stu-id="a6030-107">callee</span></span>  
 <span data-ttu-id="a6030-108">`Function`Objeto que representa la función que se invoca.</span><span class="sxs-lookup"><span data-stu-id="a6030-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="a6030-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="a6030-109">isConstructCall</span></span>  
 <span data-ttu-id="a6030-110">Indica si se trata de una llamada normal o de una llamada nueva.</span><span class="sxs-lookup"><span data-stu-id="a6030-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="a6030-111">arguments</span><span class="sxs-lookup"><span data-stu-id="a6030-111">arguments</span></span>  
 <span data-ttu-id="a6030-112">Los argumentos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a6030-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="a6030-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="a6030-113">argumentCount</span></span>  
 <span data-ttu-id="a6030-114">El número de argumentos.</span><span class="sxs-lookup"><span data-stu-id="a6030-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="a6030-115">Valor de propiedad y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6030-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="a6030-116">El resultado de la llamada, si existe.</span><span class="sxs-lookup"><span data-stu-id="a6030-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="a6030-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6030-117">Requirements</span></span>  
 <span data-ttu-id="a6030-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a6030-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a6030-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="a6030-119">See Also</span></span>  
 [<span data-ttu-id="a6030-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a6030-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)