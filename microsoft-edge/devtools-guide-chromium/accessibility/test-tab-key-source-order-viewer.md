---
description: Para ver rápidamente el orden de tabulación de las secciones de una página, use el Visor de pedidos de origen en la herramienta Accesibilidad, a la derecha de la pestaña Estilos.
title: Probar la compatibilidad con teclado con el Visor de pedidos de origen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 87cb50eee00f5ad625e900d54aa03aece96f15e9bbd86eee1bad28b485f49374
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802267"
---
# <a name="test-keyboard-support-using-the-source-order-viewer"></a>Probar la compatibilidad con teclado con el Visor de pedidos de origen

El orden de origen de un documento es importante para la tecnología de asistencia y puede ser diferente del orden en que aparecen los elementos en la página representada.  Con CSS, puede volver a ordenar los elementos de página de forma visual, pero eso no significa que la tecnología de asistencia, como los lectores de pantalla, represente elementos de página en el mismo orden.  

Para asegurarse de que el documento tiene **** un orden lógico, puede usar el Visor de pedidos de origen para etiquetar distintos elementos de página con números que especifiquen el orden en el código fuente del documento.  El **Visor de pedidos de origen** está en la pestaña **Accesibilidad** (cerca de la **pestaña** Estilos).


## <a name="analyzing-the-order-of-keyboard-access-through-sections-of-the-page"></a>Analizar el orden del acceso de teclado a través de secciones de la página

La página web de [demostración][DevToolsA11yErrorsDemopage] de pruebas de accesibilidad tiene un orden de tabulación contraintético, donde los usuarios del teclado acceden al menú de navegación de la barra lateral solo después de navegar por todos los vínculos **Más.**  El menú de navegación de la barra lateral está pensado para ser un acceso directo para llegar a lo profundo del contenido de la página.  Pero como debes pasar por toda la página antes de llegar al menú de navegación de la barra lateral, ese menú de navegación no es eficaz para los usuarios de teclado.

El `Tab` orden clave de la página de demostración es:
1. El **campo** Búsqueda y, a continuación, **el botón ir** para el **campo** De búsqueda.
1. El **botón** Más de la **sección Gatos,** para navegar a una página web de "Gatos".  A continuación, los otros botones **Más,** para Perros, Ovejas, Equinos y, a continuación, Alpacas.
1. Los vínculos azules del menú de navegación de la barra lateral: **Gatos**, **Perros**, **Ovejas, Equinos**y, a continuación, **Alpacas**. ****
1. El cuadro de texto de la donación en el formulario de donación.
1. Los botones de la barra de navegación superior: **Home**, **Adopt a pet**, **Donate**, **Jobs**y, a continuación, **About Us**.
1. Interfaz de la parte superior de la ventana del explorador.

El motivo del orden de teclas confuso es que el orden experimentado al usar `Tab` un teclado viene determinado por el orden de origen del documento.  El orden experimentado con un teclado se puede modificar mediante el atributo de los elementos, lo que quita ese `tabindex` elemento del orden de origen.

En el código fuente del documento, el menú de navegación de la barra lateral aparece después del contenido principal de la página web.  CSS se usó para colocar el menú de navegación de la barra lateral por encima de la mayoría del contenido principal de la página web. 

Puede probar el orden de los elementos de página mediante el Visor de pedidos **de origen** en la **pestaña Accesibilidad.**  El **Visor de pedidos de origen** es una característica experimental. Para obtener más información, vaya [al Visor de pedidos de origen](../experimental-features/index.md#source-order-viewer).


Para activar el Visor de pedidos de origen:

1.  En DevTools, en la parte superior derecha, seleccione el botón **Configuración** \( ![ Configuración botón ](../media/settings-button-icon.msft.png) \).  

1.  A **continuación Configuración**, seleccione **Experimentos**.  

1.  Active la casilla **Visor de pedidos de** origen.

1.  En la esquina superior derecha de la **página Configuración,** seleccione **X** para cerrar la Configuración página.  En la parte superior de DevTools, el mensaje Ha cambiado una o más configuraciones que **requieren una recarga para que su efecto.** se muestra.  Seleccione el **botón Volver a cargar DevTools.**



Para activar y usar el Visor de pedidos de origen, con la página de demostración:

1.  Abra la [página web de demostración de pruebas de][DevToolsA11yErrorsDemopage] accesibilidad en una pestaña nueva.  A **continuación, seleccione F12** para abrir DevTools.

1.  En la **herramienta Elementos,** a la derecha de la **pestaña Estilos,** seleccione la **pestaña Accesibilidad.**

1.  En la **sección Visor de pedidos de** origen, active la casilla Mostrar orden **de** origen.  En la página web representada, aparecen números que indican el orden según el orden de `Tab` las líneas de código en el archivo de origen.

1.  En el árbol DOM de la **herramienta Elementos,** seleccione un elemento de diseño principal, como el `header` elemento.  Las superposiciones numéricas ahora se muestran en secciones de la página representada, que indican el orden de origen de los distintos elementos. 

    :::image type="complex" source="../media/a11y-testing-source-order-viewer.msft.png" alt-text="Al activar el Visor de pedidos de origen, se muestra el orden de los elementos del origen como superposiciones en la página" lightbox="../media/a11y-testing-source-order-viewer.msft.png":::
        Al activar el **Visor de pedidos de origen,** se muestra el orden de los elementos del origen como superposiciones en la página
    :::image-end:::
    
1.  Desplácese por la página para ver todas las superposiciones numéricas, incluida la sección de pie de página.


## <a name="see-also"></a>Consulte también

*  [Información general sobre las pruebas de accesibilidad con DevTools](accessibility-testing-in-devtools.md)


## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  


<!-- links -->
[DevToolsA11yErrorsDemopage]: https://microsoftedge.github.io/DevToolsSamples/a11y-testing/page-with-errors.html "Página web de demostración de pruebas de accesibilidad | GitHub"
