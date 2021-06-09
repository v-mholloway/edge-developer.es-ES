---
description: Para ver rápidamente el orden de tabulación de las secciones de una página, use el Visor de pedidos de origen en la herramienta Accesibilidad, a la derecha de la pestaña Estilos.
title: Probar la compatibilidad con teclado con el Visor de pedidos de origen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7e90221b581280a6eb63cee4d073622a80871903
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597654"
---
# <a name="test-keyboard-support-using-the-source-order-viewer"></a><span data-ttu-id="147ea-104">Probar la compatibilidad con teclado con el Visor de pedidos de origen</span><span class="sxs-lookup"><span data-stu-id="147ea-104">Test keyboard support using the Source Order Viewer</span></span>

<span data-ttu-id="147ea-105">El orden de origen de un documento es importante para la tecnología de asistencia y puede ser diferente del orden en que aparecen los elementos en la página representada.</span><span class="sxs-lookup"><span data-stu-id="147ea-105">The source order of a document is important for assistive technology, and can be different than the order in which elements appear on the rendered page.</span></span>  <span data-ttu-id="147ea-106">Con CSS, puede volver a ordenar los elementos de página de forma visual, pero eso no significa que la tecnología de asistencia, como los lectores de pantalla, represente elementos de página en el mismo orden.</span><span class="sxs-lookup"><span data-stu-id="147ea-106">Using CSS, you can re-order page elements in a visual way, but that doesn't mean that assistive technology such as screen readers would represent page elements in the same order.</span></span>  

<span data-ttu-id="147ea-107">Para asegurarse de que el documento tiene \*\*\*\* un orden lógico, puede usar el Visor de pedidos de origen para etiquetar distintos elementos de página con números que especifiquen el orden en el código fuente del documento.</span><span class="sxs-lookup"><span data-stu-id="147ea-107">To ensure that the document has a logical order, you can use the **Source Order Viewer** to label different page elements with numbers that specify the order in the source code of the document.</span></span>  <span data-ttu-id="147ea-108">El **Visor de pedidos de origen** está en la pestaña **Accesibilidad** (cerca de la **pestaña** Estilos).</span><span class="sxs-lookup"><span data-stu-id="147ea-108">The **Source Order Viewer** is in the **Accessibility** tab (near the **Styles** tab).</span></span>


## <a name="analyzing-the-order-of-keyboard-access-through-sections-of-the-page"></a><span data-ttu-id="147ea-109">Analizar el orden del acceso de teclado a través de secciones de la página</span><span class="sxs-lookup"><span data-stu-id="147ea-109">Analyzing the order of keyboard access through sections of the page</span></span>

