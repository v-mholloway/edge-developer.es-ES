---
title: Abrir Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 48f80ea9f85bd3509f2ba3d834f99c25247c0761
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601890"
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
   limitations under the License. -->





# <span data-ttu-id="7508e-103">Abrir Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7508e-103">Open Microsoft Edge DevTools</span></span>   



<span data-ttu-id="7508e-104">Hay muchas maneras de abrir Microsoft Edge DevTools, ya que cada usuario desea obtener acceso rápido a distintas partes de la interfaz de usuario de DevTools.</span><span class="sxs-lookup"><span data-stu-id="7508e-104">There are many ways to open Microsoft Edge DevTools, because different users want fast access to different parts of the DevTools UI.</span></span>  

## <span data-ttu-id="7508e-105">Abrir el panel elementos para inspeccionar el DOM o CSS</span><span class="sxs-lookup"><span data-stu-id="7508e-105">Open the Elements panel to inspect the DOM or CSS</span></span>   

<span data-ttu-id="7508e-106">Cuando desee inspeccionar los estilos o los atributos de un nodo DOM, haga clic con el botón derecho en el elemento y seleccione **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="7508e-106">When you want to inspect the styles or attributes of a DOM node, right-click the element and select **Inspect**.</span></span>  

> ##### <span data-ttu-id="7508e-107">Figura 1</span><span class="sxs-lookup"><span data-stu-id="7508e-107">Figure 1</span></span>  
> <span data-ttu-id="7508e-108">La opción **inspeccionar**</span><span class="sxs-lookup"><span data-stu-id="7508e-108">The **Inspect** option</span></span>  
> ![La opción inspeccionar][ImageInspectOption]  

<span data-ttu-id="7508e-110">O pulse `Control` + `Shift` + `C` \ (Windows \) o `Command` + `Option` + `C` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="7508e-110">Or press `Control`+`Shift`+`C` \(Windows\) or `Command`+`Option`+`C` \(macOS\).</span></span>  

<!--See [Get Started With Viewing And Changing CSS][GetStartedCSS].  -->  

## <span data-ttu-id="7508e-111">Abrir el panel de consola para ver mensajes registrados o ejecutar JavaScript</span><span class="sxs-lookup"><span data-stu-id="7508e-111">Open the Console panel to view logged messages or run JavaScript</span></span>   

<span data-ttu-id="7508e-112">Pulsa `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \) para ir directamente al panel de la **consola** .</span><span class="sxs-lookup"><span data-stu-id="7508e-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to jump straight into the **Console** panel.</span></span>  

<!--See [Get Started With The Console][ConsoleGetStarted].  -->

## <span data-ttu-id="7508e-113">Abrir el último panel que tenía abierto</span><span class="sxs-lookup"><span data-stu-id="7508e-113">Open the last panel you had open</span></span>   

<span data-ttu-id="7508e-114">Pulse `Control` + `Shift` + `I` \ (Windows \) o `Command` + `Option` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="7508e-114">Press `Control`+`Shift`+`I` \(Windows\) or `Command`+`Option`+`I` \(macOS\).</span></span>  

## <span data-ttu-id="7508e-115">Abrir DevTools desde el menú principal de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7508e-115">Open DevTools from the Microsoft Edge main menu</span></span>  

<span data-ttu-id="7508e-116">Haga clic en **configuración y más (Alt + F \)** `...` y, a continuación, seleccione **más**herramientas  >  **herramientas para desarrolladores**.</span><span class="sxs-lookup"><span data-stu-id="7508e-116">Click **Settings and more \(Alt+F\)** `...` and then select **More Tools** > **Developer Tools**.</span></span>  

> ##### <span data-ttu-id="7508e-117">Figura 2</span><span class="sxs-lookup"><span data-stu-id="7508e-117">Figure 2</span></span>  
> <span data-ttu-id="7508e-118">Abrir DevTools desde el menú principal de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7508e-118">Opening DevTools from the Microsoft Edge main menu</span></span>  
> ![Abrir DevTools desde el menú principal de Microsoft Edge][ImageOpenFromMain]  

## <span data-ttu-id="7508e-120">DevTools de apertura automática en todas las pestañas nuevas</span><span class="sxs-lookup"><span data-stu-id="7508e-120">Auto-open DevTools on every new tab</span></span>   

<span data-ttu-id="7508e-121">Abra Microsoft Edge desde la línea de comandos y pase la `--auto-open-devtools-for-tabs` bandera.</span><span class="sxs-lookup"><span data-stu-id="7508e-121">Open Microsoft Edge from the command line and pass the `--auto-open-devtools-for-tabs` flag.</span></span>  

<span data-ttu-id="7508e-122">Windows \ (CMD \):</span><span class="sxs-lookup"><span data-stu-id="7508e-122">Windows \(CMD\):</span></span>  

```cmd
start msedge --auto-open-devtools-for-tabs
```  

<span data-ttu-id="7508e-123">Windows \ (PowerShell \):</span><span class="sxs-lookup"><span data-stu-id="7508e-123">Windows \(PowerShell\):</span></span>  

```powershell
Start-Process -FilePath "msedge" -ArgumentList "--auto-open-devtools-for-tabs"
```  

<span data-ttu-id="7508e-124">MacOS</span><span class="sxs-lookup"><span data-stu-id="7508e-124">macOS:</span></span>  

```bash
/Applications/Microsoft\ Edge\ Beta.app/Contents/MacOS/Microsoft\ Edge\ Beta --auto-open-devtools-for-tabs
```  

 



<!-- image links -->  

[ImagesMainIcon]: /microsoft-edge/devtools-guide-chromium/media/main-menu-icon.msft.png  

[ImageInspectOption]: /microsoft-edge/devtools-guide-chromium/media/bing-right-click-inspect.msft.png "Ilustración 1: la opción inspeccionar"  
[ImageOpenFromMain]: /microsoft-edge/devtools-guide-chromium/media/bing-customize-more-tools-developer-tools-transparent.msft.png "Ilustración 2: abrir DevTools desde el menú principal de Microsoft Edge"  

<!-- links -->  

<!--[ConsoleGetStarted]: /microsoft-edge/devtools-guide-chromium/console/get-started ""  -->  
<!--[GetStartedCSS]: /microsoft-edge/devtools-guide-chromium/css "CSS"  -->

> [!NOTE]
> <span data-ttu-id="7508e-127">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7508e-127">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7508e-128">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/open) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7508e-128">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/open) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7508e-130">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7508e-130">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
