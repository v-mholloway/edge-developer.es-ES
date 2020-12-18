---
description: Analiza un script y devuelve una función que representa el script.
title: Función JsParseScript | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 656d9a992868a3cb892808775f160092b8eaf069
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236413"
---
# <span data-ttu-id="aca63-103">Función JsParseScript</span><span class="sxs-lookup"><span data-stu-id="aca63-103">JsParseScript Function</span></span>

<span data-ttu-id="aca63-104">Analiza un script y devuelve una función que representa el script.</span><span class="sxs-lookup"><span data-stu-id="aca63-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="aca63-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aca63-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="aca63-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aca63-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="aca63-107">Script que se va a analizar.</span><span class="sxs-lookup"><span data-stu-id="aca63-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="aca63-108">Una cookie que identifica el script que puede ser usado por contextos de scripts depurables.</span><span class="sxs-lookup"><span data-stu-id="aca63-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="aca63-109">La ubicación de la que procede la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="aca63-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="aca63-110">Una función que representa el código de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="aca63-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="aca63-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aca63-111">Return Value</span></span>  
 <span data-ttu-id="aca63-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="aca63-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="aca63-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aca63-113">Remarks</span></span>  
 <span data-ttu-id="aca63-114">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="aca63-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="aca63-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aca63-115">Requirements</span></span>  
 <span data-ttu-id="aca63-116">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aca63-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aca63-117">Consulta también</span><span class="sxs-lookup"><span data-stu-id="aca63-117">See Also</span></span>  
 [<span data-ttu-id="aca63-118">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="aca63-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
