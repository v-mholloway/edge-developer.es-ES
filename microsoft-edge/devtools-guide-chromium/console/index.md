---
title: Descripción general de la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 45e2eb9d66fa284b1326e7554b6897a1e1747561
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982298"
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





# <span data-ttu-id="dbba3-103">Descripción general de la consola</span><span class="sxs-lookup"><span data-stu-id="dbba3-103">Console Overview</span></span>   

  

<span data-ttu-id="dbba3-104">Esta página explica cómo la consola de Microsoft Edge DevTools facilita el desarrollo de páginas Web.</span><span class="sxs-lookup"><span data-stu-id="dbba3-104">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="dbba3-105">La consola tiene 2 usos principales: [ver los mensajes registrados](#viewing-logged-messages) y [ejecutar JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="dbba3-105">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="dbba3-106">Ver mensajes registrados</span><span class="sxs-lookup"><span data-stu-id="dbba3-106">Viewing logged messages</span></span>   

<span data-ttu-id="dbba3-107">Los desarrolladores web suelen registrar mensajes en la consola para asegurarse de que su JavaScript funciona según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="dbba3-107">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="dbba3-108">Para registrar un mensaje, debe insertar una expresión como `console.log('Hello, Console!')` en su código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dbba3-108">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="dbba3-109">Cuando el explorador ejecuta el JavaScript y ve una expresión como esta, registra el mensaje en la consola.</span><span class="sxs-lookup"><span data-stu-id="dbba3-109">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="dbba3-110">El código HTML y JavaScript de la página.</span><span class="sxs-lookup"><span data-stu-id="dbba3-110">The HTML and JavaScript for the page.</span></span>  
      
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
                      { first: 'Henri', last: 'Matisse' }
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
      <span data-ttu-id="dbba3-111">En la siguiente ilustración, la **consola** muestra los resultados de cargar la página y esperar 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="dbba3-111">In the following figure, the **Console** displays the results of loading the page and waiting 3 seconds.</span></span>  
      
      :::image type="complex" source="../media/console-console-demo.msft.png" alt-text="Panel de consola" lightbox="../media/console-console-demo.msft.png":::
         <span data-ttu-id="dbba3-113">Panel de **consola**</span><span class="sxs-lookup"><span data-stu-id="dbba3-113">The **Console** panel</span></span>  
      :::image-end:::  
      
      <span data-ttu-id="dbba3-114">Intente determinar qué líneas de código hicieron que el explorador registre los mensajes.</span><span class="sxs-lookup"><span data-stu-id="dbba3-114">Try to determine which lines of code caused the browser to log the messages.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="dbba3-115">Los programadores de web registran los mensajes por las siguientes 2 razones generales.</span><span class="sxs-lookup"><span data-stu-id="dbba3-115">Web developers log messages for the following 2 general reasons.</span></span>  

*   <span data-ttu-id="dbba3-116">Asegurarse de que el código se esté ejecutando en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="dbba3-116">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="dbba3-117">Inspeccionar los valores de variables en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="dbba3-117">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="dbba3-118">Consulte Introducción al [registro de mensajes][DevtoolsConsoleLoggingMessages] para obtener experiencia práctica con el registro.</span><span class="sxs-lookup"><span data-stu-id="dbba3-118">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="dbba3-119">Consulta la [referencia][DevToolsConsoleAPI] de la API de consola para examinar la lista completa de `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="dbba3-119">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="dbba3-120">La principal diferencia entre los métodos radica en la forma en que se muestran los datos que se registran.</span><span class="sxs-lookup"><span data-stu-id="dbba3-120">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="dbba3-121">Ejecutar JavaScript</span><span class="sxs-lookup"><span data-stu-id="dbba3-121">Running JavaScript</span></span>   

<span data-ttu-id="dbba3-122">La **consola** también es una [REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="dbba3-122">The **Console** is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="dbba3-123">Puede ejecutar JavaScript en la **consola** para interactuar con la página que se está inspeccionando.</span><span class="sxs-lookup"><span data-stu-id="dbba3-123">You may run JavaScript in the **Console** to interact with the page being inspected.</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="dbba3-124">En la siguiente ilustración, la **consola** se muestra junto a la página de inicio de DevTools.</span><span class="sxs-lookup"><span data-stu-id="dbba3-124">In the following figure, the **Console** is shown next to the DevTools homepage.</span></span>  
      
      :::image type="complex" source="../media/devtools-console-empty.msft.png" alt-text="Panel de consola junto a la Página principal de DevTools" lightbox="../media/devtools-console-empty.msft.png":::
         <span data-ttu-id="dbba3-126">Panel de **consola** junto a la Página principal de DevTools</span><span class="sxs-lookup"><span data-stu-id="dbba3-126">The **Console** panel next to the DevTools homepage</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="dbba3-127">En la siguiente ilustración, se muestra la misma página después de usar la **consola** para cambiar el encabezado superior de la página.</span><span class="sxs-lookup"><span data-stu-id="dbba3-127">In the following figure, the same page is shown after using the **Console** to change the top heading of the page.</span></span>
      
      :::image type="complex" source="../media/devtools-console-h1-changed.msft.png" alt-text="Usar la consola para cambiar el encabezado superior de la página" lightbox="../media/devtools-console-h1-changed.msft.png":::
         <span data-ttu-id="dbba3-129">Usar la **consola** para cambiar el encabezado superior de la página</span><span class="sxs-lookup"><span data-stu-id="dbba3-129">Use the **Console** to change the top heading of the page</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="dbba3-130">Es posible modificar la página desde la **consola** porque la **consola** tiene acceso completo a la [ventana][MDNWindow] de la página.</span><span class="sxs-lookup"><span data-stu-id="dbba3-130">Modifying the page from the **Console** is possible because the **Console** has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="dbba3-131">DevTools tiene varias funciones útiles que hacen que sea más fácil inspeccionar una página.</span><span class="sxs-lookup"><span data-stu-id="dbba3-131">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="dbba3-132">Por ejemplo, supongamos que su código JavaScript contiene una función llamada `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="dbba3-132">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="dbba3-133">La ejecución `debug(hideModal)` pausa el código en la primera línea de `hideModal` la próxima vez que lo ejecute.</span><span class="sxs-lookup"><span data-stu-id="dbba3-133">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="dbba3-134">Para obtener más información sobre la lista completa de funciones de utilidades, consulte referencia de la [API de utilidades de consola][DevtoolsConsoleUtilitiesDebug].</span><span class="sxs-lookup"><span data-stu-id="dbba3-134">For more information about the full list of utility functions, see [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug].</span></span>  

<span data-ttu-id="dbba3-135">Al ejecutar JavaScript, no es necesario que interactúe con la página.</span><span class="sxs-lookup"><span data-stu-id="dbba3-135">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="dbba3-136">Puede usar la **consola** para probar código nuevo no relacionado con la página.</span><span class="sxs-lookup"><span data-stu-id="dbba3-136">You may use the **Console** to try out new code unrelated to the page.</span></span>  <span data-ttu-id="dbba3-137">Por ejemplo, supongamos que acaba de conocer el método de asignación de matriz [()][MDNMap] integrado de JavaScript y quiere experimentar con él.</span><span class="sxs-lookup"><span data-stu-id="dbba3-137">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="dbba3-138">La **consola** es un buen lugar para probar la función.</span><span class="sxs-lookup"><span data-stu-id="dbba3-138">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="dbba3-139">Para obtener más experiencia práctica con la ejecución de JavaScript en la **consola**, consulte Introducción [a la ejecución de JavaScript][DevtoolsConsoleRunningJavascript].</span><span class="sxs-lookup"><span data-stu-id="dbba3-139">For more hands-on experience with running JavaScript in the **Console**, see [Get Started With Running JavaScript][DevtoolsConsoleRunningJavascript].</span></span>  

   

  

<!-- links -->  

[DevToolsConsoleAPI]: ./api.md "Referencia de la API de consola | Microsoft docs"  
[DevtoolsConsoleLoggingMessages]: ./log.md "Introducción a la creación de mensajes de registro en la consola | Microsoft docs"  
[DevtoolsConsoleRunningJavascript]: ./javascript.md "Introducción a la ejecución de JavaScript en la consola | Microsoft docs"  
[DevtoolsConsoleUtilitiesDebug]: ./utilities.md#debug "Debug: referencia de API de utilidades de consola | Microsoft docs"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lectura: eval – imprimir bucle-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="dbba3-147">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dbba3-147">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dbba3-148">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="dbba3-148">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="dbba3-150">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dbba3-150">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
