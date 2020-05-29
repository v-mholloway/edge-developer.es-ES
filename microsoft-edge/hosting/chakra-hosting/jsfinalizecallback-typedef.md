---
description: Una devolución de llamada del finalizador.
title: JsFinalizeCallback typedef | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d2ee2c2c11e85094010cd15be59aa7ac587b614f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574600"
---
# <span data-ttu-id="57a9c-103">JsFinalizeCallback typedef</span><span class="sxs-lookup"><span data-stu-id="57a9c-103">JsFinalizeCallback Typedef</span></span>
<span data-ttu-id="57a9c-104">Una devolución de llamada del finalizador.</span><span class="sxs-lookup"><span data-stu-id="57a9c-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="57a9c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57a9c-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="57a9c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57a9c-106">Parameters</span></span>  
 <span data-ttu-id="57a9c-107">data</span><span class="sxs-lookup"><span data-stu-id="57a9c-107">data</span></span>  
 <span data-ttu-id="57a9c-108">Datos externos que se han pasado al crear el objeto que se estaba finalizando.</span><span class="sxs-lookup"><span data-stu-id="57a9c-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="57a9c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a9c-109">Requirements</span></span>  
 <span data-ttu-id="57a9c-110">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="57a9c-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="57a9c-111">Consulta también</span><span class="sxs-lookup"><span data-stu-id="57a9c-111">See Also</span></span>  
 [<span data-ttu-id="57a9c-112">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="57a9c-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)