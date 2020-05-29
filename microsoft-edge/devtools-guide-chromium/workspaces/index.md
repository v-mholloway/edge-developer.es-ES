---
title: Editar archivos con áreas de trabajo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601855"
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







# <span data-ttu-id="19e64-103">Editar archivos con áreas de trabajo</span><span class="sxs-lookup"><span data-stu-id="19e64-103">Edit Files With Workspaces</span></span>   



> [!NOTE]
> <span data-ttu-id="19e64-104">El objetivo de este tutorial es proporcionar práctica práctica para configurar y usar áreas de trabajo, de modo que pueda usar áreas de trabajo en sus propios proyectos.</span><span class="sxs-lookup"><span data-stu-id="19e64-104">The goal of this tutorial is to provide hands-on practice in setting up and using Workspaces, so that you are able to use Workspaces in your own projects.</span></span>  <span data-ttu-id="19e64-105">Puede guardar los cambios en el código fuente, en el equipo local, que ha hecho dentro de DevTools después de habilitar las áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="19e64-105">You are able to save the changes to the source code, on your local computer, that you made within DevTools after you enable Workspaces.</span></span>  

> [!CAUTION]
> <span data-ttu-id="19e64-106">**Requisitos previos**: antes de comenzar con este tutorial, debe saber cómo:</span><span class="sxs-lookup"><span data-stu-id="19e64-106">**Prerequisites**: Before beginning this tutorial, you should know how to:</span></span>  
> *   [<span data-ttu-id="19e64-107">Usar HTML, CSS y JavaScript para crear una página web</span><span class="sxs-lookup"><span data-stu-id="19e64-107">Use HTML, CSS, and JavaScript to build a web page</span></span>][MDNWebGettingStarted]  
> *   [<span data-ttu-id="19e64-108">Usar DevTools para realizar cambios básicos en CSS</span><span class="sxs-lookup"><span data-stu-id="19e64-108">Use DevTools to make basic changes to CSS</span></span>][DevToolsCssIndex]  
> *   [<span data-ttu-id="19e64-109">Ejecutar un servidor Web HTTP local</span><span class="sxs-lookup"><span data-stu-id="19e64-109">Run a local HTTP web server</span></span>][MDNSimpleLocalHTTPServer]  

## <span data-ttu-id="19e64-110">Introducción</span><span class="sxs-lookup"><span data-stu-id="19e64-110">Overview</span></span>   

<span data-ttu-id="19e64-111">Las áreas de trabajo le permiten guardar un cambio que realiza en DevTools en una copia local del mismo archivo de su equipo.</span><span class="sxs-lookup"><span data-stu-id="19e64-111">Workspaces enable you to save a change that you make in Devtools to a local copy of the same file on your computer.</span></span>  <span data-ttu-id="19e64-112">Por ejemplo, supongamos que:</span><span class="sxs-lookup"><span data-stu-id="19e64-112">For example, suppose:</span></span>  

*   <span data-ttu-id="19e64-113">Tiene el código fuente de su sitio en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="19e64-113">You have the source code for your site on your desktop.</span></span>  
*   <span data-ttu-id="19e64-114">Está ejecutando un servidor Web local desde el directorio de código fuente, de modo que el sitio sea accesible en `localhost:8080` .</span><span class="sxs-lookup"><span data-stu-id="19e64-114">You are running a local web server from the source code directory, so that the site is accessible at `localhost:8080`.</span></span>  
*   <span data-ttu-id="19e64-115">Has abierto `localhost:8080` en Microsoft Edge y estás usando DevTools para cambiar las CSS del sitio.</span><span class="sxs-lookup"><span data-stu-id="19e64-115">You opened `localhost:8080`  in Microsoft Edge, and you are using DevTools to change the CSS of the site.</span></span>  

<span data-ttu-id="19e64-116">Con las áreas de trabajo habilitadas, los cambios de CSS que realice dentro de DevTools se guardan en el código fuente de su escritorio.</span><span class="sxs-lookup"><span data-stu-id="19e64-116">With Workspaces enabled, the CSS changes that you make within DevTools are saved to the source code on your desktop.</span></span>  

## <span data-ttu-id="19e64-117">Limitaciones</span><span class="sxs-lookup"><span data-stu-id="19e64-117">Limitations</span></span>   

