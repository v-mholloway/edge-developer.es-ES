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
ms.openlocfilehash: f32488a26f3e3c926517b0e40e6aac6a309e42b8
ms.sourcegitcommit: 5ae09b1ad6cd576c9fec12538b23cd849861f2b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "11627967"
---
# <a name="managing-webview2-applications"></a>Administrar aplicaciones de WebView2  

[WebView2][WebView2Landing] es un componente que los desarrolladores usan para crear sus aplicaciones y los desarrolladores pueden implementar una actualización automática de [Evergreen WebView2 Runtime][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] en el dispositivo del usuario para que enciendan sus aplicaciones.  En este documento se describe cómo los administradores de TI pueden administrar las aplicaciones webView2 y el tiempo de ejecución.  Los comentarios tanto de los administradores de TI como de los desarrolladores son bienvenidos en el repositorio de [comentarios de WebView2][GithubMicrosoftedgeWebviewfeddback].  

## <a name="group-policies-for-webview2"></a>Directivas de grupo para WebView2  

Los administradores de TI pueden usar objetos de directiva de grupo \(GPO\) para configurar la configuración de directiva para WebView2.  El siguiente conjunto de directivas son/no son aplicables a WebView2,  

*   [Microsoft Edge: las directivas de][EdgeUpdatePolicies] actualización están disponibles para que los administradores de TI administren los aspectos de instalación y actualización de WebView2 Runtime.  El Microsoft Edge y WebView2 Runtime se actualizan con el mismo mecanismo de actualización.  A menos que una directiva, como , sea específica del canal, se aplica tanto al explorador como a `Update` WebView2 Runtime.  Por ejemplo, permite a los administradores de TI establecer el tiempo durante cada día para suprimir la actualización automática tanto para el explorador como para `UpdateSuppressed` WebView2 Runtime.  Esto permite a los administradores de TI configurar preferencias y servidores proxy una vez para que el explorador y WebView2 Runtime controlen el ancho de banda o el tráfico de red o para otros fines.  Los administradores de [TI pueden seguir Microsoft Edge la guía para][ConfigureMicrosoftEdge] configurar Microsoft Edge: actualizar directivas.  
*   [Microsoft Edge: las directivas de][EdgeBrowserPolicies] explorador no se aplican a las aplicaciones webView2.  Esto se debe a que las aplicaciones y exploradores tienen distintos casos de uso y es posible que los administradores de TI no sean conscientes de qué aplicaciones usan WebView2.  La aplicación de directivas de explorador en WebView2 puede tener consecuencias no intencionadas.  Por ejemplo, los administradores de TI pueden bloquear JavaScript en el explorador y todas las aplicaciones webView2 que usan JavaScript están rotas.  
*   [Las directivas específicas de WebView2][WebView2Policies] están disponibles para que usted administre WebView2 directamente.  Sin embargo, se recomienda a los desarrolladores implementar sus propias directivas de grupo para administrar el uso de WebView2 porque es más fácil para los administradores administrar la aplicación en lugar de administrar WebView2 directamente.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Comprender webView2 Runtime and installer (Preview): distribución de aplicaciones mediante WebView2 | Microsoft Docs"  

[WebView2Landing]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft Docs"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge: actualizar directivas | Microsoft Docs"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge: directivas de explorador | Microsoft Docs"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Configurar Microsoft Edge de directiva en Windows | Microsoft Docs"  
[WebView2Policies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge Documentación de directivas de WebView2 | Microsoft Docs" 

[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
