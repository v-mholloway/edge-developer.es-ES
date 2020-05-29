---
description: El protocolo Microsoft Edge DevTools versión 0,2 admite los siguientes puntos de conexión HTTP.
title: Puntos de conexión HTTP de Microsoft Edge DevTools Protocol versión 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: cc3d0156d92ab479168e0b588ae2b7c9faa7e58f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573724"
---
# Puntos de conexión HTTP del protocolo DevTools

> [!NOTE]
> La versión 0,2 del protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de octubre de 2018]() y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

El **Protocolo DevTools 0,2** admite los siguientes puntos de conexión http. Vea [usar el protocolo](../index.md#using-the-protocol) para obtener más información sobre la conexión a un proceso de contenido del explorador y la documentación de [dominios](domains/index.md) para la API de protocolo de DevTools basada en sockets completo.

## /json/version
Proporciona información sobre el explorador del equipo host y la versión del protocolo DevTools que admite.

**Parameters**

*Ninguno*

**Objeto devuelto**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
}
```

## /json/protocol

Proporciona toda la superficie de la API de protocolo serializada como JSON.

**Parameters**

*Ninguno*

**Objeto devuelto**

Objeto JSON que representa la superficie de API disponible para la versión actual del protocolo.

## /json/list

Proporciona una lista de candidatos de los destinos de página para la depuración.

**Parameters**

*Ninguno*

**Objeto devuelto**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## /json/close

Cierra el proceso de destino (por ejemplo, en Microsoft Edge, cierra la pestaña página).

**Parameters**

IDENTIFICADOR de destino 

**Objeto devuelto**

```
String("Target is closing")
```
