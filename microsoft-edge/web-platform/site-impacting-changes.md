---
description: Proporciona un resumen de los cambios de alto impacto que pueden afectar a la compatibilidad del sitio
title: Cambios que afectan la compatibilidad del sitio próximamente en Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidad, plataforma web
ms.openlocfilehash: 842e57af361c18715bfb3c001679fabb4a86d0dd
ms.sourcegitcommit: 9f5dd05432f87339f4c3d71f1f9ce1d06afcaf4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/23/2021
ms.locfileid: "11675144"
---
# <a name="site-compatibility-impacting-changes-coming-to-microsoft-edge"></a>Cambios que afectan la compatibilidad del sitio próximamente en Microsoft Edge  

La plataforma web es una colección de tecnologías usadas para crear páginas web.  Las tecnologías incluyen HTML, CSS, JavaScript y muchos otros estándares abiertos.  La plataforma web evoluciona constantemente para mejorar la experiencia del usuario, la seguridad y la privacidad.  En algunos casos, los cambios pueden afectar a la funcionalidad de las páginas web existentes.  Para obtener más información acerca de los próximos Chromium de la plataforma web del proyecto, vaya a Escala de [tiempo de chrome Platform Status Release][ChromestatusFeaturesSchedule].  

Microsoft Edge adopta casi todos los cambios ascendentes en la plataforma web desde el Chromium proyecto.  Entre los motivos se incluyen las razones de funcionalidad y compatibilidad.  Microsoft mantiene el control total del explorador Microsoft Edge y puede aplazar o rechazar los cambios.  El Microsoft Edge decidir si el cambio beneficia a los usuarios del explorador.  Las áreas de características Microsoft Edge planean desviarse de Chromium cambios en el tiempo o el comportamiento se observan en la tabla siguiente.  La tabla también resalta los cambios de alto impacto que el equipo Microsoft Edge está siguiendo.  

Revise este artículo con frecuencia.  El Microsoft Edge actualiza este artículo a medida que evoluciona el pensamiento, se solidifican las escalas de tiempo y se anuncian nuevos cambios.  

