---
title: Terminología de la memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: cb258135b7b3c931116d84b1e9b7a548a2b58a6d
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986272"
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
   limitations under the License. -->

# Terminología de la memoria  

En esta sección se describen los términos comunes que se usan en el análisis de memoria y se aplica a una variedad de herramientas de generación de perfiles de memoria para diferentes idiomas.  

Las cláusulas y nociones que se describen aquí hacen referencia al [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots].  Si alguna vez ha trabajado con Java, .NET o algún otro analizador de memoria, es posible que se trata de un repaso.  

## Tamaños de objeto  

Piense en la memoria como en un gráfico con tipos primitivos \ (como números y cadenas \) y objetos \ (asociantes de matrices \).  Puede representarse visualmente como un gráfico con un número de puntos interconectados, como se muestra a continuación:  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Representación visual de la memoria" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   Representación visual de la memoria  
:::image-end:::  

Un objeto puede contener memoria de dos maneras:  

*   Directamente por el objeto.  
*   De forma implícita, reteniendo referencias a otros objetos y, por lo tanto, impidiendo que un recolector de elementos no utilizados \ (**GC** por abreviado \) lo elimine automáticamente.  

Al trabajar con el panel [memoria][DevtoolsMemoryProblemsHeapSnapshots] en DevTools \ (una herramienta para investigar los problemas de memoria que se encuentran en **memoria**\), es posible que vea algunas columnas de información diferentes.  Dos que destaquen son **el tamaño superficial** y **el tamaño guardado**, pero ¿qué representa?  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tamaño Shallow y retenido" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   Tamaño Shallow y retenido  
:::image-end:::  

### Tamaño superficial  

Este es el tamaño de la memoria que posee el objeto.  

Los objetos típicos de JavaScript tienen memoria reservada para su descripción y para almacenar valores inmediatos.  Normalmente, solo las matrices y cadenas pueden tener un tamaño superficial significativo.  Sin embargo, las cadenas y las matrices externas suelen tener su almacenamiento principal en la memoria del representador y solo exponen un pequeño objeto contenedor en el montón de JavaScript.  

La memoria del representador es toda la memoria del proceso donde se representa una página inspeccionada: memoria nativa + JS memoria del montón de la memoria del montón Page + JS de todos los trabajadores dedicados iniciados por la página.  Sin embargo, incluso un objeto pequeño puede contener una gran cantidad de memoria indirectamente, impidiendo que otros objetos sean eliminados por el proceso de recolección automática de elementos no utilizados.  

### Tamaño retenido  

Este es el tamaño de memoria que se libera una vez que se elimina el objeto junto con los objetos dependientes que se han inaccesible desde las **raíces del recolector de elementos no utilizados** \ (raíces de GC \).  

Las **raíces del recolector de elementos no utilizados** \ (raíces de GC \) se componen de **identificadores** que se crean \ (local o global \) cuando se hace referencia desde código nativo a un objeto de JavaScript fuera de V8.  Puede encontrar todos los identificadores de ese tipo dentro de una instantánea de montones, en **raíces de GC**  >  **Handle scope** , **GC roots**  >  **identificadores globales**de ámbito y raíz del GC.  La descripción de los identificadores de esta documentación sin profundizar en los detalles de la implementación del explorador puede resultar confusa.  Tanto las raíces del recopilador de elementos no usados (GC) como los identificadores no son algo de lo que necesita preocuparse.  

Hay una gran cantidad de raíces de GC internas, la mayoría de las cuales no son interesantes para los usuarios.  Desde el punto de vista de las aplicaciones existen siguientes tipos de raíces.  

*   Objeto global Window \ (en cada iframe \).  Hay un campo Distance en las instantáneas de montones, que es el número de referencias de propiedad en la ruta de retención más corta de la ventana.  
*   Árbol DOM de documento compuesto de todos los nodos DOM nativos a los que se puede atravesar el documento.  Es posible que no todos los nodos tengan contenedores JS, pero si un nodo tiene un contenedor, estará activo mientras el documento está activo.  
*   A veces, el contexto del depurador puede conservar los objetos en el panel **orígenes** y la **consola** \ (por ejemplo, después de la evaluación de consola \).  Crear instantáneas de montones con un panel de **consola** desactivado y sin puntos de interrupción activos en el depurador del panel **orígenes** .

