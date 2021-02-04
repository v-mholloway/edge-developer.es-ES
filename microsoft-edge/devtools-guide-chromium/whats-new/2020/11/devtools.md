---
description: Microsoft Edge en Linux, sugerencias de webhint mejoradas en la herramienta Problemas, nuevas características de depuración de trabajo de servicio y más.
title: Novedades de DevTools (Microsoft Edge 88)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/03/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 9e4bdfcb3cc32364931894dcb3c857ac6e082809
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313089"
---
# Novedades de DevTools (Microsoft Edge 88)  

[!INCLUDE [contact DevTools team note](../../includes/edge-whats-new-note.md)]  

## Microsoft Edge y el controlador de Microsoft Edge ahora están disponibles en Linux  

<!-- Title: Microsoft Edge and Microsoft Edge Driver on Linux  -->  
<!-- Subtitle: Get Microsoft Edge Dev on Ubuntu, Debian, Fedora, and openSUSE distributions and start automating in CI/CD environments with Microsoft Edge Driver. -->  

Microsoft Edge Dev ahora es compatible con las distribuciones Ubuntu, Debian, Fedora y openSUSE.  Descargue e instale el `.deb` de Microsoft Edge Dev o el paquete de `.rpm` directamente desde el [sitio de Microsoft Edge Insider][MicrosoftinsiderDownloadPlatformLinux] o use las herramientas de administración de paquetes estándar de su distribución de Linux.  

Si está usando un entorno Linux en sus soluciones de integración y entrega continuas \(CI/CD\), el controlador de Microsoft Edge también está disponible en Linux.  Para empezar a automatizar Microsoft Edge Dev con el controlador de Microsoft Edge, navegue a la [página de Descargas del controlador de Microsoft Edge][MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads].  Para obtener ayuda con la automatización de Microsoft Edge Dev junto con el controlador de Microsoft Edge, navegue a [Usar Webdriver (Chromium) para la automatización de prueba][WebDriverChromiumMain].  

:::image type="complex" source="../../media/2020/11/edge-on-linux.msft.png" alt-text="DevTools en Microsoft Edge en Linux" lightbox="../../media/2020/11/edge-on-linux.msft.png":::
   DevTools en Microsoft Edge en Linux  
:::image-end:::  

## Sugerencias de webhint y de plataforma mejoradas en la herramienta Problemas  

<!-- Title: Improvements to Issues tool and webhint integration  -->  
<!-- Subtitle: Categories and third-party filtering make it easier to survey issues in the Issues tool.  Issues surfaced by webhint now have improved code snippets and documentation links to help you fix problems in your website.  -->  

Una herramienta de código abierto, [webhint][WebhintMain], proporciona comentarios en tiempo real para sitios web y páginas web locales.  A partir de la [versión 85 de Microsoft Edge][WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel], revise los comentarios de webhint en la herramienta [Problemas][DevtoolsIssuesIndex].  Los problemas que aparecen en la herramienta **Problemas** ahora son más fáciles de revisar con la adición de las siguientes categorías.  

*   [Accesibilidad][WebhintUserGuideHintsAccessibility]  
*   [Compatibilidad][WebhintUserGuideHintsCompatibility]  
*   [Rendimiento][WebhintUserGuideHintsPerformance]  
*   [Inconvenientes][WebhintUserGuideHintsPitfalls]  
*   [PWA][WebhintUserGuideHintsPwa]  
*   [Seguridad][WebhintUserGuideHintsSecurity]  
    
Ahora puede filtrar problemas de terceros mediante una nueva casilla.  La funcionalidad de filtro le ayuda a ocultar problemas relacionados con el código de bibliotecas de terceros u otros orígenes.  

Para ayudarle a revisar los problemas que revela [webhint][WebhintMain], la herramienta **Problemas** ahora muestra la siguiente información.  

*   Fragmentos de código mejorados.  
*   Vínculos a otros paneles relevantes.  
*   Vínculos a documentación para ayudarle a solucionar problemas de su sitio web.  
    
