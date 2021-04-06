---
description: Documentación de mensajería nativa
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/31/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: e6233289794bc1c3ef235af46402c23173c09857
ms.sourcegitcommit: e6a4f73be57439149e3cc56491d7364831d0079e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "11475214"
---
# <a name="native-messaging"></a><span data-ttu-id="be8e2-104">Mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="be8e2-104">Native messaging</span></span>  

<span data-ttu-id="be8e2-105">Las extensiones se comunican con una aplicación nativa de Win32 instalada en el dispositivo de un usuario mediante API de paso de mensajes.</span><span class="sxs-lookup"><span data-stu-id="be8e2-105">Extensions communicate with a native Win32 app installed on a user's device using message passing APIs.</span></span>  <span data-ttu-id="be8e2-106">El host de la aplicación nativa envía y recibe mensajes con extensiones mediante entrada estándar y salida estándar.</span><span class="sxs-lookup"><span data-stu-id="be8e2-106">The native app host sends and receives messages with extensions using standard input and standard output.</span></span>  <span data-ttu-id="be8e2-107">Las extensiones que usan mensajería nativa se instalan en Microsoft Edge de forma similar a cualquier otra extensión.</span><span class="sxs-lookup"><span data-stu-id="be8e2-107">Extensions using native messaging are installed in Microsoft Edge similar to any other extension.</span></span>  <span data-ttu-id="be8e2-108">Sin embargo, Microsoft Edge no instala ni administra las aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="be8e2-108">However, native apps are not installed or managed by Microsoft Edge.</span></span>  

<span data-ttu-id="be8e2-109">Para adquirir la extensión y el host de la aplicación nativa, tienes dos modelos de distribución.</span><span class="sxs-lookup"><span data-stu-id="be8e2-109">To acquire the extension and native app host, you have two distribution models.</span></span>  

*   <span data-ttu-id="be8e2-110">Empaquetar la extensión y el host juntos.</span><span class="sxs-lookup"><span data-stu-id="be8e2-110">Package your extension and the host together.</span></span>  <span data-ttu-id="be8e2-111">Cuando un usuario instala el paquete, se instalan tanto la extensión como el host.</span><span class="sxs-lookup"><span data-stu-id="be8e2-111">When a user installs the package, both the extension and the host are installed.</span></span>  
*   <span data-ttu-id="be8e2-112">Instale la extensión con el almacén de complementos de [Microsoft Edge][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]y la extensión pedirá a los usuarios que instalen el host.</span><span class="sxs-lookup"><span data-stu-id="be8e2-112">Install your extension using the [Microsoft Edge Add-ons store][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome], and your extension prompts users to install the host.</span></span>  

<span data-ttu-id="be8e2-113">Para crear la extensión para enviar y recibir mensajes con hosts de aplicaciones nativas, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="be8e2-113">To create your extension to send and receive messages with native app hosts, complete the following steps.</span></span>  

## <a name="step-1---add-permissions-to-the-extension-manifest"></a><span data-ttu-id="be8e2-114">Paso 1: Agregar permisos al manifiesto de extensión</span><span class="sxs-lookup"><span data-stu-id="be8e2-114">Step 1 - Add permissions to the extension manifest</span></span>  

<span data-ttu-id="be8e2-115">Agregue el `nativeMessaging` permiso al archivomanifest.js\*\* de\*\* la extensión.</span><span class="sxs-lookup"><span data-stu-id="be8e2-115">Add the `nativeMessaging` permission to the **manifest.json** file of the extension.</span></span>  <span data-ttu-id="be8e2-116">El siguiente fragmento de código es un ejemplo \*\* demanifest.jsen\*\*.</span><span class="sxs-lookup"><span data-stu-id="be8e2-116">The following code snippet is an example of **manifest.json**.</span></span>  

```json
{
    "name": "Native Messaging Example",
    "version": "1.0",
    "manifest_version": 2, 
    "description": "Send a message to a native app.",
    "app": { 
        "launch": { 
            "local_path": "main.html" 
        } 
    }, 
    "icons": { 
        "128": "icon-128.png"
    }, 
    "permissions": ["nativeMessaging"] 
}
```  

## <a name="step-2---create-your-native-messaging-host-manifest-file"></a><span data-ttu-id="be8e2-117">Paso 2: Crear el archivo de manifiesto de host de mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="be8e2-117">Step 2 - Create your native messaging host manifest file</span></span>  

