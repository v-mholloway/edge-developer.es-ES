---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 59e051c0537357fed89d6300db69ea479b656c7e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010519"
---
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

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

