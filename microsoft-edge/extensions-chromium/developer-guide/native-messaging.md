---
description: Documentación de mensajería nativa
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 9d33fc4e8c9449d539b6ea82cca87c3aad4d564e
ms.sourcegitcommit: 39636248d0266730089aa2e57b9cf04d9feb363d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/29/2020
ms.locfileid: "11088558"
---
# Mensajería nativa  

Las extensiones pueden comunicarse con una aplicación Win32 nativa instalada en el dispositivo de un usuario mediante las API de paso de mensajes. El host de aplicaciones nativas puede enviar y recibir mensajes con extensiones que usan la entrada estándar y la salida estándar. Las extensiones que usan mensajería nativa se instalan en Microsoft Edge de forma similar a cualquier otra extensión. Sin embargo, Microsoft Edge no instala ni administra las aplicaciones nativas.

Para adquirir la extensión y el host de aplicación nativa, puede hacer lo siguiente:

1. Empaquetar la extensión y el hospedaje juntos. Cuando los usuarios instalan el paquete, se instalan la extensión y el host.
1. Instale la extensión desde el [almacén de complementos de Microsoft Edge][EdgeAddons]y pida a los usuarios que instalen el host. 

Consulte los pasos siguientes para configurar la extensión para enviar y recibir mensajes con hosts de aplicaciones nativas.

### Paso 1: agregar permisos al manifiesto de la extensión

Agregue el permiso nativeMessaging a la **manifest.jsde** la extensión. A continuación se muestra un ejemplo de manifest.jsen:

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

### Paso 2: crear el archivo de manifiesto de host de mensajería nativa
    
Las aplicaciones nativas deben proporcionar un archivo de manifiesto de host de mensajería nativo. Este archivo de manifiesto contiene la ruta de acceso al archivo ejecutable de host de mensajería nativa, el método de comunicación con la extensión y una lista de extensiones permitidas con la que se puede comunicar. Los exploradores leen y validan el manifiesto de host de mensajería original, pero nunca lo instala ni administra el explorador. El archivo de manifiesto de host debe ser un archivo JSON válido que contenga los siguientes campos.

    
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




| Nombre | Descripción |  
|:--- |:--- |  
| `name` | Nombre del host de mensajería nativo. Los clientes pasan esta cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .  Este nombre solo debe contener caracteres alfanuméricos en minúsculas, guiones bajos y puntos.  El nombre no debe empezar ni terminar con un punto, y un punto no debe ir seguido de otro punto. |  
| `description` | Breve descripción de la aplicación. |  
| `path` | Ruta de acceso al archivo binario de host de mensajería nativo. En dispositivos con Windows, puede usar rutas relativas al directorio que contiene el archivo de manifiesto. En macOS y Linux, la ruta de acceso debe ser absoluta. El proceso de host se inicia con el directorio actual configurado en el directorio que contiene el binario de host. Por ejemplo, si este parámetro se establece en `C:\Application\nm_host.exe` , el binario se inicia con el directorio actual `C:\Application\` . |  
| `type` | Tipo de la interfaz usada para comunicarse con el host de mensajería nativo.  Actualmente solo hay un valor posible para este parámetro: `stdio` .  Este valor indica que Microsoft Edge debe usarse `stdin` y `stdout` comunicarse con el host. |  
| `allowed_origins` |  Lista de extensiones que pueden tener acceso al host de mensajería nativo.  Para permitir que la aplicación identifique y se comunique con una extensión, `allowed_origins` establezca `chrome-extension://[Microsoft-Catalog-extensionID]` en el archivo de manifiesto de host de mensajería nativa. |  


Mientras desarrolla, puede transferir su extensión para probar la mensajería nativa con el host:
1. Navegue a `edge://extensions` y, a continuación, active el botón de alternancia modo de programador. 
1. Elija cargar Desempaquetado y, a continuación, seleccione el paquete de extensión para transferirlo a la misma.  
1. Elige Aceptar.
1. Compruebe que la `edge://extensions` página ahora incluye su extensión. 
1. Copie la clave desde el identificador de la lista de extensiones de la página.

Cuando esté listo para distribuir la extensión a los usuarios, publique la extensión en el almacén de complementos de Microsoft Edge. El identificador de extensión de la extensión publicada puede ser diferente al identificador usado durante la transferencia local de la extensión. Si el identificador ha cambiado, actualiza `allowed_origins` en el archivo de manifiesto de host con el identificador de la extensión publicada. 



### Paso 3: Copie el archivo de manifiesto de host de mensajería nativa en el sistema

El paso final implica copiar el archivo de manifiesto de host de mensajería nativa en el equipo y asegurarse de que esté configurado correctamente. Siga los pasos que se indican a continuación para asegurarse de que el archivo de host de mensajería nativo se coloca en la ubicación esperada porque varía según la plataforma.
    
**Windows**. El archivo de manifiesto puede encontrarse en cualquier lugar del sistema de archivos. El instalador de la aplicación debe crear una clave del registro y establecer el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto. Los siguientes comandos son ejemplos de claves de registro.
    
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    o  
`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`,  
    
Ejecute el comando siguiente en un símbolo del sistema para agregar una clave del registro a la carpeta con el archivo de manifiesto.
    
```shell
REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
```  
    
Como alternativa, copie el comando siguiente en un archivo. reg y ejecútelo para agregar la clave del registro. 
    
```shell
Windows Registry Editor Version 5.00
[HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
@="C:\\path\\to\\nmh-manifest.json"
``` 

  Microsoft Edge consulta primero el registro de 32 bits y, a continuación, el registro de 64 bits para identificar los hosts de mensajería nativos. Si ejecuta el archivo. reg anterior como parte de una secuencia de comandos por lotes, asegúrese de ejecutarlo con un símbolo del sistema de administrador.


**MacOS**. El archivo de manifiesto debe almacenarse de la siguiente manera:

1. Los hosts de mensajería instantánea de todo el sistema, que están disponibles para todos los usuarios, se almacenan en una ubicación fija. Por ejemplo, el archivo de manifiesto debe almacenarse en `/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`

1. Los hosts de mensajería nativa específicos del usuario, que solo están disponibles para el usuario actual, se encuentran en el subdirectorio NativeMessagingHosts en el directorio del perfil de usuario. Por ejemplo, el archivo de manifiesto debe almacenarse en  
    `~/Library/Application Support/Microsoft Edge <ChannelName>/NativeMessagingHosts/com.my_company.my_application.json`

    Dónde `ChannelName` puede estar, dev o beta. Cuando se usa el canal estable, `ChannelName` no es necesario.


**Linux** El archivo de manifiesto debe almacenarse de la siguiente manera:

1. Hosts de mensajería instantánea en todo el sistema:  `~/.config/microsoft-edge/NativeMessagingHosts`

1. Hosts de mensajería nativa específicos del usuario:  `/etc/opt/edge/native-messaging-hosts`


> [!NOTE]
> Asegúrese de que proporciona permisos de lectura en el archivo de manifiesto y ejecute permisos en el ejecutable de host.


> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  


<!-- image links -->  

<!-- links -->  

[EdgeAddons]: https://microsoftedge.microsoft.com/addons/Microsoft-Edge-Extensions-Home "Complementos de Microsoft Edge"
[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
