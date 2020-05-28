---
description: Más información sobre cómo crear una extensión de Microsoft Edge
title: Crear una extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: a08fc6bd604ce810895e7103f7f6384dbedc9f78
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683654"
---
# <span data-ttu-id="85206-104">Creación de una extensión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="85206-104">Creating A Microsoft Edge Extension</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="85206-105">En esta guía, aprenderá a crear una extensión para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="85206-105">In this guide, learn to create an extension for Microsoft Edge.</span></span>  <span data-ttu-id="85206-106">Esta extensión de ejemplo le permite manipular CSS específicas para páginas de [docs.Microsoft.com][MicrosoftDocs] , como repasarle por la creación de un archivo de manifiesto, la interfaz de usuario y los scripts de contenido y de fondo.</span><span class="sxs-lookup"><span data-stu-id="85206-106">This example extension allows you to manipulate specific CSS for [docs.microsoft.com][MicrosoftDocs] pages including walking you through creation of a manifest file, the user interface, and background and content scripts.</span></span>  

:::image type="complex" source="../media/color-changer_header.png" alt-text="El cuerpo de Docs.microsoft.com cambió a azul":::
   <span data-ttu-id="85206-108">El cuerpo de Docs.microsoft.com cambió a azul</span><span class="sxs-lookup"><span data-stu-id="85206-108">Docs.microsoft.com body changed to blue</span></span>
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

<span data-ttu-id="85206-109">En este tutorial se supone que tiene conocimientos básicos sobre qué es una extensión de explorador y cómo funciona.</span><span class="sxs-lookup"><span data-stu-id="85206-109">This tutorial assumes you have basic understanding of what a browser extension is and how it work.</span></span>  <span data-ttu-id="85206-110">Para obtener más información sobre los bloques de creación de las extensiones, vea [anatomía de una extensión][MDNAnatomyExtension].</span><span class="sxs-lookup"><span data-stu-id="85206-110">For more imformation about the building blocks for extensions, see [Anatomy of an extension][MDNAnatomyExtension].</span></span>  

<span data-ttu-id="85206-111">Descarga el código de la [muestra completa en github][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="85206-111">Download the code for the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="85206-112">Crear el archivo de manifiesto</span><span class="sxs-lookup"><span data-stu-id="85206-112">Building the manifest file</span></span>  

<span data-ttu-id="85206-113">Para empezar, cree un directorio para la extensión y asígnele un nombre `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="85206-113">To begin, create a directory for your extension and name it `color-changer`.</span></span>  

<span data-ttu-id="85206-114">En la `color-changer` carpeta, cree un archivo denominado `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="85206-114">Inside the `color-changer` folder, create a file named `manifest.json`.</span></span>  <span data-ttu-id="85206-115">El `manifest.json` archivo es necesario para todas las extensiones y proporciona información importante para la extensión, desde el nombre de la extensión a los permisos.</span><span class="sxs-lookup"><span data-stu-id="85206-115">The `manifest.json` file is required for all extensions and provides important information for the extension, ranging from the extension name to the permissions.</span></span>  

> [!NOTE] 
> <span data-ttu-id="85206-116">Esta guía le guiará por todas las claves del manifiesto que debe usar en esta guía, pero para obtener una lista de todas las claves de manifiesto compatibles y recomendadas, consulte [claves de manifiesto admitidas][ExtensionsApisupportManifestKeys].</span><span class="sxs-lookup"><span data-stu-id="85206-116">This guide walks you through all the manifest keys you must use in this guide, but for a list of all supported and recommended manifest keys, see [Supported manifest keys][ExtensionsApisupportManifestKeys].</span></span>  

<span data-ttu-id="85206-117">En `manifest.json` el interior, agregue el siguiente código.</span><span class="sxs-lookup"><span data-stu-id="85206-117">Inside `manifest.json`, add the following code.</span></span>  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### <span data-ttu-id="85206-118">Definiciones de clave de manifiesto</span><span class="sxs-lookup"><span data-stu-id="85206-118">Manifest key definitions</span></span>  

| <span data-ttu-id="85206-119">Key</span><span class="sxs-lookup"><span data-stu-id="85206-119">Key</span></span> | <span data-ttu-id="85206-120">Detalles</span><span class="sxs-lookup"><span data-stu-id="85206-120">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="85206-121">name</span><span class="sxs-lookup"><span data-stu-id="85206-121">name</span></span>][MDNManifestjsonName] | <span data-ttu-id="85206-122">El nombre de la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-122">The name of the extension.</span></span>  |  
| [<span data-ttu-id="85206-123">autorización</span><span class="sxs-lookup"><span data-stu-id="85206-123">author</span></span>][MDNManifestjsonAuthor] | <span data-ttu-id="85206-124">El autor de la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-124">The author of the extension.</span></span>  |  
| [<span data-ttu-id="85206-125">version</span><span class="sxs-lookup"><span data-stu-id="85206-125">version</span></span>][MDNManifestjsonVersion] | <span data-ttu-id="85206-126">Número de versión de la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-126">The extension version number.</span></span>  |  
| [<span data-ttu-id="85206-127">description</span><span class="sxs-lookup"><span data-stu-id="85206-127">description</span></span>][MDNManifestjsonDescription] | <span data-ttu-id="85206-128">La descripción de la extensión mostrada en la sección acerca del menú extensión en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="85206-128">The description of the extension displayed in the About section of the extension menu in Microsoft Edge.</span></span>  |  
| [<span data-ttu-id="85206-129">permisos</span><span class="sxs-lookup"><span data-stu-id="85206-129">permissions</span></span>][MDNManifestjsonPermissions] | <span data-ttu-id="85206-130">Matriz de cadenas que solicitan permisos para la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-130">An array of strings requesting permissions for the extension.</span></span>  <span data-ttu-id="85206-131">Para tu extensión, Estás solicitando permisos para ver los sitios web visitados \ ("pestañas" \) y para actualizar el contenido de las direcciones URL que coincidan con " `*://docs.microsoft.com/*` ".</span><span class="sxs-lookup"><span data-stu-id="85206-131">For your extension, you are requesting permissions to see the websites visited \("tabs"\) and to update content on URLs matching "`*://docs.microsoft.com/*`".</span></span>  |  
| [<span data-ttu-id="85206-132">browser_action</span><span class="sxs-lookup"><span data-stu-id="85206-132">browser_action</span></span>][MDNManifestjsonBrowserAction] | <span data-ttu-id="85206-133">Contiene la información de un icono.</span><span class="sxs-lookup"><span data-stu-id="85206-133">Contains the information for an icon.</span></span> <span data-ttu-id="85206-134">El icono se coloca en la barra de herramientas de Microsoft Edge, a la derecha de la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="85206-134">The icon is placed on the Microsoft Edge toolbar, to the right of the address bar.</span></span>  |  

