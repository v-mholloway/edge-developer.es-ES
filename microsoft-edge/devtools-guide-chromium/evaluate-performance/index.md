---
description: Obtenga información sobre cómo evaluar el rendimiento del tiempo de ejecución en Microsoft Edge DevTools.
title: Introducción al análisis del rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 074c112b99abb4689cac2274338f2276bc46b4ae
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398724"
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

# <a name="get-started-with-analyzing-runtime-performance"></a><span data-ttu-id="4f4d0-104">Introducción al análisis del rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="4f4d0-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="4f4d0-105">Para obtener información sobre cómo hacer que las páginas se carguen más rápido, vaya a [Optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="4f4d0-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="4f4d0-106">El rendimiento en tiempo de ejecución es el rendimiento de la página cuando se ejecuta, en lugar de cargarse.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="4f4d0-107">El siguiente artículo tutorial le enseña a usar el panel Rendimiento de Microsoft Edge DevTools para analizar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="4f4d0-108">En cuanto al modelo **RAIL,** las habilidades que aprendas en este tutorial son útiles para analizar las fases respuesta, animación e inactividad de la página.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <a name="get-started"></a><span data-ttu-id="4f4d0-109">Introducción</span><span class="sxs-lookup"><span data-stu-id="4f4d0-109">Get started</span></span>  

<span data-ttu-id="4f4d0-110">En el siguiente tutorial, abra DevTools en una página en directo y use el **panel** Rendimiento para encontrar un cuello de botella de rendimiento en la página.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="4f4d0-111">Abra Microsoft Edge en **modo InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="4f4d0-112">El modo InPrivate garantiza que Microsoft Edge se ejecute en un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="4f4d0-113">Por ejemplo, si tiene muchas extensiones instaladas, las extensiones pueden crear ruido en las medidas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="4f4d0-114">Cargue la página siguiente en la ventana InPrivate.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="4f4d0-115">La página es la demostración a la que se va a crear el perfil.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="4f4d0-116">La página muestra un montón de pequeños iconos que se mueven hacia arriba y hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="4f4d0-117">Seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\) para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="La demostración a la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="4f4d0-119">La demostración a la izquierda y DevTools a la derecha</span><span class="sxs-lookup"><span data-stu-id="4f4d0-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4f4d0-120">Para el resto de las figuras, DevTools se desacopla a una ventana [independiente][DevtoolsCustomizePlacement] para centrarse mejor en el contenido.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <a name="simulate-a-mobile-cpu"></a><span data-ttu-id="4f4d0-121">Simular una CPU móvil</span><span class="sxs-lookup"><span data-stu-id="4f4d0-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="4f4d0-122">Los dispositivos móviles tienen mucha menos potencia de CPU que los equipos de escritorio y portátiles.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="4f4d0-123">Siempre que perfiles una página, usa la limitación de CPU para simular el rendimiento de la página en dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="4f4d0-124">En DevTools, elija la **herramienta** Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-124">In DevTools, choose the **Performance** tool.</span></span>  
1.  <span data-ttu-id="4f4d0-125">Asegúrese de que la casilla **Capturas de pantalla** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="4f4d0-126">Elija **Configuración de captura** \(![ Configuración de captura][ImageCaptureSettingsIcon]\).</span><span class="sxs-lookup"><span data-stu-id="4f4d0-126">Choose **Capture Settings** \(![Capture Settings][ImageCaptureSettingsIcon]\).</span></span>  <span data-ttu-id="4f4d0-127">DevTools muestra la configuración relacionada con la forma en que captura las métricas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="4f4d0-128">Para **CPU,** elija **4x slowdown**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="4f4d0-129">DevTools limita la CPU para que sea 4 veces más lenta de lo habitual.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Limitación de CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="4f4d0-131">Limitación de CPU</span><span class="sxs-lookup"><span data-stu-id="4f4d0-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4f4d0-132">Al probar otras páginas; si desea asegurarse de que cada página funciona bien en dispositivos móviles de gama baja, establezca la limitación de CPU en **6x de ralentización.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="4f4d0-133">La demostración no funciona bien con una ralentización de 6x, por lo que solo usa 4x de ralentización para fines informativos.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <a name="set-up-the-demo"></a><span data-ttu-id="4f4d0-134">Configurar la demostración</span><span class="sxs-lookup"><span data-stu-id="4f4d0-134">Set up the demo</span></span>  

