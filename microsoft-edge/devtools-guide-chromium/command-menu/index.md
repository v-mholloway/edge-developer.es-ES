---
title: Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 748008b347a3498008748b9c3f9ecc1445c47f12
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601750"
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





# <span data-ttu-id="0f782-103">Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0f782-103">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="0f782-104">El menú de comandos proporciona una forma rápida de navegar por la interfaz de usuario de Microsoft Edge DevTools y realizar tareas comunes, como la [deshabilitación de JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="0f782-104">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="0f782-105">Es posible que esté familiarizado con una característica similar de Visual Studio que se denomina [paleta de comandos][VisualStudioCodeUICommandPalette], que es la inspiración original para el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="0f782-105">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

> ##### <span data-ttu-id="0f782-106">Figura 1</span><span class="sxs-lookup"><span data-stu-id="0f782-106">Figure 1</span></span>  
> <span data-ttu-id="0f782-107">Usar el menú de comandos para deshabilitar JavaScript</span><span class="sxs-lookup"><span data-stu-id="0f782-107">Using the Command Menu to disable JavaScript</span></span>  
> ![Usar el menú de comandos para deshabilitar JavaScript][ImageDisableJS]  

## <span data-ttu-id="0f782-109">Abrir el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="0f782-109">Open the Command Menu</span></span>   

<span data-ttu-id="0f782-110">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="0f782-110">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="0f782-111">O bien, haga clic en **personalizar y controlar DevTools** `...` y, a continuación, seleccione **Ejecutar comando**.</span><span class="sxs-lookup"><span data-stu-id="0f782-111">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

> ##### <span data-ttu-id="0f782-112">Figura 2</span><span class="sxs-lookup"><span data-stu-id="0f782-112">Figure 2</span></span>  
> <span data-ttu-id="0f782-113">Comando ejecutar</span><span class="sxs-lookup"><span data-stu-id="0f782-113">Run Command</span></span>  
> ![Comando ejecutar][ImageRunCommand]  

## <span data-ttu-id="0f782-115">Ver otras acciones disponibles</span><span class="sxs-lookup"><span data-stu-id="0f782-115">See other available actions</span></span>   

<span data-ttu-id="0f782-116">Si usa el flujo de trabajo esquematizado en [abrir el menú de comandos](#open-the-command-menu), el menú de comandos se abre con un `>` carácter antepuesto al cuadro de texto del menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="0f782-116">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character prepended to the Command Menu text box.</span></span>  

> ##### <span data-ttu-id="0f782-117">Imagen 3</span><span class="sxs-lookup"><span data-stu-id="0f782-117">Figure 3</span></span>  
> <span data-ttu-id="0f782-118">El carácter de comando</span><span class="sxs-lookup"><span data-stu-id="0f782-118">The command character</span></span>  
> ![El carácter de comando][ImageCommandCharacter]  

<span data-ttu-id="0f782-120">Elimine el `>` carácter y escriba `?` para ver otras acciones disponibles en el menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="0f782-120">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

> ##### <span data-ttu-id="0f782-121">Imagen 4</span><span class="sxs-lookup"><span data-stu-id="0f782-121">Figure 4</span></span>  
> <span data-ttu-id="0f782-122">Otras acciones disponibles</span><span class="sxs-lookup"><span data-stu-id="0f782-122">Other available actions</span></span>  
> ![Otras acciones disponibles][ImageActions]  

 



<!-- image links -->  

[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command-java.msft.png "Ilustración 1: usar el menú de comandos para deshabilitar JavaScript"  
[ImageRunCommand]: /microsoft-edge/devtools-guide-chromium/media/command-menu-options-run-command.msft.png "Ilustración 2: comando ejecutar"  
[ImageCommandCharacter]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command.msft.png "Ilustración 3: el carácter de comando"  
[ImageActions]: /microsoft-edge/devtools-guide-chromium/media/command-menu-help.msft.png "Ilustración 4: otras acciones disponibles"  

<!-- links -->  

[JavascriptDisable]: /microsoft-edge/devtools-guide-chromium/javascript/disable "Deshabilitar JavaScript con Microsoft Edge DevTools"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Paleta de comandos: interfaz de usuario de Visual Studio"  

> [!NOTE]
> <span data-ttu-id="0f782-130">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0f782-130">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0f782-131">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="0f782-131">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="0f782-133">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0f782-133">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
