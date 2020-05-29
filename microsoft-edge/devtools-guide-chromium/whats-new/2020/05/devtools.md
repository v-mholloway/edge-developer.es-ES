---
title: Novedades de DevTools (Microsoft Edge 84)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f07639d3c5cd246704f3d489c0e59714a938f13d
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684941"
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

# Novedades de DevTools (Microsoft Edge 84)  

## Anuncios del equipo de Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge. Compruébelos para probar las nuevas características de la DevTools, las extensiones de código de VS y mucho más.  Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].  

### Usar el DevTools en el modo de contraste alto de Windows

Ahora, los DevTools de Microsoft Edge se muestran en el modo contraste alto cuando Windows está en modo de contraste alto.  

:::image type="complex" source="../../media/2020/05/high-contrast.msft.png" alt-text="Microsoft Edge DevTools en el modo contraste alto" lightbox="../../media/2020/05/high-contrast.msft.png":::
   Microsoft Edge DevTools en el modo contraste alto  
:::image-end:::  

[Siga las instrucciones para activar el modo de contraste alto en Windows][MicrosoftSupportWindows10HighContrastMode].  Para abrir el DevTools en Microsoft Edge, presione `F12` o `Ctrl` + `Shift` + `I` .  El DevTools se muestra en el modo contraste alto.  

> [!NOTE]
> En la actualidad, Microsoft Edge DevTools es compatible con el modo de alto contraste en Windows, pero no en macOS. 

