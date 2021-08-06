---
description: Inspeccione la accesibilidad de todos los estados de los elementos, como el contraste de texto durante el estado de desplazamiento, en el panel Estilos mediante El estado del elemento Toggle.
title: Comprobar la accesibilidad de todos los estados de elementos
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 3603723910a60f06fab30bdac4e934dbca48c5696b9a163b4ea120b4edbc822f
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802430"
---
# <a name="verify-accessibility-of-all-states-of-elements"></a>Comprobar la accesibilidad de todos los estados de elementos

<!-- 5. STYLES: TOGGLE STATE -->

Compruebe la accesibilidad de todos los estados de los elementos, como el contraste de color del texto durante el `hover` estado.  La **herramienta Inspeccionar** informa de problemas de accesibilidad de un estado a la vez.  Para comprobar la accesibilidad de los **** distintos estados de los elementos, en la pestaña Estilos, seleccione **\:hov** (**Toggle Element State**), tal como se describe en este artículo. Primero se muestra por qué es necesaria la simulación de estado con la herramienta **Inspeccionar** y, a continuación, se muestra cómo usar la simulación de estado.


## <a name="checking-text-color-contrast-in-the-default-state"></a>Comprobar el contraste de color del texto en el estado predeterminado

<!-- Inspect tool: information overlay: Accessibility section: Contrast row -->

Además de las pruebas automáticas de contraste de color en la herramienta **Problemas,** también puede usar la herramienta **Inspeccionar** para comprobar si los elementos de página individuales tienen suficiente contraste.  Si la información de contraste está disponible, la superposición **Inspeccionar** muestra la relación de contraste y un elemento de casilla.  Un icono de marca de verificación verde indica que hay suficiente contraste y un icono de alerta amarilla indica que no hay suficiente contraste.

Por ejemplo, los vínculos del menú de navegación de la barra lateral tienen suficiente contraste.  Pero el elemento **verde de** la lista Perros de la sección **Estado** de donación no tiene suficiente contraste, por lo que se marca mediante una advertencia en la superposición **Inspeccionar.**

:::row:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-enough-contrast.msft.png" alt-text="Los vínculos del menú de navegación de la barra lateral tienen suficiente contraste, como se muestra en la superposición Inspeccionar" lightbox="../media/a11y-testing-enough-contrast.msft.png":::
            Los vínculos del menú de navegación de la barra lateral tienen suficiente contraste, como se muestra en **la superposición Inspeccionar** :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/a11y-testing-not-enough-contrast.msft.png" alt-text="Un elemento que no tiene suficiente contraste se marca mediante una advertencia en la superposición Inspeccionar" lightbox="../media/a11y-testing-not-enough-contrast.msft.png":::
            Un elemento que no tiene suficiente contraste se marca mediante una advertencia en la **superposición Inspeccionar** :::image-end:::
    :::column-end:::
:::row-end:::
        

## <a name="hovering-when-the-inspect-tool-is-active-doesnt-show-the-text-color-contrast-for-the-hover-state"></a>Si se activa la herramienta Inspeccionar, no se muestra el contraste de color de texto para el estado de desplazamiento

La **superposición** de información de la herramienta Inspeccionar solo representa un solo estado.  Los elementos de la página pueden tener estados diferentes, todos los cuales deben probarse.  Por ejemplo, al pasar el puntero del mouse sobre el menú de la página de demostración de pruebas de accesibilidad, se obtiene una animación que cambia los colores. Para ello, realice los siguientes pasos:

1.  Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una pestaña nueva.

1.  Mantenga el mouse sobre los elementos de menú azul del menú de navegación de la barra lateral.  Observe que cada elemento tiene una animación.

    :::image type="complex" source="../media/a11y-testing-hover.msft.png" alt-text="Elemento de menú que muestra diferentes colores cuando el puntero del mouse está sobre él" lightbox="../media/a11y-testing-hover.msft.png":::
        Elemento de menú que muestra diferentes colores cuando el puntero del mouse está sobre él
    :::image-end:::
    
Ahora, use la herramienta Inspeccionar. Cuando se usa la herramienta Inspeccionar, las animaciones de los elementos del menú no se ejecutarán al pasar el puntero sobre ellos.  Al usar la herramienta Inspeccionar, no puede alcanzar el estado de los elementos de menú para probar la relación de contraste, ya que el estado de los estilos no `hover` `hover` se desencadena.  
    
Para confirmar que las animaciones no se ejecutan, siga estos pasos.
    
1.  Seleccione el **botón Inspeccionar** \( el botón Inspeccionar \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).

1.  Mantenga el mouse sobre los vínculos azules del menú de navegación de la barra lateral.  Las animaciones de los elementos de menú no se ejecutan. En su lugar, los elementos de menú se muestran con colores y resaltados para la superposición de flexbox.

Comprobar el contraste de texto suficiente de esta manera no es suficiente, ya que los elementos de la página podrían tener estados diferentes.