:::image type="complex" source="../../media/2020/11/issues-webhints.msft.png" alt-text="Herramienta Problemas" lightbox="../../media/2020/11/issues-webhints.msft.png":::
   Herramienta **Problemas**  
:::image-end:::  

## Las Capas compuestas ahora se encuentran en la vista 3D  

<!-- Title: 3D View is now integrated with Composited Layers  -->  
<!-- Subtitle: Composited Layers are now in 3D View.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::  

Ahora puede visualizar el contenido de las **Capas** junto con los valores de índice z y el modelo de objeto de documento \(DOM\).  Esta característica le ayuda a depurar sin cambiar entre la [vista 3D][Devtools3dViewIndex] y las herramientas de **Capas** con frecuencia.  Para obtener una experiencia de depuración visual completa, [ahora se combinan la vista 3D y las Capas compuestas][DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView].  

:::image type="complex" source="../../media/2020/11/experiments-layers.msft.png" alt-text="Panel Capas compuestas" lightbox="../../media/2020/11/experiments-layers.msft.png":::
   Panel **Capas compuestas**  
:::image-end:::  

## Definiciones de variables CSS en el panel Estilos  

<!-- Title: Jump to CSS variable definitions  -->  
<!-- Subtitle: Choose any CSS variable to navigate directly to the definition in the Styles tool. -->  

En el panel **Estilos**, [las variables CSS][MdnUsingCssCustomProperties] ahora se vinculan directamente a cada definición.  Elija la variable para ver o cambiar fácilmente la definición de la variable CSS.  En el ejemplo, DevTools muestra los atributos CSS para el `body` elemento.  Para mostrar la definición de variable de la variable CSS `--theme-body-background`, complete las siguientes acciones.  

1.  En el panel **Estilos**, elija `var(--theme-body-background)`.  
1.  El panel **Estilos** ahora muestra la definición de la variable CSS `--theme-body-background`.  
    
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

