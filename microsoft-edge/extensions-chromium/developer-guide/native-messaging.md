---
description: Documentación de mensajería nativa
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 9d33fc4e8c9449d539b6ea82cca87c3aad4d564e
ms.sourcegitcommit: 39636248d0266730089aa2e57b9cf04d9feb363d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088558"
---
# <span data-ttu-id="9faf4-104">Mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="9faf4-104">Native messaging</span></span>  

<span data-ttu-id="9faf4-105">Las extensiones pueden comunicarse con una aplicación Win32 nativa instalada en el dispositivo de un usuario mediante las API de paso de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9faf4-105">Extensions can communicate with a native Win32 application installed on a user’s device using message passing APIs.</span></span> <span data-ttu-id="9faf4-106">El host de aplicaciones nativas puede enviar y recibir mensajes con extensiones que usan la entrada estándar y la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="9faf4-106">The native application host can send and receive messages with extensions using standard input and standard output.</span></span> <span data-ttu-id="9faf4-107">Las extensiones que usan mensajería nativa se instalan en Microsoft Edge de forma similar a cualquier otra extensión.</span><span class="sxs-lookup"><span data-stu-id="9faf4-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span> <span data-ttu-id="9faf4-108">Sin embargo, Microsoft Edge no instala ni administra las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="9faf4-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>

<span data-ttu-id="9faf4-109">Para adquirir la extensión y el host de aplicación nativa, puede hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9faf4-109">To acquire the extension and native application host, you can:</span></span>

1. <span data-ttu-id="9faf4-110">Empaquetar la extensión y el hospedaje juntos.</span><span class="sxs-lookup"><span data-stu-id="9faf4-110">Package the extension and the host together.</span></span> <span data-ttu-id="9faf4-111">Cuando los usuarios instalan el paquete, se instalan la extensión y el host.</span><span class="sxs-lookup"><span data-stu-id="9faf4-111">When users install the package, both the extension and the host are installed.</span></span>
1. <span data-ttu-id="9faf4-112">Instale la extensión desde el [almacén de complementos de Microsoft Edge][EdgeAddons]y pida a los usuarios que instalen el host.</span><span class="sxs-lookup"><span data-stu-id="9faf4-112">Install the extension from the [Microsoft Edge Add-ons store][EdgeAddons], and have your extension prompt users to install the host.</span></span> 

<span data-ttu-id="9faf4-113">Consulte los pasos siguientes para configurar la extensión para enviar y recibir mensajes con hosts de aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="9faf4-113">Refer to the steps below to setup your extension to send and receive messages with native application hosts.</span></span>

### <span data-ttu-id="9faf4-114">Paso 1: agregar permisos al manifiesto de la extensión</span><span class="sxs-lookup"><span data-stu-id="9faf4-114">Step 1: Add permissions to the extension manifest</span></span>

<span data-ttu-id="9faf4-115">Agregue el permiso nativeMessaging a la **manifest.jsde** la extensión.</span><span class="sxs-lookup"><span data-stu-id="9faf4-115">Add the nativeMessaging permission to the extension’s **manifest.json** file.</span></span> <span data-ttu-id="9faf4-116">A continuación se muestra un ejemplo de manifest.jsen:</span><span class="sxs-lookup"><span data-stu-id="9faf4-116">Below is an example of manifest.json:</span></span>

```json
    {
          "name": "Native Messaging Example",
          "version": "1.0",
          "manifest_version": 2, 
          "description": "Send a message to a native application.",
          "app": { 
              "launch": { 
                  "local_path": "main.html" } 
                 }, 
          "icons": { 
              "128": "icon-128.png"}, 
          "permissions": ["nativeMessaging"] 
    }
```

### <span data-ttu-id="9faf4-117">Paso 2: crear el archivo de manifiesto de host de mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="9faf4-117">Step 2: Create your native messaging host manifest file</span></span>
    
