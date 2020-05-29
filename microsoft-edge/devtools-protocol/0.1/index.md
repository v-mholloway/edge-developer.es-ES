---
description: Notas de la versión para el protocolo Microsoft Edge DevTools, versión 0,1
title: Notas de la versión 0,1 del protocolo DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 29dc8f1b0ba67cb2b3155cb2135d488609e9bff9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573750"
---
# <span data-ttu-id="9e077-103">Notas de la versión 0,1 del protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="9e077-103">DevTools Protocol Version 0.1 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="9e077-104">El protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="9e077-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="9e077-105">La versión 0,1 del **protocolo Microsoft Edge DevTools** proporciona una vista previa temprana para probar EdgeHTML Instrumentation y la depuración remota básica en la nueva aplicación independiente [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) .</span><span class="sxs-lookup"><span data-stu-id="9e077-105">Version 0.1 of the Microsoft **Edge DevTools Protocol** provides an early preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="9e077-106">Por lo tanto, es necesario que ejecutes la [actualización del 2018 de abril de Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) o una versión posterior de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="9e077-106">As such, it requires you to be running [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) or a later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) build.</span></span>

<span data-ttu-id="9e077-107">Los objetivos del protocolo DevTools son tres veces:</span><span class="sxs-lookup"><span data-stu-id="9e077-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="9e077-108">Proporciona una API pública para que nuestra aplicación de DevTools se adjunte a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9e077-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="9e077-109">Expandir el acceso de la funcionalidad de DevTools a los clientes de herramientas externas</span><span class="sxs-lookup"><span data-stu-id="9e077-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="9e077-110">Habilitar la depuración remota en la gama de dispositivos con Windows 10 que ejecutan Micrsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9e077-110">Enable remote debugging across the range of Windows 10 devices running Micrsoft Edge</span></span> 

<span data-ttu-id="9e077-111">Esta versión preliminar proporciona funciones de depuración básicas, como establecer puntos de interrupción, avanzar por el código y explorar los seguimientos de la pila.</span><span class="sxs-lookup"><span data-stu-id="9e077-111">This preliminary release provides core debugging functionality, such as setting breakpoints, stepping through code, and exploring stack traces.</span></span> <span data-ttu-id="9e077-112">En la interfaz de usuario de Edge DevTools, se traduce a la funcionalidad disponible en el panel de [**depuración**](../../devtools-guide/debugger.md) , menos inspección de caché (para almacenamiento Web, trabajo de servicio, API de caché y IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="9e077-112">In the Edge DevTools UI, this translates to functionality available in the [**Debugger**](../../devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> 

<span data-ttu-id="9e077-113">Se agregará más funcionalidad de depurador en las próximas versiones, seguida de la instrumentación que alimenta otros paneles de [DevTools](../../devtools-guide.md) .</span><span class="sxs-lookup"><span data-stu-id="9e077-113">Further debugger functionality will be added in upcoming releases, followed by the instrumentation powering other [DevTools](../../devtools-guide.md) panels.</span></span>
