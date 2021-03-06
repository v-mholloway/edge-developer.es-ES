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
# <a name="native-messaging-in-microsoft-edge"></a>Mensajería nativa en Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <a name="native-messaging-architecture-overview"></a>Introducción a la arquitectura de mensajería nativa  

Con Windows 10 Creators Update, las extensiones de Microsoft Edge pueden usar la mensajería nativa para comunicarse con una aplicación complementaria de la Plataforma universal de Windows \(UWP\).  En un nivel alto, las extensiones de Microsoft Edge usan las mismas API para mensajería nativa que las extensiones de Chrome y Firefox.  Sin embargo, el host de mensajería nativa tendrá que implementarse con la Plataforma universal de Windows.  

> [!NOTE]
> El método descrito a continuación \(conectarse a una aplicación para UWP a través de AppService\) es el único mecanismo admitido para habilitar la comunicación entre las extensiones de Microsoft Edge y los componentes nativos.  Consulte la sección Agregar un componente [de puente](#adding-a-desktop-bridge-component) de escritorio de esta guía para obtener más información sobre cómo habilitar la comunicación con componentes win32 heredados.  

La arquitectura de mensajería nativa de Microsoft Edge aprovecha la API existente como la infraestructura subyacente de comunicación entre procesos [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) \(IPC\).  Las aplicaciones para UWP usan `AppService` la API para comunicarse entre sí.  Debido a esto, las extensiones de Microsoft Edge ahora pueden comunicarse con aplicaciones para UWP.  

![arquitectura de mensajería nativa](../media/native-messaging-architecture.png)  

### <a name="when-and-when-not-to-use-native-messaging"></a>Cuándo y cuándo no usar mensajería nativa  

La mensajería nativa agrega una nueva capa completa a la extensión.  Al implementar una aplicación complementaria para UWP para tu extensión, las siguientes posibilidades estarán disponibles para ti:  

*   Sincronizar datos \(por ejemplo credenciales\) con una aplicación para UWP complementaria.  
*   Implemente algoritmos de cifrado y descifrado más fuertes que no estén disponibles en las API web.  
*   Acceder a recursos que no son accesibles a través de API web, por ejemplo hardware o dispositivos USB  

Hay algunos casos en los que la mensajería nativa no debe usarse debido a restricciones de seguridad o directivas:  

*   Modificar la configuración del usuario en Microsoft Edge o Windows, por ejemplo, cambiar el explorador predeterminado o el proveedor de búsqueda.  
*   Acciones que infringen las directivas de Microsoft Store para aplicaciones y extensiones.  
*   Transferir datos al extremo remoto a través del host de mensajes nativo.  
*   Permitir que otras aplicaciones descarguen contenido que cambie el comportamiento de extensión.  

## <a name="demos"></a>Demos  

Para obtener una sensación de lo que es una extensión de mensajería nativa de Microsoft Edge que tiene una aplicación para UWP complementaria y un puente de escritorio, consulta los ejemplos [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) y [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) en GitHub.  

### <a name="how-it-works"></a>Cómo funciona  

El componente de extensión de Microsoft Edge del ejemplo usa su script de contenido para detectar cuándo un usuario escribe información que debe cifrarse.  La extensión lo comunica al componente puente de escritorio a través de mensajería nativa.  Cuando el usuario esté listo para enviar los datos, la extensión devolverá un valor cifrado al sitio web.  

> [!NOTE]
> Este ejemplo solo funcionará en una página web que use eventos personalizados para comunicarse con el script de contenido de la extensión.  La carpeta de ejemplo incluye [un archivo .html](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) con el que probar la extensión.  

En este ejemplo, la aplicación para UWP se usa para pasar respuestas del Puente de escritorio a Microsoft Edge, que luego se envía a la extensión de Microsoft Edge mediante devolución de llamada.  Aunque en este ejemplo se ejecuta el host de mensajería nativa en la aplicación principal, también puede ejecutarse como una tarea en segundo plano.  Cambiar entre los dos requiere editar el script en segundo plano de la extensión, cambiando la cadena dentro `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` a `"NativeMessagingHostOutOfProcess"` .  

## <a name="chrome-vs-microsoft-edge-implementation"></a>Implementación de Chrome vs Microsoft Edge  

Aunque Chrome va por la ruta de usar API de paso de mensajes para que sus extensiones se comuniquen con aplicaciones, Microsoft Edge usa la API que ahora permite que las extensiones de Microsoft Edge y las aplicaciones para UWP se [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) comuniquen.  

En esta sección se detallan las diferencias entre el modo en que Chrome y Microsoft Edge controlan la implementación de mensajería nativa.  

### <a name="registration-and-host-manifest"></a>Manifiesto de registro y host  

Para que tu aplicación sea reconocida por la extensión como un host de mensajería nativa, tendrá que registrarse.  

Para el registro de host de mensajería nativa de [Chrome,](https://developer.chrome.com/extensions/nativeMessaging) la aplicación debe instalar un archivo de manifiesto en cualquier lugar del sistema de archivos de Windows que defina la configuración del host de mensajería nativa.  

El siguiente JSON es un ejemplo de configuración para el archivo de configuración:  

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

Para instalar este archivo, la aplicación tendría que:  

1.  Registre el archivo de manifiesto en una ubicación predefinida en el Registro que defina la configuración del host:  
    *   `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
        or  
    *   `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`  
        
1.  Establezca el valor predeterminado de esa clave en la ruta de acceso completa al archivo de manifiesto, por ejemplo `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`  

Para Microsoft Edge, para registrar un \(host de mensajería nativa\) debes incluir la aplicación complementaria para UWP en el mismo paquete que la extensión y especificar la extensión AppService en el archivo de tu [`AppService`](/uwp/api/Windows.ApplicationModel.AppService?view=winrt-19041&preserve-view=true) [](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) `Package.appxmanifest` proyecto.  El `EntryPoint` usuario puede configurar los atributos `Name` y:  

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

También debe establecer qué extensiones pueden conectarse al servicio.  Dado que Microsoft Edge no tiene una propiedad de manifiesto equivalente en su AppxManifest, la aplicación para UWP deberá determinarlo y aplicarlo en tiempo de `"allowed_origins"` ejecución.  Dado que Microsoft Edge establece la conexión en nombre de la extensión, la aplicación busca el nombre de familia del paquete del autor de la llamada para determinar si Microsoft Edge está conectando la extensión para controlar o autenticar al autor de la llamada.  Por ejemplo   

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

### <a name="message-sending"></a>Envío de mensajes  

Para que una aplicación y una extensión se comuniquen entre sí, los mensajes deben enviarse a y desde ellos.  

Las extensiones de Chrome inician un mensaje con la API para entregar un mensaje al [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) host nativo mediante un canal no persistente.  

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```  

El primer parámetro es el nombre del host nativo, que Chrome busca en el Registro para el manifiesto.  El manifiesto especifica el .exe que Chrome iniciará en un espacio aislado y el mensaje se envía mediante std i/o.  
Las extensiones también establecen un canal persistente mediante la API, que toma el nombre `runtime.connectNative` del host nativo como el único parámetro.  

Microsoft Edge usa la misma construcción que la API de mensajería nativa en Chrome para permitir que las extensiones de Microsoft Edge especifiquen a qué servicio de aplicaciones se debe conectar.  El primer parámetro de `runtime.sendNativeMessage` especifica el nombre del servicio de aplicaciones.  En la [sección Registro y manifiesto de host,](#registration-and-host-manifest) se trata de `"com.microsoft.inventory"` .  La plataforma de extensión de Microsoft Edge restringe el host de mensajería nativa a ser una aplicación para UWP que se empaqueta en el mismo AppX que la extensión.  Esto mitiga los riesgos de seguridad asociados con ataques malintencionados que intenten conectar Microsoft Edge con otro nombre de familia de paquetes mediante la manipulación de entradas de manifiesto.  

Esto significa que Microsoft Edge usará el mismo nombre de familia de paquete que la extensión, además del nombre especificado en la API, para identificar de forma única al proveedor del `AppService` servicio de aplicaciones.  

> [!NOTE]
> Microsoft [Edge Extension Toolkit](./porting-chrome-extensions.md)no lo convertirá fácilmente.  Las extensiones que especifiquen el permiso se marcarán como que requieren conversión `"nativeMessaging"` manual para este componente.  

### <a name="communication-protocol"></a>Protocolo de comunicación  

El protocolo de comunicación para mensajería nativa determina cómo se formatear los mensajes antes de enviarlos.  

Chrome inicia cada host de mensajería nativa en un proceso independiente y se comunica con él mediante entrada estándar y salida estándar.  El mismo formato se usa para enviar mensajes en ambas direcciones: cada mensaje se serializa con JSON, utf-8 codificado y se precede con longitud de mensaje de 32 bits en orden de bytes nativo.  

Para Microsoft Edge, la plataforma inicia la tarea en segundo plano o la aplicación principal que implementa el servicio de aplicaciones.  Al iniciar, se `Run` invoca el método de la tarea en segundo plano:  

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

Cuando la extensión envía un mensaje a la aplicación para UWP, se genera [`onRequestReceived`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) el evento.  A continuación, este mensaje con formato JSON se en stringified en el primer par KeyValue de un [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) objeto.  :  

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```  

Cuando la aplicación para UWP envía una respuesta a la extensión, se agregará una al [`KeyValuePair`](/dotnet/api/system.collections.generic.keyvaluepair-2?view=netcore-3.1&preserve-view=true) `ValueSet` objeto.  Microsoft `Key` Edge omitirá la propiedad, pero la propiedad `Value` contendrá una cadena JSON válida.  

### <a name="callback"></a>Devolución de llamada  

Para las devoluciones de llamada, Chrome usa lo que permite que una función de devolución de llamada controle cualquier [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) respuesta asincrónica al enviar un mensaje.  

Microsoft Edge usa el método del objeto para permitir que la [`SendResponseAsync`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) aplicación envíe un objeto de vuelta a la [`AppServiceRequest`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceRequest?view=winrt-19041&preserve-view=true) [`ValueSet`](/uwp/api/Windows.Foundation.Collections.ValueSet?view=winrt-19041&preserve-view=true) extensión.  

### <a name="message-size-limit"></a>Límite de tamaño de mensaje  

Los mensajes que se envían de ida y vuelta entre una extensión y una aplicación tienen limitaciones de tamaño de mensaje diferentes para Chrome y Microsoft Edge.  

Chrome tiene las siguientes limitaciones de tamaño de mensaje:  

*   Límite de mensaje único del host de mensajería nativa: 1 MB  
*   Límite de mensaje único enviado al host de mensajería nativa: 4 GB  

Para Microsoft Edge, aunque no tiene límite en el tamaño del mensaje \(dependiente de la memoria\), Microsoft Edge se protege contra el mal comportamiento de las aplicaciones nativas imponiendo los siguientes límites de tamaño de `AppService` mensaje:  

*   Límite de mensaje único de la aplicación para UWP a la extensión: 1 MB  
*   Límite de mensaje único de extensión a aplicación para UWP: 100 MB  

### <a name="native-messaging-connections"></a>Conexiones de mensajería nativas  

Hay dos tipos de conexiones para mensajería nativa; persistente y no persistente.  
Una **conexión** persistente es una conexión que se mantiene en ejecución hasta que se destruye el puerto.  Una **conexión no persistente** es una conexión que se abre para un mensaje a la vez y se cierra después de la entrega.  

#### <a name="persistent"></a>Persistente  

Para Chrome, se crea una conexión persistente mediante la creación de un puerto de mensajería mediante [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) .  Una vez que se realiza el puerto, Chrome inicia un proceso de host de mensajería nativa que sigue ejecutándose hasta el puerto que destruyó.  

Para Microsoft Edge, una vez que se crea un puerto de mensajería mediante , Microsoft Edge inicia el y lo mantiene en ejecución hasta que `runtime.connectNative` [`AppServiceConnection`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceConnection?view=winrt-19041&preserve-view=true) se destruye el puerto.  El siguiente fragmento de código muestra cómo se establece una conexión persistente desde una aplicación para UWP.  

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```  

#### <a name="non-persistent"></a>No persistente  

Cuando se envía un mensaje con Chrome, sin crear un puerto de mensajería, Chrome inicia un nuevo proceso de host de mensajería nativa [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) para cada mensaje.  El primer mensaje generado por el proceso host se controla como una respuesta a la solicitud original y todos los demás mensajes después de que se omiten.  

Microsoft Edge detiene y finaliza la conexión después de recibir cada respuesta a cada mensaje.  En el siguiente fragmento de código se muestra una conexión no persistente que se establece con la que, a continuación, se finalizará en la aplicación para UWP después de recibir y almacenar una solicitud `AppServiceConnection` como [`AppServiceResponse`](/uwp/api/Windows.ApplicationModel.AppService.AppServiceResponse?view=winrt-19041&preserve-view=true) .  

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

### <a name="permission"></a>Permiso  

Para habilitar el uso de mensajería nativa con la extensión, tanto para Chrome como para Microsoft Edge, debe declarar el `"nativeMessaging"` permiso en el `manifest.json` archivo.  

## <a name="app-services"></a>Servicios de aplicaciones  

En esta sección se detalla el impacto que los servicios de aplicaciones tienen en el rendimiento y la memoria de mensajería nativa de Microsoft Edge.  

### <a name="performance"></a>Rendimiento  

Los servicios de aplicaciones están "patrocinados" por la aplicación en primer plano que los llama, que para fines de mensajería nativa es Microsoft Edge.  Esto significa que los servicios de aplicaciones pueden ejecutarse mientras se ejecute Microsoft Edge.  

En cuanto a la latencia, los servicios de aplicaciones usan canalizaciones con nombre que, después de la conexión inicial, permiten que dos aplicaciones se comuniquen directamente.  Este método de comunicación produce una latencia baja.  Los dispositivos con CPU lentas experimentarán cierta latencia inicial después de iniciar el proceso que hospeda el servicio de aplicaciones \(~80ms para iniciar la tarea en segundo plano en algunos dispositivos\).  Después de la puesta en marcha, el rendimiento en dispositivos de CPU lentos debe ser bueno.  

### <a name="memory"></a>Memoria  

La memoria asignada a un servicio de aplicaciones se ha quitado de la cuota asignada a Microsoft Edge.  Esto significa que si Microsoft Edge inicia demasiados servicios de aplicaciones, existe la posibilidad de que se les pueda quedár la memoria.  Los límites habituales de memoria de tareas en segundo plano se aplican en los servicios de aplicaciones.  Por ejemplo, en un dispositivo de 512 MB, una tarea en segundo plano del servicio de aplicaciones no puede tener más de 16 MB.  Este número sube a medida que los dispositivos se escalan hacia arriba.  

## <a name="creating-an-extension-with-native-messaging"></a>Creación de una extensión con mensajería nativa  

Para probar la mensajería nativa, la extensión necesita un nombre de familia de paquete.  Microsoft Edge lo usa para determinar la identidad del host de mensaje nativo, lo que significa que la extensión debe empaquetarse.  

Para crear la extensión con mensajería nativa en Visual Studio:  

1.  Crea un proyecto para UWP en Visual Studio.  
1.  [Agregar `AppService` a la aplicación para UWP](/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).  
    *   Opcionalmente, puedes [configurar `AppService` para hospedarte en la aplicación principal](/windows/uwp/launch-resume/convert-app-service-in-process) en lugar de como una tarea en segundo plano en este momento.  
1.  Crea y prueba tu proyecto para UWP.  
    *   Opcionalmente, puede agregar un componente [de Puente de escritorio](#adding-a-desktop-bridge-component).  
1.  Crea una extensión de Microsoft Edge que usa mensajería nativa para comunicarse con la aplicación complementaria para UWP.  Los archivos de extensión se pueden agregar a una carpeta denominada `Extension` en el proyecto de UWP.  Todos los archivos debajo de esta carpeta, incluidas las subcarpetas, necesitan tener sus propiedades configuradas de tal `Build Action=Content` manera que y `Copy to Output Directory=Copy Always` .  Asegúrese de `manifest.json` que también está configurado con estas propiedades.  
1.  Modifique el archivo del proyecto para incluir metadatos de extensión y convertirlo en una aplicación sin cabeza `package.manifest.xml` `AppListEntry="none"` agregando :  
    
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
    
1.  Usa el `AppService` nombre configurado para la UWP en las API de mensajería nativa.  
1.  Crea e [implementa el](#deploying) proyecto para UWP \(con el componente de puente de escritorio opcional\).  
1.  [Empaquetar](#packaging) la extensión de mensajería nativa una vez que esté lista para el envío de la Tienda  
    
> [!NOTE]
> Haga referencia [a la sección Demos](#demos) para obtener un ejemplo de una extensión de mensajería nativa completa.  

## <a name="adding-a-desktop-bridge-component"></a>Agregar un componente de puente de escritorio  

Si desea agregar un componente de Puente de escritorio al paquete, debe crear y crear el proyecto de Win32 en Visual Studio.  Para obtener información sobre cómo convertir la aplicación de win32 a UWP, consulta [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).  Una vez integrado Visual Studio, puede agregar el archivo ejecutable de Win32 al paquete siguiendo los pasos siguientes:  

1.  Agrega el proyecto win32 a la misma solución que el proyecto para UWP.  
1.  Establece el proyecto de Win32 como un proyecto dependiente para el proyecto para UWP:  
    
    ![configurar dependencias del proyecto](../media/project-dependencies.png)  
    
1.  Crea una `Win32` carpeta dentro del proyecto de UWP.  Copie los archivos binarios necesarios para el `Win32` proyecto en esta carpeta.  Configure las propiedades de todos los archivos binarios de tal `Build Action=Content` manera que y `Copy to Output Directory=Copy Always` .  
    
    ![carpeta con archivos de aplicaciones para UWP y win32](../media/desktop-bridge.png)  
    
1.  Modifique el archivo de proyecto de UWP para copiar todos los archivos binarios necesarios para el proyecto `Win32` en esta carpeta mediante el comando de evento PostBuild.  Esto garantiza que los archivos binarios actualizados se copian en la carpeta cada vez que se recompila la solución.  
    
    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```  
    
1.  Modifique `package.manifest.xml` agregando `<desktop:Extension>` el elemento al `<Extensions>` elemento:  
    
    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```  
    
## <a name="deploying"></a>Implementar  

Una vez que haya configurado el proyecto para UWP \(y opcionalmente win32 project\) como se describe anteriormente, estará listo para implementar la solución mediante Visual Studio.  

![build inprocess project](../media/native-message-uwp-debug.png)  

Una vez que la solución se implemente correctamente, debería ver la extensión en Microsoft Edge.  

![extensión que se muestra en Microsoft Edge](../media/secureextension.png)  

## <a name="packaging"></a>Empaquetado  

> [!NOTE]
> Enviar una extensión de Microsoft Edge a la Microsoft Store es actualmente una funcionalidad restringida.  [Envíe una solicitud](https://developer.microsoft.com/microsoft-edge/extensions/requests/) para que forme parte de Microsoft Store y que se considere para futuras actualizaciones.  

Puedes generar un paquete de la Tienda para su envío al Centro de desarrollo de Windows con la funcionalidad Visual Studio integrada:  

![Crear paquete de la Tienda](../media/create-store-package.png)  

## <a name="debugging"></a>Depuración  

Las instrucciones para depurar varían en función del componente que desee probar:  

### <a name="debugging-the-extension"></a>Depurar la extensión  

Una vez implementada la solución, la extensión se instalará en Microsoft Edge.  Consulta la [Guía de depuración](./debugging-extensions.md) para obtener información sobre cómo depurar una extensión.  

### <a name="debugging-the-uwp-app"></a>Depuración de la aplicación para UWP  

La aplicación para UWP se iniciará cuando la extensión intente conectarse a ella mediante [API de mensajería nativas.](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative)  Solo debes depurar la aplicación para UWP una vez que se inicie el proceso.  Esto puede configurarse mediante la página Property del proyecto:  

1.  En Visual Studio, mantenga el mouse en el proyecto de la aplicación para UWP y abra el menú contextual \(hacer clic con el botón secundario\)  
1.  Seleccionar **propiedades**  
1.  Comprobar **No iniciar, pero depurar mi código cuando se inicia**  
    
    ![cuadro de selección no iniciar](../media/native-message-do-not-launch.png)  
    
En Visual Studio ahora puede establecer puntos de interrupción en el código donde desea depurar y, a continuación, inicie el depurador presionando F5.  Una vez que interactúes con la extensión para conectarte a la aplicación para UWP, Visual Studio se adjuntará automáticamente al proceso.  

### <a name="debugging-the-desktop-bridge"></a>Depuración del puente de escritorio  

Aunque hay varios métodos para depurar un puente de escritorio \(aplicación convertida de Win32\), el único aplicable [para](/windows/msix/desktop/desktop-to-uwp-debug) estos escenarios es la opción PLMDebug.  También puede agregar código de depuración a la función de inicio para realizar una espera durante un tiempo específico, lo que le permite adjuntar Visual Studio al proceso.  
