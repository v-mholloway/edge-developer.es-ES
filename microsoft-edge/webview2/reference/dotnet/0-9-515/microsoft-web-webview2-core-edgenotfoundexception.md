---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: db4a903ca430541fa9edec9d953bf28531f7c0a4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879607"
---
# 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException (clase) 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

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

