---
description: Use el protocolo Microsoft Edge DevTools para inspeccionar y depurar el explorador Microsoft Edge (EdgeHTML).
title: Protocolo de DevTools de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 8bef24c98dae284f2111f6a16fca4a6f27c89dc4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573726"
---
# Protocolo Microsoft Edge (EdgeHTML) DevTools

> [!NOTE]
> El protocolo Microsoft Edge (EdgeHTML) DevTools solo funciona en [Windows 10 de abril de 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) y versiones posteriores.

Las herramientas de desarrollo pueden usar el **protocolo Microsoft Edge (EdgeHTML) DevTools** para inspeccionar y depurar el explorador Microsoft Edge (EdgeHTML). Proporciona un conjunto de métodos y eventos organizados en diferentes [dominios](0.2/domains/index.md) de instrumental de motor de EdgeHTML.

 Los clientes de herramientas pueden llamar a estos métodos y controlar estos eventos a través de mensajes de socket Web de JSON intercambiados con el *servidor DevTools* hospedado por Microsoft Edge (EdgeHTML) o Windows Device portal. Microsoft Edge (EdgeHTML) DevTools usa este protocolo para habilitar la [depuración remota](0.2/clients.md#microsoft-edge-devtools-preview) de una máquina host que ejecuta Microsoft Edge (EdgeHTML) desde el cliente independiente DevTools disponible en [Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj).

El protocolo de DevTools de Microsoft Edge (EdgeHTML) está diseñado para alinearse estrechamente con el protocolo de DevTools de Chrome (consulte la [WICG W3C para los protocolos de DevTools](https://github.com/WICG/devtools-protocol/)), aunque existen brechas de interoperabilidad conocidas en esta versión.

## Usar el protocolo

A continuación se explica cómo adjuntar un cliente de herramientas personalizado al servidor de DevTools en Microsoft Edge (EdgeHTML). Consulta las instrucciones de [depuración remota](0.2/clients.md#microsoft-edge-devtools-preview) si usas Microsoft Edge DevTools como tu cliente.

1. Inicie Microsoft Edge (EdgeHTML) con el puerto de depuración remota abierto y especifique la dirección URL que desea abrir. Por ejemplo:

    ```
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Si Edge ya se ha iniciado, el parámetro URL es opcional. Aparecerá un botón junto a la barra de direcciones del explorador para indicar que el **servidor de herramientas de desarrollo** ha comenzado:

    ![Servidor de herramientas de desarrollo](media/developer-tools-server.png) 

2. Use este [punto de conexión http](0.2/http.md) para obtener una lista de destinos de página que se puede adjuntar:

    ```
    http://localhost:9222/json/list
    ```

3. Conéctese a la lista `webSocketDebuggerUrl` de la página deseada para emitir [comandos de protocolo](0.2/domains/index.md) adicionales y recibir mensajes de eventos a través del servidor de socket DevTools.

## Estado y comentarios

La [versión 0,2](0.2/index.md) del protocolo DevTools proporciona dominios nuevos para la depuración de estilo y el diseño (solo lectura) de la depuración y API de consola, además de la funcionalidad de depuración básica de scripts introducida en la [versión 0,1](0.1/index.md). En la interfaz de usuario de Microsoft Edge DevTools, se traduce en la funcionalidad disponible en los paneles [**elementos**](../devtools-guide/elements.md), [**consola**](../devtools-guide/console.md) y [**depuración**](../devtools-guide/debugger.md) .

Gracias por probar el protocolo Edge DevTools. Nos encantaría oír tus comentarios a:

 - [**UserVoice de desarrollador de Microsoft Edge**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): DevTools ideas y solicitudes de características

 - [**Rastreador de problemas de EdgeHTML**](https://developer.microsoft.com/microsoft-edge/platform/issues/): protocolos, DevTools y problemas de la plataforma EdgeHTML

 - [**Centro de comentarios de Microsoft Edge DevTools**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): problemas de protocolo y DevTools y sugerencias a través de la aplicación centro de opiniones

## Preguntas frecuentes

#### ¿Se pueden conectar varios clientes al mismo servidor de DevTools?
No, no al mismo tiempo que los clientes están depurando. El último cliente con el que se conecta se iniciará el anterior. En el futuro, cuando se admitan herramientas adicionales, probablemente se admitan conexiones de cliente simultáneas.

#### ¿Tengo que usar 9222 como puerto de servidor de DevTools?
No. No obstante, puedes especificar cualquier puerto, pero asegúrate de elegir uno que no esté en uso. El puerto 9222 para la depuración remota se usa por Convención.

#### ¿Cómo puedo conectar mi cliente de herramientas personalizadas a Microsoft Edge (EdgeHTML) ejecutando el servidor de DevTools?
Consulta [*usar las*](#using-the-protocol) instrucciones de protocolo anteriores para adjuntar a Microsoft Edge (EdgeHTML) que se ejecuta en el equipo local. Si busca admitir la depuración remota, tendrá que crear un flujo de trabajo de usuario para instalar el certificado SSL de la máquina host en el cliente, por ejemplo, con un cuadro de diálogo de instalación como [Microsoft Edge DevTools Preview](./0.2/clients.md#microsoft-edge-devtools-preview) .

#### Si estoy depurando de forma remota con Edge DevTools, ¿tengo que iniciar el proceso del explorador del host con el modificador de línea cmd del *Puerto de servidor* ? 
No. Si está configurando la [depuración remota con Microsoft Edge DevTools Preview](./0.2/clients.md#microsoft-edge-devtools-preview), el `--devtools-server-port` modificador de la línea de comandos no es necesario para el borde inicial. En este caso, Windows *Device portal* está hospedando el servidor DevTools en nombre del explorador.

#### ¿Puedo usar el protocolo Edge DevTools para depurar de forma remota un proceso de WWAHost. exe o WebView?
El protocolo Edge DevTools actualmente solo admite las pestañas del explorador. No se admiten los procesos de WWAHost. exe y WebView.
