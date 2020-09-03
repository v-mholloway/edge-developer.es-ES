---
description: Guía sobre cómo abrir el menú de comandos, ejecutar comandos, ver otras acciones y mucho más.
title: Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 54dead492e7d58053efab77c82a10e7e3c912460
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993201"
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





# <span data-ttu-id="04b7c-104">Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="04b7c-104">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="04b7c-105">El menú de comandos proporciona una forma rápida de navegar por la interfaz de usuario de Microsoft Edge DevTools y realizar tareas comunes, como la [deshabilitación de JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="04b7c-105">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="04b7c-106">Es posible que esté familiarizado con una característica similar de Visual Studio que se denomina [paleta de comandos][VisualStudioCodeUICommandPalette], que es la inspiración original para el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="04b7c-106">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Usar el menú de comandos para deshabilitar JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="04b7c-108">Usar el menú de comandos para deshabilitar JavaScript</span><span class="sxs-lookup"><span data-stu-id="04b7c-108">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="04b7c-109">Abrir el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="04b7c-109">Open the Command Menu</span></span>   

<span data-ttu-id="04b7c-110">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="04b7c-110">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="04b7c-111">O bien, haga clic en **personalizar y controlar DevTools** `...` y, a continuación, seleccione **Ejecutar comando**.</span><span class="sxs-lookup"><span data-stu-id="04b7c-111">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Comando ejecutar" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="04b7c-113">Comando ejecutar</span><span class="sxs-lookup"><span data-stu-id="04b7c-113">Run Command</span></span>  
:::image-end:::  

## <span data-ttu-id="04b7c-114">Ver otras acciones disponibles</span><span class="sxs-lookup"><span data-stu-id="04b7c-114">See other available actions</span></span>   

<span data-ttu-id="04b7c-115">Si usa el flujo de trabajo esquematizado en [abrir el menú de comandos](#open-the-command-menu), el menú comando se abre con un `>` carácter preestablecido en el cuadro de texto del menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="04b7c-115">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="El carácter de comando" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="04b7c-117">El carácter de comando</span><span class="sxs-lookup"><span data-stu-id="04b7c-117">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="04b7c-118">Elimine el `>` carácter y escriba `?` para ver otras acciones disponibles en el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="04b7c-118">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Otras acciones disponibles" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="04b7c-120">Otras acciones disponibles</span><span class="sxs-lookup"><span data-stu-id="04b7c-120">Other available actions</span></span>  
:::image-end:::  

 



<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft docs"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Paleta de comandos: interfaz de usuario de Visual Studio"  

> [!NOTE]
> <span data-ttu-id="04b7c-123">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="04b7c-123">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="04b7c-124">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="04b7c-124">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="04b7c-126">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="04b7c-126">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
