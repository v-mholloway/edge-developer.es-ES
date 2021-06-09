---
description: Simular movimiento reducido con herramientas de desarrollador.
title: Simular movimiento reducido con herramientas de desarrollador (CSS prefiere el movimiento reducido)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7244c2e80bbf9070214b6abd02583792c785953c
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597057"
---
# <a name="reduced-motion-simulation"></a><span data-ttu-id="386af-104">Simulación de movimiento reducida</span><span class="sxs-lookup"><span data-stu-id="386af-104">Reduced motion simulation</span></span>  

<span data-ttu-id="386af-105">La animación en productos web puede ser un problema de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="386af-105">Animation in web products may be an accessibility problem.</span></span>  <span data-ttu-id="386af-106">Los sistemas operativos tratan este problema al incluir una opción para desactivar animaciones para evitar confusiones del usuario y posibles problemas relacionados con el estado, como desencadenar ataques.</span><span class="sxs-lookup"><span data-stu-id="386af-106">Operating systems deal with this problem by including an option to turn off animations to avoid user confusion and potential health-related problems, such as triggering seizures.</span></span>  

<span data-ttu-id="386af-107">En una página web, puede usar la consulta multimedia [CSS][MDNPrefersReducedMotion] de movimiento reducido preferido para detectar si el usuario prefiere mostrar animaciones.</span><span class="sxs-lookup"><span data-stu-id="386af-107">On a webpage, you can use the [prefers-reduced-motion][MDNPrefersReducedMotion] CSS media query to detect whether the user prefers to display any animations.</span></span>  <span data-ttu-id="386af-108">A continuación, ajusta el código de animación en una prueba para ejecutar animaciones condicionalmente.</span><span class="sxs-lookup"><span data-stu-id="386af-108">Then wrap your animation code in a test, to conditionally run animations.</span></span>  

```css
@media (prefers-reduced-motion: reduce) {
  /* in case the .header element has an animation, turn it off */
  .header {
    animation: none;
  }
}
```  

<span data-ttu-id="386af-109">A continuación, pruebe el código de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="386af-109">Then test your code, as follows.</span></span>

<span data-ttu-id="386af-110">Para simular la configuración de movimiento reducido del sistema operativo, sin tener que cambiar la configuración del sistema operativo:</span><span class="sxs-lookup"><span data-stu-id="386af-110">To simulate the operating system's reduced motion setting, without having to change your operating system setting:</span></span>

1.  <span data-ttu-id="386af-111">Abra el **Menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="386af-111">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="386af-112">Seleccione `Control` + `Shift` + `P` en Windows/Linux o `Command` + `Shift` + `P` en macOS.</span><span class="sxs-lookup"><span data-stu-id="386af-112">Select `Control`+`Shift`+`P` on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="386af-114">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="386af-114">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="386af-115">Escriba `reduced` , para activar y desactivar la simulación.</span><span class="sxs-lookup"><span data-stu-id="386af-115">Type `reduced`, to turn the simulation on and off.</span></span>  <span data-ttu-id="386af-116">Elija la opción y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="386af-116">Choose the option and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png" alt-text="Activar o desactivar la configuración de movimiento reducido preferido desde el menú comando" lightbox="../media/css-elements-styles-qs-select-reduced-motion-command-menu.msft.png":::
       <span data-ttu-id="386af-118">Activar o desactivar la configuración **de movimiento reducido** preferido desde el menú **comando**</span><span class="sxs-lookup"><span data-stu-id="386af-118">Turn on or off the **prefers reduced motion** setting from **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="386af-119">Actualice la página web y compruebe si se ejecutan las animaciones.</span><span class="sxs-lookup"><span data-stu-id="386af-119">Refresh the webpage and check whether your animations run.</span></span>


## <a name="see-also"></a><span data-ttu-id="386af-120">Consulta también</span><span class="sxs-lookup"><span data-stu-id="386af-120">See also</span></span>

* <span data-ttu-id="386af-121">[Compruebe que la página se puede usar con la animación](test-reduced-ui-motion.md) de la interfaz de usuario desactivada: un tutorial con una página de demostración, con explicaciones.</span><span class="sxs-lookup"><span data-stu-id="386af-121">[Verify that the page is usable with UI animation turned off](test-reduced-ui-motion.md) - A walkthrough using a demo page, with explanations.</span></span>

    
<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[MDNPrefersReducedMotion]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-reduced-motion "prefers-reduced-motion | MDN"  
