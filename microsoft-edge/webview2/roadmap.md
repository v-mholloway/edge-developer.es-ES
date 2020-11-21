---
description: Más información sobre lo que viene a continuación para WebView2
title: Guía básica para la vista de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 99e743db0c1fb17ea46405b08e1ed074a3386068
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182363"
---
# Guía básica de WebView2 de Microsoft Edge  

##### Última actualización: 2020 de noviembre  

El control WebView2 permite a los programadores incrustar tecnologías web en sus aplicaciones nativas.  En la siguiente página se describe la guía básica para WebView2.  

> [!NOTE]
> WebView2 está en desarrollo activo y el plan continúa evolucionando en función de los cambios en el mercado y los comentarios de los clientes, por lo que tenga en cuenta que los planes resaltados aquí no son exhaustivos y están sujetos a cambios.  

Si tiene inquietudes o preguntas sobre la hoja de ruta, envíe sus comentarios en el [repositorio de comentarios][GithubMicrosoftedgeWebviewfeedbackMain].  

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
      Versión corregida  
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
      *   [WinUI 3.0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## Tiempo de ejecución y instalador de WebView2  

El [modelo de distribución de hoja perenne][ConceptDistributionEvergreenModel] le permite dirigir o encadenar la instalación del WebView2 en el equipo del usuario.  El tiempo de ejecución de WebView2 perenne y el instalador han alcanzado la disponibilidad general \ (GA \).  

## Versión fija  

El [modelo de distribución de versiones fijo][ConceptsDistributionFixedVersionModel] le permite empaquetar los archivos binarios de Microsoft Edge dentro de su aplicación nativa.  La versión corregida alcanzó la disponibilidad general \ (GA \).  

## Disponibilidad general  

### C/C++ Win32  

El SDK Win32 C/C++ ha llegado a GA.  

### .NET  

El SDK de .NET ha llegado a GA. 

### WinUI 3.0  

Puede acceder a WebView2 en sus aplicaciones para UWP usando la [interfaz de usuario de 3,0][UwpToolkitsWinui3Index], que se encuentra en Alpha.  Para obtener más información sobre cómo mantenerse al día, consulte [Guía básica de la biblioteca de Windows UI][GithubMicrosoftUiXamlRoadmap].  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribución de versiones corregidas: distribución de aplicaciones con WebView2 | Microsoft docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Biblioteca de interfaces de usuario de Windows 3,0 Preview 1 (mayo de 2020) | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Guía básica de la biblioteca de la interfaz de usuario de Windows-Microsoft/Microsoft-UI-XAML | GitHub"  
