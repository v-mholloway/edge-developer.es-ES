---
description: Obtenga información sobre cómo guardar los cambios realizados en DevTools en el disco.
title: Editar archivos con Áreas de trabajo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f00e2e42f73f7d03c858deaf020db683391ff1f2
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519425"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="edit-files-with-workspaces"></a><span data-ttu-id="9b9ba-104">Editar archivos con Áreas de trabajo</span><span class="sxs-lookup"><span data-stu-id="9b9ba-104">Edit files with Workspaces</span></span>  

<span data-ttu-id="9b9ba-105">Este tutorial proporciona prácticas para configurar y usar un área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-105">This tutorial provides hands-on practice in setting up and using a Workspace.</span></span>  <span data-ttu-id="9b9ba-106">Después de agregar archivos a un área de trabajo, los cambios realizados en el código fuente dentro de DevTools se guardan en el equipo local y se conservan después de actualizar la página web.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-106">After you add files to a Workspace, the changes that you make in your source code within DevTools are saved on your local computer, and are preserved after you refresh the webpage.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9b9ba-107">**Requisitos previos:** antes de comenzar este tutorial, debe saber cómo realizar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-107">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="9b9ba-108">Usar html, CSS y JavaScript para crear una página web</span><span class="sxs-lookup"><span data-stu-id="9b9ba-108">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="9b9ba-109">Usar DevTools para realizar cambios básicos en CSS</span><span class="sxs-lookup"><span data-stu-id="9b9ba-109">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="9b9ba-110">Ejecutar un servidor web HTTP local</span><span class="sxs-lookup"><span data-stu-id="9b9ba-110">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a><span data-ttu-id="9b9ba-111">Información general</span><span class="sxs-lookup"><span data-stu-id="9b9ba-111">Overview</span></span>  

<span data-ttu-id="9b9ba-112">Las áreas de trabajo permiten guardar un cambio que realice en Devtools en una copia local del mismo archivo en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-112">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="9b9ba-113">Para este tutorial, debe tener la siguiente configuración en el equipo.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-113">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="9b9ba-114">Tiene el código fuente del sitio en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-114">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="9b9ba-115">Está ejecutando un servidor web local desde el directorio de código fuente, de modo que el sitio sea accesible en `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-115">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="9b9ba-116">Se abrió `localhost:8080` en Microsoft Edge y se usa DevTools para cambiar el CSS del sitio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-116">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="9b9ba-117">Con Workspaces habilitado, los cambios CSS que realices en DevTools se guardan en el código fuente del escritorio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-117">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <a name="limitations"></a><span data-ttu-id="9b9ba-118">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="9b9ba-118">Limitations</span></span>  

<span data-ttu-id="9b9ba-119">Si usa un marco moderno, probablemente transforme el código fuente de un formato fácil de mantener en un formato optimizado para ejecutarse lo más rápido posible.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-119">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="9b9ba-120">Las áreas de trabajo normalmente pueden asignar el código optimizado al código fuente original con la ayuda de [mapas de origen.][TreehouseBlogSourceMaps]</span><span class="sxs-lookup"><span data-stu-id="9b9ba-120">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="9b9ba-121">Pero hay mucha variación entre marcos sobre cómo cada marco usa mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-121">But there is a lot of variation between frameworks over how each framework uses source maps.</span></span>  <span data-ttu-id="9b9ba-122">Devtools no admite todas las variaciones.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-122">Devtools doesn't support all of the variations.</span></span>  

<span data-ttu-id="9b9ba-123">Se sabe que las áreas de trabajo no funcionan con el siguiente marco.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-123">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="9b9ba-124">Crear aplicación React</span><span class="sxs-lookup"><span data-stu-id="9b9ba-124">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a><span data-ttu-id="9b9ba-125">Característica relacionada: invalidaciones locales</span><span class="sxs-lookup"><span data-stu-id="9b9ba-125">Related feature: Local overrides</span></span>  

<span data-ttu-id="9b9ba-126">**Invalidaciones locales es** otra característica de DevTools similar a Workspaces.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-126">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="9b9ba-127">Usa Invalidaciones locales cuando quieras experimentar con los cambios en una página web y debes mostrar los cambios en las cargas de páginas web, pero no te importa asignar los cambios al código fuente de la página web.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-127">Use Local Overrides when you want to experiment with changes to a webpage, and you need to display the changes across webpage loads, but you do not care about mapping your changes to the source code of the webpage.</span></span>  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a><span data-ttu-id="9b9ba-128">Paso 1: Configurar</span><span class="sxs-lookup"><span data-stu-id="9b9ba-128">Step 1: Set up</span></span>  

