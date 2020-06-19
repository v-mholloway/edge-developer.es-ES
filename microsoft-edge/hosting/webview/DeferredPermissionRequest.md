---
description: Representa una solicitud diferida de permiso de usuario para acceder a la funcionalidad del dispositivo
title: Objeto DeferredPermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: dc1f0753f879f511fdc380c806eb88b6be358016
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752146"
---
# Objeto DeferredPermissionRequest  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Representa una solicitud diferida por el contenido de la [vista previa](../webview.md) para el permiso del usuario final para acceder a la funcionalidad de dispositivo especializada (como la ubicación geográfica o el bloqueo de puntero).  

```javascript
// In this sample, when we receive a permission request we construct some basic UI to ask the
// user if they want to give permission.
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    const requestContainer = document.createElement("div");

    // We use this function as the handler for the allow and deny buttons.
    function completeDeferredPermissionRequest(allow) {
        // Find the DeferredPermissionRequest using the id of the PermissionRequest we deferred.
        const deferredPermissionRequest = webview.getDeferredPermissionRequestById(permissionRequest.id);
        if (allow) {
            deferredPermissionRequest.allow();
        }
        else {
            deferredPermissionRequest.deny();
        }
        requestContainer.parentElement.removeChild(requestContainer);
    }

    // Construct some simple UI to tell the user about the permission request and get their
    // feedback via the allow and deny buttons
    const description = document.createElement("span");
    description.textContent = "Allow " + uri + " to access " + type + "?";

    const allow = document.createElement("button");
    allow.textContent = "Allow";
    allow.addEventListener("click", () => completeDeferredPermissionRequest(true));

    const deny = document.createElement("button");
    deny.textContent = "Deny";
    deny.addEventListener("click", () => completeDeferredPermissionRequest(false));

    requestContainer.appendChild(description);
    requestContainer.appendChild(allow);
    requestContainer.appendChild(deny);
    document.body.appendChild(requestContainer);

    permissionRequest.defer();
});
```  

## Métodos  

### permitir  

Permite la solicitud de permiso.  

```javascript
deferredPermissionRequest.allow();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

### denegar  

Deniega la solicitud de permiso.  

```javascript
deferredPermissionRequest.deny();
```  

#### Parameters  

Este método no tiene parámetros.  

#### Valor devuelto  

Este método no devuelve un valor.  

## Propiedades  

### id  

Un identificador único que se puede usar para correlacionar la DeferredPermissionRequest actual con un objeto PermissionRequest de un evento MSWebViewPermissionRequested anterior. Consulta el método **PermissionRequested. defer** .  

Esta propiedad es de solo lectura.  

```javascript
var id = deferredPermissionRequest.id;
```  

##### Valor de propiedad  

Tipo: **largo sin signo**  

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

```javascript
var type = deferredPermissionRequest.type;
```  

#### Valor de propiedad  

Tipo: **cadena**  

### uri  

Identificador uniforme de recursos (URI) del documento que solicita el permiso.  

Esta propiedad es de solo lectura.  

```javascript
var uri = deferredPermissionRequest.uri;
```  

##### Valor de propiedad  

Tipo: **cadena**  

## Requisitos  

|  |  |  
|:--- |:--- |  
| **Cliente mínimo admitido** | Windows 10 [solo aplicaciones de la tienda Windows] |  
| **Servidor mínimo admitido** | No se admite |  
| **Teléfono mínimo admitido** | No se admite |  
