---
description: Cómo buscar y analizar código JavaScript y CSS sin usar en Microsoft Edge DevTools.
title: Buscar código JavaScript y CSS sin usar con el panel Cobertura en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 092788606347352876483b1a8282fbb75b2bff66
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398766"
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

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a><span data-ttu-id="9a81f-104">Buscar código JavaScript y CSS sin usar con el panel Cobertura en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9a81f-104">Find unused JavaScript and CSS code with the Coverage panel in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="9a81f-105">El panel **Cobertura** de Microsoft Edge DevTools le ayuda a encontrar código JavaScript y CSS sin usar.</span><span class="sxs-lookup"><span data-stu-id="9a81f-105">The **Coverage** panel in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="9a81f-106">La eliminación de código no usado puede acelerar la carga de la página y guardar los datos móviles de los usuarios móviles.</span><span class="sxs-lookup"><span data-stu-id="9a81f-106">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Análisis de la cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   <span data-ttu-id="9a81f-108">Análisis de la cobertura de código</span><span class="sxs-lookup"><span data-stu-id="9a81f-108">Analyzing code coverage</span></span>  
:::image-end:::  

> [!WARNING]
> <span data-ttu-id="9a81f-109">Encontrar código sin usar es relativamente fácil.</span><span class="sxs-lookup"><span data-stu-id="9a81f-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="9a81f-110">Pero refactorizar una base de código para que cada página solo incluye el JavaScript y CSS que necesita puede resultar difícil.</span><span class="sxs-lookup"><span data-stu-id="9a81f-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="9a81f-111">En esta guía no se explica cómo refactorizar una base de código para evitar el código no usado, ya que estos refactores dependen en gran medida de la pila de tecnología.</span><span class="sxs-lookup"><span data-stu-id="9a81f-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <a name="overview"></a><span data-ttu-id="9a81f-112">Introducción</span><span class="sxs-lookup"><span data-stu-id="9a81f-112">Overview</span></span>  

<span data-ttu-id="9a81f-113">El envío de JavaScript o CSS sin usar es un problema común en el desarrollo web.</span><span class="sxs-lookup"><span data-stu-id="9a81f-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="9a81f-114">Por ejemplo, supongamos que desea usar el componente [de botón Bootstrap][BootstrapButtons] en la página.</span><span class="sxs-lookup"><span data-stu-id="9a81f-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="9a81f-115">Para usar el componente de botón, debe agregar un vínculo a la hoja de estilos de Bootstrap en su HTML, de esta forma:</span><span class="sxs-lookup"><span data-stu-id="9a81f-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="9a81f-116">Esta hoja de estilos no solo incluye el código del componente de botón.</span><span class="sxs-lookup"><span data-stu-id="9a81f-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="9a81f-117">Contiene el CSS para **todos los** componentes de Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="9a81f-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="9a81f-118">Pero no está usando ninguno de los demás componentes de Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="9a81f-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="9a81f-119">Por lo tanto, la página está descargando un montón de CSS que no necesita.</span><span class="sxs-lookup"><span data-stu-id="9a81f-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="9a81f-120">Este CSS adicional es un problema por los siguientes motivos.</span><span class="sxs-lookup"><span data-stu-id="9a81f-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="9a81f-121">El código adicional ralentiza la carga de la página.</span><span class="sxs-lookup"><span data-stu-id="9a81f-121">The extra code slows down your page load.</span></span>  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="9a81f-122">Si un usuario accede a la página en un dispositivo móvil, el código adicional usa sus datos móviles.</span><span class="sxs-lookup"><span data-stu-id="9a81f-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a><span data-ttu-id="9a81f-123">Abrir el panel Cobertura</span><span class="sxs-lookup"><span data-stu-id="9a81f-123">Open the Coverage panel</span></span>  

