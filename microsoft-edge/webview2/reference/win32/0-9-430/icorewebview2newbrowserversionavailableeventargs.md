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
ms.openlocfilehash: 3ac37f7d90fc03214381b991c8becae602bac738
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655311"
---
# interfaz ICoreWebView2NewBrowserVersionAvailableEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NewBrowserVersionAvailable.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.

## Miembros

#### get_NewVersion 

Información de versión del explorador del [ICoreWebView2Environment](ICoreWebView2Environment.md)actual.

> [get_NewVersion](#get_newversion)de HRESULT público (LPWStr * NewVersion)

