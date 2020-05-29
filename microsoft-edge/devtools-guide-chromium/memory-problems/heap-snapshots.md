---
title: Cómo grabar instantáneas de montones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e6f64b219bc2b28d01780c28cc605d56a07cb491
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611681"
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





# Cómo grabar instantáneas de montones   



Obtenga información sobre cómo grabar instantáneas de montones con el analizador de montones de Microsoft Edge DevTools y buscar pérdidas de memoria.  

El analizador de montones de DevTools de Microsoft Edge muestra la distribución de memoria mediante los objetos de JavaScript y los nodos DOM relacionados de la página.  Utilícelo para tomar instantáneas del montón \ (JS heap \) de montón de JavaScript, analizar gráficos de memoria, Comparar instantáneas y buscar pérdidas de memoria.  Vea también [objetos reteniendo árbol][DevtoolsMemoryProblems101ObjectsRetainingTree].  

## Tomar una instantánea  

En el panel **memoria** , elija **tomar instantánea**y, a continuación, haga clic en **iniciar**.  También puede pulsar `Ctrl` + `E` \ (Windows \) o `Cmd` + `E` \ (MacOS \).  

> ##### Figura 1  
> Seleccionar tipo de generación de perfiles  
> ![Seleccionar tipo de generación de perfiles][ImageProfilingType]  

Las **instantáneas** se almacenan inicialmente en la memoria del proceso del representador.  Las instantáneas se transfieren a la DevTools a petición, al hacer clic en el icono de instantánea para verlo.  

Una vez que la instantánea se ha cargado en DevTools y se ha analizado, aparece el número debajo del título de la instantánea, que muestra el [Tamaño total de los objetos de JavaScript accesibles][DevtoolsMemoryProblems101ObjectSizes].  

> ##### Figura 2  
> Tamaño total de objetos accesibles  
> ![Tamaño total de objetos accesibles][ImageTotalSize]  

> [!NOTE]
> Solo los objetos accesibles se incluyen en las instantáneas.  Además, tomar una instantánea siempre comienza con una recolección de elementos no utilizados.  

## Borrar instantáneas  

Haga clic en el icono **borrar todos los perfiles** para quitar las instantáneas \ (tanto de DevTools como de cualquier memoria asociada al proceso de representación \).  

> ##### Imagen 3  
> Quitar instantáneas  
> ![Quitar instantáneas][ImageRemoveSnapshots]  

Al cerrar la ventana DevTools, no se eliminan los perfiles de la memoria asociada con el proceso de representación.  Al volver a abrir DevTools, todas las instantáneas tomadas anteriormente volverán a aparecer en la lista de instantáneas.  

> [!NOTE]
> Pruebe este ejemplo de [objetos dispersos][GlitchDevtoolsMemoryExample03] y envíelo con el generador de perfiles de montones.  Debería ver varias asignaciones de elementos \ (objeto \).  

## Ver instantáneas  

Ver instantáneas de diferentes perspectivas para tareas diferentes.  

La **vista de Resumen** muestra los objetos agrupados por el nombre del constructor.  Se usa para buscar objetos \ (y el uso de memoria \) según el tipo agrupado por nombre de constructor.  Es especialmente útil para **rastrear las pérdidas de Dom**.

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Vista de comparación**.  Muestra la diferencia entre dos instantáneas.  Utilícelo para comparar dos (o más \) instantáneas de memoria de antes y después de una operación.  Inspeccionar el delta en la memoria liberada y el recuento de referencias le permite confirmar la presencia y la causa de una pérdida de memoria.  

**Vista de inclusión**.  Permite la exploración del contenido del montón.  La **vista contención** ofrece una mejor vista de la estructura del objeto, lo que ayuda a analizar los objetos a los que se hace referencia en el espacio de nombres global \ (ventana \) para descubrir de qué está manteniendo los objetos.  Úsela para analizar los cierres y profundizar en los objetos a un bajo nivel.  

