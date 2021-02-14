---
description: Obtenga información sobre cómo distribuir extensiones mediante métodos alternativos que no usan almacenes comprobados
title: Método alternativo para distribuir extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 9232b8912acaa52c8d97fdd5f13b82ec33c865d4
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327633"
---
# Métodos de distribución de extensión alternativos  

Por lo general, las extensiones se distribuyen a través de la tienda de complementos de Microsoft Edge. Hay algunos escenarios en los que es posible que los desarrolladores necesiten distribuir extensiones mediante métodos alternativos. Por ejemplo:

1.  La extensión está asociada a otro software y debe instalarse junto con el resto del software agrupado.   
1.  Los administradores de red desean distribuir una extensión en toda la organización.   

Las extensiones que no se cargan desde el almacén de complementos perimetrales se denominan extensiones instaladas externamente. En la lista siguiente se proporcionan métodos alternativos para distribuir extensiones instaladas externamente. 

*   Usa el Registro de Windows (solo Windows).  
*   Usa un archivo JSON de preferencias (macOS y Linux).  
    
## Antes de comenzar  

Asegúrate de publicar la extensión en el almacén de complementos de Microsoft Edge o empaquetar un archivo y asegúrate de que se instala correctamente `.crx` en el equipo.  Si instala el archivo mediante el método , asegúrese de que puede navegar a `.crx` la extensión en esa dirección `update_URL` URL.  

Además, asegúrese de que tiene la siguiente información.    

1.  La ruta de acceso del `.crx` archivo o `update_URL` la extensión.
1.  La versión de la extensión.  La información de versión está disponible en el archivo de manifiesto o en Microsoft Edge después de `edge://extensions` cargar la extensión empaquetada.   
1.  El identificador de la extensión.  La información del identificador está disponible en Microsoft Edge después `edge://extensions` de cargar la extensión empaquetada.  

> [!NOTE] 
> Los ejemplos siguientes se `1.0` usan como la versión y para el `aaaaaaaaaabbbbbbbbbbcccccccccc` identificador.  

## Usar el Registro de Windows (solo Windows)  

Para distribuir la extensión mediante el Registro de Windows, realiza los siguientes pasos.

1.  Busque o cree la siguiente clave en el Registro:  
    *   Windows de 32 bits:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions` .  
    *   Windows de 64 bits:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions` .  
1.  Cree una nueva clave o carpeta en **Extensiones** con el mismo nombre que el identificador de la extensión. Por ejemplo, cree la clave con el nombre `aaaaaaaaaabbbbbbbbbbcccccccccc` .  
1.  En la **clave Extensions,** cree la `update_url` propiedad y establezca el valor en `https://edge.microsoft.com/extensionwebstorebase/v1/crx` .  La propiedad apunta al archivo de la extensión en el almacén de `update_url` `.crx` complementos de Microsoft Edge.  

    ```json
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
    > [!NOTE]
    > Si desea instalar una extensión de Chrome Web Store, establezca el valor `update_url` en `https://clients2.google.com/service/update2/crx` .  
  
1.  Para comprobar que la extensión aparece en Microsoft Edge, vaya a `edge://extensions` .  

## Usar un archivo JSON de preferencias (macOS y Linux)  

Para distribuir la extensión mediante un archivo JSON de preferencias, siga estos pasos.

1.  Al usar Linux, asegúrate de que el archivo de extensión esté disponible en el equipo en el que `.crx` se instalará la extensión. Copia el archivo de extensión en un directorio local o usa un recurso compartido de red al que se `.crx` pueda acceder desde el equipo. 
1.  Cree un archivo JSON donde el nombre del archivo se corresponda con el identificador de la extensión. Por ejemplo, cree un archivo JSON con el nombre de archivo `aaaaaaaaaabbbbbbbbbbcccccccccc.json` .  
1.  Según el sistema operativo, guarde el archivo JSON en una de las carpetas siguientes.   
    *   **macOS**  
        *   Específico del usuario: `~USERNAME/Library/Application Support/Microsoft Edge/External Extensions/`  
        *   Todos los usuarios: `/Library/Application Support/Microsoft/Edge/External Extensions/`  
        
        Para evitar que los usuarios no autorizados instalen extensiones para todos los usuarios, asegúrese de que el archivo de extensión sea de solo lectura. Además, asegúrese de que se cumplen las siguientes condiciones:
        
        *   Todos los directorios de la ruta de acceso pertenecen a la raíz del usuario.  
        *   Todos los directorios de la ruta de acceso se asignan al `admin` grupo `wheel` o al grupo.  
        *   Todos los directorios de la ruta de acceso no se pueden escribir en el mundo.  
        *   La ruta de acceso también debe estar libre de vínculos simbólicos.  
        
    *   **Linux**  
        *   Específico del usuario: `~/.config/microsoft-edge/External Extensions/`  
        *   Todos los usuarios: `/usr/share/microsoft-edge/extensions/`  
1.  En función de su escenario, copie el código adecuado que se muestra a continuación en el archivo JSON. 
    *   Solo se aplica a Linux. Si instala desde un archivo, especifique la ubicación y la versión con `external_crx` y `external_version` .  
            
        ```json
        {
            "external_crx": "/home/share/extension.crx",
            "external_version": "1.0"
        }
        ```  

    *   Se aplica a macOS y Linux. Si instala desde una `update_URL` dirección URL de actualización, especifique la dirección URL de actualización mediante `external_update_url` . 
        
        Copie el siguiente código en el archivo JSON al instalar desde `.crx` archivos locales solo en Linux.  
    
        ```json
        {
            "external_update_url": "http://myhost.com/mytestextension/updates.xml"
        }
        ```  
 
    *  Copia el siguiente código en el archivo JSON al instalar desde el almacén de complementos de Microsoft Edge en macOS y Linux.
    
        ```json
        {
            "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
        }
        ```  
    
1.  Para instalar extensiones para configuraciones regionales específicas, enume las configuraciones regionales admitidas mediante `supported_locale` .  También puede especificar configuraciones regionales primarias para instalar la extensión para todas las configuraciones regionales de idioma que usan ese elemento primario. Por ejemplo, al usar la configuración regional primaria, la extensión se instala para todas las configuraciones regionales en inglés, como `en` `en-US` , y así `en-GB` sucesivamente.  Cuando los usuarios cambian su configuración regional en el explorador, se desinstalan las extensiones instaladas externamente.  Para instalar la extensión para cualquier configuración regional, no use `supported_locales` .  

    ```json
    {
        "external_update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx",
        "supported_locales": [ "en", "fr", "de" ]
    }
    ```  

1.  Para comprobar que la extensión está instalada en Microsoft Edge, vaya a `edge://extensions` .  

## Actualizar y desinstalar extensiones instaladas externamente

Microsoft Edge examina las entradas de metadatos en el Registro cada vez que se inicia el explorador y realiza cualquier cambio en las extensiones instaladas externamente.  

Para actualizar la extensión a una nueva versión, actualice la versión en el archivo de manifiesto y, a continuación, actualice la versión en el Registro.  

Es posible que deba desinstalar extensiones instaladas externamente, que se instalaron como parte de una agrupación de software que se instaló anteriormente en el equipo.  Para desinstalar la extensión, quite el archivo JSON de preferencias o quite la clave del Registro.   

<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  La página original se encuentra [aquí.](https://developer.chrome.com/apps/external_extensions)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
