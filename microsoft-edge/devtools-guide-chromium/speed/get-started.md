---
title: Optimizar la velocidad del sitio web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 42b742316ccaa64aa35fc1d21c5277e448b2d5b7
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984811"
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





# Optimizar la velocidad del sitio web con Microsoft Edge DevTools   



## Objetivo del tutorial  

En este tutorial aprenderás a usar Microsoft Edge DevTools para encontrar formas de cargar tus sitios web más rápido.  

## Requisitos previos  

*   Debe tener experiencia básica de desarrollo web, similar a lo que enseñamos esta [Introducción a la clase de desarrollo web][CourseraIntroductionWebDevelopmentClass].  
*   No es necesario que sepa nada sobre el rendimiento de la carga.  Puede obtener más información en este tutorial.  

## Introducción   

Es Tony.  Tony es muy famoso en el gato de la sociedad.  Ha creado un sitio web para que sus ventiladores puedan conocer sus alimentos favoritos.  Sus ventiladores adoran el sitio, pero Tony mantiene las quejas auditivas que el sitio carga lentamente.  Tony le ha pedido que le ayude a acelerar el sitio.  

:::image type="complex" source="../media/speed-tony.msft.png" alt-text="Tony el gato" lightbox="../media/speed-tony.msft.png":::
   Tony el gato  
:::image-end:::  

## Paso 1: auditar el sitio   

Siempre que lo establezca para mejorar el rendimiento de la carga de un sitio, **empiece siempre con una auditoría**.  
La auditoría tiene dos funciones importantes:  

*   Crea una **línea base** para medir los cambios posteriores.  
*   Le ofrece **consejos útiles** sobre qué cambios son más impactantes.  
    
### Configuración   

En primer lugar, debe configurar el sitio para poder realizar cambios en él más adelante.  

1.  [Abra el código fuente del sitio](https://glitch.com/edit/#!/tony).  Esta pestaña se conoce como la **pestaña Editor**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js.msft.png" alt-text="Ficha Editor" lightbox="../media/speed-glitch-tony-server-js.msft.png":::
       **Ficha Editor**  
    :::image-end:::  
    
1.  Seleccione **Tony**.  Aparece un menú.  
    
    :::image type="complex" source="../media/speed-glitch-tony-server-js-remix-project.msft.png" alt-text="El menú que aparece después de hacer clic en Tony" lightbox="../media/speed-glitch-tony-server-js-remix-project.msft.png":::
       El menú que aparece después de hacer clic en **Tony**  
    :::image-end:::  
    
1.  Seleccione **proyecto Remix**.  El nombre del proyecto cambia de **Tony** a algún nombre generado aleatoriamente.  Ahora tiene su propia copia modificable del código.  Más adelante, puedes realizar cambios en este código.  
1.  Seleccione **Mostrar** y seleccione **en una nueva ventana**.  La demostración se abre en una nueva pestaña.  Esta pestaña se conoce como la **pestaña demo**.  Es posible que el sitio tarde un rato en cargarse.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live.msft.png" alt-text="La ficha demo" lightbox="../media/speed-glitch-tony-show-live.msft.png":::
       La ficha demo  
    :::image-end:::  
    
1.  Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).  Microsoft Edge DevTools se abre junto con la demostración.  
    
    :::image type="complex" source="../media/speed-glitch-tony-show-live-console.msft.png" alt-text="DevTools y la demostración" lightbox="../media/speed-glitch-tony-show-live-console.msft.png":::
       DevTools y la demostración  
    :::image-end:::  
    
Para el resto de las capturas de pantalla de este tutorial, DevTools se muestra en una ventana independiente.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú comando, escriba `Undock` y, a continuación, seleccione **desacoplar en ventana independiente**.  

:::image type="complex" source="../media/speed-console.msft.png" alt-text="DevTools desacoplado" lightbox="../media/speed-console.msft.png":::
   DevTools desacoplado  
:::image-end:::  

### Establecer una línea base   

La línea base es un registro de cómo se realizó el sitio antes de realizar alguna mejora en el rendimiento.  

