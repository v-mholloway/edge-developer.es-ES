---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: b23b724977b9d164c48dc99d0da2e64d61539549
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655429"
---
# interfaz ICoreWebView2HttpResponseHeaders 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

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

> [GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * iterator)

#### GetIterator 

Obtiene un iterador sobre la colección de encabezados de respuesta completos.

> [GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * iterador)

