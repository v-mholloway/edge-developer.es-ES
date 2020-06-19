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
# <span data-ttu-id="a2dd9-104">Objeto PermissionRequest</span><span class="sxs-lookup"><span data-stu-id="a2dd9-104">PermissionRequest object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="a2dd9-105">Proporciona información sobre una solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-105">Provides information about a permission request.</span></span> <span data-ttu-id="a2dd9-106">Este objeto está disponible desde la propiedad permissionRequest de los argumentos del evento del evento WebView [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) .</span><span class="sxs-lookup"><span data-stu-id="a2dd9-106">This object is available from the permissionRequest property of the event args from the [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) webview event.</span></span>  

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

## <span data-ttu-id="a2dd9-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="a2dd9-107">Methods</span></span>  

### <span data-ttu-id="a2dd9-108">permitir</span><span class="sxs-lookup"><span data-stu-id="a2dd9-108">allow</span></span>  

<span data-ttu-id="a2dd9-109">Permite la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-109">Allows the request for permission.</span></span>  

#### <span data-ttu-id="a2dd9-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="a2dd9-110">Parameters</span></span>  

<span data-ttu-id="a2dd9-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-111">This method has no parameters.</span></span>  

#### <span data-ttu-id="a2dd9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2dd9-112">Return value</span></span>  

<span data-ttu-id="a2dd9-113">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-113">This method does not return a value.</span></span>  

### <span data-ttu-id="a2dd9-114">aplazar</span><span class="sxs-lookup"><span data-stu-id="a2dd9-114">defer</span></span>  

<span data-ttu-id="a2dd9-115">Si, en lugar de usar de forma sincrónica o no permitir un PermissionRequest, necesitarás tiempo para interactuar con el usuario o emprender otra acción asincrónica, llama a defer () en la PermissionRequest.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-115">If instead of synchronously allowing or disallowing a PermissionRequest, you require time to interact with the user or take some other asynchronous action, call defer() on the PermissionRequest.</span></span>  <span data-ttu-id="a2dd9-116">Ahora PermissionRequest estará disponible como DeferredPermissionRequest de getDeferredPermissionRequests y getDeferredPermissionRequestById.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-116">The PermissionRequest will now be available as a DeferredPermissionRequest from getDeferredPermissionRequests and getDeferredPermissionRequestById.</span></span>  <span data-ttu-id="a2dd9-117">Puede correlacionar el PermissionRequest actual con el DeferredPermissionRequest correspondiente a través de la propiedad ID. de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-117">You can correlate the current PermissionRequest with the corresponding DeferredPermissionRequest via the matching id property.</span></span>  

#### <span data-ttu-id="a2dd9-118">Parameters</span><span class="sxs-lookup"><span data-stu-id="a2dd9-118">Parameters</span></span>  

<span data-ttu-id="a2dd9-119">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-119">This method has no parameters.</span></span>  

#### <span data-ttu-id="a2dd9-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2dd9-120">Return value</span></span>  

<span data-ttu-id="a2dd9-121">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-121">This method does not return a value.</span></span>  

### <span data-ttu-id="a2dd9-122">denegar</span><span class="sxs-lookup"><span data-stu-id="a2dd9-122">deny</span></span>  

<span data-ttu-id="a2dd9-123">Deniega la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-123">Denies the request for permission.</span></span>  

#### <span data-ttu-id="a2dd9-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="a2dd9-124">Parameters</span></span>  

<span data-ttu-id="a2dd9-125">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-125">This method has no parameters.</span></span>  

#### <span data-ttu-id="a2dd9-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2dd9-126">Return value</span></span>  

<span data-ttu-id="a2dd9-127">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-127">This method does not return a value.</span></span>  

## <span data-ttu-id="a2dd9-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a2dd9-128">Properties</span></span>  

### <span data-ttu-id="a2dd9-129">id</span><span class="sxs-lookup"><span data-stu-id="a2dd9-129">id</span></span>  

<span data-ttu-id="a2dd9-130">Un identificador único que se puede usar para correlacionar el PermissionRequest actual con un DeferredPermissionRequest correspondiente si se usa el método defer.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-130">A unique ID that can be used to correlate the current PermissionRequest with a corresponding DeferredPermissionRequest if the defer method is used.</span></span>  <span data-ttu-id="a2dd9-131">Consulta el método defer.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-131">See the defer method.</span></span>  

