---
description: Proceso de porte de extensión de Chrome a Microsoft Edge
title: Extensión de Puerto Chrome para Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 6be7d788ac22232475e278ae9a5b04de9b6e17f7
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343139"
---
# <span data-ttu-id="55c86-104">Portabilidad de la extensión</span><span class="sxs-lookup"><span data-stu-id="55c86-104">Port your extension</span></span>  

<span data-ttu-id="55c86-105">Microsoft Edge permite portabilidad de la extensión de Chrome con cambios mínimos.</span><span class="sxs-lookup"><span data-stu-id="55c86-105">Microsoft Edge allows you to port your Chrome extension with minimal changes.</span></span>  <span data-ttu-id="55c86-106">Las API de extensión y las claves de manifiesto admitidas por Chrome son compatibles con el código con Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="55c86-106">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="55c86-107">Para obtener una lista de API admitidas por Microsoft Edge, vaya a [Compatibilidad con api][ExtensionApiSupport].</span><span class="sxs-lookup"><span data-stu-id="55c86-107">For a list of APIs supported by Microsoft Edge, navigate to [API support][ExtensionApiSupport].</span></span>  

<span data-ttu-id="55c86-108">Para portabilidad de la extensión de Chrome, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="55c86-108">To port your Chrome extension, complete the following steps.</span></span>  

1.  <span data-ttu-id="55c86-109">Revise las API de extensión de Chrome usadas en las extensiones con la lista Microsoft Edge [de API][ExtensionApiSupport] compatibles con extensiones de Chrome.</span><span class="sxs-lookup"><span data-stu-id="55c86-109">Review the Chrome extension APIs used in your extensions with the Microsoft Edge extensions [supported APIs][ExtensionApiSupport] list.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="55c86-110">Si la extensión usa API que no son compatibles con Microsoft Edge, es posible que no se porte directamente.</span><span class="sxs-lookup"><span data-stu-id="55c86-110">If your extension uses APIs that are not supported by Microsoft Edge, it may not port directly.</span></span>  
    
1.  <span data-ttu-id="55c86-111">En el archivo de manifiesto, establezca el `update_URL` campo en `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .</span><span class="sxs-lookup"><span data-stu-id="55c86-111">In the manifest file, set the `update_URL` field to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="55c86-112">El valor apunta al archivo de la extensión en el almacén de complementos Microsoft Edge y permite Microsoft Edge para buscar actualizaciones `.crx` de extensión.</span><span class="sxs-lookup"><span data-stu-id="55c86-112">The value points to the `.crx` file of your extension in the Microsoft Edge Add-ons store and allows Microsoft Edge to check for extension updates.</span></span>  
1.  <span data-ttu-id="55c86-113">Si se usa en el nombre o la descripción de la extensión, vuelva a cambiar el nombre `Chrome` de la extensión mediante `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="55c86-113">If `Chrome` is used in either the name or the description of your extension, rebrand your extension using `Microsoft Edge`.</span></span>  <span data-ttu-id="55c86-114">Para pasar el proceso de certificación, los cambios son necesarios.</span><span class="sxs-lookup"><span data-stu-id="55c86-114">To pass the certification process, the changes are required.</span></span>  
1.  <span data-ttu-id="55c86-115">Pruebe la extensión para comprobar si funciona en Microsoft Edge la [instalación local de la extensión][ExtensionsGettingStartedExtensionSideloading].</span><span class="sxs-lookup"><span data-stu-id="55c86-115">Test your extension to check if it works in Microsoft Edge by [sideloading your extension][ExtensionsGettingStartedExtensionSideloading].</span></span>  
1.  <span data-ttu-id="55c86-116">Si tiene algún problema, puede depurar las extensiones en Microsoft Edge mediante DevTools o póngase [en contacto con nosotros.][mailtoExtensionMicrosoft]</span><span class="sxs-lookup"><span data-stu-id="55c86-116">If you face any issues, you may debug your extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionMicrosoft].</span></span>  
1.  <span data-ttu-id="55c86-117">Siga las [directrices de publicación][ExtensionsPublishPublishExtension] para publicar la extensión en Microsoft Edge de complementos.</span><span class="sxs-lookup"><span data-stu-id="55c86-117">Follow the [publishing guidelines][ExtensionsPublishPublishExtension] to publish your extension on Microsoft Edge Add-ons store.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="55c86-118">Si la extensión intercambia mensajes con una aplicación nativa mediante , asegúrese de que se establece en en el archivo de manifiesto `chrome.runtime.connectNative` del host de mensajería `allowed_origins` `extension://[Microsoft-Catalog-extensionID]` nativa.</span><span class="sxs-lookup"><span data-stu-id="55c86-118">If your extension exchanges messages with a native app using `chrome.runtime.connectNative`, ensure that you set `allowed_origins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span>  <span data-ttu-id="55c86-119">La configuración permite que la aplicación identifique la extensión.</span><span class="sxs-lookup"><span data-stu-id="55c86-119">The setting allows the app to identify your extension.</span></span>  
    
## <span data-ttu-id="55c86-120">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="55c86-120">Next steps</span></span>  

<span data-ttu-id="55c86-121">Una vez que el paquete de extensión esté listo para publicarse en el almacén de complementos [Microsoft Edge,][ExtensionsPublishCreateDevAccount] cree una cuenta de desarrollador y [publique la extensión][ExtensionsPublishPublishExtension].</span><span class="sxs-lookup"><span data-stu-id="55c86-121">After your extension package is ready to publish in the Microsoft Edge Add-ons store, [create a developer account][ExtensionsPublishCreateDevAccount] and [publish your extension][ExtensionsPublishPublishExtension].</span></span>  

<!-- links -->  

[ExtensionApiSupport]: ./api-support.md "Compatibilidad con API | Microsoft Docs"  
[ExtensionsGettingStartedExtensionSideloading]: ../getting-started/extension-sideloading.md "Instalación local de la extensión | Microsoft Docs"  
[ExtensionsPublishCreateDevAccount]: ../publish/create-dev-account.md "Registro de desarrolladores | Microsoft Docs"  
[ExtensionsPublishPublishExtension]: ../publish/publish-extension.md "Publicar la extensión | Microsoft Docs"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Pagos únicos | Desarrollador de Chrome"  

[mailtoExtensionMicrosoft]: mailto:ext_dev_support@microsoft.com "ext_dev_support@microsoft.com"  
