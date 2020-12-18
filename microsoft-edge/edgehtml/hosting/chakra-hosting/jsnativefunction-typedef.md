---
description: Devolución de llamada de función.
title: JsNativeFunction typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235901"
---
# <span data-ttu-id="ad237-103">Definición de tipo JsNativeFunction</span><span class="sxs-lookup"><span data-stu-id="ad237-103">JsNativeFunction Typedef</span></span>

<span data-ttu-id="ad237-104">Devolución de llamada de función.</span><span class="sxs-lookup"><span data-stu-id="ad237-104">A function callback.</span></span>  
  
## <span data-ttu-id="ad237-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad237-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="ad237-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad237-106">Parameters</span></span>  
 <span data-ttu-id="ad237-107">destinatario</span><span class="sxs-lookup"><span data-stu-id="ad237-107">callee</span></span>  
 <span data-ttu-id="ad237-108">`Function`Objeto que representa la función que se invoca.</span><span class="sxs-lookup"><span data-stu-id="ad237-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="ad237-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="ad237-109">isConstructCall</span></span>  
 <span data-ttu-id="ad237-110">Indica si se trata de una llamada normal o de una llamada nueva.</span><span class="sxs-lookup"><span data-stu-id="ad237-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="ad237-111">arguments</span><span class="sxs-lookup"><span data-stu-id="ad237-111">arguments</span></span>  
 <span data-ttu-id="ad237-112">Los argumentos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ad237-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="ad237-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="ad237-113">argumentCount</span></span>  
 <span data-ttu-id="ad237-114">El número de argumentos.</span><span class="sxs-lookup"><span data-stu-id="ad237-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="ad237-115">Valor de propiedad y valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad237-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="ad237-116">El resultado de la llamada, si existe.</span><span class="sxs-lookup"><span data-stu-id="ad237-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="ad237-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad237-117">Requirements</span></span>  
 <span data-ttu-id="ad237-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ad237-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ad237-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="ad237-119">See Also</span></span>  
 [<span data-ttu-id="ad237-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ad237-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
