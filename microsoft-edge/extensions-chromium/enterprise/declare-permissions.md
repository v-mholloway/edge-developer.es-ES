---
description: Obtenga información sobre cómo declarar permisos para API en el manifiesto
title: Declarar permisos de API en manifiestos de extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: bc6da75baceb21bd7514cf9d6d47bbf5f1105d9d3d46acd2e0f4a536cabaa767
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11803324"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="declare-api-permissions-in-extension-manifests"></a>Declarar permisos de API en manifiestos de extensión  

Para usar la mayoría de `chrome.*` las API, la extensión debe declarar la `permissions` en el manifiesto.  Puede declarar permisos mediante una cadena de permisos de la tabla siguiente o usar un patrón para coincidir con cadenas similares.  Los permisos ayudan a restringir la extensión si se ve comprometida por malware.  Algunos permisos pueden mostrarse a los usuarios antes de la instalación de la extensión mediante advertencias de permisos.  

Si una API requiere que declare permisos en el manifiesto, revise la documentación de esa API para comprender los permisos necesarios.  Por ejemplo, la página Storage API describe cómo declarar el `storage` permiso.  

En el siguiente fragmento de código se describe cómo declarar permisos en el archivo de manifiesto.  

```json
"permissions": [
  "tabs",
  "bookmarks",
  "http://www.blogger.com/",
  "http://*.google.com/",
  "unlimitedStorage"
]
```  

En la tabla siguiente se enumeran las cadenas de permisos disponibles actualmente para usar en el manifiesto y las descripciones.  

