---
description: Notas de la versión para el protocolo Microsoft Edge DevTools, versión 0,1
title: Notas de la versión 0,1 del protocolo DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60e92cb3afa9b10b15c8ebdd520c0061fbb3b366
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236347"
---
# <span data-ttu-id="e346e-103">Notas de la versión 0,1 del protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="e346e-103">DevTools Protocol Version 0.1 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="e346e-104">El protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="e346e-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="e346e-105">La versión 0,1 del **protocolo Microsoft Edge DevTools** proporciona una vista previa temprana para probar EdgeHTML Instrumentation y la depuración remota básica en la nueva aplicación independiente [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) .</span><span class="sxs-lookup"><span data-stu-id="e346e-105">Version 0.1 of the Microsoft **Edge DevTools Protocol** provides an early preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="e346e-106">Por lo tanto, es necesario que ejecutes la [actualización del 2018 de abril de Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) o una versión posterior de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="e346e-106">As such, it requires you to be running [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) or a later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) build.</span></span>

<span data-ttu-id="e346e-107">Los objetivos del protocolo DevTools son tres veces:</span><span class="sxs-lookup"><span data-stu-id="e346e-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="e346e-108">Proporciona una API pública para que nuestra aplicación de DevTools se adjunte a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e346e-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="e346e-109">Expandir el acceso de la funcionalidad de DevTools a los clientes de herramientas externas</span><span class="sxs-lookup"><span data-stu-id="e346e-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="e346e-110">Habilitar la depuración remota en la gama de dispositivos con Windows 10 que ejecutan Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e346e-110">Enable remote debugging across the range of Windows 10 devices running Microsoft Edge</span></span> 

<span data-ttu-id="e346e-111">Esta versión preliminar proporciona funciones de depuración básicas, como establecer puntos de interrupción, avanzar por el código y explorar los seguimientos de la pila.</span><span class="sxs-lookup"><span data-stu-id="e346e-111">This preliminary release provides core debugging functionality, such as setting breakpoints, stepping through code, and exploring stack traces.</span></span> <span data-ttu-id="e346e-112">En la interfaz de usuario de Edge DevTools, se traduce a la funcionalidad disponible en el panel de [**depuración**](../../devtools-guide/debugger.md) , menos inspección de caché (para almacenamiento Web, trabajo de servicio, API de caché y IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="e346e-112">In the Edge DevTools UI, this translates to functionality available in the [**Debugger**](../../devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> 

<span data-ttu-id="e346e-113">Se agregará más funcionalidad de depurador en las próximas versiones, seguida de la instrumentación que alimenta otros paneles de [DevTools](../index.md) .</span><span class="sxs-lookup"><span data-stu-id="e346e-113">Further debugger functionality will be added in upcoming releases, followed by the instrumentation powering other [DevTools](../index.md) panels.</span></span>
