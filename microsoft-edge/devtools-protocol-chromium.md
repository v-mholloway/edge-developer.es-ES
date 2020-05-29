---
description: Actualizar al protocolo Microsoft Edge DevTools
title: Actualización del protocolo Microsoft Edge DevTools
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: f1936a83f948dd17cc76139b7fd67fc73cd692d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573768"
---
# Protocolo de DevTools Microsoft Edge (cromo)

Con el turno de la plataforma web subyacente de Microsoft Edge a cromo, el [Protocolo DevTools de Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) no recibirá más actualizaciones. El protocolo de DevTools Microsoft Edge (cromo) coincidirá con las API del Protocolo de DevTools de Chrome hacia adelante. 

Puede encontrar documentación sobre esos dominios y métodos en el [visor de protocolos de Chrome DevTools](https://chromedevtools.github.io/devtools-protocol/tot/).

> [!NOTE]
> Los métodos con el prefijo `ms` en el [Protocolo DevTools de Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) ya no se admiten en el protocolo de DevTools Microsoft Edge (cromo).

## Usar el protocolo DevTools

A continuación se explica cómo adjuntar un cliente de herramientas personalizado al servidor de DevTools en Microsoft Edge (cromo).

1. Asegúrate de que todas las instancias de Microsoft Edge (cromo) estén cerradas.

2. Inicia Microsoft Edge (cromo) con el puerto de depuración remota:

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. De manera opcional, puede iniciar una instancia independiente de Edge con un perfil de usuario distinto si lo desea:

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. A continuación, use el `list` punto de conexión http para obtener una lista de destinos de página que se puede adjuntar:

    ```
    http://localhost:9222/json/list
    ```

5. Por último, conéctese a los `webSocketDebuggerUrl` comandos de destino y de salida deseados/suscribirse a los mensajes de eventos a través del servidor de socket web DevTools.

## Puntos de conexión HTTP del protocolo DevTools

El protocolo de DevTools Microsoft Edge (cromo) admite los siguientes puntos de conexión HTTP.

## /json/version
Proporciona información sobre el explorador del equipo host y la versión del protocolo DevTools que admite.

**Parameters**

*Ninguno*

**Objeto devuelto**

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
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
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, … ]
```

## /json/close

Cierra el proceso de destino (por ejemplo, en Microsoft Edge (cromo), cierra la pestaña de la página).

**Parameters**

IDENTIFICADOR de destino 

**Objeto devuelto**

```
String(“Target is closing”)
```

## Herramientas remotas para Microsoft Edge (beta)

Ahora puede instalar las [herramientas remotas de Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) desde [Microsoft Store](https://www.microsoft.com/store/apps/windows). Esta aplicación te permite depurar de forma remota Microsoft Edge (cromo) en un dispositivo con Windows 10 de tu equipo de desarrollo.

Para obtener información sobre cómo configurar su dispositivo Windows 10 y conectarse a él desde su equipo de desarrollo, consulte [este tutorial](./devtools-guide-chromium/remote-debugging/windows.md).

Las [herramientas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usan el mismo protocolo de DevTools de Microsoft Edge (cromo) que el [DevTools](./devtools-guide-chromium.md) para comunicarse con Microsoft Edge que se ejecuta en el dispositivo de Windows 10 que desea depurar. Esta aplicación simplemente antepone `/msedge/` un identificador de proceso ( `pid` ) antes de cada llamada al Protocolo. Es compatible con los siguientes puntos de conexión HTTP.

### /msedge/json/list

Proporciona una lista de candidatos de todos los `msedge.exe` procesos (incluidos [PWAs](./progressive-web-apps-chromium/index.md) y todas las pestañas de todas las instancias de Microsoft Edge) en el dispositivo Windows 10 para la depuración.

**Parameters**

*Ninguno*

**Objeto devuelto**

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, … ]
```

### /msedge/

Funcionalmente equivalente a [/msedge/JSON/List](#msedgejsonlist). 

### /msedge/[PID]/JSON/List

Proporciona una lista de candidatos de destinos de página para la instancia de Microsoft Edge que coincide con la proporcionada `[pid]` para la depuración.

**Parameters**

*Ninguno*

**Objeto devuelto**

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, … ]
```

### /msedge/[PID]/JSON/version

Proporciona información sobre la instancia de Microsoft Edge que coincide con el proporcionado `[pid]` y la versión del protocolo DevTools que admite.

**Parameters**

*Ninguno*

**Objeto devuelto**

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```

### /msedge/[PID]/JSON/Protocol/

Proporciona toda la superficie de la API de protocolo serializada como JSON para la instancia de Microsoft Edge que coincide con el proporcionado `[pid]` .

**Parameters**

*Ninguno*

**Objeto devuelto**

Objeto JSON que representa la superficie de API disponible para la versión del protocolo que usa la instancia de Microsoft Edge que coincide con el proporcionado `[pid]` .
