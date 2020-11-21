---
description: Hospedar contenido web en tus aplicaciones Win32, .NET y UWP con el control Microsoft Edge WebView2
title: Control WebView2 de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge, Windows Forms, WinForms, WPF, .NET, WinUI, Project reunion
ms.openlocfilehash: 02d17b05364f02f26a4917b65ac497156be02b2e
ms.sourcegitcommit: fab44f7e183a3c4f12bf925512fc62d84a4d6edc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "11182370"
---
# Introducción a Microsoft Edge WebView2  

El control Microsoft Edge WebView2 permite incrustar tecnologías web \ (HTML, CSS y JavaScript \) en las aplicaciones nativas.  El control WebView2 usa [Microsoft Edge (cromo)][MicrosoftedgeinsiderMain] como motor de representación para mostrar el contenido web en aplicaciones nativas.  Con WebView2, puedes incrustar código web en diferentes partes de tu aplicación nativa o compilar toda la aplicación nativa dentro de una sola vista Web.  Para obtener información sobre cómo empezar a crear una aplicación de WebView2, vaya a [Introducción](#getting-started).  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="¿Qué es la vista previa?" lightbox="./media/WebView2/whatwebview.png":::
   ¿Qué es la vista previa?  
:::image-end:::  

## Enfoque de aplicaciones híbridas  

Los programadores suelen decidir entre crear una aplicación web o una aplicación nativa.  La decisión depende del equilibrio entre el alcance y el potencial de energía.  Las aplicaciones web permiten un amplio alcance.  Como desarrollador web, puede volver a usar la mayoría, si no todo el código, en todas las plataformas.  Las aplicaciones nativas, sin embargo, usan las capacidades de toda la plataforma nativa.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Web Native" lightbox="./media/WebView2/webnative.png":::
   Web Native  
:::image-end:::  

Las aplicaciones híbridas permiten a los desarrolladores disfrutar de lo mejor de ambos mundos.  Los programadores de aplicaciones híbridas se benefician de la Ubiquity y fortaleza de la plataforma web, así como de la potencia y capacidades completas de la plataforma nativa.  

## Beneficios de WebView2  

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Motivos de la vista en vista previa" lightbox="./media/WebView2/webviewreasons.png":::
   Motivos de la vista en vista previa  
:::image-end:::  

:::row:::
   :::column span="1":::
      **Ecosistema web \ & Aptitudes**  
      Use toda la plataforma web, bibliotecas, herramientas y talento que existen en el ecosistema Web.  
   :::column-end:::
   :::column span="1":::
      **Innovación rápida**  
      El desarrollo web permite una implementación e iteración más rápidas.  
   :::column-end:::
   :::column span="1":::
      **Compatibilidad con Windows 7, 8, 10**  
      Compatibilidad con una experiencia de usuario coherente en Windows 7, 8 y 10.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Capacidades nativas**  
      Acceder al conjunto completo de API nativas.  
   :::column-end:::
   :::column span="1":::
      **Uso compartido de código**  
      Agregar código web a su código base permite un aumento de la reutilización en varias plataformas.  
   :::column-end:::
   :::column span="1":::
      **Soporte técnico de Microsoft**  
      Microsoft proporciona soporte técnico y agrega nuevas solicitudes de características cuando WebView2 se publica como GA.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **Distribución de hoja perenne**  
      Use una versión actualizada de cromo con actualizaciones de plataforma y revisiones de seguridad regulares.  
   :::column-end:::
   :::column span="1":::
      **Fijo** \ (próximamente \)  
      Elija empaquetar los bits de cromo en la aplicación.  
   :::column-end:::
   :::column span="1":::
      **Adopción incremental**  
      Agregue componentes Web por partes a la aplicación.  
   :::column-end:::
:::row-end:::  

## Introducción  

Para compilar y probar la aplicación con el control WebView2, debe tener instalado tanto [Microsoft Edge (cromo)][MicrosoftedgeinsiderDownload] como el [SDK de WebView2][NugetPackagesMicrosoftWebWebView2] .  Seleccione una de las siguientes opciones para comenzar.  

*   [Introducción a Win32 C/C++][Webview2GettingstartedWin32]  
*   [Introducción a WPF][Webview2GettingstartedWpf]  
*   [Introducción a WinForms][Webview2GettingstartedWinforms]  
*   [Introducción a WinUI3][Webview2GettingstartedWinui]  

El repositorio de [muestras de WebView2][GithubMicrosoftedgeWebview2samples] contiene ejemplos que muestran todas las características del SDK de WebView2 y los patrones de uso de API.  A medida que se agregan más características al SDK de WebView2, se actualizarán las aplicaciones de ejemplo.  

## Plataformas compatibles  

Una disponibilidad general \ (GA \) o versión preliminar está disponible en los siguientes entornos de programación.  

*   C/C++ \ (GA \) Win32
*   .NET Framework 4.6.2 o posterior
*   .NET Core 3,1 o posterior
*   .NET 5
*   [WinUI 3,0][UwpToolkitsWinui3] \ (versión preliminar \)

Puede ejecutar aplicaciones de WebView2 en las siguientes versiones de Windows.  

*   Windows 10  
*   Windows 8.1  
*   Windows 7 \ * \ *  
*   Windows Server 2019  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server2012R2  
*   Windows Server 2008 R2 \ * \ *  

> [!IMPORTANT]
> \ * \ * WebView2 soporte técnico para Windows 7 y Windows Server 2008 R2 tiene el mismo ciclo de soporte que Microsoft Edge.  Para obtener más información, vaya a [sistemas operativos compatibles con Microsoft Edge][DeployedgeMicrosoftEdgeSupportedOS].  

## Pasos siguientes  

Para obtener más información sobre cómo crear e implementar aplicaciones de WebView2, consulte la documentación conceptual y las guías de procedimientos.  

#### Conceptos  

*   [Comprender las versiones de SDK de WebView2][Webview2ConceptsVersioning]
*   [Distribución de aplicaciones con WebView2][Webview2ConceptsDistribution]  
*   [Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras][Webview2ConceptsSecurity]
*   [Carpeta administrar datos de usuario en aplicaciones de WebView2][Webview2ConceptsUserdatafolder]
 
#### Guías de How-To  

*   [Cómo depurar con WebView2][Webview2HowtoDebug]  
*   [Automatizar y probar WebView2 con el controlador Microsoft Edge][Webview2HowtoWebdriver]


## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras | Microsoft docs"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Administración de la carpeta datos de usuario | Microsoft docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprender las versiones de SDK de WebView2 | Microsoft docs"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Introducción a WebView2 | Microsoft docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Introducción a WebView2 en las aplicaciones de Windows Forms (versión preliminar) | Microsoft docs"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Introducción a WebView2 en WinUI3 (vista previa) | Microsoft docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Introducción a WebView2 en WPF (vista previa) | Microsoft docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Cómo depurar con WebView2 | Microsoft docs"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Automatizar y probar WebView2 con el controlador Microsoft Edge | Microsoft docs"  
[Webview2Releasenotes]: ./releasenotes.md "Notas de la versión para el SDK de WebView2 | Microsoft docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Biblioteca de interfaces de usuario de Windows 3 Preview 2 (2020 de julio) | Microsoft docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Sistemas operativos compatibles con Microsoft Edge | Microsoft docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Insider de Microsoft Edge"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Galería de NuGet"  
