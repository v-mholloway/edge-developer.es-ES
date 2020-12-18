---
Description: Forzar que Microsoft Edge DevTools en el modo de vista previa de combinación de colores.
title: Forzar el modo de vista previa de la combinación de colores de Microsoft Edge DevTools (CSS prefiere la combinación de colores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 29b0121a616a037fa11b61799efeffd201eb1821
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230799"
---
# <span data-ttu-id="c23a2-104">Simulación de combinación de colores oscuro o claro</span><span class="sxs-lookup"><span data-stu-id="c23a2-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="c23a2-105">Los sistemas operativos tienen una manera de mostrar cualquier aplicación en colores más oscuros o claros.</span><span class="sxs-lookup"><span data-stu-id="c23a2-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="c23a2-106">Tener un producto Web con un tema claro en un sistema operativo de modo oscuro es Grating y puede ser un problema de accesibilidad para algunos usuarios.</span><span class="sxs-lookup"><span data-stu-id="c23a2-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="c23a2-107">En la web, puede usar la consulta de medios [preferidas-combinación de colores][MDNPrefersColorScheme] de CSS para detectar si los usuarios prefieren ver su producto en una combinación más oscura o más clara.</span><span class="sxs-lookup"><span data-stu-id="c23a2-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to see your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="c23a2-108">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] para simular un cambio de modo oscuro a claro sin tener que cambiar todo el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c23a2-108">Use [Microsoft Edge DevTools][DevtoolsGuideChromiumMain] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="c23a2-109">Abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="c23a2-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="c23a2-110">Seleccione `Control` + `Shift` + `P` en Windows/Linux o `Command` + `Shift` + `P` en MacOS.</span><span class="sxs-lookup"><span data-stu-id="c23a2-110">Select `Control`+`Shift`+`P`  on Windows/Linux or `Command`+`Shift`+`P` on macOS.</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="c23a2-112">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="c23a2-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="c23a2-113">`emulate color`En tipo, elija **EMULAr CSS preferentemente-esquema de color: oscuro** o **emular CSS preferentes-esquema de color: Light** y, a continuación, seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="c23a2-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opción de combinación de colores del menú comando" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="c23a2-115">Opción de combinación de colores del menú **comando**</span><span class="sxs-lookup"><span data-stu-id="c23a2-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="c23a2-116">Simplemente escribe `dark` o `light` no revela la herramienta adecuada, ya que también hay una forma de [elegir un tema para DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="c23a2-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsGuideChromiumCustomizeDarkTheme].</span></span>  <span data-ttu-id="c23a2-117">Si se pregunta qué elegir, asegúrese de que está seleccionando un elemento de menú de **representación** , no un elemento de menú de **apariencia** .</span><span class="sxs-lookup"><span data-stu-id="c23a2-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="c23a2-118">Después de elegir una combinación de colores, vuelva a cargar el documento actual para ver el modo simulado.</span><span class="sxs-lookup"><span data-stu-id="c23a2-118">After you choose a color scheme, reload the current document to see the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulada dentro de Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="c23a2-120">Modo de luz simulada dentro de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c23a2-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="c23a2-121">Ver y cambiar su CSS, como cualquier otra página web.</span><span class="sxs-lookup"><span data-stu-id="c23a2-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="c23a2-122">Para obtener más información, consulte Introducción [a la visualización y el cambio de CSS][DevtoolsGuideChromiumCssIndex].</span><span class="sxs-lookup"><span data-stu-id="c23a2-122">For more information, see [Get Started With Viewing And Changing CSS][DevtoolsGuideChromiumCssIndex].</span></span>  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsGuideChromiumCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema oscuro en Microsoft Edge DevTools | Microsoft docs"
[DevtoolsGuideChromiumCssIndex]: ../css/index.md "Introducción a la visualización y el cambio de CSS | Microsoft docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "preferida-combinación de colores | MDN"  
