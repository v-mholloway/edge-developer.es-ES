---
description: Simular el movimiento reducido con las herramientas de desarrollo.
title: Simular un movimiento reducido con herramientas de desarrollo (CSS prefiere reducir el movimiento)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0e5243e01ca6c9344dceffb0bf004dadccc3d4d7
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230792"
---
# <span data-ttu-id="078b9-104">Simulación de movimiento reducida</span><span class="sxs-lookup"><span data-stu-id="078b9-104">Reduced Motion Simulation</span></span>  

<span data-ttu-id="078b9-105">La animación en productos Web puede ser un problema de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="078b9-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="078b9-106">Los sistemas operativos se enfrentan al problema incluyendo una opción para desactivar las animaciones para evitar la confusión de los usuarios y posibles problemas relacionados con el estado, como desencadenar ataques.</span><span class="sxs-lookup"><span data-stu-id="078b9-106">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="078b9-107">En la web, puede usar la consulta de medios [preferidas, de CSS de movimiento reducido][MDNPrefersReducedMotion] para detectar si los usuarios prefieren ver las animaciones.</span><span class="sxs-lookup"><span data-stu-id="078b9-107">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="078b9-108">En el producto, puede ajustar el código de la animación en una prueba para evitar que se muestren animaciones para los usuarios afectados.</span><span class="sxs-lookup"><span data-stu-id="078b9-108">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="078b9-109">Con el [DevTools de Microsoft Edge][DevtoolsIndex], puede simular esta configuración de movimiento reducida sin necesidad de cambiar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="078b9-109">Using the [Microsoft Edge DevTools][DevtoolsIndex], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="078b9-110">Abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="078b9-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="078b9-111">Seleccione `Control` + `Shift` + `P` en Windows/Linux o `Command` + `Shift` + `P` en MacOS.</span><span class="sxs-lookup"><span data-stu-id="078b9-111">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="078b9-113">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="078b9-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="078b9-114">Escriba `reduced` para activar y desactivar la simulación.</span><span class="sxs-lookup"><span data-stu-id="078b9-114">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="078b9-115">Elija la opción y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="078b9-115">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activar o desactivar la opción de configuración reducir el movimiento preferido desde el menú de comandos" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="078b9-117">Activar o desactivar la opción de configuración **reducir el movimiento preferido** desde el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="078b9-117">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="078b9-118">Actualice la página actual para comprobar si las animaciones están activadas o visibles.</span><span class="sxs-lookup"><span data-stu-id="078b9-118">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "preferido: ahorro: movimiento | MDN"  
