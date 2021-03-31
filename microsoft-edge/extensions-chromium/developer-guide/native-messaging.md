---
description: Documentación de mensajería nativa
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: d9c2370d6a4f9f7cd25001c1c58ce266423af19a
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343069"
---
# <span data-ttu-id="7c1bd-104">Mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="7c1bd-104">Native messaging</span></span>  

<span data-ttu-id="7c1bd-105">Las extensiones se comunican con una aplicación nativa de Win32 instalada en el dispositivo de un usuario mediante las API de paso de mensajes.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="7c1bd-106">El host de la aplicación nativa envía y recibe mensajes con extensiones mediante la entrada estándar y la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="7c1bd-107">Las extensiones que usan mensajería nativa se instalan en Microsoft Edge de forma similar a cualquier otra extensión.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="7c1bd-108">Sin embargo, Microsoft Edge no instala ni administra las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="7c1bd-109">Para adquirir la extensión y el host de la aplicación nativa, tiene dos modelos de distribución.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="7c1bd-110">Empaquetar la extensión y el host juntos.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-110">Package your extension and the host together.</span></span>  <span data-ttu-id="7c1bd-111">Cuando un usuario instala el paquete, se instalan tanto la extensión como el host.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="7c1bd-112">Instale la extensión con el almacén de complementos de [Microsoft Edge] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]y la extensión pedirá a los usuarios que instalen el host.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-112">Install your extension using the [Microsoft Edge Add-ons store] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="7c1bd-113">Para crear la extensión para enviar y recibir mensajes con hosts de aplicaciones nativas, consulte los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="7c1bd-114">Paso 1: Agregar permisos al manifiesto de extensión</span><span class="sxs-lookup"><span data-stu-id="7c1bd-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="7c1bd-115">Agregue el `nativeMessaging` permiso al archivomanifest.js archivo de la extensión.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="7c1bd-116">El siguiente fragmento de código es un ejemplo demanifest.js en.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-116">The following code snippet is an example of **manifest.json**.</span></span>  

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

## <span data-ttu-id="7c1bd-117">Paso 2: Crear el archivo de manifiesto del host de mensajería nativo</span><span class="sxs-lookup"><span data-stu-id="7c1bd-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="7c1bd-118">Las aplicaciones nativas deben proporcionar un archivo de manifiesto de host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="7c1bd-119">El archivo de manifiesto contiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="7c1bd-120">La ruta de acceso al tiempo de ejecución del host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="7c1bd-121">El método de comunicación con la extensión.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="7c1bd-122">Una lista de extensiones permitidas a las que se comunica.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="7c1bd-123">El explorador lee y valida el manifiesto del host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="7c1bd-124">El explorador no instala ni administra el archivo de manifiesto del host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

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

<span data-ttu-id="7c1bd-125">El archivo de manifiesto de host debe ser un archivo JSON válido que contenga las siguientes claves.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7c1bd-126">Especifica el nombre del host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-126">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="7c1bd-127">Los clientes pasan esta cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="7c1bd-127">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="7c1bd-128">Este valor solo debe contener caracteres alfanuméricos en minúsculas, caracteres de subrayado y puntos.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-128">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="7c1bd-129">Este valor no debe comenzar ni terminar con un punto, y un punto no debe ir seguido de otro punto.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-129">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7c1bd-130">Describe la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-130">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7c1bd-131">Especifica la ruta de acceso al binario del host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-131">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="7c1bd-132">En dispositivos Windows, puedes usar rutas de acceso relativas al directorio que contiene el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-132">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="7c1bd-133">En macOS y Linux, la ruta de acceso debe ser absoluta.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-133">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="7c1bd-134">El proceso de host comienza con el directorio actual establecido en el directorio que contiene el binario de host.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-134">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="7c1bd-135">Por ejemplo \(Windows\), si este parámetro se establece en , el binario se inicia con `C:\Application\nm_host.exe` el directorio actual \( `C:\Application\` \).</span><span class="sxs-lookup"><span data-stu-id="7c1bd-135">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7c1bd-136">Especifica el tipo de interfaz que se usa para comunicarse con el host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-136">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="7c1bd-137">Este valor indica a Microsoft Edge que use `stdin` y se comunique con el `stdout` host.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-137">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="7c1bd-138">El único valor aceptable es `stdio` .</span><span class="sxs-lookup"><span data-stu-id="7c1bd-138">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="7c1bd-139">Especifica la lista de extensiones que tienen acceso al host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-139">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="7c1bd-140">Para permitir que la aplicación identifique y se comunique con una extensión, en el archivo de manifiesto del host de mensajería nativo, establezca el siguiente valor.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-140">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="7c1bd-141">Realizar una instalación de prueba de la extensión para probar la mensajería nativa con el host.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-141">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="7c1bd-142">Para realizar una instalación de instalación de instalación local de la extensión durante el desarrollo y `microsoft_catalog_extension_id` recuperarla, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-142">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="7c1bd-143">Navegue hasta `edge://extensions` y, a continuación, active el botón de alternancia del modo de desarrollador.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-143">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="7c1bd-144">Elija **Cargar desempaquetar**y, a continuación, seleccione el paquete de extensión para la instalación de prueba.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-144">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="7c1bd-145">Elige **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-145">Choose **OK**.</span></span>  
1.  <span data-ttu-id="7c1bd-146">Vaya a `edge://extensions` la página y compruebe que la extensión aparece en la lista.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-146">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="7c1bd-147">Copia la clave `microsoft_catalog_extension_id` de \(ID\) de la lista de extensiones de la página.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-147">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  

