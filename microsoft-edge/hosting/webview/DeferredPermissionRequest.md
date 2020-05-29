---
description: Representa una solicitud diferida de permiso de usuario para acceder a la funcionalidad del dispositivo
title: Objeto DeferredPermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, aplicaciones para Windows 10, UWP, Edge
ms.openlocfilehash: 6013f20195fc0f5d4f33b871a9c1b01392bf023e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573380"
---
# <span data-ttu-id="ffbd6-104">Objeto DeferredPermissionRequest</span><span class="sxs-lookup"><span data-stu-id="ffbd6-104">DeferredPermissionRequest object</span></span>

<span data-ttu-id="ffbd6-105">Representa una solicitud diferida por el contenido de la [vista previa](../webview.md) para el permiso del usuario final para acceder a la funcionalidad de dispositivo especializada (como la ubicación geográfica o el bloqueo de puntero).</span><span class="sxs-lookup"><span data-stu-id="ffbd6-105">Represents a deferred request by the content of the [webview](../webview.md) for end-user permission to access specialized device functionality (such as geolocation, or pointer lock).</span></span>

```js
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

## <span data-ttu-id="ffbd6-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="ffbd6-106">Methods</span></span>

### <span data-ttu-id="ffbd6-107">permitir</span><span class="sxs-lookup"><span data-stu-id="ffbd6-107">allow</span></span>

<span data-ttu-id="ffbd6-108">Permite la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-108">Allows the request for permission.</span></span>

```js
deferredPermissionRequest.allow();
```

#### <span data-ttu-id="ffbd6-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="ffbd6-109">Parameters</span></span>

<span data-ttu-id="ffbd6-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-110">This method has no parameters.</span></span>

#### <span data-ttu-id="ffbd6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffbd6-111">Return value</span></span>

<span data-ttu-id="ffbd6-112">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-112">This method does not return a value.</span></span>

### <span data-ttu-id="ffbd6-113">denegar</span><span class="sxs-lookup"><span data-stu-id="ffbd6-113">deny</span></span>

<span data-ttu-id="ffbd6-114">Deniega la solicitud de permiso.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-114">Denies the request for permission.</span></span>

```js
deferredPermissionRequest.deny();
```

#### <span data-ttu-id="ffbd6-115">Parameters</span><span class="sxs-lookup"><span data-stu-id="ffbd6-115">Parameters</span></span>

<span data-ttu-id="ffbd6-116">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-116">This method has no parameters.</span></span>

#### <span data-ttu-id="ffbd6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffbd6-117">Return value</span></span>

<span data-ttu-id="ffbd6-118">Este método no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-118">This method does not return a value.</span></span>

## <span data-ttu-id="ffbd6-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffbd6-119">Properties</span></span>

### <span data-ttu-id="ffbd6-120">id</span><span class="sxs-lookup"><span data-stu-id="ffbd6-120">id</span></span>

<span data-ttu-id="ffbd6-121">Un identificador único que se puede usar para correlacionar la DeferredPermissionRequest actual con un objeto PermissionRequest de un evento MSWebViewPermissionRequested anterior.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-121">A unique ID that can be used to correlate the current DeferredPermissionRequest with a PermissionRequest object from a previous MSWebViewPermissionRequested event.</span></span> <span data-ttu-id="ffbd6-122">Consulta el método **PermissionRequested. defer** .</span><span class="sxs-lookup"><span data-stu-id="ffbd6-122">See the **PermissionRequested.defer** method.</span></span>

<span data-ttu-id="ffbd6-123">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-123">This property is read-only.</span></span>

```js
var id = deferredPermissionRequest.id;
```

##### <span data-ttu-id="ffbd6-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ffbd6-124">Property value</span></span>

<span data-ttu-id="ffbd6-125">Tipo: **largo sin signo**</span><span class="sxs-lookup"><span data-stu-id="ffbd6-125">Type: **Unsigned long**</span></span>

### <span data-ttu-id="ffbd6-126">tipo</span><span class="sxs-lookup"><span data-stu-id="ffbd6-126">type</span></span>

<span data-ttu-id="ffbd6-127">El tipo de permiso que se solicita.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-127">The type of permission being requested.</span></span> <span data-ttu-id="ffbd6-128">Puede ser uno de los siguientes valores de tipo String:</span><span class="sxs-lookup"><span data-stu-id="ffbd6-128">This may be one of the following string values:</span></span>

- <span data-ttu-id="ffbd6-129">**Ubicación**geográfica: acceso a los datos de ubicación a través de Navigator. geolocation.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-129">**geolocation**: access to location data via navigator.geolocation.</span></span>
- <span data-ttu-id="ffbd6-130">**unlimitedIndexedDBQuota**: permitir a las API de IndexedDB ignorar el límite de tamaño de datos almacenado usual.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-130">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>
- <span data-ttu-id="ffbd6-131">**multimedia**: accede al micrófono y a la cámara a través de Navigator. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-131">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>
- <span data-ttu-id="ffbd6-132">**pointerlock**: capacidad para bloquear y controlar el puntero del mouse por medio de Element. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-132">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>
- <span data-ttu-id="ffbd6-133">**notificaciones**por mensaje: posibilidad de Mostrar notificaciones de escritorio a través de la ventana. Aviso.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-133">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>
- <span data-ttu-id="ffbd6-134">**pantalla**: capacidad para realizar capturas de pantalla a través de la API de captura multimedia.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-134">**screen**: ability to take screen shots via the Media Capture API.</span></span>
- <span data-ttu-id="ffbd6-135">**immersiveview**: capacidad para controlar una pantalla de VR.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-135">**immersiveview**: ability to control a VR display.</span></span>

<span data-ttu-id="ffbd6-136">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-136">This property is read-only.</span></span>

```js
var type = deferredPermissionRequest.type;
```

#### <span data-ttu-id="ffbd6-137">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ffbd6-137">Property value</span></span>

<span data-ttu-id="ffbd6-138">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ffbd6-138">Type: **String**</span></span>

### <span data-ttu-id="ffbd6-139">uri</span><span class="sxs-lookup"><span data-stu-id="ffbd6-139">uri</span></span>

<span data-ttu-id="ffbd6-140">Identificador uniforme de recursos (URI) del documento que solicita el permiso.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-140">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>

<span data-ttu-id="ffbd6-141">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ffbd6-141">This property is read-only.</span></span>

```js
var uri = deferredPermissionRequest.uri;
```

##### <span data-ttu-id="ffbd6-142">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ffbd6-142">Property value</span></span>

<span data-ttu-id="ffbd6-143">Tipo: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ffbd6-143">Type: **String**</span></span>

## <span data-ttu-id="ffbd6-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffbd6-144">Requirements</span></span>

|                                           |                                      |
|-------------------------------------------|--------------------------------------|
| <strong><span data-ttu-id="ffbd6-145">Cliente mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="ffbd6-145">Minimum supported client</span></span></strong> | <span data-ttu-id="ffbd6-146">Windows 10 [solo aplicaciones de la tienda Windows]</span><span class="sxs-lookup"><span data-stu-id="ffbd6-146">Windows 10 [Windows Store apps only]</span></span> |
| <strong><span data-ttu-id="ffbd6-147">Servidor mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="ffbd6-147">Minimum supported server</span></span></strong> |            <span data-ttu-id="ffbd6-148">No se admite</span><span class="sxs-lookup"><span data-stu-id="ffbd6-148">Not supported</span></span>             |
| <strong><span data-ttu-id="ffbd6-149">Teléfono mínimo admitido</span><span class="sxs-lookup"><span data-stu-id="ffbd6-149">Minimum supported phone</span></span></strong>  |            <span data-ttu-id="ffbd6-150">No se admite</span><span class="sxs-lookup"><span data-stu-id="ffbd6-150">Not supported</span></span>             |
