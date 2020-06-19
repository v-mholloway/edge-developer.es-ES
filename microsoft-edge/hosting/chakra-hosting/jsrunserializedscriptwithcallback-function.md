---
description: Ejecuta una secuencia de comandos serializada. Proporciona la capacidad de cargar de forma diferida el origen del script solo si se necesita o cuando lo necesite.
title: Función JsRunSerializedScriptWithCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84a74d3c1aa68469dfe2fe42fdee685faa4c358c
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752223"
---
# <span data-ttu-id="f5607-104">Función JsRunSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="f5607-104">JsRunSerializedScriptWithCallback Function</span></span>
<span data-ttu-id="f5607-105">Ejecuta una secuencia de comandos serializada.</span><span class="sxs-lookup"><span data-stu-id="f5607-105">Runs a serialized script.</span></span> <span data-ttu-id="f5607-106">Proporciona la capacidad de cargar de forma diferida el origen del script solo si se necesita o cuando lo necesite.</span><span class="sxs-lookup"><span data-stu-id="f5607-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="f5607-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5607-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="f5607-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5607-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="f5607-109">Devolución de llamada llamada cuando es necesario cargar el código fuente del script.</span><span class="sxs-lookup"><span data-stu-id="f5607-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="f5607-110">Devolución de llamada llamada cuando ya no se necesita el script y el código de origen serializados.</span><span class="sxs-lookup"><span data-stu-id="f5607-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="f5607-111">El script serializado.</span><span class="sxs-lookup"><span data-stu-id="f5607-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="f5607-112">Una cookie que identifica el script que puede ser usado por contextos de scripts depurables.</span><span class="sxs-lookup"><span data-stu-id="f5607-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="f5607-113">Este contexto se transmitirá a scriptLoadCallback y scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="f5607-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="f5607-114">La ubicación de la que procede la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="f5607-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="f5607-115">El resultado de ejecutar el script, si existe.</span><span class="sxs-lookup"><span data-stu-id="f5607-115">The result of running the script, if any.</span></span> <span data-ttu-id="f5607-116">Este parámetro puede ser null.</span><span class="sxs-lookup"><span data-stu-id="f5607-116">This parameter can be null.</span></span>  
  
## <span data-ttu-id="f5607-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5607-117">Return Value</span></span>  
 <span data-ttu-id="f5607-118">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="f5607-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f5607-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5607-119">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f5607-120">Esta API aún no está disponible para las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="f5607-120">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="f5607-121">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="f5607-121">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f5607-122">El motor en tiempo de ejecución retendrá el búfer hasta que se hayan recolectado como no utilizados todas las instancias de las funciones creadas desde el búfer.</span><span class="sxs-lookup"><span data-stu-id="f5607-122">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="f5607-123">A continuación, llamará a scriptUnloadCallback para informar al autor de la llamada de que es seguro liberarlo.</span><span class="sxs-lookup"><span data-stu-id="f5607-123">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="f5607-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5607-124">Requirements</span></span>  
 <span data-ttu-id="f5607-125">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f5607-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f5607-126">Consulta también</span><span class="sxs-lookup"><span data-stu-id="f5607-126">See Also</span></span>  
 [<span data-ttu-id="f5607-127">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f5607-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)