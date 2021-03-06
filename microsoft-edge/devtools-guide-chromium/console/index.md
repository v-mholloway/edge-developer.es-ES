---
description: Los principales usos de la consola de Microsoft Edge DevTools son el registro de mensajes y la ejecución de JavaScript.
title: Información general sobre la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 496caa4d304d9511d4b1c341846f377899ba4597
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399123"
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

# <a name="console-overview"></a><span data-ttu-id="8e4bb-104">Información general sobre la consola</span><span class="sxs-lookup"><span data-stu-id="8e4bb-104">Console overview</span></span>  

  

<span data-ttu-id="8e4bb-105">En esta página se explica cómo la consola DevTools de Microsoft Edge facilita el desarrollo de páginas web.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-105">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="8e4bb-106">La **consola** tiene dos usos principales: [ver mensajes registrados](#viewing-logged-messages) y [ejecutar JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="8e4bb-106">The **Console** has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <a name="viewing-logged-messages"></a><span data-ttu-id="8e4bb-107">Visualización de mensajes registrados</span><span class="sxs-lookup"><span data-stu-id="8e4bb-107">Viewing logged messages</span></span>  

<span data-ttu-id="8e4bb-108">Los desarrolladores web suelen registrar mensajes en la consola para asegurarse de que su JavaScript funciona según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-108">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="8e4bb-109">Para registrar un mensaje, inserte una expresión como `console.log('Hello, Console!')` en su JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-109">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="8e4bb-110">Cuando el explorador ejecuta JavaScript y procesa una expresión como esta, el explorador registra el mensaje en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-110">When the browser runs your JavaScript and processes an expression like it, the browser logs the message to the **Console**.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="8e4bb-111">Html y JavaScript para la página.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-111">The HTML and JavaScript for the page.</span></span>  
      
      ```html
      <!doctype html>
      <html>
          <head>
              <title>Console Demo</title>
          </head>
          <body>
              <h1>Hello, World!</h1>
              <script>
                  console.log('Loading!');
                  const h1 = document.querySelector('h1');
                  console.log(h1.textContent);
                  console.assert(document.querySelector('h2'), 'h2 not found!');
                  const artists = [
                      { first: 'René', last: 'Magritte' },
                      { first: 'Chaim', last: 'Soutine' },
                        
                  ];
                  console.table(artists);
                  setTimeout(() => {
                      h1.textContent = 'Hello, Console!';
                      console.log(h1.textContent);
                  }, 3000);
              </script>
          </body>
      </html>
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8e4bb-112">En la siguiente figura, la **consola** muestra los resultados de cargar la página y esperar 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-112">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Panel consola" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="8e4bb-114">La **herramienta Consola**</span><span class="sxs-lookup"><span data-stu-id="8e4bb-114">The **Console** tool</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="8e4bb-115">Intente determinar qué líneas de código provocaron que el explorador registrara los mensajes.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-115">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="8e4bb-116">Los desarrolladores web registrarán mensajes por los siguientes 2 motivos generales.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-116">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="8e4bb-117">Asegurarse de que el código se ejecuta en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="8e4bb-118">Inspeccionar los valores de las variables en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="8e4bb-119">Para obtener experiencia práctica con el registro, vaya a Introducción a Los mensajes [de registro.][DevtoolsConsoleLoggingMessages]</span><span class="sxs-lookup"><span data-stu-id="8e4bb-119">To get hands-on experience with logging, navigate to [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages].</span></span>  <span data-ttu-id="8e4bb-120">Para examinar la lista completa de `console` métodos, vaya a La referencia [de la API de consola.][DevToolsConsoleAPI]</span><span class="sxs-lookup"><span data-stu-id="8e4bb-120">To browse the full list of `console` methods, navigate to the [Console API Reference][DevToolsConsoleAPI].</span></span>  <span data-ttu-id="8e4bb-121">La diferencia principal entre los métodos es cómo se muestran los datos que se registran.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <a name="running-javascript"></a><span data-ttu-id="8e4bb-122">Ejecución de JavaScript</span><span class="sxs-lookup"><span data-stu-id="8e4bb-122">Running JavaScript</span></span>  

<span data-ttu-id="8e4bb-123">La **consola** también es [una REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="8e4bb-123">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="8e4bb-124">Puede ejecutar JavaScript en la **consola para** interactuar con la página que se va a inspeccionar.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-124">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="8e4bb-125">En la siguiente figura, la **consola** se muestra junto a la página principal de DevTools.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-125">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="La herramienta Consola junto a la página principal de DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="8e4bb-127">La **herramienta Consola** junto a la página principal de DevTools</span><span class="sxs-lookup"><span data-stu-id="8e4bb-127">The **Console** tool next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="8e4bb-128">En la siguiente figura, se muestra la misma página después de usar la **consola** para cambiar el encabezado superior de la página.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-128">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Usar la consola para cambiar el encabezado superior de la página" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="8e4bb-130">Usar la **consola** para cambiar el encabezado superior de la página</span><span class="sxs-lookup"><span data-stu-id="8e4bb-130">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="8e4bb-131">La modificación de la página desde la **consola** es posible porque **la consola** tiene acceso completo a la [ventana][MDNWindow] de la página.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-131">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="8e4bb-132">DevTools tiene algunas funciones de comodidad que facilitan la inspección de una página.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-132">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="8e4bb-133">Por ejemplo, supongamos que JavaScript contiene una función denominada `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="8e4bb-133">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="8e4bb-134">La `debug(hideModal)` ejecución pausa el código en la primera línea de la próxima vez que lo `hideModal` ejecute.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-134">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="8e4bb-135">Para obtener más información acerca de la lista completa de funciones de utilidad, vaya a [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span><span class="sxs-lookup"><span data-stu-id="8e4bb-135">For more information about the full list of utility functions, navigate to [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="8e4bb-136">Al ejecutar JavaScript no es necesario interactuar con la página.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-136">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="8e4bb-137">Puede usar la consola **para** probar código nuevo que no esté relacionado con la página.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-137">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="8e4bb-138">Por ejemplo, supongamos que acaba de aprender sobre el método integrado [map()][MDNMap] de matriz de JavaScript y desea experimentar con él.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-138">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="8e4bb-139">La **consola** es un buen lugar para probar la función.</span><span class="sxs-lookup"><span data-stu-id="8e4bb-139">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="8e4bb-140">Para obtener más experiencia práctica con la ejecución de JavaScript en la **consola,** vaya a Introducción a [La ejecución de JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="8e4bb-140">For more hands-on experience with running JavaScript in the **Console**, navigate to [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="8e4bb-141">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8e4bb-141">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Introducción al registro de mensajes en la consola | Microsoft Docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Introducción a la ejecución de JavaScript en la consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "debug: referencia de api de utilidades de consola | Microsoft Docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array.prototype.map() | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Bucle read-eval-print - Wikipedia"  

> [!NOTE]
> <span data-ttu-id="8e4bb-149">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8e4bb-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8e4bb-150">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="8e4bb-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8e4bb-152">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8e4bb-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
