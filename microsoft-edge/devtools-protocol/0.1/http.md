---
description: El protocolo Microsoft Edge DevTools versión 0,1 admite los siguientes puntos de conexión HTTP.
title: DevTools de protocolo de terminal de versión 0,1 HTTP (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a9d40772b8175790c034ee67236c4887d0831785
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882873"
---
# DevTools de protocolo de terminal de versión 0,1 HTTP (EdgeHTML)  

> [!NOTE]
> El protocolo Microsoft Edge DevTools solo funciona en la [actualización de Windows 10 de abril de 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) y versiones posteriores de [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) .

El **Protocolo DevTools 0,1** admite los siguientes puntos de conexión http. Vea [usar el protocolo](../index.md#using-the-protocol) para obtener más información sobre la conexión a un proceso de contenido del explorador y la documentación de [dominios](domains/index.md) para la API de protocolo de DevTools basada en sockets completo.

## /json/version
Proporciona información sobre el explorador del equipo host y la versión del protocolo DevTools que admite.

**Parameters**

*Ninguno*

**Objeto devuelto**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
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
