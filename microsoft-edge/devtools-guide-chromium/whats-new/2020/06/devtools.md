---
description: Características de depuración de cuadrícula CSS, solicitudes de edición y reproducción con la consola de red y mucho más.
title: Novedades de DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 9031f817a6079f64352c261a70eb9581213bf8c7
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408321"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-85"></a>Novedades de DevTools (Microsoft Edge 85)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Anuncios del equipo de Microsoft Edge DevTools  

Las siguientes secciones son una lista de anuncios que puede que falte del equipo de Microsoft Edge DevTools.  Echa un vistazo a los anuncios para probar nuevas características en DevTools, microsoft Visual Studio code extensions y mucho más.  Para mantenerse al día de todas las características más recientes y más importantes de las herramientas para desarrolladores, descargue los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] y siga el equipo de Microsoft [Edge DevTools en Twitter][EdgeDevToolsTwitterAccount].  

### <a name="css-grid-debugging-features"></a>Características de depuración de cuadrícula CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

El equipo de Microsoft Edge DevTools colabora con el equipo de Chrome DevTools y la comunidad chromium para agregar nuevas características de depuración de cuadrícula CSS a DevTools.  Ahora puede mostrar números de línea de cuadrícula, espacios de cuadrícula y líneas de cuadrícula extendidas como una superposición en la página.  Además, próximamente se realizarán más mejoras en las herramientas de cuadrícula.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Características de depuración de cuadrícula CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Características de depuración de cuadrícula CSS
:::image-end:::  

> [!NOTE]
> Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOn] y active la casilla situada junto a Habilitar nuevas características **de depuración de cuadrícula CSS**.  
> 
> Para probar el experimento con un ejemplo, vaya al ejemplo [del planificador de cuadrícula CSS][CodepenRachelweilYzwBzKM].  

