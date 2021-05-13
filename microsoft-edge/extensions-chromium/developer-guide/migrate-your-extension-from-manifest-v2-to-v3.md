---
description: Obtenga información sobre cómo actualizar la extensión de Manifiesto V2 a V3
title: Prepararse para actualizar las extensiones de Manifiesto V2 a V3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones perimetrales, extensiones de explorador, complementos, desarrollador, manifiesto v3, migración a manifiesto v3
ms.openlocfilehash: 5aa1aa7446a312d581bacc4fa19ba7362c6c2a3e
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564619"
---
# <a name="prepare-to-update-your-extensions-from-manifest-v2-to-v3"></a>Prepararse para actualizar las extensiones de Manifest v2 a v3  

En este documento se enumeran los cambios importantes que se implementan como parte de Manifest v3, que es la siguiente versión de la plataforma Chromium extensions.  El Microsoft Edge de extensiones actualiza este documento a medida que avanza la implementación.  Para obtener instrucciones detalladas sobre cómo migrar la extensión a Manifiesto v3, vaya a [Migrar al manifiesto V3][ChromeDeveloperDocsExtensionsMv3Mv3MigrationChecklist].  

## <a name="remotely-hosted-code"></a>Código hospedado de forma remota  

Actualmente, partes del código de extensiones se hospedan de forma remota y no lo incluyen como parte del paquete de extensión durante el proceso de validación.  Aunque esto ofrece flexibilidad para cambiar el código sin volver a enviar la extensión al almacén, es posible que el código se aproveche después de la instalación.  Para asegurarse [Microsoft Edge listas][MicrosoftMicrosoftedgeAddons] de extensiones validadas, el equipo de extensiones de Microsoft Edge no permite que las extensiones utilicen código hospedado de forma remota.  Este cambio hace que las extensiones sea más segura.  Los desarrolladores tendrán que empaquetar y enviar todo el código usado por la extensión para su validación.  Como alternativa, puede usar la `eval()` función en un entorno de espacio [aislado.][ChromeDeveloperDocsExtensionsMv2Sandboxingeval]  

## <a name="run-time-host-permissions"></a>Permisos de host en tiempo de ejecución  

En el momento de la instalación, las extensiones pueden solicitar permisos de información general para tener acceso a todos los sitios y contenido.  Estos permisos permiten que las extensiones funcionen con una intervención mínima y creen un riesgo para la privacidad y la seguridad de los usuarios.  Para mejorar la transparencia, el equipo Microsoft Edge de extensiones proporciona controles para que los usuarios permitan o restrinjan el acceso a sitios web en tiempo de ejecución.  

## <a name="cross-origin-requests-in-content-scripts"></a>Solicitudes entre orígenes en scripts de contenido  

En la actualidad, los scripts de contenido solicitan acceso a cualquier origen, incluidos los orígenes que no están permitidos por el sitio web.  El comportamiento rompe los principios entre orígenes.  En el futuro, el equipo Microsoft Edge de extensiones de contenido requiere que los scripts de contenido tengan los mismos permisos que la página web en la que se insertan los scripts, lo que cierra un posible resquicio de seguridad.  Para realizar solicitudes entre orígenes, debe usar scripts en segundo plano para retransmitir respuestas a scripts de contenido.  Estos cambios están disponibles y detrás de una marca.  Para obtener más información, vaya a este [documento][ChromiumHomeChromiumSecurityExtensionContentScriptFetches].  

## <a name="web-request-api"></a>API de solicitud web  

El equipo Microsoft Edge de extensiones de web reemplaza la API de solicitud web por [la][ChromeDeveloperDocsExtensionsReferenceDeclarativenetrequest] [API][ChromeDeveloperDocsExtensionsReferenceWebrequest] declarativa de solicitud neta, pero sigue manteniendo las capacidades de observación de la API de solicitud web.  Excepto en algunos escenarios específicos en los que la extensión requiere capacidades de observación de la API de solicitud web, el equipo de extensiones de Microsoft Edge recomienda usar solo las API de DNR.  El Microsoft Edge de extensiones cree que este cambio tendrá un impacto positivo en las extensiones que usan funcionalidades declarativas enriquecibles con características.  A medida que más extensiones se desvían a las API de DNR, este cambio mejorará la privacidad del usuario, lo que contribuye a aumentar la confianza en el uso de extensiones.  
Las empresas pueden seguir usando el comportamiento de bloqueo de la API de solicitud web para extensiones administradas a través de directivas de empresa.  Para obtener más información acerca de las directivas de extensión, vaya [a Microsoft Edge – Directivas][DeployedgeMicrosoftEdgePoliciesExtensions].  