<span data-ttu-id="9b9ba-129">Complete las siguientes acciones para obtener experiencia práctica con Workspaces.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-129">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <a name="set-up-the-demo"></a><span data-ttu-id="9b9ba-130">Configurar la demostración</span><span class="sxs-lookup"><span data-stu-id="9b9ba-130">Set up the demo</span></span>  

1.  <span data-ttu-id="9b9ba-131">[Abra la demostración][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="9b9ba-131">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Un proyecto de glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="9b9ba-133">Un proyecto de glitch</span><span class="sxs-lookup"><span data-stu-id="9b9ba-133">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="9b9ba-134">Cree un `app` directorio en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-134">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="9b9ba-135">Guarde copias de los archivos del `workspaces-demo` directorio en el `app` directorio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-135">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="9b9ba-136">Para el resto del tutorial, el directorio se conoce como `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-136">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="9b9ba-137">Inicie un servidor web local en `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-137">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="9b9ba-138">A continuación se muestra un código de ejemplo para iniciar, pero `SimpleHTTPServer` puede usar el servidor que prefiera.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-138">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="9b9ba-139">Abra una pestaña en Microsoft Edge y vaya a la versión hospedada localmente del sitio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-139">Open a tab in Microsoft Edge and navigate to locally-hosted version of the site.</span></span>  <span data-ttu-id="9b9ba-140">Debe tener acceso a ella mediante una dirección URL como `localhost:8080` o `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-140">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="9b9ba-141">El número [de puerto exacto][WikiPortURLs] puede ser diferente.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-141">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="La demostración" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="9b9ba-143">La demostración</span><span class="sxs-lookup"><span data-stu-id="9b9ba-143">The demo</span></span>  
    :::image-end:::  
    
### <a name="set-up-devtools"></a><span data-ttu-id="9b9ba-144">Configurar DevTools</span><span class="sxs-lookup"><span data-stu-id="9b9ba-144">Set up DevTools</span></span>  

1.  <span data-ttu-id="9b9ba-145">Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\) para abrir el panel Consola de DevTools. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9b9ba-145">Select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Panel consola" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="9b9ba-147">Panel **consola**</span><span class="sxs-lookup"><span data-stu-id="9b9ba-147">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b9ba-148">Vaya a la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="9b9ba-148">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="9b9ba-149">En el **panel Navegador** (a la izquierda), elija la pestaña **Sistema de** archivos.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-149">In the **Navigator** pane (on the left), choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Ficha Sistema de archivos" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="9b9ba-151">Ficha **Sistema de** archivos</span><span class="sxs-lookup"><span data-stu-id="9b9ba-151">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b9ba-152">Elija **Agregar carpeta al área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-152">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="9b9ba-153">Escriba `~/Desktop/app`.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-153">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="9b9ba-154">Elija **Permitir** para conceder permiso a DevTools para leer y escribir en el directorio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-154">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="9b9ba-155">En la **pestaña Sistema de** archivos, ahora aparece un punto verde junto a , y `index.html` `script.js` `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-155">In the **Filesystem** tab, a green dot now appears next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="9b9ba-156">Un punto verde indica que DevTools ha establecido una asignación entre un recurso de red de la página y el archivo en `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-156">A green dot indicates that DevTools has established a mapping between a network resource of the page, and the file in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="La pestaña Sistema de archivos ahora indica una asignación entre los archivos locales y los de red" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="9b9ba-158">La **pestaña Sistema de** archivos ahora indica una asignación entre los archivos locales y los de red</span><span class="sxs-lookup"><span data-stu-id="9b9ba-158">The **Filesystem** tab now indicates a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a><span data-ttu-id="9b9ba-159">Paso 2: Guardar un cambio css en disco</span><span class="sxs-lookup"><span data-stu-id="9b9ba-159">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="9b9ba-160">Abra `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-160">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9b9ba-161">La `color` propiedad de los elementos se establece en `h1` `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-161">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Ver styles.css en un editor de texto" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="9b9ba-163">Ver `styles.css` en un editor de texto</span><span class="sxs-lookup"><span data-stu-id="9b9ba-163">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b9ba-164">Elija la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-164">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="9b9ba-165">Cambia el valor de la `color` propiedad del elemento a tu color `<h1>` favorito.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-165">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="9b9ba-166">Recuerde que debe elegir el elemento en el árbol DOM para mostrar las reglas CSS que se le aplican `<h1>` en el panel **Estilos.** \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9b9ba-166">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to display the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="9b9ba-167">El punto verde junto `styles.css:1` a significa que cualquier cambio que realice se asigna a `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-167">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="El indicador verde de que el archivo está vinculado" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="9b9ba-169">El indicador verde de que el archivo está vinculado</span><span class="sxs-lookup"><span data-stu-id="9b9ba-169">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b9ba-170">Abra `styles.css` de nuevo en un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-170">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="9b9ba-171">La `color` propiedad ahora está establecida en el color favorito.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-171">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="9b9ba-172">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-172">Refresh the page.</span></span>  <span data-ttu-id="9b9ba-173">El color del `<h1>` elemento aún está establecido en el color favorito.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-173">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="9b9ba-174">El cambio permanece en una actualización, porque al realizar el cambio DevTools guardó el cambio en el disco.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-174">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="9b9ba-175">Después, al actualizar la página, el servidor local sirvió la copia modificada del archivo desde el disco.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-175">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <a name="step-3-save-an-html-change-to-disk"></a><span data-ttu-id="9b9ba-176">Paso 3: Guardar un cambio HTML en disco</span><span class="sxs-lookup"><span data-stu-id="9b9ba-176">Step 3: Save an HTML change to disk</span></span>  