Problema de [chromium #1047356][CR1047356]  

### <a name="edit-and-replay-requests-with-the-network-console"></a>Editar y reproducir solicitudes con la consola de red  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Ahora puede usar Editar **y** reproducir en solicitudes en el registro de red [mediante][DevtoolsNetworkIndexLogActivity] la consola de **red.**  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Editar y reproducir una solicitud en networklog con la consola de red" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Editar y reproducir una solicitud en [networklog][DevtoolsNetworkIndexLogActivity] con la **consola de red**  
:::image-end:::  

Un nuevo panel, la **consola de** red se abre en el cajón [DevTools][DevtoolsCustomizeIndexDrawer] y se rellena automáticamente con información para la solicitud HTTP.  Para mostrar la respuesta devuelta desde el servidor, edite la solicitud \(si es necesario\) y seleccione **Enviar**.  

También puede usar la consola **de red** para crear y enviar solicitudes HTTP directamente desde DevTools.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Panel consola de red" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   Panel **consola de red**  
:::image-end:::  

> [!TIP]
> Para mostrar **la Consola de** red en el panel principal \(top\) en lugar del cajón [DevTools][DevtoolsCustomizeIndexDrawer], vaya a herramientas de movimiento [entre paneles](#move-tools-between-panels).  

> [!NOTE]
> Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla situada junto **a Habilitar consola de red.**  
> 
> Abra el [registro de red][DevtoolsNetworkIndexLogActivity], abra el menú contextual \(haga clic con el botón secundario\) y elija Editar y **reproducir**.  

Problema de [chromium #1093687][CR1093687]  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a>Service worker respondWith events in the Timing tab  

La **pestaña Tiempo** de la herramienta **Red** ahora incluye eventos de trabajo `respondWith` de servicio.  El evento de trabajo de servicio muestra la duración del tiempo inmediatamente antes de que el controlador de eventos de trabajo de servicio comience a ejecutarse hasta el momento en que se resuelva la promesa `respondWith` `fetch` del `respondWith` `fetch` controlador.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="El evento de trabajo de servicio respondWith en la pestaña Temporización del panel Red" lightbox="../../media/2020/06/timing-tab.msft.png":::
   Evento `respondWith` de trabajo de servicio en la pestaña **Temporización** de la **herramienta Red**  
:::image-end:::  

Expanda **Respuesta recibida** para mostrar información adicional de la respuesta como , y `fetch` `CacheStorageCacheName` `serviceWorkerResponseSource` `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expandir Respuesta recibida para mostrar información adicional de la respuesta de captura" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Expandir **respuesta recibida** para mostrar información adicional de la `fetch` respuesta  
:::image-end:::  

Problema de [chromium #1066579][CR1066579]  

### <a name="webhint-feedback-in-the-issues-panel"></a>comentarios de webhint en el panel Problemas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real sobre la accesibilidad, compatibilidad entre exploradores, seguridad, rendimiento, PWA y otros problemas comunes de desarrollo web de sitios web.  Para revisar los comentarios de webhint en el panel [Problemas.][DevtoolsIssues]  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="comentarios de webhint en el panel Problemas" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   comentarios de webhint en el panel Problemas  
:::image-end:::  

> [!NOTE]
> Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla situada junto **a Habilitar webhint**.  
> 
> Abra el panel [Problemas][DevtoolsIssues] para mostrar los comentarios de webhint.  

Problema de [chromium #1070378][CR1070378]  

### <a name="move-tools-between-panels"></a>Mover herramientas entre paneles  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Normalmente, herramientas como **Elementos** y **Red** solo se pueden abrir en el panel principal \(top\) de DevTools.  Del mismo modo, las herramientas como **Vista 3D** y **Problemas** solo pueden abrirse en el panel \(bottom\) del cajón de DevTools.  Ahora puede personalizar el diseño de DevTools moviendo las herramientas entre los paneles superior e inferior.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Mover herramientas entre paneles" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Mover herramientas entre paneles  
:::image-end:::  

> [!NOTE]
> Para habilitar el experimento, vaya a Activar características [experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla situada junto a Habilitar compatibilidad para mover **fichas entre paneles.**  

Problema de [chromium #897944][CR897944]  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a>Información sobre herramientas del iniciador mejorada en el panel Red  

En Microsoft Edge 83 y 84, la información sobre herramientas de la [][DevtoolsNetworkIndexLogActivity] columna Iniciador, que muestra la causa de la solicitud de recurso, en el registro de red que se muestra con una barra de desplazamiento horizontal.  Solo pudo mostrar la pila de llamadas que inició la solicitud desplazándose horizontalmente en la información sobre herramientas.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Información sobre herramientas del iniciador en Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   Información sobre herramientas del iniciador en Microsoft Edge 84  
:::image-end:::  

A partir de Microsoft Edge 85, ahora puede mostrar la pila de llamadas del iniciador en la información sobre herramientas sin desplazarse horizontalmente.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Información sobre herramientas del iniciador en Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   Información sobre herramientas del iniciador en Microsoft Edge 85
:::image-end:::  

Problema de chromium [#1069404][CR1069404]  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

En las secciones siguientes se anuncian características adicionales disponibles en Microsoft Edge 85 que se contribuyeron al proyecto chromium de código abierto.  

### <a name="style-editing-for-css-in-js-frameworks"></a>Edición de estilos para marcos CSS-in-JS  

El **panel Estilos** ahora admite mejor los estilos de edición que se crearon con las API del modelo de objetos CSS [(CSSOM).][CsswgDraftsCssom]  Muchos marcos y bibliotecas de CSS-in-JS usan las API cssom debajo del capó para crear estilos.  

Ahora puede editar los estilos agregados en JavaScript con hojas de estilos [constructables.][WicgConstructStylesheet]  Las hojas de estilo constructables son una nueva forma de crear y distribuir estilos reutilizables al usar [Shadow DOM][MdnShadowDom].  

Por ejemplo, los `h1` estilos agregados con `CSSStyleSheet` \(CSSOM API\) no se modificaban anteriormente.  Los estilos se pueden editar ahora en el panel **Estilos.**  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Cambiar la propiedad de fondo de los estilos h1 agregados con CSSStyleSheet de rosa a azul claro" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Cambiar la `background` propiedad de los estilos `h1` agregados con de a `CSSStyleSheet` `pink` `lightblue` .
:::image-end:::  

Pruebe esta característica con un [ejemplo que use CSS-in-JS][CodepenZoherghadyaliAbdgrpz].

Problema de [chromium #946975][CR946975]  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a>Faro 6 en el panel Faro  

El panel **Faro** está ejecutando Ahora Faro 6.  Para obtener una lista completa de todos los cambios, vaya a las notas de la [versión v6.0.0][GithubGoogleChromeLighthouse600].  

Lighthouse 6.0 presenta tres nuevas métricas al informe: La mayor pintura contenta \(LCP\), Desplazamiento de diseño acumulado \(CLS\) y Tiempo total de bloqueo \(TBT\).  

La fórmula de puntuación de rendimiento también se ha repondido para reflejar mejor la experiencia de carga del usuario.  

Problema de [chromium #772558][CR772558]  

#### <a name="first-meaningful-paint-deprecation"></a>Primer desuso de pintura significativa  

First Meaningful Paint \(FMP\) está en desuso en Lighthouse 6.0.  FMP también se ha quitado del panel **Rendimiento.**  **La pintura contentful más grande** es el reemplazo recomendado para FMP.  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

Problema de chromium [#1096008][CR1096008]  

### <a name="support-for-new-javascript-features"></a>Compatibilidad con nuevas características de JavaScript  

DevTools ahora tiene mejor compatibilidad con algunas de las características más recientes del lenguaje JavaScript.  

:::row:::
   :::column span="1":::
      [Autocompletion de sintaxis][V8DevOptionalChaining] de encadenamiento opcional  
   :::column-end:::
   :::column span="2":::
      La finalización automática de la propiedad **en la consola** ahora admite la sintaxis de encadenamiento opcional, por ejemplo, ahora funciona además de y  `name?.` `name.` `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Resaltado de sintaxis para [campos privados][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      Los campos de clase privada ahora están correctamente resaltados por la sintaxis y están bastante impresos en **el** panel Orígenes.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Resaltado de sintaxis [para el operador de conjunción Nullish][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      Ahora DevTools imprime correctamente el operador de conjunción nulo en el panel **Orígenes.**  
   :::column-end:::
:::row-end:::  

Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a>Nuevas advertencias de acceso directo de la aplicación en el panel Manifiesto  

**Los accesos directos de** la aplicación ayudan a los usuarios a iniciar rápidamente tareas comunes o recomendadas dentro de una aplicación web.  

<!--todo: add App shortcuts when section is live  -->  

El **panel** Manifiesto ahora muestra advertencias para las siguientes condiciones.  

* Los iconos de acceso directo de la aplicación son menores que 96 x 96 píxeles  
* Los iconos de acceso directo de la aplicación y los iconos de manifiesto no son cuadrados \(dado que los iconos se omiten\)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Advertencias de acceso directo de aplicaciones" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Advertencias de acceso directo de aplicaciones  
:::image-end:::  

Problema de chromium [#955497][CR955497]  

### <a name="consistent-display-of-the-computed-pane"></a>Visualización coherente del panel calculado  

El **panel Calculado de** la herramienta **Elementos** ahora se muestra de forma coherente como un panel en todos los tamaños de ventanilla.  Anteriormente, el **panel Calculado** se combinaba dentro del panel **Estilos** cuando el ancho de la ventanilla de DevTools era estrecho.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="El panel Calculado se muestra de forma coherente como un panel independiente incluso cuando las DevTools son estrechas" lightbox="../../media/2020/06/computed-pane.msft.png":::
   El **panel Calculado** se muestra de forma coherente como un panel independiente incluso cuando las DevTools son estrechas.
:::image-end:::  

Problema de [chromium #1073899][CR1073899]  

### <a name="bytecode-offsets-for-webassembly-files"></a>Desplazamientos de bytecode para archivos WebAssembly  

DevTools ahora usa desplazamientos de código de bytes para mostrar números de línea de desmontaje de Wasm.  
Los números de línea hacen que sea más claro que está mirando datos binarios y es más coherente con la forma en que el tiempo de ejecución de Wasm hace referencia a las ubicaciones.  

Problema de [chromium #1071432][CR1071432]  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a>Copiar y cortar en línea en el Panel orígenes  

Al realizar copias o cortes sin selección en el editor del [panel Orígenes,][DevtoolsSourcesEditCssJavascript]DevTools copia o corta la línea de contenido actual.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Con el cursor al final de la línea 5, copiando toda la línea desde pen.js en devTools y pegando en Visual Studio código" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   Con el cursor al final de la línea 5, copiando toda la línea de **pen.js** en DevTools y pegando en [Visual Studio Code][VisualStudioCode].
:::image-end:::  

Problema de chromium [#800028][CR800028]

### <a name="console-settings-updates"></a>Actualizaciones de configuración de consola  

#### <a name="ungroup-same-console-messages"></a>Desagrupar los mismos mensajes de consola  

La **alternancia Grupo similar** en Configuración de consola ahora se aplica a los mensajes duplicados.  Anteriormente solo se aplicaba a mensajes similares.  

Por ejemplo, anteriormente, DevTools no desagrupó los mensajes `hello` aunque **group similar** está desactivado.  Ahora, los `hello` mensajes se desagrupa.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Cuando group similar is unchecked, the hello messages are ungrouped" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Cuando **group similar** is unchecked, the messages are `hello` ungrouped
:::image-end:::  

Pruebe esta característica con un [ejemplo que envíe mensajes duplicados a la consola][CodepenZoherghadyaliZyrjgdJ].  

Problema de [chromium #1082963][CR1082963]  

### <a name="persisting-selected-context-only-settings"></a>Persisting Selected context only settings  

Ahora **solo se conserva la** configuración de contexto seleccionado en Configuración de consola.  Anteriormente, la configuración se restablece cada vez que se cierra y se vuelve a abrir DevTools.  El cambio hace que el comportamiento de configuración sea coherente con otras opciones de configuración de consola.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Configuración de solo contexto seleccionada" lightbox="../../media/2020/06/selected-context.msft.png":::
   **Configuración de solo contexto** seleccionada  
:::image-end:::  

Problema de [chromium #1055875][CR1055875]  

### <a name="performance-panel-updates"></a>Actualizaciones del panel de rendimiento  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a>Información de caché de compilación de JavaScript en **la herramienta** Rendimiento  

[La información de caché de compilación de JavaScript][V8DevCodeCaching] ahora siempre se muestra en el panel **Resumen** de la **herramienta** Rendimiento.  Anteriormente, DevTools no mostraba nada relacionado con el almacenamiento en caché de código si el almacenamiento en caché de código no se hacía.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Información de caché de compilación de JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Información de caché de compilación de JavaScript  
:::image-end:::  

Problema de [chromium #912581][CR912581]  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a>Alineación del tiempo de navegación en el panel Rendimiento  

El **** panel Rendimiento usado para mostrar horas en las reglas en función del momento en que se inició la grabación.  Ahora, el tiempo ha cambiado para las grabaciones en las que el usuario navega, donde DevTools ahora muestra los tiempos de regla relativos a la navegación.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Alinear el tiempo de navegación en la herramienta Rendimiento" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Alinear el tiempo de navegación en **la herramienta Rendimiento**  
:::image-end:::  

Las horas `DOMContentLoaded` de , First Paint, First Contentful Paint y Largest Contentful Paint eventos se actualizan para ser relativos al inicio de la navegación, lo que significa que el tiempo coincide con los tiempos notificados por `PerformanceObserver` .  

Problema de [chromium #974550][CR974550]  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a>Nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y puntos de registro  

El panel **Orígenes** tiene nuevos diseños para puntos de interrupción, puntos de interrupción condicionales y puntos de registro.  Los puntos de interrupción se representan mediante un círculo rojo, al igual que [Visual Studio Code][VisualStudioCode] y [Visual Studio][VisualStudio].  Se agregan iconos para diferenciar puntos de interrupción condicionales y puntos de registro.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Puntos de interrupción" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Puntos de interrupción  
:::image-end:::  

Problema de [chromium #1041830][CR1041830]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si estás en Windows o macOS, considera usar los canales de vista [previa de Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Herramientas de desarrollo de Microsoft Edge (Chromium) | Microsoft Docs"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Drawer: personalizar Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Editar CSS y JavaScript: información general del panel orígenes | Microsoft Docs"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Actividad de red de registro: inspeccionar la actividad de red en Microsoft Edge DevTools | Microsoft Docs"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edición de estilos para marcos CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Enviar mensajes duplicados a la consola | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Ejemplo de planificador de cuadrícula CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la versión más reciente de | Errores de Chromium"  
[CR800028]: https://crbug.com/800028 "Acceso directo de línea duplicada en el editor de Herramientas de desarrollador que no funciona después de actualizar Chrome | Errores de Chromium"  
[CR912581]: https://crbug.com/912581 "Exponer los scripts almacenados en caché por V8 en DevTools/about:tracing | Errores de Chromium"  
[CR946975]: https://crbug.com/946975 "La barra lateral de estilos de DevTools no funciona con hojas de estilos construidas | Errores de Chromium"  
[CR955497]: https://crbug.com/955497 "Menú contextual de icono de aplicación para PWAs | Errores de Chromium"  
[CR974550]: https://crbug.com/974550 "Error de coincidencia de métricas entre el panel Perf y performanceObserver | Errores de Chromium"  
[CR1041830]: https://crbug.com/1041830 "Mejorar los colores de los puntos de interrupción | Errores de Chromium"  
[CR1055875]: https://crbug.com/1055875 "El valor de la configuración de consola Solo contexto seleccionado no persiste después de cerrar y volver a abrir herramientas de | Errores de Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools: mostrar la escala de tiempo de recuperación de ServiceWorkers por solicitud en el panel DevTools | Errores de Chromium"  
[CR1071432]: https://crbug.com/1071432 "Wasm Basic Developer Experience | Errores de Chromium"  
[CR1073899]: https://crbug.com/1073899 "La pestaña Estilo calculado desaparece en modo de respuesta | Errores de Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools: el resaltado de sintaxis no funciona con campos privados | Errores de Chromium"  
[CR1082963]: https://crbug.com/1082963 "No se puede deshabilitar el comportamiento de mensajes similares de grupo de la consola | Errores de Chromium"  
[CR1083214]: https://crbug.com/1083214 "acorn no admite cadenas opcionales | Errores de Chromium"  
[CR1083797]: https://crbug.com/1083797 "Se ha roto la impresión bastante para la | Errores de Chromium"  
[CR1096008]: https://crbug.com/1096008 "Quitar FMP | Errores de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS Grid/Flexbox/Table | Errores de Chromium"  
[CR1093687]: https://crbug.com/1093687 "Crear herramienta para crear y reproducir solicitudes de red sintéticas | Errores de Chromium"  
[CR1070378]: https://crbug.com/1070378 "Integrar webhint en DevTools | Errores de Chromium"  
[CR1069404]: https://crbug.com/1069404 "Los elementos emergentes del widget [Herramientas de desarrollo] son demasiado estrechos | Errores de Chromium"  
[CR897944]: https://crbug.com/897944 "Paneles de devtool arrastrables | Errores de Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0: GoogleChrome/lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/edge-developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Uso de dom de sombra | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canales de vista previa de Microsoft Edge"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Visual Studio Code"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de objetos CSS (CSSOM) | Borradores del editor de grupo de trabajo CSS de W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Campos de clase privada: campos de clase pública y privada | V8. Desarrollo"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Almacenamiento en caché de código para desarrolladores de JavaScript | V8. Desarrollo"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Nullish coalescing | V8. Desarrollo"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Cadenas opcionales | V8. Desarrollo"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos de hoja de estilos | Web Incubator CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "La web que queremos"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/06/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