<span data-ttu-id="be8e2-118">Las aplicaciones nativas deben proporcionar un archivo de manifiesto de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-118">Native apps must provide a native messaging host manifest file.</span></span>  <span data-ttu-id="be8e2-119">El archivo de manifiesto contiene la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="be8e2-119">The manifest file contains the following information.</span></span>  

*   <span data-ttu-id="be8e2-120">Ruta de acceso al tiempo de ejecución del host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-120">The path to the native messaging host runtime.</span></span>  
*   <span data-ttu-id="be8e2-121">Método de comunicación con la extensión.</span><span class="sxs-lookup"><span data-stu-id="be8e2-121">The method of communication with the extension.</span></span>  
*   <span data-ttu-id="be8e2-122">Una lista de extensiones permitidas a las que se comunica.</span><span class="sxs-lookup"><span data-stu-id="be8e2-122">A list of allowed extensions to which it communicates.</span></span>  
    
<span data-ttu-id="be8e2-123">El explorador lee y valida el manifiesto de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-123">The browser reads and validates the native messaging host manifest.</span></span>  <span data-ttu-id="be8e2-124">El explorador no instala ni administra el archivo de manifiesto de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-124">The browser doesn't install or manage the native messaging host manifest file.</span></span>  

```json
{
    "name": "com.my_company.my_app",
    "description": "My App",
    "path": "C:\\Program Files\\My App\\chrome_native_messaging_host.exe",
    "type": "stdio",
    "allowed_origins": [
        "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

<span data-ttu-id="be8e2-125">El archivo de manifiesto de host debe ser un archivo JSON válido que contenga las siguientes claves.</span><span class="sxs-lookup"><span data-stu-id="be8e2-125">The host manifest file must be a valid JSON file that contains the following keys.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="be8e2-126">Key</span><span class="sxs-lookup"><span data-stu-id="be8e2-126">Key</span></span>**  
   :::column-end:::
   :::column span="3":::
      **<span data-ttu-id="be8e2-127">Detalles</span><span class="sxs-lookup"><span data-stu-id="be8e2-127">Details</span></span>**  
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `name`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="be8e2-128">Especifica el nombre del host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-128">Specifies the name of the native messaging host.</span></span>  <span data-ttu-id="be8e2-129">Los clientes pasan la cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="be8e2-129">Clients pass the string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  
      
      *   <span data-ttu-id="be8e2-130">El valor solo debe contener caracteres alfanuméricos en minúsculas, guiones bajos y puntos.</span><span class="sxs-lookup"><span data-stu-id="be8e2-130">The value must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  
      *   <span data-ttu-id="be8e2-131">El valor no debe iniciarse ni terminar con un punto, y un punto no debe ir seguido de otro punto.</span><span class="sxs-lookup"><span data-stu-id="be8e2-131">The value must not start or end with a dot, and a dot must not be followed by another dot.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `description`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="be8e2-132">Describe la aplicación.</span><span class="sxs-lookup"><span data-stu-id="be8e2-132">Describes the app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `path`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="be8e2-133">Especifica la ruta de acceso al binario de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-133">Specifies the path to the native messaging host binary.</span></span>  
      
      *   <span data-ttu-id="be8e2-134">En dispositivos Windows, puedes usar rutas relativas al directorio que contiene el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="be8e2-134">On Windows devices, you may use relative paths to the directory that contains the manifest file.</span></span>  
      *   <span data-ttu-id="be8e2-135">En macOS y Linux, la ruta de acceso debe ser absoluta.</span><span class="sxs-lookup"><span data-stu-id="be8e2-135">On macOS and Linux, the path must be absolute.</span></span>  
          
      <span data-ttu-id="be8e2-136">El proceso de host comienza con el directorio actual establecido en el directorio que contiene el binario de host.</span><span class="sxs-lookup"><span data-stu-id="be8e2-136">The host process starts with the current directory set to the directory that contains the host binary.</span></span>  <span data-ttu-id="be8e2-137">Por ejemplo \(Windows\), si el parámetro está establecido en , el binario se inicia con `C:\App\nm_host.exe` el directorio actual \( `C:\App\` \).</span><span class="sxs-lookup"><span data-stu-id="be8e2-137">For example \(Windows\), if the parameter is set to `C:\App\nm_host.exe`, the binary is started using the current directory \(`C:\App\`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `type`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="be8e2-138">Especifica el tipo de interfaz que se usa para comunicarse con el host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-138">Specifies the type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="be8e2-139">El valor indica a Microsoft Edge que use `stdin` y se comunique con el `stdout` host.</span><span class="sxs-lookup"><span data-stu-id="be8e2-139">The value instructs Microsoft Edge to use `stdin` and `stdout` to communicate with the host.</span></span>  
      <span data-ttu-id="be8e2-140">El único valor aceptable es `stdio` .</span><span class="sxs-lookup"><span data-stu-id="be8e2-140">The only acceptable value is `stdio`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `allowed_origins` 
   :::column-end:::
   :::column span="3":::
      ---  
      
      <span data-ttu-id="be8e2-141">Especifica la lista de extensiones que tienen acceso al host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-141">Specifies the list of extensions that have access to the native messaging host.</span></span>  <span data-ttu-id="be8e2-142">Para activar la aplicación para identificar y comunicarse con una extensión, en el archivo de manifiesto de host de mensajería nativa, establezca el siguiente valor.</span><span class="sxs-lookup"><span data-stu-id="be8e2-142">To turn on your app to identify and communicate with an extension, in your native messaging host manifest file set the following value.</span></span>  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="be8e2-143">Carga local de la extensión para probar la mensajería nativa con el host.</span><span class="sxs-lookup"><span data-stu-id="be8e2-143">Sideload your extension to test native messaging with the host.</span></span>  
<span data-ttu-id="be8e2-144">Para realizar una instalación local de la extensión durante el desarrollo y `microsoft_catalog_extension_id` recuperarla, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="be8e2-144">To sideload your extension during development and retrieve `microsoft_catalog_extension_id`, complete the following actions.</span></span>  

1.  <span data-ttu-id="be8e2-145">Navegue hasta `edge://extensions` y, a continuación, active el botón de alternancia modo programador.</span><span class="sxs-lookup"><span data-stu-id="be8e2-145">Navigate to `edge://extensions`, and then turn on the Developer mode toggle button.</span></span>  
1.  <span data-ttu-id="be8e2-146">Elija **Cargar desempaquetar**y, a continuación, elija el paquete de extensión para la instalación local.</span><span class="sxs-lookup"><span data-stu-id="be8e2-146">Choose **Load unpacked**, and then choose your extension package to sideload.</span></span>  
1.  <span data-ttu-id="be8e2-147">Elige **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="be8e2-147">Choose **OK**.</span></span>  
1.  <span data-ttu-id="be8e2-148">Vaya a `edge://extensions` la página y compruebe que la extensión aparece.</span><span class="sxs-lookup"><span data-stu-id="be8e2-148">Navigate to `edge://extensions` page and verify your extension is listed.</span></span>  
1.  <span data-ttu-id="be8e2-149">Copie la clave `microsoft_catalog_extension_id` de \(ID\) de la lista de extensiones de la página.</span><span class="sxs-lookup"><span data-stu-id="be8e2-149">Copy the key from `microsoft_catalog_extension_id` \(ID\) from the extension listing on the page.</span></span>  
    
