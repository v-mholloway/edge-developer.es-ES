---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 19018ff63b62b0d76bed6dcce9cf1dbce2a37b11
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699350"
---
# interfaz ICoreWebView2HttpRequestHeaders 

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