<span data-ttu-id="9faf4-118">Las aplicaciones nativas deben proporcionar un archivo de manifiesto de host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="9faf4-118">Native applications must provide a native messaging host manifest file.</span></span> <span data-ttu-id="9faf4-119">Este archivo de manifiesto contiene la ruta de acceso al archivo ejecutable de host de mensajería nativa, el método de comunicación con la extensión y una lista de extensiones permitidas con la que se puede comunicar.</span><span class="sxs-lookup"><span data-stu-id="9faf4-119">This manifest file contains the path to the native messaging host executable, the method of communication with the extension, and a list of allowed extensions it can communicate with.</span></span> <span data-ttu-id="9faf4-120">Los exploradores leen y validan el manifiesto de host de mensajería original, pero nunca lo instala ni administra el explorador.</span><span class="sxs-lookup"><span data-stu-id="9faf4-120">Browsers read and validate the native messaging host manifest, but it’s never installed or managed by the browser.</span></span> <span data-ttu-id="9faf4-121">El archivo de manifiesto de host debe ser un archivo JSON válido que contenga los siguientes campos.</span><span class="sxs-lookup"><span data-stu-id="9faf4-121">The host manifest file must be a valid json file containing the following fields.</span></span>

    
```json
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




| <span data-ttu-id="9faf4-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="9faf4-122">Name</span></span> | <span data-ttu-id="9faf4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="9faf4-123">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="9faf4-124">Nombre del host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="9faf4-124">Name of the native messaging host.</span></span> <span data-ttu-id="9faf4-125">Los clientes pasan esta cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="9faf4-125">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="9faf4-126">Este nombre solo debe contener caracteres alfanuméricos en minúsculas, guiones bajos y puntos.</span><span class="sxs-lookup"><span data-stu-id="9faf4-126">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="9faf4-127">El nombre no debe empezar ni terminar con un punto, y un punto no debe ir seguido de otro punto.</span><span class="sxs-lookup"><span data-stu-id="9faf4-127">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="9faf4-128">Breve descripción de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9faf4-128">Brief description of the application.</span></span> |  
| `path` | <span data-ttu-id="9faf4-129">Ruta de acceso al archivo binario de host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="9faf4-129">Path to the native messaging host binary.</span></span> <span data-ttu-id="9faf4-130">En dispositivos con Windows, puede usar rutas relativas al directorio que contiene el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="9faf4-130">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span> <span data-ttu-id="9faf4-131">En macOS y Linux, la ruta de acceso debe ser absoluta.</span><span class="sxs-lookup"><span data-stu-id="9faf4-131">On macOS and Linux, the path must be absolute.</span></span> <span data-ttu-id="9faf4-132">El proceso de host se inicia con el directorio actual configurado en el directorio que contiene el binario de host.</span><span class="sxs-lookup"><span data-stu-id="9faf4-132">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="9faf4-133">Por ejemplo, si este parámetro se establece en `C:\Application\nm_host.exe` , el binario se inicia con el directorio actual `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="9faf4-133">For example, if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="9faf4-134">Tipo de la interfaz usada para comunicarse con el host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="9faf4-134">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="9faf4-135">Actualmente solo hay un valor posible para este parámetro: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="9faf4-135">Currently there's only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="9faf4-136">Este valor indica que Microsoft Edge debe usarse `stdin` y `stdout` comunicarse con el host.</span><span class="sxs-lookup"><span data-stu-id="9faf4-136">This value indicates that Microsoft Edge should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="9faf4-137">Lista de extensiones que pueden tener acceso al host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="9faf4-137">List of extensions that may have access to the native messaging host.</span></span>  <span data-ttu-id="9faf4-138">Para permitir que la aplicación identifique y se comunique con una extensión, `allowed_origins` establezca `chrome-extension://[Microsoft-Catalog-extensionID]` en el archivo de manifiesto de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="9faf4-138">To enable your application to identify and communicate with an extension, set `allowed_origins` to `chrome-extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  


