---
description: Comprender cómo administrar aplicaciones webView2
title: Administrar aplicaciones WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral, empresa, directiva de grupo, capacidad de administración
ms.openlocfilehash: 318c2da28f9e02c0dd70619070b059e6fbc0e06a
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11893621"
---
# <a name="managing-webview2-applications"></a>Administrar aplicaciones WebView2  

[WebView2][WebView2Landing] es un componente que los desarrolladores usan para crear sus aplicaciones y los desarrolladores pueden implementar una actualización automática de Evergreen WebView2 Runtime en los dispositivos de usuario para que enciendan sus aplicaciones.  En este documento se describe cómo los administradores de TI pueden administrar las aplicaciones webView2 y el tiempo de ejecución de WebView2.  Los comentarios tanto de los administradores de TI como de los desarrolladores son bienvenidos en el repositorio de [comentarios de WebView2][GithubMicrosoftedgeWebviewfeddback].  


## <a name="group-policies-for-webview2"></a>Directivas de grupo para WebView2  

Los administradores de TI pueden usar objetos de directiva de grupo \(GPO\) para configurar la configuración de directiva para WebView2.  Las siguientes directivas son relevantes para WebView2.

*   [Microsoft Edge: las directivas de][EdgeUpdatePolicies] actualización están disponibles para que los administradores de TI administren los aspectos de instalación y actualización de WebView2 Runtime.  El Microsoft Edge y WebView2 Runtime se actualizan con el mismo mecanismo de actualización.  A menos que una directiva, como , sea específica del canal, se aplica tanto al explorador como a `Update` WebView2 Runtime.  Por ejemplo, permite a los administradores de TI establecer el tiempo durante cada día para suprimir la actualización automática tanto para el explorador como para `UpdateSuppressed` WebView2 Runtime.  Esto permite a los administradores de TI configurar preferencias y servidores proxy una vez para que el explorador y WebView2 Runtime controlen el ancho de banda o el tráfico de red o para otros fines.  Los administradores de TI [pueden seguir Microsoft Edge la guía para][ConfigureMicrosoftEdge] configurar Microsoft Edge: actualizar directivas.  

*   [Microsoft Edge: las directivas de][EdgeBrowserPolicies] explorador no se aplican a las aplicaciones webView2.  Esto se debe a que las aplicaciones y exploradores tienen distintos casos de uso y es posible que los administradores de TI no conozcan qué aplicaciones usan WebView2.  La aplicación de directivas de explorador en WebView2 tendría consecuencias no intencionadas.  Por ejemplo, los administradores de TI pueden bloquear JavaScript en el explorador y eso interrumpiría las aplicaciones webView2 que usan JavaScript.  Para evitarlo, las directivas de explorador son independientes de las directivas de WebView2.

*   [Las directivas específicas de WebView2][WebView2Policies] están disponibles para usted<!--dev, or admin?--> para administrar WebView2 directamente.  Sin embargo, se recomienda que los desarrolladores de aplicaciones de WebView2 implementen sus propias directivas de grupo para administrar el uso de WebView2, ya que es más fácil para los administradores administrar la aplicación en lugar de administrar WebView2 directamente.  


## <a name="see-also"></a>Vea también

*  [Distribuir una aplicación WebView2 y El][Webview2ConceptsDistribution] tiempo de ejecución de WebView2: acerca del tiempo de ejecución de WebView2 auto actualizando.


<!-- links -->
[Webview2ConceptsDistribution]: ./distribution.md "Distribuir una aplicación WebView2 y el motor de ejecución de WebView2 | Microsoft Docs"  
[WebView2Landing]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  
<!-- external links -->
[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge: actualizar directivas | Microsoft Docs"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge: directivas de explorador | Microsoft Docs"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Configurar Microsoft Edge de directiva en Windows | Microsoft Docs"  
[WebView2Policies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge Documentación de directivas de WebView2 | Microsoft Docs" 

[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewComentarios | GitHub"  
