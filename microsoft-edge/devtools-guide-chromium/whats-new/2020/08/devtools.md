---
description: Combina los métodos abreviados de teclado Visual Studio Code, emular Surface Duo y Samsung Galaxy Fold, mejoras de superposición de cuadrícula CSS y mucho más.
title: Novedades de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ec2219e9ebdd5d79c61bcaa813f7784246b1f5d0
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564948"
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
# <a name="whats-new-in-devtools-microsoft-edge-86"></a>Novedades de DevTools (Microsoft Edge 86)  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a>Anuncios del equipo Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### <a name="match-keyboard-shortcuts-in-devtools-to-visual-studio-code"></a>Coincidencia de métodos abreviados de teclado en DevTools para Visual Studio Code  

En Microsoft Edge 86, puede hacer coincidir los métodos abreviados de teclado de DevTools con los accesos directos de [Microsoft Visual Studio Code][VisualStudioCodeMain].  

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Coincida con los métodos abreviados de teclado en DevTools para Visual Studio Code" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Coincida con los métodos abreviados de teclado en DevTools para Visual Studio Code  
:::image-end:::  

Para activar esta característica, vaya a [Personalizar métodos abreviados de teclado en el Microsoft Edge DevTools][DevtoolsCustomizeShortcuts].  

Por ejemplo, el método abreviado de teclado para pausar o continuar ejecutando un script [en Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] es `F5` .  Con el valor **preestablecido DevTools (predeterminado),** ese mismo acceso directo en DevTools es , pero cuando elige el valor preestablecido `F8` **Visual Studio Code,** ese acceso directo ahora también es `F5` .  

