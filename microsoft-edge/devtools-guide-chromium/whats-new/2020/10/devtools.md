---
description: Nuevas herramientas de depuración de cuadrícula CSS, herramienta webauthn, herramientas móviles y panel de barra lateral calculado.
title: Novedades de DevTools (Microsoft Edge 87)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0e4b1972918797d69e2068236f6d1336c54cc858
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134197"
---
# Novedades de DevTools (Microsoft Edge 87)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Mejorar la localización de DevTools  

Para satisfacer sus necesidades de traducción, el equipo de Microsoft Edge DevTools se centró en mejorar la calidad de la traducción.  A partir de la versión 87 de Microsoft Edge, varias cadenas y términos están bloqueados y no cambian incluso cuando el resto de las DevTools se muestran en otros idiomas.  La lista de cadenas y términos afectados incluye lo siguiente.  

*   Las cadenas de la herramienta **Lighthouse** .  
*   El término `service worker` .  
*   Algunos de los filtros de herramientas de **red** , como `URL` ,, `XHR` `JS` y `CSS` .  
*   La API de utilidades de consola de [$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] .  
    
[$0][DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject] está disponible en la [consola](/microsoft-edge/devtools-guide-chromium/console/index.md) para los usuarios de versiones localizadas de la DevTools.   Gracias por ayudar a la comunidad de programadores de la globalización de mejorar la localización de Microsoft Edge DevTools.  Sigue [enviando comentarios sobre la calidad de la localización](#getting-in-touch-with-microsoft-edge-devtools-team) para mejorar la compatibilidad con DevTools en todas las configuraciones regionales.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1136655][CR1136655]de problemas.  

:::image type="complex" source="../../media/2020/10/bing-network-japanese.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/bing-network-japanese.msft.png":::
   Panel de **red** con filtros no localizados  
:::image-end:::  

## Mover herramientas entre los paneles superior e inferior  

DevTools ahora es compatible con las herramientas de movimiento entre los paneles superior e inferior.  Personalice su DevTools y mejore su productividad viendo cualquier combinación de dos herramientas al mismo tiempo.  Por ejemplo, vea los **elementos** y las herramientas de **orígenes** al mismo tiempo \ (para ello, mueva la herramienta de **fuentes** al final \).  Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el [#1075732][CR1075732]de problemas.  

:::row:::
   :::column span="":::
      Para mover cualquier herramienta superior a la parte inferior, desplace el puntero sobre una pestaña, abra el menú contextual \ (haga clic con el botón derecho \) y elija **mover a la parte inferior**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-bottom.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/move-to-bottom.msft.png":::
         Mover a la parte inferior  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Para mover cualquier herramienta inferior a la parte superior, desplace el puntero sobre una pestaña, abra el menú contextual \ (haga clic con el botón derecho \) y elija **mover a la parte superior**.  
      
      :::image type="complex" source="../../media/2020/10/move-to-top.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/move-to-top.msft.png":::
         Mover al principio  
      :::image-end:::  
   :::column-end:::
:::row-end:::

## Guardar y exportar con la consola de red  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Herramienta de red con filtros no localizados":::
   Característica experimental  
:::image-end:::  

La herramienta de **consola de red** ahora tiene mayor compatibilidad con los esquemas [v 2.1][PostmanSchemaJsonCollectionv210Index] y [OpenAPI V2][SwaggerSpecificationV2] .  Para habilitar el experimento, navegue para [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla que se encuentra junto a **Habilitar consola de red**.  Para obtener más información sobre la **consola de red**, vaya a habilitar la [característica experimental consola de red][DevtoolsExperimentalFeaturesEnableNetworkConsole].  Este experimento ahora es compatible con las siguientes acciones.  

*   Guardar y exportar colecciones y entornos.  
*   Edite y exporte conjuntos de variables de entorno dentro de la herramienta de **consola de red** .  
    
Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1093687][CR1093687]de problemas.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-name.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/network-console-environments-new-name.msft.png":::
         Escriba un nombre para el nuevo entorno  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/network-console-environments-new-format.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/network-console-environments-new-format.msft.png":::
         Elegir formato para el nuevo entorno  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Herramientas de cuadrícula CSS mejoradas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Herramienta de red con filtros no localizados":::
   Característica experimental  
:::image-end:::  

Ahora, Microsoft Edge DevTools es compatible con las siguientes características para inspeccionar, visualizar y depurar las cuadrículas de CSS.  

*   Mostrar una superposición de cuadrícula simplificada con la herramienta **inspeccionar** , u obtener información más detallada con las superposiciones persistentes.  
*   Para habilitar las superposiciones de cuadrícula persistentes, elija el icono de cuadrícula junto a un elemento de contenedor de cuadrícula en la herramienta **elementos** o elija la cuadrícula en la herramienta de **diseño** .  
*   Puede habilitar superposiciones persistentes para varias cuadrículas.  
*   La nueva herramienta de **diseño** le permite alternar fácilmente las superposiciones de cuadrícula y configurar la apariencia y el contenido de cada una de ellas.  
    
Las características están activadas de forma predeterminada.  Para obtener más información sobre las características, vaya a [cuadrículas de CSS][DevtoolsCssGrid].  Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el [#1047356][CR1047356]de problemas.  Además, el equipo de Microsoft Edge DevTools está colaborando con el equipo de Chrome DevTools y la comunidad de cromo para agregar nuevas características de herramientas de Flexbox a DevTools.  Para obtener las actualizaciones de las herramientas de Flexbox en el proyecto de origen abierto de cromo, navegue hasta el [#1136394][CR1136394]de problemas.  

:::image type="complex" source="../../media/2020/10/grid-layout-pane.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/grid-layout-pane.msft.png":::
   Herramienta de **diseño** con cuadrículas  
:::image-end:::  

## Personalizar métodos abreviados de teclado en la configuración  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Herramienta de red con filtros no localizados":::
   Característica experimental  
:::image-end:::  

Ahora puede personalizar el método abreviado de teclado para cualquier acción en el DevTools.  Desde Microsoft Edge versión 84, puede elegir entre los valores preestablecidos de **Visual Studio Code** y **DevTools (predeterminado)** para los [métodos abreviados de teclado][DevtoolsCustomizeShortcuts].  A partir de la versión 87 de Microsoft Edge, puede activar el experimento **Habilitar editor de método abreviado de teclado** para personalizar aún más los [métodos abreviados de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Para habilitar el experimento, navegue para [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a **Habilitar el editor de métodos abreviados de teclado**.  Para obtener más información sobre la personalización y la edición de accesos directos, vaya a [Habilitar la característica experimental editor de método abreviado de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#174309][CR174309]de problemas.  

:::image type="complex" source="../../media/2020/10/custom-shortcut-pause-script.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/custom-shortcut-pause-script.msft.png":::
   Acceso directo personalizado para pausar un script  
:::image-end:::  

## Presentamos la extensión de código de las herramientas de Microsoft Edge para Visual Studio  

Los **elementos para Visual Studio Code** y las extensiones **de código de Visual Studio** ahora se combinan en la nueva extensión [de código de las herramientas de desarrollo de Microsoft Edge para Visual Studio][VisualStudioCodeMarketplaceMsEdgedevtools] .  Usa el DevTools de Microsoft Edge para las siguientes actividades sin salir de Visual Studio Code.  

*   Depurar DOM  
*   Editar CSS  
*   Inspeccionar el tráfico de red  

Con la extensión, Inicie Microsoft Edge, conéctese a una instancia existente del explorador o use un explorador sin cabeza directamente desde el editor.  Para empezar a colaborar y archivar problemas con sus comentarios sobre esta extensión, navegue hasta el repositorio [de código de las herramientas de desarrollo de Microsoft Edge para Visual Studio][GithubMicrosoftVscodeEdgeDevtools] en github.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/microsoft-edge-tools-full-browser.msft.png":::
         Uso de la extensión en el modo de navegador completo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/microsoft-edge-tools-headless.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/microsoft-edge-tools-headless.msft.png":::
         Uso de la extensión en modo de pantalla desatendida  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Anuncios del proyecto de cromo  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nueva herramienta webauthn  

En versiones anteriores de Microsoft Edge, no había ninguna compatibilidad nativa de depuración de webauthr.  Necesitaba autenticadores físicos para probar la aplicación web con la [API de autenticación Web][GithubW3cWebauthn].  Con la nueva herramienta **Webauthn** , podrá realizar las siguientes acciones sin usar ningún autenticador físico.

*   Emular autenticadores
*   Personalizar atributos de autenticadores
*   Inspeccionar Estados de autenticadores
    
Para obtener más información sobre la característica **Webauthn** , vaya a [emular autenticadores y depurar webauthn en Microsoft Edge DevTools][DevtoolsWebauthnIndex].  

Puede emular autenticadores y depurar la [API de autenticación Web][GithubW3cWebauthn] con la nueva herramienta [webauthn][DevtoolsWebauthnIndex] .  Para abrir la herramienta **webauthn** , elija **el icono personalizar y controlar DevTools** \ ( `...` \) > **más herramientas**  >  **webauthn**.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1034663][CR1034663]de problemas.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/more-tools-webauthn.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/more-tools-webauthn.msft.png":::
         Abrir la herramienta **Webauthn**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/webauthn-enable-virtual-auth.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/webauthn-enable-virtual-auth.msft.png":::
         Herramienta **Webauthn**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Actualizaciones de la herramienta elementos  

#### Ver el panel de la barra lateral calculado en el panel estilos  

Activar o desactivar el panel **calculado** en el panel **estilos** .  El panel **calculado** del panel **estilos** está contraído de forma predeterminada.  Para activarla, elija el botón.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1073899][CR1073899]de problemas.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/computed-sidebar-pane.msft.png":::
         Abrir el panel de la **barra lateral calculado**  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/10/computed-sidebar-pane-open.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/computed-sidebar-pane-open.msft.png":::
         Panel de **barra lateral calculado**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Agrupar las propiedades de CSS en el panel calculado  

Para ver la CSS aplicada con menos desplazamiento, Agrupe las propiedades de CSS por categorías en el panel **calculado** .  También puede concentrarse selectivamente en un conjunto de propiedades relacionadas mientras inspecciona su CSS.  Desde la herramienta **elementos** , elija un elemento.  Para agrupar \ (o desagrupar \) las propiedades de CSS, marque la casilla de verificación de **Grupo** .  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a problemas [#1096230][CR1096230], [#1084673][CR1084673]y [#1106251][CR1106251].  

:::image type="complex" source="../../media/2020/10/grouping-css-prop.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/grouping-css-prop.msft.png":::
   Agrupar propiedades CSS  
:::image-end:::  

### Lighthouse 6,4 en la herramienta Lighthouse  

La herramienta **Lighthouse** se ejecuta ahora Lighthouse 6,4.  Para obtener una lista completa de los cambios, vaya a las notas de la [versión de Lighthouse][GithubGoogleChromeLighthouseReleasesV641].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#772558][CR772558]de problemas.  

### eventos performance. Mark () en la sección intervalos  

La **sección intervalos** de una grabación en la herramienta [rendimiento][DevtoolsGuideChromiumEvaluatePerformanceReference] marca ahora los `performance.mark()` eventos.  Para probar esta característica y medir el rendimiento de su código de JavaScript, agregue `performance.mark()` eventos al código.  Por ejemplo, el siguiente fragmento de código agrega marcadores antes y después de un `for` bucle que itera de 0 a 1000 con incrementos de 7.  

```javascript
performance.mark('start');
for (var i = 0; i < 1000; i+=7;){
  console.log(i);
}
performance.mark('end');
```  

Después, abra la herramienta [rendimiento][DevtoolsGuideChromiumEvaluatePerformanceReference] y vaya a la **sección intervalos** para grabar el código JavaScript.  Los `performance.mark()` eventos que ha agregado se muestran ahora en la grabación.  

:::image type="complex" source="../../media/2020/10/perf-mark.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/perf-mark.msft.png":::
   `performance.mark` ceso  
:::image-end:::  

### Nuevos filtros de recursos URL y tipos de recursos en la herramienta red  

Use las `resource-type` `url` palabras clave New y keyword de la herramienta **red** para filtrar solicitudes de red.  Por ejemplo, use `resource-type:image` para centrarse en las solicitudes de red que son imágenes.  

:::image type="complex" source="../../media/2020/10/network-resource-type-filter.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/network-resource-type-filter.msft.png":::
   filtro de tipo de recurso  
:::image-end:::  

Para descubrir más palabras clave especiales como `resource-type` y `url` , vaya a [filtrar las solicitudes por propiedades][DevtoolsNetworkReferenceFilterRequestsProperties].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a problemas [#1121141][CR1121141] y [#1104188][CR1104188].  

### Actualización de la vista de detalles del marco  

#### Mostrar informes de COEP y de COOP al punto final  

Ver la Directiva de Embedder de origen cruzado \ (COEP \) y la Directiva de apertura cruzada de origen \ (COOP \) `reporting to` en la sección **aislamiento del & de seguridad** .  La [API de informes][MdnReportingApi] define `Report-To` , un nuevo encabezado HTTP, que le ofrece una manera de especificar los puntos de conexión de servidor para que el explorador envíe advertencias y errores.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1051466][CR1051466]de problemas.  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-1.msft.png":::
   El `reporting to` punto final  
:::image-end:::  

#### Modo de solo informe de COEP y de COOP  

DevTools ahora Mostrar la `report-only` etiqueta de COEP y Coop que están establecidas en `report-only` mode.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1051466][CR1051466]de problemas.  

:::image type="complex" source="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/https_first_party_test_glitch_me_coop-2.msft.png":::
   La `report-only` etiqueta de modo  
:::image-end:::  

### Ver y corregir problemas de contraste de color en la herramienta de información general de CSS  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Herramienta de red con filtros no localizados":::
   Característica experimental  
:::image-end:::  

La herramienta de **información general de CSS** ahora muestra una lista de elementos en la página que tienen problemas de contraste de color.  La siguiente página de demostración tiene un ejemplo de un problema de contraste de color.  

[Demostración de colores accesibles de CSS][GlitchCssOverviewAccessibleColorsDemo]  

Para habilitar este experimento, en **Settings**  >  **experimentos**de configuración, seleccione la casilla de verificación **Descripción general de CSS** .  Para ver una lista de elementos que tienen un problema de contraste de color, en **problemas de contraste**, elija **texto**.  Para abrir el elemento en la herramienta **elementos** , elija un elemento de la lista.  Para ayudar a solucionar los problemas de contraste, Microsoft Edge DevTools [ofrece automáticamente sugerencias de color][DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#1120316][CR1120316]de problemas.  

:::image type="complex" source="../../media/2020/10/css-overview.msft.png" alt-text="Herramienta de red con filtros no localizados" lightbox="../../media/2020/10/css-overview.msft.png":::
   Problemas de contraste de color bajo  
:::image-end:::  

## Descargar los canales de Microsoft Edge Preview  

Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-tool "Desuso del panel de propiedades en la herramienta elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de la cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft docs"  
[DevtoolsWhatsnew200208DevtoolsAccessibleColorSuggestionStylesPane]: ../08/devtools.md#accessible-color-suggestion-in-the-styles-pane "Sugerencia de color accesible en el panel Estilos: novedades de DevTools (Microsoft Edge 86) | Microsoft docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsGuideChromiumConsoleUtilitiesRecentlySelectedElementJavascriptObject]:  https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/console/utilities#recently-selected-element-or-javascript-object "Elemento seleccionado recientemente o objeto de JavaScript: referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar los métodos abreviados de teclado en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsGuideChromiumEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referencia del análisis de rendimiento | Microsoft docs"  
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: /microsoft-edge/devtools-guide-chromium/experimental-features#emulation-support-dual-screen-mode "Emulación: compatibilidad con el modo de pantalla dual-características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar las API experimentales: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar el editor de métodos abreviados de teclado: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulación: compatibilidad con el modo de pantalla dual-características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNetworkConsole]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-network-console "Habilitar la consola de red: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar visor de pedidos de origen-características experimentales | Microsoft docs"
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos de plegable y dos pantallas: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabla-referencia de API de consola | Microsoft docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCssGrid]:  /microsoft-edge/devtools-guide-chromium/css/grid "Inspeccionar CSS cuadrícula | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de la representación con la pestaña representación, referencia de análisis de rendimiento | Microsoft docs"  
[DevtoolsMediaIndex]: /microsoft-edge/devtools-guide-chromium/media/index "Ver y depurar información de reproductores multimedia | Microsoft docs"  
[DevtoolsNetworkReferenceFilterRequestsProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties  "Filtrar solicitudes por propiedades-referencia de análisis de red | Microsoft docs"  
[DevtoolsWebauthnIndex]: /microsoft-edge/devtools-guide-chromium/webauthn/index "Emular autenticadores y depurar webauthn en Microsoft Edge DevTools | Microsoft docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de Microsoft Edge Preview"  

[VisualStudioCode]: https://code.visualstudio.com "Código de Visual Studio"  

[VisualStudioCodeMarketplaceMsEdgedevtools]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Herramientas de Microsoft Edge para Visual Studio Code | Código de Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar métodos abreviados de teclado o enlaces de clave | Errores de cromo"
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la última versión de Lighthouse | Errores de cromo"  
[CR1034663]: https://crbug.com/1034663 "Crear un front-end para la API de pruebas de webauthn | Errores de cromo"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS/Flexbox/tables de CSS | Errores de cromo"  
[CR1051466]: https://crbug.com/1051466 "Compatibilidad con COOP/depuración COEP en DevTools | Errores de cromo"  
[CR1073899]: https://crbug.com/1073899 "La pestaña de estilo calculado desaparece en modo de respuesta | Errores de cromo"  
[CR1075732]: https://crbug.com/1075732 "Personalización de DevTools: pestañas móviles | Errores de cromo"  
[CR1084673]: https://crbug.com/1084673 "DevTools: mejora la manera en que presentamos las propiedades personalizadas de CSS ((aka). Variables de CSS) y sus valores | Errores de cromo"  
[CR1093687]: https://crbug.com/1093687 "Herramienta crear y reproducir solicitudes de red sintéticas | Errores de cromo"  
[CR1096230]: https://crbug.com/1096230 "Agrupar propiedades CSS por categorías en el panel Estilos calculados | Errores de cromo"  
[CR1104188]: https://crbug.com/1104188 "La búsqueda de herramientas de red no encuentra resultados al buscar la dirección URL completa | Errores de cromo"  
[CR1106251]: https://crbug.com/1106251 "☂ DevTools: mejorar la pestaña estilos calculados | Errores de cromo"  
[CR1120316]: https://crbug.com/1120316 "Resalte mala parte del contraste en CSS Descripción > colores | Errores de cromo"  
[CR1121141]: https://crbug.com/1121141 "Permitir filtrar por tipo de recurso en el registro de red | Errores de cromo"  
[CR1121312]: https://crbug.com/1121312 "La configuración debe quitarse del menú herramientas | Errores de cromo"  
[CR1136394]: https://crbug.com/1136394 "Herramientas de Flexbox | Errores de cromo"  
[CR1136655]: https://crbug.com/1136655 "DevTools: localización V2 | Errores de cromo"  

[MdnReportingApi]: https://developer.mozilla.org/docs/Web/API/Reporting_API "API de informes | MDN"  

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-DevTools | GitHub"  

[GithubGoogleChromeLighthouseReleasesV641]: https://github.com/GoogleChrome/lighthouse/releases/v6.4.1 "v 6.4.1-GoogleChrome/Lighthouse | GitHub"  

[GithubW3cWebauthn]: https://w3c.github.io/webauthn "Autenticación Web | GitHub"  

[GlitchCssOverviewAccessibleColorsDemo]: https://css-overview-accessible-colors-demo.glitch.me "¡ Hola! | Intento"  

[PostmanSchemaJsonCollectionv210Index]: https://schema.getpostman.com/json/collection/v2.1.0/docs/index.html "Formato de colección Postman de v 2.1.0 | Postman"  

[SwaggerSpecificationV2]: https://swagger.io/specification/v2 "Especificación de OpenAPI | Swagger"  

<!--[JecFyiDemoPerfMark]: https://jec.fyi/demo/perf-mark "" -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/10/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
