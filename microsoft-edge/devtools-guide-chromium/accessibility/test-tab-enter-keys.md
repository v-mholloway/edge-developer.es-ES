---
description: Compruebe la compatibilidad con el teclado con las teclas Tab y Enter.
title: Comprobar la compatibilidad con el teclado mediante las teclas Tab y Enter
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 48151e16a9059b5ebaadca36f29447d4ad3be8c7
ms.sourcegitcommit: 34feec6ae6241c598911dac7b63c28d655691233
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2021
ms.locfileid: "11597653"
---
# <a name="check-for-keyboard-support-by-using-the-tab-and-enter-keys"></a>Comprobar la compatibilidad con el teclado mediante las teclas Tab y Enter


No todos los usuarios tienen un puntero o un dispositivo táctil y no todos los usuarios pueden ver los proyectos web que creamos.  Por este motivo, es importante que la interfaz de usuario funcione al menos con un teclado.  Asegúrese de que puede usar la clave para mover el foco a cada control de formulario de una página web y asegúrese de que puede usar la `Tab` `Enter` clave para enviar formularios.

Puede probar la facilidad de uso de una página web para los usuarios de teclado de varias maneras:
*  Mediante el uso del teclado, en particular `Tab` las teclas , y `Shift` + `Tab` `Enter` .  Este enfoque se describe en este artículo.
*  Compruebe si hay compatibilidad con el teclado para un elemento individual mediante la **herramienta Inspeccionar.**  La superposición de información de la herramienta Inspeccionar incluye una sección **Accesibilidad** que incluye una fila con enfoque **de** teclado.  
*  Consulte la sección **** **Accesibilidad** del informe Problemas para ver los problemas de compatibilidad con el teclado.

Para comprobar si hay problemas de accesibilidad en la página de demostración con un teclado en lugar de un mouse, siga estos pasos:

1.  Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una nueva pestaña del explorador.

1.  Usa un teclado para navegar por el documento de demostración, usando las `Tab` teclas y para saltar de un elemento a `Shift` + `Tab` otro.  En la página web de demostración, `Tab` la clave primero mueve el foco al formulario de búsqueda de la `header` sección.

1.  Seleccione `Tab` para colocar el foco en un botón y, a continuación, seleccione para hacer clic en el botón `Enter` centrado.  Por ejemplo, en la página de demostración, seleccione para poner el foco en el campo Búsqueda y, a `Tab` continuación, seleccione enviar la **** `Enter` búsqueda.  Este enfoque produce el mismo resultado que seleccionar el **botón ir.**  La selección `Enter` para enviar el formulario **de** búsqueda funciona correctamente.

1.  Vuelva `Tab` a seleccionar.  El siguiente elemento en el que pone el foco es el primer vínculo **Más** de la sección de la página web, tal como `content` se indica en un esquema.
    
    :::image type="complex" source="../media/a11y-testing-keyboard-focus-on-element.msft.png" alt-text="Navegar por el documento con el teclado y la tecla "Tab". El foco se muestra en un vínculo del documento." lightbox="../media/a11y-testing-keyboard-focus-on-element.msft.png":::
        Navegar por el documento con el teclado y la tecla de tabulación. El foco se muestra en un vínculo del documento.
    :::image-end:::
    
1.  Seleccione `Tab` varias veces más hasta que pase el último vínculo **Más.**  La página se desplaza hacia arriba y parece que está en un elemento de la página, pero no hay forma de saber qué elemento es.

1.  Observe la dirección URL en la parte inferior izquierda.  Si miras a la parte inferior izquierda de la pantalla (o si usas un lector de pantalla), te das cuenta de que estás en el menú de navegación de la barra lateral con vínculos azules, ya que el explorador muestra la dirección URL a la que apunta el vínculo **Gatos** ( `#cats` ).

    :::image type="complex" source="../media/a11y-testing-lack-of-focus-style.msft.png" alt-text="La falta de estilo de foco hace imposible saber dónde se encuentra actualmente en el documento. La única sugerencia es la presentación del destino del vínculo en la esquina inferior izquierda de la pantalla" lightbox="../media/a11y-testing-lack-of-focus-style.msft.png":::
        La falta de estilo de foco hace imposible saber dónde se encuentra actualmente en el documento. La única sugerencia es la presentación del destino del vínculo en la esquina inferior izquierda de la pantalla.
    :::image-end:::

1.  Seleccione `Tab` de nuevo para ir al campo de entrada del formulario de donación.  Sin embargo, no puede alcanzar los botones situados encima del cuadro de texto seleccionando `Tab` . No puede usar el teclado para poner el foco en los **botones 50,** **100**o **200** y, a continuación, seleccionarlos.  Además, al seleccionar `Enter` no se envía el formulario de donación.

    :::image type="complex" source="../media/a11y-testing-form-field-with-outline.msft.png" alt-text="El único elemento accesible con teclado en el formulario de donación es el campo de entrada de texto" lightbox="../media/a11y-testing-form-field-with-outline.msft.png":::
        El único elemento accesible con teclado en el formulario de donación es el campo de entrada de texto
    :::image-end:::
    
1.  La selección vuelve a poner el foco en la barra de navegación superior de la página, con botones de menú para Inicio `Tab` , Adoptar **una**mascota, **Donar**, **Trabajos**y **Acerca de nosotros**. ****  Seleccione o ponga el foco en un botón de menú, tal como `Tab` `Shift` + `Tab` indica un esquema de enfoque.  A `Enter` continuación, seleccione para obtener acceso a esa sección de la página web.

    :::image type="complex" source="../media/a11y-testing-menu-with-outline.msft.png" alt-text="El menú principal tiene un resaltado y un esquema de enfoque, por lo que es accesible con teclado" lightbox="../media/a11y-testing-menu-with-outline.msft.png":::
        El menú principal tiene un resaltado y un esquema de enfoque, por lo que es accesible con teclado
    :::image-end:::
    
Basándonos en el tutorial anterior, encontramos los siguientes problemas que deben solucionarse.

*  Al usar un teclado, los vínculos azules del menú de navegación de la barra lateral no indican visualmente qué vínculo tiene el foco.  Para obtener más información, vaya a Analizar la falta de indicación del [foco del teclado en un menú de la barra lateral](test-analyze-no-focus-indicator.md).

*  En el formulario de donación, los botones de cantidad y el botón **Donar** no funcionan con un teclado.  Para obtener más información, vaya a Analizar la falta de compatibilidad [con teclado en un formulario](test-analyze-no-keyboard-support.md).

*  El orden del acceso del teclado a través de las secciones de la página no es correcto.  Navegas por todos los vínculos **Más** del documento antes de llegar al menú de navegación de la barra lateral.  Cuando la tecla pone el foco en el menú de navegación de la barra lateral, ya has recorrido `Tab` todo el contenido de la página. El menú de navegación de la barra lateral estaba pensado para proporcionar un acceso fácil al contenido de la página.  Para obtener más información sobre cómo resolver este problema, vaya a Probar compatibilidad [con teclado mediante el Visor de pedidos de origen](test-tab-key-source-order-viewer.md).


## <a name="see-also"></a>Consulta también

*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