Chromium problema [#174309][CR174309]  

### <a name="emulate-surface-duo-and-samsung-galaxy-fold"></a>Emular Surface Duo y Samsung Galaxy Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Ahora puedes probar el aspecto de tu sitio web o aplicación en dos nuevos dispositivos: [Surface Duo][MicrosoftSurfaceDevicesDuo] y Samsung [Galaxy Fold][SamsungMobileGalaxyFold] en Microsoft Edge.  

Para ayudar a mejorar su sitio web o aplicación para dispositivos plegables y de pantalla doble, use las siguientes características al [emular el dispositivo][DevtoolsDeviceModeIndex].  

*   [Expandir][DevtoolsDeviceModeDualScreenAndFoldables], que es cuando su sitio web \(o aplicación\) se extiende por las dos pantallas.
*   [Representación de la unión][DualScreenIntroductionHowWorkSeam], que es el espacio entre las dos pantallas.
*   Habilitar las API experimentales de plataforma web para tener acceso a la nueva característica de pantalla multimedia [CSS][DualScreenWebCssMediaSpanning] y a la [API getWindowSegments de JavaScript.][DualScreenWebJavascriptGetwindowsegments]  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Emulación de dispositivos para Surface Duo" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Emulación de dispositivos para Surface Duo  
:::image-end:::  

Para activar esta característica experimental, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y elija la casilla situada junto a **Emulation: Support dual screen mode**.  

Para obtener más información acerca de esta característica, vaya a Emular dispositivos de pantalla doble y plegables [en Microsoft Edge DevTools][DevtoolsDeviceModeDualScreenAndFoldables].  

Chromium problema: [#1054281][CR1054281]  

### <a name="css-grid-overlay-improvements-and-new-experimental-grid-features"></a>Mejoras de superposición de cuadrícula CSS y nuevas características de cuadrícula experimental  

Gracias por los comentarios positivos sobre las superposiciones de cuadrícula CSS mejoradas.  Las superposiciones de cuadrícula CSS ahora están habilitadas de forma predeterminada y no requieren que actives un experimento.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Superposición de cuadrícula CSS para elemento de artículo" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Superposición de cuadrícula CSS para `article` elemento  
:::image-end:::  

> [!NOTE]
> Para obtener más información acerca de las superposiciones de cuadrícula, vaya a [Características de depuración de][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]cuadrícula CSS .  

El Microsoft Edge de DevTools y el equipo de Chrome DevTools colaboran en características adicionales.  Las nuevas características incluyen varias superposiciones que son persistentes y configurables desde un nuevo panel **Diseño** de la **herramienta** Elementos.  

Para activar esta característica experimental, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y elija la casilla situada junto a Habilitar nuevas características de depuración de cuadrícula **CSS (opciones**de configuración disponibles en el panel de la barra lateral Diseño en Elementos después del reinicio).  

Para obtener más información acerca de esta característica, vaya a [Inspeccionar cuadrícula CSS en Microsoft Edge DevTools][DevtoolsCssGrid].  

Chromium problema: [#1047356][CR1047356]  

### <a name="table-copied-from-the-console-preserves-formatting"></a>La tabla copiada desde la consola conserva el formato  

En Microsoft Edge 85 o versiones anteriores, se perdió el formato de una `console.table` copiada.  Si copió el resultado [][DevtoolsConsoleApiTable] de la API de consola de la tabla y la pega, solo se guardó el texto de la tabla.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Resultado de la API de consola de tabla Microsoft Edge 85 o versiones anteriores" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Salida de la API de consola Microsoft Edge 85 o versiones anteriores  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="table Console API output from Microsoft Edge 85 or earlier pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Resultado de la API de consola Microsoft Edge 85 o versiones anteriores pegadas en Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

En Microsoft Edge 86 o posterior, al copiar una tabla de la **consola,** el formato se conserva ahora.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="resultado de la API de consola de tabla Microsoft Edge 86 o posterior" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Salida de la API de consola Microsoft Edge 86 o posterior  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="table Console API output from Microsoft Edge 86 or later pasted into Visual Studio Code" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Salida de la API de consola Microsoft Edge 86 o posterior pegada en Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium problema: [#1115011][CR1115011]  

### <a name="source-order-viewer-for-easier-accessibility-testing"></a>Visor de pedidos de origen para pruebas de accesibilidad más fáciles  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

La nueva aplicación auxiliar de accesibilidad muestra el orden de los elementos en el origen.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Activar Mostrar orden de origen" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Activar **Mostrar orden de origen**  
:::image-end:::  

Esta característica facilita la prueba de la forma en que los usuarios del lector de pantalla y el teclado experimentan su sitio web o aplicación.  Los lectores de pantalla y la navegación por teclado dependen de que el contenido se coloque en un orden determinado en el código fuente de su sitio web o aplicación, de modo que coincida con la página representada.  El Visor de pedidos de origen muestra posibles diferencias de orden entre la página representada y el código fuente.  

Para activar esta característica experimental, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y elija la casilla situada junto a **Habilitar**visor de pedidos de origen .  

Para obtener más información acerca de este experimento, vaya a [Visor de pedidos de origen][DevtoolsExperimentalFeaturesSourceOrderViewer].  

Chromium problema: [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Microsoft Edge DevTools in Traditional Chinese" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Microsoft Edge DevTools in Japanese" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### <a name="highlight-all-search-results-in-elements-tool"></a>Resaltar todos los resultados de búsqueda en la herramienta Elementos  

En Microsoft Edge 84 y 85, no se resaltó el primer resultado de búsqueda en la **herramienta** Elementos.  Los resultados de búsqueda restantes se resaltaron correctamente.  

Gracias por enviar sus comentarios y ayudar a mejorar Chromium.  Sus comentarios revelaron el [problema #1103316][CR1103316] en el proyecto de código Chromium código abierto.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Primer resultado de búsqueda resaltado en el panel Elementos Microsoft Edge 84 o posterior" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Primer resultado de búsqueda resaltado en **la herramienta Elementos** en Microsoft Edge 84 o posterior  
:::image-end:::  

El problema ahora se soluciona en todas las versiones de Microsoft Edge.  

Chromium problema: [#1103316][CR1103316]  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-media-tool"></a>Nueva herramienta multimedia  

Ahora DevTools muestra información de reproductores multimedia en la herramienta [Media][DevtoolsMediaPanelIndex].  

Para abrir la nueva **herramienta Multimedia,** complete el siguiente paso.  

1.  Elija **Personalizar y controlar DevTools** \( `...` \) > Más herramientas ****  >  **Multimedia**.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Nueva herramienta multimedia" lightbox="../../media/2020/08/media-panel.msft.png":::
       Nueva **herramienta multimedia**  
    :::image-end:::  

Antes de la nueva **herramienta Multimedia** en DevTools, la información de registro y depuración sobre los reproductores de vídeo se encontraba en la configuración **Reproductores recientes.**  Para abrir la configuración **Jugadores recientes,** vaya a `edge://media-internals` y elija la herramienta **Jugadores.**  

Vea contenido dinámico e inspeccione los posibles problemas más rápidamente, incluidos los ejemplos siguientes.  

*   ¿Por qué se descartan fotogramas?  
*   ¿Por qué JavaScript interactúa con el jugador de forma inesperada?  

### <a name="capture-node-screenshots-using-the-elements-tool-context-menu"></a>Capturar capturas de pantalla de nodo con el menú contextual de la herramienta Elementos  

Ahora puede capturar capturas de pantalla de nodo mediante el menú contextual de la **herramienta** Elementos.  

Por ejemplo, para realizar una captura de pantalla de la tabla de contenido, mantenga el mouse en el elemento, abra el menú contextual \(hacer clic con el botón secundario\) y seleccione Capturar captura de pantalla **del nodo**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Capturar capturas de pantalla de nodo" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Capturar capturas de pantalla de nodo  
:::image-end:::  

Chromium problema: [#1100253][CR1100253]  

### <a name="issues-tool-updates"></a>Problemas de actualizaciones de herramientas  

La barra de advertencia Problemas de la **herramienta Consola** ahora se reemplaza por un mensaje normal.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Problemas en el mensaje de consola" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Problemas en el mensaje de consola  
:::image-end:::  

Los problemas de cookies de terceros ahora están ocultos de forma predeterminada en la **herramienta** Problemas.  Habilite la nueva **casilla Incluir problemas de cookies de** terceros para ver los problemas.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Casilla de verificación problemas de cookies de terceros" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   Casilla de verificación problemas de cookies de terceros  
:::image-end:::  

Chromium: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### <a name="emulate-missing-local-fonts"></a>Emular fuentes locales que faltan  

Abra la [herramienta de representación y][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] use la nueva característica Deshabilitar fuentes **locales** para emular los orígenes que faltan en `local()` las `@font-face` reglas.  

Por ejemplo, cuando la fuente está instalada en el dispositivo y la regla la usa como fuente, Microsoft Edge el archivo de fuente `Rubik` `@font-face src` local del `local()` dispositivo.  

Cuando **se habilita Deshabilitar fuentes** locales, DevTools omite las fuentes y captura cada una de la `local()` red.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Emular fuentes locales que faltan" lightbox="../../media/2020/08/disable-font.msft.png":::
   Emular fuentes locales que faltan  
:::image-end:::  

Si usa dos copias diferentes de la misma fuente durante el desarrollo, como los ejemplos siguientes.  

*   Una fuente local para las herramientas de diseño.  
*   Una fuente web para el código.  

Use **Deshabilitar fuentes locales** para facilitar la realización de las siguientes tareas.  

*   Depurar y medir el rendimiento de carga y optimización de fuentes web.  
*   Compruebe la precisión de las reglas `@font-face` CSS.  
*   Descubra las diferencias entre las versiones locales instaladas en el dispositivo y una fuente web.  

Chromium problema: [#384968][CR384968]  

### <a name="emulate-inactive-users"></a>Emular usuarios inactivos  

La [API de detección de][WebDevIdleDetection] inactividad permite a los desarrolladores detectar usuarios inactivos y reaccionar en los cambios de estado de inactividad.  Ahora puede usar DevTools para emular los **** cambios de estado de inactividad en la herramienta Sensores tanto para el estado de usuario como para el estado de pantalla en lugar de esperar a que cambie el estado de inactividad real.  Puede abrir la herramienta **Sensores** desde el [cajón][DevtoolsCustomizeIndexDrawer].  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Emular usuarios inactivos" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Emular usuarios inactivos  
:::image-end:::  

Chromium problema: [#1090802][CR1090802]  

### <a name="emulate-prefers-reduced-data"></a>Emular prefers-reduced-data  

> [!NOTE]
> En Microsoft Edge 86, para habilitar esta característica, vaya a y active la marca características de plataforma `edge://flags#enable-experimental-web-platform-features` **web experimental.**  La opción de emulación solo se muestra si la marca está habilitada.  

La [consulta multimedia prefers-reduced-data][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] detecta las preferencias de contenido del usuario para los datos reducidos.  Si se selecciona, el usuario recibe contenido de página alternativo que usa menos datos.  

Ahora puede usar DevTools para emular la `prefers-reduced-data` consulta multimedia.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Emular prefers-reduced-data" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Emular prefers-reduced-data  
:::image-end:::  

Chromium problema: [#1096068][CR1096068]  

### <a name="support-for-new-javascript-features"></a>Compatibilidad con nuevas características de JavaScript  

DevTools ahora admite mejor las siguientes características del lenguaje JavaScript.  

| Característica de lenguaje JavaScript | Detalles |  
|:--- |:--- |  
| [Operadores de asignación lógica][V8FeaturesLogicalAssignment] | DevTools ahora admite la asignación lógica con los `&&=` nuevos operadores , y en las herramientas `||=` `??=` **Consola** **y** Orígenes.  |  
| Separadores [numéricos de impresión bastante][V8FeaturesNumericSeparators] | Ahora DevTools imprime correctamente los separadores numéricos en la **herramienta** Orígenes.  |  

Chromium: [1086817][CR1086817], [1080569][CR1080569]  

### <a name="lighthouse-62-in-the-lighthouse-panel"></a>Faro 6.2 en el panel Faro  

Ahora, **la herramienta Lighthouse** está ejecutando Lighthouse 6.2.  Para obtener una lista completa de los cambios, vaya a las notas [de la versión de Lighthouse][GithubGooglechromeLighthouseV620].  

Chromium problema: [#772558][CR772558]  

### <a name="deprecation-of-other-origins-listing-in-the-service-workers-pane"></a>Desuso de la descripción de otros orígenes en el panel Trabajadores de servicio  

DevTools ahora proporciona un vínculo desde el panel **Trabajadores** de servicio**\(** Herramienta de aplicación > Panel de trabajadores **de** servicio\) para ver la lista completa de trabajadores de servicio de otros orígenes.  Para obtener acceso a la lista sin abrir DevTools, vaya a `edge://service-worker-internals/?devtools` .  

Anteriormente, DevTools muestra una lista anidada en el panel **DevTools** > **DevTools.**  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Vínculo a otros orígenes" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Vínculo a otros orígenes  
:::image-end:::  

Chromium problema: [#807440][CR807440]  

### <a name="show-coverage-summary-for-filtered-items"></a>Mostrar resumen de cobertura para elementos filtrados  

DevTools ahora vuelve a calcular y mostrar un resumen de la información de cobertura dinámicamente.  La pantalla dinámica se desencadena cuando se aplican filtros en la [herramienta Cobertura.][DevtoolsCoverageIndex]  Antes de **que la herramienta** Cobertura siempre mostrara un resumen de toda la información de cobertura.  

En la primera de las siguientes figuras, el resumen se muestra inicialmente y, en la segunda de las siguientes cifras, el resumen se muestra después de aplicar el filtrado `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` CSS.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Resumen de cobertura" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Resumen de cobertura  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Resumen de cobertura para elementos filtrados" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Resumen de cobertura para elementos filtrados  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Chromium problema: [#1061385][CR1090802]  

### <a name="new-frame-details-view-in-application-panel"></a>Nueva vista detalles del marco en el panel Aplicación  

DevTools ahora muestra una vista detallada para cada fotograma.  Para acceder a él, elija un marco en el **menú Marcos** de la **herramienta** Aplicación.  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Nueva vista detallada para un marco en el panel Aplicación" lightbox="../../media/2020/08/frame-details.msft.png":::
   Nueva vista detallada para un marco en **la herramienta Aplicación**  
:::image-end:::  

Chromium problema: [#1093247][CR1093247]  

#### <a name="frame-details-for-opened-windows"></a>Detalles del marco para ventanas abiertas  

Las ventanas abiertas y las ventanas emergentes ahora también se muestran debajo del árbol de marcos.  La vista detallada de las ventanas abiertas incluye información de seguridad adicional.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Nueva vista detallada de fotogramas para ventanas abiertas" lightbox="../../media/2020/08/window-opener.msft.png":::
   Nueva vista detallada de fotogramas para ventanas abiertas  
:::image-end:::  

Chromium problema: [#1107766][CR1107766]  

#### <a name="security-and-isolation-information"></a>Información de seguridad y aislamiento  

Contexto seguro, [Cross-Origin-Embedder-Policy (COEP)][WebDevCoopCoep]y [Cross-Origin-Opener-Policy (COOP)][WebDevCoopCoep] ahora se muestran en los detalles del marco.  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Información de seguridad y aislamiento" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Información de seguridad y aislamiento  
:::image-end:::  

En el futuro, el Microsoft Edge de DevTools y el equipo de Chrome DevTools planean agregar más información de seguridad a los detalles del marco.  

Chromium problema: [#1051466][CR1051466]  

### <a name="elements-and-network-panel-updates"></a>Actualizaciones de elementos y panel de red  

#### <a name="accessible-color-suggestion-in-the-styles-pane"></a>Sugerencia de color accesible en el panel Estilos  

DevTools ahora proporciona sugerencias de color para texto de contraste de color bajo.  

En el ejemplo siguiente, `h1` tiene texto de contraste bajo.  Para corregirlo, abra el selector de color de la `color` propiedad en el panel **Estilos.**  Después de expandir la **sección Relación de contraste,** DevTools proporciona sugerencias de color AAA y AA.  Elija el color sugerido para aplicar el color.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="El selector de colores sugiere sugerencias de color AAA y AA" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   El selector de colores sugiere sugerencias de color AAA y AA  
:::image-end:::  

Chromium problema: [#1093227][CR1093227]  

#### <a name="reinstate-properties-pane-in-the-elements-panel"></a>Reinstaurar el panel Propiedades en el panel Elementos  

El **panel Propiedades** ha vuelto.  Estaba en [desuso en Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  El Microsoft Edge de DevTools y el equipo de Chrome DevTools están planeando mejoras para inspeccionar las propiedades de los elementos.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Panel Propiedades en el panel Elementos" lightbox="../../media/2020/08/properties-pane.msft.png":::
   **Panel Propiedades** de la **herramienta** Elementos  
:::image-end:::  

Chromium problema:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Human-readable `X-Client-Data` header values" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### <a name="autocomplete-custom-fonts-in-the-styles-pane"></a>Autocompletar fuentes personalizadas en el panel Estilos  

Las caras de fuente importadas ahora se agregan a la lista de autocompletar CSS al editar la `font-family` propiedad en el panel **Estilos.**  

Por ejemplo, si `monospace` es una fuente personalizada instalada en el equipo local, se muestra en la lista de finalización de CSS.  En versiones anteriores de Microsoft Edge, no se mostró la fuente.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Autocompletar fuentes personalizadas" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Autocompletar fuentes personalizadas  
:::image-end:::  

Chromium problema: [#1106221][CR1106221]  

#### <a name="consistently-display-resource-type-in-network-panel"></a>Mostrar de forma coherente el tipo de recurso en el panel Red  

Ahora DevTools muestra de forma coherente el mismo tipo de recurso que la solicitud de red original y se anexa al valor de columna Tipo cuando se produce el redireccionamiento `/ Redirect` \(Código de estado HTTP 302\). ****  

Anteriormente, DevTools cambió el tipo a `Other` veces.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Mostrar tipo de recurso de redireccionamiento" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Mostrar tipo de recurso de redireccionamiento  
:::image-end:::  

Chromium problema: [#997694][CR997694]  

#### <a name="clear-buttons-in-the-elements-and-network-tools"></a>Borrar botones en las herramientas Elementos y Red  

Los cuadros de texto siguientes ahora tienen **botones** Borrar.  

*   Los cuadros de texto de filtro del panel **Estilos** y **la herramienta Red.**  
*   Cuadro de texto de búsqueda DOM de la **herramienta** Elementos.  

Elija el **botón** Borrar para quitar cualquier texto escrito.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Borrar botones en los paneles Elementos" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Borrar botones en las **herramientas de** elementos  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Borrar botones en los paneles de red" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Borrar botones en las  **herramientas de** red  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Chromium problema: [#1067184][CR1067184]  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si está en Windows o macOS, considere la posibilidad de usar los canales [Microsoft Edge vista previa][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Desuso del panel Propiedades en el panel Elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[DevtoolsConsoleApiTable]: ../../../console/api.md#table "tabla: referencia de api de consola | Microsoft Docs"  
[DevtoolsCoverageIndex]: ../../../coverage/index.md "Busque código JavaScript y CSS sin usar con la pestaña Cobertura en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: ../../../css/grid.md "Inspeccionar css grid en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: ../../../customize/index.md#drawer "Drawer: personalice Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalización de accesos rápidos de teclado en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsDeviceModeDualScreenAndFoldables]: ../../../device-mode/dual-screen-and-foldables.md "Emular dispositivos de pantalla doble y plegables en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: ../../../evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tool "Analizar el rendimiento de representación con la herramienta de representación: referencia de análisis de rendimiento | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features/index.md#enable-experimental-apis "Enable experimental APIs - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: .. /.. /.. /experimental-features/index.md#emulation-support-dual-screen-mode "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#source-order-viewer "Source Order Viewer - Experimental features | Microsoft Docs"
<!--  [DevtoolsExperimentalFeaturesTestOnFoldableDualScreenDevices]: ../../../experimental-features/index.md#test-on-foldable-and-dual-screen-devices "Test on foldable and dual-screen devices - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsMediaPanelIndex]: .. /.. /.. /media-panel/index.md "Ver y depurar la información de los reproductores multimedia | Microsoft Docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con la unión: introducción a los dispositivos de pantalla doble | Microsoft Docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de pantalla expandida para medios CSS para la detección de pantalla doble | Microsoft Docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "API de JavaScript de getWindowSegments para dispositivos de pantalla doble | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Visual Studio Code Métodos abreviados de teclado para Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "El nuevo Surface Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar los métodos abreviados de teclado o los enlaces de teclas | Chromium errores"
[CR384968]: https://crbug.com/384968 "Opción para omitir fuentes local() | Chromium errores"  
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la versión más reciente de | Chromium errores"  
[CR807440]: https://crbug.com/807440 "Chrome se bloquea con un gran número de SWs | Chromium errores"  
[CR997694]: https://crbug.com/997694 "Las solicitudes XHR con estado 302 no se muestran en el filtro \"xhr\" del panel de red | Chromium errores"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS Grid/Flexbox/Table | Chromium errores"  
[CR1051466]: https://crbug.com/1051466 "Admite la depuración de COOP/COEP en DevTools | Chromium errores"  
[CR1054281]: https://crbug.com/1054281 "Solicitud de característica: DevTools debe emular dispositivos de pantalla doble y | Chromium errores"  
[CR1067184]: https://crbug.com/1067184 "Solicitud de característica: botón Borrar filtro en elementos de & -> de filtro de estilos | Chromium errores"  
[CR1068116]: https://crbug.com/1068116 "☂ Panel de problemas de envío | Chromium errores"  
[CR1080569]: https://crbug.com/1080569 "acorn no admite operadores de asignación lógica | Chromium errores"  
[CR1080589]: https://crbug.com/1080589 "Clasificar problemas por terceros o por terceros | Chromium errores"  
[CR1086817]: https://crbug.com/1086817 "acorn no admite separadores numéricos | Chromium errores"  
[CR1090802]: https://crbug.com/1090802 "Simular cambios de estado de inactividad desde la API de detección de inactividad | Chromium errores"  
[CR1093227]: https://crbug.com/1093227 "DevTools: sugerir colores accesibles más cercanos | Chromium errores"  
[CR1093247]: https://crbug.com/1093247 "Mostrar información sobre fotogramas en el panel de aplicaciones | Chromium errores"  
[CR1094406]: https://crbug.com/1094406 "Los desarrolladores desean un visor de pedidos de origen para AT https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: admite la emulación de la característica multimedia prefers-reduced-data | Chromium errores"  
[CR1096481]: https://crbug.com/1096481 "Problemas de colocación de banner | Chromium errores"  
[CR1100253]: https://crbug.com/1100253 "Agregar acceso directo de nodo de captura de pantalla en el menú contextual elemento | Chromium errores"  
[CR1103316]: https://crbug.com/1103316 "La búsqueda de elementos no resuelveNode (texto resaltado, etc.) en la primera búsqueda de resultados | Chromium errores"  
[CR1103854]: https://crbug.com/1103854 "Desuso de los valores X-Client-Data en Developer Tools | Chromium errores"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: "Agregar fuentes importadas a la autocompleción de familia de fuentes en el panel Estilos | https://crbug.com/1106221 Chromium errores"  
[CR1107766]: "Mostrar información sobre fotogramas generados por https://crbug.com/1107766 'window.open()' en el árbol de | Chromium errores"  
[CR1115011]: "Al copiar una tabla desde la consola, la estructura de la tabla no se https://crbug.com/1115011 conserva | Chromium errores"  
[CR1116085]: "Vuelva a traer el inspector de propiedades https://crbug.com/1116085 de DevTools | Chromium errores"  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "prefers-reduced-data: Media Queries Level 5 | Borradores del editor de grupo de trabajo CSS de W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v6.2.0: GoogleChrome/lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Búferes de protocolo | Desarrolladores de Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Galaxy Fold | Samsung Estados Unidos"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Asignación lógica | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Separadores numéricos | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Hacer que el sitio web \"cross-origin se aísla\" con COOP y COEP | web.dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Detectar usuarios inactivos con la API de detección inactiva | web.dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Evite las animaciones no compuestas | web.dev"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-86) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
