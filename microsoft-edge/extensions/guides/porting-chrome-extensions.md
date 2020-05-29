---
ms.assetid: 1319a070-c6e3-4592-9f4b-40ce1575851f
description: Aprende a migrar tu extensión Chrome a Microsoft Edge con el kit de herramientas de Microsoft Edge Extension.
title: Portabilidad de extensiones de Chrome
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: 38bf1324c2e7e6f7754912177ce0e53d6c15a276
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573572"
---
# Migración de una extensión de Chrome a Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Migrar una extensión de Chrome a Microsoft Edge es fácil con la ayuda del kit de [herramientas de extensión de Microsoft Edge](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb). Esta herramienta de desarrollador convierte una extensión Chrome desempaquetada en una extensión de Microsoft Edge desempaquetada mediante el puente de las API y expone cualquier error en el `manifest.json` archivo.


### Puentes de API
Para permitir la migración fluida de las API de Chrome a las API de Microsoft Edge compatibles, se agregan dos scripts a la carpeta de la extensión. Estas API de puente de scripts (si es necesario), lo que significa que no tendrá que preocuparse por cambiar cualquier código específico de Chrome en el script de fondo o los scripts de contenido.

Después de la conversión, los verás incluidos en el archivo de manifiesto de la extensión con la `"-ms-preload"` clave:

```json
"-ms-preload": {
  "backgroundScript": "backgroundScriptsAPIBridge.js",
  "contentScript": "contentScriptsAPIBridge.js"
}
```

## Usar el kit de herramientas de Microsoft Edge Extension

Las instrucciones siguientes detallan cómo convertir la extensión de Chrome para que se ejecute en Microsoft Edge en la edición de actualización de aniversario de Windows 10:

1. Instalar el [Kit de herramientas de Microsoft Edge Extension](https://www.microsoft.com/store/p/microsoft-edge-extension-toolkit/9nblggh4txvb).
2. Haga una copia de la carpeta de su extensión Chrome para mantener la seguridad. El proceso de conversión sobrescribirá el código. 
3. Ejecute el kit de herramientas de Microsoft Edge extension y cargue la copia de la extensión.  
 ![botón cargar extensión](./../media/save-folder.png)
4. Corrija todos los errores que se notifican en el editor de texto de la herramienta. Seleccione "volver a validar" para comprobar si hay errores después de realizar correcciones.  
 ![Extensión-kit de herramientas buscar errores](./../media/extension-toolkit.png)
5. Seleccione "guardar archivos".

Ahora puedes salir del kit de herramientas y cargar tu extensión en Microsoft Edge. 

Puede buscar problemas de plataforma conocidos con el [EdgeHTML Issue Tracker](http://issues.microsoftedge.com). Si cree que ha encontrado algo nuevo, [abra un problema](https://developer.microsoft.com/microsoft-edge/platform/issues/new/).
