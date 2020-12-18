---
description: Ejecuta un script.
title: Función JsRunScript | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunScript
helpviewer_keywords:
- JsRunScript function
ms.assetid: 8d6b8c9a-af3a-4e21-a330-5a6b535423a3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d61771991e1d22a9d71a928d785390b814a992a8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236576"
---
# <span data-ttu-id="c83ca-103">Función JsRunScript</span><span class="sxs-lookup"><span data-stu-id="c83ca-103">JsRunScript Function</span></span>

<span data-ttu-id="c83ca-104">Ejecuta un script.</span><span class="sxs-lookup"><span data-stu-id="c83ca-104">Executes a script.</span></span>  
  
## <span data-ttu-id="c83ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c83ca-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="c83ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c83ca-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="c83ca-107">Secuencia de comandos que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="c83ca-107">The script to run.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="c83ca-108">Una cookie que identifica el script que puede ser usado por contextos de scripts depurables.</span><span class="sxs-lookup"><span data-stu-id="c83ca-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="c83ca-109">La ubicación de la que procede la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="c83ca-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="c83ca-110">El resultado del script, si existe.</span><span class="sxs-lookup"><span data-stu-id="c83ca-110">The result of the script, if any.</span></span> <span data-ttu-id="c83ca-111">Este parámetro puede ser null.</span><span class="sxs-lookup"><span data-stu-id="c83ca-111">This parameter can be null.</span></span>  
  
## <span data-ttu-id="c83ca-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c83ca-112">Return Value</span></span>  
 <span data-ttu-id="c83ca-113">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="c83ca-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c83ca-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c83ca-114">Remarks</span></span>  
 <span data-ttu-id="c83ca-115">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="c83ca-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c83ca-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c83ca-116">Requirements</span></span>  
 <span data-ttu-id="c83ca-117">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c83ca-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c83ca-118">Consulta también</span><span class="sxs-lookup"><span data-stu-id="c83ca-118">See Also</span></span>  
 [<span data-ttu-id="c83ca-119">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c83ca-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
