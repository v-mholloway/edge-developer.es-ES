---
description: En esta sección se describen los términos comunes usados en el análisis de memoria y se aplica a una variedad de herramientas de generación de perfiles de memoria para diferentes idiomas.
title: Terminología de memoria
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: c9659255e2bf0082cd1be3e6615c9d54c293b967
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519313"
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

# <a name="memory-terminology"></a>Terminología de memoria  

En este artículo se describen los términos comunes usados en el análisis de memoria y se aplica a varias herramientas de generación de perfiles de memoria para diferentes idiomas.  

Los términos y nociones que se describen aquí hacen referencia al [panel Memoria][DevtoolsMemoryProblemsHeapSnapshots].  Si alguna vez ha trabajado con el Java, .NET o algún otro perfilador de memoria, este artículo puede ser un actualizador.  

## <a name="object-sizes"></a>Tamaños de objeto  

Piense en la memoria como un gráfico con tipos primitivos \(como números y cadenas\) y objetos \(matrices asociativas\).  Puede mostrarse como un gráfico con muchos puntos interconectados, como la siguiente figura.  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Representación visual de la memoria" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   Representación visual de la memoria  
:::image-end:::  

Un objeto puede contener memoria de dos maneras:  

*   Directamente por el objeto.  
*   Implícitamente manteniendo referencias a otros objetos y, por lo tanto, evitando que un recolector de elementos no utilizados desechar automáticamente esos objetos.  

Al trabajar con el [panel][DevtoolsMemoryProblemsHeapSnapshots] Memoria en DevTools \(una herramienta para investigar problemas de memoria encontrados en **Memoria**\), puede encontrarse mirando algunas columnas diferentes de información.  Dos que destacan son **Shallow Size y** **Retained Size,** pero ¿qué representan estos?  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tamaño superficial y retenido" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   Tamaño superficial y retenido  
:::image-end:::  

### <a name="shallow-size"></a>Tamaño superficial  

Este es el tamaño de la memoria que contiene el objeto.  

Los objetos JavaScript típicos tienen algo de memoria reservada para su descripción y para almacenar valores inmediatos.  Normalmente, solo las matrices y las cadenas pueden tener un tamaño superficial significativo.  Sin embargo, las cadenas y matrices externas a menudo tienen su almacenamiento principal en la memoria del representador, lo que expone solo un pequeño objeto contenedor en el montón de JavaScript.  

La memoria del representador es toda la memoria del proceso en el que se representa una página inspeccionada: memoria nativa + memoria de montón JS de la página + memoria de montón JS de todos los trabajadores dedicados iniciados por la página.  Sin embargo, incluso un objeto pequeño puede contener una gran cantidad de memoria indirectamente, al impedir que el proceso de recolección automática de elementos no utilizados desechar otros objetos.  

### <a name="retained-size"></a>Tamaño retenido  

Este es el tamaño de la memoria que se libera una vez que el objeto se elimina junto con los objetos dependientes que se han hecho inaccesibles desde las raíces del recolector **de elementos no utilizados.**  

**Las** raíces del recolector de elementos no utilizados están hechas de controladores que se crean \(local o global\) al hacer una referencia desde código nativo a un objeto JavaScript fuera de V8. ****  Todos estos controladores pueden encontrarse en una instantánea de montón en el ámbito de control de raíces **de GC**y en las raíces  >  **** de **GC**  >  **Controladores globales.**  Describir los controladores de esta documentación sin entrar en detalles de la implementación del explorador puede resultar confuso.  Tanto las raíces del recolector de elementos no utilizados como los controladores no son algo de lo que tenga que preocuparse.  

Hay muchas raíces internas del recolector de elementos no utilizados, la mayoría de las cuales no son interesantes para los usuarios.  Desde el punto de vista de las aplicaciones, hay los siguientes tipos de raíces.  

