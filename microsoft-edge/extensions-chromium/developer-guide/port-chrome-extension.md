---
description: Proceso de migración de la extensión Chrome a Microsoft Edge.
title: Extensión de cromo de puertos para el borde de Microsoft (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 1852e267579f0fb790c6b8cac75a566298223933
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015691"
---
# Extensión de cromo de puerto para Edge Microsoft \ (cromo \)  

El proceso de migración de una extensión Chrome a Microsoft Edge es muy sencillo.  Las extensiones escritas para cromo, en la mayoría de los casos, se ejecutan en Microsoft Edge con cambios mínimos.  Las API de extensión y las claves de manifiesto compatibles con Chrome son compatibles con el código de Microsoft Edge.  Sin embargo, Microsoft Edge no admite las siguientes API de extensión:  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> Para poder usar la API, el usuario debe haber iniciado sesión en Microsoft Edge mediante una cuenta de MSA o AAD `chrome.identity.getProfileUserInfo` .  Si el usuario ha iniciado sesión en Microsoft Edge mediante **ad local**, la API devuelve los `null` valores de los mensajes de correo electrónico y de identificación.  

> [!IMPORTANT]
> **Pagos**: Microsoft Edge no admite directamente una extensión que usa los [pagos de la tienda web de Chrome][ChromeDeveloperWebStorePayments] debido al requisito de usar la `identity.getAuthtoken` solicitud para obtener el token de los usuarios con sesión iniciada para enviar la solicitud de API de licencias basadas en REST.  Microsoft Edge no admite la `getAuthtoken` solicitud, por lo que este flujo no funciona.  

Para migrar su extensión de cromo, siga estos pasos:  

1.  Revise las API de extensión de Chrome que se usan en las extensiones.  Si usas características o API que Microsoft Edge no admite, es posible que no puedas migrar tu extensión.  
    
    > [!NOTE]
    > La `getAuthToken` API no funciona con Microsoft Edge, pero puede usarse `launchWebAuthFlow` para obtener un token de OAuth2 para autenticar a los usuarios.  
    
1.  Si está usando `Chrome` el nombre o la descripción de su extensión, vuelva a marcar la extensión para `Microsoft Edge` .  Debe pasar el proceso de certificación.  
    
1.  Pruebe la extensión para comprobar si funciona en Microsoft Edge.  El primer paso para ello es asegurarse de tener activadas las características del desarrollador de extensiones.  Esto le permite cargar archivos de extensión en Microsoft Edge para poder probar la extensión mientras la desarrolla.  
    
1.  Si tienes algún problema, depura las extensiones en Microsoft Edge con el DevTools o [Ponte en contacto con nosotros][mailtoExtensionPartnerOpsMicrosoft].  
    
1.  Ahora tu extensión se ha acabado y está lista para ser embalada.  Si desea prepararse para el envío al catálogo de complementos de Microsoft Edge \ (complementos de Microsoft Edge \), no necesita empaquetar la extensión.  Además, sigue nuestras [pautas de publicación][ExtensionsPublishExtension] para publicar tu extensión en los complementos de Microsoft Edge.  
    
    > [!NOTE]
    > Si su extensión intercambia mensajes con una aplicación nativa mediante la `chrome.runtime.connectNative` API, asegúrese de que establece en `allowedorigins` " `extension://[Microsoft-Catalog-extensionID]` " en el archivo de manifiesto de host de mensajería nativa.  Esto permite que la aplicación identifique la extensión.  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Publicar una extensión"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagos de pago único: Google Chrome"  
