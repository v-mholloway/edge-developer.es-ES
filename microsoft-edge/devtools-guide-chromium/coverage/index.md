---
title: Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ebb8ae15a6888ce2227ec1dc18f307b03ddf9319
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601722"
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





# <span data-ttu-id="ec09a-103">Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ec09a-103">Find Unused JavaScript And CSS Code With The Coverage Tab In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="ec09a-104">La pestaña cobertura de Microsoft Edge DevTools ayuda a buscar código de JavaScript y CSS no usado.</span><span class="sxs-lookup"><span data-stu-id="ec09a-104">The Coverage tab in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="ec09a-105">Quitar el código no usado puede acelerar la carga de la página y guardar los datos celulares de los usuarios móviles.</span><span class="sxs-lookup"><span data-stu-id="ec09a-105">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

> ##### <span data-ttu-id="ec09a-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="ec09a-106">Figure 1</span></span>  
> <span data-ttu-id="ec09a-107">Analizar la cobertura de código</span><span class="sxs-lookup"><span data-stu-id="ec09a-107">Analyzing code coverage</span></span>  
> ![Analizar la cobertura de código][ImageExample]  

> [!WARNING]
> <span data-ttu-id="ec09a-109">Encontrar un código no usado es relativamente fácil.</span><span class="sxs-lookup"><span data-stu-id="ec09a-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="ec09a-110">Pero refactorizar un código base para que cada página solo envíe el código JavaScript y CSS que necesita puede ser difícil.</span><span class="sxs-lookup"><span data-stu-id="ec09a-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="ec09a-111">En esta guía no se trata cómo refactorizar un código base para evitar el código no usado, ya que estos Refactores dependen enormemente de la pila tecnológica.</span><span class="sxs-lookup"><span data-stu-id="ec09a-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <span data-ttu-id="ec09a-112">Introducción</span><span class="sxs-lookup"><span data-stu-id="ec09a-112">Overview</span></span>   

