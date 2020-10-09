---
description: Notas de la versión para el protocolo Microsoft Edge DevTools, versión 0,1
title: Notas de la versión 0,1 del protocolo DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 3c0648467c20572a525fe257788068966efd193c
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104738"
---
# Notas de la versión 0,1 del protocolo DevTools

> [!NOTE]
> El protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

La versión 0,1 del **protocolo Microsoft Edge DevTools** proporciona una vista previa temprana para probar EdgeHTML Instrumentation y la depuración remota básica en la nueva aplicación independiente [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) . Por lo tanto, es necesario que ejecutes la [actualización del 2018 de abril de Windows 10](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) o una versión posterior de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

Los objetivos del protocolo DevTools son tres veces:

 - Proporciona una API pública para que nuestra aplicación de DevTools se adjunte a Microsoft Edge
 - Expandir el acceso de la funcionalidad de DevTools a los clientes de herramientas externas
 - Habilitar la depuración remota en la gama de dispositivos con Windows 10 que ejecutan Microsoft Edge 

Esta versión preliminar proporciona funciones de depuración básicas, como establecer puntos de interrupción, avanzar por el código y explorar los seguimientos de la pila. En la interfaz de usuario de Edge DevTools, se traduce a la funcionalidad disponible en el panel de [**depuración**](../../devtools-guide/debugger.md) , menos inspección de caché (para almacenamiento Web, trabajo de servicio, API de caché y IndexedDB). 

Se agregará más funcionalidad de depurador en las próximas versiones, seguida de la instrumentación que alimenta otros paneles de [DevTools](../../devtools-guide.md) .
