---
description: Obtén información sobre cómo puedes usar la mensajería nativa para que tu extensión se comunique con una aplicación para UWP complementaria.
title: Mensajes nativos | Extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, native, messaging, uwp
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d9a306055b8f86b92aa5c3e7cd6de44f2386307d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399361"
---
# <a name="native-messaging-in-microsoft-edge"></a><span data-ttu-id="6de3b-104">Mensajería nativa en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6de3b-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a><span data-ttu-id="6de3b-105">Introducción a la arquitectura de mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="6de3b-105">Native messaging architecture overview</span></span>  

<span data-ttu-id="6de3b-106">Con Windows 10 Creators Update, las extensiones de Microsoft Edge pueden usar la mensajería nativa para comunicarse con una aplicación complementaria de la Plataforma universal de Windows \(UWP\).</span><span class="sxs-lookup"><span data-stu-id="6de3b-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform \(UWP\) app.</span></span>  <span data-ttu-id="6de3b-107">En un nivel alto, las extensiones de Microsoft Edge usan las mismas API para mensajería nativa que las extensiones de Chrome y Firefox.</span><span class="sxs-lookup"><span data-stu-id="6de3b-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span>  <span data-ttu-id="6de3b-108">Sin embargo, el host de mensajería nativa tendrá que implementarse con la Plataforma universal de Windows.</span><span class="sxs-lookup"><span data-stu-id="6de3b-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>  

