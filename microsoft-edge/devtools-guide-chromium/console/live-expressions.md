---
description: Si en la consola se encuentra escribiendo las mismas expresiones de JavaScript varias veces, pruebe las expresiones en vivo.
title: Ver valores de expresiones de JavaScript en tiempo real con expresiones en vivo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6b66c44b77cd50bc0c1575e5eceb7c8d1a01b709
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993117"
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





# <span data-ttu-id="6522e-104">Ver valores de expresiones de JavaScript en tiempo real con expresiones en vivo</span><span class="sxs-lookup"><span data-stu-id="6522e-104">Watch JavaScript Expression Values In Real-Time With Live Expressions</span></span>   

  

<span data-ttu-id="6522e-105">Si se encuentra escribiendo la misma expresión de JavaScript en la consola varias veces, es posible que le resulte más fácil crear una **expresión en vivo**.</span><span class="sxs-lookup"><span data-stu-id="6522e-105">If you find yourself typing the same JavaScript expression in the Console repeatedly, you might find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="6522e-106">Con **expresiones en vivo** , escriba una expresión una vez y, a continuación, ancle en la parte superior de la consola.</span><span class="sxs-lookup"><span data-stu-id="6522e-106">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="6522e-107">El valor de la expresión se actualiza casi en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="6522e-107">The value of the expression updates in near real-time.</span></span>  

## <span data-ttu-id="6522e-108">Crear una expresión en directo</span><span class="sxs-lookup"><span data-stu-id="6522e-108">Create a Live Expression</span></span>   

1.  <span data-ttu-id="6522e-109">[Abra la consola][DevToolsConsoleReferenceOpenConsole].</span><span class="sxs-lookup"><span data-stu-id="6522e-109">[Open the Console][DevToolsConsoleReferenceOpenConsole].</span></span>  
1.  <span data-ttu-id="6522e-110">Haga clic en **crear expresión en directo** \ ( ![ crear expresión en directo ][ImageCreateLiveExpressionIcon] \).</span><span class="sxs-lookup"><span data-stu-id="6522e-110">Click **Create Live Expression** \(![Create Live Expression][ImageCreateLiveExpressionIcon]\).</span></span>  <span data-ttu-id="6522e-111">Aparece el cuadro de texto de la **expresión en vivo** .</span><span class="sxs-lookup"><span data-stu-id="6522e-111">The **Live Expression** text box appears.</span></span>  
    
    :::image type="complex" source="../media/console-create-live-expression.msft.png" alt-text="Escritura de Document. activeElement en el cuadro de texto de la expresión en directo" lightbox="../media/console-create-live-expression.msft.png":::
       <span data-ttu-id="6522e-113">Escribir `document.activeElement` en el cuadro de texto de la **expresión en directo**</span><span class="sxs-lookup"><span data-stu-id="6522e-113">Typing `document.activeElement` into the **Live Expression** text box</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6522e-114">Escriba `Control` + `Enter` \ (Windows \) o `Command` + `Enter` \ (MacOS \) para guardar la expresión o haga clic fuera del cuadro de texto de la **expresión en directo** .</span><span class="sxs-lookup"><span data-stu-id="6522e-114">Type `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\) to save the expression, or click outside of the **Live Expression** text box.</span></span>  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: ./reference.md#open-the-console "Abra Consola-referencia de consola | Microsoft docs"  

> [!NOTE]
> <span data-ttu-id="6522e-116">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6522e-116">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6522e-117">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="6522e-117">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6522e-119">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6522e-119">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
