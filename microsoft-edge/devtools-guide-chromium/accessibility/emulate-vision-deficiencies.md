---
description: Emular las deficiencias de la visión en Microsoft Edge DevTools.
title: Emular deficiencias de la visión en Microsoft Edge DevTools (daltonismo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5343d32992880f8c60501a86db6cb3a92f417331
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230827"
---
# <span data-ttu-id="1770a-104">Emular deficiencias visuales</span><span class="sxs-lookup"><span data-stu-id="1770a-104">Emulate vision deficiencies</span></span>

<span data-ttu-id="1770a-105">Para satisfacer mejor las necesidades de los usuarios con [deficiencia][ColorblindawarenessMain] de la visión del color \ (daltonismo \), [Microsoft Edge DevTools][DevtoolsIndex] le permite simular determinadas deficiencias de la visión del color.</span><span class="sxs-lookup"><span data-stu-id="1770a-105">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][DevtoolsIndex] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="1770a-106">La herramienta **emular deficiencias** de la visión simula las siguientes categorías.</span><span class="sxs-lookup"><span data-stu-id="1770a-106">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="1770a-107">Deficiencia de la visión del color</span><span class="sxs-lookup"><span data-stu-id="1770a-107">Color vision deficiency</span></span> | <span data-ttu-id="1770a-108">Detalles</span><span class="sxs-lookup"><span data-stu-id="1770a-108">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="1770a-109">Visión borrosa</span><span class="sxs-lookup"><span data-stu-id="1770a-109">Blurred vision</span></span> | <span data-ttu-id="1770a-110">El usuario tiene dificultades para centrarse en detalles.</span><span class="sxs-lookup"><span data-stu-id="1770a-110">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="1770a-111">Protanopia</span><span class="sxs-lookup"><span data-stu-id="1770a-111">Protanopia</span></span> | <span data-ttu-id="1770a-112">El usuario no puede percibir ninguna luz roja.</span><span class="sxs-lookup"><span data-stu-id="1770a-112">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="1770a-113">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="1770a-113">Deuteranopia</span></span> | <span data-ttu-id="1770a-114">El usuario no puede percibir ninguna luz verde.</span><span class="sxs-lookup"><span data-stu-id="1770a-114">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="1770a-115">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="1770a-115">Tritanopia</span></span> | <span data-ttu-id="1770a-116">El usuario no puede percibir ninguna luz azul.</span><span class="sxs-lookup"><span data-stu-id="1770a-116">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="1770a-117">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="1770a-117">Achromatopsia</span></span> | <span data-ttu-id="1770a-118">El usuario no puede percibir ningún color, lo que reduce todo el color a un tono de gris.</span><span class="sxs-lookup"><span data-stu-id="1770a-118">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="1770a-119">Ir a las herramientas de representación</span><span class="sxs-lookup"><span data-stu-id="1770a-119">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="1770a-120">Para simular una deficiencia de la visión que se aplica a su producto Web, abra las [herramientas de representación][DevtoolsRenderingToolsIndex].</span><span class="sxs-lookup"><span data-stu-id="1770a-120">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][DevtoolsRenderingToolsIndex].</span></span>  

1.  <span data-ttu-id="1770a-121">Para abrir las herramientas de representación, elija el `...` elemento de menú de la barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="1770a-121">To open the Rendering Tools, by choose the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="1770a-122">Elegir</span><span class="sxs-lookup"><span data-stu-id="1770a-122">Choose</span></span> `More tools`  
1.  <span data-ttu-id="1770a-123">Elegir</span><span class="sxs-lookup"><span data-stu-id="1770a-123">Choose</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir las herramientas de representación" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="1770a-125">Abrir las **herramientas de representación**</span><span class="sxs-lookup"><span data-stu-id="1770a-125">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="1770a-126">El menú de **fotorrealismo** aparece en el cajón.</span><span class="sxs-lookup"><span data-stu-id="1770a-126">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="1770a-127">Desplácese hacia abajo hasta el `Emulate vision deficiencies` elemento de menú y elija el menú desplegable para mostrar las opciones.</span><span class="sxs-lookup"><span data-stu-id="1770a-127">Scroll down to the `Emulate vision deficiencies` menu item and choose the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="El menú emular deficiencias de la visión en el alimentador de representación" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="1770a-129">El menú **emular deficiencias** de la visión en el alimentador de **representación**</span><span class="sxs-lookup"><span data-stu-id="1770a-129">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1770a-130">Elija una opción.</span><span class="sxs-lookup"><span data-stu-id="1770a-130">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Las opciones del menú emular deficiencias de visión" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="1770a-132">Las opciones del menú **emular deficiencias de visión**</span><span class="sxs-lookup"><span data-stu-id="1770a-132">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1770a-133">En la ventana principal, se muestra la simulación de la opción que ha elegido aplicada a la página actual.</span><span class="sxs-lookup"><span data-stu-id="1770a-133">The main windows displays the simulation of your chosen option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Mostrar con \* \* simulación de enfoque \* \* borroso" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="1770a-135">Mostrar con simulación de **visión borrosa**</span><span class="sxs-lookup"><span data-stu-id="1770a-135">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Pantalla con \* \* achromatopsia \* \* simulación" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="1770a-137">Mostrar con simulación de **achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="1770a-137">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="1770a-138">Usar el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="1770a-138">Use the Command Menu</span></span>  

<span data-ttu-id="1770a-139">También puede usar el **menú de comandos** para acceder a las distintas simulaciones.</span><span class="sxs-lookup"><span data-stu-id="1770a-139">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="1770a-140">Seleccione `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="1770a-140">Select `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="1770a-142">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="1770a-142">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="1770a-143">Escriba `emulate` , elija lo que desea simular y seleccione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="1770a-143">Type `emulate`, choose what you want to simulate and select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Las diferentes opciones de simulación disponibles en el menú de comandos" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="1770a-145">Las diferentes opciones de simulación disponibles en el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="1770a-145">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="1770a-146">Las herramientas **emular deficiencias** de la visión simulan aproximaciones sobre cómo una persona con deficiencias puede ver su producto.</span><span class="sxs-lookup"><span data-stu-id="1770a-146">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="1770a-147">Cada persona es diferente; por lo tanto, las deficiencias de la visión varían en gravedad de persona a persona.</span><span class="sxs-lookup"><span data-stu-id="1770a-147">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="1770a-148">Para satisfacer mejor las necesidades de los usuarios, evite cualquier combinación de colores que pueda ser un problema.</span><span class="sxs-lookup"><span data-stu-id="1770a-148">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="1770a-149">Las herramientas **emular deficiencias de Vision** no son una evaluación completa de la accesibilidad del producto.</span><span class="sxs-lookup"><span data-stu-id="1770a-149">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="1770a-150">En su lugar, las herramientas **emular deficiencias** de la visión deberían darle un buen primer paso para evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="1770a-150">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsRenderingToolsIndex]: ../rendering-tools/index.md "Analizar rendimiento en tiempo de ejecución | Microsoft docs"  

[ColorblindawarenessMain]: http://www.colourblindawareness.org "La organización de conocimiento de colores ciegos"  

[AmfcbMain]: https://www.amfcb.org "American Foundation para el color Blind (AFCB)"  

