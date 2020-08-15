---
title: Empezar a analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 94753c7024c2f4f4c96d560c815d310b1f9643a1
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931192"
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

# <span data-ttu-id="f4504-103">Empezar a analizar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="f4504-103">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="f4504-104">Para obtener más información sobre cómo hacer que las páginas se carguen más rápido, consulte [optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="f4504-104">To learn how to make your pages load faster, see [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="f4504-105">El rendimiento en tiempo de ejecución es el funcionamiento de la página cuando se está ejecutando, en lugar de cargarlo.</span><span class="sxs-lookup"><span data-stu-id="f4504-105">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="f4504-106">En el siguiente artículo de tutorial aprenderá a usar el panel de rendimiento de Microsoft Edge DevTools para analizar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f4504-106">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="f4504-107">En cuanto al modelo de **raíl** , las habilidades que aprende en este tutorial son útiles para analizar la respuesta, la animación y las fases inactivas de la página.</span><span class="sxs-lookup"><span data-stu-id="f4504-107">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="f4504-108">Comenzar</span><span class="sxs-lookup"><span data-stu-id="f4504-108">Get started</span></span>  

<span data-ttu-id="f4504-109">En el siguiente tutorial, abra DevTools en una página en vivo y use el panel **rendimiento** para encontrar un cuello de botella de rendimiento en la página.</span><span class="sxs-lookup"><span data-stu-id="f4504-109">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="f4504-110">Abre Microsoft Edge en **modo InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="f4504-110">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="f4504-111">El modo InPrivate garantiza que Microsoft Edge se ejecuta en un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="f4504-111">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="f4504-112">Por ejemplo, si tiene una gran cantidad de extensiones instaladas, las extensiones pueden crear ruido en las medidas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f4504-112">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="f4504-113">Cargue la siguiente página en la ventana InPrivate.</span><span class="sxs-lookup"><span data-stu-id="f4504-113">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="f4504-114">La página es la demostración que va a perfilar.</span><span class="sxs-lookup"><span data-stu-id="f4504-114">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="f4504-115">La página muestra una serie de pequeños iconos moviéndose hacia arriba y hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="f4504-115">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="f4504-116">Seleccione `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \) para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="f4504-116">Select `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="f4504-118">La demostración de la izquierda y DevTools a la derecha</span><span class="sxs-lookup"><span data-stu-id="f4504-118">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="f4504-119">Para el resto de las figuras, DevTools se [desacopla en una ventana independiente][DevtoolsCustomizePlacement] para centrarse mejor en el contenido.</span><span class="sxs-lookup"><span data-stu-id="f4504-119">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <span data-ttu-id="f4504-120">Simular una CPU móvil</span><span class="sxs-lookup"><span data-stu-id="f4504-120">Simulate a mobile CPU</span></span>  

