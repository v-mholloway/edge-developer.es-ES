---
description: Vea las novedades de la actualización de Microsoft Edge DevTools en la actualización de Windows 10 de octubre de 2018
title: Novedades de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, edgehtml 18
ms.custom: RS5, seodec18
ms.openlocfilehash: 604419f4c77ccaaf2dfd3179273be803cde86fc8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573775"
---
# <span data-ttu-id="b8094-104">DevTools en la actualización más reciente de Windows 10 (EdgeHTML 18)</span><span class="sxs-lookup"><span data-stu-id="b8094-104">DevTools in the latest Windows 10 update (EdgeHTML 18)</span></span>

<span data-ttu-id="b8094-105">La actualización más reciente de Microsoft Edge DevTools agrega varias ventajas a la interfaz de usuario y al Capó, incluidos nuevos paneles dedicados para el [*almacenamiento*](#storage-panel)y los [*trabajos de servicio*](#service-workers-panel) , las herramientas de [búsqueda de archivos](#source-file-search-tools) de origen en el depurador y los nuevos dominios de protocolo de [DevTools de borde](#edge-devtools-protocol-updates) para la depuración de estilo o diseño y las API de consola.</span><span class="sxs-lookup"><span data-stu-id="b8094-105">The latest update to Microsoft Edge DevTools adds a number of conveniences both to the UI and under the hood, including new dedicated panels for [*Service Workers*](#service-workers-panel) and [*Storage*](#storage-panel), source [file search](#source-file-search-tools) tools in the Debugger, and new [Edge DevTools Protocol domains](#edge-devtools-protocol-updates) for style/layout debugging and console APIs.</span></span>

<span data-ttu-id="b8094-106">Estas son las últimas características de Microsoft Edge DevTools disponibles ahora en la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span><span class="sxs-lookup"><span data-stu-id="b8094-106">Here are the latest Microsoft Edge DevTools features available now in the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span></span> <span data-ttu-id="b8094-107">Además de todo esto, también hemos corregido un número de errores de accesibilidad, confiabilidad y rendimiento para mejorar los aspectos fundamentales.</span><span class="sxs-lookup"><span data-stu-id="b8094-107">In addition to all this, we’ve also fixed a number of accessibility, reliability, and performance bugs to improve fundamentals!</span></span>

## <span data-ttu-id="b8094-108">Aplicación de DevTools</span><span class="sxs-lookup"><span data-stu-id="b8094-108">DevTools app</span></span>

<span data-ttu-id="b8094-109">Hemos actualizado la aplicación independiente [Microsoft Edge DevTools Preview](../devtools-guide.md#microsoft-store-app).</span><span class="sxs-lookup"><span data-stu-id="b8094-109">We've updated the standalone [Microsoft Edge DevTools Preview app](../devtools-guide.md#microsoft-store-app).</span></span> <span data-ttu-id="b8094-110">La versión más reciente incluye el acceso de depuración remota a la funcionalidad básica del [**depurador**](./debugger.md), [**los elementos**](./elements.md) (para las operaciones de solo lectura) y los paneles de [**consola**](./console.md) .</span><span class="sxs-lookup"><span data-stu-id="b8094-110">The latest release includes remote debugging access to core funtionality in the [**Debugger**](./debugger.md), [**Elements**](./elements.md) (for read-only operations), and [**Console**](./console.md) panels.</span></span>

## <span data-ttu-id="b8094-111">Panel de trabajo de servicios</span><span class="sxs-lookup"><span data-stu-id="b8094-111">Service Workers panel</span></span>

<span data-ttu-id="b8094-112">Ahora hay un panel dedicado a los [**trabajadores de servicios**](./service-workers.md) para inspeccionar, administrar y depurar los trabajadores del servicio del sitio.</span><span class="sxs-lookup"><span data-stu-id="b8094-112">There's now a dedicated [**Service Workers**](./service-workers.md) panel for inspecting, managing, and debugging your site's service workers.</span></span> <span data-ttu-id="b8094-113">Esto proporciona la misma funcionalidad que tenía anteriormente en el panel de *depuración* (ahora con una interfaz de usuario menos llena).</span><span class="sxs-lookup"><span data-stu-id="b8094-113">This provides the same functionality as was previously in the *Debugger* panel (now with a less-crowded UI!).</span></span>

![Panel de trabajo de servicios](./media/service_worker.png)

## <span data-ttu-id="b8094-115">Panel almacenamiento</span><span class="sxs-lookup"><span data-stu-id="b8094-115">Storage panel</span></span>

<span data-ttu-id="b8094-116">También hemos movido todos los inspectores de almacenamiento local (*almacenamiento local y sesion, IndexedDB, cookies, caché*) en el *depurador* a su panel de [**almacenamiento**](./storage.md) dedicado.</span><span class="sxs-lookup"><span data-stu-id="b8094-116">We've also moved all the local storage inspectors (*Local and Sesion Storage, IndexedDB, Cookies, Cache*) previously in the *Debugger* to their own dedicated [**Storage**](./storage.md) panel.</span></span>

![Panel almacenamiento](./media/storage_cache.png)

## <span data-ttu-id="b8094-118">Herramientas de búsqueda de archivos de origen</span><span class="sxs-lookup"><span data-stu-id="b8094-118">Source file search tools</span></span>

<span data-ttu-id="b8094-119">El [**depurador**](./debugger.md) ahora tiene un panel de [búsqueda de archivos de origen](./debugger.md#file-search) .</span><span class="sxs-lookup"><span data-stu-id="b8094-119">The [**Debugger**](./debugger.md) now has a [source file search](./debugger.md#file-search) pane.</span></span> <span data-ttu-id="b8094-120">Ábralo con el comando *Buscar en archivos* ( `Ctrl` + `Shift` + `F` ) cuando tenga una cadena específica de código que está tratando de buscar en el origen.</span><span class="sxs-lookup"><span data-stu-id="b8094-120">Open it with the *Find in files* command (`Ctrl`+`Shift`+`F`) when you have a specific string of code you're trying to find in the source.</span></span> <span data-ttu-id="b8094-121">La barra de herramientas proporciona diferentes opciones de búsqueda, incluidas las expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="b8094-121">The toolbar provides different search options, including regular expressions.</span></span> 

![Búsqueda de archivos del depurador](./media/debugger_file_search.png)

<span data-ttu-id="b8094-123">También puede abrir rápidamente cualquier archivo de origen cargado con el comando *Abrir archivo* ( `Ctrl` + `P` ).</span><span class="sxs-lookup"><span data-stu-id="b8094-123">You can also quickly open any loaded source file with the *Open file* (`Ctrl`+`P`) command.</span></span>

![Archivo de apertura de depuración](./media/debugger_open_file.png)

## <span data-ttu-id="b8094-125">Actualizaciones del protocolo Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b8094-125">Edge DevTools Protocol updates</span></span>

<span data-ttu-id="b8094-126">La [versión 0,2](../devtools-protocol/0.2/index.md) del protocolo DevTools proporciona dominios nuevos para la depuración de estilo y el diseño (solo lectura) de la depuración y API de consola, además de la funcionalidad de depuración básica de scripts introducida en la [versión 0,1](../devtools-protocol/0.1/index.md).</span><span class="sxs-lookup"><span data-stu-id="b8094-126">[Version 0.2](../devtools-protocol/0.2/index.md) of the DevTools Protocol provides new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in [Version 0.1](../devtools-protocol/0.1/index.md).</span></span> <span data-ttu-id="b8094-127">En la interfaz de usuario de Edge DevTools, esto se traduce en la funcionalidad disponible en los [**elementos**](../devtools-guide/elements.md) (para las operaciones de solo lectura), en los paneles de [**consola**](../devtools-guide/console.md) y de [**depuración**](../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="b8094-127">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../devtools-guide/elements.md) (for read-only operations), [**Console**](../devtools-guide/console.md) and [**Debugger**](../devtools-guide/debugger.md) panels.</span></span>
