---
description: Obtenga información sobre cómo usar Microsoft Edge DevTools para encontrar formas de hacer que sus sitios web se carguen más rápido.
title: Optimizar la velocidad del sitio web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e3ddadcf37303a476f3a656696b00f121f079b69
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519614"
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

# <a name="optimize-website-speed-with-microsoft-edge-devtools"></a>Optimizar la velocidad del sitio web con Microsoft Edge DevTools  

## <a name="goal-of-tutorial"></a>Objetivo del tutorial  

Este tutorial le enseña a usar Microsoft Edge DevTools para encontrar formas de hacer que sus sitios web se carguen más rápido.  

## <a name="prerequisites"></a>Requisitos previos  

*   Debe tener experiencia básica de desarrollo web, similar a lo que se enseña en esta [clase Introduction to Web Development][CourseraIntroductionWebDevelopmentClass].  
*   No es necesario saber nada sobre el rendimiento de carga.  Obtenga información sobre esto en este tutorial.  

## <a name="introduction"></a>Introducción  

Este es Tony.  Tony es muy famoso en la sociedad de gatos.  Ha creado un sitio web para que sus fans puedan aprender sobre sus alimentos favoritos.  A sus fans les encanta el sitio, pero Tony sigue escuchando quejas de que el sitio se carga lentamente.  Tony te ha pedido que le ayudes a acelerar el sitio.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony el gato" lightbox="../media/speed-tony.msft.png":::
   Tony el gato  
:::image-end:::  

## <a name="step-1-audit-the-site"></a>Paso 1: Auditar el sitio  

Siempre que se establezca para mejorar el rendimiento de carga de un sitio, **comience siempre con una auditoría**.  
La auditoría tiene 2 funciones importantes:  

*   Crea una línea **base con** la que medir los cambios posteriores.  
*   Le ofrece **sugerencias de acción sobre** los cambios que tienen más impacto.  
    
### <a name="set-up"></a>Configuración  

En primer lugar, debe configurar el sitio para poder realizar cambios en él más adelante.  

1.  [Abra el código fuente del sitio](https://glitch.com/edit/#!/tony).  Esta pestaña se conoce como pestaña **editor**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Pestaña editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       Pestaña **editor**  
    :::image-end:::  
    
1.  Elija **tony**.  Aparece un menú.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="Menú que aparece después de elegir Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       Menú que aparece después de elegir **Tony**  
    :::image-end:::  
    
1.  Elija **Remix Project**.  El nombre del proyecto cambia de **tony** a algún nombre generado aleatoriamente.  Ahora tiene su propia copia editable del código.  Más adelante, puede realizar cambios en este código.  
1.  Elija **Mostrar** y **elija En una nueva ventana**.  La demostración se abre en una pestaña nueva.  Esta pestaña se conoce como pestaña **de demostración**.  El sitio puede tardar un tiempo en cargarse.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="Pestaña de demostración" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       Pestaña de demostración  
    :::image-end:::  
    
1.  Seleccione `Control` + `Shift` + `J` \(Windows, Linux\) o `Command` + `Option` + `J` \(macOS\).  Microsoft Edge DevTools se abre junto con la demostración.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools y la demostración" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools y la demostración  
    :::image-end:::  
    
Para el resto de capturas de pantalla de este tutorial, DevTools se muestra en una ventana independiente.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) `Undock` **** para abrir el menú comando, escribir y, a continuación, seleccionar Desacoplar en una ventana independiente .  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools desacopladas" lightbox="../media/speed-console.msft.png":::
   DevTools desacopladas  
:::image-end:::  

### <a name="establish-a-baseline"></a>Establecer una línea base  

La línea base es un registro de cómo se realizó el sitio antes de realizar cualquier mejora de rendimiento.  

