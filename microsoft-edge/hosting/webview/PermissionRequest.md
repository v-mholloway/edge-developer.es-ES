---
description: Proporciona información sobre una solicitud de permiso
title: Objeto PermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: c769bf122c3ca116d5783b73d0ff4f183d2cd52d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752121"
---
# Objeto PermissionRequest  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Proporciona información sobre una solicitud de permiso. Este objeto está disponible desde la propiedad permissionRequest de los argumentos del evento del evento WebView [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) .  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});
```  

## Métodos  

### permitir  

Permite la solicitud de permiso.  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

### aplazar  

Si, en lugar de usar de forma sincrónica o no permitir un PermissionRequest, necesitarás tiempo para interactuar con el usuario o emprender otra acción asincrónica, llama a defer () en la PermissionRequest.  Ahora PermissionRequest estará disponible como DeferredPermissionRequest de getDeferredPermissionRequests y getDeferredPermissionRequestById.  Puede correlacionar el PermissionRequest actual con el DeferredPermissionRequest correspondiente a través de la propiedad ID. de coincidencia.  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

### denegar  

Deniega la solicitud de permiso.  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

## Propiedades  

### id  

Un identificador único que se puede usar para correlacionar el PermissionRequest actual con un DeferredPermissionRequest correspondiente si se usa el método defer.  Consulta el método defer.  

Esta propiedad es de solo lectura.  

##### Valor de propiedad  

Tipo: **largo sin signo**  

### situación  

Devuelve "Unknown", "aplazar", "permitir" o "denegar" para indicar el estado actual de la solicitud de permiso.  La cadena de estado se corresponde con el método allow, deny o defer que se llamó por última vez o "Unknown" si no se llamó a ninguno de los métodos.  

Esta propiedad es de solo lectura.  

#### Valor de propiedad  

Tipo: **cadena**  

### tipo  

El tipo de permiso que se solicita. Puede ser uno de los siguientes valores de tipo String:  

*   **Ubicación**geográfica: acceso a los datos de ubicación a través de Navigator. geolocation.  
*   **unlimitedIndexedDBQuota**: permitir a las API de IndexedDB ignorar el límite de tamaño de datos almacenado usual.  
*   **multimedia**: accede al micrófono y a la cámara a través de Navigator. getUserMedia.  
*   **pointerlock**: capacidad para bloquear y controlar el puntero del mouse por medio de Element. requestPointerLock.  
*   **notificaciones**por mensaje: posibilidad de Mostrar notificaciones de escritorio a través de la ventana. Aviso.  
*   **pantalla**: capacidad para realizar capturas de pantalla a través de la API de captura multimedia.  
*   **immersiveview**: capacidad para controlar una pantalla de VR.  

Esta propiedad es de solo lectura.  

#### Valor de propiedad  

Tipo: **cadena**  

### uri  

Identificador uniforme de recursos (URI) del documento que solicita el permiso.  

Esta propiedad es de solo lectura.  

#### Valor de propiedad  

Tipo: **cadena**  
