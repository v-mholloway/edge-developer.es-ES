---
description: Crear una extensión que emerja la imagen de la NASA del día
title: 'Crear un tutorial de extensión: parte 1'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge-cromo, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.openlocfilehash: 3809bfac714621cf97184127132487ed93958a2f
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104710"
---
# Crear un tutorial de extensión: parte 1  

## Introducción  

El objetivo de este tutorial es crear una extensión de Microsoft Edge (cromo) a partir de un directorio vacío. Crearemos una extensión que emerja la imagen de la NASA del día. En este tutorial, aprenderá a crear una extensión de la siguiente manera:

*   Crear un `manifest.json` archivo.  
*   Agregar iconos.  
*   Abrir un cuadro de diálogo emergente predeterminado.  

## Antes de empezar

Si desea probar la extensión completada que compilará en este tutorial, descargue el [código fuente][ArchiveExtensionGettingStartedPart1].  

## Paso 1: crear un `manifest.json` archivo

Cada paquete de extensión debe tener un `manifest.json` archivo en la raíz.  El manifiesto proporciona detalles de la extensión, la versión del paquete de extensión, el nombre y la descripción de la extensión, etc.  

En el siguiente fragmento de código se describe la información básica necesaria en el `manifest.json` archivo.  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## Paso 2: agregar iconos  

Para empezar, cree el `icons` directorio en el proyecto para almacenar los archivos de imagen de icono.  Los iconos se usan para la imagen de fondo del botón en el que los usuarios seleccionan para iniciar la extensión.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icono en la barra de herramientas para abrir la extensión&quot;:::
   Icono en la barra de herramientas para abrir la extensión
:::image-end:::

Para los iconos, recomendamos usar: 
*   `PNG` aplicar formato a los iconos, pero también puede usar los `BMP` `GIF` `ICO` `JPEG` formatos.  
*   Imágenes de 128 x 128 PX, que el explorador cambia su tamaño si es necesario.  

Los directorios de su proyecto deberían ser similares a la estructura siguiente.   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

A continuación, agregue los iconos al `manifest.json` archivo. Actualice el `manifest.json` archivo con la información de los iconos para que coincida con el siguiente fragmento de código. Los `png` archivos enumerados en el siguiente código están disponibles en el archivo de descarga mencionado anteriormente en este artículo.  

```json
{
    &quot;name&quot;: &quot;NASA picture of the day viewer&quot;,
    &quot;version&quot;: &quot;0.0.0.1&quot;,
    &quot;manifest_version&quot;: 2,
    &quot;description&quot;: &quot;A chromium extension to show the NASA picture of the day.&quot;,
    &quot;icons&quot;: {
        &quot;16&quot;: &quot;icons/nasapod16x16.png&quot;,
        &quot;32&quot;: &quot;icons/nasapod32x32.png&quot;,
        &quot;48&quot;: &quot;icons/nasapod48x48.png&quot;,
        &quot;128&quot;: &quot;icons/nasapod128x128.png"
    }
}
```  

## Paso 3: abrir un cuadro de diálogo emergente predeterminado  

Ahora, cree un `HTML` archivo que se ejecute cuando el usuario inicie la extensión.  Cree el archivo HTML denominado `popup.html` en un directorio denominado `popup` .  Cuando los usuarios seleccionan el icono para iniciar la extensión, `popup/popup.html` se muestra como un cuadro de diálogo modal.  

Agregue el código del siguiente fragmento de código para `popup.html` Mostrar la imagen de estrellas.  

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

Asegúrese de agregar el archivo de imagen `images/stars.jpeg` a la carpeta imágenes.  Los directorios de su proyecto deberían ser similares a la estructura siguiente.   

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

Por último, asegúrese de registrar el elemento emergente en `manifest.json` en `browser_action` , como se muestra en el siguiente fragmento de código.  

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

## Pasos siguientes
Eso es todo lo que necesitas para desarrollar una extensión de trabajo. Ahora, continúe con la transferencia de prueba y pruebe su extensión. Para obtener más información, consulte [transferir localmente una extensión][TestExtensionSideload].  


<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part1/part1 "Origen del paquete de extensión completado | Microsoft docs"

[TestExtensionSideload]: ./extension-sideloading.md "Probar la extensión (transferencia local) | Microsoft docs"