<span data-ttu-id="4f4d0-135">Es difícil crear una demostración de rendimiento en tiempo de ejecución que funcione de forma coherente para todos los lectores del sitio web.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="4f4d0-136">La siguiente sección te permite personalizar la demostración para asegurarte de que tu experiencia sea relativamente coherente con las capturas de pantalla y las descripciones, independientemente de tu configuración en particular.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="4f4d0-137">Elija el **botón Agregar 10** hasta que los iconos azules se muevan de forma notablemente más lenta que antes.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="4f4d0-138">En una máquina de gama alta, puede elegirla unas 20 veces.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="4f4d0-139">Elija **Optimizar**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-139">Choose **Optimize**.</span></span>  <span data-ttu-id="4f4d0-140">Los iconos azules deben moverse más rápido y sin problemas.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4f4d0-141">Para mostrar mejor una diferencia entre las versiones optimizadas y las no optimizadas, elija el botón **Restar 10** unas cuantas veces e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="4f4d0-142">Si agrega demasiados iconos azules, puede que la CPU sea máxima y, a continuación, puede que no observe una diferencia importante en los resultados de las dos versiones.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="4f4d0-143">Elija **Un-Optimize**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="4f4d0-144">Los iconos azules se mueven más lentos y con más lentitud de nuevo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <a name="record-runtime-performance"></a><span data-ttu-id="4f4d0-145">Rendimiento del tiempo de ejecución de registro</span><span class="sxs-lookup"><span data-stu-id="4f4d0-145">Record runtime performance</span></span>  

<span data-ttu-id="4f4d0-146">Cuando se ejecutó la versión optimizada de la página, los iconos azules se mueven más rápido.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="4f4d0-147">¿Por qué?</span><span class="sxs-lookup"><span data-stu-id="4f4d0-147">Why is that?</span></span>  <span data-ttu-id="4f4d0-148">Se supone que ambas versiones mueven los iconos la misma cantidad de espacio en la misma cantidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="4f4d0-149">Haga una grabación en el panel Rendimiento para obtener información sobre cómo detectar el cuello de botella de rendimiento en la versión no optimizada.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="4f4d0-150">En DevTools, elija **Record** \(![ Record][ImageRecordIcon]\).</span><span class="sxs-lookup"><span data-stu-id="4f4d0-150">In DevTools, choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  <span data-ttu-id="4f4d0-151">DevTools captura métricas de rendimiento a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Perfil de la página" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="4f4d0-153">Perfil de la página</span><span class="sxs-lookup"><span data-stu-id="4f4d0-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4d0-154">Espere unos segundos.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="4f4d0-155">Elija **Detener**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-155">Choose **Stop**.</span></span>  <span data-ttu-id="4f4d0-156">DevTools deja de grabar, procesa los datos y, a continuación, muestra los resultados en el panel Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Los resultados del perfil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="4f4d0-158">Los resultados del perfil</span><span class="sxs-lookup"><span data-stu-id="4f4d0-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4f4d0-159">Wow, es una cantidad abrumadora de datos.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="4f4d0-160">no se preocupe, pronto el proceso tiene más sentido.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-160">do not worry, soon the process makes more sense.</span></span>  

## <a name="analyze-the-results"></a><span data-ttu-id="4f4d0-161">Analizar los resultados</span><span class="sxs-lookup"><span data-stu-id="4f4d0-161">Analyze the results</span></span>  

<span data-ttu-id="4f4d0-162">Después de registrar el rendimiento de la página, mida la calidad del rendimiento de la página y busque las causas.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <a name="analyze-frames-per-second"></a><span data-ttu-id="4f4d0-163">Analizar fotogramas por segundo</span><span class="sxs-lookup"><span data-stu-id="4f4d0-163">Analyze frames per second</span></span>  