## <a name="background-service-workers"></a>Trabajadores del servicio en segundo plano  
 
Los trabajadores de servicio están disponibles para las pruebas en Canary.  Para migrar las extensiones de páginas en segundo plano a trabajadores de servicio, consulte Migración de páginas en segundo plano [a trabajadores de servicio.][ChromeDeveloperDocsExtensionsMv3MigratingToServiceWorkers]  El Microsoft Edge de extensiones de usuario está evaluando e investigando el impacto que este cambio produce tanto para los desarrolladores como para los usuarios.  El Microsoft Edge de extensiones agrega detalles adicionales sobre el cambio en este documento en el futuro.  

## <a name="when-are-these-changes-available-in-microsoft-edge"></a>¿Cuándo están disponibles estos cambios en Microsoft Edge  

La implementación de la API de solicitud neta declarativa actual está disponible en nuestros canales Estable y Beta.  Pruebe los cambios y proporcione comentarios.  El Microsoft Edge de extensiones contribuye a los esfuerzos de desarrollo e investiga más cambios.  

| Nombre del canal | Detalles |  
|:--- |:--- |  
| Microsoft Edge 84 Estable | La API de DNR está disponible para pruebas |  
| Microsoft Edge 85 Beta | La compatibilidad con la modificación de encabezados está disponible|  

Cuando se realizan los cambios en Chromium, el equipo de extensiones de Microsoft Edge comparte escalas de tiempo para que pueda actualizar el código y volver a publicar extensiones en el almacén.  

El Microsoft Edge de extensiones continúa publicando actualizaciones en el blog.  Puede proporcionar sus comentarios sobre los cambios a través de [tech Community][MicrosoftTechcommunityT5ArticlesManifestV3ChnagesAreNowAvailableInMicrosoftEdgeMP1780254].

<!-- links -->  

[DeployedgeMicrosoftEdgePoliciesExtensions]: /deployedge/microsoft-edge-policies#extensions "Extensiones - Microsoft Edge: directivas | Microsoft Docs"  

[MicrosoftMicrosoftedgeAddons]: https://microsoftedge.microsoft.com/addons "Microsoft Edge Complementos"  

[MicrosoftTechcommunityT5ArticlesManifestV3ChnagesAreNowAvailableInMicrosoftEdgeMP1780254]: https://techcommunity.microsoft.com/t5/articles/manifest-v3-changes-are-now-available-in-microsoft-edge/m-p/1780254 "Los cambios del manifiesto V3 ya están disponibles en Microsoft Edge | Microsoft Tech Community"  

[ChromeDeveloperDocsExtensionsMv2Sandboxingeval]: https://developer.chrome.com/docs/extensions/mv2/sandboxingEval "Uso de eval en extensiones de Chrome | Desarrolladores de Chrome"  
[ChromeDeveloperDocsExtensionsMv3MigratingToServiceWorkers]:  https://developer.chrome.com/docs/extensions/mv3/migrating_to_service_workers "Migración de páginas en segundo plano a trabajadores de servicio | Desarrolladores de Chrome"  
[ChromeDeveloperDocsExtensionsMv3Mv3MigrationChecklist]: https://developer.chrome.com/docs/extensions/mv3/mv3-migration-checklist "Lista de comprobación de migración de manifiesto V3 | Desarrolladores de Chrome"    

[ChromeDeveloperDocsExtensionsReferenceDeclarativenetrequest]: https://developer.chrome.com/docs/extensions/reference/declarativeNetRequest "chrome.declarativeNetRequest | Desarrolladores de Chrome"  
[ChromeDeveloperDocsExtensionsReferenceWebrequest]: https://developer.chrome.com/docs/extensions/reference/webRequest "chrome.webRequest | Desarrolladores de Chrome"  

[ChromiumHomeChromiumSecurityExtensionContentScriptFetches]: https://www.chromium.org/Home/chromium-security/extension-content-script-fetches "Cambios en solicitudes entre orígenes en scripts de contenido de extensión de Chrome | The Chromium Projects"  
