---
description: Represente una página web emulando la configuración del sistema operativo o la configuración del explorador del esquema oscuro o claro del usuario, sin tener que cambiar la configuración de su propia máquina.  Use una consulta multimedia CSS para prefers-color-scheme, junto con una opción de representación DevTools.
title: Emular esquemas oscuros o claros en la página representada
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: c233fc26af5b4c1b061b84e7dd3998b24671696b261c345d8affa8f4b550e50d
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11802623"
---
# <a name="emulate-dark-or-light-schemes-in-the-rendered-page"></a>Emular esquemas oscuros o claros en la página representada

Muchos sistemas operativos tienen una forma de mostrar cualquier aplicación en colores más oscuros o más claros.  Tener un producto web que tenga un esquema de luz en un sistema operativo en modo oscuro puede ser difícil de leer y puede ser un problema de accesibilidad para algunos usuarios.  

Para probar cómo se representará una página web cuando el usuario haya seleccionado el modo oscuro o claro, en lugar de cambiar la configuración de modo oscuro o de modo claro de su propia máquina, puede seleccionar **Emular CSS prefers-color-scheme: dark** or **light** in Microsoft Edge DevTools.  Puede hacerlo desde el menú **comando o** desde la herramienta **de** representación, como se describe a continuación.

Como alternativa, puedes hacer que tu página web seleccione automáticamente el modo oscuro o claro en función de la configuración preferida de tu equipo, **seleccionando No emulation**, que es el valor predeterminado.

Para especificar el CSS que se va a usar para esquemas claros y oscuros, use la consulta multimedia CSS [prefers-color-scheme][MDNPrefersColorScheme] para detectar si el usuario prefiere mostrar el producto en una combinación de colores oscuro o claro y, a continuación, seleccione automáticamente su propio CSS personalizado en modo claro u oscuro.  El código CSS de ejemplo se muestra [en Buscar problemas de contraste con tema oscuro y tema claro.](test-dark-mode.md)

Este artículo trata sobre cómo cambiar la apariencia de la página web en desarrollo.  Para cambiar en su lugar cómo aparece DevTools, vaya a [Aplicar temas de color a DevTools][DevtoolsCustomizeTheme].


## <a name="emulating-dark-or-light-mode-using-the-rendering-tool"></a>Emular el modo oscuro o claro con la herramienta de representación

1.  En DevTools, abra la **herramienta DevTools.**  Para ello, es posible que deba seleccionar el icono Más **herramientas** (+) en la barra de herramientas principal y, a continuación, seleccione **Representación**.

1.  En la lista desplegable Emular elementos multimedia **CSS prefers-color-scheme,** seleccione **prefers-color-scheme: dark** o **prefers-color-scheme: light**.

    :::image type="complex" source="../media/css-elements-styles-qs-simulated-light-mode.msft.png" alt-text="Emular el modo oscuro o claro con la herramienta de representación" lightbox="../media/css-elements-styles-qs-simulated-light-mode.msft.png":::
       Emular el modo oscuro o claro con la **herramienta de representación**
    :::image-end:::  

1.  Actualice la página para mostrar el resultado representado.

    Ahora puede modificar su CSS y ver el resultado representado de la misma manera que para cualquier otra página web.  Para obtener más información, vaya [a Introducción a ver y cambiar CSS][DevtoolsCssIndex].  

1.  Para restaurar la configuración, en la herramienta **Representación,** en la lista desplegable Emular elementos multimedia **CSS prefers-color-scheme,** seleccione **No emulation**.  Al actualizar la página, se aplicará la configuración de su propio sistema operativo o explorador para la preferencia del modo claro u oscuro.


## <a name="emulating-dark-or-light-mode-using-the-command-menu"></a>Emular el modo oscuro o claro mediante el menú comando

1.  Cuando DevTools tenga el **** foco, abra el menú `Ctrl` + `Shift` + `P` comando seleccionando \(Windows/Linux\) o `Command` + `Shift` + `P` \(macOS\).  

1.  Escriba "oscuro", "luz" o "emular".  A continuación, seleccione **Representación: Emular CSS prefers-color-scheme: dark** o **Rendering: Emular CSS prefers-color-scheme: light**y **seleccione Entrar**.

    :::image type="complex" source="../media/css-console-command-menu-rendering.msft.png" alt-text="Emular el modo oscuro o claro mediante los comandos Rendering: Emulate CSS prefers-color-scheme en el menú comando" lightbox="../media/css-console-command-menu-rendering.msft.png":::
        Emular el modo oscuro o claro con los comandos **Rendering: Emular CSS prefers-color-scheme** en el menú comando
    :::image-end:::  

    Seleccione un **comando Rendering** en lugar de un **comando Appearance.**  Los **comandos Rendering** afectan a la página web en desarrollo.  En **su lugar,** los comandos Appearance afectan a la parte DevTools de la ventana.

1.  Actualice la página para mostrar el resultado representado.
   
    Ahora puede modificar su CSS y ver el resultado representado de la misma manera que para cualquier otra página web.  Para obtener más información, vaya [a Introducción a ver y cambiar CSS][DevtoolsCssIndex].  

1.  Para restaurar la configuración, en el menú comando, escriba "emular" o "esquema" y, a continuación, seleccione Representación: No emular **CSS prefers-color-scheme**.  Al actualizar la página, se aplicará la configuración de su propio sistema operativo o explorador para la preferencia del modo claro u oscuro.


<!-- links -->  
[DevtoolsIndex]: ../index.md "Microsoft Edge (Chromium) Developer Tools | Microsoft Docs"  
[DevtoolsCustomizeTheme]: ../customize/theme.md "Aplicar temas de color a DevTools | Microsoft Docs"
[DevtoolsCssIndex]: ../css/index.md "Introducción a la visualización y cambio de css | Microsoft Docs"  
<!-- external links -->
[MDNPrefersColorScheme]: https://developer.mozilla.org/docs/Web/CSS/@media/prefers-color-scheme "prefers-color-scheme | MDN"  
