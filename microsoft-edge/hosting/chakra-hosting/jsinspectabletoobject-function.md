---
description: Crea un valor de JavaScript que es una proyección del puntero pasado `IInspectable` .
title: Función JsInspectableToObject | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 26ce17eb3abcefcf9a1f0cc773e9fe4c3aaf05cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573434"
---
# <span data-ttu-id="8c23c-103">Función JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="8c23c-103">JsInspectableToObject Function</span></span>
<span data-ttu-id="8c23c-104">Crea un valor de JavaScript que es una proyección del puntero pasado `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="8c23c-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="8c23c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c23c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="8c23c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c23c-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="8c23c-107">`IInspectable`A para que se proyecte.</span><span class="sxs-lookup"><span data-stu-id="8c23c-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="8c23c-108">Un valor de JavaScript que es una proyección del `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="8c23c-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="8c23c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c23c-109">Return Value</span></span>  
 <span data-ttu-id="8c23c-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="8c23c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8c23c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c23c-111">Remarks</span></span>  
 <span data-ttu-id="8c23c-112">El script puede usar el valor previsto para llamar a un objeto de WinRT.</span><span class="sxs-lookup"><span data-stu-id="8c23c-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="8c23c-113">Los hosts son responsables de exigir reglas de subprocesamiento COM.</span><span class="sxs-lookup"><span data-stu-id="8c23c-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="8c23c-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="8c23c-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="8c23c-115">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="8c23c-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="8c23c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c23c-116">Requirements</span></span>  
 <span data-ttu-id="8c23c-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8c23c-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8c23c-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="8c23c-118">See Also</span></span>  
 [<span data-ttu-id="8c23c-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8c23c-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)