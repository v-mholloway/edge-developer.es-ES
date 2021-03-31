---
description: Esta página proporciona documentación sobre la cadena de agente de usuario de Microsoft Edge
title: Cadena de agente de usuario de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidad, plataforma web, cadena de agente de usuario, cadena de UA, UA Overrides
ms.openlocfilehash: 73401219b7708a739292a46b6131fe40765e9c8c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574934"
---
# Cadena de agente de usuario de Microsoft Edge (escritorio)  

Una cadena de agente de usuario \(UA \) puede usarse para detectar qué versión de un explorador específico se está usando en un determinado sistema operativo.  Al igual que otros exploradores, Microsoft Edge incluye esta información en el `User-Agent` encabezado HTTP cada vez que realiza una solicitud a un sitio.  También se puede acceder a ella mediante JavaScript consultando el valor de `navigator.userAgent` .  

Microsoft recomienda que los desarrolladores web usen la [detección de características](https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection) siempre que sea posible para mejorar la mantenibilidad del código, reducir la fragilidad del código y eliminar el riesgo de ruptura de código en el caso de futuras actualizaciones de la cadena de agente de Office.  

Para los casos en los que la detección de características no es aplicable y se debe usar UA detección, el formato del agente de Microsoft Edge de Microsoft Edge es el siguiente:

El `User-Agent` encabezado de la solicitud tiene el siguiente formato:

```http
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43
``` 

El valor devuelto de `navigator.userAgent` tiene el siguiente formato:

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.74 Safari/537.36 Edg/79.0.309.43"
```  

Los identificadores de plataforma cambian en función del sistema operativo que se use y los números de versión también aumentan a medida que transcurre el tiempo.  Este formato es el mismo que el agente de la UA, con la adición de un nuevo `Edg` token al final.  Microsoft seleccionó el `Edg` token para evitar problemas de compatibilidad que se pueden producir al usar la cadena `Edge` , que se usa en la versión de Microsoft Edge basada en EdgeHTML.  El `Edg` token también es coherente con los [tokens existentes](https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer/) que se usan en iOS y Android.

## Asignar cadena UA a nombre del explorador
Asignar tokens de cadena UA a un nombre de explorador más legible para el usuario para su uso en el código es un patrón común en la web hoy mismo. Al asignar el nuevo `Edg` token al nombre de un explorador, Microsoft recomienda usar un nombre diferente al de los programadores que se usan en la versión heredada de Microsoft Edge para evitar que se apliquen accidentalmente las soluciones alternativas heredadas que no son aplicables a exploradores basados en cromo.

## Invalidaciones de agentes de usuario  

En ocasiones, un sitio web no reconoce la versión actualizada del agente de agente de Microsoft Edge.  Como resultado, es posible que un conjunto de características de ese sitio web no funcione correctamente.  Cuando se le notifique a Microsoft acerca de estos tipos de problemas, los propietarios del sitio web se comunican con él y le informan sobre el agente de UA actualizado.  

A menudo, los sitios necesitan actualizar y probar la lógica de detección de UA para solucionar los problemas que Microsoft notifica a los propietarios del sitio.  En estos casos, Microsoft usa una lista de reemplazos de UA en nuestros canales beta y estable para maximizar la compatibilidad de los usuarios que tienen acceso a estos sitios.  Las invalidaciones especifican nuevos valores de UA que Microsoft Edge debe enviar en lugar del agente de UA predeterminado de sitios específicos.  Puede ver la lista de reemplazos de UA que se están aplicando `edge://compat/useragent` en los canales de versión beta y estable de Microsoft Edge. 

Nuestros canales Canarias y dev actualmente no reciben invalidaciones de UA para que los desarrolladores web tengan un entorno donde puedan reproducir fácilmente problemas en sus sitios causados por el agente de Microsoft Edge predeterminado.  Si, por algún motivo, necesita poder deshabilitar el agente de inicialización de UA en los canales beta o estable de Microsoft Edge, puede ejecutar el archivo ejecutable de Microsoft Edge con el siguiente argumento de la línea de comandos:  

```shell
--disable-domain-action-user-agent-override
```  
