---
title: Marcar scripts de contenido como código de biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a5101cb8561a49ce6c271398f4c1a828984da9e3
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991160"
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

# <span data-ttu-id="ac4f2-103">Marcar las secuencias de comandos de contenido como código de biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac4f2-103">Mark content scripts as Library code</span></span>  

<span data-ttu-id="ac4f2-104">Al usar el panel **orígenes** de la DevTools de Microsoft Edge para [recorrer el código][DevToolsJavascriptStepThroughCode], a veces deténgase en el código que no reconoce.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-104">When using the **Sources** panel of Microsoft Edge DevTools to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you do not recognize.</span></span>  <span data-ttu-id="ac4f2-105">Probablemente hayas pausado el código para una de las extensiones de Microsoft Edge que instalaste.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-105">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="ac4f2-106">Complete los pasos siguientes para no hacer una pausa en el código de extensión.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-106">Complete the following steps to not pause on extension code.</span></span>  

1.  <span data-ttu-id="ac4f2-107">Abra DevTools, seleccione **personalizar y controle DevTools** \ ( `...` \) y seleccione **configuración**.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-107">Open DevTools, select **Customize and control DevTools** \(`...`\) and choose **Settings**.</span></span>  <span data-ttu-id="ac4f2-108">También puede abrir la **configuración** seleccionando `F1` .</span><span class="sxs-lookup"><span data-stu-id="ac4f2-108">You may also open **Settings** by selecting `F1`.</span></span>  

1.  <span data-ttu-id="ac4f2-109">Seleccione la pestaña **código de biblioteca** que abre la sección código de la biblioteca de **Marcos** de **configuración**.</span><span class="sxs-lookup"><span data-stu-id="ac4f2-109">Select the **Library code** tab which opens the **Framework Library Code** section of **Settings**.</span></span>  
1.  <span data-ttu-id="ac4f2-110">Active la casilla **marcar scripts de contenido como código de biblioteca** .</span><span class="sxs-lookup"><span data-stu-id="ac4f2-110">Enable the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Active la casilla marcar scripts de contenido como código de biblioteca" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="ac4f2-112">Active la casilla **marcar scripts de contenido como código de biblioteca**</span><span class="sxs-lookup"><span data-stu-id="ac4f2-112">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ac4f2-113">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ac4f2-113">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Paso 4: desplazarse por el código: Introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="ac4f2-115">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ac4f2-115">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ac4f2-116">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ac4f2-116">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ac4f2-118">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ac4f2-118">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
