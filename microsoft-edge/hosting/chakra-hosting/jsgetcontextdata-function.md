---
description: Obtiene el conjunto de datos internos en JsrtContext.
title: Función JsGetContextData | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd85ccbc4008897643ec3840e8cdeca3611a50c8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573469"
---
# <span data-ttu-id="7114b-103">Función JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="7114b-103">JsGetContextData Function</span></span>
<span data-ttu-id="7114b-104">Obtiene el conjunto de datos internos en JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="7114b-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="7114b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7114b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="7114b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7114b-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="7114b-107">Contexto del que se van a obtener los datos.</span><span class="sxs-lookup"><span data-stu-id="7114b-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="7114b-108">Puntero a los datos en los que se devolverán los datos.</span><span class="sxs-lookup"><span data-stu-id="7114b-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="7114b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7114b-109">Return Value</span></span>  
 <span data-ttu-id="7114b-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="7114b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7114b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7114b-111">Remarks</span></span>  
 <span data-ttu-id="7114b-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="7114b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7114b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7114b-113">Requirements</span></span>  
 <span data-ttu-id="7114b-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7114b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7114b-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="7114b-115">See Also</span></span>  
 [<span data-ttu-id="7114b-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7114b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)