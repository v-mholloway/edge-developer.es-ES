---
description: Use el protocolo DevTools de Microsoft Edge para inspeccionar y depurar el explorador DevTools de Microsoft Edge (EdgeHTML).
title: Protocolo DevTools de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: reference
ms.prod: microsoft-edge
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: bc95f6c167479e958ffd16137176418aba872a43
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439313"
---
# <a name="microsoft-edge-edgehtml-devtools-protocol"></a>Protocolo de Microsoft Edge (EdgeHTML) DevTools

> [!NOTE]
> El protocolo DevTools de Microsoft Edge (EdgeHTML) solo funciona en [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) y versiones posteriores.

Las herramientas de desarrollador pueden usar el protocolo **DevTools de Microsoft Edge (EdgeHTML)** para inspeccionar y depurar el explorador de Microsoft Edge (EdgeHTML). Proporciona un conjunto de métodos y eventos que se organizan en diferentes [dominios](0.2/domains/index.md) de instrumentación del motor EdgeHTML.

 Los clientes de herramientas pueden llamar a estos métodos y supervisar estos eventos a través de mensajes de socket web JSON intercambiados con *el servidor DevTools* hospedado por Microsoft Edge (EdgeHTML) o el Portal de dispositivos de Windows. Microsoft Edge (EdgeHTML) DevTools usa este protocolo para habilitar la depuración remota [de](0.2/clients.md#microsoft-edge-devtools-preview) una máquina host que ejecuta Microsoft Edge (EdgeHTML) desde el cliente independiente de DevTools disponible en [Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj).

El protocolo DevTools de Microsoft Edge (EdgeHTML) está diseñado para alinearse estrechamente con el protocolo DevTools de Chrome (consulte [W3C WICG for DevTools Protocols),](https://github.com/WICG/devtools-protocol/)aunque existen diferencias de interoperabilidad conocidas en esta versión.

## <a name="using-the-protocol"></a>Uso del protocolo

Este es el modo de adjuntar un cliente de herramientas personalizado al servidor DevTools en Microsoft Edge (EdgeHTML). Consulta las [instrucciones de depuración](0.2/clients.md#microsoft-edge-devtools-preview) remota si usas Microsoft Edge DevTools como cliente.

1. Inicie Microsoft Edge (EdgeHTML) con el puerto de depuración remota abierto, especificando la dirección URL que desea abrir. Por ejemplo:

    ```shell
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Si Edge ya se ha iniciado, el parámetro URL es opcional. Aparecerá un botón junto a la barra de direcciones del explorador para indicar que se ha iniciado el **servidor** de herramientas para desarrolladores:

    ![Servidor de herramientas para desarrolladores](media/developer-tools-server.png) 

2. Use este [extremo HTTP](0.2/http.md) para obtener una lista de destinos de página adjuntables:

    ```http
    http://localhost:9222/json/list
    ```

3. Conéctese a la lista de la página deseada para emitir más comandos de protocolo y recibir mensajes de eventos a través del servidor `webSocketDebuggerUrl` de socket [](0.2/domains/index.md) devtools.

## <a name="status-and-feedback"></a>Estado y comentarios

[La versión 0.2](0.2/index.md) del protocolo DevTools proporciona nuevos dominios para la depuración de estilo y diseño (solo lectura) y las API de consola, además de la funcionalidad principal de depuración de scripts introducida en la [versión 0.1.](0.1/index.md) En la interfaz de usuario de Microsoft Edge DevTools, esto se traduce en funcionalidad disponible en los paneles [**Elementos,**](../devtools-guide/elements.md) [**Consola**](../devtools-guide/console.md) [**y**](../devtools-guide/debugger.md) Depurador.

Gracias por probar el protocolo Edge DevTools. Nos encantaría escuchar sus comentarios en:

<!-- - [**Microsoft Edge Developer UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): DevTools feature ideas and requests-->  

 - [**Rastreador de problemas de EdgeHTML:**](https://developer.microsoft.com/microsoft-edge/platform/issues/)problemas y errores de protocolo, DevTools y plataforma EdgeHTML

 - [**Centro de comentarios de Microsoft Edge DevTools:**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344)problemas y sugerencias de Protocolo y DevTools a través de la aplicación Centro de opiniones

## <a name="faq"></a>Preguntas más frecuentes

#### <a name="can-multiple-clients-connect-to-the-same-devtools-server"></a>¿Se pueden conectar varios clientes al mismo servidor DevTools?
No, no simultáneamente cuando los clientes están depurando. El último cliente en conectarse arrancará el anterior. En el futuro, cuando se admitan herramientas adicionales, probablemente admitirán conexiones de cliente simultáneas.

#### <a name="do-i-have-to-use-9222-as-the-devtools-server-port"></a>¿Tengo que usar 9222 como puerto del servidor DevTools?
No. Puede especificar cualquier puerto, aunque asegúrese de elegir uno que aún no esté en uso. La convención usa el puerto 9222 para la depuración remota.

#### <a name="how-do-i-connect-my-custom-tooling-client-to-microsoft-edge-edgehtml-running-the-devtools-server"></a>¿Cómo conecto mi cliente de herramientas personalizado a Microsoft Edge (EdgeHTML) que ejecuta el servidor DevTools?
Consulte [*Uso de las instrucciones de*](#using-the-protocol) protocolo anteriores para adjuntar a Microsoft Edge (EdgeHTML) que se ejecuta en el equipo local. Si quiere admitir la depuración remota, deberá diseñar un flujo de trabajo de usuario para instalar el certificado SSL del equipo host en el cliente, por ejemplo, con un cuadro de diálogo de instalación como [usa Microsoft Edge DevTools Preview.](./0.2/clients.md#microsoft-edge-devtools-preview)

#### <a name="if-im-remote-debugging-using-edge-devtools-do-i-need-to-start-the-host-browser-process-with---devtools-server-port-cmd-line-switch"></a>Si estoy depurando remotamente con Edge DevTools, ¿necesito iniciar el proceso del explorador host con el modificador de línea *cmd --devtools-server-port?* 
No. Si está configurando la depuración remota con [Microsoft Edge DevTools Preview,](./0.2/clients.md#microsoft-edge-devtools-preview)el modificador de línea de comandos no `--devtools-server-port` es necesario para iniciar Edge. En este caso, Windows *Device Portal* hospeda el servidor DevTools en nombre del explorador.

#### <a name="can-i-use-the-edge-devtools-protocol-to-remotely-debug-a-wwahostexe-or-webview-process"></a>¿Puedo usar el protocolo Edge DevTools para depurar de forma remota un WWAHost.exe o un proceso de vista web?
Actualmente, el protocolo Edge DevTools solo admite pestañas de explorador. WWAHost.exe y los procesos de vista web no son compatibles.