Las siguientes características nuevas de las herramientas [Redes](#network-tool), [Aplicaciones](#application-tool) y [Fuentes](#sources-tool) le ayudan a crear su [PWA][ProgressiveWebAppsChromiumIndex].  Use las siguientes características cuando tenga dificultades para depurar el trabajo del servicio.  

El enrutamiento de solicitudes muestra los eventos `startup` y `fetch` en función de las solicitudes de red que se ejecutan a través de los trabajos de servicio.  Se obtiene acceso a las escalas de tiempo desde la herramienta **Aplicación** o **Red**.  Las escalas de tiempo ayudan cuando tiene problemas con los trabajos de servicio y desea ver si hay algún problema con el evento `startup` o `fetch`.  

### Herramienta Aplicación  

<!-- Title: Open Network tool from the Service Workers pane  -->  
<!-- Subtitle: Display additional context when debugging a service worker.  -->  

Vea toda la información de enrutamiento de solicitud de trabajo de servicio con el nuevo vínculo **Solicitudes de red**.  Para mostrar contexto adicional al depurar el trabajo de servicio, complete las siguientes acciones.  

1.  Vaya a **Aplicación** > **Trabajos de servicio**.  
1.  Elija **Solicitudes de red**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-requests.msft.png" alt-text="Abrir la herramienta Red desde el panel Trabajo de servicios" lightbox="../../media/2020/11/service-worker-application-network-requests.msft.png":::
       Abrir la herramienta **Red** desde el panel **Trabajo de servicios**
    :::image-end:::  
    
1.  La herramienta **Red** se abre en el **cajón** y muestra todas las solicitudes de red relacionadas con los trabajos de servicio.  Las solicitudes de red se filtran mediante `is:service-worker-intercepted`.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-drawer.msft.png" alt-text="Herramienta Red en el cajón" lightbox="../../media/2020/11/service-worker-application-network-drawer.msft.png":::
       Herramienta **Red** en el **Cajón**  
    :::image-end:::
    
1. Para devolver la herramienta **Red** al panel superior, cierre el **Cajón**.  
    
    :::image type="complex" source="../../media/2020/11/service-worker-application-network-return.msft.png" alt-text="Cerrar el cajón para devolver la herramienta Red" lightbox="../../media/2020/11/service-worker-application-network-return.msft.png":::
       Cerrar el **Cajón** para devolver la herramienta **Red**  
    :::image-end:::  
    
### Herramienta Red  

Depure las solicitudes de red que se ejecutan a través de los trabajos de servicio.  También puede abrir solicitudes de red desde la herramienta **Aplicación**.  Para cada solicitud, DevTools muestra la siguiente información en el panel [Intervalos][DevtoolsNetworkReferenceViewTimingBreakdownRequest].  

*   El inicio de una solicitud y la duración del arranque.  
*   Cambios en el registro de trabajos de servicio.  
*   El tiempo de ejecución de un controlador de evento `fetch`.  
*   El tiempo de ejecución de todos los eventos `fetch` para cargar un cliente.  
    
:::image type="complex" source="../../media/2020/11/network-timing-service-worker.msft.png" alt-text="Panel Intervalos" lightbox="../../media/2020/11/network-timing-service-worker.msft.png":::
   Panel **Intervalos**  
:::image-end:::  

### Herramienta Orígenes  

En versiones anteriores de Microsoft Edge, el nivel de profundidad en la pila de llamadas estaba limitado al código de JavaScript en el trabajo de servicio.  En Microsoft Edge 88, la pila de llamadas ahora muestra el iniciador de solicitudes que se ejecutan a través del trabajo de servicio.  

Para buscar el iniciador de la solicitud, use la pila de llamadas de su código JavaScript en el trabajo de servicio.  La pila de llamadas de las siguientes figuras comienza con el código de JavaScript en el trabajo de servicio y muestra una referencia a la solicitud original de la página web como `(index):157`.  En la segunda figura, se elige la referencia y se abre el iniciador que realizó la solicitud.  El iniciador de la segunda figura es la página web.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png" alt-text="El originador de la solicitud de resaltado de pila de llamadas y archivos de service-worker.js" lightbox="../../media/2020/11/service-worker-sources-stopped-at-breakpoint.msft.png":::
         El originador de solicitudes de resaltado de pila de llamadas y archivos `service-worker.js`.  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/service-worker-sources-call-stack-target.msft.png" alt-text="La página web (índice) es el iniciador de la solicitud" lightbox="../../media/2020/11/service-worker-sources-call-stack-target.msft.png":::
         La página web `(index)` es el iniciador de la solicitud  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Copiar el valor de la propiedad de una solicitud de red  

<!-- Title: Copy response JSON in Network tool using the contextual menu  -->  
<!-- Subtitle:  The Network tool now has a more consistent UX.  Easily copy the JSON response using the contextual menu.  -->  

En la herramienta **Red**, copie el valor de la propiedad de una solicitud de red con la nueva opción **Copiar valor**.  El valor de la propiedad se copia como un valor JSON descodificado.  En versiones anteriores de Microsoft Edge, tenía que copiar un valor con una de las siguientes acciones.  

*   Resalte todo el texto y cópielo.  
*   Almacene el valor como variable global, según sea el caso, y cópielo desde la [Consola][DevtoolsConsoleIndex] de DevTools.  
    
Para copiar el valor de la propiedad en el portapapeles, desplácese hasta [Copiar JSON de respuesta con formato en el portapapeles][DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard].  Para revisar el historial de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1132084][CR1132084].  

:::row:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/copy-property-value.msft.png" alt-text="Copiar el valor de la propiedad en DevTools" lightbox="../../media/2020/11/copy-property-value.msft.png":::
         Copiar el valor de la propiedad en DevTools  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../../media/2020/11/paste-property-value.msft.png" alt-text="Pegar el valor de la propiedad en Visual Studio Code" lightbox="../../media/2020/11/paste-property-value.msft.png":::
         Pegar el valor de la propiedad en Visual Studio Code  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## Personalizar métodos abreviados de teclado de varios clics  

<!-- Title: Customize multi-press keyboard shortcuts  -->  
<!-- Subtitle: Create custom multi-press keyboard shortcuts in the shortcut editor.  -->  

