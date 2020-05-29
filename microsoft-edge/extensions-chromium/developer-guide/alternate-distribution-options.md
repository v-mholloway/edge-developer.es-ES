---
description: El proceso de distribuir la extensión por mecanismo que no sean almacenes verificados
title: Método alternativo de distribuir la extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: a1a3ffe7a54f96df7e665ab5dc6f5b99bacb8b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573719"
---
# <span data-ttu-id="a7529-104">Método alternativo de distribuir la extensión</span><span class="sxs-lookup"><span data-stu-id="a7529-104">Alternate Method of Distributing Extension</span></span>  

<span data-ttu-id="a7529-105">Si es un desarrollador que desea distribuir una extensión como parte del proceso de instalación de otro software o un administrador de red que desea distribuir una extensión en su organización, Microsoft Edge admite los siguientes métodos de instalación de extensiones:</span><span class="sxs-lookup"><span data-stu-id="a7529-105">If you are a developer who wants to distribute an Extension as part of the installation process for other software, or a network admin that want to distribute an Extension throughout their organization, Microsoft Edge supports the following Extension installation methods:</span></span>  

*   **<span data-ttu-id="a7529-106">Usar el registro de Windows \ (solo para Windows \)</span><span class="sxs-lookup"><span data-stu-id="a7529-106">Using the Windows registry \(Windows only\)</span></span>**  

<span data-ttu-id="a7529-107">Microsoft Edge admite la instalación de una extensión hospedada en un `update_URL` .</span><span class="sxs-lookup"><span data-stu-id="a7529-107">Microsoft Edge supports installing an Extension hosted at an `update_URL`.</span></span>  <span data-ttu-id="a7529-108">En Windows, el `update_URL` debe apuntar al catálogo de complementos de Microsoft Edge \ (Microsoft Edge addons \) donde se debe hospedar la extensión.</span><span class="sxs-lookup"><span data-stu-id="a7529-108">On Windows, the `update_URL` must point to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\) where the Extension must be hosted.</span></span>  

> [!NOTE]
> <span data-ttu-id="a7529-109">Instalación externa de extensión a través de un archivo JSON de preferencias para macOS</span><span class="sxs-lookup"><span data-stu-id="a7529-109">External installation of Extension via a preferences json file for macOS</span></span> <!--and Linux--> <span data-ttu-id="a7529-110">aún no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="a7529-110">are not supported yet.</span></span>  <span data-ttu-id="a7529-111">Esta asistencia de características estará disponible próximamente.</span><span class="sxs-lookup"><span data-stu-id="a7529-111">This feature support will soon be available.</span></span>

## <span data-ttu-id="a7529-112">Usar el registro de Windows</span><span class="sxs-lookup"><span data-stu-id="a7529-112">Using the Windows registry</span></span>  

<span data-ttu-id="a7529-113">En primer lugar, publique la extensión en los complementos de Microsoft Edge o empaquete un archivo. CRX y asegúrese de que se instale correctamente.</span><span class="sxs-lookup"><span data-stu-id="a7529-113">First, publish the Extension in the Microsoft Edge Addons, or package a .crx file and make sure that it installs successfully.</span></span>  

<span data-ttu-id="a7529-114">Los pasos para instalar la extensión a través del registro en Windows son:</span><span class="sxs-lookup"><span data-stu-id="a7529-114">The steps to install Extension via registry in windows are:</span></span>  

*   <span data-ttu-id="a7529-115">Busque o cree la siguiente clave en el registro:</span><span class="sxs-lookup"><span data-stu-id="a7529-115">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="a7529-116">Windows de 32 bits:</span><span class="sxs-lookup"><span data-stu-id="a7529-116">32-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   <span data-ttu-id="a7529-117">Windows de 64 bits:</span><span class="sxs-lookup"><span data-stu-id="a7529-117">64-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   <span data-ttu-id="a7529-118">Cree una nueva clave \ (carpeta \) en la clave Extensions con el mismo nombre que el identificador de la extensión \ (por ejemplo, `aaaaaaaaaabbbbbbbbbbcccccccccc` \).</span><span class="sxs-lookup"><span data-stu-id="a7529-118">Create a new key \(folder\) under the Extensions key with the same name as the ID of your Extension \(for example, `aaaaaaaaaabbbbbbbbbbcccccccccc`\).</span></span>  
*   <span data-ttu-id="a7529-119">En su clave de extensión, cree una propiedad, `update_url` y establezca su valor en el valor: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (esto apunta al CRX de su extensión en los complementos de Microsoft Edge \).</span><span class="sxs-lookup"><span data-stu-id="a7529-119">In your Extension key, create a property, `update_url`, and set it to the value: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`,  \(this points to the crx of your extension in the Microsoft Edge Addons\).</span></span> <span data-ttu-id="a7529-120">Si desea instalar una extensión desde la tienda web de Chrome, proporcione la dirección URL de la actualización de la tienda web de Chrome `https://clients2.google.com/service/update2/crx` .</span><span class="sxs-lookup"><span data-stu-id="a7529-120">If you want to install an extension from the Chrome Web Store, please provide the Chrome Web Store update URL, `https://clients2.google.com/service/update2/crx`.</span></span>  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   <span data-ttu-id="a7529-121">Inicia el explorador y ve a `edge://extensions` ; deberás ver la extensión.</span><span class="sxs-lookup"><span data-stu-id="a7529-121">Launch the browser and go to `edge://extensions`; you should see the extension listed.</span></span>  

## <span data-ttu-id="a7529-122">Actualizar y desinstalar</span><span class="sxs-lookup"><span data-stu-id="a7529-122">Updating and uninstalling</span></span>  

<span data-ttu-id="a7529-123">Microsoft Edge examina las entradas de metadatos del registro cada vez que se inicia el explorador y realiza los cambios necesarios en las extensiones externas instaladas.</span><span class="sxs-lookup"><span data-stu-id="a7529-123">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any necessary changes to the installed external extensions.</span></span>  

<span data-ttu-id="a7529-124">Para actualizar la extensión a una nueva versión, actualice el archivo y, a continuación, actualice la versión en el registro.</span><span class="sxs-lookup"><span data-stu-id="a7529-124">To update your extension to a new version, update the file, and then update the version in the registry.</span></span>  

<span data-ttu-id="a7529-125">Para desinstalar la extensión \ (por ejemplo, si se desinstala el software \), quite el archivo de preferencias \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) o los metadatos del registro.</span><span class="sxs-lookup"><span data-stu-id="a7529-125">To uninstall your extension \(for example, if your software is uninstalled\), remove your preference file \(`aaaaaaaaaabbbbbbbbbbcccccccccc.json`\) or the metadata from the registry.</span></span>  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="a7529-126">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a7529-126">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a7529-127">La página original se encuentra [aquí](https://developer.chrome.com/apps/external_extensions).</span><span class="sxs-lookup"><span data-stu-id="a7529-127">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a7529-129">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a7529-129">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