1.  Seleccione la pestaña **auditorías** .  Es posible que esté oculto detrás **del** botón \ ( ![ más paneles ][ImageMorePanelsIcon] \).  Hay un Lighthouse en este panel porque el proyecto que alimenta el panel auditoría se denomina **Lighthouse**.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    :::image type="complex" source="../media/speed-audits-performance.msft.png" alt-text="Panel auditorías" lightbox="../media/speed-audits-performance.msft.png":::
       Panel **auditorías**  
    :::image-end:::  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Ajuste las opciones de configuración de auditoría a las de la ilustración anterior.  A continuación se explican las diferentes opciones:  
    
    *   **Dispositivo**.  Configuración para **dispositivos móviles** cambia la cadena de agente de usuario y simula un área de visualización móvil.  La configuración en el **escritorio** simplemente deshabilita los cambios en el **teléfono móvil** .  
    *   **Auditorías**.  Si deshabilita una categoría, evitará que el panel auditoría las ejecute y las excluirá de su informe.  Deje las otras categorías habilitadas si desea ver los tipos de recomendaciones proporcionadas.  Al deshabilitar las categorías, se acelera ligeramente el proceso de auditoría.  
    *   **Limitación**.  Configurada para **simular lentitud de 4G, con una ralentización** de la CPU de 4x simula las condiciones típicas de la navegación en un dispositivo móvil.  Se denomina "simulado" porque en realidad el panel auditorías no se limita durante el proceso de auditoría.  En su lugar, simplemente extrapola cuánto tiempo tardará la página en cargarse en condiciones móviles.  Por otro lado, la opción de configuración **aplicado** , limita la CPU y la red, con la compensación de un proceso de auditoría más largo.  
    *   **Borrar almacenamiento**.  Al habilitar esta casilla, se borra todo el almacenamiento asociado a la página antes de cada auditoría.  Deje esta configuración activada si desea auditar la experiencia de los visitantes por primera vez en su sitio.  Deshabilite esta configuración cuando quiera la experiencia de repetición de la visita.  
    
1.  Seleccione **Ejecutar Auditorías**.  Después de 10 a 30 segundos, el panel auditoría muestra un informe del rendimiento del sitio.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png" alt-text="Informe para el panel auditoría del rendimiento del sitio" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png":::
       Informe para el panel auditoría del rendimiento del sitio  
    :::image-end:::  
    
#### Control de errores de informe   

Si alguna vez recibe un error en el informe del panel auditorías, pruebe a ejecutar la pestaña demostración desde una ventana **InPrivate** sin ninguna otra pestaña abierta.  Esto asegura que está ejecutando Microsoft Edge desde un estado limpio.  Las extensiones de Microsoft Edge en particular suelen interferir con el proceso de auditoría.  

<!--todo: add screen capture for error in audit -->  
<!--
:::image type="complex" source="../media/speed-.msft.png" alt-text="A report that errored" lightbox="../media/speed-.msft.png":::
   A report that errored  
:::image-end:::  
-->  

### Comprender el informe   

El número que aparece en la parte superior del informe es la puntuación de rendimiento general para el sitio.  Después, a medida que haga cambios en el código, debería ver que este número ha aumentado.  Una puntuación mayor supone un mejor rendimiento.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png" alt-text="La puntuación general de rendimiento" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-metrics-highlighted.msft.png":::
   La puntuación general de rendimiento  
:::image-end:::  

La sección de **métricas** proporciona medidas cuantitativas en el rendimiento del sitio.  Cada métrica proporciona información sobre un aspecto diferente del rendimiento.  Por ejemplo, la **primera pintura con contenido** le indica cuando el contenido se pinta por primera vez en la pantalla, lo que es un hito importante en la percepción del usuario de la carga de la página, mientras que el tiempo de marca **interactiva** es el punto en el que la página aparece lo suficientemente lista para controlar las interacciones del usuario.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png" alt-text="La sección métrica" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-collapsed-highlighted.msft.png":::
   La sección **métrica**  
:::image-end:::  

Seleccione el botón de alternancia resaltado en la siguiente ilustración para ver una descripción de cada métrica y haga clic en **obtener más información** para leer la documentación de la misma.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png" alt-text="Seleccione el botón de alternancia resaltado para expandir los elementos de métrica" lightbox="../media/speed-glitch-tony-remix-audits-performance-metrics-expanded.msft.png":::
   Seleccione el botón de alternancia resaltado para expandir los elementos de métrica  
:::image-end:::  

A continuación, se muestra una colección de capturas de pantallas en la que se muestra cómo se ha cargado la página.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="Capturas de pantallas del aspecto de la página durante la carga" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   Capturas de pantallas del aspecto de la página durante la carga  
:::image-end:::  

