---
description: Extensiones Introducción a la parte 1
title: Crear una extensión simple que emerja la imagen de la NASA
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-cromo, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.openlocfilehash: dd5c1dab0cb9b54b79be7d2728cb9bfde0945185
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683626"
---
# Crear una extensión simple que emerja la imagen de la NASA  

[Origen del paquete de extensión completado para este elemento][ArchiveExtensionGettingStartedPart1]  

## Introducción  

En la parte 1, el objetivo es crear una extensión de cromo muy simple a partir de un directorio vacío.  El objetivo de esta extensión es completar las siguientes tareas.  

*   Crear iconos para la extensión que se puede usar en varios lugares y en tamaños diferentes  
*   Crear un `manifest.json` archivo simple  
*   Mostrar un icono de inicio que, cuando se selecciona, muestra una ventana emergente con la imagen de NASA del día  

## Conceptos básicos del archivo de manifiesto  

Cada paquete de extensión debe tener un `manifest.json` archivo en la raíz.  Debe considerar esto como el plano para la extensión.  Indica al motor del navegador qué versión de la API de extensión espera, el nombre y la descripción de la extensión, y muchos otros detalles, muchos de los cuales se tratan en esta guía de introducción a la extensión de varias partes.  

A continuación se muestra la sencilla  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## Configuración de iconos de extensión  

A continuación, agregue algunos iconos al `manifest.json` archivo \ (y cree un nuevo `/icons` directorio con los iconos archivos \).  Los iconos se usan para la imagen de fondo del botón que selecciona el usuario para iniciar la extensión \ (si hay una \) y otras ubicaciones apropiadas.  

`PNG` es el formato recomendado, pero también puede usar `BMP` , `GIF` , `ICO` y `JPEG` .  Se recomienda tener siempre al menos un icono de tamaño de 128x128 píxeles y el explorador cambiará el tamaño automáticamente según sea necesario.  

La estructura del directorio debe ser similar a la del siguiente diagrama.  

<!--  
:::image type="complex" source="./media/part1-heirarchy.png" alt-text="Directory Structure":::
   Directory Structure
:::image-end:::
-->  

<!--![Directory Structure][ImagePart1Heirarchy]  -->  

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

El `manifest.json` archivo actualizado debería aparecer de la siguiente manera.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

> [!NOTE]
> Los `png` archivos de icono enumerados anteriormente están disponibles en la descarga de zip mencionada en la parte superior de esta página.  

## Agregar un cuadro de diálogo emergente predeterminado  

Ahora, cree un `HTML` archivo que se ejecutará automáticamente cuando el usuario seleccione en el icono de extensión.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icono de identificación de barra de herramientas":::
   Icono de identificación de barra de herramientas
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

El archivo HTML se denomina `popup/popup.html` .  La selección del icono de extensión `popup/popup.html` se inicia como un cuadro de diálogo modal que permanece hacia arriba hasta que se seleccione fuera del cuadro de diálogo.  

Para ello, registre el archivo como un elemento emergente predeterminado en el en `manifest.json` el `browser_action` siguiente código.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium Extension to show the NASA Picture of the Day.",
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

En el `popup` directorio, agregue el archivo `popup.html` y, a continuación, represente la imagen de estrellas.  Este es el `popup.html` archivo.  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA Picture of the Day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="stars" />
        </div>
    </body>
</html>
```  

 Además, agregue un archivo `images/stars.jpeg` de imagen al que se hace referencia en el `popup.html` archivo.  

En el siguiente diagrama se muestra la estructura de directorios de la extensión de ejemplo.  

<!--  
:::image type="complex" source="./media/part1-heirarchy1.png" alt-text="Directory Structure for Extension":::
   Directory Structure for Extension
:::image-end:::
-->  

<!--![Directory Structure for Extension][ImagePart1Heirarchy1]  -->  

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

> [!NOTE]
> El `images/stars.jpeg` archivo que se muestra en la imagen anterior está disponible en la [descarga zip][ArchiveExtensionGettingStartedPart1].  

Eso es todo lo que necesitas para crear una extensión de trabajo.  Todo lo que queda es probarlo.  

En la siguiente sección se explica cómo cargar la extensión \ (a veces denominada carga de cara \) en el explorador Microsoft Edge \ (cromo \) para probarla.  

## Ejecuta tu extensión de forma local en el explorador mientras la desarrollas \ (carga de descarga \)  

El explorador Microsoft Edge \ (cromo \) proporciona una forma segura y sencilla de ejecutarse, así como de depurar las extensiones durante la programación.  

El proceso es muy sencillo.  Primero debes seleccionar los puntos suspensivos en la parte superior del explorador.  Después, elija en `Extensions` el menú contextual como se muestra en la siguiente imagen.  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Elegir extensiones":::
   Elegir extensiones
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

Cuando se encuentre en la página **extensiones** , tal y como se muestra en la siguiente imagen, habilite el **modo de programador** habilitando la opción de alternancia en la parte inferior izquierda de la página, tal y como se muestra en la siguiente imagen.  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Habilitar el modo de desarrollador":::
   Habilitar el modo de desarrollador
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## Instalar y actualizar las extensiones de carga  

La primera vez que desee instalar la extensión, elija la `Load Unpacked` opción tal como se muestra en la siguiente imagen.  Esto le solicita un directorio en el que tiene los activos de extensión por archivo.  Esto instala la extensión como si la hubiera descargado desde una tienda.  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Extensiones instaladas":::
   Extensiones instaladas
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

Después de instalar la extensión, puedes actualizarla seleccionando el botón que está `Reload` debajo de la lista de extensiones.  

Para quitar la extensión de su explorador, haga clic en el `Remove` botón de la parte inferior de la lista de extensiones.  

## Extensiones de depuración  

Las extensiones de depuración son muy sencillas y son compatibles con todas las características de Edge DevTools.  No obstante, esta información no se tratará en esta guía de introducción, pero es muy importante para crear las extensiones correctamente.  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Origen del paquete de extensión completado para esta parte | Microsoft docs"  
