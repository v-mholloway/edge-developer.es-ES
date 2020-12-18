---
description: Notas de la versión para el protocolo Microsoft Edge DevTools, versión 0,2
title: Notas de la versión 0,2 del protocolo Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 61d8f5b00dca3505594ca41db6c80c5ba4157092
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235952"
---
# Notas de la versión 0,2 del protocolo DevTools

> [!NOTE]
> La versión 0,2 del protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/getting-started/) .

La versión 0,2 del **protocolo Microsoft Edge DevTools** proporciona una vista previa para probar EdgeHTML Instrumentation y la depuración remota básica en la nueva aplicación independiente [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) . Por lo tanto, es necesario que ejecutes la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) o una compilación posterior de [Windows Insider Preview](https://insider.windows.com/getting-started/) .

Los objetivos del protocolo DevTools son tres veces:

 - Proporciona una API pública para que nuestra aplicación de DevTools se adjunte a Microsoft Edge
 - Expandir el acceso de la funcionalidad de DevTools a los clientes de herramientas externas
 - Habilitar la depuración remota en la gama de dispositivos con Windows 10 que ejecutan Microsoft Edge 

La versión 0,2 del protocolo DevTools incluye dominios nuevos para el estilo y el diseño (solo lectura) de depuración y API de consola, además de la funcionalidad de depuración básica de scripts introducida en la versión 0,1. En la interfaz de usuario de Edge DevTools, esto se traduce en la funcionalidad disponible en los paneles [**elementos**](../../devtools-guide/elements.md), [**consola**](../../devtools-guide/console.md) y [**depuración**](../../devtools-guide/debugger.md)  .