[#1048378][CR1048378] de problemas de cromo  

### Hacer coincidir los métodos abreviados de teclado en el código de DevTools a VS  

En su [opinión](#getting-in-touch-with-microsoft-edge-devtools-team) y el [rastreador de problemas públicos de cromo][CRIssuesList], el equipo de DevTools de Microsoft Edge aprendió que desea poder personalizar los métodos abreviados de teclado en el DevTools.  En Microsoft Edge 84, ahora puede hacer coincidir los métodos abreviados de teclado del DevTools con el [código de vs][VSCode], que es solo una de las características en las que está trabajando el equipo para la personalización de los accesos directos.  

:::image type="complex" source="../../media/2020/05/keyboard-shortcut.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a VS" lightbox="../../media/2020/05/keyboard-shortcut.msft.png":::
   Microsoft Edge DevTools en el modo contraste alto  
:::image-end:::  

Para probar el experimento, abre DevTools configuración pulsando `?` o seleccionando el icono del ![ icono ][ImageSettingsIcon] de configuración de DevTools en la esquina superior derecha de la DevTools.  Vaya a la sección **experimentos** y active la casilla **Habilitar la opción de configuración personalizada de métodos abreviados de teclado (se necesita volver a cargar)**.  Ahora vuelva a cargar el DevTools, abra la configuración de nuevo y vaya a la sección **accesos directos** .  

Seleccione **DevTools (valor predeterminado)** en la lista desplegable **coincidir con métodos abreviados preestablecidos** y seleccione **código de Visual Studio**.  Los métodos abreviados de teclado de la DevTools ahora coinciden con los métodos abreviados para acciones equivalentes en VS Code.  

Por ejemplo, el método abreviado de teclado para pausar o seguir ejecutando un script en [vs Code][VSCodeShortcuts] es `F5` .  Con el valor preestablecido **DevTools (predeterminado)** , ese mismo método abreviado de DevTools es, `F8` pero con el prefijo de código de **Visual Studio** , ese método abreviado también está ahora `F5` .  

La característica está actualmente disponible en Microsoft Edge 84 como experimento, por lo tanto, comparte tus [comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) con el equipo.  

[#174309][CR174309] de problemas de cromo  

### Emuladores de Surface de depuración remota Duo  

Ahora puede depurar de forma remota el contenido web que se ejecuta en el [emulador Surface Duo][DualScreensAndroidEmulator] con toda la potencia de [Microsoft Edge DevTools][DevToolsChromiumGuide].  

Con el [emulador Surface Duo][DualScreensAndroidEmulator], puedes probar cómo se procesa tu contenido web en una nueva clase de plegable y dispositivos de doble pantalla.  El emulador ejecuta el sistema operativo Android y proporciona la [aplicación Microsoft Edge Android][AndroidEdge].  Cargue el contenido web en la [aplicación Microsoft Edge][AndroidEdge] y depure con el [DevTools de Microsoft Edge][DevToolsChromiumGuide].  

:::image type="complex" source="../../media/2020/05/surface-duo-emulator.msft.png" alt-text="La aplicación Microsoft Edge que se ejecuta en el emulador Surface Duo" lightbox="../../media/2020/05/surface-duo-emulator.msft.png":::
   La aplicación Microsoft Edge en el emulador Surface Duo  
:::image-end:::  

La `edge://inspect` Página de una instancia de escritorio de [Microsoft Edge][DesktopEdge] muestra la **SurfaceDuoEmulator** con una lista de las pestañas abiertas o de [PWAs][PwaIndex] que se ejecutan en el [emulador Surface Duo][DualScreensAndroidEmulator].  

:::image type="complex" source="../../media/2020/05/edge-inspect.msft.png" alt-text="La página edge://inspect muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador" lightbox="../../media/2020/05/edge-inspect.msft.png":::
   La `edge://inspect` página muestra una lista de las pestañas abiertas en la aplicación Microsoft Edge que se ejecuta en el emulador
:::image-end:::  

Al seleccionar **inspeccionar** para la ficha o PWA que desea depurar, se abre la [DevTools Microsoft Edge][DevToolsChromiumGuide].  [Sigue la guía paso a paso para depurar de forma remota el contenido web en el emulador Surface Duo][DevToolsRemoteDebugDuoEmulator].  

### Cambiar el tamaño del cajón de DevTools más fácilmente  

En Microsoft Edge 83 o versiones anteriores, solo podía cambiar el tamaño del [cajón de DevTools][DevToolsDrawer] al colocar el puntero del ratón dentro de la barra de herramientas del cajón.  El cajón se comportó de forma diferente que otros controles de tamaño de los paneles de la DevTools, donde coloca el puntero sobre el borde del panel para cambiar su tamaño.  Seleccione la siguiente imagen para ver cómo ha funcionado el cambio de tamaño del cajón en la versión 83 o anterior de Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/drawer-83.msft.png" alt-text="Cambiar el tamaño del cajón de DevTools en Microsoft Edge 83" lightbox="../../media/2020/05/drawer-83.msft.gif":::
   Cambiar el tamaño del cajón de DevTools en Microsoft Edge 83
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

A partir de Microsoft Edge 84, ahora puede cambiar el tamaño de la bandeja de la caja al colocar el puntero sobre el borde del alimentador.  Este cambio alinea el comportamiento que cambia el tamaño del cajón de DevTools con la forma de cambiar el tamaño de otros paneles en el DevTools.  Seleccione la siguiente imagen para ver cómo cambiar el tamaño en acción en Microsoft Edge 84.  

:::image type="complex" source="../../media/2020/05/drawer-84.msft.png" alt-text="Cambiar el tamaño del cajón de DevTools en Microsoft Edge 84" lightbox="../../media/2020/05/drawer-84.msft.gif":::
   Cambiar el tamaño del cajón de DevTools en Microsoft Edge 84
:::image-end:::  

<!--todo:  create png that represents the gif information  -->  

[#1076112][CR1076112] de problemas de cromo  

### Los botones de navegación en el screencast muestran el foco  

Cuando se depura de forma remota un [dispositivo Android][DevToolsRemoteDebugAndroid], un [dispositivo Windows 10][DevToolsRemoteDebugWindows]o un [emulador Surface Duo][DevToolsRemoteDebugDuoEmulator], puede alternar el icono de la ![ demostración de alternancia ][ImageScreencastingIcon] en la esquina superior izquierda de la DevTools.  Con el screencasts habilitado, podrás navegar por la pestaña de Microsoft Edge en el dispositivo remoto desde la ventana de DevTools.  En Microsoft Edge 84, estos botones de navegación ahora también son accesibles desde el teclado.  

:::image type="complex" source="../../media/2020/05/screencasting-nav.msft.png" alt-text="Al presionar Mayús + Tab en la barra de URL con el screencast se muestra el foco en el botón actualizar" lightbox="../../media/2020/05/screencasting-nav.msft.png":::
   Al pulsar en `Shift` + `Tab` la barra de URL con el screencast se muestra el foco en el botón **Actualizar**
:::image-end:::  

[#1081486][CR1081486] de problemas de cromo  

### El panel de detalles del panel de red toma el foco  

En Microsoft Edge 84, el [Panel de detalles][DevToolsNetworkDetails] del panel **red** toma el foco cuando lo abre para un recurso en el [registro de red][DevToolsNetworkLog].  Este cambio permite a los lectores de pantalla leer e interactuar con el contenido del panel de **detalles** .  

:::image type="complex" source="../../media/2020/05/network-details.msft.png" alt-text="El panel de detalles del panel red toma el foco cuando se abre" lightbox="../../media/2020/05/network-details.msft.png":::
   El panel de **detalles** del panel **red** toma el foco cuando se abre
:::image-end:::  

[#963183][CR963183] de problemas de cromo  

## Anuncios del proyecto de cromo  

En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 84 que se han contribuido al proyecto de código abierto.  

### Solucionar problemas del sitio con la nueva herramienta problemas en el cajón de DevTools

La nueva herramienta **problemas** del cajón de DevTools se creó para ayudar a reducir la fatiga de las notificaciones y el desorden de la **consola**.  En la actualidad, la **consola** es el lugar más central para que los desarrolladores de sitios web, bibliotecas, marcos y Microsoft Edge registren mensajes, advertencias y errores.  La herramienta **problemas** agrega advertencias al explorador de una forma estructurada, agregada y con procedimientos, vínculos a recursos afectados en Microsoft Edge DevTools, y proporciona instrucciones sobre cómo corregir los problemas.  Con el tiempo, debería ver cada vez más advertencias en Microsoft Edge en la herramienta **problemas** en lugar de en la **consola**, lo que ayuda a reducir el desorden en la **consola**.  

Para empezar, vea [Buscar y corregir problemas con la herramienta problemas de Microsoft Edge DevTools][DevtoolsIssuesIndex].  

:::image type="complex" source="../../media/2020/05/issues.msft.png" alt-text="La herramienta problemas del cajón de DevTools" lightbox="../../media/2020/05/issues.msft.png":::
   La herramienta **problemas** del cajón de DevTools  
:::image-end:::  

[#1068116][CR1068116] de problemas de cromo  

### Ver información de accesibilidad en la información sobre herramientas del modo inspeccionar  

La información sobre herramientas del **modo de inspección** ahora indica si el elemento tiene un [nombre y una función][WebhintHintsAxeNameRoleValue] accesibles y tiene el [teclado enfocado][WebhintHintsAxeKeyboard].  

<!--todo:  add link inspect mode tooltip (WebdevCls) when section is live  -->  
<!--todo:  add link name and role (WebdevLabelsText) when section is live  -->  
<!--todo:  add link keyboard-focusable (WebdevControlFocus) when section is live  -->  

:::image type="complex" source="../../media/2020/05/a11y.msft.png" alt-text="Información sobre herramientas de modo inspeccionar con información de accesibilidad" lightbox="../../media/2020/05/a11y.msft.png":::
  Información sobre herramientas de **modo inspeccionar** con información de accesibilidad  
:::image-end:::  

[#1040025][CR1040025] de problemas de cromo  

### Actualizaciones del panel de rendimiento  

#### Ver la información de tiempo de bloqueo total en el pie de página  

Después de grabar el rendimiento de la carga, el panel **rendimiento** ahora muestra la información de tiempo de bloqueo total \ (TBT \) en el pie de página.  TBT es una métrica de rendimiento de carga que ayuda a cuantificar cuánto tarda una página en ser utilizable.  Esencialmente mide cuánto tiempo una página parece ser utilizable \ (porque el contenido se representa en la pantalla \); pero no es realmente utilizable, porque JavaScript está bloqueando el subproceso principal y, por consiguiente, la página no responde a la entrada del usuario.  TBT es la métrica principal para aproximar el primer retraso de entrada.  

<!--todo:  add link Total Blocking Time (TBT) (WebdevTbt) when section is live  -->  
<!--todo:  add link lab metric (WebdevMeasureSpeedLabField) when section is live  -->  
<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  

Para obtener información sobre el tiempo de bloqueo total, no **Refresh Page** use el ![ flujo de trabajo actualizar icono de la página actualizar página ][ImageRefreshPageIcon] para grabar el rendimiento de carga de la página.  

En su lugar, **Record** seleccione ![ el icono grabar Registro ][ImageRecordIcon] , vuelva a cargar manualmente la página, espere a que se cargue la página y, a continuación, detenga la grabación.  

Si ves `Total Blocking Time: Unavailable` , Microsoft Edge DevTools no obtiene la información necesaria de los datos internos de generación de perfiles en Microsoft Edge.  

:::image type="complex" source="../../media/2020/05/tbt.msft.png" alt-text="Información sobre el tiempo de bloqueo total en el pie de página de una grabación del panel rendimiento" lightbox="../../media/2020/05/tbt.msft.png":::
   Información sobre el tiempo de bloqueo total en el pie de página de una grabación del panel **rendimiento**  
:::image-end:::  

[#1054381][CR1054381] de problemas de cromo  

#### Diseño de eventos de desplazamiento en la nueva sección de la experiencia  

La nueva sección de **experiencia** del panel **rendimiento** le ayuda a detectar los cambios de diseño.  La función de distribución acumulativa \ (CLS \) es una métrica que ayuda a cuantificar la inestabilidad visual no deseada.

<!--todo:  add link Core Web Vitals (WebdevCoreWebVitals) when section is live  -->  
<!--todo:  add link layout shifts (WebdevCls) when section is live  -->  

Seleccione el evento de **desplazamiento de diseño** para ver los detalles de los cambios de diseño en el panel **Resumen** .  Mantenga el mouse sobre los campos **movido desde** y **movido a** para visualizar dónde se produjo el desplazamiento de diseño.  

:::image type="complex" source="../../media/2020/05/cls.msft.png" alt-text="Detalles de un desplazamiento de diseño" lightbox="../../media/2020/05/cls.msft.png":::
   Detalles de un desplazamiento de diseño  
:::image-end:::  

### Terminología de promesas más exacta en la consola  

Al iniciar sesión `Promise` , el valor proporcionado en la **consola** incorrectamente `PromiseStatus` establecido en `resolved` .  

:::image type="complex" source="../../media/2020/05/resolved.msft.png" alt-text="Un ejemplo de la consola con la terminología anterior resuelta" lightbox="../../media/2020/05/resolved.msft.png":::
   Ejemplo de la **consola** con la terminología antigua `resolved`  
:::image-end:::  

La **consola** ahora usa el término `fulfilled` , que se alinea con la `Promise` especificación.  Para obtener más información sobre la `Promise` especificación, consulte [Estados y Fates en github](https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md).  

:::image type="complex" source="../../media/2020/05/fulfilled.msft.png" alt-text="Un ejemplo de la consola con la nueva terminología completada" lightbox="../../media/2020/05/fulfilled.msft.png":::
  Un ejemplo de la **consola** con la nueva `fulfilled` terminología  
:::image-end:::  

V8 [#6751][CRV86751] de problemas  

### Actualizaciones del panel estilos  

#### Compatibilidad con la palabra clave Revert  

La interfaz de usuario de autocompletar del panel **estilos** ahora detecta la palabra clave [Revert][MDNRevert] CSS, que revierte el valor de una propiedad en cascada al valor anterior que se aplica al estilo del elemento.  

:::image type="complex" source="../../media/2020/05/revert.msft.png" alt-text="Establecer el valor de una propiedad para revertir" lightbox="../../media/2020/05/revert.msft.png":::
  Establecer el valor de una propiedad para revertir  
:::image-end:::  

[#1075437][CR1075437] de problemas de cromo  

#### Vistas previas de imágenes  

Mantenga el mouse sobre un `background-image` valor en el panel **estilos** para obtener una vista previa de la imagen en una información sobre herramientas.  

:::image type="complex" source="../../media/2020/05/image-preview.msft.png" alt-text="Mantener el puntero sobre un valor de imagen de fondo" lightbox="../../media/2020/05/image-preview.msft.png":::
  Mantener el puntero sobre un `background-image` valor  
:::image-end:::  

[#1040019][CR1040019] de problemas de cromo  

#### El selector de colores ahora usa una notación de color funcional separada por espacios  

El [módulo de color CSS nivel 4][CSSWGDraftsColor4Changes3] especifica que las funciones de color, como `rgb()` , deben admitir argumentos separados por espacios.  Por ejemplo, `rgb(0, 0, 0)` equivale a `rbg(0 0 0)`.  

Al elegir colores con el [selector de colores][DevtoolsCssReferenceColorPicker] o alternar entre representaciones de color en el panel **estilos** , si mantiene presionado `Shift` el `background-color` valor, debería ver la sintaxis de los argumentos separados por espacios.  

:::image type="complex" source="../../media/2020/05/color.msft.png" alt-text="Usar argumentos separados por espacios en el panel estilos" lightbox="../../media/2020/05/color.msft.png":::
  Usar argumentos separados por espacios en el panel **estilos**  
:::image-end:::  

También debe ver la sintaxis en el panel **calculado** y en la información sobre herramientas del **modo inspeccionar** .  

Microsoft Edge DevTools usa la nueva sintaxis porque las próximas características CSS, como [color ()][CSSWGDraftsColor4Property] , no admiten la sintaxis de argumentos separados por comas obsoletas.  

La sintaxis de argumentos separados por espacios es compatible con la mayoría de los exploradores durante un rato.  Para obtener más información, vea [¿puedo usar las notas de colores funcionales separadas por espacios?][CaniuseMDNSpaceSeparatedFunctionalColorNotations]  

[#1072952][CR1072952] de problemas de cromo  

### Desuso del panel de propiedades en el panel elementos  

El panel de **propiedades** del panel **elementos** está obsoleto.  `console.dir($0)`En su lugar, se ejecuta en la **consola** .  

:::image type="complex" source="../../media/2020/05/properties.msft.png" alt-text="El panel Propiedades obsoletas" lightbox="../../media/2020/05/properties.msft.png":::
   El panel **propiedades** obsoletas  
:::image-end:::  

#### Referencias  

*   [Console. dir ()][DevtoolsConsoleApiDir]  
*   [$0][DevtoolsConsoleUtilitiesDom]  

### Compatibilidad con los métodos abreviados de aplicaciones en el panel manifiesto  

Los accesos directos a aplicaciones ayudan a los usuarios a iniciar rápidamente las tareas comunes o recomendadas dentro de una aplicación Web.  El menú de métodos abreviados de la aplicación solo se muestra para las [aplicaciones web progresivas][PwaIndex] que se instalan en el dispositivo móvil o de escritorio del usuario.  

<!--For more information, see [Get things done quickly with app shortcuts][WebdevAppShortcuts].  -->  

<!--todo:  add link Get things done quickly with app shortcuts (WebdevAppShortcuts) when section is live -->  

:::image type="complex" source="../../media/2020/05/app-shortcuts.msft.png" alt-text="Accesos directos a aplicaciones en el panel manifiesto" lightbox="../../media/2020/05/app-shortcuts.msft.png":::
  Accesos directos a aplicaciones en el panel **manifiesto**  
:::image-end:::  

## Descargar los canales de Microsoft Edge Preview   

Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

  

Para comentar las nuevas características y cambios de la publicación, o cualquier otro tema relacionado con DevTools:  

*   Envíe sus comentarios con el icono de **comentarios** en el DevTools  
*   Tweet a [@EdgeDevTools][PostTweetEdgeDevTools]  
*   Enviar una sugerencia a [la web][TheWebWeWant] que queremos  
*   Archivar errores en esta página en el repositorio [Edge-desarrollador][GitHubMicrosoftDocsEdgeDeveloperNewIssue]  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="El icono de comentarios en el DevTools de Microsoft Edge" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  El icono de **comentarios** en el DevTools de Microsoft Edge  
:::image-end:::  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icono configuración de DevTools"
[ImageScreencastingIcon]: /microsoft-edge/devtools-guide-chromium/remote-debugging/images/toggle-screencast-icon.msft.png "Botón de alternancia de DevTools"
[ImageRefreshPageIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-page-icon.msft.png "Icono de página de actualización del panel de rendimiento de DevTools"
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png "Icono de registro del panel de rendimiento de DevTools"

<!-- links -->  

[DualScreensAndroidEmulator]: /dual-screen/android/use-emulator "Usar el emulador Surface Duo | Microsoft docs"

[DevtoolsConsoleApiDir]: /microsoft-edge/devtools-guide-chromium/console/api#dir "DIR-consola de referencia de API | Microsoft docs"  
[DevtoolsConsoleUtilitiesDom]: /microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento seleccionado recientemente o objeto de JavaScript: referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambiar los colores con el selector de colores-referencia de CSS | Microsoft docs"  
[DevToolsDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón: personalizar información general | Microsoft docs"  
[DevToolsChromiumGuide]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y solucionar problemas con la ficha problemas de Microsoft Edge DevTools | Microsoft docs"  
[DevToolsRemoteDebugAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Introducción a la depuración remota dispositivos Android | Microsoft docs"  
[DevToolsRemoteDebugDuoEmulator]: /microsoft-edge/devtools-guide-chromium/remote-debugging/surface-duo-emulator "Introducción a los emuladores de superficies de depuración remota Duo | Microsoft docs"  
[DevToolsRemoteDebugWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota dispositivos con Windows 10 | Microsoft docs"  
[DevToolsNetworkDetails]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Revise los detalles del recurso | Microsoft docs"  
[DevToolsNetworkLog]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar actividad de red | Microsoft docs"  
[PwaIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft docs"  
<!--[DevtoolsWhatsNew201901Inspect]: /microsoft-edge/devtools-guide-chromium/whats-new/2019/01/devtools#inspect "Detailed tooltips in Inspect Mode - What's New In DevTools (Edge 73) | Microsoft Docs"  -->  

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Aplicación Microsoft Edge Android"

[CaniuseMDNSpaceSeparatedFunctionalColorNotations]: https://caniuse.com/#feat=mdn-css_types_color_space_separated_functional_notation "Notas de colores funcionales separadas por espacios: MDN | ¿Puedo usar"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar métodos abreviados de teclado o enlaces de clave | Errores de cromo"  
[CR963183]: https://crbug.com/963183 "DevTools no son compatibles con WCAG | Errores de cromo"  
[CR1040019]: https://crbug.com/1040019 "DevTools: obtener fácilmente una vista previa de imágenes e imágenes de fondo en el panel estilos | Errores de cromo"  
[CR1040025]: https://crbug.com/1040025 "DevTools: Mostrar información de a11y básica en el elemento popover | Errores de cromo"  
[CR1048378]: https://crbug.com/1048378 "Compatibilidad con la interfaz de usuario de DevTools para el modo de contraste alto | Errores de cromo"  
[CR1054381]: https://crbug.com/1054381 "CR 1054381 | Errores de cromo"  
[CR1068116]: https://crbug.com/1068116 "Panel de problemas de envío | Errores de cromo"  
[CR1072952]: https://crbug.com/1072952 "DevTools: el selector de colores debe producir sintaxis de color CSS moderna | Errores de cromo"  
[CR1075437]: https://crbug.com/1075437 "DevTools: agregar compatibilidad con la palabra clave ' Revert ' de CSS | Errores de cromo"  
[CR1076112]: https://crbug.com/1076112 "Personalización de DevTools: el tamaño del cajón"  
[CR1081486]: https://crbug.com/1081486 "El foco del teclado no está visible para los botones de navegación en el modo de screencast | Errores de cromo"  
[CRV86751]: https://bugs.chromium.org/p/v8/issues/detail?id=6751 "PromiseStatus debe ser ' cumplida ', no ' resuelto ' | Errores de la V8"  

[CSSWGDraftsColor4Changes3]: https://drafts.csswg.org/css-color#changes-from-3 "Cambios de colores 3-módulo de color CSS nivel 4 | Borradores del editor del grupo de trabajo CSS W3C"  
[CSSWGDraftsColor4Property]: https://drafts.csswg.org/css-color#the-color-property "3. color de primer plano: el ' color ': módulo de color CSS nivel 4 | Borradores del editor del grupo de trabajo CSS W3C"  

[DesktopEdge]: https://www.microsoft.com/edge/ "Presentamos el nuevo Microsoft Edge"  

[GithubDomenicPromiseUnwrappingStatesFates]: https://github.com/domenic/promises-unwrapping/blob/master/docs/states-and-fates.md "Estados y Fates-Domenic/promesas: desenvolver | GitHub"  

[MDNRevert]: https://developer.mozilla.org/docs/Web/CSS/revert "revertir | MDN"  
[MDNRevertBrowserCompatibility]: https://developer.mozilla.org/docs/Web/CSS/revert#Browser_compatibility "Compatibilidad de explorador | MDN"  

[VSCode]: https://code.visualstudio.com/ "Código de Visual Studio"  
[VSCodeShortcuts]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Métodos abreviados de teclado de código de Visual Studio para Windows"  

[WebhintHintsAxeKeyboard]: https://webhint.io/docs/user-guide/hints/hint-axe/keyboard/ "Axe: teclado | Sugerencia"  
[WebhintHintsAxeNameRoleValue]: https://webhint.io/docs/user-guide/hints/hint-axe/name-role-value/ "Axe: valor del rol de nombre | Sugerencia"  

[MicrosoftSupportWindows10HighContrastMode]: https://support.microsoft.com/help/4026951/windows-10-turn-high-contrast-mode-on-or-off "Activar o desactivar el modo de alto contraste en Windows | Soporte técnico de Windows"  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools cuenta de Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Nuevo problema: MicrosoftDocs/Edge-Developer"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Canales de Microsoft Edge Preview"  
[TheWebWeWant]: https://aka.ms/webwewant "La web que queremos"  

<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebdevCoreWebVitals]: https://alphabet-dev/vitals#core-web-vitals "Core Web Vitals | alphabet-dev"  -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/05/devtools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