#### <span data-ttu-id="85206-135">browser_action definiciones de clave</span><span class="sxs-lookup"><span data-stu-id="85206-135">browser_action Key definitions</span></span>  

| <span data-ttu-id="85206-136">Key</span><span class="sxs-lookup"><span data-stu-id="85206-136">Key</span></span> | <span data-ttu-id="85206-137">Detalles</span><span class="sxs-lookup"><span data-stu-id="85206-137">Details</span></span> |  
|:--- |:--- |  
| `default_icon` | <span data-ttu-id="85206-138">El icono que se usa en la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="85206-138">The icon that is used in the toolbar.</span></span>  |  
| `default_title` | <span data-ttu-id="85206-139">El texto que se muestra cuando un usuario mantiene el puntero sobre el icono de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="85206-139">The text that is displayed when a user hovers over the icon in the toolbar.</span></span>  |  
| `default_popup` | <span data-ttu-id="85206-140">La ruta de acceso al archivo HTML de la ventana emergente.</span><span class="sxs-lookup"><span data-stu-id="85206-140">The path to the HTML file for the pop-up window.</span></span>  |  

<span data-ttu-id="85206-141">Ahora que ha creado el archivo de manifiesto, necesita una interfaz de usuario para la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-141">Now that you have created the manifest file, you need a user interface for the extension.</span></span>  

## <span data-ttu-id="85206-142">Crear la ventana emergente</span><span class="sxs-lookup"><span data-stu-id="85206-142">Creating the pop-up</span></span>  

<span data-ttu-id="85206-143">Para su extensión, cree un elemento emergente para la interfaz de usuario, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="85206-143">For your extension, create a pop-up for the user interface, like below.</span></span>  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="La interfaz emergente de la extensión":::
   <span data-ttu-id="85206-145">La interfaz emergente de la extensión</span><span class="sxs-lookup"><span data-stu-id="85206-145">The pop-up interface of the extension</span></span>
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

<span data-ttu-id="85206-146">Cree un archivo con `popup.html` el nombre en la raíz de la `color-changer` carpeta.</span><span class="sxs-lookup"><span data-stu-id="85206-146">Create a file named `popup.html` in the root of your `color-changer` folder.</span></span>  <span data-ttu-id="85206-147">Pegue el código siguiente en `popup.html` .</span><span class="sxs-lookup"><span data-stu-id="85206-147">Paste the following code into `popup.html`.</span></span>  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

