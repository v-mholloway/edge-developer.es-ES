---
description: Obtiene el nombre asociado al identificador de propiedad.
title: Función JsGetPropertyNameFromId | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 42061ab54a70fed571740961a909a6da17fb0733
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236292"
---
# <span data-ttu-id="05432-103">Función JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="05432-103">JsGetPropertyNameFromId Function</span></span>

<span data-ttu-id="05432-104">Obtiene el nombre asociado al identificador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="05432-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="05432-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05432-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="05432-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05432-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="05432-107">IDENTIFICADOR de propiedad para obtener el nombre.</span><span class="sxs-lookup"><span data-stu-id="05432-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="05432-108">Nombre asociado al identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="05432-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="05432-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05432-109">Return Value</span></span>  
 <span data-ttu-id="05432-110">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="05432-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="05432-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05432-111">Remarks</span></span>  
 <span data-ttu-id="05432-112">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="05432-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="05432-113">El búfer devuelto es válido siempre que el Runtime esté activo y no se pueda usar una vez que el Runtime se haya eliminado.</span><span class="sxs-lookup"><span data-stu-id="05432-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="05432-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05432-114">Requirements</span></span>  
 <span data-ttu-id="05432-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="05432-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="05432-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="05432-116">See Also</span></span>  
 [<span data-ttu-id="05432-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="05432-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
