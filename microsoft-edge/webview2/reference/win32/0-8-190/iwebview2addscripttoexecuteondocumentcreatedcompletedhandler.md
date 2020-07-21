---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 464192c119ddb7dd59ee7cb5981f172eb44dbb78
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885019"
---
# 0.8.355: IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir el resultado del método AddScriptToExecuteOnDocumentCreated.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.

> invocación [Invoke](#invoke)de HRESULT pública (código de código HRESULT, identificador de LPCWSTR)

