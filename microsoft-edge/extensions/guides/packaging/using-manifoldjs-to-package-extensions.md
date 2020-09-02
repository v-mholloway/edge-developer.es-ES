---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Consulta cómo empaquetar la extensión de Microsoft Edge en un instante con ManifoldJS, la Node.js herramienta de código abierto.
title: Usar ManifoldJS para empaquetar extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: 83aa57ae0e4ae302b1360be50e5158782b6fbb76
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986209"
---
# Uso de ManifoldJS para crear paquetes AppX de extensión  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS es un código abierto Node.js herramienta que le permite crear rápidamente y fácilmente crear un paquete que podrá usar para enviar a Microsoft Store.  

Si usa mensajería nativa en su extensión, debe omitir el artículo siguiente e ir a la [Mensajería nativa en Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) para obtener instrucciones de empaquetado.  

Antes de empezar, aún necesitarás leer los artículos siguientes.  

*   [Extensiones en el centro de desarrollo de Windows](./extensions-in-the-windows-dev-center.md)  
*   [Localizar paquetes de extensión](./localizing-extension-packages.md)  

> [!NOTE]
> El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.  Una vez que hayas creado, embalado y probado tu extensión, envía una solicitud en nuestro [formulario de envío de extensiones](https://developer.microsoft.com/microsoft-edge/extensions/requests).  

## Instalación de Node.js y ManifoldJS  

Lo primero que debe hacer es instalar [Node.js lts](https://nodejs.org/en/download).  
Una vez que tenga node, desde una línea de comandos (preferiblemente PowerShell), ejecute el siguiente comando para instalar ManifoldJS.  

```shell
npm install -g manifoldjs
```  

Para verificar que ha instalado correctamente ManifoldJS, ejecute `manifoldjs` desde la línea de comandos. Si no se reconoció ManifoldJS, añada `%APPDATA%\npm` a las variables de la ruta.  

## Embalaje con ManifoldJS  

Para iniciar el proceso de empaquetado, tendrá que abrir una línea de comandos y cambiar los directorios a una carpeta que será el destino de la extensión empaquetada.  

Por ejemplo:

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> El `manifoldjs` comando genera el directorio actual y sobrescribe el contenido.  

Ahora que se encuentra en la carpeta de destino, ejecute el siguiente comando.  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

El `mainifoldjs` comando se puede desglosar en las siguientes partes.  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      Cambia el nivel de registro a `debug` para obtener una impresión completa.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      Establece la única plataforma en la que ejecutar la conversión `edgeextension` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      Indica al programa que el formato del manifiesto es un `edgeextension` formato y no tiene que preocuparse si no se puede realizar la validación.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      La ruta de acceso al manifiesto de la extensión que desea convertir.  
   :::column-end:::
:::row-end:::  

Cuando ManifoldJS haya terminado de ejecutarse, tendrá una carpeta con el siguiente contenido.  

```text
┌ My Extension
└┬ edgeextension
 ├- generationInfo.json
 └┬ manifest
  ├- appxmanifest.xml
  ├┬ Assets
  |├- Square150x150Logo.png
  |├- Square44x44Logo.png
  |└- StoreLogo.png    
  └┬ Extension
   ├- manifest.json
   └- popup.html
```  
<!-- 
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
-->  

El generationInfo.jsen archivo es un registro generado al ejecutar ManifoldJS y no se incluirá en el paquete de extensión. Solo se empaquetará el contenido de la `manifest` carpeta. En la carpeta de manifiesto, la carpeta activos contiene las imágenes que se usarán en la interfaz de usuario de Windows y de Microsoft Store, mientras que la carpeta de extensiones tiene el contenido de la extensión dentro de ella.  

Ahora que tienes los archivos correctos, tendrás que editar el archivo AppXManifest generado dentro de la `manifest` carpeta. Si el manifest.jsde la extensión de archivo tiene una cadena internacionalizada para el campo "nombre", una vez ejecutado ManifoldJS, el nombre de la carpeta de capas más alta no tendrá subrayado e incluirá "MSG".

Por ejemplo, una manifest.jsen un archivo con el `"name"` campo siguiente.  

```shell
"name" : "__MSG_appName__"
```  

tendrá una carpeta de manifiesto que vive `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .  

En el archivo AppXManifest, necesitarás lo siguiente:  

 *   Reemplace los campos de identidad obligatorios y el campo PublisherDisplayName como se describe [aquí](./creating-and-testing-extension-packages.md#app-identity-template-values). Tenga en cuenta que si solo está empaquetando para fines de prueba o para la distribución empresarial, puede usar valores de marcador de posición en lugar de registrarse para una cuenta del centro de desarrollo de Windows.  
 *   Reemplace los iconos de marcador de posición de la carpeta activos por los iconos de la extensión con los mismos tamaños (150x150, 50x50, 44x44) y nombres. Consulte la guía de [diseño](./../design.md#icons-for-packaging) para obtener información sobre dónde se usan estos iconos.  
 *   Si su extensión está localizada, siga la guía de localización completa de [extensiones para Edge de Microsoft](./localizing-extension-packages.md) . Si no está localizado, solo Lea el [nombre de localizador y la descripción en la sección Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .  

Una vez que el `appxmanifest.xml` archivo esté ordenado, ejecute el siguiente comando para crear el paquete.  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

El paquete estará ahora en la carpeta **Package** que se encuentra en la carpeta edgeextension. Para obtener más información sobre cómo transferir el nuevo paquete, consulte la sección [pruebas](./creating-and-testing-extension-packages.md#testing-an-appx-package) de creación y prueba de paquetes de extensión.  

Una vez que se haya probado el paquete, puedes enviar una solicitud en nuestro [formulario de envío de extensiones](https://aka.ms/extension-request) para que la publiques en Microsoft Store.  
