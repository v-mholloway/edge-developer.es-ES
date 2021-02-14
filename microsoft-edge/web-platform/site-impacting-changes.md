---
description: Proporciona un resumen de los cambios de alto impacto que pueden afectar a la compatibilidad del sitio
title: Cambios que afectan la compatibilidad del sitio próximamente en Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidad, plataforma web
ms.openlocfilehash: 64cdb417e6bd0aa648c7e1225bb6dc522f3873ce
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327508"
---
# Cambios que afectan la compatibilidad del sitio próximamente en Microsoft Edge  

La web evoluciona constantemente para mejorar la experiencia del usuario, la seguridad y la privacidad.  En algunos casos, los cambios pueden ser lo suficientemente importantes como para afectar a la funcionalidad de las páginas existentes.  En la tabla siguiente se resumen los cambios especialmente importantes que el equipo de Microsoft Edge está realizando actualmente.  Revise este artículo con frecuencia; El equipo de Microsoft Edge actualiza la página siguiente a medida que el pensamiento evoluciona, las escalas de tiempo se solidifican y se anuncian nuevos cambios.  

| Cambiar | Canal estable | Experimentación | Información adicional |  
|:--- |:--- |:--- |:--- |
| Las cookies se utilizan de forma `SameSite=Lax` predeterminada en y `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Este cambio se está produciendo en el proyecto chromium, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, vaya a la [entrada Estado de la plataforma Chrome.][ChromePlatformStatus5088147346030592]  |  
| Directiva de referencia: valor predeterminado `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Este cambio se está produciendo en el proyecto chromium, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, vaya a la [entrada Estado de la plataforma Chrome.][ChromePlatformStatus6251880185331712]  |  
| No permitir el rechazo sincrónico `XmlHttpRequest` en el rechazo de página | [Chrome+1](#release-comments) \(Edge v83\) |  | Este cambio se está produciendo en el proyecto chromium, en el que se basa Microsoft Edge.  Al coincidir con Chrome, Microsoft Edge ofrece una directiva de grupo para desactivar este cambio hasta Edge v88.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, vaya a la [entrada Estado de la plataforma Chrome.][ChromePlatformStatus4664843055398912]  |  
| Mostrar un mensaje sutil para solicitudes de permisos de notificación | Edge v84 |  | Las solicitudes de notificación silenciosas muestran un icono de solicitud sutil en la barra de direcciones para los permisos de notificación del sitio solicitados mediante la API o la API, reemplazando la interfaz de usuario del control desplegable de permisos completa o `Notifications` `Push` estándar.  Esta característica está habilitada actualmente para todos los usuarios.  Para no participar en las solicitudes de notificación silenciosas, vaya a `edge://settings/content/notifications` .  En el futuro, el equipo de Microsoft Edge puede explorar la posibilidad de volver a habilitar el aviso de notificación de control desplegable completo en algunos escenarios.  |  
| Desactivar TLS/1.0 y TLS/1.1 de forma predeterminada | Edge v84 |  | La [directiva de grupo SSLMinVersion][DeployedgeMicrosoftEdgePoliciesSslversionmin] permite volver a habilitar TLS/1.0 y TLS/1.1; la directiva permanece disponible hasta edge v90.  |  
| Bloquear descargas de contenido mixto | [Chrome+1](#release-comments) \(Edge v86\)  |  | Este cambio se está produciendo en el proyecto chromium, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, vaya a la entrada del blog de [seguridad de Google.][GoogleBlogSecurity20200206]  La programación de lanzamiento de Microsoft en tipos de archivo para advertir o bloquear está planeada para una versión después de Chrome.  |  
| AppCache en desuso | [Chrome+1](#release-comments) \(Edge v86\)  |  | Este cambio se está produciendo en el proyecto chromium, en el que se basa Microsoft Edge.  Para obtener más información, vaya a la [documentación de WebDev][WebDevAppCacheRemoval].  La programación de lanzamiento de Microsoft para el desuso está planeada para una versión después de Chrome.  Solicitar un token [OriginTrial de AppCache][ChromeDevelopersOrigintrialsAppCacheOriginTrial] permite a los sitios seguir usando la API en desuso hasta Edge v90.  |  
| Eliminación de Adobe Flash | Edge v88  |  | Este cambio se está produciendo en el proyecto chromium, en el que se basa Microsoft Edge.  Para obtener más información, vaya al mapa [de ruta de Adobe Flash Chromium.][ChromiumFlashRoadmapSupportRemoved]  | 
| Desactivar y quitar FTP | Edge v88  | Edge Beta v87 | En Edge Beta v87, la compatibilidad con FTP está desactivada de forma predeterminada; en edge estable v87 permanece habilitado.  En Edge v88, la compatibilidad con FTP se quita por completo.  Este cambio se está produciendo en el proyecto chromium, en el que se basa Microsoft Edge.  Para obtener más información, vaya a la entrada [de estado de la plataforma Chrome.][ChromePlatformStatus6246151319715840]  Las empresas que tienen sitios que aún requieren compatibilidad con FTP pueden seguir usando FTP configurando el sitio para usar el [modo IE.][DeployedgeEdgeIeMode]  | 
| Autoupgrade mixed content images | Edge v88  |  | Las referencias a imágenes no seguras \(HTTP\) se actualizan automáticamente a HTTPS; si la imagen no está disponible a través de HTTPS, se produce un error en la descarga de la imagen. Hay [disponible una directiva][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] de grupo para controlar esta característica. Este cambio se está produciendo en el proyecto chromium, en el que se basa Microsoft Edge. Para obtener más información, vaya a la [entrada Estado de la plataforma Chrome.][ChromePlatformStatus4926989725073408]  | 
| No se puede hacer la autenticación HTTP cuando se bloquean las cookies de terceros  | Edge v87  |  | A partir de Edge v87, cuando se bloquean las cookies para solicitudes de terceros, ya sea mediante la directiva [BlockThirdPartyCookies][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] o a través de la página Configuración perimetral, la autenticación HTTP tampoco se permite. Este cambio puede afectar a las descargas de la lista de sitios del Modo de empresa para el modo [Internet Explorer][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] si el punto de conexión que hospeda la lista requiere el uso de la autenticación HTTP.  Para permitir el uso de cookies y la autenticación HTTP para las descargas de la lista de sitios del Modo de empresa, agrega un patrón de dirección URL que coincida con la directiva [CookiesAllowedForURLs.][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]  |   

##### Comentarios de la versión  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      En función de los comentarios de los usuarios y los desarrolladores, la característica o el cambio indicados incluye una versión después de Chrome.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome o Chrome+1  
   :::column-end:::
   :::column span="2":::
      En función de los comentarios de los usuarios y los desarrolladores, la característica o el cambio indicado se incluye al mismo tiempo o una versión después de Chrome.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Acerca del modo IE | Microsoft Docs"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Configurar mediante la directiva de lista de sitios web de IE del Modo de empresa: configurar directivas de modo IE | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies - Microsoft Edge - Directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls - Microsoft Edge - Directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge - Directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge - Directivas | Microsoft Docs"  

[ChromePlatformStatus4664843055398912]: https://chromestatus.com/feature/4664843055398912 "No permitir la sincronización XHR en el rechazo de página de JavaScript | Estado de la plataforma Chrome"  
[ChromePlatformStatus4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Autoupgrade Image Mixed Content | Estado de la plataforma Chrome"  
[ChromePlatformStatus5088147346030592]: https://chromestatus.com/feature/5088147346030592 "El valor predeterminado de las cookies es SameSite=Lax | Estado de la plataforma Chrome"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Compatibilidad con FTP en desuso | Estado de la plataforma Chrome"  
[ChromePlatformStatus6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Directiva de referencia: valor predeterminado de strict-origin-when-cross-origin | Estado de la plataforma Chrome"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Compatibilidad con Flash eliminada de Chromium (destino: Chrome 88+ - ene 2021): plan de desarrollo de Flash | Proyectos de Chromium"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Token OriginTrial de AppCache | Desarrolladores de Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Proteger a los usuarios de descargas inseguras en Google Chrome: blog de seguridad de Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Preparación para la eliminación de AppCache | web.dev"  

<!--todo:  cleanup links  -->  
