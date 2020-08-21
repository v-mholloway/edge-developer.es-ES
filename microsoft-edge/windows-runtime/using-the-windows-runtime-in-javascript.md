---
title: Use Windows en tiempo de ejecución en JavaScript
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 444008598a2f7a2f5257544304bed87fbfaa203a
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942172"
---
# Use Windows en tiempo de ejecución en JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Al escribir una aplicación de la plataforma universal de Windows \ (UWP \), puedes usar las clases, los métodos y las propiedades de Windows Runtime de la misma manera en que usarías objetos, métodos y propiedades de JavaScript.  En este tema, se proporciona información introductoria y vínculos a temas que explican los conceptos básicos del uso de las API de Windows Runtime en JavaScript, incluida una explicación de cómo se representan los tipos de Windows Runtime, cómo usar métodos asíncronos de Windows Runtime y cómo escuchar y controlar eventos de Windows Runtime.  

Para la documentación general del idioma, consulte la biblioteca de [referencia de JavaScript][MDNJavascriptReference] de MDN.  

> [!IMPORTANT]
> Las características de Windows en tiempo de ejecución no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.  

## Documentación de referencia de Windows Runtime  

Para obtener documentación de referencia, consulte [referencia de Windows Runtime][UwpApiIndex].  Hay ejemplos de código disponibles en JavaScript y también en C++, C# y Visual Basic.  

## Escritura de componentes de Windows Runtime en C++, C# o Visual Basic  

Para obtener instrucciones e instrucciones para escribir componentes de Windows Runtime que se pueden usar en JavaScript, consulta [creación de componentes de Windows Runtime en C++][WindowsUwpWinrtCpp] y [creación de componentes de Windows Runtime en C# y Visual Basic][WindowsUwpWinrtCsharpVb].  

## Convenciones de las mayúsculas y minúsculas con características de Windows Runtime  

Las convenciones de las mayúsculas y minúsculas de las características de Windows Runtime en JavaScript difieren ligeramente de las de otros idiomas:  

*   Los espacios de nombres y las clases están en mayúsculas y minúsculas Pascal:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Los miembros de clases, incluidos los métodos y las propiedades, y los miembros de estructuras y enumeraciones, están en mayúsculas y minúsculas:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Los nombres de eventos se muestran en minúsculas:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## Consulte también  

[Consideraciones al usar la API de Windows Runtime][WindowsRuntimeConsiderationsApi]  
[Usar métodos asíncronos en tiempo de ejecución de Windows Runtime][WindowsRuntimeAsynchronousMethods]   
[Control de los eventos de Windows Runtime en JavaScript][WindowsRuntimeEventsJavascript]   
[Representación de JavaScript de los tipos de Windows Runtime][WindowsRuntimeJavascriptTypes]   
[Proyección de JavaScript de DateTime y TimeSpan de Windows Runtime][WindowsRuntimeDatetimeTimespan]  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Consideraciones al usar la API de Windows Runtime | Microsoft docs"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Controlar eventos de Windows Runtime en JavaScript | Microsoft docs"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Representación de JavaScript de tipos de Windows Runtime | Microsoft docs"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Uso de métodos asincrónicos de Windows Runtime | Microsoft docs"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Representaciones DateTime y TimeSpan de Windows Runtime | Microsoft docs"  

[UwpApiIndex]: /uwp/api/index "Espacios de nombres de Windows para UWP | Microsoft docs"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes de Windows en tiempo de ejecución con C++/CX | Microsoft docs"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes de Windows en tiempo de ejecución con C# y Visual Basic | Microsoft docs"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Referencia de JavaScript | MDN"  
