---
title: Emular deficiencias de la visión en Microsoft Edge DevTools (daltonismo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0b608f5fe67724eee81aeb993577ee9b45cbca09
ms.sourcegitcommit: d7fdb67df0fe73fa5ae96e5a69a847d07941d0a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2020
ms.locfileid: "10758120"
---
# <span data-ttu-id="0febf-103">Emular deficiencias de la visión</span><span class="sxs-lookup"><span data-stu-id="0febf-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="0febf-104">En todo el mundo, aproximadamente el 8% de hombres y 0,5% de mujeres tienen una deficiencia de la [visión de color][ColorblindawarenessMain] que comúnmente se denomina "daltonismo".</span><span class="sxs-lookup"><span data-stu-id="0febf-104">Worldwide approximately 8% of men and 0.5% of women have a [color vision deficiency][ColorblindawarenessMain] commonly named "Color Blindness".</span></span>  <span data-ttu-id="0febf-105">[Microsoft Edge DevTools][MicrosoftEdgeDevTools] le permite emular diversas deficiencias conocidas y ofrecer una vista previa del producto para que lo revise.</span><span class="sxs-lookup"><span data-stu-id="0febf-105">[Microsoft Edge DevTools][MicrosoftEdgeDevTools] enables you to emulate various known deficiencies and provide a preview of your product for you to review.</span></span>  

| <span data-ttu-id="0febf-106">Deficiencia de color</span><span class="sxs-lookup"><span data-stu-id="0febf-106">Color Deficiency</span></span> | <span data-ttu-id="0febf-107">Detalles</span><span class="sxs-lookup"><span data-stu-id="0febf-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="0febf-108">Visión borrosa</span><span class="sxs-lookup"><span data-stu-id="0febf-108">Blurred vision</span></span> |  |   
| <span data-ttu-id="0febf-109">Protanopia</span><span class="sxs-lookup"><span data-stu-id="0febf-109">Protanopia</span></span> | <span data-ttu-id="0febf-110">La incapacidad de percibir cualquier luz roja.</span><span class="sxs-lookup"><span data-stu-id="0febf-110">The inability to perceive any red light.</span></span> |  
| <span data-ttu-id="0febf-111">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="0febf-111">Deuteranopia</span></span> | <span data-ttu-id="0febf-112">La incapacidad de percibir cualquier luz verde.</span><span class="sxs-lookup"><span data-stu-id="0febf-112">The inability to perceive any green light.</span></span> |  
| <span data-ttu-id="0febf-113">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="0febf-113">Tritanopia</span></span> | <span data-ttu-id="0febf-114">La incapacidad de percibir cualquier luz azul.</span><span class="sxs-lookup"><span data-stu-id="0febf-114">The inability to perceive any blue light.</span></span> |  
| <span data-ttu-id="0febf-115">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="0febf-115">Achromatopsia</span></span> | <span data-ttu-id="0febf-116">La incapacidad de percibir cualquier color, excepto tonos de gris.</span><span class="sxs-lookup"><span data-stu-id="0febf-116">The inability to perceive any color, except for shades of grey.</span></span> |  

## <span data-ttu-id="0febf-117">Ir a las herramientas de representación</span><span class="sxs-lookup"><span data-stu-id="0febf-117">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="0febf-118">Para probar el producto Web actual por deficiencias de color, abra las [herramientas de representación][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="0febf-118">To test your current web product for color deficiencies, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="0febf-119">Abrir las herramientas de representación seleccionando el `...` elemento de menú de la barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="0febf-119">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="0febf-120">Seleccionar</span><span class="sxs-lookup"><span data-stu-id="0febf-120">Select</span></span> `More tools`  
1.  <span data-ttu-id="0febf-121">Seleccionar</span><span class="sxs-lookup"><span data-stu-id="0febf-121">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir las herramientas de representación" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="0febf-123">Abrir las **herramientas de representación**</span><span class="sxs-lookup"><span data-stu-id="0febf-123">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="0febf-124">El menú de **fotorrealismo** aparece en la mitad inferior de la DevTools.</span><span class="sxs-lookup"><span data-stu-id="0febf-124">The **Rendering** menu appears in the bottom half of the DevTools.</span></span>  

1.  <span data-ttu-id="0febf-125">Desplácese hacia abajo hasta el `Emulate Vision deficiencies` elemento de menú y seleccione una de las opciones.</span><span class="sxs-lookup"><span data-stu-id="0febf-125">Scroll down to the `Emulate Vision deficiencies` menu item and select from the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="El menú emular deficiencias de la visión de las herramientas de representación" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="0febf-127">El menú **emular deficiencias** de la visión de las herramientas de **representación**</span><span class="sxs-lookup"><span data-stu-id="0febf-127">The **Emulate Vision Deficiencies** menu of the **Rendering** tools</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0febf-128">Elija cualquiera de las opciones</span><span class="sxs-lookup"><span data-stu-id="0febf-128">Choose any of the options</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Las opciones del menú emular deficiencias de visión" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="0febf-130">Las opciones del menú **emular deficiencias de visión**</span><span class="sxs-lookup"><span data-stu-id="0febf-130">The **Emulate Vision Deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0febf-131">La página actual se muestra en una simulación de cómo puede mostrarse a un usuario con la deficiencia elegida.</span><span class="sxs-lookup"><span data-stu-id="0febf-131">The current page is displayed in a simulation of how it may appear to a user with the chosen deficiency.</span></span>  

    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Documentación de las herramientas de desarrollo de Microsoft Edge en emulación de visión borrosa" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="0febf-133">Se muestra con la emulación de la **visión borrosa**</span><span class="sxs-lookup"><span data-stu-id="0febf-133">Displayed using **Blurred Vision** emulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Documentación de las herramientas de desarrollo de Microsoft Edge en achromatopsia Vision Emulation" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="0febf-135">Mostrar con la emulación de la **visión de achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="0febf-135">Display using **Achromatopsia Vision** emulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="0febf-136">Usar el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="0febf-136">Using the command menu</span></span>  

<span data-ttu-id="0febf-137">También puede alcanzar las distintas emulaciones sin pasar por los distintos menús mediante el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="0febf-137">You may also reach the different emulations without going through the various menus using the **Command Menu**.</span></span>  

1.  <span data-ttu-id="0febf-138">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="0febf-138">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="0febf-140">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="0febf-140">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0febf-141">Escriba `emulate` , elija lo que desea simular y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="0febf-141">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Las diferentes opciones de emulación disponibles en el menú de comandos" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="0febf-143">Las diferentes opciones de emulación disponibles en el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="0febf-143">The different emulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="0febf-144">Las herramientas de emulación son aproximaciones de la manera en que una persona con deficiencias puede ver su producto.</span><span class="sxs-lookup"><span data-stu-id="0febf-144">The emulation tools are approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="0febf-145">Cada persona es diferente; por lo tanto, las deficiencias de la visión varían en gravedad de persona a persona.</span><span class="sxs-lookup"><span data-stu-id="0febf-145">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="0febf-146">Para satisfacer mejor las necesidades de los usuarios, evite cualquier combinación de colores que pueda ser un problema.</span><span class="sxs-lookup"><span data-stu-id="0febf-146">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="0febf-147">Las herramientas de emulación no son una evaluación completa de la accesibilidad de su producto, pero usted debe tener un buen primer paso para evitar las mayores deficiencias.</span><span class="sxs-lookup"><span data-stu-id="0febf-147">The emulation tools are not a full assessment of the accessibility of your product, but you should have a good first step towards avoiding the biggest deficiencies.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "La organización de conocimiento de colores ciegos"  
[AmfcbMain]: https://www.amfcb.org "American Foundation para el color Blind (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Herramientas de representación de Microsoft Edge (cromo)"  
