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
# <span data-ttu-id="b3333-102">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="b3333-102">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="b3333-103">Al escribir una aplicación de la plataforma universal de Windows \ (UWP \), puedes usar las clases, los métodos y las propiedades de Windows Runtime de la misma manera en que usarías objetos, métodos y propiedades de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b3333-103">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="b3333-104">En este tema, se proporciona información introductoria y vínculos a temas que explican los conceptos básicos del uso de las API de Windows Runtime en JavaScript, incluida una explicación de cómo se representan los tipos de Windows Runtime, cómo usar métodos asíncronos de Windows Runtime y cómo escuchar y controlar eventos de Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="b3333-104">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="b3333-105">Para la documentación general del idioma, consulte la biblioteca de [referencia de JavaScript][MDNJavascriptReference] de MDN.</span><span class="sxs-lookup"><span data-stu-id="b3333-105">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b3333-106">Las características de Windows en tiempo de ejecución no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="b3333-106">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="b3333-107">Documentación de referencia de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b3333-107">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="b3333-108">Para obtener documentación de referencia, consulte [referencia de Windows Runtime][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="b3333-108">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="b3333-109">Hay ejemplos de código disponibles en JavaScript y también en C++, C# y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b3333-109">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <span data-ttu-id="b3333-110">Escritura de componentes de Windows Runtime en C++, C# o Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b3333-110">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="b3333-111">Para obtener instrucciones e instrucciones para escribir componentes de Windows Runtime que se pueden usar en JavaScript, consulta [creación de componentes de Windows Runtime en C++][WindowsUwpWinrtCpp] y [creación de componentes de Windows Runtime en C# y Visual Basic][WindowsUwpWinrtCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="b3333-111">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <span data-ttu-id="b3333-112">Convenciones de las mayúsculas y minúsculas con características de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b3333-112">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="b3333-113">Las convenciones de las mayúsculas y minúsculas de las características de Windows Runtime en JavaScript difieren ligeramente de las de otros idiomas:</span><span class="sxs-lookup"><span data-stu-id="b3333-113">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="b3333-114">Los espacios de nombres y las clases están en mayúsculas y minúsculas Pascal:</span><span class="sxs-lookup"><span data-stu-id="b3333-114">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="b3333-115">Los miembros de clases, incluidos los métodos y las propiedades, y los miembros de estructuras y enumeraciones, están en mayúsculas y minúsculas:</span><span class="sxs-lookup"><span data-stu-id="b3333-115">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="b3333-116">Los nombres de eventos se muestran en minúsculas:</span><span class="sxs-lookup"><span data-stu-id="b3333-116">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## <span data-ttu-id="b3333-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b3333-117">See also</span></span>  

[<span data-ttu-id="b3333-118">Consideraciones al usar la API de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b3333-118">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="b3333-119">Usar métodos asíncronos en tiempo de ejecución de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b3333-119">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="b3333-120">Control de los eventos de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="b3333-120">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="b3333-121">Representación de JavaScript de los tipos de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b3333-121">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="b3333-122">Proyección de JavaScript de DateTime y TimeSpan de Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="b3333-122">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

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
