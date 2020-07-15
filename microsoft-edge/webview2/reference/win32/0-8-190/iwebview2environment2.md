---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: d127af61bfdc9bf692fa48489d7982bf2c6cad86
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878550"
---
# 0.8.355: IWebView2Environment2 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.8.355. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface IWebView2Environment2
  : public IWebView2Environment
```

Funcionalidad adicional implementada por el objeto de entorno.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_BrowserVersionInfo](#get_browserversioninfo) | Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual, incluido el nombre del canal si no es el canal estable.

Para obtener más información, consulta la interfaz de [IWebView2Environment](IWebView2Environment.md) . Puede ejecutar QueryInterface para esta interfaz desde el objeto que implementa [IWebView2Environment](IWebView2Environment.md).

## Miembros

#### get_BrowserVersionInfo 

Información de versión del explorador del [IWebView2Environment](IWebView2Environment.md)actual, incluido el nombre del canal si no es el canal estable.

> [get_BrowserVersionInfo](#get_browserversioninfo)de HRESULT público (LPWStr * versionInfo)

Coincide con el formato de la API de GetWebView2BrowserVersionInfo. Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