Para cambiar entre las vistas, use el selector de la parte superior de la vista.  

> ##### Imagen 4  
> Cambiar el selector de vistas  
> ![Cambiar el selector de vistas][ImageSwitchViews]  

> [!NOTE]
> No todas las propiedades se almacenan en el montón de JavaScript.  Las propiedades implementadas mediante captadores que ejecutan código nativo no se capturan.  Además, no se capturan valores que no sean de cadena, como los números.  

### Vista de Resumen  

Inicialmente, se abre una instantánea en la vista de Resumen, que muestra los totales de los objetos, que se pueden expandir para mostrar las instancias:  

> ##### Imagen 5  
> Vista de Resumen  
> ![Vista de Resumen][ImageSummaryView]  

Las entradas de nivel superior son líneas de "total".  

| Entradas de nivel superior | Descripción |  
|:--- |:--- |  
| **Constructor** | Representa todos los objetos creados con este constructor.  |  
| **Distancia** | muestra la distancia a la raíz mediante la ruta de acceso más corta de los nodos.  |  
| **Tamaño superficial** | Muestra la suma de los tamaños superficiales de todos los objetos creados por una determinada función constructora.  El tamaño superficial es el tamaño de la memoria que mantiene un objeto \ (generalmente, las matrices y cadenas tienen tamaños superficiales mayores \).  Vea también [tamaños de objeto][DevtoolsMemoryProblems101ObjectSizes].  |  
| **Tamaño retenido** | Muestra el tamaño máximo retenido entre el mismo conjunto de objetos.  El tamaño de la memoria que puede liberar después de que se elimine un objeto \ (y los dependientes ya no se pueden alcanzar \) se denomina tamaño conservado.  Vea también [tamaños de objeto][DevtoolsMemoryProblems101ObjectSizes].  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

Después de expandir una línea total en la vista superior, se muestran todas las instancias.  Para cada instancia, los tamaños superficiales y retenidos se muestran en las columnas correspondientes.  El número después del `@` carácter es el identificador único del objeto, lo que le permite comparar instantáneas de montones en función de cada objeto.  

Recuerde que los objetos amarillos tienen referencias de JavaScript y los objetos rojos son nodos desvinculados a los que se hace referencia desde uno con un fondo amarillo.  

**¿Para qué se corresponden las diversas entradas de constructor \ (grupo \) en el generador de perfiles del montón?**  

> ##### Imagen 6  
> Grupos de constructores  
> ![Grupos de constructores][ImageConstructorGroups]  

| Entrada de constructor \ (grupo \) | Descripción |  
|:--- |:--- |  
| **\ (propiedad global \)** | Los objetos intermedios entre un objeto global \ (como `window` \) y un objeto al que hace referencia.  Si se crea un objeto con un constructor `Person` y es retenido por un objeto global, la ruta de retención tendrá el aspecto siguiente `[global] > \(global property\) > Person` .  Esto contrasta con la norma, donde los objetos se hacen referencia directamente entre sí.  Los objetos intermedios existen por razones de rendimiento.  Las globales se modifican periódicamente y las optimizaciones de acceso a la propiedad hacen un buen trabajo para los objetos no globales que no son aplicables a los usuarios globales.  |  
| **\ (raíces \)** | Las entradas raíz de la vista de árbol de retención son las entidades que tienen referencias al objeto seleccionado.  Las entradas también pueden ser referencias creadas por el motor para fines específicos del motor.  El motor tiene cachés que hacen referencia a objetos, pero todas estas referencias son débiles y no impiden que se recopile un objeto dado que no hay referencias realmente fuertes.  |  
| **\ (cierre \)** | Un recuento de referencias a un grupo de objetos a través de cierres de función.  |  
| **\ (matriz, cadena, número, RegExp \)** | Una lista de tipos de objeto con propiedades que hacen referencia a una matriz, una cadena, un número o una expresión regular.  |  
| **\ (código compilado \)** | Todo lo relacionado con el código compilado.  El script es similar a una función, pero se corresponde con un `<script>` cuerpo.  SharedFunctionInfos \ (SFI \) están en los objetos entre las funciones y el código compilado.  Las funciones suelen tener un contexto, mientras que SFIs no.  |  
| **HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, etc.  | Referencias a elementos o objetos de documento de un tipo específico al que hace referencia el código.  |  