La sección **oportunidades** proporciona sugerencias específicas sobre cómo mejorar el rendimiento de la carga de esta página específica.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png" alt-text="La sección oportunidades" lightbox="../media/speed-glitch-tony-remix-audits-performance-view-trace.msft.png":::
   La sección **oportunidades**  
:::image-end:::  

Seleccione una oportunidad para obtener más información sobre ella.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png" alt-text="Eliminar la oportunidad de recursos de bloqueo de procesamiento" lightbox="../media/speed-glitch-tony-remix-audits-performance-opportunities-expanded.msft.png":::
   **Eliminar la oportunidad de recursos de bloqueo de procesamiento**  
:::image-end:::  

Seleccione **más información** para ver la documentación sobre por qué es importante una oportunidad y recomendaciones específicas sobre cómo corregirla.  

:::image type="complex" source="../media/speed-web-dev-performance-audits.msft.png" alt-text="Documentación de la oportunidad eliminar recursos de bloqueo de procesamiento" lightbox="../media/speed-web-dev-performance-audits.msft.png":::
   Documentación de la oportunidad **eliminar recursos de bloqueo de procesamiento**  
:::image-end:::  

La sección **diagnósticos** proporciona más información sobre los factores que contribuyen al tiempo de carga de la página.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png" alt-text="La sección diagnósticos" lightbox="../media/speed-glitch-tony-remix-audits-performance-diagnostics.msft.png":::
   La sección **diagnósticos**  
:::image-end:::  

En la sección de **auditorías superada** se muestra lo que el sitio está haciendo correctamente.  Seleccione para expandir la sección.  

:::image type="complex" source="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png" alt-text="La sección de auditorías superada" lightbox="../media/speed-glitch-tony-remix-audits-performance-passed-audits.msft.png":::
   La sección de **auditorías superada**  
:::image-end:::  

## Paso 2: experimento   

La sección oportunidades de su informe de auditoría le ofrece sugerencias sobre cómo mejorar el rendimiento de la página.  En esta sección, implementará los cambios recomendados en el código base, auditando el sitio después de cada cambio para medir cómo afecta a la velocidad del sitio.  

### Habilitar compresión de texto   

El informe dice que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.  Habilitar la compresión de texto es una oportunidad para mejorar el rendimiento de la página.  

La compresión de texto es cuando se reduce, o comprime, el tamaño de un archivo de texto antes de enviarlo a través de la red.  Tipo de cómo puede comprimir una carpeta antes de enviarle un mensaje de correo electrónico para reducir el tamaño.  

Antes de habilitar la compresión, hay un par de maneras de comprobar manualmente si los recursos de texto están comprimidos.  

1.  Seleccione la pestaña **red** .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network.msft.png" alt-text="Panel red" lightbox="../media/speed-glitch-tony-remix-network.msft.png":::
       Panel **red**  
    :::image-end:::  
    
1.  Seleccione el icono de **configuración de red** .  
1.  Seleccione la casilla **usar filas de solicitudes grandes** .  Aumenta el alto de las filas de la tabla de solicitudes de red.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png" alt-text="Filas grandes en la tabla solicitudes de red" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows.msft.png":::
       Filas grandes en la tabla solicitudes de red  
    :::image-end:::  
    
1.  Si no ve la columna **tamaño** en la tabla de solicitudes de red, haga clic en el encabezado de tabla y, a continuación, seleccione **tamaño**.  

Cada celda de **tamaño** muestra dos valores.  El valor superior es el tamaño del recurso descargado.  
El valor inferior es el tamaño del recurso sin comprimir.  Si los dos valores son iguales, el recurso no se comprimirá cuando se envíe a través de la red.  Por ejemplo, en la ilustración anterior, los valores superiores e inferiores de `bundle.js` is `1.2 MB` y `1.2 MB` .  

Para comprobar la compresión, inspeccione los encabezados HTTP de un recurso:  

1.  Seleccione **bundle.js**.  
1.  Seleccione la pestaña **encabezados** .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png" alt-text="La pestaña encabezados" lightbox="../media/speed-glitch-tony-remix-network-use-large-request-rows-bundle-js.msft.png":::
       La pestaña **encabezados**  
    :::image-end:::  
    
