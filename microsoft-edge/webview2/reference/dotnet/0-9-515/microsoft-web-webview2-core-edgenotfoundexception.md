---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: fc65d857f11a77a1d3629d40266f0453acadaa7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886314"
---
# 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException (clase) 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft.Web.WebView2.Core.dll

```
class Microsoft.Web.WebView2.Core.EdgeNotFoundException
  : public Exception
```

La excepción que se produce cuando falta la instalación de un extremo.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[EdgeNotFoundException](#edgenotfoundexception) | Inicializa una nueva instancia de la clase EdgeNotFoundException.
[EdgeNotFoundException](#edgenotfoundexception) | Inicializa una nueva instancia de la clase EdgeNotFoundException con una referencia a la excepción interna que es la causa de esta excepción.
[EdgeNotFoundException](#edgenotfoundexception) | Inicializa una nueva instancia de la clase EdgeNotFoundException con el mensaje de error especificado.
[EdgeNotFoundException](#edgenotfoundexception) | Inicializa una nueva instancia de la clase EdgeNotFoundException con un mensaje de error especificado y una referencia a la excepción interna que es la causa de esta excepción.

## Miembros

#### EdgeNotFoundException 

Inicializa una nueva instancia de la clase EdgeNotFoundException.

> [EdgeNotFoundException](#edgenotfoundexception)pública ()

#### EdgeNotFoundException 

Inicializa una nueva instancia de la clase EdgeNotFoundException con una referencia a la excepción interna que es la causa de esta excepción.

> [EdgeNotFoundException](#edgenotfoundexception)pública (excepción interna)

##### Parameters
* `inner` Excepción que es la causa de la excepción actual.

#### EdgeNotFoundException 

Inicializa una nueva instancia de la clase EdgeNotFoundException con el mensaje de error especificado.

> Public [EdgeNotFoundException](#edgenotfoundexception)(mensaje de cadena)

##### Parameters
* `message` Mensaje de error que explica el motivo de la excepción.

#### EdgeNotFoundException 

Inicializa una nueva instancia de la clase EdgeNotFoundException con un mensaje de error especificado y una referencia a la excepción interna que es la causa de esta excepción.

> Public [EdgeNotFoundException](#edgenotfoundexception)(mensaje de cadena, excepción interna)

##### Parameters
* `message` Mensaje de error que explica el motivo de la excepción. 

* `inner` Excepción que es la causa de la excepción actual.

