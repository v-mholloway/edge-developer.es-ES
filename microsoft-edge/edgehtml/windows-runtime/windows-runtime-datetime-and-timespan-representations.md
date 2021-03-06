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
# <a name="windows-runtime-datetime-and-timespan-representations"></a><span data-ttu-id="93f2c-103">Representaciones DateTime y TimeSpan de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="93f2c-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="93f2c-104">La representación de JavaScript de fechas y horas es diferente de la versión de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="93f2c-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="93f2c-105">La estructura [DateTime][UwpWindowsFoundationDatetime] de Windows Runtime se representa en JavaScript como una [fecha][MDNDate] que tiene un almacén de respaldo que coincide con los datos \(y tiene un rango y precisión diferentes de `DateTime` JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="93f2c-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="93f2c-106">Si modifica este objeto `Date` personalizado, se convierte en un JavaScript `Date` estándar y pierde precisión.</span><span class="sxs-lookup"><span data-stu-id="93f2c-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="93f2c-107">Los valores de JavaScript se pueden pasar a Windows Runtime y se comprobarán mediante intervalos, lo que podría provocar `Date` `DateTime` excepciones de cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="93f2c-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

<span data-ttu-id="93f2c-108">La estructura [TimeSpan][UwpWindowsFoundationTimespan] de Windows Runtime se convierte en milisegundos y se devuelve como un número de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="93f2c-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <a name="see-also"></a><span data-ttu-id="93f2c-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="93f2c-109">See also</span></span>  

[<span data-ttu-id="93f2c-110">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="93f2c-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Uso de Windows Runtime en JavaScript | Microsoft Docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Microsoft Docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "TimeSpan Struct | Microsoft Docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Fecha | MDN"  