:::image type="icon" source="../../media/2020/06/experimental-tag-14px.msft.png":::

[A partir de Microsoft Edge versión 87][WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings], puede personalizar los métodos abreviados de teclado para cualquier acción en DevTools.  En Microsoft Edge versión 88, ahora puede crear métodos abreviados de teclado de varios clics.  Para establecer un método abreviado para una acción en DevTools, vaya a [Configuración][DevtoolsCustomizeIndexSettings] > **Experimentos** y elija la casilla situada junto a **Habilitar el editor de métodos abreviados de teclado**.  Para obtener más información sobre la personalización y la edición de accesos directos, vaya a [Habilitar la característica experimental del editor de método abreviado de teclado][DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor].  

Por ejemplo, el resaltado rojo muestra un método abreviado de teclado de varios clics personalizado para la acción **Iniciar grabación de eventos**.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el [Problema N.°174309][CR174309].  

:::image type="complex" source="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png" alt-text="Métodos abreviados de teclado de presión simultánea" lightbox="../../media/2020/11/multi-press-keyboard-shortcuts.msft.png":::
   Métodos abreviados de teclado de varios clics  
:::image-end:::  

## DevTools ahora coincide con el idioma del explorador  

En Microsoft Edge versión 87, si activaba la opción **Coincidir con el idioma del explorador** en la [Configuración de DevTools][DevtoolsCustomizeIndexSettings], DevTools no coincidía con el idioma del explorador.  En la versión 88 de Microsoft Edge, DevTools coincide con el idioma del explorador si se activa la opción **Coincidir con el idioma del explorador**.  Para obtener más información sobre la opción de DevTools **Coincidir con el idioma del explorador**, vaya a [Cambiar la configuración de idioma de DevTools][DevtoolsCustomizeLocalization].  

:::image type="complex" source="../../media/2020/11/startpage-devtools-settings-japanese.msft.png" alt-text="Opción de DevTools Coincidir con el idioma del explorador en japonés" lightbox="../../media/2020/11/startpage-devtools-settings-japanese.msft.png":::
   Opción de DevTools **Coincidir con el idioma del explorador** en japonés  
:::image-end:::  

## Anuncios del proyecto de Chromium  

[!INCLUDE [contact DevTools team note](../../includes/chromium-whats-new-note.md)]  

### Nuevas herramientas de visualización de ángulos CSS  

DevTools ahora es más compatible con la depuración de ángulos de CSS.  Cuando se aplica un ángulo CSS a un elemento HTML de la página, se muestra un icono de reloj junto al ángulo en la herramienta **Estilos**.  Para activar o desactivar la superposición de reloj, elija el icono de reloj.  Para cambiar el ángulo, seleccione cualquier lugar del reloj o arrastre la aguja.  Para cambiar el valor de ángulo, también puede usar los métodos abreviados de teclado y el mouse.  <!--  To learn more, navigate to [Angle Clock][DevtoolsCssReferenceChangeAngleValueWithAngleClock].  -->  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1126178][CR1126178] y [1138633][CR1138633].  

<!--todo:  add link when css angle clock section exists.  -->  

Para el ejemplo, se usa el siguiente ángulo de CSS.  

```css
background: linear-gradient(100deg, lightblue, pink);
```

:::image type="complex" source="../../media/2020/11/css-angle.msft.png" alt-text="Ángulo CSS" lightbox="../../media/2020/11/css-angle.msft.png":::
   Ángulo CSS  
:::image-end:::  

### Simular tamaño de la cuota de almacenamiento en el panel Almacenamiento  

Ahora puede invalidar el tamaño de la cuota de almacenamiento en el panel **Almacenamiento**.  Esta característica le permite simular diferentes dispositivos y probar el comportamiento de su sitio web o aplicación en escenarios de disponibilidad de disco baja.  Para simular la cuota de almacenamiento, complete las siguientes acciones.  

1.  Vaya a **Aplicación** > **Almacenamiento**.  
1.  Active la casilla **Simular cuota de almacenamiento personalizada**.  
1.  Escriba un número válido.  
    
