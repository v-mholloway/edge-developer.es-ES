---
title: Empezar a analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611744"
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







# <span data-ttu-id="4012d-103">Empezar a analizar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="4012d-103">Get Started With Analyzing Runtime Performance</span></span>   



> [!NOTE]
> <span data-ttu-id="4012d-104">Consulte [optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted] para obtener más información sobre cómo hacer que las páginas se carguen más rápido.</span><span class="sxs-lookup"><span data-stu-id="4012d-104">See [Optimize Website Speed][DevtoolsSpeedGetStarted] to learn how to make your pages load faster.</span></span>  

<span data-ttu-id="4012d-105">El rendimiento en tiempo de ejecución es el funcionamiento de la página cuando se está ejecutando, en lugar de cargarlo.</span><span class="sxs-lookup"><span data-stu-id="4012d-105">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="4012d-106">Este tutorial le enseña a usar el panel de rendimiento de Microsoft Edge DevTools para analizar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4012d-106">This tutorial teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="4012d-107">En cuanto al modelo de **raíl** , las habilidades que aprende en este tutorial son útiles para analizar la respuesta, la animación y las fases inactivas de la página.</span><span class="sxs-lookup"><span data-stu-id="4012d-107">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="4012d-108">Comenzar</span><span class="sxs-lookup"><span data-stu-id="4012d-108">Get started</span></span>   

<span data-ttu-id="4012d-109">En este tutorial, abre DevTools en una página en vivo y usa el panel rendimiento para encontrar un cuello de botella de rendimiento en la página.</span><span class="sxs-lookup"><span data-stu-id="4012d-109">In this tutorial, you open DevTools on a live page and use the Performance panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="4012d-110">Abre Microsoft Edge en **modo InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="4012d-110">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="4012d-111">El modo InPrivate garantiza que Microsoft Edge se ejecuta en un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="4012d-111">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="4012d-112">Por ejemplo, si tiene una gran cantidad de extensiones instaladas, esas extensiones podrían crear ruido en las medidas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4012d-112">For example, if you have a lot of extensions installed, those extensions might create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="4012d-113">Cargue la siguiente página en la ventana InPrivate.</span><span class="sxs-lookup"><span data-stu-id="4012d-113">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="4012d-114">Esta es la demostración que te va a perfilar.</span><span class="sxs-lookup"><span data-stu-id="4012d-114">This is the demo that you're going to profile.</span></span>  <span data-ttu-id="4012d-115">La página muestra una serie de pequeños iconos moviéndose hacia arriba y hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="4012d-115">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  <span data-ttu-id="4012d-116">Pulse `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \) para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="4012d-116">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    > ###### <span data-ttu-id="4012d-117">Figura 1</span><span class="sxs-lookup"><span data-stu-id="4012d-117">Figure 1</span></span>  
    > <span data-ttu-id="4012d-118">La demostración de la izquierda y DevTools a la derecha</span><span class="sxs-lookup"><span data-stu-id="4012d-118">The demo on the left, and DevTools on the right</span></span>  
    > ![La demostración de la izquierda y DevTools a la derecha][ImageGetStarted]  
    
    > [!NOTE]
    > <span data-ttu-id="4012d-120">Para el resto de las capturas de pantalla, DevTools se [desacopla en una ventana independiente][DevtoolsCustomizePlacement] para que puedas ver mejor el contenido.</span><span class="sxs-lookup"><span data-stu-id="4012d-120">For the rest of the screenshots, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] so that you can see the contents better.</span></span>  
    
