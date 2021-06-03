---
description: Nuevas herramientas de depuración de cuadrícula CSS, herramienta Webauthn, herramientas movebles y panel lateral calculado.
title: Novedades de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c7859631327fc031909cd25736fddb8cff3cff45
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564899"
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
# <a name="whats-new-in-devtools-microsoft-edge-87"></a>Novedades de DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## <a name="improving-devtools-localization"></a>Mejorar la localización de DevTools  

Para satisfacer sus necesidades de traducción, el Microsoft Edge de DevTools se centra en mejorar la calidad de la traducción.  A partir Microsoft Edge versión 87, varias cadenas y términos están bloqueados y no cambian incluso cuando el resto de DevTools se muestran en otros idiomas.  La lista de cadenas y términos afectados incluye lo siguiente.  

*   Las cadenas de la **herramienta Faro.**  
*   El término `service worker` .  
*   Algunos de los **filtros de** herramientas de red como , , `URL` y `XHR` `JS` `CSS` .  
*   LA API de utilidades de consola [$0.][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]  
    
[$0][DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject] ahora está disponible en la [consola para][DevtoolsConsoleIndex] los usuarios en versiones localizadas de DevTools.   Gracias a la comunidad de desarrolladores global por ayudar a mejorar la localización del Microsoft Edge DevTools.  Continúe con [el envío de comentarios sobre la calidad de localización](#getting-in-touch-with-microsoft-edge-devtools-team) para mejorar la compatibilidad con DevTools en todas las configuraciones regionales.  Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya a Problema [#1136655][CR1136655].  


:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Panel de** red con filtros no localizados  
:::image-end:::  

## <a name="move-tools-between-top-and-bottom-panels"></a>Mover herramientas entre paneles superior e inferior  

DevTools ahora admite mover herramientas entre los paneles superior e inferior.  Personalice sus DevTools y mejore su productividad viendo cualquier combinación de dos herramientas al mismo tiempo.  Por ejemplo, vea las **** **herramientas Elementos** y Orígenes al mismo tiempo \(moviendo la herramienta **Orígenes** a la parte inferior\).  Para revisar el historial de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#1075732][CR1075732].  

:::row:::
   :::column span="":::
      Para mover cualquier herramienta superior a la parte inferior, mantenga el mouse en una pestaña, abra el menú contextual \(haga clic con el botón secundario\) y elija **Mover a la parte inferior**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Desplazarse a la parte inferior" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Desplazarse a la parte inferior  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Para mover cualquier herramienta inferior a la parte superior, mantenga el mouse en una pestaña, abra el menú contextual \(hacer clic con el botón derecho\) y elija **Mover a la parte superior**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Desplazarse a la parte superior" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Desplazarse a la parte superior  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## <a name="save-and-export-using-the-network-console"></a>Guardar y exportar con la consola de red  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

La **herramienta Consola de** red ahora ha mejorado la compatibilidad con los esquemas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] y [OpenAPI v2.][SwaggerSpecificationV2]  Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y elija la casilla situada junto a **Habilitar**consola de red .  Para obtener más información acerca de **la**consola de red, vaya a [Habilitar la característica experimental de consola de red][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Este experimento ahora admite las siguientes acciones.  

*   Guardar y exportar colecciones y entornos.  
*   Edite y exporte conjuntos de variables de entorno dentro de la **herramienta Consola de** red.  
    
Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya a Problema [#1093687][CR1093687].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Escriba el nombre del nuevo entorno" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Escriba el nombre del nuevo entorno  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Elegir formato para el nuevo entorno" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Elegir formato para el nuevo entorno  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="improved-css-grid-tooling"></a>Herramientas de cuadrícula CSS mejoradas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Las Microsoft Edge DevTools ahora admiten las siguientes características para inspeccionar, ver y depurar las cuadrículas CSS.  

*   Muestra una superposición de cuadrícula simplificada con **la herramienta Inspeccionar** u obtén información más detallada con superposiciones persistentes.  
*   Para habilitar las superposiciones de cuadrícula persistentes, elija el icono de cuadrícula junto a un elemento contenedor de cuadrícula en la herramienta **Elementos** o elija la cuadrícula en la **herramienta** Diseño.  
*   Puede habilitar las superposiciones persistentes para varias cuadrículas.  
*   La nueva **herramienta Diseño** te permite alternar fácilmente las superposiciones de cuadrícula y configurar la apariencia y el contenido de cada una.  
    
Las características están activadas de forma predeterminada.  Para obtener más información acerca de las características, vaya a [cuadrículas CSS][DevtoolsCssGrid].  Para revisar el historial de esta característica en el Chromium de código abierto, vaya a Problema [#1047356][CR1047356].  Además, el equipo Microsoft Edge DevTools colabora con el equipo de Chrome DevTools y la comunidad de Chromium para agregar nuevas características de herramientas de flexbox a DevTools.  Para obtener actualizaciones sobre las herramientas de flexbox Chromium proyecto de código abierto, vaya a Problema [#1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Herramienta de diseño con cuadrículas" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Herramienta de** diseño con cuadrículas  
:::image-end:::  

## <a name="customize-keyboard-shortcuts-in-settings"></a>Personalizar accesos rápidos de teclado en Configuración  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Ahora puedes personalizar el método abreviado de teclado para cualquier acción en DevTools.  Desde Microsoft Edge versión 84, puede elegir **** entre los ajustes preestablecidos Visual Studio Code **y DevTools (predeterminado)** para los [métodos abreviados de teclado.][DevtoolsCustomizeShortcuts]  A partir Microsoft Edge versión 87, puede activar el experimento Habilitar **editor** de métodos abreviados de teclado para personalizar aún más [los métodos abreviados de teclado.][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]  

Para habilitar el experimento, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a Habilitar editor de métodos abreviados de **teclado**.  Para obtener más información acerca de la personalización y edición de accesos directos, vaya a [Editar métodos abreviados de teclado para cualquier acción en DevTools][DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools].  Para revisar las actualizaciones en tiempo real de esta característica en Chromium proyecto de código abierto, vaya a Problema [#174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Acceso directo personalizado para pausar un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Acceso directo personalizado para pausar un script  
:::image-end:::  

## <a name="introducing-the-microsoft-edge-tools-for-visual-studio-code-extension"></a>Presentación de la Microsoft Edge herramientas de Visual Studio Code extensión  

Los **elementos para Visual Studio Code** **y red** para extensiones Visual Studio Code ahora se combinan en la nueva [Microsoft Edge Developer Tools para Visual Studio Code][VisualStudioCodeMarketplaceMsEdgedevtools] extensión.  Use el Microsoft Edge DevTools para las siguientes actividades sin salir de Microsoft Visual Studio code.  

*   Depurar el DOM  
*   Editar CSS  
*   Inspeccionar el tráfico de red  

Con la extensión, inicie Microsoft Edge, conéctese a una instancia existente del explorador o use un explorador sin cabeza directamente desde el editor.  Para empezar a contribuir y archivar problemas con sus comentarios sobre esta extensión, vaya a Microsoft Edge [Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo on GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Uso de la extensión en la captura de pantalla del modo de explorador completo" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Uso de la extensión en la captura de pantalla del modo de explorador completo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Uso de la extensión en la captura de pantalla del modo sin cabeza" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Uso de la extensión en la captura de pantalla del modo sin cabeza  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="announcements-from-the-chromium-project"></a>Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### <a name="new-webauthn-tool"></a>Nueva herramienta WebAuthn  

En versiones anteriores de Microsoft Edge, no había compatibilidad de depuración nativa de WebAuthn.  Necesitaba autenticadores físicos para probar la aplicación web con la [API de autenticación web.][GithubW3cWebauthn]  Con la nueva **herramienta WebAuthn,** puede realizar las siguientes acciones sin el uso de autenticadores físicos.

*   Emular autenticadores
*   Personalizar atributos de autenticadores
*   Inspeccionar estados de autenticadores
    
Para obtener más información acerca de la característica **WebAuthn,** vaya a [Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Puede emular autenticadores y depurar la API de autenticación [web][GithubW3cWebauthn] con la nueva herramienta [WebAuthn][DevtoolsWebauthnIndex].  Para abrir la **herramienta WebAuthn,** elija el icono Personalizar y **controlar DevTools** \( \) > `...` Más **herramientas**  >  **WebAuthn**.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#1034663][CR1034663].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Abrir la herramienta WebAuthn" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Abrir la **herramienta WebAuthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Herramienta WebAuthn" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         **Herramienta WebAuthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="elements-tool-updates"></a>Actualizaciones de la herramienta Elementos  

#### <a name="view-the-computed-sidebar-pane-in-the-styles-pane"></a>Ver el panel lateral calculado en el panel Estilos  

Alterna el **panel Calculado** en el **panel Estilos.**  El **panel Calculado** del panel **Estilos** se contrae de forma predeterminada.  Para alternar, elija el botón.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Abrir el panel de la barra lateral calculada" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Abrir el **panel de la barra lateral calculada**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Panel de barra lateral computada" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Panel de barra lateral** computada  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="grouping-css-properties-in-the-computed-panel"></a>Agrupación de propiedades CSS en el panel Calculado  

Para ver el CSS aplicado con menos desplazamiento, agrupa las propiedades CSS por categorías en **el panel Calculado.**  También puede centrarse selectivamente en un conjunto de propiedades relacionadas mientras inspecciona su CSS.  En la **herramienta Elementos,** elija un elemento.  Para agrupar \(o desagrupar\) las propiedades CSS, active la **casilla Grupo.**  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto Chromium, vaya a Problemas [#1096230][CR1096230], [#1084673][CR1084673]y [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Agrupación de propiedades CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Agrupación de propiedades CSS  
:::image-end:::  

### <a name="lighthouse-64-in-the-lighthouse-tool"></a>Faro 6.4 en la herramienta Faro  

La **herramienta Lighthouse** ahora ejecuta Lighthouse 6.4.  Para obtener una lista completa de los cambios, vaya a las notas [de la versión de Lighthouse][GithubGoogleChromeLighthouseReleasesV641].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#772558][CR772558].  

### <a name="performancemark-events-in-the-timings-section"></a>eventos performance.mark() en la sección Timings  

La **sección Timings de** una grabación de la herramienta [Performance][DevtoolsEvaluatePerformanceReference] marca ahora los `performance.mark()` eventos.  Para probar esta característica y medir el rendimiento del código JavaScript, agregue `performance.mark()` eventos al código.  Por ejemplo, el siguiente fragmento de código agrega marcadores antes y después de un bucle que itera de 0 a `for` 1000 mediante incrementos de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

A continuación, abra la [herramienta][DevtoolsEvaluatePerformanceReference] Rendimiento y vaya a la **sección Timings** para registrar el código JavaScript.  Los `performance.mark()` eventos que agregó ahora se muestran en la grabación.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Eventos Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` eventos  
:::image-end:::  

### <a name="new-resource-type-and-url-filters-in-the-network-tool"></a>Nuevos filtros de tipo de recurso y url en la herramienta Red  

Use las palabras `resource-type` clave y nuevas de la herramienta `url` **Red** para filtrar las solicitudes de red.  Por ejemplo, se `resource-type:image` usa para centrarse en las solicitudes de red que son imágenes.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtro de tipo de recurso" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtro de tipo de recurso  
:::image-end:::  

Para descubrir palabras clave más especiales como y , vaya a [solicitudes de filtro por `resource-type` `url` propiedades][DevtoolsNetworkReferenceFilterRequestsProperties].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problemas [#1121141][CR1121141] y [#1104188][CR1104188].  

### <a name="frame-details-view-updates"></a>Actualización de la vista de detalles del marco  

#### <a name="display-coep-and-coop-reporting-to-endpoint"></a>Mostrar informes de COEP y COOP en el punto de conexión  

Vea el extremo Directiva de incrustación entre orígenes \(COEP\) y Directiva de apertura entre orígenes \(COOP\) en la sección Seguridad `reporting to` **& aislamiento.**  La [API de informes][MdnReportingApi] define , un nuevo encabezado HTTP, que le permite especificar los puntos de conexión del servidor para que el explorador envíe `Report-To` advertencias y errores.  Para revisar las actualizaciones en tiempo real de esta característica en el Chromium de código abierto, vaya a Problema [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="El punto de conexión de informes" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   El `reporting to` extremo  
:::image-end:::  

#### <a name="display-coep-and-coop-report-only-mode"></a>Mostrar el modo de solo informe DE COEP y COOP  

DevTools ahora muestra la `report-only` etiqueta de COEP y COOP que están establecidas en `report-only` modo.  Para revisar las actualizaciones en tiempo real de esta característica en el Chromium de código abierto, vaya a Problema [#1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="La etiqueta de modo de solo informe" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   La `report-only` etiqueta de modo  
:::image-end:::  

### <a name="view-and-fix-color-contrast-issues-in-the-css-overview-tool"></a>Ver y corregir problemas de contraste de color en la herramienta Información general de CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Ahora, **la herramienta** Información general de CSS muestra una lista de elementos de la página que tienen problemas de contraste de color.  La siguiente página de demostración tiene un ejemplo de un problema de contraste de color.  

[CSS Overview Accessible Colors Demo][GlitchCssOverviewAccessibleColorsDemo]  

Para habilitar este **** experimento, en  >  **Configuración,** seleccione la casilla **Información general de CSS.**  Para ver una lista de elementos que tienen un problema de contraste de color, en **Problemas de contraste**, elija **Texto**.  Para abrir el elemento en la **herramienta Elementos,** elija un elemento en la lista.  Para ayudar a solucionar problemas de contraste, el Microsoft Edge DevTools [proporciona automáticamente sugerencias de color.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto Chromium de código abierto, vaya a Problema [#1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problemas de contraste de color bajo" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problemas de contraste de color bajo  
:::image-end:::  

## <a name="download-the-microsoft-edge-preview-channels"></a>Descargar los canales de vista previa de Microsoft Edge  

Si está en Windows o macOS, considere la posibilidad de usar los canales [Microsoft Edge vista previa][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de versión preliminar proporcionan acceso a las características más recientes de DevTools.  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsTool]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Desuso del panel Propiedades en la herramienta Elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugerencia de color accesible en el panel Estilos: novedades de DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsConsoleIndex]: ../../../console/index.md "Use la consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesRecentlyChosenElementJavascriptObject]:  ../../../console/utilities.md#recently-chosen-element-or-javascript-object "Elemento o objeto JavaScript elegido recientemente: referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: ../../../customize/shortcuts.md "Personalización de accesos rápidos de teclado en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeShortcutsEditKeyboardShortcutsForAnyActionDevtools]: ../../../customize/shortcuts.md#edit-keyboard-shortcuts-for-any-action-in-the-devtools "Edite los métodos abreviados de teclado para cualquier acción en el archivo DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: ../../../device-mode/index.md "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReference]: ../../../evaluate-performance/reference.md "Referencia de análisis de rendimiento | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: ../../../experimental-features/index.md#emulation-support-dual-screen-mode "Emulación: admite el modo de pantalla dual: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: ../../../experimental-features.md#enable-experimental-apis "Habilitar API experimentales: características experimentales | Microsoft Docs"  
<!--  [DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: ../../../experimental-features/index.md#enable-keyboard-shortcut-editor "Enable keyboard shortcut editor - Experimental features | Microsoft Docs"  -->  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: .. /.. /.. /experimental-features/index.md#enable-new-css-grid-debugging-features "Emulation: Support dual screen mode - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: .. /.. /.. /experimental-features/index.md#enable-network-console "Enable Network Console - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: .. /.. /.. /experimental-features/index.md#enable-source-order-viewer "Enable Source Order Viewer - Experimental features | Microsoft Docs&quot; [DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: .. /.. /.. /experimental-features/index.md#testing-on-foldable-and-dual-screen-devices &quot;Testing on foldable and dual-screen devices - Experimental features | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: .. /.. /.. /experimental-features/index.md#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsConsoleApiTable]: .. /.. /.. /console/api.md#table "table- Console API reference | Microsoft Docs"  
[DevtoolsCoverageIndex]: .. /.. /.. /coverage/index.md "Buscar código JavaScript y CSS sin usar con la pestaña Cobertura en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]: .. /.. /.. /css/grid.md "Inspect CSS Grid | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: .. /.. /.. /customize/index.md#drawer "Drawer- Customize Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: .. /.. /.. /customize/index.md#settings "Configuración: Personalizar Microsoft Edge devTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: .. /.. /.. /evaluate-performance/reference.md#analyze-rendering-performance-with-the-rendering-tab "Analyze rendering performance with the Rendering tab - Performance Analysis Reference | Microsoft Docs"  
[DevtoolsMediaIndex]: .. /.. /.. /media/index.md "Ver y depurar la información de los reproductores multimedia | Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: .. /.. /.. /network/reference.md#filter-requests-by-properties "Filter requests by properties - Network Analysis reference | Microsoft Docs"  
[DevtoolsWebauthnIndex]: .. /.. /.. /webauthn/index.md "Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCodeMain]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Herramientas para Visual Studio Code | Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar los métodos abreviados de teclado o los enlaces de teclas | Chromium errores"
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la versión más reciente de | Chromium errores"  
[CR1034663]: https://crbug.com/1034663 "Crear un front-end para la API de prueba de WebAuthn | Chromium errores"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS Grid/Flexbox/Table | Chromium errores"  
[CR1051466]: https://crbug.com/1051466 "Admite la depuración de COOP/COEP en DevTools | Chromium errores"  
[CR1073899]: https://crbug.com/1073899 "La pestaña Estilo calculado desaparece en modo de respuesta | Chromium errores"  
[CR1075732]: https://crbug.com/1075732 "Personalización de DevTools: pestañas móviles | Chromium errores"  
[CR1084673]: https://crbug.com/1084673 "DevTools: mejore la forma en que presentamos propiedades personalizadas css ((aka). variables CSS) y sus valores | Chromium errores"  
[CR1093687]: https://crbug.com/1093687 "Crear herramienta para crear y reproducir solicitudes de red sintéticas | Chromium errores"  
[CR1096230]: https://crbug.com/1096230 "Agrupar propiedades CSS por categorías en el panel Estilos calculados | Chromium errores"  
[CR1104188]: https://crbug.com/1104188 "La búsqueda de herramientas de red no encuentra resultados al buscar direcciones URL | Chromium errores"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: mejorar la pestaña Estilos calculados | Chromium errores"  
[CR1120316]: https://crbug.com/1120316 "Resalte el contraste malo en Información general de CSS > colores | Chromium Errores"  
[CR1121141]: https://crbug.com/1121141 "Permitir el filtrado por tipo de recurso en el registro de red | Chromium errores"  
[CR1121312]: https://crbug.com/1121312 "Configuración debe quitarse del menú Más herramientas | Chromium errores"  
[CR1136394]: https://crbug.com/1136394 "Herramientas flexbox | Chromium Errores"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Localización V2 | Chromium errores"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Api de informes | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1: GoogleChrome/lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Hola! | Glitch"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato de colección postman v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "OpenAPI Specification | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/blog/new-in-devtools-87) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  