<span data-ttu-id="9faf4-139">Mientras desarrolla, puede transferir su extensión para probar la mensajería nativa con el host:</span><span class="sxs-lookup"><span data-stu-id="9faf4-139">While developing, you can sideload your extension to test native messaging with the host by:</span></span>
1. <span data-ttu-id="9faf4-140">Navegue a `edge://extensions` y, a continuación, active el botón de alternancia modo de programador.</span><span class="sxs-lookup"><span data-stu-id="9faf4-140">Navigating to `edge://extensions`, and then turning on the Developer mode toggle button.</span></span> 
1. <span data-ttu-id="9faf4-141">Elija cargar Desempaquetado y, a continuación, seleccione el paquete de extensión para transferirlo a la misma.</span><span class="sxs-lookup"><span data-stu-id="9faf4-141">Choose Load unpacked, and then select your extension package to sideload.</span></span>  
1. <span data-ttu-id="9faf4-142">Elige Aceptar.</span><span class="sxs-lookup"><span data-stu-id="9faf4-142">Choose OK.</span></span>
1. <span data-ttu-id="9faf4-143">Compruebe que la `edge://extensions` página ahora incluye su extensión.</span><span class="sxs-lookup"><span data-stu-id="9faf4-143">Verify the `edge://extensions` page now lists your extension.</span></span> 
1. <span data-ttu-id="9faf4-144">Copie la clave desde el identificador de la lista de extensiones de la página.</span><span class="sxs-lookup"><span data-stu-id="9faf4-144">Copy the key from ID from the extension listing on the page.</span></span>

<span data-ttu-id="9faf4-145">Cuando esté listo para distribuir la extensión a los usuarios, publique la extensión en el almacén de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9faf4-145">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span> <span data-ttu-id="9faf4-146">El identificador de extensión de la extensión publicada puede ser diferente al identificador usado durante la transferencia local de la extensión.</span><span class="sxs-lookup"><span data-stu-id="9faf4-146">The extension ID of the published extension may be different to the ID used while sideloading your extension.</span></span> <span data-ttu-id="9faf4-147">Si el identificador ha cambiado, actualiza `allowed_origins` en el archivo de manifiesto de host con el identificador de la extensión publicada.</span><span class="sxs-lookup"><span data-stu-id="9faf4-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span> 



### <span data-ttu-id="9faf4-148">Paso 3: Copie el archivo de manifiesto de host de mensajería nativa en el sistema</span><span class="sxs-lookup"><span data-stu-id="9faf4-148">Step 3: Copy the native messaging host manifest file to your system</span></span>

<span data-ttu-id="9faf4-149">El paso final implica copiar el archivo de manifiesto de host de mensajería nativa en el equipo y asegurarse de que esté configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9faf4-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it’s configured correctly.</span></span> <span data-ttu-id="9faf4-150">Siga los pasos que se indican a continuación para asegurarse de que el archivo de host de mensajería nativo se coloca en la ubicación esperada porque varía según la plataforma.</span><span class="sxs-lookup"><span data-stu-id="9faf4-150">Follow the steps below to ensure the native messaging host file is placed in the expected location because it varies by platform.</span></span>
    
<span data-ttu-id="9faf4-151">**Windows**.</span><span class="sxs-lookup"><span data-stu-id="9faf4-151">**Windows**.</span></span> <span data-ttu-id="9faf4-152">El archivo de manifiesto puede encontrarse en cualquier lugar del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="9faf4-152">The manifest file may be located anywhere in the file system.</span></span> <span data-ttu-id="9faf4-153">El instalador de la aplicación debe crear una clave del registro y establecer el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="9faf4-153">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span> <span data-ttu-id="9faf4-154">Los siguientes comandos son ejemplos de claves de registro.</span><span class="sxs-lookup"><span data-stu-id="9faf4-154">The following commands are examples of registry keys.</span></span>
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="9faf4-155">o</span><span class="sxs-lookup"><span data-stu-id="9faf4-155">or</span></span>  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="9faf4-156">,</span><span class="sxs-lookup"><span data-stu-id="9faf4-156">,</span></span>  
    