1.  Elija la **herramienta Auditorías.**  Puede estar oculto detrás del **botón Más paneles** \( Más paneles ![ ](../media/more-panels-icon.msft.png) \).  Hay un Faro en este panel porque el proyecto que impulsa el panel Auditorías se denomina **Faro**.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="La herramienta Auditorías" lightbox="../media/speed-audits-performance.msft.png":::
       La **herramienta Auditorías**  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Haga coincidir las opciones de configuración de auditoría con las de la figura anterior.  Esta es una explicación de las diferentes opciones:  
    
    *   **Dispositivo**.  Establecer en **Móvil cambia** la cadena del agente de usuario y simula una ventanilla móvil.  Si se **establece en Escritorio,** se desactivan los **cambios de** Móvil.  
    *   **Auditorías**.  Desactive una categoría para impedir que el panel Auditorías ejecute **dichas** auditorías y las excluye del informe.  Deje las otras categorías Activadas, si desea mostrar los tipos de recomendaciones que se proporcionan.  Desactiva las categorías para acelerar ligeramente el proceso de auditoría.  
    *   **Limitación**.  Establecida en **Simulated Slow 4G, 4x CPU Slowdown** simula las condiciones típicas de navegación en un dispositivo móvil.  Se denomina "simulado" porque el panel Auditorías no limita realmente durante el proceso de auditoría.  En su lugar, solo extrapola el tiempo que tarda la página en cargarse en condiciones móviles.  Por **otro lado,** la configuración Aplicado... limita realmente la CPU y la red, con la negociación de un proceso de auditoría más largo.  
    *   **Borrar almacenamiento**.  Active la casilla para borrar todo el almacenamiento asociado a la página antes de cada auditoría.  Deje esta configuración en si desea auditar la experiencia de los visitantes por primera vez en su sitio.  Desactiva esta configuración cuando quieras la experiencia de repetición de visita.  
    
1.  Elija **Ejecutar auditorías**.  Después de 10 a 30 segundos, el panel **Auditorías** muestra un informe del rendimiento del sitio.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Informe del panel Auditorías del rendimiento del sitio" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       Informe del panel Auditorías del rendimiento del sitio  
    :::image-end:::  
    
#### <a name="handling-report-errors"></a>Controlar errores de informe  

Si alguna vez recibe un error en el informe del panel Auditorías, intente ejecutar la pestaña de demostración desde una ventana **de InPrivate** sin otras pestañas abiertas.  Esto garantiza que está ejecutando Microsoft Edge desde un estado limpio.  Las extensiones de Microsoft Edge, en particular, suelen interferir con el proceso de auditoría.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### <a name="understand-your-report"></a>Comprender el informe  

El número en la parte superior del informe es la puntuación de rendimiento general del sitio.  Más adelante, al realizar cambios en el código, el número que se muestra debe aumentar.  Una puntuación más alta significa un mejor rendimiento.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="Puntuación general de rendimiento" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   Puntuación general de rendimiento  
:::image-end:::  

La **sección Métricas** proporciona medidas cuantitativas del rendimiento del sitio.  Cada métrica proporciona información sobre un aspecto diferente del rendimiento.  Por ejemplo, **First Contentful Paint** indica cuándo se pinta el contenido por primera vez en la pantalla, lo que es un hito importante en la percepción del usuario de la carga de la página, mientras que **Time To Interactive** marca el punto en el que la página parece lo suficientemente lista para controlar las interacciones del usuario.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="Sección Métricas" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   Sección **Métricas**  
:::image-end:::  

Elija el botón de alternancia resaltado en la siguiente figura para mostrar una descripción para cada métrica y elija **Obtener** más información para leer la documentación al respecto.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Elija el botón de alternancia resaltado para expandir los elementos de métricas" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Elija el botón de alternancia resaltado para expandir los elementos de métricas  
:::image-end:::  

Debajo de Métricas se muestra una colección de capturas de pantalla que muestran cómo se cargó la página.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Capturas de pantalla de cómo se veía la página durante la carga" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Capturas de pantalla de cómo se veía la página durante la carga  
:::image-end:::  

La sección Oportunidades proporciona **sugerencias** específicas sobre cómo mejorar el rendimiento de carga de esta página específica.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Sección Oportunidades" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Sección **Oportunidades**  
:::image-end:::  

Elija una oportunidad para obtener más información sobre él.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminar la oportunidad de recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Eliminar la oportunidad de recursos de bloqueo de** representación  
:::image-end:::  

Elija **Obtener más información** para mostrar documentación sobre por qué es importante una oportunidad y recomendaciones específicas sobre cómo solucionarla.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentación para la oportunidad Eliminar recursos de bloqueo de representación" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Documentación para la **oportunidad Eliminar recursos de bloqueo de** representación  
:::image-end:::  

La **sección Diagnóstico proporciona** más información sobre los factores que contribuyen al tiempo de carga de la página.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="Sección Diagnóstico" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   Sección **Diagnóstico**  
:::image-end:::  