Para obtener más información sobre cómo emular dispositivos móviles y otras características de DevTools, vaya a [Emular dispositivos móviles en Microsoft Edge DevTools ][DevtoolsDeviceModeIndex].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [945786][CR945786] y [1146985][CR1146985].  

:::image type="complex" source="../../media/2020/11/storage-quota.msft.png" alt-text="Simular tamaño de la cuota de almacenamiento" lightbox="../../media/2020/11/storage-quota.msft.png":::
   Simular tamaño de la cuota de almacenamiento  
:::image-end:::  

### Notificar errores de CORS en la herramienta Red  

Para probar esta característica, navegue a [Demo de error de CORS][GlitchCorsErrors].  Abra la herramienta **Red**, actualice la página y observe la solicitud de red de CORS errónea.  En la columna de estado se muestra el **Error de CORS**.  Al desplazar el puntero sobre el error, la información sobre herramientas muestra ahora el código de error.  En Microsoft Edge versión 87 y anteriores, DevTools solo mostraba el estado **(erróneo)** genérico para los errores de CORS.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1141824][CR1141824].  

:::image type="complex" source="../../media/2020/11/cors-err.msft.png" alt-text="Errores de CORS" lightbox="../../media/2020/11/cors-err.msft.png":::
   Errores de CORS  
:::image-end:::  

### Actualización de la vista de detalles del marco  

#### Información de aislamiento entre orígenes en la vista detalles del Marco  

El estado aislado entre orígenes se muestra ahora en la sección **Seguridad y aislamiento**.  La nueva sección **Disponibilidad de API** muestra la disponibilidad de `SharedArrayBuffer`s \(SAB\) y si los búferes se pueden compartir mediante `postMessage()`.  Se muestra una advertencia de desuso si SAB y `postMessage()` están disponibles en este momento, pero el contexto no está aislado entre orígenes.  Para obtener más información sobre el aislamiento entre orígenes y por qué es necesario para características como `SharedArrayBuffers`, vaya a [WindowOrWorkerGlobalScope.crossOriginIsolated][MdnWindoworworkerglobalscopeCrossoriginisolated].  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1139899][CR1139899].  

:::image type="complex" source="../../media/2020/11/frame-cross-origin-isolated-api.msft.png" alt-text="Información entre orígenes" lightbox="../../media/2020/11/frame-cross-origin-isolated-api.msft.png":::
   Información entre orígenes  
:::image-end:::  

#### Nueva información de trabajos web en la vista detalles del Marco  

DevTools ahora organiza los trabajos web en el marco principal correspondiente.  Por ejemplo, si el marco `someName` crea `worker.js`, entonces `worker.js` aparecerá en `someName` en la lista **Marcos**.  Para ver los detalles del trabajo web, complete las siguientes acciones.  

1.  Abra la herramienta **Aplicación**.  
1.  Expanda un marco que contenga los trabajos web.  
1.  Expanda el árbol de **Trabajos**.  
1.  Elija un trabajo.  
    
Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1122507][CR1122507] y [1051466][CR1051466].  

:::image type="complex" source="../../media/2020/11/application-frames-service-workers.msft.png" alt-text="Información de los trabajos web" lightbox="../../media/2020/11/application-frames-service-workers.msft.png":::
   Información de los trabajos web  
:::image-end:::  

#### Mostrar detalles del marco de apertura para las ventanas abiertas  

DevTools ahora organiza las [ventanas][MdnWindowConstructors] abiertas en el [Marco][MdnWindowFrames] principal correspondiente.  Por ejemplo, si el marco `top` abre un `Window` para `https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium`, entonces el `Window` aparece en `top` en la lista **Marcos**.  

Para mostrar el marco responsable de abrir otra ventana en la herramienta **Elementos**, complete las siguientes acciones.  

1.  Abra el árbol **Marcos**.  
1.  Expanda **Ventanas abiertas** y elija el `Window` correspondiente al marco principal que desea saber.  
1.  Elija el vínculo **Marco de apertura**.  

