---
description: Modelo de subprocesos
title: Modelo de subprocesos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: ad51afee97d3cc3e913ecdd73c4f0c2a99c70564
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895592"
---
# Modelo de subprocesos  

## Seguridad de los subprocesos  

El WebView2 debe crearse en un subproceso de interfaz de usuario.  Específicamente un hilo con un bombeo de mensajes.  Todas las devoluciones de llamada se producen en ese subproceso y las solicitudes en el WebView2 deben realizarse en ese subproceso.  No es seguro usar WebView2 desde otro subproceso.  

La única excepción es para la `Content` propiedad de `CoreWebView2WebResourceRequest` .  La `Content` propiedad Stream se lee desde un subproceso en segundo plano.  La secuencia debe ser ágil o crearse a partir de un STA de fondo para evitar el rendimiento en el subproceso de la interfaz de usuario.  

## Ingreso  

Las devoluciones de llamada, incluidos los controladores de eventos y los controladores de finalización, se ejecutan en serie.  Si tiene un controlador de eventos ejecutándose y comienza un bucle de mensajes, ningún otro controlador de eventos ni las devoluciones de llamada de finalización pueden comenzar a ejecutarse de forma reentrante.  

## Aplazamientos  

Algunos eventos WebView2 leen valores establecidos en sus argumentos de evento o realizan alguna acción después de que finalice el controlador de eventos.  Si también necesitas ejecutar una operación asincrónica como un controlador de eventos, puedes usar el `GetDeferral` método en los argumentos del evento de los eventos asociados.  El objeto de aplazamiento devuelto garantiza que el controlador de eventos no se considere completo hasta que `Complete` se solicite el método del `Deferral` .  

Por ejemplo, puedes usar el `NewWindowRequested` evento para proporcionar una `CoreWebView2` para conectarte como una ventana secundaria cuando se completa el controlador de eventos.  Pero si necesita crear de forma asincrónica el `CoreWebView2` , solicite el `GetDeferral` método en el `NewWindowRequestedEventArgs` .  Después de haber creado de forma asincrónica el `CoreWebView2` y `NewWindow` de establecer la propiedad de la `NewWindowRequestedEventArgs` , la solicitud `Complete` en el `Deferral` objeto se devolverá usando el `GetDeferral` método.  

<!-- links -->  