*   Objeto global window \(en cada iframe\).  En las instantáneas de montón, el campo indica el número de referencias a propiedades en la ruta de retención más corta `distance` de la ventana.  
*   El árbol DOM del documento, que consta de todos los nodos DOM nativos a los que se puede acceder recorriendo el documento.  No todos los nodos tienen contenedores de JavaScript, pero si un nodo tiene un contenedor, el nodo está activo mientras el documento está activo.  
*   A veces, el contexto de depuración retiene los objetos en la **herramienta Orígenes** y la **consola,** como después de la evaluación de la consola.  Cree instantáneas de montón con una herramienta **de consola** desactivada y sin puntos de interrupción activos en el depurador en la **herramienta Orígenes.**

>[!TIP]
> Antes de tomar una instantánea de montón en la [herramienta Memoria,][DevtoolsMemoryProblemsHeapSnapshots] desactive la herramienta **Consola** y desactive los puntos de interrupción en la **herramienta Orígenes.**  Para borrar la **herramienta Consola,** ejecute el `clear()` método.  

El gráfico de memoria comienza con una raíz, que puede ser el objeto del explorador o el `window` objeto de un Node.js `Global` módulo.  No se controla cómo se recopila el objeto raíz.  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="No puede controlar cómo se recopila el objeto raíz." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   No puede controlar cómo se recopila el objeto raíz.  
:::image-end:::  

Todo lo que no se puede obtener desde la raíz obtiene la recolección de elementos no utilizados.  