### <span data-ttu-id="4012d-121">Simular una CPU móvil</span><span class="sxs-lookup"><span data-stu-id="4012d-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="4012d-122">Los dispositivos móviles tienen mucha menos energía de CPU que los equipos de escritorio y portátiles.</span><span class="sxs-lookup"><span data-stu-id="4012d-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="4012d-123">Cada vez que perfile una página, use el límite de CPU para simular cómo se ejecuta la página en dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="4012d-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="4012d-124">En DevTools, haga clic en la pestaña **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="4012d-124">In DevTools, click the **Performance** tab.</span></span>  
1.  <span data-ttu-id="4012d-125">Asegúrese de que la casilla **capturas de pantallas** esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="4012d-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="4012d-126">Haga clic en **capturar** configuración de ![ captura ][ImageCaptureSettingsIcon] .</span><span class="sxs-lookup"><span data-stu-id="4012d-126">Click **Capture Settings** ![Capture Settings][ImageCaptureSettingsIcon].</span></span>  <span data-ttu-id="4012d-127">DevTools revela la configuración relacionada con el modo en que captura las métricas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4012d-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="4012d-128">En **CPU**, seleccione **deceleración 4**.</span><span class="sxs-lookup"><span data-stu-id="4012d-128">For **CPU**, select **4x slowdown**.</span></span>  <span data-ttu-id="4012d-129">DevTools acelera tu CPU para que sea cuatro veces más lenta de lo normal.</span><span class="sxs-lookup"><span data-stu-id="4012d-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    > ###### <span data-ttu-id="4012d-130">Figura 2</span><span class="sxs-lookup"><span data-stu-id="4012d-130">Figure 2</span></span>  
    > <span data-ttu-id="4012d-131">Límite de CPU</span><span class="sxs-lookup"><span data-stu-id="4012d-131">CPU throttling</span></span>  
    > ![Límite de CPU][ImageCPUThrottling]  
    
    > [!NOTE]
    > <span data-ttu-id="4012d-133">Cuando pruebe otras páginas, si desea asegurarse de que funcionan bien en dispositivos móviles de low-end, establezca el límite de CPU en **6X lentitud**.</span><span class="sxs-lookup"><span data-stu-id="4012d-133">When testing other pages, if you want to ensure that they work well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="4012d-134">Esta demostración no funciona bien con una ralentización de 6 veces, por lo que solo usa una ralentización 4x para fines instructivos.</span><span class="sxs-lookup"><span data-stu-id="4012d-134">This demo doesn't work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="4012d-135">Configurar la demostración</span><span class="sxs-lookup"><span data-stu-id="4012d-135">Set up the demo</span></span>  

<span data-ttu-id="4012d-136">Es difícil crear una demostración de rendimiento de tiempo de ejecución que funcione de forma coherente en todos los lectores de este sitio Web.</span><span class="sxs-lookup"><span data-stu-id="4012d-136">It is hard to create a runtime performance demo that works consistently for all readers of this website.</span></span>  <span data-ttu-id="4012d-137">Esta sección le permite personalizar la demostración para asegurarse de que su experiencia es relativamente coherente con las capturas de pantallas y descripciones que se observan en este tutorial, independientemente de su configuración particular.</span><span class="sxs-lookup"><span data-stu-id="4012d-137">This section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions you see in this tutorial, regardless of your particular setup.</span></span>

1.  <span data-ttu-id="4012d-138">Siga haciendo clic en **Agregar 10** hasta que los iconos azules se muevan notablemente más lento que antes.</span><span class="sxs-lookup"><span data-stu-id="4012d-138">Keep clicking **Add 10** until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="4012d-139">En un equipo de gama alta, puede demorar unos 20 clics.</span><span class="sxs-lookup"><span data-stu-id="4012d-139">On a high-end machine, it may take about 20 clicks.</span></span>  
1.  <span data-ttu-id="4012d-140">Haga clic en **optimizar**.</span><span class="sxs-lookup"><span data-stu-id="4012d-140">Click **Optimize**.</span></span>  <span data-ttu-id="4012d-141">Los iconos azules deberían moverse más rápido y de forma más sencilla.</span><span class="sxs-lookup"><span data-stu-id="4012d-141">The blue icons should move faster and more smoothly.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="4012d-142">Si no ve una diferencia notable entre las versiones optimizada y no optimizada, pruebe a hacer clic en **restar 10** varias veces e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="4012d-142">If you don't see a noticeable difference between the optimized and un-optimized versions, try clicking **Subtract 10** a few times and trying again.</span></span>  
    > <span data-ttu-id="4012d-143">Si agrega demasiados iconos azules, simplemente va a maximizar la CPU y no va a ver una diferencia importante en los resultados de las dos versiones.</span><span class="sxs-lookup"><span data-stu-id="4012d-143">If you add too many blue icons, you're just going to max out the CPU and you're not going to see a major difference in the results for the two versions.</span></span>  

