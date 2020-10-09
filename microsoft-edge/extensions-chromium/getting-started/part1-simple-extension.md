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
# <span data-ttu-id="66ed1-104">Crear un tutorial de extensión: parte 1</span><span class="sxs-lookup"><span data-stu-id="66ed1-104">Create an extension tutorial - Part 1</span></span>  

## <span data-ttu-id="66ed1-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="66ed1-105">Overview</span></span>  

<span data-ttu-id="66ed1-106">El objetivo de este tutorial es crear una extensión de Microsoft Edge (cromo) a partir de un directorio vacío.</span><span class="sxs-lookup"><span data-stu-id="66ed1-106">The goal for this tutorial is to build a Microsoft Edge (Chromium) extension starting with an empty directory.</span></span> <span data-ttu-id="66ed1-107">Crearemos una extensión que emerja la imagen de la NASA del día.</span><span class="sxs-lookup"><span data-stu-id="66ed1-107">We'll build an extension that pops up the NASA picture of the day.</span></span> <span data-ttu-id="66ed1-108">En este tutorial, aprenderá a crear una extensión de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="66ed1-108">In this tutorial, you'll learn how to create an extension by:</span></span>

*   <span data-ttu-id="66ed1-109">Crear un `manifest.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="66ed1-109">Creating a `manifest.json` file.</span></span>  
*   <span data-ttu-id="66ed1-110">Agregar iconos.</span><span class="sxs-lookup"><span data-stu-id="66ed1-110">Adding icons.</span></span>  
*   <span data-ttu-id="66ed1-111">Abrir un cuadro de diálogo emergente predeterminado.</span><span class="sxs-lookup"><span data-stu-id="66ed1-111">Opening a default pop-up dialog.</span></span>  

## <span data-ttu-id="66ed1-112">Antes de empezar</span><span class="sxs-lookup"><span data-stu-id="66ed1-112">Before you Begin</span></span>

<span data-ttu-id="66ed1-113">Si desea probar la extensión completada que compilará en este tutorial, descargue el [código fuente][ArchiveExtensionGettingStartedPart1].</span><span class="sxs-lookup"><span data-stu-id="66ed1-113">If you'd like to test out the completed extension that you'll build in this tutorial, download the [source code][ArchiveExtensionGettingStartedPart1].</span></span>  

## <span data-ttu-id="66ed1-114">Paso 1: crear un `manifest.json` archivo</span><span class="sxs-lookup"><span data-stu-id="66ed1-114">Step 1: Create a `manifest.json` file</span></span>

<span data-ttu-id="66ed1-115">Cada paquete de extensión debe tener un `manifest.json` archivo en la raíz.</span><span class="sxs-lookup"><span data-stu-id="66ed1-115">Every extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="66ed1-116">El manifiesto proporciona detalles de la extensión, la versión del paquete de extensión, el nombre y la descripción de la extensión, etc.</span><span class="sxs-lookup"><span data-stu-id="66ed1-116">The manifest provides details of your extension, the extension package version, the extension name and description, and so on.</span></span>  

<span data-ttu-id="66ed1-117">En el siguiente fragmento de código se describe la información básica necesaria en el `manifest.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="66ed1-117">The following code snippet outlines the basic information needed in your `manifest.json` file.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to display the NASA picture of the day."
}
```  

## <span data-ttu-id="66ed1-118">Paso 2: agregar iconos</span><span class="sxs-lookup"><span data-stu-id="66ed1-118">Step 2: Add icons</span></span>  

<span data-ttu-id="66ed1-119">Para empezar, cree el `icons` directorio en el proyecto para almacenar los archivos de imagen de icono.</span><span class="sxs-lookup"><span data-stu-id="66ed1-119">Start by creating the `icons` directory in your project to store the icon image files.</span></span>  <span data-ttu-id="66ed1-120">Los iconos se usan para la imagen de fondo del botón en el que los usuarios seleccionan para iniciar la extensión.</span><span class="sxs-lookup"><span data-stu-id="66ed1-120">The icons are used for the background image of the button that users select to launch the extension.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icono en la barra de herramientas para abrir la extensión":::
   <span data-ttu-id="66ed1-122">Icono en la barra de herramientas para abrir la extensión</span><span class="sxs-lookup"><span data-stu-id="66ed1-122">Icon on the toolbar to open your extension</span></span>
:::image-end:::

<span data-ttu-id="66ed1-123">Para los iconos, recomendamos usar:</span><span class="sxs-lookup"><span data-stu-id="66ed1-123">For icons, we recommend using:</span></span> 
*   `PNG` <span data-ttu-id="66ed1-124">aplicar formato a los iconos, pero también puede usar los `BMP` `GIF` `ICO` `JPEG` formatos.</span><span class="sxs-lookup"><span data-stu-id="66ed1-124">format for icons, but you may also use `BMP`, `GIF`, `ICO` or `JPEG` formats.</span></span>  
*   <span data-ttu-id="66ed1-125">Imágenes de 128 x 128 PX, que el explorador cambia su tamaño si es necesario.</span><span class="sxs-lookup"><span data-stu-id="66ed1-125">Images that are 128 x 128 px, which are resized by the browser if necessary.</span></span>  

<span data-ttu-id="66ed1-126">Los directorios de su proyecto deberían ser similares a la estructura siguiente.</span><span class="sxs-lookup"><span data-stu-id="66ed1-126">The directories of your project should be similar to the following structure.</span></span>   

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="66ed1-127">A continuación, agregue los iconos al `manifest.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="66ed1-127">Next, add the icons to the `manifest.json` file.</span></span> <span data-ttu-id="66ed1-128">Actualice el `manifest.json` archivo con la información de los iconos para que coincida con el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="66ed1-128">Update your `manifest.json` file with the icons information so that it matches the following code snippet.</span></span> <span data-ttu-id="66ed1-129">Los `png` archivos enumerados en el siguiente código están disponibles en el archivo de descarga mencionado anteriormente en este artículo.</span><span class="sxs-lookup"><span data-stu-id="66ed1-129">The `png` files listed in the following code are available in the download file mentioned earlier in this article.</span></span>  

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