1.  Busque un encabezado en la sección de **encabezados de respuesta** `content-encoding` .  No debe ver ninguno, lo que significa que `bundle.js` no se ha comprimido.  Cuando se comprime un recurso, este encabezado suele establecerse en `gzip` , `deflate` o `br` .  Vea las [directivas][MDNContentEncodingDirectives] para obtener una explicación de estos valores.  

Es suficiente con las explicaciones.  Para hacer algunos cambios.  Habilite la compresión de texto agregando un par de líneas de código:  

1.  En la pestaña Editor, haga clic en **server.js**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js.msft.png" alt-text="Modificar server.js" lightbox="../media/speed-glitch-tony-remix-server-js.msft.png":::
       Editar `server.js`  
    :::image-end:::  
    
1.  Agregue el código siguiente a **server.js**.  Asegúrate de poner `app.use(compression())` antes `app.use(express.static('build'))` .  

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
    > Normalmente, tiene que instalar el `compression` paquete a través de algo similar `npm i -S compression` , pero esto ya se ha hecho para usted.  
    
1.  Espere a que se implemente la nueva compilación del sitio.  La animación más sofisticada junto a **herramientas** significa que el sitio se vuelve a generar y a implementar.  El cambio está listo cuando la animación junto a **herramientas** desaparece.  Seleccione **Mostrar** y vuelva a seleccionar **una nueva ventana** .  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-server-js-edited.msft.png" alt-text="The animation that indicates that the site is getting built" lightbox="../media/speed-glitch-tony-remix-server-js-edited.msft.png":::
       The animation that indicates that the site is getting built  
    :::image-end:::  
    -->  
    
Use los flujos de trabajo que aprendió anteriormente para comprobar manualmente que la compresión funciona:  

1.  Vuelva a la pestaña demo y vuelva a cargar la página.  La columna **tamaño** debería mostrar ahora dos valores diferentes para recursos de texto como `bundle.js` .  En la ilustración siguiente, el valor superior de `256 KB` para `bundle.js` es el tamaño del archivo que se envió a través de la red y el valor inferior de `1.2 MB` es el tamaño de archivo sin comprimir.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-main.msft.png" alt-text="La columna tamaño muestra ahora 2 valores diferentes para los recursos de texto" lightbox="../media/speed-glitch-tony-remix-network-main.msft.png":::
       La columna **tamaño** muestra ahora 2 valores diferentes para los recursos de texto  
    :::image-end:::  
    
1.  La sección de **encabezados de respuesta** de `bundle.js` ahora debe incluir un `content-encoding: gzip` encabezado.
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png" alt-text="La sección de encabezados de respuesta ahora contiene un encabezado de codificación de contenido" lightbox="../media/speed-glitch-tony-remix-network-bundle-js-headers-response.msft.png":::
       La sección de **encabezados de respuesta** ahora contiene un encabezado de codificación de contenido  
    :::image-end:::  
    
Audite de nuevo la página para medir qué tipo de compresión de texto de impacto tiene en el rendimiento de carga de la página:  

1.  Seleccione la pestaña **auditorías** .  
1.  Seleccione **realizar una auditoría** \ ( ![ realizar una auditoría ][ImagePerformIcon] \).  
1.  Deje la configuración igual que antes.  
1.  Seleccione **Ejecutar auditoría**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png" alt-text="Un informe de auditoría después de habilitar la compresión de texto" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance.msft.png":::
       Un informe de auditoría después de habilitar la compresión de texto  
    :::image-end:::  
    
<!--  Woohoo!  That looks like progress.  -->  La puntuación de rendimiento general debería haber aumentado, lo que significa que el sitio se está acelerando.  

#### Compresión de texto en el mundo real   

La mayoría de los servidores realmente tienen soluciones sencillas como esta para habilitar la compresión.  Solo tiene que hacer una búsqueda para configurar cualquier servidor que use para comprimir texto.  

### Cambiar el tamaño de las imágenes   

El informe indica que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.  Cambiar el tamaño de las imágenes ayuda a reducir el tamaño de la carga de red.  Si el usuario está viendo las imágenes en una pantalla de dispositivo móvil de 500 píxeles de ancho, no hay ningún punto para enviar una imagen de ancho de 1500 píxeles.  Lo ideal es que envíes una imagen de ancho de 500 píxeles, como máximo.  

1.  En el informe, haga clic en **evitar cargas de red enormes** para ver las imágenes que se deben cambiar de tamaño.  Parece ser que 2 de los archivos jpg superan 2000 KB, lo cual es más grande de lo necesario.  
    
    <!--
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png" alt-text="Details about the properly size images opportunity" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png":::
       Details about the properly size images opportunity  
    :::image-end:::  
    -->
    