## <a name="use-state-simulation-to-simulate-the-hover-state-of-an-animated-menu-item"></a>Usar la simulación de estado para simular el estado de desplazamiento de un elemento de menú animado 

<!-- Elements tool: Styles pane: Toggle Element State -->

Cuando la **herramienta Inspeccionar** está activa, en lugar de pasar el mouse sobre un elemento animado, debe simular el estado del elemento de menú.  Para simular el estado de un elemento de menú, use la simulación de estado en el **panel Estilos.**  El **panel Estilos** tiene un botón **\:hov** (**Toggle Element State**), que muestra un grupo de casillas con la etiqueta Force **element state**.

Para activar el estado del mouse mientras se usa la herramienta Inspeccionar:

1.  Si aún no está abierto, abra la página web de demostración [de][DevToolsA11yErrorsDemopage] pruebas de accesibilidad en una nueva pestaña.  A **continuación, seleccione F12** para abrir DevTools.

1.  Seleccione el **botón Inspeccionar** \( Inspeccionar botón de herramienta \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).

1.  En la página web representada, seleccione el vínculo **azul Gatos** en el menú de navegación de la barra lateral.  Se **abre** la herramienta Elementos, con el elemento `<a href="#cats">Cats</a>` seleccionado.

    :::image type="complex" source="../media/a11y-testing-inspecting-link-to-hover.msft.png" alt-text="Inspeccionar el elemento que tiene un estado de puntero en la herramienta Elementos" lightbox="../media/a11y-testing-inspecting-link-to-hover.msft.png":::
        Inspeccionar el elemento que tiene un estado de puntero en la herramienta Elementos
    :::image-end:::

1.  Seleccione la **pestaña Estilos.**  El elemento seleccionado tiene un estado en el CSS que se aplica a él, pero que no `a` está visible en el panel `hover` **Estilos.** 

1.  En el **panel Estilos,** a la derecha de la regla de `#sidebar nav li a` estilo, seleccione el `styles.css` vínculo.  Se **abre la herramienta** Orígenes.  A continuación, busque la regla de pseudo-clase CSS `#sidebar nav li a:hover` .  Esta regla no se ejecuta cuando la **herramienta Inspeccionar** está activa.  Simularemos la ejecución de esta regla de estado en los pasos siguientes.

1.  Seleccione la **herramienta** Elementos.  A continuación, en el panel **Estilos,** seleccione **el botón :hov** (**Toggle Element State**).  Se **muestra el grupo de** casillas De estado del elemento Force.

    :::image type="complex" source="../media/a11y-testing-state-simulation.msft.png" alt-text="La herramienta de simulación de estado que muestra todas las opciones" lightbox="../media/a11y-testing-state-simulation.msft.png":::
        La herramienta de simulación de estado que muestra todas las opciones
    :::image-end:::

1.  Active la **casilla :hover.**  En el DOM, a la izquierda del elemento, aparece un punto amarillo que indica que el `<a href="#cats">Cats</a>` elemento tiene un estado simulado.  El **elemento de** menú Gatos ahora aparece en la página web como si el puntero estuviera sobre él.  Es posible que se ejecute la animación en el elemento de menú.

    :::image type="complex" source="../media/a11y-testing-hover-simulated.msft.png" alt-text="DevTools simulando un estado de puntero" lightbox="../media/a11y-testing-hover-simulated.msft.png":::
        DevTools simulando un estado de puntero
    :::image-end:::

    Después de aplicar el estado simulado, puede volver a usar la herramienta **Inspeccionar** para comprobar el contraste del elemento cuando el usuario mantiene el mouse sobre él, como se muestra a continuación.

1.  Seleccione el **botón Inspeccionar** \( Icono inspector \) en la esquina superior izquierda de DevTools para que el icono esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).

1.  Mantenga el mouse sobre el vínculo **azul Gatos** en el menú de navegación de la barra lateral.  El vínculo ahora es azul claro, debido a la animación de desplazamiento simulada.  Aparece **la** superposición de información de la herramienta **** Inspeccionar, que muestra un signo de exclamación naranja en la fila Contraste, lo que indica que el contraste no es lo suficientemente alto.

    :::image type="complex" source="../media/a11y-testing-hover-contrast-testing.msft.png" alt-text="Probar el contraste de un elemento en un estado de puntero simulado" lightbox="../media/a11y-testing-hover-contrast-testing.msft.png":::
        Probar el contraste de un elemento en un estado de puntero simulado
    :::image-end:::

La simulación de estado también es una buena forma de comprobar si se han considerado diferentes necesidades de usuario, como las necesidades de los usuarios de teclado.  Al usar las casillas De estado **del** elemento Force, puedes simular el estado para detectar que la interfaz de usuario permanece sin cambios `:focus` cuando tiene el foco. Esta falta de un indicador cuando un elemento tiene el foco es un problema.


## <a name="see-also"></a>Consulte también

*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
