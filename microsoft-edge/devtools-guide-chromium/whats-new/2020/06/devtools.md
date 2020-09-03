---
description: Características de depuración de la cuadrícula CSS, editar y reproducir solicitudes con la consola de red y mucho más.
title: Novedades de DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 96ad9a4f21c36135013033fa4de31281fe6c4e83
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993614"
---
# Novedades de DevTools (Microsoft Edge 85)  

## Anuncios del equipo de Microsoft Edge DevTools  

Las secciones siguientes son una lista de anuncios que puede haber perdido del equipo Microsoft Edge DevTools.  Vea los anuncios para probar nuevas características de la DevTools, extensiones de código de VS y mucho más.  Para estar al día de las características más recientes y las más recientes de las herramientas para desarrolladores, descargue los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] y [siga el equipo de Microsoft Edge DevTools en Twitter][EdgeDevToolsTwitterAccount].  

### Características de depuración de cuadrícula CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

El equipo de DevTools de Microsoft Edge está colaborando con el equipo de Chrome DevTools y la comunidad de cromo para agregar nuevas características de depuración de cuadrícula CSS a DevTools.  Ahora puede mostrar los números de línea de la cuadrícula, los huecos de cuadrícula y las líneas de cuadrícula extendidas como una superposición en la página.  Además, pronto estarán disponibles otras mejoras en las herramientas de cuadrícula.  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Características de depuración de cuadrícula CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   Características de depuración de cuadrícula CSS
:::image-end:::  

