---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 1daa6c3cdf03ce160968d43715f12ffa7eb41e84
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885586"
---
# 0.9.515: ICoreWebView2HttpResponseHeaders 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

Encabezados de respuesta HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Anexa la línea de encabezado con el nombre y el valor.
[Contains](#contains) | Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.
[GetHeader](#getheader) | Obtiene el primer valor de encabezado de la colección que coincide con el nombre.
[GetHeaders](#getheaders) | Obtiene los valores de encabezado que coinciden con el nombre.
[GetIterator](#getiterator) | Obtiene un iterador sobre la colección de encabezados de respuesta completos.

Se usa para construir un WebResourceResponse para el evento WebResourceRequested.

## Miembros

#### AppendHeader 

Anexa la línea de encabezado con el nombre y el valor.

> [APPENDHEADER](#appendheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)

#### Contains 

Comprueba si los encabezados contienen entradas que coinciden con el nombre de encabezado.

> el valor HRESULT público [contiene](#contains)(LPCWSTR, bool * Contains)

#### GetHeader 

Obtiene el primer valor de encabezado de la colección que coincide con el nombre.

> HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr * Value)

#### GetHeaders 

Obtiene los valores de encabezado que coinciden con el nombre.

> [GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * iterator)

#### GetIterator 

Obtiene un iterador sobre la colección de encabezados de respuesta completos.

> [GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * iterador)

