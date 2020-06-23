---
description: Comprender cómo desarrollar aplicaciones de WebView2 seguras
title: Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge, seguridad
ms.openlocfilehash: e71dbe9ad98b7156d8888da074e30a96683469d5
ms.sourcegitcommit: e49b86082da884299fdd485d3311d63a7688c0d0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/22/2020
ms.locfileid: "10755405"
---
# Procedimientos recomendados para desarrollar aplicaciones de WebView2 seguras

El [control WebView2](https://docs.microsoft.com/microsoft-edge/webview2/) permite a los programadores hospedar contenido web en sus aplicaciones nativas. Cuando se usa correctamente, el contenido Web de hospedaje ofrece varias ventajas, como el uso de interfaces de usuario basadas en Web, el acceso a características de la plataforma web, el uso compartido de código entre plataformas, etc. Para evitar las vulnerabilidades que pueden surgir al hospedar contenido Web, asegúrese de diseñar su aplicación WebView2 para supervisar estrechamente las interacciones entre el contenido web y la aplicación host. 

1. Tratar todo el contenido web como no seguro
    - Valide los mensajes web y los parámetros de objeto host antes de consumirlos, ya que los mensajes web y los parámetros pueden tener un formato incorrecto (involuntariamente o malicioso) y hacer que la aplicación se comporte de manera inesperada.
    - Compruebe siempre el origen del documento que se está ejecutando dentro de WebView2 y evalúe la confiabilidad del contenido. 

2. Diseñe mensajes Web específicos y interacciones de objeto de hospedaje en lugar de usar proxies genéricos.

3. Restrinja la funcionalidad de contenido web modificando [ICoreWebView2Settings](../reference/win32/0-9-538/icorewebview2settings) (Win32) o [CoreWebView2Settings](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings) (.net) de la siguiente manera:
    - Se establece `AreHostObjectsAllowed` en `false` si no se espera que el contenido web obtenga acceso a los objetos host.
    - Se establece `IsWebMessageEnabled` en `false` si no se espera que el contenido web publique mensajes Web en la aplicación nativa. 
    - Se establece `IsScriptEnabled` en `false` si no se espera que el contenido web ejecute scripts (por ejemplo, al mostrar contenido HTML estático).
    - Se establece `AreDefaultScriptDialogsEnabled` en `false` si no se espera que el contenido web aparezca o no en los `alert` cuadros de `prompt` diálogo.

4.  Use los `NavigationStarting` `FrameNavigationStarting` eventos y para actualizar la configuración basándose en el origen de la nueva página de la siguiente manera:
    1.  Para evitar que la aplicación navegue a determinadas páginas, use estos eventos para comprobar y, a continuación, bloquear la navegación de página o marco. 
    2.  Al navegar a una página nueva, es posible que tenga que ajustar los valores de propiedad en [ICoreWebView2Settings](../reference/win32/0-9-538/icorewebview2settings) (Win32) o [CoreWebView2Settings](../reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2settings) (.net), tal como se describe anteriormente.

5. Cuando navegue a un documento nuevo, use el `ContentLoading` evento para quitar objetos de host expuestos mediante `RemoveHostObjectFromScript` . 