<span data-ttu-id="4f4d0-164">La métrica principal para medir el rendimiento de cualquier animación es fotogramas por segundo \(FPS\).</span><span class="sxs-lookup"><span data-stu-id="4f4d0-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="4f4d0-165">Los usuarios están contentos cuando las animaciones se ejecutan a 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="4f4d0-166">Revise el **gráfico FPS.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-166">Review the **FPS** chart.</span></span>  <span data-ttu-id="4f4d0-167">Cada vez que se muestra una barra roja encima de **FPS,** significa que la velocidad de fotogramas se ha reducido tan bajo que probablemente está dañando la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-167">Whenever a red bar is displayed above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="4f4d0-168">En general, cuanto mayor sea la barra verde, mayor será el FPS.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="Gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="4f4d0-170">Gráfico **de FPS**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4d0-171">Debajo del **gráfico FPS,** se muestra el gráfico **de CPU.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-171">Below the **FPS** chart, the **CPU** chart is displayed.</span></span>  <span data-ttu-id="4f4d0-172">Los colores del gráfico **de CPU** corresponden a los colores del **panel** Resumen, en la parte inferior del panel Rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-172">The colors in the **CPU** chart correspond to the colors in the **Summary** panel, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="4f4d0-173">El hecho de que el **gráfico de CPU** esté lleno de color significa que la CPU se ha maximizado durante la grabación.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="4f4d0-174">Cada vez que la CPU se ha maximizado durante períodos largos, es un indicador de que debe encontrar formas de hacer menos trabajo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-174">Whenever the CPU maxed out for long periods, it is an indicator that you should find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Gráfico de CPU y panel Resumen" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="4f4d0-176">Gráfico **de CPU** y panel **Resumen**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-176">The **CPU** chart and **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4d0-177">Mantenga el mouse en **los gráficos FPS,** **CPU**o **NET.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="4f4d0-178">DevTools muestra una captura de pantalla de la página en ese momento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="4f4d0-179">Mueva el mouse a la izquierda y a la derecha para reproducir la grabación.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="4f4d0-180">La acción se hace referencia como depuración y resulta útil para analizar manualmente la progresión de las animaciones.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Ver una captura de pantalla de la página alrededor de la marca de 2500 ms de la grabación" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="4f4d0-182">Ver una captura de pantalla de la página alrededor de la marca de 2500 ms de la grabación</span><span class="sxs-lookup"><span data-stu-id="4f4d0-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4d0-183">En la **sección** Marcos, mantenga el mouse en uno de los cuadrados verdes.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="4f4d0-184">DevTools muestra los FPS de ese fotograma en particular.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="4f4d0-185">Cada fotograma probablemente esté muy por debajo del objetivo de 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Mantener el mouse en un marco" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="4f4d0-187">Mantener el mouse en un marco</span><span class="sxs-lookup"><span data-stu-id="4f4d0-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="4f4d0-188">Por supuesto, la pantalla indica que la página web no está funcionando bien.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-188">Of course, the display indicates that the webpage is not performing well.</span></span>  <span data-ttu-id="4f4d0-189">Pero en escenarios reales, puede que no sea tan claro, por lo que tener todas las herramientas para realizar mediciones resulta útil.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <a name="bonus-open-the-fps-meter"></a><span data-ttu-id="4f4d0-190">Bonificación: abrir el contador de FPS</span><span class="sxs-lookup"><span data-stu-id="4f4d0-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="4f4d0-191">Otra herramienta práctica es el medidor fps, que proporciona estimaciones en tiempo real de FPS a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="4f4d0-192">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="4f4d0-193">Empiece a `Rendering` escribir en el menú **comando** y elija **Mostrar representación**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="4f4d0-194">En la **herramienta De representación,** habilite **Fps Meter**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-194">In the **Rendering** tool, enable **FPS Meter**.</span></span>  <span data-ttu-id="4f4d0-195">Aparece una nueva superposición en la parte superior derecha de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="El medidor fps" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="4f4d0-197">El **medidor fps**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="4f4d0-198">Desactiva el **fps meter** y selecciona para cerrar la herramienta `Escape` **de** representación.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-198">Turn off the **FPS Meter** and select `Escape` to close the **Rendering** tool.</span></span>  <span data-ttu-id="4f4d0-199">No estás usando **fps meter** en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-199">You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <a name="find-the-bottleneck"></a><span data-ttu-id="4f4d0-200">Buscar el cuello de botella</span><span class="sxs-lookup"><span data-stu-id="4f4d0-200">Find the bottleneck</span></span>  

