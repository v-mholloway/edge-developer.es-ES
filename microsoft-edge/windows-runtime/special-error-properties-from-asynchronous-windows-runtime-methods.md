---
title: Propiedades de error especial de métodos asíncronos de Windows Runtime
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a1fccf1cec811501b94e7da4aa20b69d93754f62
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942070"
---
# Propiedades de error especiales de métodos asincrónicos de Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Puede ser difícil depurar métodos asincrónicos de Windows Runtime en JavaScript, porque el error puede producirse desde cualquier parte de la pila de llamadas.  El objeto de JavaScript `Error` tiene propiedades adicionales que solo aparecen cuando el error se produce en un método asincrónico de Windows en tiempo de ejecución cuando la aplicación se está ejecutando en modo de depuración.  
  
## Propiedades de error especial  

Un objeto de error que es el resultado de una operación asincrónica errónea de Windows Runtime en el modo de depuración tiene las siguientes propiedades especiales:  

*   `asyncOpSource` \ (Objeto \) obtiene información sobre la ubicación original en la que se realizó la llamada que produjo un error.  La propiedad `asyncOpSource.originatingCall` \ (cadena \) muestra la ubicación en el código del usuario que originó la operación asincrónica.  
*   asyncOpType \ (cadena \) obtiene el nombre del tipo de operación asincrónica que ha provocado el error.  
    
Para obtener más información sobre los errores con operaciones asincrónicas, vea:  
  
*   [Cómo controlar errores con promesas][PreviousVersionsWindowsAppsHh700337]  
*   [Solución de errores de Windows en tiempo de ejecución][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Cómo controlar errores con promesas (HTML) | Microsoft docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solución de errores de Windows Runtime (HTML) | Microsoft docs"  