<span data-ttu-id="9faf4-157">Ejecute el comando siguiente en un símbolo del sistema para agregar una clave del registro a la carpeta con el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="9faf4-157">Run the following command at a command prompt to add a registry key to the folder with the manifest file.</span></span>
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
<span data-ttu-id="9faf4-158">Como alternativa, copie el comando siguiente en un archivo. reg y ejecútelo para agregar la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="9faf4-158">Alternatively, copy the following command to a .reg file and run it to add the registry key.</span></span> 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  <span data-ttu-id="9faf4-159">Microsoft Edge consulta primero el registro de 32 bits y, a continuación, el registro de 64 bits para identificar los hosts de mensajería nativos.</span><span class="sxs-lookup"><span data-stu-id="9faf4-159">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span> <span data-ttu-id="9faf4-160">Si ejecuta el archivo. reg anterior como parte de una secuencia de comandos por lotes, asegúrese de ejecutarlo con un símbolo del sistema de administrador.</span><span class="sxs-lookup"><span data-stu-id="9faf4-160">If you run the above .reg file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>


<span data-ttu-id="9faf4-161">**MacOS**.</span><span class="sxs-lookup"><span data-stu-id="9faf4-161">**macOS**.</span></span> <span data-ttu-id="9faf4-162">El archivo de manifiesto debe almacenarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9faf4-162">The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="9faf4-163">Los hosts de mensajería instantánea de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.</span><span class="sxs-lookup"><span data-stu-id="9faf4-163">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span> <span data-ttu-id="9faf4-164">Por ejemplo, el archivo de manifiesto debe almacenarse en</span><span class="sxs-lookup"><span data-stu-id="9faf4-164">For example, the manifest file must be stored in</span></span> `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. <span data-ttu-id="9faf4-165">Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el subdirectorio NativeMessagingHosts en el directorio del perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="9faf4-165">User-specific native messaging hosts, which are available to the current user only, are located in the NativeMessagingHosts  subdirectory in the user profile directory.</span></span> <span data-ttu-id="9faf4-166">Por ejemplo, el archivo de manifiesto debe almacenarse en</span><span class="sxs-lookup"><span data-stu-id="9faf4-166">For example, the manifest file must be stored in</span></span>  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    <span data-ttu-id="9faf4-167">Dónde `ChannelName` puede estar, dev o beta.</span><span class="sxs-lookup"><span data-stu-id="9faf4-167">where `ChannelName` may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="9faf4-168">Cuando se usa el canal estable, `ChannelName` no es necesario.</span><span class="sxs-lookup"><span data-stu-id="9faf4-168">When using the Stable channel, `ChannelName` isn't required.</span></span>


<span data-ttu-id="9faf4-169">**Linux** El archivo de manifiesto debe almacenarse de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="9faf4-169">**Linux** The manifest file must be stored as follows:</span></span>

1. <span data-ttu-id="9faf4-170">Hosts de mensajería instantánea en todo el sistema:  `~/.config/microsoft-edge/NativeMessagingHosts`</span><span class="sxs-lookup"><span data-stu-id="9faf4-170">System-wide native messaging hosts:  `~/.config/microsoft-edge/NativeMessagingHosts`</span></span>

1. <span data-ttu-id="9faf4-171">Hosts de mensajería nativa específicos del usuario:  `/etc/opt/edge/native-messaging-hosts`</span><span class="sxs-lookup"><span data-stu-id="9faf4-171">User-specific native messaging hosts:  `/etc/opt/edge/native-messaging-hosts`</span></span>


> [!NOTE]
> <span data-ttu-id="9faf4-172">Asegúrese de que proporciona permisos de lectura en el archivo de manifiesto y ejecute permisos en el ejecutable de host.</span><span class="sxs-lookup"><span data-stu-id="9faf4-172">Ensure that you provide read permissions on the manifest file, and execute permissions on the host executable.</span></span>


> [!NOTE]
> <span data-ttu-id="9faf4-173">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9faf4-173">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9faf4-174">La página original se encuentra [aquí](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="9faf4-174">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9faf4-176">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9faf4-176">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos de Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
