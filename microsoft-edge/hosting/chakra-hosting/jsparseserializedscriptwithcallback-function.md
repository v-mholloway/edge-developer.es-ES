---
description: Analiza una secuencia de comandos serializada y devuelve una función que representa el script. Proporciona la capacidad de cargar de forma diferida el origen del script solo si se necesita o cuando lo necesite.
title: Función JsParseSerializedScriptWithCallback | Microsoft docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ad6d635722f0b3fea8b19f8d16679b402d1fd56e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574548"
---
# <span data-ttu-id="577a7-104">Función JsParseSerializedScriptWithCallback</span><span class="sxs-lookup"><span data-stu-id="577a7-104">JsParseSerializedScriptWithCallback Function</span></span>
<span data-ttu-id="577a7-105">Analiza una secuencia de comandos serializada y devuelve una función que representa el script.</span><span class="sxs-lookup"><span data-stu-id="577a7-105">Parses a serialized script and returns a function representing the script.</span></span> <span data-ttu-id="577a7-106">Proporciona la capacidad de cargar de forma diferida el origen del script solo si se necesita o cuando lo necesite.</span><span class="sxs-lookup"><span data-stu-id="577a7-106">Provides the ability to lazy load the script source only if/when it is needed.</span></span>  
  
## <span data-ttu-id="577a7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="577a7-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
);  
  
```  
  
#### <span data-ttu-id="577a7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="577a7-108">Parameters</span></span>  
 `scriptLoadCallback`  
 <span data-ttu-id="577a7-109">Devolución de llamada llamada cuando es necesario cargar el código fuente del script.</span><span class="sxs-lookup"><span data-stu-id="577a7-109">Callback called when the source code of the script needs to be loaded.</span></span>  
  
 `scriptUnloadCallback`  
 <span data-ttu-id="577a7-110">Devolución de llamada llamada cuando ya no se necesita el script y el código de origen serializados.</span><span class="sxs-lookup"><span data-stu-id="577a7-110">Callback called when the serialized script and source code are no longer needed.</span></span>  
  
 `buffer`  
 <span data-ttu-id="577a7-111">El script serializado.</span><span class="sxs-lookup"><span data-stu-id="577a7-111">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="577a7-112">Una cookie que identifica el script que puede ser usado por contextos de scripts depurables.</span><span class="sxs-lookup"><span data-stu-id="577a7-112">A cookie identifying the script that can be used by debuggable script contexts.</span></span>     <span data-ttu-id="577a7-113">Este contexto se transmitirá a scriptLoadCallback y scriptUnloadCallback.</span><span class="sxs-lookup"><span data-stu-id="577a7-113">This context will passed into scriptLoadCallback and scriptUnloadCallback.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="577a7-114">La ubicación de la que procede la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="577a7-114">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="577a7-115">Una función que representa el código de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="577a7-115">A function representing the script code.</span></span>  
  
## <span data-ttu-id="577a7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="577a7-116">Return Value</span></span>  
 <span data-ttu-id="577a7-117">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="577a7-117">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="577a7-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="577a7-118">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="577a7-119">Esta API aún no está disponible para las aplicaciones de la tienda.</span><span class="sxs-lookup"><span data-stu-id="577a7-119">This API is not yet available for Store apps.</span></span>  
  
 <span data-ttu-id="577a7-120">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="577a7-120">Requires an active script context.</span></span>  
  
 <span data-ttu-id="577a7-121">El motor en tiempo de ejecución retendrá el búfer hasta que se hayan recolectado como no utilizados todas las instancias de las funciones creadas desde el búfer.</span><span class="sxs-lookup"><span data-stu-id="577a7-121">The runtime will hold on to the buffer until all instances of any functions created from     the buffer are garbage collected.</span></span>  <span data-ttu-id="577a7-122">A continuación, llamará a scriptUnloadCallback para informar al autor de la llamada de que es seguro liberarlo.</span><span class="sxs-lookup"><span data-stu-id="577a7-122">It will then call scriptUnloadCallback to inform the     caller that it is safe to release.</span></span>  
  
## <span data-ttu-id="577a7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="577a7-123">Requirements</span></span>  
 <span data-ttu-id="577a7-124">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="577a7-124">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="577a7-125">Consulta también</span><span class="sxs-lookup"><span data-stu-id="577a7-125">See Also</span></span>  
 [<span data-ttu-id="577a7-126">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="577a7-126">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)