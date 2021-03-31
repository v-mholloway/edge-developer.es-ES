---
description: Forzar Microsoft Edge DevTools al modo de vista previa de esquema de colores.
title: Forzar Microsoft Edge DevTools al modo de vista previa de esquema de colores (CSS prefiere la combinación de colores)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 84f482605acd6edab6829e00d5fa31f927ebc032
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398304"
---
# <a name="dark-or-light-color-scheme-simulation"></a><span data-ttu-id="509f3-104">Simulación de combinación de colores claros o oscuros</span><span class="sxs-lookup"><span data-stu-id="509f3-104">Dark or Light Color Scheme simulation</span></span>  

<span data-ttu-id="509f3-105">Los sistemas operativos tienen una forma de mostrar cualquier aplicación en colores más oscuros o más claros.</span><span class="sxs-lookup"><span data-stu-id="509f3-105">Operating systems have a way to display any application in darker or lighter colors.</span></span>  <span data-ttu-id="509f3-106">Tener un producto web que tenga un tema claro en un sistema operativo en modo oscuro es una rejilla y puede ser un problema de accesibilidad para algunos usuarios.</span><span class="sxs-lookup"><span data-stu-id="509f3-106">Having a web product that has a light theme in a dark mode operating system is grating and can be an accessibility issue for some users.</span></span>  <span data-ttu-id="509f3-107">En la web, puede usar la consulta multimedia CSS [prefers-color-scheme][MDNPrefersColorScheme] para detectar si los usuarios prefieren mostrar el producto en una combinación de colores más oscura o más clara.</span><span class="sxs-lookup"><span data-stu-id="509f3-107">On the web, you may use the [prefers-color-scheme][MDNPrefersColorScheme] CSS Media Query to detect if users prefer to display your product in a darker or lighter colour scheme.</span></span>  <span data-ttu-id="509f3-108">Usa [Microsoft Edge DevTools para][DevtoolsIndex] simular un cambio del modo oscuro a el modo claro sin tener que cambiar todo el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="509f3-108">Use [Microsoft Edge DevTools][DevtoolsIndex] to simulate a change from dark to light mode without having to change the entire operating system.</span></span>  

1.  <span data-ttu-id="509f3-109">Abra el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="509f3-109">Open the **Command Menu**.</span></span>  
    1.  <span data-ttu-id="509f3-110">Seleccione `Control` + `Shift` + `P` \(Windows/Linux\) o `Command` + `Shift` + `P` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="509f3-110">Select `Control`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\).</span></span>  
        
        :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
           <span data-ttu-id="509f3-112">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="509f3-112">The **Command Menu**</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="509f3-113">Type `emulate color` , choose either Emulate CSS **prefers-color-scheme: dark** or Emulate CSS **prefers-color-scheme: light** and then select `Enter` .</span><span class="sxs-lookup"><span data-stu-id="509f3-113">Type `emulate color`, choose either **Emulate CSS prefers-color-scheme: dark** or **Emulate CSS prefers-color-scheme: light** and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png" alt-text="Opción combinación de colores del menú comando" lightbox="../media/css-elements-styles-qs-select-renderingmode-command-menu.msft.png":::
       <span data-ttu-id="509f3-115">Opción combinación de colores del **menú** comando</span><span class="sxs-lookup"><span data-stu-id="509f3-115">Color scheme option from **Command** Menu</span></span>  
    :::image-end:::  
    
    > [!IMPORTANT]
    > <span data-ttu-id="509f3-116">Simplemente escribiendo o no revela la herramienta adecuada, ya que también hay una forma de `dark` elegir un tema para `light` [DevTools][DevtoolsCustomizeDarkTheme].</span><span class="sxs-lookup"><span data-stu-id="509f3-116">Simply typing `dark` or `light` does not reveal the right tool, since there is also a way to [choose a theme for DevTools][DevtoolsCustomizeDarkTheme].</span></span>  <span data-ttu-id="509f3-117">Si se pregunta qué elegir, asegúrese de elegir  un elemento de menú de representación, no un **elemento de** menú de apariencia.</span><span class="sxs-lookup"><span data-stu-id="509f3-117">If you are wondering what to choose, make sure that you are choosing a **rendering** menu item, not an **appearance** menu item.</span></span>  

1.  <span data-ttu-id="509f3-118">Después de elegir una combinación de colores, actualice el documento actual para mostrar el modo simulado.</span><span class="sxs-lookup"><span data-stu-id="509f3-118">After you choose a color scheme, refresh the current document to display the simulated mode.</span></span>  
    
    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Modo de luz simulada dentro de Microsoft Edge DevTools" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       <span data-ttu-id="509f3-120">Modo de luz simulada dentro de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="509f3-120">Simulated light mode inside Microsoft Edge DevTools</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="509f3-121">Ver y cambiar el CSS como cualquier otra página web.</span><span class="sxs-lookup"><span data-stu-id="509f3-121">View and change your CSS like any other web page.</span></span>  <span data-ttu-id="509f3-122">Para obtener más información, vaya [a Introducción a Ver y cambiar CSS][DevtoolsCssIndex].</span><span class="sxs-lookup"><span data-stu-id="509f3-122">For more information, navigate to [Get Started With Viewing And Changing CSS][DevtoolsCssIndex].</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsCustomizeDarkTheme]: ../customize/dark-theme.md "Habilitar tema oscuro en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y cambio de css | Microsoft Docs"  

[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
