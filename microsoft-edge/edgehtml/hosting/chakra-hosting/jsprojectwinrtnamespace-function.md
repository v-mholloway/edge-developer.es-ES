---
description: Proyectar un espacio de nombres WinRT.
title: Función JsProjectWinRTNamespace | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f781cf90aaec68b2bd305bf34c453fc663ad0187
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236645"
---
# <span data-ttu-id="0ed63-103">Función JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="0ed63-103">JsProjectWinRTNamespace Function</span></span>

<span data-ttu-id="0ed63-104">Proyectar un espacio de nombres WinRT.</span><span class="sxs-lookup"><span data-stu-id="0ed63-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="0ed63-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ed63-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="0ed63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ed63-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="0ed63-107">El espacio de nombres WinRT que se va a proyectar.</span><span class="sxs-lookup"><span data-stu-id="0ed63-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="0ed63-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ed63-108">Return Value</span></span>  
 <span data-ttu-id="0ed63-109">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="0ed63-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0ed63-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ed63-110">Remarks</span></span>  
 <span data-ttu-id="0ed63-111">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="0ed63-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="0ed63-112">Esta API solo se admite en el modo EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="0ed63-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0ed63-113">WinRT era el nombre de la plataforma antes de la plataforma universal de Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="0ed63-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="0ed63-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ed63-114">Requirements</span></span>  
 <span data-ttu-id="0ed63-115">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0ed63-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0ed63-116">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0ed63-116">See Also</span></span>  
 [<span data-ttu-id="0ed63-117">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0ed63-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