<span data-ttu-id="85206-148">En `popup.html` , puedes crear un título, un párrafo y tres botones \ (AliceBlue, Cornsilk y restablecer \).</span><span class="sxs-lookup"><span data-stu-id="85206-148">In `popup.html`, you create a title, a paragraph, and three buttons \(Aliceblue, Cornsilk, and Reset\).</span></span>  

<span data-ttu-id="85206-149">Ahora cree una carpeta con el nombre `css` y dentro de crear un archivo denominado `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="85206-149">Now create a folder named `css` and inside create a file named `styles.css`.</span></span>  <span data-ttu-id="85206-150">Agregue los siguientes estilos.</span><span class="sxs-lookup"><span data-stu-id="85206-150">Add the styles below.</span></span>  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

<span data-ttu-id="85206-151">Esta CSS proporciona a nuestra extensión algunos estilos básicos.</span><span class="sxs-lookup"><span data-stu-id="85206-151">This CSS gives our extension some basic styles.</span></span>  <span data-ttu-id="85206-152">Puede agregar más estilos para personalizar la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-152">Feel free to add more styles to customize your extension.</span></span>  

<span data-ttu-id="85206-153">A continuación, debe crear el archivo JavaScript que interactúa con el elemento emergente.</span><span class="sxs-lookup"><span data-stu-id="85206-153">Next, you must create the JavaScript file that interacts with the pop-up.</span></span>  <span data-ttu-id="85206-154">Cree una `js` carpeta y un archivo con el nombre `popup.js` Inside.</span><span class="sxs-lookup"><span data-stu-id="85206-154">Create a `js` folder and a file named `popup.js` inside.</span></span>  <span data-ttu-id="85206-155">Actualice `popup.js` con el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="85206-155">Update `popup.js` with the following code.</span></span>  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

<span data-ttu-id="85206-156">En `popup.js` , la API de [Tabs][MDNApiTabs] le permite interactuar con las pestañas del explorador e insertar secuencias de comandos y estilos en el contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="85206-156">In `popup.js`, the [tabs][MDNApiTabs] API allows you to interact with the tabs of the browser and inject script and styles into the page content.</span></span>  <span data-ttu-id="85206-157">Con el método [Tabs. insertCSS ()][MDNApiTabsInsertcss] , inyecta el CSS especificado en la página, lo que cambia el encabezado de [docs.Microsoft.com][MicrosoftDocs] a un color diferente cuando se hace clic en el botón especificado.</span><span class="sxs-lookup"><span data-stu-id="85206-157">Using the [tabs.insertCSS()][MDNApiTabsInsertcss] method, you inject the specified CSS into the page which changes the header on [docs.microsoft.com][MicrosoftDocs] to a different color when the specified button is clicked.</span></span>  

<span data-ttu-id="85206-158">Ahora que ya tiene la funcionalidad emergente básica, agregue iconos a la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-158">Now that you have the basic pop-up functionality, add icons to the extension.</span></span>  

## <span data-ttu-id="85206-159">Agregar iconos</span><span class="sxs-lookup"><span data-stu-id="85206-159">Adding icons</span></span>  

<span data-ttu-id="85206-160">Los iconos se usan para representar la extensión en la barra de herramientas del explorador, en el menú extensiones y en otros lugares.</span><span class="sxs-lookup"><span data-stu-id="85206-160">Icons are used to represent the extension in the browser toolbar, the extensions menu, and other places.</span></span>  <span data-ttu-id="85206-161">Descarga los [iconos de tu extensión en github][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span><span class="sxs-lookup"><span data-stu-id="85206-161">Download the [icons for your extension on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span></span> <span data-ttu-id="85206-162">Para obtener más información sobre los iconos de extensión en Microsoft Edge, consulte [Guía de diseño][ExtensionsGuidesDesignIcons].</span><span class="sxs-lookup"><span data-stu-id="85206-162">For more information about extension icons in Microsoft Edge, see [Design Guide][ExtensionsGuidesDesignIcons].</span></span>  

<span data-ttu-id="85206-163">Después de descargar los iconos de extensión, guarde los iconos en una `images` carpeta dentro de `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="85206-163">After you download the extension icons, save the icons in an `images` folder inside `color-changer`.</span></span>  

<span data-ttu-id="85206-164">El icono que aparece en la barra de herramientas se establece mediante `default_icon` la tecla [browser_action][MDNManifestjsonBrowserAction] , que ya agregó al archivo de manifiesto en una sección anterior.</span><span class="sxs-lookup"><span data-stu-id="85206-164">The icon that appears in the toolbar is set using `default_icon` inside of the [browser_action][MDNManifestjsonBrowserAction] key, which you already added to your manifest file in an earlier section.</span></span>  

