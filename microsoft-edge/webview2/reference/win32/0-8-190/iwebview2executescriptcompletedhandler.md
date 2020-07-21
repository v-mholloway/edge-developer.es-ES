---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 9a075cf5e5d3e5222e76b9ba7550636a67e5696a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886013"
---
# 0.8.355: IWebView2ExecuteScriptCompletedHandler 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

La persona que llama implementa esta interfaz para recibir el resultado del método ExecuteScript.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.

## Miembros

#### Invoke 

Se llama para proporcionar al implementador el estado de finalización y el resultado de la llamada de método asincrónica correspondiente.

> invocación [Invoke](#invoke)de HRESULT pública (HRESULT ERRORCODE, LPCWSTR resultObjectAsJson)

