---
description: Identificador para un tiempo de ejecución de Chakra.
title: JsRuntimeHandle typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574524"
---
# <span data-ttu-id="3d25c-103">JsRuntimeHandle typedef</span><span class="sxs-lookup"><span data-stu-id="3d25c-103">JsRuntimeHandle Typedef</span></span>
<span data-ttu-id="3d25c-104">Identificador para un tiempo de ejecución de Chakra.</span><span class="sxs-lookup"><span data-stu-id="3d25c-104">A handle to a Chakra runtime.</span></span>  
  
## <span data-ttu-id="3d25c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d25c-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## <span data-ttu-id="3d25c-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d25c-106">Remarks</span></span>  
 <span data-ttu-id="3d25c-107">Cada tiempo de ejecución de Chakra tiene su propio motor de ejecución independiente, compilador JIT y montón recolectado de basura.</span><span class="sxs-lookup"><span data-stu-id="3d25c-107">Each Chakra runtime has its own independent execution engine, JIT compiler, and garbage collected heap.</span></span> <span data-ttu-id="3d25c-108">Como tal, cada Runtime está completamente aislado de otros runtimes.</span><span class="sxs-lookup"><span data-stu-id="3d25c-108">As such, each runtime is completely isolated from other runtimes.</span></span>  
  
 <span data-ttu-id="3d25c-109">Los Runtimes se pueden usar en cualquier subproceso, pero solo un subproceso puede llamar a tiempo de ejecución en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="3d25c-109">Runtimes can be used on any thread, but only one thread can call into a runtime at any time.</span></span>  
  
> [!WARNING]
>  <span data-ttu-id="3d25c-110">Un JsRuntimeHandle, a diferencia de otras referencias de objeto de la API de hospedaje de Chakra, no se ha recolectado como no utilizado porque contiene el montón recolectado de elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="3d25c-110">A JsRuntimeHandle, unlike other object references in the Chakra hosting API, is not garbage collected since it contains the garbage collected heap itself.</span></span> <span data-ttu-id="3d25c-111">Un tiempo de ejecución continuará existiendo hasta que se llame a JsDisposeRuntime.</span><span class="sxs-lookup"><span data-stu-id="3d25c-111">A runtime will continue to exist until JsDisposeRuntime is called.</span></span>  
  
## <span data-ttu-id="3d25c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d25c-112">Requirements</span></span>  
 <span data-ttu-id="3d25c-113">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3d25c-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3d25c-114">Consulta también</span><span class="sxs-lookup"><span data-stu-id="3d25c-114">See Also</span></span>  
 [<span data-ttu-id="3d25c-115">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3d25c-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)