1.  De nuevo en la pestaña Editor, Abra `src/model.js` .  
1.  Reemplazar `const dir = 'big'` por `const dir = 'small'` .  Este directorio contiene copias de las mismas imágenes que se han cambiado de tamaño.  
1.  Audite de nuevo la página para ver cómo este cambio afecta al rendimiento de la carga.  
    
    :::image type="complex" source="../media/speed-glitch-compression-small-images-audits-performance.msft.png" alt-text="Un informe de auditoría después de cambiar el tamaño de las imágenes" lightbox="../media/speed-glitch-compression-small-images-audits-performance.msft.png":::
       Un informe de auditoría después de cambiar el tamaño de las imágenes  
    :::image-end:::  
    
Parece que el cambio sólo tiene un efecto menor en la puntuación de rendimiento general.  Sin embargo, un elemento que indica que la puntuación no se muestra claramente es cuántos datos de red está guardando los usuarios.  El tamaño total de las fotos antiguas ocupaba alrededor de 5,3 megabytes, mientras que ahora solo es de 0,18 megabytes.  

#### Cambiar el tamaño de las imágenes en el mundo real   

En el caso de una aplicación pequeña, realizar un ajuste de tamaño único como este puede ser lo suficientemente bueno.  Pero para una aplicación de gran tamaño obviamente, esto no es escalable.  Estas son algunas estrategias para administrar imágenes en aplicaciones de gran tamaño:  

*   Cambie el tamaño de las imágenes durante el proceso de compilación.  
*   Cree varios tamaños de cada imagen durante el proceso de compilación y, a continuación, utilícelos `srcset` en el código.  En tiempo de ejecución, el explorador se ocupa de elegir el tamaño más adecuado para el dispositivo.  
    <!--See [Relative-sized images][relative].  -->
    
<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   Use una CDN de imagen que le permita cambiar el tamaño de una imagen dinámicamente cuando la solicite.  
*   Como mínimo, optimiza cada imagen.  Esto puede crear enormes descuentos.  
  La optimización es cuando se ejecuta una imagen a través de un programa especial que reduce el tamaño del archivo de imagen.  Para obtener más información, consulta la [optimización básica de imágenes][EssentialImageOptimization] .  
    
### Eliminar recursos de bloqueo de procesamiento   

El último informe indica que la eliminación de recursos de bloqueo de procesamiento es ahora la mayor oportunidad.  

Un recurso de bloqueo de representación es un archivo de JavaScript o CSS externo que el explorador debe descargar, analizar y ejecutar antes de mostrar la página.  El objetivo es ejecutar solo el código CSS básico y JavaScript necesario para mostrar la página correctamente.  

La primera tarea, a continuación, es buscar código que no es necesario ejecutar en la carga de la página.  

1.  Seleccione **eliminar recursos de bloqueo de procesamiento** para ver los recursos que están bloqueando:  
    `lodash.js` y `jquery.js` .  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png" alt-text="Más información sobre la oportunidad eliminar recursos de bloqueo de procesamiento" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded.msft.png":::
       Más información sobre la oportunidad **eliminar recursos de bloqueo de procesamiento**  
    :::image-end:::  
    
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, comience a escribir `Coverage` y, a continuación, seleccione **Mostrar cobertura**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png" alt-text="Abrir el menú de comandos desde el panel auditorías" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-command-coverage.msft.png":::
       Abrir el menú de comandos desde el panel **auditorías**  
    :::image-end:::  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png" alt-text="La ficha cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage.msft.png":::
       La ficha **cobertura**  
    :::image-end:::  
    
1.  Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).  La pestaña **cobertura** proporciona una descripción general de la parte del código de `bundle.js` , `jquery.js` y `lodash.js` se ejecuta mientras se carga la página.  En la ilustración siguiente, unos 76% y un 30% de los archivos de jQuery y Lodash no se usan, respectivamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png" alt-text="El informe de cobertura" lightbox="../media/speed-glitch-tony-remix-updated-audits-performance-oppportunities-expanded-drawer-coverage-reloaded.msft.png":::
       El informe de cobertura  
    :::image-end:::  
    
