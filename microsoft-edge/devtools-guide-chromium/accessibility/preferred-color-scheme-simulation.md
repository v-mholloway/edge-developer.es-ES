---
description: Fuerza Microsoft Edge DevTools al modo de vista previa de esquema de color.
title: Forzar Microsoft Edge DevTools en modo de vista previa de esquema de color (CSS prefiere combinación de colores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: dc2911ce7a7fcbeef7763099541822b5cd6cf053
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597066"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="d646f-104">Simulación de combinación de colores claros o oscuros</span><span class="sxs-lookup"><span data-stu-id="d646f-104">Dark or light color scheme simulation</span></span>  

<span data-ttu-id="d646f-105">Muchos sistemas operativos tienen una forma de mostrar cualquier aplicación en colores más oscuros o más claros.</span><span class="sxs-lookup"><span data-stu-id="d646f-105">Many operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="d646f-106">Tener un producto web que tiene un tema claro en un sistema operativo en modo oscuro es una rejilla y puede ser un problema de accesibilidad para algunos usuarios.</span><span class="sxs-lookup"><span data-stu-id="d646f-106">Having a web product that has a light theme in a dark-mode operating system is grating and can be an accessibility issue for some users.</span></span>  

<span data-ttu-id="d646f-107">Para una página web, puede usar la consulta multimedia CSS [prefers-color-scheme][MDNPrefersColorScheme] para detectar si el usuario prefiere mostrar el producto en una combinación de colores más oscura o más clara.</span><span class="sxs-lookup"><span data-stu-id="d646f-107">For a webpage, you can use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect whether the user prefers to display your product in a darker or lighter color scheme.</span></span>  <span data-ttu-id="d646f-108">A continuación, para probar el resultado, usa [Microsoft Edge DevTools][DevtoolsIndex] para simular un cambio del modo oscuro a claro, sin tener que cambiar la configuración de todo el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d646f-108">Then to test the result, use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode, without having to change the setting for your entire operating system.</span></span>  

**<span data-ttu-id="d646f-109">Para emular el tema oscuro o claro:</span><span class="sxs-lookup"><span data-stu-id="d646f-109">To emulate dark or light theme:</span></span>**

1.  <span data-ttu-id="d646f-110">Abra el **Menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="d646f-110">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="d646f-111">Seleccione `Ctrl` + `Shift` + `P` \(Windows/Linux\) o `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="d646f-111">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="d646f-113">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="d646f-113">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="d646f-114">Type `emulate color` , choose either Emulate CSS **prefers-color-scheme: dark** or Emulate CSS **prefers-color-scheme: light** and then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="d646f-114">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opción combinación de colores del menú comando" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="d646f-116">Opción combinación de colores del **menú** comando</span><span class="sxs-lookup"><span data-stu-id="d646f-116">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="d646f-117">Simplemente escribiendo o no revela la herramienta adecuada, ya que también hay una forma de `dark` elegir un tema para `light` [DevTools][DevtoolsCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="d646f-117">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="d646f-118">Si se pregunta qué elegir, asegúrese de elegir \*\*\*\* un elemento de menú de representación, no un **elemento de** menú de apariencia.</span><span class="sxs-lookup"><span data-stu-id="d646f-118">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="d646f-119">Después de elegir una combinación de colores, actualice el documento actual para mostrar el modo simulado.</span><span class="sxs-lookup"><span data-stu-id="d646f-119">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulada dentro Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="d646f-121">Modo de luz simulada dentro Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d646f-121">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="d646f-122">Ver y cambiar el CSS como cualquier otra página web.</span><span class="sxs-lookup"><span data-stu-id="d646f-122">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="d646f-123">Para obtener más información, vaya [a Introducción a ver y cambiar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="d646f-123">For more information, navigate to [Get started with viewing and changing CSS][DevtoolsCssIndex].</span></span>  


## <a name="see-also"></a><span data-ttu-id="d646f-124">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d646f-124">See also</span></span>

* [<span data-ttu-id="d646f-125">Comprobar si hay problemas de contraste con el tema oscuro y el tema claro</span><span class="sxs-lookup"><span data-stu-id="d646f-125">Check for contrast issues with dark theme and light theme</span></span>](test-dark-mode.md)


<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema oscuro en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y cambio de css | Microsoft Docs"  
<!-- external links -->
[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
