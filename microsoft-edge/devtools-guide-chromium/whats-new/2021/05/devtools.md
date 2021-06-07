---
description: El botón Más herramientas, documentación en contexto para empezar a usar la extensión DevTools, mayor compatibilidad para lectores de pantalla en la consola y mucho más.
title: Novedades de DevTools (Microsoft Edge 92)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ebd512800b8e55b5e9c0001c314a7c08fd242d5d
ms.sourcegitcommit: 30817cd9ae187a716d14d06962eb23b32dd54548
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "11590897"
---
# <a name="whats-new-in-devtools-microsoft-edge-92"></a>Novedades de DevTools (Microsoft Edge 92)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

> [!TIP]
> La **conferencia de Microsoft Build 2021** fue del 25 al 27 de mayo.  Este es un vídeo de Build about the updates to DevTools: [Microsoft Edge | Estado de la plataforma:][YoutubeEdgeStateOfThePlatform] Microsoft Edge una plataforma atractiva y coherente con herramientas para desarrolladores.  A medida que nuestros exploradores heredados no sean compatibles, Edge pronto será el único explorador compatible de Microsoft en Windows 10.  Únase a nosotros para obtener información sobre lo último en la plataforma perimetral, las herramientas y las aplicaciones web.


## <a name="the-close-button-is-no-longer-hidden-when-devtools-is-narrow"></a>El botón Cerrar ya no está oculto cuando DevTools es estrecho

<!-- Title: DevTools is now easier to close -->  
<!-- Subtitle: The Close button in DevTools is always displayed, even when DevTools is docked to the right and the DevTools viewport is narrow. -->  

En Microsoft Edge versión 91 o anterior, el botón Cerrar para cerrar DevTools no se muestra cuando la ventanilla de DevTools es estrecha. ****  En Microsoft Edge versión 92, **** el botón Cerrar de DevTools siempre está presente, independientemente del ancho de la ventanilla de DevTools.

:::image type="complex" source="../../media/2021/05/close-devtools-button-always-displayed.msft.png" alt-text="El botón Cerrar DevTools ahora está presente incluso cuando la ventanilla es estrecha" lightbox="../../media/2021/05/close-devtools-button-always-displayed.msft.png":::
   El **botón Cerrar** DevTools ahora está presente incluso cuando la ventanilla es estrecha  
:::image-end:::  


## <a name="add-tools-quickly-with-the-new-more-tools-button"></a>Agregar herramientas rápidamente con el nuevo botón Más herramientas

<!-- Title: Add tools quickly with the new More Tools button -->  
<!-- Subtitle: Learn about a new convenient way to open tools in Microsoft Edge DevTools. -->  

Hay una nueva forma de abrir más herramientas en Microsoft Edge DevTools: el **menú Más herramientas** ( ) `+` . El **menú Más herramientas** aparece en la barra de herramientas del panel principal y en la barra de herramientas del cajón. Al seleccionar una herramienta en el **menú Más herramientas,** se agrega la herramienta a la barra de herramientas.

Para reordenar las pestañas de cualquiera de las barras de herramientas, seleccione y arrastre las pestañas.  

El **menú Más herramientas** estaba disponible como un experimento en Microsoft Edge versión 89 y ahora siempre está presente.

:::image type="complex" source="../../media/2021/05/more-tools-button.msft.png" alt-text="El botón Más herramientas de la barra de herramientas superior y la barra de herramientas del cajón" lightbox="../../media/2021/05/more-tools-button.msft.png":::
   El **botón Más herramientas** de la barra de herramientas superior y la barra de herramientas del cajón
:::image-end:::  

:::image type="complex" source="../../media/2021/05/more-tools-menu.msft.png" alt-text="Menú Más herramientas" lightbox="../../media/2021/05/more-tools-menu.msft.png":::
   Menú **Más** herramientas
:::image-end:::  


## <a name="improvements-for-hovering-selecting-and-closing-tools"></a>Mejoras para activar, seleccionar y cerrar herramientas

<!-- Title: Improvements to tab interactions -->
<!-- Subtitle: Interactions related to hovering, selecting, and closing tools are more predictable. -->

Las pestañas de cada herramienta se han reformateado para reducir la posibilidad de cerrar accidentalmente una herramienta.  En cada pestaña de la barra de herramientas principal y en la barra de herramientas del cajón, agregamos:
*  Espaciado alrededor de la pestaña.
*  Espaciado alrededor del botón cerrar ( `x` ) de la ficha.
*  Color de fondo al pasar el mouse sobre la pestaña.
*  Información sobre herramientas para el botón cerrar ( `x` ) de la pestaña.
*  Contraste superior para el botón cerrar ( `x` ) de la ficha.

Por ejemplo, cuando estás **** en la herramienta **** Rendimiento y mantienes el mouse sobre la pestaña de la herramienta Red, estas mejoras ayudan a evitar el cierre accidental de la **herramienta Red.**

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-before.msft.png" alt-text="Pestañas antes de reformatear" lightbox="../../media/2021/05/hovering-on-tool-tab-before.msft.png":::
           Pestañas antes de reformatear :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/hovering-on-tool-tab-after.msft.png" alt-text="Pestañas después de la reformateado" lightbox="../../media/2021/05/hovering-on-tool-tab-after.msft.png":::
           Pestañas después de la reformateado :::image-end:::
    :::column-end:::