<span data-ttu-id="be8e2-150">Cuando esté listo para distribuir la extensión a los usuarios, publique la extensión en el almacén de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="be8e2-150">When you're ready to distribute your extension to users, publish your extension to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="be8e2-151">El identificador de extensión de la extensión publicada puede diferir del identificador usado durante la instalación local de la extensión.</span><span class="sxs-lookup"><span data-stu-id="be8e2-151">The extension ID of the published extension may differ from the ID used while sideloading your extension.</span></span>  <span data-ttu-id="be8e2-152">Si el identificador cambió, actualice `allowed_origins` en el archivo de manifiesto de host con el identificador de la extensión publicada.</span><span class="sxs-lookup"><span data-stu-id="be8e2-152">If the ID changed, update `allowed_origins` in the host manifest file with the ID of your published extension.</span></span>  

## <a name="step-3---copy-the-native-messaging-host-manifest-file-to-your-system"></a><span data-ttu-id="be8e2-153">Paso 3: copiar el archivo de manifiesto de host de mensajería nativa en el sistema</span><span class="sxs-lookup"><span data-stu-id="be8e2-153">Step 3 - Copy the native messaging host manifest file to your system</span></span>  

<span data-ttu-id="be8e2-154">El último paso consiste en copiar el archivo de manifiesto del host de mensajería nativa en el equipo y garantizar que el archivo de manifiesto esté configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="be8e2-154">The final step involves copying the native messaging host manifest file to your computer, and ensuring the manifest file is correctly configured.</span></span>  <span data-ttu-id="be8e2-155">Para asegurarse de que el archivo de manifiesto se coloca en la ubicación esperada, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="be8e2-155">To ensure your manifest file is placed in the expected location, complete the following the actions.</span></span>  <span data-ttu-id="be8e2-156">La ubicación varía según la plataforma.</span><span class="sxs-lookup"><span data-stu-id="be8e2-156">The location varies by platform.</span></span>

