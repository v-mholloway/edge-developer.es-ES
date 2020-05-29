---
description: Inicia la depuración en el contexto actual.
title: Función JsStartDebugging | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2c94a6f36ad72bfb9354c85d98ae0b5b4e9c77fb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574407"
---
# <span data-ttu-id="62c60-103">Función JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="62c60-103">JsStartDebugging Function</span></span>
<span data-ttu-id="62c60-104">Inicia la depuración en el contexto actual.</span><span class="sxs-lookup"><span data-stu-id="62c60-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="62c60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62c60-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="62c60-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62c60-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="62c60-107">Aplicación de depuración que se va a usar para la depuración.</span><span class="sxs-lookup"><span data-stu-id="62c60-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="62c60-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62c60-108">Return Value</span></span>  
 <span data-ttu-id="62c60-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="62c60-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="62c60-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62c60-110">Remarks</span></span>  
 <span data-ttu-id="62c60-111">El anfitrión debe asegurarse de que `CoInitializeEx` se llame con `COINIT_MULTITHREADED` o `COINIT_APARTMENTTHREADED` al menos una vez antes de usar esta API</span><span class="sxs-lookup"><span data-stu-id="62c60-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="62c60-112">El `debugApplication` parámetro no es compatible con el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="62c60-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="62c60-113">Para obtener más información sobre el uso de esta API en el modo Microsoft Edge, consulta [dirigirse a Microsoft Edge frente a motores heredados](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="62c60-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="62c60-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62c60-114">Requirements</span></span>  
 <span data-ttu-id="62c60-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="62c60-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="62c60-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="62c60-116">See Also</span></span>  
 [<span data-ttu-id="62c60-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="62c60-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)