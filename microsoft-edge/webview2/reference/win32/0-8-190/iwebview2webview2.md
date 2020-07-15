---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 52218ddcbecdaf3bdb736af877493c85d4460c10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878046"
---
# 0.8.355: IWebView2WebView2 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2WebView2
  : public IUnknown
```

Funcionalidad adicional implementada por el objeto WebView principal.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Detener](#stop) | Detenga todas las navegaciones y las búsquedas de recursos pendientes.

Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2WebView](IWebView2WebView.md). Para obtener más información, consulta la interfaz de [IWebView2WebView](IWebView2WebView.md) .

## Miembros

#### Detener 

Detenga todas las navegaciones y las búsquedas de recursos pendientes.

> [HRESULT público](#stop)()

