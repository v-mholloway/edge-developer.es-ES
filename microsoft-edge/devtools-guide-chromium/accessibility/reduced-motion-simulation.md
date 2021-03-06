---
description: Simular movimiento reducido con herramientas de desarrollador.
title: Simular movimiento reducido con herramientas de desarrollador (CSS prefiere el movimiento reducido)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 29cdbd7492665e819315910b3f743d444470cc12
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397870"
---
# <a name="reduced-motion-simulation"></a><span data-ttu-id="edacb-104">Simulación de movimiento reducida</span><span class="sxs-lookup"><span data-stu-id="edacb-104">Reduced motion simulation</span></span>  

<span data-ttu-id="edacb-105">La animación en productos web puede ser un problema de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="edacb-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="edacb-106">Los sistemas operativos tratan el problema mediante la inclusión de una opción para desactivar animaciones para evitar confusiones del usuario y posibles problemas relacionados con el estado, como desencadenar ataques.</span><span class="sxs-lookup"><span data-stu-id="edacb-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="edacb-107">En la web, puede usar la consulta multimedia CSS [prefers-reduced-motion][MDNPrefersReducedMotion] para detectar si los usuarios prefieren no ejecutar o mostrar animaciones.</span><span class="sxs-lookup"><span data-stu-id="edacb-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not run or display any animations.</span></span>  <span data-ttu-id="edacb-108">En el producto, puedes ajustar el código de animación en una prueba para evitar que se muestren animaciones para los usuarios afectados.</span><span class="sxs-lookup"><span data-stu-id="edacb-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="edacb-109">Con Microsoft [Edge DevTools,][DevtoolsIndex]puedes simular esta configuración de movimiento reducido sin tener que cambiar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="edacb-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="edacb-110">Abra el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="edacb-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="edacb-111">Selecciona `Control` + `Shift` + `P` en Windows/Linux o `Command` + `Shift` + `P` en macOS.</span><span class="sxs-lookup"><span data-stu-id="edacb-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="edacb-113">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="edacb-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="edacb-114">Escriba `reduced` , para activar y desactivar la simulación.</span><span class="sxs-lookup"><span data-stu-id="edacb-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="edacb-115">Elija la opción y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="edacb-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activar o desactivar la configuración de movimiento reducido preferido desde el menú comando" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="edacb-117">Activar o desactivar la configuración **de movimiento reducido** preferido desde el menú **comando**</span><span class="sxs-lookup"><span data-stu-id="edacb-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="edacb-118">Actualice la página actual para comprobar si las animaciones están desactivadas o visibles.</span><span class="sxs-lookup"><span data-stu-id="edacb-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