<span data-ttu-id="f4504-121">Los dispositivos móviles tienen mucha menos energía de CPU que los equipos de escritorio y portátiles.</span><span class="sxs-lookup"><span data-stu-id="f4504-121">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="f4504-122">Cada vez que perfile una página, use el límite de CPU para simular cómo se ejecuta la página en dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="f4504-122">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="f4504-123">En DevTools, elija la pestaña **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="f4504-123">In DevTools, choose the **Performance** tab.</span></span>  
1.  <span data-ttu-id="f4504-124">Asegúrese de que la casilla **capturas de pantallas** esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="f4504-124">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="f4504-125">Elija **configuración de captura** \ (! [ Configuración de capturas] [ImageCaptureSettingsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f4504-125">Choose **Capture Settings** \(![Capture Settings][ImageCaptureSettingsIcon]\).</span></span>  <span data-ttu-id="f4504-126">DevTools revela la configuración relacionada con el modo en que captura las métricas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f4504-126">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="f4504-127">En **CPU**, seleccione **deceleración 4**.</span><span class="sxs-lookup"><span data-stu-id="f4504-127">For **CPU**, select **4x slowdown**.</span></span>  <span data-ttu-id="f4504-128">DevTools acelera tu CPU para que sea cuatro veces más lenta de lo normal.</span><span class="sxs-lookup"><span data-stu-id="f4504-128">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="Limitación de CPU" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="f4504-130">Limitación de CPU</span><span class="sxs-lookup"><span data-stu-id="f4504-130">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="f4504-131">Al probar otras páginas; Si quiere asegurarse de que cada página funciona correctamente en dispositivos móviles de low-end, establezca el límite de CPU en **6X lentitud**.</span><span class="sxs-lookup"><span data-stu-id="f4504-131">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="f4504-132">La demostración no funciona bien con una ralentización de 6 veces, por lo que solo usa una ralentización 4x para fines instructivos.</span><span class="sxs-lookup"><span data-stu-id="f4504-132">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="f4504-133">Configurar la demostración</span><span class="sxs-lookup"><span data-stu-id="f4504-133">Set up the demo</span></span>  

<span data-ttu-id="f4504-134">Es difícil crear una demostración de rendimiento de tiempo de ejecución que funcione de forma coherente en todos los lectores del sitio Web.</span><span class="sxs-lookup"><span data-stu-id="f4504-134">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="f4504-135">La siguiente sección le permite personalizar la demostración para asegurarse de que su experiencia es relativamente coherente con las capturas de pantallas y las descripciones, independientemente de su configuración particular.</span><span class="sxs-lookup"><span data-stu-id="f4504-135">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="f4504-136">Elija el botón **Agregar 10** hasta que los iconos azules se muevan notablemente más lentos que antes.</span><span class="sxs-lookup"><span data-stu-id="f4504-136">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="f4504-137">En un equipo de gama alta, puedes elegirlo aproximadamente 20 veces.</span><span class="sxs-lookup"><span data-stu-id="f4504-137">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="f4504-138">Elija **optimizar**.</span><span class="sxs-lookup"><span data-stu-id="f4504-138">Choose **Optimize**.</span></span>  <span data-ttu-id="f4504-139">Los iconos azules deberían moverse más rápido y de forma más sencilla.</span><span class="sxs-lookup"><span data-stu-id="f4504-139">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f4504-140">Para mostrar mejor una diferencia entre las versiones optimizada y no optimizada, elija el botón **restar 10** varias veces e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="f4504-140">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="f4504-141">Si agrega demasiados iconos azules, puede maximizar la CPU y, a continuación, no puede observar una diferencia importante en los resultados de las dos versiones.</span><span class="sxs-lookup"><span data-stu-id="f4504-141">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="f4504-142">Elija **desoptimizar**.</span><span class="sxs-lookup"><span data-stu-id="f4504-142">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="f4504-143">Los iconos azules se mueven más lentamente y con más lentitud.</span><span class="sxs-lookup"><span data-stu-id="f4504-143">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <span data-ttu-id="f4504-144">Registrar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="f4504-144">Record runtime performance</span></span>  

<span data-ttu-id="f4504-145">Cuando ejecutó la versión optimizada de la página, los iconos azules se mueven más rápido.</span><span class="sxs-lookup"><span data-stu-id="f4504-145">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="f4504-146">¿Por qué?</span><span class="sxs-lookup"><span data-stu-id="f4504-146">Why is that?</span></span>  <span data-ttu-id="f4504-147">Se supone que ambas versiones mueven los iconos con la misma cantidad de espacio en la misma cantidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f4504-147">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="f4504-148">Realice una grabación en el panel rendimiento para obtener información sobre cómo detectar el cuello de botella de rendimiento en la versión no optimizada.</span><span class="sxs-lookup"><span data-stu-id="f4504-148">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="f4504-149">En DevTools, elija **grabar** \ (! [ Record] [ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="f4504-149">In DevTools, choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  <span data-ttu-id="f4504-150">DevTools captura métricas de rendimiento a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="f4504-150">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="Perfilar la página" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="f4504-152">Perfilar la página</span><span class="sxs-lookup"><span data-stu-id="f4504-152">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f4504-153">Espere unos segundos.</span><span class="sxs-lookup"><span data-stu-id="f4504-153">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="f4504-154">Elija **detener**.</span><span class="sxs-lookup"><span data-stu-id="f4504-154">Choose **Stop**.</span></span>  <span data-ttu-id="f4504-155">DevTools detiene la grabación, procesa los datos y, a continuación, muestra los resultados en el panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f4504-155">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="Los resultados del perfil" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="f4504-157">Los resultados del perfil</span><span class="sxs-lookup"><span data-stu-id="f4504-157">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f4504-158">Wow, eso es una cantidad abrumadora de datos.</span><span class="sxs-lookup"><span data-stu-id="f4504-158">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="f4504-159">no se preocupe, pronto el proceso tiene más sentido.</span><span class="sxs-lookup"><span data-stu-id="f4504-159">do not worry, soon the process makes more sense.</span></span>  

## <span data-ttu-id="f4504-160">Analizar los resultados</span><span class="sxs-lookup"><span data-stu-id="f4504-160">Analyze the results</span></span>  

<span data-ttu-id="f4504-161">Después de grabar el rendimiento de la página, mida la calidad del rendimiento de la página y busque las causas posibles.</span><span class="sxs-lookup"><span data-stu-id="f4504-161">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <span data-ttu-id="f4504-162">Analizar fotogramas por segundo</span><span class="sxs-lookup"><span data-stu-id="f4504-162">Analyze frames per second</span></span>  

<span data-ttu-id="f4504-163">La métrica principal para medir el rendimiento de cualquier animación es fotogramas por segundo \ (FPS \).</span><span class="sxs-lookup"><span data-stu-id="f4504-163">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="f4504-164">Los usuarios están satisfechos cuando las animaciones se ejecutan a 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="f4504-164">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="f4504-165">Fíjese en el gráfico de **fps** .</span><span class="sxs-lookup"><span data-stu-id="f4504-165">Look at the **FPS** chart.</span></span>  <span data-ttu-id="f4504-166">Cada vez que vea una barra roja encima de **fps**, significa que la velocidad de la fotogramas se ha colocado tan poco que es probable que dañe la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="f4504-166">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="f4504-167">En general, cuanto más alto sea la barra verde, mayor será el valor de FPS.</span><span class="sxs-lookup"><span data-stu-id="f4504-167">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="El gráfico de FPS" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="f4504-169">El gráfico de **fps**</span><span class="sxs-lookup"><span data-stu-id="f4504-169">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f4504-170">Debajo del gráfico de **fps** , verá el gráfico de **CPU** .</span><span class="sxs-lookup"><span data-stu-id="f4504-170">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="f4504-171">Los colores del gráfico de la **CPU** se corresponden con los colores de la pestaña **Resumen** , en la parte inferior del panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f4504-171">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="f4504-172">El hecho de que el gráfico de la **CPU** esté lleno de color significa que la CPU se ha agotado durante el tiempo de grabación.</span><span class="sxs-lookup"><span data-stu-id="f4504-172">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="f4504-173">Cada vez que se agote la CPU durante períodos prolongados, es una señal para encontrar formas de realizar menos trabajo.</span><span class="sxs-lookup"><span data-stu-id="f4504-173">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="Pestaña gráfico de CPU y Resumen" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="f4504-175">Pestaña gráfico de **CPU** y **Resumen**</span><span class="sxs-lookup"><span data-stu-id="f4504-175">The **CPU** chart and **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f4504-176">Mantenga el mouse sobre los gráficos de **fps**, **CPU**o **net** .</span><span class="sxs-lookup"><span data-stu-id="f4504-176">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="f4504-177">DevTools muestra una captura de pantalla de la página en ese momento.</span><span class="sxs-lookup"><span data-stu-id="f4504-177">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="f4504-178">Mueva el mouse hacia la izquierda y la derecha para reproducir la grabación.</span><span class="sxs-lookup"><span data-stu-id="f4504-178">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="f4504-179">Se hace referencia a la acción como limpieza y es útil para analizar manualmente el avance de las animaciones.</span><span class="sxs-lookup"><span data-stu-id="f4504-179">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="Ver una captura de pantalla de la página en la marca de 2500ms de la grabación" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="f4504-181">Ver una captura de pantalla de la página en la marca de 2500ms de la grabación</span><span class="sxs-lookup"><span data-stu-id="f4504-181">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f4504-182">En la sección **Marcos** , desplace el puntero sobre uno de los cuadrados verdes.</span><span class="sxs-lookup"><span data-stu-id="f4504-182">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="f4504-183">DevTools muestra los FPS para ese fotograma en particular.</span><span class="sxs-lookup"><span data-stu-id="f4504-183">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="f4504-184">Es probable que cada fotograma sea muy bajo el objetivo de 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="f4504-184">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="Desplazar el puntero sobre un marco" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="f4504-186">Desplazar el puntero sobre un marco</span><span class="sxs-lookup"><span data-stu-id="f4504-186">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f4504-187">Por supuesto, debería ver que la página no funciona bien.</span><span class="sxs-lookup"><span data-stu-id="f4504-187">Of course, you should see that the page is not performing well.</span></span>  <span data-ttu-id="f4504-188">Pero en escenarios reales es posible que no esté tan claro, así que tener todas las herramientas para hacer que las medidas sean útiles.</span><span class="sxs-lookup"><span data-stu-id="f4504-188">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="f4504-189">Bonificación: abrir el medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="f4504-189">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="f4504-190">Otra herramienta útil es el medidor de FPS, que proporciona estimaciones en tiempo real para FPS a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="f4504-190">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="f4504-191">Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="f4504-191">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="f4504-192">Empiece `Rendering` a escribir en el **menú de comandos** y seleccione **Mostrar procesamiento**.</span><span class="sxs-lookup"><span data-stu-id="f4504-192">Start typing `Rendering` in the **Command Menu** and select **Show Rendering**.</span></span>  
1.  <span data-ttu-id="f4504-193">En la pestaña **representación** , habilita el **medidor de fps**.</span><span class="sxs-lookup"><span data-stu-id="f4504-193">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="f4504-194">Aparece una nueva superposición en la parte superior derecha de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="f4504-194">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="El medidor de FPS" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="f4504-196">El **medidor de fps**</span><span class="sxs-lookup"><span data-stu-id="f4504-196">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="f4504-197">Deshabilite el **medidor de fps** y seleccione `Escape` para cerrar la pestaña **representación** .  No usa el **medidor de fps** en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="f4504-197">Disable the **FPS Meter** and select `Escape` to close the **Rendering** tab.  You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <span data-ttu-id="f4504-198">Encontrar el cuello de botella</span><span class="sxs-lookup"><span data-stu-id="f4504-198">Find the bottleneck</span></span>  

<span data-ttu-id="f4504-199">Después de medir y verificar que la animación no se realiza correctamente, el siguiente paso es responder a la pregunta "¿por qué?".</span><span class="sxs-lookup"><span data-stu-id="f4504-199">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="f4504-200">Cuando no se selecciona ningún evento, la pestaña **Resumen** muestra un desglose de actividad.</span><span class="sxs-lookup"><span data-stu-id="f4504-200">When no events are selected, the **Summary** tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="f4504-201">La página dedicó la mayor parte de la representación de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f4504-201">The page spent most of the time rendering.</span></span>  <span data-ttu-id="f4504-202">Puesto que el rendimiento es el arte de hacer menos trabajo, su objetivo es reducir la cantidad de tiempo dedicado al trabajo de representación.</span><span class="sxs-lookup"><span data-stu-id="f4504-202">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="La pestaña Resumen" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="f4504-204">La pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="f4504-204">The **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f4504-205">Expanda la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="f4504-205">Expand the **Main** section.</span></span>  <span data-ttu-id="f4504-206">DevTools muestra un gráfico de llamas de la actividad en el hilo principal, a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="f4504-206">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="f4504-207">El eje x representa la grabación, a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="f4504-207">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="f4504-208">Cada barra representa un evento.</span><span class="sxs-lookup"><span data-stu-id="f4504-208">Each bar represents an event.</span></span>  <span data-ttu-id="f4504-209">Una barra más ancha significa que el evento ha tardado más tiempo.</span><span class="sxs-lookup"><span data-stu-id="f4504-209">A wider bar means that event took longer.</span></span>  <span data-ttu-id="f4504-210">El eje y representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="f4504-210">The y-axis represents the call stack.</span></span>  <span data-ttu-id="f4504-211">Cuando ve eventos apilados unos sobre otros, significa que los eventos superiores provocan los eventos menores.</span><span class="sxs-lookup"><span data-stu-id="f4504-211">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="La sección principal" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="f4504-213">La sección **principal**</span><span class="sxs-lookup"><span data-stu-id="f4504-213">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f4504-214">Hay una gran cantidad de datos en la grabación.</span><span class="sxs-lookup"><span data-stu-id="f4504-214">There is a lot of data in the recording.</span></span>  <span data-ttu-id="f4504-215">Para acercar un solo evento; Elija, mantenga presionado y arrastre el cursor sobre la **información general**, que es la sección que incluye los gráficos de **fps**, **CPU**y **net** .</span><span class="sxs-lookup"><span data-stu-id="f4504-215">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="f4504-216">En la sección **principal** y en la pestaña **Resumen** solo se muestra información de la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="f4504-216">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="Acercar un evento" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="f4504-218">Acercar un evento</span><span class="sxs-lookup"><span data-stu-id="f4504-218">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="f4504-219">Otra forma de hacer zoom, centrarse en la sección **principal** , elegir el fondo o un evento, y seleccionar `W` ,, `A` `S` o `D` .</span><span class="sxs-lookup"><span data-stu-id="f4504-219">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="f4504-220">Céntrese en el triángulo rojo de la parte superior derecha del **fotograma de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="f4504-220">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="f4504-221">Siempre que vea un triángulo rojo, es una advertencia que puede haber un problema relacionado con el evento.</span><span class="sxs-lookup"><span data-stu-id="f4504-221">Whenever you see a red triangle, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f4504-222">El evento de **marco de animación desencadenado** se produce cada vez que se ejecuta una [ `requestAnimationFrame()` devolución de llamada][MDNWebRequestAnimationFrame] .</span><span class="sxs-lookup"><span data-stu-id="f4504-222">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="f4504-223">Elija el evento de **fotograma de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="f4504-223">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="f4504-224">La pestaña **Resumen** ahora muestra información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="f4504-224">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="f4504-225">Observe el vínculo **Mostrar** .</span><span class="sxs-lookup"><span data-stu-id="f4504-225">Note the **Reveal** link.</span></span>  <span data-ttu-id="f4504-226">Después de elegirlo, DevTools para resaltar el evento que inició el evento de **fotograma de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="f4504-226">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="f4504-227">Además, céntrese en el vínculo **app.js:95** .</span><span class="sxs-lookup"><span data-stu-id="f4504-227">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="f4504-228">Después de elegirlo, se muestra la línea correspondiente en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="f4504-228">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="Más información sobre el evento de marco de animación desencadenado" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="f4504-230">Más información sobre el evento de **marco de animación desencadenado**</span><span class="sxs-lookup"><span data-stu-id="f4504-230">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="f4504-231">Después de seleccionar un evento, use las teclas de dirección para seleccionar los eventos que hay junto a él.</span><span class="sxs-lookup"><span data-stu-id="f4504-231">After selecting an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="f4504-232">En el evento **app. Update** , hay un montón de eventos púrpura.</span><span class="sxs-lookup"><span data-stu-id="f4504-232">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="f4504-233">Si cada evento morado era más ancho, parece que cada uno de ellos puede tener un triángulo rojo.</span><span class="sxs-lookup"><span data-stu-id="f4504-233">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="f4504-234">Elija uno de los eventos de **diseño** púrpura.</span><span class="sxs-lookup"><span data-stu-id="f4504-234">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="f4504-235">DevTools proporciona más información sobre el evento en la pestaña **Resumen** .  De hecho, hay una advertencia sobre los reflujos forzados \ (otra palabra para el diseño \).</span><span class="sxs-lookup"><span data-stu-id="f4504-235">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="f4504-236">En la pestaña **Resumen** , elija el vínculo **app.js:71** en **diseño forzado**.</span><span class="sxs-lookup"><span data-stu-id="f4504-236">In the **Summary** tab, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="f4504-237">DevTools le lleva a la línea de código que forzó el diseño.</span><span class="sxs-lookup"><span data-stu-id="f4504-237">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="La línea de código que causó el diseño forzado" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="f4504-239">La línea de código que causó el diseño forzado</span><span class="sxs-lookup"><span data-stu-id="f4504-239">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="f4504-240">El problema con el código es que, en cada marco de animación, cambia el estilo de cada icono y, después, consulta la posición de cada icono de la página.</span><span class="sxs-lookup"><span data-stu-id="f4504-240">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="f4504-241">Dado que los estilos han cambiado, el explorador no sabe si ha cambiado la posición de cada icono, por lo que tiene que volver a distribuir el icono para calcular la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="f4504-241">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="f4504-242">Eso fue mucho para aprender.</span><span class="sxs-lookup"><span data-stu-id="f4504-242">That was a lot to learn.</span></span>  <span data-ttu-id="f4504-243">Ahora tiene una base sólida en el flujo de trabajo básico para analizar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f4504-243">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="f4504-244">Buen trabajo.</span><span class="sxs-lookup"><span data-stu-id="f4504-244">Good job.</span></span>  

### <span data-ttu-id="f4504-245">Bonificación: analizar la versión optimizada</span><span class="sxs-lookup"><span data-stu-id="f4504-245">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="f4504-246">Usando los flujos de trabajo y las herramientas que acaba de aprender, elija **optimizar** en la demostración para habilitar el código optimizado, tomar otra grabación de rendimiento y analizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="f4504-246">Using the workflows and tools that you just learned, choose **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="f4504-247">Desde la velocidad de fotogramas mejorada hasta la reducción en eventos en el gráfico de llamas de la sección **principal** , podrá ver que la versión optimizada de la aplicación hace mucho menos trabajo, lo que da como resultado un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f4504-247">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you are able to see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="f4504-248">Incluso la versión optimizada no es genial, porque manipula la `top` propiedad de todos los iconos.</span><span class="sxs-lookup"><span data-stu-id="f4504-248">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="f4504-249">Un mejor enfoque es ceñirse a las propiedades que solo afectan a la composición.</span><span class="sxs-lookup"><span data-stu-id="f4504-249">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="f4504-250">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="f4504-250">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="f4504-251">Para estar más familiarizado con el panel rendimiento, la práctica es ideal.</span><span class="sxs-lookup"><span data-stu-id="f4504-251">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="f4504-252">Pruebe a generar perfiles de las páginas y analizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="f4504-252">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="f4504-253">Si tiene preguntas sobre los resultados, use el icono para **Enviar comentarios** , seleccione `Alt` + `Shift` + `I` \ (Windows \), seleccione `Option` + `Shift` + `I` \ (MacOS \) o [Tweet el equipo de DevTools][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="f4504-253">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="f4504-254">Incluya capturas de pantallas o vínculos a páginas reproducibles, si es posible.</span><span class="sxs-lookup"><span data-stu-id="f4504-254">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="El icono \* \* comentarios \* \* en Microsoft Edge DevTools" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="f4504-256">El icono **Enviar comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f4504-256">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="f4504-257">Por último, hay muchas maneras de mejorar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f4504-257">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="f4504-258">Este artículo se centró en un cuello de botella de animación para darle un recorrido centrado en el panel rendimiento, pero es sólo uno de los muchos cuellos de botella que puede encontrar.</span><span class="sxs-lookup"><span data-stu-id="f4504-258">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- links -->

[DevtoolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Optimizar la velocidad del sitio web con Microsoft Edge DevTools"  

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
> <span data-ttu-id="f4504-263">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f4504-263">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f4504-264">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f4504-264">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f4504-266">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f4504-266">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
