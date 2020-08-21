---
title: Control de los eventos de Windows Runtime en JavaScript
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fe44457206569c1e32c40514b4b186bec50d1e3c
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942162"
---
# <span data-ttu-id="56ce5-102">Controlar eventos de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="56ce5-102">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="56ce5-103">Los eventos de Windows Runtime no se representan de la misma forma en JavaScript que en C++ o .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="56ce5-103">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="56ce5-104">No son propiedades de clase, sino que se representan como identificadores de cadena \ (minúscula \) que se pasan a los métodos y a las clases `addEventListener` `removeEventListener` .</span><span class="sxs-lookup"><span data-stu-id="56ce5-104">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="56ce5-105">Por ejemplo, puedes agregar un controlador de eventos para el evento [geolocator. PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] pasando la cadena `positionchanged` al `Geolocator.addEventListener` método:</span><span class="sxs-lookup"><span data-stu-id="56ce5-105">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="56ce5-106">También puede establecer la `locator.onpositionchanged` propiedad:</span><span class="sxs-lookup"><span data-stu-id="56ce5-106">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="56ce5-107">Otra diferencia entre .NET/C++ y JavaScript es el número de parámetros que toma un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="56ce5-107">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="56ce5-108">En .NET/C++, un controlador toma dos: el remitente del evento y los datos del evento.</span><span class="sxs-lookup"><span data-stu-id="56ce5-108">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="56ce5-109">En JavaScript, los dos se agrupan como un solo `Event` objeto.</span><span class="sxs-lookup"><span data-stu-id="56ce5-109">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="56ce5-110">En el ejemplo siguiente, el `ev` parámetro contiene el remitente del evento \ (la `target` propiedad \) y las propiedades de datos de evento \ (aquí, solo `position` \).</span><span class="sxs-lookup"><span data-stu-id="56ce5-110">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="56ce5-111">Las propiedades de los datos de evento son las documentadas para cada evento.</span><span class="sxs-lookup"><span data-stu-id="56ce5-111">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="56ce5-112">Las características de Windows en tiempo de ejecución no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="56ce5-112">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="56ce5-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="56ce5-113">See also</span></span>  

[<span data-ttu-id="56ce5-114">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="56ce5-114">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar Windows Runtime en JavaScript | Microsoft docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Clase geolocator | Microsoft docs"  
