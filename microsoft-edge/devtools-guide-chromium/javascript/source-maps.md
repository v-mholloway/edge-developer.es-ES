---
description: Mantenga el código de cliente legible y depurable incluso después de combinarlo, minifylo o compilarlo.
title: Asignar código preprocesado al código fuente
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bd04c7bae6f57d4fe3f9b293d70775aa99db3dd1
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993236"
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

# <span data-ttu-id="4f730-104">Asignar código preprocesado a código fuente</span><span class="sxs-lookup"><span data-stu-id="4f730-104">Map preprocessed code to source code</span></span>  

<span data-ttu-id="4f730-105">Mantenga el código de cliente legible y depurable incluso después de combinarlo, minifylo o compilarlo.</span><span class="sxs-lookup"><span data-stu-id="4f730-105">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="4f730-106">Use mapas de origen para asignar el código fuente al código compilado.</span><span class="sxs-lookup"><span data-stu-id="4f730-106">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="4f730-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="4f730-107">Summary</span></span>  

*   <span data-ttu-id="4f730-108">Use mapas de origen para asignar código de minified al código fuente.</span><span class="sxs-lookup"><span data-stu-id="4f730-108">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="4f730-109">Después, podrá leer y depurar el código compilado en el origen original.</span><span class="sxs-lookup"><span data-stu-id="4f730-109">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="4f730-110">Usa previamente procesadores que puedan generar mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="4f730-110">Only use pre-processors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="4f730-111">Compruebe que el servidor web puede atender mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="4f730-111">Verify that your web server is able to serve Source Maps.</span></span>  
    
<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="4f730-112">Introducción a los preprocesadores</span><span class="sxs-lookup"><span data-stu-id="4f730-112">Get started with preprocessors</span></span>  

<span data-ttu-id="4f730-113">En este artículo se explica cómo interactuar con mapas de origen de JavaScript en el panel de orígenes de DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f730-113">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="4f730-114">Usar un preprocesador admitido</span><span class="sxs-lookup"><span data-stu-id="4f730-114">Use a supported preprocessor</span></span>  

