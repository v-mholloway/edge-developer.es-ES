---
title: Emular deficiencias de la visión en Microsoft Edge DevTools (daltonismo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: b70499fa189d162fa7589966bab183f4c12f68f7
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843924"
---
# <span data-ttu-id="60a19-103">Emular deficiencias de la visión</span><span class="sxs-lookup"><span data-stu-id="60a19-103">Emulate vision deficiencies</span></span>

<span data-ttu-id="60a19-104">Para satisfacer mejor las necesidades de los usuarios con [deficiencia][ColorblindawarenessMain] de la visión del color \ (daltonismo \), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] le permite simular determinadas deficiencias de la visión del color.</span><span class="sxs-lookup"><span data-stu-id="60a19-104">To better meet the needs of your users with [color vision deficiency][ColorblindawarenessMain] \(color blindness\), [Microsoft Edge DevTools][MicrosoftEdgeDevTools] enable you to simulate specific color vision deficiencies.</span></span>  <span data-ttu-id="60a19-105">La herramienta **emular deficiencias** de la visión simula las siguientes categorías.</span><span class="sxs-lookup"><span data-stu-id="60a19-105">The **Emulate vision deficiencies** tool simulates the following categories.</span></span>  

| <span data-ttu-id="60a19-106">Deficiencia de la visión del color</span><span class="sxs-lookup"><span data-stu-id="60a19-106">Color vision deficiency</span></span> | <span data-ttu-id="60a19-107">Detalles</span><span class="sxs-lookup"><span data-stu-id="60a19-107">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="60a19-108">Visión borrosa</span><span class="sxs-lookup"><span data-stu-id="60a19-108">Blurred vision</span></span> | <span data-ttu-id="60a19-109">El usuario tiene dificultades para centrarse en detalles.</span><span class="sxs-lookup"><span data-stu-id="60a19-109">The user has difficulty focusing on fine details.</span></span> |   
| <span data-ttu-id="60a19-110">Protanopia</span><span class="sxs-lookup"><span data-stu-id="60a19-110">Protanopia</span></span> | <span data-ttu-id="60a19-111">El usuario no puede percibir ninguna luz roja.</span><span class="sxs-lookup"><span data-stu-id="60a19-111">The user is unable to perceive any red light.</span></span> |  
| <span data-ttu-id="60a19-112">Deuteranopia</span><span class="sxs-lookup"><span data-stu-id="60a19-112">Deuteranopia</span></span> | <span data-ttu-id="60a19-113">El usuario no puede percibir ninguna luz verde.</span><span class="sxs-lookup"><span data-stu-id="60a19-113">The user is unable to perceive any green light.</span></span> |  
| <span data-ttu-id="60a19-114">Tritanopia</span><span class="sxs-lookup"><span data-stu-id="60a19-114">Tritanopia</span></span> | <span data-ttu-id="60a19-115">El usuario no puede percibir ninguna luz azul.</span><span class="sxs-lookup"><span data-stu-id="60a19-115">The user is unable to perceive any blue light.</span></span> |  
| <span data-ttu-id="60a19-116">Achromatopsia</span><span class="sxs-lookup"><span data-stu-id="60a19-116">Achromatopsia</span></span> | <span data-ttu-id="60a19-117">El usuario no puede percibir ningún color, lo que reduce todo el color a un tono de gris.</span><span class="sxs-lookup"><span data-stu-id="60a19-117">The user is unable to perceive any color, which reduces all color to a shade of grey.</span></span> |  

## <span data-ttu-id="60a19-118">Ir a las herramientas de representación</span><span class="sxs-lookup"><span data-stu-id="60a19-118">Navigate to the Rendering Tools</span></span>  

<span data-ttu-id="60a19-119">Para simular una deficiencia de la visión que se aplica a su producto Web, abra las [herramientas de representación][RenderingTools].</span><span class="sxs-lookup"><span data-stu-id="60a19-119">To simulate a vision deficiency being applied for your web product, open the [Rendering Tools][RenderingTools].</span></span>  

1.  <span data-ttu-id="60a19-120">Abrir las herramientas de representación seleccionando el `...` elemento de menú de la barra de herramientas</span><span class="sxs-lookup"><span data-stu-id="60a19-120">Open the Rendering Tools by selecting the `...` menu item in the toolbar</span></span>  
1.  <span data-ttu-id="60a19-121">Seleccionar</span><span class="sxs-lookup"><span data-stu-id="60a19-121">Select</span></span> `More tools`  
1.  <span data-ttu-id="60a19-122">Seleccionar</span><span class="sxs-lookup"><span data-stu-id="60a19-122">Select</span></span> `Rendering`  
    
    :::image type="complex" source="../media/getting-to-the-rendering-tools.msft.png" alt-text="Abrir las herramientas de representación" lightbox="../media/getting-to-the-rendering-tools.msft.png":::
       <span data-ttu-id="60a19-124">Abrir las **herramientas de representación**</span><span class="sxs-lookup"><span data-stu-id="60a19-124">Opening the **Rendering Tools**</span></span>  
    :::image-end:::  

<span data-ttu-id="60a19-125">El menú de **fotorrealismo** aparece en el cajón.</span><span class="sxs-lookup"><span data-stu-id="60a19-125">The **Rendering** menu appears in the drawer.</span></span>  

