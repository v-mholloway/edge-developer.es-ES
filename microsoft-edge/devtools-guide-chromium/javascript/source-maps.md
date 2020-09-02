---
title: Asignar código preprocesado al código fuente
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 35aa864c20def5f5cd11979d6239e8316c1acbca
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986146"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="3040e-103">Asignar código preprocesado a código fuente</span><span class="sxs-lookup"><span data-stu-id="3040e-103">Map preprocessed code to source code</span></span>  

<span data-ttu-id="3040e-104">Mantenga el código de cliente legible y depurable incluso después de combinarlo, minifylo o compilarlo.</span><span class="sxs-lookup"><span data-stu-id="3040e-104">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="3040e-105">Use mapas de origen para asignar el código fuente al código compilado.</span><span class="sxs-lookup"><span data-stu-id="3040e-105">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="3040e-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="3040e-106">Summary</span></span>  

*   <span data-ttu-id="3040e-107">Use mapas de origen para asignar código de minified al código fuente.</span><span class="sxs-lookup"><span data-stu-id="3040e-107">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="3040e-108">Después, podrá leer y depurar el código compilado en el origen original.</span><span class="sxs-lookup"><span data-stu-id="3040e-108">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="3040e-109">Usa previamente procesadores que puedan generar mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="3040e-109">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="3040e-110">Compruebe que el servidor web puede atender mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="3040e-110">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="3040e-111">Introducción a los preprocesadores</span><span class="sxs-lookup"><span data-stu-id="3040e-111">Get started with preprocessors</span></span>  

<span data-ttu-id="3040e-112">En este artículo se explica cómo interactuar con mapas de origen de JavaScript en el panel de orígenes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="3040e-112">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="3040e-113">Usar un preprocesador admitido</span><span class="sxs-lookup"><span data-stu-id="3040e-113">Use a supported preprocessor</span></span>  

