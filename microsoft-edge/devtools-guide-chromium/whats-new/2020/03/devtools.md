---
description: Emular las deficiencias de la visión de color, acoplar a la izquierda en el menú de comandos y mucho más.
title: Novedades de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: c329dfba980b882b6e538447e52902e4d0cc985b
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514420"
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
# <a name="whats-new-in-devtools-microsoft-edge-83"></a>Novedades de DevTools (Microsoft Edge 83)  

Siguiendo la programación de Chromium actualizada, estamos ajustando nuestra programación para las próximas versiones de Microsoft Edge y cancelando la versión de Microsoft Edge 82. Consulta nuestra [entrada de blog][WindowsBlogStableRelease] para obtener más información.  

Estas son las nuevas características disponibles en DevTools en Microsoft Edge 83.  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Anuncios del equipo de Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede que falte del equipo de Microsoft Edge DevTools.  Echa un vistazo a los anuncios para probar nuevas características en DevTools, microsoft Visual Studio code extensions y mucho más.  Para mantenerse al día de todas las características más recientes y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] y [síganos en Twitter][EdgeDevToolsTwitterAccount].  

### <a name="remotely-debug-microsoft-edge-on-windows-10-devices"></a>Depuración remota de Microsoft Edge en dispositivos Windows 10  

La [aplicación Herramientas remotas para Microsoft Edge \(Beta\)][RemoteTools] ya está disponible en [la Microsoft Store][MicrosoftStore].  Con esta aplicación, que amplía el Portal de dispositivos [de Windows,][WindowsUwpDebugTestPerfDevicePortal]puedes conectarte desde la instancia de Microsoft Edge que se ejecuta en el equipo de desarrollo a un dispositivo remoto de Windows 10, mostrar una lista de destinos \(todas las pestañas de Microsoft Edge y [PWAs][ProgressiveWebAppsChromiumIndex] abiertas en el dispositivo Windows 10\) y usar DevTools en el equipo de desarrollo en un destino que se ejecuta en el dispositivo remoto de Windows 10.  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="La aplicación Herramientas remotas para Microsoft Edge (Beta) disponible en Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   La [aplicación Herramientas remotas para Microsoft Edge (Beta)][RemoteTools] disponible en [Microsoft Store][MicrosoftStore]  
:::image-end:::  

