---
description: Encuentre información sobre las API actuales y futuras, así como sus problemas conocidos o incompatibilidades con Chrome.
title: 'Extensiones: API compatibles'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b8cf13f42c99779f23eaa7b941093752fb25b207
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236599"
---
# API compatibles  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

A continuación se muestra una lista detallada de los miembros de la API admitidos. El desarrollo de la plataforma de extensión está en curso, por lo que debe consultar las actualizaciones con frecuencia.

> [!NOTE]
>  - Para Microsoft Edge, todas las API de extensión están bajo el `browser` espacio de nombres, por ejemplo, `browser.browserAction.disable()` .
>  - Las API de extensión de Microsoft Edge usan devoluciones de llamada, no promesas.


## Problemas de repaso

Los siguientes problemas conocidos abarcan la plataforma de extensión y se corregirán en un futuro próximo:

- Al usar la `url()` propiedad CSS, las direcciones URL absolutas `ms-browser-extension://` que usen no funcionarán como en Chrome. Para evitar este problema, use rutas de referencia relativas a los recursos (a partir del directorio raíz de la extensión).
- `window.open()` no funciona en scripts de fondo de extensión. Usa `browser.windows.create()` en su lugar.
- Las cookies compartidas son compatibles, pero la secuencia de comandos de fondo de extensión no tendrá acceso a las cookies de sesión establecidas en la pestaña antes de habilitar la extensión. Este problema no afecta a las cookies persistentes.
- Si solo se especifican permisos no compatibles para una extensión, es decir, `activeTab`, el intento de transferir la extensión provocará que se desinstale la extensión con el siguiente mensaje: "se ha producido un problema con las extensiones, así que tuvimos que volver a instalarlas. Tendrás que volver a activarlos.
- La activación de una descarga mediante una etiqueta de delimitador oculta fallará de las secuencias de comandos en segundo plano. Esto debe hacerse desde una página de extensión.


## marcadores

`bookmarks`Se admiten las siguientes API:

| API                                   | Problemas conocidos                                             | Incompatibilidades con Chrome
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [marcadores](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks) | | |
| [marcadores. crear](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/create) | | |
| [marcadores. quitar](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/remove) | | |
| [bookmarks. getTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/getTree) |  | |
| [marcadores. mover](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/move) | | |
| [bookmarks. removeTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/removeTree) | | |
| [bookmarks. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/update)            | | |


## browserAction

`browserAction`Se admiten las siguientes API:

| API                                   | Problemas conocidos                                             | Incompatibilidades con Chrome
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [browserAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction) | | |
| [browserAction. Disable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/disable) | | |
| [browserAction. Enable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/enable) | | |
| [browserAction.getBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeBackgroundColor) |  | |
| [browserAction.setBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeBackgroundColor) | | |
| [browserAction. unclicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/onClicked) | | |
| [browserAction.setBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeText)            | | |
| [browserAction.setPopup](https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setPopup)  | | |
| [browserAction.getBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeText)   | | |
| [browserAction.setIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setIcon) | `browserAction.setIcon` no se conserva. <br/><br/> El `imageData` parámetro no es compatible. <br/><br/> `path` es un parámetro obligatorio.| |
| [browserAction.getTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getTitle) | | |
| [browserAction.setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setTitle) | | |

## contextMenus

`contextMenus`Se admiten las siguientes API:

