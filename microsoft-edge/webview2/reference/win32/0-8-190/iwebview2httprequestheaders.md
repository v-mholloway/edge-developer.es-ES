---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: aea00f37f28034e1b7a33d4fd11c5ed78f779d00
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655362"
---
# interfaz IWebView2HttpRequestHeaders 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

Encabezados de solicitud HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[GetHeader](#getheader) | Obtiene el valor de encabezado que coincide con el nombre.
[Contains](#contains) | Comprueba si los encabezados contienen una entrada que coincide con el nombre de encabezado.
[SetHeader](#setheader) | Agrega o actualiza el encabezado que coincide con el nombre.
[RemoveHeader](#removeheader) | Quita el encabezado que coincide con el nombre.
[GetIterator](#getiterator) | Obtiene un iterador en la colección de encabezados de solicitud.

Se usa para inspeccionar la solicitud HTTP en el evento WebResourceRequested y el evento NavigationStarting. Ten en cuenta que puedes modificar los encabezados de la solicitud HTTP desde un evento de WebResourceRequested, pero no desde un evento de NavigationStarting.

## Miembros

#### GetHeader 

Obtiene el valor de encabezado que coincide con el nombre.

> HRESULT público [GetHeader](#getheader)(LPCWSTR Name, LPWStr * Value)

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

> [GETITERATOR](#getiterator)HRESULT ([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) * * iterador)

