---
description: Vea las novedades de la actualización de Microsoft Edge DevTools en la actualización de Windows 10 de octubre de 2018
title: Novedades de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, edgehtml 18
ms.custom: RS5, seodec18
ms.openlocfilehash: 604419f4c77ccaaf2dfd3179273be803cde86fc8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573775"
---
# DevTools en la actualización más reciente de Windows 10 (EdgeHTML 18)

La actualización más reciente de Microsoft Edge DevTools agrega varias ventajas a la interfaz de usuario y al Capó, incluidos nuevos paneles dedicados para el [*almacenamiento*](#storage-panel)y los [*trabajos de servicio*](#service-workers-panel) , las herramientas de [búsqueda de archivos](#source-file-search-tools) de origen en el depurador y los nuevos dominios de protocolo de [DevTools de borde](#edge-devtools-protocol-updates) para la depuración de estilo o diseño y las API de consola.

Estas son las últimas características de Microsoft Edge DevTools disponibles ahora en la [actualización de Windows 10 de octubre de 2018](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)). Además de todo esto, también hemos corregido un número de errores de accesibilidad, confiabilidad y rendimiento para mejorar los aspectos fundamentales.

## Aplicación de DevTools

Hemos actualizado la aplicación independiente [Microsoft Edge DevTools Preview](../devtools-guide.md#microsoft-store-app). La versión más reciente incluye el acceso de depuración remota a la funcionalidad básica del [**depurador**](./debugger.md), [**los elementos**](./elements.md) (para las operaciones de solo lectura) y los paneles de [**consola**](./console.md) .

## Panel de trabajo de servicios

Ahora hay un panel dedicado a los [**trabajadores de servicios**](./service-workers.md) para inspeccionar, administrar y depurar los trabajadores del servicio del sitio. Esto proporciona la misma funcionalidad que tenía anteriormente en el panel de *depuración* (ahora con una interfaz de usuario menos llena).

![Panel de trabajo de servicios](./media/service_worker.png)

## Panel almacenamiento

También hemos movido todos los inspectores de almacenamiento local (*almacenamiento local y sesion, IndexedDB, cookies, caché*) en el *depurador* a su panel de [**almacenamiento**](./storage.md) dedicado.

![Panel almacenamiento](./media/storage_cache.png)

## Herramientas de búsqueda de archivos de origen

El [**depurador**](./debugger.md) ahora tiene un panel de [búsqueda de archivos de origen](./debugger.md#file-search) . Ábralo con el comando *Buscar en archivos* ( `Ctrl` + `Shift` + `F` ) cuando tenga una cadena específica de código que está tratando de buscar en el origen. La barra de herramientas proporciona diferentes opciones de búsqueda, incluidas las expresiones regulares. 

![Búsqueda de archivos del depurador](./media/debugger_file_search.png)

También puede abrir rápidamente cualquier archivo de origen cargado con el comando *Abrir archivo* ( `Ctrl` + `P` ).

![Archivo de apertura de depuración](./media/debugger_open_file.png)

## Actualizaciones del protocolo Edge DevTools

La [versión 0,2](../devtools-protocol/0.2/index.md) del protocolo DevTools proporciona dominios nuevos para la depuración de estilo y el diseño (solo lectura) de la depuración y API de consola, además de la funcionalidad de depuración básica de scripts introducida en la [versión 0,1](../devtools-protocol/0.1/index.md). En la interfaz de usuario de Edge DevTools, esto se traduce en la funcionalidad disponible en los [**elementos**](../devtools-guide/elements.md) (para las operaciones de solo lectura), en los paneles de [**consola**](../devtools-guide/console.md) y de [**depuración**](../devtools-guide/debugger.md) .