<span data-ttu-id="ec09a-113">El envío de código JavaScript o CSS sin usar es un problema común en el desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="ec09a-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="ec09a-114">Por ejemplo, supongamos que desea usar el [componente del botón bootstrap][BootstrapButtons] en la página.</span><span class="sxs-lookup"><span data-stu-id="ec09a-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="ec09a-115">Para usar el componente Button, necesita agregar un vínculo a la hoja de estilos bootstrap en el código HTML, como este:</span><span class="sxs-lookup"><span data-stu-id="ec09a-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="ec09a-116">Esta hoja de estilos no incluye simplemente el código del componente de botón.</span><span class="sxs-lookup"><span data-stu-id="ec09a-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="ec09a-117">Contiene la CSS de **todos** los componentes de bootstrap.</span><span class="sxs-lookup"><span data-stu-id="ec09a-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="ec09a-118">Pero no usa ninguno de los otros componentes de bootstrap.</span><span class="sxs-lookup"><span data-stu-id="ec09a-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="ec09a-119">Por lo tanto, la página está descargando un montón de CSS que no necesita.</span><span class="sxs-lookup"><span data-stu-id="ec09a-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="ec09a-120">Esta CSS adicional es un problema por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="ec09a-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="ec09a-121">El código adicional ralentiza la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="ec09a-121">The extra code slows down your page load.</span></span>  <!--See [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="ec09a-122">Si un usuario accede a la página en un dispositivo móvil, el código adicional usa sus datos móviles.</span><span class="sxs-lookup"><span data-stu-id="ec09a-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  

<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <span data-ttu-id="ec09a-123">Abrir la pestaña cobertura</span><span class="sxs-lookup"><span data-stu-id="ec09a-123">Open the Coverage tab</span></span>   

1.  <span data-ttu-id="ec09a-124">[Abrir el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="ec09a-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="ec09a-125">Comience `coverage` a escribir, seleccione el comando **Mostrar cobertura** y, a continuación, presione `Enter` para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="ec09a-125">Start typing `coverage`, select the **Show Coverage** command, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="ec09a-126">La pestaña **cobertura** se abre en el **cajón**.</span><span class="sxs-lookup"><span data-stu-id="ec09a-126">The **Coverage** tab opens in the **Drawer**.</span></span>  

    > ##### <span data-ttu-id="ec09a-127">Figura 2</span><span class="sxs-lookup"><span data-stu-id="ec09a-127">Figure 2</span></span>  
    > <span data-ttu-id="ec09a-128">La ficha **cobertura**</span><span class="sxs-lookup"><span data-stu-id="ec09a-128">The **Coverage** tab</span></span>  
    > ![La ficha cobertura][ImageCoverage]  

## <span data-ttu-id="ec09a-130">Registrar la cobertura de código</span><span class="sxs-lookup"><span data-stu-id="ec09a-130">Record code coverage</span></span>   

1.  <span data-ttu-id="ec09a-131">Haga clic en uno de los siguientes botones de la pestaña **cobertura** :</span><span class="sxs-lookup"><span data-stu-id="ec09a-131">Click one of the following buttons in the **Coverage** tab:</span></span>  
    *   <span data-ttu-id="ec09a-132">Haga clic en **empezar a instrumentar cobertura y volver a cargar página** ![ iniciar la cobertura de instrumentación y recargar página ][ImageReloadIcon] si desea ver qué código se necesita para cargar la página.</span><span class="sxs-lookup"><span data-stu-id="ec09a-132">Click **Start Instrumenting Coverage And Reload Page** ![Start Instrumenting Coverage And Reload Page][ImageReloadIcon] if you want to see what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="ec09a-133">Haga clic en cobertura del instrumento de **cobertura del instrumento** ![ ][ImageRecordIcon] si desea ver qué código se usa después de interactuar con la página.</span><span class="sxs-lookup"><span data-stu-id="ec09a-133">Click **Instrument Coverage** ![Instrument Coverage][ImageRecordIcon] if you want to see what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="ec09a-134">Haga clic en **detener la cobertura de la instrumentación y mostrar resultados** ![ detener la instrumentación de la cobertura y mostrar resultados ][ImageStopIcon] cuando desee detener la grabación de la cobertura de código.</span><span class="sxs-lookup"><span data-stu-id="ec09a-134">Click **Stop Instrumenting Coverage And Show Results** ![Stop Instrumenting Coverage And Show Results][ImageStopIcon] when you want to stop recording code coverage.</span></span>  

## <span data-ttu-id="ec09a-135">Analizar la cobertura de código</span><span class="sxs-lookup"><span data-stu-id="ec09a-135">Analyze code coverage</span></span>   

<span data-ttu-id="ec09a-136">La tabla de la pestaña **cobertura** le muestra los recursos que se han analizado y la cantidad de código que se usa dentro de cada recurso.</span><span class="sxs-lookup"><span data-stu-id="ec09a-136">The table in the **Coverage** tab shows you what resources were analyzed, and how much code is used within each resource.</span></span> <span data-ttu-id="ec09a-137">Haga clic en una fila para abrir ese recurso en el panel **orígenes** y ver un desglose línea por línea de código usado y código no usado.</span><span class="sxs-lookup"><span data-stu-id="ec09a-137">Click a row to open that resource in the **Sources** panel and see a line-by-line breakdown of used code and unused code.</span></span>  

> ##### <span data-ttu-id="ec09a-138">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="ec09a-138">Figure 3</span></span>  
> <span data-ttu-id="ec09a-139">Un informe de cobertura de código</span><span class="sxs-lookup"><span data-stu-id="ec09a-139">A code coverage report</span></span>  
> ![Un informe de cobertura de código][ImageExample]  

*   <span data-ttu-id="ec09a-141">La columna **URL** es la dirección URL del recurso que se analizó.</span><span class="sxs-lookup"><span data-stu-id="ec09a-141">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="ec09a-142">En la columna **tipo** se indica si el recurso contiene CSS, JavaScript o ambos.</span><span class="sxs-lookup"><span data-stu-id="ec09a-142">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="ec09a-143">La columna **total bytes** es el tamaño total del recurso en bytes.</span><span class="sxs-lookup"><span data-stu-id="ec09a-143">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="ec09a-144">La columna **bytes no usados** es el número de bytes que no se han usado.</span><span class="sxs-lookup"><span data-stu-id="ec09a-144">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="ec09a-145">La última columna sin nombre es una visualización de las columnas bytes **totales** y **bytes no usados** .</span><span class="sxs-lookup"><span data-stu-id="ec09a-145">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="ec09a-146">La sección roja de la barra es bytes no usados.</span><span class="sxs-lookup"><span data-stu-id="ec09a-146">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="ec09a-147">La sección verde es bytes usados.</span><span class="sxs-lookup"><span data-stu-id="ec09a-147">The green section is used bytes.</span></span>  

 



<!-- image links -->  

[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  
[ImageStopIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-icon.msft.png  

[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage.msft.png "Ilustración 1: analizar la cobertura de código"  
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/coverage-console-drawer-coverage-empty.msft.png "Ilustración 2: la pestaña cobertura"  
[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage-selected.msft.png "Ilustración 3: un informe de cobertura de código"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Botones: bootstrap"  

> [!NOTE]
> <span data-ttu-id="ec09a-153">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ec09a-153">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ec09a-154">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/coverage/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ec09a-154">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ec09a-156">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ec09a-156">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  