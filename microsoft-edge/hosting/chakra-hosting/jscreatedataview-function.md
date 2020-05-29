---
description: Crea un objeto de JavaScript `DataView` .
title: Función JsCreateDataView | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573507"
---
# <span data-ttu-id="95a96-103">Función JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="95a96-103">JsCreateDataView Function</span></span>
<span data-ttu-id="95a96-104">Crea un objeto de JavaScript `DataView` .</span><span class="sxs-lookup"><span data-stu-id="95a96-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="95a96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95a96-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="95a96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95a96-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="95a96-107">Objeto existente `ArrayBuffer` para usar como almacenamiento para el objeto de resultado `DataView` .</span><span class="sxs-lookup"><span data-stu-id="95a96-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="95a96-108">Desplazamiento en bytes desde el inicio de `arrayBuffer` para el resultado `DataView` a la referencia.</span><span class="sxs-lookup"><span data-stu-id="95a96-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="95a96-109">El número de bytes en el ArrayBuffer de resultado de DataView al que hacer referencia.</span><span class="sxs-lookup"><span data-stu-id="95a96-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="95a96-110">Nuevo objeto DataView.</span><span class="sxs-lookup"><span data-stu-id="95a96-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="95a96-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95a96-111">Return Value</span></span>  
 <span data-ttu-id="95a96-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="95a96-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="95a96-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95a96-113">Remarks</span></span>  
 <span data-ttu-id="95a96-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="95a96-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="95a96-115">Esta API solo se admite en el modo Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="95a96-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="95a96-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a96-116">Requirements</span></span>  
 <span data-ttu-id="95a96-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="95a96-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="95a96-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="95a96-118">See Also</span></span>  
 [<span data-ttu-id="95a96-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="95a96-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)