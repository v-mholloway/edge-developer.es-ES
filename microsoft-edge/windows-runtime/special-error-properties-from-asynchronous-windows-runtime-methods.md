---
title: Propiedades de error especiales de métodos asincrónicos de Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: 5cf2604e26c84e769cf44e0879ee137cbfbe8b90
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574915"
---
# Propiedades de error especiales de métodos asincrónicos de Windows Runtime  

Puede ser difícil depurar métodos asincrónicos de Windows Runtime en JavaScript, porque el error puede producirse desde cualquier parte de la pila de llamadas. El objeto de JavaScript `Error` tiene propiedades adicionales que solo aparecen cuando el error se produce en un método asincrónico de Windows en tiempo de ejecución cuando la aplicación se está ejecutando en modo de depuración.  
  
## Propiedades de error especial  

Un objeto de error que es el resultado de una operación asincrónica errónea de Windows Runtime en el modo de depuración tiene las siguientes propiedades especiales:  

*   `asyncOpSource` \ (Objeto \) obtiene información sobre la ubicación original en la que se realizó la llamada que produjo un error. La propiedad `asyncOpSource.originatingCall` \ (cadena \) muestra la ubicación en el código del usuario que originó la operación asincrónica.  
*   asyncOpType \ (cadena \) obtiene el nombre del tipo de operación asincrónica que ha provocado el error.  
    
Para obtener más información sobre los errores con operaciones asincrónicas, vea:  
  
*   [Cómo controlar errores con promesas][PreviousVersionsWindowsAppsHh700337]  
*   [Solución de errores de Windows en tiempo de ejecución][PreviousVersionsWindowsAppsHh974350]  

<!-- image links -->  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Cómo controlar errores con las promesas (HTML)"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solución de errores de Windows Runtime (HTML)"  
