---
title: Representaciones DateTime y TimeSpan de Windows en tiempo de ejecución
ms.custom: ''
ms.date: 07/29/2020
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
ms.openlocfilehash: 1c51bba74bb7e5182eb25342badcae848eeba339
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942055"
---
# <span data-ttu-id="5ad78-102">Representaciones DateTime y TimeSpan de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="5ad78-102">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="5ad78-103">La representación de JavaScript de las fechas y horas es distinta de la versión de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="5ad78-103">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="5ad78-104">La estructura [DateTime][UwpWindowsFoundationDatetime] de Windows Runtime se representa en JavaScript como una [fecha][MDNDate] que tiene un almacén de respaldo que coincide con los `DateTime` datos \ (y tiene un intervalo y una precisión diferentes al JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="5ad78-104">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="5ad78-105">Si modifica este objeto personalizado `Date` , se convierte en un JavaScript estándar `Date` y pierde precisión.</span><span class="sxs-lookup"><span data-stu-id="5ad78-105">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="5ad78-106">Los valores de JavaScript se `Date` pueden pasar a un Windows en tiempo de ejecución `DateTime` y se comprobarán por intervalos, lo que puede dar como resultado una cálculo de referencias de excepciones.</span><span class="sxs-lookup"><span data-stu-id="5ad78-106">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="5ad78-107">La estructura de [TimeSpan][UwpWindowsFoundationTimespan] de Windows Runtime se convierte en milisegundos y se devuelve como un número de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5ad78-107">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="5ad78-108">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5ad78-108">See also</span></span>  

[<span data-ttu-id="5ad78-109">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="5ad78-109">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar Windows Runtime en JavaScript | Microsoft docs"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime struct | Microsoft docs"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "La estructura TimeSpan | Microsoft docs"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Fecha | MDN"  