<span data-ttu-id="3040e-114">Debe usar un minifier que sea capaz de crear mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="3040e-114">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, see the preprocessor support section.  -->  <span data-ttu-id="3040e-115">Para obtener una vista extendida, consulte la página de [mapas de origen: idiomas, herramientas y otra información][GitHubWikiSourceMapsLanguagesTools] .</span><span class="sxs-lookup"><span data-stu-id="3040e-115">For an extended view, see the [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="3040e-116">Los siguientes tipos de preprocesadores se suelen usar en combinación con mapas de origen:</span><span class="sxs-lookup"><span data-stu-id="3040e-116">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="3040e-117">Transpiladores \ ([Babel][BabelJS], [traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="3040e-117">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="3040e-118">Compiladores \ ([compilador de cierre][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="3040e-118">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="3040e-119">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="3040e-119">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <span data-ttu-id="3040e-120">Mapas de origen en el panel de orígenes de DevTools</span><span class="sxs-lookup"><span data-stu-id="3040e-120">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="3040e-121">Los mapas de origen de los preprocesadores hacen que DevTools cargue los archivos originales además de sus minified.</span><span class="sxs-lookup"><span data-stu-id="3040e-121">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="3040e-122">A continuación, puede usar los originales para establecer puntos de interrupción y recorrer el código.</span><span class="sxs-lookup"><span data-stu-id="3040e-122">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="3040e-123">Mientras tanto, Microsoft Edge ejecuta el código de minified.</span><span class="sxs-lookup"><span data-stu-id="3040e-123">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="3040e-124">Esto le ofrece la ilusión de ejecutar un sitio de desarrollo en producción.</span><span class="sxs-lookup"><span data-stu-id="3040e-124">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="3040e-125">Al ejecutar mapas de origen en DevTools, debes tener en cuenta que el código JavaScript no está compilado y que puedes ver todos los archivos JavaScript individuales a los que hace referencia.</span><span class="sxs-lookup"><span data-stu-id="3040e-125">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="3040e-126">Este es el uso de la asignación de origen, pero, en realidad, ejecuta el código compilado en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="3040e-126">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="3040e-127">Los errores, registros y puntos de interrupción se asignan al código de desarrollo para la depuración formidable.</span><span class="sxs-lookup"><span data-stu-id="3040e-127">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="3040e-128">Por ello, le da la sensación de que está ejecutando un sitio de desarrollo en producción.</span><span class="sxs-lookup"><span data-stu-id="3040e-128">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="3040e-129">Habilitar mapas de origen en la configuración</span><span class="sxs-lookup"><span data-stu-id="3040e-129">Enable Source Maps in settings</span></span>  

<span data-ttu-id="3040e-130">Los mapas de origen están habilitados de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="3040e-130">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="3040e-131">, pero si deseas volver a activarlos o habilitarlos; en primer lugar, abre DevTools, haz clic en el botón **personalizar DevTools** \ ( `...` \) y selecciona **configuración**.</span><span class="sxs-lookup"><span data-stu-id="3040e-131">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** \(`...`\) button, and select **Settings**.</span></span>  <span data-ttu-id="3040e-132">En el panel **preferencias** , en **fuentes**, active la casilla **Habilitar mapas de origen de JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="3040e-132">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="3040e-133">También puede **Activar habilitar mapas de origen CSS**.</span><span class="sxs-lookup"><span data-stu-id="3040e-133">You may also check **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Habilitar mapas de origen" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="3040e-135">Habilitar mapas de origen de JavaScript</span><span class="sxs-lookup"><span data-stu-id="3040e-135">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <span data-ttu-id="3040e-136">Depurar con mapas de origen</span><span class="sxs-lookup"><span data-stu-id="3040e-136">Debugging with Source Maps</span></span>  

<span data-ttu-id="3040e-137">Al depurar el código y los mapas de origen habilitados, los mapas de origen se muestran en dos lugares:</span><span class="sxs-lookup"><span data-stu-id="3040e-137">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="3040e-138">En la consola \ (el vínculo al origen debe ser el archivo original, no el generado \)</span><span class="sxs-lookup"><span data-stu-id="3040e-138">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="3040e-139">Al repasar por el código \ (los vínculos en la pila de llamadas deben abrir el archivo de origen original \)</span><span class="sxs-lookup"><span data-stu-id="3040e-139">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <span data-ttu-id="3040e-140">@sourceURL y displayName</span><span class="sxs-lookup"><span data-stu-id="3040e-140">@sourceURL and displayName</span></span>  

<span data-ttu-id="3040e-141">Aunque no forme parte de la especificación del mapa de origen, el `@sourceURL` le permite hacer un desarrollo mucho más fácil cuando se trabaja con evaluaciones.</span><span class="sxs-lookup"><span data-stu-id="3040e-141">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="3040e-142">Este ayudante es muy similar a la `//# sourceMappingURL` propiedad y se menciona realmente en las especificaciones del mapa de origen V3.</span><span class="sxs-lookup"><span data-stu-id="3040e-142">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="3040e-143">Al incluir el siguiente comentario especial en el código, que se evaluación, podrás nombrar las evaluaciones y los estilos y los scripts en línea, de modo que cada uno aparezca como más nombres lógicos en tu DevTools.</span><span class="sxs-lookup"><span data-stu-id="3040e-143">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="3040e-144">Vaya a la página siguiente.</span><span class="sxs-lookup"><span data-stu-id="3040e-144">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="3040e-145">demo</span><span class="sxs-lookup"><span data-stu-id="3040e-145">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="3040e-146">Complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="3040e-146">Complete the following actions.</span></span>  

1.  <span data-ttu-id="3040e-147">Abra el DevTools y vaya al panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="3040e-147">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="3040e-148">Escribe un nombre de archivo en el campo **nombre de tu código:** entrada.</span><span class="sxs-lookup"><span data-stu-id="3040e-148">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="3040e-149">Haga clic en el botón **compilar** .</span><span class="sxs-lookup"><span data-stu-id="3040e-149">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="3040e-150">Aparece una alerta con la suma evaluada del origen de CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="3040e-150">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="3040e-151">Si expande el subpanel **orígenes** , ahora verá un nuevo archivo con el nombre de archivo personalizado que escribió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3040e-151">If you expand the **Sources** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="3040e-152">Si hace doble clic para ver este archivo, contiene el JavaScript compilado para el origen original.</span><span class="sxs-lookup"><span data-stu-id="3040e-152">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="3040e-153">En la última línea, sin embargo, es un `// @sourceURL` comentario que indica el archivo de origen original.</span><span class="sxs-lookup"><span data-stu-id="3040e-153">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="3040e-154">Esto puede ayudarle a realizar la depuración mientras trabaja con abstracciones de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="3040e-154">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Trabajar con sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="3040e-156">Trabajar con</span><span class="sxs-lookup"><span data-stu-id="3040e-156">Work with</span></span> `sourceURL`  
:::image-end:::  

## <span data-ttu-id="3040e-157">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="3040e-157">Getting in touch with the Microsoft Edge DevTools team</span></span>

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel es un compilador de JavaScript"  

[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  

[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Un ejemplo sencillo de nombre de evaluación de//# sourceURL"  

[DartMain]: https://www.dartlang.org "Lenguaje de programación DART"  

[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/cierre-compilador | GitHub"  

[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  

[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Mapas de origen: idiomas, herramientas y otra información | Wiki de GitHub"  

[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Introducción-Google/traceur-Compiler | Wiki de GitHub"  

[TypeScriptMain]: https://www.typescriptlang.org "TypeScript"  

> [!NOTE]
> <span data-ttu-id="3040e-167">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3040e-167">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3040e-168">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Paul Bakaus][PaulBakaus] \ (Open Web Developer defensor, Google: Tools, performance, Animation y UX \).</span><span class="sxs-lookup"><span data-stu-id="3040e-168">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3040e-170">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3040e-170">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