<span data-ttu-id="19e64-118">Si está usando un marco moderno, probablemente transforme el código fuente desde un formato que sea fácil de mantener en un formato optimizado para ejecutarse lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="19e64-118">If you are using a modern framework, it probably transforms your source code from a format that is easy to maintain into a format that is optimized to run as quickly as possible.</span></span>  
<span data-ttu-id="19e64-119">Las áreas de trabajo suelen poder asignar el código optimizado de nuevo al código fuente original con la ayuda de [mapas de origen][TreehouseBlogSourceMaps].</span><span class="sxs-lookup"><span data-stu-id="19e64-119">Workspaces is usually able to map the optimized code back to your original source code with the help of [source maps][TreehouseBlogSourceMaps].</span></span>  <span data-ttu-id="19e64-120">Sin embargo, hay una gran variación entre los marcos sobre cómo usan mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="19e64-120">But there is a lot of variation between frameworks over how they use source maps.</span></span>  <span data-ttu-id="19e64-121">DevTools simplemente admite todas las variantes.</span><span class="sxs-lookup"><span data-stu-id="19e64-121">Devtools simply does support all the variations.</span></span>  

<span data-ttu-id="19e64-122">Las áreas de trabajo no funcionan con estos marcos:</span><span class="sxs-lookup"><span data-stu-id="19e64-122">Workspaces is known to not work with these frameworks:</span></span>  

*   <span data-ttu-id="19e64-123">Crear una aplicación de reAct</span><span class="sxs-lookup"><span data-stu-id="19e64-123">Create React App</span></span>  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## <span data-ttu-id="19e64-124">Característica relacionada: reemplazos locales</span><span class="sxs-lookup"><span data-stu-id="19e64-124">Related feature: Local Overrides</span></span>   

<span data-ttu-id="19e64-125">Los **reemplazos locales** son otra característica de DevTools similar a las áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="19e64-125">**Local Overrides** is another DevTools feature that is similar to Workspaces.</span></span>  <span data-ttu-id="19e64-126">Use reemplazos locales cuando desee experimentar con los cambios realizados en una página y necesite ver los cambios en todas las páginas, pero no le importa asignar los cambios al código fuente de la página.</span><span class="sxs-lookup"><span data-stu-id="19e64-126">Use Local Overrides when you want to experiment with changes to a page, and you need to see those changes across page loads, but you do not care about mapping your changes to the source code of the page.</span></span>  

<!--Todo: add section when content is ready  -->  

## <span data-ttu-id="19e64-127">Paso 1: configuración</span><span class="sxs-lookup"><span data-stu-id="19e64-127">Step 1: Setup</span></span>   

<span data-ttu-id="19e64-128">Complete este tutorial para obtener experiencia práctica con áreas de trabajo.</span><span class="sxs-lookup"><span data-stu-id="19e64-128">Complete this tutorial to get hands-on experience with Workspaces.</span></span>  

### <span data-ttu-id="19e64-129">Configurar la demostración</span><span class="sxs-lookup"><span data-stu-id="19e64-129">Set up the demo</span></span>   