| Cambio | Canal estable | Experimentación | Información adicional |  
|:--- |:--- |:--- |:--- |
| No permitir el despido `XmlHttpRequest` sincrónico en la página | [Chrome+1](#release-comments) \(Edge v83\) |  | Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa.  Al coincidir con Chrome, Microsoft Edge ofrece una directiva de grupo para desactivar este cambio hasta edge v88.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, vaya a la [entrada Estado de la plataforma Chrome][ChromestatusFeature4664843055398912].  |  
| Mostrar un mensaje sutil para solicitudes de permisos de notificación | Edge v84 |  | Las solicitudes de notificación silenciosas muestran un icono de solicitud sutil en la barra de direcciones para los permisos de notificación del sitio solicitados mediante la API or, reemplazando la interfaz de usuario de aviso de control de control de permisos completo o `Notifications` `Push` estándar.  Esta característica está habilitada actualmente para todos los usuarios.  Para desactivar las solicitudes de notificación silenciosas, vaya a `edge://settings/content/notifications` .  En el futuro, el Microsoft Edge puede explorar la posibilidad de volver a habilitar el mensaje de notificación de control total en algunos escenarios.  |  
| Desactivar TLS/1.0 y TLS/1.1 | Edge v84 |  |  |  
| Cookies predeterminadas en `SameSite=Lax` y `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, vaya a la [entrada Estado de la plataforma Chrome][ChromestatusFeature5088147346030592].  |  
| Directiva de referencia: Valor predeterminado en `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa.  Para obtener más información, incluida la escala de tiempo planeada por Google para este cambio, vaya a la [entrada Estado de la plataforma Chrome][ChromestatusFeature6251880185331712].  |  
| Deprecate AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa.  Para obtener más información, vaya a la [documentación de WebDev][WebDevAppCacheRemoval].  La programación de lanzamiento de Microsoft para la eliminación está planeada para una versión después de Chrome.  Solicitar un token [OriginTrial][ChromeDevelopersOrigintrialsAppCacheOriginTrial] de AppCache permite a los sitios seguir usando la API en desuso hasta edge v90.  |  
| Autenticación HTTP no permitido cuando se bloquean cookies de terceros  | Edge v87  |  | A partir de Edge v87, cuando las cookies se bloquean para solicitudes de terceros, el uso de la directiva [BlockThirdPartyCookies][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] o la alternancia de , la autenticación HTTP también no `edge://settings` está permitido. Este cambio puede afectar Enterprise de la lista de sitios del modo de acceso para el modo [Internet Explorer][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] si el extremo que hospeda la lista requiere el uso de la autenticación HTTP.  Para permitir el uso de cookies y autenticación HTTP para descargas de listas de sitios de modo Enterprise, agregue un patrón de dirección URL correspondiente a la directiva [CookiesAllowedForURLs.][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]  |
| Eliminación de Adobe Flash | Edge v88  |  | Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa.  Para obtener más información, vaya a [Adobe Flash Chromium Roadmap][ChromiumFlashRoadmapSupportRemoved].  | 
| Quitar compatibilidad con FTP | Edge v88  | Beta v87 | En Edge v88, la compatibilidad con FTP se quita por completo.  Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa.  Para obtener más información, vaya a [la Entrada de estado de la plataforma Chrome][ChromestatusFeature6246151319715840].  Las empresas que tienen sitios que aún requieren compatibilidad con FTP pueden seguir usando FTP configurando el sitio para que use [el modo IE][DeployedgeEdgeIeMode].  | 
| Autoupgrade mixed content images | Edge v88  |  | Las referencias a imágenes no seguras \(HTTP\) se actualizan automáticamente a HTTPS; si la imagen no está disponible a través de HTTPS, se produce un error en la descarga de la imagen. Hay [disponible una directiva][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] de grupo para controlar esta característica. Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa. Para obtener más información, vaya a la [entrada Estado de la plataforma Chrome][ChromestatusFeature4926989725073408].  | 
| Eliminación de 3DES en TLS  | Edge v93  |  | A partir de Edge v93, se quitará la compatibilidad TLS_RSA_WITH_3DES_EDE_CBC_SHA conjunto de cifrado. Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa. Para obtener más información, vaya a la [entrada Estado de la plataforma Chrome][ChromestatusFeature6678134168485888]. Además, en Edge v93, una directiva de compatibilidad estará disponible para admitir escenarios que necesitan conservar la compatibilidad con servidores obsoletos. Esta directiva de compatibilidad se volverá obsoleta y dejará de funcionar en Edge v95. Asegúrese de actualizar los servidores afectados antes de ese momento. |
| Restringir las solicitudes de red privada para proteger contextos  | Edge v93  |  | A partir de Edge v93, el acceso a recursos en redes locales (intranet) desde páginas en Internet requiere que esas páginas se entreguen a través de HTTPS. Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa. Para obtener más información, vaya a la [entrada Estado de la plataforma Chrome][ChromestatusFeature5436853517811712]. Hay dos directivas de compatibilidad disponibles para admitir escenarios que necesitan conservar la compatibilidad con páginas no seguras: [InsecurePrivateNetworkRequestAllowed][DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowed] e [InsecurePrivateNetworkRequestAllowedForUrls][DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowedForUrls]. |
| Semántica de plan B SDP de WebRTC en desuso | [Chrome+1](#release-comments) \(Edge v94\)  |  | Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa. Este cambio deja en desuso un dialecto del Protocolo de descripción de sesión (SDP) heredado denominado Plan B. Este formato SDP se está reemplazando por el plan unificado, que es un formato SDP compatible con especificación y compatible entre exploradores. Para obtener más información, vaya a la entrada Estado de la plataforma [Chrome][ChromestatusFeature5823036655665152] y [PSA: Timeline for Plan B SDP Deprecation and Removal - Please Migrate to Unified Plan][PSADeprecateWebRTCPlanB]. La programación de lanzamiento de Microsoft para la eliminación está planeada para una versión después de Chrome. Solicitar un token de prueba de origen inverso plan B de [WebRTC][ChromeDevelopersOrigintrialsWebRTCPlanBOriginTrial] permite a los sitios seguir usando la API en desuso hasta edge v96. |
| Bloquear descargas de contenido mixto | Edge v94  |  | La descarga de archivos desde direcciones URL HTTP se bloqueará en las páginas HTTPS. Este cambio se está produciendo en el Chromium proyecto, en el que Microsoft Edge se basa.  Para obtener más información, vaya a la entrada [del blog de seguridad de Google][GoogleBlogSecurity20200206]. |  

##### <a name="release-comments"></a>Comentarios de publicación  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      En función de los comentarios del usuario y del desarrollador, la característica indicada o el cambio incluye una versión después de Chrome.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome o Chrome+1  
   :::column-end:::
   :::column span="2":::
      En función de los comentarios del usuario y del desarrollador, la característica o cambio indicados se incluye al mismo tiempo o una versión después de Chrome.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "Acerca del modo IE | Microsoft Docs"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Configure using the Use the Enterprise Mode IE website list policy - Configure IE mode policies | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies - Microsoft Edge- Directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls - Microsoft Edge- Directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge- Directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge- Directivas | Microsoft Docs"  
[DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowed]: /deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed "InsecurePrivateNetworkRequestsAllowed - Microsoft Edge- Policies | Microsoft Docs"
[DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowedForUrls]: /deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls "InsecurePrivateNetworkRequestsAllowedForUrls - Microsoft Edge - Policies | Microsoft Docs"

[ChromestatusFeaturesSchedule]: https://www.chromestatus.com/features/schedule "Línea de tiempo de lanzamiento | Estado de la plataforma Chrome"  
[ChromestatusFeature4664843055398912]: https://chromestatus.com/feature/4664843055398912 "No permitir la sincronización XHR en el rechazo de página JavaScript | Estado de la plataforma Chrome"  
[ChromestatusFeature4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Autoupgrade Image Mixed Content | Estado de la plataforma Chrome"  
[ChromestatusFeature5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Las cookies son el valor predeterminado de SameSite=Lax | Estado de la plataforma Chrome"  
[ChromestatusFeature6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Compatibilidad con FTP en desuso | Estado de la plataforma Chrome"  
[ChromestatusFeature6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Directiva de referencia: valor predeterminado en strict-origin-when-cross-origin | Estado de la plataforma Chrome"  
[ChromestatusFeature6678134168485888]: https://chromestatus.com/feature/6678134168485888 "Quitar 3DES en tls | Estado de la plataforma Chrome"
[ChromestatusFeature5436853517811712]: https://chromestatus.com/feature/5436853517811712 "Restringir las solicitudes de red privada para subrecursos para proteger contextos | Estado de la plataforma Chrome"
[ChromestatusFeature5823036655665152]: https://www.chromestatus.com/feature/5823036655665152 "[WebRTC] Desuso y quitar plan B (en desuso) | Estado de la plataforma Chrome"
[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Compatibilidad con Flash eliminada de Chromium (destino: Chrome 88+ - ene 2021) - Mapa de ruta de Flash | Chromium Proyectos"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "AppCache OriginTrial token | Desarrolladores de Chrome"  
[ChromeDevelopersOrigintrialsWebRTCPlanBOriginTrial]: https://developer.chrome.com/origintrials/#/view_trial/3892235977954951169 "WebRTC Plan B Reverse Origin Trial Token | Desarrolladores de Chrome"

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Proteger a los usuarios de descargas inseguras en Google Chrome: blog de seguridad de Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Preparación para la eliminación de AppCache | web.dev"  

[PSADeprecateWebRTCPlanB]: https://groups.google.com/g/discuss-webrtc/c/UBtZfawdIAA/m/-UVQQcubBQAJ "PSA: escala de tiempo para la eliminación y desuso de SDP del plan B: migrar al plan unificado"

<!--todo:  cleanup links  -->  
