---
description: Documentación de mensajería nativa
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/31/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 523340b302f62fd98f7ec12037d56d9d401df156e9ab0851e9b6f96fc3a1ef46
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11807489"
---
# <a name="native-messaging"></a>Mensajería nativa  

Las extensiones se comunican con una aplicación nativa de Win32 instalada en el dispositivo de un usuario mediante API de paso de mensajes.  El host de la aplicación nativa envía y recibe mensajes con extensiones mediante entrada estándar y salida estándar.  Las extensiones que usan mensajería nativa se instalan en Microsoft Edge similares a cualquier otra extensión.  Sin embargo, las aplicaciones nativas no están instaladas ni administradas por Microsoft Edge.  

Para adquirir la extensión y el host de la aplicación nativa, tienes dos modelos de distribución.  

*   Empaquetar la extensión y el host juntos.  Cuando un usuario instala el paquete, se instalan tanto la extensión como el host.  
*   Instale la extensión mediante el [Microsoft Edge complementos y][MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]la extensión pide a los usuarios que instalen el host.  

Para crear la extensión para enviar y recibir mensajes con hosts de aplicaciones nativas, siga estos pasos.  

## <a name="step-1---add-permissions-to-the-extension-manifest"></a>Paso 1: Agregar permisos al manifiesto de extensión  

Agregue el `nativeMessaging` permiso al archivomanifest.js** de** la extensión.  El siguiente fragmento de código es un ejemplo ** demanifest.jsen**.  

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

## <a name="step-2---create-your-native-messaging-host-manifest-file"></a>Paso 2: Crear el archivo de manifiesto de host de mensajería nativa  

Las aplicaciones nativas deben proporcionar un archivo de manifiesto de host de mensajería nativa.  El archivo de manifiesto contiene la siguiente información.  

*   Ruta de acceso al tiempo de ejecución del host de mensajería nativa.  
*   Método de comunicación con la extensión.  
*   Una lista de extensiones permitidas a las que se comunica.  
    
El explorador lee y valida el manifiesto de host de mensajería nativa.  El explorador no instala ni administra el archivo de manifiesto de host de mensajería nativa.  

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

El archivo de manifiesto de host debe ser un archivo JSON válido que contenga las siguientes claves.  

