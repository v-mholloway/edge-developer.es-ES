---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, control de explorador, HTML Edge
ms.openlocfilehash: 4f7cf3b73e9f354d86e2595a4ed0d4bccda95285
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655234"
---
# interfaz ICoreWebView2Deferral 

> [!NOTE]
> Esta interfaz puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.430. Consulta la [referencia](../../../webview2-api-reference.md) de la API más reciente.

```
interface ICoreWebView2Deferral
  : public IUnknown
```

Esta interfaz se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[Completar](#complete) | Completa el evento diferido asociado.

## Miembros

#### Completar 

Completa el evento diferido asociado.

> HRESULT público [completado](#complete)()

Solo se debe llamar a complete una vez por cada aplazamiento tomado.

