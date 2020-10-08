---
description: Documentación de mensajería nativa
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/06/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: c5da9acf79225c88ad5829c2b7f57d1d833ca49b
ms.sourcegitcommit: 75c200a029d19fe372c1505c0006dbfbfad90bf5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "11100255"
---
# <span data-ttu-id="83dcf-104">Mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="83dcf-104">Native messaging</span></span>  

<span data-ttu-id="83dcf-105">Las extensiones se comunican con una aplicación Win32 nativa instalada en el dispositivo de un usuario mediante las API de paso de mensajes.</span><span class="sxs-lookup"><span data-stu-id="83dcf-105">Extensions communicate with a native Win32 application installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="83dcf-106">El anfitrión de la aplicación nativa envía y recibe mensajes con extensiones que usan la entrada estándar y la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="83dcf-106">The native application host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="83dcf-107">Las extensiones que usan mensajería nativa se instalan en Microsoft Edge de forma similar a cualquier otra extensión.</span><span class="sxs-lookup"><span data-stu-id="83dcf-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="83dcf-108">Sin embargo, Microsoft Edge no instala ni administra las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="83dcf-108">However, native applications are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="83dcf-109">Para adquirir la extensión y el host de aplicaciones nativas, tiene dos modelos de distribución.</span><span class="sxs-lookup"><span data-stu-id="83dcf-109">To acquire the extension and native application host, you have two distribution models.</span></span>  

*   <span data-ttu-id="83dcf-110">Empaquete la extensión y el hospedaje juntos.</span><span class="sxs-lookup"><span data-stu-id="83dcf-110">Package your extension and the host together.</span></span>  <span data-ttu-id="83dcf-111">Cuando un usuario instala el paquete, se instalan tanto la extensión como el host.</span><span class="sxs-lookup"><span data-stu-id="83dcf-111">When a user installs the package, both the extension and the host are installed.</span></span>
*   <span data-ttu-id="83dcf-112">Instale la extensión con el [almacén de complementos de Microsoft Edge][EdgeAddons]y su extensión pide a los usuarios que instalen el host.</span><span class="sxs-lookup"><span data-stu-id="83dcf-112">Install your extension using the [Microsoft Edge Add-ons store][EdgeAddons], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="83dcf-113">Para crear su extensión para enviar y recibir mensajes con hosts de aplicaciones nativas, consulte los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="83dcf-113">To create your extension to send and receive messages with native application hosts, refer to the following steps.</span></span>  

## <span data-ttu-id="83dcf-114">Paso 1: agregar permisos al manifiesto de la extensión</span><span class="sxs-lookup"><span data-stu-id="83dcf-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="83dcf-115">Agregue el `nativeMessaging` permiso al **manifest.jsen** el archivo de la extensión.</span><span class="sxs-lookup"><span data-stu-id="83dcf-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="83dcf-116">El siguiente fragmento de código es un ejemplo de **manifest.js**.</span><span class="sxs-lookup"><span data-stu-id="83dcf-116">The following code snippet is an example of **manifest.json**.</span></span>  

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

## <span data-ttu-id="83dcf-117">Paso 2: crear el archivo de manifiesto de host de mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="83dcf-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="83dcf-118">Las aplicaciones nativas deben proporcionar un archivo de manifiesto de host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-118">Native applications must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="83dcf-119">El archivo de manifiesto contiene la ruta de acceso al motor de tiempo de ejecución de mensajería nativa, el método de comunicación con la extensión y una lista de extensiones permitidas a las que se comunica.</span><span class="sxs-lookup"><span data-stu-id="83dcf-119">The manifest file contains the path to the native messaging host runtime, the method of communication with the extension, and a list of allowed extensions to which it communicates.</span></span>  <span data-ttu-id="83dcf-120">El explorador Lee y valida el manifiesto de host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-120">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="83dcf-121">El explorador no instala ni administra el archivo de manifiesto de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="83dcf-121">The browser does not install or manage the native messaging host manifest file.</span></span>  

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

