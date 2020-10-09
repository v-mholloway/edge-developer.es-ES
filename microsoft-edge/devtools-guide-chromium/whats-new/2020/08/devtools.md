---
description: Hacer coincidir los métodos abreviados de teclado con el código de Visual Studio, emular Surface Duo y el plegado de Samsung Galaxy, mejoras de la cuadrícula CSS y mucho más.
title: Novedades de DevTools (Microsoft Edge 86)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 74fb4e276547d9f653a5bcbdcab9c4406d09a81a
ms.sourcegitcommit: 912609aa49864e3363aaa3b245ff2aa4bec3fc3e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104864"
---
# Novedades de DevTools (Microsoft Edge 86)  

## Anuncios del equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

### Hacer coincidir los métodos abreviados de teclado en DevTools a Visual Studio Code  

En Microsoft Edge 86, puedes hacer coincidir los métodos abreviados de teclado del DevTools con tus accesos directos en [Visual Studio Code][VisualStudioCode]. 

:::image type="complex" source="../../media/2020/08/keyboard-shortcut.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/keyboard-shortcut.msft.png":::
   Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio  
:::image-end:::  

Para activar esta característica, vaya a [personalizar los métodos abreviados de teclado en el DevTools de Microsoft Edge][DevtoolsCustomizeShortcuts].  

Por ejemplo, el método abreviado de teclado para pausar o seguir ejecutando un script en [Visual Studio Code][VisualStudioCodeShortcutsKeyboardWindows] es `F5` .  Con el valor preestablecido **DevTools (predeterminado)** , ese mismo método abreviado de DevTools es `F8` , pero cuando eliges el ajuste preestablecido de **Visual Studio** , ahora también está el método abreviado `F5` .  