:::row-end:::

Estas mejoras son especialmente relevantes para los usuarios de DevTools localizados, en los que las pestañas pueden ser más estrechas y fáciles de cerrar accidentalmente.

:::image type="complex" source="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png" alt-text="Localized DevTools con pestañas estrechas" lightbox="../../media/2021/05/hovering-reduced-chance-of-closing-tab.msft.png":::
   Localized DevTools con pestañas estrechas
:::image-end:::

También facilitamos volver a agregar una herramienta que ha cerrado agregando un menú Más herramientas [a](#add-tools-quickly-with-the-new-more-tools-button) la barra de herramientas principal y la barra de herramientas del cajón.


## <a name="better-support-for-screen-readers-in-the-console"></a>Mejor compatibilidad con lectores de pantalla en la consola

<!-- Title: Better screen reader support in the Console -->
<!-- Subtitle: Assistive technologies can now announce autocomplete suggestions and evaluated expressions in the Console. -->

Antes de Microsoft Edge versión 92, en la **Consola,** las tecnologías de asistencia, como los lectores de pantalla, no anunciaban sugerencias de autocompletar ni los resultados de las expresiones evaluadas. Esto se ha corregido ahora.

:::row:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png" alt-text="En la consola, los lectores de pantalla ahora anuncian la sugerencia de autocompletar seleccionada actualmente" lightbox="../../media/2021/05/screen-reader-support-in-console-autocomplete.msft.png":::
           En la **Consola,** los lectores de pantalla ahora anuncian la sugerencia de autocompletar seleccionada actualmente :::image-end:::
    :::column-end:::
    :::column:::
        :::image type="complex" source="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png" alt-text="En la consola, los lectores de pantalla ahora anuncian el resultado de una expresión evaluada" lightbox="../../media/2021/05/screen-reader-support-in-console-evaluated-expression.msft.png":::
           En la **consola,** ahora los lectores de pantalla anuncian el resultado de una expresión evaluada :::image-end:::
    :::column-end:::
:::row-end:::


## <a name="microsoft-edge-developer-tools-for-visual-studio-code-version-118"></a>Microsoft Edge Developer Tools para Visual Studio Code versión 1.1.8

El [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] extension version 1.1.8 for Microsoft Visual Studio Code tiene los siguientes cambios desde la versión anterior.  Microsoft Visual Studio Code actualiza las extensiones automáticamente.  Para actualizar manualmente a la versión 1.1.8, vaya [a Actualizar una extensión manualmente.][VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]  

Puede presentar problemas y contribuir a la extensión en [vscode-edge-devtools GitHub repositorio][GithubMicrosoftVscodeEdgeDevtools].  

### <a name="in-context-documentation-and-ui-to-make-it-easier-to-use-the-devtools-extension"></a>Documentación e interfaz de usuario en contexto para facilitar el uso de la extensión DevTools

<!-- Title: In-context documentation and UI make it easier to get started using the Developer Tools extension -->  
<!-- Subtitle: The Microsoft Edge Developer Tools for Visual Studio Code extension now presents helpful text, buttons, and links, and opens a documentation page with guidance on how to get started. -->  

La versión 1.1.8 de la extensión [Microsoft Edge Developer Tools for Visual Studio Code][VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools] ahora presenta una forma más sencilla de iniciar una nueva instancia de Microsoft Edge, presentando instrucciones, botones, vínculos y una página de documentación que le guiará.

*  Cuando selecciona el botón herramientas de **** **Microsoft Edge** en la barra de actividades de Visual Studio Code, el panel Herramientas de **Microsoft Edge:** Destinos ahora presenta texto explicativo, botones y vínculos para guiarlo, en lugar de un panel en blanco.

*  Al abrir una nueva instancia de Microsoft Edge desde dentro de Visual Studio Code, Microsoft Edge muestra ahora una página de inicio que explica cómo usar la extensión Herramientas de desarrollo, en lugar de una página en blanco.

*  El **panel herramientas Microsoft Edge:** destinos ahora tiene un botón Generar **launch.jsen** y las instrucciones, para ayudar a iniciar el proyecto para la depuración en Microsoft Edge.

Para obtener más información, vaya [a Uso de las herramientas][GithubIoDevToolsUsing].


## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si tiene Windows, Linux o macOS, considere la posibilidad de usar los [canales de versión preliminar de Microsoft Edge][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  


## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]

<!-- links -->  
[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubIoDevToolsUsing]: https://microsoft.github.io/vscode-edge-devtools/using.html "Uso de las herramientas | GitHub"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de versiones preliminares de Microsoft Edge"  

[VisualstudioCodeDocsEditorExtensionGalleryUpdateExtensionManually]: https://code.visualstudio.com/docs/editor/extension-gallery#_update-an-extension-manually "Actualizar una extensión manualmente: Marketplace de extensiones | Visual Studio Code"  

[VisualstudioMarketplaceMsEdgedevtoolsVscodeEdgeDevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Herramientas de desarrollador para Visual Studio Code | Visual Studio Marketplace"  

[YoutubeEdgeStateOfThePlatform]: https://www.youtube.com/watch?v=sU0WRZ0kkNo "Microsoft Edge: Estado de la plataforma | YouTube"

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