> [!NOTE]
> <span data-ttu-id="be8e2-157">Asegúrese de proporcionar permisos de lectura en el archivo de manifiesto y ejecutar permisos en el tiempo de ejecución del host.</span><span class="sxs-lookup"><span data-stu-id="be8e2-157">Ensure that you provide read permissions on the manifest file, and run permissions on the host runtime.</span></span>  

### [<a name="windows"></a><span data-ttu-id="be8e2-158">Windows</span><span class="sxs-lookup"><span data-stu-id="be8e2-158">Windows</span></span>](#tab/windows/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="be8e2-159">El archivo de manifiesto puede encontrarse en cualquier lugar del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="be8e2-159">The manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="be8e2-160">El instalador de la aplicación debe crear una clave del Registro y establecer el valor predeterminado de la clave en la ruta de acceso completa del archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="be8e2-160">The app installer must create a registry key and set the default value of the key to the full path of the manifest file.</span></span>  <span data-ttu-id="be8e2-161">Las siguientes ubicaciones son ejemplos de claves del Registro.</span><span class="sxs-lookup"><span data-stu-id="be8e2-161">The following locations are examples of registry keys.</span></span>  

```output
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app
```  

<span data-ttu-id="be8e2-162">Para agregar una clave del Registro al directorio con la clave de manifiesto, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="be8e2-162">To add a registry key to the directory with the manifest key, complete one of the following actions.</span></span>  

*   <span data-ttu-id="be8e2-163">Ejecute el comando en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="be8e2-163">Run command in command prompt.</span></span>  
    
    1.  <span data-ttu-id="be8e2-164">Ejecute el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="be8e2-164">Run the following command.</span></span>  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
        
*   <span data-ttu-id="be8e2-165">Cree un `.reg` archivo y ejecutarlo.</span><span class="sxs-lookup"><span data-stu-id="be8e2-165">Create a `.reg` file and run it.</span></span>  
    
    1.  <span data-ttu-id="be8e2-166">Copie el siguiente comando en un `.reg` archivo.</span><span class="sxs-lookup"><span data-stu-id="be8e2-166">Copy the following command into a `.reg` file.</span></span>  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  <span data-ttu-id="be8e2-167">Ejecute el `.reg` archivo.</span><span class="sxs-lookup"><span data-stu-id="be8e2-167">Run the `.reg` file.</span></span>  
        
<span data-ttu-id="be8e2-168">Microsoft Edge consulta la `HKEY_CURRENT_USER` clave raíz seguida de `HKEY_LOCAL_MACHINE` .</span><span class="sxs-lookup"><span data-stu-id="be8e2-168">Microsoft Edge queries the `HKEY_CURRENT_USER` root key followed by `HKEY_LOCAL_MACHINE`.</span></span>  <span data-ttu-id="be8e2-169">En ambas claves, primero se busca en el Registro de 32 bits y, a continuación, se busca en el Registro de 64 bits para identificar hosts de mensajería nativos.</span><span class="sxs-lookup"><span data-stu-id="be8e2-169">In both of the keys, the 32-bit registry is searched first, and then the 64-bit registry is searched to identify native messaging hosts.</span></span>  <span data-ttu-id="be8e2-170">La clave del Registro especifica la ubicación del manifiesto del host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="be8e2-170">The registry key specifies the location of the native messaging host manifest.</span></span>  <span data-ttu-id="be8e2-171">Si las entradas del Registro de Microsoft Edge no tienen la ubicación del manifiesto del host, las ubicaciones del Registro Chromium y Chrome se usan como opciones de reserva.</span><span class="sxs-lookup"><span data-stu-id="be8e2-171">If the registry entries for Microsoft Edge don't have the location of the host manifest, the Chromium and Chrome registry locations are used as fallback options.</span></span>  <span data-ttu-id="be8e2-172">Si Microsoft Edge encuentra la clave del Registro en cualquiera de las ubicaciones enumeradas anteriormente, no consulta las ubicaciones que aparecen en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="be8e2-172">If Microsoft Edge finds the registry key at any of the previously listed locations, it doesn't query the locations that are listed in the following code snippet.</span></span>  <span data-ttu-id="be8e2-173">Si ejecuta el archivo creado como parte de un `.reg` script por lotes, asegúrese de ejecutarlo con un símbolo del sistema de administrador.</span><span class="sxs-lookup"><span data-stu-id="be8e2-173">If you run your created `.reg` file as part of a batch script, ensure you run it using an administrator command prompt.</span></span>

