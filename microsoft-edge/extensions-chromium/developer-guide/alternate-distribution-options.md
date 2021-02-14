---
description: Obtenga información sobre cómo distribuir extensiones mediante métodos alternativos que no usan almacenes comprobados
title: Método alternativo para distribuir extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 9232b8912acaa52c8d97fdd5f13b82ec33c865d4
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327633"
---
# <span data-ttu-id="7cb4d-104">Métodos de distribución de extensión alternativos</span><span class="sxs-lookup"><span data-stu-id="7cb4d-104">Alternate extension distribution methods</span></span>  

<span data-ttu-id="7cb4d-105">Por lo general, las extensiones se distribuyen a través de la tienda de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-105">Generally, extensions are distributed through the Microsoft Edge add-ons store.</span></span> <span data-ttu-id="7cb4d-106">Hay algunos escenarios en los que es posible que los desarrolladores necesiten distribuir extensiones mediante métodos alternativos.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-106">There are some scenarios where developers may need to distribute extensions using alternate methods.</span></span> <span data-ttu-id="7cb4d-107">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7cb4d-107">For example:</span></span>

1.  <span data-ttu-id="7cb4d-108">La extensión está asociada a otro software y debe instalarse junto con el resto del software agrupado.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-108">The extension is associated with other software, and it should be installed together with the rest of the bundled software.</span></span>   
1.  <span data-ttu-id="7cb4d-109">Los administradores de red desean distribuir una extensión en toda la organización.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-109">Network administrators want to distribute an extension throughout their organization.</span></span>   

<span data-ttu-id="7cb4d-110">Las extensiones que no se cargan desde el almacén de complementos perimetrales se denominan extensiones instaladas externamente.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-110">Extensions that are not loaded from the Edge add-ons store are referred to as externally installed extensions.</span></span> <span data-ttu-id="7cb4d-111">En la lista siguiente se proporcionan métodos alternativos para distribuir extensiones instaladas externamente.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-111">The following list provides alternate methods of distributing externally installed extensions.</span></span> 

*   <span data-ttu-id="7cb4d-112">Usa el Registro de Windows (solo Windows).</span><span class="sxs-lookup"><span data-stu-id="7cb4d-112">Use the Windows registry (Windows only).</span></span>  
*   <span data-ttu-id="7cb4d-113">Usa un archivo JSON de preferencias (macOS y Linux).</span><span class="sxs-lookup"><span data-stu-id="7cb4d-113">Use a preferences JSON file (macOS and Linux).</span></span>  
    
## <span data-ttu-id="7cb4d-114">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="7cb4d-114">Before you begin</span></span>  

<span data-ttu-id="7cb4d-115">Asegúrate de publicar la extensión en el almacén de complementos de Microsoft Edge o empaquetar un archivo y asegúrate de que se instala correctamente `.crx` en el equipo.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-115">Ensure that you publish your extension in the Microsoft Edge Add-ons store, or package a `.crx` file and ensure that it installs successfully on your computer.</span></span>  <span data-ttu-id="7cb4d-116">Si instala el archivo mediante el método , asegúrese de que puede navegar a `.crx` la extensión en esa dirección `update_URL` URL.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-116">If you install the `.crx` file using the `update_URL`, ensure you can navigate to your extension at that URL.</span></span>  

<span data-ttu-id="7cb4d-117">Además, asegúrese de que tiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-117">Also, ensure that you have the following information.</span></span>    

1.  <span data-ttu-id="7cb4d-118">La ruta de acceso del `.crx` archivo o `update_URL` la extensión.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-118">The file path of the `.crx` file, or the `update_URL` of your extension.</span></span>
1.  <span data-ttu-id="7cb4d-119">La versión de la extensión.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-119">The version of your extension.</span></span>  <span data-ttu-id="7cb4d-120">La información de versión está disponible en el archivo de manifiesto o en Microsoft Edge después de `edge://extensions` cargar la extensión empaquetada.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-120">The version information is available in your manifest file, or in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>   
1.  <span data-ttu-id="7cb4d-121">El identificador de la extensión.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-121">The ID of your extension.</span></span>  <span data-ttu-id="7cb4d-122">La información del identificador está disponible en Microsoft Edge después `edge://extensions` de cargar la extensión empaquetada.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-122">The ID information is available in Microsoft Edge at `edge://extensions` after you load the packed extension.</span></span>  