<span data-ttu-id="a2dd9-132">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-132">This property is read-only.</span></span>  

##### <span data-ttu-id="a2dd9-133">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a2dd9-133">Property value</span></span>  

<span data-ttu-id="a2dd9-134">Tipo: **largo sin signo**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-134">Type: **Unsigned long**</span></span>  

### <span data-ttu-id="a2dd9-135">situación</span><span class="sxs-lookup"><span data-stu-id="a2dd9-135">state</span></span>  

<span data-ttu-id="a2dd9-136">Devuelve "Unknown", "aplazar", "permitir" o "denegar" para indicar el estado actual de la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-136">Returns "unknown", "defer", "allow", or "deny" to indicate the current state of permission request.</span></span>  <span data-ttu-id="a2dd9-137">La cadena de estado se corresponde con el método allow, deny o defer que se llamó por última vez o "Unknown" si no se llamó a ninguno de los métodos.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-137">The state string will correspond to whichever method allow, deny, or defer was called last or "unknown" if none of the methods have been called.</span></span>  

<span data-ttu-id="a2dd9-138">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-138">This property is read-only.</span></span>  

#### <span data-ttu-id="a2dd9-139">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a2dd9-139">Property value</span></span>  

<span data-ttu-id="a2dd9-140">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-140">Type: **String**</span></span>  

### <span data-ttu-id="a2dd9-141">tipo</span><span class="sxs-lookup"><span data-stu-id="a2dd9-141">type</span></span>  

<span data-ttu-id="a2dd9-142">El tipo de permiso que se solicita.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-142">The type of permission being requested.</span></span> <span data-ttu-id="a2dd9-143">Puede ser uno de los siguientes valores de tipo String:</span><span class="sxs-lookup"><span data-stu-id="a2dd9-143">This may be one of the following string values:</span></span>  

*   <span data-ttu-id="a2dd9-144">**Ubicación**geográfica: acceso a los datos de ubicación a través de Navigator. geolocation.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-144">**geolocation**: access to location data via navigator.geolocation.</span></span>  
*   <span data-ttu-id="a2dd9-145">**unlimitedIndexedDBQuota**: permitir a las API de IndexedDB ignorar el límite de tamaño de datos almacenado usual.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-145">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>  
*   <span data-ttu-id="a2dd9-146">**multimedia**: accede al micrófono y a la cámara a través de Navigator. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-146">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>  
*   <span data-ttu-id="a2dd9-147">**pointerlock**: capacidad para bloquear y controlar el puntero del mouse por medio de Element. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-147">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>  
*   <span data-ttu-id="a2dd9-148">**notificaciones**por mensaje: posibilidad de Mostrar notificaciones de escritorio a través de la ventana. Aviso.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-148">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>  
*   <span data-ttu-id="a2dd9-149">**pantalla**: capacidad para realizar capturas de pantalla a través de la API de captura multimedia.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-149">**screen**: ability to take screen shots via the Media Capture API.</span></span>  
*   <span data-ttu-id="a2dd9-150">**immersiveview**: capacidad para controlar una pantalla de VR.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-150">**immersiveview**: ability to control a VR display.</span></span>  

<span data-ttu-id="a2dd9-151">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-151">This property is read-only.</span></span>  

#### <span data-ttu-id="a2dd9-152">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a2dd9-152">Property value</span></span>  

<span data-ttu-id="a2dd9-153">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-153">Type: **String**</span></span>  

### <span data-ttu-id="a2dd9-154">uri</span><span class="sxs-lookup"><span data-stu-id="a2dd9-154">uri</span></span>  

<span data-ttu-id="a2dd9-155">Identificador uniforme de recursos (URI) del documento que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-155">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>  

<span data-ttu-id="a2dd9-156">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a2dd9-156">This property is read-only.</span></span>  

#### <span data-ttu-id="a2dd9-157">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a2dd9-157">Property value</span></span>  

<span data-ttu-id="a2dd9-158">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a2dd9-158">Type: **String**</span></span>  
