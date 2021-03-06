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
# <a name="handling-windows-runtime-events-in-javascript"></a>Control de los eventos de Windows Runtime en JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Los eventos de Windows Runtime no se representan de la misma manera en JavaScript que en C++ o en el .NET Framework.  No son propiedades de clase, sino que se representan como identificadores de cadena \(minúsculas\) que se pasan a los métodos y la `addEventListener` `removeEventListener` clase.  Por ejemplo, puede agregar un controlador de eventos para el evento [Geolocator.PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] pasando la cadena `positionchanged` al `Geolocator.addEventListener` método:  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

También puede establecer la `locator.onpositionchanged` propiedad:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Otra diferencia entre .NET/C++ y JavaScript es el número de parámetros tomados por un controlador de eventos.  En .NET/C++, un controlador toma dos: el remitente del evento y los datos del evento.  En JavaScript, los dos se agrupan como un único `Event` objeto.  En el siguiente ejemplo, el parámetro contiene tanto el remitente del evento \(la propiedad\) como las propiedades de datos del evento `ev` `target` \(aquí, solo `position` \).  Las propiedades de datos de evento son las que se documentan para cada evento.  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Las características de Windows Runtime no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.  

## <a name="see-also"></a>Consulte también  

[Use Windows en tiempo de ejecución en JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Uso de Windows Runtime en JavaScript | Microsoft Docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Clase Geolocator | Microsoft Docs"  