> [!NOTE] 
> <span data-ttu-id="7cb4d-123">Los ejemplos siguientes se `1.0` usan como la versión y para el `aaaaaaaaaabbbbbbbbbbcccccccccc` identificador.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-123">The following examples use `1.0` as the version, and `aaaaaaaaaabbbbbbbbbbcccccccccc` for the ID.</span></span>  

## <span data-ttu-id="7cb4d-124">Usar el Registro de Windows (solo Windows)</span><span class="sxs-lookup"><span data-stu-id="7cb4d-124">Use the Windows registry (Windows only)</span></span>  

<span data-ttu-id="7cb4d-125">Para distribuir la extensión mediante el Registro de Windows, realiza los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-125">To distribute your extension using the Windows registry, perform the following steps.</span></span>

1.  <span data-ttu-id="7cb4d-126">Busque o cree la siguiente clave en el Registro:</span><span class="sxs-lookup"><span data-stu-id="7cb4d-126">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="7cb4d-127">Windows de 32 bits:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-127">32-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`.</span></span>  
    *   <span data-ttu-id="7cb4d-128">Windows de 64 bits:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-128">64-bit Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`.</span></span>  
1.  <span data-ttu-id="7cb4d-129">Cree una nueva clave o carpeta en **Extensiones** con el mismo nombre que el identificador de la extensión.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-129">Create a new key, or folder, under **Extensions** with the same name as the ID of your extension.</span></span> <span data-ttu-id="7cb4d-130">Por ejemplo, cree la clave con el nombre `aaaaaaaaaabbbbbbbbbbcccccccccc` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-130">For example, create the key with the name `aaaaaaaaaabbbbbbbbbbcccccccccc`.</span></span>  
1.  <span data-ttu-id="7cb4d-131">En la **clave Extensions,** cree la `update_url` propiedad y establezca el valor en `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-131">In the **Extensions** key, create the `update_url` property, and set the value to `https://edge.microsoft.com/extensionwebstorebase/v1/crx`.</span></span>  <span data-ttu-id="7cb4d-132">La propiedad apunta al archivo de la extensión en el almacén de `update_url` `.crx` complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-132">The `update_url` property points to the `.crx` file of your extension in the Microsoft Edge Add-ons store.</span></span>  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="7cb4d-133">Si desea instalar una extensión de Chrome Web Store, establezca el valor `update_url` en `https://clients2.google.com/service/update2/crx` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-133">If you want to install an extension from the Chrome Web Store, set the value of `update_url` to `https://clients2.google.com/service/update2/crx`.</span></span>  
  
