---
description: Proceso de porte de la extensión de Chrome a Microsoft Edge.
title: Extensión port Chrome a Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 64a92927b9fe7658562f87f326bb9ac148991031
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327697"
---
# Portabilidad de la extensión  

Microsoft Edge le permite portabilidad de la extensión de Chrome con cambios mínimos.  Las API de extensión y las claves de manifiesto compatibles con Chrome son compatibles con código con Microsoft Edge.  Para obtener una lista de las API admitidas por Microsoft Edge, vaya al [soporte técnico de la API.][ExtensionApiSupport]  

Para portabilidad de la extensión de Chrome, siga estos pasos.  

1.  Revisa las API de extensión de Chrome que se usan en las extensiones con la lista de API compatibles con [extensiones de][ExtensionApiSupport] Microsoft Edge.  
    
    > [!NOTE]
    > Si la extensión usa API que no son compatibles con Microsoft Edge, es posible que no se porte directamente.  
    
1.  En el archivo de manifiesto, establezca `update_URL` el campo en `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  El valor apunta al archivo de la extensión en el almacén de complementos de Microsoft Edge y permite a Microsoft Edge comprobar si hay actualizaciones `.crx` de extensión.  
1.  Si se usa en el nombre o la descripción de la extensión, vuelva a cambiar el nombre `Chrome` de la extensión con `Microsoft Edge` .  Para pasar el proceso de certificación, se requieren los cambios.  
1.  Pruebe la extensión para comprobar si funciona en Microsoft Edge mediante [la instalación de prueba de la extensión.][ExtensionsGettingStartedExtensionSideloading]  
1.  Si tiene algún problema, puede depurar las extensiones en Microsoft Edge con DevTools o ponerse [en contacto con nosotros.][mailtoExtensionMicrosoft]  
1.  Sigue las [directrices de publicación][ExtensionsPublishPublishExtension] para publicar la extensión en la Tienda de complementos de Microsoft Edge.  
    
    > [!NOTE]
    > Si la extensión intercambia mensajes con una aplicación nativa mediante, asegúrese de establecerla en el archivo de manifiesto del `chrome.runtime.connectNative` `allowed_origins` host de mensajería `extension://[Microsoft-Catalog-extensionID]` nativo.  La configuración permite que la aplicación identifique la extensión.  
    
## Pasos siguientes  

Cuando el paquete de extensión esté listo para publicarse en la tienda de complementos de Microsoft [Edge,][ExtensionsPublishCreateDevAccount] cree una cuenta de desarrollador y [publique la extensión.][ExtensionsPublishPublishExtension]  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Compatibilidad con API | Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Instalación local de la extensión | Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro de desarrolladores | Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publicar la extensión | Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pago único | Chrome Developer"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