:::row:::
   :::column span="1":::
      **Key**  
   :::column-end:::
   :::column span="3":::
      **Detalles**  
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `name`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Especifica el nombre del host de mensajería nativa.  Los clientes pasan la cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .  
      
      *   El valor solo debe contener caracteres alfanuméricos en minúsculas, guiones bajos y puntos.  
      *   El valor no debe iniciarse ni terminar con un punto, y un punto no debe ir seguido de otro punto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `description`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Describe la aplicación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `path`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Especifica la ruta de acceso al binario de host de mensajería nativa.  
      
      *   En Windows dispositivos, puede usar rutas de acceso relativas al directorio que contiene el archivo de manifiesto.  
      *   En macOS y Linux, la ruta de acceso debe ser absoluta.  
          
      El proceso de host comienza con el directorio actual establecido en el directorio que contiene el binario de host.  Por ejemplo \(Windows\), si el parámetro está establecido en , el binario se inicia con `C:\App\nm_host.exe` el directorio actual \( `C:\App\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `type`  
   :::column-end:::
   :::column span="3":::
      ---  
      
      Especifica el tipo de interfaz que se usa para comunicarse con el host de mensajería nativa.  El valor indica Microsoft Edge usar `stdin` y comunicarse con el `stdout` host.  
      El único valor aceptable es `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ---  
      
      `allowed_origins` 
   :::column-end:::
   :::column span="3":::
      ---  
      
      Especifica la lista de extensiones que tienen acceso al host de mensajería nativa.  Para activar la aplicación para identificar y comunicarse con una extensión, en el archivo de manifiesto de host de mensajería nativa, establezca el siguiente valor.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Carga local de la extensión para probar la mensajería nativa con el host.  
Para realizar una instalación local de la extensión durante el desarrollo y `microsoft_catalog_extension_id` recuperarla, complete las siguientes acciones.  

1.  Navegue hasta `edge://extensions` y, a continuación, active el botón de alternancia modo programador.  
1.  Elija **Cargar desempaquetar**y, a continuación, elija el paquete de extensión para la instalación local.  
1.  Elige **Aceptar**.  
1.  Vaya a `edge://extensions` la página y compruebe que la extensión aparece.  
1.  Copie la clave `microsoft_catalog_extension_id` de \(ID\) de la lista de extensiones de la página.  
    
Cuando esté listo para distribuir la extensión a los usuarios, publique la extensión en el almacén Microsoft Edge complementos.  El identificador de extensión de la extensión publicada puede diferir del identificador usado durante la instalación local de la extensión.  Si el identificador cambió, actualice `allowed_origins` en el archivo de manifiesto de host con el identificador de la extensión publicada.  

## <a name="step-3---copy-the-native-messaging-host-manifest-file-to-your-system"></a>Paso 3: copiar el archivo de manifiesto de host de mensajería nativa en el sistema  

El último paso consiste en copiar el archivo de manifiesto del host de mensajería nativa en el equipo y garantizar que el archivo de manifiesto esté configurado correctamente.  Para asegurarse de que el archivo de manifiesto se coloca en la ubicación esperada, complete las siguientes acciones.  La ubicación varía según la plataforma.

> [!NOTE]
> Asegúrese de proporcionar permisos de lectura en el archivo de manifiesto y ejecutar permisos en el tiempo de ejecución del host.  

### [<a name="windows"></a>Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

El archivo de manifiesto puede encontrarse en cualquier lugar del sistema de archivos.  El instalador de la aplicación debe crear una clave del Registro y establecer el valor predeterminado de la clave en la ruta de acceso completa del archivo de manifiesto.  Las siguientes ubicaciones son ejemplos de claves del Registro.  

```output
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app

HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app
```  

Para agregar una clave del Registro al directorio con la clave de manifiesto, complete una de las siguientes acciones.  

*   Ejecute el comando en el símbolo del sistema.  
    
    1.  Ejecute el siguiente comando.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
        
*   Cree un `.reg` archivo y ejecutarlo.  
    
    1.  Copie el siguiente comando en un `.reg` archivo.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_app]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Ejecute el `.reg` archivo.  
        
Microsoft Edge consulta la `HKEY_CURRENT_USER` clave raíz seguida de `HKEY_LOCAL_MACHINE` .  En ambas claves, primero se busca en el Registro de 32 bits y, a continuación, se busca en el Registro de 64 bits para identificar hosts de mensajería nativos.  La clave del Registro especifica la ubicación del manifiesto del host de mensajería nativa.  Si las entradas del Registro de Microsoft Edge no tienen la ubicación del manifiesto de host, las ubicaciones del registro Chromium y Chrome se usan como opciones de reserva.  Si Microsoft Edge la clave del Registro en cualquiera de las ubicaciones enumeradas anteriormente, no consulta las ubicaciones que aparecen en el siguiente fragmento de código.  Si ejecuta el archivo creado como parte de un `.reg` script por lotes, asegúrese de ejecutarlo con un símbolo del sistema de administrador.

La siguiente lista es el orden de búsqueda de las ubicaciones del Registro.  

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
> Si tiene extensiones en los complementos de Microsoft Edge y chrome webstore, debe agregar los IDs de extensión correspondientes a ambos almacenes en el archivo de manifiesto de host porque solo se lee el manifiesto de host correspondiente a la primera ubicación del Registro `allowed_origins` encontrada.  

### [<a name="macos"></a>macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Para almacenar el archivo de manifiesto, complete una de las siguientes acciones.  

*   Los hosts de mensajería nativa de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.  Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
*   Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio de perfiles de usuario.  Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_app.json
    ```  
    
    La  `{Channel_Name}` entrada debe ser uno de los siguientes `Microsoft Edge {Channel_Name}` valores.  
    
    *   `Canary`  
    *   `Dev`  
    *   `Beta`  
        
    Cuando se usa el canal Estable, ` {Channel_Name}` no es necesario.  
    
### [<a name="linux"></a>Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Para almacenar el archivo de manifiesto, complete una de las siguientes acciones.  

*   Los hosts de mensajería nativa de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.  El archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio de perfiles de usuario.  El archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

<!-- links -->  

[MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos de Microsoft Edge"

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí.](https://developer.chrome.com/extensions/nativeMessaging)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
