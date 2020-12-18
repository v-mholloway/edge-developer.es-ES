---
description: Obtiene el conjunto de datos internos en JsrtContext.
title: Función JsGetContextData | Microsoft docs
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8f5f70a9c36fea355792050c1a2a810bca2d07b3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236203"
---
# <span data-ttu-id="b74e3-103">Función JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="b74e3-103">JsGetContextData Function</span></span>

<span data-ttu-id="b74e3-104">Obtiene el conjunto de datos internos en JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="b74e3-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="b74e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b74e3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="b74e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b74e3-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="b74e3-107">Contexto del que se van a obtener los datos.</span><span class="sxs-lookup"><span data-stu-id="b74e3-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="b74e3-108">Puntero a los datos en los que se devolverán los datos.</span><span class="sxs-lookup"><span data-stu-id="b74e3-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="b74e3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b74e3-109">Return Value</span></span>  
 <span data-ttu-id="b74e3-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="b74e3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b74e3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b74e3-111">Remarks</span></span>  
 <span data-ttu-id="b74e3-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="b74e3-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b74e3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b74e3-113">Requirements</span></span>  
 <span data-ttu-id="b74e3-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b74e3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b74e3-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="b74e3-115">See Also</span></span>  
 [<span data-ttu-id="b74e3-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b74e3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