### <a name="change-html-from-the-elements-panel"></a><span data-ttu-id="9b9ba-177">Cambiar HTML desde el Panel de elementos</span><span class="sxs-lookup"><span data-stu-id="9b9ba-177">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="9b9ba-178">Puede realizar cambios en el html desde el Panel de elementos, pero los cambios realizados en el árbol DOM no se guardan en el disco y solo tienen efecto en la sesión del explorador actual.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-178">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="9b9ba-179">El árbol DOM no es html.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-179">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-tool"></a><span data-ttu-id="9b9ba-180">Cambiar HTML desde la herramienta Orígenes</span><span class="sxs-lookup"><span data-stu-id="9b9ba-180">Change HTML from the Sources tool</span></span>  

<span data-ttu-id="9b9ba-181">Si desea guardar un cambio en el HTML de la página web, use la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-181">If you want to save a change to the HTML of the webpage, use the **Sources** tool.</span></span>  

1.  <span data-ttu-id="9b9ba-182">Vaya a la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="9b9ba-182">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="9b9ba-183">En el **panel** Navegador (a la izquierda), elija la **pestaña** Página.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-183">In the **Navigator** pane (on the left), choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="9b9ba-184">Elija **(índice)**.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-184">Choose **(index)**.</span></span>  <span data-ttu-id="9b9ba-185">Se abre el CÓDIGO HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-185">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="9b9ba-186">Reemplace `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-186">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="9b9ba-187">Revise la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-187">Review the following figure.</span></span>  
1.  <span data-ttu-id="9b9ba-188">Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-188">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="9b9ba-189">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-189">Refresh the page.</span></span>  <span data-ttu-id="9b9ba-190">El `<h1>` elemento sigue mostrando el texto nuevo después de actualizar la página.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-190">The `<h1>` element continues to display the new text after the page is refreshed.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Cambiar HTML desde la herramienta Orígenes" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="9b9ba-192">Cambiar HTML desde la **herramienta Orígenes**</span><span class="sxs-lookup"><span data-stu-id="9b9ba-192">Change HTML from the **Sources** tool</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b9ba-193">Abra `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="9b9ba-193">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="9b9ba-194">El `<h1>` elemento contiene el texto nuevo.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-194">The `<h1>` element contains the new text.</span></span>  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a><span data-ttu-id="9b9ba-195">Paso 4: Guardar un cambio de JavaScript en disco</span><span class="sxs-lookup"><span data-stu-id="9b9ba-195">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="9b9ba-196">El lugar principal para usar el editor de código de DevTools es la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="9b9ba-196">The main place to use the code editor of DevTools is the **Sources** tool.</span></span>  <span data-ttu-id="9b9ba-197">Pero a veces es necesario tener acceso a otras herramientas, como la **herramienta Elementos** o el panel **Consola,** mientras se editan archivos.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-197">But sometimes you need to access other tools, such as the **Elements** tool or the **Console** panel, while editing files.</span></span>  <span data-ttu-id="9b9ba-198">La **herramienta Origen rápido** le proporciona solo el editor de la herramienta **Orígenes,** mientras que cualquier herramienta está abierta.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-198">The **Quick Source** tool gives you just the editor from the **Sources** tool, while any tool is open.</span></span>  

