---
description: Comprender cómo administrar aplicaciones webView2
title: Administrar aplicaciones de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral, empresa, directiva de grupo, capacidad de administración
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057868"
---
# Administrar aplicaciones de WebView2  

[WebView2][WebView2Landing] es un componente que los desarrolladores usan para crear sus aplicaciones y los desarrolladores pueden implementar una actualización automática de [Evergreen WebView2 Runtime][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] en el dispositivo del usuario para que enciendan sus aplicaciones.  En este documento se describe cómo los administradores de TI pueden administrar las aplicaciones webView2 y el tiempo de ejecución.  Los comentarios tanto de los administradores de TI como de los desarrolladores son bienvenidos en el repositorio de [comentarios de WebView2][GithubMicrosoftedgeWebviewfeddback].  

##  <a name="group-policies-for-webview2"></a>Directivas de grupo para WebView2  

Los administradores de TI pueden usar objetos de directiva de grupo \(GPO\) para configurar la configuración de directiva para WebView2.  El siguiente conjunto de directivas son/no son aplicables a WebView2,  

*   [Microsoft Edge: las directivas de][EdgeUpdatePolicies] actualización están disponibles para que los administradores de TI administren los aspectos de instalación y actualización de WebView2 Runtime.  El Microsoft Edge y WebView2 Runtime se actualizan con el mismo mecanismo de actualización.  A menos que una directiva, como , sea específica del canal, se aplica tanto al explorador como a `Update` WebView2 Runtime.  Por ejemplo, permite a los administradores de TI establecer el tiempo durante cada día para suprimir la actualización automática tanto para el explorador como para `UpdateSuppressed` WebView2 Runtime.  Esto permite a los administradores de TI configurar preferencias y servidores proxy una vez para que el explorador y WebView2 Runtime controlen el ancho de banda o el tráfico de red o para otros fines.  Los administradores de [TI pueden seguir Microsoft Edge la guía para][ConfigureMicrosoftEdge] configurar Microsoft Edge: actualizar directivas.  
*   [Microsoft Edge: las directivas de][EdgeBrowserPolicies] explorador no se aplican a las aplicaciones webView2.  Esto se debe a que las aplicaciones y exploradores tienen distintos casos de uso y es posible que los administradores de TI no sean conscientes de qué aplicaciones usan WebView2.  La aplicación de directivas de explorador en WebView2 puede tener consecuencias no intencionadas.  Por ejemplo, los administradores de TI pueden bloquear JavaScript en el explorador y todas las aplicaciones webView2 que usan JavaScript están rotas.  
*   \(Próximamente\) Directivas específicas de WebView2: WebView2 expondrá un pequeño conjunto adicional de directivas de grupo en casos en los que la administración de WebView2 tenga sentido directamente.  Se recomienda a los desarrolladores de aplicaciones implementar sus propias directivas de grupo para administrar su uso de WebView2, ya que es más sencillo para los administradores de TI administrar la aplicación en lugar de WebView2 directamente.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Comprender webView2 Runtime and installer (Preview): distribución de aplicaciones mediante WebView2 | Microsoft Docs"  

[WebView2Landing]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge: actualizar directivas | Microsoft Docs"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge: directivas de explorador | Microsoft Docs"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Configurar Microsoft Edge de directiva en Windows | Microsoft Docs"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
