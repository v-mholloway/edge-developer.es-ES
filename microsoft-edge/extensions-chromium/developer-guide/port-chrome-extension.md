---
description: Proceso de porte de extensión de Chrome a Microsoft Edge
title: Portabilidad de una extensión de Chrome a Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 82a96215a0b25be6b2b56227fb77eea09314157f
ms.sourcegitcommit: dc445eae30234af1ad3fa42645aabb940529912b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934294"
---
# <a name="port-a-chrome-extension-to-microsoft-edge"></a>Portabilidad de una extensión de Chrome a Microsoft Edge

Microsoft Edge permite portabilidad de la extensión de Chrome a Microsoft Edge con cambios mínimos.  Las API de extensión y las claves de manifiesto admitidas por Chrome son compatibles con el código con Microsoft Edge.  Para obtener una lista de API admitidas por Microsoft Edge, vaya a [Compatibilidad con api][ExtensionApiSupport].  

Para portabilidad de la extensión de Chrome, siga estos pasos.  

1.  Revise las API de extensión de Chrome usadas en las extensiones con la lista Microsoft Edge [de API][ExtensionApiSupport] compatibles con extensiones de Chrome.  
    
    > [!NOTE]
    > Si la extensión usa API que no son compatibles con Microsoft Edge, es posible que no se porte directamente.  
    
1.  En el archivo de manifiesto, establezca el `update_URL` campo en `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  El valor apunta al archivo de la extensión en el sitio web de Microsoft Edge complementos y permite Microsoft Edge para `.crx` buscar actualizaciones de extensión.  
1.  Si se usa en el nombre o la descripción de la extensión, vuelva a cambiar el nombre `Chrome` de la extensión mediante `Microsoft Edge` .  Para pasar el proceso de certificación, los cambios son necesarios.  
1.  Pruebe la extensión para comprobar si funciona en Microsoft Edge la [instalación local de la extensión][ExtensionsGettingStartedExtensionSideloading].  
1.  Si tiene algún problema, puede depurar las extensiones en Microsoft Edge mediante DevTools o póngase [en contacto con nosotros.][mailtoExtensionMicrosoft]  
1.  Siga las [directrices de publicación][ExtensionsPublishPublishExtension] para publicar la extensión en Microsoft Edge sitio web de complementos.  
    
    > [!NOTE]
    > Si la extensión intercambia mensajes con una aplicación nativa mediante , asegúrese de que se establece en en el archivo de manifiesto `chrome.runtime.connectNative` del host de mensajería `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` nativa.  La configuración permite que la aplicación identifique la extensión.  
    
## <a name="next-steps"></a>Pasos siguientes  

Una vez que el paquete de extensión esté listo para publicarse en el sitio web Microsoft Edge complementos, [cree][ExtensionsPublishCreateDevAccount] una cuenta de desarrollador y [publique la extensión][ExtensionsPublishPublishExtension].  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Compatibilidad con API | Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Instalación local de la extensión | Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registrarse como desarrollador de Microsoft Edge extensión | Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publicar la extensión | Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagos únicos | Desarrollador de Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
