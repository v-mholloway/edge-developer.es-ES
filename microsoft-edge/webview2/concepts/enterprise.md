---
description: Comprender cómo administrar las aplicaciones de WebView2
title: Administración de aplicaciones de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control del explorador, HTML Edge, Enterprise, Directiva de grupo, facilidad de administración
ms.openlocfilehash: 1eb8b9dc1637daa8d10004ab8c340fe9ae33e38b
ms.sourcegitcommit: 24151cc65bad92d751a8e7a868c102e1121456e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/22/2020
ms.locfileid: "11057868"
---
# Administración de aplicaciones de WebView2  

[WebView2][WebView2Landing] es un componente que los programadores usan para crear sus aplicaciones, y los desarrolladores pueden implementar un [tiempo de ejecución de actualización automática de WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview] en un dispositivo de usuario para potenciar sus aplicaciones.  Este documento describe cómo los administradores de TI pueden administrar las aplicaciones de WebView2 y el tiempo de ejecución.  Los comentarios de los administradores de ti y los desarrolladores son la bienvenida del [repositorio de comentarios de WebView2][GithubMicrosoftedgeWebviewfeddback].  

## Directivas de grupo para WebView2  

Los administradores de TI pueden usar objetos de directiva de grupo \ (GPO \) para establecer la configuración de la Directiva para WebView2.  El siguiente conjunto de directivas no es aplicable a WebView2,  

*   [Microsoft Edge: las directivas de actualización][EdgeUpdatePolicies] están disponibles para que los administradores de ti administren los aspectos de instalación y actualización del tiempo de ejecución de WebView2.  El explorador Microsoft Edge y WebView2 Runtime se actualizan con el mismo mecanismo de actualización.  A menos que una directiva, como `Update` , sea específica de canal, se aplica al explorador y al tiempo de ejecución WebView2.  Por ejemplo, `UpdateSuppressed` permite a los administradores de TI establecer el tiempo durante cada día para suprimir la actualización automática tanto en el explorador como en el tiempo de ejecución WebView2.  Esto permite a los administradores de ti configurar las preferencias y los proxies una vez, tanto para el explorador como para el tiempo de ejecución de WebView2, controlar el tráfico o el ancho de banda de la red o para otros fines.  Los administradores de TI pueden seguir [la guía de Microsoft Edge][ConfigureMicrosoftEdge] para configurar las directivas de Microsoft Edge.  
*   [Las directivas de explorador de Microsoft Edge][EdgeBrowserPolicies] no se aplican a las aplicaciones de WebView2.  Esto se debe a su diseño porque las aplicaciones y los exploradores tienen diferentes casos de uso y es posible que los administradores de ti no sean conscientes de las aplicaciones que usan WebView2.  Aplicar directivas del explorador en WebView2 puede tener consecuencias no deseadas.  Por ejemplo, los administradores de TI pueden bloquear JavaScript en el explorador y todas las aplicaciones de WebView2 que usen JavaScript están dañadas.  
*   \ (Próximamente \) directivas específicas de WebView2: WebView2 expondrá un pequeño conjunto adicional de directivas de grupo en aquellos casos en los que la administración de WebView2 directamente tenga sentido.  Recomendamos a los desarrolladores de aplicaciones que implementen sus propias directivas de grupo para administrar el uso de WebView2, ya que es más sencillo para los administradores de ti administrar la aplicación en lugar de WebView2 directamente.  

<!-- Links -->  

[Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview]: ./distribution.md#understanding-the-webview2-runtime "Comprender el motor de tiempo de ejecución y el instalador de WebView2 (versión preliminar): distribución de aplicaciones con WebView2 | Microsoft docs"  

[WebView2Landing]: ../index.md "Introducción a Microsoft Edge WebView2 (versión preliminar) | Microsoft docs"  

[EdgeUpdatePolicies]: /deployedge/microsoft-edge-update-policies "Microsoft Edge: directivas de actualización | Microsoft docs"  
[EdgeBrowserPolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge: directivas del explorador | Microsoft docs"  
[ConfigureMicrosoftEdge]: /deployedge/configure-microsoft-edge "Configurar las opciones de directiva de Microsoft Edge en Windows | Microsoft docs"  


[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  
