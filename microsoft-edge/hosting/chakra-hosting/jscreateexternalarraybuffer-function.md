---
description: Crea un objeto de JavaScript `ArrayBuffer` para obtener acceso a la memoria externa.
title: Función JsCreateExternalArrayBuffer | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573501"
---
# <span data-ttu-id="4f6dd-103">Función JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="4f6dd-103">JsCreateExternalArrayBuffer Function</span></span>
<span data-ttu-id="4f6dd-104">Crea un objeto de JavaScript `ArrayBuffer` para obtener acceso a la memoria externa.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="4f6dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f6dd-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="4f6dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f6dd-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="4f6dd-107">Puntero a la memoria externa.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="4f6dd-108">El número de bytes de la memoria externa.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="4f6dd-109">Una devolución de llamada para cuando el objeto está finalizado.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="4f6dd-110">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="4f6dd-111">El estado proporcionado por el usuario que se devolverá a finalizeCallback.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="4f6dd-112">El `ArrayBuffer` objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="4f6dd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f6dd-113">Return Value</span></span>  
 <span data-ttu-id="4f6dd-114">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4f6dd-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f6dd-115">Remarks</span></span>  
 <span data-ttu-id="4f6dd-116">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="4f6dd-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4f6dd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f6dd-117">Requirements</span></span>  
 <span data-ttu-id="4f6dd-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4f6dd-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4f6dd-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="4f6dd-119">See Also</span></span>  
 [<span data-ttu-id="4f6dd-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4f6dd-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)