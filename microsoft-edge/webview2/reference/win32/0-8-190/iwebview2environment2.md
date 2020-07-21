---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: e3177f159ff397ee9d4781936aa32f2715d4af02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886090"
---
# 0.8.355: IWebView2Environment2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

