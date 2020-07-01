---
title: Simular un movimiento reducido con herramientas de desarrollo (CSS prefiere reducir el movimiento)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f1bf90de4ac1832fff07e9ac963c26f92adeea2c
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843987"
---
# <span data-ttu-id="61170-103">Simulación de movimiento reducida</span><span class="sxs-lookup"><span data-stu-id="61170-103">Reduced Motion Simulation</span></span>  

<span data-ttu-id="61170-104">La animación en productos Web puede ser un problema de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="61170-104">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="61170-105">Los sistemas operativos se enfrentan al problema incluyendo una opción para desactivar las animaciones para evitar la confusión de los usuarios y posibles problemas relacionados con el estado, como desencadenar ataques.</span><span class="sxs-lookup"><span data-stu-id="61170-105">Operating Systems deal with the problem by including an option to turn off animations to avoid user confusion and potential health related problems such as triggering seizures.</span></span>  <span data-ttu-id="61170-106">En la web, puede usar la consulta de medios [preferidas, de CSS de movimiento reducido][MDNPrefersReducedMotion] para detectar si los usuarios prefieren ver las animaciones.</span><span class="sxs-lookup"><span data-stu-id="61170-106">On the web, you may use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS Media Query to detect if users prefer to not see any animations.</span></span>  <span data-ttu-id="61170-107">En el producto, puede ajustar el código de la animación en una prueba para evitar que se muestren animaciones para los usuarios afectados.</span><span class="sxs-lookup"><span data-stu-id="61170-107">In your product, you may wrap your animation code in a test to avoid animations showing up for the affected users.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="61170-108">Con el [DevTools de Microsoft Edge][DevtoolsGuideChromiumMain], puede simular esta configuración de movimiento reducida sin necesidad de cambiar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="61170-108">Using the [Microsoft Edge DevTools][DevtoolsGuideChromiumMain], you may simulate this reduced motion setting without having to change your operating system.</span></span>  

1.  <span data-ttu-id="61170-109">Abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="61170-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="61170-110">Pulse `Control` + `Shift` + `P` en Windows o `Command` + `Shift` + `P` en MacOS.</span><span class="sxs-lookup"><span data-stu-id="61170-110">Press `Control`+`Shift`+`P`  on Windows or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="61170-112">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="61170-112">The **Command Menu**</span></span>  
        :::image-end:::   
        
1.  <span data-ttu-id="61170-113">Escriba `reduced` para activar y desactivar la simulación.</span><span class="sxs-lookup"><span data-stu-id="61170-113">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="61170-114">Seleccione la opción y pulse `Enter` .</span><span class="sxs-lookup"><span data-stu-id="61170-114">Select the option and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activar o desactivar la opción de configuración reducir el movimiento preferido desde el menú de comandos" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="61170-116">Activar o desactivar la opción de configuración **reducir el movimiento preferido** desde el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="61170-116">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="61170-117">Actualice la página actual para comprobar si las animaciones están activadas o visibles.</span><span class="sxs-lookup"><span data-stu-id="61170-117">Refresh the current page to test whether your animations are turned off or visible.</span></span>  
    
<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Ilustración 1: el menú de comandos"  
[ImageToggleReducedMotionFromCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png "Ilustración 2: conmutar movimiento reducido desde la paleta de comandos"

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Herramientas para desarrolladores de Microsoft Edge (cromo) Microsoft | Microsoft docs"  

[MDNPrefersReducedMotion]: https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion "preferido: ahorro: movimiento | MDN"  
