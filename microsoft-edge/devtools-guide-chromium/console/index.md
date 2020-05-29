---
title: Descripción general de la consola
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6062afb929a5d763c095d4915a2960993bc5ab4c
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601792"
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





# <span data-ttu-id="1c4dd-103">Descripción general de la consola</span><span class="sxs-lookup"><span data-stu-id="1c4dd-103">Console Overview</span></span>   

  

<span data-ttu-id="1c4dd-104">Esta página explica cómo la consola de Microsoft Edge DevTools facilita el desarrollo de páginas Web.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-104">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="1c4dd-105">La consola tiene 2 usos principales: [ver los mensajes registrados](#viewing-logged-messages) y [ejecutar JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="1c4dd-105">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="1c4dd-106">Ver mensajes registrados</span><span class="sxs-lookup"><span data-stu-id="1c4dd-106">Viewing logged messages</span></span>   

<span data-ttu-id="1c4dd-107">Los desarrolladores web suelen registrar mensajes en la consola para asegurarse de que su JavaScript funciona según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-107">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="1c4dd-108">Para registrar un mensaje, debe insertar una expresión como `console.log('Hello, Console!')` en su código JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-108">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="1c4dd-109">Cuando el explorador ejecuta el JavaScript y ve una expresión como esta, registra el mensaje en la consola.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-109">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  <span data-ttu-id="1c4dd-110">Por ejemplo, supongamos que está escribiendo HTML y JavaScript para una página:</span><span class="sxs-lookup"><span data-stu-id="1c4dd-110">For example, suppose that you are writing the HTML and JavaScript for a page:</span></span>  

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
        {
          first: 'René',
          last: 'Magritte'
        },
        {
          first: 'Chaim',
          last: 'Soutine'
        },
        {
          first: 'Henri',
          last: 'Matisse'
        }
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

