---
title: Acelerar el tiempo de ejecución de JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 801de4beeec29010ef63b2bcda950b57d4e544f7
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986188"
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

# Acelerar el tiempo de ejecución de JavaScript  

Identifica funciones caras usando el panel **memoria** .  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Perfiles de ejemplo" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Perfiles de ejemplo  
:::image-end:::  

### Resumen  

*   Registre exactamente las funciones a las que se llamó y la cantidad de memoria que requiere cada una con el muestreo de asignación en el panel **memoria** .  
*   Visualice sus perfiles como un gráfico de llamas.  
    
## Grabar un perfil de muestreo  

Si observas Jank en tu JavaScript, recopila un perfil de muestreo.  Los perfiles de muestreo muestran dónde se gasta el tiempo de ejecución en las funciones de la página.  

1.  Vaya al panel **memoria** de DevTools.  
1.  Seleccione el botón de opción **muestreo de asignación** .  
1.  Selecciona **Inicio**.  
1.  En función de lo que intente analizar, puede volver a cargar la página, interactuar con la página o simplemente permitir la ejecución de la página.  
1.  Haga clic en el botón **detener** cuando haya terminado.  
    
> [!NOTE]
> También puede usar la [API utilidades de consola][DevtoolsConsoleUtilities] para grabar y agrupar perfiles desde la línea de comandos.  

## Ver perfil de muestreo  

Cuando termine de grabar, DevTools rellenará automáticamente el panel **memoria** en **perfiles de muestreo** con los datos de su grabación.  

La vista predeterminada es **gruesa \ (inferior arriba \)**.  Esta vista le permite ver qué funciones tuvieron el mayor impacto en el rendimiento y examinar las rutas de llamadas a esas funciones.  

### Cambiar el criterio de ordenación  

Para cambiar el orden de clasificación, seleccione el menú desplegable junto al icono **función seleccionada** \ ( ![ enfoque seleccionado de la función ][ImageFocusIcon] \) y, a continuación, elija una de las siguientes opciones.

**Gráfico**.  Muestra un gráfico cronológico de grabación.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Gráfico de llamas  
:::image-end:::  

**\ (Inferior arriba \)**.  Enumera las funciones por su impacto en el rendimiento y permite examinar las rutas de la llamada a las funciones.  Esta es la vista predeterminada.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Gráfico grueso" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   Gráfico grueso  
:::image-end:::  

**Tree \ (arriba \)**.  Se muestra una imagen general de la estructura de llamadas, empezando en la parte superior de la pila de llamadas.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Gráfico de árbol" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   Gráfico de árbol  
:::image-end:::  

### Excluir funciones  

Para excluir una función de su perfil de muestreo, selecciónela y, a continuación, seleccione el botón **excluir la función** seleccionada \ ( ![ excluir función seleccionada ][ImageExcludeIcon] \).  La función de solicitud \ (primario \) de la función excluida \ (secundario \) se cobra con la memoria asignada a la función excluida \ (hijo \).  

Seleccione el botón **restaurar todas las funciones** \ ( ![ restaurar todas las funciones ][ImageRestoreIcon] \) para volver a restaurar todas las funciones excluidas en la grabación.  

## Ver perfil de muestreo como gráfico  

La vista de gráfico proporciona una representación visual del perfil de muestreo a lo largo del tiempo.  

Después de [grabar un perfil de muestreo](#record-a-sampling-profile), visualice la grabación como un gráfico de llama [cambiando el criterio de ordenación](#change-sort-order) a **gráfico**.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Vista de gráfico de llamas" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   Vista de gráfico de llamas  
:::image-end:::  

El gráfico de llamas se divide en dos partes.  

| clasificación | Elemento | Descripción |  
| --- |:--- |:--- |  
| uno | Introducción | Una vista de las aves de toda la grabación.  El alto de las barras corresponde a la profundidad de la pila de llamadas.  Por lo tanto, cuanto más alto es la barra, más profunda es la pila de llamadas.  |  
| 1 | Pilas de llamadas | Esta es una vista en profundidad de las funciones a las que se llamó durante la grabación.  El eje horizontal es tiempo y eje vertical es la pila de llamadas.  Las pilas están organizadas de arriba a abajo.  Por lo tanto, la función de la parte superior llamará a la que se encuentra debajo, y así sucesivamente.  |  

Las funciones están coloreadas de forma aleatoria.  No hay ninguna correlación de los colores que se usan en los otros paneles.  Sin embargo, las funciones siempre tienen el mismo color en todas las invocaciones, de modo que pueda ver los patrones en cada tiempo de ejecución.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Gráfico de llamas con anotaciones" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   Gráfico de llamas con anotaciones  
:::image-end:::  

Una pila de llamadas altas no es necesariamente importante, simplemente significa que se llamó a una gran cantidad de funciones.  Pero una barra amplia significa que una función tarda mucho tiempo en completarse.  Son candidatos para la optimización.  

### Acercar partes específicas de la grabación  

Seleccione, mantenga y arrastre el ratón a la izquierda y a la derecha en la información general para acercar determinadas partes de la pila de llamadas.  Después de aplicar el zoom, la pila de llamadas muestra automáticamente la parte de la grabación que seleccionó.  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Gráfico ampliado" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   Gráfico ampliado  
:::image-end:::  

### Ver detalles de la función  

Seleccione en una función para ver la definición en el panel **fuentes** .  

Pase el puntero sobre una función para mostrar el nombre y los datos de tiempo.  Se proporciona la siguiente información.  

| Todo | Descripción |  
|:--- |:--- |  
| **Name** | El nombre de la función.  |  
| **Tamaño propio** | Tamaño de la invocación actual de la función, incluidas solo las instrucciones de la función.  |  
| **Tamaño total** | Tamaño de la invocación actual de esta función y de las funciones a las que llamó.  |  
| **Dirección URL** | La ubicación de la definición de función en el formato de `base.js:261` donde `base.js` es el nombre del archivo en el que se define la función y `261` es el número de línea de la definición.  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Ver detalles de las funciones en el gráfico" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   Ver detalles de las funciones en el gráfico  
:::image-end:::  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "Perfil: referencia de API de utilidades de consola | Microsoft docs"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd: referencia de API de utilidades de consola | Microsoft docs"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