<span data-ttu-id="4f4d0-201">Después de medir y comprobar que la animación no funciona bien, el siguiente paso es responder a la pregunta "¿por qué?".</span><span class="sxs-lookup"><span data-stu-id="4f4d0-201">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="4f4d0-202">Cuando no se elige ningún evento, el panel **Resumen** muestra un desglose de la actividad.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-202">When no events are chosen, the **Summary** panel shows you a breakdown of activity.</span></span>  <span data-ttu-id="4f4d0-203">La página pasó la mayor parte del tiempo en representarse.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-203">The page spent most of the time rendering.</span></span>  <span data-ttu-id="4f4d0-204">Dado que el rendimiento es el arte de hacer menos trabajo, el objetivo es reducir la cantidad de tiempo dedicado a realizar el trabajo de representación.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-204">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="El panel Resumen" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="4f4d0-206">El **panel Resumen**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-206">The **Summary** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4d0-207">Expanda la **sección** Principal.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-207">Expand the **Main** section.</span></span>  <span data-ttu-id="4f4d0-208">DevTools muestra un gráfico de actividad de llama en el subproceso principal, con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-208">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="4f4d0-209">El eje X representa la grabación, con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-209">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="4f4d0-210">Cada barra representa un evento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-210">Each bar represents an event.</span></span>  <span data-ttu-id="4f4d0-211">Una barra más ancha significa que el evento tardó más tiempo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-211">A wider bar means that event took longer.</span></span>  <span data-ttu-id="4f4d0-212">El eje Y representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-212">The y-axis represents the call stack.</span></span>  <span data-ttu-id="4f4d0-213">Cuando los eventos se apilan entre sí, significa que los eventos superiores provocaron los eventos inferiores.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-213">When events are stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="Sección Principal" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="4f4d0-215">Sección \*\*\*\* Principal</span><span class="sxs-lookup"><span data-stu-id="4f4d0-215">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4f4d0-216">Hay una gran cantidad de datos en la grabación.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-216">There is a lot of data in the recording.</span></span>  <span data-ttu-id="4f4d0-217">Para acercar un solo evento; elija, mantenga y arrastre el cursor sobre overview **,** que es la sección que incluye los gráficos **FPS,** **CPU**y **NET.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-217">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="4f4d0-218">La **sección** Principal y el panel **Resumen** solo muestran información para la parte elegida de la grabación.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-218">The **Main** section and **Summary** panel only display information for the chosen portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Acercar un evento" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="4f4d0-220">Acercar un evento</span><span class="sxs-lookup"><span data-stu-id="4f4d0-220">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4f4d0-221">Otra forma de acercar, centrar la **sección Principal,** elegir el fondo o un evento y seleccionar `W` , , o `A` `S` `D` .</span><span class="sxs-lookup"><span data-stu-id="4f4d0-221">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="4f4d0-222">Céntrate en el triángulo rojo de la parte superior derecha del evento Fotograma de animación **desencadenado.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-222">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4f4d0-223">Cada vez que se muestra un triángulo rojo, es una advertencia de que puede haber un problema relacionado con el evento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-223">Whenever a red triangle is displayed, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4f4d0-224">El **evento Animation Frame Fired** se produce siempre que se ejecuta una [ `requestAnimationFrame()` devolución][MDNWebRequestAnimationFrame] de llamada.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-224">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="4f4d0-225">Elija el **evento Fotograma de** animación desencadenado.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-225">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4f4d0-226">El **panel Resumen** ahora muestra información sobre ese evento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-226">The **Summary** panel now shows you information about that event.</span></span>  <span data-ttu-id="4f4d0-227">Tenga en cuenta **el vínculo** Revelar.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-227">Note the **Reveal** link.</span></span>  <span data-ttu-id="4f4d0-228">Después de elegirla, DevTools resaltará el evento que inició el **evento Animation Frame Fired.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-228">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4f4d0-229">Además, céntrate en **el vínculoapp.js:95.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-229">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="4f4d0-230">Después de elegirla, se muestra la línea relevante en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-230">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Más información sobre el evento Animation Frame Fired" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="4f4d0-232">Más información sobre el evento **Animation Frame Fired**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-232">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4f4d0-233">Después de elegir un evento, usa las teclas de flecha para seleccionar los eventos junto a él.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-233">After choosing an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="4f4d0-234">En el **evento app.update,** hay un montón de eventos púrpura.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-234">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="4f4d0-235">Si cada evento púrpura era más ancho, parece que cada uno puede tener un triángulo rojo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-235">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="4f4d0-236">Elija uno de los eventos **layout púrpura.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-236">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="4f4d0-237">DevTools proporciona más información sobre el evento en el panel **Resumen.**</span><span class="sxs-lookup"><span data-stu-id="4f4d0-237">DevTools provides more information about the event in the **Summary** panel.</span></span>  <span data-ttu-id="4f4d0-238">De hecho, hay una advertencia sobre los flujos forzados \(otra palabra para layout\).</span><span class="sxs-lookup"><span data-stu-id="4f4d0-238">Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="4f4d0-239">En el **panel** Resumen, elija el \*\* vínculoapp.js:71\*\* en **Diseño forzado**.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-239">In the **Summary** panel, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="4f4d0-240">DevTools te lleva a la línea de código que forzó el diseño.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-240">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="La línea de código que provocó el diseño forzado" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="4f4d0-242">La línea de código que provocó el diseño forzado</span><span class="sxs-lookup"><span data-stu-id="4f4d0-242">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="4f4d0-243">El problema con el código es que, en cada fotograma de animación, cambia el estilo de cada icono y, a continuación, consulta la posición de cada icono en la página.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-243">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="4f4d0-244">Dado que los estilos cambiaron, el explorador no sabe si cada posición de icono cambió, por lo que debe volver a diseño el icono para calcular la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-244">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > To learn more, navigate to [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts].  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="4f4d0-245">Eso era mucho que aprender.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-245">That was a lot to learn.</span></span>  <span data-ttu-id="4f4d0-246">Ahora tiene una base sólida en el flujo de trabajo básico para analizar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-246">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="4f4d0-247">Buen trabajo.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-247">Good job.</span></span>  