[#174309][CR174309] de problemas de cromo  

### Emula Surface Duo y Samsung Galaxy Fold  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio":::
   Característica experimental  
:::image-end:::  

Ahora puede probar el aspecto de su sitio web o aplicación en dos nuevos dispositivos:  [Surface Duo][MicrosoftSurfaceDevicesDuo] y [Samsung Galaxy Foldr][SamsungMobileGalaxyFold] en Microsoft Edge.  

Para ayudar a mejorar el sitio web o la aplicación para los dispositivos de plegable y pantalla doble, usa las siguientes características al [emular el dispositivo][DevtoolsDeviceModeIndex].  

*   [Expansión][DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices], que es cuando su sitio web \ (o aplicación \) aparece en las dos pantallas.
*   [Representando la costura][DualScreenIntroductionHowWorkSeam], que es el espacio entre las dos pantallas.
*   [Habilitar las API experimentales de la plataforma web][DevtoolsExperimentalFeaturesEnableExperimentalApis] para acceder a la nueva [característica de expansión de pantalla multimedia de CSS][DualScreenWebCssMediaSpanning] y [API de getWindowSegments de JavaScript][DualScreenWebJavascriptGetwindowsegments].  

:::image type="complex" source="../../media/2020/08/surface-duo-device-emulation.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/surface-duo-device-emulation.msft.png":::
   Emulación de dispositivos para Surface Duo  
:::image-end:::  

Para activar esta característica experimental, navegue para [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a **emulación: modo de pantalla doble de soporte**.  

Para obtener más información sobre este experimento, vaya a [emulación: compatibilidad con el modo de pantalla doble][DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode].  

Problema de cromo: [#1054281][CR1054281]  

### Mejoras de superposición de cuadrícula CSS y nuevas características de cuadrícula experimental  

Agradecemos tus comentarios positivos sobre las superposiciones de cuadrícula CSS mejoradas.  Las superposiciones de cuadrícula CSS ahora están habilitadas de forma predeterminada y no requieren que se active un experimento.  

:::image type="complex" source="../../media/2020/08/css-grid-overlay-article.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/css-grid-overlay-article.msft.png":::
   Superposición de cuadrícula CSS para `article` elemento  
:::image-end:::  

> [!NOTE]
> Para obtener más información sobre las superposiciones de cuadrícula, vaya a [características de depuración de cuadrícula de CSS][DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures].  

El equipo de Microsoft Edge DevTools y el equipo de DevTools de Chrome colaboran en características adicionales.  Las nuevas características incluyen varias superposiciones que son persistentes y se pueden configurar desde un nuevo panel de **diseño** en el panel **elementos** .  

Para activar esta característica experimental, vaya a [Activar características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla situada junto a **Habilitar nuevas características de depuración de cuadrícula CSS (opciones de configuración disponibles en el panel de la barra lateral de diseño en elementos después de reiniciar)**.  

Para obtener más información sobre este experimento, navegue para [Habilitar nuevas características de depuración de cuadrícula CSS][DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures].  

Problema de cromo: [#1047356][CR1047356]  

### La tabla copiada de la consola conserva el formato  

En Microsoft Edge 85 o versiones anteriores, se perdió el formato de una copiada `console.table` .  Si ha copiado el resultado de la API de consola de [tabla][DevtoolsConsoleApiTable] y lo ha pegado, solo se conservará el texto de la tabla.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/console-table-beta.msft.png":::
         `table` Salida de la API de consola en Microsoft Edge 85 o versiones anteriores  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/console-table-beta-paste-visual-studio-code.msft.png":::
         `table` Salida de la API de consola de Microsoft Edge 85 o versiones anteriores pegadas en código de Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

En Microsoft Edge 86 o posterior, al copiar una tabla desde la **consola**, se conserva el formato.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/console-table-canary.msft.png":::
         `table` Salida de la API de consola en Microsoft Edge 86 o posterior  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/console-table-canary-paste-visual-studio-code.msft.png":::
         `table` Salida de la API de consola de Microsoft Edge 86 o posterior pegada en el código de Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Error de cromo: [#1115011] [CR1115011]  

### Visor de pedidos de origen para realizar pruebas de accesibilidad más sencillas  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio":::
   Característica experimental  
:::image-end:::  

La nueva aplicación auxiliar de accesibilidad muestra el orden de los elementos en el origen.  

:::image type="complex" source="../../media/2020/08/source-order-viewer.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/source-order-viewer.msft.png":::
   Activar **Mostrar orden de origen**  
:::image-end:::  

Esta característica hace que sea más fácil comprobar la forma en que los usuarios del teclado y el lector de pantalla experimentan su sitio web o aplicación.  Los lectores de pantalla y la navegación mediante teclado dependen del contenido que se coloca en un orden determinado en el código fuente de su sitio web o aplicación, de modo que coincida con la página representada.  El visor del pedido de origen muestra posibles diferencias en el orden entre la página representada y el código fuente.  

Para activar esta característica experimental, navegue para [activar las características experimentales][DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures] y seleccione la casilla que se encuentra junto a **Habilitar el visor de orden de origen**.  

Para obtener más información sobre este experimento, vaya a [Habilitar el visor de orden de origen][DevtoolsExperimentalFeaturesEnableSourceOrderViewer].  

Problema de cromo: [#1094406][CR1094406]  

<!--
### DevTools language enhancements  

Your feedback and internal discoveries uncovered which text strings used in the Microsoft Edge feedback should remain untranslated or create confusion when translated.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-stable.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="localization-improvements-chinese-complex-stable.msft.png":::
         Microsoft Edge DevTools 85 and earlier in Traditional Chinese  
      :::image-end:::  
   :::column-end:::  
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/localization-improvements-chinese-complex-canary.msft.png":::
         Microsoft Edge DevTools 86  or later in Traditional Chinese  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

To meet your translation needs, the Microsoft Edge DevTools team is focused on improving translation quality.  

The current effort to improve translation quality enables easier support for more languages in the future.  
-->  

### Resaltar todos los resultados de búsqueda en la herramienta elementos  

En Microsoft Edge 84 y 85, el primer resultado de búsqueda en el panel **elementos** no resaltado.  El resto de los resultados de la búsqueda estaban resaltados correctamente.  

Gracias por enviar tus comentarios y de mejorar el cromo.  Su comentario no cubierto [#1103316][CR1103316] problema en el proyecto de cromo de código abierto.  

:::image type="complex" source="../../media/2020/08/elements- search-highlight-fixed.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/elements- search-highlight-fixed.msft.png":::
   Primer resultado de búsqueda resaltado en el panel **elementos** en Microsoft Edge 84 o posterior  
:::image-end:::  

Ahora el problema se ha corregido en todas las versiones de Microsoft Edge.  

Problema de cromo: [#1103316][CR1103316]  

## Anuncios del proyecto de cromo  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nuevo panel multimedia  

DevTools ahora muestra la información de los reproductores multimedia en el panel [multimedia][DevtoolsMediaPanelIndex] .  

Para abrir el nuevo panel **multimedia** , complete el paso siguiente.  

1.  Elija **personalizar y controlar DevTools** \ ( `...` \) > **más**  >  **medios**de herramientas.  
    
    :::image type="complex" source="../../media/2020/08/media-panel.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/media-panel.msft.png":::
       Nuevo panel **multimedia**  
    :::image-end:::  

Antes del nuevo panel **multimedia** de DevTools, la información de registro y depuración de los reproductores de vídeo se encontró en la configuración de **reproductores recientes** .  Para abrir la configuración de **reproductores recientes** , vaya a `edge://media-internals` la ficha **reproductores** y elija.  

Ver contenido en vivo e inspeccionar problemas potenciales más rápidamente, incluidos los siguientes ejemplos.  

*   ¿Por qué se eliminan los marcos?  
*   ¿Por qué JavaScript interactúa con el reproductor de forma inesperada?  

### Captura de capturas de nodo con el menú contextual del panel de elementos  

Ahora puede capturar capturas de pantalla de nodo usando el menú contextual en el panel **elementos** .  

Por ejemplo, para tomar una captura de pantalla de la tabla de contenido, mantenga el puntero sobre el elemento, abra el menú contextual \ (haga clic con el botón derecho \) y seleccione **capturar nodo captura de pantalla**.  

:::image type="complex" source="../../media/2020/08/capture-node-screenshot.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/capture-node-screenshot.msft.png":::
   Capturar capturas de nodo  
:::image-end:::  

Problema de cromo: [#1100253][CR1100253]  

### Actualizaciones de la herramienta problemas  

La barra de advertencias de problemas del panel de la **consola** se reemplaza por un mensaje normal.  

<!--todo: this figure need to be updated  -->  

:::image type="complex" source="../../media/2020/08/issue-console-msg.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/issue-console-msg.msft.png":::
   Problemas en el mensaje de consola  
:::image-end:::  

Los problemas de cookies de terceros ahora están ocultos de forma predeterminada en la herramienta **problemas** .  Active la casilla **incluir problemas de cookie de terceros** para ver los problemas.  

:::image type="complex" source="../../media/2020/08/third-party-cookies.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/third-party-cookies.msft.png":::
   casilla de verificación de problemas de cookies de terceros  
:::image-end:::  

Problemas de cromo: [1096481][CR1096481], [1068116][CR1068116], [1080589][CR1080589]  

### Emular las fuentes locales que faltan  

Abra la [herramienta de representación][DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance] y use la nueva característica **deshabilitar fuentes locales** para emular los orígenes que faltan `local()` en `@font-face` las reglas.  

Por ejemplo, cuando la `Rubik` fuente está instalada en el dispositivo y la `@font-face src` regla la usa como `local()` fuente, Microsoft Edge usa el archivo de fuente local del dispositivo.  

Cuando **deshabilitar fuentes locales** está habilitado, DevTools ignora las `local()` fuentes y las recupera desde la red.  

:::image type="complex" source="../../media/2020/08/disable-font.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/disable-font.msft.png":::
   Emular las fuentes locales que faltan  
:::image-end:::  

Si usa dos copias diferentes de la misma fuente durante el desarrollo, como los siguientes ejemplos.  

*   Una fuente local para las herramientas de diseño.  
*   Una fuente web para tu código.  

Use **deshabilitar fuentes locales** para que le resulte más fácil completar las siguientes tareas.  

*   Depure y mida el rendimiento de carga y la optimización de fuentes web.  
*   Verifica la precisión de las `@font-face` reglas de CSS.  
*   Descubra las diferencias entre las versiones locales instaladas en el dispositivo y una fuente web.  

Problema de cromo: [#384968][CR384968]  

### Emular usuarios inactivos  

La [API de detección de inactividad][WebDevIdleDetection] permite a los programadores detectar usuarios inactivos y reaccionar según los cambios de estado de inactividad.  Ahora puede usar DevTools para emular los cambios de estado de inactividad en la herramienta **sensores** para el estado del usuario y el estado de la pantalla en lugar de esperar a que cambie el estado real de inactividad.  Puede abrir la herramienta de **sensores** desde el [cajón][DevtoolsCustomizeIndexDrawer].  

:::image type="complex" source="../../media/2020/08/emulate-idle.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/emulate-idle.msft.png":::
   Emular usuarios inactivos  
:::image-end:::  

Problema de cromo: [#1090802][CR1090802]  

### Emular preferidos: datos reducidos  

> [!NOTE]
> En Microsoft Edge 86, para habilitar esta característica, vaya a `edge://flags#enable-experimental-web-platform-features` la bandera **experimental características de plataforma web** y enciéndala.  La opción de emulación solo se muestra si la marca está habilitada.  

La consulta de medios de [datos preferidos-datos][CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData] detecta las preferencias de contenido de usuario para reducir los datos.  Si se selecciona, el usuario recibe contenido de página alternativo que usa menos datos.  

Ahora puede usar DevTools para emular la `prefers-reduced-data` consulta multimedia.  

:::image type="complex" source="../../media/2020/08/emulate-prefers-reduced-data.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/emulate-prefers-reduced-data.msft.png":::
   Emular preferidos: datos reducidos  
:::image-end:::  

Problema de cromo: [#1096068][CR1096068]  

### Compatibilidad con las nuevas características de JavaScript  

DevTools ahora admite las siguientes características del lenguaje JavaScript.  

| Característica del lenguaje JavaScript | Detalles |  
|:--- |:--- |  
| [Operadores de asignación lógica][V8FeaturesLogicalAssignment] | DevTools ahora admite la asignación lógica con los `&&=` operadores New, `||=` y `??=` en los paneles **Console (consola** ) y **Sources (orígenes** ).  |  
| [Separadores numéricos][V8FeaturesNumericSeparators] muy imprimibles | DevTools ahora correctamente: imprime los separadores numéricos en el panel **fuentes** .  |  

Problemas de cromo: [1086817][CR1086817], [1080569][CR1080569]  

### Lighthouse 6,2 en el panel de Lighthouse  

El panel de **Lighthouse** ahora se ejecuta Lighthouse 6,2.  Para obtener una lista completa de los cambios, vaya a las notas de la [versión de Lighthouse][GithubGooglechromeLighthouseV620].  

Problema de cromo: [#772558][CR772558]  

### Desuso de otras listas de orígenes en el panel de trabajo de servicios  

DevTools ahora proporciona un vínculo desde el panel de **trabajo de servicios** \ (panel de**aplicaciones** > panel de **trabajo de servicios** \) para ver la lista completa de trabajadores de servicios de otros orígenes.  Para acceder a la lista sin abrir la DevTools, vaya a `edge://service-worker-internals/?devtools` .  

Anteriormente, DevTools mostrado una lista anidada en el panel de **aplicaciones** > panel de **trabajo de servicios** .  

:::image type="complex" source="../../media/2020/08/sw-other-origins.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/sw-other-origins.msft.png":::
   Vincular a otros orígenes  
:::image-end:::  

Problema de cromo: [#807440][CR807440]  

### Mostrar Resumen de cobertura para elementos filtrados  

DevTools ahora recalcular y mostrar un resumen de la información de cobertura de forma dinámica.  La pantalla dinámica se desencadena cuando se aplican filtros en la herramienta de [cobertura][DevtoolsCoverageIndex] .  Antes de que la herramienta de **cobertura** siempre muestre un resumen de toda la información de cobertura.  

En la primera de las siguientes figuras, el resumen se muestra inicialmente `344 kB of 1.7 MB (20%) used so far.  1.4 MB unused.` y en el segundo de las siguientes figuras, el Resumen `26.8 kB of 408 kB (7%) used so far.  381 kB unused.` se muestra después de aplicar el filtrado CSS.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/coverage-compare.msft.png":::
         Resumen de la cobertura  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/coverage-compare-css-filter.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/coverage-compare-css-filter.msft.png":::
         Resumen de la cobertura de los elementos filtrados  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Problema de cromo: [#1061385][CR1090802]  

### Vista de detalles del nuevo marco en el panel de aplicación  

DevTools ahora mostrar una vista detallada de cada marco.  Para acceder a ella, elija un marco en el menú **Marcos** en el panel **aplicación** .  

:::image type="complex" source="../../media/2020/08/frame-details.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/frame-details.msft.png":::
   Nueva vista detallada de un marco en el panel de **aplicaciones**  
:::image-end:::  

Problema de cromo: [#1093247][CR1093247]  

#### Detalles de trama para las ventanas abiertas  

Las ventanas abiertas y las ventanas emergentes se muestran ahora también en el árbol de Marcos.  La vista detallada de las ventanas abiertas incluye información de seguridad adicional.  

:::image type="complex" source="../../media/2020/08/window-opener.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/window-opener.msft.png":::
   Vista detallada de nuevo marco para ventanas abiertas  
:::image-end:::  

Error de cromo: [#1107766] [CR1107766]  

#### Información de seguridad y aislamiento  

En los detalles de la trama, ahora se muestra el contexto seguro, la [Directiva de origen cruzado-Embedder (COEP)][WebDevCoopCoep]y las [directivas de apertura cruzada entre orígenes (COOP)][WebDevCoopCoep] .  

:::image type="complex" source="../../media/2020/08/coep-coop.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/coep-coop.msft.png":::
   Información de seguridad y aislamiento  
:::image-end:::  

En el futuro, el equipo de Microsoft Edge DevTools y el equipo de Chrome DevTools planean agregar más información de seguridad a los detalles del marco.  

Problema de cromo: [#1051466][CR1051466]  

### Elementos y actualizaciones del panel de red  

#### Sugerencia de color accesible en el panel estilos  

DevTools ahora ofrece sugerencias de color para el texto de contraste de color bajo.  

En el ejemplo siguiente, `h1` hay texto de bajo contraste.  Para corregirlo, abra el selector de color de la `color` propiedad en el panel **estilos** .  Después de expandir la sección **relación de contraste** , DevTools ofrece sugerencias de color AA y AAA.  Seleccione el color sugerido para aplicar el color.  

:::image type="complex" source="../../media/2020/08/contrast-color-suggestion.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/contrast-color-suggestion.msft.png":::
   El selector de colores sugiere sugerencias de color AA y AAA  
:::image-end:::  

Problema de cromo: [#1093227][CR1093227]  

#### Panel de propiedades de restablecer en el panel elementos  

El panel **propiedades** está atrás.  Quedó [obsoleto en Microsoft Edge 84][DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel].  El equipo de Microsoft Edge DevTools y el equipo de Chrome DevTools están planeando las mejoras para inspeccionar las propiedades de los elementos.  

:::image type="complex" source="../../media/2020/08/properties-pane.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/properties-pane.msft.png":::
   Panel de **propiedades** en el panel **elementos**  
:::image-end:::  

Problema de cromo:  <!--  [#1105205][CR1105205],  -->  [#1116085] [CR1116085]  

<!--  
#### Human-readable X-Client-Data header values in the Network panel  

When inspecting a network resource in the Network panel, DevTools now formats any `X-Client-Data` header values in **Headers** pane as code.  

The `X-Client-Data` HTTP header contains a list of experiment IDs and Microsoft Edge flags that are enabled in your browser.  The raw header values look like opaque strings since the values are `base-64-encoded`, serialized [protocol buffers][GoogleDevelopersProtocolBuffers].  To make the contents more transparent to developers, DevTools now shows the decoded values.  

:::image type="complex" source="../../media/2020/08/x-client-data.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/x-client-data.msft.png":::
   Human-readable `X-Client-Data` header values  
:::image-end:::  

Chromium issue: [#1103854][CR1103854]  
-->  

#### Autocompletar fuentes personalizadas en el panel estilos  

Las caras de las fuentes importadas se agregan ahora a la lista de autocompletar CSS al editar la `font-family` propiedad en el panel **estilos** .  

Por ejemplo, si `monospace` es una fuente personalizada instalada en la máquina local, se muestra en la lista de finalización de CSS. En versiones anteriores de Microsoft Edge, no se mostraba la fuente.

:::image type="complex" source="../../media/2020/08/font-auto-complete.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/font-auto-complete.msft.png":::
   Autocompletar fuentes personalizadas  
:::image-end:::  

Error de cromo: [#1106221] [CR1106221]  

#### Mostrar el tipo de recurso de forma coherente en el panel red  

DevTools ahora muestra el mismo tipo de recurso que la solicitud de red original y anexa `/ Redirect` al valor de la columna **Type** cuando el redireccionamiento ha transformado \ (código de estado http 302 \).  

Anteriormente DevTools cambiado el tipo a `Other` veces.  

:::image type="complex" source="../../media/2020/08/network-redirect.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/network-redirect.msft.png":::
   Mostrar tipo de recurso de redirección  
:::image-end:::  

Problema de cromo: [#997694][CR997694]  

#### Botones borrar en los paneles elementos y red  

Los siguientes cuadros de texto ahora tienen botones **claros** .  

*   Los cuadros de texto de filtro en el panel **estilos** y en el panel **red** .  
*   Cuadro de texto de búsqueda de DOM en el panel **elementos** .  

Haga clic en el botón **Borrar** para quitar el texto de la imagen.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-elements.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/clear-button-elements.msft.png":::
         Botones Borrar de los paneles **elementos**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/08/clear-button-network.msft.png" alt-text="Hacer coincidir los métodos abreviados de teclado en el código de DevTools a Visual Studio" lightbox="../../media/2020/08/clear-button-network.msft.png":::
         Botones borrar en los paneles de **red**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Problema de cromo: [#1067184][CR1067184]  

## Descargar los canales de Microsoft Edge Preview  

Si está en Windows o macOS, considere la posibilidad de usar los [canales de Microsoft Edge Preview][MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- image links -->  

[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png "Icono configuración de DevTools"  

<!-- links -->  

[DevtoolsWhatsnew200205DevtoolsDeprecationPropertiesPaneElementsPanel]: ../05/devtools.md#deprecation-of-the-properties-pane-in-the-elements-panel "Desuso del panel de propiedades en el panel de elementos: novedades de DevTools (Microsoft Edge 84) | Microsoft docs"  
[DevtoolsWhatsnew200206DevtoolsCssGridDebuggingFeatures]: ../06/devtools.md#css-grid-debugging-features "Características de depuración de la cuadrícula CSS: novedades de DevTools (Microsoft Edge 85) | Microsoft docs"  

[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomizeShortcuts]: /microsoft-edge/devtools-guide-chromium/customize/shortcuts "Personalizar los métodos abreviados de teclado en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableExperimentalApis]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-experimental-apis "Habilitar las API experimentales: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableNewCssGridDebuggingFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-new-css-grid-debugging-features "Emulación: compatibilidad con el modo de pantalla dual-características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableSourceOrderViewer]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-source-order-viewer "Habilitar visor de pedidos de origen-características experimentales | Microsoft docs"
[DevtoolsExperimentalFeaturesEmulationSupportDualScreenMode]: https://review.docs.microsoft.com/microsoft-edge/devtools-guide-chromium/experimental-features?branch=user/zoghadya/dual-screen-experiment#emulation-support-dual-screen-mode "Emulación: compatibilidad con el modo de pantalla dual-características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesTestingOnFoldableDualScreenDevices]: /microsoft-edge/devtools-guide-chromium/experimental-features#testing-on-foldable-and-dual-screen-devices "Pruebas en dispositivos de plegable y dos pantallas: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnExperimentalFeatures]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activar características experimentales: características experimentales | Microsoft docs"  
[DevtoolsConsoleApiTable]: /microsoft-edge/devtools-guide-chromium/console/api#table "tabla-referencia de API de consola | Microsoft docs"  
[DevtoolsCoverageIndex]: /microsoft-edge/devtools-guide-chromium/coverage/index "Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Cajón-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsEvaluatePerformanceReferenceAnalyzeRenderingPerformance]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Analizar el rendimiento de la representación con la pestaña representación, referencia de análisis de rendimiento | Microsoft docs"  
[DevtoolsMediaPanelIndex]: /microsoft-edge/devtools-guide-chromium/media-panel/index "Ver y depurar información de reproductores multimedia | Microsoft docs"  

[DualScreenIntroductionHowWorkSeam]:  /dual-screen/introduction#how-to-work-with-the-seam "Cómo trabajar con las costuras-Introducción a los dispositivos de doble pantalla | Microsoft docs"  
[DualScreenWebCssMediaSpanning]: /dual-screen/web/css-media-spanning "Característica de expansión de pantalla multimedia CSS para detección de pantalla doble | Microsoft docs"  
[DualScreenWebJavascriptGetwindowsegments]: /dual-screen/web/javascript-getwindowsegments "La API de JavaScript de getWindowSegments para dispositivos de doble pantalla | Microsoft docs"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de Microsoft Edge Preview"  

[VisualStudioCode]: https://code.visualstudio.com "Código de Visual Studio "  
[VisualStudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Métodos abreviados de teclado de código de Visual Studio para Windows"  

[MicrosoftSurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "La nueva superficie Duo"  

[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools cuenta de Twitter"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"  

[CR174309]: https://crbug.com/174309 "DevTools: permitir personalizar métodos abreviados de teclado o enlaces de clave | Errores de cromo"
[CR384968]: https://crbug.com/384968 "Opción para omitir las fuentes locales () | Errores de cromo"  
[CR772558]: https://crbug.com/772558 "DevTools: actualizar a la última versión de Lighthouse | Errores de cromo"  
[CR807440]: https://crbug.com/807440 "Chrome se bloquea con grandes cantidades de SWs | Errores de cromo"  
[CR997694]: https://crbug.com/997694 "Las solicitudes de XHR con el estado 302 no se muestran en el filtro \ "XHR \" en el panel red | Errores de cromo"  
[CR1047356]: https://crbug.com/1047356 "Herramientas CSS/Flexbox/Table de CSS"  
[CR1051466]: https://crbug.com/1051466 "Compatibilidad con COOP/depuración COEP en DevTools | Errores de cromo"  
[CR1054281]: https://crbug.com/1054281 "Solicitud de característica: DevTools debe emular plegable y dispositivos de pantalla dual | Errores de cromo"  
[CR1067184]: https://crbug.com/1067184 "Solicitud de característica: botón Borrar filtro en los elementos del & de red: entradas del filtro de estilo de > | Errores de cromo"  
[CR1068116]: https://crbug.com/1068116 "Panel de problemas de envío de ☂ | Errores de cromo"  
[CR1080569]: https://crbug.com/1080569 "ACORN no admite operadores de asignación lógica | Errores de cromo"  
[CR1080589]: https://crbug.com/1080589 "Clasificar problemas por terceros o por terceros | Errores de cromo"  
[CR1086817]: https://crbug.com/1086817 "ACORN no admite separadores numéricos | Errores de cromo"  
[CR1090802]: https://crbug.com/1090802 "Simular cambios de estado de inactividad de API de detección de inactividad | Errores de cromo"  
[CR1093227]: https://crbug.com/1093227 "DevTools: sugerir color más accesible | Errores de cromo"  
[CR1093247]: https://crbug.com/1093247 "Mostrar información sobre marcos en el panel aplicación | Errores de cromo"  
[CR1094406]: https://crbug.com/1094406 "Los desarrolladores desean un visor de pedidos de origen para al https://webwewant.fyi/wants/64/"  
[CR1096068]: https://crbug.com/1096068 "DevTools: compatibilidad emulando la característica de medios de datos preferidos, menos-datos | Errores de cromo"  
[CR1096481]: https://crbug.com/1096481 "Ubicación del banner de problemas | Errores de cromo"  
[CR1100253]: https://crbug.com/1100253 "Agregar acceso directo al nodo de captura en el menú contextual del elemento | Errores de cromo"  
[CR1103316]: https://crbug.com/1103316 "La búsqueda de elementos no resolveNode (resaltar texto, etc.) en el primer resultado de búsqueda | Errores de cromo"  
[CR1103854]: https://crbug.com/1103854 "Desproteger los valores de datos de X-Client en herramientas para desarrolladores | Errores de cromo"  
<!--  [CR1105205]: https://crbug.com/1105205 "Issue 1105205 | Chromium bugs"  -->  
[CR1106221]: https://crbug.com/1106221 "agregar fuentes importadas a la autocompletada de la familia de fuentes en el panel estilos | Errores de cromo "  
[CR1107766]: https://crbug.com/1107766 "Mostrar información sobre fotogramas generados por" Window. Open () "en árbol de marcos | Errores de cromo "  
[CR1115011]: https://crbug.com/1115011 "al copiar una tabla desde la consola, no se conserva la estructura de la tabla | Errores de cromo "  
[CR1116085]: https://crbug.com/1116085 "vuelve al inspector de propiedades de DevTools | Errores de cromo "  

[CsswgDraftsMediaqueries5DescdefMediaPrefersReducedData]: https://drafts.csswg.org/mediaqueries-5#descdef-media-prefers-reduced-data "preferidas, menos-consultas de medios de datos nivel 5 | Borradores del editor del grupo de trabajo CSS W3C"  

[GithubGooglechromeLighthouseV620]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.2.0 "v 6.2.0-GoogleChrome/Lighthouse | GitHub"  

[GoogleDevelopersProtocolBuffers]: https://developers.google.com/protocol-buffers "Búferes de protocolo | Desarrolladores de Google"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/us/mobile/galaxy-fold "Plegado de Galaxy | Samsung, Estados Unidos"  

[V8FeaturesLogicalAssignment]: https://v8.dev/features/logical-assignment "Asignación lógica | V8"  
[V8FeaturesNumericSeparators]: https://v8.dev/features/numeric-separators "Separadores numéricos | V8"  

[WebDevCoopCoep]: https://web.dev/coop-coep "Cómo convertir tu sitio web \ "aislamiento de origen cruzado \" usando COOP y COEP | Web. dev"  
[WebDevIdleDetection]: https://web.dev/idle-detection "Detectar usuarios inactivos con la API de detección de inactividad | Web. dev"  
[WebDevNonCompositedAnimations]: https://web.dev/non-composited-animations "Evitar animaciones no compuestas | Web. dev"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/08/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