La **sección Auditorías pasadas** muestra lo que el sitio está haciendo correctamente.  Elija expandir la sección.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="Sección Auditorías pasadas" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   Sección **Auditorías pasadas**  
:::image-end:::  

## <a name="step-2-experiment"></a>Paso 2: Experimento  

La sección Oportunidades del informe de auditoría le ofrece sugerencias sobre cómo mejorar el rendimiento de la página.  En esta sección, se implementan los cambios recomendados en la base de código, auditando el sitio después de cada cambio para medir cómo afecta a la velocidad del sitio.  

### <a name="enable-text-compression"></a>Habilitar compresión de texto  

El informe indica que evitar enormes cargas de red es una de las principales oportunidades para mejorar el rendimiento de la página.  Habilitar la compresión de texto es una oportunidad para mejorar el rendimiento de la página.  

La compresión de texto es cuando se reduce o se comprime el tamaño de un archivo de texto antes de enviarlo a través de la red.  Similar a cómo archivar un directorio antes de enviarlo para reducir el tamaño.  

Antes de habilitar la compresión, estas son algunas formas de comprobar manualmente si los recursos de texto están comprimidos.  

1.  Elija la **herramienta Red.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panel Red" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       La **herramienta Red**  
    :::image-end:::  
    
1.  Elija el **icono Configuración de** red.  
1.  Seleccione la casilla **Usar filas de solicitud grandes.**  Aumenta el alto de las filas de la tabla de solicitudes de red.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Filas grandes en la tabla de solicitudes de red" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Filas grandes en la tabla de solicitudes de red  
    :::image-end:::  
    
1.  Si no **se muestra** la columna Tamaño de la tabla de solicitudes de red, elija el encabezado de la tabla > **Size**.  

Cada **celda Size** muestra dos valores.  El valor superior es el tamaño del recurso descargado.  
El valor inferior es el tamaño del recurso sin comprimir.  Si los dos valores son los mismos, no se está comprimiendo el recurso cuando se envía a través de la red.  Por ejemplo, en la figura anterior, los valores superior e inferior `bundle.js` para son `1.2 MB` y `1.2 MB` .  

Compruebe la compresión inspeccionando los encabezados HTTP de un recurso:  

1.  Elija `bundle.js` .  
1.  Elija el panel **Encabezados.**  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="Panel Encabezados" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       Panel **Encabezados**  
    :::image-end:::  
    
1.  Busque un **encabezado en la sección Encabezados** de `content-encoding` respuesta.  No `content-encoding` se muestra un encabezado, lo que significa que no se `bundle.js` comprimió.  Cuando se comprime un recurso, este encabezado normalmente se establece en `gzip` , `deflate` o `br` .  Para obtener una explicación de los valores, vaya a [Directivas][MDNContentEncodingDirectives].  

Suficiente con las explicaciones.  Hora de realizar algunos cambios.  Habilite la compresión de texto agregando un par de líneas de código:  

1.  En la pestaña editor, elija **server.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Editar server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Editar `server.js`  
    :::image-end:::  
    
1.  Agregue el siguiente código a **server.js**.  Asegúrese de colocar antes `app.use(compression())` `app.use(express.static('build'))` .  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > Por lo general, debe instalar el paquete a través de algo `compression` como , pero esto ya se ha hecho por `npm i -S compression` usted.  
    
1.  Espere a que Glitch implemente la nueva compilación del sitio.  La animación de lujo junto **a Herramientas** significa que el sitio se está recompilando y reimplementando.  El cambio está listo cuando desaparece la animación junto **a Herramientas.**  Elija **Mostrar** y **vuelva a elegir En una nueva** ventana.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Use los flujos de trabajo que aprendió anteriormente para comprobar manualmente que la compresión funciona:  

1.  Vuelva a la pestaña de demostración y actualice la página.  La **columna** Tamaño ahora debe mostrar 2 valores diferentes para recursos de texto como `bundle.js` .  En la figura siguiente, el valor superior de for es el tamaño del archivo que se envió a través de la red y el valor inferior de es el tamaño del archivo `256 KB` `bundle.js` sin `1.2 MB` comprimir.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La columna Tamaño muestra ahora 2 valores diferentes para recursos de texto" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       La **columna** Tamaño muestra ahora 2 valores diferentes para recursos de texto  
    :::image-end:::  
    
