---
description: Depure Microsoft Edge de forma remota en dispositivos con Windows 10, nuevas maneras de obtener acceso a la configuración y mucho más.
title: Novedades de DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 94b8d067738a1749f136edf2a562652bece183a9
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993432"
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

# Novedades de DevTools (Microsoft Edge 83)  

Después de la programación de cromo actualizada, estamos ajustando nuestra programación para las próximas versiones de Microsoft Edge y cancelando la versión 82 de Microsoft Edge. Para obtener más información, consulta nuestra [entrada de blog][WindowsBlogStableRelease] .  

Estas son las nuevas características disponibles en el DevTools en Microsoft Edge 83.  

## Anuncios del equipo de Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede haber perdido del equipo de DevTools de Microsoft Edge. Compruébelos para probar las nuevas características de la DevTools, las extensiones de código de VS y mucho más.  Para mantenerte al tanto de las últimas y mejores características de las herramientas para desarrolladores, descarga los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y mantente [en Twitter][EdgeDevToolsTwitterAccount].  

### Depurar Microsoft Edge de forma remota en dispositivos con Windows 10  

La aplicación [de herramientas remotas para Microsoft Edge \ (beta \)][RemoteTools] ya está disponible en [Microsoft Store][MicrosoftStore].  Con esta aplicación, que extiende [Windows Device portal][WindowsUwpDebugTestPerfDevicePortal], podrás conectarte desde la instancia de Microsoft Edge que se ejecuta en el equipo de desarrollo a un dispositivo de Windows 10 remoto, ver una lista de destinos \ (todas las pestañas de Microsoft Edge y [PWAs][PprgressiveWebAppsChromiumIndex] abiertas en el dispositivo Windows 10) y usar el DevTools en el equipo de desarrollo con un destino que se ejecute en el dispositivo remoto  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="La aplicación de herramientas remotas para Microsoft Edge (beta) disponible en Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   Ilustración 1: aplicación de [herramientas remotas para Microsoft Edge (beta)][RemoteTools] disponible en [Microsoft Store][MicrosoftStore]  
:::image-end:::  

[Lea nuestra guía para configurar su dispositivo Windows 10 y su equipo de desarrollo para la depuración remota][DevtoolsRemoteDebuggingWindows].  Para informarnos sobre la experiencia de depuración remota, haga [clic en el][PostTweetEdgeDevTools] icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

### Nuevas formas de obtener acceso a la configuración  

Hay toneladas de opciones de configuración para el DevTools que puede personalizar para DevTools la apariencia y el funcionamiento de la manera que necesita. En Microsoft Edge 83, obtener acceso a la [configuración][DevtoolsCustomizeIndexSettings] de la DevTools es ahora mucho más fácil. Abra configuración con el icono de engranaje junto a alertas de consola y el menú principal.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="El icono de engranaje abre la configuración en el DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   Ilustración 2: el icono de engranaje abre la **configuración** en el DevTools  
:::image-end:::  

También puede abrir la [configuración][DevtoolsCustomizeIndexSettings] desde el **menú principal** , en **más herramientas**.

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Menú principal > más herramientas > configuración" lightbox="../../media/2020/03/settings2.msft.png":::
   Ilustración 3: **menú principal**  >  **más**  >  **Opciones de configuración** de herramientas  
:::image-end:::  

