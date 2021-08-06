---
description: Comprueba que las páginas web se pueden usar con la animación de la interfaz de usuario desactivada (movimiento reducido) con la característica multimedia Emular CSS prefiere la lista desplegable de movimiento reducido en la herramienta de representación.
title: Verificar si la página se puede usar con la animación de la interfaz de usuario desactivada
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 13c41918aee9e590a0e89707d3ee031751af42a2a4d8f2f9d7fc79f48dd39867
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802245"
---
# <a name="verify-that-the-page-is-usable-with-ui-animation-turned-off"></a>Verificar si la página se puede usar con la animación de la interfaz de usuario desactivada

Una página web no debe mostrar animaciones a un usuario que a desactivar las animaciones en el sistema operativo.  Las animaciones pueden ayudar a la facilidad de uso de un producto, pero también pueden causar distracción, confusión o náuseas.

Para comprobar que una página web se puede usar con **** la animación de la interfaz de usuario desactivada (movimiento reducido), en la herramienta Representación, usa la lista desplegable Emular medios **CSS prefers-reduced-motion.**

En la página web de demostración de pruebas de accesibilidad, cuando desactivas las animaciones en el sistema operativo o emulas esa configuración mediante DevTools, la página web no usa un desplazamiento suave al seleccionar los vínculos del menú de navegación de la barra lateral.  Esto se logra ajustando la configuración de desplazamiento suave en CSS **** en una consulta multimedia y, a continuación, mediante la herramienta de representación para emular la configuración del sistema operativo para la animación reducida.

Para comprobar si la página se puede usar con animaciones desactivadas:

1.  Abra la [página web de demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad en una nueva pestaña del explorador y, a continuación, seleccione **F12** para abrir DevTools.

1.  En la parte superior de DevTools, seleccione la herramienta **Orígenes** y, a continuación, en el **panel** navegación de la izquierda, seleccione `styles.css` .  El archivo CSS aparece en el **panel Editor.**

1.  Seleccione **Ctrl+F** en Windows/Linux o **Comando+F** en macOS y, a continuación, escriba `@media` .  Se muestra la siguiente consulta multimedia CSS, que confirma que se usa en la página web.

    ```css
    @media (prefers-reduced-motion: no-preference) {
      html {
        scroll-behavior: smooth;
      }
    }
    ```

    A continuación, emula la configuración del sistema operativo para reducir la animación, como se muestra a continuación.

1.  Seleccione **Esc** para abrir el cajón en la parte inferior de DevTools.  Seleccione el **botón Más herramientas** ( ) en la parte superior del cajón para ver la lista de herramientas y, a continuación, seleccione **+** **Representación**.  

1.  En la lista desplegable Emular medios **CSS prefers-reduced-motion,** seleccione **prefers-reduced-motion: reduced**.

    :::image type="complex" source="../media/a11y-testing-simulating-reduced-motion.msft.png" alt-text="Simulación de movimiento reducido y CSS que asegura que el desplazamiento suave solo se produce cuando el usuario lo desea" lightbox="../media/a11y-testing-simulating-reduced-motion.msft.png":::
        Simulación de movimiento reducido y CSS que asegura que el desplazamiento suave solo se produce cuando el usuario lo desea
    :::image-end:::

1.  En la página web, seleccione los elementos de menú azul, como **Equinos** o **Alpacas**.  Ahora, la página web se desplaza instantáneamente a la sección seleccionada, en lugar de usar la animación de desplazamiento suave.

1.  En la **herramienta Representación,** debajo **de Emular**la característica multimedia CSS prefiere el movimiento reducido, seleccione **Sin emulación** para quitar esta configuración.
   
Observe que la página web de demostración todavía ejecuta las siguientes animaciones, incluso con la configuración de emulación y consulta multimedia anterior. Al crear el producto web, asegúrese de corregir todas las animaciones similares.  
*  Animación de los elementos del menú azul al pasar el puntero sobre ellos.
*  Animación de los círculos en los **vínculos Más** al pasar el puntero sobre ellos.



## <a name="see-also"></a>Consulte también

*  [Simulación de movimiento reducida](reduced-motion-simulation.md)
*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
