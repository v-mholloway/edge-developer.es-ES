---
description: Desenvuelve un objeto de JavaScript en un `IInspectable` puntero.
title: Función JsObjectToInspectable | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7127e1cf1372020e0df00b81ed172739379426f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574556"
---
# <span data-ttu-id="d96cd-103">Función JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="d96cd-103">JsObjectToInspectable Function</span></span>
<span data-ttu-id="d96cd-104">Desenvuelve un objeto de JavaScript en un `IInspectable` puntero.</span><span class="sxs-lookup"><span data-stu-id="d96cd-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="d96cd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d96cd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="d96cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d96cd-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="d96cd-107">Un valor de JavaScript al que se debe proyectar `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="d96cd-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="d96cd-108">Un `IInspectable` valor del objeto.</span><span class="sxs-lookup"><span data-stu-id="d96cd-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="d96cd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d96cd-109">Return Value</span></span>  
 <span data-ttu-id="d96cd-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="d96cd-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d96cd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d96cd-111">Remarks</span></span>  
 <span data-ttu-id="d96cd-112">Los hosts son responsables de exigir reglas de subprocesamiento COM.</span><span class="sxs-lookup"><span data-stu-id="d96cd-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="d96cd-113">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="d96cd-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d96cd-114">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d96cd-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="d96cd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d96cd-115">Requirements</span></span>  
 <span data-ttu-id="d96cd-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d96cd-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d96cd-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d96cd-117">See Also</span></span>  
 [<span data-ttu-id="d96cd-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d96cd-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)