<span data-ttu-id="83dcf-122">El archivo de manifiesto de host debe ser un archivo JSON válido que contenga las siguientes claves.</span><span class="sxs-lookup"><span data-stu-id="83dcf-122">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="83dcf-123">Especifica el nombre del host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-123">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="83dcf-124">Los clientes pasan esta cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="83dcf-124">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="83dcf-125">Este valor solo debe contener caracteres alfanuméricos en minúsculas, guiones bajos y puntos.</span><span class="sxs-lookup"><span data-stu-id="83dcf-125">This value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="83dcf-126">Este valor no debe comenzar ni terminar con un punto, y un punto no debe ir seguido de otro punto.</span><span class="sxs-lookup"><span data-stu-id="83dcf-126">This value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="83dcf-127">Describe la aplicación.</span><span class="sxs-lookup"><span data-stu-id="83dcf-127">Describes the application.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="83dcf-128">Especifica la ruta de acceso al archivo binario de host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-128">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="83dcf-129">En dispositivos con Windows, puede usar rutas relativas al directorio que contiene el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="83dcf-129">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="83dcf-130">En macOS y Linux, la ruta de acceso debe ser absoluta.</span><span class="sxs-lookup"><span data-stu-id="83dcf-130">On macOS and Linux, the path must be absolute.</span></span>  
      
      <span data-ttu-id="83dcf-131">El proceso de hospedaje se inicia con el directorio actual configurado en el directorio que contiene el binario de host.</span><span class="sxs-lookup"><span data-stu-id="83dcf-131">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="83dcf-132">Por ejemplo \ (Windows \), si este parámetro se establece en `C:\Application\nm_host.exe` , el binario se inicia con el directorio actual \ ( `C:\Application\` \).</span><span class="sxs-lookup"><span data-stu-id="83dcf-132">For example \(Windows\), if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory \(`C:\Application\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="83dcf-133">Especifica el tipo de la interfaz usada para comunicarse con el host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-133">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="83dcf-134">Este valor indica a Microsoft Edge que use `stdin` y `stdout` se comunique con el host.</span><span class="sxs-lookup"><span data-stu-id="83dcf-134">This value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="83dcf-135">El único valor aceptable es `stdio` .</span><span class="sxs-lookup"><span data-stu-id="83dcf-135">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="83dcf-136">Especifica la lista de extensiones que tienen acceso al host de mensajería nativo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-136">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="83dcf-137">Para permitir que la aplicación identifique y se comunique con una extensión, en el archivo de manifiesto del host de mensajería nativa, establezca el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="83dcf-137">To enable your application to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="83dcf-138">Transfiera localmente su extensión para probar la mensajería nativa con el host.</span><span class="sxs-lookup"><span data-stu-id="83dcf-138">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="83dcf-139">Para transferir su extensión durante el desarrollo y recuperar `microsoft_catalog_extension_id` , complete los siguientes pasos.</span><span class="sxs-lookup"><span data-stu-id="83dcf-139">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following steps.</span></span>  

1.  <span data-ttu-id="83dcf-140">Vaya a `edge://extensions` y, a continuación, active el botón de alternancia modo de programador.</span><span class="sxs-lookup"><span data-stu-id="83dcf-140">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="83dcf-141">Elija **cargar desempaquetado**y, a continuación, seleccione el paquete de extensión para transferirlo a la misma.</span><span class="sxs-lookup"><span data-stu-id="83dcf-141">Choose **Load unpacked**, and then select your extension package to sideload.</span></span>  
1.  <span data-ttu-id="83dcf-142">Elige **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="83dcf-142">Choose **OK**.</span></span>
1.  <span data-ttu-id="83dcf-143">Vaya a `edge://extensions` la página y compruebe que la extensión aparece en la lista.</span><span class="sxs-lookup"><span data-stu-id="83dcf-143">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="83dcf-144">Copia la clave de `microsoft_catalog_extension_id` \ (ID \) de la lista de extensiones de la página.</span><span class="sxs-lookup"><span data-stu-id="83dcf-144">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>

<span data-ttu-id="83dcf-145">Cuando esté listo para distribuir la extensión a los usuarios, publique la extensión en el almacén de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="83dcf-145">When you are ready to distribute your extension to users, publish your extension to the Microsoft Edge add-ons store.</span></span>  <span data-ttu-id="83dcf-146">El identificador de extensión de la extensión publicada puede diferir del identificador usado durante la transferencia local de la extensión.</span><span class="sxs-lookup"><span data-stu-id="83dcf-146">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="83dcf-147">Si el identificador ha cambiado, actualiza `allowed_origins` en el archivo de manifiesto de host con el identificador de la extensión publicada.</span><span class="sxs-lookup"><span data-stu-id="83dcf-147">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <span data-ttu-id="83dcf-148">Paso 3: copiar el archivo de manifiesto de host de mensajería nativa en el sistema</span><span class="sxs-lookup"><span data-stu-id="83dcf-148">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="83dcf-149">El paso final consiste en copiar el archivo de manifiesto de host de mensajería nativa en el equipo y asegurarse de que esté configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="83dcf-149">The final step involves copying the native messaging host manifest file to your computer, and ensuring it is configured correctly.</span></span>  <span data-ttu-id="83dcf-150">Para asegurarse de que el archivo de manifiesto se coloca en la ubicación esperada, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="83dcf-150">To ensure your manifest file is placed in the expected location, complete the following the steps.</span></span>  <span data-ttu-id="83dcf-151">La ubicación varía según la plataforma.</span><span class="sxs-lookup"><span data-stu-id="83dcf-151">The location varies by platform.</span></span>  

### [<span data-ttu-id="83dcf-152">Windows</span><span class="sxs-lookup"><span data-stu-id="83dcf-152">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="83dcf-153">El archivo de manifiesto puede encontrarse en cualquier lugar del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="83dcf-153">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="83dcf-154">El instalador de la aplicación debe crear una clave del registro y establecer el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="83dcf-154">The application installer must create a registry key and set the default value of that key to the full path of the manifest file.</span></span>  <span data-ttu-id="83dcf-155">Los siguientes comandos son ejemplos de claves de registro.</span><span class="sxs-lookup"><span data-stu-id="83dcf-155">The following commands are examples of registry keys.</span></span>  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

<span data-ttu-id="83dcf-156">Para agregar una clave del registro en el directorio con la clave del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="83dcf-156">To add a registry key to the directory with the manifest key.</span></span>  

*   <span data-ttu-id="83dcf-157">Comando ejecutar en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="83dcf-157">Run command in command prompt.</span></span>    
    
    1.  <span data-ttu-id="83dcf-158">Ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="83dcf-158">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   <span data-ttu-id="83dcf-159">Cree un `.reg` archivo y ejecútelo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-159">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="83dcf-160">Copie el comando siguiente en un `.reg` archivo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-160">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="83dcf-161">Ejecute el `.reg` archivo.</span><span class="sxs-lookup"><span data-stu-id="83dcf-161">Run the `.reg` file.</span></span>  
    
<span data-ttu-id="83dcf-162">Microsoft Edge consulta primero el registro de 32 bits y, a continuación, el registro de 64 bits para identificar los hosts de mensajería nativos.</span><span class="sxs-lookup"><span data-stu-id="83dcf-162">Microsoft Edge queries the 32-bit registry first, and then the 64-bit registry to identify native messaging hosts.</span></span>  <span data-ttu-id="83dcf-163">Si ejecuta el archivo anterior `.reg` como parte de una secuencia de comandos por lotes, asegúrese de ejecutarlo con un símbolo del sistema de administrador.</span><span class="sxs-lookup"><span data-stu-id="83dcf-163">If you run the above `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>  

### [<span data-ttu-id="83dcf-164">macOS</span><span class="sxs-lookup"><span data-stu-id="83dcf-164">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="83dcf-165">Para almacenar el archivo de manifiesto, lleve a cabo una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="83dcf-165">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="83dcf-166">Los hosts de mensajería instantánea de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.</span><span class="sxs-lookup"><span data-stu-id="83dcf-166">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="83dcf-167">Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="83dcf-167">For example, the manifest file must be stored in following location.</span></span> 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   <span data-ttu-id="83dcf-168">Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio del perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="83dcf-168">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="83dcf-169">Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="83dcf-169">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    <span data-ttu-id="83dcf-170">El  `{Channel_Name}` `Microsoft Edge {Channel_Name}` debe ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="83dcf-170">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   <span data-ttu-id="83dcf-171">Canary</span><span class="sxs-lookup"><span data-stu-id="83dcf-171">Canary</span></span>  
    *   <span data-ttu-id="83dcf-172">Dev</span><span class="sxs-lookup"><span data-stu-id="83dcf-172">Dev</span></span>  
    *   <span data-ttu-id="83dcf-173">Beta</span><span class="sxs-lookup"><span data-stu-id="83dcf-173">Beta</span></span>  

    <span data-ttu-id="83dcf-174">Cuando se usa el canal estable, `{Channel_Name}` no es necesario.</span><span class="sxs-lookup"><span data-stu-id="83dcf-174">When using the Stable channel, `{Channel_Name}` is not required.</span></span>  

### [<span data-ttu-id="83dcf-175">Linux</span><span class="sxs-lookup"><span data-stu-id="83dcf-175">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="83dcf-176">Para almacenar el archivo de manifiesto, lleve a cabo una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="83dcf-176">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="83dcf-177">Los hosts de mensajería instantánea de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.</span><span class="sxs-lookup"><span data-stu-id="83dcf-177">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="83dcf-178">El archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="83dcf-178">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="83dcf-179">Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio del perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="83dcf-179">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="83dcf-180">El archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="83dcf-180">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> <span data-ttu-id="83dcf-181">Asegúrese de que proporciona permisos de lectura en el archivo de manifiesto y ejecute permisos en el motor en tiempo de ejecución del host.</span><span class="sxs-lookup"><span data-stu-id="83dcf-181">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="83dcf-182">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83dcf-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="83dcf-183">La página original se encuentra [aquí](https://developer.chrome.com/extensions/nativeMessaging).</span><span class="sxs-lookup"><span data-stu-id="83dcf-183">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="83dcf-185">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83dcf-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos de Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