1.  Seleccione la fila **jquery.js** .  DevTools abre el archivo en el panel fuentes.  Se ejecutó una línea de código si tiene una barra azul al lado.  Una barra roja significa que no se ha ejecutado y, por supuesto, no es necesaria en la carga de la página.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png" alt-text="Visualización del archivo jQuery en el panel orígenes" lightbox="../media/speed-glitch-tony-remix-updated-sources-drawer-coverage-reloaded-jquery-js.msft.png":::
       Visualización del archivo jQuery en el panel **orígenes**  
    :::image-end:::  
    
1.  Desplácese un poco por el código jQuery.  Algunas de las líneas que reciben "ejecutar" son realmente solo Comentarios.  La ejecución de este código a través de un minifier que elimina los comentarios es otra forma de reducir el tamaño de este archivo.  

En Resumen, cuando está trabajando con su propio código, la pestaña cobertura le ayuda a analizar el código, línea por línea, y solo envía el código necesario para la carga de la página.  

¿Los `jquery.js` archivos y son `lodash.js` necesarios para cargar la página?  La pestaña bloqueo de solicitud muestra lo que sucede cuando los recursos no están disponibles.  

1.  Seleccione la pestaña **red** .  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para volver a abrir el menú de comandos.  
1.  Comience `blocking` a escribir y, a continuación, seleccione **Mostrar bloqueo de solicitud**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png" alt-text="La ficha solicitar bloqueo" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-empty.msft.png":::
       La ficha **solicitar bloqueo**  
    :::image-end:::  
    
1.  Seleccione **Agregar patrón** \ ( ![ Agregar patrón ][ImageAddPatternIcon] \), escriba `/libs/*` y, a continuación, presione `Enter` para confirmar.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png" alt-text="Agregar un patrón para bloquear cualquier solicitud al directorio de bibliotecas" lightbox="../media/speed-glitch-tony-remix-updated-network-drawer-request-blocking-added.msft.png":::
       Agregar un patrón para bloquear cualquier solicitud al `libs` directorio  
    :::image-end:::  
    
1.  Actualiza la página.  Las solicitudes jQuery y Lodash son rojas, lo que significa que las solicitudes se han bloqueado.   Aún se carga la página y es interactiva, por lo que parece que no se necesitan estos recursos.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png" alt-text="El panel red muestra que las solicitudes han sido bloqueadas" lightbox="../media/speed-glitch-tony-remix-updated-network-reloaded-drawer-request-blocking-added.msft.png":::
       El panel **red** muestra que las solicitudes han sido bloqueadas  
    :::image-end:::  
    
1.  Seleccione **quitar todos los patrones** \ ( ![ quitar todos los patrones ][ImageRemoveIcon] \) para eliminar el `/libs/*` patrón de bloqueo.  
    
En general, la pestaña bloqueo de solicitudes es útil para simular cómo se comporta la página cuando un recurso determinado no está disponible.  

Ahora, quite las referencias a estos archivos del código y audite de nuevo la página:  

1.  De nuevo en la pestaña Editor, Abra `template.html` .  
1.  Elimina `<script src="/libs/lodash.js">` y `<script src="/libs/jquery.js"></script>`.  
1.  Espere a que el sitio se vuelva a compilar y a implementar.  
1.  Audite la página de nuevo desde el panel **auditorías** .  Tu puntuación general debería haber mejorado de nuevo.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png" alt-text="Un informe de auditoría después de quitar los recursos de bloqueo de representación" lightbox="../media/speed-glitch-tony-remix-updated-2-audits-performance.msft.png":::
       Un informe de **Auditoría** después de quitar los recursos de bloqueo de representación  
    :::image-end:::  
    
#### Optimizar la ruta de representación crítica en el mundo real   

La **ruta de representación crítica** se refiere al código que necesita para cargar una página.  En general, para acelerar la carga de páginas solo tienes que enviar código crítico durante la carga de la página y, a continuación, cargar de forma diferida todo lo demás.  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   Es improbable que encuentre secuencias de comandos que pueda quitar de forma inadecuada, pero es posible que encuentre muchas secuencias de comandos que no necesita solicitar durante la carga de la página y que, en su lugar, las solicite.  <!--See [Using async or defer][async].  -->  
*   Si está usando un marco, compruebe si tiene un modo de producción.  Este modo puede usar una característica, como el [agitador de árboles][WebpackTreeShaking] , para eliminar el código innecesario que está bloqueando el procesamiento crítico.  
    
<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### Hacer menos trabajo del subproceso principal   

