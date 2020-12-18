---
description: Identificador para un tiempo de ejecución de Chakra.
title: JsRuntimeHandle typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: ab08243505b9699fe07ca2e80f7294adf9eb78ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236063"
---
# <span data-ttu-id="45628-103">Definición de tipo JsRuntimeHandle</span><span class="sxs-lookup"><span data-stu-id="45628-103">JsRuntimeHandle Typedef</span></span>

<span data-ttu-id="45628-104">Identificador para un tiempo de ejecución de Chakra.</span><span class="sxs-lookup"><span data-stu-id="45628-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="45628-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45628-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="45628-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45628-106">Remarks</span></span>  
 <span data-ttu-id="45628-107">Cada tiempo de ejecución de Chakra tiene su propio motor de ejecución independiente, compilador JIT y montón recolectado de basura.</span><span class="sxs-lookup"><span data-stu-id="45628-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="45628-108">Como tal, cada Runtime está completamente aislado de otros runtimes.</span><span class="sxs-lookup"><span data-stu-id="45628-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="45628-109">Los Runtimes se pueden usar en cualquier subproceso, pero solo un subproceso puede llamar a tiempo de ejecución en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="45628-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="45628-110">Un JsRuntimeHandle, a diferencia de otras referencias de objeto de la API de hospedaje de Chakra, no se ha recolectado como no utilizado porque contiene el montón recolectado de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="45628-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="45628-111">Un tiempo de ejecución continuará existiendo hasta que se llame a JsDisposeRuntime.</span><span class="sxs-lookup"><span data-stu-id="45628-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="45628-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45628-112">Requirements</span></span>  
 <span data-ttu-id="45628-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="45628-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="45628-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="45628-114">See Also</span></span>  
 [<span data-ttu-id="45628-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="45628-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