1.  La **sección Encabezados de** respuesta para ahora debe incluir un `bundle.js` `content-encoding: gzip` encabezado.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La sección Encabezados de respuesta ahora contiene un encabezado de codificación de contenido" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       La **sección Encabezados de** respuesta ahora contiene un encabezado de codificación de contenido  
    :::image-end:::  
    
Audite la página de nuevo para medir qué tipo de compresión de texto de impacto tiene en el rendimiento de carga de la página:  

1.  Elija la **herramienta Auditorías.**  
1.  Elija **Realizar una auditoría** \( Realizar una auditoría ![ ](../media/perform-icon.msft.png) \).  
1.  Deje la configuración igual que antes.  
1.  Elija **Ejecutar auditoría**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Informe auditorías después de habilitar la compresión de texto" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Informe auditorías después de habilitar la compresión de texto  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  La puntuación general de rendimiento debería haber aumentado, lo que significa que el sitio es cada vez más rápido.  

#### <a name="text-compression-in-the-real-world"></a>Compresión de texto en el mundo real  

La mayoría de los servidores realmente tienen correcciones sencillas como esta para habilitar la compresión.  Simplemente haga una búsqueda sobre cómo configurar cualquier servidor que use para comprimir texto.  

### <a name="resize-images"></a>Cambiar el tamaño de las imágenes  

El informe indica que evitar enormes cargas de red es una de las principales oportunidades para mejorar el rendimiento de la página.  El tamaño de las imágenes ayuda a reducir el tamaño de la carga de red.  Si el usuario está viendo las imágenes en una pantalla de dispositivo móvil de 500 píxeles de ancho, realmente no tiene sentido enviar una imagen de 1500 píxeles.  Lo ideal es enviar una imagen de 500 píxeles, como máximo.  

1.  En el informe, elija **Evitar enormes cargas de red** para mostrar qué imágenes deben cambiar de tamaño.  Parece que 2 de los archivos jpg tienen más de 2000 KB, lo que es más grande de lo necesario.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  De nuevo en la pestaña editor, abra `src/model.js` .  
1.  Reemplace `const dir = 'big'` por `const dir = 'small'` .  Este directorio contiene copias de las mismas imágenes que se han cambiado de tamaño.  
1.  Audite la página de nuevo para mostrar cómo afecta el cambio al rendimiento de carga.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Un informe de auditorías después de redimensionar imágenes" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Un informe de auditorías después de redimensionar imágenes  
    :::image-end:::  
    
El cambio que se muestra solo tiene un efecto menor en la puntuación de rendimiento general.  Sin embargo, una cosa que la puntuación no muestra claramente es la cantidad de datos de red que está guardando los usuarios.  El tamaño total de las fotos antiguas era de unos 5,3 megabytes, mientras que ahora solo es de 0,18 megabytes.  

#### <a name="resizing-images-in-the-real-world"></a>Cambio de tamaño de imágenes en el mundo real  

Para una aplicación pequeña, hacer un cambio de tamaño único como este puede ser lo suficientemente bueno.  Pero para una aplicación grande, esto obviamente no es escalable.  Estas son algunas estrategias para administrar imágenes en aplicaciones grandes:  

