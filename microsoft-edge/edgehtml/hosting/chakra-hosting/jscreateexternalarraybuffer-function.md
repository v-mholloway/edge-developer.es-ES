---
description: Crea un objeto de JavaScript `ArrayBuffer` para obtener acceso a la memoria externa.
title: Función JsCreateExternalArrayBuffer | Microsoft docs
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 78c0d3c8b298876358f247c86a488b6f10e52c6d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236469"
---
# <span data-ttu-id="9dc97-103">Función JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="9dc97-103">JsCreateExternalArrayBuffer Function</span></span>

<span data-ttu-id="9dc97-104">Crea un objeto de JavaScript `ArrayBuffer` para obtener acceso a la memoria externa.</span><span class="sxs-lookup"><span data-stu-id="9dc97-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="9dc97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9dc97-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="9dc97-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9dc97-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="9dc97-107">Puntero a la memoria externa.</span><span class="sxs-lookup"><span data-stu-id="9dc97-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="9dc97-108">El número de bytes de la memoria externa.</span><span class="sxs-lookup"><span data-stu-id="9dc97-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="9dc97-109">Una devolución de llamada para cuando el objeto está finalizado.</span><span class="sxs-lookup"><span data-stu-id="9dc97-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="9dc97-110">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="9dc97-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="9dc97-111">El estado proporcionado por el usuario que se devolverá a finalizeCallback.</span><span class="sxs-lookup"><span data-stu-id="9dc97-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="9dc97-112">El `ArrayBuffer` objeto nuevo.</span><span class="sxs-lookup"><span data-stu-id="9dc97-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="9dc97-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9dc97-113">Return Value</span></span>  
 <span data-ttu-id="9dc97-114">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="9dc97-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9dc97-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9dc97-115">Remarks</span></span>  
 <span data-ttu-id="9dc97-116">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="9dc97-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="9dc97-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dc97-117">Requirements</span></span>  
 <span data-ttu-id="9dc97-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9dc97-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9dc97-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="9dc97-119">See Also</span></span>  
 [<span data-ttu-id="9dc97-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9dc97-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