## <span data-ttu-id="66ed1-130">Paso 3: abrir un cuadro de diálogo emergente predeterminado</span><span class="sxs-lookup"><span data-stu-id="66ed1-130">Step 3: Open a default pop-up dialog</span></span>  

<span data-ttu-id="66ed1-131">Ahora, cree un `HTML` archivo que se ejecute cuando el usuario inicie la extensión.</span><span class="sxs-lookup"><span data-stu-id="66ed1-131">Now, create a `HTML` file that's run when the user launches your extension.</span></span>  <span data-ttu-id="66ed1-132">Cree el archivo HTML denominado `popup.html` en un directorio denominado `popup` .</span><span class="sxs-lookup"><span data-stu-id="66ed1-132">Create the HTML file called `popup.html` in a directory called `popup`.</span></span>  <span data-ttu-id="66ed1-133">Cuando los usuarios seleccionan el icono para iniciar la extensión, `popup/popup.html` se muestra como un cuadro de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="66ed1-133">When users select the icon to launch the extension, `popup/popup.html` is displayed as a modal dialog.</span></span>  

<span data-ttu-id="66ed1-134">Agregue el código del siguiente fragmento de código para `popup.html` Mostrar la imagen de estrellas.</span><span class="sxs-lookup"><span data-stu-id="66ed1-134">Add the code from the following code snippet to `popup.html` to display the stars image.</span></span>  

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

<span data-ttu-id="66ed1-135">Asegúrese de agregar el archivo de imagen `images/stars.jpeg` a la carpeta imágenes.</span><span class="sxs-lookup"><span data-stu-id="66ed1-135">Ensure that you add the image file `images/stars.jpeg` to the images folder.</span></span>  <span data-ttu-id="66ed1-136">Los directorios de su proyecto deberían ser similares a la estructura siguiente.</span><span class="sxs-lookup"><span data-stu-id="66ed1-136">The directories of your project should be similar to the following structure.</span></span>   

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

<span data-ttu-id="66ed1-137">Por último, asegúrese de registrar el elemento emergente en `manifest.json` en `browser_action` , como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="66ed1-137">Finally, ensure you register the pop-up in `manifest.json` under `browser_action`, as shown in the following code snippet.</span></span>  

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

## <span data-ttu-id="66ed1-138">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="66ed1-138">Next steps</span></span>
<span data-ttu-id="66ed1-139">Eso es todo lo que necesitas para desarrollar una extensión de trabajo.</span><span class="sxs-lookup"><span data-stu-id="66ed1-139">That's everything you need to develop a working extension.</span></span> <span data-ttu-id="66ed1-140">Ahora, continúe con la transferencia de prueba y pruebe su extensión.</span><span class="sxs-lookup"><span data-stu-id="66ed1-140">Now, continue on to sideload and test your extension.</span></span> <span data-ttu-id="66ed1-141">Para obtener más información, consulte [transferir localmente una extensión][TestExtensionSideload].</span><span class="sxs-lookup"><span data-stu-id="66ed1-141">For more information, see [Sideload an extension][TestExtensionSideload].</span></span>  


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
