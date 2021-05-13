---
description: Abra la consola, cree una expresión en directo y establezca la expresión en document.activeElement.
title: Rastrear qué elemento tiene el foco
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e7d7bc9ebf8dd891bf7531d8dd283801a01fc3c1
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564598"
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
# <a name="track-which-element-has-focus"></a><span data-ttu-id="05223-104">Rastrear qué elemento tiene el foco</span><span class="sxs-lookup"><span data-stu-id="05223-104">Track which element has focus</span></span>  

<span data-ttu-id="05223-105">Supongamos que está probando la accesibilidad de navegación del teclado de una página.</span><span class="sxs-lookup"><span data-stu-id="05223-105">Suppose that you are testing the keyboard navigation accessibility of a page.</span></span>  <span data-ttu-id="05223-106">Al navegar por la página con la clave, el anillo de enfoque a veces desaparece porque `Tab` el elemento que tiene el foco está oculto.</span><span class="sxs-lookup"><span data-stu-id="05223-106">When navigating the page with the `Tab` key, the focus ring sometimes disappears because the element that has focus is hidden.</span></span>  

<span data-ttu-id="05223-107">Complete las siguientes acciones para realizar un seguimiento del elemento centrado en DevTools.</span><span class="sxs-lookup"><span data-stu-id="05223-107">Complete the following actions to track the focused element in DevTools.</span></span>  

1.  <span data-ttu-id="05223-108">Abra la **consola**.</span><span class="sxs-lookup"><span data-stu-id="05223-108">Open the **Console**.</span></span>  
1.  <span data-ttu-id="05223-109">Elija **Crear expresión en directo** \( Crear expresión en directo ![ ](../media/create-live-expression-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="05223-109">Choose **Create Live Expression** \(![Create Live Expression](../media/create-live-expression-icon.msft.png)\).</span></span>  
    
    :::image type="complex" source="../media/accessibility-console-create-live-expression-empty.msft.png" alt-text="Crear una expresión en directo" lightbox="../media/accessibility-console-create-live-expression-empty.msft.png":::
       <span data-ttu-id="05223-111">Crear una expresión en directo</span><span class="sxs-lookup"><span data-stu-id="05223-111">Create a Live Expression</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="05223-112">Escriba `document.activeElement`.</span><span class="sxs-lookup"><span data-stu-id="05223-112">Type `document.activeElement`.</span></span>  
1.  <span data-ttu-id="05223-113">Elige fuera de la **interfaz de usuario de Expresión** en directo para guardar.</span><span class="sxs-lookup"><span data-stu-id="05223-113">Choose outside of the **Live Expression** UI to save.</span></span>  
    
<span data-ttu-id="05223-114">El valor que se muestra `document.activeElement` a continuación es el resultado de la expresión.</span><span class="sxs-lookup"><span data-stu-id="05223-114">The value displayed below `document.activeElement` is the result of the expression.</span></span>  

<span data-ttu-id="05223-115">Dado que esa expresión siempre representa el elemento centrado, ahora tiene una forma de realizar siempre un seguimiento de qué elemento tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="05223-115">Since that expression always represents the focused element, you now have a way to always keep track of which element has focus.</span></span>  

*   <span data-ttu-id="05223-116">Mantenga el mouse sobre el resultado para resaltar el elemento centrado en la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="05223-116">Hover on the result to highlight the focused element in the viewport.</span></span>  
*   <span data-ttu-id="05223-117">Mantenga el mouse sobre el resultado, abra el menú contextual \(clic con el botón derecho\) y elija Mostrar en el **panel** Elementos para mostrar el elemento en el árbol DOM de la **herramienta** Elementos.</span><span class="sxs-lookup"><span data-stu-id="05223-117">Hover on the result, open the contextual menu \(right-click\), and choose **Reveal in Elements panel** to show the element in the DOM Tree on the **Elements** tool.</span></span>  
*   <span data-ttu-id="05223-118">Mantenga el mouse sobre el resultado, abra el menú contextual \(haga clic con el botón secundario\) y elija Almacenar como **variable global** para crear una referencia variable al nodo que puede usar en la **consola**.</span><span class="sxs-lookup"><span data-stu-id="05223-118">Hover on the result, open the contextual menu \(right-click\), and choose **Store as global variable** to create a variable reference to the node that you are able to use in the **Console**.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="05223-119">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="05223-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="05223-120">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="05223-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="05223-121">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="05223-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/accessibility/focus) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="05223-123">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="05223-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
