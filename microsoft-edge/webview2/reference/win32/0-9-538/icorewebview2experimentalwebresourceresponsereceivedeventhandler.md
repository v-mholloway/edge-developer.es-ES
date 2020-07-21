---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
ms.openlocfilehash: 9447420abddfdb44394042d6742ed1dafd299adf
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886565"
---
# interfaz ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
  : public IUnknown
```

Se desencadena cuando se recibe una respuesta para una solicitud de un recurso Web en la vista Web.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

El anfitrión puede usar este evento para ver la solicitud y la respuesta reales de un recurso Web. Esto incluye cualquier modificación de solicitud o respuesta realizada por la pila de red (como agregar encabezados de autorización) después de que se haya desencadenado el evento WebResourceRequested para la solicitud asociada. Las modificaciones realizadas en los objetos de solicitud o respuesta se pasan por alto.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador los argumentos del evento para el evento correspondiente.

> invocación [Invoke](#invoke)pública de HRESULT ([ICoreWebView2Experimental](icorewebview2experimental.md) * Sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) * args)

