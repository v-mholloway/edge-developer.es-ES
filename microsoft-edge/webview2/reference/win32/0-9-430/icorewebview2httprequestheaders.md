---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 04a8bf376ad7649021c4ab1555c3090cce5b52fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885614"
---
# 0.9.430: ICoreWebView2HttpRequestHeaders 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

Encabezados de solicitud HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[GetHeader](#getheader) | Obtiene el valor de encabezado que coincide con el nombre.
[GetHeaders](#getheaders) | Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.
[Contains](#contains) | Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.
[SetHeader](#setheader) | Agrega o actualiza el encabezado que coincide con el nombre.
[RemoveHeader](#removeheader) | Quita el encabezado que coincide con el nombre.
[GetIterator](#getiterator) | Obtiene un iterador en la colección de encabezados de solicitud.

Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting. Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.

## Miembros

#### GetHeader 

Obtiene el valor de encabezado que coincide con el nombre.

> HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr * Value)

#### GetHeaders 

Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.

> [GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * iterator)

#### Contains 

Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.

> el valor HRESULT público [contiene](#contains)(LPCWSTR, bool * Contains)

#### SetHeader 

Agrega o actualiza el encabezado que coincide con el nombre.

> [SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)

#### RemoveHeader 

Quita el encabezado que coincide con el nombre.

> [REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)

#### GetIterator 

Obtiene un iterador en la colección de encabezados de solicitud.

> [GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * iterador)