1.  <span data-ttu-id="9a81f-124">[Abra el menú de comandos][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="9a81f-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="9a81f-125">Empiece a `coverage` escribir , seleccione el comando Mostrar **cobertura** y, a continuación, seleccione para ejecutar `Enter` el comando.</span><span class="sxs-lookup"><span data-stu-id="9a81f-125">Start typing `coverage`, select the **Show Coverage** command, and then select `Enter` to run the command.</span></span>  <span data-ttu-id="9a81f-126">El panel **Cobertura** se abre en el **cajón**.</span><span class="sxs-lookup"><span data-stu-id="9a81f-126">The **Coverage** panel opens in the **Drawer**.</span></span>  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="El panel Cobertura" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       <span data-ttu-id="9a81f-128">El panel **Cobertura**</span><span class="sxs-lookup"><span data-stu-id="9a81f-128">The **Coverage** panel</span></span>  
    :::image-end:::  
    
## <a name="record-code-coverage"></a><span data-ttu-id="9a81f-129">Cobertura de código de registro</span><span class="sxs-lookup"><span data-stu-id="9a81f-129">Record code coverage</span></span>  

1.  <span data-ttu-id="9a81f-130">Elija uno de los botones siguientes en **el** panel Cobertura.</span><span class="sxs-lookup"><span data-stu-id="9a81f-130">Choose one of the following buttons in the **Coverage** panel.</span></span>  
    *   <span data-ttu-id="9a81f-131">Elija **Start Instrumenting Coverage and Reload Page** \( Start Instrumenting Coverage and Reload Page \) si desea revisar qué código es necesario ![ para cargar la ][ImageReloadIcon] página.</span><span class="sxs-lookup"><span data-stu-id="9a81f-131">Choose **Start Instrumenting Coverage And Reload Page** \(![Start Instrumenting Coverage And Reload Page][ImageReloadIcon]\) if you want to review what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="9a81f-132">Elija **Cobertura de instrumento** \( Cobertura de instrumento \) si desea revisar qué código se usa después de interactuar con la ![ ][ImageRecordIcon] página.</span><span class="sxs-lookup"><span data-stu-id="9a81f-132">Choose **Instrument Coverage** \(![Instrument Coverage][ImageRecordIcon]\) if you want to review what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="9a81f-133">Elija **Detener la cobertura de instrumentación y Mostrar** resultados \( Detener la cobertura de instrumentación y Mostrar ![ resultados \) cuando desee detener la grabación de la cobertura de ][ImageStopIcon] código.</span><span class="sxs-lookup"><span data-stu-id="9a81f-133">Choose **Stop Instrumenting Coverage And Show Results** \(![Stop Instrumenting Coverage And Show Results][ImageStopIcon]\) when you want to stop recording code coverage.</span></span>  
    
## <a name="analyze-code-coverage"></a><span data-ttu-id="9a81f-134">Analizar la cobertura de código</span><span class="sxs-lookup"><span data-stu-id="9a81f-134">Analyze code coverage</span></span>  

<span data-ttu-id="9a81f-135">La tabla del panel **Cobertura** muestra los recursos analizados y la cantidad de código que se usa en cada recurso.</span><span class="sxs-lookup"><span data-stu-id="9a81f-135">The table in the **Coverage** panel displays the resources that were analyzed, and how much code is used within each resource.</span></span>  <span data-ttu-id="9a81f-136">Elija una fila para abrir ese recurso en el panel **Orígenes** y revise un desglose línea por línea del código usado y el código no usado.</span><span class="sxs-lookup"><span data-stu-id="9a81f-136">Choose a row to open that resource in the **Sources** panel and review a line-by-line breakdown of used code and unused code.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Un informe de cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   <span data-ttu-id="9a81f-138">Un informe de cobertura de código</span><span class="sxs-lookup"><span data-stu-id="9a81f-138">A code coverage report</span></span>  
:::image-end:::  

*   <span data-ttu-id="9a81f-139">La **columna URL** es la dirección URL del recurso analizado.</span><span class="sxs-lookup"><span data-stu-id="9a81f-139">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="9a81f-140">La **columna Tipo** indica si el recurso contiene CSS, JavaScript o ambos.</span><span class="sxs-lookup"><span data-stu-id="9a81f-140">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="9a81f-141">La **columna Bytes totales** es el tamaño total del recurso en bytes.</span><span class="sxs-lookup"><span data-stu-id="9a81f-141">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="9a81f-142">La **columna Bytes sin** usar es el número de bytes que no se usaron.</span><span class="sxs-lookup"><span data-stu-id="9a81f-142">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="9a81f-143">La última columna sin nombre es una visualización de las columnas **Bytes totales** y **Bytes no** usados.</span><span class="sxs-lookup"><span data-stu-id="9a81f-143">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="9a81f-144">La sección roja de la barra es bytes no usados.</span><span class="sxs-lookup"><span data-stu-id="9a81f-144">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="9a81f-145">La sección verde se usa bytes.</span><span class="sxs-lookup"><span data-stu-id="9a81f-145">The green section is used bytes.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9a81f-146">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9a81f-146">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecute comandos con el menú Comando de Microsoft Edge DevTools | Microsoft Docs"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Botones - Bootstrap"  

> [!NOTE]
> <span data-ttu-id="9a81f-149">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9a81f-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9a81f-150">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/coverage/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9a81f-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9a81f-152">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9a81f-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
