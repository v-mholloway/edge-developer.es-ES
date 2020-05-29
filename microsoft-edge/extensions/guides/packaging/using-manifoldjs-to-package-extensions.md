---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Consulta cómo empaquetar la extensión de Microsoft Edge en un instante con ManifoldJS, la herramienta de código abierto de node. js.
title: Uso de ManifoldJS para empaquetar extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: cca83a26c9f80eca6454e3b5b329f72a7491b6e2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573575"
---
# Uso de ManifoldJS para crear paquetes AppX de extensión  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS es una herramienta de Open Source. js que le permite crear de forma rápida y fácilmente un paquete que se puede usar para enviarlo a Microsoft Store.

Si usa mensajería nativa en su extensión, debe omitir esta acción e ir a la [Mensajería nativa en Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) para obtener instrucciones de empaquetado. 

Antes de empezar, aún necesitarás leer los artículos siguientes:

- [Extensiones en el centro de desarrollo de Windows](./extensions-in-the-windows-dev-center.md)
- [Localización de paquetes de extensiones](./localizing-extension-packages.md)

> [!NOTE]
> El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida. Una vez que hayas creado, embalado y probado tu extensión, envía una solicitud en nuestro [formulario de envío de extensiones](https://aka.ms/extension-request).


## Instalar node. js y ManifoldJS

Lo primero que debe hacer es instalar [node. js lts](https://nodejs.org/en/download/).
Una vez que tenga node, desde una línea de comandos (preferiblemente PowerShell), ejecute el siguiente comando para instalar ManifoldJS:

`npm install -g manifoldjs`

Para verificar que ha instalado correctamente ManifoldJS, ejecute `manifoldjs` desde la línea de comandos. Si no se reconoció ManifoldJS, añada `%APPDATA%\npm` a las variables de la ruta.

## Embalaje con ManifoldJS

Para iniciar el proceso de empaquetado, tendrá que abrir una línea de comandos y cambiar los directorios a una carpeta que será el destino de la extensión empaquetada.

Por ejemplo:

`cd C:\manifoldJSTest`

> [!NOTE]
> ManifoldJS se enviará en el directorio actual y podrá sobrescribir el contenido.



Ahora que se encuentra en la carpeta de destino, ejecute el siguiente comando:

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


Este comando se puede dividir en las siguientes partes:
 -    **-l depurar**: cambia el nivel de registro a "debug" para obtener una impresión completa.
 -    **-p edgeextension**: establece la única plataforma en la que se ejecutará la conversión en edgeextension.
 -    **-f edgeextension**: indica al programa que el formato del manifiesto es un formato de edgeextension y no se produce un error en la validación.
 -    **-m \ < ubicación de la extensión > \manifest.JSON**: la ruta de acceso al manifiesto de la extensión que desea convertir.


Cuando ManifoldJS haya terminado de ejecutarse, tendrá una carpeta con el siguiente contenido:

    My Extension
        edgeextension
            generationInfo.json
            manifest
                   appxmanifest.xml
                Assets
                    Square150x150Logo.png
                    Square44x44Logo.png
                    StoreLogo.png    
                Extension
                    manifest.json
                    popup.html
                    ...
                ...

El archivo generationInfo. JSON es un registro generado al ejecutar ManifoldJS y no se incluirá en el paquete de extensión. Solo se empaquetará el contenido de la carpeta del **manifiesto** . En la carpeta de manifiesto, la carpeta activos contiene las imágenes que se usarán en la interfaz de usuario de Windows y de Microsoft Store, mientras que la carpeta de extensiones tiene el contenido de la extensión dentro de ella.


Ahora que tienes los archivos correctos, tendrás que editar el archivo AppXManifest generado dentro de la carpeta del **manifiesto** . Si el archivo manifest. JSON de la extensión tiene una cadena internacionalizada para el campo "Name", una vez ejecutado ManifoldJS, el nombre de la carpeta de capas más alta no tendrá subrayado e incluirá "MSG".

Por ejemplo, un archivo manifest. JSON con el siguiente `"name"` campo:

`"name" : "__MSG_appName__"`

tendrá una carpeta de manifiesto que vive `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .

En el archivo AppXManifest, tendrás que:
 -    Reemplace los campos de identidad obligatorios y el campo PublisherDisplayName como se describe [aquí](./creating-and-testing-extension-packages.md#app-identity-template-values). Ten en cuenta que si solo tienes que empaquetar para pruebas o para la distribución empresarial, puedes usar valores de marcador de posición en lugar de registrarse para una cuenta del centro de desarrollo de Windows.
 -    Reemplace los iconos de marcador de posición de la carpeta activos por los iconos de la extensión con los mismos tamaños (150x150, 50x50, 44x44) y nombres. Consulte la guía de [diseño](./../design.md#icons-for-packaging) para obtener información sobre dónde se usan estos iconos.
 - Si su extensión está localizada, siga la guía de localización completa de [extensiones para Edge de Microsoft](./localizing-extension-packages.md) . Si no está localizado, lea solo el [nombre y la descripción del localizador en la sección Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .

Una vez que el archivo appxmanifest. XML esté ordenado, ejecuta el siguiente comando para crear el paquete:

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

El paquete estará ahora en la carpeta **Package** que se encuentra en la carpeta edgeextension. Consulte la sección sobre cómo crear y [probar paquetes](./creating-and-testing-extension-packages.md#testing-an-appx-package) de extensiones ' para obtener información sobre cómo transferir el nuevo paquete.

Una vez que se haya probado el paquete, puedes enviar una solicitud en nuestro [formulario de envío de extensiones](https://aka.ms/extension-request) para que la publiques en Microsoft Store.
