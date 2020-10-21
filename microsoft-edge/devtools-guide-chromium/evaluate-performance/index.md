---
description: Obtenga información sobre cómo evaluar el rendimiento en tiempo de ejecución en Microsoft Edge DevTools.
title: Empezar a analizar el rendimiento en tiempo de ejecución
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7cb1d8f073cdb8a43093514dd7dea86d72102011
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124988"
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

# <span data-ttu-id="b580b-104">Empezar a analizar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b580b-104">Get started with analyzing Runtime performance</span></span>  

> [!NOTE]
> <span data-ttu-id="b580b-105">Para obtener más información sobre cómo agilizar la carga de las páginas, navegue para [optimizar la velocidad del sitio web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="b580b-105">To learn how to make your pages load faster, navigate to [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

<span data-ttu-id="b580b-106">El rendimiento en tiempo de ejecución es el funcionamiento de la página cuando se está ejecutando, en lugar de cargarlo.</span><span class="sxs-lookup"><span data-stu-id="b580b-106">Runtime performance is how your page performs when it is running, as opposed to loading.</span></span>  <span data-ttu-id="b580b-107">En el siguiente artículo de tutorial aprenderá a usar el panel de rendimiento de Microsoft Edge DevTools para analizar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b580b-107">The following tutorial article teaches you how to use the Microsoft Edge DevTools Performance panel to analyze runtime performance.</span></span>  <span data-ttu-id="b580b-108">En cuanto al modelo de **raíl** , las habilidades que aprende en este tutorial son útiles para analizar la respuesta, la animación y las fases inactivas de la página.</span><span class="sxs-lookup"><span data-stu-id="b580b-108">In terms of the **RAIL** model, the skills you learn in this tutorial are useful for analyzing the Response, Animation, and Idle phases of your page.</span></span>  

<!--todo: add rail link when section is ready -->  

## <span data-ttu-id="b580b-109">Comenzar</span><span class="sxs-lookup"><span data-stu-id="b580b-109">Get started</span></span>  

<span data-ttu-id="b580b-110">En el siguiente tutorial, abra DevTools en una página en vivo y use el panel **rendimiento** para encontrar un cuello de botella de rendimiento en la página.</span><span class="sxs-lookup"><span data-stu-id="b580b-110">In the following tutorial, you open DevTools on a live page and use the **Performance** panel to find a performance bottleneck on the page.</span></span>  

1.  <span data-ttu-id="b580b-111">Abre Microsoft Edge en **modo InPrivate**.</span><span class="sxs-lookup"><span data-stu-id="b580b-111">Open Microsoft Edge in **InPrivate Mode**.</span></span>  <span data-ttu-id="b580b-112">El modo InPrivate garantiza que Microsoft Edge se ejecuta en un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="b580b-112">InPrivate Mode ensures that Microsoft Edge runs in a clean state.</span></span>  <span data-ttu-id="b580b-113">Por ejemplo, si tiene una gran cantidad de extensiones instaladas, las extensiones pueden crear ruido en las medidas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b580b-113">For example, if you have a lot of extensions installed, the extensions may create noise in your performance measurements.</span></span>  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  <span data-ttu-id="b580b-114">Cargue la siguiente página en la ventana InPrivate.</span><span class="sxs-lookup"><span data-stu-id="b580b-114">Load the following page in your InPrivate window.</span></span>  <span data-ttu-id="b580b-115">La página es la demostración que va a perfilar.</span><span class="sxs-lookup"><span data-stu-id="b580b-115">The page is the demo that you are going to profile.</span></span>  <span data-ttu-id="b580b-116">La página muestra una serie de pequeños iconos moviéndose hacia arriba y hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="b580b-116">The page shows a bunch of little icons moving up and down.</span></span>  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/sluggish/
    ```  
    
1.  <span data-ttu-id="b580b-117">Seleccione `Control` + `Shift` + `I` \ (Windows, Linux \) o `Command` + `Option` + `I` \ (MacOS \) para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="b580b-117">Select `Control`+`Shift`+`I` \(Windows, Linux\) or `Command`+`Option`+`I` \(macOS\) to open DevTools.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-get-started-side-by-side.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-get-started-side-by-side.msft.png":::
       <span data-ttu-id="b580b-119">La demostración de la izquierda y DevTools a la derecha</span><span class="sxs-lookup"><span data-stu-id="b580b-119">The demo on the left, and DevTools on the right</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b580b-120">Para el resto de las figuras, DevTools se [desacopla en una ventana independiente][DevtoolsCustomizePlacement] para centrarse mejor en el contenido.</span><span class="sxs-lookup"><span data-stu-id="b580b-120">For the rest of the figures, DevTools is [undocked to a separate window][DevtoolsCustomizePlacement] to better focus on the contents.</span></span>  
    
### <span data-ttu-id="b580b-121">Simular una CPU móvil</span><span class="sxs-lookup"><span data-stu-id="b580b-121">Simulate a mobile CPU</span></span>  

<span data-ttu-id="b580b-122">Los dispositivos móviles tienen mucha menos energía de CPU que los equipos de escritorio y portátiles.</span><span class="sxs-lookup"><span data-stu-id="b580b-122">Mobile devices have much less CPU power than desktops and laptops.</span></span>  <span data-ttu-id="b580b-123">Cada vez que perfile una página, use el límite de CPU para simular cómo se ejecuta la página en dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="b580b-123">Whenever you profile a page, use CPU Throttling to simulate how your page performs on mobile devices.</span></span>  

1.  <span data-ttu-id="b580b-124">En DevTools, elija la pestaña **rendimiento** .</span><span class="sxs-lookup"><span data-stu-id="b580b-124">In DevTools, choose the **Performance** tab.</span></span>  
1.  <span data-ttu-id="b580b-125">Asegúrese de que la casilla **capturas de pantallas** esté habilitada.</span><span class="sxs-lookup"><span data-stu-id="b580b-125">Make sure that the **Screenshots** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="b580b-126">Elija **configuración de captura** \ (! [ Configuración de capturas] [ImageCaptureSettingsIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b580b-126">Choose **Capture Settings** \(![Capture Settings][ImageCaptureSettingsIcon]\).</span></span>  <span data-ttu-id="b580b-127">DevTools revela la configuración relacionada con el modo en que captura las métricas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b580b-127">DevTools reveals settings related to how it captures performance metrics.</span></span>  
1.  <span data-ttu-id="b580b-128">Para **CPU**, elija **aceleración 4x**.</span><span class="sxs-lookup"><span data-stu-id="b580b-128">For **CPU**, choose **4x slowdown**.</span></span>  <span data-ttu-id="b580b-129">DevTools acelera tu CPU para que sea cuatro veces más lenta de lo normal.</span><span class="sxs-lookup"><span data-stu-id="b580b-129">DevTools throttles your CPU so that it is 4 times slower than usual.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-settings.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-capture-settings.msft.png":::
       <span data-ttu-id="b580b-131">Limitación de CPU</span><span class="sxs-lookup"><span data-stu-id="b580b-131">CPU throttle</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b580b-132">Al probar otras páginas; Si quiere asegurarse de que cada página funciona correctamente en dispositivos móviles de low-end, establezca el límite de CPU en **6X lentitud**.</span><span class="sxs-lookup"><span data-stu-id="b580b-132">When testing other pages; if you want to ensure that each page works well on low-end mobile devices, set CPU Throttling to **6x slowdown**.</span></span>  <span data-ttu-id="b580b-133">La demostración no funciona bien con una ralentización de 6 veces, por lo que solo usa una ralentización 4x para fines instructivos.</span><span class="sxs-lookup"><span data-stu-id="b580b-133">The demo does not work well with 6x slowdown, so it just uses 4x slowdown for instructional purposes.</span></span>  
    
### <span data-ttu-id="b580b-134">Configurar la demostración</span><span class="sxs-lookup"><span data-stu-id="b580b-134">Set up the demo</span></span>  

<span data-ttu-id="b580b-135">Es difícil crear una demostración de rendimiento de tiempo de ejecución que funcione de forma coherente en todos los lectores del sitio Web.</span><span class="sxs-lookup"><span data-stu-id="b580b-135">It is hard to create a runtime performance demo that works consistently for all readers of the website.</span></span>  <span data-ttu-id="b580b-136">La siguiente sección le permite personalizar la demostración para asegurarse de que su experiencia es relativamente coherente con las capturas de pantallas y las descripciones, independientemente de su configuración particular.</span><span class="sxs-lookup"><span data-stu-id="b580b-136">The following section lets you customize the demo to ensure that your experience is relatively consistent with the screenshots and descriptions, regardless of your particular set up.</span></span>

1.  <span data-ttu-id="b580b-137">Elija el botón **Agregar 10** hasta que los iconos azules se muevan notablemente más lentos que antes.</span><span class="sxs-lookup"><span data-stu-id="b580b-137">Choose the **Add 10** button until the blue icons move noticeably slower than before.</span></span>  <span data-ttu-id="b580b-138">En un equipo de gama alta, puedes elegirlo aproximadamente 20 veces.</span><span class="sxs-lookup"><span data-stu-id="b580b-138">On a high-end machine, you may to choose it about 20 times.</span></span>  
1.  <span data-ttu-id="b580b-139">Elija **optimizar**.</span><span class="sxs-lookup"><span data-stu-id="b580b-139">Choose **Optimize**.</span></span>  <span data-ttu-id="b580b-140">Los iconos azules deberían moverse más rápido y de forma más sencilla.</span><span class="sxs-lookup"><span data-stu-id="b580b-140">The blue icons should move faster and more smoothly.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b580b-141">Para mostrar mejor una diferencia entre las versiones optimizada y no optimizada, elija el botón **restar 10** varias veces e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b580b-141">To better display a difference between the optimized and un-optimized versions, choose the **Subtract 10** button a few times and try again.</span></span>  
    > <span data-ttu-id="b580b-142">Si agrega demasiados iconos azules, puede maximizar la CPU y, a continuación, no puede observar una diferencia importante en los resultados de las dos versiones.</span><span class="sxs-lookup"><span data-stu-id="b580b-142">If you add too many blue icons, you may max out the CPU and then you may not observe a major difference in the results for the two versions.</span></span>  
    
1.  <span data-ttu-id="b580b-143">Elija **desoptimizar**.</span><span class="sxs-lookup"><span data-stu-id="b580b-143">Choose **Un-Optimize**.</span></span>  <span data-ttu-id="b580b-144">Los iconos azules se mueven más lentamente y con más lentitud.</span><span class="sxs-lookup"><span data-stu-id="b580b-144">The blue icons move slower and with more sluggishness again.</span></span>  
    
### <span data-ttu-id="b580b-145">Registrar el rendimiento en tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="b580b-145">Record runtime performance</span></span>  

<span data-ttu-id="b580b-146">Cuando ejecutó la versión optimizada de la página, los iconos azules se mueven más rápido.</span><span class="sxs-lookup"><span data-stu-id="b580b-146">When you ran the optimized version of the page, the blue icons move faster.</span></span>  <span data-ttu-id="b580b-147">¿Por qué?</span><span class="sxs-lookup"><span data-stu-id="b580b-147">Why is that?</span></span>  <span data-ttu-id="b580b-148">Se supone que ambas versiones mueven los iconos con la misma cantidad de espacio en la misma cantidad de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b580b-148">Both versions are supposed to move the icons the same amount of space in the same amount of time.</span></span>  <span data-ttu-id="b580b-149">Realice una grabación en el panel rendimiento para obtener información sobre cómo detectar el cuello de botella de rendimiento en la versión no optimizada.</span><span class="sxs-lookup"><span data-stu-id="b580b-149">Take a recording in the Performance panel to learn how to detect the performance bottleneck in the un-optimized version.</span></span>  

1.  <span data-ttu-id="b580b-150">En DevTools, elija **grabar** \ (! [ Record] [ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b580b-150">In DevTools, choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  <span data-ttu-id="b580b-151">DevTools captura métricas de rendimiento a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="b580b-151">DevTools captures performance metrics as the page runs.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-profiling.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-profiling.msft.png":::
       <span data-ttu-id="b580b-153">Perfilar la página</span><span class="sxs-lookup"><span data-stu-id="b580b-153">Profile the page</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b580b-154">Espere unos segundos.</span><span class="sxs-lookup"><span data-stu-id="b580b-154">Wait a few seconds.</span></span>  
1.  <span data-ttu-id="b580b-155">Elija **detener**.</span><span class="sxs-lookup"><span data-stu-id="b580b-155">Choose **Stop**.</span></span>  <span data-ttu-id="b580b-156">DevTools detiene la grabación, procesa los datos y, a continuación, muestra los resultados en el panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b580b-156">DevTools stops recording, processes the data, then displays the results on the Performance panel.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-capture-results.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-capture-results.msft.png":::
       <span data-ttu-id="b580b-158">Los resultados del perfil</span><span class="sxs-lookup"><span data-stu-id="b580b-158">The results of the profile</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b580b-159">Wow, eso es una cantidad abrumadora de datos.</span><span class="sxs-lookup"><span data-stu-id="b580b-159">Wow, that is an overwhelming amount of data.</span></span>  <span data-ttu-id="b580b-160">no se preocupe, pronto el proceso tiene más sentido.</span><span class="sxs-lookup"><span data-stu-id="b580b-160">do not worry, soon the process makes more sense.</span></span>  

## <span data-ttu-id="b580b-161">Analizar los resultados</span><span class="sxs-lookup"><span data-stu-id="b580b-161">Analyze the results</span></span>  

<span data-ttu-id="b580b-162">Después de grabar el rendimiento de la página, mida la calidad del rendimiento de la página y busque las causas posibles.</span><span class="sxs-lookup"><span data-stu-id="b580b-162">After you record the performance of the page, measure the quality of the performance of the page and find the any causes.</span></span>  

### <span data-ttu-id="b580b-163">Analizar fotogramas por segundo</span><span class="sxs-lookup"><span data-stu-id="b580b-163">Analyze frames per second</span></span>  

<span data-ttu-id="b580b-164">La métrica principal para medir el rendimiento de cualquier animación es fotogramas por segundo \ (FPS \).</span><span class="sxs-lookup"><span data-stu-id="b580b-164">The main metric for measuring the performance of any animation is frames per second \(FPS\).</span></span>  <span data-ttu-id="b580b-165">Los usuarios están satisfechos cuando las animaciones se ejecutan a 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="b580b-165">Users are happy when animations run at 60 FPS.</span></span>  

1.  <span data-ttu-id="b580b-166">Fíjese en el gráfico de **fps** .</span><span class="sxs-lookup"><span data-stu-id="b580b-166">Look at the **FPS** chart.</span></span>  <span data-ttu-id="b580b-167">Cada vez que vea una barra roja encima de **fps**, significa que la velocidad de la fotogramas se ha colocado tan poco que es probable que dañe la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="b580b-167">Whenever you see a red bar above **FPS**, it means that the framerate dropped so low that it is probably harming the user experience.</span></span>  <span data-ttu-id="b580b-168">En general, cuanto más alto sea la barra verde, mayor será el valor de FPS.</span><span class="sxs-lookup"><span data-stu-id="b580b-168">In general, the higher the green bar, the higher the FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-fps-chart.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-fps-chart.msft.png":::
       <span data-ttu-id="b580b-170">El gráfico de **fps**</span><span class="sxs-lookup"><span data-stu-id="b580b-170">The **FPS** chart</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b580b-171">Debajo del gráfico de **fps** , verá el gráfico de **CPU** .</span><span class="sxs-lookup"><span data-stu-id="b580b-171">Below the **FPS** chart you see the **CPU** chart.</span></span>  <span data-ttu-id="b580b-172">Los colores del gráfico de la **CPU** se corresponden con los colores de la pestaña **Resumen** , en la parte inferior del panel rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b580b-172">The colors in the **CPU** chart correspond to the colors in the **Summary** tab, at the bottom of the Performance panel.</span></span>  <span data-ttu-id="b580b-173">El hecho de que el gráfico de la **CPU** esté lleno de color significa que la CPU se ha agotado durante el tiempo de grabación.</span><span class="sxs-lookup"><span data-stu-id="b580b-173">The fact that the **CPU** chart is full of color means that the CPU was maxed out during the recording.</span></span>  <span data-ttu-id="b580b-174">Cada vez que se agote la CPU durante períodos prolongados, es una señal para encontrar formas de realizar menos trabajo.</span><span class="sxs-lookup"><span data-stu-id="b580b-174">Whenever you see the CPU maxed out for long periods, it is a cue to find ways to do less work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-cpu-chart.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-cpu-chart.msft.png":::
       <span data-ttu-id="b580b-176">Pestaña gráfico de **CPU** y **Resumen**</span><span class="sxs-lookup"><span data-stu-id="b580b-176">The **CPU** chart and **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b580b-177">Mantenga el mouse sobre los gráficos de **fps**, **CPU**o **net** .</span><span class="sxs-lookup"><span data-stu-id="b580b-177">Hover on the **FPS**, **CPU**, or **NET** charts.</span></span>  <span data-ttu-id="b580b-178">DevTools muestra una captura de pantalla de la página en ese momento.</span><span class="sxs-lookup"><span data-stu-id="b580b-178">DevTools shows a screenshot of the page at that point in time.</span></span>  <span data-ttu-id="b580b-179">Mueva el mouse hacia la izquierda y la derecha para reproducir la grabación.</span><span class="sxs-lookup"><span data-stu-id="b580b-179">Move your mouse left and right to replay the recording.</span></span>  <span data-ttu-id="b580b-180">Se hace referencia a la acción como limpieza y es útil para analizar manualmente el avance de las animaciones.</span><span class="sxs-lookup"><span data-stu-id="b580b-180">The action is referenced as scrubbing, and it is useful for manually analyzing the progression of animations.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-screenshot-hover.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-screenshot-hover.msft.png":::
       <span data-ttu-id="b580b-182">Ver una captura de pantalla de la página en la marca de 2500ms de la grabación</span><span class="sxs-lookup"><span data-stu-id="b580b-182">View a screenshot of the page around the 2500ms mark of the recording</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b580b-183">En la sección **Marcos** , desplace el puntero sobre uno de los cuadrados verdes.</span><span class="sxs-lookup"><span data-stu-id="b580b-183">In the **Frames** section, hover on one of the green squares.</span></span>  <span data-ttu-id="b580b-184">DevTools muestra los FPS para ese fotograma en particular.</span><span class="sxs-lookup"><span data-stu-id="b580b-184">DevTools shows you the FPS for that particular frame.</span></span>  <span data-ttu-id="b580b-185">Es probable que cada fotograma sea muy bajo el objetivo de 60 FPS.</span><span class="sxs-lookup"><span data-stu-id="b580b-185">Each frame is probably well below the target of 60 FPS.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-frame-hover.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-frame-hover.msft.png":::
       <span data-ttu-id="b580b-187">Desplazar el puntero sobre un marco</span><span class="sxs-lookup"><span data-stu-id="b580b-187">Hover on a frame</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b580b-188">Por supuesto, debería ver que la página no funciona bien.</span><span class="sxs-lookup"><span data-stu-id="b580b-188">Of course, you should see that the page is not performing well.</span></span>  <span data-ttu-id="b580b-189">Pero en escenarios reales es posible que no esté tan claro, así que tener todas las herramientas para hacer que las medidas sean útiles.</span><span class="sxs-lookup"><span data-stu-id="b580b-189">But in real scenarios, it may not be so clear, so having all of the tools to make measurements comes in handy.</span></span>  

#### <span data-ttu-id="b580b-190">Bonificación: abrir el medidor de FPS</span><span class="sxs-lookup"><span data-stu-id="b580b-190">Bonus: Open the FPS meter</span></span>  

<span data-ttu-id="b580b-191">Otra herramienta útil es el medidor de FPS, que proporciona estimaciones en tiempo real para FPS a medida que se ejecuta la página.</span><span class="sxs-lookup"><span data-stu-id="b580b-191">Another handy tool is the FPS meter, which provides real-time estimates for FPS as the page runs.</span></span>  

1.  <span data-ttu-id="b580b-192">Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="b580b-192">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
1.  <span data-ttu-id="b580b-193">Empiece `Rendering` a escribir en el **menú de comandos** y elija **Mostrar procesamiento**.</span><span class="sxs-lookup"><span data-stu-id="b580b-193">Start typing `Rendering` in the **Command Menu** and choose **Show Rendering**.</span></span>  
1.  <span data-ttu-id="b580b-194">En la pestaña **representación** , habilita el **medidor de fps**.</span><span class="sxs-lookup"><span data-stu-id="b580b-194">In the **Rendering** tab, enable **FPS Meter**.</span></span>  <span data-ttu-id="b580b-195">Aparece una nueva superposición en la parte superior derecha de la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="b580b-195">A new overlay appears in the top-right of your viewport.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-fps-meter-overlay.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-fps-meter-overlay.msft.png":::
       <span data-ttu-id="b580b-197">El **medidor de fps**</span><span class="sxs-lookup"><span data-stu-id="b580b-197">The **FPS meter**</span></span>  
        :::image-end:::  
    
1.  <span data-ttu-id="b580b-198">Deshabilite el **medidor de fps** y seleccione `Escape` para cerrar la pestaña **representación** .  No usa el **medidor de fps** en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="b580b-198">Disable the **FPS Meter** and select `Escape` to close the **Rendering** tab.  You are not using **FPS Meter** in this tutorial.</span></span>  
    
### <span data-ttu-id="b580b-199">Encontrar el cuello de botella</span><span class="sxs-lookup"><span data-stu-id="b580b-199">Find the bottleneck</span></span>  

<span data-ttu-id="b580b-200">Después de medir y verificar que la animación no se realiza correctamente, el siguiente paso es responder a la pregunta "¿por qué?".</span><span class="sxs-lookup"><span data-stu-id="b580b-200">After you measured and verified that the animation is not performing well, the next step is to answer the question "why?".</span></span>  

1.  <span data-ttu-id="b580b-201">Cuando no se selecciona ningún evento, la pestaña **Resumen** muestra un desglose de actividad.</span><span class="sxs-lookup"><span data-stu-id="b580b-201">When no events are selected, the **Summary** tab shows you a breakdown of activity.</span></span>  <span data-ttu-id="b580b-202">La página dedicó la mayor parte de la representación de tiempo.</span><span class="sxs-lookup"><span data-stu-id="b580b-202">The page spent most of the time rendering.</span></span>  <span data-ttu-id="b580b-203">Puesto que el rendimiento es el arte de hacer menos trabajo, su objetivo es reducir la cantidad de tiempo dedicado al trabajo de representación.</span><span class="sxs-lookup"><span data-stu-id="b580b-203">Since performance is the art of doing less work, your goal is to reduce the amount of time spent doing rendering work.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-summary-tab.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-summary-tab.msft.png":::
       <span data-ttu-id="b580b-205">La pestaña **Resumen**</span><span class="sxs-lookup"><span data-stu-id="b580b-205">The **Summary** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b580b-206">Expanda la sección **principal** .</span><span class="sxs-lookup"><span data-stu-id="b580b-206">Expand the **Main** section.</span></span>  <span data-ttu-id="b580b-207">DevTools muestra un gráfico de llamas de la actividad en el hilo principal, a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="b580b-207">DevTools shows you a flame chart of activity on the main thread, over time.</span></span>  <span data-ttu-id="b580b-208">El eje x representa la grabación, a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="b580b-208">The x-axis represents the recording, over time.</span></span>  <span data-ttu-id="b580b-209">Cada barra representa un evento.</span><span class="sxs-lookup"><span data-stu-id="b580b-209">Each bar represents an event.</span></span>  <span data-ttu-id="b580b-210">Una barra más ancha significa que el evento ha tardado más tiempo.</span><span class="sxs-lookup"><span data-stu-id="b580b-210">A wider bar means that event took longer.</span></span>  <span data-ttu-id="b580b-211">El eje y representa la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="b580b-211">The y-axis represents the call stack.</span></span>  <span data-ttu-id="b580b-212">Cuando ve eventos apilados unos sobre otros, significa que los eventos superiores provocan los eventos menores.</span><span class="sxs-lookup"><span data-stu-id="b580b-212">When you see events stacked on top of each other, it means the upper events caused the lower events.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-main.msft.png":::
       <span data-ttu-id="b580b-214">La sección **principal**</span><span class="sxs-lookup"><span data-stu-id="b580b-214">The **Main** section</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b580b-215">Hay una gran cantidad de datos en la grabación.</span><span class="sxs-lookup"><span data-stu-id="b580b-215">There is a lot of data in the recording.</span></span>  <span data-ttu-id="b580b-216">Para acercar un solo evento; Elija, mantenga presionado y arrastre el cursor sobre la **información general**, que es la sección que incluye los gráficos de **fps**, **CPU**y **net** .</span><span class="sxs-lookup"><span data-stu-id="b580b-216">To Zoom into a single event; choose, hold, and dragg your cursor over the **Overview**, which is the section that includes the **FPS**, **CPU**, and **NET** charts.</span></span>  <span data-ttu-id="b580b-217">En la sección **principal** y en la pestaña **Resumen** solo se muestra información de la parte seleccionada de la grabación.</span><span class="sxs-lookup"><span data-stu-id="b580b-217">The **Main** section and **Summary** tab only display information for the selected portion of the recording.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-performance-main-zoomed.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-main-zoomed.msft.png":::
       <span data-ttu-id="b580b-219">Acercar un evento</span><span class="sxs-lookup"><span data-stu-id="b580b-219">Zoom into an event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b580b-220">Otra forma de hacer zoom, centrarse en la sección **principal** , elegir el fondo o un evento, y seleccionar `W` ,, `A` `S` o `D` .</span><span class="sxs-lookup"><span data-stu-id="b580b-220">Another way to zoom, focus the **Main** section, choose the background or an event, and select `W`, `A`, `S`, or `D`.</span></span>  
    
    1.  <span data-ttu-id="b580b-221">Céntrese en el triángulo rojo de la parte superior derecha del **fotograma de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="b580b-221">Focus on the red triangle in the top-right of the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="b580b-222">Siempre que vea un triángulo rojo, es una advertencia que puede haber un problema relacionado con el evento.</span><span class="sxs-lookup"><span data-stu-id="b580b-222">Whenever you see a red triangle, it is a warning that there may be an issue related to the event.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b580b-223">El evento de **marco de animación desencadenado** se produce cada vez que se ejecuta una [ `requestAnimationFrame()` devolución de llamada][MDNWebRequestAnimationFrame] .</span><span class="sxs-lookup"><span data-stu-id="b580b-223">The **Animation Frame Fired** event occurs whenever a [`requestAnimationFrame()` callback][MDNWebRequestAnimationFrame] is run.</span></span>  
    
1.  <span data-ttu-id="b580b-224">Elija el evento de **fotograma de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="b580b-224">Choose the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="b580b-225">La pestaña **Resumen** ahora muestra información sobre el evento.</span><span class="sxs-lookup"><span data-stu-id="b580b-225">The **Summary** tab now shows you information about that event.</span></span>  <span data-ttu-id="b580b-226">Observe el vínculo **Mostrar** .</span><span class="sxs-lookup"><span data-stu-id="b580b-226">Note the **Reveal** link.</span></span>  <span data-ttu-id="b580b-227">Después de elegirlo, DevTools para resaltar el evento que inició el evento de **fotograma de animación desencadenado** .</span><span class="sxs-lookup"><span data-stu-id="b580b-227">After you choose it, DevTools to highlights the event that initiated the **Animation Frame Fired** event.</span></span>  <span data-ttu-id="b580b-228">Además, céntrese en el vínculo **app.js:95** .</span><span class="sxs-lookup"><span data-stu-id="b580b-228">Also, focus on the **app.js:95** link.</span></span>  <span data-ttu-id="b580b-229">Después de elegirlo, se muestra la línea correspondiente en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="b580b-229">After you choose it, the relevant line in the source code is displayed.</span></span>
    
    :::image type="complex" source="../media/evaluate-performance-performance-animation-frame-fired.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-performance-animation-frame-fired.msft.png":::
       <span data-ttu-id="b580b-231">Más información sobre el evento de **marco de animación desencadenado**</span><span class="sxs-lookup"><span data-stu-id="b580b-231">More information about the **Animation Frame Fired** event</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b580b-232">Después de seleccionar un evento, use las teclas de dirección para seleccionar los eventos que hay junto a él.</span><span class="sxs-lookup"><span data-stu-id="b580b-232">After selecting an event, use the arrow keys to select the events next to it.</span></span>  
    
1.  <span data-ttu-id="b580b-233">En el evento **app. Update** , hay un montón de eventos púrpura.</span><span class="sxs-lookup"><span data-stu-id="b580b-233">Under the **app.update** event, there is a bunch of purple events.</span></span>  <span data-ttu-id="b580b-234">Si cada evento morado era más ancho, parece que cada uno de ellos puede tener un triángulo rojo.</span><span class="sxs-lookup"><span data-stu-id="b580b-234">If each purple event was wider, it looks as though each one may have a red triangle on it.</span></span>  
1.  <span data-ttu-id="b580b-235">Elija uno de los eventos de **diseño** púrpura.</span><span class="sxs-lookup"><span data-stu-id="b580b-235">Choose one of the purple **Layout** events.</span></span>  <span data-ttu-id="b580b-236">DevTools proporciona más información sobre el evento en la pestaña **Resumen** .  De hecho, hay una advertencia sobre los reflujos forzados \ (otra palabra para el diseño \).</span><span class="sxs-lookup"><span data-stu-id="b580b-236">DevTools provides more information about the event in the **Summary** tab.  Indeed, there is a warning about forced reflows \(another word for layout\).</span></span>  
    
1.  <span data-ttu-id="b580b-237">En la pestaña **Resumen** , elija el vínculo **app.js:71** en **diseño forzado**.</span><span class="sxs-lookup"><span data-stu-id="b580b-237">In the **Summary** tab, choose the **app.js:71** link under **Layout Forced**.</span></span>  <span data-ttu-id="b580b-238">DevTools le lleva a la línea de código que forzó el diseño.</span><span class="sxs-lookup"><span data-stu-id="b580b-238">DevTools takes you to the line of code that forced the layout.</span></span>  
    
    :::image type="complex" source="../media/evaluate-performance-sources-app-update.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-sources-app-update.msft.png":::
       <span data-ttu-id="b580b-240">La línea de código que causó el diseño forzado</span><span class="sxs-lookup"><span data-stu-id="b580b-240">The line of code that caused the forced layout</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b580b-241">El problema con el código es que, en cada marco de animación, cambia el estilo de cada icono y, después, consulta la posición de cada icono de la página.</span><span class="sxs-lookup"><span data-stu-id="b580b-241">The problem with the code is that, in each animation frame, it changes the style for each icon, and then queries the position of each icon on the page.</span></span>  <span data-ttu-id="b580b-242">Dado que los estilos han cambiado, el explorador no sabe si ha cambiado la posición de cada icono, por lo que tiene que volver a distribuir el icono para calcular la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="b580b-242">Because the styles changed, the browser does not know if each icon position changed, so it has to re-layout the icon in order to compute the new position.</span></span>  <!--  > See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->
    
<!-- todo: add layouts section when available -->

<span data-ttu-id="b580b-243">Eso fue mucho para aprender.</span><span class="sxs-lookup"><span data-stu-id="b580b-243">That was a lot to learn.</span></span>  <span data-ttu-id="b580b-244">Ahora tiene una base sólida en el flujo de trabajo básico para analizar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b580b-244">You now have a solid foundation in the basic workflow for analyzing runtime performance.</span></span>  <span data-ttu-id="b580b-245">Buen trabajo.</span><span class="sxs-lookup"><span data-stu-id="b580b-245">Good job.</span></span>  

### <span data-ttu-id="b580b-246">Bonificación: analizar la versión optimizada</span><span class="sxs-lookup"><span data-stu-id="b580b-246">Bonus: Analyze the optimized version</span></span>  

<span data-ttu-id="b580b-247">Usando los flujos de trabajo y las herramientas que acaba de aprender, elija **optimizar** en la demostración para habilitar el código optimizado, tomar otra grabación de rendimiento y analizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="b580b-247">Using the workflows and tools that you just learned, choose **Optimize** on the demo to enable the optimized code, take another performance recording, and then analyze the results.</span></span>  <span data-ttu-id="b580b-248">Desde la velocidad de fotogramas mejorada hasta la reducción en eventos en el gráfico de llamas de la sección **principal** , podrá ver que la versión optimizada de la aplicación hace mucho menos trabajo, lo que da como resultado un mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b580b-248">From the improved framerate to the reduction in events in the flame chart in the **Main** section, you are able to see that the optimized version of the app does much less work, resulting in better performance.</span></span>  

> [!NOTE]
> <span data-ttu-id="b580b-249">Incluso la versión optimizada no es genial, porque manipula la `top` propiedad de todos los iconos.</span><span class="sxs-lookup"><span data-stu-id="b580b-249">Even the optimized version is not great, because it manipulates the `top` property of every icon.</span></span>  <span data-ttu-id="b580b-250">Un mejor enfoque es ceñirse a las propiedades que solo afectan a la composición.</span><span class="sxs-lookup"><span data-stu-id="b580b-250">A better approach is to stick to properties that only affect compositing.</span></span>  <!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## <span data-ttu-id="b580b-251">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="b580b-251">Next steps</span></span>

<!--The foundation for understanding performance is the RAIL model.  The RAIL model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

<span data-ttu-id="b580b-252">Para estar más familiarizado con el panel rendimiento, la práctica es ideal.</span><span class="sxs-lookup"><span data-stu-id="b580b-252">To get more comfortable with the Performance panel, practice makes perfect.</span></span>  <span data-ttu-id="b580b-253">Pruebe a generar perfiles de las páginas y analizar los resultados.</span><span class="sxs-lookup"><span data-stu-id="b580b-253">Try profiling your pages and analyzing the results.</span></span>  <span data-ttu-id="b580b-254">Si tiene alguna pregunta sobre los resultados, use el icono para **Enviar comentarios** , seleccione `Alt` + `Shift` + `I` \ (Windows, Linux \), seleccione `Option` + `Shift` + `I` \ (MacOS \) o [Tweet el equipo de DevTools][TwitterEdgeDevtools].</span><span class="sxs-lookup"><span data-stu-id="b580b-254">If you have any questions about your results, use the **Send Feedback** icon, select `Alt`+`Shift`+`I` \(Windows, Linux\), select `Option`+`Shift`+`I` \(macOS\), or [tweet the DevTools team][TwitterEdgeDevtools].</span></span>  <span data-ttu-id="b580b-255">Incluya capturas de pantallas o vínculos a páginas reproducibles, si es posible.</span><span class="sxs-lookup"><span data-stu-id="b580b-255">Include screenshots or links to reproducible pages, if possible.</span></span>  

:::image type="complex" source="../media/evaluate-performance-feedback-icon.msft.png" alt-text="La demostración de la izquierda y DevTools a la derecha" lightbox="../media/evaluate-performance-feedback-icon.msft.png":::
   <span data-ttu-id="b580b-257">El icono **Enviar comentarios** en el DevTools de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b580b-257">The **Send Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- To really become an expert in runtime performance, you must learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

<span data-ttu-id="b580b-258">Por último, hay muchas maneras de mejorar el rendimiento en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b580b-258">Last, there are many ways to improve runtime performance.</span></span>  <span data-ttu-id="b580b-259">Este artículo se centró en un cuello de botella de animación para darle un recorrido centrado en el panel rendimiento, pero es sólo uno de los muchos cuellos de botella que puede encontrar.</span><span class="sxs-lookup"><span data-stu-id="b580b-259">This article focused on one particular animation bottleneck to give you a focused tour through the Performance panel, but it is only one of many bottlenecks you may encounter.</span></span>  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

## <span data-ttu-id="b580b-260">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b580b-260">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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
> <span data-ttu-id="b580b-265">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b580b-265">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b580b-266">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b580b-266">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b580b-268">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b580b-268">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
