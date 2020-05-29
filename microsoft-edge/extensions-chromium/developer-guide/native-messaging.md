---
description: Diferencia de mensajería nativa de la documentación de Chrome
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/31/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 0fe45ea681c54ddea7b27a8d954022b8bda45770
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573715"
---
# <span data-ttu-id="aaad3-104">Mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="aaad3-104">Native Messaging</span></span>  

<span data-ttu-id="aaad3-105">Microsoft Edge ahora permite que la extensión instalada desde el catálogo de complementos de Microsoft Edge \ (Microsoft Edge addons \) intercambie mensajes con una aplicación nativa usando las API de paso de mensajes.</span><span class="sxs-lookup"><span data-stu-id="aaad3-105">Microsoft Edge now allows Extension installed from Microsoft Edge Addons catalog \(Microsoft Edge Addons\) to exchange messages with a native application using message passing APIs.</span></span>  <span data-ttu-id="aaad3-106">Para habilitar la característica, debe asegurarse de seguir estos pasos al implementar el host de mensajería nativa de su aplicación nativa.</span><span class="sxs-lookup"><span data-stu-id="aaad3-106">To enable the feature, you need to make sure of following things while implementing native messaging host of your Native Application.</span></span>  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  <span data-ttu-id="aaad3-107">**Host de mensajería nativa**:</span><span class="sxs-lookup"><span data-stu-id="aaad3-107">**Native messaging host**:</span></span>  
    
    <span data-ttu-id="aaad3-108">Para registrar un host de mensajería nativo, la aplicación debe instalar un archivo de manifiesto que defina la configuración de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="aaad3-108">In order to register a native messaging host the application must install a manifest file that defines the native messaging host configuration.</span></span>  <span data-ttu-id="aaad3-109">A continuación se muestra un ejemplo del archivo de manifiesto:</span><span class="sxs-lookup"><span data-stu-id="aaad3-109">Below is an example of the manifest file:</span></span>  
    
    ```xml
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
    ```  
    
<span data-ttu-id="aaad3-110">El archivo de manifiesto de host de mensajería nativa debe ser JSON válido y contiene los siguientes campos:</span><span class="sxs-lookup"><span data-stu-id="aaad3-110">The native messaging host manifest file must be valid JSON and contains the following fields:</span></span>  

| <span data-ttu-id="aaad3-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="aaad3-111">Name</span></span> | <span data-ttu-id="aaad3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="aaad3-112">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="aaad3-113">Nombre del host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="aaad3-113">Name of the native messaging host.</span></span> <span data-ttu-id="aaad3-114">Los clientes pasan esta cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="aaad3-114">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="aaad3-115">Este nombre solo debe contener caracteres alfanuméricos en minúsculas, guiones bajos y puntos.</span><span class="sxs-lookup"><span data-stu-id="aaad3-115">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="aaad3-116">El nombre no debe empezar ni terminar con un punto, y un punto no debe ir seguido de otro punto.</span><span class="sxs-lookup"><span data-stu-id="aaad3-116">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="aaad3-117">Descripción breve de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aaad3-117">Short application description.</span></span> |  
| `path` | <span data-ttu-id="aaad3-118">Ruta de acceso al archivo binario de host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="aaad3-118">Path to the native messaging host binary.</span></span>  <span data-ttu-id="aaad3-119">En Windows, la ruta de acceso puede ser relativa al directorio en el que se encuentra el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="aaad3-119">On Windows, the path may be relative to the directory in which the manifest file is located.</span></span>  <span data-ttu-id="aaad3-120">En macOS, la ruta de acceso debe ser absoluta.</span><span class="sxs-lookup"><span data-stu-id="aaad3-120">On macOS, the path must be absolute.</span></span>  <span data-ttu-id="aaad3-121">El proceso de host se inicia con el directorio actual configurado en el directorio que contiene el binario de host.</span><span class="sxs-lookup"><span data-stu-id="aaad3-121">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="aaad3-122">Por ejemplo, si este parámetro se establece en `C:\Application\nm_host.exe` , el binario se inicia con el directorio actual `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="aaad3-122">For example if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="aaad3-123">Tipo de la interfaz usada para comunicarse con el host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="aaad3-123">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="aaad3-124">Actualmente solo hay un valor posible para este parámetro: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="aaad3-124">Currently there is only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="aaad3-125">Este valor indica que Chrome debe usarse `stdin` y `stdout` comunicarse con el host.</span><span class="sxs-lookup"><span data-stu-id="aaad3-125">This value indicates that Chrome should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="aaad3-126">lista de extensiones que deberían tener acceso al host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="aaad3-126">list of Extension that should access to the native messaging host.</span></span>  <span data-ttu-id="aaad3-127">Para habilitar la aplicación nativa, identifique y comuníquese con la extensión de complementos de Microsoft Edge, establecida `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` en el archivo de manifiesto de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="aaad3-127">To enable your Native Application identify and communicate with Microsoft Edge Addons Extension, set `allowedorigins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  