1.  <span data-ttu-id="19e64-130">[Abra la demostración][GlitchWorkspacesDemo].</span><span class="sxs-lookup"><span data-stu-id="19e64-130">[Open the demo][GlitchWorkspacesDemo].</span></span>  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### <span data-ttu-id="19e64-131">Figura 1</span><span class="sxs-lookup"><span data-stu-id="19e64-131">Figure 1</span></span>  
    > <span data-ttu-id="19e64-132">Un proyecto de problema en ![ un proyecto de problema][ImageGlitchProject]</span><span class="sxs-lookup"><span data-stu-id="19e64-132">A Glitch project ![A Glitch project][ImageGlitchProject]</span></span>  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  <span data-ttu-id="19e64-133">Cree un `app` directorio en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="19e64-133">Create an `app` directory on your desktop.</span></span>  <span data-ttu-id="19e64-134">Guarde copias de los archivos en el `workspaces-demo` directorio.</span><span class="sxs-lookup"><span data-stu-id="19e64-134">Save copies of the files in the `workspaces-demo` directory.</span></span>  <span data-ttu-id="19e64-135">Para el resto de este tutorial, este directorio se conoce como `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="19e64-135">For the rest of this tutorial this directory is referred to as `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="19e64-136">Inicie un servidor Web local en `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="19e64-136">Start a local web server in `~/Desktop/app`.</span></span>  <span data-ttu-id="19e64-137">A continuación encontrará código de ejemplo para el inicio `SimpleHTTPServer` , pero puede usar cualquier servidor que prefiera.</span><span class="sxs-lookup"><span data-stu-id="19e64-137">Below is some sample code for starting up `SimpleHTTPServer`, but you may use whatever server you prefer.</span></span>  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  <span data-ttu-id="19e64-138">Abra una pestaña en Microsoft Edge y vaya a la versión hospedada localmente del sitio.</span><span class="sxs-lookup"><span data-stu-id="19e64-138">Open a tab in Microsoft Edge and go to locally-hosted version of the site.</span></span>  <span data-ttu-id="19e64-139">Debería poder acceder a ella usando una dirección URL como `localhost:8080` o `http://0.0.0.0:8080` .</span><span class="sxs-lookup"><span data-stu-id="19e64-139">You should be able to access it using a URL like `localhost:8080` or `http://0.0.0.0:8080`.</span></span>  <span data-ttu-id="19e64-140">El [número de Puerto][WikiPortURLs] exacto puede ser diferente.</span><span class="sxs-lookup"><span data-stu-id="19e64-140">The exact [port number][WikiPortURLs] may be different.</span></span>  
    
    > ##### <span data-ttu-id="19e64-141">Figura 2</span><span class="sxs-lookup"><span data-stu-id="19e64-141">Figure 2</span></span>  
    > <span data-ttu-id="19e64-142">La demostración</span><span class="sxs-lookup"><span data-stu-id="19e64-142">The demo</span></span>  
    > <span data-ttu-id="19e64-143">! [Demostración] [ImageDemo]</span><span class="sxs-lookup"><span data-stu-id="19e64-143">![The demo][ImageDemo]</span></span>  

### <span data-ttu-id="19e64-144">Configurar DevTools</span><span class="sxs-lookup"><span data-stu-id="19e64-144">Set up DevTools</span></span>   

1.  <span data-ttu-id="19e64-145">Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para abrir el panel de **consola** de DevTools.</span><span class="sxs-lookup"><span data-stu-id="19e64-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console** panel of DevTools.</span></span>  
    
    > ##### <span data-ttu-id="19e64-146">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="19e64-146">Figure 3</span></span>  
    > <span data-ttu-id="19e64-147">Panel de **consola**</span><span class="sxs-lookup"><span data-stu-id="19e64-147">The **Console** panel</span></span>  
    > <span data-ttu-id="19e64-148">! [Panel de consola] [ImageConsolePanel]</span><span class="sxs-lookup"><span data-stu-id="19e64-148">![The Console panel][ImageConsolePanel]</span></span>  

1.  <span data-ttu-id="19e64-149">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="19e64-149">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="19e64-150">Haga clic en la pestaña **sistema de archivos** .</span><span class="sxs-lookup"><span data-stu-id="19e64-150">Click the **Filesystem** tab.</span></span>  
    
    > ##### <span data-ttu-id="19e64-151">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="19e64-151">Figure 4</span></span>  
    > <span data-ttu-id="19e64-152">Ficha **filesystem**</span><span class="sxs-lookup"><span data-stu-id="19e64-152">The **Filesystem** tab</span></span>  
    > <span data-ttu-id="19e64-153">! [Ficha filesystem] [ImageFilesystem]</span><span class="sxs-lookup"><span data-stu-id="19e64-153">![The Filesystem tab][ImageFilesystem]</span></span>  

1.  <span data-ttu-id="19e64-154">Haga clic en **Agregar carpeta al área de trabajo**.</span><span class="sxs-lookup"><span data-stu-id="19e64-154">Click **Add Folder To Workspace**.</span></span>  
1.  <span data-ttu-id="19e64-155">Seleccione `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="19e64-155">Select `~/Desktop/app`.</span></span>  
1.  <span data-ttu-id="19e64-156">Haga clic en **permitir** para dar a DevTools permiso de lectura y escritura en el directorio.</span><span class="sxs-lookup"><span data-stu-id="19e64-156">Click **Allow** to give DevTools permission to read and write to the directory.</span></span>  
    <span data-ttu-id="19e64-157">En la ficha **filesystem** , ahora hay un punto verde junto a `index.html` , `script.js` y `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="19e64-157">In the **Filesystem** tab, there is now a green dot next to `index.html`, `script.js`, and `styles.css`.</span></span>  <span data-ttu-id="19e64-158">Estos puntos verdes indican que DevTools ha establecido una asignación entre los recursos de red de la página y los archivos de `~/Desktop/app` .</span><span class="sxs-lookup"><span data-stu-id="19e64-158">These green dots mean that DevTools has established a mapping between the network resources of the page, and the files in `~/Desktop/app`.</span></span>  
    
    > ##### <span data-ttu-id="19e64-159">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="19e64-159">Figure 5</span></span>  
    > <span data-ttu-id="19e64-160">La ficha **filesystem** ahora muestra una asignación entre los archivos locales y los de red</span><span class="sxs-lookup"><span data-stu-id="19e64-160">The **Filesystem** tab now shows a mapping between the local files and the network ones</span></span>  
    > <span data-ttu-id="19e64-161">! [La ficha filesystem ahora muestra una asignación entre los archivos locales y las redes] [ImageMapping]</span><span class="sxs-lookup"><span data-stu-id="19e64-161">![The Filesystem tab now shows a mapping between the local files and the network ones][ImageMapping]</span></span>  

