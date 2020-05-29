---
title: Optimizar la velocidad del sitio web con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7efc76fbcb3d1ed6cbd0760f789c8c952030d70c
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611892"
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

> ##### Figura 1  
> Tony el gato  
> ![Tony el gato][ImageTony]  

## Paso 1: auditar el sitio   

Siempre que lo establezca para mejorar el rendimiento de la carga de un sitio, **empiece siempre con una auditoría**.  
La auditoría tiene dos funciones importantes:  

*   Crea una **línea base** para medir los cambios posteriores.  
*   Le ofrece **consejos útiles** sobre qué cambios son más impactantes.  

### Configuración   

En primer lugar, debe configurar el sitio para poder realizar cambios en él más adelante.  

1.  [Abra el código fuente del sitio](https://glitch.com/edit/#!/tony).  Esta pestaña se conoce como la **pestaña Editor**.  
    
    > ##### Figura 2  
    > Ficha Editor  
    > ![Ficha Editor][ImageEditor]  

1.  Seleccione **Tony**.  Aparece un menú.  
    
    > ##### Imagen 3  
    > El menú que aparece después de hacer clic en **Tony**  
    > ![El menú que aparece después de hacer clic en Tony][ImageMenu]  
    
1.  Seleccione **proyecto Remix**.  El nombre del proyecto cambia de **Tony** a algún nombre generado aleatoriamente.  Ahora tiene su propia copia modificable del código.  Más adelante, puedes realizar cambios en este código.  
1.  Seleccione **Mostrar** y seleccione **en una nueva ventana**.  La demostración se abre en una nueva pestaña.  Esta pestaña se conoce como la **pestaña demo**.  Es posible que el sitio tarde un rato en cargarse.  
    
    > ##### Imagen 4  
    > La ficha demo  
    > ![La ficha demo][ImageDemo]  

1.  Pulse `Control` + `Shift` + `J` \ (Windows \) o `Command` + `Option` + `J` \ (MacOS \).  Microsoft Edge DevTools se abre junto con la demostración.  
    
    > ##### Imagen 5  
    > DevTools y la demostración  
    > ![DevTools y la demostración][ImageDevtools]  

Para el resto de las capturas de pantalla de este tutorial, DevTools se muestra en una ventana independiente.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú comando, escriba `Undock` y, a continuación, seleccione **desacoplar en ventana independiente**.  

> ##### Imagen 6  
> DevTools desacoplado  
> ![DevTools desacoplado][ImageUndocked]  

### Establecer una línea base   

La línea base es un registro de cómo se realizó el sitio antes de realizar alguna mejora en el rendimiento.  

1.  Seleccione la pestaña **auditorías** .  Es posible que esté oculto detrás **del** ![ botón más paneles ][ImageMorePanelsIcon] .  Hay un Lighthouse en este panel porque el proyecto que alimenta el panel auditoría se denomina **Lighthouse**.  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    > ##### Imagen 7  
    > Panel auditorías  
    > ![Panel auditorías][ImageAudits]  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  Ajuste la configuración de la auditoría a las opciones de la [Ilustración 7](#figure-7).  A continuación se explican las diferentes opciones:  

    *   **Dispositivo**.  Configuración para **dispositivos móviles** cambia la cadena de agente de usuario y simula un área de visualización móvil.  La configuración en el **escritorio** simplemente deshabilita los cambios en el **teléfono móvil** .  
    *   **Auditorías**.  Si deshabilita una categoría, evitará que el panel auditoría las ejecute y las excluirá de su informe.  Deje las otras categorías habilitadas si desea ver los tipos de recomendaciones proporcionadas.  Al deshabilitar las categorías, se acelera ligeramente el proceso de auditoría.  
    *   **Limitación**.  Configurada para **simular lentitud de 4G, con una ralentización** de la CPU de 4x simula las condiciones típicas de la navegación en un dispositivo móvil.  Se denomina "simulado" porque en realidad el panel auditorías no se limita durante el proceso de auditoría.  En su lugar, simplemente extrapola cuánto tiempo tardará la página en cargarse en condiciones móviles.  Por otro lado, la opción de configuración **aplicado** , limita la CPU y la red, con la compensación de un proceso de auditoría más largo.  
    *   **Borrar almacenamiento**.  Al habilitar esta casilla, se borra todo el almacenamiento asociado a la página antes de cada auditoría.  Deje esta configuración activada si desea auditar la experiencia de los visitantes por primera vez en su sitio.  Deshabilite esta configuración cuando quiera la experiencia de repetición de la visita.  

1.  Seleccione **Ejecutar Auditorías**.  Después de 10 a 30 segundos, el panel auditoría muestra un informe del rendimiento del sitio.  
    
    > ##### Imagen 8  
    > Informe para el panel auditoría del rendimiento del sitio  
    > ![Informe para el panel auditoría del rendimiento del sitio][ImageReport]  

#### Control de errores de informe   

Si alguna vez recibe un error en el informe del panel auditorías, pruebe a ejecutar la pestaña demostración desde una ventana **InPrivate** sin ninguna otra pestaña abierta.  Esto asegura que está ejecutando Microsoft Edge desde un estado limpio.  Las extensiones de Microsoft Edge en particular suelen interferir con el proceso de auditoría.  

<!--todo: add screen capture for error in audit -->  
<!--
> ##### old Figure 9  
> A report that errored  
> ![A report that errored][ImageError]  
-->  

### Comprender el informe   

El número que aparece en la parte superior del informe es la puntuación de rendimiento general para el sitio.  Después, a medida que haga cambios en el código, debería ver que este número ha aumentado.  Una puntuación mayor supone un mejor rendimiento.  

> ##### Imagen 9  
> La puntuación general de rendimiento  
> ! [La puntuación general de rendimiento] [ImageOverall]  

La sección de **métricas** proporciona medidas cuantitativas en el rendimiento del sitio.  Cada métrica proporciona información sobre un aspecto diferente del rendimiento.  Por ejemplo, la **primera pintura con contenido** le indica cuando el contenido se pinta por primera vez en la pantalla, lo que es un hito importante en la percepción del usuario de la carga de la página, mientras que el tiempo de marca **interactiva** es el punto en el que la página aparece lo suficientemente lista para controlar las interacciones del usuario.  

> ##### Imagen 10  
> La sección métrica  
> ! [Sección de métricas] [ImageMetrics]  

Seleccione el botón de alternancia resaltado en la [figura 11](#figure-11) para ver una descripción de cada métrica y haga clic en **obtener más información** para leer la documentación.  

> ##### Imagen 11  
> Seleccione el botón de alternancia resaltado para expandir los elementos de **métrica**  
> ! [Seleccione el botón de alternancia resaltado para expandir los elementos de métricas] [ImageFirstMeaningfulPaint]  

A continuación, se muestra una colección de capturas de pantallas en la que se muestra cómo se ha cargado la página.  

> ##### Imagen 12  
> Capturas de pantallas del aspecto de la página durante la carga  
> ! [Capturas de pantallas de cómo se vio la página durante la carga] [ImageScreenshots]  

La sección **oportunidades** proporciona sugerencias específicas sobre cómo mejorar el rendimiento de la carga de esta página específica.  

> ##### Imagen 13  
> La sección oportunidades  
> ! [Sección de oportunidades] [ImageOpportunities]  

Seleccione una oportunidad para obtener más información sobre ella.  

> ##### Imagen 14  
> **Eliminar la oportunidad de recursos de bloqueo de procesamiento**  
> ! [Eliminar oportunidad de recursos de bloqueo de procesamiento] [ImageCompression]  

Seleccione **más información** para ver la documentación sobre por qué es importante una oportunidad y recomendaciones específicas sobre cómo corregirla.  

> ##### Imagen 15  
> Documentación de la oportunidad **eliminar recursos de bloqueo de procesamiento**  
> ! [Documentación para la oportunidad eliminar recursos de bloqueo de representación] [ImageReference]  

La sección **diagnósticos** proporciona más información sobre los factores que contribuyen al tiempo de carga de la página.  

> ##### Imagen 16  
> La sección diagnósticos  
> ! [Sección de diagnósticos] [ImageDiagnostics]  

En la sección de **auditorías superada** se muestra lo que el sitio está haciendo correctamente.  Seleccione para expandir la sección.  

> ##### Imagen 17  
> La sección de auditorías superada  
> ! [Sección de auditorías superada] [ImagePassed]  

## Paso 2: experimento   

La sección oportunidades de su informe de auditoría le ofrece sugerencias sobre cómo mejorar el rendimiento de la página.  En esta sección, implementará los cambios recomendados en el código base, auditando el sitio después de cada cambio para medir cómo afecta a la velocidad del sitio.  

### Habilitar compresión de texto   

El informe dice que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.  Habilitar la compresión de texto es una oportunidad para mejorar el rendimiento de la página.  

La compresión de texto es cuando se reduce, o comprime, el tamaño de un archivo de texto antes de enviarlo a través de la red.  Tipo de cómo puede comprimir una carpeta antes de enviarle un mensaje de correo electrónico para reducir el tamaño.  

Antes de habilitar la compresión, hay un par de maneras de comprobar manualmente si los recursos de texto están comprimidos.  

1.  Seleccione la pestaña **red** .  
    
    > ##### Ilustración 18  
    > Panel red  
    > ! [Panel de red] [ImageNetwork]  
    
1.  Seleccione el icono de **configuración de red** .  
1.  Seleccione la casilla **usar filas de solicitudes grandes** .  Aumenta el alto de las filas de la tabla de solicitudes de red.  
    
    > ##### Ilustración 19  
    > Filas grandes en la tabla solicitudes de red  
    > ! [Filas grandes en la tabla solicitudes de red] [ImageLargeRows]  
    
1.  Si no ve la columna **tamaño** en la tabla de solicitudes de red, haga clic en el encabezado de tabla y, a continuación, seleccione **tamaño**.  

Cada celda de **tamaño** muestra dos valores.  El valor superior es el tamaño del recurso descargado.  
El valor inferior es el tamaño del recurso sin comprimir.  Si los dos valores son iguales, el recurso no se comprimirá cuando se envíe a través de la red.  Por ejemplo, en la [figura 19](#figure-19) los valores superiores e inferiores de is `bundle.js` `1.2 MB` y `1.2 MB` .  

Para comprobar la compresión, inspeccione los encabezados HTTP de un recurso:  

1.  Seleccione **bundle. js**.  
1.  Seleccione la pestaña **encabezados** .  
    
    > ##### Ilustración 20  
    > La pestaña encabezados  
    > ! [Ficha encabezados] [ImageHeaders]  
    
1.  Busque un encabezado en la sección de **encabezados de respuesta** `content-encoding` .  No debe ver ninguno, lo que significa que `bundle.js` no se ha comprimido.  Cuando se comprime un recurso, este encabezado suele establecerse en `gzip` , `deflate` o `br` .  Vea las [directivas][MDNContentEncodingDirectives] para obtener una explicación de estos valores.  

Es suficiente con las explicaciones.  Para hacer algunos cambios.  Habilite la compresión de texto agregando un par de líneas de código:  

1.  En la pestaña Editor, haga clic en **Server. js**.  
    
    > ##### Ilustración 21  
    > Edición de Server. js  
    > ! [Editing Server. js] [ImageServer]  
    
1.  Agregue el código siguiente a **Server. js**.  Asegúrate de poner `app.use(compression())` antes `app.use(express.static('build'))` .  

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
    > ##### Old Figure 22  
    > The animation that indicates that the site is getting built  
    > ![The animation that indicates that the site is getting built][ImageBuilding]  
    -->  
    
Use los flujos de trabajo que aprendió anteriormente para comprobar manualmente que la compresión funciona:  

1.  Vuelva a la pestaña demo y vuelva a cargar la página.  La columna **tamaño** debería mostrar ahora dos valores diferentes para recursos de texto como `bundle.js` .  En la [Figura 23](#figure-23) , el valor superior de `256 KB` para `bundle.js` es el tamaño del archivo que se envió a través de la red y el valor inferior de `1.2 MB` es el tamaño de archivo descomprimido.  
    
    > ##### Ilustración 22  
    > La columna tamaño muestra ahora 2 valores diferentes para los recursos de texto  
    > ! [La columna tamaño ahora muestra 2 valores diferentes para los recursos de texto] [ImageRequests]  
    
1.  La sección de **encabezados de respuesta** de `bundle.js` ahora debe incluir un `content-encoding: gzip` encabezado.
    
    > ##### Ilustración 23  
    > La sección de encabezados de respuesta ahora contiene un encabezado de codificación de contenido  
    > ! [La sección de encabezados de respuesta ahora contiene un encabezado de codificación de contenido] [ImageGzip]  
    
Audite de nuevo la página para medir qué tipo de compresión de texto de impacto tiene en el rendimiento de carga de la página:  

1.  Seleccione la pestaña **auditorías** .  
1.  Seleccione **realizar una** auditoría para realizar una auditoría ![ ][ImagePerformIcon] .  
1.  Deje la configuración igual que antes.  
1.  Seleccione **Ejecutar auditoría**.  
    
    > ##### Ilustración 24  
    > Un informe de auditoría después de habilitar la compresión de texto  
    > ! [Informe de auditoría después de habilitar la compresión de texto] [ImageReport2]  
    
Woohoo!  El aspecto es el mismo.  La puntuación de rendimiento general debería haber aumentado, lo que significa que el sitio se está acelerando.  

#### Compresión de texto en el mundo real   

La mayoría de los servidores realmente tienen soluciones sencillas como esta para habilitar la compresión.  Solo tiene que hacer una búsqueda para configurar cualquier servidor que use para comprimir texto.  

### Cambiar el tamaño de las imágenes   

El informe indica que evitar cargas enormes de red es una de las principales oportunidades para mejorar el rendimiento de la página.  Cambiar el tamaño de las imágenes ayuda a reducir el tamaño de la carga de red.  Si el usuario está viendo las imágenes en una pantalla de dispositivo móvil de 500 píxeles de ancho, no hay ningún punto para enviar una imagen de ancho de 1500 píxeles.  Lo ideal es que envíes una imagen de ancho de 500 píxeles, como máximo.  

1.  En el informe, haga clic en **evitar cargas de red enormes** para ver las imágenes que se deben cambiar de tamaño.  Parece ser que 2 de los archivos jpg superan 2000 KB, lo cual es más grande de lo necesario.  
    
    <!--
    > ##### Old Figure 27  
    > Details about the **Properly size images** opportunity  
    > ![Details about the properly size images opportunity][ImageResize]  
    -->

1.  De nuevo en la pestaña Editor, Abra `src/model.js` .  
1.  Reemplazar `const dir = 'big'` por `const dir = 'small'` .  Este directorio contiene copias de las mismas imágenes que se han cambiado de tamaño.  
1.  Audite de nuevo la página para ver cómo este cambio afecta al rendimiento de la carga.  
    
    > ##### Ilustración 25  
    > Un informe de auditoría después de cambiar el tamaño de las imágenes  
    > ! [Informe de auditoría después de cambiar el tamaño de las imágenes] [ImageReport3]  

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
    
    > ##### Ilustración 26  
    > Más información sobre la oportunidad **eliminar recursos de bloqueo de procesamiento**  
    > ! [Más información sobre la oportunidad para eliminar recursos de bloqueo de representación] [ImageRender]  
    
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, comience a escribir `Coverage` y, a continuación, seleccione **Mostrar cobertura**.  
    
    > ##### Ilustración 27  
    > Abrir el menú de comandos desde el panel auditorías  
    > ! [Abrir el menú de comandos del panel auditorías] [ImageCommandMenu]  
    
    > ##### Ilustración 28  
    > La ficha cobertura  
    > ! [Ficha cobertura] [ImageCoverage]  
    
1.  Seleccione **Actualizar** ![ actualización ][ImageRefreshIcon] .  La pestaña **cobertura** proporciona una descripción general de la parte del código de `bundle.js` , `jquery.js` y `lodash.js` se ejecuta mientras se carga la página.  La [figura 30](#figure-30) indica 76 que no se usan los archivos de jQuery y Lodash, respectivamente.  
    
    > ##### Ilustración 29  
    > El informe de cobertura  
    > ! [Informe de cobertura] [ImageCoverageReport]  
    
1.  Seleccione la fila **jQuery. js** .  DevTools abre el archivo en el panel fuentes.  Se ejecutó una línea de código si tiene una barra azul al lado.  Una barra roja significa que no se ha ejecutado y, por supuesto, no es necesaria en la carga de la página.  
    
    > ##### Ilustración 30  
    > Visualización del archivo jQuery en el panel orígenes  
    > ! [Visualización del archivo jQuery en el panel orígenes] [ImageJQuery]  
    
1.  Desplácese un poco por el código jQuery.  Algunas de las líneas que reciben "ejecutar" son realmente solo Comentarios.  La ejecución de este código a través de un minifier que elimina los comentarios es otra forma de reducir el tamaño de este archivo.  

En Resumen, cuando está trabajando con su propio código, la pestaña cobertura le ayuda a analizar el código, línea por línea, y solo envía el código necesario para la carga de la página.  

¿Los `jquery.js` archivos y son `lodash.js` necesarios para cargar la página?  La pestaña bloqueo de solicitud muestra lo que sucede cuando los recursos no están disponibles.  

1.  Seleccione la pestaña **red** .  
1.  Pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para volver a abrir el menú de comandos.  
1.  Comience `blocking` a escribir y, a continuación, seleccione **Mostrar bloqueo de solicitud**.  
    
    > ##### Ilustración 31  
    > La ficha solicitar bloqueo  
    > ! [Ficha de bloqueo de solicitud] [ImageBlocking]  
    
1.  Seleccione **Agregar** patrón ![ Agregar patrón ][ImageAddPatternIcon] , escriba `/libs/*` y, a continuación, presione `Enter` para confirmar.  
    
    > ##### Ilustración 32  
    > Agregar un patrón para bloquear cualquier solicitud al `libs` directorio  
    > ! [Agregando un patrón para bloquear cualquier solicitud al directorio de bibliotecas] [ImageLibs]  
    
1.  Actualiza la página.  Las solicitudes jQuery y Lodash son rojas, lo que significa que las solicitudes se han bloqueado.   Aún se carga la página y es interactiva, por lo que parece que no se necesitan estos recursos.  
    
    > ##### Ilustración 33  
    > El panel red muestra que las solicitudes han sido bloqueadas  
    > ! [El panel red muestra que las solicitudes han sido bloqueadas] [ImageBlockedLibs]  
    
1.  Seleccionar **quitar todos los patrones** ![ quite todos los patrones ][ImageRemoveIcon] para eliminar el `/libs/*` patrón de bloqueo.  

En general, la pestaña bloqueo de solicitudes es útil para simular cómo se comporta la página cuando un recurso determinado no está disponible.  

Ahora, quite las referencias a estos archivos del código y audite de nuevo la página:  

1.  De nuevo en la pestaña Editor, Abra `template.html` .  
1.  Elimina `<script src="/libs/lodash.js">` y `<script src="/libs/jquery.js"></script>`.  
1.  Espere a que el sitio se vuelva a compilar y a implementar.  
1.  Audite la página de nuevo desde el panel **auditorías** .  Tu puntuación general debería haber mejorado de nuevo.  
    
    > ##### Ilustración 34  
    > Un informe de auditoría después de quitar los recursos de bloqueo de representación  
    > ! [Informe de auditoría después de quitar los recursos de bloqueo de representación] [ImageReport4]  

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
1.  Seleccione configuración de captura de **configuración** de ![ captura ][ImageCaptureIcon] .  
1.  Configure la **red** como **3G lento** y **CPU** a **6X lentitud**.  Por lo general, los dispositivos móviles tienen más restricciones de hardware que los equipos portátiles o de escritorio, por lo que esta configuración le permite experimentar la carga de la página como si estuviera usando un dispositivo menos eficaz.  
1.  Seleccione **Actualizar** ![ actualización ][ImageRefreshIcon] .  DevTools actualiza la página y, a continuación, genera una visualización de todo el trabajo realizado para cargarla.  Esta visualización se conoce como la **traza**.  
    
    > ##### Ilustración 35  
    > Seguimiento del panel rendimiento de la carga de páginas  
    > ! [El seguimiento del panel rendimiento de la carga de página] [ImagePerformance]  

La traza muestra la actividad cronológicamente, de izquierda a derecha.  Los gráficos de CPS, CPU y NET de la parte superior le ofrecen una descripción general de los fotogramas por segundo, la actividad de la CPU y la actividad de la red.  El bloque de amarillo seleccionado que se muestra en la [figura 37](#figure-37) significa que la CPU estaba completamente ocupada con la actividad de scripting.  Esta es una pista de que puede acelerar la carga de la página haciendo menos trabajo de JavaScript.  

> ##### Ilustración 36  
> La sección información general de la traza  
> ! [Sección información general de la traza] [ImageOverview]  

Investigue el seguimiento para encontrar formas de hacer que el trabajo de JavaScript sea menor:  

1.  Seleccione la sección **intervalos** para expandirlo.  Basándose en el hecho de que puede haber una gran cantidad de medidas de [intervalos][MDNUserTimingApi] de reAct, parece que la aplicación de Tony usa el modo de desarrollo de reAct.  El cambio al modo de producción de reAct puede dar lugar a un resultado de fácil rendimiento.  
    
    > ##### Ilustración 37  
    > La sección intervalos  
    > ! [Sección intervalos] [ImageUserTiming]  

1.  Vuelva a seleccionar los **intervalos** para contraer la sección.  
1.  Examinar la sección **principal** .  En esta sección se muestra un registro cronológico de la actividad principal de la conversación, de izquierda a derecha.  El eje y (de arriba a abajo) muestra por qué se produjeron eventos.  Por ejemplo, en la [figura 39](#figure-39), el `Evaluate Script` evento ha provocado la ejecución de la `(anonymous)` función, provocada por la ejecución `(anonymous)` , que ha provocado que se ejecutó `__webpack__require__` , etc.  
    
    > ##### Ilustración 38  
    > La sección principal  
    > ! [Sección principal] [ImageMain]  

1.  Desplácese hacia abajo hasta la parte inferior de la sección **principal** .  Cuando se usa un marco, la mayor parte de la actividad superior está causada por el marco de trabajo, que normalmente está fuera de su control.  La actividad causada por la aplicación suele estar en la parte inferior.  En esta aplicación, parece que una función llamada `App` está causando un gran número de solicitudes a una `mineBitcoin` función.  Suena como Tony podría estar usando los dispositivos de sus ventiladores para minar cryptocurrency...  
    
    > ##### Ilustración 39  
    > Mantener el mouse sobre la `mineBitcoin` actividad  
    > ! [Situar el puntero sobre la actividad de mineBitcoin] [ImageMine]  
    
    > [!NOTE]
    > A pesar de que las solicitudes que el marco de trabajo realiza generalmente están fuera de su control, a veces puede estructurar la aplicación de forma que el marco de trabajo se ejecute ineficazmente.  Reestructurar la aplicación para usar el marco de forma eficaz es una forma de hacer menos trabajo de los subprocesos principales.  Sin embargo, esto requiere un conocimiento profundo de cómo funciona el marco y qué tipo de cambios se realizan en el código propio para poder usar el marco de forma más eficaz.  

1.  Expanda la sección de **abajo** .  Esta pestaña desglosa qué actividades ocuparon la mayor parte del tiempo.  Si no ve nada en la sección de la parte inferior, haga clic en la etiqueta de la sección **principal** .  En la sección de la **parte inferior** se muestra solo la información de cualquier actividad o grupo de actividades que haya seleccionado actualmente.  Por ejemplo, si hizo clic en una de las `mineBitcoin` actividades, la sección de **abajo** se mostrará solo la información de esa actividad.  
    
    > ##### Ilustración 40  
    > La pestaña abajo  
    > ! [La pestaña de la parte inferior] [ImageBottomUp]  

La columna **Self Time** muestra la cantidad de tiempo que se dedicó directamente en cada actividad.  Por ejemplo, la [figura 41](#figure-41) muestra que aproximadamente el 63% del tiempo de rosca principal se dedicó a la `mineBitcoin` función.  

Tiempo para ver si usar el modo de producción y reducir la actividad de JavaScript puede acelerar la carga de la página.  Empezar con el modo de producción:  

1.  En la pestaña Editor, Abra `webpack.config.js` .  
1.  Cambiar `"mode":"development"` a `"mode":"production"` .  
1.  Espere a que se implemente la nueva compilación.  
1.  Vuelva a auditar la página.  
    
    > ##### Ilustración 41  
    > Un informe de auditoría después de configurar WebPack para usar el modo de producción  
    > ! [Informe de auditoría después de configurar WebPack para usar el modo de producción] [ImageReport5]  

Reduzca la actividad de JavaScript eliminando la solicitud a `mineBitcoin` :  

1.  En la pestaña Editor, Abra `src/App.jsx` .  
1.  Comente la solicitud para `this.mineBitcoin(1500)` en el `constructor` .  
1.  Espere a que se implemente la nueva compilación.  
1.  Vuelva a auditar la página.  
    
    > ##### Ilustración 42  
    > Un informe de auditoría después de quitar el trabajo de JavaScript innecesario  
    > ! [Informe de auditoría después de quitar el trabajo de JavaScript innecesario] [ImageReport6]  

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

<!--    -->  



<!-- image links -->  

[ImageAddPatternIcon]: /microsoft-edge/devtools-guide-chromium/media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-panels-icon.msft.png  
[ImagePerformIcon]: /microsoft-edge/devtools-guide-chromium/media/perform-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRemoveIcon]: /microsoft-edge/devtools-guide-chromium/media/remove-icon.msft.png  

[ImageTony]: /microsoft-edge/devtools-guide-chromium/media/speed-tony.msft.png "Ilustración 1: Tony the cat"  
[ImageEditor]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js.msft.png "Ilustración 2: la ficha Editor"  
[ImageMenu]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js-remix-project.msft.png "Ilustración 3: el menú que aparece después de hacer clic en Tony"  
[ImageDemo]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live.msft.png "Ilustración 4: la pestaña demo"  
[ImageDevtools]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live-console.msft.png "Ilustración 5: DevTools y la demostración"  
[ImageUndocked]: /microsoft-edge/devtools-guide-chromium/media/speed-console.msft.png "Ilustración 6: DevTools desacoplado"  
[ImageAudits]: /microsoft-edge/devtools-guide-chromium/media/speed-audits-performance.msft.png "Ilustración 7: panel auditorías"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png "Ilustración 8: el informe para el panel auditorías del rendimiento del sitio"  
<!--[ImageError]: /microsoft-edge/devtools-guide-chromium/media/speed-.msft.png "Old Figure 9: A report that errored"  -->  
[ImageOverall]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Metrics-collapsed-Metrics-Highlighted.msft.png "Ilustración 9: la puntuación de rendimiento general"  
[ImageMetrics]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Metrics-collapsed-Highlighted.msft.png "Figura 10: la sección métrica"  
[ImageFirstMeaningfulPaint]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Metrics-Expanded.msft.png "ilustración 11: seleccionar el botón de alternancia resaltado para expandir los elementos de métrica"  
[ImageScreenshots]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-View-Trace.msft.png "Ilustración 12: capturas de pantallas de la página durante la carga  
[ImageOpportunities]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Opportunities.msft.png "figura 13: sección oportunidades"  
[ImageCompression]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Opportunities-Expanded.msft.png "Ilustración 14: eliminar la oportunidad de recursos de bloqueo de procesamiento"  
[ImageReference]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-web-dev-performance-Audits.msft.png "Ilustración 15: documentación para la oportunidad eliminar recursos de bloqueo de representación"  
[ImageDiagnostics]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Diagnostics.msft.png "Figura 16: la sección de diagnóstico"  
[ImagePassed]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Audits-performance-Passed-Audits.msft.png "Ilustración 17: la sección de auditorías superada"  
[ImageNetwork]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network.msft.png "ilustración 18: el panel red"  
[ImageLargeRows]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network-use-Large-request-Rows.msft.png "Ilustración 19: filas grandes en la tabla solicitudes de red"  
[ImageHeaders]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network-use-Large-request-Rows-bundle-JS.msft.png "Ilustración 20: la pestaña encabezados"  
[ImageServer]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Server-JS.msft.png "figura 21: edición de Server. js"  
<!--[ImageBuilding]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-server-js-edited.msft.png "Old Figure 22: The animation that indicates that the site is getting built"  -->  
[ImageRequests]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network-Main.msft.png "Ilustración 22: la columna tamaño ahora muestra 2 valores diferentes para los recursos de texto"  
[ImageGzip]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Network-bundle-JS-headers-Response.msft.png "Ilustración 23: la sección de encabezados de respuesta ahora contiene un `content-encoding` encabezado"  
[ImageReport2]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance.msft.png "Ilustración 24: un informe de auditoría después de habilitar la compresión de texto"  
<!--[ImageResize]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png "Old Figure 27: Details about the properly size images opportunity"  -->
[ImageReport3]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Compression-Small-images-Audits-performance.msft.png "figura 25: un informe de auditoría después de cambiar el tamaño de las imágenes"  
[ImageRender]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance-oppportunities-Expanded.msft.png "ilustración 26: más información sobre la oportunidad eliminar recursos de bloqueo de representación"  
[ImageCommandMenu]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance-oppportunities-Expanded-Command-coverage.msft.png "Ilustración 27: abrir el menú de comandos desde el panel auditoría"  
[ImageCoverage]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance-oppportunities-Expanded-Drawer-coverage.msft.png "Ilustración 28: la pestaña cobertura"  
[ImageCoverageReport]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Audits-performance-oppportunities-Expanded-Drawer-Coverage-reloaded.msft.png "Ilustración 29: el informe de cobertura"  
[ImageJQuery]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-sources-Drawer-Coverage-reloaded-jQuery-js.msft.png "Ilustración 30: ver el archivo jQuery en el panel orígenes"  
[ImageBlocking]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Network-Drawer-request-blocking-Empty.msft.png "Ilustración 31: la pestaña bloqueo de solicitudes"  
[ImageLibs]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Network-Drawer-request-blocking-Added.msft.png "ilustración 32: agregar un patrón para bloquear cualquier solicitud al directorio de bibliotecas"  
[ImageBlockedLibs]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-Network-reloaded-Drawer-request-blocking-Added.msft.png "Ilustración 33: el panel red muestra que las solicitudes han sido bloqueadas"  
[ImageReport4]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-2-Audits-performance.msft.png "Ilustración 34: un informe de auditoría después de quitar los recursos de bloqueo de representación"  
[ImagePerformance]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU.msft.png "Ilustración 35: seguimiento del panel de rendimiento de la carga de la página"  
[ImageOverview]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-Main-Highlight.msft.png "Ilustración 36: la sección de información general de la traza"  
[ImageUserTiming]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings.msft.png "Ilustración 37: la sección intervalos"  
[ImageMain]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-Main.msft.png "Ilustración 38: la sección principal"  
[ImageMine]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings-minebitcoin.msft.png "Ilustración 39: mantener el puntero sobre la actividad de mineBitcoin"  
[ImageBottomUp]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings-Summary-minebitcoin.msft.png "Ilustración 40: la pestaña de abajo arriba"  
[ImageReport5]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-3-Audits-performance.msft.png "Ilustración 41: un informe de auditoría después de configurar WebPack para usar el modo de producción"  
[ImageReport6]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Speed-Glitch-Tony-Remix-Updated-4-Audits-performance.msft.png "Ilustración 42: un informe de auditoría después de quitar el trabajo de JavaScript innecesario"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Referencia de análisis de rendimiento"  

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
