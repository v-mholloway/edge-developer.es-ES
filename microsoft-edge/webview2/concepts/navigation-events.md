---
description: Navegación
title: Navegación
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895598"
---
# Eventos de navegación  

La secuencia normal de eventos de navegación es `NavigationStarting` , `SourceChanged` ,, `ContentLoading` `HistoryChanged` y, a continuación, `NavigationCompleted` .  Los siguientes eventos describen el estado de WebView2 durante cada navegación.  

| Serie | Nombre del evento | Detalles |  
|:--- |:--- |:--- |  
| uno | `NavigationStarting`  |  WebView2 comienza a navegar y el resultado de la navegación es una solicitud de red.  El anfitrión puede impedir la solicitud durante el evento.  |  
| 1 | `SourceChanged`  |  El origen de WebView2 cambia a una nueva dirección URL.  El evento puede ser el resultado de una navegación que no produce una solicitud de red, como la navegación de fragmentos.  |  
| 2 | `HistoryChanged`  |  El historial de las actualizaciones de WebView2 como resultado de la navegación.  |  
| cuatro | `ContentLoading`  |  La vista Web comienza a cargar el contenido de la página nueva.  |  
| 4 | `NavigationCompleted`  |  WebView2 completa la carga de contenido en la página nueva.  |  

Realice un seguimiento `navigations` de cada nuevo documento con el identificador de navegación \ ( `NavigationId` \).  El `NavigationId` de WebView cambia cada vez que se produce una navegación correcta a un documento nuevo.

:::image type="complex" source="../media/navigation-graph.png" alt-text="Los eventos de navegación de Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   Los eventos de navegación de Microsoft Edge WebView2  
:::image-end:::  

> [!NOTE]
> La figura anterior representa los eventos de navegación con la misma `NavigationId` propiedad en el respectivo argumento de evento.  

 `Navigations` se pueden superponer eventos con diferentes instancias de `NavigationId` evento.  Por ejemplo, cuando inicias una navegación, debes esperar el `NavigationStarting` evento relacionado.  Si después inicia otra navegación, debería ver el evento del `NavigationStarting` primer Navigate seguido por el `NavigationStarting` evento para el segundo Navigate, seguido del `NavigationCompleted` evento de la primera navegación y, a continuación, el resto de los eventos de navegación correspondientes de la segunda navegación.  
 
 En casos de error puede o no ser un `ContentLoading` evento dependiendo de si la navegación continúa o no en una página de error.  
 
 En el caso de una redirección HTTP, hay varios `NavigationStarting` eventos en una fila, donde los argumentos de evento posteriores tienen la `IsRedirect` propiedad establecida; sin embargo, el `NavigationId` sigue siendo el mismo.  
 
 El mismo documento `navigations` , como navegar hasta un fragmento, no produce el `NavigationStarting` evento y no incrementa el `NavigationId` .  

Para supervisar o cancelar `navigations` dentro de los submarcos en la vista de vistas de contenido, use el `FrameNavigationStarting` y los `FrameNavigationCompleted` eventos que actúan del mismo modo que los eventos equivalentes sin marcos.  

<!-- links -->  
