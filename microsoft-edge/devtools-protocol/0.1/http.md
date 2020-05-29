---
description: El protocolo Microsoft Edge DevTools versión 0,1 admite los siguientes puntos de conexión HTTP.
title: Puntos de conexión DevTools HTTP versión 0,1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 5b1cf0d347fec5bfe20b2574afcd635ee569c92d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573751"
---
# <span data-ttu-id="06219-103">Puntos de conexión HTTP del protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="06219-103">DevTools Protocol HTTP Endpoints</span></span>

> [!NOTE]
> <span data-ttu-id="06219-104">El protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="06219-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="06219-105">El **Protocolo DevTools 0,1** admite los siguientes puntos de conexión http.</span><span class="sxs-lookup"><span data-stu-id="06219-105">**DevTools Protocol 0.1** supports the following HTTP endpoints.</span></span> <span data-ttu-id="06219-106">Vea [usar el protocolo](../index.md#using-the-protocol) para obtener más información sobre la conexión a un proceso de contenido del explorador y la documentación de [dominios](domains/index.md) para la API de protocolo de DevTools basada en sockets completo.</span><span class="sxs-lookup"><span data-stu-id="06219-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="06219-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="06219-107">/json/version</span></span>
<span data-ttu-id="06219-108">Proporciona información sobre el explorador del equipo host y la versión del protocolo DevTools que admite.</span><span class="sxs-lookup"><span data-stu-id="06219-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="06219-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="06219-109">Parameters</span></span>**

*<span data-ttu-id="06219-110">Ninguno</span><span class="sxs-lookup"><span data-stu-id="06219-110">None</span></span>*

**<span data-ttu-id="06219-111">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="06219-111">Return object</span></span>**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## <span data-ttu-id="06219-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="06219-112">/json/protocol</span></span>

<span data-ttu-id="06219-113">Proporciona toda la superficie de la API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="06219-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="06219-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="06219-114">Parameters</span></span>**

*<span data-ttu-id="06219-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="06219-115">None</span></span>*

**<span data-ttu-id="06219-116">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="06219-116">Return object</span></span>**

<span data-ttu-id="06219-117">Objeto JSON que representa la superficie de API disponible para la versión actual del protocolo.</span><span class="sxs-lookup"><span data-stu-id="06219-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="06219-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="06219-118">/json/list</span></span>

<span data-ttu-id="06219-119">Proporciona una lista de candidatos de los destinos de página para la depuración.</span><span class="sxs-lookup"><span data-stu-id="06219-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="06219-120">Parameters</span><span class="sxs-lookup"><span data-stu-id="06219-120">Parameters</span></span>**

*<span data-ttu-id="06219-121">Ninguno</span><span class="sxs-lookup"><span data-stu-id="06219-121">None</span></span>*

**<span data-ttu-id="06219-122">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="06219-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="06219-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="06219-123">/json/close</span></span>

<span data-ttu-id="06219-124">Cierra el proceso de destino (por ejemplo, en Microsoft Edge, cierra la pestaña página).</span><span class="sxs-lookup"><span data-stu-id="06219-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="06219-125">Parameters</span><span class="sxs-lookup"><span data-stu-id="06219-125">Parameters</span></span>**

<span data-ttu-id="06219-126">IDENTIFICADOR de destino</span><span class="sxs-lookup"><span data-stu-id="06219-126">Target ID</span></span> 

**<span data-ttu-id="06219-127">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="06219-127">Return object</span></span>**

```
String("Target is closing")
```