1.  <span data-ttu-id="7cb4d-134">Para comprobar que la extensión aparece en Microsoft Edge, vaya a `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-134">Verify that your extension is listed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="7cb4d-135">Usar un archivo JSON de preferencias (macOS y Linux)</span><span class="sxs-lookup"><span data-stu-id="7cb4d-135">Use a preferences JSON file (macOS and Linux)</span></span>  

<span data-ttu-id="7cb4d-136">Para distribuir la extensión mediante un archivo JSON de preferencias, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-136">To distribute your extension using a preferences JSON file, perform the following steps.</span></span>

1.  <span data-ttu-id="7cb4d-137">Al usar Linux, asegúrate de que el archivo de extensión esté disponible en el equipo en el que `.crx` se instalará la extensión.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-137">When using Linux, ensure your `.crx` extension file is available on the machine that the extension will be installed on.</span></span> <span data-ttu-id="7cb4d-138">Copia el archivo de extensión en un directorio local o usa un recurso compartido de red al que se `.crx` pueda acceder desde el equipo.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-138">Copy the `.crx` extension file to a local directory, or use a  network share that is reachable from the machine.</span></span> 
1.  <span data-ttu-id="7cb4d-139">Cree un archivo JSON donde el nombre del archivo se corresponda con el identificador de la extensión.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-139">Create a JSON file where the name of the file corresponds to the ID of your extension.</span></span> <span data-ttu-id="7cb4d-140">Por ejemplo, cree un archivo JSON con el nombre de archivo `aaaaaaaaaabbbbbbbbbbcccccccccc.json` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-140">For example, create a JSON file with the file name `aaaaaaaaaabbbbbbbbbbcccccccccc.json`.</span></span>  
1.  <span data-ttu-id="7cb4d-141">Según el sistema operativo, guarde el archivo JSON en una de las carpetas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-141">Depending on your operating system, save the JSON file to one of the following folders.</span></span>   
    *   **<span data-ttu-id="7cb4d-142">macOS</span><span class="sxs-lookup"><span data-stu-id="7cb4d-142">macOS</span></span>**  
        *   <span data-ttu-id="7cb4d-143">Específico del usuario:</span><span class="sxs-lookup"><span data-stu-id="7cb4d-143">User specific:</span></span> `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   <span data-ttu-id="7cb4d-144">Todos los usuarios:</span><span class="sxs-lookup"><span data-stu-id="7cb4d-144">All users:</span></span> `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        <span data-ttu-id="7cb4d-145">Para evitar que los usuarios no autorizados instalen extensiones para todos los usuarios, asegúrese de que el archivo de extensión sea de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-145">To prevent unauthorized users from installing extensions for all users, ensure your extension file is read only.</span></span> <span data-ttu-id="7cb4d-146">Además, asegúrese de que se cumplen las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="7cb4d-146">Additionally, ensure that the following conditions are met:</span></span>
        
        *   <span data-ttu-id="7cb4d-147">Todos los directorios de la ruta de acceso pertenecen a la raíz del usuario.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-147">Every directory in the path is owned by the user root.</span></span>  
        *   <span data-ttu-id="7cb4d-148">Todos los directorios de la ruta de acceso se asignan al `admin` grupo `wheel` o al grupo.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-148">Every directory in the path is assigned to the `admin` or `wheel` group.</span></span>  
        *   <span data-ttu-id="7cb4d-149">Todos los directorios de la ruta de acceso no se pueden escribir en el mundo.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-149">Every directory in the path isn't world writable.</span></span>  
        *   <span data-ttu-id="7cb4d-150">La ruta de acceso también debe estar libre de vínculos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-150">The path must also be free of symbolic links.</span></span>  
        
    *   **<span data-ttu-id="7cb4d-151">Linux</span><span class="sxs-lookup"><span data-stu-id="7cb4d-151">Linux</span></span>**  
        *   <span data-ttu-id="7cb4d-152">Específico del usuario:</span><span class="sxs-lookup"><span data-stu-id="7cb4d-152">User specific:</span></span> `~/.config/microsoft-edge/External Extensions/`  
        *   <span data-ttu-id="7cb4d-153">Todos los usuarios:</span><span class="sxs-lookup"><span data-stu-id="7cb4d-153">All users:</span></span> `/usr/share/microsoft-edge/extensions/`  
1.  <span data-ttu-id="7cb4d-154">En función de su escenario, copie el código adecuado que se muestra a continuación en el archivo JSON.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-154">Depending on your scenario, copy the appropriate code that follows to your JSON file.</span></span> 
    *   <span data-ttu-id="7cb4d-155">Solo se aplica a Linux.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-155">Applies to Linux only.</span></span> <span data-ttu-id="7cb4d-156">Si instala desde un archivo, especifique la ubicación y la versión con `external_crx` y `external_version` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-156">If you install from a file, specify the location and version using `external_crx` and `external_version`.</span></span>  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   <span data-ttu-id="7cb4d-157">Se aplica a macOS y Linux.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-157">Applies to macOS and Linux.</span></span> <span data-ttu-id="7cb4d-158">Si instala desde una `update_URL` dirección URL de actualización, especifique la dirección URL de actualización mediante `external_update_url` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-158">If you install from an `update_URL`, specify the update URL using `external_update_url`.</span></span> 
        
        <span data-ttu-id="7cb4d-159">Copie el siguiente código en el archivo JSON al instalar desde `.crx` archivos locales solo en Linux.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-159">Copy the following code to your JSON file when installing from local `.crx` files on Linux only.</span></span>  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  <span data-ttu-id="7cb4d-160">Copia el siguiente código en el archivo JSON al instalar desde el almacén de complementos de Microsoft Edge en macOS y Linux.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-160">Copy the following code to your JSON file when installing from the Microsoft Edge add-ons store on macOS and Linux.</span></span>
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  <span data-ttu-id="7cb4d-161">Para instalar extensiones para configuraciones regionales específicas, enume las configuraciones regionales admitidas mediante `supported_locale` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-161">To install extensions for specific locales, list the supported locales using `supported_locale`.</span></span>  <span data-ttu-id="7cb4d-162">También puede especificar configuraciones regionales primarias para instalar la extensión para todas las configuraciones regionales de idioma que usan ese elemento primario.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-162">You may also specify parent locales to install your extension for all language locales that use that parent.</span></span> <span data-ttu-id="7cb4d-163">Por ejemplo, al usar la configuración regional primaria, la extensión se instala para todas las configuraciones regionales en inglés, como `en` `en-US` , y así `en-GB` sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-163">For example, when using the parent locale `en`, your extension installs for all English locales, such as `en-US`, `en-GB`, and so on.</span></span>  <span data-ttu-id="7cb4d-164">Cuando los usuarios cambian su configuración regional en el explorador, se desinstalan las extensiones instaladas externamente.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-164">When users change their locale in their browser, externally installed extensions are uninstalled.</span></span>  <span data-ttu-id="7cb4d-165">Para instalar la extensión para cualquier configuración regional, no use `supported_locales` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-165">To install your extension for any locale, do not use `supported_locales`.</span></span>  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  <span data-ttu-id="7cb4d-166">Para comprobar que la extensión está instalada en Microsoft Edge, vaya a `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="7cb4d-166">Verify that your extension is installed in Microsoft Edge by navigating to `edge://extensions`.</span></span>  

