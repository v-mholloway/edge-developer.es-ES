---
description: Representaciones DateTime y TimeSpan de Windows en tiempo de ejecución
title: Representaciones DateTime y TimeSpan de Windows en tiempo de ejecución
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: c2627826755f041a440112c3390ecb17d1f703ce
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398129"
---
# <a name="windows-runtime-datetime-and-timespan-representations"></a>Representaciones DateTime y TimeSpan de Windows Runtime  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

La representación de JavaScript de fechas y horas es diferente de la versión de Windows Runtime.  La estructura [DateTime][UwpWindowsFoundationDatetime] de Windows Runtime se representa en JavaScript como una [fecha][MDNDate] que tiene un almacén de respaldo que coincide con los datos \(y tiene un rango y precisión diferentes de `DateTime` JavaScript `Date` \).  Si modifica este objeto `Date` personalizado, se convierte en un JavaScript `Date` estándar y pierde precisión.  Los valores de JavaScript se pueden pasar a Windows Runtime y se comprobarán mediante intervalos, lo que podría provocar `Date` `DateTime` excepciones de cálculo de referencias.  

La estructura [TimeSpan][UwpWindowsFoundationTimespan] de Windows Runtime se convierte en milisegundos y se devuelve como un número de JavaScript.  

## <a name="see-also"></a>Consulte también  

[Use Windows en tiempo de ejecución en JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Uso de Windows Runtime en JavaScript | Microsoft Docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Microsoft Docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan Struct | Microsoft Docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Fecha | MDN"  
