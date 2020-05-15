---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: c3ba6ac3a2478861abb7b26e726a9cbd606b0eb9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655245"
---
# interfaz ICoreWebView2ContentLoadingEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

Argumentos de evento para el evento ContentLoading.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_IsErrorPage](#get_iserrorpage) | True si el contenido cargado es una página de error.
[get_NavigationId](#get_navigationid) | IDENTIFICADOR de la navegación.

## Miembros

#### get_IsErrorPage 

True si el contenido cargado es una página de error.

> [get_IsErrorPage](#get_iserrorpage)de HRESULT público (bool * IsErrorPage)

#### get_NavigationId 

IDENTIFICADOR de la navegación.

> [get_NavigationId](#get_navigationid)de HRESULT público (UINT64 * navigation_id)