>[!TIP]
> Para borrar el panel de la **consola** , ejecute `clear()` y desactive los puntos de interrupción en el panel **fuentes** antes de tomar una instantánea del montón en el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots].

El gráfico de memoria se inicia con una raíz, que puede ser el `window` objeto del explorador o el `Global` objeto de un módulo Node.js.  No controla cómo se recolecta este objeto raíz (M.c. d).  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="No puede controlar cómo se recolectan los elementos no utilizados en el objeto raíz." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   No puede controlar cómo se recolectan los elementos no utilizados en el objeto raíz.  
:::image-end:::  

Lo que no sea accesible desde la raíz obtiene el recolector de elementos no usados \ (M.c. d \).  

> [!NOTE]
> Las columnas [tamaño superficial](#shallow-size) y [tamaño retenido](#retained-size) representan datos en bytes.  

## Árbol de objetos reteniendo  

El montón es una red de objetos interconectados.  En el mundo matemático, esta estructura se denomina gráfico **o gráfico de memoria** .  Un gráfico se crea a partir de los **nodos** conectados por medio de **bordes**, de los cuales se proporcionan etiquetas.  

*   Los **nodos** \ (u **objetos**\) se etiquetan con el nombre de la función **constructora** que se usó para crearlos.  
*   Los **bordes** se etiquetan con los nombres de **las propiedades**.  

Obtenga información sobre [Cómo grabar un perfil con el generador de perfiles del montón][DevtoolsMemoryProblemsHeapSnapshots].  En la siguiente ilustración, algunas de las cosas llamativas que puede ver en el registro de instantáneas de montones en el [Panel memoria][DevtoolsMemoryProblemsHeapSnapshots] incluyen distancia: la distancia desde la raíz del recolector de elementos no utilizados \ (GC \).  Si casi todos los objetos del mismo tipo se encuentran a la misma distancia y algunos están a una mayor distancia, es algo que vale la pena investigar.  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distancia desde la raíz" lightbox="../media/memory-problems-root.msft.png":::
   Distancia desde la raíz  
:::image-end:::  

## Dominators  

Los objetos Dominator se componen de una estructura de árbol, ya que cada objeto tiene exactamente un Dominator.  Un Dominator de un objeto puede carecer de referencias directas a un objeto que domina; es decir, el árbol de Dominator no es un árbol de expansión del gráfico.  

En la siguiente ilustración, la siguiente instrucción es verdadera.  

*   El nodo 1 domina el nodo 2  
*   El nodo 2 predomina los nodos 3, 4 y 6  
*   Nodo 3 domina el nodo 5  
*   El nodo 5 domina el nodo 8  
*   El nodo 6 domina el nodo 7  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Estructura de árbol de Dominator" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   Estructura de árbol de Dominator  
:::image-end:::  

En la siguiente ilustración, node `#3` es el Dominator de `#10` , pero `#7` también existe en cada path simple desde el recolector de elementos no utilizados \ (GC \) a `#10` .  Por lo tanto, un objeto B es un Dominator de un objeto A si B existe en cada ruta simple de la raíz al objeto a.  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Ilustración Dominator animada" lightbox="../media/memory-problems-dominators.msft.gif":::
   Ilustración Dominator animada  
:::image-end:::  

## Características específicas de V8  

Al generar perfiles de memoria, resulta útil comprender por qué las instantáneas de montones se ven de una determinada manera.  En esta sección se describen algunos temas relacionados con la memoria que corresponden específicamente a la **máquina virtual de JavaScript V8** \ (V8 VM o VM \).  

### Representación de objeto de JavaScript  

Hay tres tipos primitivos:  

*   Números \ (por ejemplo `3.14159...` \)  
*   Booleanos \ ( `true` o `false` \)  
*   Cadenas \ (por ejemplo `"Werner Heisenberg"` \)  

Los tipos primitivos no pueden hacer referencia a otros valores y siempre son hojas o nodos de terminación.  

**Los números** se pueden almacenar como:  

*   valores enteros de 31 bits inmediatos denominados **pequeños enteros** \ (**SMI**s \) o  
*   objetos Heap, denominados **números de montones**. Los números de montones se usan para almacenar valores que no se ajustan al formulario de SMI, como valores **Double**o cuando es necesario aplicar la **conversión boxing**a un valor, como establecer propiedades en él.  

Las **cadenas** pueden almacenarse en:  

*   el **montón de VM**o
*   externamente en la **memoria del representador**.  Se crea un **objeto contenedor** y se usa para acceder a un almacenamiento externo donde, por ejemplo, se almacenan los orígenes de script y otro contenido que se recibe de la web, en lugar de copiarse en el montón de la VM.

La memoria de los nuevos objetos de JavaScript se asigna desde un montón de JavaScript dedicado \ (o **montón VM**\).  Estos objetos se administran mediante el recolector de elementos no utilizados en V8 y, por lo tanto, permanecen activos siempre que haya al menos una referencia fuerte.  

Todo lo que no esté en el montón de JavaScript se denomina **objeto nativo**.  Los objetos nativos, a diferencia de los objetos Heap, no se administran en el recolector de elementos no utilizados de la V8 durante su período de duración, y solo se puede acceder a ellos desde JavaScript mediante el objeto wrapper de JavaScript.  

La **cadena cons** es un objeto que consta de pares de cadenas almacenadas y, a continuación, se unen, y es un resultado de una concatenación.  La Unión del contenido de la **cadena cons** solo se produce cuando es necesario. Un ejemplo sería cuando es necesario construir una subcadena de una cadena combinada.

Por ejemplo, si concatena `a` y `b` , obtiene una cadena `(a, b)` que representa el resultado de la concatenación.  Si más adelante se ha concatenado `d` con ese resultado, obtendrá otra **cadena de cons**: `((a, b, d)` .  

**Matriz** es un objeto con teclas numéricas. Las **matrices** se usan ampliamente en la máquina virtual V8 para almacenar grandes cantidades de datos. Se realiza una copia de seguridad de los conjuntos de pares clave-valor, como diccionarios, por **matriz**.  

Un objeto de JavaScript típico se almacena como uno de los dos tipos de **matriz** :  

*   propiedades con nombre y  
*   elementos numéricos  

Cuando hay un pequeño número de propiedades, las propiedades se almacenan internamente en el objeto de JavaScript.  

**Map** es un objeto que describe el tipo de objeto que es y el diseño. Por ejemplo, los mapas se usan para describir jerarquías de objetos implícitas para un [acceso rápido a la propiedad][V8FastProperties].  

### Grupos de objetos  

Cada grupo de **objetos nativos** está compuesto de objetos que contienen referencias mutuas entre sí.  Considere, por ejemplo, un subárbol DOM en el que cada nodo tiene un vínculo al elemento primario relativo y vincula al siguiente elemento secundario y al elemento relacionado siguiente, por lo tanto, formando un gráfico conectado.  

> [!NOTE]
> Los objetos nativos no se representan en el montón de JavaScript.  La falta de representación es el motivo por el que los objetos nativos tienen el tamaño cero. En su lugar, se crean objetos contenedores.  

Cada objeto contenedor mantiene una referencia al objeto nativo correspondiente, para redirigir comandos a él.  A su vez, un grupo de objetos contiene objetos contenedores.  Sin embargo, esto no crea un ciclo que no se puede cobrar porque el recolector de elementos no usados \ (GC \) es lo suficientemente inteligente para liberar los grupos de objetos cuyos contenedores ya no se hacen referencia. Pero olvidar liberar un único contenedor alberga todo el grupo y los contenedores asociados.  

## Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Cómo grabar instantáneas de montones | Microsoft docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propiedades rápidas de V8 | V8"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) y está creada por [Meggin Kearney][MegginKearney] \ (editor técnico \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
