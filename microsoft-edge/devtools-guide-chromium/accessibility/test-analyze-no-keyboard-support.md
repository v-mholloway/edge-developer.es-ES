---
description: Analizar la falta de compatibilidad con teclado en un formulario que usa el elemento div con la herramienta Inspeccionar y la pestaña Escuchas de eventos.
title: Analizar la compatibilidad con teclado en formularios con DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 16ec030ed433fc24d3b2b88bfb423a2479996dfe
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597696"
---
# <a name="analyze-keyboard-support-on-forms-using-the-devtools"></a><span data-ttu-id="1c428-104">Analizar la compatibilidad con teclado en formularios con DevTools</span><span class="sxs-lookup"><span data-stu-id="1c428-104">Analyze keyboard support on forms using the DevTools</span></span>

<span data-ttu-id="1c428-105">En este artículo se usa **la herramienta Inspeccionar** y la pestaña Escuchas de eventos para analizar la falta de compatibilidad con el teclado en una página de demostración que tiene **botones** que usan el `div` elemento.</span><span class="sxs-lookup"><span data-stu-id="1c428-105">This article uses the **Inspect** tool and **Event Listeners** tab to analyze the lack of keyboard support on a demo page which has buttons that use the `div` element.</span></span>

<span data-ttu-id="1c428-106">En el **formulario Donar,** los botones de cantidad y el botón **Donar** no funcionan con un teclado.</span><span class="sxs-lookup"><span data-stu-id="1c428-106">On the **Donate** form, the amount buttons and **Donate** button doesn't work with a keyboard.</span></span>  <span data-ttu-id="1c428-107">La depuración del formulario de donación requiere comprender por qué la falta de estilo de foco no se marca como un problema con herramientas de prueba automáticas como **la herramienta Problemas.**</span><span class="sxs-lookup"><span data-stu-id="1c428-107">Debugging the donation form requires understanding why the lack of focus styling isn't flagged as a problem with automatic testing tools like the **Issues** tool.</span></span>  <span data-ttu-id="1c428-108">En este ejemplo, los botones se implementan mediante elementos, que estas herramientas no reconocen como `div` un control en un formulario.</span><span class="sxs-lookup"><span data-stu-id="1c428-108">In this example, the buttons are implemented using `div` elements, which are not recognized by these tools as a control on a form.</span></span>

<span data-ttu-id="1c428-109">Para usar la herramienta Inspeccionar y la pestaña Escuchas de eventos para analizar la falta de compatibilidad con el teclado en la página de demostración:</span><span class="sxs-lookup"><span data-stu-id="1c428-109">To use the Inspect tool and Event Listeners tab to analyze the lack of keyboard support on the demo page:</span></span>

<!-- 1. Inspect tool: Accessibility section: keyboard-focusable row -->

1.  <span data-ttu-id="1c428-110">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="1c428-110">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>
    
1.  <span data-ttu-id="1c428-111">Seleccione el **botón Inspeccionar** \( Inspeccionar icono \) en la esquina superior izquierda de DevTools para que el botón esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).</span><span class="sxs-lookup"><span data-stu-id="1c428-111">Select the **Inspect** \(![Inspect icon](../media/inspect-icon.msft.png)\) button in the top-left corner of DevTools so that the button is highlighted (blue).</span></span>

1.  <span data-ttu-id="1c428-112">Mantenga el mouse sobre los botones de donación **50,** **100**y **200.**</span><span class="sxs-lookup"><span data-stu-id="1c428-112">Hover over the **50**, **100**, and **200** donation buttons.</span></span>  <span data-ttu-id="1c428-113">La herramienta Inspeccionar aparece en la página web, como una superposición.</span><span class="sxs-lookup"><span data-stu-id="1c428-113">The Inspect tool appears on the webpage, as an overlay.</span></span>  <span data-ttu-id="1c428-114">La **fila centrada en** el teclado de la superposición Inspeccionar muestra que ninguno de los botones de cantidad de donación es accesible para el teclado, como indica un círculo gris con línea diagonal.</span><span class="sxs-lookup"><span data-stu-id="1c428-114">The **keyboard-focusable** row of the Inspect overlay shows that none of the donation amount buttons are keyboard-accessible, as indicated by a gray circle with diagonal line.</span></span>  <span data-ttu-id="1c428-115">Los botones no tienen nombre y tienen un rol de porque son elementos, lo que significa que los botones no son accesibles para la tecnología `generic` `div` de asistencia.</span><span class="sxs-lookup"><span data-stu-id="1c428-115">The buttons have no name, and have a role of `generic` because they are `div` elements, which means that the buttons aren't accessible to assistive technology.</span></span>

    :::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Al inspeccionar los botones del formulario, se muestra que no son accesibles con teclado" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
        <span data-ttu-id="1c428-117">Al inspeccionar los botones del formulario, se muestra que no son accesibles con teclado</span><span class="sxs-lookup"><span data-stu-id="1c428-117">Inspecting the buttons of the form shows that they aren't keyboard-accessible</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="1c428-118">Cuando la **herramienta Inspeccionar** esté activa, en la página web, seleccione el **cuadro** de texto Otra entrada, encima del **botón Donar.**</span><span class="sxs-lookup"><span data-stu-id="1c428-118">When the **Inspect** tool is active, on the webpage, select the **Other** input textbox, above the **Donate** button.</span></span>  <span data-ttu-id="1c428-119">Se **abre** la herramienta Elementos, que muestra el árbol DOM de la página web.</span><span class="sxs-lookup"><span data-stu-id="1c428-119">The **Elements** tool opens, showing the DOM tree for the webpage.</span></span>  <span data-ttu-id="1c428-120">El elemento `<input id="freedonation" class="smallinput">` está seleccionado.</span><span class="sxs-lookup"><span data-stu-id="1c428-120">The element `<input id="freedonation" class="smallinput">` is selected.</span></span>

    ```html
    <div class="donationrow">
        <div class="donationbutton">50</div>
        <div class="donationbutton">100</div>
        <div class="donationbutton">200</div>
    </div>
    <div class="donationrow">
        <label for="freedonation">Other</label>
        <input id="freedonation" class="smallinput">
    </div>
    <div class="donationrow">
        <div class="submitbutton">Donate</div>
    </div>
    ```

    <span data-ttu-id="1c428-121">El uso de los elementos and en el cuadro de texto Otros es válido, lo que significa que la etiqueta Otros está vinculada `label` `input` correctamente con el cuadro de texto de entrada. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="1c428-121">The use of the `label` and `input` elements on the **Other** textbox is valid, which means that the **Other** label is correctly linked with the input textbox.</span></span>  <span data-ttu-id="1c428-122">El `input` cuadro de texto también es accesible con teclado.</span><span class="sxs-lookup"><span data-stu-id="1c428-122">The `input` textbox is also keyboard-accessible.</span></span>  <span data-ttu-id="1c428-123">El resto del marcado del formulario son elementos, que son fáciles de `div` aplicar, pero que no tienen ningún significado semántico.</span><span class="sxs-lookup"><span data-stu-id="1c428-123">The rest of the form's markup are `div` elements, which are easy to style, but have no semantic meaning.</span></span>

    <!-- 2. Elements tool: Event Listeners tab -->

    <span data-ttu-id="1c428-124">La funcionalidad del formulario se crea con JavaScript y puede probarla comprobando la pestaña **Escuchas de** eventos, de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="1c428-124">The form's functionality is created with JavaScript, and you can test this by checking the **Event Listeners** tab, as follows.</span></span>

1.  <span data-ttu-id="1c428-125">Con el elemento aún seleccionado en el árbol DOM, seleccione la pestaña Escuchas de eventos a la derecha de la pestaña Estilos y, a `<input id="freedonation" class="smallinput">` continuación, expanda la escucha de \*\*\*\* \*\*\*\* `click` eventos.</span><span class="sxs-lookup"><span data-stu-id="1c428-125">With the element `<input id="freedonation" class="smallinput">` still selected in the DOM tree, select the **Event Listeners** tab to the right of the **Styles** tab, and then expand the `click` event listener.</span></span>

    :::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="La herramienta escuchas de eventos que muestra dónde está JavaScript que hace que el formulario funcione" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
        <span data-ttu-id="1c428-127">La herramienta escuchas de eventos que muestra dónde está JavaScript que hace que el formulario funcione</span><span class="sxs-lookup"><span data-stu-id="1c428-127">The Event listeners tool showing you where the JavaScript is that makes the form work</span></span>
    :::image-end:::

1.  <span data-ttu-id="1c428-128">Seleccione el `buttons.js:18` vínculo.</span><span class="sxs-lookup"><span data-stu-id="1c428-128">Select the `buttons.js:18` link.</span></span>  <span data-ttu-id="1c428-129">Se **abre la herramienta** Orígenes, que muestra el JavaScript aplicado.</span><span class="sxs-lookup"><span data-stu-id="1c428-129">The **Sources** tool opens, showing the applied JavaScript.</span></span>

    :::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="El JavaScript responsable de la funcionalidad del formulario de donación, que se muestra en la herramienta Orígenes" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
        <span data-ttu-id="1c428-131">El JavaScript responsable de la funcionalidad del formulario de donación, que se muestra en la herramienta Orígenes</span><span class="sxs-lookup"><span data-stu-id="1c428-131">The JavaScript responsible for the donation form's functionality, shown in the Sources tool</span></span>
    :::image-end:::

```javascript
donations.addEventListener('click', e => {
  let t = e.target;
  if (t.classList.contains('donationbutton')) {
    if (currentbutton) { currentbutton.classList.remove('current'); }
    t.classList.add('current');
    currentbutton = t;
    e.preventDefault();
  }
  if (t.classList.contains('submitbutton')) {
    alert('Thanks for your donation!')
  } 
})
```

<span data-ttu-id="1c428-132">Usar un `click` evento para leer los botones es una buena práctica, ya que un evento se dispara tanto en la interacción con el puntero del mouse como con el `click` teclado.</span><span class="sxs-lookup"><span data-stu-id="1c428-132">Using a `click` event to read the buttons is good practice, because a `click` event fires both on mouse pointer and keyboard interaction.</span></span>  <span data-ttu-id="1c428-133">Sin embargo, como un elemento no es accesible para teclado y este botón Donar se implementa como un elemento ( ), esta funcionalidad de JavaScript nunca se ejecuta a menos que use un mouse u otro origen de un evento, como un botón especial disponible en algunos `div` \*\*\*\* `div` `<div class="submitbutton">Donate</div>` `click` teclados.</span><span class="sxs-lookup"><span data-stu-id="1c428-133">However, because a `div` element isn't keyboard-accessible, and this **Donate** button is implemented as a `div` element (`<div class="submitbutton">Donate</div>`), this JavaScript functionality never runs unless you use a mouse or another source of a `click` event, such as a special button available on some keyboards.</span></span>

<span data-ttu-id="1c428-134">Este es un ejemplo clásico en el que Se agregó JavaScript para crear funciones `button` que los elementos proporcionan de forma nativa.</span><span class="sxs-lookup"><span data-stu-id="1c428-134">This is a classic example where JavaScript was added to create functionality that `button` elements provide natively.</span></span>  <span data-ttu-id="1c428-135">La simulación de la funcionalidad de los `div` botones con elementos acabó produciendo una experiencia inaccesible.</span><span class="sxs-lookup"><span data-stu-id="1c428-135">Simulating the functionality of buttons with `div` elements ended up producing an inaccessible experience.</span></span>


## <a name="see-also"></a><span data-ttu-id="1c428-136">Consulta también</span><span class="sxs-lookup"><span data-stu-id="1c428-136">See also</span></span>

*  [<span data-ttu-id="1c428-137">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="1c428-137">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="1c428-138">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="1c428-138">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
