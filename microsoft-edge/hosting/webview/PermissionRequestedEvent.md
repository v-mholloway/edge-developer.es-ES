---
description: Proporciona información de eventos sobre la solicitud de permiso actual.
title: Objeto PermissionRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 9bb6cfdbe3cc430f109ea3a258b6c1a176b05da3
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752023"
---
# <span data-ttu-id="26cb9-104">Objeto PermissionRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="26cb9-104">PermissionRequestedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="26cb9-105">Proporciona información de eventos sobre la solicitud de permiso actual.</span><span class="sxs-lookup"><span data-stu-id="26cb9-105">Provides event information about the current permission request.</span></span>  

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

## <span data-ttu-id="26cb9-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26cb9-106">Properties</span></span>  

### <span data-ttu-id="26cb9-107">permissionRequest</span><span class="sxs-lookup"><span data-stu-id="26cb9-107">permissionRequest</span></span>  

<span data-ttu-id="26cb9-108">Devuelve un objeto **[PermissionRequest](permissionrequest.md)** que representa la solicitud de permiso de usuario final que realiza el contenido de la [vista en WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="26cb9-108">Returns a **[PermissionRequest](permissionrequest.md)** object that represents the end-user permission request made by content of the [webview](../webview.md).</span></span>  

<span data-ttu-id="26cb9-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="26cb9-109">This property is read-only.</span></span>  
