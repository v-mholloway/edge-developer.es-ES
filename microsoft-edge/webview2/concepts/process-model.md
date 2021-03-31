---
description: Modelo de proceso
title: Modelo de proceso
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895593"
---
# Modelo de proceso  

WebView2 usa el mismo modelo de proceso que el explorador Microsoft Edge.  Para obtener más información sobre el modelo de proceso del explorador, vea [arquitectura del explorador en el explorador web moderno][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]. 

Un proceso del explorador está asociado con los procesos de representación y otros procesos de utilidades, tal y como se describe en este artículo.  Además, en el caso de WebView2, hay aplicaciones de hospedaje que solicitan procesos mediante WebView2.  

:::image type="complex" source="../media/process-model-1.png" alt-text="Proceso 1" lightbox="../media/process-model-1.png":::
   Proceso 1  
:::image-end:::  

Se especifica un proceso de explorador por carpeta de datos de usuario en una sesión de usuario que ofrece servicio a cualquier proceso de solicitud de WebView2 que especifique la carpeta de datos de usuario.  Esto significa que un proceso del explorador puede estar atendiendo a varios procesos de solicitud y un proceso de solicitud puede estar usando varios procesos de explorador.  

:::image type="complex" source="../media/process-model-2.png" alt-text="Proceso 2" lightbox="../media/process-model-2.png":::
   Proceso 2  
:::image-end:::  

Un proceso de explorador tiene varios procesos de representación asociados.  Los procesos del explorador se crean según sea necesario para dar servicio a varios fotogramas en diferentes instancias de WebView2.  La cantidad de procesos de representación varía según la característica de explorador de aislamiento del sitio y el número de orígenes distintos desconectados representados en instancias asociadas de WebView2.  La característica explorador de aislamiento del sitio se describe en el contenido anterior.  

`CoreWebView2Environment`Representa una carpeta de datos de usuario y el proceso del explorador.  El `CoreWebView2` no se corresponde directamente con ningún conjunto de procesos, ya que un WebView2 usa varios procesos de representación, en función del aislamiento del sitio, como se ha descrito anteriormente.  

Puede reaccionar ante los bloqueos y bloqueos en estos procesos del explorador y el representador con el `ProcessFailed` evento de `CoreWebView2` .  

Puede apagar de forma segura los procesos del explorador y el representador asociados con el `Close` método de `CoreWebView2Controller` .  

Para abrir la ventana del administrador de tareas del explorador desde la ventana **DevTools** de una instancia de WebView2, puede seleccionar `Shift` + `Escape` o mantener el mouse en la barra de título de la ventana de DevTools, abrir el menú contextual \(haga clic con el botón secundario del mouse \) y elija `Browser task manager` .  Se muestran todos los procesos asociados con el proceso del explorador de su WebView2, incluidos los propósitos relacionados.  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Arquitectura del navegador-en el explorador web moderno (parte 1)"  
