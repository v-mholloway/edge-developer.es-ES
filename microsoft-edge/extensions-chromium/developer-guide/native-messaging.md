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
# Mensajería nativa  

Las extensiones se comunican con una aplicación Win32 nativa instalada en el dispositivo de un usuario mediante las API de paso de mensajes.  El anfitrión de la aplicación nativa envía y recibe mensajes con extensiones que usan la entrada estándar y la salida estándar.  Las extensiones que usan mensajería nativa se instalan en Microsoft Edge de forma similar a cualquier otra extensión.  Sin embargo, Microsoft Edge no instala ni administra las aplicaciones nativas.  

Para adquirir la extensión y el host de aplicaciones nativas, tiene dos modelos de distribución.  

*   Empaquete la extensión y el hospedaje juntos.  Cuando un usuario instala el paquete, se instalan tanto la extensión como el host.
*   Instale la extensión con el [almacén de complementos de Microsoft Edge][EdgeAddons]y su extensión pide a los usuarios que instalen el host.  

Para crear su extensión para enviar y recibir mensajes con hosts de aplicaciones nativas, consulte los pasos siguientes.  

## Paso 1: agregar permisos al manifiesto de la extensión  

Agregue el `nativeMessaging` permiso al **manifest.jsen** el archivo de la extensión.  El siguiente fragmento de código es un ejemplo de **manifest.js**.  

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

## Paso 2: crear el archivo de manifiesto de host de mensajería nativa  

Las aplicaciones nativas deben proporcionar un archivo de manifiesto de host de mensajería nativo.  El archivo de manifiesto contiene la ruta de acceso al motor de tiempo de ejecución de mensajería nativa, el método de comunicación con la extensión y una lista de extensiones permitidas a las que se comunica.  El explorador Lee y valida el manifiesto de host de mensajería nativo.  El explorador no instala ni administra el archivo de manifiesto de host de mensajería nativa.  

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

El archivo de manifiesto de host debe ser un archivo JSON válido que contenga las siguientes claves.  

:::row:::
   :::column span="1":::
      `name`  
   :::column-end:::
   :::column span="2":::
      Especifica el nombre del host de mensajería nativo.  Los clientes pasan esta cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .  
      
      *   Este valor solo debe contener caracteres alfanuméricos en minúsculas, guiones bajos y puntos.  
      *   Este valor no debe comenzar ni terminar con un punto, y un punto no debe ir seguido de otro punto.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `description`  
   :::column-end:::
   :::column span="2":::
      Describe la aplicación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `path`  
   :::column-end:::
   :::column span="2":::
      Especifica la ruta de acceso al archivo binario de host de mensajería nativo.  
      
      *   En dispositivos con Windows, puede usar rutas relativas al directorio que contiene el archivo de manifiesto.  
      *   En macOS y Linux, la ruta de acceso debe ser absoluta.  
      
      El proceso de hospedaje se inicia con el directorio actual configurado en el directorio que contiene el binario de host.  Por ejemplo \ (Windows \), si este parámetro se establece en `C:\Application\nm_host.exe` , el binario se inicia con el directorio actual \ ( `C:\Application\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      Especifica el tipo de la interfaz usada para comunicarse con el host de mensajería nativo.  Este valor indica a Microsoft Edge que use `stdin` y `stdout` se comunique con el host.  
      El único valor aceptable es `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      Especifica la lista de extensiones que tienen acceso al host de mensajería nativo.  Para permitir que la aplicación identifique y se comunique con una extensión, en el archivo de manifiesto del host de mensajería nativa, establezca el valor siguiente.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Transfiera localmente su extensión para probar la mensajería nativa con el host.  
Para transferir su extensión durante el desarrollo y recuperar `microsoft_catalog_extension_id` , complete los siguientes pasos.  

1.  Vaya a `edge://extensions` y, a continuación, active el botón de alternancia modo de programador.  
1.  Elija **cargar desempaquetado**y, a continuación, seleccione el paquete de extensión para transferirlo a la misma.  
1.  Elige **Aceptar**.
1.  Vaya a `edge://extensions` la página y compruebe que la extensión aparece en la lista.  
1.  Copia la clave de `microsoft_catalog_extension_id` \ (ID \) de la lista de extensiones de la página.

Cuando esté listo para distribuir la extensión a los usuarios, publique la extensión en el almacén de complementos de Microsoft Edge.  El identificador de extensión de la extensión publicada puede diferir del identificador usado durante la transferencia local de la extensión.  Si el identificador ha cambiado, actualiza `allowed_origins` en el archivo de manifiesto de host con el identificador de la extensión publicada.  

## Paso 3: copiar el archivo de manifiesto de host de mensajería nativa en el sistema  

El paso final consiste en copiar el archivo de manifiesto de host de mensajería nativa en el equipo y asegurarse de que esté configurado correctamente.  Para asegurarse de que el archivo de manifiesto se coloca en la ubicación esperada, siga estos pasos.  La ubicación varía según la plataforma.  

### [Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

El archivo de manifiesto puede encontrarse en cualquier lugar del sistema de archivos.  El instalador de la aplicación debe crear una clave del registro y establecer el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto.  Los siguientes comandos son ejemplos de claves de registro.  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

Para agregar una clave del registro en el directorio con la clave del manifiesto.  

*   Comando ejecutar en el símbolo del sistema.    
    
    1.  Ejecute el siguiente comando.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   Cree un `.reg` archivo y ejecútelo.  
    
    1.  Copie el comando siguiente en un `.reg` archivo.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Ejecute el `.reg` archivo.  
    
Microsoft Edge consulta primero el registro de 32 bits y, a continuación, el registro de 64 bits para identificar los hosts de mensajería nativos.  Si ejecuta el archivo anterior `.reg` como parte de una secuencia de comandos por lotes, asegúrese de ejecutarlo con un símbolo del sistema de administrador.  

### [macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Para almacenar el archivo de manifiesto, lleve a cabo una de las siguientes acciones.  

*   Los hosts de mensajería instantánea de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.  Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación. 
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio del perfil de usuario.  Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    El  `{Channel_Name}` `Microsoft Edge {Channel_Name}` debe ser uno de los siguientes valores:  
    
    *   Canary  
    *   Dev  
    *   Beta  

    Cuando se usa el canal estable, `{Channel_Name}` no es necesario.  

### [Linux](#tab/linux/)  

<a id="copy-manifest-file"></a>  

Para almacenar el archivo de manifiesto, lleve a cabo una de las siguientes acciones.  

*   Los hosts de mensajería instantánea de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.  El archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    /etc/opt/edge/native-messaging-hosts
    ```
    
*   Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio del perfil de usuario.  El archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    ~/.config/microsoft-edge/NativeMessagingHosts
    ```  
    
* * *  

> [!NOTE]
> Asegúrese de que proporciona permisos de lectura en el archivo de manifiesto y ejecute permisos en el motor en tiempo de ejecución del host.  

<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos de Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
