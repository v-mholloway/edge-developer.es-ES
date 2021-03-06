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
# <a name="using-the-windows-runtime-in-javascript"></a><span data-ttu-id="94143-103">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="94143-103">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="94143-104">Cuando escribes una aplicación de la Plataforma universal de Windows \(UWP\), puedes usar clases, métodos y propiedades de Windows Runtime de la misma manera que usaríamos objetos, métodos y propiedades nativos de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="94143-104">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="94143-105">En este tema se proporciona información introductoria y vínculos a temas que explican los conceptos básicos del uso de LAS API de Windows Runtime en JavaScript, incluida una explicación de cómo se representan los tipos de Windows Runtime, cómo usar métodos asincrónicos de Windows Runtime y cómo escuchar y controlar eventos de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="94143-105">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="94143-106">Para obtener documentación general sobre el idioma, consulte la biblioteca de referencias [de JavaScript de MDN.][MDNJavascriptReference]</span><span class="sxs-lookup"><span data-stu-id="94143-106">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="94143-107">Las características de Windows Runtime no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="94143-107">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="windows-runtime-reference-documentation"></a><span data-ttu-id="94143-108">Documentación de referencia de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="94143-108">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="94143-109">Para obtener documentación de referencia, consulta [Referencia de Windows Runtime][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="94143-109">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="94143-110">Los ejemplos de código están disponibles en JavaScript y también en C++, C# y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="94143-110">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <a name="writing-windows-runtime-components-in-c-c-or-visual-basic"></a><span data-ttu-id="94143-111">Escribir componentes de Windows Runtime en C++, C# o Visual Basic</span><span class="sxs-lookup"><span data-stu-id="94143-111">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="94143-112">Para obtener instrucciones y directrices para escribir componentes de Windows Runtime que se pueden consumir en JavaScript, consulta Crear componentes de Windows Runtime en [C++][WindowsUwpWinrtCpp] y Crear componentes de [Windows Runtime][WindowsUwpWinrtCsharpVb]en C# y Visual Basic .</span><span class="sxs-lookup"><span data-stu-id="94143-112">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <a name="casing-conventions-with-windows-runtime-features"></a><span data-ttu-id="94143-113">Convenciones de mayúsculas y minúsculas con características de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="94143-113">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="94143-114">Las convenciones de mayúsculas y minúsculas para las características de Windows Runtime en JavaScript difieren ligeramente de las de otros idiomas:</span><span class="sxs-lookup"><span data-stu-id="94143-114">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="94143-115">Los espacios de nombres y las clases están en el caso de Pascal:</span><span class="sxs-lookup"><span data-stu-id="94143-115">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="94143-116">Los miembros de clases, incluidos los métodos y propiedades, y los miembros de estructuras y enumeraciones, están en mayúsculas y minúsculas:</span><span class="sxs-lookup"><span data-stu-id="94143-116">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="94143-117">Los nombres de eventos son en minúsculas:</span><span class="sxs-lookup"><span data-stu-id="94143-117">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  
    
## <a name="see-also"></a><span data-ttu-id="94143-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94143-118">See also</span></span>  

[<span data-ttu-id="94143-119">Consideraciones al usar la API de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="94143-119">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="94143-120">Usar métodos asíncronos en tiempo de ejecución de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="94143-120">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="94143-121">Control de los eventos de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="94143-121">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="94143-122">Representación de JavaScript de los tipos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="94143-122">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="94143-123">Proyección de JavaScript de Windows Runtime DateTime y TimeSpan</span><span class="sxs-lookup"><span data-stu-id="94143-123">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

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