Su último informe muestra algunos ahorros potenciales menores en la sección oportunidades, pero si ve en la sección diagnósticos, parece que la mayor parte de la actividad principal es la actividad de subprocesos.  

El subproceso principal es el lugar donde el explorador hace la mayor parte del trabajo necesario para mostrar una página, como analizar y ejecutar HTML, CSS y JavaScript.  

El objetivo es usar el panel rendimiento para analizar qué trabajo está haciendo el subproceso principal mientras se carga la página y buscar formas de aplazar o quitar el trabajo innecesario.  

1.  Seleccione la pestaña **rendimiento** .  
1.  Seleccione **configuración de captura** \ ( ![ configuración de captura ][ImageCaptureIcon] \).  
1.  Configure la **red** como **3G lento** y **CPU** a **6X lentitud**.  Por lo general, los dispositivos móviles tienen más restricciones de hardware que los equipos portátiles o de escritorio, por lo que esta configuración le permite experimentar la carga de la página como si estuviera usando un dispositivo menos eficaz.  
1.  Seleccione **Actualizar** \ ( ![ actualizar ][ImageRefreshIcon] \).  DevTools actualiza la página y, a continuación, genera una visualización de todo el trabajo realizado para cargarla.  Esta visualización se conoce como la **traza**.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png" alt-text="Seguimiento del panel rendimiento de la carga de páginas" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu.msft.png":::
       Seguimiento del panel **rendimiento** de la carga de páginas  
    :::image-end:::  
    
La traza muestra la actividad cronológicamente, de izquierda a derecha.  Los gráficos de CPS, CPU y NET de la parte superior le ofrecen una descripción general de los fotogramas por segundo, la actividad de la CPU y la actividad de la red.  El bloque de amarillo seleccionado que aparece en la ilustración después de lo siguiente, la CPU estaba completamente ocupada por la actividad de scripting.  Esta es una pista de que puede acelerar la carga de la página haciendo menos trabajo de JavaScript.  

:::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png" alt-text="La sección información general de la traza" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main-highlight.msft.png":::
   La sección información general de la traza  
:::image-end:::  

Investigue el seguimiento para encontrar formas de hacer que el trabajo de JavaScript sea menor:  

1.  Seleccione la sección **intervalos** para expandirlo.  Basándose en el hecho de que puede haber una gran cantidad de medidas de [intervalos][MDNUserTimingApi] de reAct, parece que la aplicación de Tony usa el modo de desarrollo de reAct.  El cambio al modo de producción de reAct puede dar lugar a un resultado de fácil rendimiento.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png" alt-text="La sección intervalos" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings.msft.png":::
       La sección **intervalos**  
    :::image-end:::  
    
1.  Vuelva a seleccionar los **intervalos** para contraer la sección.  
1.  Examinar la sección **principal** .  En esta sección se muestra un registro cronológico de la actividad principal de la conversación, de izquierda a derecha.  El eje y (de arriba a abajo) muestra por qué se produjeron eventos.  Por ejemplo, en el figyre después de lo siguiente, el `Evaluate Script` evento ha provocado la ejecución de la `(anonymous)` función, que ha provocado que `(anonymous)` se ejecutara, `__webpack__require__` y así sucesivamente.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png" alt-text="La sección principal" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-main.msft.png":::
       La sección **principal**  
    :::image-end:::  
    
1.  Desplácese hacia abajo hasta la parte inferior de la sección **principal** .  Cuando se usa un marco, la mayor parte de la actividad superior está causada por el marco de trabajo, que normalmente está fuera de su control.  La actividad causada por la aplicación suele estar en la parte inferior.  En esta aplicación, parece que una función llamada `App` está causando un gran número de solicitudes a una `mineBitcoin` función.  Suena como Tony podría estar usando los dispositivos de sus ventiladores para minar cryptocurrency...  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png" alt-text="Desplazarse por la actividad de mineBitcoin" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-minebitcoin.msft.png":::
       Desplazar el puntero sobre la `mineBitcoin` actividad  
    :::image-end:::  
    
    > [!NOTE]
    > A pesar de que las solicitudes que el marco de trabajo realiza generalmente están fuera de su control, a veces puede estructurar la aplicación de forma que el marco de trabajo se ejecute ineficazmente.  Reestructurar la aplicación para usar el marco de forma eficaz es una forma de hacer menos trabajo de los subprocesos principales.  Sin embargo, esto requiere un conocimiento profundo de cómo funciona el marco y qué tipo de cambios se realizan en el código propio para poder usar el marco de forma más eficaz.  
    
