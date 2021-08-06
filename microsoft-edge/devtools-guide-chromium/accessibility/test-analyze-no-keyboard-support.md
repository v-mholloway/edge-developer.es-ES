---
description: Analizar la falta de compatibilidad con teclado en un formulario que usa el elemento div con la herramienta Inspeccionar y la pestaña Escuchas de eventos.
title: Analizar la compatibilidad con teclado en formularios con DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: c8fb22e42d0edd8e064a06983b66e6c3c2c974b73cbab4209daee1ac2c818f58
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802565"
---
# <a name="analyze-keyboard-support-on-forms-using-the-devtools"></a>Analizar la compatibilidad con teclado en formularios con DevTools

En este artículo se usa **la herramienta Inspeccionar** y la pestaña Escuchas de eventos para analizar la falta de compatibilidad con el teclado en una página de demostración que tiene **botones** que usan el `div` elemento.

En el **formulario Donar,** los botones de cantidad y el botón **Donar** no funcionan con un teclado.  La depuración del formulario de donación requiere comprender por qué la falta de estilo de foco no se marca como un problema con herramientas de prueba automáticas como **la herramienta Problemas.**  En este ejemplo, los botones se implementan mediante elementos, que estas herramientas no reconocen como `div` un control en un formulario.

Para usar la herramienta Inspeccionar y la pestaña Escuchas de eventos para analizar la falta de compatibilidad con el teclado en la página de demostración:

<!-- 1. Inspect tool: Accessibility section: keyboard-focusable row -->

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.
    
1.  Seleccione el **botón Inspeccionar** \( Inspeccionar icono \) en la esquina superior izquierda de DevTools para que el botón esté ![ resaltado ](../media/inspect-icon.msft.png) (azul).

1.  Mantenga el mouse sobre los botones de donación **50,** **100**y **200.**  La herramienta Inspeccionar aparece en la página web, como una superposición.  La **fila centrada en** el teclado de la superposición Inspeccionar muestra que ninguno de los botones de cantidad de donación es accesible para el teclado, como indica un círculo gris con línea diagonal.  Los botones no tienen nombre y tienen un rol de porque son elementos, lo que significa que los botones no son accesibles para la tecnología `generic` `div` de asistencia.

    :::image type="complex" source="../media/a11y-testing-donation-button-info.msft.png" alt-text="Al inspeccionar los botones del formulario, se muestra que no son accesibles con teclado" lightbox="../media/a11y-testing-donation-button-info.msft.png":::
        Al inspeccionar los botones del formulario, se muestra que no son accesibles con teclado
    :::image-end:::
    
1.  Cuando la **herramienta Inspeccionar** esté activa, en la página web, seleccione el **cuadro** de texto Otra entrada, encima del **botón Donar.**  Se **abre** la herramienta Elementos, que muestra el árbol DOM de la página web.  El elemento `<input id="freedonation" class="smallinput">` está seleccionado.

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

    El uso de los elementos and en el cuadro de texto Otros es válido, lo que significa que la etiqueta Otros está vinculada `label` `input` correctamente con el cuadro de texto de entrada. **** ****  El `input` cuadro de texto también es accesible con teclado.  El resto del marcado del formulario son elementos, que son fáciles de `div` aplicar, pero que no tienen ningún significado semántico.

    <!-- 2. Elements tool: Event Listeners tab -->

    La funcionalidad del formulario se crea con JavaScript y puede probarla comprobando la pestaña **Escuchas de** eventos, de la siguiente manera.

1.  Con el elemento aún seleccionado en el árbol DOM, seleccione la pestaña Escuchas de eventos a la derecha de la pestaña Estilos y, a `<input id="freedonation" class="smallinput">` continuación, expanda la escucha de **** **** `click` eventos.

    :::image type="complex" source="../media/a11y-testing-event-handlers-on-button.msft.png" alt-text="La herramienta escuchas de eventos que muestra dónde está JavaScript que hace que el formulario funcione" lightbox="../media/a11y-testing-event-handlers-on-button.msft.png":::
        La herramienta escuchas de eventos que muestra dónde está JavaScript que hace que el formulario funcione
    :::image-end:::

1.  Seleccione el `buttons.js:18` vínculo.  Se **abre la herramienta** Orígenes, que muestra el JavaScript aplicado.

    :::image type="complex" source="../media/a11y-testing-form-handling-javascript.msft.png" alt-text="El JavaScript responsable de la funcionalidad del formulario de donación, que se muestra en la herramienta Orígenes" lightbox="../media/a11y-testing-form-handling-javascript.msft.png":::
        El JavaScript responsable de la funcionalidad del formulario de donación, que se muestra en la herramienta Orígenes
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

Usar un `click` evento para leer los botones es una buena práctica, ya que un evento se dispara tanto en la interacción con el puntero del mouse como con el `click` teclado.  Sin embargo, como un elemento no es accesible para teclado y este botón Donar se implementa como un elemento ( ), esta funcionalidad de JavaScript nunca se ejecuta a menos que use un mouse u otro origen de un evento, como un botón especial disponible en algunos `div` **** `div` `<div class="submitbutton">Donate</div>` `click` teclados.

Este es un ejemplo clásico en el que Se agregó JavaScript para crear funciones `button` que los elementos proporcionan de forma nativa.  La simulación de la funcionalidad de los `div` botones con elementos acabó produciendo una experiencia inaccesible.


## <a name="see-also"></a>Consulte también

*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
