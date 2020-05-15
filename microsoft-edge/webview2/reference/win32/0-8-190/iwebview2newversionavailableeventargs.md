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
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655410"
---
# interfaz IWebView2NewVersionAvailableEventArgs 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

Argumentos de evento para el evento NewVersionAvailable.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.

## Miembros

#### get_NewVersion 

Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual.

> [get_NewVersion](#get_newversion)de HRESULT público (LPWStr * NewVersion)