<span data-ttu-id="4f730-115">Debe usar un minifier que sea capaz de crear mapas de origen.</span><span class="sxs-lookup"><span data-stu-id="4f730-115">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, see the preprocessor support section.  -->  <span data-ttu-id="4f730-116">Para obtener una vista extendida, consulte la página de [mapas de origen: idiomas, herramientas y otra información][GitHubWikiSourceMapsLanguagesTools] .</span><span class="sxs-lookup"><span data-stu-id="4f730-116">For an extended view, see the [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="4f730-117">Los siguientes tipos de preprocesadores se suelen usar en combinación con mapas de origen:</span><span class="sxs-lookup"><span data-stu-id="4f730-117">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="4f730-118">Transpiladores \ ([Babel][BabelJS], [traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="4f730-118">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="4f730-119">Compiladores \ ([compilador de cierre][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="4f730-119">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="4f730-120">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="4f730-120">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  
    
## <span data-ttu-id="4f730-121">Mapas de origen en el panel de orígenes de DevTools</span><span class="sxs-lookup"><span data-stu-id="4f730-121">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="4f730-122">Los mapas de origen de los preprocesadores hacen que DevTools cargue los archivos originales además de sus minified.</span><span class="sxs-lookup"><span data-stu-id="4f730-122">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="4f730-123">A continuación, puede usar los originales para establecer puntos de interrupción y recorrer el código.</span><span class="sxs-lookup"><span data-stu-id="4f730-123">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="4f730-124">Mientras tanto, Microsoft Edge ejecuta el código de minified.</span><span class="sxs-lookup"><span data-stu-id="4f730-124">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="4f730-125">Esto le ofrece la ilusión de ejecutar un sitio de desarrollo en producción.</span><span class="sxs-lookup"><span data-stu-id="4f730-125">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="4f730-126">Al ejecutar mapas de origen en DevTools, debes tener en cuenta que el código JavaScript no está compilado y que puedes ver todos los archivos JavaScript individuales a los que hace referencia.</span><span class="sxs-lookup"><span data-stu-id="4f730-126">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="4f730-127">Este es el uso de la asignación de origen, pero, en realidad, ejecuta el código compilado en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="4f730-127">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="4f730-128">Los errores, registros y puntos de interrupción se asignan al código de desarrollo para la depuración formidable.</span><span class="sxs-lookup"><span data-stu-id="4f730-128">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="4f730-129">Por ello, le da la sensación de que está ejecutando un sitio de desarrollo en producción.</span><span class="sxs-lookup"><span data-stu-id="4f730-129">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="4f730-130">Habilitar mapas de origen en la configuración</span><span class="sxs-lookup"><span data-stu-id="4f730-130">Enable Source Maps in settings</span></span>  

<span data-ttu-id="4f730-131">Los mapas de origen están habilitados de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="4f730-131">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="4f730-132">, pero si deseas volver a activarlos o habilitarlos; en primer lugar, abre DevTools, haz clic en el botón **personalizar DevTools** \ ( `...` \) y selecciona **configuración**.</span><span class="sxs-lookup"><span data-stu-id="4f730-132">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** \(`...`\) button, and select **Settings**.</span></span>  <span data-ttu-id="4f730-133">En el panel **preferencias** , en **fuentes**, active la casilla **Habilitar mapas de origen de JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="4f730-133">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="4f730-134">También puede **Activar habilitar mapas de origen CSS**.</span><span class="sxs-lookup"><span data-stu-id="4f730-134">You may also check **Enable CSS Source Maps**.</span></span>  

:::image type="complex" source="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png" alt-text="Habilitar mapas de origen" lightbox="../media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png":::
   **<span data-ttu-id="4f730-136">Habilitar mapas de origen de JavaScript</span><span class="sxs-lookup"><span data-stu-id="4f730-136">Enable JavaScript Source Maps</span></span>**  
:::image-end:::  

### <span data-ttu-id="4f730-137">Depurar con mapas de origen</span><span class="sxs-lookup"><span data-stu-id="4f730-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="4f730-138">Al depurar el código y los mapas de origen habilitados, los mapas de origen se muestran en dos lugares:</span><span class="sxs-lookup"><span data-stu-id="4f730-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="4f730-139">En la consola \ (el vínculo al origen debe ser el archivo original, no el generado \)</span><span class="sxs-lookup"><span data-stu-id="4f730-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="4f730-140">Al repasar por el código \ (los vínculos en la pila de llamadas deben abrir el archivo de origen original \)</span><span class="sxs-lookup"><span data-stu-id="4f730-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  
    
<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: ../debug/breakpoints/step-code.md ""  -->  

## <span data-ttu-id="4f730-141">@sourceURL y displayName</span><span class="sxs-lookup"><span data-stu-id="4f730-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="4f730-142">Aunque no forme parte de la especificación del mapa de origen, el `@sourceURL` le permite hacer un desarrollo mucho más fácil cuando se trabaja con evaluaciones.</span><span class="sxs-lookup"><span data-stu-id="4f730-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="4f730-143">Este ayudante es muy similar a la `//# sourceMappingURL` propiedad y se menciona realmente en las especificaciones del mapa de origen V3.</span><span class="sxs-lookup"><span data-stu-id="4f730-143">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="4f730-144">Al incluir el siguiente comentario especial en el código, que se evaluación, podrás nombrar las evaluaciones y los estilos y los scripts en línea, de modo que cada uno aparezca como más nombres lógicos en tu DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f730-144">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="4f730-145">Vaya a la página siguiente.</span><span class="sxs-lookup"><span data-stu-id="4f730-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="4f730-146">demo</span><span class="sxs-lookup"><span data-stu-id="4f730-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="4f730-147">Complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="4f730-147">Complete the following actions.</span></span>  

1.  <span data-ttu-id="4f730-148">Abra el DevTools y vaya al panel **fuentes** .</span><span class="sxs-lookup"><span data-stu-id="4f730-148">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="4f730-149">Escribe un nombre de archivo en el campo **nombre de tu código:** entrada.</span><span class="sxs-lookup"><span data-stu-id="4f730-149">Enter in a filename into the **Name your code:** input field.</span></span>  
1.  <span data-ttu-id="4f730-150">Haga clic en el botón **compilar** .</span><span class="sxs-lookup"><span data-stu-id="4f730-150">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="4f730-151">Aparece una alerta con la suma evaluada del origen de CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="4f730-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  
    
<span data-ttu-id="4f730-152">Si expande el subpanel **orígenes** , ahora verá un nuevo archivo con el nombre de archivo personalizado que escribió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4f730-152">If you expand the **Sources** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="4f730-153">Si hace doble clic para ver este archivo, contiene el JavaScript compilado para el origen original.</span><span class="sxs-lookup"><span data-stu-id="4f730-153">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="4f730-154">En la última línea, sin embargo, es un `// @sourceURL` comentario que indica el archivo de origen original.</span><span class="sxs-lookup"><span data-stu-id="4f730-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="4f730-155">Esto puede ayudarle a realizar la depuración mientras trabaja con abstracciones de lenguaje.</span><span class="sxs-lookup"><span data-stu-id="4f730-155">This may help you with debugging while working with language abstractions.</span></span>  

:::image type="complex" source="../media/javascript-sources-page-coffeeeeeeee.msft.png" alt-text="Trabajar con sourceURL" lightbox="../media/javascript-sources-page-coffeeeeeeee.msft.png":::
   <span data-ttu-id="4f730-157">Trabajar con</span><span class="sxs-lookup"><span data-stu-id="4f730-157">Work with</span></span> `sourceURL`  
:::image-end:::  

## <span data-ttu-id="4f730-158">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4f730-158">Getting in touch with the Microsoft Edge DevTools team</span></span>

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
> <span data-ttu-id="4f730-168">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4f730-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4f730-169">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) y está creada por [Meggin Kearney][MegginKearney] \ (Tech Write \) y [Paul Bakaus][PaulBakaus] \ (Open Web Developer defensor, Google: Tools, performance, Animation y UX \).</span><span class="sxs-lookup"><span data-stu-id="4f730-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4f730-171">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4f730-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  