Se muestran los detalles sobre el marco que causaba la apertura de otro `Window`.  Para mostrar el abridor en la herramienta **Elementos**, complete las siguientes acciones.  

1.  Abra el árbol **Marcos**.  
1.  Elija una ventana abierta para abrir los detalles de `Window`.  
1.  Elija el vínculo **Marco de apertura**.  
    
Para revisar el historial de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1107766][CR1107766].  

:::image type="complex" source="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png" alt-text="Detalles del marco abierto" lightbox="../../media/2020/11/application-frames-opened-windows-security-opener-frame.msft.png":::
   Detalles del marco abierto  
:::image-end:::  

### Copiar el seguimiento de la pila para el iniciador de red  

Para copiar el seguimiento de la pila en el portapapeles, complete las siguientes acciones.  

1.  Abra el menú contextual \(haga clic con el botón derecho\).  
1.  Elija **Copiar**  >  **Copiar seguimiento de la pila**.  
    
Para revisar el historial de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1139615][CR1139615].

:::image type="complex" source="../../media/2020/11/copy-stacktrace.msft.png" alt-text="Copiar seguimiento de la pila" lightbox="../../media/2020/11/copy-stacktrace.msft.png":::
   Copiar seguimiento de la pila  
:::image-end:::  

### Vista previa de valor de variable Wasm en mouseover  

Use esta característica para revisar el valor de una variable webassembly \(Wasm\) cuando se haya pausado el código.  Para mostrar el valor actual de una variable, desplace el puntero sobre una variable.  Para revisar las actualizaciones en tiempo real de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1058836][CR1058836] y [1071432][CR1071432].  

:::image type="complex" source="../../media/2020/11/wasm-mouseover.msft.png" alt-text="Vista previa de variable Wasm en mouseover" lightbox="../../media/2020/11/wasm-mouseover.msft.png":::
   Vista previa de variable Wasm en mouseover  
:::image-end:::  

### Unidades de medida coherentes para tamaños de archivos y memoria  

DevTools ahora usa `kB` de forma consistente para mostrar los tamaños de los archivos y de la memoria.  Anteriormente, DevTools combinaba `kB` y `KiB`.

*   `kB` o kilobytes \(10^3 o 1000bytes\)  
*   `KiB` o kibibytes \(2^10 o 1024bytes\)  
    
Por ejemplo, la herramienta **Red** anteriormente usaba `kB` en las etiquetas, pero usaba `KiB` en los cálculos.  Sus comentarios mostraron que esta inconstancia ocasionó confusión.  Para revisar el historial de esta característica en el proyecto de origen abierto Chromium, navegue hasta el problema [1035309][CR1035309].  

## Descargar los canales de vista previa de Microsoft Edge  

Si está en Windows, Linux o macOS, considere la posibilidad de usar los canales de vista previa de [Microsoft Edge][MicrosoftEdgePreviewChannels] como explorador de desarrollo predeterminado.  Los canales de vista previa proporcionan acceso a las características más recientes de DevTools.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[Devtools3dViewIndex]: /microsoft-edge/devtools-guide-chromium/3d-view/index "Vista 3D | Microsoft Docs"  
[DevtoolsConsoleIndex]: /microsoft-edge/devtools-guide-chromium/console/index "Descripción general de la consola | Microsoft Docs"  
[DevtoolsCustomizeIndexSettings]: /microsoft-edge/devtools-guide-chromium/customize/index#settings "Configuración: personalizar Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsCustomizeLocalization]: /microsoft-edge/devtools-guide-chromium/customize/localization "Cambiar la configuración de idioma de DevTools | Microsoft Docs"  
[DevtoolsDeviceModeIndex]: /microsoft-edge/devtools-guide-chromium/device-mode/index "Emular dispositivos móviles en Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsExperimentalFeaturesEnableKeyboardShortcutEditor]: /microsoft-edge/devtools-guide-chromium/experimental-features#enable-keyboard-shortcut-editor "Habilitar el editor de métodos abreviados de teclado: características experimentales | Microsoft Docs"  
[DevtoolsExperimentalFeaturesTurnOnCompositedLayers3dView]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-composited-layers-in-3d-view "Activar Capas compuestas en la vista 3D: características experimentales | Microsoft Docs"  
[DevtoolsIssuesIndex]: /microsoft-edge/devtools-guide-chromium/issues/index "Buscar y solucionar problemas con la herramienta Problemas de Microsoft Edge DevTools | Microsoft Docs"  
[DevtoolsNetworkReferenceCopyFormattedResponseJsonClipboard]: /microsoft-edge/devtools-guide-chromium/network/reference#copy-formatted-response-json-to-the-clipboard "Copiar JSON de respuesta con formato en el portapapeles: referencia de análisis de red | Microsoft Docs"  
[DevtoolsNetworkReferenceViewTimingBreakdownRequest]: /microsoft-edge/devtools-guide-chromium/network/reference#view-the-timing-breakdown-of-a-request "Ver el desglose de intervalos de una solicitud: referencia de análisis de red | Microsoft Docs"  
[WebDriverChromiumMain]: /microsoft-edge/webdriver-chromium "Usar Webdriver (Chromium) para la automatización de prueba | Microsoft Docs"  

