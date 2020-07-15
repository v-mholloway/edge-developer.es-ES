---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2587a3e07869076be659e29d484a647b74c2bd7f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880552"
---
# 0.9.515: ICoreWebView2HttpRequestHeaders 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

Encabezados de solicitud HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Contains](#contains) | Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.
[GetHeader](#getheader) | Obtiene el valor de encabezado que coincide con el nombre.
[GetHeaders](#getheaders) | Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.
[GetIterator](#getiterator) | Obtiene un iterador en la colección de encabezados de solicitud.
[RemoveHeader](#removeheader) | Quita el encabezado que coincide con el nombre.
[SetHeader](#setheader) | Agrega o actualiza el encabezado que coincide con el nombre.

Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting. Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.

## Miembros

#### Contains 

Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.

> el valor HRESULT público [contiene](#contains)(LPCWSTR, bool * Contains)

#### GetHeader 

Obtiene el valor de encabezado que coincide con el nombre.

> HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr * Value)

#### GetHeaders 

Obtiene el valor de encabezado que coincide con el nombre mediante un iterador.

> [GETHEADERS](#getheaders)HRESULT público (LPCWSTR Name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * iterator)

#### GetIterator 

Obtiene un iterador en la colección de encabezados de solicitud.

> [GETITERATOR](#getiterator)HRESULT ([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * iterador)

#### RemoveHeader 

Quita el encabezado que coincide con el nombre.

> [REMOVEHEADER](#removeheader)HRESULT público (LPCWSTR Name)

#### SetHeader 

Agrega o actualiza el encabezado que coincide con el nombre.

> [SETHEADER](#setheader)HRESULT público (LPCWSTR Name, LPCWSTR Value)

