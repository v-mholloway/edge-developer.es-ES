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
# Controlar eventos de Windows Runtime en JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Los eventos de Windows Runtime no se representan de la misma forma en JavaScript que en C++ o .NET Framework.  No son propiedades de clase, sino que se representan como identificadores de cadena \ (minúscula \) que se pasan a los métodos y a las clases `addEventListener` `removeEventListener` .  Por ejemplo, puedes agregar un controlador de eventos para el evento [geolocator. PositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] pasando la cadena `positionchanged` al `Geolocator.addEventListener` método:  

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

Otra diferencia entre .NET/C++ y JavaScript es el número de parámetros que toma un controlador de eventos.  En .NET/C++, un controlador toma dos: el remitente del evento y los datos del evento.  En JavaScript, los dos se agrupan como un solo `Event` objeto.  En el ejemplo siguiente, el `ev` parámetro contiene el remitente del evento \ (la `target` propiedad \) y las propiedades de datos de evento \ (aquí, solo `position` \).  Las propiedades de los datos de evento son las documentadas para cada evento.  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Las características de Windows en tiempo de ejecución no están disponibles para las aplicaciones que se ejecutan en Internet Explorer.  

## Consulte también  

[Use Windows en tiempo de ejecución en JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Usar Windows Runtime en JavaScript | Microsoft docs"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Clase geolocator | Microsoft docs"  