[Lee nuestra guía para configurar el dispositivo Windows 10 y la máquina de desarrollo para la depuración remota.][DevtoolsRemoteDebuggingWindows]  Háganos saber acerca de su experiencia de depuración remota [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

### <a name="new-ways-to-access-settings"></a>Nuevas formas de acceder a la configuración  

Hay un montón de opciones de configuración para DevTools que puedes personalizar para que DevTools se vea, se sienta y funcione de la forma que necesita. En Microsoft Edge 83, ahora es mucho más fácil obtener acceso a [Configuración][DevtoolsCustomizeIndexSettings] en DevTools.  Abre Configuración con el icono de engranaje junto a Alertas de consola y el menú principal.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="El icono de engranaje abre Configuración en DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   El icono de engranaje abre **Configuración** en DevTools  
:::image-end:::  

También puede abrir Configuración desde [el][DevtoolsCustomizeIndexSettings] menú **principal en** **Más herramientas.**

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menú principal > Más herramientas > configuración" lightbox="../../media/2020/03/settings2.msft.png":::
   **Menú principal**  >  **Más herramientas**  >  **Configuración**  
:::image-end:::  

Problema de [chromium #1050855][CR1050855]

### <a name="new-and-improved-infobars"></a>Infobars nuevas y mejoradas

Las barras de notificación informativos \(infobars\) de DevTools ahora tienen una apariencia mejorada y más funcionalidad. En Microsoft Edge 83, las barras de información son más fáciles de leer y proporcionar botones para que puedas realizar la acción pertinente de inmediato.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Infobar para imprimir un archivo minificado en Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   Infobar para imprimir un archivo minificado en Microsoft Edge versión 83  
:::image-end:::  

Problema de [chromium #1056348][CR1056348]

### <a name="navigate-the-color-picker-with-your-keyboard"></a>Navegar por el Selector de colores con el teclado  

El [Selector de colores][DevtoolsCssReferenceColorPicker] es una GUI en el panel [Elementos][DevtoolsCssIndex] para cambiar `color` y `background-color` declaraciones.  En versiones anteriores de Microsoft Edge, no podía navegar por la sección **Sombras** del Selector de [colores][DevtoolsCssReferenceColorPicker] con el teclado.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Ahora puedes usar el teclado para mover el selector en la sección Sombras del Selector de colores" lightbox="../../media/2020/03/color-picker.msft.png":::
   Ahora puedes usar el teclado para mover el selector en la sección **Sombras** del [Selector de colores][DevtoolsCssReferenceColorPicker]  
:::image-end:::  

En Microsoft Edge 83, ahora puedes usar el teclado para mover el selector en la sección **Sombras** del Selector de colores.  

Problema de [chromium #963183][CR963183]  

### <a name="properties-tab-now-populates-after-a-page-refresh"></a>La pestaña Propiedades se rellena ahora después de una actualización de página  

En Microsoft Edge 81 **** y versiones anteriores, las actualizaciones de página han roto la pestaña Propiedades del [panel][DevtoolsCssIndex] Elementos.  Al actualizar la página, la pestaña **Propiedades** no rellenaba las propiedades del elemento seleccionado actualmente.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="En Microsoft Edge 81 y versiones anteriores, la pestaña Propiedades estaba en blanco después de una actualización de página" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   En Microsoft Edge 81 y versiones anteriores, la **pestaña Propiedades** estaba en blanco después de una actualización de página  
:::image-end:::  

En Microsoft Edge 83, ahora puede mostrar las propiedades del elemento seleccionado actualmente después de una actualización de página en la **pestaña Propiedades**.  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="En Microsoft Edge 83, la pestaña Propiedades muestra las propiedades del elemento seleccionado actualmente después de una actualización de página" lightbox="../../media/2020/03/properties-in-82.msft.png":::
   En Microsoft Edge 83, la pestaña **Propiedades** muestra las propiedades del elemento seleccionado actualmente después de una actualización de página  
:::image-end:::  

Problema de [chromium #1050999][CR1050999]  

### <a name="use-the-arrow-keys-to-scroll-in-the-changes-tool"></a>Usar las teclas de flecha para desplazarse en la herramienta Cambios  

La **herramienta Cambios realiza** un seguimiento de los cambios realizados en CSS o JavaScript en DevTools.  Puede usar la herramienta **Cambios** para mostrar rápidamente todos los cambios y volver a usarlos en el editor/IDE.  

Para abrir la **herramienta Cambios,** seleccione `Ctrl` + `Shift` + `P` en DevTools para abrir el [menú comando][DevToolsCommandMenuIndex] y escriba `changes` .  elija y ejecute el **comando Mostrar cambios** para abrir la herramienta **Cambios** en el cajón DevTools.  

Cuando haya realizado un cambio en un archivo minificado, la herramienta **Cambios** permite desplazarse horizontalmente para mostrar todo el código minificado.  A partir de Microsoft Edge 83, ahora puede desplazarse horizontalmente con las teclas de flecha del teclado.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de flecha para mostrar el código minificado en la herramienta Cambios" lightbox="../../media/2020/03/changes.msft.png":::
   En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de flecha para mostrar los cambios realizados en el código **minificado** en la herramienta Cambios  
:::image-end:::  

Si usas lectores de pantalla o el teclado para navegar [][PostTweetEdgeDevTools] por DevTools, envíanos tus comentarios tuiteando o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Problema de [chromium #963183][CR963183]  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

En las secciones siguientes se anuncian características adicionales disponibles en Microsoft Edge 83 que se contribuyeron al proyecto chromium de código abierto.  

### <a name="emulate-vision-deficiencies"></a>Emular deficiencias visuales  

Abra la [pestaña Representación][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] y use la nueva característica **Emular** deficiencias de visión para obtener una mejor idea de cómo las personas con diferentes tipos de deficiencias de visión experimentan su sitio.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emular la visión borrosa" lightbox="../../media/2020/03/vision.msft.png":::
   Emular la visión borrosa  
:::image-end:::  

DevTools es capaz de emular la visión borrosa y los siguientes [tipos de deficiencias de la visión de color.][ColorBlindnessTypes]  

| Deficiencia de la visión de color | Detalles |  
|:--- |:--- |  
| Protanopia | La incapacidad de percibir cualquier luz roja. |  
| Deuteranopia | La incapacidad de percibir cualquier luz verde. |  
| Tritanopia | La incapacidad de percibir cualquier luz azul. |  
| Achromatopsia | La incapacidad de percibir cualquier color, excepto para las sombras de gris \(extremadamente rara\). |  

Existen versiones menos extremas de estas deficiencias de visión de color y, de hecho, son más comunes.  
Por ejemplo, protanomaly es una sensibilidad reducida a la luz roja (a diferencia de la protanopia, que es la incapacidad completa para percibir la luz roja). Sin embargo, estas deficiencias de visión **-omaly** no están tan claramente definidas: cada persona con una deficiencia de visión de este tipo es diferente y puede ver las cosas de forma diferente \(ser capaz de percibir más o menos de los colores relevantes\).  

Al diseñar para las simulaciones más extremas en DevTools, se garantiza que las aplicaciones web sean accesibles para las personas con protanomaly, deuteranomaly, tritanomaly y achromatomaly también.  

Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Problema de [chromium #1003700][CR1003700]  

### <a name="emulate-locales"></a>Emular configuraciones regionales  

Emular configuraciones regionales estableciendo una ubicación en **Ubicación de**  >  **sensores**. [Abra el **menú comando y** ][DevToolsCommandMenuIndex] escriba para obtener acceso a la pestaña `Sensors` **Sensores.**  Después de realizar estas acciones, DevTools modifica la configuración regional predeterminada actual, lo que afecta al código siguiente.  

*   `Intl.*` API, por ejemplo: `new Intl.NumberFormat().resolvedOptions().locale`  
*   Otras API de JavaScript con configuración regional, `String.prototype.localeCompare` como y , por `*.prototype.toLocaleString` ejemplo: `123_456..toLocaleString()`  
*   API de DOM como `navigator.language` y `navigator.languages`  
*   Encabezado de solicitud HTTP [Accept-Language][MDNAcceptLanguage]  

> [!NOTE]
> Las actualizaciones `navigator.language` a y no son `navigator.languages` visibles inmediatamente, pero solo después de la siguiente navegación o actualización de página.  Los cambios en el `Accept-Language` encabezado HTTP solo se reflejan para las solicitudes posteriores.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emular una configuración regional" lightbox="../../media/2020/03/locale.msft.png":::
   Emular una configuración regional  
:::image-end:::  

Para probar una demostración, vaya al [ejemplo de código dependiente de la configuración regional][MathiasByensLocaleDemo].

Problema de [chromium #1051822][CR1051822]

### <a name="cross-origin-embedder-policy-coep-debugging"></a>Depuración de directiva de incrustación entre orígenes (COEP)  

El panel Red ahora proporciona información de depuración de directivas [de incrustación entre][COEP] orígenes.  

La **columna** Estado ahora proporciona una explicación rápida de por qué se bloqueó una solicitud, así como un vínculo para ver los encabezados de esa solicitud para su posterior depuración:  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Solicitudes bloqueadas en la columna **Status**" lightbox="../../media/2020/03/status.msft.png":::
   Solicitudes bloqueadas en la **columna** Estado  
:::image-end:::  

La **sección Encabezados de** respuesta de la pestaña **Encabezados** proporciona más instrucciones sobre cómo resolver los problemas:  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Más instrucciones en la sección Encabezados de respuesta" lightbox="../../media/2020/03/guidance.msft.png":::
   Más instrucciones en la sección **Encabezados de** respuesta  
:::image-end:::  

Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Problema de [chromium #1051466][CR1051466]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y puntos de registro  

El panel Orígenes tiene nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y puntos de registro:  

*   Puntos de interrupción \(![Punto de interrupción](../../media/2020/03/breakpoint.msft.png)\) se representan mediante círculos rojos.  
*   Puntos de interrupción condicionales \(![Punto de interrupción condicional](../../media/2020/03/conditional.msft.png)\) están representados por círculos semi-rojos de medio blanco.  
*   Logpoints \(![Logpoint](../../media/2020/03/logpoint.msft.png)\) se representan mediante círculos rojos con iconos de consola.  

La motivación de los nuevos iconos era hacer que la interfaz de usuario fuera más coherente con otras herramientas de depuración DE GUI \(que normalmente colorean puntos de interrupción rojo\) y hacer que sea más fácil distinguir entre las 3 características de un vistazo.  

Problema de [chromium #1041830][CR1041830]  

### <a name="view-network-requests-that-set-a-specific-cookie-path"></a>Ver solicitudes de red que establecen una ruta de acceso de cookie específica  

Use la palabra clave de filtro nueva de la herramienta Red para centrarse en las solicitudes de red `cookie-path` que establecen una ruta de acceso de cookie [específica.][MDNCookiePath] ****  

Consulte [Filtrar solicitudes por propiedades para][DevtoolsNetworkReferenceFilterRequestsProperties] detectar más palabras clave como `cookie-path` .

### <a name="dock-to-left-from-the-command-menu"></a>Acoplar a la izquierda desde el menú comando  

Abra el [menú comando][DevToolsCommandMenuIndex] y ejecute el comando para `Dock to left` mover DevTools a la izquierda de la ventanilla.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools acoplada a la izquierda de la ventanilla" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   DevTools acoplada a la izquierda de la ventanilla  
:::image-end:::  

> [!NOTE]
> La **característica Acoplar a la** izquierda ha estado disponible desde Microsoft Edge 75, pero anteriormente solo era accesible desde el menú [principal][DevtoolsCustomizePlacementsChangeMainMenu].  La nueva característica de Microsoft Edge 83 es que ahora puede tener acceso a esta característica desde el menú de comandos.  

Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Problema de [chromium #1011679][CR1011679]  

### <a name="the-audits-panel-is-now-the-lighthouse-panel"></a>El panel Auditorías es ahora el panel Faro  

El equipo de DevTools recibió con frecuencia comentarios de desarrolladores web que, aunque era posible ejecutar [Lighthouse][GithubGoogleChromeLighthouse] desde DevTools, cuando lo intentaron no pudieron encontrar el panel "Faro", por lo que el panel **Auditorías** ahora es el **panel** Faro.  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Panel De faro" lightbox="../../media/2020/03/lighthouse.msft.png":::
   Panel De faro  
:::image-end:::  

> [!NOTE]
> El panel **Faro** proporciona vínculos al contenido hospedado en sitios web de terceros.  Microsoft no es responsable y no tiene control sobre el contenido de estos sitios ni sobre los datos que puedan recopilar.  

### <a name="delete-all-local-overrides-in-a-folder"></a>Eliminar todas las invalidaciones locales de una carpeta  

Después de configurar **Invalidaciones** locales, puede mantener el mouse en un directorio, abrir el menú contextual \(hacer clic con el botón secundario\) y elegir la nueva opción **Eliminar** todas las invalidaciones para eliminar todas las invalidaciones locales de esa carpeta.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Eliminar todas las invalidaciones" lightbox="../../media/2020/03/overrides.msft.png":::
   Eliminar todas las invalidaciones  
:::image-end:::  

Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Problema de [chromium #1016501][CR1016501]  

### <a name="updated-long-tasks-ui"></a>Interfaz de usuario de tareas largas actualizada  

Una **tarea larga** es código JavaScript que monopoliza el subproceso principal durante mucho tiempo, lo que hace que una página web se congele.  

Has podido visualizar tareas largas en el [panel][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] Rendimiento desde hace tiempo, pero en Microsoft Edge 83 se ha actualizado la interfaz de usuario de visualización de tareas largas en el panel Rendimiento.  La parte tarea larga de una tarea ahora se coloreó con un fondo rojo a rayas.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="La nueva interfaz de usuario de tarea larga" lightbox="../../media/2020/03/long-task.msft.png":::
   La nueva interfaz de usuario de tarea larga  
:::image-end:::  

Envía tus comentarios [tuiteando][PostTweetEdgeDevTools] o publicando el icono [Enviar](#getting-in-touch-with-microsoft-edge-devtools-team) comentarios.  

Problema de [chromium #1054447][CR1054447]  

### <a name="maskable-icon-support-in-the-manifest-pane"></a>Compatibilidad con iconos enmascarables en el panel Manifiesto  

Android Oreo introdujo iconos adaptables, que muestran iconos de aplicaciones en una variedad de formas en diferentes modelos de dispositivos.  **Los iconos enmascarables** son un nuevo formato de icono que admite iconos adaptables, que te permiten asegurarte de que el icono [de PWA][ProgressiveWebAppsChromiumIndex] se vea bien en dispositivos que admitan el estándar de iconos enmascarables.  

Habilita la nueva **casilla Mostrar solo** el área **** mínima segura para iconos enmascarables en el panel Manifiesto para comprobar que el icono enmascarable se ve bien en dispositivos Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Mostrar solo el área segura mínima para iconos enmascarables" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   La **casilla Mostrar solo el área segura mínima para iconos enmascarables**  
:::image-end:::  

> [!NOTE]
> Esta característica se inicia en Microsoft Edge 81.  Las actualizaciones que se tratan aquí en Microsoft Edge 83 no se han cubierto en [What's New In DevTools (Microsoft Edge 81).][WhatsNew81]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de versión preliminar de Microsoft Edge  

Si estás en Windows o macOS, considera usar los canales de vista [previa de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[WhatsNew81]: ../01/devtools.md "Novedades de DevTools (Microsoft Edge 81) | Microsoft Docs"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambie los colores con el selector de | Microsoft Docs"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y cambio de css | Microsoft Docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Cambiar la ubicación desde el menú principal | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Ver la actividad del subproceso | Microsoft Docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de representación con la pestaña Representación | Microsoft Docs"  
[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft Docs"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota de dispositivos Windows 10 | Microsoft Docs"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Puntos de interrupción de línea de código: cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrar solicitudes por propiedades: referencia de análisis de red | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalización de Microsoft Edge DevTools | Microsoft Docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Introducción al Portal de dispositivos windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Herramientas remotas para Microsoft Edge (Beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de versiones preliminares de Microsoft Edge"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Actualización de versiones de canal estables para Microsoft Edge"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/programador perimetral - GitHub"  

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  
[TheWebWeWant]: https://webwewant.fyi "La web que queremos"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Tipos de ceguera de color"  

[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language | MDN"  
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives "Set-Cookie | MDN"  

[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Ejemplo de código dependiente de la configuración regional"  

[CR963183]: https://crbug.com/963183 "Problema 963183: DevTools no son compatibles con WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problema 1003700: Agregar compatibilidad con DevTools para la simulación de deficiencia de visión de color"  
[CR1011679]: https://crbug.com/1011679 "Problema 1011679: Introducir &quot;Acoplar a la izquierda&quot; mediante el menú de comandos"  
[CR1016501]: https://crbug.com/1016501 "Problema 1016501: Solicitud de característica: botón para eliminar todas las invalidaciones locales"  
[CR1050999]: https://crbug.com/1050999 "Problema 1050999: Pestaña Propiedades"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: Compatibilidad con la depuración DE COOP/COEP en DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problema 1054447: Actualizar métricas de rendimiento en la escala de tiempo de DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: agregar interfaz de usuario para emular la configuración regional"
[CR1041830]: https://crbug.com/1041830 "Problema 1041830: Mejorar los colores de los puntos de interrupción"
[CR1050855]: https://crbug.com/1050855 "Problema 1050855: La vista Configuración es difícil de detectar"
[CR1056348]: https://crbug.com/1056348 "Problema 1056348: Actualización de componentes de infobar"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "COOP y COEP explicados: directiva de abridor entre orígenes"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "COOP y COEP explicados: directiva de incrustación entre orígenes"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "| GitHub"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-83) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
