---
description: Obtenga información sobre las claves de manifiesto compatibles, así como sus problemas conocidos o incompatibilidades con Chrome.
title: 'Extensiones: claves de manifiesto compatibles'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: deeff12251d25efaed1b40c98594c616a0d9c99a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573665"
---
# Claves de manifiesto compatibles  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Cada extensión tiene un archivo de manifiesto con formato JSON, denominado manifest. JSON. Este archivo proporciona información importante para la extensión que va desde su nombre a sus permisos. A menos que se especifique en una nota a continuación, las propiedades del manifiesto de Microsoft Edge siguen la misma implementación que Chrome.

Este es un ejemplo de un [archivo de manifiesto JSON de Microsoft Edge](./supported-manifest-keys/json-manifest-example.md).

## Claves necesarias

Las teclas siguientes son obligatorias:

Key | Problemas conocidos | Incompatibilidades con Chrome
:------------ | :------------- | :--------------
[autorización](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author)  | | 
[name](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) | | |
[version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/version) | | |

## Claves recomendadas

Se recomienda usar las siguientes teclas:

Key | Problemas conocidos | Incompatibilidades con Chrome
:------------ | :------------- | :--------------
browser_specific_settings | | Indica el estado preferido de la extensión en el explorador. El explorador puede o no decidir si lo respeta en una versión futura, en función de factores como la reputación de la extensión o el número total de botones que ya están en la barra de direcciones del usuario. Puede usarse para indicar la posición predeterminada del `browserAction` icono. </br></br> `"browser_specific_settings": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;`"edge": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`"browser_action_next_to_addressbar": true`</br>&nbsp;&nbsp;&nbsp;&nbsp;`}`</br>`}` </br></br> No se admite en Chrome.|
[default_locale](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/default_locale)| | |
[description](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/description) | | |
[iconos](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/icons) | | |
[manifest_version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/manifest_version) | | Actualmente ignorado en Microsoft Edge.



## teclas browser_action o page_action

Solo puede incluir una de las siguientes teclas (o ninguna):

Key | Problemas conocidos | Incompatibilidades con Chrome
:------------ | :------------- | :--------------
[browser_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action)  | | Microsoft Edge no admite la siguiente sintaxis:  `browser_action : {"default_icon" : "icon.png" }`   <br/>Debe especificarse el tamaño de los iconos. <br/>Tamaños preferidos: 20px, 25px, 30px, 40px. <br/> Otros tamaños admitidos: 19px, 35px, 38px.|
[page_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action) | | Microsoft Edge no admite la siguiente sintaxis:  `page_action : {"default_icon" : "icon.png" }`   <br/>Debe especificarse el tamaño de los iconos. <br/>Tamaños preferidos: 20px, 25px, 30px, 40px. <br/>Otros tamaños admitidos: 19px, 35px, 38px.|

## Teclas opcionales

Las teclas siguientes son opcionales:

Key | Problemas conocidos | Incompatibilidades con Chrome
:------------ | :------------- | :--------------
[fondo](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/background) | | Persistente es un campo obligatorio para Microsoft Edge.
[content_scripts](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/content_scripts)  | | |
[content_security_policy](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_security_policy)  | La Directiva de seguridad de contenido de una página bloquea WebSockets en scripts de contenido y genera una excepción no definida. | Las extensiones de Microsoft Edge solo admiten [restricciones de directiva predeterminadas](https://developer.mozilla.org/Add-ons/WebExtensions/Content_Security_Policy#Default_content_security_policy)actualmente: `script-src 'self'; object-src 'self'` |
[incógnito](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/incognito) | | | 
key  | | |
options_page | | |
[permisos](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions)  | | |
short_name  | | |
[web_accessible_resources](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/web_accessible_resources) | | |

### Permisos admitidos
Se admiten los siguientes [permisos](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions) :


| Permiso         | Descripción                                                                                                                                                                                                                                                                         |
|:-------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \ <all_urls \ >       | Permite que el fondo y los scripts de contenido interactúen con todas las páginas web con [privilegios](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions#Host_permissions)adicionales.                                                                                  |
| contextMenus       | Proporciona acceso a la `contextMenus` API. Esto permite agregar elementos al menú contextual de Microsoft Edge.                                                                                                                                                                                     |
| cookies            | Proporciona acceso a la `cookies` API. Esto permite consultar y modificar las cookies, así como recibir una notificación cuando cambien.                                                                                                                                                           |
| geolocalización        | Permitir que la extensión use la `geolocation` API de HTML5 sin pedir permiso al usuario.                                                                                                                                                                                   |
| está               | Proporciona acceso a la `idle` API. Permite detectar cuándo cambia el estado de inactividad de la máquina.                                                                                                                                                                                    |
| almacenamiento            | Proporciona acceso a la `storage` API. Esto permite almacenar, recuperar y realizar un seguimiento de los cambios realizados en los datos de usuario.                                                                                                                                                                             |
| pestañas               | Proporciona acceso a la `tabs` API para interactuar con el sistema de pestañas del explorador. Esto permite crear, modificar y reorganizar las pestañas en el explorador, incluidas las direcciones URL asociadas a cada pestaña.                                                                                       |
| unlimitedStorage   | Permite el [almacenamiento. local](https://developer.mozilla.org/Add-ons/WebExtensions/API/storage/local) para tener almacenamiento ilimitado (según los recursos del sistema) en lugar de 5 MB. El almacenamiento máximo por pareja de valor de clave también aumenta de 5 MB a ilimitado (dependiendo de los recursos del sistema). |
| navegación en      | Proporciona acceso a la `webNavigation` API. Esto permite recibir notificaciones sobre el estado de las solicitudes de navegación.                                                                                                                                                              |
| WebRequest         | Proporciona acceso a la `webRequest` API. Esto permite observar y analizar el tráfico, así como interceptar, bloquear o modificar solicitudes en el vuelo.                                                                                                                               |
| webRequestBlocking | Necesario si una extensión usa la `webRequest` API de un modo de bloqueo.                                                                                                                                                                                                           |

'""'
