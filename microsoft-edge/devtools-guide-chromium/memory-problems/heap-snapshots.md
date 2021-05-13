---
description: Obtenga información sobre cómo grabar instantáneas de montón con el Microsoft Edge de perfiles de montón de DevTools y buscar pérdidas de memoria.
title: Cómo grabar instantáneas de montón
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 5f097cc45facc7f366a99a9564cf6f3d443f2058
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565018"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="how-to-record-heap-snapshots"></a>Cómo grabar instantáneas de montón  

Obtenga información sobre cómo grabar instantáneas de montón con el Microsoft Edge de perfiles de montón de DevTools y buscar pérdidas de memoria.  

El Microsoft Edge de perfiles de montón de DevTools muestra la distribución de memoria por los objetos JavaScript y los nodos DOM relacionados de la página.  Úselo para tomar instantáneas de montón de JavaScript \(JS heap\), analizar gráficos de memoria, comparar instantáneas y encontrar pérdidas de memoria.  Vaya a [Árbol de retención de objetos][DevtoolsMemoryProblems101ObjectsRetainingTree].  

## <a name="take-a-snapshot"></a>Tomar una instantánea  

En el panel **Memoria,** elija **Tomar instantánea**y, a continuación, **elija Inicio**.  También puede seleccionar `Ctrl` + `E` \(Windows, Linux\) o `Cmd` + `E` \(macOS\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Elegir tipo de generación de perfiles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Elegir tipo de generación de perfiles  
:::image-end:::  

**Las instantáneas** se almacenan inicialmente en la memoria del proceso del representador.  Las instantáneas se transfieren a DevTools a petición, cuando se elige en el icono de instantánea para verlo.  

Después de cargar la instantánea en DevTools y analizarla, aparece el número debajo del título de la instantánea y muestra el tamaño total de los objetos [de JavaScript accesibles.][DevtoolsMemoryProblems101ObjectSizes]  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Tamaño total de los objetos accesibles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Tamaño total de los objetos accesibles  
:::image-end:::  

> [!NOTE]
> Solo los objetos accesibles se incluyen en las instantáneas.  Además, tomar una instantánea siempre comienza con una recolección de elementos no utilizados.  

## <a name="clear-snapshots"></a>Borrar instantáneas  

Elija **Borrar todos los perfiles** icono para quitar instantáneas \(tanto de DevTools como de cualquier memoria asociada con el proceso del representador\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Quitar instantáneas" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Quitar instantáneas  
:::image-end:::  

Cerrar la ventana DevTools no elimina los perfiles de la memoria asociada con el proceso del representador.  Al volver a abrir DevTools, todas las instantáneas tomadas anteriormente vuelven a aparecer en la lista de instantáneas.  

> [!NOTE]
> Pruebe este ejemplo de [objetos dispersos][GlitchDevtoolsMemoryExample03] y de perfiles con el Profiler de montón.  Se muestra un número de asignaciones de elementos \(object\).  

## <a name="view-snapshots"></a>Ver instantáneas  

Ver instantáneas desde diferentes perspectivas para distintas tareas.  

**La vista resumen** muestra objetos agrupados por el nombre del constructor.  Úselo para buscar objetos \(y el uso de memoria\) en función del tipo agrupado por el nombre del constructor.  Es especialmente útil para realizar un **seguimiento de las pérdidas de DOM.**

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Vista de comparación**.  Muestra la diferencia entre dos instantáneas.  Úselo para comparar dos instantáneas de memoria \(o más\) de antes y después de una operación.  Inspeccionar el delta en la memoria liberada y el recuento de referencias le permite confirmar la presencia y la causa de una pérdida de memoria.  

**Vista de contención**.  Permite explorar el contenido del montón.  **La vista de** contención proporciona una mejor vista de la estructura de objetos, lo que ayuda a analizar los objetos a los que se hace referencia en el espacio de nombres global \(window\) para averiguar qué está manteniendo los objetos alrededor.  Úselo para analizar los cierres y profundizar en los objetos en un nivel bajo.  

Para cambiar entre vistas, use el selector en la parte superior de la vista.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Selector de vistas de conmutador" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Selector de vistas de conmutador  
:::image-end:::  

> [!NOTE]
> No todas las propiedades se almacenan en el montón de JavaScript.  Las propiedades implementadas mediante getters que ejecutan código nativo no se capturan.  Además, no se capturan valores que no sean de cadena, como números.  

### <a name="summary-view"></a>Vista de resumen  

Inicialmente, se abre una instantánea en la vista Resumen, que muestra totales de objeto, que se pueden expandir para mostrar instancias:  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Vista de resumen" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   **Vista de resumen**  
:::image-end:::  

Las entradas de nivel superior son líneas "totales".  

| Entradas de nivel superior | Descripción |  
|:--- |:--- |  
| **Constructor** | Representa todos los objetos creados con este constructor.  |  
| **Distancia** | muestra la distancia a la raíz mediante la ruta de acceso sencilla más corta de los nodos.  |  
| **Tamaño superficial** | Muestra la suma de tamaños superficiales de todos los objetos creados por una función de constructor determinada.  El tamaño superficial es el tamaño de la memoria que contiene un objeto \(por lo general, las matrices y las cadenas tienen tamaños superficiales más grandes\).  Vaya a [Tamaños de objeto][DevtoolsMemoryProblems101ObjectSizes].  |  
| **Tamaño retenido** | Muestra el tamaño máximo retenido entre el mismo conjunto de objetos.  El tamaño de memoria que puede liberar después de eliminar un objeto \(y los dependientes ya no son accesibles\) se denomina tamaño retenido.  Vaya a [Tamaños de objeto][DevtoolsMemoryProblems101ObjectSizes].  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

Después de expandir una línea total en la vista superior, se muestran todas las instancias.  Para cada instancia, los tamaños superficiales y retenido se muestran en las columnas correspondientes.  El número después del carácter es el identificador único del objeto, lo que permite comparar instantáneas de montón `@` por objeto.  

Recuerde que los objetos amarillos tienen referencias de JavaScript y los objetos rojos son nodos separados a los que se hace referencia desde uno con un fondo amarillo.  

**¿A qué corresponden las distintas entradas del constructor \(group\) en el perfilador de montón?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Grupos de constructores" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   **Grupos de constructores**  
:::image-end:::  

| Entrada constructor \(group\) | Descripción |  
|:--- |:--- |  
| **\(global property\)** | Los objetos intermedios entre un objeto global \(like \) y un objeto al que `window` hace referencia.  Si un objeto se crea con un constructor y lo mantiene un objeto global, la ruta de retención `Person` puede representarse como `[global] > \(global property\) > Person` .  Esto contrasta con la norma, donde los objetos se hacen referencia directamente entre sí.  Existen objetos intermedios por motivos de rendimiento.  Los globales se modifican regularmente y las optimizaciones de acceso a propiedades hacen un buen trabajo para los objetos no globales no son aplicables a los globales.  |  
| **\(roots\)** | Las entradas raíz de la vista de árbol de retención son las entidades que tienen referencias al objeto seleccionado.  Las entradas también pueden ser referencias creadas por el motor para fines específicos del motor.  El motor tiene cachés que hacen referencia a objetos, pero todas estas referencias son débiles y no impiden que se repile un objeto dado que no hay referencias realmente seguras.  |  
| **\(closure\)** | Recuento de referencias a un grupo de objetos mediante cierres de función.  |  
| **\(array, string, number, regexp\)** | Una lista de tipos de objeto con propiedades que hacen referencia a una matriz, cadena, número o expresión regular.  |  
| **\(código compilado\)** | Todo lo relacionado con el código compilado.  El script es similar a una función, pero corresponde a un `<script>` cuerpo.  SharedFunctionInfos \(SFI\) son objetos que se encuentran entre funciones y código compilado.  Las funciones suelen tener un contexto, mientras que las SFI no.  |  
| **HTMLDivElement**, **HTMLAnchorElement,** **DocumentFragment,** y así sucesivamente.  | Referencias a elementos u objetos de documento de un tipo concreto al que hace referencia el código.  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a>Vista de comparación  

Busque objetos filtrados comparando varias instantáneas entre sí.  Para comprobar que una determinada operación de aplicación no crea pérdidas \(por ejemplo, normalmente un par de operaciones directas e inversas, como abrir un documento y, a continuación, cerrarlo, no debe dejar elementos no utilizados\), puede seguir el escenario siguiente:  

1.  Realice una instantánea de montón antes de realizar una operación.  
1.  Realice una operación \(interactuar con una página de alguna manera que crea que está causando una pérdida\).  
1.  Realizar una operación inversa \(hacer la interacción opuesta y repetirla unas cuantas veces\).  
1.  Tome una segunda instantánea de montón y cambie la vista de esta a **Comparación**, comparándolo con **la instantánea 1**.  
    
En la **vista** Comparación, se muestra la diferencia entre dos instantáneas.  Al expandir una entrada total, se muestran las instancias de objeto agregadas y eliminadas.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Vista de comparación" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   **Vista de** comparación  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a>Vista Contención  

La **vista Contención** es esencialmente una "vista visual de aves" de la estructura de objetos de la aplicación.  Le permite echar un vistazo dentro de los cierres de funciones, observar objetos internos de máquina virtual \(VM\) que juntos son los objetos de JavaScript y comprender la cantidad de memoria que la aplicación usa en un nivel muy bajo.  

| Puntos de entrada de vista de contención | Descripción |  
|:--- |:--- |  
| **Objetos DOMWindow** | Objetos globales para código JavaScript.  |  
| **Raíces de GC** | Las raíces de GC reales usadas por la recolección de elementos no utilizados de la máquina virtual.  Las raíces de GC se componen de mapas de objetos integrados, tablas de símbolos, pilas de subprocesos de VM, cachés de compilación, ámbitos de identificador y controladores globales.  |  
| **Objetos nativos** | Los objetos del explorador se "insertan" dentro de la máquina virtual de JavaScript \(JavaScript VM\) para permitir la automatización, por ejemplo, nodos DOM, reglas CSS.  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Vista Contención" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   **Vista Contención**  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Sugerencia sobre los cierres.  Asigne un nombre a las funciones para que pueda distinguir fácilmente entre los cierres de la instantánea.  Por ejemplo, en este ejemplo no se usan funciones con nombre.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> El fragmento de código siguiente usa funciones con nombre.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > Pruebe este ejemplo de por qué [ `eval` es malo][GlitchDevtoolsMemoryExample07] analizar el impacto de los cierres en la memoria.  También puede interesarle seguirlo con este ejemplo que le lleva a través de la grabación de asignaciones [de montón][GlitchDevtoolsMemoryExample08].  
> 

## <a name="look-up-color-coding"></a>Buscar codificación de color  

Las propiedades y los valores de propiedad de los objetos tienen diferentes tipos y se colore en consecuencia.  Cada propiedad tiene uno de cuatro tipos.  

| Tipo de propiedad | Descripción |  
|:--- |:--- |  
| **a: (propiedad)** | Una propiedad regular con un nombre, a la que se tiene acceso a través del operador \(dot\) o mediante la notación `.` `[` `]` \(brackets\), por ejemplo `["foo bar"]` .  |  
| **0: elemento** | Una propiedad regular con un índice numérico al que se accede a través `[` `]` de la notación \(brackets\).  |  
| **a: var de contexto** |  Variable en un contexto de función, accesible por el nombre de la variable desde dentro de un cierre de función.  |  
| **a: prop del sistema** | Una propiedad agregada por la máquina virtual de JavaScript, a la que no se puede acceder desde el código JavaScript.  |  

Objetos designados `System` como no tienen un tipo de JavaScript correspondiente.  Cada uno forma parte de la implementación del sistema de objetos de la vm de Javascript.  V8 asigna la mayoría de los objetos internos en el mismo montón que los objetos JS del usuario.  Por lo tanto, estos son solo internos de V8.  

## <a name="find-a-specific-object"></a>Buscar un objeto específico  

Para buscar un objeto en el montón recopilado, puede buscar con `Ctrl` + `F` y proporcionar el identificador del objeto.  

## <a name="uncover-dom-leaks"></a>Descubrir fugas de DOM  

El profiler de montón tiene la capacidad de reflejar dependencias bidireccionales entre objetos nativos del explorador \(nodos DOM, reglas CSS\) y objetos JavaScript.
Esto ayuda a descubrir las pérdidas invisibles que se están produciendo debido a los subárboles DOM desasociados olvidados que flotan alrededor.  

Las pérdidas de DOM pueden ser más grandes de lo que crees.  Tenga en cuenta el ejemplo siguiente.  ¿Cuándo es #tree GC?  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

El mantiene una referencia al elemento primario `#leaf` relevante \(parentNode\) y recursivamente hasta , por lo que solo cuando leafRef se anula es el árbol WHOLE debajo de un candidato para `#tree` `#tree` GC.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Subárboles DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   Subárboles DOM  
:::image-end:::  

> [!NOTE]
> Ejemplos: pruebe este ejemplo de un nodo [DOM][GlitchDevtoolsMemoryExample06] de pérdida para comprender dónde se puede producir una pérdida y cómo detectarlo.  También puede ver este ejemplo de [pérdidas dom siendo más grandes][GlitchDevtoolsMemoryExample09]de lo esperado.  

Para obtener más información sobre las pérdidas de DOM y los fundamentos del análisis de memoria, consulte Búsqueda y depuración de pérdidas de memoria con el Microsoft Edge [DevTools][GonzaloRuizdeVillaMemory] de Gonzalo Ruiz de Villa.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Tamaños de objeto: terminología de memoria | Microsoft Docs"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Árbol de retención de objetos: terminología de memoria | Microsoft Docs"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html - Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "memoria | Diapositivas"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) y es creado por [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
