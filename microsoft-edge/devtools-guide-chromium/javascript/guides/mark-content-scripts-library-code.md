---
description: Habilite "Marcar scripts de contenido como código de biblioteca" en Configuración > código de biblioteca de Framework.
title: Marcar scripts de contenido como código de biblioteca
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c1571ab909aac09e4593413e96f7d4b7723c7759
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519348"
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

# <a name="mark-content-scripts-as-library-code"></a><span data-ttu-id="ee285-104">Marcar scripts de contenido como código de biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee285-104">Mark content scripts as Library code</span></span>  

<span data-ttu-id="ee285-105">Cuando usa la herramienta **Orígenes** para pasar por [el código,][DevToolsJavascriptStepThroughCode]a veces se pausa en el código que no reconoce.</span><span class="sxs-lookup"><span data-stu-id="ee285-105">When you use the **Sources** tool to [step through code][DevToolsJavascriptStepThroughCode], sometimes you pause on code that you don't recognize.</span></span>  <span data-ttu-id="ee285-106">Probablemente haya pausado el código para una de las extensiones de Microsoft Edge que instaló.</span><span class="sxs-lookup"><span data-stu-id="ee285-106">You probably paused on code for one of the Microsoft Edge Extensions that you installed.</span></span>  <span data-ttu-id="ee285-107">Para no pausar el código de extensión, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="ee285-107">To not pause on extension code, complete the following actions.</span></span>  

1.  <span data-ttu-id="ee285-108">En DevTools, en la parte superior derecha, elija el icono de engranaje (**Configuración**).</span><span class="sxs-lookup"><span data-stu-id="ee285-108">In DevTools, in the upper right, choose the gear icon (**Settings**).</span></span>  <span data-ttu-id="ee285-109">Aparece la página **Settings**.</span><span class="sxs-lookup"><span data-stu-id="ee285-109">The **Settings** page appears.</span></span>  
1.  <span data-ttu-id="ee285-110">Debajo **de Configuración,** elija **Omitir lista**.</span><span class="sxs-lookup"><span data-stu-id="ee285-110">Below **Settings**, choose **Ignore List**.</span></span>  <span data-ttu-id="ee285-111">Aparece **la sección Código de biblioteca** de marcos de **Configuración.**</span><span class="sxs-lookup"><span data-stu-id="ee285-111">The **Framework Library Code** section of **Settings** appears.</span></span>  
1.  <span data-ttu-id="ee285-112">Active la casilla **Marcar scripts de contenido como código de biblioteca.**</span><span class="sxs-lookup"><span data-stu-id="ee285-112">Turn on the **Mark content scripts as Library code** checkbox.</span></span>  
    
    :::image type="complex" source="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png" alt-text="Habilitar la casilla Marcar scripts de contenido como código de biblioteca" lightbox="../../media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png":::
       <span data-ttu-id="ee285-114">Habilitar la casilla **Marcar scripts de contenido como código de biblioteca**</span><span class="sxs-lookup"><span data-stu-id="ee285-114">Enable the **Mark content scripts as Library code** checkbox</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ee285-115">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ee285-115">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Paso 4: Paso a paso por el código: introducción a la depuración de JavaScript en Microsoft Edge DevTools | Microsoft Docs"  

> [!NOTE]
> <span data-ttu-id="ee285-117">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ee285-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ee285-118">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="ee285-118">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ee285-120">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ee285-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
