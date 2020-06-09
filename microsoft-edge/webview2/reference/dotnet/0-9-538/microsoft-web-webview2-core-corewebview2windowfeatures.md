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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699452"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures 

> [!NOTE]
> Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

Características de la ventana de una ventana emergente de vista previa.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Altura](#height) | El alto de la ventana.
[Izquierda](#left) | La posición izquierda de la ventana.
[Barra](#menubar) | Si se muestra o no la barra de menús.
[Barras](#scrollbars) | Si se muestran o no las barras de desplazamiento.
[Estado](#status) | Si desea o no agregar una barra de estado.
[Barra de herramientas](#toolbar) | Si desea que se muestre o no la barra de herramientas del explorador.
[Top](#top) | La posición superior de la ventana.
[Ancho](#width) | Ancho de la ventana.
[HasPosition](#hasposition) | Ha especificado valores de la izquierda y de la parte superior.
[HasSize](#hassize) | Ha especificado valores de alto y ancho.

## Miembros

#### Altura 

El alto de la ventana.

> [alto](#height) de uint público

#### Izquierda 

La posición izquierda de la ventana.

> uint público [restante](#left)

Dará un error si HasPosition es falso.

#### Barra 

Si se muestra o no la barra de menús.

> [MenuBar](#menubar) de public int

#### Barras 

Si se muestran o no las barras de desplazamiento.

> Barras de [desplazamiento](#scrollbars) public int

#### Estado 

Si desea o no agregar una barra de estado.

> [Estado](#status) de public int

#### Barra de herramientas 

Si desea que se muestre o no la barra de herramientas del explorador.

> Barra de [herramientas](#toolbar) int pública

#### Top 

La posición superior de la ventana.

> uint público [superior](#top)

Dará un error si HasPosition es falso.

#### Ancho 

Ancho de la ventana.

> [ancho](#width) de uint público

#### HasPosition 

Ha especificado valores de la izquierda y de la parte superior.

> public int [HasPosition](#hasposition)()

#### HasSize 

Ha especificado valores de alto y ancho.

> public int [HasSize](#hassize)()

