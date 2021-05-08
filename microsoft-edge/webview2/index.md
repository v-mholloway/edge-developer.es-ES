---
description: Hospedar contenido web en las aplicaciones de Win32, .NET y UWP con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 Control
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, CoreWebView2, ICoreWebView2Host, control de explorador, edge html, Windows Forms, WinForms, WPF, .NET, WinUI, Project Reunion
ms.openlocfilehash: 9c1aa073294fc649223da19c44850dc4335f6c00
ms.sourcegitcommit: 7f7922dbb6af87ecac1378d18359125770c5b8e5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536873"
---
# <a name="introduction-to-microsoft-edge-webview2"></a>Introducción a Microsoft Edge WebView2  

El Microsoft Edge WebView2 permite insertar tecnologías web \(HTML, CSS y JavaScript\) en las aplicaciones nativas.  El control WebView2 [usa Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] como motor de representación para mostrar el contenido web en aplicaciones nativas.  Con WebView2, puedes insertar código web en diferentes partes de la aplicación nativa.  Crea toda la aplicación nativa en una sola instancia de WebView.  Para obtener información sobre cómo empezar a crear una aplicación WebView2, vaya a [Introducción](#get-started).  

:::image type="complex" source="./media/WebView2/what-webview.png" alt-text="¿Qué es WebView?" lightbox="./media/WebView2/what-webview.png":::
   ¿Qué es WebView?  
:::image-end:::    

## <a name="hybrid-app-approach"></a>Enfoque de aplicación híbrida  

A menudo, los desarrolladores deben decidir entre crear una aplicación web o una aplicación nativa.  La decisión depende del equilibrio entre el alcance y la potencia.  Las aplicaciones web permiten un amplio alcance.  Como desarrollador web, puede reutilizar la mayor parte del código en diferentes plataformas.  Para acceder a todas las funcionalidades de una plataforma nativa, usa una aplicación nativa.  

:::image type="complex" source="./media/WebView2/web-native.png" alt-text="Nativo web" lightbox="./media/WebView2/web-native.png":::
   Nativo web  
:::image-end:::    

Las aplicaciones híbridas permiten a los desarrolladores disfrutar de lo mejor de ambos mundos.  Los desarrolladores de aplicaciones híbridas se benefician de las siguientes ventajas.  

*   La ubicuidad y la fuerza de la plataforma web.  
*   La potencia y las capacidades completas de la plataforma nativa.  
    
## <a name="webview2-benefits"></a>Ventajas de WebView2   

:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-web-ecosystem-skillset-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-rapid-innovation-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-windows-7-8-10-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="web-ecosystem--skillset"></a>Conjunto de aptitudes & web  
   :::column-end:::
   :::column span="1":::
      ### <a name="rapid-innovation"></a>Innovación rápida  
   :::column-end:::
   :::column span="1":::
      ### <a name="windows-7-8-and-10-support"></a>Windows compatibilidad con 7, 8 y 10  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Use toda la plataforma web, bibliotecas, herramientas y talento que existe en el ecosistema web.  
   :::column-end:::
   :::column span="1":::
      El desarrollo web permite una implementación e iteración más rápidas.  
   :::column-end:::
   :::column span="1":::
      Compatibilidad con una experiencia de usuario coherente en Windows 7, Windows 8 y Windows 10.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-native-capabilities-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-code-sharing-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-microsoft-support-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="native-capabilities"></a>Funcionalidades nativas  
   :::column-end:::
   :::column span="1":::
      ### <a name="code-sharing"></a>Uso compartido de código  
   :::column-end:::
   :::column span="1":::
      ### <a name="microsoft-support"></a>Soporte técnico de Microsoft  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Obtenga acceso al conjunto completo de API nativas.  
   :::column-end:::
   :::column span="1":::
      Agregar código web a la base de código permite una mayor reutilización en varias plataformas.  
   :::column-end:::
   :::column span="1":::
      Microsoft proporciona soporte técnico y agrega nuevas solicitudes de características cuando WebView2 se publica en Disponibilidad general \(GA\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-evergreen-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-fixed-small.msft.png":::  
   :::column-end:::
   :::column span="1":::
      :::image type="icon" source="./media/webview-reasons-incremental-adoption-small.msft.png":::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ### <a name="evergreen-distribution"></a>Distribución de Evergreen  
   :::column-end:::
   :::column span="1":::
      ### <a name="fixed"></a>Corregido  
   :::column-end:::
   :::column span="1":::
      ### <a name="incremental-adoption"></a>Adopción incremental  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Confíe en una versión actualizada de Chromium actualizaciones de plataforma y revisiones de seguridad normales.  
   :::column-end:::
   :::column span="1":::
      \(coming soon\) Elige empaquetar los Chromium bits de la aplicación.  
   :::column-end:::
   :::column span="1":::
      Agrega componentes web pieza a pieza a la aplicación.  
   :::column-end:::
:::row-end:::  

## <a name="get-started"></a>Comenzar  

Para crear y probar la aplicación con el control WebView2, debes tener <!--both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and  -->el [SDK de WebView2][NugetPackagesMicrosoftWebWebView2] instalado.  Seleccione una de las siguientes opciones para empezar.  

*   [Introducción con Win32 C/C++][Webview2GetStartedWin32]  
*   [Introducción wpf][Webview2GetStartedWpf]  
*   [Introducción con WinForms][Webview2GetStartedWinforms]  
*   [Introducción con WinUI3][Webview2GetStartedWinui]  
    
El repositorio de ejemplos de [WebView2][GithubMicrosoftedgeWebview2samples] contiene ejemplos que muestran todas las características del SDK de WebView2 y los patrones de uso de la API.  A medida que se agregan más características al SDK de WebView2, las aplicaciones de ejemplo se actualizarán.  

## <a name="supported-platforms"></a>Plataformas compatibles  

Una versión de disponibilidad general \(GA\) o vista previa está disponible en los siguientes entornos de programación.  

*   Win32 C/C++ \(GA\)  
*   .NET Framework 4.5 o posterior  
*   .NET Core 3.1 o posterior  
*   .NET 5  
*   [WinUI 3.0][UwpToolkitsWinui3] \(Preview\)  
    
Puede ejecutar aplicaciones webView2 en las siguientes versiones de Windows.  

*   Windows 10  
*   Windows 8.1  
*   Windows 7 \*\*  
*   Windows Server 2019  
*   Windows Server 2016  
*   Windows Server 2012  
*   Windows Server 2012 R2  
*   Windows Server 2008 R2 \*\*  
    
> [!IMPORTANT]
> \*\* La compatibilidad con WebView2 para Windows 7 y Windows Server 2008 R2 tiene el mismo ciclo de compatibilidad que Microsoft Edge.  Para obtener más información, vaya [a Microsoft Edge sistemas operativos compatibles.][DeployedgeMicrosoftEdgeSupportedOS]  

## <a name="next-steps"></a>Pasos siguientes  

Para obtener más información sobre cómo crear e implementar aplicaciones webView2, revise la documentación conceptual y las guías de cómo hacerlo.  

### <a name="concepts"></a>Conceptos  

*   [Comprender las versiones del SDK de WebView2][Webview2ConceptsVersioning]  
*   [Distribución de aplicaciones con WebView2][Webview2ConceptsDistribution]  
*   [Procedimientos recomendados para desarrollar aplicaciones webview2 seguras][Webview2ConceptsSecurity]  
*   [Administrar carpeta de datos de usuario en aplicaciones webView2][Webview2ConceptsUserDataFolder]  
 
### <a name="how-to-guides"></a>How-To guías  

*   [Cómo depurar con WebView2][Webview2HowToDebug]  
*   [Automatizar y probar WebView2 con Microsoft Edge controlador][Webview2HowToWebdriver]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Procedimientos recomendados para desarrollar aplicaciones webview2 seguras | Microsoft Docs"  
[Webview2ConceptsUserDataFolder]: ./concepts/user-data-folder.md "Administrar la carpeta de datos de usuario | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Comprender las versiones del SDK de WebView2 | Microsoft Docs"  
[Webview2GetStartedWin32]: ./get-started/win32.md "Introducción a WebView2 | Microsoft Docs"  
[Webview2GetStartedWinforms]: ./get-started/winforms.md "Introducción a WebView2 en Windows forms (versión preliminar) | Microsoft Docs"  
[Webview2GetStartedWinui]: ./get-started/winui.md "Introducción a WebView2 en WinUI3 (versión preliminar) | Microsoft Docs"  
[Webview2GetStartedWpf]: ./get-started/wpf.md "Introducción a WebView2 en WPF (versión preliminar) | Microsoft Docs"  
[Webview2HowToDebug]: ./how-to/debug.md "Cómo depurar con WebView2 | Microsoft Docs"  
[Webview2HowToWebdriver]: ./how-to/webdriver.md "Automatizar y probar WebView2 con Microsoft Edge driver | Microsoft Docs"  
[Webview2ReleaseNotes]: ./release-notes.md "Notas de la versión de WebView2 SDK | Microsoft Docs"  

[UwpToolkitsWinui3]: /uwp/toolkits/winui3/index "Windows Biblioteca de interfaz de usuario 3 Versión preliminar 2 (julio de 2020) | Microsoft Docs"  

[DeployedgeMicrosoftEdgeSupportedOS]: /deployedge/microsoft-edge-supported-operating-systems "Microsoft Edge sistemas operativos compatibles | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft.Web.WebView2 | NuGet Galería"  
