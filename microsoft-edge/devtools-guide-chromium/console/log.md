---
description: Obtenga información sobre cómo registrar mensajes en la consola.
title: Introducción al registro de mensajes en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 96e3ad76fb86e32cf58abe6187fa0d6e75a2c00a
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125275"
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

# <span data-ttu-id="968d0-104">Introducción al registro de mensajes en la consola</span><span class="sxs-lookup"><span data-stu-id="968d0-104">Get Started With Logging Messages In The Console</span></span>  

<span data-ttu-id="968d0-105">Este tutorial interactivo le muestra cómo registrar y filtrar mensajes en la consola de [DevTools de Microsoft Edge][MicrosoftEdgeDevTools] .</span><span class="sxs-lookup"><span data-stu-id="968d0-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="968d0-107">Mensajes en la **consola**</span><span class="sxs-lookup"><span data-stu-id="968d0-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="968d0-108">Este tutorial está pensado para completarse en orden.</span><span class="sxs-lookup"><span data-stu-id="968d0-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="968d0-109">Se da por hecho que comprende los aspectos básicos del desarrollo web, como el uso de JavaScript para agregar interactividad a una página.</span><span class="sxs-lookup"><span data-stu-id="968d0-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <span data-ttu-id="968d0-110">Configurar la demostración y las DevTools</span><span class="sxs-lookup"><span data-stu-id="968d0-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="968d0-111">Este tutorial está diseñado para que puedas abrir la demostración y probar todos los flujos de trabajo tú mismo.</span><span class="sxs-lookup"><span data-stu-id="968d0-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="968d0-112">Cuando sigues físicamente, es más probable que recuerdes los flujos de trabajo más adelante.</span><span class="sxs-lookup"><span data-stu-id="968d0-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="968d0-113">Espera `Control` \ (Windows, Linux \) o `Command` \ (MacOS \) y elige **ejemplos de registro de consola** para abrirlos en una nueva pestaña.</span><span class="sxs-lookup"><span data-stu-id="968d0-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="968d0-114">Ejemplos del registro de consola</span><span class="sxs-lookup"><span data-stu-id="968d0-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="Mensajes en la consola" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="968d0-115">Centre la demostración y, a continuación, seleccione `Control` + `Shift` + `J` \ (Windows, Linux \) o `Command` + `Option` + `J` \ (MacOS \) para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="968d0-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="968d0-116">De forma predeterminada, DevTools se abre a la derecha de la demostración.</span><span class="sxs-lookup"><span data-stu-id="968d0-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="968d0-118">DevTools se abre a la derecha de la demostración</span><span class="sxs-lookup"><span data-stu-id="968d0-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="968d0-119">[Acople DevTools en la parte inferior de la ventana][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="968d0-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="968d0-121">DevTools acoplado a la parte inferior de la demostración</span><span class="sxs-lookup"><span data-stu-id="968d0-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="968d0-122">[Desacople DevTools en una ventana independiente][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="968d0-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="968d0-124">Explorador en una ventana independiente</span><span class="sxs-lookup"><span data-stu-id="968d0-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="968d0-125">[Desacople DevTools en una ventana independiente][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="968d0-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="968d0-127">DevTools desacoplado en una ventana independiente</span><span class="sxs-lookup"><span data-stu-id="968d0-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="968d0-128">Ver mensajes registrados desde JavaScript</span><span class="sxs-lookup"><span data-stu-id="968d0-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="968d0-129">La mayoría de los mensajes que ve en la consola provienen de los programadores web que escribieron el JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="968d0-129">Most messages that you see in the Console come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="968d0-130">El objetivo de esta sección es presentarle los diferentes tipos de mensajes que probablemente verá en la consola y explicar cómo puede registrar cada tipo de mensaje desde su propio JavaScript.</span><span class="sxs-lookup"><span data-stu-id="968d0-130">The goal of this section is to introduce you to the different message types that you are likely to see in the Console, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="968d0-131">Haga clic en el botón **información de registro** de la demostración.</span><span class="sxs-lookup"><span data-stu-id="968d0-131">Click the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="968d0-132">se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="968d0-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="968d0-134">La **consola** después de hacer clic en **información de registro**</span><span class="sxs-lookup"><span data-stu-id="968d0-134">The **Console** after clicking **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-135">Junto al `Hello, Console!` mensaje en la consola, elija **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="968d0-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="968d0-136">El panel orígenes se abre y resalta la línea de código que causó que el mensaje se registre en la consola.</span><span class="sxs-lookup"><span data-stu-id="968d0-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="968d0-137">El mensaje se registró cuando se ejecutó el JavaScript de la página `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="968d0-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="968d0-139">DevTools abre el panel **fuentes** después de hacer clic en</span><span class="sxs-lookup"><span data-stu-id="968d0-139">DevTools opens the **Sources** panel after you click</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-140">Vuelva a la **consola** con uno de los siguientes flujos de trabajo:</span><span class="sxs-lookup"><span data-stu-id="968d0-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="968d0-141">Haga clic en la pestaña **consola** .</span><span class="sxs-lookup"><span data-stu-id="968d0-141">Click the **Console** tab.</span></span>  
    *   <span data-ttu-id="968d0-142">Seleccione `Control` + `[` \ (Windows, Linux \) o `Command` + `[` \ (MacOS \) hasta que el panel de la consola esté en el foco.</span><span class="sxs-lookup"><span data-stu-id="968d0-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the Console panel is in focus.</span></span>  
    *   <span data-ttu-id="968d0-143">[Abra el menú de comandos][DevToolsCommandMenu], empiece `Console` a escribir, seleccione el comando **Mostrar panel de consola** y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="968d0-143">[Open the Command Menu][DevToolsCommandMenu], start typing `Console`, select the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="968d0-144">Haga clic en el botón **registrar ADVERTENCIA** de la demostración.</span><span class="sxs-lookup"><span data-stu-id="968d0-144">Click the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="968d0-145">se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="968d0-145">gets logged to the Console.</span></span>  <span data-ttu-id="968d0-146">Los mensajes con formato como este son advertencias.</span><span class="sxs-lookup"><span data-stu-id="968d0-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="968d0-148">La **consola** después de elegir **registrar ADVERTENCIA**</span><span class="sxs-lookup"><span data-stu-id="968d0-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="968d0-149">Si desea ver el código que causó un mensaje para que se registre de una determinada manera, haga clic en un script \ (como `log.js:12` \) para ver el código que causó el formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="968d0-149">If you want to see the code that caused a message to get logged a certain way, click on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="968d0-150">Haga clic en el icono **expandir** \ ( ![ expandir ][ImageExpandIcon] \) que hay delante de `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="968d0-150">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="968d0-151">DevTools muestra el [seguimiento][WikiStackTrace] de la pila que se dirige a la llamada.</span><span class="sxs-lookup"><span data-stu-id="968d0-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="968d0-153">Un seguimiento de pila</span><span class="sxs-lookup"><span data-stu-id="968d0-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="968d0-154">El seguimiento de la pila le indica que se ha llamado a una función llamada `logWarning` , que a su vez llamó a una función llamada `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="968d0-154">The stack trace is telling you that a function named `logWarning` was called, which in turn called a function named `quoteDante`.</span></span>  <span data-ttu-id="968d0-155">En otras palabras, la llamada que ocurrió en primer lugar se encuentra en la parte inferior del seguimiento de pila.</span><span class="sxs-lookup"><span data-stu-id="968d0-155">In other words, the call that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="968d0-156">Puedes registrar los seguimientos de la pila en cualquier momento llamando a `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="968d0-156">You may log stack traces at any time by calling `console.trace()`.</span></span>  

1.  <span data-ttu-id="968d0-157">Elija **registrar error**.</span><span class="sxs-lookup"><span data-stu-id="968d0-157">Choose **Log Error**.</span></span>  <span data-ttu-id="968d0-158">Se ha registrado el siguiente mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="968d0-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="968d0-160">Un mensaje de error</span><span class="sxs-lookup"><span data-stu-id="968d0-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-161">Elija **tabla de registro**.</span><span class="sxs-lookup"><span data-stu-id="968d0-161">Choose **Log Table**.</span></span>  <span data-ttu-id="968d0-162">Se graba en la consola una tabla sobre artistas famosos.</span><span class="sxs-lookup"><span data-stu-id="968d0-162">A table about famous artists gets logged to the Console.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="968d0-163">La `birthday` columna solo se rellena para una fila.</span><span class="sxs-lookup"><span data-stu-id="968d0-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="968d0-164">Revise el código para determinar el motivo.</span><span class="sxs-lookup"><span data-stu-id="968d0-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="968d0-166">Una tabla en la **consola**</span><span class="sxs-lookup"><span data-stu-id="968d0-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-167">Elija **grupo de registro**.</span><span class="sxs-lookup"><span data-stu-id="968d0-167">Choose **Log Group**.</span></span>  <span data-ttu-id="968d0-168">Los nombres de las cuatro tortugas famosas y de lucha contra delitos se agrupan debajo de la `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="968d0-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="968d0-170">Un grupo de mensajes en la **consola**</span><span class="sxs-lookup"><span data-stu-id="968d0-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-171">Elija **registro personalizado**.</span><span class="sxs-lookup"><span data-stu-id="968d0-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="968d0-172">Se graba en la consola un mensaje con un borde rojo y un fondo azul.</span><span class="sxs-lookup"><span data-stu-id="968d0-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="968d0-174">Un mensaje con formato personalizado en la **consola**</span><span class="sxs-lookup"><span data-stu-id="968d0-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="968d0-175">La idea principal es que cuando quieras registrar mensajes en la consola desde tu código JavaScript, usas uno de los `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="968d0-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="968d0-176">Cada método da formato a los mensajes de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="968d0-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="968d0-177">Hay aún más métodos de los que se han demostrado en esta sección.</span><span class="sxs-lookup"><span data-stu-id="968d0-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="968d0-178">En este tutorial se muestra cómo explorar el resto de los métodos.</span><span class="sxs-lookup"><span data-stu-id="968d0-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <span data-ttu-id="968d0-179">Ver los mensajes registrados por el explorador</span><span class="sxs-lookup"><span data-stu-id="968d0-179">View messages logged by the browser</span></span>  

<span data-ttu-id="968d0-180">El explorador también registra mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="968d0-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="968d0-181">Esto suele ocurrir cuando hay un problema con la página.</span><span class="sxs-lookup"><span data-stu-id="968d0-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="968d0-182">Elija **causa 404**.</span><span class="sxs-lookup"><span data-stu-id="968d0-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="968d0-183">El explorador registra un código de Estado HTTP de `404` error de red porque el JavaScript de la página ha intentado buscar un archivo que no existe.</span><span class="sxs-lookup"><span data-stu-id="968d0-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="968d0-185">`404`Error en la **consola**</span><span class="sxs-lookup"><span data-stu-id="968d0-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-186">Elija **causar un error**.</span><span class="sxs-lookup"><span data-stu-id="968d0-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="968d0-187">El explorador registra una no capturada `TypeError` porque el JavaScript está intentando actualizar un nodo Dom que no existe.</span><span class="sxs-lookup"><span data-stu-id="968d0-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="968d0-189">A `TypeError` en la **consola**</span><span class="sxs-lookup"><span data-stu-id="968d0-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-190">Haga clic en la lista desplegable **niveles de registro** y habilite la opción **detallado** si está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="968d0-190">Click the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="968d0-191">Para obtener más información sobre el filtrado, vaya a la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="968d0-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="968d0-192">Tiene que hacer esto para asegurarse de que el siguiente mensaje que inicie sesión está visible.</span><span class="sxs-lookup"><span data-stu-id="968d0-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="968d0-193">Si la lista desplegable niveles predeterminados está deshabilitado, es posible que tenga que cerrar la barra lateral de la **consola** .</span><span class="sxs-lookup"><span data-stu-id="968d0-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="968d0-194">Filtrar por origen del mensaje a continuación para obtener más información sobre la barra lateral de la **consola** .</span><span class="sxs-lookup"><span data-stu-id="968d0-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="968d0-196">Habilitar el nivel de registro detallado</span><span class="sxs-lookup"><span data-stu-id="968d0-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-197">Elija **causar infracción**.</span><span class="sxs-lookup"><span data-stu-id="968d0-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="968d0-198">La página deja de responder durante unos segundos y, a continuación, el explorador registra el mensaje `[Violation] 'click' handler took 3000ms` en la consola.</span><span class="sxs-lookup"><span data-stu-id="968d0-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="968d0-199">La duración exacta puede variar.</span><span class="sxs-lookup"><span data-stu-id="968d0-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="968d0-201">Violación en la **consola**</span><span class="sxs-lookup"><span data-stu-id="968d0-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="968d0-202">Filtrar mensajes</span><span class="sxs-lookup"><span data-stu-id="968d0-202">Filter messages</span></span>  

<span data-ttu-id="968d0-203">En algunas páginas verás que la consola está inundada de mensajes.</span><span class="sxs-lookup"><span data-stu-id="968d0-203">On some pages you see the Console get flooded with messages.</span></span>  <span data-ttu-id="968d0-204">DevTools proporciona varias formas diferentes de filtrar los mensajes que no son relevantes para la tarea que está realizando.</span><span class="sxs-lookup"><span data-stu-id="968d0-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <span data-ttu-id="968d0-205">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="968d0-205">Filter by log level</span></span>  

<span data-ttu-id="968d0-206">`console`A cada método se le asigna un nivel de gravedad: `Verbose` ,, `Info` `Warning` o `Error` .</span><span class="sxs-lookup"><span data-stu-id="968d0-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="968d0-207">Por ejemplo, `console.log()` es un `Info` mensaje de nivel, mientras que `console.error()` es `Error` un mensaje de nivel.</span><span class="sxs-lookup"><span data-stu-id="968d0-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="968d0-208">Haga clic en la lista desplegable **niveles de registro** y deshabilite **errores**.</span><span class="sxs-lookup"><span data-stu-id="968d0-208">Click the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="968d0-209">Un nivel se deshabilita cuando ya no hay una marca de verificación junto a él.</span><span class="sxs-lookup"><span data-stu-id="968d0-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="968d0-210">Los `Error` mensajes de nivel desaparecen.</span><span class="sxs-lookup"><span data-stu-id="968d0-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="968d0-212">Deshabilitar mensajes de nivel de error en la **consola**</span><span class="sxs-lookup"><span data-stu-id="968d0-212">Disabling Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-213">Vuelva a hacer clic en la lista desplegable **niveles de registro** y vuelva a habilitar los **errores**.</span><span class="sxs-lookup"><span data-stu-id="968d0-213">Click the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="968d0-214">Los `Error` mensajes del nivel volverán a aparecer.</span><span class="sxs-lookup"><span data-stu-id="968d0-214">The `Error`-level messages reappear.</span></span>  

### <span data-ttu-id="968d0-215">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="968d0-215">Filter by text</span></span>  

<span data-ttu-id="968d0-216">Cuando desee ver solo los mensajes que incluyan una cadena exacta, escríbala en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="968d0-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="968d0-217">Escriba `Dave` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="968d0-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="968d0-218">Todos los mensajes que no incluyan la cadena `Dave` están ocultos.</span><span class="sxs-lookup"><span data-stu-id="968d0-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="968d0-219">También puede ver la `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="968d0-219">You might also see the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="968d0-220">Es un error.</span><span class="sxs-lookup"><span data-stu-id="968d0-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="968d0-222">Filtrar cualquier mensaje que no incluya</span><span class="sxs-lookup"><span data-stu-id="968d0-222">Filtering out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-223">Eliminar `Dave` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="968d0-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="968d0-224">Todos los mensajes volverán a aparecer.</span><span class="sxs-lookup"><span data-stu-id="968d0-224">All the messages reappear.</span></span>  

### <span data-ttu-id="968d0-225">Filtrar por expresión regular</span><span class="sxs-lookup"><span data-stu-id="968d0-225">Filter by regular expression</span></span>  

<span data-ttu-id="968d0-226">Cuando desee mostrar todos los mensajes que incluyan un patrón de texto, en lugar de una cadena específica, use una [expresión regular][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="968d0-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="968d0-227">Escriba `/^[AH]/` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="968d0-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="968d0-228">Escriba este patrón en [Regex][|::ref1::|Main] para obtener una explicación de lo que está haciendo.</span><span class="sxs-lookup"><span data-stu-id="968d0-228">Type this pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="968d0-230">Filtrar los mensajes que no coincidan con el patrón</span><span class="sxs-lookup"><span data-stu-id="968d0-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-231">Eliminar `/^[AH]/` en el cuadro de texto **filtro** .</span><span class="sxs-lookup"><span data-stu-id="968d0-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="968d0-232">Todos los mensajes volverán a verse.</span><span class="sxs-lookup"><span data-stu-id="968d0-232">All messages are visible again.</span></span>  

### <span data-ttu-id="968d0-233">Filtrar por origen del mensaje</span><span class="sxs-lookup"><span data-stu-id="968d0-233">Filter by message source</span></span>  

<span data-ttu-id="968d0-234">Si desea ver solo los mensajes procedentes de una dirección URL determinada, use la **barra lateral**.</span><span class="sxs-lookup"><span data-stu-id="968d0-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="968d0-235">Elija **Mostrar la barra lateral de consola** \ ( ![ Mostrar barra lateral de consola ][ImageShowConsoleSidebarIcon] \).</span><span class="sxs-lookup"><span data-stu-id="968d0-235">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="968d0-237">La barra lateral</span><span class="sxs-lookup"><span data-stu-id="968d0-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-238">Haga clic en el icono **expandir** \ ( ![ expandir ][ImageExpandIcon] \) junto al número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="968d0-238">Click the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="968d0-239">En la siguiente ilustración, el número de mensajes se indica como **13 mensajes**.</span><span class="sxs-lookup"><span data-stu-id="968d0-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="968d0-240">La **barra lateral** muestra una lista de las direcciones URL que han provocado el registro de mensajes.</span><span class="sxs-lookup"><span data-stu-id="968d0-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="968d0-241">Por ejemplo, se `log.js` produjeron 11 mensajes.</span><span class="sxs-lookup"><span data-stu-id="968d0-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="968d0-243">Ver el origen de los mensajes en la barra lateral</span><span class="sxs-lookup"><span data-stu-id="968d0-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="968d0-244">Filtrar por mensajes de usuario</span><span class="sxs-lookup"><span data-stu-id="968d0-244">Filter by user messages</span></span>  

<span data-ttu-id="968d0-245">Anteriormente, cuando se hace clic en **información de registro**, se llama a un script para `console.log('Hello, Console!')` registrar el mensaje en la consola.</span><span class="sxs-lookup"><span data-stu-id="968d0-245">Earlier, when you clicked **Log Info**, a script called `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="968d0-246">Los mensajes registrados de JavaScript como este se denominan **mensajes de usuario**.</span><span class="sxs-lookup"><span data-stu-id="968d0-246">Messages logged from JavaScript like this are called **user messages**.</span></span>  <span data-ttu-id="968d0-247">Por el contrario, cuando hace clic en la **causa 404**, el explorador registra un `Error` mensaje que indica que no se pudo encontrar el recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="968d0-247">In contrast, when you clicked **Cause 404**, the browser logged an `Error`-level message stating that the requested resource could not be found.</span></span>  <span data-ttu-id="968d0-248">Mensajes como los que se consideran **mensajes del explorador**.</span><span class="sxs-lookup"><span data-stu-id="968d0-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="968d0-249">Use la **barra lateral** para filtrar los mensajes del explorador y mostrar solo los mensajes de usuario.</span><span class="sxs-lookup"><span data-stu-id="968d0-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="968d0-250">Elija **9 mensajes de usuario**.</span><span class="sxs-lookup"><span data-stu-id="968d0-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="968d0-251">Los mensajes del explorador están ocultos.</span><span class="sxs-lookup"><span data-stu-id="968d0-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="968d0-253">Filtrar los mensajes del explorador</span><span class="sxs-lookup"><span data-stu-id="968d0-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="968d0-254">Elija **13 mensajes** para volver a mostrar todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="968d0-254">Choose **13 Messages** to show all messages again.</span></span>  

## <span data-ttu-id="968d0-255">Usar la consola junto con cualquier otro panel</span><span class="sxs-lookup"><span data-stu-id="968d0-255">Use the Console alongside any other panel</span></span>  

<span data-ttu-id="968d0-256">¿Qué sucede si está editando estilos, pero necesita consultar rápidamente el registro de consola para buscar algo?</span><span class="sxs-lookup"><span data-stu-id="968d0-256">What if you are editing styles, but you need to quickly check the Console log for something?</span></span>  <span data-ttu-id="968d0-257">Use el cajón.</span><span class="sxs-lookup"><span data-stu-id="968d0-257">Use the Drawer.</span></span>  

1.  <span data-ttu-id="968d0-258">Haga clic en la pestaña **elementos** .</span><span class="sxs-lookup"><span data-stu-id="968d0-258">Click the **Elements** tab.</span></span>  
1.  <span data-ttu-id="968d0-259">Seleccione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="968d0-259">Select `Escape`.</span></span>  <span data-ttu-id="968d0-260">Se abrirá la ficha **Console** del **cajón** .</span><span class="sxs-lookup"><span data-stu-id="968d0-260">The **Console** tab of the **Drawer** opens.</span></span>  <span data-ttu-id="968d0-261">Tiene todas las características del panel de la consola que ha estado usando en este tutorial.</span><span class="sxs-lookup"><span data-stu-id="968d0-261">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="968d0-263">Ficha de **consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="968d0-263">The **Console** tab in the **Drawer**</span></span>  
    :::image-end:::  
    
<!--## Next steps  -->

<!--
*   See [Console Reference][DevToolsConsoleApi] to explore more features and workflows related to the Console UI.
*   See [Console API Reference][DevToolsConsoleReference] to learn more about all of the `console` methods that were demonstrated in [View messages logged from JavaScript(#view-messages-logged-from-javascript) and explore the other `console` methods that were not covered in this tutorial.  
*   See [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  

## <span data-ttu-id="968d0-264">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="968d0-264">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Herramientas de desarrollador de Microsoft Edge \ (cromo \) | Microsoft docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de DevTools de Microsoft Edge | Microsoft docs"  
[DevToolsConsoleApi]: ./api.md "Referencia de la API de consola | Microsoft docs"  
[DevToolsConsoleReference]: ./reference.md "Referencia de consola | Microsoft docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introducción a la creación de mensajes de registro | Intento"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expresiones regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExer"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Seguimiento de la pila-Wikipedia"  
> [!NOTE]
> <span data-ttu-id="968d0-274">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="968d0-274">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="968d0-275">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/log) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="968d0-275">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="968d0-277">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="968d0-277">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