<!--todo: add heap profiling summary section when available -->  

### Vista comparación  

Busque objetos perdidos comparando varias instantáneas entre sí.  Para comprobar que una determinada operación de la aplicación no crea fugas \ (por ejemplo, normalmente un par de operaciones directas e inversas, como abrir un documento y, a continuación, cerrarla, no debe salir de los residuos \), puede seguir el siguiente escenario:  

1.  Tomar una instantánea del montón antes de realizar una operación.  
1.  Realice una operación \ (interactúe con una página de alguna manera que considere que está causando una fuga \).  
1.  Realizar una operación inversa \ (hacer la interacción opuesta y repetir varias veces \).  
1.  Tomar una segunda instantánea del montón y cambiar la vista de esta para **compararla, comparándola**con la **instantánea 1**.  

En la vista **comparación** , se muestra la diferencia entre dos instantáneas.  Al expandir una entrada total, se muestran instancias de objeto eliminadas y agregadas.  

> ##### Imagen 7  
> Vista comparación  
> ![Vista comparación][ImageComparisonView]  

<!--todo: add HeapProfilingComparison section when available  -->  

### Vista de contención  

La vista **contención** es esencialmente una "vista de pájaro" de la estructura de objetos de la aplicación.  Le permite realizar un vistazo a los cierres de función para observar los objetos internos de la máquina virtual \ (VM \) que juntos componen los objetos de JavaScript y comprender cuánta memoria usa la aplicación en un nivel muy bajo.  

| Puntos de entrada de la vista de contención | Descripción |  
|:--- |:--- |  
| **Objetos DOMWindow** | Objetos globales para el código de JavaScript.  |  
| **Raíces de GC** | Las raíces de GC reales usadas por el uso de los elementos no usados de la máquina virtual.  Las raíces de GC se componen de mapas de objetos integrados, tablas de símbolos, pilas de subprocesos de VM, memorias caché de compilación, ámbitos de administración y identificadores globales.  |  
| **Objetos nativos** | Los objetos del explorador "se insertan" dentro de la máquina virtual de JavaScript \ (Java VM \) para permitir la automatización, por ejemplo, los nodos DOM, las reglas CSS.  |  

> ##### Imagen 8  
> Vista de contención  
> ![Vista de contención][ImageContainmentView]  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Información sobre cierres.  Asigne un nombre a las funciones de modo que pueda distinguir fácilmente entre cierres de la instantánea.  Por ejemplo, en este ejemplo no se usan funciones con nombre.  
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
> Este ejemplo usa funciones con nombre:  
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
> > ##### old Figure 9  
> > Name functions to distinguish between closures  
> > ![Name functions to distinguish between closures][ImageDomLeaks]  
> -->  
> 
> > [!NOTE]
> > Pruebe este ejemplo para saber [por qué `eval` es malo][GlitchDevtoolsMemoryExample07] analizar el impacto de los cierres en la memoria.  También puede estar interesado en seguirlo con este ejemplo que le guiará a través de la grabación de [asignaciones del montón][GlitchDevtoolsMemoryExample08].  
> 

## Buscar códigos de colores  

Las propiedades y los valores de propiedad de los objetos tienen tipos diferentes y se colorean según corresponda.  Cada propiedad tiene uno de cuatro tipos.  