### <a name="bonus-analyze-the-optimized-version"></a><span data-ttu-id="4f4d0-248">Bonus: Analizar la versión optimizada</span><span class="sxs-lookup"><span data-stu-id="4f4d0-248">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="4f4d0-249">Con los flujos de trabajo y las herramientas que acaba de aprender, elija **Optimizar** en la demostración para habilitar el código optimizado, realizar otra grabación de rendimiento y, a continuación, analizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-249">Using the workflows and tools that you just learned, choose **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="4f4d0-250">Desde la velocidad de fotogramas mejorada hasta la \*\*\*\* reducción de eventos en el gráfico de llamas en la sección Principal, la versión optimizada de la aplicación hace mucho menos trabajo, lo que resulta en un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-250">From the improved framerate to the reduction in events in the flame chart in the **Main** section, the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="4f4d0-251">Incluso la versión optimizada no es excelente, ya que manipula la `top` propiedad de cada icono.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-251">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="4f4d0-252">Un enfoque mejor es seguir las propiedades que solo afectan a la composición.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-252">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > For more information, navigate to [Use transform and opacity changes for animations][RenderingCompositor].  -->  

<!--todo: add rendering section when available -->

## <a name="next-steps"></a><span data-ttu-id="4f4d0-253">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="4f4d0-253">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
To learn more, navigate to [Measure Performance With The RAIL Model][RAIL].  -->  

<span data-ttu-id="4f4d0-254">Para sentirse más cómodo con la **herramienta Rendimiento,** la práctica hace que sea perfecto.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-254">To get more comfortable with the **Performance** tool, practice makes perfect.</span></span>  <span data-ttu-id="4f4d0-255">Intente generar perfiles de las páginas y analizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-255">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="4f4d0-256">Si tienes alguna pregunta sobre los \*\*\*\* resultados, usa el icono Enviar comentarios, selecciona `Alt` + `Shift` + `I` \(Windows, Linux\), `Option` + `Shift` + `I` selecciona \(macOS\) o [tuitea][TwitterEdgeDevtools]el equipo de DevTools .</span><span class="sxs-lookup"><span data-stu-id="4f4d0-256">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="4f4d0-257">Incluya capturas de pantalla o vínculos a páginas reproducibles, si es posible.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-257">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="El icono **Comentarios** en Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="4f4d0-259">El **icono Enviar comentarios** en Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4f4d0-259">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="4f4d0-260">Por último, hay muchas formas de mejorar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-260">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="4f4d0-261">Este artículo se ha centrado en un cuello de botella de animación determinado para ofrecerte un recorrido centrado a través del panel Rendimiento, pero solo es uno de los muchos cuellos de botella que puedes encontrar.</span><span class="sxs-lookup"><span data-stu-id="4f4d0-261">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4f4d0-262">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4f4d0-262">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de Microsoft Edge DevTools (desacoplar, acoplar a abajo, acoplar a la izquierda)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimizar la velocidad del sitio web con Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools: publicar un mensaje de | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window.requestAnimationFrame\(\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> <span data-ttu-id="4f4d0-267">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4f4d0-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4f4d0-268">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4f4d0-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4f4d0-270">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4f4d0-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