*   Cambie el tamaño de las imágenes durante el proceso de compilación.  
*   Cree varios tamaños de cada imagen durante el proceso de compilación y, a continuación, `srcset` úselo en el código.  En tiempo de ejecución, el explorador se encarga de elegir el tamaño más adecuado para el dispositivo.  
    <!--Navigate to [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Usa una red CDN de imagen que te permite cambiar el tamaño dinámicamente de una imagen cuando la solicites.  
*   Como mínimo, optimice cada imagen.  Esto puede crear grandes ahorros.  
  La optimización es cuando se ejecuta una imagen a través de un programa especial que reduce el tamaño del archivo de imagen.  Para obtener más sugerencias, vaya a [Optimización de imagen esencial.][EssentialImageOptimization]  
    
### <a name="eliminate-render-blocking-resources"></a>Eliminar recursos de bloqueo de representación  

El informe más reciente indica que eliminar los recursos de bloqueo de representación es ahora la mayor oportunidad.  

Un recurso de bloqueo de representación es un archivo JavaScript o CSS externo que el explorador debe descargar, analizar y ejecutar antes de mostrar la página.  El objetivo es ejecutar solo el código CSS y JavaScript principal necesario para mostrar la página correctamente.  

La primera tarea, a continuación, es buscar código que no es necesario ejecutar en la carga de página.  

1.  Elija **Eliminar recursos de bloqueo de representación** para mostrar los recursos que están bloqueando:  
    `lodash.js` y `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Más información sobre la oportunidad Eliminar recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Más información sobre la oportunidad **Eliminar recursos de bloqueo de** representación  
    :::image-end:::  
    
1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) `Coverage` **** para abrir el menú comando, empiece a escribir y, a continuación, elija Mostrar cobertura .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Abra el menú comando desde el panel Auditorías" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Abra el menú comando desde el panel **Auditorías**  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="La herramienta Cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       La **herramienta Cobertura**  
    :::image-end:::  
    
1.  Elija **Actualizar** \( ![ Actualizar ](../media/reload-icon.msft.png) \).  La **herramienta Cobertura** proporciona información general sobre la cantidad de código en , y se ejecuta mientras se carga la `bundle.js` `jquery.js` `lodash.js` página.  En la figura siguiente, aproximadamente el 76 % y el 30 % de los archivos jQuery y Lodash no se usan, respectivamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="El informe de cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       El informe de cobertura  
    :::image-end:::  
    
1.  Elija la `jquery.js` fila.  DevTools abre el archivo en la **herramienta Orígenes.**  Si se ejecutó una línea de código, aparece una barra azul junto a ella.  Una barra roja significa que la línea de código no se ha ejecutado y, definitivamente, no es necesaria en la carga de la página web.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Visualización del archivo jQuery en la herramienta Orígenes" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Visualización del archivo jQuery en la **herramienta Orígenes**  
    :::image-end:::  
    
1.  Desplácese por el código jQuery.  Algunas de las líneas que se ejecutan son solo comentarios.  Para quitar comentarios y reducir el tamaño del archivo, ejecute el código a través de una aplicación o un script de compresión.  

En resumen, cuando trabaja con su **** propio código, la herramienta Cobertura le ayuda a analizar el código, línea por línea y solo enviar el código necesario para la carga de página.  

¿Son `jquery.js` necesarios los archivos y incluso para cargar la `lodash.js` página?  La **herramienta de bloqueo** de solicitudes muestra lo que sucede cuando los recursos no están disponibles.  

1.  Elija la **herramienta Red.**  
1.  Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) para abrir de nuevo el menú comando.  
1.  Empiece a escribir `blocking` y, a continuación, **elija Mostrar bloqueo de solicitudes**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="La herramienta de bloqueo de solicitudes" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       La **herramienta de bloqueo de solicitudes**  
    :::image-end:::  
    
1.  Elija **Agregar patrón** \( Agregar patrón ![ ](../media/add-pattern-icon.msft.png) \), escriba `/libs/*` y, a continuación, `Enter` seleccione para confirmar.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Agregar un patrón para bloquear cualquier solicitud al directorio libs" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Agregar un patrón para bloquear cualquier solicitud al `libs` directorio  
    :::image-end:::  
    
1.  Actualiza la página.  Las solicitudes jQuery y Lodash son de color rojo, lo que significa que las solicitudes se bloquearon.   La página aún se carga y es interactiva, por lo que parece que estos recursos no son necesarios.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="El panel Red muestra que las solicitudes se han bloqueado" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       La **herramienta Red** muestra que las solicitudes se han bloqueado  
    :::image-end:::  
    
1.  Elija **Quitar todos los patrones** \( Quitar todos los patrones ![ ](../media/remove-icon.msft.png) \) para eliminar el patrón de `/libs/*` bloqueo.  
    
En general, la **herramienta de bloqueo de** solicitudes es útil para simular cómo se comporta la página cuando un recurso determinado no está disponible.  

Ahora, quite las referencias a estos archivos del código y vuelva a auditar la página:  

1.  De nuevo en la pestaña editor, abra `template.html` .  
1.  Elimina `<script src="/libs/lodash.js">` y `<script src="/libs/jquery.js"></script>`.  
1.  Espere a que el sitio vuelva a compilarse e implementarse de nuevo.  
1.  Vuelva a auditar la página desde la **herramienta Auditorías.**  La puntuación general debería haber mejorado de nuevo.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Un informe de auditorías después de quitar los recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Un **informe de auditorías** después de quitar los recursos de bloqueo de representación  
    :::image-end:::  
    
#### <a name="optimizing-the-critical-rendering-path-in-the-real-world"></a>Optimización de la ruta de representación crítica en el mundo real  

La **ruta de representación crítica** hace referencia al código que necesita para cargar una página.  En general, acelera la carga de la página solo enviando código crítico durante la carga de la página y, a continuación, cargando todo lo demás.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   Es poco probable que pueda encontrar scripts que pueda quitar directamente, pero es posible que encuentre muchos scripts que no necesita solicitar durante la carga de la página y, en su lugar, se pueden solicitar de forma asincrónica.  <!--Navigate to [Using async or defer][async].  -->  
*   Si usa un marco, compruebe si tiene un modo de producción.  Este modo puede usar [][WebpackTreeShaking] una característica como la agitación de árbol para eliminar el código innecesario que bloquea la representación crítica.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <a name="do-less-main-thread-work"></a>Hacer menos trabajo de subprocesos principales  

El informe más reciente muestra algunos posibles ahorros menores en la sección Oportunidades, pero si mira hacia abajo en la sección Diagnósticos, parece que el cuello de botella más grande es demasiada actividad de subprocesos principal.  

El subproceso principal es donde el explorador realiza la mayor parte del trabajo necesario para mostrar una página, como analizar y ejecutar HTML, CSS y JavaScript.  

El objetivo es usar el panel Rendimiento para analizar el trabajo que está realizando el subproceso principal mientras se carga la página y encontrar formas de aplazar o quitar el trabajo innecesario.  

1.  Elija la **herramienta** Rendimiento.  
1.  Elija **Configuración de captura** \( Configuración de captura ![ ](../media/capture-icon.msft.png) \).  
1.  Establezca **Network** en **Slow 3G** y **CPU** en **6x slowdown**.  Los dispositivos móviles suelen tener más restricciones de hardware que portátiles o escritorios, por lo que esta configuración te permite experimentar la carga de la página como si estuvieras usando un dispositivo menos eficaz.  
1.  Elija **Actualizar** \( ![ Actualizar ](../media/reload-icon.msft.png) \).  DevTools actualiza la página y, a continuación, genera una visualización de todo el trabajo realizado para cargar la página.  Esta visualización se conoce como **seguimiento**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Seguimiento de la herramienta rendimiento de la carga de página" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       Seguimiento **de la herramienta** rendimiento de la carga de página  
    :::image-end:::  
    
El seguimiento muestra la actividad cronológicamente, de izquierda a derecha.  Los gráficos DE FPS, CPU y NET en la parte superior le dan información general sobre fotogramas por segundo, actividad de CPU y actividad de red.  El bloque de color amarillo resaltado en la figura después de la siguiente, la CPU estaba completamente ocupada con la actividad de scripting.  Esta es una pista de que puede acelerar la carga de página haciendo menos trabajo de JavaScript.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="La sección Información general del seguimiento" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   La sección Información general del seguimiento  
:::image-end:::  

Investigue el seguimiento para encontrar formas de hacer menos trabajo de JavaScript:  

1.  Elija la **sección Timings** para expandirla.  Basándose en el hecho de que puede haber un montón de medidas de [timings][MDNUserTimingApi] de React, parece que la aplicación de Tony está usando el modo de desarrollo de React.  Cambiar al modo de producción de React puede producir algunas ganancias de rendimiento fáciles.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="Sección Timings" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       Sección **Timings**  
    :::image-end:::  
    
1.  Elija **Timings** de nuevo para contraer esa sección.  
1.  Examine la **sección** Principal.  En esta sección se muestra un registro cronológico de la actividad del subproceso principal, de izquierda a derecha.  El eje Y (de arriba a abajo) muestra por qué se produjeron eventos.  Por ejemplo, en la higoría después de lo siguiente, el evento provocó la ejecución de la función, lo que provocó la ejecución, lo que provocó la `Evaluate Script` `(anonymous)` `(anonymous)` `__webpack__require__` ejecución, y así sucesivamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="Sección Principal" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       Sección **** Principal  
    :::image-end:::  
    
1.  Desplácese hacia abajo hasta la parte inferior de **la sección** Principal.  Cuando se usa un marco, la mayor parte de la actividad superior se debe al marco, que suele estar fuera de su control.  La actividad causada por la aplicación suele estar en la parte inferior.  En esta aplicación, parece que una función llamada está provocando muchas solicitudes `App` a una `mineBitcoin` función.  Parece que Tony puede estar usando los dispositivos de sus fans para extraer criptodivisa...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Mantener el mouse en la actividad mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Mantener el mouse en la `mineBitcoin` actividad  
    :::image-end:::  
    
    > [!NOTE]
    > Aunque las solicitudes que realiza el marco suelen estar fuera de tu control, a veces puedes estructurar la aplicación de una manera que haga que el marco se ejecute de forma ineficaz.  Reestructurar la aplicación para usar el marco de forma eficiente es una forma de hacer menos trabajo principal de subprocesos.  Sin embargo, esto requiere una comprensión profunda de cómo funciona el marco y qué tipo de cambios realiza en su propio código para poder usar el marco de trabajo de forma más eficiente.  
    
1.  Expanda la **sección Abajo** arriba.  Esta pestaña desglosa las actividades que más tiempo tardaron en realizarse.  Si no se muestra nada en la Bottom-Up, elija la etiqueta de **la sección** Principal.  La **sección Abajo arriba** solo muestra información sobre cualquier actividad o grupo de actividad que haya seleccionado actualmente.  Por ejemplo, si elige una de las actividades, la sección Abajo arriba solo mostrará `mineBitcoin` información para esa actividad. ****  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="La Bottom-Up pestaña" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       Ficha **Abajo arriba**  
    :::image-end:::  
    
La **columna Tiempo de** autoservicio muestra cuánto tiempo se ha invertido directamente en cada actividad.  Por ejemplo, en la siguiente figura, aproximadamente el 63 % del tiempo de subproceso principal se ha invertido en la `mineBitcoin` función.  

Tiempo para revisar si el uso del modo de producción y la reducción de la actividad de JavaScript pueden acelerar la carga de la página.  Comience con el modo de producción:  

1.  En la pestaña editor, abra `webpack.config.js` .  
1.  Cambiar `"mode":"development"` a `"mode":"production"` .  
1.  Espere a que se implemente la nueva compilación.  
1.  Vuelva a auditar la página.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Informe auditorías después de configurar webpack para usar el modo de producción" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Informe auditorías después de configurar webpack para usar el modo de producción  
    :::image-end:::  
    
Reduzca la actividad de JavaScript quitando la solicitud a `mineBitcoin` :  

1.  En la pestaña editor, abra `src/App.jsx` .  
1.  Comenta la solicitud en `this.mineBitcoin(1500)` `constructor` el archivo .  
1.  Espere a que se implemente la nueva compilación.  
1.  Vuelva a auditar la página.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Un informe de auditorías después de quitar el trabajo de JavaScript innecesario" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Un informe de auditorías después de quitar el trabajo de JavaScript innecesario  
    :::image-end:::  
    
Parece que el último cambio causó un salto masivo en el rendimiento.  

> [!NOTE]
> En esta sección se proporciona una introducción bastante breve al panel Rendimiento.  Para obtener más información sobre cómo analizar el rendimiento de la página, vaya a [Referencia de análisis de rendimiento][DevtoolsEvaluatePerformanceReference].  

<!--todo: add section when available -->  

#### <a name="doing-less-main-thread-work-in-the-real-world"></a>Hacer menos trabajo de subprocesos principales en el mundo real  

En general, la **herramienta** Rendimiento es la forma más común de comprender qué actividad realiza el sitio a medida que se carga y encontrar formas de quitar actividad innecesaria.  

Si prefiere un enfoque que se parece más a , la API de tiempo de usuario le permite marcar arbitrariamente determinadas fases del ciclo de vida de la aplicación, con el fin de realizar un seguimiento del tiempo que tarda cada una de estas `console.log()` fases. [][MDNUserTimingApi]  

## <a name="summary"></a>Resumen  

*   Siempre que se configure para optimizar el rendimiento de carga de un sitio, comience siempre con una auditoría.  La auditoría establece una línea base y le ofrece sugerencias sobre cómo mejorar.  
*   Realice un cambio a la vez y audite la página web después de cada cambio para mostrar cómo ese cambio aislado afecta al rendimiento.  

<!--
## Next steps  

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referencia de análisis de rendimiento | Microsoft Docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introducción a la clase de desarrollo web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimización de imagen esencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directivas: codificación de contenido | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "Api de tiempo de usuario | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Tree Shaking | webpack"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
