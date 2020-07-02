---
description: Más información sobre lo que viene a continuación para WebView2
title: Guía básica para la vista de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 151eca3da5909b9d418451617b6bf09319752c55
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844414"
---
# Guía básica de WebView2 de Microsoft Edge  

##### Última actualización: 2020 de mayo de  

El control WebView2 permite a los programadores incrustar tecnologías web en sus aplicaciones nativas.  En la siguiente página se describe la guía básica para WebView2.  

> [!NOTE]
> WebView2 está en desarrollo activo y el plan continúa evolucionando en función de los cambios en el mercado y los comentarios de los clientes, por lo que tenga en cuenta que los planes resaltados aquí no son exhaustivos y están sujetos a cambios.  

Si tienes inquietudes o preguntas sobre la hoja de ruta, deja comentarios en el [repositorio de comentarios][GithubMicrosoftedgeWebviewfeedbackMain].  

El equipo de WebView2 está planeando los siguientes esfuerzos importantes para futuras actualizaciones.  

:::row:::
   :::column span="1":::
      Instalador de tiempo de ejecución de WebView2  
   :::column-end:::
   :::column span="2":::
      *   Cuarto trimestre de 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Versión fija  
   :::column-end:::
   :::column span="2":::
      *   Cuarto trimestre de 2020  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Disponibilidad general  
   :::column-end:::
   :::column span="2":::
      *   C/C++ \ Win32 \ (Q4 2020 \)  
      *   .NET \ (Q4 2020 \)  
      *   [WinUI 3,0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## Tiempo de ejecución y instalador de WebView2  

El [modelo de distribución de hoja perenne][ConceptDistributionEvergreenModel] le permite dirigir o encadenar la instalación del WebView2 en el equipo del usuario.  Se espera que la versión preliminar del tiempo de ejecución y el instalador de WebView2 estén disponibles T3 2020 y GA en el cuarto trimestre de 2020.  

## Versión fija  

El [modelo de distribución de versiones fijo][ConceptsDistributionFixedVersionModel] le permite empaquetar los archivos binarios de Microsoft Edge dentro de su aplicación nativa.  En la actualidad, el trabajo de ingeniería está en camino con una vista previa anticipada para prepararse hacia el final del T3 2020 y GA Q4 2020.  

## Disponibilidad general  

### C/C++ Win32  

Se espera que el SDK de Win32 C/C++ se GA en el cuarto trimestre de 2020, poco después del tiempo de ejecución de WebView2 y el instalador GA.  

### .NET  

El SDK de .NET contiene el SDK de Win32 C/C++.  Se espera que el SDK de .NET esté disponible poco después de Win32 C/C++ GA en el cuarto trimestre de 2020.  

### WinUI 3,0  

Puedes acceder a WebView2 en tus aplicaciones para UWP usando la [interfaz de usuario de 3,0][UwpToolkitsWinui3Index], actualmente en Alpha.  Para obtener más información sobre cómo mantenerse al día, consulte [Guía básica de la biblioteca de Windows UI][GithubMicrosoftUiXamlRoadmap].  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribución de versiones corregidas: distribución de aplicaciones con WebView2 | Microsoft docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Biblioteca de interfaces de usuario de Windows 3,0 Preview 1 (mayo de 2020) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Guía básica de la biblioteca de la interfaz de usuario de Windows-Microsoft/Microsoft-UI-XAML | GitHub"  
