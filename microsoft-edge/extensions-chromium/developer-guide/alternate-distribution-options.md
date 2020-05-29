---
description: El proceso de distribuir la extensión por mecanismo que no sean almacenes verificados
title: Método alternativo de distribuir la extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: a1a3ffe7a54f96df7e665ab5dc6f5b99bacb8b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573719"
---
# Método alternativo de distribuir la extensión  

Si es un desarrollador que desea distribuir una extensión como parte del proceso de instalación de otro software o un administrador de red que desea distribuir una extensión en su organización, Microsoft Edge admite los siguientes métodos de instalación de extensiones:  

*   **Usar el registro de Windows \ (solo para Windows \)**  

Microsoft Edge admite la instalación de una extensión hospedada en un `update_URL` .  En Windows, el `update_URL` debe apuntar al catálogo de complementos de Microsoft Edge \ (Microsoft Edge addons \) donde se debe hospedar la extensión.  

> [!NOTE]
> Instalación externa de extensión a través de un archivo JSON de preferencias para macOS <!--and Linux--> aún no son compatibles.  Esta asistencia de características estará disponible próximamente.

## Usar el registro de Windows  

En primer lugar, publique la extensión en los complementos de Microsoft Edge o empaquete un archivo. CRX y asegúrese de que se instale correctamente.  

Los pasos para instalar la extensión a través del registro en Windows son:  

*   Busque o cree la siguiente clave en el registro:  
    *   Windows de 32 bits:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   Windows de 64 bits:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   Cree una nueva clave \ (carpeta \) en la clave Extensions con el mismo nombre que el identificador de la extensión \ (por ejemplo, `aaaaaaaaaabbbbbbbbbbcccccccccc` \).  
*   En su clave de extensión, cree una propiedad, `update_url` y establezca su valor en el valor: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (esto apunta al CRX de su extensión en los complementos de Microsoft Edge \). Si desea instalar una extensión desde la tienda web de Chrome, proporcione la dirección URL de la actualización de la tienda web de Chrome `https://clients2.google.com/service/update2/crx` .  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   Inicia el explorador y ve a `edge://extensions` ; deberás ver la extensión.  

## Actualizar y desinstalar  

Microsoft Edge examina las entradas de metadatos del registro cada vez que se inicia el explorador y realiza los cambios necesarios en las extensiones externas instaladas.  

Para actualizar la extensión a una nueva versión, actualice el archivo y, a continuación, actualice la versión en el registro.  

Para desinstalar la extensión \ (por ejemplo, si se desinstala el software \), quite el archivo de preferencias \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) o los metadatos del registro.  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/apps/external_extensions).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