## <span data-ttu-id="7cb4d-167">Actualizar y desinstalar extensiones instaladas externamente</span><span class="sxs-lookup"><span data-stu-id="7cb4d-167">Update and uninstall externally installed extensions</span></span>

<span data-ttu-id="7cb4d-168">Microsoft Edge examina las entradas de metadatos en el Registro cada vez que se inicia el explorador y realiza cualquier cambio en las extensiones instaladas externamente.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-168">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any changes to the externally installed extensions.</span></span>  

<span data-ttu-id="7cb4d-169">Para actualizar la extensión a una nueva versión, actualice la versión en el archivo de manifiesto y, a continuación, actualice la versión en el Registro.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-169">To update your extension to a new version, update the version in the manifest file, and then update the version in the registry.</span></span>  

<span data-ttu-id="7cb4d-170">Es posible que deba desinstalar extensiones instaladas externamente, que se instalaron como parte de una agrupación de software que se instaló anteriormente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-170">You may need to uninstall externally installed extensions, which were installed as part of a bundle of software that was previously installed on the machine.</span></span>  <span data-ttu-id="7cb4d-171">Para desinstalar la extensión, quite el archivo JSON de preferencias o quite la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="7cb4d-171">To uninstall your extension, remove your preferences JSON file or remove the key from the registry.</span></span>   

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="7cb4d-172">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7cb4d-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  <span data-ttu-id="7cb4d-173">La página original se encuentra [aquí.](https://developer.chrome.com/apps/external_extensions)</span><span class="sxs-lookup"><span data-stu-id="7cb4d-173">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7cb4d-175">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7cb4d-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
