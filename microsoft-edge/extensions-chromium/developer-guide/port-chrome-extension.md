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
# <span data-ttu-id="c487a-104">Migrar la extensión</span><span class="sxs-lookup"><span data-stu-id="c487a-104">Port your extension</span></span>  

<span data-ttu-id="c487a-105">Microsoft Edge te permite portar tu extensión de cromo con cambios mínimos.</span><span class="sxs-lookup"><span data-stu-id="c487a-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="c487a-106">Las API de extensión y las claves de manifiesto compatibles con Chrome son compatibles con el código de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c487a-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="c487a-107">Para obtener una lista de las API admitidas por Microsoft Edge, ve a [compatibilidad con API][ExtensionApiSupport].</span><span class="sxs-lookup"><span data-stu-id="c487a-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="c487a-108">Para migrar su extensión Chrome, siga los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="c487a-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="c487a-109">Revise las API de extensión de cromo usadas en las extensiones con la lista de [API compatibles][ExtensionApiSupport] con las extensiones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c487a-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c487a-110">Si tu extensión usa API que no son compatibles con Microsoft Edge, es posible que no se porten directamente.</span><span class="sxs-lookup"><span data-stu-id="c487a-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="c487a-111">Si el nombre `Chrome` se usa en el nombre o la descripción de la extensión, remarca la extensión para `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="c487a-111">If the name `Chrome` is being used in either the name or the description of the extension, rebrand the extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="c487a-112">Este paso es necesario para aprobar el proceso de certificación.</span><span class="sxs-lookup"><span data-stu-id="c487a-112">This step is required to pass the certification process.</span></span>  
1.  <span data-ttu-id="c487a-113">Pruebe la extensión para comprobar si funciona en Microsoft Edge mediante la función de prueba de [la extensión][ExtensionsGettingStartedExtensionSideloading].</span><span class="sxs-lookup"><span data-stu-id="c487a-113">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="c487a-114">Si estás de cara a cualquier problema, puedes depurar las extensiones en Microsoft Edge con el DevTools o [Ponte en contacto con nosotros][mailtoExtensionMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="c487a-114">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="c487a-115">Siga las [instrucciones de publicación][ExtensionsPublishPublishExtension] para publicar su extensión en el almacén de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c487a-115">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="c487a-116">Si la extensión intercambia mensajes con una aplicación nativa mediante la `chrome.runtime.connectNative` API, asegúrese de que `allowed_origins` establece `extension://[Microsoft-Catalog-extensionID]` en el archivo de manifiesto de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="c487a-116">If the extension exchanges messages with a native app using `chrome.runtime.connectNative` API, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="c487a-117">Esto permite que la aplicación identifique la extensión.</span><span class="sxs-lookup"><span data-stu-id="c487a-117">This enables the app to identify the extension.</span></span>  
    
## <span data-ttu-id="c487a-118">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="c487a-118">Next steps</span></span>  

<span data-ttu-id="c487a-119">Una vez que el paquete de extensiones esté listo para publicarse en el almacenamiento de complementos de Microsoft Edge, [crea una cuenta de desarrollador][ExtensionsPublishCreateDevAccount] y [publica la extensión][ExtensionsPublishPublishExtension].</span><span class="sxs-lookup"><span data-stu-id="c487a-119">Once your extension package is ready to be published to Microsoft Edge add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Compatibilidad con API | Microsoft docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Transferir la extensión | Microsoft docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro para desarrolladores | Microsoft docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publicar la extensión | Microsoft docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagos de pago único | Desarrollador de Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
