---
description: Devuelve un valor que indica si un objeto es extensible o no.
title: Función JsGetExtensionAllowed | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3baa6449294f7b055251d861a32095deb1bdfe9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573459"
---
# <span data-ttu-id="c051c-103">Función JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="c051c-103">JsGetExtensionAllowed Function</span></span>
<span data-ttu-id="c051c-104">Devuelve un valor que indica si un objeto es extensible o no.</span><span class="sxs-lookup"><span data-stu-id="c051c-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="c051c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c051c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="c051c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c051c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="c051c-107">Objeto que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="c051c-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="c051c-108">Si el objeto es extensible o no.</span><span class="sxs-lookup"><span data-stu-id="c051c-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="c051c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c051c-109">Return Value</span></span>  
 <span data-ttu-id="c051c-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c051c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c051c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c051c-111">Remarks</span></span>  
 <span data-ttu-id="c051c-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="c051c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c051c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c051c-113">Requirements</span></span>  
 <span data-ttu-id="c051c-114">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c051c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c051c-115">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c051c-115">See Also</span></span>  
 [<span data-ttu-id="c051c-116">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c051c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)