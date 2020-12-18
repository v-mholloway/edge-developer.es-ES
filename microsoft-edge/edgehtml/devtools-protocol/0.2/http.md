---
description: El protocolo Microsoft Edge DevTools versión 0,2 admite los siguientes puntos de conexión HTTP.
title: Puntos de conexión HTTP de Microsoft Edge DevTools Protocol, versión 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a0e100cee6a73d688b9b74a9b38d1dd37722428f
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236338"
---
# <span data-ttu-id="39edb-103">Puntos de conexión HTTP de Microsoft Edge DevTools Protocol, versión 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="39edb-103">Microsoft Edge DevTools Protocol Version 0.2 HTTP Endpoints (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="39edb-104">La versión 0,2 del protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de octubre de 2018]() y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="39edb-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update]() and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="39edb-105">El **Protocolo DevTools 0,2** admite los siguientes puntos de conexión http.</span><span class="sxs-lookup"><span data-stu-id="39edb-105">**DevTools Protocol 0.2** supports the following HTTP endpoints.</span></span> <span data-ttu-id="39edb-106">Vea [usar el protocolo](../index.md#using-the-protocol) para obtener más información sobre la conexión a un proceso de contenido del explorador y la documentación de [dominios](domains/index.md) para la API de protocolo de DevTools basada en sockets completo.</span><span class="sxs-lookup"><span data-stu-id="39edb-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="39edb-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="39edb-107">/json/version</span></span>
<span data-ttu-id="39edb-108">Proporciona información sobre el explorador del equipo host y la versión del protocolo DevTools que admite.</span><span class="sxs-lookup"><span data-stu-id="39edb-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="39edb-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="39edb-109">Parameters</span></span>**

*<span data-ttu-id="39edb-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="39edb-110">None</span></span>*

**<span data-ttu-id="39edb-111">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="39edb-111">Return object</span></span>**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
}
```

## <span data-ttu-id="39edb-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="39edb-112">/json/protocol</span></span>

<span data-ttu-id="39edb-113">Proporciona toda la superficie de la API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="39edb-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="39edb-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="39edb-114">Parameters</span></span>**

*<span data-ttu-id="39edb-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="39edb-115">None</span></span>*

**<span data-ttu-id="39edb-116">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="39edb-116">Return object</span></span>**

<span data-ttu-id="39edb-117">Objeto JSON que representa la superficie de API disponible para la versión actual del protocolo.</span><span class="sxs-lookup"><span data-stu-id="39edb-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="39edb-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="39edb-118">/json/list</span></span>

<span data-ttu-id="39edb-119">Proporciona una lista de candidatos de los destinos de página para la depuración.</span><span class="sxs-lookup"><span data-stu-id="39edb-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="39edb-120">Parameters</span><span class="sxs-lookup"><span data-stu-id="39edb-120">Parameters</span></span>**

*<span data-ttu-id="39edb-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="39edb-121">None</span></span>*

**<span data-ttu-id="39edb-122">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="39edb-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="39edb-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="39edb-123">/json/close</span></span>

<span data-ttu-id="39edb-124">Cierra el proceso de destino (por ejemplo, en Microsoft Edge, cierra la pestaña página).</span><span class="sxs-lookup"><span data-stu-id="39edb-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="39edb-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="39edb-125">Parameters</span></span>**

<span data-ttu-id="39edb-126">IDENTIFICADOR de destino</span><span class="sxs-lookup"><span data-stu-id="39edb-126">Target ID</span></span> 

**<span data-ttu-id="39edb-127">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="39edb-127">Return object</span></span>**

```
String("Target is closing")
```
