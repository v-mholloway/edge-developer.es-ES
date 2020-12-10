---
description: Microsoft Edge en Linux, sugerencias de webhint mejoradas en la herramienta problemas, nuevas características de depuración de trabajo de servicio y más.
title: Novedades de DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 500b64e7b51e0f02c9fcbcb7a83e8273b3a5a0d7
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2020
ms.locfileid: "11205246"
---
# Novedades de DevTools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Microsoft Edge y el controlador Microsoft Edge ahora están disponibles en Linux  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

Microsoft Edge dev ahora es compatible con las distribuciones Ubuntu, Debian, Fedora y openSUSE.  Descarga e instala el programa o el `.deb` `.rpm` paquete de Microsoft Edge directamente desde el [sitio de Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] o usa las herramientas de administración de paquetes estándar de tu distribución de Linux.  

Si está usando un entorno Linux en sus soluciones de integración y entrega continuas \ (CI/CD \), el controlador Microsoft Edge también está disponible en Linux.  Para empezar a automatizar Microsoft Edge dev con el controlador de Microsoft Edge, vaya a la [Página de descargas del controlador de Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Para obtener ayuda con la automatización de Microsoft Edge dev junto con el controlador de Microsoft Edge, navegue para [usar Webdriver (cromo) para la automatización de prueba][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools en Microsoft Edge en Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools en Microsoft Edge en Linux  
:::image-end:::  

## Sugerencias de webhint y de plataforma mejoradas en la herramienta problemas  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Una herramienta de código abierto, [webhint][WebhintMain], proporciona comentarios en tiempo real para sitios web y páginas web locales.  A partir de la [versión 85 de Microsoft Edge][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], revise los comentarios de webhint en la herramienta [problemas][DevtoolsIssuesIndex] .  Los problemas que aparecen en la herramienta **problemas** ahora son más fáciles de revisar con la adición de las siguientes categorías.  

*   [Accesibilidad][WebhintUserGuideHintsAccessibility]  
*   [Compatibilidad][WebhintUserGuideHintsCompatibility]  
*   [Rendimiento][WebhintUserGuideHintsPerformance]  
*   [Problemas][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Seguridad][WebhintUserGuideHintsSecurity]  
    
Ahora puede filtrar problemas de terceros mediante una nueva casilla.  La funcionalidad de filtro le ayuda a ocultar problemas relacionados con el código de bibliotecas de terceros u otros orígenes.  

Para ayudarle a revisar los problemas que revela [webhint][WebhintMain], la herramienta **problemas** ahora muestra la siguiente información.  

*   Fragmentos de código mejorados.  
*   Vínculos a otros paneles relevantes.  
*   Vínculos a la documentación para ayudarle a solucionar problemas de su sitio Web.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Herramienta problemas" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   Herramienta **problemas**  
:::image-end:::  

## Las capas compuestas ahora se encuentran en la vista 3D  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

Ahora puede visualizar el contenido de las **capas** junto con los valores de índice z y el modelo de objeto de documento \ (Dom \).  Esta característica le ayuda a depurar sin cambiar entre la [vista 3D][Devtools3dViewIndex] y las herramientas de **capas** con frecuencia.  Para obtener una experiencia de depuración visual completa, [ahora se combinan la vista 3D y las capas compuestas][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Panel capas compuestas" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Panel **capas compuestas**  
:::image-end:::  

## Definiciones de variables CSS en el panel estilos  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

En el panel **estilos** , [las variables CSS][MdnUsingCssCustomProperties] ahora se vinculan directamente a cada definición.  Elija la variable para ver o cambiar fácilmente la definición de la variable CSS.  En el ejemplo, DevTools muestra los atributos CSS para el `body` elemento.  Para mostrar la definición de variable de la `--theme-body-background` variable CSS, complete las siguientes acciones.  

1.  En el panel **estilos** , elija `var(--theme-body-background)` .  
1.  El panel **estilos** ahora muestra la definición de la `--theme-body-background` variable CSS.  
    
:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support.msft.png" alt-text="Variable CSS vinculada al estilo" lightbox="../../media/2020/11/css-variable-support.msft.png":::
         Variable CSS vinculada al estilo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/css-variable-support-target.msft.png" alt-text="Variable CSS vinculada al destino de estilo" lightbox="../../media/2020/11/css-variable-support-target.msft.png":::
         Variable CSS vinculada al destino de estilo  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Mejoras en la depuración de trabajos de servicio  

<!-- Title:  Service worker debugging improvements in the Network, Application, and Sources tools  -->  
<!-- Subtitle:  Making service workers easier to debug for progressive web applications and more.  -->  

Las siguientes características nuevas de las herramientas de [redes](#network-tool), [aplicaciones](#application-tool)y [fuentes](#sources-tool) le ayudan a crear su [PWA][ProgressiveWebAppsChromiumIndex].  Use las siguientes características cuando tenga dificultades para depurar el trabajo del servicio.  

Enrutamiento de solicitudes muestra `startup` los `fetch` eventos y en función de las solicitudes de red que se ejecutan a través de los trabajos de servicio.  Se obtiene acceso a las escalas de tiempo desde la herramienta **aplicación** o **red** .  La ayuda de las escalas de tiempo cuando tienes problemas con los trabajadores del servicio y deseas ver si hay algún problema con el `startup` `fetch` evento o.  

### Herramienta de aplicación  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Vea la información de enrutamiento de toda la solicitud de trabajo de servicio con el vínculo nuevas **solicitudes de red** .  Para mostrar contexto adicional al depurar el trabajo del servicio, complete las siguientes acciones.  

1.  Vaya a los trabajadores del servicio de **aplicaciones**  >  ****.  
1.  Elija **solicitudes de red**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Abrir la herramienta de red desde el panel de trabajo de servicios" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Abrir la herramienta de **red** desde el panel de **trabajo de servicios**
    :::image-end:::  
    
1.  La herramienta **red** se abre en el **cajón** y muestra todas las solicitudes de red relacionadas con los trabajadores del servicio.  Las solicitudes de red se filtran mediante `is:service-worker-intercepted` .  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Herramienta de red del cajón" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       Herramienta de **red** del **cajón**  
    :::image-end:::
    
1. Para volver a la herramienta de **red** en el panel superior, cierre el **cajón**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Cerrar el cajón para devolver la herramienta red" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Cerrar el **cajón** para devolver la herramienta **red**  
    :::image-end:::  
    
### Herramienta red  

Depure las solicitudes de red que se ejecutan a través de los trabajos de servicio.  También puede abrir solicitudes de red desde la herramienta de la **aplicación** .  Para cada solicitud, DevTools Mostrar la siguiente información en el panel [intervalos][DevtoolsNetworkReferenceViewTimingBreakdownRequest] .  

*   El inicio de una solicitud y la duración del bootstrap.  
*   Cambios en el registro de trabajadores del servicio.  
*   El Runtime de un `fetch` controlador de eventos.  
*   El motor en tiempo de ejecución de todos los `fetch` eventos para cargar un cliente.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Panel intervalos" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Panel **intervalos**  
:::image-end:::  

### Herramienta orígenes  

En versiones anteriores de Microsoft Edge, el nivel de profundidad en la pila de llamadas estaba limitado al código de JavaScript en el trabajo del servicio.  En Microsoft Edge 88, la pila de llamadas ahora muestra el iniciador de solicitudes que se ejecutan a través del trabajo del servicio.  

Para localizar el iniciador de la solicitud, usa la pila de llamadas de tu código de JavaScript en el trabajo del servicio.  La pila de llamadas de las siguientes figuras comienza con el código de JavaScript en el trabajo del servicio y muestra una referencia a la solicitud original de la Página Web `(index):157` .  En la segunda figura, se elige la referencia y se abre el iniciador que realizó la solicitud.  El iniciador de la segunda figura es la Página Web.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="El remitente de la solicitud de resaltado de pila de llamadas y archivos de service-worker.js" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         El `service-worker.js` originador de solicitudes de resaltado de pila de llamadas y archivos  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="La página web (índice) es el iniciador de la solicitud" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         La `(index)` Página Web es el iniciador de solicitudes  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Copiar el valor de la propiedad de una solicitud de red  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

En la herramienta **red** , copie el valor de la propiedad de una solicitud de red con la opción nuevo **valor de copiado** .  El valor de la propiedad se copia como un valor JSON descodificado.  En versiones anteriores de Microsoft Edge, tenía que copiar un valor con una de las siguientes acciones.  

*   Resaltar todo el texto y copiarlo.  
*   Almacene el valor como variable global, según sea el caso, y cópielo desde la [consola][DevtoolsConsoleIndex]de DevTools.  
    
Para copiar el valor de la propiedad en el portapapeles, desplácese hasta [copiar JSON de respuesta con formato en el portapapeles][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1132084][CR1132084].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copiar el valor de la propiedad en DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Copiar el valor de la propiedad en DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Pegar el valor de la propiedad en código de Visual Studio" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Pegar el valor de la propiedad en código de Visual Studio  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Personalizar métodos abreviados de teclado de pulsación múltiple  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[Desde Microsoft Edge versión 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], puede personalizar los métodos abreviados de teclado para cualquier acción en DevTools.  En Microsoft Edge versión 88, ahora puede crear métodos abreviados de teclado de varios clics.  Para establecer un método abreviado para una acción en el DevTools, vaya a experimentos de [configuración][DevtoolsCustomizeIndexSettings]  >  **** y elija la casilla situada junto a **Habilitar el editor de métodos abreviados de teclado**.  Para obtener más información sobre la personalización y la edición de accesos directos, vaya a [Habilitar la característica experimental editor de método abreviado de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Por ejemplo, el resaltado rojo muestra un método abreviado de teclado con varias pulsaciones personalizado para la acción **iniciar grabación de eventos** .  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a [#174309 de problemas][CR174309].  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Métodos abreviados de teclado para cuerda" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Métodos abreviados de teclado de varias pulsaciones  
:::image-end:::  

## Anuncios del proyecto de cromo  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nuevas herramientas de visualización de ángulos CSS  

DevTools ahora es más compatible con la depuración de ángulos de CSS.  Cuando se aplica un ángulo CSS a un elemento HTML de la página, se muestra un icono de reloj junto al ángulo en la herramienta **estilos** .  Para activar o desactivar la superposición de reloj, elija el icono de reloj.  Para cambiar el ángulo, seleccione cualquier lugar del reloj o arrastre la aguja.  Para cambiar el valor de ángulo, también puede usar los métodos abreviados de teclado y el mouse.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a los problemas [1126178][CR1126178] y [1138633][CR1138633].  

<!--todo:  add link when css angle clock section exists.  -->  

Para el ejemplo se usa el siguiente ángulo de CSS.  

```css
background: linear-gradient(100deg, lightblue, pink);
```  

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Ángulo CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   Ángulo CSS  
:::image-end:::  

### Simular tamaño de la cuota de almacenamiento en el panel almacenamiento  

Ahora puede invalidar el tamaño de la cuota de almacenamiento en el panel **almacenamiento** .  Esta característica te permite simular diferentes dispositivos y probar el comportamiento de tu sitio web o aplicación en escenarios de disponibilidad de espacio reducido.  Para simular la cuota de almacenamiento, complete las siguientes acciones.  

1.  Vaya a ****  >  **almacenamiento**de aplicaciones.  
1.  Active la casilla **simular cuota de almacenamiento personalizada** .  
1.  Escribe un número válido.  
    
Para obtener más información sobre cómo emular dispositivos móviles y otras características de la DevTools, vaya a [emular dispositivos móviles en Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a los problemas [945786][CR945786] y [1146985][CR1146985].  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simular tamaño de la cuota de almacenamiento" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Simular tamaño de la cuota de almacenamiento  
:::image-end:::  

### Notificar errores de CORS en la herramienta red  

Para probar esta característica, navegue a la [demostración de error de CORS][GlitchCorsErrors].  Abra la herramienta **red** , actualice la página y observe la solicitud de red de CORS errónea.  En la columna Estado se muestra el **error de CORS**.  Al desplazar el puntero sobre el error, la información sobre herramientas muestra ahora el código de error.  En Microsoft Edge versión 87 y anteriores, DevTools solo se muestra el estado Generic **(Failed)** para los errores de CORS.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya al problema [1141824][CR1141824].  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Errores de CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   Errores de CORS  
:::image-end:::  

### Actualización de la vista de detalles del marco  

#### Información de aislamiento entre orígenes en la vista detalles del marco  

El estado aislado de origen se muestra ahora en la sección **aislamiento del & de seguridad** .  La nueva sección **disponibilidad de API** muestra la disponibilidad de `SharedArrayBuffer` s \ (Sab \) y si los búferes se pueden compartir mediante `postMessage()` .  Se muestra una advertencia de desuso si SAB y `postMessage()` está disponible en este momento, pero el contexto no está aislado de origen cruzado.  Para obtener más información sobre el aislamiento entre orígenes y por qué es necesario para características como `SharedArrayBuffers` , vaya a [WindowOrWorkerGlobalScope. crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1139899][CR1139899].  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Información de origen cruzado" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Información de origen cruzado  
:::image-end:::  

#### Nueva información de trabajadores web en la vista detalles del marco  

DevTools ahora organiza los trabajadores web en el marco principal correspondiente.  Por ejemplo, si el `someName` marco se crea `worker.js` , `worker.js` aparecerá en `someName` la lista de **Marcos** .  Para ver los detalles del trabajo Web, complete las siguientes acciones.  

1.  Abrir herramienta de **aplicación** .  
1.  Expandir un marco que contiene usuarios de Web.  
1.  Expanda el árbol de **trabajadores** .  
1.  Elija un trabajador.  
    
Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a los problemas [1122507][CR1122507] y [1051466][CR1051466].  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Información de los trabajadores web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Información de los trabajadores web  
:::image-end:::  

#### Mostrar detalles de la trama de apertura para las ventanas abiertas  

DevTools ahora organiza las [ventanas][MdnWindowConstructors] abiertas en el [marco][MdnWindowFrames]principal correspondiente.  Por ejemplo, si el `top` marco abre un `Window` a `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium` , entonces el `Window` aparece debajo `top` de en la lista de **Marcos** .  

Para mostrar el marco responsable de abrir otra ventana en la herramienta **elementos** , complete las siguientes acciones.  

1.  Abra el árbol de **Marcos** .  
1.  Expanda las **ventanas abiertas** y elija el `Window` correspondiente al marco principal que desea saber.  
1.  Elija el vínculo de **marco de apertura** .  

Se muestran los detalles sobre el fotograma que causaba la apertura de otro `Window` .  Para mostrar el abrir en la herramienta **elementos** , complete las siguientes acciones.  

1.  Abra el árbol de **Marcos** .  
1.  Elija una ventana abierta para abrir los `Window` detalles.  
1.  Elija el vínculo de **marco de apertura** .  
    
Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1107766][CR1107766].  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Detalles del fotograma abierto" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Detalles del fotograma abierto  
:::image-end:::  

### Copiar StackTrace para el iniciador de red  

Para copiar StackTrace en el portapapeles, complete las siguientes acciones.  

1.  Abra el menú contextual \ (haga clic con el botón derecho \).  
1.  Elija **copiar**  >  **copia de StackTrace**.  
    
Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1139615][CR1139615].

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copiar StackTrace" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Copiar StackTrace  
:::image-end:::  

### Vista previa de valor de variable de WASM en mouseover  

Use esta característica para revisar el valor de una variable webassembly \ (WASM \) cuando se haya pausado el código.  Para mostrar el valor actual de una variable, desplace el puntero sobre una variable.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto de cromo, vaya a los problemas [1058836][CR1058836] y [1071432][CR1071432].  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Vista previa de WASM variable en mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Vista previa de WASM variable en mouseover  
:::image-end:::  

### Unidades de medida coherentes para tamaños de archivos y memoria  

DevTools ahora `kB` para mostrar de forma coherente los tamaños de los archivos y de la memoria.  Anteriormente DevTools Mixed `kB` y `KiB` .

*   `kB` o kilobytes \ (10 ^ 3 o 1000 bytes \)  
*   `KiB` o Kibibyte \ (2 ^ 10 o 1024 bytes \)  
    
Por ejemplo, la herramienta de **red** que se usó anteriormente `kB` en las etiquetas, pero que se usa `KiB` en los cálculos.  Sus comentarios mostraron que esta incoherencia ocasionó confusión.  Para revisar el historial de esta característica en el proyecto de origen abierto de cromo, navegue hasta el problema [1035309][CR1035309].  

## Descargar los canales de Microsoft Edge Preview  

Si está en Windows, Linux o macOS, considere la posibilidad de usar el [canales de Microsoft Edge Preview] [MicrosoftEdgePreviewChannels] como su explorador de desarrollo predeterminado.  Los canales de previsualización proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Vista 3D | Microsoft docs"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Descripción general de la consola | Microsoft docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración-personalizar Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar el editor de métodos abreviados de teclado: características experimentales | Microsoft docs"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Activar capas compuestas en vista 3D: características experimentales | Microsoft docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y solucionar problemas con la herramienta de problemas de Microsoft Edge DevTools | Microsoft docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copiar JSON de respuesta con formato en el portapapeles: referencia de análisis de red | Microsoft docs"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Ver el desglose de intervalos de una solicitud-referencia de análisis de red | Microsoft docs"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Usar Webdriver (cromo) para automatización de prueba | Microsoft docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft docs"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Personalizar los métodos abreviados de teclado en configuración-novedades de DevTools (Microsoft Edge 87) | Microsoft docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "Comentarios sobre webhint en el panel problemas: novedades de DevTools (Microsoft Edge 85) | Microsoft docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar Webdriver | Microsoft Developer"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Descargar los canales de Insider de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Código de Visual Studio"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de cromo"  

[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir para personalizar métodos abreviados de teclado o enlaces de clave | Errores de cromo"  
[CR945786]: https://crbug.com/945786 "Problema 945786: DevTools: permitir invalidar Navigator. Storage. Calculate () | Errores de cromo"  
[CR1029427]: https://crbug.com/1029427 "Problema 1029427: reducir la sobrecarga de rendimiento del envío de mensajes de protocolo en el front-end | Errores de cromo"  
[CR1035309]: https://crbug.com/1035309 "Problema 1035309: DevTools debe usar de forma coherente MB para significar megabyte, no Mebibyte | Errores de cromo"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: compatibilidad con COOP/depuración de COEP en DevTools | Errores de cromo"  
[CR1058836]: https://crbug.com/1058836 "Problema 1058836: experiencia del usuario en la depuración de WASM | Errores de cromo"  
[CR1071432]: https://crbug.com/1071432 "Problema 1071432: ☂️ WASM Basic Developer Experience | Errores de cromo"  
[CR1107766]: https://crbug.com/1107766 "Problema 1107766: Mostrar información sobre los marcos generados por ' Window. Open () ' en árbol de marcos | Errores de cromo"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: información de los trabajadores superficiales en la vista árbol de marcos | Errores de cromo"  
[CR1126178]: https://crbug.com/1126178 "Problema 1126178: ☂ DevTools: CSS <Type> Components | Errores de cromo"  
[CR1130556]: https://crbug.com/1130556 "Problema 1130556: DevTools: comprobar las reservas de imagen (emulación) | Errores de cromo"  
[CR1132084]: https://crbug.com/1132084 "Problema 1132084: no se puede copiar fácilmente la carga de la solicitud JSON | Errores de cromo"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: herramientas de Flexbox | Errores de cromo"  
[CR1138633]: https://crbug.com/1138633 "Problema 1138633: DevTools: el componente> Angle <de CSS debe reflejar la apariencia de la propiedad que se encuentra en el fondo del reloj | Errores de cromo"  
[CR1139615]: https://crbug.com/1139615 "Problema 1139615: el iniciador de red debe ofrecer la posibilidad de copiar el seguimiento de la pila | Errores de cromo"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: disponibilidad del informe de API validada en la vista detalles del marco | Errores de cromo"  
[CR1139945]: https://crbug.com/1139945 "Problema 1139945: iconos de las propiedades de CSS de Flexbox en el panel estilos | Errores de cromo"  
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: mejorar el informe de errores de CORS en DevTools | Errores de cromo"  
[CR1144090]: https://crbug.com/1144090 "Problema 1144090: agregar adornos de estilo Flex al árbol de elementos | Errores de cromo"  
[CR1146985]: https://crbug.com/1146985 "Problema 1146985: el texto borrado se sigue viendo en el cuadro de texto de la sección ' almacenamiento ' de la ventana ' herramientas de desarrollo ' | Errores de cromo"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Errores de CORS | Intento"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Uso compartido de recursos entre orígenes (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propiedades personalizadas (variables) de CSS | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Constructores-Window | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window. frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope. crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "sugerencia"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Accesibilidad | sugerencia"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilidad | sugerencia"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Rendimiento | sugerencia"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Problemas | sugerencia"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | sugerencia"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Seguridad | sugerencia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/11/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \ (defensor para desarrolladores, Chrome DevTools \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
