---
title: Representaciones DateTime y TimeSpan de Windows Runtime
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d3e138493b80face1238118a99c03f6015a6a8ef
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574909"
---
# Representaciones DateTime y TimeSpan de Windows Runtime  

La representación de JavaScript de las fechas y horas es distinta de la versión de Windows Runtime.  La estructura [DateTime][UwpWindowsFoundationDatetime] de Windows Runtime se representa en JavaScript como una [fecha][MDNDate] que tiene un almacén de respaldo que coincide con los `DateTime` datos \ (y tiene un intervalo y una precisión diferentes al JavaScript `Date` \).  Si modifica este objeto personalizado `Date` , se convierte en un JavaScript estándar `Date` y pierde precisión.  Los valores de JavaScript se `Date` pueden pasar a un Windows en tiempo de ejecución `DateTime` y se comprobarán por intervalos, lo que puede dar como resultado una cálculo de referencias de excepciones.  

 La estructura de [TimeSpan][UwpWindowsFoundationTimespan] de Windows Runtime se convierte en milisegundos y se devuelve como un número de JavaScript.  

## Consulta también  

[Usar Windows Runtime en JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Usar Windows Runtime en JavaScript"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Estructura DateTime"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Estructura TimeSpan"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Fecha | MDN"  
