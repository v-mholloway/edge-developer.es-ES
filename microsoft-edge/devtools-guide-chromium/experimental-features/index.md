---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, experiment
ms.openlocfilehash: b366cfeccafe874bc9e76d3b66659122c5d07c69
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398682"
---
# <a name="experimental-features"></a>Características experimentales  

Microsoft Edge DevTools proporciona acceso a características experimentales que aún están en desarrollo.  Puede probar y [proporcionar comentarios antes](#providing-feedback-on-experimental-features) de publicar cada característica.  

Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, es posible que obtenga las características experimentales más recientes con el canal de Microsoft Edge Canary.  

## <a name="turn-on-experimental-features"></a>Activar características experimentales  

Para activar las características experimentales \(or off\) en Microsoft Edge, siga estos pasos.  

1.  [Abra DevTools][DevtoolsOpenMain].  
    *   Seleccione `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).  Para obtener más información, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  
1.  Abra el [panel][DevToolsCustomizeIndexSettings] Configuración.  
    *   Seleccione `Shift` + `?` .  Para obtener más información, vaya a [Métodos abreviados de teclado de Microsoft Edge DevTools][DevToolsShortcuts].  
1.  En el lado izquierdo del **panel Configuración,** elija la **sección** Experimentos.  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="La página Experimentos en Configuración" lightbox="../media/experiments-devtools.msft.png":::
       La **página Experimentos** en **Configuración**  
    :::image-end:::  
    
1.  En la **página Experimentos,** desplácese por la lista de todas las características experimentales disponibles y elija la casilla junto a cada característica que desee probar.  
1.  Cierre y vuelva a abrir Microsoft Edge DevTools.  
    
> [!NOTE]
> Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.  Para desactivar una característica experimental, abra la página **Experimentos** y desactive la casilla de la característica experimental que desea desactivar.  

## <a name="highlighted-experimental-features"></a>Características experimentales resaltadas  

En las secciones siguientes se describen las nuevas características experimentales que están disponibles en Microsoft Edge.  

| Característica experimental | Versión de Microsoft Edge |  
|:--- |:--- |  
| [Habilitar webhint](#enable-webhint) | 85 o posterior |  
| [Habilitar consola de red](#enable-network-console) | 85 o posterior |  
| [Visor de pedidos de origen](#source-order-viewer) | 86 o posterior |  
| [Habilitar el editor de métodos abreviados de teclado](#enable-keyboard-shortcut-editor) | 87 o posterior |  
| [Habilitar capas compuestas en la vista 3D](#enable-composited-layers-in-3d-view) | 87 o posterior |  
| [Habilitar la nueva herramienta Editor de fuentes en el panel Estilos](#enable-new-font-editor-tool-within-the-styles-pane) | 89 o posterior |  
| [Habilitar nuevas características de depuración de CSS Flexbox](#enable-new-css-flexbox-debugging-features) | 89 o posterior |  
| [Habilitar menús de pestañas + botón para abrir más herramientas](#enable--button-tab-menus-to-open-more-tools) | 89 o posterior |  
| [Pestaña Habilitar bienvenida](#enable-welcome-tool) | 89 o posterior |  

### <a name="enable-new-css-grid-debugging-features"></a>Habilitar nuevas características de depuración de cuadrícula CSS  

Esta característica experimental proporciona una serie de visualizaciones nuevas que le ayudarán a depurar diseños de cuadrícula CSS.  Para obtener una vista previa de las características experimentales más recientes, [habilite este experimento](#turn-on-experimental-features) y vuelva a cargar DevTools.  Este experimento está en la versión 87 o posterior de Microsoft Edge de forma predeterminada.  

#### <a name="viewing-on-hover-grid-overlays-with-the-inspect-tool"></a>Visualización de superposiciones de cuadrícula activa con la herramienta Inspeccionar  

La **herramienta Inspeccionar** proporciona una forma rápida de identificar y visualizar diseños de cuadrícula CSS en un sitio web al pasar el puntero sobre ellos con el mouse.  Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.  A continuación, mantenga el `Grid` mouse en un elemento de la página web que está depurando.  Los contornos se muestran alrededor de la cuadrícula y el sombreado indica la ubicación de los espacios de cuadrícula si están presentes.  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Visualización de cuadrículas con la herramienta Inspeccionar" lightbox="../media/grid-inspect.msft.png":::
   Visualización de cuadrículas con la **herramienta Inspeccionar**  
:::image-end:::  

#### <a name="viewing-persistent-grid-overlays"></a>Visualización de superposiciones de cuadrícula persistentes  

En Microsoft Edge versión 86 o posterior, la característica de cuadrícula CSS experimental también ofrece la opción de habilitar las superposiciones de cuadrícula persistentes.  Las superposiciones persistentes proporcionan varias ventajas.  

*   Las superposiciones persistentes permanecen visibles en la página a medida que se desplaza, mueve el mouse y usa otras características de DevTools.  
*   Varias superposiciones persistentes pueden estar activadas al mismo tiempo, lo que te permite revisar varios diseños de cuadrícula a la vez.  
*   Las superposiciones persistentes ofrecen muchas opciones de configuración, como ocultar o mostrar nombres en el área de cuadrícula, espacios de cuadrícula, tamaños de pista, y así sucesivamente.  
    
Las dos formas de alternar una superposición de cuadrícula persistente.  

*   Elija el **icono** óvalo Cuadrícula junto a cualquier elemento Grid que se muestra en el árbol DOM de la **herramienta** Elementos.  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Icono ovalado de cuadrícula en la herramienta Elementos" lightbox="../media/grid-adorner.msft.png":::
       Icono ovalado de cuadrícula en **la herramienta** Elementos  
    :::image-end:::  
    
*   Abra el nuevo panel **Diseño** ubicado en la herramienta Elementos y seleccione la casilla situada junto a cada elemento Grid que desee resaltar.  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Panel Diseño en DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       **Panel Diseño** en DevTools  
    :::image-end:::  
    
#### <a name="configuring-persistent-overlays"></a>Configuración de superposiciones persistentes  

En Microsoft Edge versión 86 o posterior, el **nuevo** panel Diseño se encuentra en la herramienta **Elementos** junto con los paneles **Estilos** **y Calculados.**  El panel **Diseño** muestra las opciones de configuración de las superposiciones persistentes.  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Característica de depuración de cuadrícula CSS" lightbox="../media/experiments-grid.msft.png":::
   Característica de depuración de cuadrícula CSS  
:::image-end:::  

### <a name="enable-support-to-move-tabs-between-panels"></a>Habilitar la compatibilidad para mover pestañas entre paneles  

Normalmente, herramientas como **** Elementos **y** Red solo se pueden abrir en el panel principal que se encuentra en la parte superior de DevTools.  Herramientas como **vista 3D** y problemas que normalmente solo se abren en el panel **** **DevTools** que se encuentra en la parte inferior.  Después de elegir el experimento, puede mover herramientas entre los paneles superior e inferior.  Para mover una herramienta, mantenga el mouse en la pestaña, abra el menú contextual \(hacer clic con el botón secundario\) y elija Mover a la parte superior **o** Mover a la **parte inferior**.   Este experimento le permite personalizar el diseño de DevTools.  Para mostrar u ocultar el panel **De cajón,** seleccione `Escape` .  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Mover herramientas entre paneles" lightbox="../media/experiments-move-panels.msft.png":::
   Mover herramientas entre paneles  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-webhint"></a>Habilitar webhint  

[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real para sitios web y páginas web locales.  El tipo de comentarios proporcionados [por webhint][WebhintMain].  

*   accesibilidad  
*   compatibilidad entre exploradores  
*   seguridad  
*   rendimiento  
*   Aplicaciones web progresivas (PWA)  
*   otros problemas comunes de desarrollo web  
    
El [experimento webhint][WebhintMain] muestra los comentarios de webhint en el panel [Problemas.][DevtoolsIssues]  Elija un problema para mostrar la documentación de la solución y una lista de los recursos afectados en su sitio web.  Elija un vínculo de recurso para abrir el panel **Network**, **Sources**o **Elements** relevante en DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   comentarios de webhint en el panel **Problemas**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="enable-network-console"></a>Habilitar consola de red  

**Consola de** red es el título de trabajo de un experimento para realizar solicitudes de red sintéticas a través de HTTP.  Puede usar el experimento **consola de** red para enviar solicitudes de API web.  

Después de activar el experimento, asegúrese de reiniciar DevTools.  Para usar la **consola de red,** siga estos pasos.  

1.  Abra el **panel** Red.  
1.  Busque la solicitud de red que desea cambiar y reenviar.  
1.  Abra el menú contextual \(right-click\) y elija **Editar y reproducir**.  
1.  Cuando se **abra la consola de** red, edite la información de solicitud de red.  
1.  Elija **Enviar**.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Consola de red en el cajón de la consola" lightbox="../media/network-network-console.msft.png":::
   **Consola de red** en el **cajón de la** consola  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### <a name="source-order-viewer"></a>Visor de pedidos de origen  

**El Visor de pedidos de** origen es un experimento que muestra el orden de los elementos en el origen de la página web.  El orden de visualización en pantalla puede diferir del orden del origen, lo que confunde el lector de pantalla y los usuarios de teclado.  Use el **experimento Visor de pedidos de** origen para encontrar las diferencias entre el orden de visualización en pantalla y el orden del origen.  

Después de activar el experimento, asegúrese de reiniciar DevTools.  Para usar **el Visor de pedidos de origen,** siga estos pasos.  

1.  Abra la **herramienta** Elementos.  
1.  Abra el **panel Accesibilidad** en el panel \(bottom\) del cajón.  
1.  En la **sección Visor de pedidos de** origen, elija la casilla Mostrar orden **de** origen.  
1.  Resalte cualquier elemento HTML para mostrar una superposición que el orden en el origen de la página web.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visor de pedidos de origen en el panel Accesibilidad" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Visor de pedidos de origen** en el panel **Accesibilidad**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### <a name="enable-keyboard-shortcut-editor"></a>Habilitar el editor de métodos abreviados de teclado

Con el **experimento Habilitar editor de métodos** abreviados de teclado activado, puedes personalizar los métodos abreviados de teclado para cualquier acción en DevTools.  Para personalizar el método abreviado de teclado de una acción específica, siga estos pasos.  

1.  [Abra DevTools][DevtoolsOpenMain].  
1.  Abra [Configuración][DevToolsCustomizeIndexSettings].  
    *   Seleccione `Shift` + `?` .  
1.  Vaya a la **página Accesos directos.**  
1.  Elija la acción que desea personalizar.  
1.  Elija el **icono Editar** \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Elija la acción que desea personalizar en la página Accesos directos de Configuración" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Elija la acción que desea personalizar en la página **Accesos directos** de [Configuración][DevToolsCustomizeIndexSettings]  
    :::image-end:::  
    
1.  En el teclado, seleccione las teclas que se enlazarán a la acción.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Elija las claves que desea asignar a la acción" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Elija las claves que desea asignar a la acción  
    :::image-end:::  
    
1.  Para guardar el nuevo método abreviado de teclado, elija la marca de verificación \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)\) icono.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado  
    :::image-end:::  
    
1.  Seleccione el nuevo método abreviado de teclado para desencadenar la acción en DevTools.  
    
En la **página Accesos directos,** el icono **Método** abreviado de teclado personalizado \( ![ CustomKeyboardShortcut \) muestra los ](../media/custom-keyboard-shortcut-icon.msft.png) métodos abreviados de teclado personalizados.  Para restablecer todos los accesos directos, elija **Restaurar métodos abreviados predeterminados.**  

Para descartar los cambios mientras edita los métodos abreviados de teclado para una acción, elija el icono X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).  Para quitar accesos directos para una acción específica, elija el icono Eliminar **acceso directo** \( ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).  Para agregar varios métodos abreviados para una acción, elija **Agregar un acceso directo.**  

> [!NOTE]
> Si un método abreviado de teclado está asignado actualmente a otra acción, es posible que no lo guarde para una nueva acción.  Primero debe eliminar el método abreviado de teclado de la acción anterior y, a continuación, agregarlo a la nueva acción.  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-composited-layers-in-3d-view"></a>Habilitar capas compuestas en la vista 3D  

Ahora puede visualizar capas junto con índices z y el modelo de objetos de documento \(DOM\).  Esta característica le ayuda a depurar sin cambiar de contexto con tanta frecuencia.  Identificó que la reducción del cambio de contexto era un punto de dolor importante.  No siempre está claro cómo el código que escribe afecta a la aplicación web.  Para obtener una experiencia de depuración visual completa, ahora se combinan la vista 3D y las Capas compuestas.  

Después de activar el experimento, asegúrese de reiniciar DevTools.  Para usar **capas compuestas,** siga estos pasos.  

1.  En el cajón, elija la **herramienta Vista 3D.**  
1.  Abra el **panel Capas compuestas.**  
1.  Se muestran todas las capas pintadas de la aplicación.  Pruebe esta característica con sus propias aplicaciones web.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   Panel **Capas compuestas**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### <a name="enable-new-font-editor-tool-within-the-styles-pane"></a>Habilitar la nueva herramienta Editor de fuentes en el panel Estilos  

Ahora puede usar el nuevo Editor de [fuentes][DevtoolsInspectStylesEditFonts] visual para editar fuentes.  Úselo para definir fuentes y características de fuente.  El Editor **de fuentes visual** le ayuda a completar las siguientes acciones.  

*   Cambiar entre unidades para distintas propiedades de fuente  
*   Cambiar entre palabras clave para distintas propiedades de fuente  
*   Convertir unidades  
*   Generar código CSS preciso  
    
Después de activar el experimento, asegúrese de reiniciar DevTools.  Para usar el nuevo Editor de **fuentes visuales,** siga estos pasos.  

1.  Abra la **herramienta** Elementos.  
1.  Abra el **panel Estilos.**  
1.  Elija el **icono Editor de** fuentes.  
    
Para obtener más información sobre el nuevo **Editor**de fuentes visual, vaya a Editar estilos y configuraciones de fuentes CSS en el panel Estilos [en DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="Se resalta el panel Editor de fuentes visuales" lightbox="../media/font-editor-open.msft.png":::
   Se resalta **el panel Editor de** fuentes visuales  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-new-css-flexbox-debugging-features"></a>Habilitar nuevas características de depuración de CSS Flexbox  

Esta característica experimental proporciona muchas visualizaciones nuevas que le ayudarán a depurar diseños de CSS Flexbox.  Para obtener una vista previa de las características experimentales más recientes, [activa este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.  

#### <a name="display-persistent-overlays-on-flexbox-layouts-with-the-inspect-tool"></a>Mostrar superposiciones persistentes en diseños de Flexbox con la herramienta Inspeccionar  

La **herramienta Inspeccionar** proporciona una forma rápida de identificar y visualizar diseños de CSS Flexbox en un sitio web activando el mouse sobre ellos.  Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.  A continuación, mientras depura el sitio web, mantenga el mouse en un contenedor flexible para mostrar los contornos alrededor del contenedor flexible.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Mostrar contenedores de Flexbox con la herramienta Inspeccionar" lightbox="../media/flexbox-hover.msft.png":::
   Mostrar contenedores de Flexbox con **la herramienta Inspeccionar**  
:::image-end:::  

#### <a name="display-persistent-overlays-on-flexbox-layouts"></a>Mostrar superposiciones persistentes en diseños de Flexbox  

En Microsoft Edge versión 89 o posterior, la característica experimental CSS Flexbox también ofrece la opción de activar superposiciones persistentes en diseños de Flexbox.  Las superposiciones persistentes proporcionan las siguientes ventajas.  

*   Las superposiciones persistentes permanecen visibles en la página web a medida que se desplaza, mueve el mouse y usa otras características de DevTools.
*   Se pueden usar varias superposiciones persistentes al mismo tiempo, para permitirle revisar varios diseños de Flexbox a la vez.  
*   Las superposiciones persistentes ofrecen opciones de configuración de color.  
    
Para alternar las superposiciones persistentes en el diseño de Flexbox, use una de las siguientes acciones.  

*   Elija el **icono oval de Flexbox** junto a cualquier contenedor de Flexbox que se muestre en el árbol DOM de la **herramienta** Elementos.  
*   Abra el nuevo panel **Diseño** ubicado en la **herramienta Elementos** y seleccione la casilla situada junto a cada contenedor de Flexbox que desee resaltar.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Iconos de Flex y panel Diseño en DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Iconos de Flex y panel **Diseño** en DevTools  
:::image-end:::  

#### <a name="configure-persistent-overlays"></a>Configurar superposiciones persistentes  

Para configurar opciones para superposiciones persistentes para cuadrículas CSS o diseños de Flexbox, use el **panel** Diseño.  El **panel** Diseño se encuentra en la **herramienta Elementos** junto a los paneles **Estilos** **y** Calculados.  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panel Diseño" lightbox="../media/flexbox-layout.msft.png":::
   Panel Diseño  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable--button-tab-menus-to-open-more-tools"></a>Habilitar menús de pestañas + botón para abrir más herramientas  

Ahora puede abrir más herramientas con el nuevo icono **Más herramientas** \( `+` \).  Después de activar los menús de la pestaña Habilitar + botón para abrir más herramientas experimentar y volver a cargar DevTools, se muestra un signo más \( \) a la derecha del grupo de **pestañas** en la parte superior `+` de DevTools.  Para mostrar una lista de otras herramientas que puede agregar a la barra de pestañas, elija el nuevo icono **Más** herramientas \( `+` \).  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Más herramientas en el panel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Más herramientas** en el panel superior
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### <a name="enable-welcome-tool"></a>Habilitar herramienta de bienvenida

Este experimento reemplaza la herramienta **Novedades** por la nueva **herramienta De** bienvenida.  Muestra un diseño actualizado para el siguiente contenido.  

*   Vínculos a documentos para desarrolladores  
*   las características más recientes  
*   notas de la versión  
*   Opción para ponerse en contacto con el equipo de Microsoft Edge DevTools  
    
La **herramienta De** bienvenida se abre automáticamente después de cada actualización de Microsoft Edge.  Para evitar que se muestre la herramienta **de** bienvenida después de cada actualización, desactive la casilla situada junto a la pestaña Abrir después de cada **actualización** en el **título de** la herramienta de bienvenida.  

Si prefiere la herramienta **novedades** original, [][DevtoolsCustomizeIndexSettings]vaya a Experimentos de configuración y quite la casilla situada junto a  >  **** La pestaña Habilitar **bienvenida**.  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Herramienta de bienvenida" lightbox="../media/experiments-welcome.msft.png":::
   **Herramienta de** bienvenida  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## <a name="previous-experimental-features"></a>Características experimentales anteriores  

*   [La vista 3D][Devtools3dViewIndex] ya está disponible y activada de forma predeterminada en Microsoft Edge versión 83 o posterior.  
*   [Activar la compatibilidad para mover pestañas][DevtoolsMoveTabs] entre paneles ya está disponible y activada de forma predeterminada en Microsoft Edge versión 85 o posterior.  
*   [Personalizar métodos abreviados de][DevtoolsCustomKeyboardShortcuts] teclado ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 86 o posterior.  
*   [Emulación: el modo de pantalla dual ya][DevtoolsDeviceModeDualScreenAndFoldables] está disponible y activado de forma predeterminada en Microsoft Edge versión 89 o posterior.  
*   [Activar nuevas características de depuración de][DevtoolsCssGrid] cuadrícula CSS ahora está disponible y activada de forma predeterminada en Microsoft Edge versión 89 o posterior.  
    
## <a name="providing-feedback-on-experimental-features"></a>Proporcionar comentarios sobre características experimentales  

Para proporcionar comentarios sobre los experimentos de Microsoft Edge DevTools o cualquier otra cosa relacionada con DevTools.  

*   Enviar sus comentarios con el icono **Enviar comentarios** en DevTools  
*   Tweet en [@EdgeDevTools][TwitterEdgedevtools]  
    
:::image type="complex" source="../media/bing-devtools-send-feedback.msft.png" alt-text="El icono Enviar comentarios en Microsoft Edge DevTools" lightbox="../media/bing-devtools-send-feedback.msft.png":::
   El **icono Enviar comentarios** en Microsoft Edge DevTools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  
-->  

<!-- links -->  

[Devtools3dViewIndex]: ../3d-view/index.md "Vista 3D | Microsoft Docs"  
[DevtoolsCssGrid]: ../css/grid.md "Inspeccionar CSS Grid en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsMoveTabs]: ../customize/index.md "Personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Editar estilos y configuraciones de fuentes CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personalización de métodos abreviados de teclado en las herramientas de desarrollo de Microsoft Edge | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abra Microsoft Edge DevTools | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias web de pantalla doble | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el emulador de Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la costura: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de pantalla de medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Escritorio remoto | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Galaxy Fold | Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
