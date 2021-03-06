---
description: Use Windows en tiempo de ejecución en JavaScript
title: Use Windows en tiempo de ejecución en JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4e137526ce147cdeb82749474bd43d1b3697361b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399326"
---
# <a name="using-the-windows-runtime-in-javascript"></a>Use Windows en tiempo de ejecución en JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Cuando escribes una aplicación de la Plataforma universal de Windows \(UWP\), puedes usar clases, métodos y propiedades de Windows Runtime de la misma manera que usaríamos objetos, métodos y propiedades nativos de JavaScript.  En este tema se proporciona información introductoria y vínculos a temas que explican los conceptos básicos del uso de LAS API de Windows Runtime en JavaScript, incluida una explicación de cómo se representan los tipos de Windows Runtime, cómo usar métodos asincrónicos de Windows Runtime y cómo escuchar y controlar eventos de Windows Runtime.  

Para obtener documentación general sobre el idioma, consulte la biblioteca de referencias [de JavaScript de MDN.][MDNJavascriptReference]  

> [!IMPORTANT]
> Las características de Windows Runtime no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.  

## <a name="windows-runtime-reference-documentation"></a>Documentación de referencia de Windows Runtime  

Para obtener documentación de referencia, consulta [Referencia de Windows Runtime][UwpApiIndex].  Los ejemplos de código están disponibles en JavaScript y también en C++, C# y Visual Basic.  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a>Escribir componentes de Windows Runtime en C++, C# o Visual Basic  

Para obtener instrucciones y directrices para escribir componentes de Windows Runtime que se pueden consumir en JavaScript, consulta Crear componentes de Windows Runtime en [C++][WindowsUwpWinrtCpp] y Crear componentes de [Windows Runtime][WindowsUwpWinrtCsharpVb]en C# y Visual Basic .  

## <a name="casing-conventions-with-windows-runtime-features"></a>Convenciones de mayúsculas y minúsculas con características de Windows Runtime  

Las convenciones de mayúsculas y minúsculas para las características de Windows Runtime en JavaScript difieren ligeramente de las de otros idiomas:  

*   Los espacios de nombres y las clases están en el caso de Pascal:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Los miembros de clases, incluidos los métodos y propiedades, y los miembros de estructuras y enumeraciones, están en mayúsculas y minúsculas:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Los nombres de eventos son en minúsculas:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a>Consulte también  

[Consideraciones al usar la API de Windows Runtime][WindowsRuntimeConsiderationsApi]  
[Usar métodos asíncronos en tiempo de ejecución de Windows Runtime][WindowsRuntimeAsynchronousMethods]   
[Control de los eventos de Windows Runtime en JavaScript][WindowsRuntimeEventsJavascript]   
[Representación de JavaScript de los tipos de Windows Runtime][WindowsRuntimeJavascriptTypes]   
[Proyección de JavaScript de Windows Runtime DateTime y TimeSpan][WindowsRuntimeDatetimeTimespan]  

<!-- links -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Consideraciones al usar la API de Windows Runtime | Microsoft Docs"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Controlar eventos de Windows Runtime en JavaScript | Microsoft Docs"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Representación de JavaScript de tipos de Windows Runtime | Microsoft Docs"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Uso de métodos asincrónicos de Windows Runtime | Microsoft Docs"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Representaciones de DateTime y TimeSpan de Windows Runtime | Microsoft Docs"  

[UwpApiIndex]: /uwp/api/index "Espacios de nombres de Windows UWP | Microsoft Docs"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Componentes de Windows Runtime con C++/CX | Microsoft Docs"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Componentes de Windows Runtime con C# y Visual Basic | Microsoft Docs"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Referencia de JavaScript | MDN"  
