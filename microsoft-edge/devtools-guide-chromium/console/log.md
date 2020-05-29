---
title: Introducción al registro de mensajes en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: d3dbec41bc1e53b5e9001551c796e5a495dd331e
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601736"
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





# <span data-ttu-id="ceaf4-103">Introducción al registro de mensajes en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-103">Get Started With Logging Messages In The Console</span></span>   



<span data-ttu-id="ceaf4-104">Este tutorial interactivo le muestra cómo registrar y filtrar mensajes en la consola de [DevTools de Microsoft Edge][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-104">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

> ##### <span data-ttu-id="ceaf4-105">Figura 1</span><span class="sxs-lookup"><span data-stu-id="ceaf4-105">Figure 1</span></span>  
> <span data-ttu-id="ceaf4-106">Mensajes en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-106">Messages in the Console</span></span>  
> ![Mensajes en la consola][ImageLogExample]  

<span data-ttu-id="ceaf4-108">Este tutorial está pensado para completarse en orden.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="ceaf4-109">Se da por hecho que comprende los aspectos básicos del desarrollo web, como el uso de JavaScript para agregar interactividad a una página.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="ceaf4-110">Configurar la demostración y las DevTools</span><span class="sxs-lookup"><span data-stu-id="ceaf4-110">Set up the demo and DevTools</span></span>   

<span data-ttu-id="ceaf4-111">Este tutorial está diseñado para que puedas abrir la demostración y probar todos los flujos de trabajo tú mismo.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="ceaf4-112">Cuando sigues físicamente, es más probable que recuerdes los flujos de trabajo más adelante.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="ceaf4-113">Mantenga `Control` \ (Windows \) o `Command` \ (MacOS \) y haga clic en **ejemplos del registro de consola** para abrirlos en una nueva pestaña.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-113">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="ceaf4-114">Ejemplos del registro de consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!-- > [!TIP]
    > Move the demo to a separate window.  
    > 
    > > ##### old Figure 2  
    > > The tutorial on the left, and the demo on the right  
    > > ![The tutorial on the left, and the demo on the right][ImageLogSetUp1]  -->
    
1.  <span data-ttu-id="ceaf4-115">Centre la demostración y, a continuación, pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-115">Focus the demo and then press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="ceaf4-116">De forma predeterminada, DevTools se abre a la derecha de la demostración.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-116">By default DevTools opens to the right of the demo.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="ceaf4-117">Figure 2</span></span>  
    > <span data-ttu-id="ceaf4-118">DevTools se abre a la derecha de la demostración</span><span class="sxs-lookup"><span data-stu-id="ceaf4-118">DevTools opens to the right of the demo</span></span>  
    > <span data-ttu-id="ceaf4-119">! [DevTools se abre a la derecha de la demostración] [ImageDevToolsRight]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-119">![DevTools opens to the right of the demo][ImageDevToolsRight]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="ceaf4-120">[Acople DevTools en la parte inferior de la ventana o desacoplelo en una ventana independiente][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="ceaf4-120">[Dock DevTools to the bottom of the window or undock it into a separate window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-121">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="ceaf4-121">Figure 3</span></span>  
    > <span data-ttu-id="ceaf4-122">DevTools acoplado a la parte inferior de la demostración</span><span class="sxs-lookup"><span data-stu-id="ceaf4-122">DevTools docked to the bottom of the demo</span></span>  
    > <span data-ttu-id="ceaf4-123">! [DevTools acoplada a la parte inferior de la demostración] [ImageDevToolsBottom]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-123">![DevTools docked to the bottom of the demo][ImageDevToolsBottom]</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-124">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="ceaf4-124">Figure 4</span></span>  
    > <span data-ttu-id="ceaf4-125">Explorador en una ventana independiente</span><span class="sxs-lookup"><span data-stu-id="ceaf4-125">Browser in a separate window</span></span>  
    > <span data-ttu-id="ceaf4-126">! [Explorador en una ventana independiente] [ImageDevToolsSeparateBrowse]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-126">![Browser in a separate window][ImageDevToolsSeparateBrowse]</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-127">Imagen 5</span><span class="sxs-lookup"><span data-stu-id="ceaf4-127">Figure 5</span></span>  
    > <span data-ttu-id="ceaf4-128">DevTools desacoplado en una ventana independiente</span><span class="sxs-lookup"><span data-stu-id="ceaf4-128">DevTools undocked in a separate window</span></span>  
    > <span data-ttu-id="ceaf4-129">! [DevTools desacoplado en una ventana independiente] [ImageDevToolsSeparateDevTools]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-129">![DevTools undocked in a separate window][ImageDevToolsSeparateDevTools]</span></span>  
    
## <span data-ttu-id="ceaf4-130">Ver mensajes registrados desde JavaScript</span><span class="sxs-lookup"><span data-stu-id="ceaf4-130">View messages logged from JavaScript</span></span>   

<span data-ttu-id="ceaf4-131">La mayoría de los mensajes que ve en la consola provienen de los programadores web que escribieron el JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-131">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="ceaf4-132">El objetivo de esta sección es presentarle los diferentes tipos de mensajes que probablemente verá en la consola y explicar cómo puede registrar cada tipo de mensaje desde su propio JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-132">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="ceaf4-133">Haga clic en el botón **información de registro** de la demostración.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-133">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="ceaf4-134">se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-134">gets logged to the Console.</span></span>
    
    > ##### <span data-ttu-id="ceaf4-135">Imagen 6</span><span class="sxs-lookup"><span data-stu-id="ceaf4-135">Figure 6</span></span>  
    > <span data-ttu-id="ceaf4-136">La consola después de hacer clic en **información de registro**</span><span class="sxs-lookup"><span data-stu-id="ceaf4-136">The Console after clicking **Log Info**</span></span>  
    > <span data-ttu-id="ceaf4-137">! [La consola después de hacer clic en información de registro] [ImageLogInfo]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-137">![The Console after clicking Log Info][ImageLogInfo]</span></span>  
    
1.  <span data-ttu-id="ceaf4-138">Junto al `Hello, Console!` mensaje en la consola, haga clic en **log. js: 2**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-138">Next to the `Hello, Console!` message in the Console click **log.js:2**.</span></span>  <span data-ttu-id="ceaf4-139">El panel orígenes se abre y resalta la línea de código que causó que el mensaje se registre en la consola.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-139">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="ceaf4-140">El mensaje se registró cuando se ejecutó el JavaScript de la página `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-140">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    > ##### <span data-ttu-id="ceaf4-141">Imagen 7</span><span class="sxs-lookup"><span data-stu-id="ceaf4-141">Figure 7</span></span>  
    > <span data-ttu-id="ceaf4-142">DevTools abre el panel orígenes después de hacer clic en **log. js: 2**</span><span class="sxs-lookup"><span data-stu-id="ceaf4-142">DevTools opens the Sources panel after you click **log.js:2**</span></span>  
    > <span data-ttu-id="ceaf4-143">! [DevTools abre el panel orígenes después de hacer clic en log. js: 2]. [ImageSourceLog]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-143">![DevTools opens the Sources panel after you click log.js:2][ImageSourceLog]</span></span>  
    
1.  <span data-ttu-id="ceaf4-144">Vuelva a la consola con uno de los siguientes flujos de trabajo:</span><span class="sxs-lookup"><span data-stu-id="ceaf4-144">Navigate back to the Console using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="ceaf4-145">Haga clic en la pestaña **consola** .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-145">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="ceaf4-146">Pulse `Control` + `[` \ (Windows \) o `Command` + `[` \ (MacOS \) hasta que el panel de la consola esté en el foco.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-146">Press `Control`+`[` \(Windows\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="ceaf4-147">[Abra el menú de comandos][DevToolsCommandMenu], empiece `Console` a escribir, seleccione el comando **Mostrar panel de consola** y, a continuación, presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-147">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then press `Enter`.</span></span>  
    
1.  <span data-ttu-id="ceaf4-148">Haga clic en el botón **registrar ADVERTENCIA** de la demostración.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-148">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="ceaf4-149">se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-149">gets logged to the Console.</span></span>  <span data-ttu-id="ceaf4-150">Los mensajes con formato como este son advertencias.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-150">Messages formatted like this are warnings.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-151">Imagen 8</span><span class="sxs-lookup"><span data-stu-id="ceaf4-151">Figure 8</span></span>  
    > <span data-ttu-id="ceaf4-152">La consola después de hacer clic en **Advertencia de registro**</span><span class="sxs-lookup"><span data-stu-id="ceaf4-152">The Console after clicking **Log Warning**</span></span>  
    > <span data-ttu-id="ceaf4-153">! [La consola después de hacer clic en ADVERTENCIA de registro] [ImageConsoleLogWarning]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-153">![The Console after clicking Log Warning][ImageConsoleLogWarning]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="ceaf4-154">Si desea ver el código que causó un mensaje para que se registre de una determinada manera, haga clic en un script \ (como `log.js:12` \) para ver el código que causó el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-154">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="ceaf4-155">Haga clic **Expand** ![ en el icono de expandir que hay ][ImageExpandIcon] delante `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-155">Click the **Expand** ![Expand][ImageExpandIcon] icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="ceaf4-156">DevTools muestra el [seguimiento][WikiStackTrace] de la pila que se dirige a la llamada.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-156">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-157">Imagen 9</span><span class="sxs-lookup"><span data-stu-id="ceaf4-157">Figure 9</span></span>  
    > <span data-ttu-id="ceaf4-158">Un seguimiento de pila</span><span class="sxs-lookup"><span data-stu-id="ceaf4-158">A stack trace</span></span>  
    > <span data-ttu-id="ceaf4-159">! [Un seguimiento de pila] [ImageStackTrace]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-159">![A stack trace][ImageStackTrace]</span></span>  
    
    <span data-ttu-id="ceaf4-160">El seguimiento de la pila le indica que se ha llamado a una función llamada `logWarning` , que a su vez llamó a una función llamada `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-160">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="ceaf4-161">En otras palabras, la llamada que ocurrió en primer lugar se encuentra en la parte inferior del seguimiento de pila.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-161">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="ceaf4-162">Puedes registrar los seguimientos de la pila en cualquier momento llamando a `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-162">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="ceaf4-163">Haga clic en **registrar error**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-163">Click **Log Error**.</span></span>  <span data-ttu-id="ceaf4-164">Se ha registrado el siguiente mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="ceaf4-164">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    > ##### <span data-ttu-id="ceaf4-165">Imagen 10</span><span class="sxs-lookup"><span data-stu-id="ceaf4-165">Figure 10</span></span>  
    > <span data-ttu-id="ceaf4-166">Un mensaje de error</span><span class="sxs-lookup"><span data-stu-id="ceaf4-166">An error message</span></span>  
    > <span data-ttu-id="ceaf4-167">! [Mensaje de error] [ImageLogError]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-167">![An error message][ImageLogError]</span></span>  
    
1.  <span data-ttu-id="ceaf4-168">Haga clic en **tabla de registro**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-168">Click **Log Table**.</span></span>  <span data-ttu-id="ceaf4-169">Se graba en la consola una tabla sobre artistas famosos.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-169">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="ceaf4-170">La `birthday` columna solo se rellena para una fila.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-170">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="ceaf4-171">Consulte el código para averiguar el motivo.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-171">Check the code to figure out why that is.</span></span>
    
    > ##### <span data-ttu-id="ceaf4-172">Imagen 11</span><span class="sxs-lookup"><span data-stu-id="ceaf4-172">Figure 11</span></span>  
    > <span data-ttu-id="ceaf4-173">Una tabla en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-173">A table in the Console</span></span>  
    > <span data-ttu-id="ceaf4-174">! [Una tabla en la consola] [ImageConsoleTable]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-174">![A table in the Console][ImageConsoleTable]</span></span>  
    
1.  <span data-ttu-id="ceaf4-175">Haga clic en **grupo de registro**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-175">Click **Log Group**.</span></span>  <span data-ttu-id="ceaf4-176">Los nombres de las cuatro tortugas famosas y de lucha contra delitos se agrupan debajo de la `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-176">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-177">Imagen 12</span><span class="sxs-lookup"><span data-stu-id="ceaf4-177">Figure 12</span></span>  
    > <span data-ttu-id="ceaf4-178">Un grupo de mensajes en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-178">A group of messages in the Console</span></span>  
    > <span data-ttu-id="ceaf4-179">! [Un grupo de mensajes en la consola] [ImageConsoleLogGroup]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-179">![A group of messages in the Console][ImageConsoleLogGroup]</span></span>  
    
1.  <span data-ttu-id="ceaf4-180">Haga clic en **registro personalizado**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-180">Click **Log Custom**.</span></span>  <span data-ttu-id="ceaf4-181">Se graba en la consola un mensaje con un borde rojo y un fondo azul.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-181">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-182">Imagen 13</span><span class="sxs-lookup"><span data-stu-id="ceaf4-182">Figure 13</span></span>  
    > <span data-ttu-id="ceaf4-183">Un mensaje con formato personalizado en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-183">A message with custom formatting in the Console</span></span>  
    > <span data-ttu-id="ceaf4-184">! [Mensaje con formato personalizado en la consola] [ImageConsoleLogCustomFormatting]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-184">![A message with custom formatting in the Console][ImageConsoleLogCustomFormatting]</span></span>  
    
<span data-ttu-id="ceaf4-185">La idea principal es que cuando quieras registrar mensajes en la consola desde tu código JavaScript, usas uno de los `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-185">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="ceaf4-186">Cada método da formato a los mensajes de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-186">Each method formats messages differently.</span></span>  

<span data-ttu-id="ceaf4-187">Hay aún más métodos de los que se han demostrado en esta sección.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-187">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="ceaf4-188">En este tutorial se muestra cómo explorar el resto de los métodos.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-188">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="ceaf4-189">Ver los mensajes registrados por el explorador</span><span class="sxs-lookup"><span data-stu-id="ceaf4-189">View messages logged by the browser</span></span>   

<span data-ttu-id="ceaf4-190">El explorador también registra mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-190">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="ceaf4-191">Esto suele ocurrir cuando hay un problema con la página.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-191">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="ceaf4-192">Haga clic en **Cause 404**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-192">Click **Cause 404**.</span></span>  <span data-ttu-id="ceaf4-193">El explorador registra un `404` error de red porque el código JavaScript de la página ha intentado buscar un archivo que no existe.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-193">The browser logs a `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-194">Imagen 14</span><span class="sxs-lookup"><span data-stu-id="ceaf4-194">Figure 14</span></span>  
    > <span data-ttu-id="ceaf4-195">Error 404 en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-195">A 404 error in the Console</span></span>  
    > <span data-ttu-id="ceaf4-196">! [Error 404 en la consola] [ImageConsoleLogError]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-196">![A 404 error in the Console][ImageConsoleLogError]</span></span>  
    
1.  <span data-ttu-id="ceaf4-197">Haga clic en **causa del error**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-197">Click **Cause Error**.</span></span>  <span data-ttu-id="ceaf4-198">El explorador registra una no capturada `TypeError` porque el JavaScript está intentando actualizar un nodo Dom que no existe.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-198">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-199">Imagen 15</span><span class="sxs-lookup"><span data-stu-id="ceaf4-199">Figure 15</span></span>  
    > <span data-ttu-id="ceaf4-200">Un TypeError en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-200">A TypeError in the Console</span></span>  
    > <span data-ttu-id="ceaf4-201">! [Un TypeError en la consola] [ImageConsoleLogTypeError]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-201">![A TypeError in the Console][ImageConsoleLogTypeError]</span></span>  
    
1.  <span data-ttu-id="ceaf4-202">Haga clic en la lista desplegable **niveles de registro** y habilite la opción **detallado** si está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-202">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="ceaf4-203">Para obtener más información sobre el filtrado, vaya a la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-203">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="ceaf4-204">Tiene que hacer esto para asegurarse de que el siguiente mensaje que inicie sesión está visible.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-204">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-205">Imagen 16</span><span class="sxs-lookup"><span data-stu-id="ceaf4-205">Figure 16</span></span>  
    > <span data-ttu-id="ceaf4-206">Habilitar el nivel de registro **detallado**</span><span class="sxs-lookup"><span data-stu-id="ceaf4-206">Enabling the **Verbose** log level</span></span>  
    > <span data-ttu-id="ceaf4-207">! [Habilitar el nivel de registro detallado] [ImageVerboseLogLevel]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-207">![Enabling the Verbose log level][ImageVerboseLogLevel]</span></span>  
    
1.  <span data-ttu-id="ceaf4-208">Haga clic en **causa de infracción**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-208">Click **Cause Violation**.</span></span>  <span data-ttu-id="ceaf4-209">La página deja de responder durante unos segundos y, a continuación, el explorador registra el mensaje `[Violation] 'click' handler took 3000ms` en la consola.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-209">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="ceaf4-210">La duración exacta puede variar.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-210">The exact duration may vary.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-211">Imagen 17</span><span class="sxs-lookup"><span data-stu-id="ceaf4-211">Figure 17</span></span>  
    > <span data-ttu-id="ceaf4-212">Violación en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-212">A violation in the Console</span></span>  
    > <span data-ttu-id="ceaf4-213">! [Infracción en la consola] [ImageConsoleLogViolation]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-213">![A violation in the Console][ImageConsoleLogViolation]</span></span>  
    
## <span data-ttu-id="ceaf4-214">Filtrar mensajes</span><span class="sxs-lookup"><span data-stu-id="ceaf4-214">Filter messages</span></span>   

<span data-ttu-id="ceaf4-215">En algunas páginas verás que la consola está inundada de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-215">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="ceaf4-216">DevTools proporciona varias formas diferentes de filtrar los mensajes que no son relevantes para la tarea que está realizando.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-216">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="ceaf4-217">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="ceaf4-217">Filter by log level</span></span>   

<span data-ttu-id="ceaf4-218">`console`A cada método se le asigna un nivel de gravedad: `Verbose` ,, `Info` `Warning` o `Error` .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-218">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="ceaf4-219">Por ejemplo, `console.log()` es un `Info` mensaje de nivel, mientras que `console.error()` es `Error` un mensaje de nivel.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-219">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="ceaf4-220">Haga clic en la lista desplegable **niveles de registro** y deshabilite **errores**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-220">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="ceaf4-221">Un nivel se deshabilita cuando ya no hay una marca de verificación junto a él.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-221">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="ceaf4-222">Los `Error` mensajes de nivel desaparecen.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-222">The `Error`-level messages disappear.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-223">Ilustración 18</span><span class="sxs-lookup"><span data-stu-id="ceaf4-223">Figure 18</span></span>  
    > <span data-ttu-id="ceaf4-224">Deshabilitar `Error` el nivel de mensajes en la consola</span><span class="sxs-lookup"><span data-stu-id="ceaf4-224">Disabling `Error`-level messages in the Console</span></span>  
    > <span data-ttu-id="ceaf4-225">! [Deshabilitar mensajes de nivel de error en la consola] [ImageConsoleDisablingLogError]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-225">![Disabling Error-level messages in the Console][ImageConsoleDisablingLogError]</span></span>  
    
1.  <span data-ttu-id="ceaf4-226">Vuelva a hacer clic en la lista desplegable **niveles de registro** y vuelva a habilitar los **errores**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-226">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="ceaf4-227">Los `Error` mensajes del nivel volverán a aparecer.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-227">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="ceaf4-228">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="ceaf4-228">Filter by text</span></span>   

<span data-ttu-id="ceaf4-229">Cuando desee ver solo los mensajes que incluyan una cadena exacta, escríbala en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-229">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="ceaf4-230">Escriba `Dave` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-230">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="ceaf4-231">Todos los mensajes que no incluyan la cadena `Dave` están ocultos.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-231">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="ceaf4-232">También puede ver la `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-232">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="ceaf4-233">Es un error.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-233">That is a bug.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-234">Ilustración 19</span><span class="sxs-lookup"><span data-stu-id="ceaf4-234">Figure 19</span></span>  
    > <span data-ttu-id="ceaf4-235">Filtrar cualquier mensaje que no incluya</span><span class="sxs-lookup"><span data-stu-id="ceaf4-235">Filtering out any message that does not include</span></span> `Dave`  
    > <span data-ttu-id="ceaf4-236">! [Filtrar cualquier mensaje que no incluya Dave] [ImageLogTextFiltering]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-236">![Filtering out any message that does not include Dave][ImageLogTextFiltering]</span></span>  
    
1.  <span data-ttu-id="ceaf4-237">Eliminar `Dave` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-237">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="ceaf4-238">Todos los mensajes volverán a aparecer.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-238">All the messages reappear.</span></span>  

### <span data-ttu-id="ceaf4-239">Filtrar por expresión regular</span><span class="sxs-lookup"><span data-stu-id="ceaf4-239">Filter by regular expression</span></span>   

<span data-ttu-id="ceaf4-240">Cuando desee mostrar todos los mensajes que incluyan un patrón de texto, en lugar de una cadena específica, use una [expresión regular][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="ceaf4-240">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="ceaf4-241">Escriba `/^[AH]/` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-241">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="ceaf4-242">Escriba este patrón en [Regex][|::ref1::|Main] para obtener una explicación de lo que está haciendo.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-242">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-243">Ilustración 20</span><span class="sxs-lookup"><span data-stu-id="ceaf4-243">Figure 20</span></span>  
    > <span data-ttu-id="ceaf4-244">Filtrar los mensajes que no coincidan con el patrón</span><span class="sxs-lookup"><span data-stu-id="ceaf4-244">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    > <span data-ttu-id="ceaf4-245">! [Filtrar cualquier mensaje que no coincida con un patrón] [ImageLogRegExFiltering]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-245">![Filtering out any message that does not match a pattern][ImageLogRegExFiltering]</span></span>  
    
1.  <span data-ttu-id="ceaf4-246">Eliminar `/^[AH]/` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-246">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="ceaf4-247">Todos los mensajes volverán a verse.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-247">All messages are visible again.</span></span>  

### <span data-ttu-id="ceaf4-248">Filtrar por origen del mensaje</span><span class="sxs-lookup"><span data-stu-id="ceaf4-248">Filter by message source</span></span>   

<span data-ttu-id="ceaf4-249">Si desea ver solo los mensajes procedentes de una dirección URL determinada, use la **barra lateral**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-249">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="ceaf4-250">Haga clic en **Mostrar la barra lateral de consola** ![ Mostrar la barra lateral ][ImageShowConsoleSidebarIcon] .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-250">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon].</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-251">Ilustración 21</span><span class="sxs-lookup"><span data-stu-id="ceaf4-251">Figure 21</span></span>  
    > <span data-ttu-id="ceaf4-252">La barra lateral</span><span class="sxs-lookup"><span data-stu-id="ceaf4-252">The Sidebar</span></span>  
    > <span data-ttu-id="ceaf4-253">! [Barra lateral] [ImageConsoleSidebar]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-253">![The Sidebar][ImageConsoleSidebar]</span></span>  
    
1.  <span data-ttu-id="ceaf4-254">Haga clic **en el** ![ icono expandir expandir ][ImageExpandIcon] situado junto al número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-254">Click the **Expand** ![Expand][ImageExpandIcon] icon next to the number of messages.</span></span>  <span data-ttu-id="ceaf4-255">En la [figura 21](#figure-21), la cantidad de mensajes se indica como **13 mensajes**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-255">In [Figure 21](#figure-21), the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="ceaf4-256">La **barra lateral** muestra una lista de las direcciones URL que han provocado el registro de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-256">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="ceaf4-257">Por ejemplo, se `log.js` produjeron 11 mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-257">For example, `log.js` caused 11 messages.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-258">Ilustración 22</span><span class="sxs-lookup"><span data-stu-id="ceaf4-258">Figure 22</span></span>  
    > <span data-ttu-id="ceaf4-259">Ver el origen de los mensajes en la barra lateral</span><span class="sxs-lookup"><span data-stu-id="ceaf4-259">Viewing the source of messages in the Sidebar</span></span>  
    > <span data-ttu-id="ceaf4-260">! [Ver el origen de los mensajes en la barra lateral] [ImageConsoleSidebarLogSource]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-260">![Viewing the source of messages in the Sidebar][ImageConsoleSidebarLogSource]</span></span>  
    
### <span data-ttu-id="ceaf4-261">Filtrar por mensajes de usuario</span><span class="sxs-lookup"><span data-stu-id="ceaf4-261">Filter by user messages</span></span>   

<span data-ttu-id="ceaf4-262">Anteriormente, cuando se hace clic en **información de registro**, se llama a un script para `console.log('Hello, Console!')` registrar el mensaje en la consola.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-262">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="ceaf4-263">Los mensajes registrados de JavaScript como este se denominan **mensajes de usuario**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-263">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="ceaf4-264">Por el contrario, cuando hace clic en la **causa 404**, el explorador registra un `Error` mensaje que indica que no se pudo encontrar el recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-264">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="ceaf4-265">Mensajes como los que se consideran **mensajes del explorador**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-265">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="ceaf4-266">Use la **barra lateral** para filtrar los mensajes del explorador y mostrar solo los mensajes de usuario.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-266">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="ceaf4-267">Haga clic en **9 mensajes de usuario**.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-267">Click **9 User Messages**.</span></span>  <span data-ttu-id="ceaf4-268">Los mensajes del explorador están ocultos.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-268">The browser messages are hidden.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-269">Ilustración 23</span><span class="sxs-lookup"><span data-stu-id="ceaf4-269">Figure 23</span></span>  
    > <span data-ttu-id="ceaf4-270">Filtrar los mensajes del explorador</span><span class="sxs-lookup"><span data-stu-id="ceaf4-270">Filtering out browser messages</span></span>  
    > <span data-ttu-id="ceaf4-271">! [Filtrar los mensajes del explorador] [ImageConsoleLogBrowserFiltering]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-271">![Filtering out browser messages][ImageConsoleLogBrowserFiltering]</span></span>  
    
1.  <span data-ttu-id="ceaf4-272">Haga clic en **13 mensajes** para volver a mostrar todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-272">Click **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="ceaf4-273">Usar la consola junto con cualquier otro panel</span><span class="sxs-lookup"><span data-stu-id="ceaf4-273">Use the Console alongside any other panel</span></span>   

<span data-ttu-id="ceaf4-274">¿Qué sucede si está editando estilos, pero necesita consultar rápidamente el registro de consola para buscar algo?</span><span class="sxs-lookup"><span data-stu-id="ceaf4-274">What if you are editing styles, but you need to quickly check the Console log for something?</span></span> <span data-ttu-id="ceaf4-275">Use el cajón.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-275">Use the Drawer.</span></span>  

1.  <span data-ttu-id="ceaf4-276">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-276">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="ceaf4-277">Presione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-277">Press `Escape`.</span></span>  <span data-ttu-id="ceaf4-278">Se abrirá la ficha Console del **cajón** .</span><span class="sxs-lookup"><span data-stu-id="ceaf4-278">The Console tab of the **Drawer** opens.</span></span>  <span data-ttu-id="ceaf4-279">Tiene todas las características del panel de la consola que ha estado usando en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="ceaf4-279">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    > ##### <span data-ttu-id="ceaf4-280">Ilustración 24</span><span class="sxs-lookup"><span data-stu-id="ceaf4-280">Figure 24</span></span>  
    > <span data-ttu-id="ceaf4-281">Ficha de consola en el cajón</span><span class="sxs-lookup"><span data-stu-id="ceaf4-281">The Console tab in the Drawer</span></span>  
    > <span data-ttu-id="ceaf4-282">! [Ficha de consola en el cajón] [ImageDrawerConsole]</span><span class="sxs-lookup"><span data-stu-id="ceaf4-282">![The Console tab in the Drawer][ImageDrawerConsole]</span></span>  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

 



<!-- image links -->  

[ImageExpandIcon]: /microsoft-edge/devtools-guide-chromium/media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageLogExample]: /microsoft-edge/devtools-guide-chromium/media/console-ars-technica-console-onload.msft.png "Ilustración 1: mensajes en la consola"  
<!--[ImageLogSetUp1]: /microsoft-edge/devtools-guide-chromium/media/log-set-up-1.msft.png "old Figure 2: The tutorial on the left, and the demo on the right"  -->  
[ImageDevToolsRight]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-example-DevTools-Right-Console.msft.png "Figura 2: DevTools se abre a la derecha de la demostración"  
[ImageDevToolsBottom]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-example-DevTools-Bottom-Console.msft.png "Ilustración 3: DevTools acoplado a la parte inferior de la demostración"  
[ImageDevToolsSeparateBrowse]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-example-DevTools-separate-Console-Browse.msft.png "Ilustración 4: explorador en una ventana independiente"  
[ImageDevToolsSeparateDevTools]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-example-DevTools-separate-Console-DevTools.msft.png "Ilustración 5: DevTools desacoplado en una ventana independiente"  
[ImageLogInfo]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-info.msft.png "Ilustración 6: la consola después de hacer clic en información de registro"  
[ImageSourceLog]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-sources-logjs.msft.png "Figura 7: DevTools abre el panel orígenes después de hacer clic en log. js: 2"  
[ImageConsoleLogWarning]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-warning.msft.png "Ilustración 8: la consola después de hacer clic en ADVERTENCIA de registro"  
[ImageStackTrace]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-Warning-Expanded.msft.png "Ilustración 9: un seguimiento de la pila"  
[ImageLogError]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-error.msft.png "Figura 10: un mensaje de error"  
[ImageConsoleTable]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-Table.msft.png "ilustración 11: una tabla en la consola"  
[ImageConsoleLogGroup]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-Group.msft.png "Ilustración 12: un grupo de mensajes en la consola"  
[ImageConsoleLogCustomFormatting]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-log-Custom.msft.png "ilustración 13: un mensaje con formato personalizado en la consola"  
[ImageConsoleLogError]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-404.msft.png "Ilustración 14: error 404 en la consola"  
[ImageConsoleLogTypeError]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-error.msft.png "Figura 15: un TypeError en la consola"  
[ImageVerboseLogLevel]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-error-log-levels.msft.png "Figura 16: habilitar el nivel de registro detallado"  
[ImageConsoleLogViolation]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-Violation.msft.png "Ilustración 17: una infracción en la consola"  
[ImageConsoleDisablingLogError]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-cause-Violation-log-levels.msft.png "ilustración 18: deshabilitar mensajes de nivel de error en la consola"  
[ImageLogTextFiltering]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-All-messages-Text-Filter.msft.png "Ilustración 19: filtrar cualquier mensaje que no incluya Dave"  
[ImageLogRegExFiltering]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-All-messages-regex-Filter.msft.png "figura 20: filtrar los mensajes que no coincidan con un patrón"  
[ImageConsoleSidebar]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-All-messages.msft.png "ilustración 21: la barra lateral"  
[ImageConsoleSidebarLogSource]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-Expanded-All-messages.msft.png "Ilustración 22: ver el origen de los mensajes en la barra lateral"  
[ImageConsoleLogBrowserFiltering]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Sidebar-User-messages.msft.png "Ilustración 23: filtrar los mensajes del explorador"  
[ImageDrawerConsole]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Console-Elements-Drawer-Console-Sidebar-All-messages.msft.png "Ilustración 24: ficha consola en el cajón"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas de desarrollador de Microsoft Edge \ (cromo \)"  
[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  
[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Cambiar la ubicación de DevTools de Microsoft Edge (desacoplar, acoplar a la parte inferior, acoplar a la izquierda)"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de la API de consola"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference "Referencia de consola"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introducción a la creación de mensajes de registro | Intento"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expresiones regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExer"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Seguimiento de la pila-Wikipedia"  


> [!NOTE]
> <span data-ttu-id="ceaf4-316">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ceaf4-316">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ceaf4-317">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/log) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ceaf4-317">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ceaf4-319">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ceaf4-319">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