<span data-ttu-id="85206-165">La `icons` clave define los iconos que se deben usar en los menús de configuración de extensiones.</span><span class="sxs-lookup"><span data-stu-id="85206-165">The `icons` key defines which icons should be used in the Extensions settings menus.</span></span>  <span data-ttu-id="85206-166">A continuación, está especificando varios iconos con diferentes tamaños para tener en cuenta diferentes resoluciones de pantalla.</span><span class="sxs-lookup"><span data-stu-id="85206-166">Below, you are specifying multiple icons with different sizes to account for different screen resolutions.</span></span>  <span data-ttu-id="85206-167">El nombre de los iconos `25` y `48` el alto en píxeles de los iconos.</span><span class="sxs-lookup"><span data-stu-id="85206-167">The name of the icons, `25` and `48` are the heights in pixels of the icons.</span></span>  

<span data-ttu-id="85206-168">En el archivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] , incluye una clave de nivel superior para `icons` .</span><span class="sxs-lookup"><span data-stu-id="85206-168">In the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file, include a top-level key for `icons`.</span></span>  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### <span data-ttu-id="85206-169">Definiciones de clave de manifiesto</span><span class="sxs-lookup"><span data-stu-id="85206-169">Manifest Key definitions</span></span>  

| <span data-ttu-id="85206-170">Key</span><span class="sxs-lookup"><span data-stu-id="85206-170">Key</span></span> | <span data-ttu-id="85206-171">Detalles</span><span class="sxs-lookup"><span data-stu-id="85206-171">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="85206-172">iconos</span><span class="sxs-lookup"><span data-stu-id="85206-172">icons</span></span>][MDNManifestjsonIcons] | <span data-ttu-id="85206-173">Los iconos de la extensión con pares clave-valor en el tamaño de la imagen `px` y la ruta de la imagen en relación con el directorio raíz de la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-173">The icons for your extension with key-value pairs of image size in `px` and image path relative to the root directory of the extension.</span></span> |  

> [!NOTE]
> <span data-ttu-id="85206-174">Use los iconos denominados `inactive##.png` que se encuentran en la carpeta imágenes, más adelante en esta guía.</span><span class="sxs-lookup"><span data-stu-id="85206-174">Use the icons named `inactive##.png` located in the images folder later in this guide.</span></span>  

## <span data-ttu-id="85206-175">Probar la extensión</span><span class="sxs-lookup"><span data-stu-id="85206-175">Testing the extension</span></span>  

<span data-ttu-id="85206-176">Ahora que ha agregado la interfaz de usuario y ha creado iconos, pruebe la extensión.</span><span class="sxs-lookup"><span data-stu-id="85206-176">Now that you have added the user interface and created icons, test your extension.</span></span>  <span data-ttu-id="85206-177">Siga los pasos para [Agregar una extensión][ExtensionsGuidesAddingRemovingExtensionsAdding] a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="85206-177">Walk through the steps for [Adding an extension][ExtensionsGuidesAddingRemovingExtensionsAdding] to Microsoft Edge.</span></span>  <span data-ttu-id="85206-178">Después, vuelva a esta guía.</span><span class="sxs-lookup"><span data-stu-id="85206-178">Afterwards, return to this guide.</span></span>  

