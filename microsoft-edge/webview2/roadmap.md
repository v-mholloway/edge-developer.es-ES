---
description: Obtenga información sobre lo que viene a continuación para WebView2
title: Guía básica para Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, html perimetral
ms.openlocfilehash: 0f51b5cab32bdb9b9aa9b6baceef5fe5a17eea54
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398416"
---
# <a name="microsoft-edge-webview2-roadmap"></a>Microsoft Edge Guía básica de WebView2  

> [!NOTE]
> Last Updated: November 2020  

El control WebView2 permite a los desarrolladores insertar tecnologías web en sus aplicaciones nativas.  En la página siguiente se describe el plan de ruta posible para WebView2.  

> [!NOTE]
> WebView2 está en desarrollo activo y la hoja de ruta sigue evolucionando en función de los cambios del mercado y los comentarios de los clientes, por lo que tenga en cuenta que los planes descritos aquí no son exhaustivos y están sujetos a cambios.  

Si tiene dudas o dudas sobre la guía básica, proporcione sus comentarios en el repositorio [de comentarios][GithubMicrosoftedgeWebviewfeedbackMain].  

El equipo de WebView2 está planeando los siguientes esfuerzos principales para futuras actualizaciones.  

:::row:::
   :::column span="1":::
      Instalador de Tiempo de ejecución de WebView2  
   :::column-end:::
   :::column span="2":::
      *   P4 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Versión corregida  
   :::column-end:::
   :::column span="2":::
      *   P4 2020  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Disponibilidad general  
   :::column-end:::
   :::column span="2":::
      *   Win32 C/C++ \(Q4 2020\)  
      *   .NET \(Q4 2020\)  
      *   [WinUI 3.0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## <a name="webview2-runtime-and-installer"></a>WebView2 Runtime and Installer  

[El modelo de distribución Evergreen][ConceptDistributionEvergreenModel] permite dirigir o encadenar la instalación de WebView2 Runtime en la máquina del usuario.  El tiempo de ejecución e instalador de Evergreen WebView2 ha alcanzado la disponibilidad general \(GA\).  

## <a name="fixed-version"></a>Versión fija  

[El modelo de distribución de versiones][ConceptsDistributionFixedVersionModel] fijas permite empaquetar los archivos binarios Microsoft Edge dentro de la aplicación nativa.  La versión fija ha alcanzado la disponibilidad general \(GA\).  

## <a name="general-availability"></a>Disponibilidad general  

### <a name="win32-cc"></a>Win32 C/C++  

El SDK de C/C++ de Win32 ha llegado a GA.  

### <a name="net"></a>.NET  

El SDK de .NET ha llegado a GA. 

### <a name="winui-30"></a>WinUI 3.0  

Puedes acceder a WebView2 en tus aplicaciones para UWP con [Win UI 3.0][UwpToolkitsWinui3Index], actualmente en alfa.  Para obtener más información sobre cómo mantenerse actualizado, vaya a Windows guía básica de biblioteca de la interfaz [de usuario.][GithubMicrosoftUiXamlRoadmap]  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Modelo de distribución evergreen: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Modelo de distribución de versiones fijas: distribución de aplicaciones con WebView2 | Microsoft Docs"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Windows Biblioteca de interfaz de usuario 3.0 Versión preliminar 1 (mayo de 2020) | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "Windows Guía básica de la biblioteca de la interfaz de usuario: microsoft/microsoft-ui-xaml | GitHub"  