1.  <span data-ttu-id="4012d-144">Haga clic en **quitar la optimización**.</span><span class="sxs-lookup"><span data-stu-id="4012d-144">Click **Un-Optimize**.</span></span>  <span data-ttu-id="4012d-145">Los iconos azules se mueven más lentamente y con más Jank de nuevo.</span><span class="sxs-lookup"><span data-stu-id="4012d-145">The blue icons move slower and with more jank again.</span></span>  

### <span data-ttu-id="4012d-146">Registrar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="4012d-146">Record runtime performance</span></span>   

<span data-ttu-id="4012d-147">Cuando ejecutó la versión optimizada de la página, los iconos azules se mueven más rápido.</span><span class="sxs-lookup"><span data-stu-id="4012d-147">When you ran the optimized version of the page, the blue icons move faster.</span></span>  
<span data-ttu-id="4012d-148">¿Por qué?</span><span class="sxs-lookup"><span data-stu-id="4012d-148">Why is that?</span></span>  <span data-ttu-id="4012d-149">Se supone que ambas versiones mueven los iconos con la misma cantidad de espacio en la misma cantidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="4012d-149">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="4012d-150">Realice una grabación en el panel rendimiento para obtener información sobre cómo detectar el cuello de botella de rendimiento en la versión no optimizada.</span><span class="sxs-lookup"><span data-stu-id="4012d-150">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="4012d-151">En DevTools **, haga clic en grabar** ![ Registro ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="4012d-151">In DevTools, click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="4012d-152">DevTools captura métricas de rendimiento a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="4012d-152">DevTools captures performance metrics as the page runs.</span></span>  
    
    > ###### <span data-ttu-id="4012d-153">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="4012d-153">Figure 3</span></span> 
    > <span data-ttu-id="4012d-154">Perfilar la página</span><span class="sxs-lookup"><span data-stu-id="4012d-154">Profiling the page</span></span>  
    > ![Perfilar la página][ImagePageProfiling]  
    
1.  <span data-ttu-id="4012d-156">Espere unos segundos.</span><span class="sxs-lookup"><span data-stu-id="4012d-156">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="4012d-157">Haga clic en **detener**.</span><span class="sxs-lookup"><span data-stu-id="4012d-157">Click **Stop**.</span></span>  <span data-ttu-id="4012d-158">DevTools detiene la grabación, procesa los datos y, a continuación, muestra los resultados en el panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4012d-158">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    > ###### <span data-ttu-id="4012d-159">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="4012d-159">Figure 4</span></span>  
    > <span data-ttu-id="4012d-160">Los resultados del perfil</span><span class="sxs-lookup"><span data-stu-id="4012d-160">The results of the profile</span></span>  
    > ![Los resultados del perfil][ImageProfileResults]  

<span data-ttu-id="4012d-162">Wow, eso es una cantidad abrumadora de datos.</span><span class="sxs-lookup"><span data-stu-id="4012d-162">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="4012d-163">No te preocupes, pronto hará más sentido.</span><span class="sxs-lookup"><span data-stu-id="4012d-163">Don't worry, it'll all make more sense shortly.</span></span>  

## <span data-ttu-id="4012d-164">Analizar los resultados</span><span class="sxs-lookup"><span data-stu-id="4012d-164">Analyze the results</span></span>   

<span data-ttu-id="4012d-165">Una vez que haya realizado una grabación del rendimiento de la página, puede medir cuál es el rendimiento de la página y encontrar las causas.</span><span class="sxs-lookup"><span data-stu-id="4012d-165">Once you've got a recording the performance of the page, you can measure how poor the performance of the page is, and find the any causes.</span></span>  

### <span data-ttu-id="4012d-166">Analizar fotogramas por segundo</span><span class="sxs-lookup"><span data-stu-id="4012d-166">Analyze frames per second</span></span>  

<span data-ttu-id="4012d-167">La métrica principal para medir el rendimiento de cualquier animación es fotogramas por segundo \ (FPS \).</span><span class="sxs-lookup"><span data-stu-id="4012d-167">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="4012d-168">Los usuarios están satisfechos cuando las animaciones se ejecutan a 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="4012d-168">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="4012d-169">Fíjese en el gráfico de **fps** .</span><span class="sxs-lookup"><span data-stu-id="4012d-169">Look at the **FPS** chart.</span></span>  <span data-ttu-id="4012d-170">Cada vez que vea una barra roja encima de **fps**, significa que la velocidad de la fotogramas se ha colocado tan poco que es probable que dañe la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="4012d-170">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="4012d-171">En general, cuanto más alto sea la barra verde, mayor será el valor de FPS.</span><span class="sxs-lookup"><span data-stu-id="4012d-171">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    > ###### <span data-ttu-id="4012d-172">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="4012d-172">Figure 5</span></span>  
    > <span data-ttu-id="4012d-173">El gráfico de FPS</span><span class="sxs-lookup"><span data-stu-id="4012d-173">The FPS chart</span></span>  
    > ![El gráfico de FPS][ImageFPSChart]  

1.  <span data-ttu-id="4012d-175">Debajo del gráfico de **fps** , verá el gráfico de **CPU** .</span><span class="sxs-lookup"><span data-stu-id="4012d-175">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="4012d-176">Los colores del gráfico de la **CPU** se corresponden con los colores de la pestaña **Resumen** , en la parte inferior del panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4012d-176">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="4012d-177">El hecho de que el gráfico de la **CPU** esté lleno de color significa que la CPU se ha agotado durante el tiempo de grabación.</span><span class="sxs-lookup"><span data-stu-id="4012d-177">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="4012d-178">Cada vez que se agote la CPU durante períodos prolongados, es una señal para encontrar formas de realizar menos trabajo.</span><span class="sxs-lookup"><span data-stu-id="4012d-178">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    > ###### <span data-ttu-id="4012d-179">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="4012d-179">Figure 6</span></span>  
    > <span data-ttu-id="4012d-180">Pestaña gráfico de CPU y Resumen</span><span class="sxs-lookup"><span data-stu-id="4012d-180">The CPU chart and Summary tab</span></span>  
    > ![Pestaña gráfico de CPU y Resumen][ImageCPUSummary]  

1.  <span data-ttu-id="4012d-182">Mantenga el mouse sobre los gráficos de **fps**, **CPU**o **net** .</span><span class="sxs-lookup"><span data-stu-id="4012d-182">Hover your mouse over the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="4012d-183">DevTools muestra una captura de pantalla de la página en ese momento.</span><span class="sxs-lookup"><span data-stu-id="4012d-183">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="4012d-184">Mueva el mouse hacia la izquierda y la derecha para reproducir la grabación.</span><span class="sxs-lookup"><span data-stu-id="4012d-184">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="4012d-185">Esto se conoce como limpieza y es útil para analizar manualmente el avance de las animaciones.</span><span class="sxs-lookup"><span data-stu-id="4012d-185">This is called scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    > ###### <span data-ttu-id="4012d-186">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="4012d-186">Figure 7</span></span>  
    > <span data-ttu-id="4012d-187">Ver una captura de pantalla de la página en la 2500ms marca de la grabación</span><span class="sxs-lookup"><span data-stu-id="4012d-187">Viewing a screenshot of the page around the 2500ms mark of the recording</span></span>  
    > ![Ver una captura de pantalla de la página en la 2500ms marca de la grabación][ImageViewingScreenshot]  

1.  <span data-ttu-id="4012d-189">En la sección **Marcos** , sitúe el mouse sobre uno de los cuadrados verdes.</span><span class="sxs-lookup"><span data-stu-id="4012d-189">In the **Frames** section, hover your mouse over one of the green squares.</span></span>  <span data-ttu-id="4012d-190">DevTools muestra los FPS para ese fotograma en particular.</span><span class="sxs-lookup"><span data-stu-id="4012d-190">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="4012d-191">Es probable que cada fotograma sea muy bajo el objetivo de 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="4012d-191">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    > ###### <span data-ttu-id="4012d-192">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="4012d-192">Figure 8</span></span>  
    > <span data-ttu-id="4012d-193">Mantener el puntero sobre un marco</span><span class="sxs-lookup"><span data-stu-id="4012d-193">Hovering over a frame</span></span>  
    > ![Mantener el puntero sobre un marco][ImageFrameHover]  

<span data-ttu-id="4012d-195">Por supuesto, con esta demostración es bastante obvio que la página no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="4012d-195">Of course, with this demo, it is pretty obvious that the page is not performing well.</span></span>  <span data-ttu-id="4012d-196">Pero en escenarios reales es posible que no esté tan claro, así que tener todas estas herramientas para hacer que las medidas sean útiles.</span><span class="sxs-lookup"><span data-stu-id="4012d-196">But in real scenarios, it may not be so clear, so having all of these tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="4012d-197">Bonificación: abrir el medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="4012d-197">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="4012d-198">Otra herramienta útil es el medidor de FPS, que proporciona estimaciones en tiempo real para FPS a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="4012d-198">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="4012d-199">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="4012d-199">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="4012d-200">Empiece `Rendering` a escribir en el menú de comandos y seleccione **Mostrar procesamiento**.</span><span class="sxs-lookup"><span data-stu-id="4012d-200">Start typing `Rendering` in the Command Menu and select **Show Rendering**.</span></span>  
1.  <span data-ttu-id="4012d-201">En la pestaña **representación** , habilita el **medidor de fps**.</span><span class="sxs-lookup"><span data-stu-id="4012d-201">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="4012d-202">Aparece una nueva superposición en la parte superior derecha de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="4012d-202">A new overlay appears in the top-right of your viewport.</span></span>  
    
    > ###### <span data-ttu-id="4012d-203">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="4012d-203">Figure 9</span></span>  
    > <span data-ttu-id="4012d-204">El medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="4012d-204">The FPS meter</span></span>  
    > ![El medidor de FPS][ImageFPSMeter]  

1.  <span data-ttu-id="4012d-206">Deshabilite el **medidor de fps** y pulse `Escape` para cerrar la pestaña **representación** .  No lo usaremos en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="4012d-206">Disable the **FPS Meter** and press `Escape` to close the **Rendering** tab.  You won't be using it in this tutorial.</span></span>  

### <span data-ttu-id="4012d-207">Encontrar el cuello de botella</span><span class="sxs-lookup"><span data-stu-id="4012d-207">Find the bottleneck</span></span>  

<span data-ttu-id="4012d-208">Ahora que ya ha medido y verificado que la animación no se realiza correctamente, la siguiente pregunta que debe responder es: ¿por qué?</span><span class="sxs-lookup"><span data-stu-id="4012d-208">Now that you've measured and verified that the animation is not performing well, the next question to answer is:  why?</span></span>  

1.  <span data-ttu-id="4012d-209">Observe la pestaña Resumen.  Cuando no se selecciona ningún evento, en esta pestaña se muestra un desglose de la actividad.</span><span class="sxs-lookup"><span data-stu-id="4012d-209">Note the summary tab.  When no events are selected, this tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="4012d-210">La página dedicó la mayor parte de su tiempo de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="4012d-210">The page spent most of its time rendering.</span></span>  <span data-ttu-id="4012d-211">Puesto que el rendimiento es el arte de hacer menos trabajo, su objetivo es reducir la cantidad de tiempo dedicado al trabajo de representación.</span><span class="sxs-lookup"><span data-stu-id="4012d-211">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    > ###### <span data-ttu-id="4012d-212">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="4012d-212">Figure 10</span></span>  
    > <span data-ttu-id="4012d-213">La pestaña Resumen</span><span class="sxs-lookup"><span data-stu-id="4012d-213">The Summary tab</span></span>  
    > ![La pestaña Resumen][ImageSummaryTab]  

1.  <span data-ttu-id="4012d-215">Expanda la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="4012d-215">Expand the **Main** section.</span></span>  <span data-ttu-id="4012d-216">DevTools muestra un gráfico de llamas de la actividad en el hilo principal, a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="4012d-216">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="4012d-217">El eje x representa la grabación, a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="4012d-217">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="4012d-218">Cada barra representa un evento.</span><span class="sxs-lookup"><span data-stu-id="4012d-218">Each bar represents an event.</span></span>  <span data-ttu-id="4012d-219">Una barra más ancha significa que el evento ha tardado más tiempo.</span><span class="sxs-lookup"><span data-stu-id="4012d-219">A wider bar means that event took longer.</span></span>  <span data-ttu-id="4012d-220">El eje y representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="4012d-220">The y-axis represents the call stack.</span></span>  <span data-ttu-id="4012d-221">Cuando ve eventos apilados unos sobre otros, significa que los eventos superiores provocan los eventos menores.</span><span class="sxs-lookup"><span data-stu-id="4012d-221">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    > ##### <span data-ttu-id="4012d-222">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="4012d-222">Figure 11</span></span>  
    > <span data-ttu-id="4012d-223">La sección principal</span><span class="sxs-lookup"><span data-stu-id="4012d-223">The Main section</span></span>  
    > ![La sección principal][ImageMainSection]  

1.  <span data-ttu-id="4012d-225">Hay una gran cantidad de datos en la grabación.</span><span class="sxs-lookup"><span data-stu-id="4012d-225">There is a lot of data in the recording.</span></span>  <span data-ttu-id="4012d-226">Para acercar un solo evento, haga clic, mantenga presionado y arrastre el mouse sobre la **información general**, que es la sección que incluye los gráficos de **fps**, **CPU**y **net** .</span><span class="sxs-lookup"><span data-stu-id="4012d-226">Zoom in on a single event by clicking, holding, and dragging your mouse over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="4012d-227">En la sección **principal** y en la pestaña **Resumen** solo se muestra información de la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="4012d-227">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    > ###### <span data-ttu-id="4012d-228">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="4012d-228">Figure 12</span></span>  
    > <span data-ttu-id="4012d-229">Acercar un solo evento</span><span class="sxs-lookup"><span data-stu-id="4012d-229">Zoomed in on a single event</span></span>  
    > ![Acercar un evento][ImageZoomedAnimation]  
    
    > [!NOTE]
    > <span data-ttu-id="4012d-231">Otra forma de acercar la vista es resaltar la sección **principal** haciendo clic en el fondo o seleccionando un evento y, a continuación, presionando las `W` teclas,, `A` `S` y `D` .</span><span class="sxs-lookup"><span data-stu-id="4012d-231">Another way to zoom is to focus the **Main** section by clicking its background or selecting an event, and then press the `W`, `A`, `S`, and `D` keys.</span></span>  
    
    1.  <span data-ttu-id="4012d-232">Ten en cuenta que el triángulo rojo de la parte superior derecha del **fotograma de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="4012d-232">Note the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4012d-233">Siempre que vea un triángulo rojo, es una advertencia que puede haber un problema relacionado con este evento.</span><span class="sxs-lookup"><span data-stu-id="4012d-233">Whenever you see a red triangle, it is a warning that there may be an issue related to this event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="4012d-234">El evento de **marco de animación desencadenado** se produce cada vez que se ejecuta una [ `requestAnimationFrame()` devolución de llamada][MDNWebRequestAnimationFrame] .</span><span class="sxs-lookup"><span data-stu-id="4012d-234">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="4012d-235">Haga clic en el evento de **marco de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="4012d-235">Click the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4012d-236">La pestaña **Resumen** ahora muestra información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="4012d-236">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="4012d-237">Observe el vínculo **Mostrar** .</span><span class="sxs-lookup"><span data-stu-id="4012d-237">Note the **Reveal** link.</span></span>  <span data-ttu-id="4012d-238">Al hacer clic, se resalta el evento que inició el evento de **fotograma de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="4012d-238">Clicking that causes DevTools to highlight the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="4012d-239">Observe también el vínculo **app. js: 95** .</span><span class="sxs-lookup"><span data-stu-id="4012d-239">Also note the **app.js:95** link.</span></span>  <span data-ttu-id="4012d-240">Haga clic en para ir a la línea correspondiente en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="4012d-240">Clicking that jumps you to the relevant line in the source code.</span></span>
    
    > ##### <span data-ttu-id="4012d-241">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="4012d-241">Figure 13</span></span>  
    > <span data-ttu-id="4012d-242">Más información sobre el evento de marco de animación desencadenado</span><span class="sxs-lookup"><span data-stu-id="4012d-242">More information about the Animation Frame Fired event</span></span>  
    > ![Más información sobre el evento de marco de animación desencadenado][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > <span data-ttu-id="4012d-244">Después de seleccionar un evento, use las teclas de dirección para seleccionar los eventos que hay junto a él.</span><span class="sxs-lookup"><span data-stu-id="4012d-244">After selecting an event, use the arrow keys to select the events next to it.</span></span>  

1.  <span data-ttu-id="4012d-245">En el evento **app. Update** , hay un montón de eventos púrpura.</span><span class="sxs-lookup"><span data-stu-id="4012d-245">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="4012d-246">Si fuesen más anchos, parece que cada uno de ellos puede tener un triángulo rojo.</span><span class="sxs-lookup"><span data-stu-id="4012d-246">If they were wider, it looks as though each one might have a red triangle on it.</span></span>  <span data-ttu-id="4012d-247">Haga clic en uno de los eventos de **diseño** morados ahora.</span><span class="sxs-lookup"><span data-stu-id="4012d-247">Click one of the purple **Layout** events now.</span></span>  <span data-ttu-id="4012d-248">DevTools proporciona más información sobre el evento en la pestaña **Resumen** .  De hecho, hay una advertencia sobre los reflujos forzados \ (otra palabra para el diseño \).</span><span class="sxs-lookup"><span data-stu-id="4012d-248">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  

1.  <span data-ttu-id="4012d-249">En la pestaña **Resumen** , haga clic en el vínculo **app. js: 71** del **diseño forzado**.</span><span class="sxs-lookup"><span data-stu-id="4012d-249">In the **Summary** tab, click the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="4012d-250">DevTools le lleva a la línea de código que forzó el diseño.</span><span class="sxs-lookup"><span data-stu-id="4012d-250">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    > ##### <span data-ttu-id="4012d-251">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="4012d-251">Figure 14</span></span>  
    > <span data-ttu-id="4012d-252">La línea de código que causó el diseño forzado</span><span class="sxs-lookup"><span data-stu-id="4012d-252">The line of code that caused the forced layout</span></span>  
    > ![La línea de código que causó el diseño forzado][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > <span data-ttu-id="4012d-254">El problema con este código es que, en cada marco de animación, cambia el estilo de cada icono y, después, consulta la posición de cada icono de la página.</span><span class="sxs-lookup"><span data-stu-id="4012d-254">The problem with this code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="4012d-255">Como los estilos han cambiado, el explorador no sabe si cada posición de icono ha cambiado, por lo que tiene que volver a distribuir el icono para calcular su posición.</span><span class="sxs-lookup"><span data-stu-id="4012d-255">Because the styles changed, the browser doesn't know if each icon position changed, so it has to re-layout the icon in order to compute its position.</span></span>  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

<span data-ttu-id="4012d-256">Phew!</span><span class="sxs-lookup"><span data-stu-id="4012d-256">Phew!</span></span>  <span data-ttu-id="4012d-257">Eso fue mucho para llevarlo, pero ahora tiene una base sólida en el flujo de trabajo básico para analizar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4012d-257">That was a lot to take in, but you now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="4012d-258">Buen trabajo.</span><span class="sxs-lookup"><span data-stu-id="4012d-258">Good job.</span></span>  

### <span data-ttu-id="4012d-259">Bonificación: analizar la versión optimizada</span><span class="sxs-lookup"><span data-stu-id="4012d-259">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="4012d-260">Con los flujos de trabajo y las herramientas que acaba de aprender, haga clic en **optimizar** en la demostración para habilitar el código optimizado, realice otra grabación de rendimiento y, a continuación, analice los resultados.</span><span class="sxs-lookup"><span data-stu-id="4012d-260">Using the workflows and tools that you just learned, click **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="4012d-261">Desde la velocidad de fotogramas mejorada hasta la reducción en eventos en el gráfico de llamas de la sección **principal** , puede ver que la versión optimizada de la aplicación hace mucho menos trabajo, lo que da como resultado un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="4012d-261">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you can see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="4012d-262">Incluso esta versión "optimizada" no es tan buena, ya que sigue manipulando la `top` propiedad de cada icono.</span><span class="sxs-lookup"><span data-stu-id="4012d-262">Even this "optimized" version isn't that great, because it still manipulates the `top` property of each icon.</span></span>  <span data-ttu-id="4012d-263">Un mejor enfoque es ceñirse a las propiedades que solo afectan a la composición.</span><span class="sxs-lookup"><span data-stu-id="4012d-263">A better approach is to stick to properties that only affect compositing.</span></span>  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="4012d-264">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="4012d-264">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="4012d-265">Para estar más familiarizado con el panel rendimiento, la práctica es ideal.</span><span class="sxs-lookup"><span data-stu-id="4012d-265">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="4012d-266">Pruebe a generar perfiles de sus propias páginas y analizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="4012d-266">Try profiling your own pages and analyzing the results.</span></span>  <span data-ttu-id="4012d-267">Si tiene alguna pregunta sobre los resultados, use el icono de **comentarios** , pulse `Alt`  +  `Shift`  +  `I` en Windows ( `Option`  +  `Shift`  +  `I` en MacOS) o en [Tweet][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="4012d-267">If you have any questions about your results, use the **Feedback** icon, press `Alt` + `Shift` + `I` on Windows (`Option` + `Shift` + `I` on macOS), or [tweet at us][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="4012d-268">Incluya capturas de pantallas o vínculos a páginas reproducibles, si es posible.</span><span class="sxs-lookup"><span data-stu-id="4012d-268">Include screenshots or links to reproducible pages, if possible.</span></span>

> ##### <span data-ttu-id="4012d-269">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="4012d-269">Figure 15</span></span>
> <span data-ttu-id="4012d-270">El icono de **comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="4012d-270">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![El icono \* \* comentarios \* \* en Microsoft Edge DevTools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="4012d-272">Por último, hay muchas maneras de mejorar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="4012d-272">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="4012d-273">Este tutorial se centró en un cuello de botella de animación para darle un recorrido centrado en el panel rendimiento, pero es solo uno de los muchos cuellos de botella que puede encontrar.</span><span class="sxs-lookup"><span data-stu-id="4012d-273">This tutorial focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Ilustración 1: la demostración de la izquierda y DevTools a la derecha"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Ilustración 2: límite de CPU"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Ilustración 3: generación de perfiles de la página"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Ilustración 4: los resultados del perfil"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Ilustración 5: gráfico de FPS"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Ilustración 6: el gráfico de la CPU y la pestaña Resumen, resaltados en azul"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Ilustración 7: ver una captura de pantalla de la página en la 2500ms marca de la grabación"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Ilustración 8: mantener el puntero sobre un marco"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Ilustración 9: el medidor de FPS"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Ilustración 10: la pestaña Resumen"  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "Ilustración 11: la sección principal"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Ilustración 12: zoom en un único marco de animación que se desencadena evento"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Ilustración 13: más información sobre el evento de marco de animación desencadenado"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Ilustración 14: la línea de código que causó el diseño forzado"  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Ilustración 15: el icono * * comentarios * * en Microsoft Edge DevTools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimizar la velocidad del sitio web con Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools: envía un tweet | Twitter"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

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
> <span data-ttu-id="4012d-293">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4012d-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4012d-294">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4012d-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4012d-296">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4012d-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