<span data-ttu-id="147ea-110">La página web de [demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad tiene un orden de tabulación contraintético, donde los usuarios del teclado acceden al menú de navegación de la barra lateral solo después de navegar por todos los vínculos **Más.**</span><span class="sxs-lookup"><span data-stu-id="147ea-110">The [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] has a counterintuitive tabbing order, where keyboard users access the sidebar navigation menu only after tabbing through all the **More** links.</span></span>  <span data-ttu-id="147ea-111">El menú de navegación de la barra lateral está pensado para ser un acceso directo para llegar a lo profundo del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="147ea-111">The sidebar navigation menu is meant to be a shortcut to reach deep into the page content.</span></span>  <span data-ttu-id="147ea-112">Pero como debes pasar por toda la página antes de llegar al menú de navegación de la barra lateral, ese menú de navegación no es eficaz para los usuarios de teclado.</span><span class="sxs-lookup"><span data-stu-id="147ea-112">But because you need to go through the entire page before you reach the sidebar navigation menu, that navigation menu is ineffective for keyboard users.</span></span>

<span data-ttu-id="147ea-113">El `Tab` orden clave de la página de demostración es:</span><span class="sxs-lookup"><span data-stu-id="147ea-113">The `Tab` key order on the demo page is:</span></span>
1. <span data-ttu-id="147ea-114">El **campo** Búsqueda y, a continuación, **el botón ir** para el **campo** De búsqueda.</span><span class="sxs-lookup"><span data-stu-id="147ea-114">The **Search** field, then the **go** button for the **Search** field.</span></span>
1. <span data-ttu-id="147ea-115">El **botón** Más de la **sección Gatos,** para navegar a una página web de "Gatos".</span><span class="sxs-lookup"><span data-stu-id="147ea-115">The **More** button in the **Cats** section, to navigate to a "Cats" webpage.</span></span>  <span data-ttu-id="147ea-116">A continuación, los otros botones **Más,** para Perros, Ovejas, Equinos y, a continuación, Alpacas.</span><span class="sxs-lookup"><span data-stu-id="147ea-116">Then the other **More** buttons, for Dogs, Sheep, Horses, and then Alpacas.</span></span>
1. <span data-ttu-id="147ea-117">Los vínculos azules del menú de navegación de la barra lateral: **Gatos**, **Perros**, **Ovejas, Equinos**y, a continuación, **Alpacas**. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="147ea-117">The blue links of the sidebar navigation menu: **Cats**, **Dogs**, **Sheep**, **Horses**, and then **Alpacas**.</span></span>
1. <span data-ttu-id="147ea-118">El cuadro de texto de la donación en el formulario de donación.</span><span class="sxs-lookup"><span data-stu-id="147ea-118">The donation textbox in the donation form.</span></span>
1. <span data-ttu-id="147ea-119">Los botones de la barra de navegación superior: **Home**, **Adopt a pet**, **Donate**, **Jobs**y, a continuación, **About Us**.</span><span class="sxs-lookup"><span data-stu-id="147ea-119">The buttons in the top navigation bar: **Home**, **Adopt a pet**, **Donate**, **Jobs**, and then **About Us**.</span></span>
1. <span data-ttu-id="147ea-120">Interfaz de la parte superior de la ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="147ea-120">The browser's top-of-window interface.</span></span>

<span data-ttu-id="147ea-121">El motivo del orden de teclas confuso es que el orden experimentado al usar `Tab` un teclado viene determinado por el orden de origen del documento.</span><span class="sxs-lookup"><span data-stu-id="147ea-121">The reason for the confusing `Tab` key order is that the order experienced when using a keyboard is determined by the source order of the document.</span></span>  <span data-ttu-id="147ea-122">El orden experimentado con un teclado se puede modificar mediante el atributo de los elementos, lo que quita ese `tabindex` elemento del orden de origen.</span><span class="sxs-lookup"><span data-stu-id="147ea-122">The order experienced using a keyboard can be modified using the `tabindex` attribute on elements, which takes that element out of the source order.</span></span>

<span data-ttu-id="147ea-123">En el código fuente del documento, el menú de navegación de la barra lateral aparece después del contenido principal de la página web.</span><span class="sxs-lookup"><span data-stu-id="147ea-123">In the source code of the document, the sidebar navigation menu appears after the main content of the webpage.</span></span>  <span data-ttu-id="147ea-124">CSS se usó para colocar el menú de navegación de la barra lateral por encima de la mayoría del contenido principal de la página web.</span><span class="sxs-lookup"><span data-stu-id="147ea-124">CSS was used to position the sidebar navigation menu above most of the main content of the webpage.</span></span> 

<span data-ttu-id="147ea-125">Puede probar el orden de los elementos de página mediante el Visor de pedidos **de origen** en la **pestaña Accesibilidad.**  El **Visor de pedidos de origen** es una característica experimental.</span><span class="sxs-lookup"><span data-stu-id="147ea-125">You can test the order of page elements by using the **Source Order Viewer** in the **Accessibility** tab.  The **Source Order Viewer** is an experimental feature.</span></span> <span data-ttu-id="147ea-126">Para obtener más información, vaya [al Visor de pedidos de origen](../experimental-features/index.md#source-order-viewer).</span><span class="sxs-lookup"><span data-stu-id="147ea-126">For more information, navigate to [Source Order Viewer](../experimental-features/index.md#source-order-viewer).</span></span>


<span data-ttu-id="147ea-127">Para activar el Visor de pedidos de origen:</span><span class="sxs-lookup"><span data-stu-id="147ea-127">To turn on the Source Order Viewer:</span></span>

1.  <span data-ttu-id="147ea-128">En DevTools, en la parte superior derecha, seleccione el botón **Configuración** \( ![ Configuración botón ](../media/settings-button-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="147ea-128">In DevTools, in the upper right, select the **Settings** \(![Settings button](../media/settings-button-icon.msft.png)\) button.</span></span>  

1.  <span data-ttu-id="147ea-129">A **continuación Configuración**, seleccione **Experimentos**.</span><span class="sxs-lookup"><span data-stu-id="147ea-129">Below **Settings**, select **Experiments**.</span></span>  

1.  <span data-ttu-id="147ea-130">Active la casilla **Visor de pedidos de** origen.</span><span class="sxs-lookup"><span data-stu-id="147ea-130">Select the **Source Order Viewer** checkbox.</span></span>

1.  <span data-ttu-id="147ea-131">En la esquina superior derecha de la **página Configuración,** seleccione **X** para cerrar la Configuración página.</span><span class="sxs-lookup"><span data-stu-id="147ea-131">In the upper-right corner of the **Settings** page, select **X** to close the Settings page.</span></span>  <span data-ttu-id="147ea-132">En la parte superior de DevTools, el mensaje Ha cambiado una o más configuraciones que **requieren una recarga para que su efecto.**</span><span class="sxs-lookup"><span data-stu-id="147ea-132">At the top of DevTools, the message **One or more settings have changed which require a reload to take effect.**</span></span> <span data-ttu-id="147ea-133">se muestra.</span><span class="sxs-lookup"><span data-stu-id="147ea-133">is displayed.</span></span>  <span data-ttu-id="147ea-134">Seleccione el **botón Volver a cargar DevTools.**</span><span class="sxs-lookup"><span data-stu-id="147ea-134">Select the **Reload DevTools** button.</span></span>



<span data-ttu-id="147ea-135">Para activar y usar el Visor de pedidos de origen, con la página de demostración:</span><span class="sxs-lookup"><span data-stu-id="147ea-135">To activate and use the Source Order Viewer, with the demo page:</span></span>

1.  <span data-ttu-id="147ea-136">Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una pestaña nueva.  A **continuación, seleccione F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="147ea-136">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab.  Then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="147ea-137">En la **herramienta Elementos,** a la derecha de la **pestaña Estilos,** seleccione la **pestaña Accesibilidad.**</span><span class="sxs-lookup"><span data-stu-id="147ea-137">In the **Elements** tool, to the right of the **Styles** tab, select the **Accessibility** tab.</span></span>

1.  <span data-ttu-id="147ea-138">En la **sección Visor de pedidos de** origen, active la casilla Mostrar orden **de** origen.</span><span class="sxs-lookup"><span data-stu-id="147ea-138">In the **Source Order Viewer** section, select the **Show source order** checkbox.</span></span>  <span data-ttu-id="147ea-139">En la página web representada, aparecen números que indican el orden según el orden de `Tab` las líneas de código en el archivo de origen.</span><span class="sxs-lookup"><span data-stu-id="147ea-139">In the rendered webpage, numbers appear, indicating the `Tab` order as controlled by the order of lines of code in the source file.</span></span>

1.  <span data-ttu-id="147ea-140">En el árbol DOM de la **herramienta Elementos,** seleccione un elemento de diseño principal, como el `header` elemento.</span><span class="sxs-lookup"><span data-stu-id="147ea-140">In the DOM tree in the **Elements** tool, select a major layout element, such as the `header` element.</span></span>  <span data-ttu-id="147ea-141">Las superposiciones numéricas ahora se muestran en secciones de la página representada, que indican el orden de origen de los distintos elementos.</span><span class="sxs-lookup"><span data-stu-id="147ea-141">Numeric overlays are now displayed on sections of the rendered page, which indicate the source order of the different elements.</span></span> 

    :::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="Al activar el Visor de pedidos de origen, se muestra el orden de los elementos del origen como superposiciones en la página" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
        <span data-ttu-id="147ea-143">Al activar el **Visor de pedidos de origen,** se muestra el orden de los elementos del origen como superposiciones en la página</span><span class="sxs-lookup"><span data-stu-id="147ea-143">Activating the **Source Order Viewer** shows the order of the elements in the source as overlays on the page</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="147ea-144">Desplácese por la página para ver todas las superposiciones numéricas, incluida la sección de pie de página.</span><span class="sxs-lookup"><span data-stu-id="147ea-144">Scroll the page to see all of the numeric overlays, including on the page footer section.</span></span>


## <a name="see-also"></a><span data-ttu-id="147ea-145">Consulta también</span><span class="sxs-lookup"><span data-stu-id="147ea-145">See also</span></span>

*  [<span data-ttu-id="147ea-146">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="147ea-146">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="147ea-147">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="147ea-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
