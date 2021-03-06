---
description: Usa DevTools en el modo de contraste alto de Windows, coincide con los métodos abreviados de teclado en DevTools para Visual Studio código y mucho más.
title: Novedades de DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 701c328c1dc975a81129049fe2931139757205c3
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398577"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <a name="whats-new-in-devtools-microsoft-edge-84"></a>Novedades de DevTools (Microsoft Edge 84)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Anuncios del equipo de Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede que falte del equipo de Microsoft Edge DevTools.  Echa un vistazo a los anuncios para probar nuevas características en DevTools, microsoft Visual Studio code extensions y mucho más.  Para mantenerse al día de todas las características más recientes y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] y [síganos en Twitter][EdgeDevToolsTwitterAccount].  

### <a name="use-the-devtools-in-windows-high-contrast-mode"></a>Usar DevTools en el modo de contraste alto de Windows

Las DevTools de Microsoft Edge ahora se muestran en modo de contraste alto cuando Windows está en modo de contraste alto.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools en modo de contraste alto" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Microsoft Edge DevTools en modo de contraste alto  
:::image-end:::  

[Siga las instrucciones para activar el modo de contraste alto en Windows][MicrosoftSupportWindows10HighContrastMode].  Para abrir DevTools en Microsoft Edge, seleccione `F12` o `Ctrl` + `Shift` + `I` .  Las DevTools se muestran en modo de contraste alto.  

> [!NOTE]
> Microsoft Edge DevTools admite actualmente el modo de contraste alto en Windows, pero no en macOS.  

