---
description: Las últimas características experimentales de Microsoft Edge DevTools
title: Características experimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, experiment
ms.openlocfilehash: 32eaa3e8d41efefa669142297891e7c62cf4eb5b
ms.sourcegitcommit: d53421b7219ad87fa9d58f601d9c61ee44c2e43a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313468"
---
# Características experimentales  

Las DevTools de Microsoft Edge proporcionan acceso a características experimentales que aún están en desarrollo.  Puedes probar y [proporcionar comentarios antes de](#providing-feedback-on-experimental-features) que se lanza cada característica.  

Aunque las características experimentales están disponibles en todos los canales de Microsoft Edge, puede obtener las últimas características experimentales con el canal Canary de Microsoft Edge.  

## Activar características experimentales  

Para activar \(o desactivar\) las características experimentales en Microsoft Edge, sigue estos pasos.  

1.  [Abra DevTools][DevtoolsOpenMain].  
    *   Selecciona `Control` + `Shift` + `I` \(Windows, Linux\) o `Command` + `Option` + `I` \(macOS\).  Para obtener más información, vaya a [los métodos abreviados de teclado de DevTools de Microsoft Edge.][DevToolsShortcuts]  
1.  Abra el [panel][DevToolsCustomizeIndexSettings] Configuración.  
    *   Seleccione `Shift` + `?` .  Para obtener más información, vaya a [los métodos abreviados de teclado de DevTools de Microsoft Edge.][DevToolsShortcuts]  
1.  En el lado izquierdo del **panel** Configuración, elija la **sección** Experimentos.  
    
    :::image type="complex" source="../media/experiments-devtools.msft.png" alt-text="La página Experimentos en Configuración" lightbox="../media/experiments-devtools.msft.png":::
       La **página Experimentos** en **Configuración**  
    :::image-end:::  
    
1.  En la **página Experimentos, desplázate** por la lista de todas las características experimentales disponibles y elige la casilla junto a cada característica que quieras probar.  
1.  Cierre y vuelva a abrir Microsoft Edge DevTools.  
    
> [!NOTE]
> Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.  Para desactivar una característica experimental, abre la página **Experimentos** y desactiva la casilla de la característica experimental que quieres desactivar.  

## Características experimentales resaltadas  

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
| [Habilitar los menús de la pestaña + botón para abrir más herramientas](#enable--button-tab-menus-to-open-more-tools) | 89 o posterior |  
| [Habilitar la pestaña de bienvenida](#enable-welcome-tool) | 89 o posterior |  

### Habilitar nuevas características de depuración de cuadrícula CSS  

Esta característica experimental proporciona una serie de visualizaciones nuevas que te ayudarán a depurar diseños de cuadrícula CSS.  Para obtener una vista previa de las características experimentales más recientes, [habilita este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.  Este experimento está en modo predeterminado en Microsoft Edge versión 87 o posterior.  

#### Visualización de superposiciones de cuadrícula activa con la herramienta Inspeccionar  

La **herramienta Inspect** proporciona una forma rápida de identificar y visualizar diseños de cuadrícula CSS en un sitio web al pasar el puntero sobre ellos con el mouse.  Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.  A continuación, mantenga el mouse sobre un elemento Grid en el sitio web que está depurando.  Los contornos se muestran alrededor de la cuadrícula y el sombreado indica la ubicación de las separaciones de cuadrícula si están presentes.  

:::image type="complex" source="../media/grid-inspect.msft.png" alt-text="Visualización de cuadrículas con la herramienta Inspeccionar" lightbox="../media/grid-inspect.msft.png":::
   Visualización de cuadrículas con la **herramienta Inspeccionar**  
:::image-end:::  

#### Visualización de superposiciones de cuadrícula persistentes  

En Microsoft Edge versión 86 o posterior, la característica experimental de cuadrícula CSS también ofrece la opción de habilitar las superposiciones de cuadrícula persistentes.  Las superposiciones persistentes proporcionan varias ventajas.  

*   Las superposiciones persistentes permanecen visibles en la página mientras se desplaza, mueve el mouse y usa otras características de DevTools.  
*   Se pueden habilitar varias superposiciones persistentes al mismo tiempo, lo que te permite revisar varios diseños de cuadrícula a la vez.  
*   Las superposiciones persistentes ofrecen muchas opciones de configuración, como ocultar o mostrar nombres en el área de cuadrícula, intervalos de cuadrícula, tamaños de pista, entre otros.  
    
Las dos formas de alternar una superposición de cuadrícula persistente.  

*   Elige el **icono de** óvalo De cuadrícula junto a cualquier elemento Grid que se muestra en el árbol DOM de la **herramienta** Elementos.  
    
    :::image type="complex" source="../media/grid-adorner.msft.png" alt-text="Icono de óvalo de cuadrícula en la herramienta Elementos" lightbox="../media/grid-adorner.msft.png":::
       Icono de óvalo de cuadrícula en **la herramienta** Elementos  
    :::image-end:::  
    
*   Abre el nuevo panel **Diseño** ubicado en la herramienta Elementos y elige la casilla junto a cada elemento grid que quieras resaltar.  
    
    :::image type="complex" source="../media/grid-layout-zoom.msft.png" alt-text="Panel de diseño en DevTools" lightbox="../media/grid-layout-zoom.msft.png":::
       Panel **de** diseño en DevTools  
    :::image-end:::  
    
#### Configuración de superposiciones persistentes  

En Microsoft Edge versión 86 o posterior, el **** **nuevo** panel **** Diseño se encuentra en la herramienta Elementos junto con las pestañas **Estilos** y Calculados.  El panel **Diseño** muestra las opciones de configuración de las superposiciones persistentes.  

:::image type="complex" source="../media/experiments-grid.msft.png" alt-text="Característica de depuración de cuadrícula CSS" lightbox="../media/experiments-grid.msft.png":::
   Característica de depuración de cuadrícula CSS  
:::image-end:::  

### Habilitar la compatibilidad para mover fichas entre paneles  

Normalmente, herramientas como **Elementos** y **Red** solo se pueden abrir en el panel principal que se encuentra en la parte superior de Las DevTools.  Herramientas como **vista 3D** y **problemas** que normalmente solo se abren en el **panel** de cajón que se encuentra en la parte inferior de DevTools.  Después de elegir el experimento, puedes mover herramientas entre los paneles superior e inferior.  Para mover una herramienta, mantenga el mouse sobre la pestaña, abra **** el menú contextual \(haga clic con el botón secundario\) y elija Mover a la parte superior o **Mover a la parte inferior.**   Este experimento te permite personalizar el diseño de DevTools.  Para mostrar u ocultar el panel **Del cajón,** seleccione `Escape` .  

:::image type="complex" source="../media/experiments-move-panels.msft.png" alt-text="Mover fichas entre paneles" lightbox="../media/experiments-move-panels.msft.png":::
   Mover fichas entre paneles  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar webhint  

[webhint es][WebhintMain] una herramienta de código abierto que proporciona comentarios en tiempo real para sitios web y páginas web locales.  El tipo de comentarios proporcionados por [webhint][WebhintMain].  

*   accesibilidad  
*   compatibilidad entre exploradores  
*   seguridad  
*   rendimiento  
*   Aplicaciones web progresivas (PDA)  
*   otros problemas comunes de desarrollo web  
    
El [experimento de webhint][WebhintMain] muestra los comentarios de webhint en el panel [Problemas.][DevtoolsIssues]  Elija un problema para mostrar la documentación de la solución y una lista de los recursos afectados en su sitio web.  Elige un vínculo de recurso para abrir el panel **Red,** **Orígenes**o **Elementos** relevante en DevTools.  

:::image type="complex" source="../media/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../media/experiments-webhint.msft.png":::
   comentarios de webhint en el panel **Problemas**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Habilitar consola de red  

**Consola de** red es el título de trabajo de un experimento para realizar solicitudes de red sintéticas a través de HTTP.  Puedes usar el experimento **de consola de** red para enviar solicitudes de API web.  

Después de activar el experimento, asegúrate de reiniciar DevTools.  Para usar la **Consola de red,** siga estos pasos.  

1.  Abra el **panel** Red.  
1.  Busque la solicitud de red que desea cambiar y volver a enviar.  
1.  Abra el menú contextual \(right-click\) y elija **Editar y reproducir.**  
1.  Cuando se **abra la consola de** red, edite la información de solicitud de red.  
1.  Elija **Enviar**.  
    
:::image type="complex" source="../media/network-network-console.msft.png" alt-text="Consola de red en el cajón de la consola" lightbox="../media/network-network-console.msft.png":::
   **Consola de red** en el **cajón de la** consola  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Visor de pedidos de origen  

**El Visor de orden de** origen es un experimento que muestra el orden de los elementos en el origen de la página web.  El orden de visualización en pantalla puede diferir del orden del origen, lo que confunde a los usuarios de lector de pantalla y teclado.  Usa el **experimento Visor de pedidos de** origen para encontrar las diferencias entre el orden de visualización en pantalla y el orden del origen.  

Después de activar el experimento, asegúrate de reiniciar DevTools.  Para usar el **Visor de pedidos de origen,** siga estos pasos.  

1.  Abra la **herramienta** Elementos.  
1.  Abra el **panel Accesibilidad** en el panel del cajón \(inferior\).  
1.  En la **sección Visor de pedidos de** origen, seleccione la casilla Mostrar pedido **de** origen.  
1.  Resalte cualquier elemento HTML para mostrar una superposición según el orden en el origen de la página web.  
    
:::image type="complex" source="../media/experiments-source-order-viewer.msft.png" alt-text="Visor de pedidos de origen en el panel Accesibilidad" lightbox="../media/experiments-source-order-viewer.msft.png":::
   **Visor de pedidos de origen** en el panel **Accesibilidad**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

### Habilitar el editor de métodos abreviados de teclado

Con el **experimento Habilitar el editor de** métodos abreviados de teclado activado, puedes personalizar los métodos abreviados de teclado para cualquier acción en DevTools.  Para personalizar el método abreviado de teclado para una acción específica, siga estos pasos.  

1.  [Abra DevTools][DevtoolsOpenMain].  
1.  Abra [Configuración.][DevToolsCustomizeIndexSettings]  
    *   Seleccione `Shift` + `?` .  
1.  Vaya a la **página Accesos directos.**  
1.  Elija la acción que desea personalizar.  
1.  Elija el **icono** Editar \( ![ EditKeyboardShortcut ](../media/edit-keyboard-shortcut-icon.msft.png) \).  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png" alt-text="Elija la acción que desea personalizar en la página Accesos directos en Configuración" lightbox="../media/experiments-custom-keyboard-shortcuts-select-action.msft.png":::
       Elija la acción que desea personalizar en la página **Accesos directos** en [Configuración][DevToolsCustomizeIndexSettings]  
    :::image-end:::  
    
1.  En el teclado, selecciona las teclas para enlazar a la acción.  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png" alt-text="Seleccionar las claves para asignar a la acción" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Seleccionar las claves para asignar a la acción  
    :::image-end:::  
    
1.  Para guardar el nuevo método abreviado de teclado, elija la marca de verificación \(![CheckmarkKeyboardShortcut](../media/checkmark-keyboard-shortcut-icon.msft.png)Icono \).  
    
    :::image type="complex" source="../media/experiments-custom-keyboard-shortcuts-save-shortcut.msft.png" alt-text="Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado" lightbox="../media/experiments-custom-keyboard-shortcuts-enter-key.msft.png":::
       Elija el icono de marca de verificación para guardar el nuevo método abreviado de teclado  
    :::image-end:::  
    
1.  Selecciona el nuevo método abreviado de teclado para desencadenar la acción en DevTools.  
    
En la **página Accesos directos,** el icono **de** método abreviado de teclado personalizado \( ![ CustomKeyboardShortcut \) muestra los ](../media/custom-keyboard-shortcut-icon.msft.png) métodos abreviados de teclado personalizados.  Para restablecer todos los accesos directos, elija **Restaurar accesos directos predeterminados.**  

Para descartar los cambios mientras edita los métodos abreviados de teclado para una acción, elija el icono X \( ![ XKeyboardShortcut ](../media/discard-changes-keyboard-shortcut-icon.msft.png) \).  Para quitar accesos directos de una acción específica, elija el icono Eliminar acceso directo **\(** ![ DeleteKeyboardShortcut ](../media/delete-keyboard-shortcut-icon.msft.png) \).  Para agregar varios accesos directos para una acción, elija **Agregar un acceso directo.**  

> [!NOTE]
> Si un método abreviado de teclado está asignado actualmente a otra acción, es posible que no lo guarde para una nueva acción.  Primero debe eliminar el método abreviado de teclado de la acción anterior y, a continuación, agregarlo a la nueva acción.  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Habilitar capas compuestas en la vista 3D  

Ahora puede visualizar capas junto a índices z y el modelo de objetos de documento \(DOM\).  Esta característica le ayuda a depurar sin cambiar de contexto con tanta frecuencia.  Identificaste que la reducción del cambio de contexto era un punto difícil.  No siempre está claro cómo afecta el código que escribe a la aplicación web.  Para obtener una experiencia de depuración visual completa, ahora se combinan la vista 3D y las Capas compuestas.  

Después de activar el experimento, asegúrate de reiniciar DevTools.  Para usar **capas compuestas,** siga estos pasos.  

1.  En el cajón, elija la **herramienta Vista 3D.**  
1.  Abra el **panel Capas compuestas.**  
1.  Se muestran todas las capas pintadas de la aplicación.  Pruebe esta característica con sus propias aplicaciones web.  
    
:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../media/experiments-layers.msft.png":::
   Panel **Capas compuestas**  
:::image-end:::  

<!--Available in Microsoft Edge version 87 and later.  -->  

### Habilitar la nueva herramienta Editor de fuentes en el panel Estilos  

Ahora puede usar el nuevo Editor de [fuentes][DevtoolsInspectStylesEditFonts] visual para editar fuentes.  Úselo para definir fuentes y características de fuente.  El Editor **de fuentes visual** le ayuda a completar las siguientes acciones.  

*   Cambiar entre unidades para distintas propiedades de fuente  
*   Cambiar entre palabras clave para distintas propiedades de fuente  
*   Convertir unidades  
*   Generar código CSS preciso  
    
Después de activar el experimento, asegúrate de reiniciar DevTools.  Para usar el nuevo Editor de **fuentes visual,** siga estos pasos.  

1.  Abra la **herramienta** Elementos.  
1.  Abra el **panel Estilos.**  
1.  Elija el icono **del Editor de** fuentes.  
    
Para obtener más información acerca del nuevo **Editor**de fuentes visual, vaya a Editar estilos y configuraciones de fuente CSS en el panel Estilos [de DevTools][DevtoolsInspectStylesEditFonts].  

:::image type="complex" source="../media/font-editor-open.msft.png" alt-text="El panel Editor de fuentes visual está resaltado" lightbox="../media/font-editor-open.msft.png":::
   El panel **Editor de fuentes** visual está resaltado  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Habilitar nuevas características de depuración de CSS Flexbox  

Esta característica experimental proporciona muchas visualizaciones nuevas que le ayudarán a depurar diseños CSS Flexbox.  Para obtener una vista previa de las características experimentales más recientes, [activa este experimento](#turn-on-experimental-features) y vuelve a cargar DevTools.  

#### Mostrar superposiciones persistentes en diseños de Flexbox con la herramienta Inspeccionar  

La **herramienta Inspect** proporciona una forma rápida de identificar y visualizar diseños CSS Flexbox en un sitio web al mantener el puntero sobre ellos con el mouse.  Elija el **icono Inspeccionar** \( Inspeccionar \) en la esquina superior izquierda ![ de ](../media/inspect-icon.msft.png) DevTools.  A continuación, al depurar el sitio web, mantenga el puntero sobre un contenedor flexible para mostrar esquemas alrededor del contenedor flex.  

:::image type="complex" source="../media/flexbox-hover.msft.png" alt-text="Mostrar contenedores de Flexbox con la herramienta Inspeccionar" lightbox="../media/flexbox-hover.msft.png":::
   Mostrar contenedores de Flexbox con la **herramienta Inspeccionar**  
:::image-end:::  

#### Mostrar superposiciones persistentes en diseños de Flexbox  

En Microsoft Edge versión 89 o posterior, la característica experimental CSS Flexbox también ofrece la opción de activar superposiciones persistentes en diseños de Flexbox.  Las superposiciones persistentes proporcionan las siguientes ventajas.  

*   Las superposiciones persistentes permanecen visibles en la página web mientras se desplaza, mueve el mouse y usa otras características de DevTools.
*   Se pueden usar varias superposiciones persistentes al mismo tiempo, para permitirle revisar varios diseños de Flexbox a la vez.  
*   Las superposiciones persistentes ofrecen opciones de configuración de color.  
    
Para alternar las superposiciones persistentes en el diseño de Flexbox, usa una de las siguientes acciones.  

*   Elija el icono del óvalo de **Flexbox** junto a cualquier contenedor de Flexbox que se muestra en el árbol DOM de la **herramienta** Elementos.  
*   Abre el nuevo panel **diseño** que se encuentra en la herramienta **Elementos** y elige la casilla junto a cada contenedor de Flexbox que quieras resaltar.  
    
:::image type="complex" source="../media/flexbox-overlay.msft.png" alt-text="Iconos flexibles y panel diseño en DevTools" lightbox="../media/flexbox-overlay.msft.png":::
   Iconos flexibles y panel **diseño** en DevTools  
:::image-end:::  

#### Configurar superposiciones persistentes  

Para configurar las opciones de las superposiciones persistentes para cuadrículas CSS o diseños de Flexbox, usa el **panel** Diseño.  El **panel** Diseño se encuentra en la herramienta **Elementos** junto a los paneles **Estilos** **y Calculados.**  

:::image type="complex" source="../media/flexbox-layout.msft.png" alt-text="Panel de diseño" lightbox="../media/flexbox-layout.msft.png":::
   Panel de diseño  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Habilitar los menús de la pestaña + botón para abrir más herramientas  

Ahora puede abrir más herramientas con el nuevo icono **Más herramientas** \( `+` \).  Después de activar los **menús** de la pestaña Habilitar + botón para abrir más herramientas y volver a cargar DevTools, se muestra un signo más \( \) a la derecha del grupo de pestañas en la parte superior de `+` DevTools.  Para mostrar una lista de otras herramientas que puede agregar a la barra de pestañas, elija el nuevo icono **Más** herramientas \( `+` \).  

:::image type="complex" source="../media/experiments-more-tools-button.msft.png" alt-text="Más herramientas en el panel superior" lightbox="../media/experiments-more-tools-button.msft.png":::
   **Más herramientas** en el panel superior
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

### Habilitar herramienta de bienvenida

Este experimento reemplaza la **herramienta Novedades** por la nueva **herramienta de** bienvenida.  Muestra un diseño actualizado para el siguiente contenido.  

*   Vínculos a documentos para desarrolladores  
*   las características más recientes  
*   notas de la versión  
*   Opción para ponerse en contacto con el equipo de DevTools de Microsoft Edge  
    
La **herramienta de** bienvenida se abre automáticamente después de cada actualización de Microsoft Edge.  Para evitar que se muestre la herramienta **de** bienvenida después de cada actualización, desactive la casilla situada junto a la pestaña **Abrir** después de cada actualización bajo el título **de** la herramienta de bienvenida.  

Si prefieres la **herramienta** Novedades original, ve a Experimentos de configuración y quita la casilla junto a [][DevtoolsCustomizeIndexSettings]  >  **** Habilitar **pestaña de bienvenida.**  

:::image type="complex" source="../media/experiments-welcome.msft.png" alt-text="Herramienta de bienvenida" lightbox="../media/experiments-welcome.msft.png":::
   **Herramienta de** bienvenida  
:::image-end:::  

<!--Available in Microsoft Edge version 89 and later.  -->  

## Características experimentales anteriores  

*   [La vista 3D][Devtools3dViewIndex] ahora está disponible y activada de forma predeterminada en Microsoft Edge versión 83 o posterior.  
*   [Activar la compatibilidad para mover fichas][DevtoolsMoveTabs] entre paneles ya está disponible y activado de forma predeterminada en Microsoft Edge versión 85 o posterior.  
*   [Personalizar los métodos abreviados de][DevtoolsCustomKeyboardShortcuts] teclado ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 86 o posterior.  
*   [Emulación: el modo de pantalla dual compatible][DevtoolsDeviceModeDualScreenAndFoldables] ahora está disponible y activado de forma predeterminada en Microsoft Edge versión 89 o posterior.  
*   [Activar las nuevas características de depuración de][DevtoolsCssGrid] cuadrícula CSS ya está disponible y activada de forma predeterminada en Microsoft Edge versión 89 o posterior.  
    
## Proporcionar comentarios sobre las características experimentales  

Para proporcionar comentarios sobre los experimentos de Microsoft Edge DevTools o cualquier otra cosa relacionada con DevTools.  

*   Envía tus comentarios mediante el icono **Enviar** comentarios en DevTools  
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
[DevtoolsCssGrid]: ../css/grid.md "Inspeccionar la cuadrícula CSS en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsMoveTabs]: ../customize/index.md "Personalizar las devTools de Microsoft Edge | Microsoft Docs"  
[DevToolsCustomizeIndexSettings]: ../customize/index.md#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsInspectStylesEditFonts]: ../inspect-styles/edit-fonts.md "Edite la configuración y los estilos de fuente CSS en el panel Estilos de DevTools | Microsoft Docs"  
[DevtoolsIssues]: ../issues/index.md "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsShortcuts]: ../shortcuts/index.md "Métodos abreviados de teclado de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomKeyboardShortcuts]: ../customize/shortcuts.md "Personalizar los métodos abreviados de teclado en las DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsOpenMain]: ../open/index.md "Abra las DevTools de Microsoft Edge | Microsoft Docs"  

[DualScreenWebIndex]: /dual-screen/web/index "Experiencias web de pantalla doble | Microsoft Docs"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtener el emulador de Surface Duo | Microsoft Docs"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la seam: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Característica de pantalla multimedia CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clientes de Escritorio remoto | Microsoft Docs"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../device-mode/dual-screen-and-foldables.md "Emular dispositivos de doble pantalla y plegado en Microsoft Edge DevTools | Microsoft Docs"

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "webhint"  