<span data-ttu-id="be8e2-174">La siguiente lista es el orden de búsqueda de las ubicaciones del Registro.</span><span class="sxs-lookup"><span data-stu-id="be8e2-174">The following list is the search order for the registry locations.</span></span>  

```output
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\

HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Google\Chrome\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Chromium\NativeMessagingHosts\
HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\
```  
 
> [!NOTE] 
> <span data-ttu-id="be8e2-175">Si tiene extensiones en los complementos de Microsoft Edge y chrome webstore, debe agregar los IDs de extensión correspondientes a ambos almacenes en el archivo de manifiesto de host porque solo se lee el manifiesto de host correspondiente a la primera ubicación del Registro `allowed_origins` encontrada.</span><span class="sxs-lookup"><span data-stu-id="be8e2-175">If you have extensions on the Microsoft Edge Add-ons and the Chrome Webstore, you must add the extension IDs corresponding to both the stores in the `allowed_origins` of the host manifest file because only the host manifest corresponding to the first registry location found is read.</span></span>  

### [<a name="macos"></a><span data-ttu-id="be8e2-176">macOS</span><span class="sxs-lookup"><span data-stu-id="be8e2-176">macOS</span></span>](#tab/macos/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="be8e2-177">Para almacenar el archivo de manifiesto, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="be8e2-177">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="be8e2-178">Los hosts de mensajería nativa de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.</span><span class="sxs-lookup"><span data-stu-id="be8e2-178">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="be8e2-179">Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="be8e2-179">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
*   <span data-ttu-id="be8e2-180">Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio de perfiles de usuario.</span><span class="sxs-lookup"><span data-stu-id="be8e2-180">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="be8e2-181">Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="be8e2-181">For example, the manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
    <span data-ttu-id="be8e2-182">La  `{Channel_Name}` entrada debe ser uno de los siguientes `Microsoft Edge {Channel_Name}` valores.</span><span class="sxs-lookup"><span data-stu-id="be8e2-182">The  `{Channel_Name}` in `Microsoft Edge {Channel_Name}` must be one of the following values.</span></span>  
    
    *   `Canary`  
    *   `Dev`  
    *   `Beta`  
        
    <span data-ttu-id="be8e2-183">Cuando se usa el canal Estable, ` {Channel_Name}` no es necesario.</span><span class="sxs-lookup"><span data-stu-id="be8e2-183">When using the Stable channel, ` {Channel_Name}` isn't required.</span></span>  
    
### [<a name="linux"></a><span data-ttu-id="be8e2-184">Linux</span><span class="sxs-lookup"><span data-stu-id="be8e2-184">Linux</span></span>](#tab/linux/)  

<a id="copy-manifest-file"></a>  

<span data-ttu-id="be8e2-185">Para almacenar el archivo de manifiesto, complete una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="be8e2-185">To store the manifest file, complete one of the following actions.</span></span>  

*   <span data-ttu-id="be8e2-186">Los hosts de mensajería nativa de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.</span><span class="sxs-lookup"><span data-stu-id="be8e2-186">System-wide native messaging hosts, which are available to all users, are stored in a fixed location.</span></span>  <span data-ttu-id="be8e2-187">El archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="be8e2-187">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   <span data-ttu-id="be8e2-188">Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio de perfiles de usuario.</span><span class="sxs-lookup"><span data-stu-id="be8e2-188">User-specific native messaging hosts, which are available to the current user only, are located in the `NativeMessagingHosts` subdirectory in the user profile directory.</span></span>  <span data-ttu-id="be8e2-189">El archivo de manifiesto debe almacenarse en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="be8e2-189">The manifest file must be stored in following location.</span></span>  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

<!-- links -->  

[MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos de Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="be8e2-191">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="be8e2-191">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="be8e2-192">La página original se encuentra [aquí.](https://developer.chrome.com/extensions/nativeMessaging)</span><span class="sxs-lookup"><span data-stu-id="be8e2-192">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="be8e2-194">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="be8e2-194">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
