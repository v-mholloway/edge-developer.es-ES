---
description: Documentación de mensajería nativa
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 2d629762d4c7c75832905cfbf8c2d5311191092d
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327704"
---
# Mensajería nativa  

Las extensiones se comunican con una aplicación nativa de Win32 instalada en el dispositivo de un usuario mediante las API de paso de mensajes.  El host de la aplicación nativa envía y recibe mensajes con extensiones mediante la entrada estándar y la salida estándar.  Las extensiones que usan mensajería nativa se instalan en Microsoft Edge de forma similar a cualquier otra extensión.  Sin embargo, Microsoft Edge no instala ni administra las aplicaciones nativas.  

Para adquirir la extensión y el host de la aplicación nativa, tiene dos modelos de distribución.  

*   Empaquetar la extensión y el host juntos.  Cuando un usuario instala el paquete, se instalan tanto la extensión como el host.  
*   Instala la extensión con [el almacén de] [MicrosoftMicrosoftedgeAddonsMicrosoftEdgeExtensionsHome]complementos de Microsoft Edge y la extensión pide a los usuarios que instalen el host.  

Para crear la extensión para enviar y recibir mensajes con hosts de aplicaciones nativas, consulte los pasos siguientes.  

## Paso 1: Agregar permisos al manifiesto de extensión  

Agregue el `nativeMessaging` permiso al archivomanifest.js** archivo** de la extensión.  El siguiente fragmento de código es un ejemplo demanifest.js** en**.  

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

## Paso 2: Crear el archivo de manifiesto del host de mensajería nativo  

Las aplicaciones nativas deben proporcionar un archivo de manifiesto de host de mensajería nativo.  El archivo de manifiesto contiene la siguiente información.  

*   La ruta de acceso al tiempo de ejecución del host de mensajería nativo.  
*   El método de comunicación con la extensión.  
*   Una lista de extensiones permitidas a las que se comunica.  
    
El explorador lee y valida el manifiesto del host de mensajería nativa.  El explorador no instala ni administra el archivo de manifiesto del host de mensajería nativa.  

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
      
      *   Este valor solo debe contener caracteres alfanuméricos en minúsculas, caracteres de subrayado y puntos.  
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
      Especifica la ruta de acceso al binario del host de mensajería nativo.  
      
      *   En dispositivos Windows, puedes usar rutas de acceso relativas al directorio que contiene el archivo de manifiesto.  
      *   En macOS y Linux, la ruta de acceso debe ser absoluta.  
      
      El proceso de host comienza con el directorio actual establecido en el directorio que contiene el binario de host.  Por ejemplo \(Windows\), si este parámetro se establece en , el binario se inicia con `C:\Application\nm_host.exe` el directorio actual \( `C:\Application\` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `type`  
   :::column-end:::
   :::column span="2":::
      Especifica el tipo de interfaz que se usa para comunicarse con el host de mensajería nativo.  Este valor indica a Microsoft Edge que use `stdin` y se comunique con el `stdout` host.  
      El único valor aceptable es `stdio` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `allowed_origins` 
   :::column-end:::
   :::column span="2":::
      Especifica la lista de extensiones que tienen acceso al host de mensajería nativo.  Para permitir que la aplicación identifique y se comunique con una extensión, en el archivo de manifiesto del host de mensajería nativo, establezca el siguiente valor.  
      
      ```json
      "allowed_origins": ["chrome-extension://{microsoft_catalog_extension_id}"]
      ```  
   :::column-end:::
:::row-end:::  

Realizar una instalación de prueba de la extensión para probar la mensajería nativa con el host.  
Para realizar una instalación de instalación local de la extensión durante el desarrollo y `microsoft_catalog_extension_id` recuperarla, siga estos pasos.  

1.  Navegue hasta `edge://extensions` y, a continuación, active el botón de alternancia del modo de desarrollador.  
1.  Elija **Cargar desempaquetar**y, a continuación, seleccione el paquete de extensión para la instalación de prueba.  
1.  Elige **Aceptar**.  
1.  Vaya a `edge://extensions` la página y compruebe que la extensión aparece en la lista.  
1.  Copia la clave `microsoft_catalog_extension_id` de \(ID\) de la lista de extensiones de la página.  

Cuando estés listo para distribuir la extensión a los usuarios, publica la extensión en la tienda de complementos de Microsoft Edge.  El identificador de extensión de la extensión publicada puede ser diferente del identificador usado durante la instalación de la instalación de la extensión.  Si el identificador ha cambiado, actualice `allowed_origins` el archivo de manifiesto de host con el identificador de la extensión publicada.  

## Paso 3: Copiar el archivo de manifiesto del host de mensajería nativa en el sistema  

El paso final implica copiar el archivo de manifiesto del host de mensajería nativa en el equipo y asegurarse de que el archivo de manifiesto está configurado correctamente.  Para asegurarse de que el archivo de manifiesto se coloca en la ubicación esperada, siga estos pasos.  La ubicación varía según la plataforma.  

### [Windows](#tab/windows/)  

<a id="copy-manifest-file"></a>  

El archivo de manifiesto puede estar ubicado en cualquier parte del sistema de archivos.  El instalador de la aplicación debe crear una clave del Registro y establecer el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto.  Los siguientes comandos son ejemplos de claves del Registro.  

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

```text
HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application
```

Para agregar una clave del Registro al directorio con la clave de manifiesto.  

*   Ejecute el comando en el símbolo del sistema.  
    
    1.  Ejecute el siguiente comando.  
        
        ```shell
        REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
        ```  
    
*   Cree un `.reg` archivo y ejecutarlo.  
    
    1.  Copie el siguiente comando en un `.reg` archivo.  
        
        ```shell
        Windows Registry Editor Version 5.00
        [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
        @="C:\\path\\to\\nmh-manifest.json"
        ```  
        
    1.  Ejecute el `.reg` archivo.  
    
Microsoft Edge consulta la `HKEY_CURRENT_USER` clave raíz seguida de `HKEY_LOCAL_MACHINE` .  En ambas claves, primero se busca en el Registro de 32 bits y, a continuación, se busca en el Registro de 64 bits para identificar hosts de mensajería nativos.  La clave del Registro especifica la ubicación del manifiesto del host de mensajería nativo.  Si Microsoft Edge encuentra la clave del Registro en cualquiera de las ubicaciones enumeradas anteriormente, no consulta las ubicaciones que aparecen en este párrafo.  Si ejecuta el archivo anterior como parte de un script por lotes, asegúrese de `.reg` ejecutarlo mediante un símbolo del sistema de administrador.  

### [macOS](#tab/macos/)  

<a id="copy-manifest-file"></a>  

Para almacenar el archivo de manifiesto, complete una de las siguientes acciones.  

*   Los hosts de mensajería nativa de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija.  Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    /Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
*   Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el `NativeMessagingHosts` subdirectorio del directorio de perfiles de usuario.  Por ejemplo, el archivo de manifiesto debe almacenarse en la siguiente ubicación.  
    
    ```bash
    ~/Library/Application Support/Microsoft Edge {Channel_Name}/NativeMessagingHosts/com.my_company.my_application.json
    ```  
    
    La  `{Channel_Name}` entrada debe ser uno de los siguientes `Microsoft Edge {Channel_Name}` valores.  
    
    *   Canary  
    *   Dev  
    *   Beta  

    Cuando se usa el canal estable, `{Channel_Name}` no es necesario.  

### [Linux](#tab/linux/)  

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

> [!NOTE]
> Asegúrese de proporcionar permisos de lectura en el archivo de manifiesto y de ejecutar permisos en el tiempo de ejecución del host.  

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
