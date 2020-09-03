---
description: Obtenga información sobre cómo guardar los cambios realizados en DevTools en el disco.
title: Editar archivos con áreas de trabajo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fd72021e75c536fa38c27ae17e4b1678eb4ca85f
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992725"
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

# <span data-ttu-id="1d38c-104">Editar archivos con áreas de trabajo</span><span class="sxs-lookup"><span data-stu-id="1d38c-104">Edit files with Workspaces</span></span>  

> [!NOTE]
> <span data-ttu-id="1d38c-105">El objetivo de este tutorial es proporcionar práctica práctica para configurar y usar áreas de trabajo, de modo que pueda usar áreas de trabajo en sus propios proyectos.</span><span class="sxs-lookup"><span data-stu-id="1d38c-105">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="1d38c-106">Puede guardar los cambios en el código fuente, en el equipo local, que ha hecho dentro de DevTools después de habilitar las áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1d38c-106">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="1d38c-107">**Requisitos previos**: antes de comenzar con este tutorial, debe saber cómo realizar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="1d38c-107">**Prerequisites**: Before beginning this tutorial, you should know how to perform the following actions.</span></span>  
> 
> *   [<span data-ttu-id="1d38c-108">Usar HTML, CSS y JavaScript para crear una página web</span><span class="sxs-lookup"><span data-stu-id="1d38c-108">Use html, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="1d38c-109">Usar DevTools para realizar cambios básicos en CSS</span><span class="sxs-lookup"><span data-stu-id="1d38c-109">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="1d38c-110">Ejecutar un servidor Web HTTP local</span><span class="sxs-lookup"><span data-stu-id="1d38c-110">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="1d38c-111">Introducción</span><span class="sxs-lookup"><span data-stu-id="1d38c-111">Overview</span></span>  

<span data-ttu-id="1d38c-112">Las áreas de trabajo le permiten guardar un cambio que realiza en DevTools en una copia local del mismo archivo de su equipo.</span><span class="sxs-lookup"><span data-stu-id="1d38c-112">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="1d38c-113">Para este tutorial, debe tener la siguiente configuración en su equipo.</span><span class="sxs-lookup"><span data-stu-id="1d38c-113">For this tutorial, you should have the following settings on your machine.</span></span>  

*   <span data-ttu-id="1d38c-114">Tiene el código fuente de su sitio en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-114">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="1d38c-115">Está ejecutando un servidor Web local desde el directorio de código fuente, de modo que el sitio sea accesible en `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-115">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="1d38c-116">Has abierto `localhost:8080` en Microsoft Edge y estás usando DevTools para cambiar las CSS del sitio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-116">You opened `localhost:8080` in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="1d38c-117">Con las áreas de trabajo habilitadas, los cambios de CSS que realice dentro de DevTools se guardan en el código fuente de su escritorio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-117">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="1d38c-118">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="1d38c-118">Limitations</span></span>  

<span data-ttu-id="1d38c-119">Si está usando un marco moderno, probablemente transforme el código fuente desde un formato que sea fácil de mantener en un formato optimizado para ejecutarse lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="1d38c-119">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  

<span data-ttu-id="1d38c-120">Las áreas de trabajo suelen poder asignar el código optimizado de nuevo al código fuente original con la ayuda de [mapas de origen][TreehouseBlogSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="1d38c-120">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="1d38c-121">Sin embargo, hay una gran variedad de variaciones entre marcos que usan mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="1d38c-121">But there is a lot of variation between frameworks over how each uses source maps.</span></span>  <span data-ttu-id="1d38c-122">DevTools simplemente admite todas las variantes.</span><span class="sxs-lookup"><span data-stu-id="1d38c-122">Devtools simply does support all of the variations.</span></span>  

<span data-ttu-id="1d38c-123">Las áreas de trabajo no funcionan con el siguiente marco.</span><span class="sxs-lookup"><span data-stu-id="1d38c-123">Workspaces is known to not work with the following framework.</span></span>  

*   <span data-ttu-id="1d38c-124">Crear una aplicación de reAct</span><span class="sxs-lookup"><span data-stu-id="1d38c-124">Create React App</span></span>  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <span data-ttu-id="1d38c-125">Característica relacionada: reemplazos locales</span><span class="sxs-lookup"><span data-stu-id="1d38c-125">Related feature: Local overrides</span></span>  

<span data-ttu-id="1d38c-126">Los **reemplazos locales** son otra característica de DevTools similar a las áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1d38c-126">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="1d38c-127">Use reemplazos locales cuando desee experimentar con los cambios realizados en una página y necesite ver los cambios en todas las páginas, pero no le importa asignar los cambios al código fuente de la página.</span><span class="sxs-lookup"><span data-stu-id="1d38c-127">Use Local Overrides when you want to experiment with changes to a page, and you need to see the changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="1d38c-128">Paso 1: configurar</span><span class="sxs-lookup"><span data-stu-id="1d38c-128">Step 1: Set up</span></span>  

<span data-ttu-id="1d38c-129">Complete las acciones siguientes para obtener experiencia práctica con áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="1d38c-129">Complete the following actions, to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="1d38c-130">Configurar la demostración</span><span class="sxs-lookup"><span data-stu-id="1d38c-130">Set up the demo</span></span>  

1.  <span data-ttu-id="1d38c-131">[Abra la demostración][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="1d38c-131">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Un proyecto de problema" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       <span data-ttu-id="1d38c-133">Un proyecto de problema</span><span class="sxs-lookup"><span data-stu-id="1d38c-133">A Glitch project</span></span>  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="1d38c-134">Cree un `app` directorio en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-134">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="1d38c-135">Guarde copias de los archivos desde el `workspaces-demo` directorio en el `app` directorio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-135">Save copies of the files from the `workspaces-demo` directory to the `app` directory.</span></span>  <span data-ttu-id="1d38c-136">En el resto del tutorial, se hace referencia al directorio como `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-136">For the rest of the tutorial, the directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="1d38c-137">Inicie un servidor Web local en `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-137">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="1d38c-138">A continuación encontrará código de ejemplo para el inicio `SimpleHTTPServer` , pero puede usar cualquier servidor que prefiera.</span><span class="sxs-lookup"><span data-stu-id="1d38c-138">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
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
    
1.  <span data-ttu-id="1d38c-139">Abra una pestaña en Microsoft Edge y vaya a la versión hospedada localmente del sitio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-139">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="1d38c-140">Debería poder acceder a ella usando una dirección URL como `localhost:8080` o `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-140">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="1d38c-141">El [número de Puerto][WikiPortURLs] exacto puede ser diferente.</span><span class="sxs-lookup"><span data-stu-id="1d38c-141">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="La demostración" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       <span data-ttu-id="1d38c-143">La demostración</span><span class="sxs-lookup"><span data-stu-id="1d38c-143">The demo</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="1d38c-144">Configurar DevTools</span><span class="sxs-lookup"><span data-stu-id="1d38c-144">Set up DevTools</span></span>  

1.  <span data-ttu-id="1d38c-145">Seleccione `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para abrir el panel de **consola** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="1d38c-145">Select `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Panel de consola" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       <span data-ttu-id="1d38c-147">Panel de **consola**</span><span class="sxs-lookup"><span data-stu-id="1d38c-147">The **Console** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1d38c-148">Elija la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-148">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="1d38c-149">Elija la ficha **filesystem** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-149">Choose the **Filesystem** tab.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Ficha filesystem" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       <span data-ttu-id="1d38c-151">Ficha **filesystem**</span><span class="sxs-lookup"><span data-stu-id="1d38c-151">The **Filesystem** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1d38c-152">Elija **Agregar carpeta al área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="1d38c-152">Choose **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="1d38c-153">Escribe `~/Desktop/app`.</span><span class="sxs-lookup"><span data-stu-id="1d38c-153">Type `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="1d38c-154">Elija **permitir** para dar a DevTools permiso de lectura y escritura en el directorio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-154">Choose **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="1d38c-155">En la ficha **filesystem** , ahora hay un punto verde junto a `index.html` , `script.js` y `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-155">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="1d38c-156">Estos puntos verdes indican que DevTools ha establecido una asignación entre los recursos de red de la página y los archivos de `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-156">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="La ficha filesystem ahora muestra una asignación entre los archivos locales y los de red" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       <span data-ttu-id="1d38c-158">La ficha **filesystem** ahora muestra una asignación entre los archivos locales y los de red</span><span class="sxs-lookup"><span data-stu-id="1d38c-158">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1d38c-159">Paso 2: guardar un cambio de CSS en disco</span><span class="sxs-lookup"><span data-stu-id="1d38c-159">Step 2: Save a CSS change to disk</span></span>  

1.  <span data-ttu-id="1d38c-160">Abra `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-160">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1d38c-161">La `color` propiedad de `h1` elementos se establece en `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-161">The `color` property of `h1` elements is set to `fuchsia`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Ver estilos. CSS en un editor de texto" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       <span data-ttu-id="1d38c-163">Ver `styles.css` en un editor de texto</span><span class="sxs-lookup"><span data-stu-id="1d38c-163">View `styles.css` in a text editor</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1d38c-164">Elija la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-164">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="1d38c-165">Cambie el valor de la `color` propiedad del `<h1>` elemento a su color favorito.</span><span class="sxs-lookup"><span data-stu-id="1d38c-165">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="1d38c-166">Recuerde que debe elegir el `<h1>` elemento en el **árbol DOM** para ver las reglas CSS que se aplican en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-166">Remember that you need to choose the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="1d38c-167">El punto verde junto a `styles.css:1` significa que todos los cambios que realice se asignan a `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-167">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="El indicador verde indica que el archivo está vinculado" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       <span data-ttu-id="1d38c-169">El indicador verde indica que el archivo está vinculado</span><span class="sxs-lookup"><span data-stu-id="1d38c-169">The green indicator that the file is linked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1d38c-170">`styles.css`Vuelva a abrir en un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="1d38c-170">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="1d38c-171">La `color` propiedad ya está configurada con su color favorito.</span><span class="sxs-lookup"><span data-stu-id="1d38c-171">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="1d38c-172">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="1d38c-172">Refresh the page.</span></span>  <span data-ttu-id="1d38c-173">El color del `<h1>` elemento se mantiene establecido en el color que prefiera.</span><span class="sxs-lookup"><span data-stu-id="1d38c-173">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="1d38c-174">El cambio se mantiene durante una actualización, porque cuando realizó el cambio DevTools guardado el cambio en el disco.</span><span class="sxs-lookup"><span data-stu-id="1d38c-174">The change remains across a refresh, because when you made the change DevTools saved the change to disk.</span></span>  <span data-ttu-id="1d38c-175">Y, después, cuando haya actualizado la página, el servidor local ha servido la copia modificada del archivo desde el disco.</span><span class="sxs-lookup"><span data-stu-id="1d38c-175">And then, when you refreshed the page, your local server served the modified copy of the file from disk.</span></span>  
    
## <span data-ttu-id="1d38c-176">Paso 3: guardar un cambio HTML en el disco</span><span class="sxs-lookup"><span data-stu-id="1d38c-176">Step 3: Save an HTML change to disk</span></span>  

### <span data-ttu-id="1d38c-177">Cambiar HTML desde el panel elementos</span><span class="sxs-lookup"><span data-stu-id="1d38c-177">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="1d38c-178">Puede realizar cambios en el HTML desde el panel elemento, pero sus cambios en el árbol DOM no se guardan en el disco y solo afectan a la sesión actual del explorador.</span><span class="sxs-lookup"><span data-stu-id="1d38c-178">You may make changes to the html from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  

<span data-ttu-id="1d38c-179">El árbol DOM no es HTML.</span><span class="sxs-lookup"><span data-stu-id="1d38c-179">The DOM tree is not html.</span></span>  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tab.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** panel  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <span data-ttu-id="1d38c-180">Cambiar HTML desde el panel orígenes</span><span class="sxs-lookup"><span data-stu-id="1d38c-180">Change HTML from the Sources panel</span></span>  

<span data-ttu-id="1d38c-181">Si desea guardar un cambio en el código HTML de la página, hágalo usando el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-181">If you want to save a change to the html of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="1d38c-182">Elija la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-182">Choose the **Sources** tab.</span></span>  
1.  <span data-ttu-id="1d38c-183">Elija la pestaña **Página** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-183">Choose the **Page** tab.</span></span>  
1.  <span data-ttu-id="1d38c-184">Elija **(índice)**.</span><span class="sxs-lookup"><span data-stu-id="1d38c-184">Choose **(index)**.</span></span>  <span data-ttu-id="1d38c-185">Se abrirá el código HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="1d38c-185">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="1d38c-186">Reemplazar `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-186">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="1d38c-187">Consulte la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="1d38c-187">See the following figure.</span></span>  
1.  <span data-ttu-id="1d38c-188">Seleccione `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-188">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="1d38c-189">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="1d38c-189">Refresh the page.</span></span>  <span data-ttu-id="1d38c-190">El `<h1>` elemento aún muestra el nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="1d38c-190">The `<h1>` element is still displaying the new text.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Cambiar HTML desde el panel orígenes" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       <span data-ttu-id="1d38c-192">Cambiar HTML desde el panel **orígenes**</span><span class="sxs-lookup"><span data-stu-id="1d38c-192">Change HTML from the **Sources** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1d38c-193">Abra `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="1d38c-193">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="1d38c-194">El `<h1>` elemento contiene el nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="1d38c-194">The `<h1>` element contains the new text.</span></span>  
    
## <span data-ttu-id="1d38c-195">Paso 4: guardar un cambio de JavaScript en el disco</span><span class="sxs-lookup"><span data-stu-id="1d38c-195">Step 4: Save a JavaScript change to disk</span></span>  

<span data-ttu-id="1d38c-196">El panel **orígenes** también es el lugar donde se pueden realizar cambios en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1d38c-196">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="1d38c-197">Sin embargo, a veces necesita acceder a otros paneles, como el panel **elementos** o el panel de **consola** , mientras realiza cambios en su sitio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-197">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="1d38c-198">Hay una forma de abrir el panel **fuentes** junto con otros paneles.</span><span class="sxs-lookup"><span data-stu-id="1d38c-198">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="1d38c-199">Elija la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-199">Choose the **Elements** tab.</span></span>  
1.  <span data-ttu-id="1d38c-200">Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="1d38c-200">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="1d38c-201">Se abrirá el **menú de comandos** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-201">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="1d38c-202">Escriba `QS` y, a continuación, seleccione **Mostrar fuente rápida**.</span><span class="sxs-lookup"><span data-stu-id="1d38c-202">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="1d38c-203">En la parte inferior de la ventana de DevTools ahora hay una ficha de **fuente rápida** .  La pestaña muestra el contenido de `index.html` , que es el último archivo editado en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-203">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="1d38c-204">La pestaña **origen rápido** le ofrece el editor del panel **fuentes** , de modo que pueda editar archivos mientras tiene otros paneles abiertos.</span><span class="sxs-lookup"><span data-stu-id="1d38c-204">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Abrir la pestaña origen rápido mediante el menú de comandos" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       <span data-ttu-id="1d38c-206">Abrir la pestaña **origen rápido** mediante el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="1d38c-206">Open the **Quick Source** tab using **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1d38c-207">Seleccione `Control` + `P` \ (Windows \) o `Command` + `P` \ (MacOS \) para abrir el cuadro de diálogo **Abrir archivo** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-207">Select `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="1d38c-208">Consulte la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="1d38c-208">See the following figure.</span></span>  
1.  <span data-ttu-id="1d38c-209">Escriba `script` y, a continuación, seleccione **app/script.js**.</span><span class="sxs-lookup"><span data-stu-id="1d38c-209">Type `script`, then select **app/script.js**.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Abrir script.js con el cuadro de diálogo Abrir archivo" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       <span data-ttu-id="1d38c-211">Abrir `script.js` con el cuadro de diálogo **Abrir archivo**</span><span class="sxs-lookup"><span data-stu-id="1d38c-211">Open `script.js` using the **Open File** dialog</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="1d38c-212">El `Save Changes To Disk With Workspaces` vínculo de la demostración se ha estilo regularmente.</span><span class="sxs-lookup"><span data-stu-id="1d38c-212">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="1d38c-213">Agregue el código siguiente en la parte inferior de **script.js** mediante la pestaña de **origen rápido** .</span><span class="sxs-lookup"><span data-stu-id="1d38c-213">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="1d38c-214">Seleccione `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="1d38c-214">Select `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="1d38c-215">Actualiza la página.</span><span class="sxs-lookup"><span data-stu-id="1d38c-215">Refresh the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1d38c-216">El vínculo de la página está en cursiva.</span><span class="sxs-lookup"><span data-stu-id="1d38c-216">The link on the page is now italicized.</span></span>  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="El vínculo de la página se ha en cursiva" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       <span data-ttu-id="1d38c-218">El vínculo de la página se ha en cursiva</span><span class="sxs-lookup"><span data-stu-id="1d38c-218">The link on the page is now italicized</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="1d38c-219">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="1d38c-219">Next steps</span></span>  

<span data-ttu-id="1d38c-220">Use lo que ha aprendido en este tutorial para configurar áreas de trabajo en su propio proyecto.</span><span class="sxs-lookup"><span data-stu-id="1d38c-220">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
    -->  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Archivos de demostración de áreas de trabajo | Intento"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Contenido-CSS: hojas de estilos en cascada | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Introducción a la web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Ejecutando un servidor HTTP local simple | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introducción a DOM-API Web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Introducción a los mapas de origen | Blog de Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Puerto \ (red del equipo \)-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="1d38c-229">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1d38c-229">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1d38c-230">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1d38c-230">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1d38c-232">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1d38c-232">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
