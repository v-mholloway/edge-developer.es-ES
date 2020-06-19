---
description: Esta página proporciona un resumen de cambios de alto impacto que podrían afectar a la compatibilidad del sitio
title: Cambios que afectan a la compatibilidad del sitio que llegan a Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidad, plataforma web
ms.openlocfilehash: 6a57ffb4a2c36420d1abe4ec151342e5b77d4c7c
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752195"
---
# Cambios que afectan a la compatibilidad del sitio que llegan a Microsoft Edge  

La web está evolucionando constantemente para mejorar la experiencia, la seguridad y la privacidad del usuario.  En algunos casos, los cambios pueden ser lo suficientemente significativos como para influir en la funcionalidad de las páginas existentes.  En la tabla siguiente se resumen los cambios de gran impacto que el equipo de Microsoft Edge está siguiendo actualmente.  Inténtalo de nuevo a menudo; el equipo de Microsoft Edge actualiza esta página según evoluciona el pensamiento, se consolidan las escalas de tiempo y se anuncian nuevos cambios.  

| Cambio | Canal estable | Experimentación | Información adicional |  
|:--- |:--- |:--- |:--- |
| Las cookies tienen como predeterminada `SameSite=Lax` | [Cromo o cromo + 1](#release-comments)  | Canarias V82, dev V82 | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, revise la entrada de estado de la [plataforma de cromo][ChromePlatformStatus5088147346030592].  |  
| Directiva de referencia de sitios: predeterminada para `strict-origin-when-cross-origin` | [Cromo o cromo + 1](#release-comments)  | Canarias V79, dev V79 | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, revise la entrada de estado de la [plataforma de cromo][ChromePlatformStatus6251880185331712].  |  
| No permitir XmlHttpRequest sincrónico en el descarte de página | [Chrome + 1](#release-comments) \ (Edge V83 \) |  | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  El cromo coincidente, Microsoft Edge ofrece una directiva de grupo para deshabilitar este cambio hasta Edge 88.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, revise la entrada de estado de la [plataforma de cromo][ChromePlatformStatus4664843055398912].  |  
| Mostrar sutil aviso de solicitudes de permisos de notificación |  | Canarias V83, dev V83 | Ahora, los usuarios pueden optar por no molestar las solicitudes de notificación en `edge://settings/content/notifications` .  Con esta opción habilitada, Microsoft Edge muestra un icono de solicitud sutil en la barra de direcciones para los sitios que solicitan que los usuarios envíen notificaciones futuras a través de la `Notifications` `Push` API o.  Este icono sutil reemplaza la solicitud de permiso de control flotante.  Un experimento en la Canarias y el desarrollo activa este comportamiento de forma predeterminada para algunos usuarios en todos los sitios que solicitan permisos de notificaciones.  Los usuarios pueden dejar de participar `edge://settings/content/notifications` .  En el futuro, el equipo de Microsoft Edge puede explorar la visualización de la indicación de control flotante en situaciones específicas, en función de los comportamientos del usuario y otros datos introducidos.  |  
| Deshabilitar TLS/1.0 y TLS/1.1 de forma predeterminada | Edge v84 |  | Para ayudar a descubrir los sitios afectados, puedes establecer la `edge://flags/#display-legacy-tls-warnings` marca para hacer que Microsoft Edge muestre un aviso "no seguro" de no bloqueo al cargar páginas que requieran protocolos TLS heredados.  La Directiva de grupo [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] permite volver a habilitar TLS/1.0 y TLS/1.1; la política estará disponible hasta el borde 88.  |  
| Bloquear descargas de contenido mixto | [Chrome + 1](#release-comments) \ (Edge V85 \)  |  | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, revise la [entrada de blog de seguridad de Google][GoogleBlogSecurity20200206].  La programación de lanzamiento de Microsoft sobre tipos de archivo para advertir o bloquear está planificada para una versión posterior a Chrome.  |  
| Eliminación de Adobe Flash | Edge V88  |  | Este cambio sucede en el proyecto de cromo, en el que se basa Microsoft Edge.  Para obtener más información, consulta la [Guía básica de cromo de Adobe Flash](https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021-).  | 
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


<!-- image links -->  

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin-Microsoft Edge-directivas"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "No permitir la sincronización de XHR en la página de estado de la plataforma JavaScript-Chrome"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Cookies de forma predeterminada en SameSite = LAX: estado de la plataforma Chrome"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Directiva de sitios de referencia: valor predeterminado para el estado de la plataforma de origen de los cruces"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Proteger a los usuarios de descargas no seguras en Google Chrome-blog de seguridad en línea de Google"  
