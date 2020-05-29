---
description: Use el panel de emulación para probar diferentes perfiles de explorador, tamaños de pantalla y resoluciones, y coordenadas de ubicación GPS
title: 'DevTools: emulación'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, emulación de dispositivos, diseño dinámico, ubicación geográfica, resolución
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573838"
---
# Emulación

El panel de *emulación* le ayuda a:
 - Simular diversos [perfiles de dispositivos](#device), [exploradores](#browser-profile), [tamaños de pantalla y resoluciones](#display)
 - Probar distintas [configuraciones y coordenadas geolocales](#geolocation)

![El panel de emulación DevTools de Microsoft Edge](./media/emulation.png)

1. El botón **conservar la configuración de emulación** guardará los cambios que haya realizado desde la configuración de emulación de escritorio predeterminada, incluso cuando cierra y vuelve a abrir la DevTools. 

2. El botón **restablecer configuración de emulación** restablecerá la configuración de emulación al perfil de explorador de *escritorio* predeterminado y a la cadena de agente de usuario de Microsoft Edge con GPS desactivado.

3. Cuando se cambia la configuración predeterminada de cualquiera de estas opciones, la pestaña **emulación** mostrará una alerta informativa para indicar que se está emulando algún aspecto del comportamiento del explorador.

## Dispositivo

Elija entre una lista preestablecida de perfiles de dispositivo de Windows que configure automáticamente las demás opciones de emulación o especifique su propia configuración *personalizada* . Cambie de nuevo a *predeterminado* para restablecer todas las herramientas de emulación.

## Modo

### Perfil de explorador
Una forma rápida de simular una página en un dispositivo Windows Phone es cambiar la configuración del **Perfil del explorador** a *Windows Phone*.

#### Cadena de agente de usuario

Modificar la cadena de agente de usuario para imitar a otro explorador es un buen primer paso en la depuración de errores que solo ocurren en Microsoft Edge. 

Los scripts de front-end y/o back-end a veces usan la cadena de agente de usuario para detectar qué explorador está usando. Y incluso si no usa la detección del explorador en su propio código, es posible que esté usando una biblioteca de JavaScript de terceros o una secuencia de comandos del servidor que sí lo hace.

El problema con la detección de explorador es que a menudo se usa para cambiar de tamaño o cambiar las características de una página web en función de lo que el desarrollador que escribe la secuencia de comandos cree que su explorador puede hacer, en lugar de detectar qué es lo que su explorador puede hacer realmente usando la detección de características. Esto puede provocar un comportamiento inesperado, ya que el código destinado a Windows Internet Explorer 8 puede ejecutarse de forma muy diferente en Microsoft Edge. o una característica que el explorador sea perfectamente capaz de admitir puede estar deshabilitada debido a una suposición realizada por el desarrollador.

Si al cambiar la cadena de agente de usuario se elimina el problema, es probable que la detección del explorador causase.

## Pantalla

La emulación de pantalla le permite obtener una vista previa del sitio en diferentes tamaños y resoluciones de pantalla: desde monitores de escritorio convencionales hasta pantallas móviles más pequeñas o pantallas de alta resolución más recientes.

Las emulaciones están adaptadas para probar y hacer coincidir las dimensiones físicas de las pantallas que se están emulando. Es posible que los píxeles emulados parezcan comprimidos o expandidos, y no se recomienda la emulación si necesita probar la posición perfecta de los elementos HTML en píxeles. La emulación es, no obstante, adecuada para probar diseños con capacidad de respuesta e identificar problemas de posicionamiento de elementos más grandes.

### Orientación

Elija entre el modo *horizontal* o el *vertical* .

### Resolución

Elija una lista preestablecida de resoluciones de dispositivos populares o especifique su propia configuración *personalizada* . Se admiten resoluciones de hasta 80 pulgadas y 3820 x 2160.

## Geolocalización

Si su sitio usa la [API de ubicación](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) geográfica para proporcionar servicios basados en la ubicación, puede probar fácilmente distintas coordenadas GPS y Estados de los sensores desde la comodidad de su escritorio. Esta configuración invalidará las coordenadas de GPS reales y el estado de sensor en los equipos que admitan geolocalización. 

Al igual que con el uso de datos personales en la web, los usuarios primero tendrán que conceder permiso a su sitio para usar su ubicación. Puede probar cómo se comporta su sitio con y sin permisos de ubicación en el panel de *configuración* de Microsoft Edge:

**...** >  **Configuración**  >  **Ver configuración avanzada**  >  Permisos de sitio **Web**  >  **Administrar**

![Administrar permisos de sitio web desde el panel de configuración de Microsoft Edge](./media/settings_manage_permissions.png)

## Abreviados

| Acción                   | Método abreviado               |
|:-------------------------|:-----------------------|
| Restablecer la configuración de emulación | `CTRL` + `SHIFT` + `L` |
