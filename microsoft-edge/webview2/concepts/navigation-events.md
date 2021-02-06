---
description: Navegación
title: Navegación
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/05/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones wpf, wpf, edge, ICoreWebView2, ICoreWebView2Host, control de explorador, edge html
ms.openlocfilehash: ac15b9f32a29c64bbdc2a7886fa654a2d71a5453
ms.sourcegitcommit: 4cea8cf99b5f12db9d2daba99bbf48f3ccc537fe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "11314800"
---
# Eventos de navegación  

La secuencia normal de eventos de navegación `NavigationStarting` es `SourceChanged` , , `ContentLoading` `HistoryChanged` y, a `NavigationCompleted` continuación, .  Los siguientes eventos describen el estado de WebView2 durante cada navegación.  

| Secuencia | Nombre del evento | Detalles |  
|:--- |:--- |:--- |  
| 1 | `NavigationStarting`  |  WebView2 comienza a navegar y la navegación da como resultado una solicitud de red.  El host puede no permitir la solicitud durante el evento.  |  
| 2 | `SourceChanged`  |  El origen de WebView2 cambia a una nueva dirección URL.  El evento puede ser el resultado de una navegación que no provoca una solicitud de red, como una navegación por fragmentos.  |  
| 3 | `HistoryChanged`  |  El historial de actualizaciones de WebView2 como resultado de la navegación.  |  
| 4 | `ContentLoading`  |  WebView2 comienza a cargar contenido para la nueva página.  |  
| 5 | `NavigationCompleted`  |  WebView2 completa la carga de contenido en la nueva página.  |  

Realiza `navigations` un seguimiento de cada nuevo documento con el identificador de navegación \( `NavigationId` \).  El `NavigationId` elemento WebView cambia cada vez que hay una navegación correcta a un nuevo documento.

:::image type="complex" source="../media/navigation-graph.png" alt-text="Eventos de navegación de Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   Eventos de navegación de Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> La figura anterior representa los eventos de navegación con la misma `NavigationId` propiedad en el argumento de evento respectivo.  

 `Navigations` los eventos con diferentes instancias de `NavigationId` evento pueden superponerse.  Por ejemplo, al iniciar una navegación, debe esperar al evento `NavigationStarting` relacionado.  Si, a continuación, inicia otra navegación, debería ver el evento de la primera navegación seguido del evento para la segunda navegación, seguido del evento para la primera navegación y, a continuación, todos los demás eventos de navegación adecuados para la segunda `NavigationStarting` `NavigationStarting` `NavigationCompleted` navegación.  
 
 En los casos de error puede haber o no un evento dependiendo de si la `ContentLoading` navegación continúa a una página de error.  
 
 En el caso de un redireccionamiento HTTP, hay varios eventos en una fila, donde los argumentos de eventos posteriores tienen la propiedad establecida, pero el `NavigationStarting` `IsRedirect` resto permanece `NavigationId` igual.  
 
 El mismo documento, como navegar a un fragmento, no produce el `navigations` evento y no incrementa el archivo `NavigationStarting` `NavigationId` .  

Para supervisar o cancelar dentro de subframes en webView, usa los eventos que actúan igual que los eventos equivalentes que no son `navigations` `FrameNavigationStarting` `FrameNavigationCompleted` equivalentes a fotogramas.  

<!-- links -->  