> [!NOTE]
> <span data-ttu-id="6de3b-109">El método descrito a continuación \(conectarse a una aplicación para UWP a través de AppService\) es el único mecanismo admitido para habilitar la comunicación entre las extensiones de Microsoft Edge y los componentes nativos.</span><span class="sxs-lookup"><span data-stu-id="6de3b-109">The method outlined below \(connecting to a UWP app via AppService\) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span>  <span data-ttu-id="6de3b-110">Consulte la sección Agregar un componente [de puente](#adding-a-desktop-bridge-component) de escritorio de esta guía para obtener más información sobre cómo habilitar la comunicación con componentes win32 heredados.</span><span class="sxs-lookup"><span data-stu-id="6de3b-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span>  

<span data-ttu-id="6de3b-111">La arquitectura de mensajería nativa de Microsoft Edge aprovecha la API existente como la infraestructura subyacente de comunicación entre procesos [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(IPC\).</span><span class="sxs-lookup"><span data-stu-id="6de3b-111">The native messaging architecture in Microsoft Edge leverages the existing [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API as the underlying inter-process communication \(IPC\) infrastructure.</span></span>  <span data-ttu-id="6de3b-112">Las aplicaciones para UWP usan `AppService` la API para comunicarse entre sí.</span><span class="sxs-lookup"><span data-stu-id="6de3b-112">UWP apps use the `AppService` API to communicate with one another.</span></span>  <span data-ttu-id="6de3b-113">Debido a esto, las extensiones de Microsoft Edge ahora pueden comunicarse con aplicaciones para UWP.</span><span class="sxs-lookup"><span data-stu-id="6de3b-113">Because of this, Microsoft Edge extensions are now able to communicate with UWP apps.</span></span>  

![arquitectura de mensajería nativa](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a><span data-ttu-id="6de3b-115">Cuándo y cuándo no usar mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="6de3b-115">When and when not to use native messaging</span></span>  

<span data-ttu-id="6de3b-116">La mensajería nativa agrega una nueva capa completa a la extensión.</span><span class="sxs-lookup"><span data-stu-id="6de3b-116">Native messaging adds a whole new layer to your extension.</span></span>  <span data-ttu-id="6de3b-117">Al implementar una aplicación complementaria para UWP para tu extensión, las siguientes posibilidades estarán disponibles para ti:</span><span class="sxs-lookup"><span data-stu-id="6de3b-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>  

*   <span data-ttu-id="6de3b-118">Sincronizar datos \(por ejemplo credenciales\) con una aplicación para UWP complementaria.</span><span class="sxs-lookup"><span data-stu-id="6de3b-118">Synchronize data \(for example credentials\) with a companion UWP app.</span></span>  
*   <span data-ttu-id="6de3b-119">Implemente algoritmos de cifrado y descifrado más fuertes que no estén disponibles en las API web.</span><span class="sxs-lookup"><span data-stu-id="6de3b-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>  
*   <span data-ttu-id="6de3b-120">Acceder a recursos que no son accesibles a través de API web, por ejemplo hardware o dispositivos USB</span><span class="sxs-lookup"><span data-stu-id="6de3b-120">Access resources that are not accessible through web APIs, for example hardware or USB devices</span></span>  

<span data-ttu-id="6de3b-121">Hay algunos casos en los que la mensajería nativa no debe usarse debido a restricciones de seguridad o directivas:</span><span class="sxs-lookup"><span data-stu-id="6de3b-121">There are a few instances where native messaging should not be used due to security or policy restrictions:</span></span>  

*   <span data-ttu-id="6de3b-122">Modificar la configuración del usuario en Microsoft Edge o Windows, por ejemplo, cambiar el explorador predeterminado o el proveedor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="6de3b-122">Modifying user settings in either Microsoft Edge or Windows, for example changing the default browser or search provider.</span></span>  
*   <span data-ttu-id="6de3b-123">Acciones que infringen las directivas de Microsoft Store para aplicaciones y extensiones.</span><span class="sxs-lookup"><span data-stu-id="6de3b-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>  
*   <span data-ttu-id="6de3b-124">Transferir datos al extremo remoto a través del host de mensajes nativo.</span><span class="sxs-lookup"><span data-stu-id="6de3b-124">Transferring data to remote endpoint via native message host.</span></span>  
*   <span data-ttu-id="6de3b-125">Permitir que otras aplicaciones descarguen contenido que cambie el comportamiento de extensión.</span><span class="sxs-lookup"><span data-stu-id="6de3b-125">Allowing other apps to download content that changes extension behavior.</span></span>  

## <a name="demos"></a><span data-ttu-id="6de3b-126">Demos</span><span class="sxs-lookup"><span data-stu-id="6de3b-126">Demos</span></span>  

<span data-ttu-id="6de3b-127">Para obtener una sensación de lo que es una extensión de mensajería nativa de Microsoft Edge que tiene una aplicación para UWP complementaria y un puente de escritorio, consulta los ejemplos [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) y [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) en GitHub.</span><span class="sxs-lookup"><span data-stu-id="6de3b-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>  

### <a name="how-it-works"></a><span data-ttu-id="6de3b-128">Cómo funciona</span><span class="sxs-lookup"><span data-stu-id="6de3b-128">How it works</span></span>  

<span data-ttu-id="6de3b-129">El componente de extensión de Microsoft Edge del ejemplo usa su script de contenido para detectar cuándo un usuario escribe información que debe cifrarse.</span><span class="sxs-lookup"><span data-stu-id="6de3b-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span>  <span data-ttu-id="6de3b-130">La extensión lo comunica al componente puente de escritorio a través de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="6de3b-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span>  <span data-ttu-id="6de3b-131">Cuando el usuario esté listo para enviar los datos, la extensión devolverá un valor cifrado al sitio web.</span><span class="sxs-lookup"><span data-stu-id="6de3b-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>  

> [!NOTE]
> <span data-ttu-id="6de3b-132">Este ejemplo solo funcionará en una página web que use eventos personalizados para comunicarse con el script de contenido de la extensión.</span><span class="sxs-lookup"><span data-stu-id="6de3b-132">This sample will only work on a webpage that uses custom events to communicate with the content script of the extension.</span></span>  <span data-ttu-id="6de3b-133">La carpeta de ejemplo incluye [un archivo .html](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) con el que probar la extensión.</span><span class="sxs-lookup"><span data-stu-id="6de3b-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>  

<span data-ttu-id="6de3b-134">En este ejemplo, la aplicación para UWP se usa para pasar respuestas del Puente de escritorio a Microsoft Edge, que luego se envía a la extensión de Microsoft Edge mediante devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6de3b-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span>  <span data-ttu-id="6de3b-135">Aunque en este ejemplo se ejecuta el host de mensajería nativa en la aplicación principal, también puede ejecutarse como una tarea en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6de3b-135">While this example has the native messaging host run in the main app, it is also able to run as a background task.</span></span>  <span data-ttu-id="6de3b-136">Cambiar entre los dos requiere editar el script en segundo plano de la extensión, cambiando la cadena dentro `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` a `"NativeMessagingHostOutOfProcess"` .</span><span class="sxs-lookup"><span data-stu-id="6de3b-136">Switching between the two requires editing the background script of the extension, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>  

## <a name="chrome-vs-microsoft-edge-implementation"></a><span data-ttu-id="6de3b-137">Implementación de Chrome vs Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6de3b-137">Chrome vs Microsoft Edge implementation</span></span>  

<span data-ttu-id="6de3b-138">Aunque Chrome va por la ruta de usar API de paso de mensajes para que sus extensiones se comuniquen con aplicaciones, Microsoft Edge usa la API que ahora permite que las extensiones de Microsoft Edge y las aplicaciones para UWP se [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) comuniquen.</span><span class="sxs-lookup"><span data-stu-id="6de3b-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>  

<span data-ttu-id="6de3b-139">En esta sección se detallan las diferencias entre el modo en que Chrome y Microsoft Edge controlan la implementación de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="6de3b-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>  

### <a name="registration-and-host-manifest"></a><span data-ttu-id="6de3b-140">Manifiesto de registro y host</span><span class="sxs-lookup"><span data-stu-id="6de3b-140">Registration and host manifest</span></span>  

<span data-ttu-id="6de3b-141">Para que tu aplicación sea reconocida por la extensión como un host de mensajería nativa, tendrá que registrarse.</span><span class="sxs-lookup"><span data-stu-id="6de3b-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>  

<span data-ttu-id="6de3b-142">Para el registro de host de mensajería nativa de [Chrome,](https://developer.chrome.com/extensions/nativeMessaging) la aplicación debe instalar un archivo de manifiesto en cualquier lugar del sistema de archivos de Windows que defina la configuración del host de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="6de3b-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>  

<span data-ttu-id="6de3b-143">El siguiente JSON es un ejemplo de configuración para el archivo de configuración:</span><span class="sxs-lookup"><span data-stu-id="6de3b-143">The following JSON is an example of settings for the config file:</span></span>  

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

<span data-ttu-id="6de3b-144">Para instalar este archivo, la aplicación tendría que:</span><span class="sxs-lookup"><span data-stu-id="6de3b-144">To install this file, the app would need to:</span></span>  

1.  <span data-ttu-id="6de3b-145">Registre el archivo de manifiesto en una ubicación predefinida en el Registro que defina la configuración del host:</span><span class="sxs-lookup"><span data-stu-id="6de3b-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        <span data-ttu-id="6de3b-146">or</span><span class="sxs-lookup"><span data-stu-id="6de3b-146">or</span></span>  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  <span data-ttu-id="6de3b-147">Establezca el valor predeterminado de esa clave en la ruta de acceso completa al archivo de manifiesto, por ejemplo</span><span class="sxs-lookup"><span data-stu-id="6de3b-147">Set the default value of that key to the full path to the manifest file, for example</span></span> `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

<span data-ttu-id="6de3b-148">Para Microsoft Edge, para registrar un \(host de mensajería nativa\) debes incluir la aplicación complementaria para UWP en el mismo paquete que la extensión y especificar la extensión AppService en el archivo de tu [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) [](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) `Package.appxmanifest` proyecto.</span><span class="sxs-lookup"><span data-stu-id="6de3b-148">For Microsoft Edge, in order to register an [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(native messaging host\) you must include the UWP companion app in the same package as your extension and specify the [AppService extension](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in the `Package.appxmanifest` file of your project.</span></span>  <span data-ttu-id="6de3b-149">El `EntryPoint` usuario puede configurar los atributos `Name` y:</span><span class="sxs-lookup"><span data-stu-id="6de3b-149">The `EntryPoint` and `Name` attributes may be configured by you:</span></span>  

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

<span data-ttu-id="6de3b-150">También debe establecer qué extensiones pueden conectarse al servicio.</span><span class="sxs-lookup"><span data-stu-id="6de3b-150">You also need to set which extensions are allowed to connect to the service.</span></span>  <span data-ttu-id="6de3b-151">Dado que Microsoft Edge no tiene una propiedad de manifiesto equivalente en su AppxManifest, la aplicación para UWP deberá determinarlo y aplicarlo en tiempo de `"allowed_origins"` ejecución.</span><span class="sxs-lookup"><span data-stu-id="6de3b-151">Because Microsoft Edge does not have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span>  <span data-ttu-id="6de3b-152">Dado que Microsoft Edge establece la conexión en nombre de la extensión, la aplicación busca el nombre de familia del paquete del autor de la llamada para determinar si Microsoft Edge está conectando la extensión para controlar o autenticar al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6de3b-152">Since Microsoft Edge establishes the connection on behalf of the extension, the app looks up the Package Family Name of the caller to determine if extension is being connected by Microsoft Edge to control or authenticate the caller.</span></span>  <span data-ttu-id="6de3b-153">Por ejemplo</span><span class="sxs-lookup"><span data-stu-id="6de3b-153">For example</span></span>   

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

### <a name="message-sending"></a><span data-ttu-id="6de3b-154">Envío de mensajes</span><span class="sxs-lookup"><span data-stu-id="6de3b-154">Message sending</span></span>  

<span data-ttu-id="6de3b-155">Para que una aplicación y una extensión se comuniquen entre sí, los mensajes deben enviarse a y desde ellos.</span><span class="sxs-lookup"><span data-stu-id="6de3b-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>  

<span data-ttu-id="6de3b-156">Las extensiones de Chrome inician un mensaje con la API para entregar un mensaje al [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) host nativo mediante un canal no persistente.</span><span class="sxs-lookup"><span data-stu-id="6de3b-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span>  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

<span data-ttu-id="6de3b-157">El primer parámetro es el nombre del host nativo, que Chrome busca en el Registro para el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="6de3b-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span>  <span data-ttu-id="6de3b-158">El manifiesto especifica el .exe que Chrome iniciará en un espacio aislado y el mensaje se envía mediante std i/o.</span><span class="sxs-lookup"><span data-stu-id="6de3b-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span>  
<span data-ttu-id="6de3b-159">Las extensiones también establecen un canal persistente mediante la API, que toma el nombre `runtime.connectNative` del host nativo como el único parámetro.</span><span class="sxs-lookup"><span data-stu-id="6de3b-159">Extensions also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span>  

<span data-ttu-id="6de3b-160">Microsoft Edge usa la misma construcción que la API de mensajería nativa en Chrome para permitir que las extensiones de Microsoft Edge especifiquen a qué servicio de aplicaciones se debe conectar.</span><span class="sxs-lookup"><span data-stu-id="6de3b-160">Microsoft Edge uses the same construct as the native messaging API in Chrome to allow Microsoft Edge extensions to specify which app service to connect to.</span></span>  <span data-ttu-id="6de3b-161">El primer parámetro de `runtime.sendNativeMessage` especifica el nombre del servicio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6de3b-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span>  <span data-ttu-id="6de3b-162">En la [sección Registro y manifiesto de host,](#registration-and-host-manifest) se trata de `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="6de3b-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span>  <span data-ttu-id="6de3b-163">La plataforma de extensión de Microsoft Edge restringe el host de mensajería nativa a ser una aplicación para UWP que se empaqueta en el mismo AppX que la extensión.</span><span class="sxs-lookup"><span data-stu-id="6de3b-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span>  <span data-ttu-id="6de3b-164">Esto mitiga los riesgos de seguridad asociados con ataques malintencionados que intenten conectar Microsoft Edge con otro nombre de familia de paquetes mediante la manipulación de entradas de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="6de3b-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span>  

<span data-ttu-id="6de3b-165">Esto significa que Microsoft Edge usará el mismo nombre de familia de paquete que la extensión, además del nombre especificado en la API, para identificar de forma única al proveedor del `AppService` servicio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6de3b-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="6de3b-166">Microsoft [Edge Extension Toolkit](./porting-chrome-extensions.md)no lo convertirá fácilmente.</span><span class="sxs-lookup"><span data-stu-id="6de3b-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span>  <span data-ttu-id="6de3b-167">Las extensiones que especifiquen el permiso se marcarán como que requieren conversión `"nativeMessaging"` manual para este componente.</span><span class="sxs-lookup"><span data-stu-id="6de3b-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>  

### <a name="communication-protocol"></a><span data-ttu-id="6de3b-168">Protocolo de comunicación</span><span class="sxs-lookup"><span data-stu-id="6de3b-168">Communication protocol</span></span>  

<span data-ttu-id="6de3b-169">El protocolo de comunicación para mensajería nativa determina cómo se formatear los mensajes antes de enviarlos.</span><span class="sxs-lookup"><span data-stu-id="6de3b-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>  

<span data-ttu-id="6de3b-170">Chrome inicia cada host de mensajería nativa en un proceso independiente y se comunica con él mediante entrada estándar y salida estándar.</span><span class="sxs-lookup"><span data-stu-id="6de3b-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span>  <span data-ttu-id="6de3b-171">El mismo formato se usa para enviar mensajes en ambas direcciones: cada mensaje se serializa con JSON, utf-8 codificado y se precede con longitud de mensaje de 32 bits en orden de bytes nativo.</span><span class="sxs-lookup"><span data-stu-id="6de3b-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>  

<span data-ttu-id="6de3b-172">Para Microsoft Edge, la plataforma inicia la tarea en segundo plano o la aplicación principal que implementa el servicio de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6de3b-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span>  <span data-ttu-id="6de3b-173">Al iniciar, se `Run` invoca el método de la tarea en segundo plano:</span><span class="sxs-lookup"><span data-stu-id="6de3b-173">On startup, the `Run` method of the background task is invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service is not stopped and ended.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```  

<span data-ttu-id="6de3b-174">Cuando la extensión envía un mensaje a la aplicación para UWP, se genera [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) el evento.</span><span class="sxs-lookup"><span data-stu-id="6de3b-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) event will be raised.</span></span>  <span data-ttu-id="6de3b-175">A continuación, este mensaje con formato JSON se en stringified en el primer par KeyValue de un [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) objeto.</span><span class="sxs-lookup"><span data-stu-id="6de3b-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object.</span></span>  <span data-ttu-id="6de3b-176">:</span><span class="sxs-lookup"><span data-stu-id="6de3b-176">:</span></span>  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

<span data-ttu-id="6de3b-177">Cuando la aplicación para UWP envía una respuesta a la extensión, se agregará una al [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) `ValueSet` objeto.</span><span class="sxs-lookup"><span data-stu-id="6de3b-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) will be added to the `ValueSet` object.</span></span>  <span data-ttu-id="6de3b-178">Microsoft `Key` Edge omitirá la propiedad, pero la propiedad `Value` contendrá una cadena JSON válida.</span><span class="sxs-lookup"><span data-stu-id="6de3b-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>  

### <a name="callback"></a><span data-ttu-id="6de3b-179">Devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="6de3b-179">Callback</span></span>  

<span data-ttu-id="6de3b-180">Para las devoluciones de llamada, Chrome usa lo que permite que una función de devolución de llamada controle cualquier [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) respuesta asincrónica al enviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="6de3b-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>  

<span data-ttu-id="6de3b-181">Microsoft Edge usa el método del objeto para permitir que la [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) aplicación envíe un objeto de vuelta a la [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) extensión.</span><span class="sxs-lookup"><span data-stu-id="6de3b-181">Microsoft Edge uses the [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) method  of the [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) object to let the app send a [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) object back to the extension.</span></span>  

### <a name="message-size-limit"></a><span data-ttu-id="6de3b-182">Límite de tamaño de mensaje</span><span class="sxs-lookup"><span data-stu-id="6de3b-182">Message size limit</span></span>  

<span data-ttu-id="6de3b-183">Los mensajes que se envían de ida y vuelta entre una extensión y una aplicación tienen limitaciones de tamaño de mensaje diferentes para Chrome y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6de3b-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>  

<span data-ttu-id="6de3b-184">Chrome tiene las siguientes limitaciones de tamaño de mensaje:</span><span class="sxs-lookup"><span data-stu-id="6de3b-184">Chrome has the following message size limitations:</span></span>  

*   <span data-ttu-id="6de3b-185">Límite de mensaje único del host de mensajería nativa: 1 MB</span><span class="sxs-lookup"><span data-stu-id="6de3b-185">Single message limit from native messaging host:  1 MB</span></span>  
*   <span data-ttu-id="6de3b-186">Límite de mensaje único enviado al host de mensajería nativa: 4 GB</span><span class="sxs-lookup"><span data-stu-id="6de3b-186">Single message limit sent to native messaging host:  4 GB</span></span>  

<span data-ttu-id="6de3b-187">Para Microsoft Edge, aunque no tiene límite en el tamaño del mensaje \(dependiente de la memoria\), Microsoft Edge se protege contra el mal comportamiento de las aplicaciones nativas imponiendo los siguientes límites de tamaño de `AppService` mensaje:</span><span class="sxs-lookup"><span data-stu-id="6de3b-187">For Microsoft Edge, while `AppService` has no limit on message size \(dependent on memory\), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>  

*   <span data-ttu-id="6de3b-188">Límite de mensaje único de la aplicación para UWP a la extensión: 1 MB</span><span class="sxs-lookup"><span data-stu-id="6de3b-188">Single message limit from UWP app to extension: 1 MB</span></span>  
*   <span data-ttu-id="6de3b-189">Límite de mensaje único de extensión a aplicación para UWP: 100 MB</span><span class="sxs-lookup"><span data-stu-id="6de3b-189">Single message limit from extension to UWP app: 100 MB</span></span>  

### <a name="native-messaging-connections"></a><span data-ttu-id="6de3b-190">Conexiones de mensajería nativas</span><span class="sxs-lookup"><span data-stu-id="6de3b-190">Native messaging connections</span></span>  

<span data-ttu-id="6de3b-191">Hay dos tipos de conexiones para mensajería nativa; persistente y no persistente.</span><span class="sxs-lookup"><span data-stu-id="6de3b-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>  
<span data-ttu-id="6de3b-192">Una **conexión** persistente es una conexión que se mantiene en ejecución hasta que se destruye el puerto.</span><span class="sxs-lookup"><span data-stu-id="6de3b-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span>  <span data-ttu-id="6de3b-193">Una **conexión no persistente** es una conexión que se abre para un mensaje a la vez y se cierra después de la entrega.</span><span class="sxs-lookup"><span data-stu-id="6de3b-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>  

#### <a name="persistent"></a><span data-ttu-id="6de3b-194">Persistente</span><span class="sxs-lookup"><span data-stu-id="6de3b-194">Persistent</span></span>  

<span data-ttu-id="6de3b-195">Para Chrome, se crea una conexión persistente mediante la creación de un puerto de mensajería mediante [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) .</span><span class="sxs-lookup"><span data-stu-id="6de3b-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="6de3b-196">Una vez que se realiza el puerto, Chrome inicia un proceso de host de mensajería nativa que sigue ejecutándose hasta el puerto que destruyó.</span><span class="sxs-lookup"><span data-stu-id="6de3b-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>  

<span data-ttu-id="6de3b-197">Para Microsoft Edge, una vez que se crea un puerto de mensajería mediante , Microsoft Edge inicia el y lo mantiene en ejecución hasta que `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) se destruye el puerto.</span><span class="sxs-lookup"><span data-stu-id="6de3b-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) and keeps it running until the port is destroyed.</span></span>  <span data-ttu-id="6de3b-198">El siguiente fragmento de código muestra cómo se establece una conexión persistente desde una aplicación para UWP.</span><span class="sxs-lookup"><span data-stu-id="6de3b-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span>  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a><span data-ttu-id="6de3b-199">No persistente</span><span class="sxs-lookup"><span data-stu-id="6de3b-199">Non-persistent</span></span>  

<span data-ttu-id="6de3b-200">Cuando se envía un mensaje con Chrome, sin crear un puerto de mensajería, Chrome inicia un nuevo proceso de host de mensajería nativa [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) para cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="6de3b-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span>  <span data-ttu-id="6de3b-201">El primer mensaje generado por el proceso host se controla como una respuesta a la solicitud original y todos los demás mensajes después de que se omiten.</span><span class="sxs-lookup"><span data-stu-id="6de3b-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>  

<span data-ttu-id="6de3b-202">Microsoft Edge detiene y finaliza la conexión después de recibir cada respuesta a cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="6de3b-202">Microsoft Edge stops and ends the connection after every response to each message has been received.</span></span>  <span data-ttu-id="6de3b-203">En el siguiente fragmento de código se muestra una conexión no persistente que se establece con la que, a continuación, se finalizará en la aplicación para UWP después de recibir y almacenar una solicitud `AppServiceConnection` como [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="6de3b-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true).</span></span>  

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

### <a name="permission"></a><span data-ttu-id="6de3b-204">Permiso</span><span class="sxs-lookup"><span data-stu-id="6de3b-204">Permission</span></span>  

<span data-ttu-id="6de3b-205">Para habilitar el uso de mensajería nativa con la extensión, tanto para Chrome como para Microsoft Edge, debe declarar el `"nativeMessaging"` permiso en el `manifest.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="6de3b-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you must declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>  

## <a name="app-services"></a><span data-ttu-id="6de3b-206">Servicios de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6de3b-206">App services</span></span>  

<span data-ttu-id="6de3b-207">En esta sección se detalla el impacto que los servicios de aplicaciones tienen en el rendimiento y la memoria de mensajería nativa de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6de3b-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>  

### <a name="performance"></a><span data-ttu-id="6de3b-208">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="6de3b-208">Performance</span></span>  

<span data-ttu-id="6de3b-209">Los servicios de aplicaciones están "patrocinados" por la aplicación en primer plano que los llama, que para fines de mensajería nativa es Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6de3b-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span>  <span data-ttu-id="6de3b-210">Esto significa que los servicios de aplicaciones pueden ejecutarse mientras se ejecute Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6de3b-210">This means that app services can run as long as Microsoft Edge is running.</span></span>  

<span data-ttu-id="6de3b-211">En cuanto a la latencia, los servicios de aplicaciones usan canalizaciones con nombre que, después de la conexión inicial, permiten que dos aplicaciones se comuniquen directamente.</span><span class="sxs-lookup"><span data-stu-id="6de3b-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span>  <span data-ttu-id="6de3b-212">Este método de comunicación produce una latencia baja.</span><span class="sxs-lookup"><span data-stu-id="6de3b-212">This method of communication produces low latency.</span></span>  <span data-ttu-id="6de3b-213">Los dispositivos con CPU lentas experimentarán cierta latencia inicial después de iniciar el proceso que hospeda el servicio de aplicaciones \(~80ms para iniciar la tarea en segundo plano en algunos dispositivos\).</span><span class="sxs-lookup"><span data-stu-id="6de3b-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service \(~80ms to startup the background task on some devices\).</span></span>  <span data-ttu-id="6de3b-214">Después de la puesta en marcha, el rendimiento en dispositivos de CPU lentos debe ser bueno.</span><span class="sxs-lookup"><span data-stu-id="6de3b-214">After start-up, performance on slow CPU devices should be good.</span></span>  

### <a name="memory"></a><span data-ttu-id="6de3b-215">Memoria</span><span class="sxs-lookup"><span data-stu-id="6de3b-215">Memory</span></span>  

<span data-ttu-id="6de3b-216">La memoria asignada a un servicio de aplicaciones se ha quitado de la cuota asignada a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6de3b-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span>  <span data-ttu-id="6de3b-217">Esto significa que si Microsoft Edge inicia demasiados servicios de aplicaciones, existe la posibilidad de que se les pueda quedár la memoria.</span><span class="sxs-lookup"><span data-stu-id="6de3b-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span>  <span data-ttu-id="6de3b-218">Los límites habituales de memoria de tareas en segundo plano se aplican en los servicios de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="6de3b-218">The usual background task memory caps are enforced on app services.</span></span>  <span data-ttu-id="6de3b-219">Por ejemplo, en un dispositivo de 512 MB, una tarea en segundo plano del servicio de aplicaciones no puede tener más de 16 MB.</span><span class="sxs-lookup"><span data-stu-id="6de3b-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span>  <span data-ttu-id="6de3b-220">Este número sube a medida que los dispositivos se escalan hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="6de3b-220">This number goes up as the devices scale up.</span></span>  

## <a name="creating-an-extension-with-native-messaging"></a><span data-ttu-id="6de3b-221">Creación de una extensión con mensajería nativa</span><span class="sxs-lookup"><span data-stu-id="6de3b-221">Creating an extension with native messaging</span></span>  

<span data-ttu-id="6de3b-222">Para probar la mensajería nativa, la extensión necesita un nombre de familia de paquete.</span><span class="sxs-lookup"><span data-stu-id="6de3b-222">In order to test native messaging, your extension needs a Package Family Name.</span></span>  <span data-ttu-id="6de3b-223">Microsoft Edge lo usa para determinar la identidad del host de mensaje nativo, lo que significa que la extensión debe empaquetarse.</span><span class="sxs-lookup"><span data-stu-id="6de3b-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span>  

<span data-ttu-id="6de3b-224">Para crear la extensión con mensajería nativa en Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="6de3b-224">To create your extension with native messaging in Visual Studio:</span></span>  

1.  <span data-ttu-id="6de3b-225">Crea un proyecto para UWP en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6de3b-225">Create a UWP project in Visual Studio.</span></span>  
1.  <span data-ttu-id="6de3b-226">[Agregar `AppService` a la aplicación para UWP](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="6de3b-226">[Add `AppService` to your UWP app](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>  
    *   <span data-ttu-id="6de3b-227">Opcionalmente, puedes [configurar `AppService` para hospedarte en la aplicación principal](/windows/uwp/launch-resume/convert-app-service-in-process) en lugar de como una tarea en segundo plano en este momento.</span><span class="sxs-lookup"><span data-stu-id="6de3b-227">You can optionally [configure `AppService` to be hosted in the main app](/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>  
1.  <span data-ttu-id="6de3b-228">Crea y prueba tu proyecto para UWP.</span><span class="sxs-lookup"><span data-stu-id="6de3b-228">Build and test your UWP project.</span></span>  
    *   <span data-ttu-id="6de3b-229">Opcionalmente, puede agregar un componente [de Puente de escritorio](#adding-a-desktop-bridge-component).</span><span class="sxs-lookup"><span data-stu-id="6de3b-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>  
1.  <span data-ttu-id="6de3b-230">Crea una extensión de Microsoft Edge que usa mensajería nativa para comunicarse con la aplicación complementaria para UWP.</span><span class="sxs-lookup"><span data-stu-id="6de3b-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span>  <span data-ttu-id="6de3b-231">Los archivos de extensión se pueden agregar a una carpeta denominada `Extension` en el proyecto de UWP.</span><span class="sxs-lookup"><span data-stu-id="6de3b-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span>  <span data-ttu-id="6de3b-232">Todos los archivos debajo de esta carpeta, incluidas las subcarpetas, necesitan tener sus propiedades configuradas de tal `Build Action=Content` manera que y `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="6de3b-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  <span data-ttu-id="6de3b-233">Asegúrese de `manifest.json` que también está configurado con estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6de3b-233">Make sure `manifest.json` is also configured with these properties.</span></span>  
1.  <span data-ttu-id="6de3b-234">Modifique el archivo del proyecto para incluir metadatos de extensión y convertirlo en una aplicación sin cabeza `package.manifest.xml` `AppListEntry="none"` agregando :</span><span class="sxs-lookup"><span data-stu-id="6de3b-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>  
    
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
    
1.  <span data-ttu-id="6de3b-235">Usa el `AppService` nombre configurado para la UWP en las API de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="6de3b-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>  
1.  <span data-ttu-id="6de3b-236">Crea e [implementa el](#deploying) proyecto para UWP \(con el componente de puente de escritorio opcional\).</span><span class="sxs-lookup"><span data-stu-id="6de3b-236">Build and [deploy](#deploying) the UWP project \(with the optional Desktop Bridge component\).</span></span>  
1.  <span data-ttu-id="6de3b-237">[Empaquetar](#packaging) la extensión de mensajería nativa una vez que esté lista para el envío de la Tienda</span><span class="sxs-lookup"><span data-stu-id="6de3b-237">[Package](#packaging) your native messaging extension once it is ready for Store submission</span></span>  
    
> [!NOTE]
> <span data-ttu-id="6de3b-238">Haga referencia [a la sección Demos](#demos) para obtener un ejemplo de una extensión de mensajería nativa completa.</span><span class="sxs-lookup"><span data-stu-id="6de3b-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>  

## <a name="adding-a-desktop-bridge-component"></a><span data-ttu-id="6de3b-239">Agregar un componente de puente de escritorio</span><span class="sxs-lookup"><span data-stu-id="6de3b-239">Adding a Desktop Bridge component</span></span>  

<span data-ttu-id="6de3b-240">Si desea agregar un componente de Puente de escritorio al paquete, debe crear y crear el proyecto de Win32 en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6de3b-240">If you want to add a Desktop Bridge component to your package, you must create and build your Win32 project in Visual Studio.</span></span>  <span data-ttu-id="6de3b-241">Para obtener información sobre cómo convertir la aplicación de win32 a UWP, consulta [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span><span class="sxs-lookup"><span data-stu-id="6de3b-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span>  <span data-ttu-id="6de3b-242">Una vez integrado Visual Studio, puede agregar el archivo ejecutable de Win32 al paquete siguiendo los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="6de3b-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>  

1.  <span data-ttu-id="6de3b-243">Agrega el proyecto win32 a la misma solución que el proyecto para UWP.</span><span class="sxs-lookup"><span data-stu-id="6de3b-243">Add the Win32 project to the same solution as the UWP project.</span></span>  
1.  <span data-ttu-id="6de3b-244">Establece el proyecto de Win32 como un proyecto dependiente para el proyecto para UWP:</span><span class="sxs-lookup"><span data-stu-id="6de3b-244">Set the Win32 project as a dependent project for the UWP project:</span></span>  
    
    ![configurar dependencias del proyecto](../media/project-dependencies.png)  
    
1.  <span data-ttu-id="6de3b-246">Crea una `Win32` carpeta dentro del proyecto de UWP.</span><span class="sxs-lookup"><span data-stu-id="6de3b-246">Create a `Win32` folder within the UWP project.</span></span>  <span data-ttu-id="6de3b-247">Copie los archivos binarios necesarios para el `Win32` proyecto en esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="6de3b-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span>  <span data-ttu-id="6de3b-248">Configure las propiedades de todos los archivos binarios de tal `Build Action=Content` manera que y `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="6de3b-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>  
    
    ![carpeta con archivos de aplicaciones para UWP y win32](../media/desktop-bridge.png)  
    
1.  <span data-ttu-id="6de3b-250">Modifique el archivo de proyecto de UWP para copiar todos los archivos binarios necesarios para el proyecto `Win32` en esta carpeta mediante el comando de evento PostBuild.</span><span class="sxs-lookup"><span data-stu-id="6de3b-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span>  <span data-ttu-id="6de3b-251">Esto garantiza que los archivos binarios actualizados se copian en la carpeta cada vez que se recompila la solución.</span><span class="sxs-lookup"><span data-stu-id="6de3b-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  <span data-ttu-id="6de3b-252">Modifique `package.manifest.xml` agregando `<desktop:Extension>` el elemento al `<Extensions>` elemento:</span><span class="sxs-lookup"><span data-stu-id="6de3b-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a><span data-ttu-id="6de3b-253">Implementar</span><span class="sxs-lookup"><span data-stu-id="6de3b-253">Deploying</span></span>  

<span data-ttu-id="6de3b-254">Una vez que haya configurado el proyecto para UWP \(y opcionalmente win32 project\) como se describe anteriormente, estará listo para implementar la solución mediante Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6de3b-254">Once you have configured your UWP project \(and optionally Win32 project\) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>  

![build inprocess project](../media/native-message-uwp-debug.png)  

<span data-ttu-id="6de3b-256">Una vez que la solución se implemente correctamente, debería ver la extensión en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6de3b-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>  

![extensión que se muestra en Microsoft Edge](../media/secureextension.png)  

## <a name="packaging"></a><span data-ttu-id="6de3b-258">Empaquetado</span><span class="sxs-lookup"><span data-stu-id="6de3b-258">Packaging</span></span>  

> [!NOTE]
> <span data-ttu-id="6de3b-259">Enviar una extensión de Microsoft Edge a la Microsoft Store es actualmente una funcionalidad restringida.</span><span class="sxs-lookup"><span data-stu-id="6de3b-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="6de3b-260">[Envíe una solicitud](https://developer.microsoft.com/microsoft-edge/extensions/requests/) para que forme parte de Microsoft Store y que se considere para futuras actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="6de3b-260">[Send a request](https://developer.microsoft.com/microsoft-edge/extensions/requests/) to be a part of the Microsoft Store, and be considered for future updates.</span></span>  

<span data-ttu-id="6de3b-261">Puedes generar un paquete de la Tienda para su envío al Centro de desarrollo de Windows con la funcionalidad Visual Studio integrada:</span><span class="sxs-lookup"><span data-stu-id="6de3b-261">You may generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>  

![Crear paquete de la Tienda](../media/create-store-package.png)  

## <a name="debugging"></a><span data-ttu-id="6de3b-263">Depuración</span><span class="sxs-lookup"><span data-stu-id="6de3b-263">Debugging</span></span>  

<span data-ttu-id="6de3b-264">Las instrucciones para depurar varían en función del componente que desee probar:</span><span class="sxs-lookup"><span data-stu-id="6de3b-264">The instructions for debugging vary depending on which component you want to test out:</span></span>  

### <a name="debugging-the-extension"></a><span data-ttu-id="6de3b-265">Depurar la extensión</span><span class="sxs-lookup"><span data-stu-id="6de3b-265">Debugging the extension</span></span>  

<span data-ttu-id="6de3b-266">Una vez implementada la solución, la extensión se instalará en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6de3b-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span>  <span data-ttu-id="6de3b-267">Consulta la [Guía de depuración](./debugging-extensions.md) para obtener información sobre cómo depurar una extensión.</span><span class="sxs-lookup"><span data-stu-id="6de3b-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>  

### <a name="debugging-the-uwp-app"></a><span data-ttu-id="6de3b-268">Depuración de la aplicación para UWP</span><span class="sxs-lookup"><span data-stu-id="6de3b-268">Debugging the UWP app</span></span>  

<span data-ttu-id="6de3b-269">La aplicación para UWP se iniciará cuando la extensión intente conectarse a ella mediante [API de mensajería nativas.](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)</span><span class="sxs-lookup"><span data-stu-id="6de3b-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span>  <span data-ttu-id="6de3b-270">Solo debes depurar la aplicación para UWP una vez que se inicie el proceso.</span><span class="sxs-lookup"><span data-stu-id="6de3b-270">You must debug the UWP app only once the process starts.</span></span>  <span data-ttu-id="6de3b-271">Esto puede configurarse mediante la página Property del proyecto:</span><span class="sxs-lookup"><span data-stu-id="6de3b-271">This may be configured using the Property page of the project:</span></span>  

1.  <span data-ttu-id="6de3b-272">En Visual Studio, mantenga el mouse en el proyecto de la aplicación para UWP y abra el menú contextual \(hacer clic con el botón secundario\)</span><span class="sxs-lookup"><span data-stu-id="6de3b-272">In Visual Studio, hover on your UWP app project and open the contextual menu \(right-click\)</span></span>  
1.  <span data-ttu-id="6de3b-273">Seleccionar **propiedades**</span><span class="sxs-lookup"><span data-stu-id="6de3b-273">Select **Properties**</span></span>  
1.  <span data-ttu-id="6de3b-274">Comprobar **No iniciar, pero depurar mi código cuando se inicia**</span><span class="sxs-lookup"><span data-stu-id="6de3b-274">Check **Do not launch, but debug my code when it starts**</span></span>  
    
    ![cuadro de selección no iniciar](../media/native-message-do-not-launch.png)  
    
<span data-ttu-id="6de3b-276">En Visual Studio ahora puede establecer puntos de interrupción en el código donde desea depurar y, a continuación, inicie el depurador presionando F5.</span><span class="sxs-lookup"><span data-stu-id="6de3b-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span>  <span data-ttu-id="6de3b-277">Una vez que interactúes con la extensión para conectarte a la aplicación para UWP, Visual Studio se adjuntará automáticamente al proceso.</span><span class="sxs-lookup"><span data-stu-id="6de3b-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>  

### <a name="debugging-the-desktop-bridge"></a><span data-ttu-id="6de3b-278">Depuración del puente de escritorio</span><span class="sxs-lookup"><span data-stu-id="6de3b-278">Debugging the Desktop Bridge</span></span>  

<span data-ttu-id="6de3b-279">Aunque hay varios métodos para depurar un puente de escritorio \(aplicación convertida de Win32\), el único aplicable [para](/windows/msix/desktop/desktop-to-uwp-debug) estos escenarios es la opción PLMDebug.</span><span class="sxs-lookup"><span data-stu-id="6de3b-279">Even though there are various [methods for debugging a Desktop Bridge](/windows/msix/desktop/desktop-to-uwp-debug) \(converted Win32 app\), the only one applicable for this scenarios is the PLMDebug option.</span></span>  <span data-ttu-id="6de3b-280">También puede agregar código de depuración a la función de inicio para realizar una espera durante un tiempo específico, lo que le permite adjuntar Visual Studio al proceso.</span><span class="sxs-lookup"><span data-stu-id="6de3b-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>  