> [!NOTE]
> Las columnas [Tamaño superficial y](#shallow-size) Tamaño [retenido](#retained-size) representan datos en bytes.  

## <a name="objects-retaining-tree"></a>Árbol de retención de objetos  

El montón es una red de objetos interconectados.  En el mundo matemático, esta estructura se denomina gráfico **o** gráfico de memoria.  Un gráfico se construye a partir de **nodos conectados** mediante **bordes,** a los que se les dan etiquetas.  

*   **Los** nodos \(u **objetos**\) se etiquetan con el nombre de la **función de constructor** que se usó para crearlos.  
*   **Los** bordes se etiquetan con los nombres de **las propiedades**.  

Obtenga [información sobre cómo grabar un perfil mediante el Profiler de montón][DevtoolsMemoryProblemsHeapSnapshots].  En la siguiente figura, algunos de los aspectos [][DevtoolsMemoryProblemsHeapSnapshots] notables de la grabación de instantáneas de montón en la herramienta Memoria incluyen distancia: la distancia desde la raíz del recolector de elementos no utilizados.  Si casi todos los objetos del mismo tipo están a la misma distancia y algunos están a una distancia mayor, eso es algo que vale la pena investigar.  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distancia desde la raíz" lightbox="../media/memory-problems-root.msft.png":::
   Distancia desde la raíz  
:::image-end:::  

## <a name="dominators"></a>Dominadores  

Los objetos dominantes se componen de una estructura de árbol porque cada objeto tiene exactamente un dominante.  Un dominante de un objeto puede carecer de referencias directas a un objeto que domina; es decir, el árbol del dominante no es un árbol de expansión del gráfico.  

En la siguiente figura, se cumple la siguiente instrucción.  

*   El nodo 1 domina el nodo 2  
*   El nodo 2 domina los nodos 3, 4 y 6  
*   El nodo 3 domina el nodo 5  
*   El nodo 5 domina el nodo 8  
*   El nodo 6 domina el nodo 7  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Estructura de árbol de dominio" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   Estructura de árbol de dominio  
:::image-end:::  

En la siguiente figura, node es el dominante de , pero también existe en todas las rutas `#3` `#10` `#7` sencillas de recolector de elementos no utilizados a `#10` .  Por lo tanto, un objeto B es un dominante de un objeto A si B existe en todas las rutas de acceso sencillas desde la raíz al objeto A.  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Ilustración de un domador animado" lightbox="../media/memory-problems-dominators.msft.gif":::
   Ilustración de un domador animado  
:::image-end:::  

## <a name="v8-specifics"></a>Detalles de V8  

Al generar perfiles de memoria, resulta útil comprender por qué las instantáneas de montón tienen un aspecto determinado.  En esta sección se describen algunos temas relacionados con la memoria que corresponden específicamente a la máquina **virtual V8 JavaScript** \(V8 VM o VM\).  

### <a name="javascript-object-representation"></a>Representación de objetos de JavaScript  

Hay tres tipos primitivos:  

*   Números \(por ejemplo `3.14159...` \)  
*   Booleans \( `true` o `false` \)  
*   Cadenas \(por ejemplo `"Werner Heisenberg"` \)  

Los primitivos no pueden hacer referencia a otros valores y siempre son hojas o nodos de finalización.  

**Los** números se pueden almacenar como:  

*   valores enteros inmediatos de 31 bits **denominados enteros pequeños** \(**SMI**s\) o  
*   objetos de montón, denominados números **de montón**. Los números de montón se usan para almacenar valores que no caben en el formulario SMI, como **dobles,** o cuando es necesario boxe un **valor,** como establecer propiedades en él.  

**Las cadenas** pueden almacenarse en:  

*   el **montón de vm**o
*   externamente en la **memoria del representador**.  Se **crea un** objeto contenedor y se usa para obtener acceso al almacenamiento externo donde, por ejemplo, se almacenan orígenes de scripts y otro contenido que se recibe de la Web, en lugar de copiarse en el montón de vm.

La memoria de los nuevos objetos JavaScript se asigna desde un montón de JavaScript dedicado \(o **montón de vm**\).  El recolector de elementos no utilizados administra estos objetos en V8 y, por lo tanto, permanecen vivos siempre que haya al menos una referencia segura a ellos.  

Cualquier cosa que no esté en el montón de JavaScript se denomina **objeto nativo**.  El recolector de elementos no utilizados V8 no administra los objetos nativos, a diferencia de los objetos montón, y solo se puede obtener acceso a ellos desde JavaScript mediante el objeto contenedor de JavaScript.  

**La cadena Cons** es un objeto que consta de pares de cadenas almacenadas y luego unidas, y es el resultado de la concatenación.  La unión del contenido **de la cadena cons** se produce solo según sea necesario.  Por ejemplo, cuando es necesario construir una subcadena de una cadena unida.

Por ejemplo, si concatena y `a` , obtiene una cadena que representa el resultado de la `b` `(a, b)` concatenación.  Si más tarde concatena con `d` ese resultado, obtiene otra **cadena de cons**: `((a, b, d)` .  

**Array** es un objeto con claves numéricas. **Las matrices** se usan ampliamente en la vm V8 para almacenar grandes cantidades de datos. Las matrices copian una copia de seguridad de los conjuntos de pares clave-valor, como **diccionarios.**  

Un objeto JavaScript típico se almacena como solo uno de los dos tipos **de matriz:**  

*   propiedades con nombre y  
*   elementos numéricos  

Cuando hay un número reducido de propiedades, las propiedades se almacenan internamente en el objeto JavaScript.  

**Map** es un objeto que describe tanto el tipo de objeto que es como el diseño. Por ejemplo, los mapas se usan para describir jerarquías de objetos implícitos para [el acceso rápido a propiedades][V8FastProperties].  

### <a name="object-groups"></a>Grupos de objetos  

Cada **grupo de objetos** nativos está hecho de objetos que tienen referencias mutuas entre sí.  Tenga en cuenta, por ejemplo, un subárbol DOM donde cada nodo tiene un vínculo al elemento primario relativo y vínculos al siguiente elemento secundario y al siguiente elemento del mismo nivel, formando así un gráfico conectado.  

> [!NOTE]
> Los objetos nativos no se representan en el montón de JavaScript.  La falta de representación es la razón por la que los objetos nativos tienen un tamaño cero. En su lugar, se crean objetos contenedor.  

Cada objeto contenedor contiene una referencia al objeto nativo correspondiente, para redirigir comandos a él.  A su vez, un grupo de objetos contiene objetos contenedor.  Sin embargo, esto no crea un ciclo irreconectable, ya que recolector de elementos no utilizados es lo suficientemente inteligente como para liberar grupos de objetos cuyos contenedores ya no se hacen referencia.  Pero el olvido de liberar un solo contenedor contiene todo el grupo y los contenedores asociados.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Cómo grabar instantáneas de montón | Microsoft Docs"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propiedades rápidas en V8 | V8"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) y es creado por [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
