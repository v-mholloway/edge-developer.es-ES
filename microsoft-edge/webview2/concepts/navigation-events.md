---
description: Navegación
title: Navegación | WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: d133bfb99808d0e036c4b46be9ef82039aee49eb
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535709"
---
# <a name="navigation-events"></a>Eventos de navegación  

:::row:::
   :::column span="1":::
      Plataformas compatibles:
   :::column-end:::
   :::column span="2":::
      Win32, Windows Forms, WinUi, WPF
   :::column-end:::
:::row-end:::  

Los eventos de navegación se ejecutan cuando se producen acciones asincrónicas específicas al contenido mostrado en una instancia webView2.  Por ejemplo, cuando un usuario de WebView2 navega a un nuevo sitio web, el contenido nativo escucha el evento change `NavigationStarting` using.  Cuando se completa la acción de navegación, `NavigationCompleted` se ejecuta.  Para obtener un buen ejemplo de eventos de navegación, vaya a [WebView2 Introducción guía][Webview2IndexGetStarted].  

<!--todo:  Move the relevant information out of the get started guide to better focus the content and leave the most concise elements in the get started guide.  -->   

La secuencia normal de eventos de navegación es `NavigationStarting` `SourceChanged` , , , `ContentLoading` `HistoryChanged` y, a continuación, `NavigationCompleted` .  Los siguientes eventos describen el estado de WebView2 durante cada navegación.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/navigation-graph.png" alt-text="Eventos de navegación Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
         Eventos de navegación Microsoft Edge WebView2  
      :::image-end:::  
      
      > [!NOTE]
      > La figura representa eventos de navegación con la misma `NavigationId` propiedad en el argumento de evento respectivo.  
   :::column-end:::
   :::column span="2":::
      | Secuencia | Nombre del evento | Detalles |  
      |:--- |:--- |:--- |  
      | 1 | `NavigationStarting`  |  WebView2 comienza a navegar y la navegación da como resultado una solicitud de red.  El host puede no permitir la solicitud durante el evento.  |  
      | 2 | `SourceChanged`  |  El origen de WebView2 cambia a una nueva dirección URL.  El evento puede ser el resultado de una acción de navegación que no provoca una solicitud de red, como una navegación por fragmentos.  |  
      | 3 | `ContentLoading`  |  WebView inicia la carga de contenido de la nueva página.  |  
      | 4 | `HistoryChanged`  |  La navegación hace que se actualice el historial de WebView2.  |  
      | 5 | `NavigationCompleted`  |  WebView2 completa la carga de contenido en la nueva página.  |  
   :::column-end:::
:::row-end:::

Realice un seguimiento de los eventos de navegación a cada nuevo documento mediante el identificador de navegación \( `NavigationId` event\).  El evento WebView cambia cada vez que se completa una navegación `NavigationId` correcta a un nuevo documento.  

 Los eventos de navegación con diferentes instancias de `NavigationId` evento pueden superponerse.  Por ejemplo, al iniciar un evento de navegación, debe esperar al evento `NavigationStarting` relacionado.  Si, a continuación, inicia otra navegación, debería ver el evento de la primera navegación seguido del evento de la segunda navegación, seguido del evento para la primera navegación y, a continuación, todos los demás eventos de navegación adecuados para la segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegación.  
 
 En casos de error, puede haber o no un evento en función de si la `ContentLoading` navegación continúa en una página de error.  
 
 Si se produce un redireccionamiento HTTP, hay varios eventos en una fila, donde los argumentos de evento posteriores tienen la propiedad establecida, pero el `NavigationStarting` `IsRedirect` evento permanece `NavigationId` igual.  
 
 Los mismos eventos de navegación de documentos, como navegar a un fragmento, no resultan en el evento y no `NavigationStarting` incrementan el `NavigationId` evento.  

Para supervisar o cancelar eventos de navegación dentro de subframes en una instancia WebView2, use los eventos y que actúan igual que los eventos equivalentes que no son `FrameNavigationStarting` `FrameNavigationCompleted` de fotogramas.  

## <a name="see-also"></a>Consulta también  

*   Para empezar a usar WebView2, vaya a Guías de Introducción [WebView2.][Webview2IndexGetStarted]  
*   Para obtener un ejemplo completo de las funcionalidades de WebView2, vaya a [WebView2Samples repo][GithubMicrosoftedgeWebview2samples] en GitHub.  
*   Para obtener información más detallada acerca de las API de WebView2, vaya a [Referencia de API][DotnetApiMicrosoftWebWebview2WpfWebview2].  
*   Para obtener más información acerca de WebView2, vaya a [Recursos de WebView2][Webview2IndexNextSteps].  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Getting in touch with the Microsoft Edge WebView team  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2IndexGetStarted]: ../index.md#get-started "Introducción: introducción a Microsoft Edge WebView2 | Microsoft Docs"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Pasos siguientes: Introducción a Microsoft Edge WebView2 | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Clase WebView2 | Microsoft Docs"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
