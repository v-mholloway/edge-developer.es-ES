---
description: Una guía sobre cómo abrir el menú comando, ejecutar comandos, revisar otras acciones y mucho más.
title: Ejecutar comandos con el menú Microsoft Edge comando DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 973b440a27b0c4c06ba118fc09e4162a8fa346e8
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564493"
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
# <a name="run-commands-with-the-microsoft-edge-devtools-command-menu"></a><span data-ttu-id="96d7f-104">Ejecutar comandos con el menú Microsoft Edge comando DevTools</span><span class="sxs-lookup"><span data-stu-id="96d7f-104">Run commands with the Microsoft Edge DevTools Command Menu</span></span>  

<span data-ttu-id="96d7f-105">El menú de comandos proporciona una forma rápida de navegar por la Microsoft Edge de DevTools y realizar tareas comunes, como [deshabilitar JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="96d7f-105">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="96d7f-106">Es posible que esté familiarizado con una característica similar en Microsoft Visual Studio Code denominada paleta de comandos [,][VisualStudioCodeUICommandPalette]que fue la inspiración original del menú de comandos.</span><span class="sxs-lookup"><span data-stu-id="96d7f-106">You may be familiar with a similar feature in Microsoft Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Uso del menú comando para deshabilitar JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   <span data-ttu-id="96d7f-108">Uso del menú comando para deshabilitar JavaScript</span><span class="sxs-lookup"><span data-stu-id="96d7f-108">Using the Command Menu to disable JavaScript</span></span>  
:::image-end:::  

## <a name="open-the-command-menu"></a><span data-ttu-id="96d7f-109">Abrir el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="96d7f-109">Open the Command Menu</span></span>  

<span data-ttu-id="96d7f-110">Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="96d7f-110">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="96d7f-111">O elija **Personalizar y controlar DevTools** \( `...` \) > Ejecutar **comando**.</span><span class="sxs-lookup"><span data-stu-id="96d7f-111">Or choose **Customize And Control DevTools** \(`...`\) > **Run Command**.</span></span>  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Ejecutar comando" lightbox="../media/command-menu-options-run-command.msft.png":::
   <span data-ttu-id="96d7f-113">Ejecutar comando</span><span class="sxs-lookup"><span data-stu-id="96d7f-113">Run Command</span></span>  
:::image-end:::  

## <a name="display-other-available-actions"></a><span data-ttu-id="96d7f-114">Mostrar otras acciones disponibles</span><span class="sxs-lookup"><span data-stu-id="96d7f-114">Display other available actions</span></span>  

<span data-ttu-id="96d7f-115">Si usa el flujo de trabajo descrito en [Abrir el](#open-the-command-menu)menú de comandos , el menú comando se abre con un carácter previamente escrito en el cuadro de texto Menú `>` de comandos.</span><span class="sxs-lookup"><span data-stu-id="96d7f-115">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character pre-pended to the Command Menu text box.</span></span>  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="El carácter de comando" lightbox="../media/command-menu-run-command.msft.png":::
   <span data-ttu-id="96d7f-117">El carácter de comando</span><span class="sxs-lookup"><span data-stu-id="96d7f-117">The command character</span></span>  
:::image-end:::  

<span data-ttu-id="96d7f-118">Elimine el `>` carácter y el tipo para mostrar `?` otras acciones que están disponibles en el menú comando.</span><span class="sxs-lookup"><span data-stu-id="96d7f-118">Delete the `>` character and type `?` to display other actions that are available from the Command Menu.</span></span>  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Otras acciones disponibles" lightbox="../media/command-menu-help.msft.png":::
   <span data-ttu-id="96d7f-120">Otras acciones disponibles</span><span class="sxs-lookup"><span data-stu-id="96d7f-120">Other available actions</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="96d7f-121">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="96d7f-121">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Deshabilitar JavaScript con Microsoft Edge DevTools | Microsoft Docs"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Paleta de comandos: Visual Studio Code interfaz de usuario"  

> [!NOTE]
> <span data-ttu-id="96d7f-124">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96d7f-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="96d7f-125">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="96d7f-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="96d7f-127">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="96d7f-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