<span data-ttu-id="1c4dd-111">En la [Ilustración 1](#figure-1) se muestra el aspecto que tiene la consola después de cargar la página y esperar 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-111">[Figure 1](#figure-1) shows what the Console looks like after loading the page and waiting 3 seconds.</span></span>  <span data-ttu-id="1c4dd-112">Intenta averiguar qué líneas de código hicieron que el explorador registre los mensajes.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-112">Try to figure out which lines of code caused the browser to log the messages.</span></span>  

> ##### <span data-ttu-id="1c4dd-113">Figura 1</span><span class="sxs-lookup"><span data-stu-id="1c4dd-113">Figure 1</span></span>  
> <span data-ttu-id="1c4dd-114">Panel de consola</span><span class="sxs-lookup"><span data-stu-id="1c4dd-114">The Console panel</span></span>  
> ![Panel de consola][ImageConsole]  

<span data-ttu-id="1c4dd-116">Los programadores web registran los mensajes por dos razones generales:</span><span class="sxs-lookup"><span data-stu-id="1c4dd-116">Web developers log messages for 2 general reasons:</span></span>  

*   <span data-ttu-id="1c4dd-117">Asegurarse de que el código se esté ejecutando en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="1c4dd-118">Inspeccionar los valores de variables en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="1c4dd-119">Consulte Introducción al [registro de mensajes][DevtoolsConsoleLoggingMessages] para obtener experiencia práctica con el registro.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="1c4dd-120">Consulta la [referencia][DevToolsConsoleAPI] de la API de consola para examinar la lista completa de `console` métodos.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="1c4dd-121">La principal diferencia entre los métodos radica en la forma en que se muestran los datos que se registran.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="1c4dd-122">Ejecutar JavaScript</span><span class="sxs-lookup"><span data-stu-id="1c4dd-122">Running JavaScript</span></span>   

<span data-ttu-id="1c4dd-123">La consola también es una [REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="1c4dd-123">The Console is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="1c4dd-124">Puede ejecutar JavaScript en la consola para interactuar con la página que se está inspeccionando.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-124">You may run JavaScript in the Console to interact with the page being inspected.</span></span>  <span data-ttu-id="1c4dd-125">Por ejemplo, la [ilustración 2](#figure-2) muestra la consola junto a la página de inicio de DevTools, y la [figura 3](#figure-3) muestra la misma página después de usar la consola para cambiar el encabezado superior de la página.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-125">For example, [Figure 2](#figure-2) shows the Console next to the DevTools homepage, and [Figure 3](#figure-3) shows that same page after using the Console to change the top heading of the page.</span></span>  

> ##### <span data-ttu-id="1c4dd-126">Figura 2</span><span class="sxs-lookup"><span data-stu-id="1c4dd-126">Figure 2</span></span>  
> <span data-ttu-id="1c4dd-127">Panel de consola junto a la Página principal de DevTools</span><span class="sxs-lookup"><span data-stu-id="1c4dd-127">The Console panel next to the DevTools homepage</span></span>  
> ![Panel de consola junto a la Página principal de DevTools][ImageConsoleOverview]  

> ##### <span data-ttu-id="1c4dd-129">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="1c4dd-129">Figure 3</span></span>  
> <span data-ttu-id="1c4dd-130">Usar la consola para cambiar el encabezado superior de la página</span><span class="sxs-lookup"><span data-stu-id="1c4dd-130">Using the Console to change the top heading of the page</span></span>  
> ![Usar la consola para cambiar el encabezado superior de la página][ImageConsoleChangeTitle]  

<span data-ttu-id="1c4dd-132">Es posible modificar la página desde la consola porque la consola tiene acceso completo a la [ventana][MDNWindow] de la página.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-132">Modifying the page from the Console is possible because the Console has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="1c4dd-133">DevTools tiene varias funciones útiles que hacen que sea más fácil inspeccionar una página.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-133">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="1c4dd-134">Por ejemplo, supongamos que su código JavaScript contiene una función llamada `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="1c4dd-134">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="1c4dd-135">La ejecución `debug(hideModal)` pausa el código en la primera línea de `hideModal` la próxima vez que lo ejecute.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-135">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="1c4dd-136">Consulte [referencia][DevtoolsConsoleUtilitiesDebug] de la API de utilidades de consola para ver la lista completa de funciones de utilidades.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-136">See [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug] to see the full list of utility functions.</span></span>  

<span data-ttu-id="1c4dd-137">Al ejecutar JavaScript, no es necesario que interactúe con la página.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-137">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="1c4dd-138">Puede usar la consola para probar código nuevo no relacionado con la página.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-138">You may use the Console to try out new code unrelated to the page.</span></span>  <span data-ttu-id="1c4dd-139">Por ejemplo, supongamos que acaba de conocer el método de asignación de matriz [()][MDNMap] integrado de JavaScript y quiere experimentar con él.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-139">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="1c4dd-140">La **consola** es un buen lugar para probar la función.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-140">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="1c4dd-141">Consulte Introducción a la [ejecución de JavaScript][ImageConsoleChangeTitle] para obtener experiencia práctica de ejecución de JavaScript en la consola.</span><span class="sxs-lookup"><span data-stu-id="1c4dd-141">See [Get Started With Running JavaScript][ImageConsoleChangeTitle] to get hands-on experience with running JavaScript in the Console.</span></span>  

   

  

<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-console-demo.msft.png "Ilustración 1: panel de consola"  
[ImageConsoleChangeTitle]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-h1-changed.msft.png "Ilustración 3: usar la consola para cambiar el encabezado superior de la página"  
[ImageConsoleOverview]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-empty.msft.png "Ilustración 2: el panel de la consola junto a la Página principal de DevTools"  

<!-- links -->  

[DevToolsConsoleAPI]: /microsoft-edge/devtools-guide-chromium/console/api "Referencia de la API de consola"  
[DevtoolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Introducción al registro de mensajes en la consola"  
[DevtoolsConsoleRunningJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Introducción a la ejecución de JavaScript en la consola"  
[DevtoolsConsoleUtilitiesDebug]: /microsoft-edge/devtools-guide-chromium/console/utilities#debug "Debug: referencia de API de utilidades de consola"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Ventana | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Lectura: eval – imprimir bucle-Wikipedia"  

> [!NOTE]
> <span data-ttu-id="1c4dd-152">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c4dd-152">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="1c4dd-153">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="1c4dd-153">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="1c4dd-155">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="1c4dd-155">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
