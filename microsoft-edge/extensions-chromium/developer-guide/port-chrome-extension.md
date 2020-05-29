---
description: Proceso de migración de la extensión Chrome a Microsoft Edge.
title: Extensión de cromo de puertos para el borde de Microsoft (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 794e8806a95ce0a70069c65c306c30131b01e24d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573714"
---
# <span data-ttu-id="2318f-104">Extensión de cromo de puerto para Edge Microsoft \ (cromo \)</span><span class="sxs-lookup"><span data-stu-id="2318f-104">Port Chrome Extension To Microsoft \(Chromium\) Edge</span></span>  

<span data-ttu-id="2318f-105">El proceso de migración de una extensión Chrome a Microsoft Edge es muy sencillo.</span><span class="sxs-lookup"><span data-stu-id="2318f-105">The process of porting a Chrome Extension to Microsoft Edge is very straightforward.</span></span>  <span data-ttu-id="2318f-106">Las extensiones escritas para cromo, en la mayoría de los casos, se ejecutan en Microsoft Edge con cambios mínimos.</span><span class="sxs-lookup"><span data-stu-id="2318f-106">Extensions written for Chromium, in most cases, run on Microsoft Edge with minimal changes.</span></span>  <span data-ttu-id="2318f-107">Las API de extensión y las claves de manifiesto compatibles con Chrome son compatibles con el código de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2318f-107">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="2318f-108">Sin embargo, Microsoft Edge no admite las siguientes API de extensión:</span><span class="sxs-lookup"><span data-stu-id="2318f-108">However, Microsoft Edge does not support the following Extension APIs:</span></span>  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> <span data-ttu-id="2318f-109">Para poder usar la API, el usuario debe haber iniciado sesión en Microsoft Edge mediante una cuenta de MSA o AAD `chrome.identity.getProfileUserInfo` .</span><span class="sxs-lookup"><span data-stu-id="2318f-109">The user must be signed into Microsoft Edge using an MSA or AAD account in order to use the `chrome.identity.getProfileUserInfo` API.</span></span>  <span data-ttu-id="2318f-110">Si el usuario ha iniciado sesión en Microsoft Edge mediante **ad local**, la API devuelve los `null` valores de los mensajes de correo electrónico y de identificación.</span><span class="sxs-lookup"><span data-stu-id="2318f-110">If the user is signed into Microsoft Edge using **On-premise AD**, the API returns `null` for the email and ID values.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="2318f-111">**Pagos**: Microsoft Edge no admite directamente una extensión que usa los [pagos de la tienda web de Chrome][ChromeDeveloperWebStorePayments] debido al requisito de usar la `identity.getAuthtoken` solicitud para obtener el token de los usuarios con sesión iniciada para enviar la solicitud de API de licencias basadas en REST.</span><span class="sxs-lookup"><span data-stu-id="2318f-111">**Payments**:  Microsoft Edge does not directly support an Extension that uses [Chrome Web Store payments][ChromeDeveloperWebStorePayments] due to the requirement to use the `identity.getAuthtoken` request to get the token for signed-in users to send the REST-based licensing API request.</span></span>  <span data-ttu-id="2318f-112">Microsoft Edge no admite la `getAuthtoken` solicitud, por lo que este flujo no funciona.</span><span class="sxs-lookup"><span data-stu-id="2318f-112">Microsoft Edge does not support the `getAuthtoken` request, so this flow does not work.</span></span>  

<span data-ttu-id="2318f-113">Para migrar su extensión de cromo, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="2318f-113">To port your Chrome Extension, follow these steps:</span></span>  

1.  <span data-ttu-id="2318f-114">Revise las API de extensión de Chrome que se usan en las extensiones.</span><span class="sxs-lookup"><span data-stu-id="2318f-114">Review the Chrome Extension APIs used in your Extensions.</span></span>  <span data-ttu-id="2318f-115">Si usas características o API que Microsoft Edge no admite, es posible que no puedas migrar tu extensión.</span><span class="sxs-lookup"><span data-stu-id="2318f-115">If you are using features or APIs that are not supported by Microsoft Edge, you may not be able to port your Extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="2318f-116">La `getAuthToken` API no funciona con Microsoft Edge, pero puede usarse `launchWebAuthFlow` para obtener un token de OAuth2 para autenticar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="2318f-116">The `getAuthToken` API does not work with Microsoft Edge, however you may use `launchWebAuthFlow` to fetch an OAuth2 token to authenticate users.</span></span>  
    
1.  <span data-ttu-id="2318f-117">Si está usando `Chrome` el nombre o la descripción de su extensión, vuelva a marcar la extensión para `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="2318f-117">If you are using `Chrome` in the name or description of your Extension, re-brand the Extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="2318f-118">Debe pasar el proceso de certificación.</span><span class="sxs-lookup"><span data-stu-id="2318f-118">You must pass the certification process.</span></span>  
    
1.  <span data-ttu-id="2318f-119">Pruebe la extensión para comprobar si funciona en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2318f-119">Test your Extension to check if it works in Microsoft Edge.</span></span>  <span data-ttu-id="2318f-120">El primer paso para ello es asegurarse de tener activadas las características del desarrollador de extensiones.</span><span class="sxs-lookup"><span data-stu-id="2318f-120">The first step to do this is to ensure that you have Extension developer features turned on.</span></span>  <span data-ttu-id="2318f-121">Esto le permite cargar archivos de extensión en Microsoft Edge para poder probar la extensión mientras la desarrolla.</span><span class="sxs-lookup"><span data-stu-id="2318f-121">This enables you to side load Extension files in Microsoft Edge so that you are able to test your Extension while developing it.</span></span>  
    
1.  <span data-ttu-id="2318f-122">Si tienes algún problema, depura las extensiones en Microsoft Edge con el DevTools o [Ponte en contacto con nosotros][mailtoExtensionPartnerOpsMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="2318f-122">If you have any issues, debug your Extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionPartnerOpsMicrosoft].</span></span>  
    
1.  <span data-ttu-id="2318f-123">Ahora tu extensión se ha acabado y está lista para ser embalada.</span><span class="sxs-lookup"><span data-stu-id="2318f-123">Now your Extension is finally polished up and ready to be packaged.</span></span>  <span data-ttu-id="2318f-124">Si desea prepararse para el envío al catálogo de complementos de Microsoft Edge \ (complementos de Microsoft Edge \), no necesita empaquetar la extensión.</span><span class="sxs-lookup"><span data-stu-id="2318f-124">If you wish to prepare for submission to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\), you do not need to package your Extension.</span></span>  <span data-ttu-id="2318f-125">Además, sigue nuestras [pautas de publicación][ExtensionsPublishExtension] para publicar tu extensión en los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2318f-125">Further, follow our [publishing guidelines][ExtensionsPublishExtension] to publish your Extension on Microsoft Edge Addons.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="2318f-126">Si su extensión intercambia mensajes con una aplicación nativa mediante la `chrome.runtime.connectNative` API, asegúrese de que establece en `allowedorigins` " `extension://[Microsoft-Catalog-extensionID]` " en el archivo de manifiesto de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="2318f-126">If your Extension exchanges messages with a native application using `chrome.runtime.connectNative` API, ensure that you set `allowedorigins` to "`extension://[Microsoft-Catalog-extensionID]`" in your native messaging host manifest file.</span></span>  <span data-ttu-id="2318f-127">Esto permite que la aplicación identifique la extensión.</span><span class="sxs-lookup"><span data-stu-id="2318f-127">This enables the app to identify the Extension.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Publicar una extensión"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagos de pago único: Google Chrome"  
