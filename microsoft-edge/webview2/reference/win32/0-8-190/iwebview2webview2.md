---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: 64dac6c56576b618cbdc84da2c8fcbcd0e41028f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884739"
---
# 0.8.355: IWebView2WebView2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