| API                    | Problemas conocidos | Incompatibilidades con Chrome
|------------------------|--------------|----------------------|
| [contextMenus](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus)  |  | |
| [contextMenus. ContextType](https://developer.mozilla.org/Add-ons/WebExtensions/API/contextMenus/ContextType) | `"page_action"` `ContextType` no se mostrará en el menú contextual acción de página.| Microsoft Edge no es compatible con el `"launcher"` `ContextType` .|
| [contextMenus. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/create)    | Cuando las extensiones no proporcionan una `contextmenuid` , la `id` generada no es única. | |
| [contextMenus. unclicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/onClicked) | | |
| [contextMenus. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/remove) | | |
| [contextMenus. removeAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/removeAll) | | |
| [contextMenus. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/update) | | |

## cookies

`cookies`Se admiten las siguientes API:

| API                    | Problemas conocidos | Incompatibilidades con Chrome
|------------------------|--------------|----------------------|
| [cookies](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/cookies)  |  | |
| [cookies. get](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/get)    |  | |
| [cookies. getAll](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAll) |   | Si no se proporciona una dirección URL, solo se recuperarán las cookies de las direcciones URL de las pestañas abiertas actualmente. En Chrome, se obtienen todas las cookies en el equipo de un usuario. |
| [cookies. getAllCookieStores](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAllCookieStores)  | | Siempre devuelve el mismo almacén de cookies predeterminado con el identificador "0". Todas las cookies pertenecen a este almacén. |
| [cookies. onchange](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/onChanged)    | | No se admite. |
| [cookies. quitar](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/remove) |  | |
| [cookies. Set](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/set)    |  | |



## extensiones

`extension`Se admiten las siguientes API:

| API                                   | Problemas conocidos | Incompatibilidades con Chrome
|---------------------------------------|----------------------------------------------------------|-------------|
[extensiones](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension) | | |
[extensión. getBackgroundPage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getBackgroundPage) | | |
[extensión. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getURL) | | |
[extensión. getViews](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/getViews) | | |
[extensión. isAllowedIncognitoAccess](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/isAllowedIncognitoAccess) | | | 
[extension.inIncognitoContext](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/inIncognitoContext) | | | 



## i18n

`i18n`Se admiten las siguientes API:

API | Problemas conocidos | Incompatibilidades con Chrome
:------| :-------- | :---------------------
[i18n](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n) | | |
[i18n. getAcceptLanguages](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getAcceptLanguages) | | |
[i18n. getMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/i18n/getMessage) | `i18n.getMessage` con una clave no válida se produce una excepción en lugar de no tener éxito. <br/><br/> `i18n.getMessage` el argumento espera cadenas, pero también debe permitir un int o iniciar una excepción. | |
[i18n. getUILanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getUILanguage) | | |

## está

`idle`Se admiten las siguientes API:

API | Problemas conocidos | Incompatibilidades con Chrome
:------| :-------- | :---------------------
[está](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle) | | |
[idle. setDetectionInterval](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/setDetectionInterval) | | |
[idle. queryState](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/queryState) | | |

## notificaciones

`notifications`Se admiten las siguientes API:

API | Problemas conocidos | Incompatibilidades con Chrome
:------| :-------- | :---------------------
[notificaciones](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) | | |
[notificaciones. NotificationOptions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/NotificationOptions) | | |
[notificaciones. TemplateType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/TemplateType) | | |
[notificaciones. borrar](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/clear) | | |
[notificaciones. crear](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/create) | | |
[notifications. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/getAll) | | |
[notificaciones. actualizar](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/update) | | |
[notificaciones. onButtonClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onButtonClicked) | | |
[notificaciones. unclicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClicked) | | |
[notificaciones. OnClose](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClosed) | | |
notificaciones. onPermissionLevelChanged | | |
notificaciones. getPermissionLevel | | |

## pageAction

`pageAction`Se admiten las siguientes API:

API | Problemas conocidos | Incompatibilidades con Chrome
:------------ | :------------- | :--------------------
[pageAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction) | | |
[pageAction.getPopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getPopup) | | |
[pageAction.getTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getTitle) | | |
[pageAction. Hide](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/hide) | | |
[pageAction. unclicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/onClicked) | | |
[pageAction.setIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setIcon) | | El `imageData` parámetro no es compatible. <br/><br/> `path` es un parámetro obligatorio. |
[pageAction.setPopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setPopup) | | |
[pageAction.setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setTitle) | | |
[pageAction. show](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/show) | | |



## motores

`runtime`Se admiten las siguientes API:

API | Problemas conocidos | Incompatibilidades con Chrome
:------------ | :------------- | :-------------------
[motores](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime) | | |
[Runtime. Port. disconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Port. OnDisconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Port. PostMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Connect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connect) | | |
[Runtime. connectNative](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) | | |
[runtime.id](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id) | | |
[Runtime. getBackgroundPage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/getBackgroundPage) | | |
[Runtime. getManifest](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getManifest) | | |
[Runtime. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getURL) | | |
[Runtime. lastError](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/lastError) | | |
[Runtime. Reload](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/reload) | | |
[Runtime. sendMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage) | Las páginas de extensión de Microsoft Edge pueden usarse `runtime.sendMessage` / `onMessage` para enviar mensajes a sí mismos. <br/><br/> `runtime.sendmessage` no es compatible con las páginas del sitio. | Microsoft Edge no admite el `options` parámetro.|
[Runtime. sendNativeMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) | | |
[Runtime. setUninstallUrl](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/setUninstallUrl) | | |
[Runtime. conecto](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onConnect) | | |
[Runtime. en la instalación](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onInstalled) | | |
[Runtime. el mensaje](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onMessage) | `tab` el objeto en el `runtime.onMessage` evento no está implementado por completo. | `MessageSender.tlsChannelId` no es compatible con Microsoft Edge.|

## almacenamiento

`storage`Se admiten las siguientes API:

API | Problemas conocidos | Incompatibilidades con Chrome
:------------ | :------------- | :------------------------
[almacenamiento](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage) |  | |
[almacenamiento. local. get](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/get)  | | |
[Storage. local. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/remove)  | | |
[Storage. local. Set](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/set)  | | |
[almacenamiento. local. borrar](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/clear) | | |
[Storage. local. getBytesInUse](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/getBytesInUse) | | `storage.local` los datos se conservan en otro formato que el cromo, lo que hace que se devuelva un valor diferente al realizar la llamada `storage.local.getBytesInUse` .  <br/><br/>Por ejemplo: `storage.local.set({ "k": { "s": "âas" } }` devuelve 13 en Chrome y 50 en Microsoft Edge.|
[Storage. Sync. get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/get) | Si la cantidad combinada de caracteres de los `name` campos y del `author` manifiesto es superior a 31 caracteres, `storage.sync` es posible que el espacio de nombres no funcione. | |
[Storage. Sync. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/remove) | | |
[Storage. Sync. Set](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/set) | | |
[almacenamiento. onchange](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/onChanged) | | |

## pestañas

`tabs`Se admiten las siguientes API:

API | Problemas conocidos | Incompatibilidades con Chrome
:------------ | :------------- | :----------------
[pestañas](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[Tabs. captureVisibleTab](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/captureVisibleTab) | | |
[pestañas. crear](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/create) | | `selected`, `pinned` , y `openerTabId` no son compatibles. |
[Tabs. detectLanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/detectLanguage) | | |
[tabs.executeScript](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/executeScript) | `runAt` se omite, aunque se haya activado. El script que se ejecuta en un marco específico aún no es compatible. | |
[pestañas. get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/get) | Las páginas de opciones, cuando se solicita una pestaña que no está en la ventana, fallan esta llamada. | |
[Tabs. getCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/getCurrent) | | |
[Tabs. insertCSS](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/insertCSS) | `runAt` se omite, aunque se haya activado. | `cssOrigin` no es compatible. |
[Tabs. Onactivated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onActivated) | | |
[pestañas. adjuntas](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onAttached) | | |
[Tabs. Created](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onCreated) | | |
[Tabs. undetach](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[Tabs. Quito](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onRemoved) | | |
[Tabs. en reemplazo](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/onReplaced) | | |
[Tabs. Actualiz.](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onUpdated) | Después de desinstalar o volver a instalar, la dirección URL no se recibirá hasta que se reinicie Microsoft Edge. | |
[pestañas. Query](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/query) | `pinned`, `audible` y `muted` aún no se admiten. <br/><br/> `"popup"` `windowType` aún no es compatible. | `highlighted` no es compatible. <br/><br/> `"panel"`, `"app"` , y `"devtools"` `windowType` no son compatibles. |
[pestañas. recargar](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/reload) | | Microsoft Edge no admite promesas. |
[pestañas. quitar](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/remove) | | |
[Tabs. sendMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/sendMessage) | Mensajería un marco específico aún no es compatible. `tabs.sendMessage` nunca envía una respuesta después de una actualización de pestaña si no hay `runtime.onMessage` escuchas presentes en la pestaña recepción. | |
[pestañas. Limitado](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/Tab) | `audible`las propiedades,,, `mutedInfo` `inPrivate` `width` y `height` aún no se admiten. | `openerTabId`, `selected` y `highlighted` no se admiten propiedades. |
[Tabs. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/update) | `pinned` y `muted` aún no son compatibles. | `highlighted` y `selected` no son compatibles. |


## navegación en

`webNavigation`Se admiten las siguientes API:


| API                                                                                                                                                           | Problemas conocidos                                | Incompatibilidades con Chrome                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [navegación en](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation)                                                     | Los identificadores de tabulación son incorrectos.                      | Filtrar, TransitionTypes y TransitionQualifiers no se admiten. <br/><br/> En el caso de una pestaña, todos serán `processIds` iguales. |
| [Navegación en webgetAllFrames](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getAllFrames)                           | No incluye elementos Object-as-iframe. |                                                                                                                             |
| [webnavigation. getFrame](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getFrame)                                   |                                             |                                                                                                                             |
| [Navegación en webonBeforeNavigate](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onBeforeNavigate)                   |                                             |                                                                                                                             |
| [navegación en confirmada](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onCommitted)                                           |                                             |                                                                                                                             |
| [webnavigation. alcompletado](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCompleted)                             |                                             |                                                                                                                             |
| [Navegación en webonCreatedNavigationTarget](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCreatedNavigationTarget) |                                             |                                                                                                                             |
| [Navegación en webonDOMContentLoaded](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onDOMContentLoaded)               |                                             |                                                                                                                             |
| [Navegación en webonErrorOccurred](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onErrorOccurred)                     |                                             |                                                                                                                             |
| [Navegación en webonHistoryStateUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onHistoryStateUpdated)         |                                             |                                                                                                                             |
| [Navegación en webonReferenceFragmentUpdated](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onReferenceFragmentUpdated)            |                                             |                                                                                                                             |
| [Navegación en webonTabReplaced](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onTabReplaced)                         |                                             | No se admite.                                                                                                              |
| [Navegación en webTransitionType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionType)                       |                                             |                                                                                                                             |
| [Navegación en webTransitionQualifier](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionQualifier)             |                                             |                                                                                                                             |

## WebRequest

`webRequest`Se admiten las siguientes API:

API | Problemas conocidos | Incompatibilidades con Chrome
:------ | :----- | :-------
[WebRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest) | `webRequest` no es compatible con la sincronización sincrónica `XmlHttpRequests` . | No se admiten las solicitudes de red desde extensiones, como opciones, páginas emergentes o de fondo.<br/><br/> `<object>` `<embed>` No se admiten las solicitudes y elementos de red.<br/><br/> Los encabezados no se pueden modificar en las solicitudes almacenadas en caché.  |
[handlerBehaviorChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/handlerBehaviorChanged) | | Los cambios de controlador se administran automáticamente en Microsoft Edge.<br/><br/>La llamada no tiene ningún efecto.  |
[onAuthRequired](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onAuthRequired) | | |
[onBeforeRedirect](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRedirect) | | |
[onBeforeRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRequest) | | `requestBody` no es compatible. |
[onBeforeSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeSendHeaders) | | |
[Mi](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onCompleted) | | |
[onErrorOccurred](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onErrorOccurred) | | |
[onHeadersReceived](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onHeadersReceived) | |  |
[onResponseStarted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onResponseStarted) | |  |
[onSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onSendHeaders) | | |

## windows

`windows`Se admiten las siguientes API:


| API                                                                                                                               | Problemas conocidos                                                   | Incompatibilidades con Chrome                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [windows](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows)                                     |                                                                | `Window` los objetos no admiten `alwaysOnTop` propiedades en Microsoft Edge. <br/><br/>InPrivate no es compatible. |
| [ventana. CreateType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/CreateType)                            |                                                                | `"panel"` y `"detached_panel"` no son compatibles con Microsoft Edge.                                           |
| [Windows. Create](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/create)                                    |                                                                | `tabId` no se admite el parámetro de recortar una pestaña.                                                       |
| [Windows. get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/get)                             |                                                                |                                                                                                                 |
| [Windows. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getAll)                       | `windows.getAll({populate: true})` falta la `tabs` propiedad. |                                                                                                                 |
| [Windows. getCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getCurrent)               |                                                                |                                                                                                                 |
| [Windows. getLastFocused](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getLastFocused)       |                                                                |                                                                                                                 |
| [Windows. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/update)                       | No se admite la especificación de la posición.                          | `"minimized"`/`"maximized"`/`"fullscreen"` y `drawAttention` no son compatibles con Microsoft Edge.             |
| [Windows. Created](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/onCreated)                 |                                                                | `WindowType` no se admite el filtro.                                                                           |
| [Windows. onFocusChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/onFocusChanged)                    |                                                                | `WindowType` no se admite el filtro.                                                                           |
| [ventana. WindowState](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowState)                          | `"minimized"`, `"maximized"` , `"fullscreen"` no son compatibles. | `"docked"` no es compatible con Microsoft Edge.                                                                  |
| [ventana. WindowType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowType)                            |                                                                | `"panel"`, `"app"` y `"devtools"` no son compatibles con Microsoft Edge.                                       |
| [ventana. WINDOW_ID_CURRENT](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_CURRENT) |                                                                |                                                                                                                 |
| [ventana. WINDOW_ID_NONE](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_NONE)       |                                                                |                                                                                                                 |
