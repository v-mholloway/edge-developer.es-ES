---
description: Más información sobre cómo actualizar la extensión de manifest V2 a V3
title: Prepararse para actualizar las extensiones del manifiesto V2 a V3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de perímetro, extensiones de explorador, addons, desarrollador, manifiesto V3, migrar a manifest V3'
ms.openlocfilehash: 262a5cab54dd23f596791c93ec1238619e247333
ms.sourcegitcommit: 1ad087b00df16fd7718a5d95226de57e29b335e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "11117835"
---
# Prepararse para actualizar las extensiones del manifiesto V2 a V3 

En este documento se enumeran los cambios importantes que se implementan como parte del manifiesto V3, que es la siguiente versión de la plataforma extensiones de cromo. Actualizaremos este documento a medida que se progrese la implementación. Para obtener instrucciones detalladas sobre cómo migrar su extensión al manifiesto V3, vaya a [migrar al manifiesto V3][Google_Migrate_to_MV3]. 

## Código hospedado de forma remota  

Hoy, las extensiones pueden hospedar partes de su código de forma remota y no incluirla como parte del paquete de extensión durante el proceso de validación. A pesar de que esto ofrece flexibilidad para cambiar el código sin reenviar la extensión a la tienda, el código puede ser aprovechado después de la instalación. Para garantizar que los [Complementos de Microsoft Edge][EdgeAddons] enumeren las extensiones validadas, no permitimos que las extensiones usen código hospedado de forma remota. Este cambio hace que las extensiones sean más seguras. Los desarrolladores necesitarán empaquetar y enviar todo el código que se usa en la extensión para la validación. Como alternativa, los desarrolladores pueden usar la función eval () en un [entorno de espacio aislado][sandboxingEval]. 

## Permisos de host en tiempo de ejecución  

En el momento de la instalación, las extensiones pueden solicitar permisos globales para obtener acceso a todos los sitios y contenido. Estos permisos permiten que las extensiones funcionen con una mínima intervención y crean un riesgo para la privacidad y la seguridad del usuario. Para mejorar la transparencia, proporcionamos controles para que los usuarios permitan o restrinjan el acceso a los sitios web en tiempo de ejecución. 

## Solicitudes de origen cruzado en scripts de contenido  

Hoy, los scripts de contenido pueden solicitar acceso a cualquier origen, incluidos los orígenes no permitidos por el sitio Web. Este comportamiento rompe los principios de origen cruzado. En el futuro, requerimos que los scripts de contenido tengan los mismos permisos que la página en la que se insertan, cerrando una posible Laguna de seguridad. Para realizar solicitudes de origen cruzado, tendrá que usar scripts de segundo plano para retransmitir respuestas a los scripts de contenido. Estos cambios están disponibles y detrás de una marca. Para obtener más información, vaya a este [documento][CORS]. 

## API de solicitudes Web  

Reemplazamos la [API de solicitudes web][WebRequestAPI] con la [API de solicitudes de red declarativa][DeclarativeNetRequestAPI], pero continuamos manteniendo las capacidades de observación de la API de solicitudes Web. A excepción de algunos escenarios específicos en los que la extensión necesita capacidades de observación de la API de solicitudes Web, le recomendamos que use solo las API de DNR. Creemos que este cambio tendrá un impacto positivo en las extensiones que usan capacidades declarativas enriquecidas con características. A medida que se pasa más extensiones a las API de DNR, este cambio mejorará la privacidad de los usuarios, lo que contribuye a mejorar la confianza en el uso de extensiones.
Las empresas pueden continuar usando el comportamiento de bloqueo de la API de solicitudes web para las extensiones administradas mediante directivas de empresa. Para obtener más información sobre las directivas de extensión, vaya a [Microsoft Edge: directivas][MicrosoftEdgePolicies]. 

## Trabajadores de servicio en segundo plano  
 
Los trabajadores del servicio están disponibles para realizar pruebas en la Canarias. Para migrar las extensiones de las páginas de fondo a los trabajos de servicio, consulte [migrar de páginas de fondo a trabajos de servicio][ServiceWorkers]. Estamos evaluando & investigando el impacto que este cambio aporta a los usuarios y a los programadores. Agregaremos más detalles sobre este cambio a este documento en el futuro. 

## ¿Cuándo estarán disponibles estos cambios en Microsoft Edge?

La implementación de la API de la solicitud de red declarativa actual está disponible en nuestros canales de versión estable y beta. Los programadores pueden probar estos cambios y enviar comentarios. Contribuiremos a realizar esfuerzos de desarrollo y a investigar cambios adicionales. 

| Nombre del canal | Descripción |
|:--- |:--- |  
| Microsoft Edge 84 estable | La API de DNR está disponible para pruebas |  
| Microsoft Edge 85 beta | La compatibilidad con la modificación de encabezados está disponible| 

Cuando se realicen cambios en el cromo, compartiremos escalas de tiempo para que los desarrolladores puedan actualizar su código y volver a publicar las extensiones para la tienda. 

Continuaremos publicando actualizaciones en nuestro blog. Puede enviar sus comentarios sobre estos cambios a través de [TechCommunity][TechCommunity].

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/ "Complementos de Microsoft Edge"  
[MicrosoftBlog]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration/  
[MicrosoftEdgePolicies]: https://docs.microsoft.com/deployedge/microsoft-edge-policies#extensions 

[TechCommunity]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Comunidad tecnológica"  


[Google_Migrate_to_MV3]: https://developer.chrome.com/extensions/migrating_to_manifest_v3   
[SandboxingEval]: https://developer.chrome.com/apps/sandboxingEval "Usar eval en las extensiones de Chrome. Puede."
[CORS]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Cambios en las solicitudes de origen cruzado en scripts de contenido de extensión"
[WebRequestAPI]: https://developer.chrome.com/extensions/webRequest "API de solicitudes Web"  
[DeclarativeNetRequestAPI]: https://developer.chrome.com/extensions/declarativeNetRequest/ "API de solicitudes de red declarativa"
[ServiceWorkers]:  https://developers.chrome.com/extensions/migrating_to_service_workers


