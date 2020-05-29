---
description: Más información sobre cómo puedes usar la mensajería nativa para que tu extensión se comunique con una aplicación para UWP complementaria.
title: Extensiones-mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, nativo, mensajería, UWP
ms.openlocfilehash: 83f80e112180317c38763225c1cdd015da4238b0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573611"
---
# Mensajería nativa en Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## Descripción general de la arquitectura de mensajería nativa

Con Windows 10 Creators Update, las extensiones de Microsoft Edge pueden usar la mensajería nativa para comunicarse con una aplicación complementaria de la plataforma universal de Windows (UWP).  En un nivel alto, las extensiones de Microsoft Edge usan las mismas API para la mensajería nativa que las Extensiones Chrome y Firefox. Sin embargo, el host de mensajería nativo deberá implementarse con la plataforma universal de Windows.

> [!NOTE]
> El método que se describe a continuación (que se conecta a una aplicación para UWP a través de AppService) es el único mecanismo admitido para habilitar la comunicación entre las extensiones de Microsoft Edge y los componentes nativos. Para obtener más información sobre cómo habilitar la comunicación con componentes heredados de Win32, consulte la sección [Agregar un componente de puente de escritorio](#adding-a-desktop-bridge-component) de esta guía. 

 La arquitectura de mensajería nativa de Microsoft Edge aprovecha la [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API existente como infraestructura de comunicación entre procesos (IPC) subyacente. Las aplicaciones para UWP usan la `AppService` API para comunicarse entre sí. Por eso, las extensiones de Microsoft Edge ahora pueden comunicarse con aplicaciones para UWP.

![arquitectura de mensajería nativa](./../media/native-messaging-architecture.png)


### Cuándo y cuándo no usar la mensajería nativa

La mensajería nativa agrega una capa completamente nueva a la extensión. Al implementar una aplicación complementaria para UWP para tu extensión, las siguientes posibilidades estarán disponibles:

* Sincronizar datos (por ejemplo, credenciales) con una aplicación para UWP complementaria.
* Implemente algoritmos de cifrado/descifrado más estrictos que no estén disponibles en las API Web.
* Acceso a recursos que no son accesibles a través de las API Web, por ejemplo, dispositivos de hardware o USB

Hay algunos casos en los que no se puede usar la mensajería nativa por restricciones de seguridad o de directiva:

* Modificar la configuración de usuario en Microsoft Edge o Windows, por ejemplo, cambiar el explorador predeterminado o el proveedor de búsqueda.
* Acciones que infringen las directivas de Microsoft Store para las aplicaciones y las extensiones.
* Transfiriendo datos a un extremo remoto a través de un host de mensajes nativo.
* Permitir que otras aplicaciones descarguen contenido que cambia el comportamiento de la extensión.

## Demos

Para tener una idea de lo que parece una extensión de mensajería nativa de Microsoft Edge que tiene una aplicación para UWP complementaria y un puente de escritorio, consulta los ejemplos de [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) y [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) en github.

### Cómo funciona

El componente de extensión de Microsoft Edge de la muestra usa su script de contenido para detectar cuando un usuario escribe información que se debe cifrar. La extensión comunica esto al componente de puente de escritorio a través de la mensajería nativa. Cuando el usuario está listo para enviar los datos, la extensión devolverá un valor cifrado al sitio Web.

> [!NOTE]
> Este ejemplo solo funciona en una página web que usa eventos personalizados para comunicarse con el script de contenido de la extensión. La carpeta de ejemplo incluye un [archivo. html](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) para probar la extensión.

En este ejemplo, se usa la aplicación para UWP para pasar las respuestas del puente de escritorio a Microsoft Edge, que se envían a la extensión de Microsoft Edge a través de la devolución de llamada. Aunque este ejemplo tiene el host de mensajería nativo ejecutándose en la aplicación principal, también puede ejecutarse como una tarea en segundo plano. Para cambiar entre los dos, es necesario editar la secuencia de comandos de fondo de la extensión, cambiando la cadena de `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` a a `"NativeMessagingHostOutOfProcess"` .

## Implementación de Chrome y Microsoft Edge

Mientras que Chrome dirige las API de paso de mensajes para que sus extensiones se comuniquen con las aplicaciones, Microsoft Edge usa la [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API que ahora permite que las extensiones de Microsoft Edge y las aplicaciones para UWP se comuniquen.

En esta sección se detallan las diferencias entre la implementación de mensajería nativa de Chrome y Microsoft Edge.

### Registro y manifiesto del host
Para que tu extensión sea reconocida por tu extensión como host de mensajería nativa, tendrás que registrarte.


Para el registro de host de [Mensajería nativa de Chrome](https://developer.chrome.com/extensions/nativeMessaging) , la aplicación debe instalar un archivo de manifiesto en cualquier parte del sistema de archivos de Windows que defina la configuración de host de mensajería nativa.

El siguiente JSON es un ejemplo de cómo se puede configurar el archivo de configuración:

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

1. Registre el archivo de manifiesto en una ubicación predefinida en el registro que defina la configuración del host:
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

     o
   - `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

2. Establezca el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto, por ejemplo,  `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`




Para Microsoft Edge, para registrar un [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) (host de mensajería nativo), tendrás que incluir la aplicación complementaria de UWP en el mismo paquete que la extensión y especificar la [extensión de AppService](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) en el archivo del proyecto `Package.appxmanifest` . El `EntryPoint` `Name` usuario puede configurar los atributos y:

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


También necesitará establecer qué extensiones están autorizadas a conectarse al servicio. Debido a que Microsoft Edge no tiene una `"allowed_origins"` propiedad de manifiesto equivalente en tu AppxManifest, la aplicación para UWP deberá determinarlo y aplicarlo en tiempo de ejecución. Como Microsoft Edge va a establecer la conexión en nombre de la extensión, la aplicación puede buscar el nombre de familia de la persona que llama para determinar si está conectado por Microsoft Edge para controlar o autenticar a la persona que llama. P. ej. 

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



### Envío de mensajes

Para que una aplicación y una extensión se comuniquen entre sí, los mensajes se deben enviar y recibir.

Las extensiones de Chrome inician un mensaje con la [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API para enviar un mensaje al host nativo mediante un canal no persistente. 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```

El primer parámetro es el nombre del host nativo, en el que busca el cromo en el registro. El manifiesto especifica el archivo. exe que se iniciará en un espacio aislado y el mensaje se enviará con la e/s estándar. Las extensiones también pueden establecer un canal persistente mediante la `runtime.connectNative` API, que toma el nombre del host nativo como el único parámetro. 

Microsoft Edge usa la misma construcción que la API de mensajería nativa de Chrome para permitir que las extensiones de Microsoft Edge especifiquen a qué servicio de aplicaciones conectar. El primer parámetro de `runtime.sendNativeMessage` especifica el nombre del servicio de aplicaciones. En la sección [registro y manifiesto del host](#registration-and-host-manifest) , este es el `"com.microsoft.inventory"` . La plataforma de extensión de Microsoft Edge restringe que el host de mensajería nativa sea una aplicación para UWP que esté empaquetada en el mismo AppX que la extensión. Esto atenúa los riesgos de seguridad asociados con ataques maliciosos que intentan conectar Microsoft Edge con otro nombre de familia de paquetes mediante la manipulación de entradas de manifiesto. 

Esto significa que Microsoft Edge usará el mismo nombre de familia de paquete que la extensión, además del `AppService` nombre especificado en la API, para identificar de forma única el proveedor del servicio de aplicaciones.  

> [!NOTE]
> El [Kit de herramientas de extensión de Microsoft Edge](./porting-chrome-extensions.md)no lo convertirá fácilmente. Todas las extensiones que especifiquen el `"nativeMessaging"` permiso se marcarán como obligatorias para este componente.





### Protocolo de comunicación

El protocolo de comunicación para la mensajería instantánea determina cómo se aplica el formato a los mensajes antes de enviarlos.

Chrome inicia cada host de mensajería nativo en un proceso independiente y se comunica con él con la entrada estándar y la salida estándar. El mismo formato se usa para enviar mensajes en ambas direcciones: cada mensaje se serializa con JSON, UTF-8 codificado y viene precedido de la longitud del mensaje de 32 bits en el orden de bytes nativo.


En Microsoft Edge, la plataforma de la tarea en segundo plano y la aplicación principal que implementa el servicio de aplicaciones se iniciará con la plataforma. Al iniciar, se invocará el método de la tarea en segundo plano `Run` :  

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

Cuando la extensión envíe un mensaje a tu aplicación para UWP, se [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) generará el evento. A continuación, este mensaje con formato JSON se stringified en el primer par de KeyValue de un [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objeto. :

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```

Cuando la aplicación para UWP vuelve a enviar una respuesta a tu extensión, se [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) agregará un a al `ValueSet` objeto. `Key`Microsoft Edge omitirá la propiedad, pero la propiedad contendrá `Value` una cadena JSON válida.

### Devolución

Para devoluciones de llamada, usa Chrome, [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) lo que permite que una función de devolución de llamada controle cualquier respuesta asincrónica envíe un mensaje.

Microsoft Edge usa el [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) método del objeto [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) para permitir que la aplicación envíe un [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) objeto de nuevo a la extensión.


### Límite de tamaño de mensaje
Los mensajes que se envían entre una extensión y una aplicación tienen diferentes limitaciones de tamaño de mensaje para Chrome y Microsoft Edge.

Chrome tiene las siguientes limitaciones de tamaño de mensaje:
- Límite de mensaje único del host de mensajería nativa: 1 MB
- Límite de mensaje único enviado al host de mensajería nativo: 4 GB

Para Microsoft Edge, a pesar de `AppService` que no haya límite en el tamaño de los mensajes (en función de la memoria), Microsoft Edge se protege en sí mismo frente a aplicaciones nativas que imponen los siguientes límites de tamaño de mensaje:
- Un solo límite de mensajes de la aplicación para UWP para la extensión: 1 MB
- Solo límite de mensajes de la extensión a la aplicación para UWP: 100 MB



### Conexiones de mensajería nativas

Existen dos tipos de conexiones para la mensajería instantánea; persistentes y no persistentes.
Una conexión **persistente** es una conexión que se mantiene en ejecución hasta que se destruye el puerto. Una conexión **no persistente** es una conexión que se abre para un mensaje a la vez y se cierra después de la entrega.

#### Persistente

En el caso de Chrome, una conexión persistente se realiza mediante la creación de un puerto de mensajería con [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) . Una vez que se haya creado el puerto, Chrome inicia un proceso de host de mensajería nativo que sigue ejecutándose hasta el puerto que ha destruido.

Para Microsoft Edge, una vez que se crea un puerto de mensajería con `runtime.connectNative` , Microsoft Edge inicia el [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) y lo mantiene en ejecución hasta que se destruya el puerto. En el siguiente fragmento de código se muestra cómo se establece una conexión persistente desde una aplicación para UWP. 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```

#### No persistente

Cuando se envía un mensaje mediante el uso [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) de Chrome, sin crear un puerto de mensajería, Chrome inicia un nuevo proceso de host de mensajería nativo para cada mensaje. El primer mensaje generado por el proceso de host se trata como respuesta a la solicitud original y todos los demás mensajes después de que se pase por alto.

Microsoft Edge finalizará la conexión después de que se reciba la respuesta de cada mensaje. El siguiente fragmento de código muestra una conexión no persistente establecida con `AppServiceConnection` que se terminará dentro de la aplicación para UWP después de que se haya recibido una solicitud y se haya almacenado como un [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .

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

### Permiso

Para habilitar el uso de mensajería nativa con tu extensión, para Chrome y Microsoft Edge, necesitarás declarar el `"nativeMessaging"` permiso en el `manifest.json` archivo.


## Servicios de aplicaciones
Esta sección detalla el impacto que los servicios de la aplicación tienen en el rendimiento y la memoria de Microsoft Edge.

### Rendimiento

Los servicios de aplicaciones son "patrocinados" por la aplicación en primer plano que los llama, que para fines de mensajería nativa es Microsoft Edge. Esto significa que los servicios de aplicaciones se pueden ejecutar siempre que se esté ejecutando Microsoft Edge.

En relación con la latencia, los servicios de aplicaciones usan canalizaciones con nombre que, después de la conexión inicial, permiten que dos aplicaciones se comuniquen directamente. Este método de comunicación produce una latencia baja. Los dispositivos con CPU lentas experimentarán cierta latencia inicial después de iniciar el proceso que hospeda el servicio de aplicaciones (~ 80ms para iniciar la tarea en segundo plano en algunos dispositivos). Después del inicio, el rendimiento de los dispositivos de CPU lentos debe ser bueno. 


### Memoria
La memoria asignada a un servicio de aplicaciones se saca de la cuota asignada a Microsoft Edge. Esto significa que si Microsoft Edge inicia demasiados servicios de aplicaciones, existe la posibilidad de que se agote la memoria. Los límites de memoria de tareas en segundo plano habituales se aplican en los servicios de aplicación. Por ejemplo, en un dispositivo de 512 MB, una tarea en segundo plano de App Service no puede tener más de 16 MB. Este número sube a medida que los dispositivos se escalan.


## Crear una extensión con mensajería nativa

Para poder probar la mensajería nativa, tu extensión necesita un nombre de familia de paquete. Microsoft Edge lo usa para determinar la identidad de host del mensaje nativo, lo que significa que se debe empaquetar la extensión. 


Para crear su extensión con mensajería nativa en Visual Studio:

1. Crea un proyecto de UWP en Visual Studio.
2. [Agrega `AppService` a tu aplicación para UWP](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).
   - De forma opcional, puedes [configurar `AppService` para que se hospede en la aplicación principal](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) en lugar de hacerlo como una tarea en segundo plano en este momento.
3. Compila y prueba el proyecto de UWP.
   - Opcionalmente, puede Agregar un [componente de puente de escritorio](#adding-a-desktop-bridge-component).
4. Crea una extensión de Microsoft Edge que usa la mensajería nativa para comunicarse con la aplicación complementaria para UWP. Los archivos de extensión se pueden agregar a una carpeta con `Extension` el nombre del proyecto para UWP. Todos los archivos que están debajo de esta carpeta, incluidas las subcarpetas, deben tener sus propiedades configuradas de esa forma `Build Action=Content` y `Copy to Output Directory=Copy Always` . Asegúrese `manifest.json` de que también está configurada con estas propiedades.
5. Modifique el `package.manifest.xml` archivo del proyecto para que incluya metadatos de extensión y conviértalo en una aplicación sin encabezado agregando `AppListEntry="none"` :

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

6. Usa el `AppService` nombre configurado para el UWP en las API de mensajería nativa.
7. Compila e [implementa](#deploying) el proyecto de UWP (con el componente opcional de puente de escritorio).
8. [Empaquetar](#packaging) la extensión de mensajería nativa una vez que esté lista para el envío a la tienda

> [!NOTE]
> Para obtener un ejemplo de una extensión de mensajería nativa completa, consulte la sección [demos](#demos) .


## Agregar un componente de puente de escritorio 
Si desea agregar un componente de puente de escritorio al paquete, tendrá que crear y compilar el proyecto Win32 en Visual Studio. Para obtener información sobre cómo convertir tu aplicación Win32 a UWP, consulta [portar aplicaciones a Windows 10 a través del puente de escritorio](/windows/uwp/porting/desktop-to-uwp-root). Una vez que se ha integrado Visual Studio, puede Agregar el archivo ejecutable de Win32 al paquete siguiendo estos pasos:

1. Agregue el proyecto Win32 a la misma solución que el proyecto de UWP. 

2. Establezca el proyecto Win32 como un proyecto dependiente para el proyecto de UWP:

    ![configurar las dependencias del proyecto](./../media/project-dependencies.PNG)

3. Crea una `Win32` carpeta en el proyecto de UWP. Copie los binarios necesarios para el `Win32` proyecto en esta carpeta. Configure las propiedades de todos los binarios `Build Action=Content` `Copy to Output Directory=Copy Always` .

    ![carpeta con archivos de la aplicación para UWP y Win32](./../media/desktop-bridge.png)

4. Modifica el archivo de proyecto de UWP para copiar todos los binarios necesarios para el `Win32` proyecto en esta carpeta mediante el comando de evento postbuild. Esto garantiza que los binarios actualizados se copian en la carpeta cada vez que se recompila la solución.

    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```


5. Modifique `package.manifest.xml` agregando el `<desktop:Extension>` elemento al `<Extensions>` elemento:

    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```

## Implementar
Una vez que hayas configurado el proyecto de UWP (y, opcionalmente, un proyecto Win32) como se describe anteriormente, ya puedes implementar la solución con Visual Studio.

![proyecto de compilación de InProcess](../media/native-message-uwp-debug.PNG)

Una vez que la solución se haya implementado correctamente, deberías ver tu extensión en Microsoft Edge.

![se muestra la extensión en Microsoft Edge](../media/secureextension.png)

## Gabinete

> [!NOTE]
> El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida. Póngase en [contacto con nosotros](https://aka.ms/extension-request) con sus solicitudes para formar parte de Microsoft Store y le daremos una actualización futura.


Puedes generar un paquete de tienda para enviarlo al centro de desarrollo de Windows con la funcionalidad integrada de Visual Studio:


![Creando el paquete de la tienda](../media/create-store-package.PNG)

## Depuración
Las instrucciones para la depuración varían según el componente que desea probar:

### Depurar la extensión
Una vez implementada la solución, la extensión se instalará en Microsoft Edge. Consulte la guía de [depuración](./debugging-extensions.md) para obtener información sobre cómo depurar una extensión.


### Depurar la aplicación para UWP
La aplicación para UWP se iniciará cuando la extensión intente conectarse a ella mediante las [API de mensajería nativa](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative). Solo tendrás que depurar la aplicación para UWP una vez que se inicie el proceso. Puede configurarse mediante la página de propiedades del proyecto:

1.  En Visual Studio, haz clic con el botón derecho en el proyecto de la aplicación para UWP
2.  Seleccione propiedades
3.  Active "no iniciar, pero depure mi código cuando se inicie"

    ![selección de la casilla no iniciar](../media/native-message-do-not-launch.png)

En Visual Studio, ahora puedes establecer puntos de interrupción en el código en el que quieras depurar y, a continuación, iniciar el depurador presionando F5. Una vez que interactúes con la extensión para conectarte a la aplicación para UWP, Visual Studio se asociará automáticamente al proceso.


### Depurar el puente de escritorio
Aunque hay varios [métodos para depurar un puente de escritorio](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (aplicación Win32 convertida), la única opción aplicable para este escenario es la opción PLMDebug. También puede agregar código de depuración a la función de inicio para realizar una espera durante un tiempo específico, lo que le permite adjuntar Visual Studio al proceso.
