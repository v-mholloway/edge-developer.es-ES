---
title: Rastrear qué elemento tiene el foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5261824b725384240453f216071255494e88e98d
ms.sourcegitcommit: 2fa65cca74c5214601900579c0ce9f946ad8a27e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10991172"
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

# <span data-ttu-id="4e6c6-103">Rastrear qué elemento tiene el foco</span><span class="sxs-lookup"><span data-stu-id="4e6c6-103">Track Which Element Has Focus</span></span>  

<span data-ttu-id="4e6c6-104">Suponga que está probando la accesibilidad de navegación por el teclado de una página.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-104">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="4e6c6-105">Al navegar por la página con la `Tab` tecla, el anillo de foco desaparece a veces, porque el elemento que tiene el foco está oculto.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-105">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="4e6c6-106">Complete las acciones siguientes para realizar un seguimiento del elemento que tiene el foco en DevTools.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-106">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="4e6c6-107">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-107">Open the **Console**.</span></span>  
1.  <span data-ttu-id="4e6c6-108">Haga clic en **crear expresión en directo** \ ( ![ crear expresión en directo ][ImageCreateIcon] \).</span><span class="sxs-lookup"><span data-stu-id="4e6c6-108">Click **Create Live Expression** \(![Create Live Expression][ImageCreateIcon]\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Crear una expresión en directo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="4e6c6-110">Crear una expresión en directo</span><span class="sxs-lookup"><span data-stu-id="4e6c6-110">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="4e6c6-111">Escribe `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-111">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="4e6c6-112">Haga clic fuera de la interfaz de usuario de **Live Expression** para guardar.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-112">Click outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="4e6c6-113">El valor que se ve a continuación `document.activeElement` es el resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-113">The value that you see below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="4e6c6-114">Dado que esa expresión siempre representa el elemento que tiene el foco, ahora tienes una manera de realizar un seguimiento de qué elemento tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-114">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="4e6c6-115">Desplace el puntero sobre el resultado para resaltar el elemento que tiene el foco en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-115">Hover over the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="4e6c6-116">Haga clic con el botón derecho en el resultado y seleccione Mostrar **en el panel de elementos** para mostrar el elemento en el árbol DOM en el panel **elementos** .</span><span class="sxs-lookup"><span data-stu-id="4e6c6-116">Right-click the result and select **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** panel.</span></span>  
*   <span data-ttu-id="4e6c6-117">Haga clic con el botón secundario en el resultado y seleccione **almacenar como variable global** para crear una referencia de variable al nodo que se puede usar en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="4e6c6-117">Right-click the result and select **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <span data-ttu-id="4e6c6-118">Ponerse en contacto con el equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4e6c6-118">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCreateIcon]: ../media/create-live-expression-icon.msft.png  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="4e6c6-119">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e6c6-119">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4e6c6-120">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="4e6c6-120">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4e6c6-122">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e6c6-122">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