<span data-ttu-id="85206-179">Después de agregar la extensión, vaya a cualquier página de [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="85206-179">After you add your extension, navigate to any [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="85206-180">Verá la siguiente ventana emergente después de hacer clic en la acción del explorador.</span><span class="sxs-lookup"><span data-stu-id="85206-180">You should see the following pop-up after clicking on the browser action.</span></span>  <span data-ttu-id="85206-181">El color del cuerpo del [docs.Microsoft.com][MicrosoftDocs] también debe cambiar de color.</span><span class="sxs-lookup"><span data-stu-id="85206-181">The color of the [docs.microsoft.com][MicrosoftDocs] body should also change color.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="El encabezado de Docs.microsoft.com cambió a AliceBlue":::
         <span data-ttu-id="85206-183">El encabezado de Docs.microsoft.com cambió a AliceBlue</span><span class="sxs-lookup"><span data-stu-id="85206-183">Docs.microsoft.com header changed to Aliceblue</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="El encabezado de Docs.microsoft.com cambió a Cornsilk":::
         <span data-ttu-id="85206-185">El encabezado de Docs.microsoft.com cambió a Cornsilk</span><span class="sxs-lookup"><span data-stu-id="85206-185">Docs.microsoft.com header changed to Cornsilk</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

<span data-ttu-id="85206-186">Si encuentra algún error o funcionalidad que no funcione, consulte la guía de las [extensiones de depuración][ExtensionsGuidesDebuggingExtensions] o descargue el [ejemplo completo en github][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="85206-186">If you encounter any errors or functionality that does not work, see the [Debugging extensions][ExtensionsGuidesDebuggingExtensions] guide or download the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="85206-187">Agregar contenido y secuencias de comandos de fondo</span><span class="sxs-lookup"><span data-stu-id="85206-187">Adding content and background scripts</span></span>  

<span data-ttu-id="85206-188">Ir un paso más allá y agregar lógica para deshabilitar la extensión para que no funcione en páginas fuera del dominio [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="85206-188">Go one step further and add logic to disable the extension from working on pages outside the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  

<span data-ttu-id="85206-189">Primero debe crear un [script de contenido][MDNContentScripts].</span><span class="sxs-lookup"><span data-stu-id="85206-189">You must first create a [content script][MDNContentScripts].</span></span>  <span data-ttu-id="85206-190">A continuación, debe crear scripts de contenido que se ejecuten en el contexto de una página web determinada, puedan tener acceso al contenido de una página web y podrán comunicarse con scripts en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="85206-190">Next, you must create content scripts that run in the context of a particular web page, are able to access the content of a web page, and are able to communicate with background scripts.</span></span>  <span data-ttu-id="85206-191">En el `js` directorio, cree un archivo con `content.js` el nombre y agregue el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="85206-191">Inside of your `js` directory, create a file named `content.js` and add the following code.</span></span>  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

<span data-ttu-id="85206-192">Este script obtiene la dirección URL de la página actual a través de `document.location.href` y comprueba si la página actual se encuentra en el dominio [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="85206-192">This script gets the URL of the current page through `document.location.href` and verifies whether the current page is on the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  <span data-ttu-id="85206-193">Si la página no está en el dominio [docs.Microsoft.com][MicrosoftDocs] \ (por ejemplo [https://www.bing.com/][|::ref1::|] \), las rutas de los iconos inactivos \ (iconos gris \) se envían al script de fondo con [Runtime. SendMessage ()][MDNApiRuntimeSendmessage].</span><span class="sxs-lookup"><span data-stu-id="85206-193">If the page is not on the [docs.microsoft.com][MicrosoftDocs] domain \(for example  [https://www.bing.com/][|::ref1::|]\), the paths to the inactive icons \(grayed out icons\) are sent to the background script using [runtime.sendMessage()][MDNApiRuntimeSendmessage].</span></span>  

<span data-ttu-id="85206-194">Debe actualizar el archivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] para incluir la siguiente `content_scripts` clave.</span><span class="sxs-lookup"><span data-stu-id="85206-194">You must update the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file to include the following `content_scripts` key.</span></span>  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### <span data-ttu-id="85206-195">Definiciones de clave de manifiesto</span><span class="sxs-lookup"><span data-stu-id="85206-195">Manifest Key definitions</span></span>  

| <span data-ttu-id="85206-196">Key</span><span class="sxs-lookup"><span data-stu-id="85206-196">Key</span></span> | <span data-ttu-id="85206-197">Detalles</span><span class="sxs-lookup"><span data-stu-id="85206-197">Details</span></span> |  
|:--- |:---- |  
| [<span data-ttu-id="85206-198">content_scripts</span><span class="sxs-lookup"><span data-stu-id="85206-198">content_scripts</span></span>][MDNManifestjsonContentScripts] | <span data-ttu-id="85206-199">Contiene la información sobre qué scripts de contenido debe cargar el explorador.</span><span class="sxs-lookup"><span data-stu-id="85206-199">Contains the information about which content scripts the browser should load.</span></span> |  

#### <span data-ttu-id="85206-200">content_scripts definiciones de clave</span><span class="sxs-lookup"><span data-stu-id="85206-200">content_scripts Key definitions</span></span>  

| <span data-ttu-id="85206-201">Key</span><span class="sxs-lookup"><span data-stu-id="85206-201">Key</span></span> | <span data-ttu-id="85206-202">Detalles</span><span class="sxs-lookup"><span data-stu-id="85206-202">Details</span></span> |  
|:--- |:---- |  
| `matches` <span data-ttu-id="85206-203">\ (requerido \)</span><span class="sxs-lookup"><span data-stu-id="85206-203">\(required\)</span></span> | <span data-ttu-id="85206-204">El modelo de dirección URL que debe coincidir antes de cargar el script de contenido.</span><span class="sxs-lookup"><span data-stu-id="85206-204">The URL pattern to match prior to loading the content script.</span></span> |  
| `js` | <span data-ttu-id="85206-205">El script que debe cargarse en las direcciones URL coincidentes.</span><span class="sxs-lookup"><span data-stu-id="85206-205">The script that should be loaded on matching URLs.</span></span> |  
| `run_at` | <span data-ttu-id="85206-206">Especifica dónde se insertan los archivos JavaScript de la `js` clave.</span><span class="sxs-lookup"><span data-stu-id="85206-206">Specifies where the JavaScript files from the `js` key are injected.</span></span> |  

<span data-ttu-id="85206-207">A continuación, debe crear un [script de fondo][MDNAnatomyExtensionBackgroundScripts].</span><span class="sxs-lookup"><span data-stu-id="85206-207">Next, you must create a [background script][MDNAnatomyExtensionBackgroundScripts].</span></span>  <span data-ttu-id="85206-208">Los scripts de fondo se ejecutan en el fondo del explorador, se ejecutan independientemente de la duración de una página web o ventana del explorador, y pueden comunicarse con scripts de contenido.</span><span class="sxs-lookup"><span data-stu-id="85206-208">Background scripts run in the background of the browser, run independently of the lifetime of a web page or browser window, and are able to communicate with content scripts.</span></span>  

<span data-ttu-id="85206-209">En la `js` carpeta, cree un archivo con `background.js` el nombre y agregue el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="85206-209">Inside of your `js` folder, create a file named `background.js` and add the following code.</span></span>  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

<span data-ttu-id="85206-210">El método [Runtime.][MDNApiRuntimeOnmessage] método de mensaje escucha en [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] de la secuencia de comandos de contenido.</span><span class="sxs-lookup"><span data-stu-id="85206-210">The [runtime.onMessage][MDNApiRuntimeOnmessage] method listens for [runtime.sendMessage()][MDNApiRuntimeSendmessage] from the content script.</span></span>  <span data-ttu-id="85206-211">Si el dominio de la página no es [docs.Microsoft.com][MicrosoftDocs], el método [browserAction. setIcon ()][MDNApiBrowseractionSeticon] establece las rutas de los iconos en las imágenes inactivas.</span><span class="sxs-lookup"><span data-stu-id="85206-211">If the domain of the page is not [docs.microsoft.com][MicrosoftDocs], then [browserAction.setIcon()][MDNApiBrowseractionSeticon] method sets the icon paths to the inactive images.</span></span>  

<span data-ttu-id="85206-212">La secuencia de comandos también deshabilita la acción del explorador \ ([browserAction. Disable][MDApiBrowseractionDisable]\), de modo que los usuarios no puedan hacer clic en la acción del explorador fuera de una página [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="85206-212">The script also disables the browser action \([browserAction.disable][MDApiBrowseractionDisable]\), so that users are not able to click on the browser action outside of a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  

<span data-ttu-id="85206-213">Debe agregar el script de fondo al archivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] .</span><span class="sxs-lookup"><span data-stu-id="85206-213">You must add the background script to the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file.</span></span>  <span data-ttu-id="85206-214">Agregue la siguiente `background` clave al manifiesto.</span><span class="sxs-lookup"><span data-stu-id="85206-214">Add the following `background` key to your manifest.</span></span>  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### <span data-ttu-id="85206-215">Definiciones de clave de manifiesto</span><span class="sxs-lookup"><span data-stu-id="85206-215">Manifest Key definitions</span></span>  

| <span data-ttu-id="85206-216">Key</span><span class="sxs-lookup"><span data-stu-id="85206-216">Key</span></span> | <span data-ttu-id="85206-217">Detalles</span><span class="sxs-lookup"><span data-stu-id="85206-217">Details</span></span>|  
|:--- |:--- |  
| [<span data-ttu-id="85206-218">fondo</span><span class="sxs-lookup"><span data-stu-id="85206-218">background</span></span>][MDNManifestjsonBackground] | <span data-ttu-id="85206-219">Contiene los scripts de fondo.</span><span class="sxs-lookup"><span data-stu-id="85206-219">Contains the background scripts.</span></span> |  

#### <span data-ttu-id="85206-220">definiciones de teclas de fondo</span><span class="sxs-lookup"><span data-stu-id="85206-220">background Key definitions</span></span>  

| <span data-ttu-id="85206-221">Key</span><span class="sxs-lookup"><span data-stu-id="85206-221">Key</span></span> | <span data-ttu-id="85206-222">Detalles</span><span class="sxs-lookup"><span data-stu-id="85206-222">Details</span></span> |  
|:--- |:--- |  
| `scripts` | <span data-ttu-id="85206-223">La ruta de acceso a un archivo JavaScript.</span><span class="sxs-lookup"><span data-stu-id="85206-223">The path to a JavaScript file.</span></span> |  
| `persistent` <span data-ttu-id="85206-224">(obligatorio)</span><span class="sxs-lookup"><span data-stu-id="85206-224">(required)</span></span> | <span data-ttu-id="85206-225">Debe establecerse en `true` o `false` .</span><span class="sxs-lookup"><span data-stu-id="85206-225">This must be set to `true` or `false`.</span></span>  <span data-ttu-id="85206-226">Si se establece en `true` , el script de fondo se carga y se conserva para toda la sección de exploración.</span><span class="sxs-lookup"><span data-stu-id="85206-226">If set to `true`, the background script is loaded and persists for the entire browsing section.</span></span>  <span data-ttu-id="85206-227">Si se establece en `false` , el script de fondo se carga con un retraso y se conserva para la sesión de exploración.</span><span class="sxs-lookup"><span data-stu-id="85206-227">If set to `false`, the background script is loaded with a delay and persists for the browsing session.</span></span> |  

<span data-ttu-id="85206-228">Vuelva a cargar la extensión y vuelva a probar.</span><span class="sxs-lookup"><span data-stu-id="85206-228">Reload your extension and test again.</span></span>  <span data-ttu-id="85206-229">Para volver a cargar la extensión: haga clic en **...** para ver la configuración y más en Microsoft Edge, haga clic en **extensiones**, haga clic en la extensión \ (**cambiador de color**\) y haga clic en **volver a cargar extensión**.</span><span class="sxs-lookup"><span data-stu-id="85206-229">To reload your extension: click the **...** for settings and more in Microsoft Edge, click **Extensions**, click on your extension \(**Color Changer**\), and click **Reload extension**.</span></span>  

<span data-ttu-id="85206-230">Ahora, abra una nueva pestaña o actualice una pestaña existente que no sea una página de [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="85206-230">Now, open a new tab or refresh an existing tab that is not a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="85206-231">Debe ver el icono inactivo y no podrá hacer clic en la acción del explorador.</span><span class="sxs-lookup"><span data-stu-id="85206-231">You should see the inactive icon and not be able to click on the browser action.</span></span>  

<span data-ttu-id="85206-232">¡Enhorabuena!</span><span class="sxs-lookup"><span data-stu-id="85206-232">Congratulations!</span></span>  <span data-ttu-id="85206-233">Has creado una extensión para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="85206-233">You created an extension for Microsoft Edge!</span></span>  <span data-ttu-id="85206-234">Ver el [ejemplo completo en github][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="85206-234">View the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  <span data-ttu-id="85206-235">Continúe leyendo para obtener más información sobre las extensiones.</span><span class="sxs-lookup"><span data-stu-id="85206-235">Continue reading to learn more about extensions.</span></span>  

## <span data-ttu-id="85206-236">Escribir una extensión más compleja</span><span class="sxs-lookup"><span data-stu-id="85206-236">Writing a more complex extension</span></span>  

<span data-ttu-id="85206-237">¿Desea escribir una extensión más compleja?</span><span class="sxs-lookup"><span data-stu-id="85206-237">Want to write a more complex extension?</span></span>  <span data-ttu-id="85206-238">Eche un vistazo a la extensión Beastify de MDN en el artículo, [su segunda extensión][MDNYourSecondWebextension].</span><span class="sxs-lookup"><span data-stu-id="85206-238">Take a look at the Beastify extension on MDN in the article, [Your second extension][MDNYourSecondWebextension].</span></span>  <span data-ttu-id="85206-239">El modelo de extensión de Microsoft Edge difiere ligeramente del modelo de extensión para Firefox, la extensión Beastify creada en [tu segunda extensión][MDNYourSecondWebextension] se adaptaba a la función en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="85206-239">The extension model for Microsoft Edge differs slightly from the extension model for Firefox, the Beastify extension created in [Your second extension][MDNYourSecondWebextension] was adapted to function in Microsoft Edge.</span></span>  <span data-ttu-id="85206-240">Compruébalo en [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span><span class="sxs-lookup"><span data-stu-id="85206-240">Check it out on [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span></span>  

<span data-ttu-id="85206-241">Mientras recorres el artículo de MDN, [tu segunda extensión][MDNYourSecondWebextension], ten en cuenta las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="85206-241">While walking through the article on MDN, [Your second extension][MDNYourSecondWebextension], keep in mind the following sections.</span></span>  

### <span data-ttu-id="85206-242">API</span><span class="sxs-lookup"><span data-stu-id="85206-242">APIs</span></span>  

<span data-ttu-id="85206-243">Consulta la página [API compatibles][ExtensionsAPIsupportApis] para obtener una lista de las API de extensiones admitidas en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="85206-243">See the [Supported APIs][ExtensionsAPIsupportApis] page for a list of supported extensions APIs in Microsoft Edge.</span></span>  

### <span data-ttu-id="85206-244">Tamaños de icono</span><span class="sxs-lookup"><span data-stu-id="85206-244">Icon sizes</span></span>  

<span data-ttu-id="85206-245">Los tamaños de icono de extensión preferidos para Microsoft Edge son `20px` ,, `25px` `30px` y `40px` .</span><span class="sxs-lookup"><span data-stu-id="85206-245">Preferred extension icon sizes for Microsoft Edge are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="85206-246">Otros tamaños admitidos son `19px` , `35px` y `38px` .</span><span class="sxs-lookup"><span data-stu-id="85206-246">Other supported sizes are `19px`, `35px`, and `38px`.</span></span>  <span data-ttu-id="85206-247">Para obtener más información sobre los tamaños de los iconos y procedimientos recomendados, consulte la guía de [diseño][ExtensionsGuidesDesign] .</span><span class="sxs-lookup"><span data-stu-id="85206-247">For more info on icon sizes and best practices, see the [Design][ExtensionsGuidesDesign] guide.</span></span>  

### <span data-ttu-id="85206-248">JavaScript</span><span class="sxs-lookup"><span data-stu-id="85206-248">JavaScript</span></span>  

<span data-ttu-id="85206-249">El modelo de extensión de Microsoft Edge no admite promesas de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="85206-249">The extension model for Microsoft Edge does not support JavaScript Promises.</span></span>  <span data-ttu-id="85206-250">En su lugar, use devoluciones de llamada.</span><span class="sxs-lookup"><span data-stu-id="85206-250">Instead, use callbacks.</span></span>  <span data-ttu-id="85206-251">Para obtener más ejemplos de cómo usar las devoluciones de llamada en una extensión, eche un vistazo a las demostraciones de [impresión rápida][GithubMicrosoftEdgeExtensionsDemosQuickPrint] y de [intercambio de texto][GithubMicrosoftEdgeExtensionsDemosTextSwap] .</span><span class="sxs-lookup"><span data-stu-id="85206-251">For more examples of using callbacks in an extension, take a look at the  [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] and [Text Swap][GithubMicrosoftEdgeExtensionsDemosTextSwap] demos.</span></span>  

<span data-ttu-id="85206-252">Recorra el ejemplo de [impresión rápida][GithubMicrosoftEdgeExtensionsDemosQuickPrint] en el siguiente vídeo.</span><span class="sxs-lookup"><span data-stu-id="85206-252">Walk through the [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] example in the following video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### <span data-ttu-id="85206-253">Manifest. JSON</span><span class="sxs-lookup"><span data-stu-id="85206-253">Manifest.json</span></span>  

*   <span data-ttu-id="85206-254">La `author` clave es necesaria en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="85206-254">The `author` key is required in Microsoft Edge</span></span>  
*   <span data-ttu-id="85206-255">La `activeTab` clave no es compatible con Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="85206-255">The `activeTab` key is not supported in Microsoft Edge</span></span>  

<span data-ttu-id="85206-256">Para obtener más información sobre [las extensiones del explorador][MDNBrowserExtensions], consulte los [documentos web de MDN][MDNWebDocs].</span><span class="sxs-lookup"><span data-stu-id="85206-256">For more information on [Browser Extensions][MDNBrowserExtensions], see [MDN web docs][MDNWebDocs].</span></span>  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Agregar una extensión: agregar, mover y quitar extensiones para Microsoft Edge | Microsoft docs"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Extensiones de depuración | Microsoft docs"  
[ExtensionsGuidesDesign]: ./design.md "Directrices de diseño para Microsoft Edge Extensions | Microsoft docs"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Iconos: pautas de diseño para las extensiones de Microsoft Edge | Microsoft docs"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md "API admitidas | Microsoft docs"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Claves de manifiesto admitidas | Microsoft docs"  

[MicrosoftDocs]: https://docs.microsoft.com "Microsoft docs"  

[MDNWebDocs]: https://developer.mozilla.org "Documentos web de MDN"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Extensiones de explorador | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Anatomía de una extensión | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Scripts en segundo plano: Anatomía de una extensión | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "browserAction. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction. setIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. el mensaje-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. sendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "fichas-API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Tabs. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de contenido | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "autor-manifest. JSON | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "Background-manifest. JSON | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest. JSON | MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Descripción: manifest. JSON | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "iconos-manifest. JSON | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "Name-manifest. JSON | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "Permissions-manifest. JSON | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "version-manifest. JSON | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Tu segunda extensión | MDN"  

[Bing]: https://www.bing.com "Bing"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Cambiador de color-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Imágenes: cambio de color-MicrosoftEdge/MicrosoftEdge-dedemos-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest. JSON-color Changer-MicrosoftEdge/MicrosoftEdge-dedemos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Impresión rápida: MicrosoftEdge/MicrosoftEdge: demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Intercambio de texto: MicrosoftEdge MicrosoftEdge-Extensions-demos | GitHub"  
