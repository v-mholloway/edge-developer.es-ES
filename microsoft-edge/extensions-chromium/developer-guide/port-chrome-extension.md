---
description: Proceso de migración de la extensión Chrome a Microsoft Edge.
title: Extensión de cromo de puerto para Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 0f767107bfb259476d1ab35d081fb9bb05c81b46
ms.sourcegitcommit: e79503c6c53ea9b7de58f8cf1532b5c82116a6eb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/03/2020
ms.locfileid: "11195162"
---
# Migrar la extensión  

Microsoft Edge te permite portar tu extensión de cromo con cambios mínimos.  Las API de extensión y las claves de manifiesto compatibles con Chrome son compatibles con el código de Microsoft Edge.  Para obtener una lista de las API admitidas por Microsoft Edge, ve a [compatibilidad con API][ExtensionApiSupport].  

Para migrar su extensión Chrome, siga los pasos que se indican a continuación.  

1.  Revise las API de extensión de cromo usadas en las extensiones con la lista de [API compatibles][ExtensionApiSupport] con las extensiones de Microsoft Edge.  
    
    > [!NOTE]
    > Si tu extensión usa API que no son compatibles con Microsoft Edge, es posible que no se porten directamente.  
    
1.  Si el nombre `Chrome` se usa en el nombre o la descripción de la extensión, remarca la extensión para `Microsoft Edge` .  Este paso es necesario para aprobar el proceso de certificación.  
1.  Pruebe la extensión para comprobar si funciona en Microsoft Edge mediante la función de prueba de [la extensión][ExtensionsGettingStartedExtensionSideloading].  
1.  Si estás de cara a cualquier problema, puedes depurar las extensiones en Microsoft Edge con el DevTools o [Ponte en contacto con nosotros][mailtoExtensionMicrosoft].  
1.  Siga las [instrucciones de publicación][ExtensionsPublishPublishExtension] para publicar su extensión en el almacén de complementos de Microsoft Edge.  
    
    > [!NOTE]
    > Si la extensión intercambia mensajes con una aplicación nativa mediante la `chrome.runtime.connectNative` API, asegúrese de que `allowed_origins` establece `extension://[Microsoft-Catalog-extensionID]` en el archivo de manifiesto de host de mensajería nativa.  Esto permite que la aplicación identifique la extensión.  
    
## Pasos siguientes  

Una vez que el paquete de extensiones esté listo para publicarse en el almacenamiento de complementos de Microsoft Edge, [crea una cuenta de desarrollador][ExtensionsPublishCreateDevAccount] y [publica la extensión][ExtensionsPublishPublishExtension].  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Compatibilidad con API | Microsoft docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Transferir la extensión | Microsoft docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro para desarrolladores | Microsoft docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publicar la extensión | Microsoft docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagos de pago único | Desarrollador de Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