<!--  [DevtoolsCssReferenceChangeAngleValueWithAngleClock]: /microsoft-edge/devtools-guide-chromium/css/reference#change-angle-value-with-the-angle-clock "Change angle value with the Angle Clock - CSS reference | Microsoft Docs"  -->  

[ProgressiveWebAppsChromiumIndex]: /microsoft-edge/progressive-web-apps-chromium/index "Aplicaciones web progresivas en Windows | Microsoft Docs"  

[WhatsNew202010DevtoolsCustomizeKeyboardShortcutsSettings]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/10/devtools#customize-keyboard-shortcuts-in-settings "Personalizar los métodos abreviados de teclado en Configuración: novedades de DevTools (Microsoft Edge 87) | Microsoft Docs"  
[WhatsNew202006DevtoolsWebhintFeedbackInTheIssuesPanel]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/06/devtools#webhint-feedback-in-the-issues-panel "Comentarios sobre webhint en el panel Problemas: novedades de DevTools (Microsoft Edge 85) | Microsoft Docs"  

[MicrosoftDeveloperMicrosoftEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver#downloads "Descargar WebDriver | Desarrollador de Microsoft"  

[MicrosoftinsiderDownloadPlatformLinux]: https://www.microsoftedgeinsider.com/download?platform=linux "Descargar Microsoft Edge Insider Channels"  

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download "Canales de vista previa de Microsoft Edge"  

[VisualStudioCode]: https://code.visualstudio.com "Visual Studio Code"  

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Errores de Chromium"  

[CR174309]: https://crbug.com/174309 "Problema 174309: DevTools: permitir la personalización de métodos abreviados de teclado o enlaces de clave | Errores de Chromium"  
[CR945786]: https://crbug.com/945786 "Problema 945786: DevTools: permitir invalidar navigator.storage.estimate() | Errores de Chromium"  
[CR1029427]: https://crbug.com/1029427 "Problema 1029427: reducir la sobrecarga de rendimiento del envío de mensajes de protocolo en el front-end | Errores de Chromium"  
[CR1035309]: https://crbug.com/1035309 "Problema 1035309: DevTools debe usar de forma coherente MB para significar megabyte, no mebibyte | Errores de Chromium"  
[CR1051466]: https://crbug.com/1051466 "Problema 1051466: compatibilidad con la depuración de COOP/COEP en DevTools | Errores de Chromium"  
[CR1058836]: https://crbug.com/1058836 "Problema 1058836: problemas UX en torno a la depuración de Wasm | Errores de Chromium"  
[CR1071432]: https://crbug.com/1071432 "Problema 1071432: ☂︝ experiencia básica del desarrollador de Wasm | Errores de Chromium"  
[CR1107766]: https://crbug.com/1107766 "Problema 1107766: mostrar información sobre los marcos generados por 'window.open()' en el árbol de marcos | Errores de Chromium"  
[CR1122507]: https://crbug.com/1122507 "Problema 1122507: información de los trabajos superficiales en la vista de árbol de marcos | Errores de Chromium"  
[CR1126178]: https://crbug.com/1126178 "Problema 1126178: ☂ DevTools: componentes <Type> de CSS | Errores de Chromium"  
[CR1130556]: https://crbug.com/1130556 "Problema 1130556: DevTools: comprobar las reservas de imagen (emulación) | Errores de Chromium"  
[CR1132084]: https://crbug.com/1132084 "Problema 1132084: no se puede copiar fácilmente la carga útil de la solicitud JSON | Errores de Chromium"  
[CR1136394]: https://crbug.com/1136394 "Problema 1136394: herramientas de la caja flexible | Errores de Chromium"  
[CR1138633]: https://crbug.com/1138633 "Problema 1138633: DevTools: el componente <angle> de CSS debe reflejar la apariencia de la propiedad que se encuentra en el fondo del reloj | Errores de Chromium"  
[CR1139615]: https://crbug.com/1139615 "Problema 1139615: el iniciador de red debe ofrecer la posibilidad de copiar el seguimiento de la pila | Errores de Chromium"  
[CR1139899]: https://crbug.com/1139899 "Problema 1139899: informar la disponibilidad de la API validada en la vista detalles del marco | Errores de Chromium"  
[CR1139945]: https://crbug.com/1139945 "Problema 1139945: iconos de las propiedades de CSS de la caja flexible en el panel Estilos | Errores de Chromium"  
[CR1141824]: https://crbug.com/1141824 "Problema 1141824: mejorar el informe de errores de CORS en DevTools | Errores de Chromium"  
[CR1144090]: https://crbug.com/1144090 "Problema 1144090: agregar adornos de estilo flexibles al árbol Elementos | Errores de cromo"  
[CR1146985]: https://crbug.com/1146985 "Problema 1146985: el texto borrado se sigue viendo en el cuadro de texto de la sección 'Almacenamiento ' de la ventana 'Dev Tools' | Errores de Chromium"  

[GlitchCorsErrors]: https://cors-errors.glitch.me "Errores de CORS | Problema"  

[MdnCors]: https://developer.mozilla.org/docs/Web/HTTP/CORS "Uso compartido de recursos entre orígenes (CORS) | MDN"  
[MdnUsingCssCustomProperties]: https://developer.mozilla.org/docs/Web/CSS/Using_CSS_custom_properties "Usar propiedades personalizadas de CSS (variables) | MDN"  
[MdnWindowConstructors]: https://developer.mozilla.org/docs/Web/API/Window#Constructors "Constructores: ventana | MDN"  
[MdnWindowFrames]: https://developer.mozilla.org/docs/Web/API/Window/frames "Window.frames | MDN"  
[MdnWindoworworkerglobalscopeCrossoriginisolated]: https://developer.mozilla.org/docs/Web/API/WindowOrWorkerGlobalScope/crossOriginIsolated "WindowOrWorkerGlobalScope.crossOriginIsolated | MDN"  

[WebhintMain]: https://webhint.io "webhint"  
[WebhintUserGuideHintsAccessibility]: https://webhint.io/docs/user-guide/hints/accessibility "Accesibilidad | webhint"  
[WebhintUserGuideHintsCompatibility]: https://webhint.io/docs/user-guide/hints/compatibility "Compatibilidad | webhint"  
[WebhintUserGuideHintsPerformance]: https://webhint.io/docs/user-guide/hints/performance "Rendimiento | webhint"  
[WebhintUserGuideHintsPitfalls]: https://webhint.io/docs/user-guide/hints/pitfalls "Inconvenientes | webhint"  
[WebhintUserGuideHintsPwa]: https://webhint.io/docs/user-guide/hints/pwa "PWA | webhint"  
[WebhintUserGuideHintsSecurity]: https://webhint.io/docs/user-guide/hints/security "Seguridad | webhint"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/updates/2020/11/devtools/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
