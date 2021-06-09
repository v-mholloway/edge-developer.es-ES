---
description: Comprueba que las páginas web se pueden usar con la animación de la interfaz de usuario desactivada (movimiento reducido) con la característica multimedia Emular CSS prefiere la lista desplegable de movimiento reducido en la herramienta de representación.
title: Comprobar que la página se puede usar con la animación de la interfaz de usuario desactivada
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ec30925b706b4b1c6dfaaa6ce66a38fab8759ac2
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597657"
---
# <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off"></a><span data-ttu-id="d6b4a-104">Comprobar que la página se puede usar con la animación de la interfaz de usuario desactivada</span><span class="sxs-lookup"><span data-stu-id="d6b4a-104">Verify that the page is usable with UI animation turned off</span></span>

<span data-ttu-id="d6b4a-105">Una página web no debe mostrar animaciones a un usuario que a desactivar las animaciones en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-105">A webpage should not show animations to a user who turned off animations in the operating system.</span></span>  <span data-ttu-id="d6b4a-106">Las animaciones pueden ayudar a la facilidad de uso de un producto, pero también pueden causar distracción, confusión o náuseas.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-106">Animations can help the usability of a product, but they can also cause distraction, confusion, or nausea.</span></span>

<span data-ttu-id="d6b4a-107">Para comprobar que una página web se puede usar con \*\*\*\* la animación de la interfaz de usuario desactivada (movimiento reducido), en la herramienta Representación, usa la lista desplegable Emular medios **CSS prefers-reduced-motion.**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-107">To check that a webpage is usable with UI animation turned off (reduced motion), in the **Rendering** tool, use the **Emulate CSS media feature prefers-reduced-motion** dropdown list.</span></span>

<span data-ttu-id="d6b4a-108">En la página web de demostración de pruebas de accesibilidad, cuando desactivas las animaciones en el sistema operativo o emulas esa configuración mediante DevTools, la página web no usa un desplazamiento suave al seleccionar los vínculos del menú de navegación de la barra lateral.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-108">In the accessibility-testing demo webpage, when you turn off animations in the operating system, or emulate that settings by using DevTools, the webpage doesn't use smooth scrolling when you select the links of the sidebar navigation menu.</span></span>  <span data-ttu-id="d6b4a-109">Esto se logra ajustando la configuración de desplazamiento suave en CSS \*\*\*\* en una consulta multimedia y, a continuación, mediante la herramienta de representación para emular la configuración del sistema operativo para la animación reducida.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-109">This is achieved by wrapping the smooth-scrolling setting in CSS in a media query, and then using the **Rendering** tool to emulate the operating system setting for reduced animation.</span></span>

<span data-ttu-id="d6b4a-110">Para comprobar si la página se puede usar con animaciones desactivadas:</span><span class="sxs-lookup"><span data-stu-id="d6b4a-110">To check whether the page is usable with animations turned off:</span></span>

1.  <span data-ttu-id="d6b4a-111">Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-111">Open the [accessibility-testing demo webpage][DevToolsA11yErrorsDemopage] in a new tab of the browser, and then select **F12** to open DevTools.</span></span>

1.  <span data-ttu-id="d6b4a-112">En la parte superior de DevTools, seleccione la herramienta **Orígenes** y, a continuación, en el **panel** navegación de la izquierda, seleccione `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="d6b4a-112">At the top of DevTools, select the **Sources** tool, and then in the **Navigation** pane on the left, select `styles.css`.</span></span>  <span data-ttu-id="d6b4a-113">El archivo CSS aparece en el **panel Editor.**</span><span class="sxs-lookup"><span data-stu-id="d6b4a-113">The CSS file appears in the **Editor** pane.</span></span>

1.  <span data-ttu-id="d6b4a-114">Seleccione **Ctrl+F** en Windows/Linux o **Comando+F** en macOS y, a continuación, escriba `@media` .</span><span class="sxs-lookup"><span data-stu-id="d6b4a-114">Select **Ctrl+F** on Windows/Linux or **Command+F** on macOS, and then enter `@media`.</span></span>  <span data-ttu-id="d6b4a-115">Se muestra la siguiente consulta multimedia CSS, que confirma que se usa en la página web.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-115">The following CSS media query is displayed, which confirms that it is used on the webpage.</span></span>

    ```css
    @media (prefers-reduced-motion: no-preference) {
      html {
        scroll-behavior: smooth;
      }
    }
    ```

    <span data-ttu-id="d6b4a-116">A continuación, emula la configuración del sistema operativo para reducir la animación, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-116">Next, emulate the operating system setting to reduce animation, as follows.</span></span>

1.  <span data-ttu-id="d6b4a-117">Seleccione **Esc** para abrir el cajón en la parte inferior de DevTools.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-117">Select **Esc** to open the Drawer at the bottom of DevTools.</span></span>  <span data-ttu-id="d6b4a-118">Seleccione el **botón Más herramientas** ( ) en la parte superior del cajón para ver la lista de herramientas y, a continuación, seleccione **+** **Representación**.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-118">Select the **More tools** (**+**) button at the top of the Drawer to see the list of tools, and then select **Rendering**.</span></span>  

1.  <span data-ttu-id="d6b4a-119">En la lista desplegable Emular medios **CSS prefers-reduced-motion,** seleccione **prefers-reduced-motion: reduced**.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-119">In the **Emulate CSS media feature prefers-reduced-motion** dropdown list, select **prefers-reduced-motion: reduced**.</span></span>

    :::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulación de movimiento reducido y CSS que asegura que el desplazamiento suave solo se produce cuando el usuario lo desea" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
        <span data-ttu-id="d6b4a-121">Simulación de movimiento reducido y CSS que asegura que el desplazamiento suave solo se produce cuando el usuario lo desea</span><span class="sxs-lookup"><span data-stu-id="d6b4a-121">Simulating reduced motion and the CSS that makes sure that smooth scrolling only happens when the user wants it</span></span>
    :::image-end:::

1.  <span data-ttu-id="d6b4a-122">En la página web, seleccione los elementos de menú azul, como **Equinos** o **Alpacas**.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-122">In the webpage, select the blue menu items, such as **Horses** or **Alpacas**.</span></span>  <span data-ttu-id="d6b4a-123">Ahora, la página web se desplaza instantáneamente a la sección seleccionada, en lugar de usar la animación de desplazamiento suave.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-123">Now the webpage instantly scrolls to the selected section, rather than using the smooth-scrolling animation.</span></span>

1.  <span data-ttu-id="d6b4a-124">En la **herramienta Representación,** debajo **de Emular**la característica multimedia CSS prefiere el movimiento reducido, seleccione **Sin emulación** para quitar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-124">In the **Rendering** tool, below **Emulate CSS media feature prefers-reduced-motion**, select **No emulation** to remove this setting.</span></span>
   
<span data-ttu-id="d6b4a-125">Observe que la página web de demostración todavía ejecuta las siguientes animaciones, incluso con la configuración de emulación y consulta multimedia anterior.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-125">Notice that the demo webpage still runs the following animations, even with the above media query and emulation settings.</span></span> <span data-ttu-id="d6b4a-126">Al crear el producto web, asegúrese de corregir todas las animaciones similares.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-126">When building your web product, ensure you fix all similar animations.</span></span>  
*  <span data-ttu-id="d6b4a-127">Animación de los elementos del menú azul al pasar el puntero sobre ellos.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-127">Animation of the blue menu items when you hover over them.</span></span>
*  <span data-ttu-id="d6b4a-128">Animación de los círculos en los **vínculos Más** al pasar el puntero sobre ellos.</span><span class="sxs-lookup"><span data-stu-id="d6b4a-128">Animation of the circles on the **More** links when you hover over them.</span></span>



## <a name="see-also"></a><span data-ttu-id="d6b4a-129">Consulta también</span><span class="sxs-lookup"><span data-stu-id="d6b4a-129">See also</span></span>

*  [<span data-ttu-id="d6b4a-130">Simulación de movimiento reducida</span><span class="sxs-lookup"><span data-stu-id="d6b4a-130">Reduced motion simulation</span></span>](reduced-motion-simulation.md)
*  [<span data-ttu-id="d6b4a-131">Información general sobre las pruebas de accesibilidad con DevTools</span><span class="sxs-lookup"><span data-stu-id="d6b4a-131">Overview of accessibility testing using DevTools</span></span>](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d6b4a-132">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d6b4a-132">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
