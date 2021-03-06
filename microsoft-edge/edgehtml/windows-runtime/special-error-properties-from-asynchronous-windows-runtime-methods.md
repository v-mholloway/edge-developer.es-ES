---
description: Propiedades de error especial de métodos asíncronos de Windows Runtime
title: Propiedades de error especial de métodos asíncronos de Windows Runtime
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9f2fdb007f00c2ab1d1a2050378af80f0075db6
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398843"
---
# <a name="special-error-properties-from-asynchronous-windows-runtime-methods"></a>Propiedades de error especiales de métodos asíncronos de Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Puede ser difícil depurar métodos asincrónicos de Windows Runtime en JavaScript, ya que el error puede producirse desde algún lugar profundo de la pila de llamadas.  El objeto JavaScript tiene propiedades adicionales que solo aparecen cuando se produce el error desde un método asincrónico de Windows Runtime cuando la aplicación se ejecuta `Error` en modo de depuración.  
  
## <a name="special-error-properties"></a>Propiedades de error especiales  

Un objeto de error que resulta de una operación asincrónica de Windows Runtime con error en modo de depuración tiene las siguientes propiedades especiales:  

*   `asyncOpSource` \(Object\) Obtiene información sobre la ubicación original donde se realizó la llamada que produjo un error.  La propiedad \(String\) muestra la ubicación en el código del usuario que `asyncOpSource.originatingCall` originó la operación asincrónica.  
*   asyncOpType \(String\) Obtiene el nombre del tipo de operación asincrónica que ha producido el error.  
    
Para obtener más información acerca de los errores con operaciones asincrónicas, vea:  

*   [Cómo controlar errores con promesas][PreviousVersionsWindowsAppsHh700337]  
*   [Solución de errores de Windows Runtime][PreviousVersionsWindowsAppsHh974350]  
    
<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Cómo controlar errores con promesas (HTML) | Microsoft Docs"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Solución de problemas de errores de Windows Runtime (HTML) | Microsoft Docs"  