1.  <span data-ttu-id="60a19-126">Desplácese hacia abajo hasta el `Emulate vision deficiencies` elemento de menú y seleccione el menú desplegable para mostrar las opciones.</span><span class="sxs-lookup"><span data-stu-id="60a19-126">Scroll down to the `Emulate vision deficiencies` menu item and select the drop-down menu to display the options.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu.msft.png" alt-text="El menú emular deficiencias de la visión en el alimentador de representación" lightbox="../media/accessibility-emulate-vision-menu.msft.png":::
       <span data-ttu-id="60a19-128">El menú **emular deficiencias** de la visión en el alimentador de **representación**</span><span class="sxs-lookup"><span data-stu-id="60a19-128">The **Emulate vision deficiencies** menu on the **Rendering** drawer</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="60a19-129">Elija una opción.</span><span class="sxs-lookup"><span data-stu-id="60a19-129">Choose an option.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulate-vision-menu-options.msft.png" alt-text="Las opciones del menú emular deficiencias de visión" lightbox="../media/accessibility-emulate-vision-menu-options.msft.png":::
       <span data-ttu-id="60a19-131">Las opciones del menú **emular deficiencias de visión**</span><span class="sxs-lookup"><span data-stu-id="60a19-131">The **Emulate vision deficiencies** menu options</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="60a19-132">En la ventana principal se muestra la simulación de la opción seleccionada que se ha aplicado a la página actual.</span><span class="sxs-lookup"><span data-stu-id="60a19-132">The main windows displays the simulation of your selected option applied to the current page.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-blurred-vision-emulation.msft.png" alt-text="Mostrar con \* \* simulación de enfoque \* \* borroso" lightbox="../media/accessibility-blurred-vision-emulation.msft.png":::
             <span data-ttu-id="60a19-134">Mostrar con simulación de **visión borrosa**</span><span class="sxs-lookup"><span data-stu-id="60a19-134">Display using **Blurred Vision** simulation</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/accessibility-achromatopsia-emulation.msft.png" alt-text="Pantalla con \* \* achromatopsia \* \* simulación" lightbox="../media/accessibility-achromatopsia-emulation.msft.png":::
             <span data-ttu-id="60a19-136">Mostrar con simulación de **achromatopsia**</span><span class="sxs-lookup"><span data-stu-id="60a19-136">Display using **Achromatopsia** simulation</span></span> :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="60a19-137">Usar el menú de comandos</span><span class="sxs-lookup"><span data-stu-id="60a19-137">Use the Command Menu</span></span>  

<span data-ttu-id="60a19-138">También puede usar el **menú de comandos** para acceder a las distintas simulaciones.</span><span class="sxs-lookup"><span data-stu-id="60a19-138">You may also use **Command Menu** to access the different simulations.</span></span>  

1.  <span data-ttu-id="60a19-139">Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**.</span><span class="sxs-lookup"><span data-stu-id="60a19-139">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="El menú de comandos" lightbox="../media/css-console-command-menu-rendering.msft.png":::
       <span data-ttu-id="60a19-141">El **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="60a19-141">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="60a19-142">Escriba `emulate` , elija lo que desea simular y presione `Enter` .</span><span class="sxs-lookup"><span data-stu-id="60a19-142">Type `emulate`, choose what you want to simulate and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/accessibility-emulation-command-menu-results.msft.png" alt-text="Las diferentes opciones de simulación disponibles en el menú de comandos" lightbox="../media/accessibility-emulation-command-menu-results.msft.png":::
       <span data-ttu-id="60a19-144">Las diferentes opciones de simulación disponibles en el **menú de comandos**</span><span class="sxs-lookup"><span data-stu-id="60a19-144">The different simulation options available in the **Command Menu**</span></span>  
    :::image-end:::  
    
> [!IMPORTANT]
> <span data-ttu-id="60a19-145">Las herramientas **emular deficiencias** de la visión simulan aproximaciones sobre cómo una persona con deficiencias puede ver su producto.</span><span class="sxs-lookup"><span data-stu-id="60a19-145">The **Emulate vision deficiencies** tools simulate approximations of how a person with each deficiency may see your product.</span></span>  <span data-ttu-id="60a19-146">Cada persona es diferente; por lo tanto, las deficiencias de la visión varían en gravedad de persona a persona.</span><span class="sxs-lookup"><span data-stu-id="60a19-146">Each person is different, therefore vision deficiencies vary in severity from person to person.</span></span>  <span data-ttu-id="60a19-147">Para satisfacer mejor las necesidades de los usuarios, evite cualquier combinación de colores que pueda ser un problema.</span><span class="sxs-lookup"><span data-stu-id="60a19-147">To better meet the needs of your users, avoid any color combination that may be an issue.</span></span>  <span data-ttu-id="60a19-148">Las herramientas **emular deficiencias de Vision** no son una evaluación completa de la accesibilidad del producto.</span><span class="sxs-lookup"><span data-stu-id="60a19-148">The **Emulate vision deficiencies** tools are not a full accessibility assessment of your product.</span></span>  <span data-ttu-id="60a19-149">En su lugar, las herramientas **emular deficiencias** de la visión deberían darle un buen primer paso para evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="60a19-149">Instead, the **Emulate vision deficiencies** tools should  give you a good first step to avoid problems.</span></span>  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[ColorblindawarenessMain]: http://www.colourblindawareness.org "La organización de conocimiento de colores ciegos"  
[AmfcbMain]: https://www.amfcb.org "American Foundation para el color Blind (AFCB)"  
[RenderingTools]: /microsoft-edge/devtools-guide-chromium/rendering-tools "Herramientas de representación de Microsoft Edge (cromo)"  
