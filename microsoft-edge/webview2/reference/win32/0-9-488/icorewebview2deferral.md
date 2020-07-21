---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: b30b6e35388ab01433b2c879db82d9c4136fae99
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885427"
---
# 0.9.515: ICoreWebView2Deferral 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

