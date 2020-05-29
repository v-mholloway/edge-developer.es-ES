---
description: Características agregadas a Microsoft Edge DevTools en la actualización de Windows 10 de abril de 2018 (EdgeHTML de 17)
title: DevTools en EdgeHTML 17
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, edgehtml 17
ms.custom: seodec18
ms.openlocfilehash: cc110071422f858acf840c1eaf100696a6e3cf03
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573769"
---
# DevTools en la actualización de Windows 10 de abril de 2018 (EdgeHTML 17)

La EdgeHTML 17 de la DevTools se envía de dos maneras: como las herramientas integradas en el explorador ( `F12` ) para Microsoft Edge y la vista previa como una aplicación independiente de [Windows 10](#microsoft-edge-devtools-app-preview) en Microsoft Store.

Las herramientas se han actualizado con varias características principales, entre las que se incluyen compatibilidad básica para la [depuración remota](../../devtools-guide.md#remote-debugging) (a través de nuestro nuevo [Protocolo de DevTools](#devtools-protocol)), [características de depuración de PWA](#pwa-debugging), administración de la [memoria caché de IndexedDB](#indexeddb-inspection), [acoplamiento vertical](#docking-to-the-right-in-microsoft-edge) y mucho más. También hemos continuado el [esfuerzo de refactorización](./edgehtml-16.md) general de la última versión, como parte de las inversiones continuas en rendimiento y confiabilidad.

Estas son las características más recientes de Microsoft Edge DevTools que se incluían en la [actualización de Windows 10 de abril de 2018](/windows/uwp/whats-new/windows-10-build-17134) ([EdgeHTML 17](https://aka.ms/devguide_edgehtml_17)).

## Vista previa de la aplicación Microsoft Edge DevTools

![Aplicación de DevTools de Microsoft Edge](../../devtools-protocol/media/microsoft-edge-devtools.png) 

Las [**DevTools de Microsoft Edge**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) ya están disponibles para su versión preliminar como una aplicación independiente de Windows 10 en Microsoft Store. La versión de la tienda viene con un panel de *selección* para adjuntar a destinos de página locales y remotos y un diseño con fichas para facilitar el cambio entre instancias de DevTools. Además, exclusivo de la aplicación DevTools es la capacidad de depurar contenido web en aplicaciones (como complementos para Office, Cortana, EdgeHTML [WebView](../../webview.md)y [PWAs instalado en Windows](../../progressive-web-apps-edgehtml/windows-features.md)).

Las DevToolss de borde también siguen disponibles ( `F12` ) desde el explorador (sin el panel de selector).

Disociar el DevTools desde el explorador ofrece estas ventajas de experiencia de usuario y arquitectura:

- El DevTools se ejecuta en un espacio aislado de contenedor de aplicación independiente de Microsoft Edge, lo que proporciona una mayor confiabilidad para ambos.
- La aplicación facilita el cambio entre las pestañas de la instancia de DevTools activa (en lugar de tener que cambiar entre las pestañas abiertas de Microsoft Edge).
- Podemos instrumentar el motor de explorador *EdgeHTML* y abrirlo en el ecosistema de DevTools más grande con las [API entre navegadores](https://github.com/WICG/devtools-protocol/).
- Podemos enviar actualizaciones de DevTools independientemente del ciclo de lanzamiento de Windows (y EdgeHTML).

Consulte la *Guía de DevTools* para obtener más información sobre la [depuración local y remota con la aplicación de DevTools](../../devtools-guide.md).

## Protocolo DevTools

Las herramientas para desarrolladores pueden usar el [**protocolo Microsoft Edge DevTools**](../../devtools-protocol/index.md) para inspeccionar y depurar el explorador Microsoft Edge. Proporciona un conjunto de métodos y eventos organizados en diferentes [dominios](../../devtools-protocol/0.1/domains/index.md) de instrumental de motor de EdgeHTML.

 Los clientes de herramientas pueden llamar a estos métodos y controlar estos eventos a través de mensajes de socket Web de JSON intercambiados con el *servidor DevTools* hospedado por Microsoft Edge o [Windows Device portal](/windows/mixed-reality/using-the-windows-device-portal). 
 
 Microsoft Edge DevTools usa este protocolo para habilitar la [depuración remota](../../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) de una máquina host que ejecuta Microsoft Edge desde el [cliente de DevTools independiente](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) disponible en Microsoft Store. Esta compatibilidad con versión preliminar está limitada a la depuración de JS en otro dispositivo de escritorio o VM. A lo largo del tiempo, agregaremos compatibilidad para el conjunto completo de DevTools con cualquier instancia de EdgeHTML en cualquier dispositivo de Windows 10.  
 
 Las últimas compilaciones de [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual Studio 15,7 Preview 1 o posterior) usan el protocolo DevTools para habilitar el inicio y la depuración de Microsoft Edge (código JavaScript) desde el IDE de Visual Studio de cualquier proyecto de ASP.net o .net Core.

## Inspección de IndexedDB

Nuevo en el [**depurador**](../debugger.md) esta versión es un [Administrador de IndexedDB](../storage.md#indexeddb-manager) con compatibilidad para inspeccionar y actualizar los almacenes de objetos y eliminar entradas individuales de clave y valor. Más funciones en versiones futuras.

## Depuración de PWA

La compatibilidad para la depuración de aplicaciones web progresivas (PWAs) ahora está habilitada de forma predeterminada, proporcionando pestañas de herramientas para los [**trabajos de servicio**](../service-workers.md), la [**API de caché**](../storage.md#cache-manager)y la administración de [**IndexedDB**](../storage.md#indexeddb-manager) .

Además, la [barra de herramientas del panel red](../network.md#toolbar) tiene un botón nuevo, **omitir trabajo del servicio para todas las solicitudes de red**, para activar o desactivar los trabajadores del servicio registrados como proxies de red:

![Botón de la barra de herramientas red: omitir trabajo de servicio para todas las solicitudes de red](../media/network_toolbar_bypass_sw.png)

Puede depurar [PWA como una aplicación de Windows 10 instalada](../../progressive-web-apps-edgehtml/windows-features.md) si la selecciona en la lista de destinos [**locales**](../../progressive-web-apps-edgehtml/windows-features.md#debug-your-pwa-edgehtml-as-a-windows-app) (ficha explorador/PWA/WebView) en el selector de la [aplicación de DevTools independiente](../../devtools-guide.md#microsoft-store-app).  

## Acoplar a la derecha en Microsoft Edge

Ahora puede acoplar el DevTools a la derecha de la página que está depurando en Microsoft Edge, además de acoplar en la parte inferior y desacoplar la DevTools de la ventana del explorador. Usar `Ctrl+Shift+D` para alternar entre la **parte inferior**de la base de acoplamiento, la **derecha del**Dock y el **desacoplamiento** de las posiciones, o los iconos de la esquina superior derecha de la DevTools:

![Opciones de acoplamiento de DevTools (en estado desacoplado)](../media/docking_buttons.png) 
