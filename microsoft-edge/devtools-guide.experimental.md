---
description: Familiarizarse con las herramientas para desarrolladores de Microsoft Edge
title: Herramientas de desarrollo de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 47b7a3f4f523170f4dfb6f3ef674cecfdc0e157c
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645332"
---
# Herramientas de desarrollo de Microsoft Edge  

> [!NOTE]
> Los sitios web de Microsoft Edge DevTools ayudar a crear y probar sitios Web.  Si ha abierto el DevTools por error, solo tiene `F12` que presionar para cerrar.  

Microsoft Edge DevTools está integrado con [TypeScript](https://www.typescriptlang.org/), con tecnología de [código abierto](https://github.com/Microsoft/ChakraCore), optimizado para los flujos de trabajo front-end modernos y ahora disponible como una [aplicación independiente de Windows 10](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) en Microsoft Store.

Para obtener más información sobre las características más recientes, consulte [*DevTools en la actualización más reciente de Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).

## Herramientas básicas

![Microsoft Edge DevTools](./devtools-guide/media/devtools.png)

La DevTools de Microsoft Edge incluye:

 - Un panel [**elementos**](./devtools-guide/elements.md) para editar HTML y CSS, inspeccionar propiedades de accesibilidad, ver detectores de eventos y establecer puntos de interrupción de mutación Dom
 - Una [**consola**](./devtools-guide/console.md) para ver y filtrar los mensajes de registro, inspeccionar objetos de JavaScript y nodos DOM y ejecutar JavaScript en el contexto de la ventana o el marco seleccionado
 - Un [**depurador**](./devtools-guide/debugger.md) para recorrer el código, establecer relojes y puntos de interrupción, editar en vivo el código e inspeccionar el almacenamiento web y las cachés de cookies
 - Panel de [**red**](./devtools-guide/network.md) para supervisar e inspeccionar solicitudes y respuestas desde la red y la caché del explorador 
 - Un panel de [**rendimiento**](./devtools-guide/performance.md) para perfilar el tiempo y los recursos del sistema que necesita su sitio
 - Panel [**memoria**](./devtools-guide/memory.md) para medir el uso de los recursos de memoria y Comparar instantáneas de montones en diferentes Estados de ejecución de código
 - Un panel de [**emulación**](./devtools-guide/emulation.md) para probar su sitio con diferentes perfiles de explorador, resoluciones de pantalla y coordenadas de ubicación GPS

¡ Sigue enviando tus [comentarios y solicitudes de características](#feedback)!

> [!TIP]
> **[Prueba en Microsoft Edge sin cargo desde cualquier explorador](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: nos asociamos con [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) para ofrecer pruebas gratuitas en vivo y en tiempo real en Microsoft Edge.

## Aplicación de la Microsoft Store

Los **DevTools de Microsoft Edge** [ya están disponibles para su vista previa](./devtools-guide/whats-new.md) como una [aplicación independiente de Windows 10 en Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), además de la experiencia de herramientas en el explorador ( `F12` ). La versión de la tienda viene con un panel de *selección* para adjuntar a destinos de página locales y remotos y un diseño con fichas para facilitar el cambio entre instancias de DevTools.

### Depuración local

Para depurar una página de forma local, simplemente inicia la aplicación *Microsoft Edge DevTools* . El panel **local** de selector mostrará todos los procesos de contenido de Active EdgeHTML, incluidas las pestañas del explorador abierto, que ejecutan [PWAs](./progressive-web-apps-edgehtml/index.md) (procesos de*WWAHost. exe* ) y los controles de [WebView](./webview.md) . Haga clic en el destino deseado para adjuntar y abrir una nueva pestaña de la DevTools.

![Panel local de la aplicación DevTools](./devtools-guide/media/chooser_local.png)

### Depuración remota

La aplicación *Microsoft Edge DevTools* presenta compatibilidad básica para la depuración de páginas en un equipo remoto a través de nuestro nuevo [**Protocolo de DevTools**](./devtools-protocol/index.md). En esta versión, se obtiene acceso remoto a la funcionalidad básica del panel [**depurador**](./devtools-guide/debugger.md) , menos inspección de la memoria caché (para almacenamiento Web, trabajo de servicio, API de caché y IndexedDB). La depuración remota está limitada a los hosts de *escritorio* con *Microsoft Edge* que se ejecutan en versiones futuras.

Para comenzar, consulta la sección [*Microsoft Edge DevTools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) de los documentos de [Protocolo de DevTools](./devtools-protocol/index.md) .

![Panel remoto de aplicaciones de DevTools](./devtools-guide/media/chooser_remote.png)

## Comentarios

Envíanos tus comentarios para que podamos seguir mejorando el DevTools de Microsoft Edge para ti. Simplemente abre las herramientas ( `F12` ) y haz clic en el botón [**Enviar comentarios**](#microsoft-edge-developer-tools) .

También puede Agregar y votar las solicitudes de herramientas a nuestro [Foro de UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/84475-f12-developer-tools) y convertirse en [Windows Insider](https://insider.windows.com/) para obtener una vista previa de las [características más recientes que van a DevTools](./devtools-guide/whats-new.md). Use la aplicación **Hub de comentarios** de Windows para publicar, votar, realizar un seguimiento y obtener soporte técnico para sugerencias y problemas generales de Windows.

## Métodos abreviados generales

Estos métodos abreviados controlan la ventana principal de DevTools y/o funcionan en todas las herramientas.

Acción | Método abreviado
:------------ | :-------------
Mostrar u ocultar DevTools (se abre en el panel de última vista) | F12, Ctrl + Mayús + I
Activar o desactivar el acoplamiento (desacoplar/abajo/derecha) | Ctrl + Mayús + D 
Mostrar código fuente HTML no modificable en el depurador | Ctrl + U
Mostrar u ocultar consola en la parte inferior de cualquier otra herramienta  | Ctrl +**`**
Cambiar a elementos (explorador DOM) | Ctrl + 1
Cambiar a consola |  Ctrl + 2
Cambiar a depurador | Ctrl + 3
Cambiar a red | Ctrl + 4
Cambiar al rendimiento | Ctrl + 5
Cambiar a memoria | Ctrl + 6
Cambiar a la emulación | Ctrl + 7
Documento de ayuda | F1
Siguiente herramienta | Ctrl + F6
Herramienta anterior | Ctrl + Mayús + F6
Herramienta anterior (desde historial) | Ctrl + Mayús + [
Herramienta siguiente (desde historial) | Ctrl + Mayús +]
Submarco siguiente    | F6
Submarco anterior | Mayús + F6
Coincidencia siguiente en el cuadro de búsqueda | F3
Coincidencia anterior en el cuadro de búsqueda | MAYÚS + F3
Buscar en el cuadro de búsqueda | Ctrl+F
Dar el foco a la consola en la parte inferior | Alt + Mayús + I
Acoplar/desacoplar herramientas (alternar acoplamiento) | Ctrl+P  
Iniciar DevTools a la consola | Ctrl + Mayús + J
Actualiza la página. **Nota:** si está depurando un punto de interrupción o pausado, se reanudará la ejecución en primer lugar. | Ctrl + Mayús + F5 o Ctrl + R
