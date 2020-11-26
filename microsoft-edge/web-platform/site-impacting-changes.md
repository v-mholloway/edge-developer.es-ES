---
description: Proporciona un resumen de los cambios de alto impacto que pueden afectar a la compatibilidad del sitio.
title: Cambios que afectan a la compatibilidad del sitio que llegan a Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidad, plataforma web
ms.openlocfilehash: 8c872546b29633cb22e0095fdd1a0326f89fc087
ms.sourcegitcommit: 5d3802721036dc7cd90e9e6f7ac90dc3acc24eec
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "11191558"
---
# Cambios que afectan a la compatibilidad del sitio que llegan a Microsoft Edge  

La web evoluciona constantemente para mejorar la experiencia del usuario, la seguridad y la privacidad.  En algunos casos, los cambios pueden ser lo suficientemente significativos como para influir en la funcionalidad de las páginas existentes.  En la tabla siguiente se resumen los cambios de gran impacto que el equipo de Microsoft Edge está siguiendo actualmente.  Revise este artículo con frecuencia; el equipo de Microsoft Edge actualiza la siguiente página a medida que evoluciona el pensamiento, se consolidan las escalas de tiempo y se anuncian nuevos cambios.  

| Cambiar | Canal estable | Experimentación | Información adicional |  
|:--- |:--- |:--- |:--- |
| Cookies de forma predeterminada `SameSite=Lax` y `SameSite=None-requires-Secure` | [Chrome + 1](#release-comments) \ (Edge V86 \)  | Canarias V82, dev V82 | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, navegue a la entrada de estado de la [plataforma de cromo][ChromePlatformStatus5088147346030592].  |  
| Directiva de referencia de sitios: predeterminada para `strict-origin-when-cross-origin` | [Chrome + 1](#release-comments) \ (Edge V86 \)  | Canarias V79, dev V79 | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, navegue a la entrada de estado de la [plataforma de cromo][ChromePlatformStatus6251880185331712].  |  
| No permitir la sincronización sincrónica `XmlHttpRequest` en la página | [Chrome + 1](#release-comments) \ (Edge V83 \) |  | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Cromo coincidente, Microsoft Edge ofrece una directiva de grupo para desactivar este cambio hasta Edge V88.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, navegue a la entrada de estado de la [plataforma de cromo][ChromePlatformStatus4664843055398912].  |  
| Mostrar sutil aviso de solicitudes de permisos de notificación | Edge v84 |  | Las solicitudes de notificación silenciosas muestran un icono de solicitud sutil en la barra de direcciones para permisos de notificación de sitio solicitados mediante la `Notifications` `Push` API o, reemplazando la interfaz de usuario del mensaje flotante de permiso completo o estándar.  Esta característica está actualmente habilitada para todos los usuarios.  Para no participar en las solicitudes de notificación, vaya a `edge://settings/content/notifications` .  En el futuro, el equipo de Microsoft Edge puede explorar la reactivación del aviso de notificación de control flotante en algunos escenarios.  |  
| Desactivar TLS/1.0 y TLS/1.1 de forma predeterminada | Edge v84 |  | La Directiva de grupo [SSLMinVersion][DeployedgePoliciesSslversionmin] permite volver a habilitar TLS/1.0 y TLS/1.1; la política estará disponible hasta el borde de la periferia.  |  
| Bloquear descargas de contenido mixto | [Chrome + 1](#release-comments) \ (Edge V86 \)  |  | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, vaya a la [entrada de blog seguridad de Google][GoogleBlogSecurity20200206].  La programación de lanzamiento de Microsoft sobre tipos de archivo para advertir o bloquear está planificada para una versión posterior a Chrome.  |  
| Desuso AppCache | [Chrome + 1](#release-comments) \ (Edge V86 \)  |  | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, vaya a la [documentación del WebDev][WebDevAppCacheRemoval].  La programación de lanzamiento de Microsoft para la degradación está planificada para una versión posterior a Chrome.  Solicitar un [token de OriginTrial de AppCache][ChromeDevelopersOrigintrialsAppCacheOriginTrial] permite a los sitios continuar usando la API obsoleta hasta que es Edge V90.  |  
| Eliminación de Adobe Flash | Edge V88  |  | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, vaya a la [Guía básica de cromo de Adobe Flash][ChromiumFlashRoadmapSupportRemoved].  | 
| Desactivar y quitar FTP | Edge V88  | Versión beta de Edge V87 | En Edge beta V87, la compatibilidad con FTP está desactivada de forma predeterminada; en la V87 de borde estable, permanece habilitado.  En Edge V88, la compatibilidad con FTP se ha eliminado por completo.  Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, vaya a la entrada de estado de la [plataforma de cromo][ChromePlatformStatus6246151319715840].  Las empresas que dispongan de sitios que aún necesiten compatibilidad con FTP pueden seguir usando el FTP configurando el sitio para usar el [modo IE][DeployedgeEdgeIeMode].  | 
| Autoactualizar imágenes de contenido mixtas | Edge V88  |  | Las referencias no seguras (HTTP) a las imágenes se actualizan automáticamente a HTTPS; Si la imagen no está disponible a través de HTTPS, se produce un error en la descarga de la imagen. Hay disponible una [Directiva de grupo][DeployedgePoliciesInsecurecontentallowedforurls] para controlar esta característica. Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge. Para obtener más información, vaya a la entrada de estado de la [plataforma de cromo][ChromePlatformStatus4926989725073408].  |  

##### Publicar comentarios  

:::row:::
   :::column span="1":::
      Chrome + 1
   :::column-end:::
   :::column span="2":::
      En función de los comentarios de los usuarios y los programadores, la característica indicada o el cambio se envía una versión posterior a Chrome.
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Cromo o cromo + 1
   :::column-end:::
   :::column span="2":::
      En función de los comentarios de los usuarios y los programadores, la característica o el cambio indicado se suministran al mismo tiempo o una versión posterior a Chrome.
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Acerca del modo IE | Microsoft docs"  
[DeployedgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls-Microsoft Edge-Policies | Microsoft docs"  
[DeployedgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin-Microsoft Edge-Policies | Microsoft docs"  

[ChromePlatformStatus4664843055398912]: https://chromestatus.com/feature/4664843055398912 "No permitir la sincronización de XHR en la página JavaScript de desecho | Estado de la plataforma Chrome"  
[ChromePlatformStatus4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Imagen de AutoUpgrade contenido mixto | Estado de la plataforma Chrome"  
[ChromePlatformStatus5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Las cookies se envían de forma predeterminada a SameSite = LAX | Estado de la plataforma Chrome"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Compatibilidad con FTP en desuso | Estado de la plataforma Chrome"  
[ChromePlatformStatus6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Directiva de sitios de referencia: valor predeterminado para el origen estricto-origen del tiempo Estado de la plataforma Chrome"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Compatibilidad con Flash quitada de cromo (destino: Chrome 88 +-ene 2021)-Guía rápida | Proyectos de cromo"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache OriginTrial token | Desarrolladores de Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Proteger a los usuarios de descargas no seguras en Google Chrome-blog de seguridad en línea de Google" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Preparando para quitar AppCache | Web. dev"  

<!--todo:  cleanup links  -->  
