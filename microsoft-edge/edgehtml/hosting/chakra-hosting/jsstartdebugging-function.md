---
description: Inicia la depuración en el contexto actual.
title: Función JsStartDebugging | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9685779911db8e3045986682b66d13e38c70fe8d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236573"
---
# <span data-ttu-id="facac-103">Función JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="facac-103">JsStartDebugging Function</span></span>

<span data-ttu-id="facac-104">Inicia la depuración en el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="facac-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="facac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="facac-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="facac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="facac-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="facac-107">Aplicación de depuración que se va a usar para la depuración.</span><span class="sxs-lookup"><span data-stu-id="facac-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="facac-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="facac-108">Return Value</span></span>  
 <span data-ttu-id="facac-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="facac-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="facac-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="facac-110">Remarks</span></span>  
 <span data-ttu-id="facac-111">El anfitrión debe asegurarse de que `CoInitializeEx` se llame con `COINIT_MULTITHREADED` o `COINIT_APARTMENTTHREADED` al menos una vez antes de usar esta API</span><span class="sxs-lookup"><span data-stu-id="facac-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="facac-112">El `debugApplication` parámetro no es compatible con el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="facac-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="facac-113">Para obtener más información sobre el uso de esta API en el modo Microsoft Edge, consulta [dirigirse a Microsoft Edge frente a motores heredados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="facac-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="facac-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="facac-114">Requirements</span></span>  
 <span data-ttu-id="facac-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="facac-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="facac-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="facac-116">See Also</span></span>  
 [<span data-ttu-id="facac-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="facac-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
