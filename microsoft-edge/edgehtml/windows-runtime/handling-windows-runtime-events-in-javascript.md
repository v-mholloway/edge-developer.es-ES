---
description: Control de los eventos de Windows Runtime en JavaScript
title: Control de los eventos de Windows Runtime en JavaScript
ms.custom: ''
ms.date: 11/03/2020
ms.prod: microsoft-edge
ms.technology: windows-integration
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 08562f7ebff0c02b96bfc8229238a62463b95451
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397527"
---
# <a name="handling-windows-runtime-events-in-javascript"></a><span data-ttu-id="20c8f-103">Control de los eventos de Windows Runtime en JavaScript</span><span class="sxs-lookup"><span data-stu-id="20c8f-103">Handling Windows Runtime events in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="20c8f-104">Los eventos de Windows Runtime no se representan de la misma manera en JavaScript que en C++ o en el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="20c8f-104">Windows Runtime events are not represented in the same way in JavaScript as they are in C++ or the .NET Framework.</span></span>  <span data-ttu-id="20c8f-105">No son propiedades de clase, sino que se representan como identificadores de cadena \(minúsculas\) que se pasan a los métodos y la `addEventListener` `removeEventListener` clase.</span><span class="sxs-lookup"><span data-stu-id="20c8f-105">They are not class properties, but rather are represented as \(lowercase\) string identifiers that are passed to the class's `addEventListener` and `removeEventListener` methods.</span></span>  <span data-ttu-id="20c8f-106">Por ejemplo, puede agregar un controlador de eventos para el evento [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] pasando la cadena `positionchanged` al `Geolocator.addEventListener` método:</span><span class="sxs-lookup"><span data-stu-id="20c8f-106">For example, you can add an event handler for the [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] event by passing the string `positionchanged` to the `Geolocator.addEventListener` method:</span></span>  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

<span data-ttu-id="20c8f-107">También puede establecer la `locator.onpositionchanged` propiedad:</span><span class="sxs-lookup"><span data-stu-id="20c8f-107">You can also set the `locator.onpositionchanged` property:</span></span>  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

<span data-ttu-id="20c8f-108">Otra diferencia entre .NET/C++ y JavaScript es el número de parámetros tomados por un controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="20c8f-108">Another difference between .NET/C++ and JavaScript is the number of parameters taken by an event handler.</span></span>  <span data-ttu-id="20c8f-109">En .NET/C++, un controlador toma dos: el remitente del evento y los datos del evento.</span><span class="sxs-lookup"><span data-stu-id="20c8f-109">In .NET/C++, a handler takes two:  the event sender, and the event data.</span></span>  <span data-ttu-id="20c8f-110">En JavaScript, los dos se agrupan como un único `Event` objeto.</span><span class="sxs-lookup"><span data-stu-id="20c8f-110">In JavaScript, the two are bundled as a single `Event` object.</span></span>  <span data-ttu-id="20c8f-111">En el siguiente ejemplo, el parámetro contiene tanto el remitente del evento \(la propiedad\) como las propiedades de datos del evento `ev` `target` \(aquí, solo `position` \).</span><span class="sxs-lookup"><span data-stu-id="20c8f-111">In the following example, the `ev` parameter contains both the sender of the event \(the `target` property\) and the event data properties \(here, just `position`\).</span></span>  <span data-ttu-id="20c8f-112">Las propiedades de datos de evento son las que se documentan para cada evento.</span><span class="sxs-lookup"><span data-stu-id="20c8f-112">The event data properties are the ones that are documented for each event.</span></span>  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> <span data-ttu-id="20c8f-113">Las características de Windows Runtime no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="20c8f-113">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="20c8f-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="20c8f-114">See also</span></span>  

[<span data-ttu-id="20c8f-115">Use Windows en tiempo de ejecución en JavaScript</span><span class="sxs-lookup"><span data-stu-id="20c8f-115">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Uso de Windows Runtime en JavaScript | Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Clase Geolocator | Microsoft Docs"  