1.  **<span data-ttu-id="aaad3-128">Ubicación de host de mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="aaad3-128">Native messaging host location</span></span>**  
    
    <span data-ttu-id="aaad3-129">La ubicación del archivo de manifiesto depende de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="aaad3-129">The location of the manifest file depends on the platform.</span></span>  
    
    <span data-ttu-id="aaad3-130">En Windows, el archivo de manifiesto puede encontrarse en cualquier lugar del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="aaad3-130">On Windows, the manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="aaad3-131">El instalador de la aplicación debe crear la clave del registro</span><span class="sxs-lookup"><span data-stu-id="aaad3-131">The application installer must create registry key</span></span>  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="aaad3-132">o</span><span class="sxs-lookup"><span data-stu-id="aaad3-132">or</span></span>  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="aaad3-133">,</span><span class="sxs-lookup"><span data-stu-id="aaad3-133">,</span></span>  
    
    <span data-ttu-id="aaad3-134">y establezca el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="aaad3-134">and set default value of that key to the full path to the manifest file.</span></span>  <span data-ttu-id="aaad3-135">Por ejemplo, con el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="aaad3-135">For example, using the following command:</span></span>  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    <span data-ttu-id="aaad3-136">o mediante el siguiente archivo. reg:</span><span class="sxs-lookup"><span data-stu-id="aaad3-136">or using the following .reg file:</span></span>  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    <span data-ttu-id="aaad3-137">Cuando Microsoft Edge busca hosts de mensajería nativos, se realiza una consulta en primer lugar el registro de 32 bits y, después, el registro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="aaad3-137">When Microsoft Edge looks for native messaging hosts, the 32-bit registry is queried first, then the 64-bit registry.</span></span>  

<span data-ttu-id="aaad3-138">En macOS, los hosts de mensajería nativa de todo el sistema se buscan en una ubicación fija, mientras que los host de mensajería nativa de nivel de usuario se buscan en un subdirectorio del directorio de Perfil de usuario denominado `NativeMessagingHosts` .</span><span class="sxs-lookup"><span data-stu-id="aaad3-138">On macOS, the system-wide native messaging hosts are looked up at a fixed location, while the user-level native messaging hosts are looked up in a subdirectory within the user profile directory called `NativeMessagingHosts`.</span></span>  

<span data-ttu-id="aaad3-139">Microsoft Edge en macOS \ (todo el sistema \):</span><span class="sxs-lookup"><span data-stu-id="aaad3-139">Microsoft Edge on macOS \(system-wide\) :</span></span>  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

<span data-ttu-id="aaad3-140">Microsoft Edge en macOS \ (específica del usuario, ruta de acceso predeterminada \):</span><span class="sxs-lookup"><span data-stu-id="aaad3-140">Microsoft Edge on macOS \(user-specific, default path\):</span></span>  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` <span data-ttu-id="aaad3-141">puede ser Canarias, dev o beta.</span><span class="sxs-lookup"><span data-stu-id="aaad3-141">may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="aaad3-142">Para un canal estable, solo se `Microsoft Edge` debe usar `<ChannelName`>'.</span><span class="sxs-lookup"><span data-stu-id="aaad3-142">For stable channel, only `Microsoft Edge` should be used, `<ChannelName`>\` is not required.</span></span>

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="aaad3-143">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aaad3-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aaad3-144">La página original se encuentra [aquí](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="aaad3-144">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="aaad3-146">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aaad3-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