| Tipo de propiedad | Descripción |  
|:--- |:--- |  
| **a: (propiedad)** | Una propiedad normal con un nombre, al que se accede mediante el `.` operador \ (punto \) o mediante la `[` `]` notación \ (corchetes \), por ejemplo `["foo bar"]` .  |  
| **elemento 0:** | Una propiedad normal con un índice numérico, al que se accede mediante la `[` `]` notación \ (corchetes \).  |  
| **a: var de contexto** |  Variable en un contexto de función, accesible por el nombre de la variable desde un cierre de función.  |  
| **a: Prop del sistema** | Una propiedad agregada por la VM de JavaScript, no accesible desde el código de JavaScript.  |  

Los objetos designados como `System` no tienen un tipo de JavaScript correspondiente.  Cada uno es parte de la implementación del sistema de objetos de la VM de JavaScript.  V8 asigna la mayoría de los objetos internos en el mismo montón que los objetos JS del usuario.  Por eso, son solo 8.  

## Buscar un objeto específico  

Para encontrar un objeto en el montón recopilado, puede realizar la búsqueda con `Ctrl` + `F` el identificador de objeto y darle el nombre.  

## Descubrir fugas de DOM  

El generador de perfiles de pila tiene la capacidad de reflejar las dependencias bidireccionales entre objetos nativos del explorador \ (nodos DOM, reglas CSS \) y objetos JavaScript.
Esto ayuda a descubrir de otra manera las pérdidas invisibles debido a la olvido de subárboles de DOM desvinculados.  

Las fugas de DOM pueden ser más grandes de lo que crees.  Considere el siguiente ejemplo.  ¿Cuándo está el #tree GC?  

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

El `#leaf` mantiene una referencia a los elementos primarios \ (parentNode \) y, de forma recursiva, hasta el momento en que `#tree` el leafRef se ha anulado es todo el árbol bajo `#tree` un candidato para GC.  

> ##### Imagen 9  
> Subárboles DOM  
> ! [Subárboles DOM] [ImageTreeGc]  

> [!NOTE]
> Ejemplos: Pruebe este ejemplo de un [nodo DOM de pérdida][GlitchDevtoolsMemoryExample06] de información para comprender dónde se puede filtrar y cómo detectarlo.  También puede ver este ejemplo de [fugas de Dom de mayor tamaño de lo esperado][GlitchDevtoolsMemoryExample09].  

Para obtener más información sobre las pérdidas de DOM y el análisis de memoria fundamentos de desprotección [Buscar y depurar pérdidas de memoria con Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] por Gonzalo Ruiz de Villa.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageProfilingType]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png "Ilustración 1: seleccionar el tipo de generación de perfiles"  
[ImageTotalSize]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png "Ilustración 2: tamaño total de los objetos que se puede alcanzar"  
[ImageRemoveSnapshots]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png "Ilustración 3: quitar instantáneas"  
[ImageSwitchViews]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png "Ilustración 4: selector cambiar vistas"  
[ImageSummaryView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png "Ilustración 5: vista de Resumen"  
[ImageConstructorGroups]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png "Ilustración 6: grupos de constructores"  
[ImageComparisonView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png "Ilustración 7: vista comparación"  
[ImageContainmentView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png "Ilustración 8: vista de contención"  
<!--[ImageDomLeaks]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-domleaks.msft.png "old Figure 9: Name functions to distinguish between closures"  -->  
[ImageTreeGc]:/Microsoft-Edge/DevTools-Guide-Chromium/media/Memory-problems-Tree-GC.msft.png "Ilustración 9: subárboles DOM"  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#object-sizes "Tamaños de objetos: terminología de memoria"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#objects-retaining-tree "Objetos que conservan la terminología de la memoria de árbol"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "Example-03. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "Example-06. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "Example-07. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "Example-08. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "Example-09. html-Microsoft Edge (cromo) DevTools | Intento"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "Example-10. html-Microsoft Edge (cromo) DevTools | Intento"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "memoria | Las"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) y está creada por [Meggin Kearney][MegginKearney] \ (editor técnico \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