<span data-ttu-id="9b9ba-199">Para abrir el editor de código DevTools junto con otras herramientas, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="9b9ba-199">To open the DevTools code editor alongside other tools, do the following:</span></span>  

1.  <span data-ttu-id="9b9ba-200">Vaya a la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-200">Navigate to the **Elements** tool.</span></span>  
1.  <span data-ttu-id="9b9ba-201">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="9b9ba-201">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="9b9ba-202">Se **abre el menú** comando.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-202">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="9b9ba-203">Escriba `Quick Source` y, a continuación, **elija Mostrar origen rápido**.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-203">Type `Quick Source`, and then choose **Show Quick Source**.</span></span>  <span data-ttu-id="9b9ba-204">En la parte inferior de la ventana DevTools, aparece la herramienta **Origen** rápido, que muestra el contenido de , que es el último archivo que editó `index.html` en la **herramienta** Orígenes.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-204">At the bottom of the DevTools window, the **Quick Source** tool appears, displaying the contents of `index.html`, which is the last file you edited in the **Sources** tool.</span></span>    
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Abra la herramienta Origen rápido mediante el menú Comando" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="9b9ba-206">Abra la **herramienta Origen rápido** mediante el menú **Comando**</span><span class="sxs-lookup"><span data-stu-id="9b9ba-206">Open the **Quick Source** tool by using the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9b9ba-207">Seleccione `Control` + `P` \(Windows, Linux\) o `Command` + `P` \(macOS\) para abrir el **cuadro de diálogo Abrir** archivo.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-207">Select `Control`+`P` \(Windows, Linux\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="9b9ba-208">Revise la siguiente figura.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-208">Review the following figure.</span></span>  
1.  <span data-ttu-id="9b9ba-209">Escriba `script` , luego elija **app/script.js**.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-209">Type `script`, then choose **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Abra script.js mediante el cuadro de diálogo Abrir archivo" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="9b9ba-211">Abrir `script.js` con el cuadro de diálogo **Abrir** archivo</span><span class="sxs-lookup"><span data-stu-id="9b9ba-211">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="9b9ba-212">El `Save Changes To Disk With Workspaces` vínculo de la demostración tiene un estilo regular.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-212">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="9b9ba-213">Agregue el siguiente código a la parte inferior de **script.js** mediante la **herramienta Origen** rápido.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-213">Add the following code to the bottom of **script.js** using the **Quick Source** tool.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="9b9ba-214">Seleccione `Control` + `S` \(Windows, Linux\) o `Command` + `S` \(macOS\) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-214">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="9b9ba-215">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-215">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9b9ba-216">El vínculo de la página ahora está en cursiva.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-216">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="El vínculo de la página ahora está en cursiva" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="9b9ba-218">El vínculo de la página ahora está en cursiva</span><span class="sxs-lookup"><span data-stu-id="9b9ba-218">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="9b9ba-219">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="9b9ba-219">Next steps</span></span>  

<span data-ttu-id="9b9ba-220">Usa lo que has aprendido en este tutorial para configurar áreas de trabajo en tu propio proyecto.</span><span class="sxs-lookup"><span data-stu-id="9b9ba-220">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9b9ba-221">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9b9ba-221">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Introducción a la visualización y cambio de css | Microsoft Docs"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Workspaces Archivos de demostración | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Contenido : CSS: hojas de estilos en cascada | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Introducción al sitio web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Ejecutar un servidor HTTP local simple | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM: API web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Una introducción a los mapas de origen | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \(computer networking\) - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="9b9ba-230">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9b9ba-230">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9b9ba-231">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9b9ba-231">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9b9ba-233">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9b9ba-233">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
