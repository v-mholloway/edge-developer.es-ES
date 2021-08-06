---
description: Actualizar al protocolo Microsoft Edge DevTools
title: Microsoft Edge Actualización del protocolo DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: d87732fddcab8d6f587a4bc667ec3a7d805ae0caa48f14d16a770a4a8d133ae6
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11798347"
---
# <a name="microsoft-edge-chromium-devtools-protocol-overview"></a>Microsoft Edge (Chromium) DevTools Protocol overview  

Con el cambio en la plataforma web subyacente de Microsoft Edge a Chromium, el protocolo [DevTools de Microsoft Edge (EdgeHTML)](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) no recibirá más actualizaciones.  El Microsoft Edge \(Chromium\) DevTools Protocol coincidirá con las API del protocolo DevTools de Chrome en el futuro.  

Puedes encontrar documentación sobre esos dominios y métodos haciendo referencia al [Visor de protocolos de Chrome DevTools](https://chromedevtools.github.io/devtools-protocol/tot).  

> [!NOTE]
> Los métodos con prefijo en el protocolo `ms` [DevTools de Microsoft Edge (EdgeHTML)](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) ya no se admiten en el protocolo DevTools de Microsoft Edge \(Chromium\).  

## <a name="using-the-devtools-protocol"></a>Uso del protocolo DevTools  

Este es el modo de adjuntar un cliente de herramientas personalizado al servidor DevTools en Microsoft Edge \(Chromium\).  

1.  Asegúrese de que todas las instancias Microsoft Edge \(Chromium\) estén cerradas.  
1.  Inicie Microsoft Edge \(Chromium\) con el puerto de depuración remota:. 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  Opcionalmente, puede iniciar una instancia independiente de Edge con un perfil de usuario distinto si lo desea.  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  A continuación, use el extremo HTTP `list` para obtener una lista de destinos de página adjuntables.  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  Por último, conéctese al destino deseado y emita comandos/suscríbete a los mensajes de evento a través del servidor de `webSocketDebuggerUrl` socket web DevTools.  

## <a name="devtools-protocol-http-endpoints"></a>Extremos HTTP del protocolo DevTools  

El Microsoft Edge \(Chromium\) DevTools Protocol admite los siguientes extremos HTTP.  

## <a name="jsonversion"></a>/json/version  

Proporciona información sobre el explorador del equipo host y qué versión del protocolo DevTools admite.  

**Parameters**  

**Ninguno**  

**Return (objeto)**  

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

## <a name="jsonprotocol"></a>/json/protocol  

Proporciona toda la superficie de API de protocolo serializada como JSON.  

**Parameters**  

**Ninguno**  

**Return (objeto)**  

Objeto JSON que representa la superficie de API disponible para la versión actual del protocolo.  

## <a name="jsonlist"></a>/json/list  

Proporciona una lista de candidatos de destinos de página para la depuración.  

**Parameters**  

**Ninguno**  

**Return (objeto)**  

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, ...  ]
```  

## <a name="jsonclose"></a>/json/close  

Cierra el proceso de destino \(por ejemplo, en Microsoft Edge \(Chromium\), cierra la pestaña de página\).  

**Parameters**  

Id. de destino  

**Return (objeto)**  

```
String(“Target is closing”)
```  

## <a name="remote-tools-for-microsoft-edge-beta"></a>Herramientas remotas para Microsoft Edge (Beta)  

Ahora puede instalar las Herramientas remotas [para Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) desde el [Microsoft Store](https://www.microsoft.com/store/apps/windows).  Esta aplicación te permite depurar de forma remota Microsoft Edge (Chromium) que se ejecuten en un Windows 10 desde el equipo de desarrollo.  

Para obtener información sobre cómo configurar el dispositivo Windows 10 y conectarse a él desde el equipo de desarrollo, vaya a Introducción con depuración [remota Windows 10 dispositivos](../devtools-guide-chromium/remote-debugging/windows.md).  

Remote [Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usa el mismo protocolo de devTools de Microsoft Edge (Chromium) que de [devTools](../devtools-guide-chromium/index.md) para comunicarse con Microsoft Edge que se ejecuta en el dispositivo Windows 10 que desea depurar.  Esta aplicación solo antepone y `/msedge/` un identificador de proceso ( ) antes de cada llamada al `pid` protocolo.  Admite los siguientes puntos de conexión HTTP.  

### <a name="msedgejsonlist"></a>/msedge/json/list  

Proporciona una lista de candidatos de todos los procesos `msedge.exe` \(incluidos [los PWA](../progressive-web-apps-chromium/index.md) y todas las pestañas en todas las instancias de Microsoft Edge\) en el dispositivo Windows 10 para la depuración.  

**Parameters**  

**Ninguno**  

**Return (objeto)**  

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
}, ...  ]
```  

### <a name="msedge"></a>/msedge/  

Funcionalmente equivalente a [/msedge/json/list](#msedgejsonlist).  

### <a name="msedgepidjsonlist"></a>/msedge/[pid]/json/list  

Proporciona una lista candidata de destinos de página para la Microsoft Edge que coincide con la proporcionada `[pid]` para la depuración.  

**Parameters**  

**Ninguno**  

**Return (objeto)**  

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
}, ...  ]
```  

### <a name="msedgepidjsonversion"></a>/msedge/[pid]/json/version  

Proporciona información sobre la Microsoft Edge que coincide con la proporcionada y qué versión del `[pid]` protocolo DevTools admite.  

**Parameters**  

**Ninguno**  

**Return (objeto)**  

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

### <a name="msedgepidjsonprotocol"></a>/msedge/[pid]/json/protocol/  

Proporciona toda la superficie de api de protocolo serializada como JSON para la Microsoft Edge que coincide con el `[pid]` proporcionado .  

**Parameters**  

**Ninguno**  

**Return (objeto)**  

Objeto JSON que representa la superficie de API disponible para la versión del protocolo que usa la instancia Microsoft Edge que coincide con la `[pid]` proporcionada.  
