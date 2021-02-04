---
description: Nuevas herramientas de depuración de cuadrícula CSS, herramienta Webauthn, herramientas que se pueden mover y panel lateral calculado.
title: Novedades de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: cf3a685a1a4e9a3f13d2401a6294058a71dd5104
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313033"
---
# Novedades de DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Mejorar la localización de DevTools  

Para satisfacer sus necesidades de traducción, el equipo de DevTools de Microsoft Edge se centra en mejorar la calidad de la traducción.  A partir de la versión 87 de Microsoft Edge, varias cadenas y términos están bloqueados y no cambian incluso cuando el resto de Las DevTools se muestran en otros idiomas.  La lista de cadenas y términos afectados incluye lo siguiente.  

*   Las cadenas de la herramienta **Desgarro.**  
*   El término `service worker` .  
*   Algunos de los **filtros de** la herramienta De red, como , `URL` y `XHR` `JS` `CSS` .  
*   La API de utilidades de consola de [$0.][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] ahora está disponible en la [consola para](/microsoft-edge/devtools-guide-chromium/console/index.md) los usuarios en versiones localizadas de DevTools.   Gracias a la comunidad de desarrolladores global por ayudar a mejorar la localización de Microsoft Edge DevTools.  Continúa [envíando comentarios sobre la calidad de localización](#getting-in-touch-with-microsoft-edge-devtools-team) para mejorar la compatibilidad con DevTools en todas las configuraciones regionales.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al problema [#1136655][CR1136655].  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   **Panel de** red con filtros no localizados  
:::image-end:::  

## Mover herramientas entre paneles superior e inferior  

DevTools ahora admite mover herramientas entre los paneles superior e inferior.  Personaliza tus DevTools y mejora la productividad viendo cualquier combinación de dos herramientas al mismo tiempo.  Por ejemplo, vea las **** **herramientas Elementos** y Orígenes al mismo tiempo \(moviendo la herramienta **Orígenes** a la parte inferior\).  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya al problema [#1075732][CR1075732].  

:::row:::
   :::column span="":::
      Para mover cualquier herramienta superior a la parte inferior, mantenga el mouse sobre una pestaña, abra el menú contextual \(haga clic con el botón secundario\) y elija **Mover a la parte inferior.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Moverse a la parte inferior" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Moverse a la parte inferior  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Para mover cualquier herramienta inferior a la parte superior, mantenga el mouse sobre una pestaña, abra el menú contextual \(haga clic con el botón secundario\) y elija Mover **a la parte superior.**  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Desplazarse a la parte superior" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Desplazarse a la parte superior  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## Guardar y exportar con la consola de red  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

La **herramienta Consola de** red ha mejorado la compatibilidad con los esquemas [Postman v2.1][PostmanSchemaJsonCollectionv210Index] y [OpenAPI v2.][SwaggerSpecificationV2]  Para habilitar el experimento, ve a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y elige la casilla situada junto **a Habilitar consola de red.**  Para obtener más información acerca de **la Consola de red,** vaya [a Habilitar la característica Experimental de consola de red.][DevtoolsExperimentalFeaturesEnableNetworkConsole]  Este experimento ahora admite las siguientes acciones.  

*   Guardar y exportar colecciones y entornos.  
*   Edite y exporte conjuntos de variables de entorno dentro de la **herramienta Consola de** red.  
    
Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al problema [#1093687][CR1093687].  

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

## Herramientas de cuadrícula CSS mejoradas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Las DevTools de Microsoft Edge ahora admiten las siguientes características para inspeccionar, ver y depurar las cuadrículas CSS.  

*   Muestra una superposición de cuadrícula simplificada con la herramienta **Inspeccionar** u obtén información más detallada con superposiciones persistentes.  
*   Para habilitar las superposiciones de cuadrícula persistentes, elige el icono de cuadrícula junto a un elemento contenedor de cuadrícula en la herramienta **Elementos** o elige la cuadrícula en la **herramienta Diseño.**  
*   Puedes habilitar las superposiciones persistentes para varias cuadrículas.  
*   La nueva **herramienta de** diseño te permite alternar fácilmente las superposiciones de cuadrícula y configurar la apariencia y el contenido de cada una.  
    
Las características están activadas de forma predeterminada.  Para obtener más información acerca de las características, vaya a [cuadrículas CSS.][DevtoolsCssGrid]  Para revisar el historial de esta característica en el proyecto de código abierto chromium, vaya a Problema [#1047356][CR1047356].  Además, el equipo de DevTools de Microsoft Edge colabora con el equipo de Chrome DevTools y la comunidad de Chromium para agregar nuevas características de herramientas de flexbox a DevTools.  Para obtener actualizaciones sobre las herramientas de flexbox en el proyecto de código abierto chromium, vaya al [problema #1136394][CR1136394].  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Herramienta de diseño con cuadrículas" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   **Herramienta de** diseño con cuadrículas  
:::image-end:::  

## Personalizar los métodos abreviados de teclado en Configuración  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

Ahora puedes personalizar el método abreviado de teclado para cualquier acción en DevTools.  Desde la versión 84 de Microsoft Edge, puedes elegir entre Visual Studio **Code** y **DevTools (predeterminado)** preestablecidos para [métodos abreviados de teclado.][DevtoolsCustomizeShortcuts]  A partir de la versión 87 de Microsoft Edge, puedes activar el experimento Habilitar **editor** de métodos abreviados de teclado para personalizar aún más [los métodos abreviados de teclado.][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]  

Para habilitar el experimento, ve a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y elige la casilla junto **a Habilitar editor de métodos abreviados de teclado.**  Para obtener más información sobre la personalización y la edición de accesos directos, vaya a [Habilitar la característica experimental del editor de método abreviado de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al problema [#174309][CR174309].  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Acceso directo personalizado para pausar un script" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Acceso directo personalizado para pausar un script  
:::image-end:::  

## Presentación de las herramientas de Microsoft Edge para la Visual Studio de código  

Los **elementos para Visual Studio code** y network for Visual Studio Code **extensions** ahora se combinan en las nuevas herramientas de desarrollo de Microsoft Edge para Visual Studio de [código.][VisualStudioCodeMarketplaceMsEdgedevtools]  Usa las DevTools de Microsoft Edge para las siguientes actividades sin salir Visual Studio código.  

*   Depurar el DOM  
*   Editar CSS  
*   Inspeccionar el tráfico de red  

Con la extensión, inicie Microsoft Edge, conéctese a una instancia existente del explorador o use un explorador sin cabeza directamente desde el editor.  Para empezar a colaborar y archivar problemas con sus comentarios sobre esta extensión, vaya [a Microsoft Edge Developer Tools for Visual Studio Code][GithubMicrosoftVscodeEdgeDevtools] repo en GitHub.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Usar la extensión en la captura de pantalla del modo de explorador completo" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Usar la extensión en la captura de pantalla del modo de explorador completo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Usar la extensión en la captura de pantalla del modo sin cabeza" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Usar la extensión en la captura de pantalla del modo sin cabeza  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nueva herramienta WebAuthn  

En versiones anteriores de Microsoft Edge, no había compatibilidad nativa de depuración de WebAuthn.  Necesitaba autenticadores físicos para probar la aplicación web con la [API de autenticación web.][GithubW3cWebauthn]  Con la nueva **herramienta WebAuthn,** puede realizar las siguientes acciones sin el uso de autenticadores físicos.

*   Emular autenticadores
*   Personalizar atributos de autenticadores
*   Inspeccionar los estados de autenticadores
    
Para obtener más información acerca de **la característica WebAuthn,** vaya a [Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools.][DevtoolsWebauthnIndex]  

Puede emular autenticadores y depurar la API de [autenticación web][GithubW3cWebauthn] con la nueva [herramienta WebAuthn.][DevtoolsWebauthnIndex]  Para abrir la **herramienta WebAuthn,** elija el icono Personalizar y **controlar DevTools** \( \) > `...` Más **herramientas**  >  **WebAuthn**.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al problema [#1034663][CR1034663].  

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

### Actualizaciones de herramientas de elementos  

#### Ver el panel de la barra lateral calculada en el panel Estilos  

Alterna el **panel Calculado** en el **panel Estilos.**  El **panel Calculado** del panel **Estilos** está contraído de forma predeterminada.  Para alternar, elija el botón.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al problema [#1073899][CR1073899].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Abrir el panel de la barra lateral calculada" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Abrir el **panel de la barra lateral** calculada  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Panel de barra lateral calculado" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         **Panel de barra lateral** calculado  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Agrupación de propiedades CSS en el panel Calculado  

Para ver el CSS aplicado con menos desplazamiento, agrupa las propiedades CSS por categorías en **el panel Calculado.**  También puede centrarse selectivamente en un conjunto de propiedades relacionadas mientras inspecciona su CSS.  En la **herramienta Elementos,** elija un elemento.  Para agrupar \(o desagrupar\) las propiedades CSS, activa o desactiva la **casilla grupo.**  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya a Problemas [#1096230,][CR1096230] [#1084673][CR1084673]y [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Agrupación de propiedades CSS" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Agrupación de propiedades CSS  
:::image-end:::  

### Pie 6.4 en la herramienta Desalmón  

Ahora, **la** herramienta Deseste está ejecutando la versión 6.4.  Para obtener una lista completa de los cambios, vaya a las notas de la [versión Desenlaz.][GithubGoogleChromeLighthouseReleasesV641]  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al problema [#772558][CR772558].  

### eventos performance.mark() en la sección Intervalos  

La **sección Intervalos de** una grabación de la herramienta [Rendimiento][DevtoolsGuideChromiumEvaluatePerformanceReference] marca ahora `performance.mark()` los eventos.  Para probar esta característica y medir el rendimiento del código JavaScript, agregue `performance.mark()` eventos al código.  Por ejemplo, el siguiente fragmento de código agrega marcadores antes y después de un bucle que itera de 0 a `for` 1000 con incrementos de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

A continuación, abra [la herramienta][DevtoolsGuideChromiumEvaluatePerformanceReference] Rendimiento y vaya a la sección **Intervalos** para registrar el código JavaScript.  Los `performance.mark()` eventos que agregó ahora se muestran en la grabación.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Eventos Performance.mark" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` events  
:::image-end:::  

### Nuevos filtros de tipo de recurso y url en la herramienta Red  

Use las palabras `resource-type` clave y las nuevas de la herramienta `url` **Red** para filtrar las solicitudes de red.  Por ejemplo, se `resource-type:image` usa para centrarse en las solicitudes de red que son imágenes.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="filtro de tipo de recurso" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtro de tipo de recurso  
:::image-end:::  

Para detectar palabras clave más especiales, como `resource-type` y , navegue a las solicitudes de filtro por `url` [propiedades.][DevtoolsNetworkReferenceFilterRequestsProperties]  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya a Problemas [#1121141][CR1121141] y [#1104188][CR1104188].  

### Actualización de la vista de detalles del marco  

#### Mostrar informes COEP y COEXIST en el punto de conexión  

Consulta el extremo directiva de incrustación entre orígenes \(COEP\) y la directiva de apertura entre orígenes \(COEXIST\) en la sección Seguridad `reporting to` **& aislamiento.**  La [API de informes][MdnReportingApi] define un nuevo encabezado HTTP que permite especificar los puntos de conexión del servidor para que el explorador envíe `Report-To` advertencias y errores.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al [problema #1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="El informe al punto de conexión" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   El `reporting to` extremo  
:::image-end:::  

#### Mostrar el modo coep y de solo informe DEER  

DevTools muestra ahora la `report-only` etiqueta de COEP y COEXIST que están establecidas en `report-only` modo.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al [problema #1051466][CR1051466].  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="La etiqueta de modo de solo informe" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   La `report-only` etiqueta de modo  
:::image-end:::  

### Ver y corregir problemas de contraste de color en la herramienta de información general de CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Característica experimental":::
   Característica experimental  
:::image-end:::  

La **herramienta de información general** de CSS ahora muestra una lista de elementos en la página que tienen problemas de contraste de color.  La siguiente página de demostración tiene un ejemplo de un problema de contraste de color.  

[Demostración de colores accesibles de información general de CSS][GlitchCssOverviewAccessibleColorsDemo]  

Para habilitar este experimento, en **Experimentos**  >  **de configuración,** selecciona la casilla De información **general de CSS.**  Para ver una lista de elementos que tienen un problema de contraste de color, en **Problemas de contraste**, elija **Texto**.  Para abrir el elemento en la herramienta **Elementos,** elija un elemento de la lista.  Para ayudar a solucionar problemas de contraste, las DevTools de Microsoft Edge proporcionan automáticamente [sugerencias de color.][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de código abierto chromium, vaya al problema [#1120316][CR1120316].  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Problemas de contraste de color bajo" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problemas de contraste de color bajo  
:::image-end:::  

## Descargar los canales de vista previa de Microsoft Edge  

Si está en Windows o macOS, considere la posibilidad de usar los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Desuso del panel Propiedades en la herramienta Elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft Docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugerencia de color accesible en el panel Estilos: novedades de DevTools (Microsoft Edge 86) | Microsoft Docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento seleccionado recientemente o objeto JavaScript: referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar los métodos abreviados de teclado en las DevTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referencia de análisis de rendimiento | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulación: admite el modo de pantalla doble- Características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar API experimentales: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar el editor de métodos abreviados de teclado: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulación: admite el modo de pantalla doble- Características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Habilitar consola de red: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar el Visor de pedidos de origen: características experimentales | Microsoft Docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos de doble pantalla y plegados: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft Docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabla: referencia de api de consola | Microsoft Docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Busque código JavaScript y CSS sin usar con la pestaña Cobertura en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspeccionar la cuadrícula CSS | Microsoft Docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón: personalizar las devTools de Microsoft Edge | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de representación con la pestaña Representación: referencia de análisis de rendimiento | Microsoft Docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Ver y depurar información de reproductores multimedia | Microsoft Docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtrar solicitudes por propiedades: referencia de análisis de red | Microsoft Docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emular autenticadores y depurar WebAuthn en Microsoft Edge DevTools | Microsoft Docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Tools for Visual Studio Code | Visual Studio código"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR174309]: https://crbug.com/174309 "DevTools: permite personalizar los métodos abreviados de teclado o los enlaces de teclas | Errores de Chromium"
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la última versión de La última versión de La | Errores de Chromium"  
[CR1034663]: https://crbug.com/1034663 "Crear un front-end para la API de prueba de WebAuthn | Errores de Chromium"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS Grid/Flexbox/Table | Errores de Chromium"  
[CR1051466]: https://crbug.com/1051466 "Compatibilidad con la depuración DEER/COEP en DevTools | Errores de Chromium"  
[CR1073899]: https://crbug.com/1073899 "La pestaña estilo calculado desaparece en el modo de respuesta | Errores de Chromium"  
[CR1075732]: https://crbug.com/1075732 "Personalización de DevTools: pestañas movibles | Errores de Chromium"  
[CR1084673]: https://crbug.com/1084673 "DevTools: mejora la forma en que presentamos las propiedades personalizadas css (también conocido como). variables CSS) y sus valores | Errores de Chromium"  
[CR1093687]: https://crbug.com/1093687 "Crear una herramienta para crear y reproducir solicitudes de red sintética | Errores de Chromium"  
[CR1096230]: https://crbug.com/1096230 "Agrupar propiedades CSS por categorías en el panel Estilos calculados | Errores de Chromium"  
[CR1104188]: https://crbug.com/1104188 "La búsqueda de herramientas de red no encuentra resultados al buscar direcciones URL | Errores de Chromium"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: mejorar la pestaña Estilos calculados | Errores de Chromium"  
[CR1120316]: https://crbug.com/1120316 "Resaltar el contraste no bueno en Información general de CSS > colores | Chromium Bugs"  
[CR1121141]: https://crbug.com/1121141 "Permitir el filtrado por tipo de recurso en el registro de | Errores de Chromium"  
[CR1121312]: https://crbug.com/1121312 "La configuración debe quitarse del menú Más herramientas | Errores de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Herramientas de Flexbox | Chromium Bugs"  
[CR1136655]: https://crbug.com/1136655 "Devtools: Localización V2 | Errores de Chromium"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "Api de informes | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v6.4.1: GoogleChrome/| GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "Hola, | Problemas"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Postman Collection Format v2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "OpenAPI Specification | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/10/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen