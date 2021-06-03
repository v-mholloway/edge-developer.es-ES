---
description: Identifique funciones costosas mediante el Microsoft Edge de memoria de DevTools.
title: Acelerar el tiempo de ejecución de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: bbac00ab46e205fb692cc3de3e5f08ba854b0911
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565088"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->
# <a name="speed-up-javascript-runtime"></a>Acelerar el tiempo de ejecución de JavaScript  

Identificar funciones costosas mediante la **herramienta Memoria.**  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfiles de ejemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Perfiles de ejemplo  
:::image-end:::  

### <a name="summary"></a>Resumen  

*   Registre exactamente qué funciones se llamaron y cuánta memoria necesita cada una con el muestreo de asignación en la **herramienta Memoria.**  
*   Visualiza los perfiles como un gráfico de llamas.  
    
## <a name="record-a-sampling-profile"></a>Registrar un perfil de muestreo  

Si observa jank en JavaScript, recopile un perfil de muestreo.  Los perfiles de muestreo muestran dónde se dedica el tiempo de ejecución en las funciones de la página.  

1.  Vaya a la **herramienta Memoria** de DevTools.  
1.  Elija el **botón de radio Asignación de** muestreo.  
1.  Elija **Inicio**.  
1.  Según lo que intente analizar, puede actualizar la página, interactuar con la página o simplemente dejar que se ejecute la página.  
1.  Elija el **botón** Detener cuando haya terminado.  
    
> [!NOTE]
> También puede usar la [API de utilidades de consola][DevtoolsConsoleUtilities] para registrar y agrupar perfiles desde la línea de comandos.  

## <a name="view-sampling-profile"></a>Ver perfil de muestreo  

Cuando termine de grabar, DevTools rellena automáticamente el **panel** Memoria en **PERFILES** DE MUESTREO con los datos de la grabación.  

La vista predeterminada es **Heavy \(Bottom Up\)**.  Esta vista le permite revisar qué funciones tuvieron más impacto en el rendimiento y examinar la ruta de acceso de solicitud para cada función.  

### <a name="change-sort-order"></a>Cambiar criterio de ordenación  

Para cambiar el orden de ordenación, seleccione el menú desplegable junto al icono de la función seleccionada de foco **\(** Función seleccionada por foco \) y, a continuación, elija una de ![ las siguientes ](../media/focus-icon.msft.png) opciones.

**Gráfico**.  Muestra un gráfico cronológico de la grabación.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Gráfico de llamas  
:::image-end:::  

**Heavy \(Bottom Up\)**.  Enumera las funciones por impacto en el rendimiento y permite examinar las rutas de acceso de llamadas a las funciones.  Esta es la vista predeterminada.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Gráfico pesado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Gráfico pesado  
:::image-end:::  

**Tree \(Top Down\)**.  Muestra una imagen general de la estructura de llamadas, comenzando en la parte superior de la pila de llamadas.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Gráfico de árbol" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Gráfico de árbol  
:::image-end:::  

### <a name="exclude-functions"></a>Funciones de exclusión  

Para excluir una función del perfil de muestreo, selecciónla y, a continuación, elija el botón excluir la función seleccionada **\(** ![ excluir la función seleccionada ](../media/exclude-icon.msft.png) \).  La función de solicitud \(parent\) de la función excluida \(child\) se carga con la memoria asignada a la función excluida \(child\).  

Elija el **botón restaurar todas las funciones** \( restaurar todas las funciones \) para restaurar todas las funciones excluidas de nuevo en la ![ ](../media/restore-icon.msft.png) grabación.  

## <a name="view-sampling-profile-as-chart"></a>Ver perfil de muestreo como gráfico  

La vista Gráfico proporciona una representación visual del perfil de muestreo con el tiempo.  

Después de [grabar un perfil de muestreo,](#record-a-sampling-profile)vea la grabación como un gráfico de llama cambiando el criterio de [ordenación](#change-sort-order) a **Gráfico**.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Vista gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Vista gráfico de llamas  
:::image-end:::  

El gráfico de llama se divide en dos partes.  

| index | Parte | Descripción |  
| --- |:--- |:--- |  
| 1 | Introducción | Una vista visual de toda la grabación.  El alto de las barras corresponde a la profundidad de la pila de llamadas.  Por lo tanto, cuanto mayor sea la barra, más profunda será la pila de llamadas.  |  
| 2 | Pilas de llamadas | Se trata de una vista detallada de las funciones a las que se llamó durante la grabación.  El eje horizontal es el tiempo y el eje vertical es la pila de llamadas.  Las pilas están organizadas de arriba abajo.  Por lo tanto, la función en la parte superior llamada a la que está debajo de ella, y así sucesivamente.  |  

Las funciones se coloreadas aleatoriamente.  No hay ninguna correlación con los colores usados en los otros paneles.  Sin embargo, las funciones siempre tienen el mismo color entre invocaciones para que pueda observar patrones en cada tiempo de ejecución.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Gráfico de llama anotado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Gráfico de llama anotado  
:::image-end:::  

Una pila de llamadas alta no es necesariamente significativa, solo significa que se llamaron a muchas funciones.  Pero una barra ancha significa que una función tardó mucho tiempo en completarse.  Estos son los candidatos para la optimización.  

### <a name="zoom-in-on-specific-parts-of-recording"></a>Acercar partes específicas de la grabación  

Elija, mantenga presionado y arrastre el mouse hacia la izquierda y la derecha a través de la información general para acercarse a partes concretas de la pila de llamadas.  Después de hacer zoom, la pila de llamadas muestra automáticamente la parte de la grabación que seleccionó.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Gráfico zoomed" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Gráfico zoomed  
:::image-end:::  

### <a name="view-function-details"></a>Ver detalles de la función  

Elija una función para ver la definición en la **herramienta** Orígenes.  

Mantenga el mouse sobre una función para mostrar el nombre y los datos de temporización.  Se proporciona la siguiente información.  

| Detalle | Descripción |  
|:--- |:--- |  
| **Name** | Nombre de la función.  |  
| **Tamaño propio** | Tamaño de la invocación actual de la función, incluidas solo las instrucciones de la función.  |  
| **Tamaño total** | El tamaño de la invocación actual de esta función y las funciones a las que llamó.  |  
| **Dirección URL** | La ubicación de la definición de función en forma de dónde es el nombre del archivo donde se define la función y es el número de línea `base.js:261` `base.js` de la `261` definición.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Ver detalles de funciones en el gráfico" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Ver detalles de funciones en el gráfico  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referencia de API de utilidades de consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "perfil: referencia de api de utilidades de consola | Microsoft Docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd: referencia de api de utilidades de consola | Microsoft Docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) se encuentra aquí y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) y [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
