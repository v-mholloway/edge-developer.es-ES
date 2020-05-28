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
# <span data-ttu-id="b1b52-104">Crear una extensión simple que emerja la imagen de la NASA</span><span class="sxs-lookup"><span data-stu-id="b1b52-104">Build A Simple Extension That Pops Up NASA Picture Of The Day</span></span>  

[<span data-ttu-id="b1b52-105">Origen del paquete de extensión completado para este elemento</span><span class="sxs-lookup"><span data-stu-id="b1b52-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart1]  

## <span data-ttu-id="b1b52-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="b1b52-106">Overview</span></span>  

<span data-ttu-id="b1b52-107">En la parte 1, el objetivo es crear una extensión de cromo muy simple a partir de un directorio vacío.</span><span class="sxs-lookup"><span data-stu-id="b1b52-107">In part 1, the goal is to build a very simple Edge Chromium Extension starting with an empty directory.</span></span>  <span data-ttu-id="b1b52-108">El objetivo de esta extensión es completar las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="b1b52-108">The goal for this Extension is to complete the following tasks.</span></span>  

*   <span data-ttu-id="b1b52-109">Crear iconos para la extensión que se puede usar en varios lugares y en tamaños diferentes</span><span class="sxs-lookup"><span data-stu-id="b1b52-109">Create icons for the Extension that may be used in multiple places and in different sizes</span></span>  
*   <span data-ttu-id="b1b52-110">Crear un `manifest.json` archivo simple</span><span class="sxs-lookup"><span data-stu-id="b1b52-110">Create a simple `manifest.json` file</span></span>  
*   <span data-ttu-id="b1b52-111">Mostrar un icono de inicio que, cuando se selecciona, muestra una ventana emergente con la imagen de NASA del día</span><span class="sxs-lookup"><span data-stu-id="b1b52-111">Display a launch icon that when selected displays a pop-up window containing the NASA picture of the day</span></span>  

## <span data-ttu-id="b1b52-112">Conceptos básicos del archivo de manifiesto</span><span class="sxs-lookup"><span data-stu-id="b1b52-112">The manifest file basics</span></span>  

<span data-ttu-id="b1b52-113">Cada paquete de extensión debe tener un `manifest.json` archivo en la raíz.</span><span class="sxs-lookup"><span data-stu-id="b1b52-113">Every Extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="b1b52-114">Debe considerar esto como el plano para la extensión.</span><span class="sxs-lookup"><span data-stu-id="b1b52-114">You should think of this as the blueprint for the Extension.</span></span>  <span data-ttu-id="b1b52-115">Indica al motor del navegador qué versión de la API de extensión espera, el nombre y la descripción de la extensión, y muchos otros detalles, muchos de los cuales se tratan en esta guía de introducción a la extensión de varias partes.</span><span class="sxs-lookup"><span data-stu-id="b1b52-115">It tells the browser engine what version of the Extension API the Extension expects, the name and description of the Extension, and lots of other details, many of which are discussed in this multi-part Extension Getting Started guide.</span></span>  

<span data-ttu-id="b1b52-116">A continuación se muestra la sencilla</span><span class="sxs-lookup"><span data-stu-id="b1b52-116">Below is the simple</span></span>  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## <span data-ttu-id="b1b52-117">Configuración de iconos de extensión</span><span class="sxs-lookup"><span data-stu-id="b1b52-117">Extension icons setup</span></span>  

<span data-ttu-id="b1b52-118">A continuación, agregue algunos iconos al `manifest.json` archivo \ (y cree un nuevo `/icons` directorio con los iconos archivos \).</span><span class="sxs-lookup"><span data-stu-id="b1b52-118">Next add some icons to `manifest.json` file \(and create a new `/icons` directory with the icons files\).</span></span>  <span data-ttu-id="b1b52-119">Los iconos se usan para la imagen de fondo del botón que selecciona el usuario para iniciar la extensión \ (si hay una \) y otras ubicaciones apropiadas.</span><span class="sxs-lookup"><span data-stu-id="b1b52-119">The icons are used for the background image of the button the user selects to launch the extension \(if there is one\), and other places that are appropriate.</span></span>  

`PNG` <span data-ttu-id="b1b52-120">es el formato recomendado, pero también puede usar `BMP` , `GIF` , `ICO` y `JPEG` .</span><span class="sxs-lookup"><span data-stu-id="b1b52-120">is the recommended format, but you may also use `BMP`, `GIF`, `ICO` and `JPEG`.</span></span>  <span data-ttu-id="b1b52-121">Se recomienda tener siempre al menos un icono de tamaño de 128x128 píxeles y el explorador cambiará el tamaño automáticamente según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b1b52-121">It is recommended to always have at least a 128x128 pixels size icon and the browser automatically resizes it as necessary.</span></span>  

<span data-ttu-id="b1b52-122">La estructura del directorio debe ser similar a la del siguiente diagrama.</span><span class="sxs-lookup"><span data-stu-id="b1b52-122">Your directory structure should look like the following diagram.</span></span>  

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

<span data-ttu-id="b1b52-123">El `manifest.json` archivo actualizado debería aparecer de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="b1b52-123">Your updated `manifest.json` file should appear as follows.</span></span>  

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
> <span data-ttu-id="b1b52-124">Los `png` archivos de icono enumerados anteriormente están disponibles en la descarga de zip mencionada en la parte superior de esta página.</span><span class="sxs-lookup"><span data-stu-id="b1b52-124">The icon `png` files listed previous code are available in the zip download mentioned at the top of this page.</span></span>  

## <span data-ttu-id="b1b52-125">Agregar un cuadro de diálogo emergente predeterminado</span><span class="sxs-lookup"><span data-stu-id="b1b52-125">Adding a default pop-up dialog</span></span>  

<span data-ttu-id="b1b52-126">Ahora, cree un `HTML` archivo que se ejecutará automáticamente cuando el usuario seleccione en el icono de extensión.</span><span class="sxs-lookup"><span data-stu-id="b1b52-126">Now, create an `HTML` file that is automatically run when the user selects on the extension icon.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Icono de identificación de barra de herramientas":::
   <span data-ttu-id="b1b52-128">Icono de identificación de barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="b1b52-128">Toolbar Badge Icon</span></span>
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

<span data-ttu-id="b1b52-129">El archivo HTML se denomina `popup/popup.html` .</span><span class="sxs-lookup"><span data-stu-id="b1b52-129">The HTML file is named `popup/popup.html`.</span></span>  <span data-ttu-id="b1b52-130">La selección del icono de extensión `popup/popup.html` se inicia como un cuadro de diálogo modal que permanece hacia arriba hasta que se seleccione fuera del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b1b52-130">Selecting the Extension icon launches `popup/popup.html` as modal dialog that stays up until you select outside the dialog.</span></span>  

<span data-ttu-id="b1b52-131">Para ello, registre el archivo como un elemento emergente predeterminado en el en `manifest.json` el `browser_action` siguiente código.</span><span class="sxs-lookup"><span data-stu-id="b1b52-131">For this, register the file as a default pop-up in the `manifest.json` under `browser_action` in the following code.</span></span>  

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

<span data-ttu-id="b1b52-132">En el `popup` directorio, agregue el archivo `popup.html` y, a continuación, represente la imagen de estrellas.</span><span class="sxs-lookup"><span data-stu-id="b1b52-132">In the `popup` directory , add the file `popup.html` and have it render the stars image.</span></span>  <span data-ttu-id="b1b52-133">Este es el `popup.html` archivo.</span><span class="sxs-lookup"><span data-stu-id="b1b52-133">Here is the `popup.html` file.</span></span>  

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

 <span data-ttu-id="b1b52-134">Además, agregue un archivo `images/stars.jpeg` de imagen al que se hace referencia en el `popup.html` archivo.</span><span class="sxs-lookup"><span data-stu-id="b1b52-134">Also, add an image file `images/stars.jpeg` that is referenced in the `popup.html` file.</span></span>  

<span data-ttu-id="b1b52-135">En el siguiente diagrama se muestra la estructura de directorios de la extensión de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b1b52-135">The directory structure for the example Extension is displayed in the following diagram.</span></span>  

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
> <span data-ttu-id="b1b52-136">El `images/stars.jpeg` archivo que se muestra en la imagen anterior está disponible en la [descarga zip][ArchiveExtensionGettingStartedPart1].</span><span class="sxs-lookup"><span data-stu-id="b1b52-136">The `images/stars.jpeg` file listed in the previous image is available in the [zip download][ArchiveExtensionGettingStartedPart1].</span></span>  

<span data-ttu-id="b1b52-137">Eso es todo lo que necesitas para crear una extensión de trabajo.</span><span class="sxs-lookup"><span data-stu-id="b1b52-137">That is everything you need to build a working Extension.</span></span>  <span data-ttu-id="b1b52-138">Todo lo que queda es probarlo.</span><span class="sxs-lookup"><span data-stu-id="b1b52-138">All that is left to is test it.</span></span>  

<span data-ttu-id="b1b52-139">En la siguiente sección se explica cómo cargar la extensión \ (a veces denominada carga de cara \) en el explorador Microsoft Edge \ (cromo \) para probarla.</span><span class="sxs-lookup"><span data-stu-id="b1b52-139">The next section explains how to load the Extension \(sometimes called side loading\) into the Microsoft Edge \(Chromium\) browser to test it.</span></span>  

## <span data-ttu-id="b1b52-140">Ejecuta tu extensión de forma local en el explorador mientras la desarrollas \ (carga de descarga \)</span><span class="sxs-lookup"><span data-stu-id="b1b52-140">Run your Extension locally in your browser while developing it \(side-loading\)</span></span>  

<span data-ttu-id="b1b52-141">El explorador Microsoft Edge \ (cromo \) proporciona una forma segura y sencilla de ejecutarse, así como de depurar las extensiones durante la programación.</span><span class="sxs-lookup"><span data-stu-id="b1b52-141">The Microsoft Edge \(Chromium\) browser provides a safe and simple way for you to run as well as debug your Extensions while you are developing.</span></span>  

<span data-ttu-id="b1b52-142">El proceso es muy sencillo.</span><span class="sxs-lookup"><span data-stu-id="b1b52-142">The process is quite simple.</span></span>  <span data-ttu-id="b1b52-143">Primero debes seleccionar los puntos suspensivos en la parte superior del explorador.</span><span class="sxs-lookup"><span data-stu-id="b1b52-143">You must first select the three dots at the top of your browser.</span></span>  <span data-ttu-id="b1b52-144">Después, elija en `Extensions` el menú contextual como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="b1b52-144">Next, choose `Extensions` from the context menu as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Elegir extensiones":::
   <span data-ttu-id="b1b52-146">Elegir extensiones</span><span class="sxs-lookup"><span data-stu-id="b1b52-146">Choose Extensions</span></span>
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

<span data-ttu-id="b1b52-147">Cuando se encuentre en la página **extensiones** , tal y como se muestra en la siguiente imagen, habilite el **modo de programador** habilitando la opción de alternancia en la parte inferior izquierda de la página, tal y como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="b1b52-147">When you are on the **Extensions** page as shown in the following image, enable the **Developer mode** by enabling the toggle at the bottom left of the page as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Habilitar el modo de desarrollador":::
   <span data-ttu-id="b1b52-149">Habilitar el modo de desarrollador</span><span class="sxs-lookup"><span data-stu-id="b1b52-149">Enable Developer Mode</span></span>
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## <span data-ttu-id="b1b52-150">Instalar y actualizar las extensiones de carga</span><span class="sxs-lookup"><span data-stu-id="b1b52-150">Installing and updating side-loaded Extensions</span></span>  

<span data-ttu-id="b1b52-151">La primera vez que desee instalar la extensión, elija la `Load Unpacked` opción tal como se muestra en la siguiente imagen.</span><span class="sxs-lookup"><span data-stu-id="b1b52-151">The first time you want to install your Extension, you choose the `Load Unpacked` option as shown in the following image.</span></span>  <span data-ttu-id="b1b52-152">Esto le solicita un directorio en el que tiene los activos de extensión por archivo.</span><span class="sxs-lookup"><span data-stu-id="b1b52-152">This prompts you for a directory where you have your Extension assets file by file.</span></span>  <span data-ttu-id="b1b52-153">Esto instala la extensión como si la hubiera descargado desde una tienda.</span><span class="sxs-lookup"><span data-stu-id="b1b52-153">This installs the Extension as if you had downloaded it from a store.</span></span>  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Extensiones instaladas":::
   <span data-ttu-id="b1b52-155">Extensiones instaladas</span><span class="sxs-lookup"><span data-stu-id="b1b52-155">Installed Extensions</span></span>
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

<span data-ttu-id="b1b52-156">Después de instalar la extensión, puedes actualizarla seleccionando el botón que está `Reload` debajo de la lista de extensiones.</span><span class="sxs-lookup"><span data-stu-id="b1b52-156">After you install your Extension, you may update it by selecting the `Reload` button under your Extension listing.</span></span>  

<span data-ttu-id="b1b52-157">Para quitar la extensión de su explorador, haga clic en el `Remove` botón de la parte inferior de la lista de extensiones.</span><span class="sxs-lookup"><span data-stu-id="b1b52-157">To remove the Extension from your browser, click the `Remove` button on the bottom of the Extension listing.</span></span>  

## <span data-ttu-id="b1b52-158">Extensiones de depuración</span><span class="sxs-lookup"><span data-stu-id="b1b52-158">Debugging Extensions</span></span>  

<span data-ttu-id="b1b52-159">Las extensiones de depuración son muy sencillas y son compatibles con todas las características de Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b1b52-159">Debugging Extensions is quite easy and supports all of the features in Edge Chromium DevTools.</span></span>  <span data-ttu-id="b1b52-160">No obstante, esta información no se tratará en esta guía de introducción, pero es muy importante para crear las extensiones correctamente.</span><span class="sxs-lookup"><span data-stu-id="b1b52-160">Those details however are not covered in this getting started guide but are very important to successfully build Extensions.</span></span>  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Origen del paquete de extensión completado para esta parte | Microsoft docs"  
