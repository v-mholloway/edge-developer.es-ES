---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 23ee363fd90416d07c76644879a5f4b6cc2acabe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655389"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver 

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

Se crea un receptor para un evento de protocolo DevTools en particular y le permite suscribirse y anular la suscripción de ese evento.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived) | Suscribirse a un evento de DevToolsProtocol.

Obtenido del objeto WebView a través de GetDevToolsProtocolEventReceiver.

## Miembros

#### DevToolsProtocolEventReceived 

Suscribirse a un evento de DevToolsProtocol.

> evento público EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)

Se llamará al método Invoke del controlador siempre que se desencadene el evento DevToolsProtocol correspondiente. Se llamará a Invoke con el objeto de parámetro de un evento que contiene el objeto de parámetro del protocolo DevTools como una cadena JSON.

