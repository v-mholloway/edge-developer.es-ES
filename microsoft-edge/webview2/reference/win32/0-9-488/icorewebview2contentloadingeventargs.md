---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: c6bb99078b5574ba89c0d66b49e2c63cd6888d28
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655354"
---
# interfaz ICoreWebView2ContentLoadingEventArgs 

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

