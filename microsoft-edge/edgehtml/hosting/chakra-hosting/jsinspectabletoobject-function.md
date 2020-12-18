---
description: Crea un valor de JavaScript que es una proyección del puntero pasado `IInspectable` .
title: Función JsInspectableToObject | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236462"
---
# <span data-ttu-id="76557-103">Función JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="76557-103">JsInspectableToObject Function</span></span>

<span data-ttu-id="76557-104">Crea un valor de JavaScript que es una proyección del puntero pasado `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="76557-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="76557-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76557-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="76557-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76557-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="76557-107">`IInspectable`A para que se proyecte.</span><span class="sxs-lookup"><span data-stu-id="76557-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="76557-108">Un valor de JavaScript que es una proyección del `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="76557-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="76557-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76557-109">Return Value</span></span>  
 <span data-ttu-id="76557-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="76557-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="76557-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76557-111">Remarks</span></span>  
 <span data-ttu-id="76557-112">El script puede usar el valor previsto para llamar a un objeto de WinRT.</span><span class="sxs-lookup"><span data-stu-id="76557-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="76557-113">Los hosts son responsables de exigir reglas de subprocesamiento COM.</span><span class="sxs-lookup"><span data-stu-id="76557-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="76557-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="76557-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="76557-115">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="76557-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="76557-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76557-116">Requirements</span></span>  
 <span data-ttu-id="76557-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="76557-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="76557-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="76557-118">See Also</span></span>  
 [<span data-ttu-id="76557-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="76557-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
