---
description: Representaciones DateTime y TimeSpan de Windows en tiempo de ejecución
title: Representaciones DateTime y TimeSpan de Windows en tiempo de ejecución
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
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1ee3d601e727601aba03f2ff7efa532171b8f815
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236192"
---
# <span data-ttu-id="10cb1-103">Representaciones DateTime y TimeSpan de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="10cb1-103">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="10cb1-104">La representación de JavaScript de las fechas y horas es distinta de la versión de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="10cb1-104">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="10cb1-105">La estructura [DateTime][UwpWindowsFoundationDatetime] de Windows Runtime se representa en JavaScript como una [fecha][MDNDate] que tiene un almacén de respaldo que coincide con los `DateTime` datos \ (y tiene un intervalo y una precisión diferentes al JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="10cb1-105">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="10cb1-106">Si modifica este objeto personalizado `Date` , se convierte en un JavaScript estándar `Date` y pierde precisión.</span><span class="sxs-lookup"><span data-stu-id="10cb1-106">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="10cb1-107">Los valores de JavaScript se `Date` pueden pasar a un Windows en tiempo de ejecución `DateTime` y se comprobarán por intervalos, lo que puede dar como resultado una cálculo de referencias de excepciones.</span><span class="sxs-lookup"><span data-stu-id="10cb1-107">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="10cb1-108">La estructura de [TimeSpan][UwpWindowsFoundationTimespan] de Windows Runtime se convierte en milisegundos y se devuelve como un número de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="10cb1-108">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="10cb1-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="10cb1-109">See also</span></span>  

[<span data-ttu-id="10cb1-110">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="10cb1-110">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar Windows Runtime en JavaScript | Microsoft docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime struct | Microsoft docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "La estructura TimeSpan | Microsoft docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Fecha | MDN"  