> [!NOTE]
> Para habilitar el experimento, vea [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla situada junto a **Habilitar nuevas características de depuración de la cuadrícula CSS**.  
> 
> Para probar el experimento con un ejemplo, consulta [ejemplo de planeación de cuadrícula CSS][CodepenRachelweilYzwBzKM].  

[#1047356][CR1047356] de problemas de cromo  

### Editar y reproducir solicitudes con la consola de red  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Ahora puede usar **Editar y reproducir** en las solicitudes en el [registro de red][DevtoolsNetworkIndexLogActivity] con la consola de **red**.  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Editar y reproducir una solicitud en el NetworkLog con la consola de red" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   Editar y reproducir una solicitud en el [NetworkLog][DevtoolsNetworkIndexLogActivity] con la **consola de red**  
:::image-end:::  

Un panel nuevo, la **consola de red** se abre en el [cajón de DevTools][DevtoolsCustomizeIndexDrawer] y se rellena automáticamente con información para la solicitud HTTP.  Para ver la respuesta devuelta desde el servidor, edite \ (si es necesario \) y seleccione **Enviar**.  

También puede usar la **consola de red** para crear y enviar solicitudes HTTP directamente desde el DevTools.  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Panel de consola de red" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   Panel de **consola de red**  
:::image-end:::  

> [!TIP]
> Para ver la **consola de red** en el panel \ (superior \) en lugar del [alimentador de DevTools][DevtoolsCustomizeIndexDrawer], consulte movimiento de [herramientas entre paneles](#move-tools-between-panels).  

> [!NOTE]
> Para habilitar el experimento, consulte [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla que se encuentra junto a **Habilitar la consola de red**.  
> 
> Abra el [registro de red][DevtoolsNetworkIndexLogActivity], abra el menú contextual \ (haga clic con el botón derecho del ratón \) y seleccione **Editar y reproducir**.  

[#1093687][CR1093687] de problemas de cromo  

### Eventos de respondWith de trabajo de servicio en la pestaña intervalos  

La ficha **intervalos** del panel **red** ahora incluye `respondWith` eventos de trabajo de servicio.  El `respondWith` evento de trabajo de servicio muestra la duración desde el momento en que el `fetch` controlador de eventos de trabajo de servicio comienza a ejecutarse hasta el momento en que `respondWith` se liquida la promesa del `fetch` controlador.  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="El evento de trabajo del servicio respondWith en la ficha intervalos del panel red" lightbox="../../media/2020/06/timing-tab.msft.png":::
   El `respondWith` evento de trabajo de servicio en la pestaña **intervalos** del panel **red**  
:::image-end:::  

Expanda la **respuesta recibida** para ver información adicional de la `fetch` respuesta como `CacheStorageCacheName` , `serviceWorkerResponseSource` y `ResponseTime` .  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Expandir respuesta recibida para ver información adicional de la respuesta de Fetch" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   Expandir **respuesta recibida** para ver información adicional de la `fetch` respuesta  
:::image-end:::  

[#1066579][CR1066579] de problemas de cromo  

### Comentarios sobre webhint en el panel problemas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

[webhint][WebhintMain] es una herramienta de código abierto que proporciona comentarios en tiempo real sobre accesibilidad, compatibilidad entre exploradores, seguridad, rendimiento, PWAs y otros problemas comunes de desarrollo web de los sitios Web.  Ahora puede ver comentarios sobre webhint en el panel [problemas][DevtoolsIssues] .  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Comentarios sobre webhint en el panel problemas" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   Comentarios sobre webhint en el panel problemas  
:::image-end:::  

> [!NOTE]
> Para habilitar el experimento, vea [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla que se encuentra junto a **Habilitar webhint**.  
> 
> Abra el panel [problemas][DevtoolsIssues] para ver los comentarios de webhint.  

[#1070378][CR1070378] de problemas de cromo  

### Mover herramientas entre paneles  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Normalmente, las herramientas, como **los elementos** y la **red** , solo se pueden abrir en el panel \ (parte superior \) de DevTools.  De forma similar, las herramientas, como la **vista 3D** y los **problemas** , solo se pueden abrir en el panel del cajón \ (inferior \) de DevTools.  Ahora puede personalizar el diseño de DevTools moviendo las herramientas entre los paneles superior e inferior.  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Mover pestañas entre paneles" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   Mover pestañas entre paneles  
:::image-end:::  

> [!NOTE]
> Para habilitar el experimento, vea [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOn] y seleccione la casilla junto a **habilitar soporte técnico para mover las tabulaciones entre los paneles**.  

[#897944][CR897944] de problemas de cromo  

### Información sobre herramientas de iniciador mejorada en el panel red  

En Microsoft Edge 83 y 84, información sobre herramientas para la columna Initiator, que muestra la causa de la solicitud de recursos, en el [registro de red][DevtoolsNetworkIndexLogActivity] que se muestra con una barra de desplazamiento horizontal.  Solo pudimos ver la pila de llamadas que inició la solicitud desplazándose horizontalmente en la información sobre herramientas.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Información sobre herramientas de iniciador en Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   Información sobre herramientas de iniciador en Microsoft Edge 84  
:::image-end:::  

A partir de Microsoft Edge 85, ahora puedes ver la pila de llamadas de iniciador en la información sobre herramientas sin tener que desplazarse horizontalmente.  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Información sobre herramientas de iniciador en Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   Información sobre herramientas de iniciador en Microsoft Edge 85
:::image-end:::  

[#1069404][CR1069404] de problemas de cromo  

## Anuncios del proyecto de cromo  

En las siguientes secciones se anuncian características adicionales disponibles en Microsoft Edge 85 que se han contribuido al proyecto de código abierto.  

### Edición de estilos para marcos CSS-en-JS  

El panel **estilos** ahora tiene mejor compatibilidad para editar los estilos que se crearon con las API del [modelo de objetos CSS (CSSOM)][CsswgDraftsCssom] .  Muchos marcos y bibliotecas CSS-en-JS usan las API de CSSOM en el capó para construir estilos.  

Ahora puede editar los estilos agregados en JavaScript con [hojas de estilo construyebles][WicgConstructStylesheet].  Las hojas de estilo creativas son una nueva forma de crear y distribuir estilos reutilizables al usar la [sombra de Dom][MdnShadowDom].  

Por ejemplo, los `h1` estilos agregados con `CSSStyleSheet` \ (API de CSSOM \) no se podían modificar anteriormente.  Ahora los estilos se pueden editar en el panel **estilos** .  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Cambiar la propiedad Background de los estilos H1 agregados con CSSStyleSheet de rosa a lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   Cambiar la `background` propiedad de los `h1` estilos agregados con `CSSStyleSheet` from `pink` a `lightblue` .
:::image-end:::  

Proporciona a esta característica una prueba con un [ejemplo que usa CSS-in-JS][CodepenZoherghadyaliAbdgrpz].

[#946975][CR946975] de problemas de cromo  

### Lighthouse 6 en el panel de Lighthouse  

El panel de **Lighthouse** ahora se ejecuta Lighthouse 6.  Para obtener una lista completa de todos los cambios, consulte las notas de la [versión v 6.0.0][GithubGoogleChromeLighthouse600].  

Lighthouse 6,0 introduce tres nuevas métricas en el informe: pintura con el contenido más grande \ (LCP \), turno de distribución acumulativa \ (CLS \) y tiempo de bloqueo total \ (TBT \).  

La fórmula de puntuación de rendimiento también se ha recargado para reflejar mejor la experiencia de carga del usuario.  

[#772558][CR772558] de problemas de cromo  

#### Primer desuso de pintura significativo  

La primera pintura significativa \ (FMP \) está en desuso en Lighthouse 6,0.  FMP también se ha eliminado del panel **rendimiento** .  La **mayor pintura** con el contenido es el reemplazo recomendado para FMP.  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

[#1096008][CR1096008] de problemas de cromo  

### Compatibilidad con las nuevas características de JavaScript  

DevTools ahora es una mejor compatibilidad para algunas de las características más recientes del lenguaje JavaScript.  

:::row:::
   :::column span="1":::
      Finalización automática de sintaxis de [encadenamiento opcional][V8DevOptionalChaining]  
   :::column-end:::
   :::column span="2":::
      La finalización automática de la propiedad en la **consola** ahora admite la sintaxis de encadenamiento opcional; por ejemplo,  `name?.` ahora funciona además de `name.` y `name[` .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Resaltado de sintaxis para [campos privados][V8DevClassFieldsPrivate]  
   :::column-end:::
   :::column span="2":::
      Ahora, los campos de clase privados se resaltan correctamente y se resaltan en el panel **fuentes** .  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Resaltado de sintaxis para el [operador de fusión con valores nulos][V8DevNullishCoalescing]
   :::column-end:::
   :::column span="2":::
      Ahora DevTools correctamente: imprime el operador de fusión de NULL en el panel **fuentes** .  
   :::column-end:::
:::row-end:::  

Problemas de cromo [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]  

### Advertencias de nuevo acceso directo a la aplicación en el panel manifiesto  

Los **accesos directos a aplicaciones** ayudan a los usuarios a iniciar rápidamente las tareas comunes o recomendadas dentro de una aplicación Web.  

<!--todo: add App shortcuts when section is live  -->  

En el panel **manifiesto** ahora se muestran advertencias para las siguientes condiciones.  

* Los iconos de acceso directo de la aplicación son menores que 96 píxeles  
* Los iconos de acceso directo de la aplicación y los iconos de manifiesto no son cuadrados \ (porque los iconos se ignoran \)  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Advertencias de acceso directo a la aplicación" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   Advertencias de acceso directo a la aplicación  
:::image-end:::  

[#955497][CR955497] de problemas de cromo  

### Visualización coherente del panel calculado  

El panel **calculado** del panel **elementos** se muestra ahora de forma coherente en todos los tamaños de la ventanilla.  Anteriormente el panel **calculado** se combinó en el panel **estilos** cuando el ancho de la ventanilla de DevTools era estrecho.  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="El panel calculado se muestra de forma coherente como un panel independiente incluso cuando el DevTools es estrecho." lightbox="../../media/2020/06/computed-pane.msft.png":::
   El panel **calculado** se muestra de forma coherente como un panel independiente incluso cuando el DevTools es estrecho.
:::image-end:::  

[#1073899][CR1073899] de problemas de cromo  

### Desplazamientos de código de bytes para archivos webassembly  

DevTools ahora usa desplazamientos de código de byte para mostrar los números de línea de WASM desensamblador.  
Los números de línea marcan más claramente que estás buscando datos binarios y son más coherentes con el modo en que el tiempo de ejecución de WASM hace referencia a ubicaciones.  

[#1071432][CR1071432] de problemas de cromo  

### Copia y corte de línea en el panel orígenes  

Al realizar una operación de copiar o cortar sin selección en el [Editor del panel orígenes][DevtoolsSourcesEditCssJavascript], DevTools copia o corta la línea de contenido actual.  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Con el cursor al final de la línea 5, copiando toda la línea desde pen.js en el DevTools y pegando en VS" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   Con el cursor al final de la línea 5, copiando toda la línea desde **pen.js** en el DevTools y pegando en [vs Code][VSCode].
:::image-end:::  

[#800028][CR800028] de problemas de cromo

### Actualizaciones de configuración de consola  

#### Desagrupar los mismos mensajes de consola  

El botón de alternancia **similar** en la configuración de la consola se aplica a los mensajes duplicados.  Anteriormente se acaba de aplicar a mensajes similares.  

Por ejemplo, anteriormente, DevTools no desagrupaba los `hello` mensajes aunque el **grupo es similar** .  Ahora, los `hello` mensajes están desagrupados.  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Cuando agrupar similares está desactivado, los mensajes de saludo no se agrupan" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   Cuando **agrupar similares** está desactivado, los `hello` mensajes no se agrupan.
:::image-end:::  

Proporciona a esta característica una prueba con un [ejemplo que envía mensajes duplicados a la consola][CodepenZoherghadyaliZyrjgdJ].  

[#1082963][CR1082963] de problemas de cromo  

### Conservar la configuración de solo contexto seleccionada  

La configuración de **contexto seleccionada solo** en la configuración de la consola se conserva.  Anteriormente, la configuración se restableció cada vez que cerraste y reabros DevTools.  El cambio hace que el ajuste del comportamiento sea coherente con otras opciones de configuración de la consola.  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Configuración de contexto seleccionado únicamente" lightbox="../../media/2020/06/selected-context.msft.png":::
   Configuración de **contexto seleccionado únicamente**  
:::image-end:::  

[#1055875][CR1055875] de problemas de cromo  

### Actualizaciones del panel de rendimiento  

#### Información de caché de compilación de JavaScript en el panel rendimiento  

La información de la [caché de compilación de JavaScript][V8DevCodeCaching] se muestra ahora siempre en la pestaña Resumen del panel rendimiento.  Anteriormente, DevTools no mostraba nada relacionado con el almacenamiento en caché del código si no se produjera el almacenamiento en caché de código.  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Información de caché de compilación de JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   Información de caché de compilación de JavaScript  
:::image-end:::  

[#912581][CR912581] de problemas de cromo  

#### Alineación de la navegación en el panel rendimiento  

El panel de **rendimiento** que se usa para mostrar las horas en las reglas en función del inicio de la grabación.  Ahora se ha cambiado el intervalo de tiempo para las grabaciones en las que el usuario navega, donde DevTools ahora muestra las horas relacionadas con la navegación.  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Alinear los intervalos de navegación en el panel rendimiento" lightbox="../../media/2020/06/nav-timing.msft.png":::
   Alinear los intervalos de navegación en el panel **rendimiento**  
:::image-end:::  

Las horas de `DOMContentLoaded` , primera pintura con control de contenido y los mayores eventos de pintura con contenido se actualizan para que sean relativas al inicio de la navegación, lo que significa que los intervalos coinciden con los intervalos que informaron `PerformanceObserver` .  

[#974550][CR974550] de problemas de cromo  

### Nuevos iconos para puntos de interrupción, puntos de interrupción condicionales y logpoints  

El panel **orígenes** tiene nuevos diseños para puntos de interrupción, puntos de interrupción condicionales y logpoints.  Los puntos de interrupción están representados por un círculo rojo, como [vs Code][VSCode] y [Visual Studio][VS].  Se agregan iconos para diferenciar los puntos de interrupción y logpoints.  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Puntos de interrupción" lightbox="../../media/2020/06/breakpoints.msft.png":::
   Puntos de interrupción  
:::image-end:::  

[#1041830][CR1041830] de problemas de cromo  

## Descargar los canales de Microsoft Edge Preview  

Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo) | Microsoft docs"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón-personalizar Microsoft Edge DevTools | Microsoft docs"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft docs"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Buscar y solucionar problemas con la herramienta de problemas de Microsoft Edge DevTools | Microsoft docs"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Información general del panel editar CSS y JavaScript | Microsoft docs"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar actividad de red: inspeccionar actividad de red en Microsoft Edge DevTools | Microsoft docs"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Edición de estilos para marcos CSS-en-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Enviar mensajes duplicados a la consola | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Ejemplo de programador de cuadrícula CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"  

[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la última versión de Lighthouse | Errores de cromo"  
[CR800028]: https://crbug.com/800028 "El método abreviado de línea duplicado en el editor herramientas de desarrollo no funciona después de la actualización Chrome | Errores de cromo"  
[CR912581]: https://crbug.com/912581 "Exponga qué scripts se almacenaron en caché de código en V8 en DevTools/acerca de: Tracing | Errores de cromo"  
[CR946975]: https://crbug.com/946975 "La barra lateral estilos de DevTools no funciona con hojas de estilos construidas | Errores de cromo"  
[CR955497]: https://crbug.com/955497 "Menú contextual del icono de la aplicación para PWAs | Errores de cromo"  
[CR974550]: https://crbug.com/974550 "La métrica entre el panel de rendimiento y performanceObserver | Errores de cromo"  
[CR1041830]: https://crbug.com/1041830 "Mejorar los colores de los puntos de interrupción | Errores de cromo"  
[CR1055875]: https://crbug.com/1055875 "El valor de la configuración de la consola solo de contexto seleccionado no se conserva después de cerrar y volver a abrir las herramientas de desarrollo | Errores de cromo"  
[CR1066579]: https://crbug.com/1066579 "DevTools: Mostrar la escala de tiempo de captura de ServiceWorkers por solicitud en el panel red | Errores de cromo"  
[CR1071432]: https://crbug.com/1071432 "Experiencia de desarrollador básica de WASM | Errores de cromo"  
[CR1073899]: https://crbug.com/1073899 "La pestaña de estilo calculado desaparece en modo de respuesta | Errores de cromo"  
[CR1073903]: https://crbug.com/1073903 "DevTools: el resaltado de sintaxis no funciona con los campos privados | Errores de cromo"  
[CR1082963]: https://crbug.com/1082963 "No se puede deshabilitar el grupo de consola de mensajes similares comportamiento | Errores de cromo"  
[CR1083214]: https://crbug.com/1083214 "ACORN no admite el encadenamiento opcional | Errores de cromo"  
[CR1083797]: https://crbug.com/1083797 "Impresión con sangría dañada para la combinación nula | Errores de cromo"  
[CR1096008]: https://crbug.com/1096008 "Quitar FMP | Errores de cromo"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS/Flexbox/tables de CSS | Errores de cromo"  
[CR1093687]: https://crbug.com/1093687 "Herramienta crear y reproducir solicitudes de red sintéticas | Errores de cromo"  
[CR1070378]: https://crbug.com/1070378 "Integrar webhint en DevTools | Errores de cromo"  
[CR1069404]: https://crbug.com/1069404 "Las ventanas emergentes de widgets de [dev Tools] son demasiado limitadas | Errores de cromo"  
[CR897944]: https://crbug.com/897944 "Paneles de devtool arrastrables | Errores de cromo"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/Lighthouse | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nuevo problema: MicrosoftDocs/Edge-Developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Usar DOM de sombra | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canales de Microsoft Edge Preview"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Código de Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modelo de objetos CSS (CSSOM) | Borradores del editor del grupo de trabajo CSS W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publicar un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Campos de clase privados: campos de clase pública y privada | V8. Desarrolladores"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Almacenamiento en caché de código para desarrolladores de JavaScript | V8. Desarrolladores"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Fusión nula | V8. Desarrolladores"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Encadenamiento opcional | V8. Desarrolladores"  

[WebhintMain]: https://webhint.io "sugerencia"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objetos de hoja de estilos que se construyen | Autoincubadora CG"

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
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/06/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
