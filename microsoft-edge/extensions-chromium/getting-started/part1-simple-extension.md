---
description: Crear una extensión que emergente la imagen de la NASA del día
title: 'Crear un tutorial de extensión: parte 1'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo web, html, css, javascript, desarrollador, extensiones
ms.openlocfilehash: 278a99ef4be8ad4472cf5aa37b18b5cfdbd3bb79
ms.sourcegitcommit: dc445eae30234af1ad3fa42645aabb940529912b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934504"
---
# <a name="create-an-extension-tutorial---part-1"></a>Crear un tutorial de extensión: parte 1  

## <a name="overview"></a>Información general  

El objetivo de este tutorial es crear una extensión Microsoft Edge (Chromium), empezando por un directorio vacío.  Está creando una extensión que muestra la imagen de la NASA del día.  En este tutorial, aprenderás a crear una extensión mediante:

*   Crear un `manifest.json` archivo.  
*   Agregar iconos.  
*   Abrir un cuadro de diálogo emergente predeterminado.  

## <a name="before-you-begin"></a>Antes de empezar

Para probar la extensión completada que está creando en este tutorial, descargue el [código fuente][ArchiveExtensionGettingStartedPart1].  

## <a name="step-1-create-a-manifestjson-file"></a>Paso 1: Crear una manifest.jsen el archivo

Cada paquete de extensión debe tener `manifest.json` un archivo en la raíz.  El manifiesto proporciona detalles de la extensión, la versión del paquete de extensión, el nombre y la descripción de la extensión, y así sucesivamente.  

El siguiente fragmento de código describe la información básica necesaria en el `manifest.json` archivo.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <a name="step-2-add-icons"></a>Paso 2: Agregar iconos  

Comience creando el `icons` directorio en el proyecto para almacenar los archivos de imagen de icono.  Los iconos se usan para la imagen de fondo del botón que los usuarios seleccionan para iniciar la extensión.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icono de la barra de herramientas para abrir la extensión":::
   Icono de la barra de herramientas para abrir la extensión  
:::image-end:::  

Para los iconos, se recomienda usar: 
*   `PNG` formato de iconos, pero también puede usar `BMP` , `GIF` o `ICO` `JPEG` formatos.  
*   Imágenes de 128 x 128 px, que el explorador cambia de tamaño si es necesario.  

Los directorios del proyecto deben ser similares a la siguiente estructura.   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

A continuación, agregue los iconos al `manifest.json` archivo. Actualice el `manifest.json` archivo con la información de iconos para que coincida con el siguiente fragmento de código. Los `png` archivos enumerados en el siguiente código están disponibles en el archivo de descarga mencionado anteriormente en este artículo.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

## <a name="step-3-open-a-default-pop-up-dialog"></a>Paso 3: Abrir un cuadro de diálogo emergente predeterminado  

Ahora, cree un `HTML` archivo para que se ejecute cuando el usuario inicie la extensión.  Cree el archivo HTML denominado `popup.html` en un directorio denominado `popup` .  Cuando los usuarios seleccionan el icono para iniciar la extensión, `popup/popup.html` se muestra como un cuadro de diálogo modal.  

Agregue el código del siguiente fragmento de código para `popup.html` mostrar la imagen de estrellas.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA picture of the day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="Display the stars image" />
        </div>
    </body>
</html>
```  

Asegúrese de agregar el archivo de imagen `images/stars.jpeg` a la carpeta de imágenes.  Los directorios del proyecto deben ser similares a la siguiente estructura.   

```shell
└── part1
    ├── _manifest.json
    ├── icons
    │   ├── nasapod16x16.png
    │   ├── nasapod32x32.png
    │   ├── nasapod48x48.png
    │   └── nasapod128x128.png
    ├── images
    │   └── stars.jpeg
    └── popup
        └── popup.html
```  

Por último, asegúrese de registrar la ventana emergente en `manifest.json` , como se muestra en el siguiente fragmento de `browser_action` código.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to display the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    }
}
```  

## <a name="next-steps"></a>Pasos siguientes
Eso es todo lo que necesita para desarrollar una extensión de trabajo.  Ahora, continúe con la instalación local y pruebe la extensión. Para obtener más información, vaya [a Sideload an extension][TestExtensionSideload].  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Origen del paquete de extensión completado | Microsoft Docs"

[TestExtensionSideload]: ./extension-sideloading.md "Probar la extensión (sideloading) | Microsoft Docs"
