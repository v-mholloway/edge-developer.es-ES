---
description: Serializa una secuencia de comandos analizada en un búfer del que se puede volver a usar.
title: Función JsSerializeScript | Microsoft docs
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 236cf40c91256e999d5390acd395b1e97fe538ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236588"
---
# <span data-ttu-id="11c90-103">Función JsSerializeScript</span><span class="sxs-lookup"><span data-stu-id="11c90-103">JsSerializeScript Function</span></span>

<span data-ttu-id="11c90-104">Serializa una secuencia de comandos analizada en un búfer del que se puede volver a usar.</span><span class="sxs-lookup"><span data-stu-id="11c90-104">Serializes a parsed script to a buffer than can be reused.</span></span>  
  
## <span data-ttu-id="11c90-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11c90-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### <span data-ttu-id="11c90-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11c90-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="11c90-107">Script que se va a serializar.</span><span class="sxs-lookup"><span data-stu-id="11c90-107">The script to serialize.</span></span>  
  
 `buffer`  
 <span data-ttu-id="11c90-108">El búfer en el que se coloca el script serializado.</span><span class="sxs-lookup"><span data-stu-id="11c90-108">The buffer to put the serialized script into.</span></span> <span data-ttu-id="11c90-109">Puede ser null.</span><span class="sxs-lookup"><span data-stu-id="11c90-109">Can be null.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="11c90-110">En la entrada, el tamaño del búfer, en bytes; al salir, el tamaño del búfer, en bytes, necesario para mantener el script serializado.</span><span class="sxs-lookup"><span data-stu-id="11c90-110">On entry, the size of the buffer, in bytes; on exit, the size of the buffer, in bytes, required to hold the serialized script.</span></span>  
  
## <span data-ttu-id="11c90-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11c90-111">Return Value</span></span>  
 <span data-ttu-id="11c90-112">El código `JsNoError` si la operación se realizó correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="11c90-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="11c90-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11c90-113">Remarks</span></span>  
 `JsSerializeScript` <span data-ttu-id="11c90-114">analiza un script y, a continuación, almacena el formulario analizado de la secuencia de comandos en un formato independiente del tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="11c90-114">parses a script and then stores the parsed form of the script in a runtime-independent format.</span></span> <span data-ttu-id="11c90-115">El script serializado se puede deserializar en cualquier Runtime sin necesidad de volver a analizar el script.</span><span class="sxs-lookup"><span data-stu-id="11c90-115">The serialized script then can be deserialized in any runtime without requiring the script to be re-parsed.</span></span>  
  
 <span data-ttu-id="11c90-116">Requiere un contexto de script activo.</span><span class="sxs-lookup"><span data-stu-id="11c90-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="11c90-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c90-117">Requirements</span></span>  
 <span data-ttu-id="11c90-118">**Encabezado:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="11c90-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="11c90-119">Consulta también</span><span class="sxs-lookup"><span data-stu-id="11c90-119">See Also</span></span>  
 [<span data-ttu-id="11c90-120">Referencia (tiempo de ejecución de JavaScript)</span><span class="sxs-lookup"><span data-stu-id="11c90-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
