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
ms.openlocfilehash: 4b9ad48d9b09343bad04d4acbe7c49750e76427d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655433"
---
# interfaz IWebView2HttpHeadersCollectionIterator 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Iterador para una colección de encabezados HTTP.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Obtén el nombre y el valor del encabezado HTTP actual del iterador.
[MoveNext](#movenext) | Mover el iterador al siguiente encabezado HTTP de la colección.

Consulte [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) y [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).

## Miembros

#### GetCurrentHeader 

Obtén el nombre y el valor del encabezado HTTP actual del iterador.

> [GetCurrentHeader](#getcurrentheader)(valor de HRESULT) público (LPWStr * Name, LPWStr * Value)

Este método producirá un error si la última llamada a MoveNext estableció has_next en FALSE.

#### MoveNext 

Mover el iterador al siguiente encabezado HTTP de la colección.

> HRESULT público [MoveNext](#movenext)(BOOL * has_next)

El parámetro has_next se establecerá en FALSE si no hay más encabezados HTTP. Después de esto, se producirá un error en el método GetCurrentHeader, si se llama.

