---
description: Notas de la versión para el protocolo Microsoft Edge DevTools, versión 0,2
title: Notas de la versión 0,2 del protocolo Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: c4c54273d123c605181ee4b53aa441768a8711bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573725"
---
# <span data-ttu-id="e7af1-103">Notas de la versión 0,2 del protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="e7af1-103">DevTools Protocol Version 0.2 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="e7af1-104">La versión 0,2 del protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="e7af1-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/getting-started/) builds.</span></span>

<span data-ttu-id="e7af1-105">La versión 0,2 del **protocolo Microsoft Edge DevTools** proporciona una vista previa para probar EdgeHTML Instrumentation y la depuración remota básica en la nueva aplicación independiente [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) .</span><span class="sxs-lookup"><span data-stu-id="e7af1-105">Version 0.2 of the Microsoft **Edge DevTools Protocol** provides a preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="e7af1-106">Por lo tanto, es necesario que ejecutes la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) o una compilación posterior de [Windows Insider Preview](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="e7af1-106">As such, it requires you to be running the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later [Windows Insider Preview](https://insider.windows.com/getting-started/) build.</span></span>

<span data-ttu-id="e7af1-107">Los objetivos del protocolo DevTools son tres veces:</span><span class="sxs-lookup"><span data-stu-id="e7af1-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="e7af1-108">Proporciona una API pública para que nuestra aplicación de DevTools se adjunte a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e7af1-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="e7af1-109">Expandir el acceso de la funcionalidad de DevTools a los clientes de herramientas externas</span><span class="sxs-lookup"><span data-stu-id="e7af1-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="e7af1-110">Habilitar la depuración remota en la gama de dispositivos con Windows 10 que ejecutan Micrsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e7af1-110">Enable remote debugging across the range of Windows 10 devices running Micrsoft Edge</span></span> 

<span data-ttu-id="e7af1-111">La versión 0,2 del protocolo DevTools incluye dominios nuevos para el estilo y el diseño (solo lectura) de depuración y API de consola, además de la funcionalidad de depuración básica de scripts introducida en la versión 0,1.</span><span class="sxs-lookup"><span data-stu-id="e7af1-111">Version 0.2 of the DevTools Protocol includes new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="e7af1-112">En la interfaz de usuario de Edge DevTools, esto se traduce en la funcionalidad disponible en los paneles [**elementos**](../../devtools-guide/elements.md), [**consola**](../../devtools-guide/console.md) y [**depuración**](../../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="e7af1-112">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md)  panels.</span></span>
