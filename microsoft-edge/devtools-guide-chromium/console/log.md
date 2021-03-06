---
description: Obtenga información sobre cómo registrar mensajes en la consola.
title: Introducción al registro de mensajes en la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e2ea1a8327dd2a591e067b69198c4509b2abcb2d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399172"
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

# <a name="get-started-with-logging-messages-in-the-console"></a><span data-ttu-id="b9563-104">Introducción al registro de mensajes en la consola</span><span class="sxs-lookup"><span data-stu-id="b9563-104">Get started with logging messages in the Console</span></span>  

<span data-ttu-id="b9563-105">En este tutorial interactivo se muestra cómo registrar y filtrar mensajes en la [consola de Microsoft Edge DevTools.][MicrosoftEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="b9563-105">This interactive tutorial shows you how to log and filter messages in the [Microsoft Edge DevTools][MicrosoftEdgeDevTools] console.</span></span>  

:::image type="complex" source="../media/console-ars-technica-console-onload.msft.png" alt-text="Mensajes en la consola" lightbox="../media/console-ars-technica-console-onload.msft.png":::
   <span data-ttu-id="b9563-107">Mensajes en la **consola**</span><span class="sxs-lookup"><span data-stu-id="b9563-107">Messages in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="b9563-108">Este tutorial está pensado para completarse en orden.</span><span class="sxs-lookup"><span data-stu-id="b9563-108">This tutorial is intended to be completed in order.</span></span>  <span data-ttu-id="b9563-109">Se supone que comprende los conceptos básicos del desarrollo web, como cómo usar JavaScript para agregar interactividad a una página.</span><span class="sxs-lookup"><span data-stu-id="b9563-109">It assumes that you understand the fundamentals of web development, such as how to use JavaScript to add interactivity to a page.</span></span>  

## <a name="set-up-the-demo-and-devtools"></a><span data-ttu-id="b9563-110">Configurar la demostración y DevTools</span><span class="sxs-lookup"><span data-stu-id="b9563-110">Set up the demo and DevTools</span></span>  

<span data-ttu-id="b9563-111">Este tutorial está diseñado para que pueda abrir la demostración y probar todos los flujos de trabajo usted mismo.</span><span class="sxs-lookup"><span data-stu-id="b9563-111">This tutorial is designed so that you are able to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="b9563-112">Cuando se sigue físicamente, es más probable que recuerde los flujos de trabajo más adelante.</span><span class="sxs-lookup"><span data-stu-id="b9563-112">When you physically follow along, you are more likely to remember the workflows later.</span></span>  

1.  <span data-ttu-id="b9563-113">Mantenga `Control` presionado \(Windows, Linux\) o `Command` \(macOS\) y elija **Ejemplos** de registro de consola para abrir en una nueva pestaña.</span><span class="sxs-lookup"><span data-stu-id="b9563-113">Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **Console Log Examples** to open in a new tab.</span></span>  
    
    [<span data-ttu-id="b9563-114">Ejemplos de registro de consola</span><span class="sxs-lookup"><span data-stu-id="b9563-114">Console Log Examples</span></span>][GlitchDevToolsConsoleLogExamples]
    
    <!--
    > [!TIP]
    > Move the demo to a separate window.  
    > 
    > :::image type="complex" source="../media/log-set-up-1.msft.png" alt-text="The tutorial on the left, and the demo on the right" lightbox="../media/log-set-up-1.msft.png":::
    >    The tutorial on the left, and the demo on the right  
    > :::image-end:::  
    -->
    
1.  <span data-ttu-id="b9563-115">Centra la demostración y, a `Control` + `Shift` + `J` continuación, selecciona \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\) para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="b9563-115">Focus the demo and then select `Control`+`Shift`+`J` \(Windows, Linux\) or `Command`+`Option`+`J` \(macOS\) to open DevTools.</span></span>  <span data-ttu-id="b9563-116">De forma predeterminada, DevTools se abre a la derecha de la demostración.</span><span class="sxs-lookup"><span data-stu-id="b9563-116">By default DevTools opens to the right of the demo.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/console-example-devtools-right-console.msft.png" alt-text="DevTools se abre a la derecha de la demostración" lightbox="../media/console-example-devtools-right-console.msft.png":::
             <span data-ttu-id="b9563-118">DevTools se abre a la derecha de la demostración</span><span class="sxs-lookup"><span data-stu-id="b9563-118">DevTools opens to the right of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="b9563-119">[Dock DevTools en la parte inferior de la ventana][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="b9563-119">[Dock DevTools to the bottom of the window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-bottom-console.msft.png" alt-text="DevTools acoplada a la parte inferior de la demostración" lightbox="../media/console-example-devtools-bottom-console.msft.png":::
             <span data-ttu-id="b9563-121">DevTools acoplada a la parte inferior de la demostración</span><span class="sxs-lookup"><span data-stu-id="b9563-121">DevTools docked to the bottom of the demo</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="b9563-122">[Desacoplar DevTools en una ventana independiente.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="b9563-122">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-browse.msft.png" alt-text="Explorador en una ventana independiente" lightbox="../media/console-example-devtools-separate-console-browse.msft.png":::
             <span data-ttu-id="b9563-124">Explorador en una ventana independiente</span><span class="sxs-lookup"><span data-stu-id="b9563-124">Browser in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          > [!TIP]
          > <span data-ttu-id="b9563-125">[Desacoplar DevTools en una ventana independiente.][DevToolsCustomizePlacement]</span><span class="sxs-lookup"><span data-stu-id="b9563-125">[Undock DevTools into a separate window][DevToolsCustomizePlacement].</span></span>  
          
          :::image type="complex" source="../media/console-example-devtools-separate-console-devtools.msft.png" alt-text="DevTools desacoplada en una ventana independiente" lightbox="../media/console-example-devtools-separate-console-devtools.msft.png":::
             <span data-ttu-id="b9563-127">DevTools desacoplada en una ventana independiente</span><span class="sxs-lookup"><span data-stu-id="b9563-127">DevTools undocked in a separate window</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="view-messages-logged-from-javascript"></a><span data-ttu-id="b9563-128">Ver mensajes registrados desde JavaScript</span><span class="sxs-lookup"><span data-stu-id="b9563-128">View messages logged from JavaScript</span></span>  

<span data-ttu-id="b9563-129">La mayoría de los mensajes que se muestran en la **consola** provienen de los desarrolladores web que escribieron el JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="b9563-129">Most messages that are displayed in the **Console** come from the web developers who wrote the JavaScript of the page.</span></span>  <span data-ttu-id="b9563-130">El objetivo de esta sección es presentarle los diferentes tipos de \*\*\*\* mensajes que probablemente revise en la consola y explicar cómo puede registrar cada tipo de mensaje usted mismo desde su propio JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b9563-130">The goal of this section is to introduce you to the different message types that you are likely to review in the **Console**, and explain how you may log each message type yourself from your own JavaScript.</span></span>  

1.  <span data-ttu-id="b9563-131">Elija el **botón Información de** registro en la demostración.</span><span class="sxs-lookup"><span data-stu-id="b9563-131">Choose the **Log Info** button in the demo.</span></span>  `Hello, Console!` <span data-ttu-id="b9563-132">se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="b9563-132">gets logged to the Console.</span></span>
    
    :::image type="complex" source="../media/console-log-info.msft.png" alt-text="La consola después de elegir Información de registro" lightbox="../media/console-log-info.msft.png":::
       <span data-ttu-id="b9563-134">La **consola** después de elegir Información **de registro**</span><span class="sxs-lookup"><span data-stu-id="b9563-134">The **Console** after you choose **Log Info**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-135">Junto al `Hello, Console!` mensaje de la consola, elija **log.js:2**.</span><span class="sxs-lookup"><span data-stu-id="b9563-135">Next to the `Hello, Console!` message in the Console choose **log.js:2**.</span></span>  <span data-ttu-id="b9563-136">El panel Orígenes se abre y resalta la línea de código que hizo que el mensaje se registrara en la consola.</span><span class="sxs-lookup"><span data-stu-id="b9563-136">The Sources panel opens and highlights the line of code that caused the message to get logged to the Console.</span></span>  <span data-ttu-id="b9563-137">El mensaje se registró cuando se ejecutó el JavaScript de la página `console.log('Hello, Console!')` .</span><span class="sxs-lookup"><span data-stu-id="b9563-137">The message was logged when the JavaScript of the page ran `console.log('Hello, Console!')`.</span></span>
    
    :::image type="complex" source="../media/console-sources-logjs.msft.png" alt-text="DevTools abre la herramienta Orígenes después de elegir log.js:2" lightbox="../media/console-sources-logjs.msft.png":::
       <span data-ttu-id="b9563-139">DevTools abre la **herramienta Orígenes** después de elegir</span><span class="sxs-lookup"><span data-stu-id="b9563-139">DevTools opens the **Sources** tool after you choose</span></span> `log.js:2`  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-140">Vuelva a la **consola con** cualquiera de los siguientes flujos de trabajo:</span><span class="sxs-lookup"><span data-stu-id="b9563-140">Navigate back to the **Console** using any of the following workflows:</span></span>  
    
    *   <span data-ttu-id="b9563-141">Elija la **herramienta Consola.**</span><span class="sxs-lookup"><span data-stu-id="b9563-141">Choose the **Console** tool.</span></span>  
    *   <span data-ttu-id="b9563-142">Seleccione `Control` + `[` \(Windows, Linux\) o `Command` + `[` \(macOS\) hasta que la **herramienta** Consola esté en el foco.</span><span class="sxs-lookup"><span data-stu-id="b9563-142">Select `Control`+`[` \(Windows, Linux\) or `Command`+`[` \(macOS\) until the **Console** tool is in focus.</span></span>  
    *   <span data-ttu-id="b9563-143">[Abra el menú comando][DevToolsCommandMenu], escriba , elija el comando `Console` Mostrar panel de **consola** y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b9563-143">[Open the Command Menu][DevToolsCommandMenu], type `Console`, choose the **Show Console Panel** command, and then select `Enter`.</span></span>  
    
1.  <span data-ttu-id="b9563-144">Elija el **botón Advertencia de** registro en la demostración.</span><span class="sxs-lookup"><span data-stu-id="b9563-144">Choose the **Log Warning** button in the demo.</span></span>  `Abandon Hope All Ye Who Enter` <span data-ttu-id="b9563-145">se registra en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="b9563-145">gets logged to the **Console**.</span></span>  <span data-ttu-id="b9563-146">Los mensajes con este formato son advertencias.</span><span class="sxs-lookup"><span data-stu-id="b9563-146">Messages formatted like this are warnings.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning.msft.png" alt-text="La consola después de elegir Advertencia de registro" lightbox="../media/console-log-warning.msft.png":::
       <span data-ttu-id="b9563-148">La **consola** después de elegir Advertencia **de registro**</span><span class="sxs-lookup"><span data-stu-id="b9563-148">The **Console** after you choose **Log Warning**</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="b9563-149">Si desea mostrar el código que provocó que un mensaje se registrara de una forma determinada, elija un script \(como \) para ver el código que hizo que el mensaje se aplicara `log.js:12` formato.</span><span class="sxs-lookup"><span data-stu-id="b9563-149">If you want to display the code that caused a message to get logged a certain way, choose on a script \(such as `log.js:12`\) to view the code that caused the message to get formatted.</span></span>  

1.  <span data-ttu-id="b9563-150">Elija el **icono Expandir** \( ![ Expandir ][ImageExpandIcon] \) delante de `Abandon Hope All Ye Who Enter` .</span><span class="sxs-lookup"><span data-stu-id="b9563-150">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon in front of `Abandon Hope All Ye Who Enter`.</span></span>  <span data-ttu-id="b9563-151">DevTools muestra el [seguimiento de la pila][WikiStackTrace] que conduce a la llamada.</span><span class="sxs-lookup"><span data-stu-id="b9563-151">DevTools shows the [stack trace][WikiStackTrace] leading up to the call.</span></span>  
    
    :::image type="complex" source="../media/console-log-warning-expanded.msft.png" alt-text="Seguimiento de una pila" lightbox="../media/console-log-warning-expanded.msft.png":::
       <span data-ttu-id="b9563-153">Seguimiento de una pila</span><span class="sxs-lookup"><span data-stu-id="b9563-153">A stack trace</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="b9563-154">El seguimiento de la pila le está diciendo que se ejecuta una función denominada , que a su vez `logWarning` ejecuta una función denominada `quoteDante` .</span><span class="sxs-lookup"><span data-stu-id="b9563-154">The stack trace is telling you that a function named `logWarning` is run, which in turn runs a function named `quoteDante`.</span></span>  <span data-ttu-id="b9563-155">En otras palabras, la solicitud que se ha producido primero se encuentra en la parte inferior del seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="b9563-155">In other words, the request that happened first is at the bottom of the stack trace.</span></span>  <span data-ttu-id="b9563-156">Puede registrar los seguimientos de la pila en cualquier momento ejecutando `console.trace()` .</span><span class="sxs-lookup"><span data-stu-id="b9563-156">You may log stack traces at any time by running `console.trace()`.</span></span>  

1.  <span data-ttu-id="b9563-157">Elija **Error de registro**.</span><span class="sxs-lookup"><span data-stu-id="b9563-157">Choose **Log Error**.</span></span>  <span data-ttu-id="b9563-158">Se registra el siguiente mensaje de error:</span><span class="sxs-lookup"><span data-stu-id="b9563-158">The following error message gets logged:</span></span> `I'm sorry, Dave.  I'm afraid I can't do that.`  
    
    :::image type="complex" source="../media/console-log-error.msft.png" alt-text="Un mensaje de error" lightbox="../media/console-log-error.msft.png":::
       <span data-ttu-id="b9563-160">Un mensaje de error</span><span class="sxs-lookup"><span data-stu-id="b9563-160">An error message</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-161">Elija **Tabla de registro**.</span><span class="sxs-lookup"><span data-stu-id="b9563-161">Choose **Log Table**.</span></span>  <span data-ttu-id="b9563-162">Una tabla sobre los artistas famosos se registra en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="b9563-162">A table about famous artists gets logged to the **Console**.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b9563-163">La `birthday` columna solo se rellena para una fila.</span><span class="sxs-lookup"><span data-stu-id="b9563-163">The `birthday` column is only populated for one row.</span></span>  <span data-ttu-id="b9563-164">Revise el código para determinar por qué es.</span><span class="sxs-lookup"><span data-stu-id="b9563-164">Review the code to determine why that is.</span></span>
    
    :::image type="complex" source="../media/console-log-table.msft.png" alt-text="Una tabla en la consola" lightbox="../media/console-log-table.msft.png":::
       <span data-ttu-id="b9563-166">Una tabla en la **consola**</span><span class="sxs-lookup"><span data-stu-id="b9563-166">A table in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-167">Elija **Grupo de registros**.</span><span class="sxs-lookup"><span data-stu-id="b9563-167">Choose **Log Group**.</span></span>  <span data-ttu-id="b9563-168">Los nombres de 4 tortugas conocidas que luchan contra el crimen se agrupan bajo la `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b9563-168">The names of 4 famous, crime-fighting turtles are grouped under the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  
    
    :::image type="complex" source="../media/console-log-group.msft.png" alt-text="Un grupo de mensajes en la consola" lightbox="../media/console-log-group.msft.png":::
       <span data-ttu-id="b9563-170">Un grupo de mensajes en la **consola**</span><span class="sxs-lookup"><span data-stu-id="b9563-170">A group of messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-171">Elija **Registro personalizado**.</span><span class="sxs-lookup"><span data-stu-id="b9563-171">Choose **Log Custom**.</span></span>  <span data-ttu-id="b9563-172">Un mensaje con un borde rojo y un fondo azul se registra en la consola.</span><span class="sxs-lookup"><span data-stu-id="b9563-172">A message with a red border and blue background gets logged to the Console.</span></span>  
    
    :::image type="complex" source="../media/console-log-custom.msft.png" alt-text="Un mensaje con formato personalizado en la consola" lightbox="../media/console-log-custom.msft.png":::
       <span data-ttu-id="b9563-174">Un mensaje con formato personalizado en la **consola**</span><span class="sxs-lookup"><span data-stu-id="b9563-174">A message with custom formatting in the **Console**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="b9563-175">La idea principal aquí es que cuando quiera registrar mensajes en la consola desde JavaScript, use uno de los `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="b9563-175">The main idea here is that when you want to log messages to the Console from your JavaScript, you use one of the `console` methods.</span></span>  <span data-ttu-id="b9563-176">Cada método da formato a los mensajes de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="b9563-176">Each method formats messages differently.</span></span>  

<span data-ttu-id="b9563-177">Hay incluso más métodos de los que se han demostrado en esta sección.</span><span class="sxs-lookup"><span data-stu-id="b9563-177">There are even more methods than what has been demonstrated in this section.</span></span>  <span data-ttu-id="b9563-178">En este tutorial se muestra cómo explorar el resto de los métodos.</span><span class="sxs-lookup"><span data-stu-id="b9563-178">This tutorial shows you how to explore the rest of the methods.</span></span>  

## <a name="view-messages-logged-by-the-browser"></a><span data-ttu-id="b9563-179">Ver mensajes registrados por el explorador</span><span class="sxs-lookup"><span data-stu-id="b9563-179">View messages logged by the browser</span></span>  

<span data-ttu-id="b9563-180">El explorador también registra los mensajes en la consola.</span><span class="sxs-lookup"><span data-stu-id="b9563-180">The browser logs messages to the Console, too.</span></span>  <span data-ttu-id="b9563-181">Esto suele ocurrir cuando hay un problema con la página.</span><span class="sxs-lookup"><span data-stu-id="b9563-181">This usually happens when there is a problem with the page.</span></span>  

1.  <span data-ttu-id="b9563-182">Elija **Causa 404**.</span><span class="sxs-lookup"><span data-stu-id="b9563-182">Choose **Cause 404**.</span></span>  <span data-ttu-id="b9563-183">El explorador registra un código de estado HTTP de error de red porque javascript de la página intentó capturar `404` un archivo que no existe.</span><span class="sxs-lookup"><span data-stu-id="b9563-183">The browser logs an HTTP status code of `404` network error because the JavaScript of the page tried to fetch a file that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-404.msft.png" alt-text="Error 404 en la consola" lightbox="../media/console-cause-404.msft.png":::
       <span data-ttu-id="b9563-185">Error `404` en la **consola**</span><span class="sxs-lookup"><span data-stu-id="b9563-185">A `404` error in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-186">Elija **Causar error**.</span><span class="sxs-lookup"><span data-stu-id="b9563-186">Choose **Cause Error**.</span></span>  <span data-ttu-id="b9563-187">El explorador registra un error porque JavaScript está intentando actualizar un nodo `TypeError` DOM que no existe.</span><span class="sxs-lookup"><span data-stu-id="b9563-187">The browser logs an uncaught `TypeError` because the JavaScript is trying to update a DOM node that does not exist.</span></span>  
    
    :::image type="complex" source="../media/console-cause-error.msft.png" alt-text="TypeError en la consola" lightbox="../media/console-cause-error.msft.png":::
       <span data-ttu-id="b9563-189">A `TypeError` en la **consola**</span><span class="sxs-lookup"><span data-stu-id="b9563-189">A `TypeError` in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-190">Elija el **desplegable Niveles de registro** y habilite la opción **Detallado** si está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="b9563-190">Choose the **Log Levels** dropdown and enable the **Verbose** option if it is disabled.</span></span>  <span data-ttu-id="b9563-191">Obtenga más información sobre el filtrado en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="b9563-191">You learn more about filtering in the next section.</span></span>  <span data-ttu-id="b9563-192">Debe hacer esto para asegurarse de que el siguiente mensaje que inicie sesión esté visible.</span><span class="sxs-lookup"><span data-stu-id="b9563-192">You need to do this to make sure that the next message you log is visible.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="b9563-193">Si el desplegable Niveles predeterminados está deshabilitado, es posible que deba cerrar la barra lateral **de la** consola.</span><span class="sxs-lookup"><span data-stu-id="b9563-193">If the Default Levels dropdown is disabled, you may need to close the **Console** Sidebar.</span></span>  <span data-ttu-id="b9563-194">Filtra por origen de mensaje a continuación para obtener más información acerca de la **barra lateral de** la consola.</span><span class="sxs-lookup"><span data-stu-id="b9563-194">Filter by Message Source below for more information about the **Console** Sidebar.</span></span>
    
    :::image type="complex" source="../media/console-cause-error-log-levels.msft.png" alt-text="Habilitar el nivel de registro detallado" lightbox="../media/console-cause-error-log-levels.msft.png":::
       <span data-ttu-id="b9563-196">Habilitar el nivel de registro detallado</span><span class="sxs-lookup"><span data-stu-id="b9563-196">Enabling the Verbose log level</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-197">Elija **Causa infracción**.</span><span class="sxs-lookup"><span data-stu-id="b9563-197">Choose **Cause Violation**.</span></span>  <span data-ttu-id="b9563-198">La página deja de responder durante unos segundos y, a continuación, el explorador registra el mensaje `[Violation] 'click' handler took 3000ms` en la consola.</span><span class="sxs-lookup"><span data-stu-id="b9563-198">The page becomes unresponsive for a few seconds and then the browser logs the message `[Violation] 'click' handler took 3000ms` to the Console.</span></span>  <span data-ttu-id="b9563-199">La duración exacta puede variar.</span><span class="sxs-lookup"><span data-stu-id="b9563-199">The exact duration may vary.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation.msft.png" alt-text="Una infracción en la consola" lightbox="../media/console-cause-violation.msft.png":::
       <span data-ttu-id="b9563-201">Una infracción en la **consola**</span><span class="sxs-lookup"><span data-stu-id="b9563-201">A violation in the **Console**</span></span>  
    :::image-end:::  
    
## <a name="filter-messages"></a><span data-ttu-id="b9563-202">Filtrar mensajes</span><span class="sxs-lookup"><span data-stu-id="b9563-202">Filter messages</span></span>  

<span data-ttu-id="b9563-203">En algunas páginas web se revisa que **la consola** se inunda de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b9563-203">On some webpages you review the **Console** get flooded with messages.</span></span>  <span data-ttu-id="b9563-204">DevTools proporciona muchas formas diferentes de filtrar los mensajes que no son relevantes para la tarea que se está haciendo.</span><span class="sxs-lookup"><span data-stu-id="b9563-204">DevTools provides many different ways to filter out messages that are not relevant to the task at hand.</span></span>  

### <a name="filter-by-log-level"></a><span data-ttu-id="b9563-205">Filtrar por nivel de registro</span><span class="sxs-lookup"><span data-stu-id="b9563-205">Filter by log level</span></span>  

<span data-ttu-id="b9563-206">A `console` cada método se le asigna un nivel de gravedad: , `Verbose` , , o `Info` `Warning` `Error` .</span><span class="sxs-lookup"><span data-stu-id="b9563-206">Each `console` method is assigned a severity level: `Verbose`, `Info`, `Warning`, or `Error`.</span></span>  <span data-ttu-id="b9563-207">Por ejemplo, `console.log()` es un `Info` mensaje -level, mientras `console.error()` que es un mensaje de `Error` -level.</span><span class="sxs-lookup"><span data-stu-id="b9563-207">For example, `console.log()` is an `Info`-level message, whereas `console.error()` is an `Error`-level message.</span></span>  

1.  <span data-ttu-id="b9563-208">Elija el **desplegable Niveles de registro** y deshabilite **Errores**.</span><span class="sxs-lookup"><span data-stu-id="b9563-208">Choose the **Log Levels** dropdown and disable **Errors**.</span></span>  <span data-ttu-id="b9563-209">Un nivel está deshabilitado cuando ya no hay una marca de verificación junto a él.</span><span class="sxs-lookup"><span data-stu-id="b9563-209">A level is disabled when there is no longer a checkmark next to it.</span></span>  <span data-ttu-id="b9563-210">Los `Error` mensajes -level desaparecen.</span><span class="sxs-lookup"><span data-stu-id="b9563-210">The `Error`-level messages disappear.</span></span>  
    
    :::image type="complex" source="../media/console-cause-violation-log-levels.msft.png" alt-text="Deshabilitar mensajes de nivel de error en la consola" lightbox="../media/console-cause-violation-log-levels.msft.png":::
       <span data-ttu-id="b9563-212">Deshabilitar mensajes de nivel de error en la **consola**</span><span class="sxs-lookup"><span data-stu-id="b9563-212">Disable Error-level messages in the **Console**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-213">Vuelva a **elegir el desplegable Niveles de** registro y vuelva a habilitar **Errores**.</span><span class="sxs-lookup"><span data-stu-id="b9563-213">Choose the **Log Levels** dropdown again and re-enable **Errors**.</span></span>  <span data-ttu-id="b9563-214">Los `Error` mensajes -level reaparecen.</span><span class="sxs-lookup"><span data-stu-id="b9563-214">The `Error`-level messages reappear.</span></span>  

### <a name="filter-by-text"></a><span data-ttu-id="b9563-215">Filtrar por texto</span><span class="sxs-lookup"><span data-stu-id="b9563-215">Filter by text</span></span>  

<span data-ttu-id="b9563-216">Cuando solo desee ver mensajes que incluyan una cadena exacta, escriba esa cadena en el **cuadro de** texto Filtrar.</span><span class="sxs-lookup"><span data-stu-id="b9563-216">When you want to only view messages that include an exact string, type that string into the **Filter** text box.</span></span>  

1.  <span data-ttu-id="b9563-217">Escriba `Dave` en el cuadro **de** texto Filtrar.</span><span class="sxs-lookup"><span data-stu-id="b9563-217">Type `Dave` into the **Filter** text box.</span></span>  <span data-ttu-id="b9563-218">Todos los mensajes que no incluyen la cadena `Dave` están ocultos.</span><span class="sxs-lookup"><span data-stu-id="b9563-218">All messages that do not include the string `Dave` are hidden.</span></span>  <span data-ttu-id="b9563-219">También puede revisar la `Adolescent Irradiated Espionage Tortoises` etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b9563-219">You may also review the `Adolescent Irradiated Espionage Tortoises` label.</span></span>  <span data-ttu-id="b9563-220">Es un error.</span><span class="sxs-lookup"><span data-stu-id="b9563-220">That is a bug.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-text-filter.msft.png" alt-text="Filtrar cualquier mensaje que no incluya a Dave" lightbox="../media/console-all-messages-text-filter.msft.png":::
       <span data-ttu-id="b9563-222">Filtrar cualquier mensaje que no incluya</span><span class="sxs-lookup"><span data-stu-id="b9563-222">Filter out any message that does not include</span></span> `Dave`  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-223">Eliminar `Dave` del cuadro **de** texto Filtro.</span><span class="sxs-lookup"><span data-stu-id="b9563-223">Delete `Dave` from the **Filter** text box.</span></span>  <span data-ttu-id="b9563-224">Todos los mensajes reaparecen.</span><span class="sxs-lookup"><span data-stu-id="b9563-224">All the messages reappear.</span></span>  

### <a name="filter-by-regular-expression"></a><span data-ttu-id="b9563-225">Filtrar por expresión regular</span><span class="sxs-lookup"><span data-stu-id="b9563-225">Filter by regular expression</span></span>  

<span data-ttu-id="b9563-226">Cuando desee mostrar todos los mensajes que incluyen un patrón de texto, en lugar de una cadena específica, use una [expresión regular][MDNRegularExpressions].</span><span class="sxs-lookup"><span data-stu-id="b9563-226">When you want to show all messages that include a pattern of text, rather than a specific string, use a [regular expression][MDNRegularExpressions].</span></span>  

1.  <span data-ttu-id="b9563-227">Escriba `/^[AH]/` en el cuadro **de** texto Filtrar.</span><span class="sxs-lookup"><span data-stu-id="b9563-227">Type `/^[AH]/` into the **Filter** text box.</span></span>  <span data-ttu-id="b9563-228">Escriba el patrón en [RegExr][|::ref1::|Main] para obtener una explicación de lo que está haciendo.</span><span class="sxs-lookup"><span data-stu-id="b9563-228">Type the pattern into [RegExr][|::ref1::|Main] for an explanation of what it is doing.</span></span>  
    
    :::image type="complex" source="../media/console-all-messages-regex-filter.msft.png" alt-text="Filtrar cualquier mensaje que no coincida con un patrón" lightbox="../media/console-all-messages-regex-filter.msft.png":::
       <span data-ttu-id="b9563-230">Filtrar cualquier mensaje que no coincida con el patrón</span><span class="sxs-lookup"><span data-stu-id="b9563-230">Filtering out any message that does not match the pattern</span></span> `/^[AH]/`  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-231">Eliminar `/^[AH]/` del cuadro **de** texto Filtro.</span><span class="sxs-lookup"><span data-stu-id="b9563-231">Delete `/^[AH]/` from the **Filter** text box.</span></span>  <span data-ttu-id="b9563-232">Todos los mensajes están visibles de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b9563-232">All messages are visible again.</span></span>  

### <a name="filter-by-message-source"></a><span data-ttu-id="b9563-233">Filtrar por origen de mensaje</span><span class="sxs-lookup"><span data-stu-id="b9563-233">Filter by message source</span></span>  

<span data-ttu-id="b9563-234">Cuando solo desee ver los mensajes que provenían de una dirección URL determinada, use la **barra lateral**.</span><span class="sxs-lookup"><span data-stu-id="b9563-234">When you want to only view the messages that came from a certain URL, use the **Sidebar**.</span></span>  

1.  <span data-ttu-id="b9563-235">Elija **Mostrar barra lateral de la** consola \( Mostrar barra lateral de la consola ![ ][ImageShowConsoleSidebarIcon] \).</span><span class="sxs-lookup"><span data-stu-id="b9563-235">Choose **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\).</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-all-messages.msft.png" alt-text="La barra lateral" lightbox="../media/console-sidebar-all-messages.msft.png":::
       <span data-ttu-id="b9563-237">La barra lateral</span><span class="sxs-lookup"><span data-stu-id="b9563-237">The Sidebar</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-238">Elija el **icono Expandir** \( ![ Expandir ][ImageExpandIcon] \) junto al número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="b9563-238">Choose the **Expand** \(![Expand][ImageExpandIcon]\) icon next to the number of messages.</span></span>  <span data-ttu-id="b9563-239">En la siguiente figura, el número de mensajes se indica como **13 Mensajes**.</span><span class="sxs-lookup"><span data-stu-id="b9563-239">In the following figure, the number of messages is indicated as **13 Messages**.</span></span>  <span data-ttu-id="b9563-240">La **barra** lateral muestra una lista de direcciones URL que provocaron que se registraron los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b9563-240">The **Sidebar** shows a list of URLs that caused messages to be logged.</span></span>  <span data-ttu-id="b9563-241">Por ejemplo, `log.js` causó 11 mensajes.</span><span class="sxs-lookup"><span data-stu-id="b9563-241">For example, `log.js` caused 11 messages.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-expanded-all-messages.msft.png" alt-text="Ver el origen de los mensajes en la barra lateral" lightbox="../media/console-sidebar-expanded-all-messages.msft.png":::
       <span data-ttu-id="b9563-243">Ver el origen de los mensajes en la barra lateral</span><span class="sxs-lookup"><span data-stu-id="b9563-243">Viewing the source of messages in the Sidebar</span></span>  
    :::image-end:::  
    
### <a name="filter-by-user-messages"></a><span data-ttu-id="b9563-244">Filtrar por mensajes de usuario</span><span class="sxs-lookup"><span data-stu-id="b9563-244">Filter by user messages</span></span>  

<span data-ttu-id="b9563-245">Anteriormente, cuando elige **Información de registro**, un script denominado para registrar el mensaje en la `console.log('Hello, Console!')` consola.</span><span class="sxs-lookup"><span data-stu-id="b9563-245">Earlier, when you choose **Log Info**, a script named `console.log('Hello, Console!')` in order to log the message to the Console.</span></span>  <span data-ttu-id="b9563-246">Los mensajes registrados desde JavaScript como este se **denominan mensajes de usuario**.</span><span class="sxs-lookup"><span data-stu-id="b9563-246">Messages logged from JavaScript like this are named **user messages**.</span></span>  <span data-ttu-id="b9563-247">En cambio, al elegir **Causa 404,** el explorador registra un mensaje de nivel que indica que no se encuentra `Error` el recurso solicitado.</span><span class="sxs-lookup"><span data-stu-id="b9563-247">In contrast, when you choose **Cause 404**, the browser logs an `Error`-level message stating that the requested resource is not found.</span></span>  <span data-ttu-id="b9563-248">Mensajes como ese se consideran mensajes **del explorador**.</span><span class="sxs-lookup"><span data-stu-id="b9563-248">Messages like that are considered **browser messages**.</span></span>  <span data-ttu-id="b9563-249">Usa la **barra lateral para** filtrar los mensajes del explorador y solo mostrar mensajes de usuario.</span><span class="sxs-lookup"><span data-stu-id="b9563-249">Use the **Sidebar** to filter out browser messages and only show user messages.</span></span>  

1.  <span data-ttu-id="b9563-250">Elija **9 mensajes de usuario**.</span><span class="sxs-lookup"><span data-stu-id="b9563-250">Choose **9 User Messages**.</span></span>  <span data-ttu-id="b9563-251">Los mensajes del explorador están ocultos.</span><span class="sxs-lookup"><span data-stu-id="b9563-251">The browser messages are hidden.</span></span>  
    
    :::image type="complex" source="../media/console-sidebar-user-messages.msft.png" alt-text="Filtrado de mensajes del explorador" lightbox="../media/console-sidebar-user-messages.msft.png":::
       <span data-ttu-id="b9563-253">Filtrado de mensajes del explorador</span><span class="sxs-lookup"><span data-stu-id="b9563-253">Filtering out browser messages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b9563-254">Elija **13 Mensajes para** volver a mostrar todos los mensajes.</span><span class="sxs-lookup"><span data-stu-id="b9563-254">Choose **13 Messages** to show all messages again.</span></span>  

## <a name="use-the-console-alongside-any-other-tools"></a><span data-ttu-id="b9563-255">Usar la consola junto con otras herramientas</span><span class="sxs-lookup"><span data-stu-id="b9563-255">Use the Console alongside any other tools</span></span>  

<span data-ttu-id="b9563-256">Si está editando estilos, pero necesita comprobar rápidamente si hay algo en el registro de consola, Use the Drawer.</span><span class="sxs-lookup"><span data-stu-id="b9563-256">If you are editing styles, but you need to quickly check the Console log for something, Use the Drawer.</span></span>  

1.  <span data-ttu-id="b9563-257">Elija la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="b9563-257">Choose the **Elements** tool.</span></span>  
1.  <span data-ttu-id="b9563-258">Seleccione `Escape` .</span><span class="sxs-lookup"><span data-stu-id="b9563-258">Select `Escape`.</span></span>  <span data-ttu-id="b9563-259">Se **abre la herramienta** Consola en **el** cajón.</span><span class="sxs-lookup"><span data-stu-id="b9563-259">The **Console** tool in the **Drawer** opens.</span></span>  <span data-ttu-id="b9563-260">Tiene todas las características del panel consola que ha estado usando a lo largo de este tutorial.</span><span class="sxs-lookup"><span data-stu-id="b9563-260">It has all of the features of the Console panel that you have been using throughout this tutorial.</span></span>  
    
    :::image type="complex" source="../media/console-elements-drawer-console-sidebar-all-messages.msft.png" alt-text="La herramienta Consola en el cajón" lightbox="../media/console-elements-drawer-console-sidebar-all-messages.msft.png":::
         <span data-ttu-id="b9563-262">La **herramienta Consola** en el **cajón**</span><span class="sxs-lookup"><span data-stu-id="b9563-262">The **Console** tool in the **Drawer**</span></span>  
    :::image-end:::  
    
## <a name="see-also"></a><span data-ttu-id="b9563-263">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b9563-263">See also</span></span>  

*   <span data-ttu-id="b9563-264">Para explorar más características y flujos de trabajo relacionados con **la** interfaz de usuario de consola, vaya a Referencia [de consola][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="b9563-264">To explore more features and workflows related to the **Console** UI,navigate to [Console Reference][DevToolsConsoleApi].</span></span>  
*   <span data-ttu-id="b9563-265">Para obtener más información sobre todos los métodos que se muestran en Ver mensajes registrados desde JavaScript y explorar los otros métodos que no se tratan en este artículo, vaya a `console` Console API [](#view-messages-logged-from-javascript) `console` [Reference][DevToolsConsoleReference].</span><span class="sxs-lookup"><span data-stu-id="b9563-265">To learn more about all of the `console` methods demonstrated in [View messages logged from JavaScript](#view-messages-logged-from-javascript) and explore the other `console` methods not covered in this article, navigate to [Console API Reference][DevToolsConsoleReference].</span></span>  
<!--*   Navigate to [Get Started](/microsoft-edge/devtools-guide-chromium/#start) to explore what else you are able to do with DevTools.  -->  
     
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b9563-266">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b9563-266">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExpandIcon]: ../media/expand-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Herramientas para desarrolladores de Microsoft Edge \(Chromium\) | Microsoft Docs"  
[DevToolsCommandMenu]: ../command-menu/index.md "Ejecute comandos con el menú Comando de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizePlacement]: ../customize/placement.md "Cambiar la ubicación de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsConsoleApi]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevToolsConsoleReference]: ./reference.md "Referencia de consola | Microsoft Docs"  

[GlitchDevToolsConsoleLogExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/log.html "Introducción al registro de mensajes | Glitch"  

[MDNRegularExpressions]: https://developer.mozilla.org/docs/Web/JavaScript/Guide/Regular_Expressions "Expresiones regulares | MDN"  

[RegExrMain]: https://regexr.com "RegExr"  

[WikiStackTrace]: https://en.wikipedia.org/wiki/Stack_trace "Seguimiento de pila : Wikipedia"  
> [!NOTE]
> <span data-ttu-id="b9563-276">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b9563-276">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b9563-277">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/log) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="b9563-277">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/log) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b9563-279">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b9563-279">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
