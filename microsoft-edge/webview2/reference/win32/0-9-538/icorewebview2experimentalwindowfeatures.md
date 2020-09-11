---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: ee740f7d227ae98d451ba1c5e8f1017fe92514a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011373"
---
# 0.9.579: ICoreWebView2ExperimentalWindowFeatures 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

Características de la ventana de una ventana emergente de vista previa.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[get_Height](#get_height) | El alto de la ventana.
[get_Left](#get_left) | La posición izquierda de la ventana. Dará un error si HasPosition es falso.
[get_MenuBar](#get_menubar) | Si se muestra o no la barra de menús.
[get_ScrollBars](#get_scrollbars) | Si se muestran o no las barras de desplazamiento.
[get_Status](#get_status) | Si desea o no agregar una barra de estado.
[get_Toolbar](#get_toolbar) | Si desea que se muestre o no la barra de herramientas del explorador.
[get_Top](#get_top) | La posición superior de la ventana. Dará un error si HasPosition es falso.
[get_Width](#get_width) | Ancho de la ventana.
[HasPosition](#hasposition) | Ha especificado valores de la izquierda y de la parte superior.
[HasSize](#hassize) | Ha especificado valores de alto y ancho.

Estos campos coinciden con el ' windowFeatures ' pasado a Window. Open según lo especificado en [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)

## Miembros

#### get_Height 

El alto de la ventana.

> [get_Height](#get_height)de HRESULT público (UINT32 * height)

El valor mínimo es 100. Dará un error si HasSize es falso.

#### get_Left 

La posición izquierda de la ventana. Dará un error si HasPosition es falso.

> [get_Left](#get_left)de HRESULT público (UINT32 * Left)

#### get_MenuBar 

Si se muestra o no la barra de menús.

> [get_MenuBar](#get_menubar)de HRESULT público (bool * MenuBar)

#### get_ScrollBars 

Si se muestran o no las barras de desplazamiento.

> [get_ScrollBars](#get_scrollbars)de HRESULT público (bool * ScrollBars)

#### get_Status 

Si desea o no agregar una barra de estado.

> [get_Status](#get_status)de HRESULT público (bool * status)

#### get_Toolbar 

Si desea que se muestre o no la barra de herramientas del explorador.

> [get_Toolbar](#get_toolbar)de HRESULT público (una barra de herramientas de bool *)

#### get_Top 

La posición superior de la ventana. Dará un error si HasPosition es falso.

> [get_Top](#get_top)de HRESULT público (UINT32 * Top)

#### get_Width 

Ancho de la ventana.

> [get_Width](#get_width)de HRESULT público (UINT32 * width)

El valor mínimo es 100. Dará un error si HasSize es falso.

#### HasPosition 

Ha especificado valores de la izquierda y de la parte superior.

> [HASPOSITION](#hasposition)HRESULT público (bool * HasPosition)

#### HasSize 

Ha especificado valores de alto y ancho.

> [HASSIZE](#hassize)HRESULT público (bool * HasSize)

