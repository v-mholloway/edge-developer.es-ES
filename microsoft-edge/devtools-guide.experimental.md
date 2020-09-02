---
description: Familiarizarse con las herramientas para desarrolladores de Microsoft Edge
title: Herramientas de desarrollo de Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 3aee2ab67c6e703a0a31b58b5bf985a23fcbb481
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986223"
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

Sigue enviando tus [comentarios y solicitudes de características](#getting-in-touch-with-the-microsoft-edge-devtools-team).

> [!TIP]
> **[Prueba en Microsoft Edge sin cargo desde cualquier explorador](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: nos asociamos con [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) para ofrecer pruebas gratuitas en vivo y en tiempo real en Microsoft Edge.

## Aplicación de la Microsoft Store

Los **DevTools de Microsoft Edge** [ya están disponibles para su vista previa](./devtools-guide/whats-new.md) como una [aplicación independiente de Windows 10 en Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), además de la experiencia de herramientas en el explorador ( `F12` ). Con la versión de la tienda incluye un panel *selector* que permite adjuntar a destinos de página remotos y locales abiertos, así como un diseño con fichas para facilitar el cambio entre instancias de DevTools.

### Depuración local

Para depurar una página de forma local, simplemente inicia la aplicación *Microsoft Edge DevTools* . El panel **local** de selector mostrará todos los procesos de contenido de EdgeHTML activos, incluidas las pestañas del explorador abierto, la ejecución de [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost.exe* procesos) y los controles de [WebView](./webview.md) . Haga clic en el destino deseado para adjuntar y abrir una nueva pestaña de la DevTools.

![Panel local de la aplicación DevTools](./devtools-guide/media/chooser_local.png)

### Depuración remota

La aplicación *Microsoft Edge DevTools* presenta compatibilidad básica para la depuración de páginas en un equipo remoto a través de nuestro nuevo [**Protocolo de DevTools**](./devtools-protocol/index.md). En esta versión, se obtiene acceso remoto a la funcionalidad básica del panel [**depurador**](./devtools-guide/debugger.md) , menos inspección de la memoria caché (para almacenamiento Web, trabajo de servicio, API de caché y IndexedDB). La depuración remota está limitada a los hosts de *escritorio* con *Microsoft Edge* que se ejecutan en versiones futuras.

Para empezar, consulte la sección Microsoft Edge DevTools de los documentos del [Protocolo DevTools](./devtools-protocol/index.md).

![Panel remoto de la aplicación DevTools](./devtools-guide/media/chooser_remote.png)

## Accesos directos generales

Estos métodos abreviados controlan la ventana principal de DevTools y/o funcionan en todas las herramientas.

Acción | Acceso directo
:------------ | :-------------
Mostrar u ocultar DevTools (se abre en el panel de última vista) | F12, Ctrl + Mayús + I
Activar o desactivar el acoplamiento (desacoplar/abajo/derecha) | Ctrl + Mayús + D 
Mostrar en el depurador el código fuente HTML no modificable | Ctrl + U
Mostrar u ocultar consola en la parte inferior de cualquier otra herramienta  | Ctrl +**`**
Cambiar a elementos (explorador DOM) | Ctrl + 1
Cambiar a consola |  Ctrl + 2
Cambiar a depurador | Ctrl + 3
Cambiar a red | Ctrl + 4
Cambiar a rendimiento | Ctrl + 5
Cambiar a memoria | Ctrl + 6
Cambiar a emulación | Ctrl + 7
Documento de ayuda | F1
Siguiente herramienta | Ctrl + F6
Herramienta anterior | Ctrl + Mayús + F6
Herramienta anterior (desde historial) | Ctrl + Mayús + [
Herramienta siguiente (desde historial) | Ctrl + Mayús +]
Submarco siguiente    | F6
Submarco anterior | Mayús + F6
Siguiente coincidencia en el cuadro de búsqueda | F3
Coincidencia anterior en el cuadro de búsqueda | MAYÚS + F3
Buscar en el cuadro de búsqueda | Ctrl+F
Establecer el foco en la consola en la parte inferior | Alt + Mayús + I
Acoplar/desacoplar herramientas (alternar acoplamiento) | Ctrl+P  
Iniciar DevTools en la consola | Ctrl + Mayús + J
Actualiza la página. **Nota:** si está depurando un punto de interrupción o pausado, se reanudará la ejecución en primer lugar. | Ctrl + Mayús + F5 o Ctrl + R

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./devtools-guide-chromium/includes/contact-devtools-team-note.md)]  
