---
description: Modelo de proceso
title: Proceso de | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: 149234fe99485460f9d0c677b176a42d3b1e5050
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11470854"
---
# <a name="process-model"></a>Modelo de proceso  

:::row:::
   :::column span="1":::
      Plataformas compatibles:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

WebView2 usa el mismo modelo de proceso que el explorador de Microsoft Edge.  Para obtener más información sobre el modelo de proceso del explorador, vaya a [Arquitectura del explorador: vea][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]el explorador web moderno.  

Un proceso de explorador está asociado con los procesos del representador y otros procesos de utilidad, como se describe en ese artículo.  Además, si se especifica WebView2, los procesos de solicitud de aplicaciones host usan WebView2.  

:::image type="complex" source="../media/process-model-1.png" alt-text="Proceso 1" lightbox="../media/process-model-1.png":::
   Proceso 1  
:::image-end:::  

Un proceso de explorador está asociado a una sola carpeta de datos de usuario.  Un proceso de solicitud puede especificar más de una carpeta de datos de usuario.  Un proceso de solicitud que especifica más de una carpeta de datos de usuario está asociado con el mismo número de procesos de explorador.  
Por ejemplo, un proceso de solicitud que solicita acceso a dos carpetas de datos de usuario usa dos procesos de explorador.  

:::image type="complex" source="../media/process-model-2.png" alt-text="Proceso 2" lightbox="../media/process-model-2.png":::
   Proceso 2  
:::image-end:::  

Un proceso de explorador está asociado a varios procesos de representador.  Una instancia de WebView 2 crea un proceso de explorador para los marcos de servicio.  Un proceso de explorador puede estar asociado a varios fotogramas.  Un proceso de explorador puede asociarse con diferentes instancias de WebView2.  El número de procesos de representación varía en función de las siguientes condiciones.  

*   Uso de la característica de aislamiento del sitio web en el explorador.  
*   Número de orígenes desconectados distintos representados en instancias asociadas de WebView2.  

La característica del explorador de aislamiento del sitio web se describe en el contenido anterior. 
<!--todo:  which previous content?  -->  
 

Representa `CoreWebView2Environment` una carpeta de datos de usuario y un proceso de explorador.  El no corresponde directamente a ningún conjunto de procesos, ya que un WebView2 usa varios procesos de representador según el aislamiento del sitio web como se describió `CoreWebView2` anteriormente.  

Para reaccionar ante bloqueos y bloqueos en los procesos del explorador y del representador, use el `ProcessFailed` evento `CoreWebView2` de .  

Para cerrar de forma segura los procesos asociados de explorador y representador, use el `Close` método `CoreWebView2Controller` de .  

Para abrir la ventana Administrador de tareas del explorador desde la **ventana DevTools** de una instancia WebView2, complete las siguientes acciones.  

*   Seleccione `Shift` + `Escape` .  
*   Mantenga el mouse en la barra de título de la ventana DevTools, abra el menú contextual \(haga clic con el botón secundario\) y elija `Browser task manager` .  

Se muestran todos los procesos asociados con el proceso de explorador de webView2, incluidos los propósitos asociados.  

## <a name="see-also"></a>Consulte también  

*   Para empezar a usar WebView2, vaya a Guías de introducción a [WebView2.][Webview2IndexGettingStarted]  
*   Para obtener un ejemplo completo de las capacidades de WebView2, vaya al repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samples] en GitHub.  
*   Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGettingStarted]: ../index.md#getting-started "Introducción: introducción a Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Arquitectura del explorador: aspecto interno del explorador web moderno (parte 1)"  
