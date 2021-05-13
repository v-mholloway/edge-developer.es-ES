---
description: Emular las deficiencias de visión en Microsoft Edge DevTools.
title: Emular las deficiencias de la visión Microsoft Edge DevTools (daltonismo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 1ab224f1dc70618dbef77ec6e6dbc22a0d1f47fb
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564605"
---
# <a name="emulate-vision-deficiencies"></a><span data-ttu-id="616c6-104">Emular deficiencias visuales</span><span class="sxs-lookup"><span data-stu-id="616c6-104">Emulate vision deficiencies</span></span>  

<span data-ttu-id="616c6-105">Para satisfacer mejor las necesidades de los usuarios con deficiencia de visión de [color][ColorblindawarenessMain] \(daltonismo\), [Microsoft Edge DevTools][DevtoolsIndex] le permiten simular deficiencias específicas de la visión de color.</span><span class="sxs-lookup"><span data-stu-id="616c6-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] allow you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="616c6-106">La **herramienta Emular deficiencias de visión** simula las siguientes categorías.</span><span class="sxs-lookup"><span data-stu-id="616c6-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="616c6-107">Deficiencia de la visión del color</span><span class="sxs-lookup"><span data-stu-id="616c6-107">Color vision deficiency</span></span> | <span data-ttu-id="616c6-108">Detalles</span><span class="sxs-lookup"><span data-stu-id="616c6-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="616c6-109">Visión borrosa</span><span class="sxs-lookup"><span data-stu-id="616c6-109">Blurred vision</span></span> | <span data-ttu-id="616c6-110">El usuario tiene dificultades para centrarse en detalles finos.</span><span class="sxs-lookup"><span data-stu-id="616c6-110">The user has difficulty focusing on fine details.</span></span> |  
| <span data-ttu-id="616c6-111">Protanopia</span><span class="sxs-lookup"><span data-stu-id="616c6-111">Protanopia</span></span> | <span data-ttu-id="616c6-112">El usuario no puede percibir ninguna luz roja.</span><span class="sxs-lookup"><span data-stu-id="616c6-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="616c6-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="616c6-113">Deuteranopia</span></span> | <span data-ttu-id="616c6-114">El usuario no puede percibir ninguna luz verde.</span><span class="sxs-lookup"><span data-stu-id="616c6-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="616c6-115">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="616c6-115">Tritanopia</span></span> | <span data-ttu-id="616c6-116">El usuario no puede percibir ninguna luz azul.</span><span class="sxs-lookup"><span data-stu-id="616c6-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="616c6-117">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="616c6-117">Achromatopsia</span></span> | <span data-ttu-id="616c6-118">El usuario no puede percibir ningún color, lo que reduce todo el color a una sombra de gris.</span><span class="sxs-lookup"><span data-stu-id="616c6-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <a name="navigate-to-the-rendering-tools"></a><span data-ttu-id="616c6-119">Vaya a herramientas de representación</span><span class="sxs-lookup"><span data-stu-id="616c6-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="616c6-120">Para simular una deficiencia de visión que se está aplicando para el producto web, abra las herramientas [de representación][DevtoolsRenderingToolsIndex].</span><span class="sxs-lookup"><span data-stu-id="616c6-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="616c6-121">Para abrir las herramientas de representación, elija el elemento `...` de menú de la barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="616c6-121">To open the Rendering Tools, choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="616c6-122">Elegir **más herramientas**</span><span class="sxs-lookup"><span data-stu-id="616c6-122">Choose **More tools**</span></span>  
1.  <span data-ttu-id="616c6-123">Elegir **representación**</span><span class="sxs-lookup"><span data-stu-id="616c6-123">Choose **Rendering**</span></span>  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir las herramientas de representación" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="616c6-125">Abrir las herramientas **de representación**</span><span class="sxs-lookup"><span data-stu-id="616c6-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="616c6-126">El **menú** Representación aparece en el cajón.</span><span class="sxs-lookup"><span data-stu-id="616c6-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="616c6-127">Desplácese hacia abajo hasta el `Emulate vision deficiencies` elemento de menú y elija el menú desplegable para mostrar las opciones.</span><span class="sxs-lookup"><span data-stu-id="616c6-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="Menú Emular deficiencias de visión en el cajón de representación" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="616c6-129">Menú **Emular deficiencias de visión** en el **cajón de representación**</span><span class="sxs-lookup"><span data-stu-id="616c6-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="616c6-130">Elija una opción.</span><span class="sxs-lookup"><span data-stu-id="616c6-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Opciones del menú Emular deficiencias de la visión" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="616c6-132">Opciones **del menú Emular deficiencias** de visión</span><span class="sxs-lookup"><span data-stu-id="616c6-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="616c6-133">Las ventanas principales muestran la simulación de la opción elegida aplicada a la página actual.</span><span class="sxs-lookup"><span data-stu-id="616c6-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Mostrar con la simulación de visión borrosa" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="616c6-135">Visualización con **simulación de visión borrosa**</span><span class="sxs-lookup"><span data-stu-id="616c6-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Mostrar con la simulación **Achromatopsia**" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="616c6-137">Mostrar con **la simulación de Achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="616c6-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="use-the-command-menu"></a><span data-ttu-id="616c6-138">Usar el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="616c6-138">Use the Command Menu</span></span>  

<span data-ttu-id="616c6-139">También puede usar el **menú comando para** tener acceso a las diferentes simulaciones.</span><span class="sxs-lookup"><span data-stu-id="616c6-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="616c6-140">Seleccione `Ctrl` + `Shift` + `P` \(Windows/Linux\) o `Command` + `Shift` + `P` \(macOS\) para \*\*\*\* abrir el menú de comandos .</span><span class="sxs-lookup"><span data-stu-id="616c6-140">Select `Ctrl`+`Shift`+`P` \(Windows/Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="616c6-142">Menú **comando**</span><span class="sxs-lookup"><span data-stu-id="616c6-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="616c6-143">Escriba `emulate` , elija lo que desea simular y elija `Enter` .</span><span class="sxs-lookup"><span data-stu-id="616c6-143">Type `emulate`, choose what you want to simulate and choose `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Las distintas opciones de simulación disponibles en el menú comando" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="616c6-145">Las distintas opciones de simulación disponibles en el **menú comando**</span><span class="sxs-lookup"><span data-stu-id="616c6-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="616c6-146">Las **herramientas Emular deficiencias de** visión simulan aproximaciones de cómo una persona con cada deficiencia puede ver el producto.</span><span class="sxs-lookup"><span data-stu-id="616c6-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="616c6-147">Cada persona es diferente, por lo tanto, las deficiencias de la vista varían en la gravedad de una persona a otra.</span><span class="sxs-lookup"><span data-stu-id="616c6-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="616c6-148">Para satisfacer mejor las necesidades de los usuarios, evite cualquier combinación de colores que pueda ser un problema.</span><span class="sxs-lookup"><span data-stu-id="616c6-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="616c6-149">Las **herramientas Emular deficiencias** de visión no son una evaluación de accesibilidad completa del producto.</span><span class="sxs-lookup"><span data-stu-id="616c6-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="616c6-150">En su lugar, **las herramientas Emular** deficiencias de visión deben darle un buen primer paso para evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="616c6-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevToolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analizar el rendimiento en tiempo de ejecución | Microsoft Docs"  

[ColorblindawarenessMain]: https://www.colourblindawareness.org "La organización de concienciación de ciegos de color"  

[AmfcbMain]: https://www.amfcb.org "The American Foundation for the Color Blind (AFCB)"  