[#1050855][CR1050855] de problemas de cromo

### Infobars nuevos y mejorados

Las barras de notificación informativas \ (infobars \) en DevTools ahora tienen un aspecto mejorado y una mayor funcionalidad. En Microsoft Edge 83, infobars son más fáciles de leer y proporcionan botones para que puedas llevar a cabo la acción pertinente de inmediato.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Barra de barra para imprimir un archivo minified en Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   Ilustración 4: barra de barra para imprimir un archivo minified en Microsoft Edge versión 83  
:::image-end:::  

[#1056348][CR1056348] de problemas de cromo

### Navegar por el selector de colores con el teclado  

El [selector de colores][DevtoolsCssReferenceColorPicker] es una GUI en el [Panel elementos][DevtoolsCssIndex] para el cambio `color` y las `background-color` declaraciones.  En versiones anteriores de Microsoft Edge, no se podía navegar por la sección **sombras** del selector de [colores][DevtoolsCssReferenceColorPicker] con el teclado.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Ahora puede usar el teclado para mover el selector en la sección sombras del selector de colores." lightbox="../../media/2020/03/color-picker.msft.png":::
   Ilustración 5: ahora puede usar el teclado para mover el selector en la sección **sombras** del [selector de colores][DevtoolsCssReferenceColorPicker] .  
:::image-end:::  

En Microsoft Edge 83, ahora puede usar el teclado para mover el selector en la sección **sombras** del selector de colores.  

[#963183][CR963183] de problemas de cromo  

### La pestaña propiedades ahora se rellena después de actualizar una página  

En Microsoft Edge 81 y versiones anteriores, la **pestaña propiedades** del [Panel elementos][DevtoolsCssIndex] se interrumpió por actualizaciones de página.  Cuando ha actualizado la página, la **pestaña propiedades** no ha rellenado las propiedades del elemento seleccionado actualmente.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="En Microsoft Edge 81 y versiones anteriores, la pestaña propiedades estaba en blanco después de actualizar una página" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   Ilustración 6: en Microsoft Edge 81 y versiones anteriores, la **pestaña propiedades** estaba en blanco después de actualizar una página  
:::image-end:::  

En Microsoft Edge 83, ahora puede ver las propiedades del elemento seleccionado en ese momento después de actualizar una página en la **pestaña propiedades**.  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="En Microsoft Edge 83, la pestaña propiedades muestra las propiedades del elemento seleccionado actualmente después de actualizar una página." lightbox="../../media/2020/03/properties-in-82.msft.png":::
   Ilustración 7: en Microsoft Edge 83, la **pestaña propiedades** muestra las propiedades del elemento seleccionado actualmente después de actualizar una página.  
:::image-end:::  

[#1050999][CR1050999] de problemas de cromo  

### Use las teclas de dirección para desplazarse por la herramienta de cambios  

La **herramienta cambios** realiza un seguimiento de los cambios realizados en CSS o JavaScript en el DevTools.  Puede usar la **herramienta cambios** para ver rápidamente todos los cambios y recuperarlos en el editor o IDE.  

Para abrir la **herramienta de cambios** , pulsa `Ctrl` + `Shift` + `P` en el DevTools para abrir el menú de [comandos][DevToolsCommandMenuIndex] y escribir `changes` .  Seleccione y ejecute el comando **Mostrar cambios** para abrir la **herramienta de cambios** del alimentador de DevTools.  

Una vez que haya realizado un cambio en un archivo minified, la **herramienta cambios** le permitirá desplazarse horizontalmente para ver todo el código minified.  A partir de Microsoft Edge 83, ahora puede desplazarse horizontalmente con las teclas de dirección del teclado.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="En Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de dirección para ver el código de minified en la herramienta de cambios" lightbox="../../media/2020/03/changes.msft.png":::
   Ilustración 8: en Microsoft Edge 83, puede desplazarse horizontalmente con las teclas de dirección para ver los cambios que realizó en el código de minified en la **herramienta de cambios**  
:::image-end:::  

Si usa lectores de pantalla o el teclado para desplazarse por la DevTools, envíenos sus comentarios con un [Tweet][PostTweetEdgeDevTools] o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#963183][CR963183] de problemas de cromo  

## Anuncios del proyecto de cromo  

En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 83 que se han contribuido al proyecto de código abierto.  

### Emular deficiencias de la visión  

Abra la [pestaña representación][DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab] y use la nueva característica **emular deficiencias de Vision** para obtener una mejor idea de cómo las personas con diferentes tipos de deficiencias visuales experimentan su sitio.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Emular visión borrosa" lightbox="../../media/2020/03/vision.msft.png":::
   Ilustración 9: emular una visión borrosa  
:::image-end:::  

DevTools es capaz de emular una visión borrosa y los siguientes [tipos de deficiencias de la visión del color][ColorBlindnessTypes].  

| Deficiencia de la visión del color | Detalles |  
|:--- |:--- |  
| Protanopia | La incapacidad de percibir cualquier luz roja. |  
| Deuteranopia | La incapacidad de percibir cualquier luz verde. |  
| Tritanopia | La incapacidad de percibir cualquier luz azul. |  
| Achromatopsia | La incapacidad de percibir cualquier color, excepto tonos de gris \ (muy raro \). |  

Existen versiones menos extremas de estas deficiencias de la visión del color y, de hecho, son más comunes.  
Por ejemplo, protanomaly es una sensibilidad reducida a la luz roja (a diferencia de Protanopia, que es la incapacidad completa de percibir la luz roja). Sin embargo, estas deficiencias visuales de Omaly no están claramente definidas: todas las personas con dicha deficiencia visual son diferentes y pueden ver de manera diferente (pueden percibir más/menos los colores pertinentes).  

Al diseñar las simulaciones más extremas en DevTools, se garantiza que las aplicaciones web estarán accesibles para las personas con protanomaly, deuteranomaly, tritanomaly y achromatomaly también.  

Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1003700][CR1003700] de problemas de cromo  

### Emular configuraciones regionales  

Para emular configuraciones regionales, configura una ubicación en la ubicación de los **sensores**  >  **Location**. [Abrir el **menú de comandos** ][DevToolsCommandMenuIndex] y escribir `Sensors` para acceder a la ficha **sensores** .  Después de realizar estas acciones, DevTools modifica la configuración regional predeterminada actual, lo que afecta al siguiente código.  

*   `Intl.*` API, por ejemplo: `new Intl.NumberFormat().resolvedOptions().locale`  
*   Otras API de JavaScript que reconocen la configuración regional, como `String.prototype.localeCompare` y `*.prototype.toLocaleString` , por ejemplo: `123_456..toLocaleString()`  
*   Las API de DOM, como `navigator.language` y `navigator.languages`  
*   El [`Accept-Language`][MDNAcceptLanguage] encabezado de la solicitud http  

> [!NOTE]
> Actualizaciones de `navigator.language` y `navigator.languages` no visibles inmediatamente, pero solo después de la siguiente navegación o actualización de la página.  Los cambios en el `Accept-Language` encabezado HTTP solo se reflejan en solicitudes posteriores.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Emular una configuración regional" lightbox="../../media/2020/03/locale.msft.png":::
   Ilustración 10: emular una configuración regional  
:::image-end:::  

Para probar una demostración, consulta [ejemplo de código dependiente de la configuración regional][MathiasByensLocaleDemo].

[#1051822][CR1051822] de problemas de cromo

### Depuración de directivas de Embedder entre orígenes (COEP)  

El panel red ahora proporciona información de depuración de [directivas de Embedder entre orígenes][COEP] .  

La columna **Estado** ahora ofrece una explicación rápida del motivo por el que se bloqueó una solicitud, así como un vínculo para ver los encabezados de la solicitud para una mayor depuración:  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Solicitudes bloqueadas en la columna * * Estado * *" lightbox="../../media/2020/03/status.msft.png":::
   Ilustración 11: solicitudes bloqueadas en la columna Estado  
:::image-end:::  

La sección de **encabezados de respuesta** de la pestaña **encabezados** proporciona más información sobre cómo resolver los problemas:  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Más información en la sección de encabezados de respuesta" lightbox="../../media/2020/03/guidance.msft.png":::
   Ilustración 12: más instrucciones en la sección de encabezados de respuesta  
:::image-end:::  

Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1051466][CR1051466] de problemas de cromo  

### Nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y logpoints  

El panel orígenes tiene nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y logpoints:  

*   Puntos de interrupción \ (![Punto](../../media/2020/03/breakpoint.msft.png)\) se representan mediante círculos rojos.  
*   Puntos de interrupción condicionales \ (![Punto de interrupción condicional](../../media/2020/03/conditional.msft.png)\) se representan mediante círculos de doble cara de color rojo.  
*   Logpoints \(![Logpoint](../../media/2020/03/logpoint.msft.png)\) se representan mediante círculos rojos con iconos de consola.  

El motivo por el que los nuevos iconos era hacer que la interfaz de usuario sea más coherente con otras herramientas de depuración de GUI \ (que suelen tener puntos de interrupción de color rojo \) y para que sea más fácil distinguir las tres características de un vistazo.  

[#1041830][CR1041830] de problemas de cromo  

### Ver las solicitudes de red que establecen una ruta de cookie específica  

Use la nueva `cookie-path` palabra clave de filtro en el panel **red** para centrarse en las solicitudes de red que establecen una [ruta de cookie][MDNCookiePath]específica.  

Desproteja las [solicitudes de filtro por propiedades][DevtoolsNetworkReferenceFilterRequestsProperties] para descubrir más palabras clave como `cookie-path` .

### Acoplar a la izquierda desde el menú de comandos  

Abra el [menú de comandos][DevToolsCommandMenuIndex] y ejecute el `Dock to left` comando para mover DevTools a la izquierda de su ventanilla.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools acoplado a la izquierda de la ventanilla" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   Ilustración 13: DevTools acoplado a la izquierda de la ventanilla  
:::image-end:::  

> [!NOTE]
> La característica **acoplar a la izquierda** está disponible desde el 75 de Microsoft Edge, pero anteriormente solo era posible acceder a ella desde el [**menú principal**][DevtoolsCustomizePlacementsChangeMainMenu].  La nueva característica de Microsoft Edge 83 es que ahora puede acceder a esta característica desde el menú de comandos.  

Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1011679][CR1011679] de problemas de cromo  

### El panel auditorías es ahora el panel de Lighthouse  

El equipo DevTools con frecuencia recibe comentarios de los programadores de Internet que, aunque fuera posible ejecutar [Lighthouse][GithubGoogleChromeLighthouse] desde DevTools, cuando lo intentaron no podían encontrar el panel de la Lighthouse, por lo que el panel **auditorías** es ahora el panel de **Lighthouse** .  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="El panel de Lighthouse" lightbox="../../media/2020/03/lighthouse.msft.png":::
   Ilustración 14: el panel de Lighthouse  
:::image-end:::  

> [!NOTE]
> El panel de **Lighthouse** proporciona vínculos a contenido hospedado en sitios web de terceros.  Microsoft no se responsabiliza y no tiene ningún control sobre el contenido de estos sitios y los datos que pueden recopilar.  

### Eliminar todos los reemplazos locales de una carpeta  

Después de configurar los **reemplazos locales** , puede hacer clic con el botón secundario del mouse en una carpeta y seleccionar la nueva opción **eliminar todas las sustituciones** para eliminar todos los reemplazos locales de esa carpeta.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Eliminar todas las invalidaciones" lightbox="../../media/2020/03/overrides.msft.png":::
   Ilustración 15: eliminar todas las invalidaciones  
:::image-end:::  

Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1016501][CR1016501] de problemas de cromo  

### Interfaz de usuario de tareas largas actualizada  

Una **tarea larga** es código JavaScript que monopoliza el subproceso principal durante mucho tiempo, lo que provoca la inmovilización de una página web.  

Ya ha podido [visualizar tareas largas en el panel rendimiento][DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity] por un momento, pero en Microsoft Edge 83 se ha actualizado la interfaz de usuario de visualización de tareas largas en el panel rendimiento.  La parte de tarea larga de una tarea ahora está coloreada con un fondo con bandas de color rojo.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="La nueva interfaz de usuario de tareas largas" lightbox="../../media/2020/03/long-task.msft.png":::
   Ilustración 16: la nueva interfaz de usuario de tareas largas  
:::image-end:::  

Envíe sus [comentarios con un][PostTweetEdgeDevTools] comentario o haga clic en el icono para [Enviar comentarios](#getting-in-touch-with-microsoft-edge-devtools-team) .  

[#1054447][CR1054447] de problemas de cromo  

### Compatibilidad con el icono enmascarable en el panel manifiesto  

Android Oreo presentó iconos adaptables, que muestran los iconos de la aplicación en una variedad de formas en diferentes modelos de dispositivos.  Los **iconos Enmascarables** son un nuevo formato de icono que admite iconos adaptables, que le permiten asegurarse de que el icono de [PWA][PprgressiveWebAppsChromiumIndex] se ve bien en los dispositivos que admiten el estándar de iconos Enmascarables.  

Active la casilla nuevo **Mostrar solo el área mínima segura para los iconos Enmascarables** en el panel **manifiesto** para comprobar que el icono enmascarable es adecuado en dispositivos Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="La casilla Mostrar solo el área de seguridad mínima para iconos Enmascarables" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   Ilustración 17: la casilla **Mostrar solo el área mínima segura para los iconos Enmascarables**  
:::image-end:::  

> [!NOTE]
> Esta característica se inició en Microsoft Edge 81.  Las actualizaciones descritas aquí en Microsoft Edge 83 no se cubren en [novedades de DevTools (Microsoft edge 81)][WhatsNew81].  

## Descargar los canales de Microsoft Edge Preview  

Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/Edge-Developer-GitHub"  
[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de Microsoft Edge Preview"  
[TheWebWeWant]: https://webwewant.fyi "La web que queremos"  

[WhatsNew81]: ../01/devtools.md "Novedades de DevTools (Microsoft Edge 81) | Microsoft docs"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCssReferenceColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Cambiar colores con el selector de colores | Microsoft docs"  
[DevtoolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Introducción a la visualización y el cambio de CSS | Microsoft docs"  
[DevtoolsCustomizePlacementsChangeMainMenu]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Cambiar la ubicación desde el menú principal | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceViewMainThreadActivity]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Ver actividad de subproceso principal | Microsoft docs"  
[DevtoolsEvaluatePreformanceReferenceAnalyzeRenderingTab]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de la representación con la ficha representación | Microsoft docs"  
[PprgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft docs"  
[DevtoolsRemoteDebuggingWindows]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Introducción a la depuración remota dispositivos con Windows 10 | Microsoft docs"  
[DevtoolsJavascriptBreakpointsLineCode]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Puntos de interrupción de línea de código: Cómo pausar el código con puntos de interrupción en Microsoft Edge DevTools | Microsoft docs"
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Filtrar solicitudes por propiedades-referencia de análisis de red | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  

[WindowsUwpDebugTestPerfDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Información general de Windows Device portal"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Herramientas remotas para Microsoft Edge (beta)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  

[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20 "Actualizar en las versiones de canal estable para Microsoft Edge"

[MicrosoftVisualstudio]: https://visualstudio.microsoft.com "Visual Studio"  

[VisualstudioCode]: https://code.visualstudio.com "Código de Visual Studio"  

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness "Tipos de daltonismo"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Accept-Language"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Ejemplo de código dependiente de la configuración regional"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[CR963183]: https://crbug.com/963183 "Problema 963183: DevTools no son compatibles con WCAG"  
[CR1003700]: https://crbug.com/1003700 "Problema 1003700: agregar compatibilidad DevTools para simulación de deficiencias de la visión del color"  
[CR1011679]: https://crbug.com/1011679 "Problema 1011679: presentar ' acoplar a la izquierda ' con el menú de comandos"  
[CR1016501]: https://crbug.com/1016501 "Problema 1016501: solicitud de característica: botón para eliminar todos los reemplazos locales"  
[CR1050999]: https://crbug.com/1050999 "Problema 1050999: ficha Propiedades"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: compatibilidad con COOP/depuración de COEP en DevTools"  
[CR1054447]: https://crbug.com/1054447 "Problema 1054447: actualizar las métricas de rendimiento en la escala de tiempo de DevTools"  
[CR1051822]: https://crbug.com/1051822 "Problema 1051822: DevTools: agregar una interfaz de usuario para emular la configuración regional"
[CR1041830]: https://crbug.com/1041830 "Problema 1041830: mejorar los colores de los puntos de interrupción"
[CR1050855]: https://crbug.com/1050855 "Problema 1050855: la vista de configuración es difícil de detectar"
[CR1056348]: https://crbug.com/1056348 "Problema 1056348: actualización de componentes de barra de error"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Explicación de COOP y COEP explicado: política de apertura entre orígenes cruzados"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Normas de COOP y COEP explicadas: política de Embedder de origen cruzado"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Repositorio de GitHub Lighthouse"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/03/devtools/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