<span data-ttu-id="7c1bd-148">Cuando estés listo para distribuir la extensión a los usuarios, publica la extensión en la tienda de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-148">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="7c1bd-149">El identificador de extensión de la extensión publicada puede ser diferente del identificador usado al cargar localmente la extensión.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-149">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="7c1bd-150">Si el identificador ha cambiado, actualice `allowed_origins` el archivo de manifiesto de host con el identificador de la extensión publicada.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-150">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="7c1bd-151">Paso 3: Copiar el archivo de manifiesto del host de mensajería nativa en el sistema</span><span class="sxs-lookup"><span data-stu-id="7c1bd-151">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="7c1bd-152">El paso final implica copiar el archivo de manifiesto del host de mensajería nativa en el equipo y asegurarse de que el archivo de manifiesto está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-152">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="7c1bd-153">Para asegurarse de que el archivo de manifiesto se coloca en la ubicación esperada, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-153">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="7c1bd-154">La ubicación varía según la plataforma.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-154">The location varies by platform.</span></span>  

### [<span data-ttu-id="7c1bd-155">Windows</span><span class="sxs-lookup"><span data-stu-id="7c1bd-155">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="7c1bd-156">El archivo de manifiesto puede estar ubicado en cualquier parte del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-156">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="7c1bd-157">El instalador de la aplicación debe crear una clave del Registro y establecer el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-157">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="7c1bd-158">Los siguientes comandos son ejemplos de claves del Registro.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-158">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="7c1bd-159">Para agregar una clave del Registro al directorio con la clave de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-159">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="7c1bd-160">Ejecute el comando en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-160">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="7c1bd-161">Ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-161">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="7c1bd-162">Cree un `.reg` archivo y ejecutarlo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-162">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="7c1bd-163">Copie el siguiente comando en un `.reg` archivo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-163">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="7c1bd-164">Ejecute el `.reg` archivo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-164">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="7c1bd-165">Microsoft Edge consulta la `HKEY_CURRENT_USER` clave raíz seguida de `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="7c1bd-165">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="7c1bd-166">En ambas claves, primero se busca en el Registro de 32 bits y, a continuación, se busca en el Registro de 64 bits para identificar hosts de mensajería nativos.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-166">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="7c1bd-167">La clave del Registro especifica la ubicación del manifiesto del host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-167">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="7c1bd-168">Si Microsoft Edge encuentra la clave del Registro en cualquiera de las ubicaciones enumeradas anteriormente, no consulta las ubicaciones que aparecen en este párrafo.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-168">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in this paragraph.</span></span>  <span data-ttu-id="7c1bd-169">Si ejecuta el archivo anterior como parte de un script por lotes, asegúrese de `.reg` ejecutarlo mediante un símbolo del sistema de administrador.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-169">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="7c1bd-170">macOS</span><span class="sxs-lookup"><span data-stu-id="7c1bd-170">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="7c1bd-171">Para almacenar el archivo de manifiesto, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-171">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="7c1bd-172">Los hosts de mensajería nativa de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-172">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="7c1bd-173">Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-173">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="7c1bd-174">Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio de perfiles de usuario.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-174">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="7c1bd-175">Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-175">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="7c1bd-176">La  `{Channel_Name}` entrada debe ser uno de los siguientes `Microsoft Edge {Channel_Name}` valores.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-176">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="7c1bd-177">Canary</span><span class="sxs-lookup"><span data-stu-id="7c1bd-177">Canary</span></span>  
    *   <span data-ttu-id="7c1bd-178">Dev</span><span class="sxs-lookup"><span data-stu-id="7c1bd-178">Dev</span></span>  
    *   <span data-ttu-id="7c1bd-179">Beta</span><span class="sxs-lookup"><span data-stu-id="7c1bd-179">Beta</span></span>  

    <span data-ttu-id="7c1bd-180">Cuando se usa el canal estable, `{Channel_Name}` no es necesario.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-180">When using the Stable channel, `{Channel_Name}` isn't required.</span></span>  

### [<span data-ttu-id="7c1bd-181">Linux</span><span class="sxs-lookup"><span data-stu-id="7c1bd-181">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="7c1bd-182">Para almacenar el archivo de manifiesto, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-182">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="7c1bd-183">Los hosts de mensajería nativa de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-183">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="7c1bd-184">El archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-184">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="7c1bd-185">Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio de perfiles de usuario.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-185">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="7c1bd-186">El archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-186">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="7c1bd-187">Asegúrese de proporcionar permisos de lectura en el archivo de manifiesto y de ejecutar permisos en el tiempo de ejecución del host.</span><span class="sxs-lookup"><span data-stu-id="7c1bd-187">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  


 [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos de Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="7c1bd-189">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7c1bd-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7c1bd-190">La página original se encuentra [aquí.](https://developer.chrome.com/extensions/nativeMessaging)</span><span class="sxs-lookup"><span data-stu-id="7c1bd-190">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7c1bd-192">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7c1bd-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