| Cadena de permisos | Detalles |  
|:--- |:--- |  
| `activeTab` | Solicita que se concedan permisos a la extensión de acuerdo con la `activeTab` especificación. |  
| `alarms` | Proporciona a la extensión acceso a la `chrome.alarms` API. |  
| `background` | Hace Microsoft Edge inicio temprano y apagado tarde, de modo que las extensiones pueden tener una vida más larga.  Cuando cualquier extensión instalada tiene permiso, Microsoft Edge se ejecuta invisiblemente tan pronto como el usuario inicia sesión en el equipo del usuario y antes de que el usuario inicie `background` Microsoft Edge.  El permiso también hace que Microsoft Edge en ejecución, incluso después de que se cierre su última ventana, hasta que el usuario salga explícitamente `background` de Microsoft Edge.  Este permiso no afecta a las extensiones que están desactivadas en el explorador.  El `background` permiso se usa normalmente en una página en segundo plano. |  
| `bookmarks` | Proporciona a la extensión acceso a la `chrome.bookmarks` API. |  
| `browsingData` | Proporciona a la extensión acceso a la `chrome.browsingData` API. |  
| `certificateProvider` | Proporciona a la extensión acceso a la `chrome.certificateProvider` API. |  
| `clipboardRead` | Obligatorio si la extensión usa `document.execCommand('paste')` . |  
| `clipboardWrite` | Indica que la extensión usa `document.execCommand('copy')` o `document.execCommand('cut')` . |  
| `contentSettings` | Proporciona a la extensión acceso a la `chrome.contentSettings` API. |  
| `contextMenus` | Proporciona a la extensión acceso a la `chrome.contextMenus` API. |  
| `cookies` | Proporciona a la extensión acceso a la `chrome.cookies` API. |  
| `debugger` | Proporciona a la extensión acceso a la `chrome.debugger` API. |  
| `declarativeContent` | Proporciona a la extensión acceso a la `chrome.declarativeContent` API. |  
| `declarativeNetRequest` | Proporciona a la extensión acceso a la `chrome.declarativeNetRequest` API. |  
| `declarativeNetRequestFeedback` | Concede a la extensión acceso a eventos y métodos dentro de la `chrome.declarativeNetRequest` API, que devuelve información sobre las reglas declarativas coincidentes. |  
| `declarativeWebRequest` | Proporciona a la extensión acceso a la `chrome.declarativeWebRequest` API. |  
| `desktopCapture` | Proporciona a la extensión acceso a la `chrome.desktopCapture` API. |  
| `documentScan` | Proporciona a la extensión acceso a la `chrome.documentScan` API. |  
| `downloads` | Proporciona a la extensión acceso a la `chrome.downloads` API. |  
| `enterprise.deviceAttributes` | Proporciona a la extensión acceso a la `chrome.enterprise.deviceAttributes` API. |  
| `enterprise.hardwarePlatform` | Proporciona a la extensión acceso a la `chrome.enterprise.hardwarePlatform` API. |  
| `enterprise.networkingAttributes` | Proporciona a la extensión acceso a la `chrome.enterprise.networkingAttributes` API. |  
| `enterprise.platformKeys` | Proporciona a la extensión acceso a la `chrome.enterprise.platformKeys` API. |  
| `experimental` | Obligatorio si la extensión usa alguna `chrome.experimental.*` API. |  
| `fileBrowserHandler` | Proporciona a la extensión acceso a la `chrome.fileBrowserHandler` API. |  
| `fileSystemProvider` | Proporciona a la extensión acceso a la `chrome.fileSystemProvider` API. |  
| `fontSettings` | Proporciona a la extensión acceso a la `chrome.fontSettings` API. |  
| `geolocation` | Permite que la extensión use la API de geolocalización sin pedir permiso al usuario. |  
| `history` | Proporciona a la extensión acceso a la `chrome.history` API. |  
| `identity` | Proporciona a la extensión acceso a la `chrome.identity` API. |  
| `idle` | Proporciona a la extensión acceso a la `chrome.idle` API. |  
| `loginState` | Proporciona a la extensión acceso a la `chrome.loginState` API. |  
| `management` | Proporciona a la extensión acceso a la `chrome.management` API. |  
| `nativeMessaging` | Proporciona a la extensión acceso a la API de mensajería nativa. |  
| `notifications` | Proporciona a la extensión acceso a la `chrome.notifications` API. |  
| `pageCapture` | Proporciona a la extensión acceso a la `chrome.pageCapture` API. |  
| `platformKeys` | Proporciona a la extensión acceso a la `chrome.platformKeys` API. |  
| `power` | Proporciona a la extensión acceso a la `chrome.power` API. |  
| `printerProvider` | Proporciona a la extensión acceso a la `chrome.printerProvider` API. |  
| `printing` | Proporciona a la extensión acceso a la `chrome.printing` API. |  
| `printingMetrics` | Proporciona a la extensión acceso a la `chrome.printingMetrics` API. |  
| `privacy` | Proporciona a la extensión acceso a la `chrome.privacy` API. |  
| `processes` | Proporciona a la extensión acceso a la `chrome.processes` API. |  
| `proxy` | Proporciona a la extensión acceso a la `chrome.proxy` API. |  
| `scripting` | Proporciona a la extensión acceso a la `chrome.scripting` API. |  
| `search` | Proporciona a la extensión acceso a la `chrome.search` API. |  
| `sessions` | Proporciona a la extensión acceso a la `chrome.sessions` API. |  
| `signedInDevices` | Proporciona a la extensión acceso a la `chrome.signedInDevices` API. |  
| `storage` | Proporciona a la extensión acceso a la `chrome.storage` API. |  
| `system.cpu` | Proporciona a la extensión acceso a la `chrome.system.cpu` API. |  
| `system.display` | Proporciona a la extensión acceso a la `chrome.system.display` API. |  
| `system.memory` | Proporciona a la extensión acceso a la `chrome.system.memory` API. |  
| `system.storage` | Proporciona a la extensión acceso a la `chrome.system.storage` API. |  
| `tabCapture` | Proporciona a la extensión acceso a la `chrome.tabCapture` API. |  
| `tabGroups` | Proporciona a la extensión acceso a la `chrome.tabGroups` API. |  
| `tabs` | Proporciona a la extensión acceso a campos con privilegios de los objetos que pueden usar varias `Tab` API, `chrome.tabs` incluidas y `chrome.windows` .  En muchas circunstancias, la extensión no necesita declarar el permiso para hacer `tabs` uso de estas API. |  
| `topSites` | Proporciona a la extensión acceso a la `chrome.topSites` API. |  
| `tts` | Proporciona a la extensión acceso a la `chrome.tts` API. |  
| `ttsEngine` | Proporciona a la extensión acceso a la `chrome.ttsEngine` API. |  
| `unlimitedStorage` | Proporciona una cuota ilimitada para almacenar datos del lado cliente, como bases de datos y archivos de almacenamiento local.  Sin este permiso, la extensión está limitada a 5 MB de almacenamiento local. |  
| `vpnProvider` | Proporciona a la extensión acceso a la `chrome.vpnProvider` API. |  
| `wallpaper` | Proporciona a la extensión acceso a la `chrome.wallpaper` API. |  
| `webNavigation` | Proporciona a la extensión acceso a la `chrome.webNavigation` API. |  
| `webRequest` | Proporciona a la extensión acceso a la `chrome.webRequest` API. |  
| `webRequestBlocking` | Obligatorio si la extensión usa la `chrome.webRequest` API para bloquear solicitudes. |  

<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí.](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
