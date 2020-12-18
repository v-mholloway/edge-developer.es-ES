---
description: Una referencia a un objeto perteneciente al recolector de elementos no utilizados de Chakra.
title: JsRef typedef | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 69d13472b15b5d448908b5dafb2e3d7dc0ace7e4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235904"
---
# <span data-ttu-id="dbc25-103">Definición de tipo JsRef</span><span class="sxs-lookup"><span data-stu-id="dbc25-103">JsRef Typedef</span></span>

<span data-ttu-id="dbc25-104">Una referencia a un objeto perteneciente al recolector de elementos no utilizados de Chakra.</span><span class="sxs-lookup"><span data-stu-id="dbc25-104">A reference to an object owned by the Chakra garbage collector.</span></span>  
  
## <span data-ttu-id="dbc25-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dbc25-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRef;  
```  
  
## <span data-ttu-id="dbc25-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dbc25-106">Remarks</span></span>  
 <span data-ttu-id="dbc25-107">Un tiempo de ejecución de Chakra realizará un seguimiento automático de las referencias de JsRef siempre que estén almacenadas en variables locales o en parámetros (es decir, en la pila).</span><span class="sxs-lookup"><span data-stu-id="dbc25-107">A Chakra runtime will automatically track JsRef references as long as they are on stored in local variables or in parameters (i.e. on the stack).</span></span> <span data-ttu-id="dbc25-108">Almacenar un JsRef en cualquier lugar que no sea en la pila requiere llamar a JsAddRef y JsRelease para administrar la duración del objeto; de lo contrario, el recolector de elementos no utilizados puede liberar el objeto mientras aún está en uso.</span><span class="sxs-lookup"><span data-stu-id="dbc25-108">Storing a JsRef somewhere other than on the stack requires calling JsAddRef and JsRelease to manage the lifetime of the object, otherwise the garbage collector may free the object while it is still in use.</span></span>  
  
## <span data-ttu-id="dbc25-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc25-109">Requirements</span></span>  
 <span data-ttu-id="dbc25-110">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dbc25-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dbc25-111">Consulta también</span><span class="sxs-lookup"><span data-stu-id="dbc25-111">See Also</span></span>  
 [<span data-ttu-id="dbc25-112">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dbc25-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
