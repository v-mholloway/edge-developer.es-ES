---
description: Una devolución de llamada del finalizador.
title: JsFinalizeCallback typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 794edbb3a61c8c213c0908740ed0a867488a2c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236211"
---
# <span data-ttu-id="4b543-103">Definición de tipo JsFinalizeCallback</span><span class="sxs-lookup"><span data-stu-id="4b543-103">JsFinalizeCallback Typedef</span></span>

<span data-ttu-id="4b543-104">Una devolución de llamada del finalizador.</span><span class="sxs-lookup"><span data-stu-id="4b543-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="4b543-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b543-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="4b543-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b543-106">Parameters</span></span>  
 <span data-ttu-id="4b543-107">data</span><span class="sxs-lookup"><span data-stu-id="4b543-107">data</span></span>  
 <span data-ttu-id="4b543-108">Datos externos que se han pasado al crear el objeto que se estaba finalizando.</span><span class="sxs-lookup"><span data-stu-id="4b543-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="4b543-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b543-109">Requirements</span></span>  
 <span data-ttu-id="4b543-110">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4b543-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4b543-111">Consulta también</span><span class="sxs-lookup"><span data-stu-id="4b543-111">See Also</span></span>  
 [<span data-ttu-id="4b543-112">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4b543-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
