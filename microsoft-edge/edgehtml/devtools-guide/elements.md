---
description: Use el panel elementos para inspeccionar el HTML, CSS, DOM y la accesibilidad de la página.
title: Elementos DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, elementos, HTML, CSS, puntos de interrupción de Dom, eventos, accesibilidad
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 14052bc40b9f94e628f0b575ede6c1ca8ccf179a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236013"
---
# <span data-ttu-id="01396-104">Elementos</span><span class="sxs-lookup"><span data-stu-id="01396-104">Elements</span></span>

<span data-ttu-id="01396-105">El panel **elementos** le ayuda a:</span><span class="sxs-lookup"><span data-stu-id="01396-105">The **Elements** panel helps you to:</span></span>

* <span data-ttu-id="01396-106">[Identificar y modificar elementos en el árbol HTML](#html-tree-view) de la página actual</span><span class="sxs-lookup"><span data-stu-id="01396-106">[Identify and edit elements in the HTML tree](#html-tree-view) of the current page</span></span>
* <span data-ttu-id="01396-107">[Inspeccionar y modificar CSS](./elements/styles.md) en la página, incluidos los pseudo-Estados y los pseudo-elementos</span><span class="sxs-lookup"><span data-stu-id="01396-107">[Inspect and modify CSS](./elements/styles.md) on the page, including pseudo-states and pseudo-elements</span></span>
* <span data-ttu-id="01396-108">[Comprender el diseño CSS y la cascada de estilos](./elements/computed.md) que se producen en la página</span><span class="sxs-lookup"><span data-stu-id="01396-108">[Understand the CSS layout and style cascade](./elements/computed.md) happening on the page</span></span>
* <span data-ttu-id="01396-109">[Realizar un seguimiento de los controladores de eventos no fiables](./elements/events.md) para poder depurarlos</span><span class="sxs-lookup"><span data-stu-id="01396-109">[Track down rogue event handlers](./elements/events.md) so you can debug them</span></span>
* <span data-ttu-id="01396-110">[Establecer puntos de interrupción de depuración para cambios visuales inesperados](./elements/dom-breakpoints.md) para saltar al código que los causa</span><span class="sxs-lookup"><span data-stu-id="01396-110">[Set debugging breakpoints for unexpected visual changes](./elements/dom-breakpoints.md) to jump into the code causing them</span></span>
* <span data-ttu-id="01396-111">[Obtener información detallada sobre las fuentes usadas en la página](./elements/fonts.md) y desde dónde se están cargando</span><span class="sxs-lookup"><span data-stu-id="01396-111">[Get detailed information about the fonts used on the page](./elements/fonts.md) and where they're loading from</span></span>
* <span data-ttu-id="01396-112">[Ver la página desde el punto de vista de un lector de pantalla](./elements/accessibility.md) para comprobar y probar la accesibilidad</span><span class="sxs-lookup"><span data-stu-id="01396-112">[View your page from a screen reader's point of view](./elements/accessibility.md) to verify and test accessibility</span></span> 
* <span data-ttu-id="01396-113">[Revisar una diferencia continuada de los cambios de CSS](./elements/changes.md) que realiza mientras depura la interfaz de usuario de la página</span><span class="sxs-lookup"><span data-stu-id="01396-113">[Review a running diff of the CSS changes](./elements/changes.md) you make as you debug the UI of your page</span></span>

## <span data-ttu-id="01396-114">Vista de árbol HTML</span><span class="sxs-lookup"><span data-stu-id="01396-114">HTML tree view</span></span>

![Panel de elementos de DevTools de Microsoft Edge](./media/elements.png)

1. <span data-ttu-id="01396-116">Use la herramienta **Select Element** ( `Ctrl+B` ) para localizar un elemento en la **vista de árbol HTML** haciendo clic en él en la página.</span><span class="sxs-lookup"><span data-stu-id="01396-116">Use the **Select element** (`Ctrl+B`) tool to locate an element in the **HTML tree view** by clicking on it in the page.</span></span>

2. <span data-ttu-id="01396-117">Use la herramienta de **resaltado de elementos** ( `Ctrl+Shift+L` ) para localizar un elemento en la página moviendo el puntero sobre él en la **vista de árbol HTML**.</span><span class="sxs-lookup"><span data-stu-id="01396-117">Use the **Element highlighting** (`Ctrl+Shift+L`) tool to locate an element on the page by hovering over it in the **HTML tree view**.</span></span>

3. <span data-ttu-id="01396-118">Abra la herramienta **selector de colores** ( `Ctrl+K` ) para ver una lista de los colores que se usan en la página actual.</span><span class="sxs-lookup"><span data-stu-id="01396-118">Open the **Color picker** (`Ctrl+K`) tool to see a list of the colors in use on the current page.</span></span> <span data-ttu-id="01396-119">Al hacer clic en un color de la lista encontrará más detalles (matiz, saturación, luminosidad, alfa).</span><span class="sxs-lookup"><span data-stu-id="01396-119">Clicking on a color on the list will provide further details (Hue, Saturation, Lightness, Alpha).</span></span> <span data-ttu-id="01396-120">El *selector de colores* también se abre al hacer clic en el cuadrado coloreado junto a un valor de color en el panel **estilos** , lo que permite editar el color de un elemento de página y ver inmediatamente los resultados.</span><span class="sxs-lookup"><span data-stu-id="01396-120">The *Color picker* also opens when you click on the colored square next to a color value in the **Styles** pane, allowing you to edit the color of a page element and immediately see the results.</span></span>

4. <span data-ttu-id="01396-121">El botón de **accesibilidad Tree** ( `Ctrl+Shift+A` ) abrirá el panel [árbol de accesibilidad](./elements/accessibility.md) , que muestra la estructura de la página tal como aparecería ante una tecnología de asistencia, como la Screenreader de [narrador de Windows](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) .</span><span class="sxs-lookup"><span data-stu-id="01396-121">The **Accessibility tree** (`Ctrl+Shift+A`) button will open the [Accessibility tree](./elements/accessibility.md) pane showing the structure of your page as it would appear to an assistive technology, such as the [Windows Narrator](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) screenreader.</span></span>

5. <span data-ttu-id="01396-122">También puede **encontrar** ( `Ctrl+F` ) un elemento en la vista de árbol HTML buscando el nombre de la etiqueta, los atributos o el contenido de texto.</span><span class="sxs-lookup"><span data-stu-id="01396-122">You can also **Find** (`Ctrl+F`) an element in the HTML tree view by searching for its tag name, attributes, or text content.</span></span>

### <span data-ttu-id="01396-123">Editar elementos</span><span class="sxs-lookup"><span data-stu-id="01396-123">Editing elements</span></span>

<span data-ttu-id="01396-124">Puede editar un elemento haciendo clic con el botón secundario en la vista de árbol HTML y seleccionando **Editar como HTML** en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="01396-124">You can edit an element by right-clicking on it within the HTML tree view and selecting **Edit as HTML** from the context menu.</span></span> <span data-ttu-id="01396-125">El menú contextual también proporciona opciones para eliminar, cortar, copiar, pegar, establecer pseudoclase de CSS (*: activo*, *: foco*, *: suspender*, *: visitado*) y agregar atributos.</span><span class="sxs-lookup"><span data-stu-id="01396-125">The context menu also provides options to delete, cut, copy, paste, set CSS pseudo-classes (*:active*, *:focus*, *:hover*, *:visited*) and add attributes.</span></span> <span data-ttu-id="01396-126">Otra forma de modificar un atributo o su valor es hacer doble clic en él desde la vista de árbol HTML.</span><span class="sxs-lookup"><span data-stu-id="01396-126">Another way to edit an attribute and/or its value is to double-click it from the HTML tree view.</span></span>

![Menú contextual de vista de árbol HTML](./media/elements_html_tree_context.png)

> [!NOTE]
> <span data-ttu-id="01396-128">Editar el árbol HTML no afecta al marcado de origen subyacente.</span><span class="sxs-lookup"><span data-stu-id="01396-128">Editing the HTML tree does not affect the underlying source markup.</span></span> <span data-ttu-id="01396-129">Si actualiza la página, revertirá los cambios y representará solo el diseño determinado por el origen de la página.</span><span class="sxs-lookup"><span data-stu-id="01396-129">Refreshing the page will revert your changes and render only the layout determined by the page source.</span></span> <span data-ttu-id="01396-130">Puede **copiar** el código HTML modificado en el portapapeles haciendo clic con el botón secundario en el elemento deseado (o el `html` elemento global, si quiere que toda la página) Abra el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="01396-130">You can **Copy** your modified HTML to the clipboard by right-clicking the desired element (or the global `html` element, if you want the entire page) to open up the context menu.</span></span> <span data-ttu-id="01396-131">(Las opciones de**cortar** y **pegar** también están disponibles).</span><span class="sxs-lookup"><span data-stu-id="01396-131">(**Cut** and **Paste** options are also available).</span></span>

<span data-ttu-id="01396-132">En el panel [estilos](./elements/styles.md) , también puede Agregar, eliminar o modificar los pseudo-Estados CSS y los pseudo-elementos.</span><span class="sxs-lookup"><span data-stu-id="01396-132">From the [Styles](./elements/styles.md) pane you can also add/delete/edit CSS pseudo-states and pseudo-elements.</span></span>

## <span data-ttu-id="01396-133">Paneles de herramientas</span><span class="sxs-lookup"><span data-stu-id="01396-133">Tool Panes</span></span>

<span data-ttu-id="01396-134">Una vez que haya seleccionado un elemento de página de interés, puede usar los paneles de herramientas para inspeccionar más los distintos estilos y propiedades de accesibilidad, ver sus agentes de escucha de eventos y establecer puntos de interrupción de mutación de DOM.</span><span class="sxs-lookup"><span data-stu-id="01396-134">Once you have selected a page element of interest, you can use the tool panes to further inspect its different styles and accessibility properties, view its event listeners, and set DOM mutation breakpoints.</span></span>

![Paneles de herramientas en el panel elementos](./media/elements_toolpanes.png)

1. <span data-ttu-id="01396-136">[**Estilos**](./elements/styles.md): estilos aplicados actualmente organizados por hoja de estilos</span><span class="sxs-lookup"><span data-stu-id="01396-136">[**Styles**](./elements/styles.md): Currently applied styles organized by stylesheet</span></span>

2. <span data-ttu-id="01396-137">[**Calculado**](./elements/computed.md): estilos aplicados actualmente organizados por atributos CSS</span><span class="sxs-lookup"><span data-stu-id="01396-137">[**Computed**](./elements/computed.md): Currently applied styles organized by CSS attributes</span></span>

3. <span data-ttu-id="01396-138">[**Eventos**](./elements/events.md): agentes de escucha de eventos registrados en el elemento actual y elementos antecesores</span><span class="sxs-lookup"><span data-stu-id="01396-138">[**Events**](./elements/events.md): Event listeners registered on the current element and ancestor elements</span></span>

4. <span data-ttu-id="01396-139">[**Puntos de interrupción Dom**](./elements/dom-breakpoints.md): puntos de interrupción de mutación Dom</span><span class="sxs-lookup"><span data-stu-id="01396-139">[**DOM breakpoints**](./elements/dom-breakpoints.md): DOM Mutation Breakpoints</span></span> 

5. <span data-ttu-id="01396-140">[**Fuentes**](./elements/fonts.md): fuentes aplicadas actualmente para un elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="01396-140">[**Fonts**](./elements/fonts.md): Currently applied fonts for a selected element</span></span>

6. <span data-ttu-id="01396-141">[**Accesibilidad**](./elements/accessibility.md): propiedades de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="01396-141">[**Accessibility**](./elements/accessibility.md):  Accessibility properties</span></span>

7. <span data-ttu-id="01396-142">[**Cambios**](./elements/changes.md): cambios de CSS realizados durante la sesión de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="01396-142">[**Changes**](./elements/changes.md): CSS changes made during diagnostic session</span></span>  

## <span data-ttu-id="01396-143">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="01396-143">Shortcuts</span></span>

| <span data-ttu-id="01396-144">Acción</span><span class="sxs-lookup"><span data-stu-id="01396-144">Action</span></span>               | <span data-ttu-id="01396-145">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="01396-145">Shortcut</span></span>               |
|:---------------------|:-----------------------|
| <span data-ttu-id="01396-146">Panel elementos</span><span class="sxs-lookup"><span data-stu-id="01396-146">Elements panel</span></span>       | `Ctrl` + `1`           |
| <span data-ttu-id="01396-147">Resaltado de elementos</span><span class="sxs-lookup"><span data-stu-id="01396-147">Element highlighting</span></span> | `Ctrl` + `Shift` + `L` |
| <span data-ttu-id="01396-148">Seleccionar elemento</span><span class="sxs-lookup"><span data-stu-id="01396-148">Select element</span></span>       | `Ctrl` + `B`           |
| <span data-ttu-id="01396-149">Selector de colores</span><span class="sxs-lookup"><span data-stu-id="01396-149">Color picker</span></span>         | `Ctrl` + `K`           |
| <span data-ttu-id="01396-150">Árbol de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="01396-150">Accessibility tree</span></span>   | `Ctrl` + `Shift` + `A` |