## <span data-ttu-id="19e64-162">Paso 2: guardar un cambio de CSS en disco</span><span class="sxs-lookup"><span data-stu-id="19e64-162">Step 2: Save a CSS change to disk</span></span>   

1.  <span data-ttu-id="19e64-163">Abra `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="19e64-163">Open `styles.css`.</span></span>  
    
    > [!NOTE]
    ><span data-ttu-id="19e64-164">La `color` propiedad de `h1` elementos se establece en `fuchsia` .</span><span class="sxs-lookup"><span data-stu-id="19e64-164">The `color` property of `h1` elements is set to `fuchsia`.</span></span>
    
    > ##### <span data-ttu-id="19e64-165">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="19e64-165">Figure 6</span></span>  
    > <span data-ttu-id="19e64-166">Ver `styles.css` en un editor de texto</span><span class="sxs-lookup"><span data-stu-id="19e64-166">Viewing `styles.css` in a text editor</span></span>  
    > <span data-ttu-id="19e64-167">! [Visualizando Styles. CSS en un editor de texto] [ImageStylesFuchsia]</span><span class="sxs-lookup"><span data-stu-id="19e64-167">![Viewing styles.css in a text editor][ImageStylesFuchsia]</span></span>  


1.  <span data-ttu-id="19e64-168">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="19e64-168">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="19e64-169">Cambie el valor de la `color` propiedad del `<h1>` elemento a su color favorito.</span><span class="sxs-lookup"><span data-stu-id="19e64-169">Change the value of the `color` property of the `<h1>` element to your favorite color.</span></span>  
    <span data-ttu-id="19e64-170">Recuerde que debe hacer clic en el `<h1>` elemento del **árbol DOM** para ver las reglas de CSS que se aplican en el panel **estilos** .</span><span class="sxs-lookup"><span data-stu-id="19e64-170">Remember that you need to click the `<h1>` element in the **DOM Tree** in order to see the CSS rules applied to it in the **Styles** pane.</span></span>  <span data-ttu-id="19e64-171">El punto verde junto a `styles.css:1` significa que todos los cambios que realice se asignan a `~/Desktop/app/styles.css` .</span><span class="sxs-lookup"><span data-stu-id="19e64-171">The green dot next to `styles.css:1` means that any change that you make are mapped to `~/Desktop/app/styles.css`.</span></span>  
    
    > ##### <span data-ttu-id="19e64-172">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="19e64-172">Figure 7</span></span>  
    > <span data-ttu-id="19e64-173">El indicador verde indica que el archivo está vinculado</span><span class="sxs-lookup"><span data-stu-id="19e64-173">The green indicator that the file is linked</span></span>  
    > <span data-ttu-id="19e64-174">! [El indicador verde indica que el archivo está vinculado] [ImageStylesGreen]</span><span class="sxs-lookup"><span data-stu-id="19e64-174">![The green indicator that the file is linked][ImageStylesGreen]</span></span>  

1.  <span data-ttu-id="19e64-175">`styles.css`Vuelva a abrir en un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="19e64-175">Open `styles.css` in a text editor again.</span></span>  <span data-ttu-id="19e64-176">La `color` propiedad ya está configurada con su color favorito.</span><span class="sxs-lookup"><span data-stu-id="19e64-176">The `color` property is now set to your favorite color.</span></span>  
1.  <span data-ttu-id="19e64-177">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="19e64-177">Reload the page.</span></span>  <span data-ttu-id="19e64-178">El color del `<h1>` elemento se mantiene establecido en el color que prefiera.</span><span class="sxs-lookup"><span data-stu-id="19e64-178">The color of the `<h1>` element is still set to your favorite color.</span></span>  <span data-ttu-id="19e64-179">Esto funciona porque, al realizar el cambio, DevTools guardado el cambio en el disco.</span><span class="sxs-lookup"><span data-stu-id="19e64-179">This works because when you made the change, DevTools saved the change to disk.</span></span>  <span data-ttu-id="19e64-180">Y después, cuando vuelva a cargar la página, el servidor local sirvió la copia modificada del archivo desde el disco.</span><span class="sxs-lookup"><span data-stu-id="19e64-180">And then, when you reloaded the page, your local server served the modified copy of the file from disk.</span></span>  

## <span data-ttu-id="19e64-181">Paso 3: guardar un cambio HTML en el disco</span><span class="sxs-lookup"><span data-stu-id="19e64-181">Step 3: Save an HTML change to disk</span></span>   

### <span data-ttu-id="19e64-182">Cambiar HTML desde el panel elementos</span><span class="sxs-lookup"><span data-stu-id="19e64-182">Change HTML from the Elements Panel</span></span>  

<span data-ttu-id="19e64-183">Puede realizar cambios en el HTML desde el panel elemento, pero sus cambios en el árbol DOM no se guardan en el disco y solo afectan a la sesión actual del explorador.</span><span class="sxs-lookup"><span data-stu-id="19e64-183">You may make changes to the HTML from the Element Panel, but your changes to the DOM tree are not saved to disk and only effect the current browser session.</span></span>  
<span data-ttu-id="19e64-184">El árbol DOM no es HTML.</span><span class="sxs-lookup"><span data-stu-id="19e64-184">The DOM tree is not HTML.</span></span>  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### <span data-ttu-id="19e64-185">Cambiar HTML desde el panel orígenes</span><span class="sxs-lookup"><span data-stu-id="19e64-185">Change HTML from the Sources panel</span></span>   

<span data-ttu-id="19e64-186">Si desea guardar un cambio en el código HTML de la página, hágalo usando el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="19e64-186">If you want to save a change to the HTML of the page, do it using the **Sources** panel.</span></span>  

1.  <span data-ttu-id="19e64-187">Haga clic en la pestaña **orígenes** .</span><span class="sxs-lookup"><span data-stu-id="19e64-187">Click the **Sources** tab.</span></span>  
1.  <span data-ttu-id="19e64-188">Haga clic en la pestaña **Página** .</span><span class="sxs-lookup"><span data-stu-id="19e64-188">Click the **Page** tab.</span></span>  
1.  <span data-ttu-id="19e64-189">Haga clic en **(índice)**.</span><span class="sxs-lookup"><span data-stu-id="19e64-189">Click **(index)**.</span></span>  <span data-ttu-id="19e64-190">Se abrirá el código HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="19e64-190">The HTML for the page opens.</span></span>  
1.  <span data-ttu-id="19e64-191">Reemplazar `<h1>Workspaces Demo</h1>` por `<h1>I ❤️  Cake</h1>` .</span><span class="sxs-lookup"><span data-stu-id="19e64-191">Replace `<h1>Workspaces Demo</h1>` with `<h1>I ❤️  Cake</h1>`.</span></span>  <span data-ttu-id="19e64-192">Consulte la [figura 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="19e64-192">See [Figure 8](#figure-8).</span></span>  
1.  <span data-ttu-id="19e64-193">Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="19e64-193">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="19e64-194">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="19e64-194">Reload the page.</span></span>  <span data-ttu-id="19e64-195">El `<h1>` elemento aún muestra el nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="19e64-195">The `<h1>` element is still displaying the new text.</span></span>  
    
    > ##### <span data-ttu-id="19e64-196">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="19e64-196">Figure 8</span></span>  
    > <span data-ttu-id="19e64-197">La línea 12 se ha configurado en</span><span class="sxs-lookup"><span data-stu-id="19e64-197">Line 12 has been set to</span></span> `I ❤️  Cake`  
    > <span data-ttu-id="19e64-198">! [Cambiar HTML desde el panel orígenes] [ImageSourcesCakeHTML]</span><span class="sxs-lookup"><span data-stu-id="19e64-198">![Changing HTML from the Sources panel][ImageSourcesCakeHTML]</span></span>  

1.  <span data-ttu-id="19e64-199">Abra `~/Desktop/app/index.html` .</span><span class="sxs-lookup"><span data-stu-id="19e64-199">Open `~/Desktop/app/index.html`.</span></span>  <span data-ttu-id="19e64-200">El `<h1>` elemento contiene el nuevo texto.</span><span class="sxs-lookup"><span data-stu-id="19e64-200">The `<h1>` element contains the new text.</span></span>  

## <span data-ttu-id="19e64-201">Paso 4: guardar un cambio de JavaScript en el disco</span><span class="sxs-lookup"><span data-stu-id="19e64-201">Step 4: Save a JavaScript change to disk</span></span>   

<span data-ttu-id="19e64-202">El panel **orígenes** también es el lugar donde se pueden realizar cambios en JavaScript.</span><span class="sxs-lookup"><span data-stu-id="19e64-202">The **Sources** panel is also the place to make changes to JavaScript.</span></span>  <span data-ttu-id="19e64-203">Sin embargo, a veces necesita acceder a otros paneles, como el panel **elementos** o el panel de **consola** , mientras realiza cambios en su sitio.</span><span class="sxs-lookup"><span data-stu-id="19e64-203">But sometimes you need to access other panels, such as the **Elements** panel or the **Console** panel, while making changes to your site.</span></span>  <span data-ttu-id="19e64-204">Hay una forma de abrir el panel **fuentes** junto con otros paneles.</span><span class="sxs-lookup"><span data-stu-id="19e64-204">There is a way to have the **Sources** panel open alongside other panels.</span></span>  

1.  <span data-ttu-id="19e64-205">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="19e64-205">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="19e64-206">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="19e64-206">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  <span data-ttu-id="19e64-207">Se abrirá el **menú de comandos** .</span><span class="sxs-lookup"><span data-stu-id="19e64-207">The **Command Menu** opens.</span></span>  
1.  <span data-ttu-id="19e64-208">Escriba `QS` y, a continuación, seleccione **Mostrar fuente rápida**.</span><span class="sxs-lookup"><span data-stu-id="19e64-208">Type `QS`, then select **Show Quick Source**.</span></span>  <span data-ttu-id="19e64-209">En la parte inferior de la ventana de DevTools ahora hay una ficha de **fuente rápida** .  La pestaña muestra el contenido de `index.html` , que es el último archivo editado en el panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="19e64-209">At the bottom of your DevTools window there is now a **Quick Source** tab.  The tab is displaying the contents of `index.html`, which is the last file you edited in the **Sources** panel.</span></span>  <span data-ttu-id="19e64-210">La pestaña **origen rápido** le ofrece el editor del panel **fuentes** , de modo que pueda editar archivos mientras tiene otros paneles abiertos.</span><span class="sxs-lookup"><span data-stu-id="19e64-210">The **Quick Source** tab gives you the editor from the **Sources** panel, so that you are able to edit files while having other panels open.</span></span>  
    
    > ##### <span data-ttu-id="19e64-211">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="19e64-211">Figure 9</span></span>  
    > <span data-ttu-id="19e64-212">Abrir la pestaña de **origen rápido** con el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="19e64-212">Opening the **Quick Source** tab using the **Command Menu**</span></span>  
    > <span data-ttu-id="19e64-213">! [Abrir la pestaña de origen rápido mediante el menú de comandos] [ImageCommandMenuQuickSource]</span><span class="sxs-lookup"><span data-stu-id="19e64-213">![Opening the Quick Source tab using Command Menu][ImageCommandMenuQuickSource]</span></span>  

1.  <span data-ttu-id="19e64-214">Pulse `Control` + `P` \ (Windows \) o `Command` + `P` \ (MacOS \) para abrir el cuadro de diálogo **Abrir archivo** .</span><span class="sxs-lookup"><span data-stu-id="19e64-214">Press `Control`+`P` \(Windows\) or `Command`+`P` \(macOS\) to open the **Open File** dialog.</span></span>  <span data-ttu-id="19e64-215">Consulte la [figura 10](#figure-10).</span><span class="sxs-lookup"><span data-stu-id="19e64-215">See [Figure 10](#figure-10).</span></span>  
1.  <span data-ttu-id="19e64-216">Escriba `script` y, a continuación, seleccione **App/script. js**.</span><span class="sxs-lookup"><span data-stu-id="19e64-216">Type `script`, then select **app/script.js**.</span></span>  
    
    > ##### <span data-ttu-id="19e64-217">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="19e64-217">Figure 10</span></span>  
    > <span data-ttu-id="19e64-218">Abrir `script.js` con el cuadro de diálogo **Abrir archivo**</span><span class="sxs-lookup"><span data-stu-id="19e64-218">Opening `script.js` using the **Open File** dialog</span></span>  
    > <span data-ttu-id="19e64-219">! [Abriendo script. js con el cuadro de diálogo Abrir archivo] [ImageOpenFileDialog]</span><span class="sxs-lookup"><span data-stu-id="19e64-219">![Opening script.js using the Open File dialog][ImageOpenFileDialog]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="19e64-220">El `Save Changes To Disk With Workspaces` vínculo de la demostración se ha estilo regularmente.</span><span class="sxs-lookup"><span data-stu-id="19e64-220">The `Save Changes To Disk With Workspaces` link in the demo is styled regularly.</span></span>  
    
1.  <span data-ttu-id="19e64-221">Agregue el código siguiente en la parte inferior de **script. js** con la pestaña de **origen rápido** .</span><span class="sxs-lookup"><span data-stu-id="19e64-221">Add the following code to the bottom of **script.js** using the **Quick Source** tab.</span></span>  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  <span data-ttu-id="19e64-222">Pulse `Control` + `S` \ (Windows \) o `Command` + `S` \ (MacOS \) para guardar el cambio.</span><span class="sxs-lookup"><span data-stu-id="19e64-222">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save the change.</span></span>  
1.  <span data-ttu-id="19e64-223">Vuelva a cargar la página.</span><span class="sxs-lookup"><span data-stu-id="19e64-223">Reload the page.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="19e64-224">El vínculo de la página ahora está en cursiva.</span><span class="sxs-lookup"><span data-stu-id="19e64-224">The link on the page is now italic.</span></span>
    
    > ##### <span data-ttu-id="19e64-225">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="19e64-225">Figure 11</span></span>  
    > <span data-ttu-id="19e64-226">El vínculo de la página ahora está en cursiva</span><span class="sxs-lookup"><span data-stu-id="19e64-226">The link on the page is now italic</span></span>  
    > <span data-ttu-id="19e64-227">! [El vínculo de la página ahora está en cursiva] [ImageScriptItalic]</span><span class="sxs-lookup"><span data-stu-id="19e64-227">![The link on the page is now italic][ImageScriptItalic]</span></span>  

## <span data-ttu-id="19e64-228">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="19e64-228">Next steps</span></span>   

<span data-ttu-id="19e64-229">Use lo que ha aprendido en este tutorial para configurar áreas de trabajo en su propio proyecto.</span><span class="sxs-lookup"><span data-stu-id="19e64-229">Use what you have learned in this tutorial to set up Workspaces in your own project.</span></span>  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Ilustración 1: un proyecto de problema con un nombre generado aleatoriamente"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[ImageDemo]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo.msft.png "Ilustración 2: la demostración"  
[ImageConsolePanel]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Console.msft.png "Ilustración 3: el panel de consola"  
[ImageFilesystem]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-sources-filesystem.msft.png "Ilustración 4: la ficha filesystem"  
[ImageMapping]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-sources-filesystem-Folder.msft.png "Figura 5: la ficha filesystem ahora muestra una asignación entre los archivos locales y los de red"  
[ImageStylesFuchsia]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-sources-filesystem-CSS.msft.png "Ilustración 6: visualización de estilos. CSS en un editor de texto"  
[ImageStylesGreen]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Elements-Styles-CSS.msft.png "Ilustración 7: el indicador verde que está vinculado al archivo"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-sources-Page-H1.msft.png "Ilustración 8: cambiar HTML desde el panel orígenes"  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Search-show-Quick-Source.msft.png "Ilustración 9: abrir la pestaña de origen rápido con el menú de comandos"  
[ImageOpenFileDialog]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Search-script.msft.png "Figura 10: abrir script. js con el cuadro de diálogo Abrir archivo"  
[ImageScriptItalic]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Workspaces-Workspaces-demo-Elements-Styles-Quick-Source-script.msft.png "ilustración 11: el vínculo de la página ahora está en cursiva"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS"  

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
> <span data-ttu-id="19e64-249">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="19e64-249">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="19e64-250">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="19e64-250">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="19e64-252">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="19e64-252">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
