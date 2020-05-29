---
description: Diferencia de mensajería nativa de la documentación de Chrome
title: Mensajería nativa
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/31/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 0fe45ea681c54ddea7b27a8d954022b8bda45770
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573715"
---
# Mensajería nativa  

Microsoft Edge ahora permite que la extensión instalada desde el catálogo de complementos de Microsoft Edge \ (Microsoft Edge addons \) intercambie mensajes con una aplicación nativa usando las API de paso de mensajes.  Para habilitar la característica, debe asegurarse de seguir estos pasos al implementar el host de mensajería nativa de su aplicación nativa.  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  **Host de mensajería nativa**:  
    
    Para registrar un host de mensajería nativo, la aplicación debe instalar un archivo de manifiesto que defina la configuración de host de mensajería nativa.  A continuación se muestra un ejemplo del archivo de manifiesto:  
    
    ```xml
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
    
El archivo de manifiesto de host de mensajería nativa debe ser JSON válido y contiene los siguientes campos:  

| Nombre | Descripción |  
|:--- |:--- |  
| `name` | Nombre del host de mensajería nativo. Los clientes pasan esta cadena a `runtime.connectNative` o `runtime.sendNativeMessage` .  Este nombre solo debe contener caracteres alfanuméricos en minúsculas, guiones bajos y puntos.  El nombre no debe empezar ni terminar con un punto, y un punto no debe ir seguido de otro punto. |  
| `description` | Descripción breve de la aplicación. |  
| `path` | Ruta de acceso al archivo binario de host de mensajería nativo.  En Windows, la ruta de acceso puede ser relativa al directorio en el que se encuentra el archivo de manifiesto.  En macOS, la ruta de acceso debe ser absoluta.  El proceso de host se inicia con el directorio actual configurado en el directorio que contiene el binario de host. Por ejemplo, si este parámetro se establece en `C:\Application\nm_host.exe` , el binario se inicia con el directorio actual `C:\Application\` . |  
| `type` | Tipo de la interfaz usada para comunicarse con el host de mensajería nativo.  Actualmente solo hay un valor posible para este parámetro: `stdio` .  Este valor indica que Chrome debe usarse `stdin` y `stdout` comunicarse con el host. |  
| `allowed_origins` |  lista de extensiones que deberían tener acceso al host de mensajería nativo.  Para habilitar la aplicación nativa, identifique y comuníquese con la extensión de complementos de Microsoft Edge, establecida `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` en el archivo de manifiesto de host de mensajería nativa. |  

1.  **Ubicación de host de mensajería nativa**  
    
    La ubicación del archivo de manifiesto depende de la plataforma.  
    
    En Windows, el archivo de manifiesto puede encontrarse en cualquier lugar del sistema de archivos.  El instalador de la aplicación debe crear la clave del registro  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    o  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`,  
    
    y establezca el valor predeterminado de esa clave en la ruta de acceso completa del archivo de manifiesto.  Por ejemplo, con el siguiente comando:  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    o mediante el siguiente archivo. reg:  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    Cuando Microsoft Edge busca hosts de mensajería nativos, se realiza una consulta en primer lugar el registro de 32 bits y, después, el registro de 64 bits.  

En macOS, los hosts de mensajería nativa de todo el sistema se buscan en una ubicación fija, mientras que los host de mensajería nativa de nivel de usuario se buscan en un subdirectorio del directorio de Perfil de usuario denominado `NativeMessagingHosts` .  

Microsoft Edge en macOS \ (todo el sistema \):  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

Microsoft Edge en macOS \ (específica del usuario, ruta de acceso predeterminada \):  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` puede ser Canarias, dev o beta. Para un canal estable, solo se `Microsoft Edge` debe usar `<ChannelName`>'.

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/extensions/nativeMessaging).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
