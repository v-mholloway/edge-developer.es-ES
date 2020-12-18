---
description: Más información sobre cómo puedes usar la mensajería nativa para que tu extensión se comunique con una aplicación para UWP complementaria.
title: Extensiones-mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, nativo, mensajería, UWP
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 983ae11822edabc0f27bd6c02f9397104b082ad6
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236502"
---
# <span data-ttu-id="a99c0-104">Mensajería nativa en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a99c0-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="a99c0-105">Descripción general de la arquitectura de mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="a99c0-105">Native messaging architecture overview</span></span>

<span data-ttu-id="a99c0-106">Con Windows 10 Creators Update, las extensiones de Microsoft Edge pueden usar la mensajería nativa para comunicarse con una aplicación complementaria de la plataforma universal de Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="a99c0-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform (UWP) app.</span></span>  <span data-ttu-id="a99c0-107">En un nivel alto, las extensiones de Microsoft Edge usan las mismas API para la mensajería nativa que las Extensiones Chrome y Firefox.</span><span class="sxs-lookup"><span data-stu-id="a99c0-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span> <span data-ttu-id="a99c0-108">Sin embargo, el host de mensajería nativo deberá implementarse con la plataforma universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="a99c0-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>

> [!NOTE]
> <span data-ttu-id="a99c0-109">El método que se describe a continuación (que se conecta a una aplicación para UWP a través de AppService) es el único mecanismo admitido para habilitar la comunicación entre las extensiones de Microsoft Edge y los componentes nativos.</span><span class="sxs-lookup"><span data-stu-id="a99c0-109">The method outlined below (connecting to a UWP app via AppService) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span> <span data-ttu-id="a99c0-110">Para obtener más información sobre cómo habilitar la comunicación con componentes heredados de Win32, consulte la sección [Agregar un componente de puente de escritorio](#adding-a-desktop-bridge-component) de esta guía.</span><span class="sxs-lookup"><span data-stu-id="a99c0-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span> 

 <span data-ttu-id="a99c0-111">La arquitectura de mensajería nativa de Microsoft Edge aprovecha la [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API existente como infraestructura de comunicación entre procesos (IPC) subyacente.</span><span class="sxs-lookup"><span data-stu-id="a99c0-111">Microsoft Edge's native messaging architecture leverages the existing [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API as the underlying inter-process communication (IPC) infrastructure.</span></span> <span data-ttu-id="a99c0-112">Las aplicaciones para UWP usan la `AppService` API para comunicarse entre sí.</span><span class="sxs-lookup"><span data-stu-id="a99c0-112">UWP apps use the `AppService` API to communicate with one another.</span></span> <span data-ttu-id="a99c0-113">Por eso, las extensiones de Microsoft Edge ahora pueden comunicarse con aplicaciones para UWP.</span><span class="sxs-lookup"><span data-stu-id="a99c0-113">Because of this, Microsoft Edge extensions can now communicate with UWP apps.</span></span>

![arquitectura de mensajería nativa](./../media/native-messaging-architecture.png)

### <span data-ttu-id="a99c0-115">Cuándo y cuándo no usar la mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="a99c0-115">When and when not to use native messaging</span></span>

<span data-ttu-id="a99c0-116">La mensajería nativa agrega una capa completamente nueva a la extensión.</span><span class="sxs-lookup"><span data-stu-id="a99c0-116">Native messaging adds a whole new layer to your extension.</span></span> <span data-ttu-id="a99c0-117">Al implementar una aplicación complementaria para UWP para tu extensión, las siguientes posibilidades estarán disponibles:</span><span class="sxs-lookup"><span data-stu-id="a99c0-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>

* <span data-ttu-id="a99c0-118">Sincronizar datos (por ejemplo, credenciales) con una aplicación para UWP complementaria.</span><span class="sxs-lookup"><span data-stu-id="a99c0-118">Synchronize data (e.g. credentials) with a companion UWP app.</span></span>
* <span data-ttu-id="a99c0-119">Implemente algoritmos de cifrado/descifrado más estrictos que no estén disponibles en las API Web.</span><span class="sxs-lookup"><span data-stu-id="a99c0-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>
* <span data-ttu-id="a99c0-120">Acceso a recursos que no son accesibles a través de las API Web, por ejemplo, dispositivos de hardware o USB</span><span class="sxs-lookup"><span data-stu-id="a99c0-120">Access resources that are not accessible through web APIs, e.g. hardware or USB devices</span></span>

<span data-ttu-id="a99c0-121">Hay algunos casos en los que no se puede usar la mensajería nativa por restricciones de seguridad o de directiva:</span><span class="sxs-lookup"><span data-stu-id="a99c0-121">There are a few instances where native messaging can't be used due to security or policy restrictions:</span></span>

* <span data-ttu-id="a99c0-122">Modificar la configuración de usuario en Microsoft Edge o Windows, por ejemplo, cambiar el explorador predeterminado o el proveedor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a99c0-122">Modifying user settings in either Microsoft Edge or Windows, e.g. changing the default browser or search provider.</span></span>
* <span data-ttu-id="a99c0-123">Acciones que infringen las directivas de Microsoft Store para las aplicaciones y las extensiones.</span><span class="sxs-lookup"><span data-stu-id="a99c0-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>
* <span data-ttu-id="a99c0-124">Transfiriendo datos a un extremo remoto a través de un host de mensajes nativo.</span><span class="sxs-lookup"><span data-stu-id="a99c0-124">Transferring data to remote endpoint via native message host.</span></span>
* <span data-ttu-id="a99c0-125">Permitir que otras aplicaciones descarguen contenido que cambia el comportamiento de la extensión.</span><span class="sxs-lookup"><span data-stu-id="a99c0-125">Allowing other apps to download content that changes extension behavior.</span></span>

## <span data-ttu-id="a99c0-126">Demos</span><span class="sxs-lookup"><span data-stu-id="a99c0-126">Demos</span></span>

<span data-ttu-id="a99c0-127">Para tener una idea de lo que parece una extensión de mensajería nativa de Microsoft Edge que tiene una aplicación para UWP complementaria y un puente de escritorio, consulta los ejemplos de [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) y [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) en github.</span><span class="sxs-lookup"><span data-stu-id="a99c0-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>

### <span data-ttu-id="a99c0-128">Cómo funciona</span><span class="sxs-lookup"><span data-stu-id="a99c0-128">How it works</span></span>

<span data-ttu-id="a99c0-129">El componente de extensión de Microsoft Edge de la muestra usa su script de contenido para detectar cuando un usuario escribe información que se debe cifrar.</span><span class="sxs-lookup"><span data-stu-id="a99c0-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span> <span data-ttu-id="a99c0-130">La extensión comunica esto al componente de puente de escritorio a través de la mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="a99c0-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span> <span data-ttu-id="a99c0-131">Cuando el usuario está listo para enviar los datos, la extensión devolverá un valor cifrado al sitio Web.</span><span class="sxs-lookup"><span data-stu-id="a99c0-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>

> [!NOTE]
> <span data-ttu-id="a99c0-132">Este ejemplo solo funciona en una página web que usa eventos personalizados para comunicarse con el script de contenido de la extensión.</span><span class="sxs-lookup"><span data-stu-id="a99c0-132">This sample will only work on a webpage that uses custom events to communicate with the extension's content script.</span></span> <span data-ttu-id="a99c0-133">La carpeta de ejemplo incluye un [archivo. html](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) para probar la extensión.</span><span class="sxs-lookup"><span data-stu-id="a99c0-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>

<span data-ttu-id="a99c0-134">En este ejemplo, se usa la aplicación para UWP para pasar las respuestas del puente de escritorio a Microsoft Edge, que se envían a la extensión de Microsoft Edge a través de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a99c0-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span> <span data-ttu-id="a99c0-135">Aunque este ejemplo tiene el host de mensajería nativo ejecutándose en la aplicación principal, también puede ejecutarse como una tarea en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a99c0-135">While this example has the native messaging host run in the main app, it's also able to run as a background task.</span></span> <span data-ttu-id="a99c0-136">Para cambiar entre los dos, es necesario editar la secuencia de comandos de fondo de la extensión, cambiando la cadena de `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` a a `"NativeMessagingHostOutOfProcess"` .</span><span class="sxs-lookup"><span data-stu-id="a99c0-136">Switching between the two requires editing the extension's background script, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>

## <span data-ttu-id="a99c0-137">Implementación de Chrome y Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a99c0-137">Chrome vs Microsoft Edge implementation</span></span>

<span data-ttu-id="a99c0-138">Mientras que Chrome dirige las API de paso de mensajes para que sus extensiones se comuniquen con las aplicaciones, Microsoft Edge usa la [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API que ahora permite que las extensiones de Microsoft Edge y las aplicaciones para UWP se comuniquen.</span><span class="sxs-lookup"><span data-stu-id="a99c0-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>

<span data-ttu-id="a99c0-139">En esta sección se detallan las diferencias entre la implementación de mensajería nativa de Chrome y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a99c0-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>

### <span data-ttu-id="a99c0-140">Registro y manifiesto del host</span><span class="sxs-lookup"><span data-stu-id="a99c0-140">Registration and host manifest</span></span>
<span data-ttu-id="a99c0-141">Para que tu extensión sea reconocida por tu extensión como host de mensajería nativa, tendrás que registrarte.</span><span class="sxs-lookup"><span data-stu-id="a99c0-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>

<span data-ttu-id="a99c0-142">Para el registro de host de [Mensajería nativa de Chrome](https://developer.chrome.com/extensions/nativeMessaging) , la aplicación debe instalar un archivo de manifiesto en cualquier parte del sistema de archivos de Windows que defina la configuración de host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="a99c0-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>

<span data-ttu-id="a99c0-143">El siguiente JSON es un ejemplo de cómo se puede configurar el archivo de configuración:</span><span class="sxs-lookup"><span data-stu-id="a99c0-143">The following JSON is an example of how the config file can be set up:</span></span>

```json
{
   "name": "com.my_company.my_application",
   "description": "My Application",
   "path": "C:\\ProgramFiles\\MyApplication\\chrome_native_messaging_host.exe",
   "type": "stdio",
   "allowed_origins": [
      "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```  

<span data-ttu-id="a99c0-144">Para instalar este archivo, la aplicación tendría que:</span><span class="sxs-lookup"><span data-stu-id="a99c0-144">To install this file, the app would need to:</span></span>

1.  <span data-ttu-id="a99c0-145">Registre el archivo de manifiesto en una ubicación predefinida en el registro que defina la configuración del host:</span><span class="sxs-lookup"><span data-stu-id="a99c0-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>
    -   ```text
        HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application
        ```  
        
        <span data-ttu-id="a99c0-146">o</span><span class="sxs-lookup"><span data-stu-id="a99c0-146">or</span></span>
        
    -   ```text
        HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application
        ```  
        
2.  <span data-ttu-id="a99c0-147">Establezca el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto, por ejemplo,</span><span class="sxs-lookup"><span data-stu-id="a99c0-147">Set the default value of that key to the full path to the manifest file, e.g.</span></span> 
    
    ```text
    [HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
<span data-ttu-id="a99c0-148">Para Microsoft Edge, para registrar un [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) (host de mensajería nativo), tendrás que incluir la aplicación complementaria de UWP en el mismo paquete que la extensión y especificar la [extensión de AppService](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) en el archivo del proyecto `Package.appxmanifest` .</span><span class="sxs-lookup"><span data-stu-id="a99c0-148">For Microsoft Edge, in order to register an [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx)(native messaging host) you'll need to include the UWP companion app in the same package as your extension and specify the [AppService extension](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in your project's `Package.appxmanifest` file.</span></span> <span data-ttu-id="a99c0-149">El `EntryPoint` `Name` usuario puede configurar los atributos y:</span><span class="sxs-lookup"><span data-stu-id="a99c0-149">The `EntryPoint` and `Name` attributes can be configured by you:</span></span>

```xml
...
<Applications>    
    <Application Id="App"         
        <Extensions>        
            <uap:Extension Category="windows.appService" EntryPoint="MyAppService.Inventory">          
            <uap:AppService Name="com.microsoft.inventory"/>        
            </uap:Extension>      
        </Extensions>      
        ...    
    </Application>
</Applications>
```


<span data-ttu-id="a99c0-150">También necesitará establecer qué extensiones están autorizadas a conectarse al servicio.</span><span class="sxs-lookup"><span data-stu-id="a99c0-150">You'll also need to set which extension(s) are allowed to connect to the service.</span></span> <span data-ttu-id="a99c0-151">Debido a que Microsoft Edge no tiene una `"allowed_origins"` propiedad de manifiesto equivalente en tu AppxManifest, la aplicación para UWP deberá determinarlo y aplicarlo en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="a99c0-151">Because Microsoft Edge doesn't have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span> <span data-ttu-id="a99c0-152">Como Microsoft Edge va a establecer la conexión en nombre de la extensión, la aplicación puede buscar el nombre de familia de la persona que llama para determinar si está conectado por Microsoft Edge para controlar o autenticar a la persona que llama.</span><span class="sxs-lookup"><span data-stu-id="a99c0-152">Since Microsoft Edge will be establishing the connection on behalf of the extension, the app can look up the caller's Package Family Name to determine if they're being connected by Microsoft Edge to control or authenticate the caller.</span></span> <span data-ttu-id="a99c0-153">P. ej.</span><span class="sxs-lookup"><span data-stu-id="a99c0-153">E.g.</span></span> 

```csharp
protected async override void
OnBackgroundActivated(BackgroundActivatedEventArgs args)
{
    IBackgroundTaskInstance taskInstance = args.TaskInstance;
    if (taskInstance.TriggerDetails is AppServiceTriggerDetails)
    {
        AppServiceTriggerDetails appService = taskInstance.TriggerDetails as AppServiceTriggerDetails;
        if (appService.CallerPackageFamilyName == EdgePFN)
        {
            // Establish the connection
        }
        else
        {
            // Reject the connection
        }
    }
}
```  

### <span data-ttu-id="a99c0-154">Envío de mensajes</span><span class="sxs-lookup"><span data-stu-id="a99c0-154">Message sending</span></span>

<span data-ttu-id="a99c0-155">Para que una aplicación y una extensión se comuniquen entre sí, los mensajes se deben enviar y recibir.</span><span class="sxs-lookup"><span data-stu-id="a99c0-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>

<span data-ttu-id="a99c0-156">Las extensiones de Chrome inician un mensaje con la [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API para enviar un mensaje al host nativo mediante un canal no persistente.</span><span class="sxs-lookup"><span data-stu-id="a99c0-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span> 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

<span data-ttu-id="a99c0-157">El primer parámetro es el nombre del host nativo, en el que busca el cromo en el registro.</span><span class="sxs-lookup"><span data-stu-id="a99c0-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span> <span data-ttu-id="a99c0-158">El manifiesto especifica el archivo. exe que se iniciará en un espacio aislado y el mensaje se enviará con la e/s estándar.</span><span class="sxs-lookup"><span data-stu-id="a99c0-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span> <span data-ttu-id="a99c0-159">Las extensiones también pueden establecer un canal persistente mediante la `runtime.connectNative` API, que toma el nombre del host nativo como el único parámetro.</span><span class="sxs-lookup"><span data-stu-id="a99c0-159">Extensions can also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span> 

<span data-ttu-id="a99c0-160">Microsoft Edge usa la misma construcción que la API de mensajería nativa de Chrome para permitir que las extensiones de Microsoft Edge especifiquen a qué servicio de aplicaciones conectar.</span><span class="sxs-lookup"><span data-stu-id="a99c0-160">Microsoft Edge uses the same construct as Chrome's native messaging API to allow Microsoft Edge extensions to specify which app service to connect to.</span></span> <span data-ttu-id="a99c0-161">El primer parámetro de `runtime.sendNativeMessage` especifica el nombre del servicio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a99c0-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span> <span data-ttu-id="a99c0-162">En la sección [registro y manifiesto del host](#registration-and-host-manifest) , este es el `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="a99c0-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span> <span data-ttu-id="a99c0-163">La plataforma de extensión de Microsoft Edge restringe que el host de mensajería nativa sea una aplicación para UWP que esté empaquetada en el mismo AppX que la extensión.</span><span class="sxs-lookup"><span data-stu-id="a99c0-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span> <span data-ttu-id="a99c0-164">Esto atenúa los riesgos de seguridad asociados con ataques maliciosos que intentan conectar Microsoft Edge con otro nombre de familia de paquetes mediante la manipulación de entradas de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a99c0-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span> 

<span data-ttu-id="a99c0-165">Esto significa que Microsoft Edge usará el mismo nombre de familia de paquete que la extensión, además del `AppService` nombre especificado en la API, para identificar de forma única el proveedor del servicio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a99c0-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="a99c0-166">El [Kit de herramientas de extensión de Microsoft Edge](./porting-chrome-extensions.md)no lo convertirá fácilmente.</span><span class="sxs-lookup"><span data-stu-id="a99c0-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span> <span data-ttu-id="a99c0-167">Todas las extensiones que especifiquen el `"nativeMessaging"` permiso se marcarán como obligatorias para este componente.</span><span class="sxs-lookup"><span data-stu-id="a99c0-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>

### <span data-ttu-id="a99c0-168">Protocolo de comunicación</span><span class="sxs-lookup"><span data-stu-id="a99c0-168">Communication protocol</span></span>

<span data-ttu-id="a99c0-169">El protocolo de comunicación para la mensajería instantánea determina cómo se aplica el formato a los mensajes antes de enviarlos.</span><span class="sxs-lookup"><span data-stu-id="a99c0-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>

<span data-ttu-id="a99c0-170">Chrome inicia cada host de mensajería nativo en un proceso independiente y se comunica con él con la entrada estándar y la salida estándar.</span><span class="sxs-lookup"><span data-stu-id="a99c0-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span> <span data-ttu-id="a99c0-171">El mismo formato se usa para enviar mensajes en ambas direcciones: cada mensaje se serializa con JSON, UTF-8 codificado y viene precedido de la longitud del mensaje de 32 bits en el orden de bytes nativo.</span><span class="sxs-lookup"><span data-stu-id="a99c0-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>

<span data-ttu-id="a99c0-172">En Microsoft Edge, la plataforma de la tarea en segundo plano y la aplicación principal que implementa el servicio de aplicaciones se iniciará con la plataforma.</span><span class="sxs-lookup"><span data-stu-id="a99c0-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span> <span data-ttu-id="a99c0-173">Al iniciar, se invocará el método de la tarea en segundo plano `Run` :</span><span class="sxs-lookup"><span data-stu-id="a99c0-173">On startup, the background task's `Run` method will be invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service isn't terminated.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```  

<span data-ttu-id="a99c0-174">Cuando la extensión envíe un mensaje a tu aplicación para UWP, se [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) generará el evento.</span><span class="sxs-lookup"><span data-stu-id="a99c0-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) event will be raised.</span></span> <span data-ttu-id="a99c0-175">A continuación, este mensaje con formato JSON se stringified en el primer par de KeyValue de un [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objeto.</span><span class="sxs-lookup"><span data-stu-id="a99c0-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object.</span></span> <span data-ttu-id="a99c0-176">:</span><span class="sxs-lookup"><span data-stu-id="a99c0-176">:</span></span>

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

<span data-ttu-id="a99c0-177">Cuando la aplicación para UWP vuelve a enviar una respuesta a tu extensión, se [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) agregará un a al `ValueSet` objeto.</span><span class="sxs-lookup"><span data-stu-id="a99c0-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) will be added to the `ValueSet` object.</span></span> <span data-ttu-id="a99c0-178">`Key`Microsoft Edge omitirá la propiedad, pero la propiedad contendrá `Value` una cadena JSON válida.</span><span class="sxs-lookup"><span data-stu-id="a99c0-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>

### <span data-ttu-id="a99c0-179">Devolución</span><span class="sxs-lookup"><span data-stu-id="a99c0-179">Callback</span></span>

<span data-ttu-id="a99c0-180">Para devoluciones de llamada, usa Chrome, [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) lo que permite que una función de devolución de llamada controle cualquier respuesta asincrónica envíe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a99c0-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>

<span data-ttu-id="a99c0-181">Microsoft Edge usa el [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) método del objeto [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) para permitir que la aplicación envíe un [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objeto de nuevo a la extensión.</span><span class="sxs-lookup"><span data-stu-id="a99c0-181">Microsoft Edge uses the [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) object's [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) method to let the app send a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object back to the extension.</span></span>


### <span data-ttu-id="a99c0-182">Límite de tamaño de mensaje</span><span class="sxs-lookup"><span data-stu-id="a99c0-182">Message size limit</span></span>
<span data-ttu-id="a99c0-183">Los mensajes que se envían entre una extensión y una aplicación tienen diferentes limitaciones de tamaño de mensaje para Chrome y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a99c0-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>

<span data-ttu-id="a99c0-184">Chrome tiene las siguientes limitaciones de tamaño de mensaje:</span><span class="sxs-lookup"><span data-stu-id="a99c0-184">Chrome has the following message size limitations:</span></span>
-   <span data-ttu-id="a99c0-185">Límite de mensaje único del host de mensajería nativa: 1 MB</span><span class="sxs-lookup"><span data-stu-id="a99c0-185">Single message limit from native messaging host: 1 MB</span></span>
-   <span data-ttu-id="a99c0-186">Límite de mensaje único enviado al host de mensajería nativo: 4 GB</span><span class="sxs-lookup"><span data-stu-id="a99c0-186">Single message limit sent to native messaging host: 4 GB</span></span>
    
<span data-ttu-id="a99c0-187">Para Microsoft Edge, a pesar de `AppService` que no haya límite en el tamaño de los mensajes (en función de la memoria), Microsoft Edge se protege en sí mismo frente a aplicaciones nativas que imponen los siguientes límites de tamaño de mensaje:</span><span class="sxs-lookup"><span data-stu-id="a99c0-187">For Microsoft Edge, while `AppService` has no limit on message size (dependent on memory), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>
-   <span data-ttu-id="a99c0-188">Un solo límite de mensajes de la aplicación para UWP para la extensión: 1 MB</span><span class="sxs-lookup"><span data-stu-id="a99c0-188">Single message limit from UWP app to extension: 1 MB</span></span>
-   <span data-ttu-id="a99c0-189">Solo límite de mensajes de la extensión a la aplicación para UWP: 100 MB</span><span class="sxs-lookup"><span data-stu-id="a99c0-189">Single message limit from extension to UWP app: 100 MB</span></span>
    
### <span data-ttu-id="a99c0-190">Conexiones de mensajería nativas</span><span class="sxs-lookup"><span data-stu-id="a99c0-190">Native messaging connections</span></span>

<span data-ttu-id="a99c0-191">Existen dos tipos de conexiones para la mensajería instantánea; persistentes y no persistentes.</span><span class="sxs-lookup"><span data-stu-id="a99c0-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>
<span data-ttu-id="a99c0-192">Una conexión **persistente** es una conexión que se mantiene en ejecución hasta que se destruye el puerto.</span><span class="sxs-lookup"><span data-stu-id="a99c0-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span> <span data-ttu-id="a99c0-193">Una conexión **no persistente** es una conexión que se abre para un mensaje a la vez y se cierra después de la entrega.</span><span class="sxs-lookup"><span data-stu-id="a99c0-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>

#### <span data-ttu-id="a99c0-194">Persistente</span><span class="sxs-lookup"><span data-stu-id="a99c0-194">Persistent</span></span>

<span data-ttu-id="a99c0-195">En el caso de Chrome, una conexión persistente se realiza mediante la creación de un puerto de mensajería con [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) .</span><span class="sxs-lookup"><span data-stu-id="a99c0-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="a99c0-196">Una vez que se haya creado el puerto, Chrome inicia un proceso de host de mensajería nativo que sigue ejecutándose hasta el puerto que ha destruido.</span><span class="sxs-lookup"><span data-stu-id="a99c0-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>

<span data-ttu-id="a99c0-197">Para Microsoft Edge, una vez que se crea un puerto de mensajería con `runtime.connectNative` , Microsoft Edge inicia el [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) y lo mantiene en ejecución hasta que se destruya el puerto.</span><span class="sxs-lookup"><span data-stu-id="a99c0-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) and keeps it running until the port is destroyed.</span></span> <span data-ttu-id="a99c0-198">En el siguiente fragmento de código se muestra cómo se establece una conexión persistente desde una aplicación para UWP.</span><span class="sxs-lookup"><span data-stu-id="a99c0-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span> 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <span data-ttu-id="a99c0-199">No persistente</span><span class="sxs-lookup"><span data-stu-id="a99c0-199">Non-persistent</span></span>

<span data-ttu-id="a99c0-200">Cuando se envía un mensaje mediante el uso [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) de Chrome, sin crear un puerto de mensajería, Chrome inicia un nuevo proceso de host de mensajería nativo para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="a99c0-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span> <span data-ttu-id="a99c0-201">El primer mensaje generado por el proceso de host se trata como respuesta a la solicitud original y todos los demás mensajes después de que se pase por alto.</span><span class="sxs-lookup"><span data-stu-id="a99c0-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>

<span data-ttu-id="a99c0-202">Microsoft Edge finalizará la conexión después de que se reciba la respuesta de cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="a99c0-202">Microsoft Edge will terminate the connection after every messages' response has been received.</span></span> <span data-ttu-id="a99c0-203">El siguiente fragmento de código muestra una conexión no persistente establecida con `AppServiceConnection` que se terminará dentro de la aplicación para UWP después de que se haya recibido una solicitud y se haya almacenado como un [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .</span><span class="sxs-lookup"><span data-stu-id="a99c0-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse).</span></span>

```csharp
using (var connection = new AppServiceConnection())
{    
    //Set up a new app service connection
    connection.AppServiceName = "com.microsoft.randomnumbergenerator";
    connection.PackageFamilyName = "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe";
    AppServiceConnectionStatus status = await connection.OpenAsync();
    AppServiceResponse response = await connection.SendMessageAsync(inputs);
}
```  

### <span data-ttu-id="a99c0-204">Permiso</span><span class="sxs-lookup"><span data-stu-id="a99c0-204">Permission</span></span>

<span data-ttu-id="a99c0-205">Para habilitar el uso de mensajería nativa con tu extensión, para Chrome y Microsoft Edge, necesitarás declarar el `"nativeMessaging"` permiso en el `manifest.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="a99c0-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you'll need to declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>

## <span data-ttu-id="a99c0-206">Servicios de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a99c0-206">App services</span></span>
<span data-ttu-id="a99c0-207">Esta sección detalla el impacto que los servicios de la aplicación tienen en el rendimiento y la memoria de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a99c0-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>

### <span data-ttu-id="a99c0-208">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="a99c0-208">Performance</span></span>

<span data-ttu-id="a99c0-209">Los servicios de aplicaciones son "patrocinados" por la aplicación en primer plano que los llama, que para fines de mensajería nativa es Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a99c0-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span> <span data-ttu-id="a99c0-210">Esto significa que los servicios de aplicaciones se pueden ejecutar siempre que se esté ejecutando Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a99c0-210">This means that app services can run as long as Microsoft Edge is running.</span></span>

<span data-ttu-id="a99c0-211">En relación con la latencia, los servicios de aplicaciones usan canalizaciones con nombre que, después de la conexión inicial, permiten que dos aplicaciones se comuniquen directamente.</span><span class="sxs-lookup"><span data-stu-id="a99c0-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span> <span data-ttu-id="a99c0-212">Este método de comunicación produce una latencia baja.</span><span class="sxs-lookup"><span data-stu-id="a99c0-212">This method of communication produces low latency.</span></span> <span data-ttu-id="a99c0-213">Los dispositivos con CPU lentas experimentarán cierta latencia inicial después de iniciar el proceso que hospeda el servicio de aplicaciones (~ 80ms para iniciar la tarea en segundo plano en algunos dispositivos).</span><span class="sxs-lookup"><span data-stu-id="a99c0-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service (~80ms to startup the background task on some devices).</span></span> <span data-ttu-id="a99c0-214">Después del inicio, el rendimiento de los dispositivos de CPU lentos debe ser bueno.</span><span class="sxs-lookup"><span data-stu-id="a99c0-214">After start-up, performance on slow CPU devices should be good.</span></span> 

### <span data-ttu-id="a99c0-215">Memoria</span><span class="sxs-lookup"><span data-stu-id="a99c0-215">Memory</span></span>
<span data-ttu-id="a99c0-216">La memoria asignada a un servicio de aplicaciones se saca de la cuota asignada a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a99c0-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span> <span data-ttu-id="a99c0-217">Esto significa que si Microsoft Edge inicia demasiados servicios de aplicaciones, existe la posibilidad de que se agote la memoria.</span><span class="sxs-lookup"><span data-stu-id="a99c0-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span> <span data-ttu-id="a99c0-218">Los límites de memoria de tareas en segundo plano habituales se aplican en los servicios de aplicación.</span><span class="sxs-lookup"><span data-stu-id="a99c0-218">The usual background task memory caps are enforced on app services.</span></span> <span data-ttu-id="a99c0-219">Por ejemplo, en un dispositivo de 512 MB, una tarea en segundo plano de App Service no puede tener más de 16 MB.</span><span class="sxs-lookup"><span data-stu-id="a99c0-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span> <span data-ttu-id="a99c0-220">Este número sube a medida que los dispositivos se escalan.</span><span class="sxs-lookup"><span data-stu-id="a99c0-220">This number goes up as the devices scale up.</span></span>

## <span data-ttu-id="a99c0-221">Crear una extensión con mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="a99c0-221">Creating an extension with native messaging</span></span>

<span data-ttu-id="a99c0-222">Para poder probar la mensajería nativa, tu extensión necesita un nombre de familia de paquete.</span><span class="sxs-lookup"><span data-stu-id="a99c0-222">In order to test native messaging, your extension needs a Package Family Name.</span></span> <span data-ttu-id="a99c0-223">Microsoft Edge lo usa para determinar la identidad de host del mensaje nativo, lo que significa que se debe empaquetar la extensión.</span><span class="sxs-lookup"><span data-stu-id="a99c0-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span> 

<span data-ttu-id="a99c0-224">Para crear su extensión con mensajería nativa en Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="a99c0-224">To create your extension with native messaging in Visual Studio:</span></span>

1.  <span data-ttu-id="a99c0-225">Crea un proyecto de UWP en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a99c0-225">Create a UWP project in Visual Studio.</span></span>
2.  <span data-ttu-id="a99c0-226">[Agrega `AppService` a tu aplicación para UWP](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="a99c0-226">[Add `AppService` to your UWP app](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>
    -   <span data-ttu-id="a99c0-227">De forma opcional, puedes [configurar `AppService` para que se hospede en la aplicación principal](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) en lugar de hacerlo como una tarea en segundo plano en este momento.</span><span class="sxs-lookup"><span data-stu-id="a99c0-227">You can optionally [configure `AppService` to be hosted in the main app](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>
3.  <span data-ttu-id="a99c0-228">Compila y prueba el proyecto de UWP.</span><span class="sxs-lookup"><span data-stu-id="a99c0-228">Build and test your UWP project.</span></span>
    -   <span data-ttu-id="a99c0-229">Opcionalmente, puede Agregar un [componente de puente de escritorio](#adding-a-desktop-bridge-component).</span><span class="sxs-lookup"><span data-stu-id="a99c0-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>
4.  <span data-ttu-id="a99c0-230">Crea una extensión de Microsoft Edge que usa la mensajería nativa para comunicarse con la aplicación complementaria para UWP.</span><span class="sxs-lookup"><span data-stu-id="a99c0-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span> <span data-ttu-id="a99c0-231">Los archivos de extensión se pueden agregar a una carpeta con `Extension` el nombre del proyecto para UWP.</span><span class="sxs-lookup"><span data-stu-id="a99c0-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span> <span data-ttu-id="a99c0-232">Todos los archivos que están debajo de esta carpeta, incluidas las subcarpetas, deben tener sus propiedades configuradas de esa forma `Build Action=Content` y `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="a99c0-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span> <span data-ttu-id="a99c0-233">Asegúrese `manifest.json` de que también está configurada con estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a99c0-233">Make sure `manifest.json` is also configured with these properties.</span></span>
5.  <span data-ttu-id="a99c0-234">Modifique el `package.manifest.xml` archivo del proyecto para que incluya metadatos de extensión y conviértalo en una aplicación sin encabezado agregando `AppListEntry="none"` :</span><span class="sxs-lookup"><span data-stu-id="a99c0-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>
    
    ```xml
    <Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10" 
    xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities" 
    xmlns:mp="http://schemas.microsoft.com/appx/2014/phone/manifest" 
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10" 
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap uap3 mp rescap build" 
    xmlns:build="http://schemas.microsoft.com/developer/appx/2015/build">

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.15063.0" MaxVersionTested="10.0.15063.0" />
    </Dependencies>

       <Application Id="App" Executable="$targetnametoken$.exe" EntryPoint="NativeMessagingHostInProcess.App">
          <uap:VisualElements AppListEntry="none"
            DisplayName="SecureInput"
            Square150x150Logo="Assets\Square150x150Logo.png"
            Square44x44Logo="Assets\Square44x44Logo.png"
            Description="NativeMessagingHostInProcess"
            BackgroundColor="transparent">
          </uap:VisualElements>
          <Extensions>
            <uap3:Extension Category="windows.appExtension">
                <uap3:AppExtension
                    Name="com.microsoft.edge.extension"
                    Id="EdgeExtension"
                    PublicFolder="Extension"
                    DisplayName="ms-resource:DisplayName">
                </uap3:AppExtension>
            </uap3:Extension>
          </Extensions>
    </Application>
    ```
    
6.  <span data-ttu-id="a99c0-235">Usa el `AppService` nombre configurado para el UWP en las API de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="a99c0-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>
7.  <span data-ttu-id="a99c0-236">Compila e [implementa](#deploying) el proyecto de UWP (con el componente opcional de puente de escritorio).</span><span class="sxs-lookup"><span data-stu-id="a99c0-236">Build and [deploy](#deploying) the UWP project (with the optional Desktop Bridge component).</span></span>
8.  <span data-ttu-id="a99c0-237">[Empaquetar](#packaging) la extensión de mensajería nativa una vez que esté lista para el envío a la tienda</span><span class="sxs-lookup"><span data-stu-id="a99c0-237">[Package](#packaging) your native messaging extension once it's ready for Store submission</span></span>
    
> [!NOTE]
> <span data-ttu-id="a99c0-238">Para obtener un ejemplo de una extensión de mensajería nativa completa, consulte la sección [demos](#demos) .</span><span class="sxs-lookup"><span data-stu-id="a99c0-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>

## <span data-ttu-id="a99c0-239">Agregar un componente de puente de escritorio</span><span class="sxs-lookup"><span data-stu-id="a99c0-239">Adding a Desktop Bridge component</span></span> 
<span data-ttu-id="a99c0-240">Si desea agregar un componente de puente de escritorio al paquete, tendrá que crear y compilar el proyecto Win32 en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a99c0-240">If you want to add a Desktop Bridge component to your package, you'll need to create and build your Win32 project in Visual Studio.</span></span> <span data-ttu-id="a99c0-241">Para obtener información sobre cómo convertir tu aplicación Win32 a UWP, consulta [portar aplicaciones a Windows 10 a través del puente de escritorio](/windows/uwp/porting/desktop-to-uwp-root).</span><span class="sxs-lookup"><span data-stu-id="a99c0-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span> <span data-ttu-id="a99c0-242">Una vez que se ha integrado Visual Studio, puede Agregar el archivo ejecutable de Win32 al paquete siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a99c0-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>

1.  <span data-ttu-id="a99c0-243">Agregue el proyecto Win32 a la misma solución que el proyecto de UWP.</span><span class="sxs-lookup"><span data-stu-id="a99c0-243">Add the Win32 project to the same solution as the UWP project.</span></span> 
2.  <span data-ttu-id="a99c0-244">Establezca el proyecto Win32 como un proyecto dependiente para el proyecto de UWP:</span><span class="sxs-lookup"><span data-stu-id="a99c0-244">Set the Win32 project as a dependent project for the UWP project:</span></span>
    
    ![configurar las dependencias del proyecto](./../media/project-dependencies.PNG)
    
3.  <span data-ttu-id="a99c0-246">Crea una `Win32` carpeta en el proyecto de UWP.</span><span class="sxs-lookup"><span data-stu-id="a99c0-246">Create a `Win32` folder within the UWP project.</span></span> <span data-ttu-id="a99c0-247">Copie los binarios necesarios para el `Win32` proyecto en esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="a99c0-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span> <span data-ttu-id="a99c0-248">Configure las propiedades de todos los binarios `Build Action=Content` `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="a99c0-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>
    
    ![carpeta con archivos de la aplicación para UWP y Win32](./../media/desktop-bridge.png)
    
4.  <span data-ttu-id="a99c0-250">Modifica el archivo de proyecto de UWP para copiar todos los binarios necesarios para el `Win32` proyecto en esta carpeta mediante el comando de evento postbuild.</span><span class="sxs-lookup"><span data-stu-id="a99c0-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span> <span data-ttu-id="a99c0-251">Esto garantiza que los binarios actualizados se copian en la carpeta cada vez que se recompila la solución.</span><span class="sxs-lookup"><span data-stu-id="a99c0-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```
    
5.  <span data-ttu-id="a99c0-252">Modifique `package.manifest.xml` agregando el `<desktop:Extension>` elemento al `<Extensions>` elemento:</span><span class="sxs-lookup"><span data-stu-id="a99c0-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```
    
## <span data-ttu-id="a99c0-253">Implementar</span><span class="sxs-lookup"><span data-stu-id="a99c0-253">Deploying</span></span>
<span data-ttu-id="a99c0-254">Una vez que hayas configurado el proyecto de UWP (y, opcionalmente, un proyecto Win32) como se describe anteriormente, ya puedes implementar la solución con Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a99c0-254">Once you have configured your UWP project (and optionally Win32 project) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>

![proyecto de compilación de InProcess](../media/native-message-uwp-debug.PNG)

<span data-ttu-id="a99c0-256">Una vez que la solución se haya implementado correctamente, deberías ver tu extensión en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a99c0-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>

![se muestra la extensión en Microsoft Edge](../media/secureextension.png)

## <span data-ttu-id="a99c0-258">Empaquetado</span><span class="sxs-lookup"><span data-stu-id="a99c0-258">Packaging</span></span>

> [!NOTE]
> <span data-ttu-id="a99c0-259">El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.</span><span class="sxs-lookup"><span data-stu-id="a99c0-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="a99c0-260">Póngase en [contacto con nosotros](https://aka.ms/extension-request) con sus solicitudes para formar parte de Microsoft Store y le daremos una actualización futura.</span><span class="sxs-lookup"><span data-stu-id="a99c0-260">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>

<span data-ttu-id="a99c0-261">Puedes generar un paquete de tienda para enviarlo al centro de desarrollo de Windows con la funcionalidad integrada de Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="a99c0-261">You can generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>

![Creando el paquete de la tienda](../media/create-store-package.PNG)

## <span data-ttu-id="a99c0-263">Depuración</span><span class="sxs-lookup"><span data-stu-id="a99c0-263">Debugging</span></span>
<span data-ttu-id="a99c0-264">Las instrucciones para la depuración varían según el componente que desea probar:</span><span class="sxs-lookup"><span data-stu-id="a99c0-264">The instructions for debugging vary depending on which component you want to test out:</span></span>

### <span data-ttu-id="a99c0-265">Depurar la extensión</span><span class="sxs-lookup"><span data-stu-id="a99c0-265">Debugging the extension</span></span>
<span data-ttu-id="a99c0-266">Una vez implementada la solución, la extensión se instalará en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a99c0-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span> <span data-ttu-id="a99c0-267">Consulte la guía de [depuración](./debugging-extensions.md) para obtener información sobre cómo depurar una extensión.</span><span class="sxs-lookup"><span data-stu-id="a99c0-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>


### <span data-ttu-id="a99c0-268">Depurar la aplicación para UWP</span><span class="sxs-lookup"><span data-stu-id="a99c0-268">Debugging the UWP app</span></span>
<span data-ttu-id="a99c0-269">La aplicación para UWP se iniciará cuando la extensión intente conectarse a ella mediante las [API de mensajería nativa](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span><span class="sxs-lookup"><span data-stu-id="a99c0-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="a99c0-270">Solo tendrás que depurar la aplicación para UWP una vez que se inicie el proceso.</span><span class="sxs-lookup"><span data-stu-id="a99c0-270">You'll need to debug the UWP app only once the process starts.</span></span> <span data-ttu-id="a99c0-271">Puede configurarse mediante la página de propiedades del proyecto:</span><span class="sxs-lookup"><span data-stu-id="a99c0-271">This can be configured via the project's Property page:</span></span>

1.  <span data-ttu-id="a99c0-272">En Visual Studio, haz clic con el botón derecho en el proyecto de la aplicación para UWP</span><span class="sxs-lookup"><span data-stu-id="a99c0-272">In Visual Studio, right click your UWP app project</span></span>
2.  <span data-ttu-id="a99c0-273">Seleccione propiedades</span><span class="sxs-lookup"><span data-stu-id="a99c0-273">Select Properties</span></span>
3.  <span data-ttu-id="a99c0-274">Active "no iniciar, pero depure mi código cuando se inicie"</span><span class="sxs-lookup"><span data-stu-id="a99c0-274">Check "Do not launch, but debug my code when it starts"</span></span>
    
    ![selección de la casilla no iniciar](../media/native-message-do-not-launch.png)
    
<span data-ttu-id="a99c0-276">En Visual Studio, ahora puedes establecer puntos de interrupción en el código en el que quieras depurar y, a continuación, iniciar el depurador presionando F5.</span><span class="sxs-lookup"><span data-stu-id="a99c0-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span> <span data-ttu-id="a99c0-277">Una vez que interactúes con la extensión para conectarte a la aplicación para UWP, Visual Studio se asociará automáticamente al proceso.</span><span class="sxs-lookup"><span data-stu-id="a99c0-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>

### <span data-ttu-id="a99c0-278">Depurar el puente de escritorio</span><span class="sxs-lookup"><span data-stu-id="a99c0-278">Debugging the Desktop Bridge</span></span>
<span data-ttu-id="a99c0-279">Aunque hay varios [métodos para depurar un puente de escritorio](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (aplicación Win32 convertida), la única opción aplicable para este escenario es la opción PLMDebug.</span><span class="sxs-lookup"><span data-stu-id="a99c0-279">Even though there are various [methods for debugging a Desktop Bridge](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (converted Win32 app), the only one applicable for this scenarios is the PLMDebug option.</span></span> <span data-ttu-id="a99c0-280">También puede agregar código de depuración a la función de inicio para realizar una espera durante un tiempo específico, lo que le permite adjuntar Visual Studio al proceso.</span><span class="sxs-lookup"><span data-stu-id="a99c0-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>
