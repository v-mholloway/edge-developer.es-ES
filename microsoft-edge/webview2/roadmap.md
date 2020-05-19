---
description: Más información sobre lo que viene a continuación para WebView2
title: Guía básica para la vista de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: bc55c5a731ab6cba8f9be15208029aad0ad5357a
ms.sourcegitcommit: a75e062b71831ea850c85287a8d7d7ce3b55ec84
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659747"
---
# Guía básica de WebView2 de Microsoft Edge

##### Última actualización: 2020 de mayo de

El control WebView2 permite a los programadores incrustar tecnologías web en sus aplicaciones nativas. Este documento describe la guía básica para WebView2. 

> [!NOTE]
> WebView2 está en desarrollo activo y el plan seguirá evolucionando en función de los cambios en el mercado y los comentarios de los clientes, por lo que tenga en cuenta que los planes resaltados aquí no son exhaustivos y están sujetos a cambios. 

Si tienes inquietudes o preguntas sobre la hoja de ruta, deja comentarios en el [repositorio de comentarios](https://github.com/MicrosoftEdge/WebViewFeedback).

El equipo de WebView2 tiene una serie de esfuerzos importantes:

1.  WebView2 Runtime Installer (Q4 2020)
2.  Versión fija (Q4 2020)
3.  Disponibilidad general 
    *   C/C++ Win32 (Q4 2020)
    *   .NET (Q4 2020)
    *   [WinUI 3,0](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md)

## WebView2 Runtime & Installer

WebView2 modelo de distribución de [hoja perenne](./concepts/distribution.md#microsoft-edge-webview2-runtime) le permitirá dirigir o encadenar la instalación de WebView2 Runtime en el equipo del usuario. Se espera que la versión preliminar del tiempo de ejecución y el instalador de WebView2 estén disponibles T3 2020 y GA en el cuarto trimestre de 2020.

## Versión fija

El modelo de distribución [fija](./concepts/distribution.md#roadmap) de WebView2 le permite empaquetar los archivos binarios de Microsoft Edge dentro de su aplicación nativa. En la actualidad, el trabajo de ingeniería está en camino con una vista previa anticipada para prepararse hacia el final del T3 2020 y GA Q4 2020.

## Disponibilidad general 

### C/C++ Win32

Se espera que el SDK de Win32 C/C++ se GA en el cuarto trimestre de 2020, poco después del tiempo de ejecución de WebView2 y el instalador GA.

### .NET

El SDK de .NET contiene el SDK de Win32 C/C++. Se espera que el SDK de .NET esté disponible poco después de Win32 C/C++ GA en el cuarto trimestre de 2020.

### WinUI 3,0

Puedes poner WebView2 a las aplicaciones para UWP a través de la [interfaz de usuario de 3,0](/uwp/toolkits/winui3/), actualmente en Alpha. Desproteja la [Guía básica de la biblioteca de Windows UI](https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md) para mantenerte al día.  
