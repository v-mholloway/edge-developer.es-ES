---
description: Use el panel de emulación para probar diferentes perfiles de explorador, tamaños de pantalla y resoluciones, y coordenadas de ubicación GPS
title: 'DevTools: emulación'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, emulación de dispositivos, diseño dinámico, ubicación geográfica, resolución
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: af740472f22a8b322c03cb672a3da909ef195fac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236139"
---
# Emulación  

> [!NOTE]
> El nuevo Microsoft Edge se ha creado con cromo y comienza en la versión 75.  Para obtener más información, [descarga el nuevo Microsoft Edge][MicrosoftNewEdge]y prueba las nuevas [herramientas para desarrolladores de Microsoft Edge (cromo)][DevtoolsGuideChromium].  
> 
> Para emular diferentes dispositivos, exploradores, tamaños de pantalla y resoluciones en el nuevo DevTools, vaya a [emular dispositivos móviles en Microsoft Edge \ (cromo \) DevTools][DevtoolsGuideChromiumDeviceMode].  

El panel de **emulación** ayuda a realizar las siguientes actividades.    

*   Simular diversos [perfiles de dispositivos](#device), [exploradores](#browser-profile), [tamaños de pantalla y resoluciones](#display)  
*   Probar distintas [configuraciones y coordenadas geolocales](#geolocation)  

:::image type="complex" source="./media/emulation.png" alt-text="El panel de emulación DevTools de Microsoft Edge" lightbox="./media/emulation.png":::
   El panel de **emulación** DevTools de Microsoft Edge  
:::image-end:::  

1.  El botón **conservar la configuración de emulación** guarda los cambios realizados en la configuración de emulación de escritorio predeterminada, incluso cuando se cierra y vuelve a abrir la DevTools.  

1.  El botón **restablecer configuración de emulación** restablece la configuración de emulación al perfil de explorador de escritorio predeterminado y a la cadena de agente de usuario de Microsoft Edge con GPS desactivado.  

1.  Cuando se cambia la configuración predeterminada de cualquiera de estas opciones, la pestaña **emulación** muestra una alerta informativa para indicar que se está emulando algún aspecto del comportamiento de su explorador.  

## Dispositivo  

Elija entre una lista preestablecida de perfiles de dispositivo de Windows que configure automáticamente las demás opciones de emulación o especifique su propia configuración **personalizada** .  Cambie de nuevo a **predeterminado** para restablecer todas las herramientas de emulación.  

## Modo  

### Perfil de explorador  

Una forma rápida de simular una página en un dispositivo Windows Phone es cambiar la configuración del **Perfil del explorador** a **Windows Phone**.  

#### Cadena de agente de usuario  

Modificar la cadena de agente de usuario para imitar a otro explorador es un buen primer paso en la depuración de errores que solo ocurren en Microsoft Edge.  

Los scripts usan la cadena de agente de usuario para detectar qué explorador se usa.  El script puede ser front-end, back-end o front-end y back-end.  Aunque el código no usa la detección del explorador, el código puede heredarlo de una biblioteca de JavaScript de terceros o de una secuencia de comandos del servidor.  

El problema con la detección de explorador es que puede escalar \ (o cambiar \) características en la página web con suposiciones acerca de las capacidades del explorador. En su lugar, debe considerar la posibilidad de usar la detección de características para detectar las capacidades de su explorador.  Se puede producir un comportamiento inesperado debido a una de las siguientes situaciones:  

*   El código dirigido a Windows Internet Explorer 8 puede ejecutarse de forma diferente en Microsoft Edge.  
*   Una característica que el explorador debe admitir está deshabilitada debido a una suposición realizada por el desarrollador.  

Si al cambiar la cadena de agente de usuario se elimina el problema, es probable que la detección del explorador causase.  

## Pantalla  

Emulación de pantalla para obtener una vista previa del sitio en diferentes tamaños y resoluciones de pantalla.  

*   monitores de escritorio convencionales  
*   pantallas móviles más pequeñas  
*   pantallas más recientes de alta resolución  

Las emulaciones están adaptadas para intentar coincidir las dimensiones físicas de las pantallas que se están emulando.  Los píxeles emulados pueden parecer comprimidos o expandidos. No se recomienda la emulación si necesita probar la posición perfecta de los elementos HTML en píxeles.  La emulación es, no obstante, adecuada para probar diseños con capacidad de respuesta e identificar problemas de posicionamiento de elementos más grandes.  

### Orientación  

Elija entre el modo **horizontal** o el **vertical** .  

### Resolución  

Elija una lista preestablecida de resoluciones de dispositivos populares o especifique su propia configuración **personalizada** .  Se admiten resoluciones de hasta 80 pulgadas y 3820 x 2160.  

## Geolocalización  

Si su sitio Web usa la [API de ubicación geográfica][MdnGeolocationUsing] para proporcionar servicios basados en la ubicación, las siguientes actividades estarán disponibles desde la comodidad de su escritorio.  

*   Pruebe fácilmente distintas coordenadas GPS  
*   prueba fácilmente diferentes Estados de los sensores  

La configuración suplanta las coordenadas de GPS reales y el estado de sensor en dispositivos que admiten geolocalización.  

Tu sitio web debe solicitar y tener permiso de un usuario antes de usar la ubicación del dispositivo.  Pruebe cómo se comporta su sitio con y sin permisos de ubicación en el panel de **configuración** de Microsoft Edge.  

**...** >  **Configuración**  >  **Ver configuración avanzada**  >  Permisos de sitio **Web**  >  **Administrar**  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Administrar permisos de sitio web desde el panel de configuración de Microsoft Edge" lightbox="./media/settings_manage_permissions.png":::
   Administrar permisos de sitio web desde el panel de **configuración** de Microsoft Edge  
:::image-end:::  

## Accesos directos

| Acción  | Acceso directo  |  
|:--- |:--- |  
| Restablecer la configuración de emulación | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Descargar nuevo explorador Microsoft Edge"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "API de ubicación geográfica | MDN"  