Problema de [chromium #1048378][CR1048378]  

### <a name="match-keyboard-shortcuts-in-the-devtools-to-visual-studio-code"></a>Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código  

De [sus](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios y del rastreador de problemas [públicos chromium,][CRIssuesList]el equipo de DevTools de Microsoft Edge aprendió que deseaba la posibilidad de personalizar los métodos abreviados de teclado en DevTools.  En Microsoft Edge 84, ahora puedes hacer coincidir los métodos abreviados de teclado en DevTools [para Visual Studio Code,][VisualStudioCode]que es solo una de las características en las que el equipo está trabajando para personalizar los accesos directos.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio código" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Microsoft Edge DevTools en modo de contraste alto  
:::image-end:::  

Para probar el experimento, abra Configuración de DevTools seleccionando o seleccionando el icono Configuración de DevTools en la esquina superior derecha de `?` ![ ][ImageSettingsIcon] DevTools.  Vaya a la **sección Experimentos y** active la pestaña Habilitar la configuración de métodos abreviados de teclado **personalizados (requiere volver a cargar).**  Ahora vuelve a cargar DevTools, abre Configuración de nuevo y navega a la sección **Accesos directos.**  

Elija **DevTools (Valor predeterminado)** en el menú desplegable Coincidencia **de accesos directos** de la lista desplegable preestablecido y **seleccione Visual Studio Código**.  Los métodos abreviados de teclado de DevTools ahora coinciden con los métodos abreviados para acciones equivalentes en Visual Studio código.  

Por ejemplo, el método abreviado de teclado para pausar o continuar ejecutando un script [en Visual Studio Code][VisualStudioCodeShortcuts] es `F5` .  Con el valor **preestablecido DevTools (predeterminado),** ese mismo acceso directo en DevTools es, pero con el valor preestablecido Visual Studio `F8` **Code,** ese acceso directo ahora también es `F5` .  

La característica está disponible actualmente en Microsoft Edge 84 como un experimento, así que comparta sus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) con el equipo.  

Problema de [chromium #174309][CR174309]  

### <a name="remote-debug-surface-duo-emulators"></a>Emuladores de Surface Duo de depuración remota  

Ahora puedes depurar de forma remota el contenido web que se ejecuta en el emulador [de Surface Duo][DualScreensAndroidEmulator] con toda la potencia de Microsoft Edge [DevTools][DevToolsChromiumGuide].  

Con el [emulador de Surface Duo,][DualScreensAndroidEmulator]puedes probar cómo se representa el contenido web en una nueva clase de dispositivos de pantalla doble y plegables.  El emulador ejecuta el sistema operativo Android y proporciona la [aplicación Android de Microsoft Edge.][AndroidEdge]  Cargue el contenido web en la [aplicación Microsoft Edge][AndroidEdge] y depurelo con Microsoft Edge [DevTools][DevToolsChromiumGuide].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="La aplicación de Microsoft Edge que se ejecuta en el emulador de Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   La aplicación Microsoft Edge en el emulador de Surface Duo  
:::image-end:::  

La página de una instancia de escritorio de Microsoft Edge muestra `edge://inspect` **SurfaceDuoEmulator** [][DesktopEdge] con una lista de las pestañas abiertas o [pwas][PwaIndex] que se ejecutan en el emulador [de Surface Duo][DualScreensAndroidEmulator].  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="La edge://inspect muestra una lista de las pestañas abiertas en la aplicación de Microsoft Edge que se ejecuta en el emulador" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación microsoft edge que se ejecuta en el emulador
:::image-end:::  

Elija **inspeccionar** la pestaña o PWA que desea depurar para abrir [Microsoft Edge DevTools][DevToolsChromiumGuide].  Sigue la guía paso a paso para depurar de forma remota el contenido [web en el emulador de Surface Duo.][DevToolsRemoteDebugDuoEmulator]  

### <a name="resize-the-devtools-drawer-more-easily"></a>Cambiar el tamaño del cajón de DevTools más fácilmente  

En Microsoft Edge 83 o versiones anteriores, solo era posible cambiar el tamaño del cajón [de DevTools][DevToolsDrawer] activando el mouse dentro de la barra de herramientas del cajón.  El drawer se comportó de forma diferente que los demás controles de cambio de tamaño de los paneles de DevTools donde se mantiene el mouse en el borde del panel para cambiar su tamaño.  Elija la siguiente imagen para mostrar cómo funcionaba el tamaño del cajón en la versión 83 o anterior de Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Redimensionar el cajón de DevTools en Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Redimensionar el cajón de DevTools en Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

A partir de Microsoft Edge 84, ahora puedes cambiar el tamaño del cajón activando el mouse sobre el borde del cajón.  Este cambio alinea el comportamiento cambiando el tamaño del cajón de DevTools con la forma en que cambia el tamaño de otros paneles en DevTools.  Elija la siguiente imagen para mostrar el tamaño en acción en Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Redimensionar el cajón de DevTools en Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Redimensionar el cajón de DevTools en Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

Problema de [chromium #1076112][CR1076112]  

### <a name="screencasting-navigation-buttons-display-focus"></a>Foco de visualización de botones de navegación de difusión por pantalla  

Al depurar de forma remota un dispositivo [Android,][DevToolsRemoteDebugAndroid]un dispositivo [Windows 10][DevToolsRemoteDebugWindows]o un emulador de [Surface Duo,][DevToolsRemoteDebugDuoEmulator]puedes alternar la difusión por pantalla con el icono Alternar difusión en pantalla en la esquina superior izquierda de ![ ][ImageScreencastingIcon] DevTools.  Con la difusión por pantalla habilitada, puedes navegar por la pestaña de Microsoft Edge en el dispositivo remoto desde la ventana DevTools.  En Microsoft Edge 84, estos botones de navegación ahora también son accesibles con el teclado.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Seleccionar Mayús+Tab en la barra url proyectada en pantalla muestra el foco en el botón Actualizar" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   Select `Shift` + `Tab` from the screencasted URL bar shows focus on the **Refresh** button
:::image-end:::  

Problema de [chromium #1081486][CR1081486]  

### <a name="network-panel-details-pane-is-now-accessible"></a>Panel de red Panel Detalles panel ahora es accesible  

En Microsoft Edge 84, el **** panel Detalles de la herramienta Red ahora se centra cuando se abre para un recurso en el registro [de red][DevToolsNetworkLog]. [][DevToolsNetworkDetails]  Este cambio permite a los lectores de pantalla leer e interactuar con el contenido del **panel** Detalles.  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="El panel Detalles del panel Red se centra cuando se abre" lightbox="../../media/2020/05/network-details.msft.png":::
   El **panel Detalles** de la herramienta **Red** se centra cuando se abre
:::image-end:::  

Problema de [chromium #963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

En las secciones siguientes se anuncian características adicionales disponibles en Microsoft Edge 84 que se contribuyeron al proyecto chromium de código abierto.  

### <a name="fix-site-issues-with-the-new-issues-tool-in-the-devtools-drawer"></a>Corregir problemas del sitio con la nueva herramienta Problemas en el cajón de DevTools

La nueva **herramienta Problemas** del cajón DevTools se creó para ayudar a reducir la fatiga y el desorden de notificaciones de la **consola.**  Actualmente, la **consola es** el lugar central para que desarrolladores de sitios web, bibliotecas, marcos y Microsoft Edge registren mensajes, advertencias y errores.  La **herramienta Problemas** agrega advertencias desde el explorador de una forma estructurada, agregada y que puede actuar, vínculos a recursos afectados dentro de Microsoft Edge DevTools y proporciona instrucciones sobre cómo solucionar los problemas.  Con el tiempo, cada vez hay más advertencias en Microsoft Edge en la herramienta Problemas en lugar de en la consola **,** lo que debería ayudar a reducir el desorden en la **** **consola**.  

Para empezar, vaya a [Buscar y corregir problemas con la herramienta Microsoft Edge DevTools Issues][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="La herramienta Problemas en el cajón de DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   La **herramienta Problemas** en el cajón de DevTools  
:::image-end:::  

Problema de [chromium #1068116][CR1068116]  

### <a name="view-accessibility-information-in-the-inspect-mode-tooltip"></a>Ver información de accesibilidad en la información sobre herramientas del modo de inspección  

La **información sobre** herramientas del modo de inspección ahora indica si el elemento tiene un nombre y un [rol][WebhintHintsAxeNameRoleValue] accesibles y si se puede centrar en [el teclado.][WebhintHintsAxeKeyboard]  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Información sobre herramientas del modo de inspección con información de accesibilidad" lightbox="../../media/2020/05/a11y.msft.png":::
  Información **sobre herramientas del modo de** inspección con información de accesibilidad  
:::image-end:::  

Problema de [chromium #1040025][CR1040025]  

### <a name="performance-panel-updates"></a>Actualizaciones del panel de rendimiento  

#### <a name="view-total-blocking-time-information-in-the-footer"></a>Ver información de tiempo de bloqueo total en el pie de página  

Después de grabar el rendimiento de carga, **el** panel Rendimiento muestra ahora información del tiempo de bloqueo total \(TBT\) en el pie de página.  TBT es una métrica de rendimiento de carga que ayuda a cuantificar el tiempo que tarda una página en usarse.  Básicamente mide cuánto tiempo parece que una página puede usarse \(porque el contenido se representa en la pantalla\); pero en realidad no se puede usar, porque JavaScript bloquea el subproceso principal y, por lo tanto, la página no responde a la entrada del usuario.  TBT es la métrica principal para aproximar el retraso de primera entrada.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Para obtener información sobre el tiempo **** total de bloqueo, no use el flujo de trabajo del icono Actualizar página ![ Actualizar página para registrar el rendimiento de carga de ][ImageRefreshPageIcon] página.  

En su lugar, **seleccione Grabar** icono de registro, vuelva a cargar manualmente la página, espere a que se cargue la página y, a ![ continuación, detenga la ][ImageRecordIcon] grabación.  

Si se muestra, Microsoft Edge DevTools no ha obtiene la información necesaria de los datos de generación de perfiles `Total Blocking Time: Unavailable` internos en Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Información de tiempo de bloqueo total en el pie de página de una grabación del panel Rendimiento" lightbox="../../media/2020/05/tbt.msft.png":::
   Información de tiempo de bloqueo total en el pie de página de una **grabación del** panel Rendimiento  
:::image-end:::  

Problema de [chromium #1054381][CR1054381]  

#### <a name="layout-shift-events-in-the-new-experience-section"></a>Eventos Shift de diseño en la nueva sección Experiencia  

La nueva **sección Experiencia** del panel **Rendimiento** le ayuda a detectar los turnos de diseño.  Cumulative Layout Shift \(CLS\) es una métrica que ayuda a cuantificar la inestabilidad visual no deseada.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Elija el **evento Layout Shift** para mostrar los detalles del turno de diseño en el panel **Resumen.**  Mantenga el mouse en **los campos Movido de** y Movido **a** para visualizar dónde se produjo el cambio de diseño.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Los detalles de un turno de diseño" lightbox="../../media/2020/05/cls.msft.png":::
   Los detalles de un turno de diseño  
:::image-end:::  

### <a name="more-accurate-promise-terminology-in-the-console"></a>Terminología de promesas más precisa en la consola  

Al registrar un `Promise` , el valor **proporcionado** incorrectamente por la consola se establece `PromiseStatus` en `resolved` .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Un ejemplo de la consola mediante la terminología antigua resuelta" lightbox="../../media/2020/05/resolved.msft.png":::
   Un ejemplo de la **consola con** la `resolved` terminología antigua  
:::image-end:::  

La **consola** ahora usa el término `fulfilled` , que se alinea con la `Promise` especificación.  Para obtener más información acerca de `Promise` la especificación, vaya a [Estados y destinos en GitHub](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Un ejemplo de la consola mediante la nueva terminología cumplida" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Un ejemplo de la **consola mediante** la `fulfilled` nueva terminología  
:::image-end:::  

Problema V8 [#6751][CRV86751]  

### <a name="styles-pane-updates"></a>Actualizaciones del panel Estilos  

#### <a name="support-for-the-revert-keyword"></a>Compatibilidad con la palabra clave revert  

La interfaz de usuario de autocompletar del panel **Estilos** ahora detecta la palabra clave [CSS][MDNRevert] revert, que revierte el valor en cascada de una propiedad al valor anterior aplicado al estilo del elemento.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Establecer el valor de una propiedad para revertir" lightbox="../../media/2020/05/revert.msft.png":::
  Establecer el valor de una propiedad para revertir  
:::image-end:::  

Problema de [chromium #1075437][CR1075437]  

#### <a name="image-previews"></a>Vistas previas de imágenes  

Mantenga el mouse sobre un valor en el panel Estilos para mostrar una `background-image` vista previa de la imagen en una información sobre herramientas. ****  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Mantener el mouse sobre un valor de imagen de fondo" lightbox="../../media/2020/05/image-preview.msft.png":::
  Pasar el puntero sobre un `background-image` valor  
:::image-end:::  

Problema de [chromium #1040019][CR1040019]  

#### <a name="color-picker-now-uses-space-separated-functional-color-notation"></a>El Selector de colores ahora usa la notación de color funcional separada por espacios  

[Css Color Module Level 4][CSSWGDraftsColor4Changes3] especifica que las funciones de color, como `rgb()` , deben admitir argumentos separados por espacios.  Por ejemplo, `rgb(0, 0, 0)` equivale a `rbg(0 0 0)`.  

Al elegir colores [][DevtoolsCssReferenceColorPicker] con el Selector de colores o **** alternar entre representaciones de color en el panel Estilos manteniendo y seleccionando el valor, se muestra la sintaxis del argumento separado `Shift` por `background-color` espacios.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Uso de argumentos separados por espacios en el panel Estilos" lightbox="../../media/2020/05/color.msft.png":::
  Uso de argumentos separados por espacios en el **panel Estilos**  
:::image-end:::  

También debe mostrar la sintaxis en el **panel Calculado** y la información sobre herramientas del **modo de** inspección.  

Microsoft Edge DevTools usa la nueva sintaxis porque las próximas características CSS como [color()][CSSWGDraftsColor4Property] no admiten la sintaxis de argumentos separados por comas en desuso.  

La sintaxis de argumentos separados por espacios se ha admitido en la mayoría de los exploradores durante un tiempo.  Para obtener más información, vaya [a ¿Puedo usar: notaciones de color funcionales separadas por espacios?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

Problema de [chromium #1072952][CR1072952]  

### <a name="deprecation-of-the-properties-pane-in-the-elements-panel"></a>Desuso del panel Propiedades en el panel Elementos  

El **panel Propiedades** de la herramienta **Elementos** está en desuso.  En `console.dir($0)` su lugar, ejecute **en la** consola.  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="El panel Propiedades en desuso" lightbox="../../media/2020/05/properties.msft.png":::
   El panel Propiedades **en desuso**  
:::image-end:::  

#### <a name="references"></a>Referencias  

*   [console.dir()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesDom]  

### <a name="app-shortcuts-support-in-the-manifest-pane"></a>Compatibilidad con accesos directos de aplicaciones en el panel Manifiesto  

Los accesos directos de la aplicación ayudan a los usuarios a iniciar rápidamente tareas comunes o recomendadas dentro de una aplicación web.  El menú de accesos directos de la aplicación solo se muestra para [las aplicaciones web][PwaIndex] progresivas que están instaladas en el dispositivo móvil o de escritorio del usuario.  

<!--For more information, navigate to [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Accesos directos de la aplicación en el panel Manifiesto" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Accesos directos de la aplicación en el **panel** Manifiesto  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si estás en Windows o macOS, considera usar los canales de vista [previa de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Getting in touch with Microsoft Edge Devtools team  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/settings-icon.msft.png  
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/toggle-screencast-icon.msft.png  
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/refresh-page-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/media/record-icon.msft.png  

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Usa el emulador de Surface Duo | Microsoft Docs"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "dir: referencia de api de consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento seleccionado recientemente o objeto JavaScript: referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambiar colores con el Selector de colores: referencia CSS | Microsoft Docs"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer: personalizar información general | Microsoft Docs"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y corregir problemas con la pestaña Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Introducción a los emuladores de Surface Duo de depuración remota | Microsoft Docs"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota de dispositivos Windows 10 | Microsoft Docs"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Inspeccione los detalles del recurso | Microsoft Docs"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar actividad de red | Microsoft Docs"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft Docs"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicación Android de Microsoft Edge"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notaciones de color funcionales separadas por espacios: MDN | ¿Puedo usar?"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar los métodos abreviados de teclado o los enlaces de teclas | Errores de Chromium"  
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Errores de Chromium"  
[CR1040019]: https://crbug.com/1040019 "DevTools: vista previa de imágenes e imágenes de fondo fácilmente en el panel Estilos | Errores de Chromium"  
[CR1040025]: https://crbug.com/1040025 "DevTools: muestra información básica de a11y en elementos emergentes | Errores de Chromium"  
[CR1048378]: https://crbug.com/1048378 "Compatibilidad con la interfaz de usuario de DevTools para el modo de contraste alto | Errores de Chromium"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Errores de Chromium"  
[CR1068116]: https://crbug.com/1068116 "Enviar problemas de panel | Errores de Chromium"  
[CR1072952]: https://crbug.com/1072952 "DevTools: el selector de colores debe producir una sintaxis de color CSS moderna | Errores de Chromium"  
[CR1075437]: https://crbug.com/1075437 "DevTools: agregue compatibilidad con la palabra clave y el valor css 'revert' | Errores de Chromium"  
[CR1076112]: https://crbug.com/1076112 "Personalización de Devtools: cambiador de tamaño de cajón"  
[CR1081486]: https://crbug.com/1081486 "El foco del teclado no está visible para los botones de navegación en modo de difusión | Errores de Chromium"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus debe ser "cumplido", no "resuelto" | Errores de V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Cambios de Colors 3 - CSS Color Module Level 4 | Borradores del editor de grupo de trabajo CSS de W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. Color de primer plano: el 'color' - Módulo de color CSS Nivel 4 | Borradores del editor de grupo de trabajo CSS de W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Presentación del nuevo Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Estados y destinos: domenic/promises-unwrapping | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "revertir | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilidad del explorador | MDN"  

[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio código"  
[VisualStudioCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio métodos abreviados de teclado de código para Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: Teclado | WebHint"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: Name Role Value | WebHint"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Activar o desactivar el modo de contraste alto en Windows | Compatibilidad con Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/edge-developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de vista previa de Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/05/devtools/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