1.  Expanda la sección de **abajo** .  Esta pestaña desglosa qué actividades ocuparon la mayor parte del tiempo.  Si no ve nada en la sección de la parte inferior, haga clic en la etiqueta de la sección **principal** .  En la sección de la **parte inferior** se muestra solo la información de cualquier actividad o grupo de actividades que haya seleccionado actualmente.  Por ejemplo, si hizo clic en una de las `mineBitcoin` actividades, la sección de **abajo** se mostrará solo la información de esa actividad.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png" alt-text="La pestaña abajo" lightbox="../media/speed-glitch-tony-remix-performance-slow-network-slow-cpu-timings-summary-minebitcoin.msft.png":::
       La pestaña **abajo**  
    :::image-end:::  
    
La columna **Self Time** muestra la cantidad de tiempo que se dedicó directamente en cada actividad.  Por ejemplo, en la siguiente ilustración, se dedicó un 63% del tiempo de rosca principal en la `mineBitcoin` función.  

Tiempo para ver si usar el modo de producción y reducir la actividad de JavaScript puede acelerar la carga de la página.  Empezar con el modo de producción:  

1.  En la pestaña Editor, Abra `webpack.config.js` .  
1.  Cambiar `"mode":"development"` a `"mode":"production"` .  
1.  Espere a que se implemente la nueva compilación.  
1.  Vuelva a auditar la página.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png" alt-text="Un informe de auditoría después de configurar WebPack para usar el modo de producción" lightbox="../media/speed-glitch-tony-remix-updated-3-audits-performance.msft.png":::
       Un informe de auditoría después de configurar WebPack para usar el modo de producción  
    :::image-end:::  
    
Reduzca la actividad de JavaScript eliminando la solicitud a `mineBitcoin` :  

1.  En la pestaña Editor, Abra `src/App.jsx` .  
1.  Comente la solicitud para `this.mineBitcoin(1500)` en el `constructor` .  
1.  Espere a que se implemente la nueva compilación.  
1.  Vuelva a auditar la página.  
    
    :::image type="complex" source="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png" alt-text="Un informe de auditoría después de quitar el trabajo de JavaScript innecesario" lightbox="../media/speed-glitch-tony-remix-updated-4-audits-performance.msft.png":::
       Un informe de auditoría después de quitar el trabajo de JavaScript innecesario  
    :::image-end:::  
    
Parece que el último cambio causó un aumento de rendimiento masivo.  

> [!NOTE]
> En esta sección se ofreció una breve introducción al panel rendimiento.  Consulte [referencia de análisis de rendimiento][DevtoolsEvaluatePerformanceReference] para obtener más información sobre cómo analizar el rendimiento de la página.  

<!--todo: add section when available -->  

#### Trabajar con menos subprocesos principales en el mundo real   

En general, el panel **rendimiento** es la manera más común de comprender qué actividad hace el sitio mientras se carga, y buscar formas de quitar actividades innecesarias.  

Si prefiere un método que se sienta `console.log()` de la mejor manera, la [API de temporización de usuario][MDNUserTimingApi] le permite marcar arbitrariamente determinadas fases del ciclo de vida de la aplicación para realizar un seguimiento del tiempo que toma cada una de esas fases.  

## Resumen   

*   Siempre que lo establezca para optimizar el rendimiento de la carga de un sitio, empiece siempre con una auditoría.  La auditoría establece una línea de base y le ofrece sugerencias sobre cómo mejorar.  
*   Realice un cambio a la vez y audite la página después de cada cambio para ver cómo afecta el cambio en el rendimiento.  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--  
  


-->  

<!-- image links -->  

[ImageAddPatternIcon]: ../media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: ../media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: ../media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: ../media/more-panels-icon.msft.png  
[ImagePerformIcon]: ../media/perform-icon.msft.png  
[ImageRefreshIcon]: ../media/reload-icon.msft.png  
[ImageRemoveIcon]: ../media/remove-icon.msft.png  
<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: ../evaluate-performance/reference.md "Referencia del análisis de rendimiento | Microsoft docs"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Introducción a la clase de desarrollo web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimización de imagen esencial"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directivas-codificación de contenido | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de temporización de usuario | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Sacudida de árboles | paquete de WebPack"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
