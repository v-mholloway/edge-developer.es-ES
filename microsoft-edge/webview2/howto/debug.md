---
description: Más información sobre cómo depurar controles WebView2.
title: Depurar WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 7e3ee11de443713a14684023fcd90de3cb1d265a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697752"
---
# Cómo depurar al desarrollar con controles WebView2  

El objetivo del control Microsoft Edge WebView2 es combinar lo mejor de las características de desarrollo de aplicaciones nativas y Web y las herramientas de desarrollador.  En este artículo se describen las distintas herramientas que se deben usar al desarrollar con controles WebView2.  

## Microsoft Edge DevTools  

Use [las herramientas de desarrollador de Microsoft Edge (cromo)](/microsoft-edge/devtools-guide-chromium) para depurar contenido web que se muestra en controles WebView2, de la misma manera que si estuviera usando Microsoft Edge.  Para abrir la DevTools, establezca el foco en la ventana WebView y, a continuación, use cualquiera de las opciones siguientes.  
*   Seleccione `F12` .  
*   Seleccione `Ctrl` + `Shift` + `I` .  
*   Abra el menú contextual \ (haga clic con el botón derecho \) > seleccione `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!NOTE]
> Cuando depure la aplicación en Visual Studio con el depurador nativo adjunto, seleccionar `F12` puede desencadenar el depurador nativo en lugar de las herramientas de desarrollo.  Use `Ctrl` + `Shift` + `I` o use el menú contextual \ (haga clic con el botón derecho \) para evitar esta situación.  

## Visual Studio  

Use el depurador de scripts en Visual Studio 2019 versión 16,4 Preview 2 o una versión posterior para depurar el script en Visual Studio.  Compruebe que el componente **diagnóstico de JavaScript** en **desarrollo de escritorio con** la carga de trabajo de C++ está instalado.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnósticos de JavaScript de Visual Studio":::
   Diagnósticos de JavaScript de Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Para habilitar la depuración de scripts WebView2, abra el menú contextual \ (haga clic con el botón derecho \) en el proyecto > seleccione **propiedades**.  En **propiedades de configuración**, seleccione **depuración**.  En la propiedad **tipo de depuración** , elija **JavaScript (WebView2)** de la lista de opciones. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Depurador de JavaScript de Visual Studio":::
   Depurador de JavaScript de Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## Visual Studio Code  

Puede usar código de Visual Studio para depurar scripts que se ejecutan en controles WebView2.  Para obtener más información, consulte [aplicaciones de WebView de Microsoft Edge (cromo)](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).  

<!--todo:  add See also heading  -->  

## Ponerse en contacto con el equipo de la vista de WebView de Microsoft Edge  

Ayuda a crear una experiencia WebView2 más rica compartiendo tus comentarios.  Visita el [repositorio de comentarios](https://aka.ms/webviewfeedback) para enviar solicitudes de características o informes de errores.  
