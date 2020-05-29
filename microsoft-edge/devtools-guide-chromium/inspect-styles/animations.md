---
title: Inspeccionar animaciones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6466c7f0e1f8680a2429b565e8022d152d05d733
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10574478"
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





# Inspeccionar animaciones   



Inspeccione y modifique las animaciones con el inspector de animación de Microsoft Edge DevTools.  

> ##### Figura 1  
> Inspector de animación  
> ![Inspector de animación][ImageAnimationInspector]  

### Resumen  

*   Capture animaciones abriendo el inspector de animación.  El inspector de animación detecta y ordena automáticamente las animaciones en grupos.  
*   Inspeccione las animaciones y reduzca la velocidad de cada una de ellas, reproduzca cada una o vea el código de origen.  
*   Modifique las animaciones cambiando los intervalos, el retraso, la duración o los desplazamientos de los fotogramas clave.  

## Introducción   

El inspector de animación de Microsoft Edge DevTools tiene dos propósitos principales.  

*   Inspeccionar animaciones.  Desea ralentizar, reproducir o inspeccionar el código fuente de un grupo de animación.  
*   Modificar animaciones.  Desea modificar el intervalo, el retraso, la duración o los desplazamientos de los fotogramas clave de un grupo de animaciones.  Actualmente, no se admite la edición de curvas y la edición de fotogramas.  

El inspector de animación admite animaciones CSS, transiciones CSS y animaciones web.  `requestAnimationFrame` Actualmente, no se admiten las animaciones.  

### ¿Qué es un grupo de animación?  

Un grupo de animación es un grupo de animaciones que pueden estar relacionadas entre sí.  Por el momento, la web no tiene ningún concepto real de animación grupal, por lo que los diseñadores y los programadores de movimiento tienen que componer animaciones individuales para que las animaciones se representen como un efecto visual coherente.  El inspector de animación predice qué animaciones se relacionan según el tiempo de Inicio \ (excluyendo demoras, etc. \).  El inspector de animación también agrupa las animaciones en paralelo.  
En otras palabras, se agrupan juntos un conjunto de animaciones que se desencadenan en el mismo bloque de script.  Si una animación es asincrónica, se coloca en un grupo independiente.  

## Comenzar  

Hay dos formas de abrir el inspector de animación:  

*   Abrir el menú de **DevTools personalizar y controlar**  
    1.  Vaya al submenú **más herramientas** .  
    1.  Seleccione **animaciones**:  
        
        > ##### Figura 2  
        > Animaciones a través del menú principal  
        > ![Animaciones a través del menú principal][ImageAnimationsViaMainMenu]  
        
*   Abrir el **menú de comandos**  
    1.  Escribe `Drawer: Show Animations`.  

El inspector de animación se abre como una pestaña junto al cajón de consola.  Como el inspector de animación es una pestaña de cajón, puede usar el inspector de animación desde cualquier panel de DevTools.  

> ##### Imagen 3  
> Inspector de animación vacío  
> ![Inspector de animación vacío][ImageEmptyAnimationInspector]  

El inspector de animación se agrupa en cuatro secciones principales \ (o paneles \).  En esta guía se hace referencia a cada panel de la siguiente manera:  

| | Panel | Descripción |  
| --- |:--- |:--- |  
| uno | **Controles** | Desde aquí puede borrar todos los grupos de animación capturados actualmente o cambiar la velocidad del grupo de animación seleccionado actualmente. |  
| 1 | **Introducción** | Seleccione un grupo de animación aquí para inspeccionarlo y modificarlo en el panel de **detalles** . |  
| 2 | **Línea de tiempo** | PAUSE e inicie una animación desde aquí, o vaya a un punto específico de la animación. |  
| cuatro | **Detalles** | Inspeccionar y modificar el grupo de animación seleccionado actualmente. |  

> ##### Imagen 4  
> Inspector de animación con anotaciones  
> ![Inspector de animación con anotaciones][ImageAnnotatedAnimationInspector]  

Para capturar una animación, solo tiene que realizar la interacción que desencadena la animación mientras el inspector de animación está abierto.  Si se desencadena una animación durante la carga de la página, vuelva a cargar la página con el inspector de animación abierto para detectar la animación.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## Inspeccionar animaciones   

Una vez capturada una animación, hay varias maneras de reproducirla:  

*   Mantenga el mouse sobre la miniatura en el panel de **información general** para ver una vista previa de ella.  
*   Seleccione el grupo animación en el panel de **Descripción general** \ (para que se muestre en el panel de **detalles** \) y pulse el icono **reproducir** volver a ![ reproducir ][ImageReplayButtonIcon] .  La animación se reproduce en la ventanilla.  Haga clic en los iconos de iconos de velocidad de animación **velocidad** de animación ![ ][ImageAnimationSpeedButtonsIcon] para cambiar la velocidad de vista previa del grupo de animación seleccionado actualmente.  Puede usar la barra vertical roja para cambiar la posición actual.  
*   Haga clic y arrastre la barra vertical roja para borrar la animación de la ventanilla.  

### Ver detalles de la animación  

Después de capturar un grupo de animaciones, haga clic en él en el panel de **información general** para ver los detalles.  En el panel **detalles** , se asigna una fila a cada animación.  

> ##### Imagen 5  
> Detalles del grupo animación  
> ![Detalles del grupo animación][ImageAnimationGroupDetails]  

Mantenga el mouse sobre una animación para resaltarla en el área de visualización.  Haga clic en la animación para seleccionarla en el panel **elementos** .  

> ##### Imagen 6  
> Desplace el puntero sobre la animación para resaltarla en el área de visualización  
> ![Desplace el puntero sobre la animación para resaltarla en el área de visualización][ImageHoverOverAnimationHighlightViewport]  

La definición más a la izquierda es la más oscura de una animación.  La sección derecha, más atenuada representa las iteraciones.  Por ejemplo, en la [figura 7](#figure-7), las secciones dos y tres representan iteraciones de la sección uno.  

> ##### Imagen 7  
> Diagrama de iteraciones de animación  
> ![Diagrama de iteraciones de animación][ImageDiagramAnimationIterations]  

Si se aplica la misma animación a dos elementos, el inspector de animación asigna el mismo color a los elementos.  El color es aleatorio y no tiene importancia.  Por ejemplo, en la [figura 8](#figure-8) los dos elementos `div.cwccw.earlier` y `div.cwccw.later` tienen la misma animación \ ( `spinrightleft` \) aplicada, como los `div.ccwcw.earlier` elementos y `div.ccwcw.later` .  

> ##### Imagen 8  
> Animaciones con códigos de color  
> ![Animaciones con códigos de color][ImageColorCodedAnimations]  

## Modificar animaciones   

Hay tres maneras en las que puede modificar una animación con el inspector de animación:  

*   Duración de la animación.  
*   Intervalos de fotogramas clave.  
*   Retardo de inicio.  

Para esta sección, suponga que la [figura 9](#figure-9) representa la animación original:  

> ##### Imagen 9  
> Animación original antes de la modificación  
> ![Animación original antes de la modificación][ImageOriginalAnimationBeforeModification]  

Para cambiar la duración de una animación, haga clic y arrastre el primer o el último círculo.  

> ##### Imagen 10  
> Duración modificada  
> ![Duración modificada][ImageModifiedDuration]  

Si la animación define reglas de fotograma clave, se representan como círculos interiores blancos.  Haga clic y arrastre uno de estos para cambiar los intervalos del fotograma clave.  

> ##### Imagen 11  
> Fotograma clave modificado  
> ![Fotograma clave modificado][ImageModifiedKeyframe]  

Para agregar un retraso a una animación, haga clic en él y arrástrelo a cualquier lugar excepto los círculos.  

> ##### Imagen 12  
> Retraso modificado  
> ![Retraso modificado][ImageModifiedDelay]  

<!--   -->  



<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: /microsoft-edge/devtools-guide-chromium/media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/replay-button-icon.msft.png  

[ImageAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-completed.msft.png "Ilustración 1: inspector de animación"  
[ImageAnimationsViaMainMenu]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-more-tools-animations.msft.png "Ilustración 2: animaciones a través del menú principal"  
[ImageEmptyAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations.msft.png "Ilustración 3: inspector de animación vacío"  
[ImageAnnotatedAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png "Ilustración 4: inspector de animación con anotaciones"  
[ImageAnimationGroupDetails]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png "Ilustración 5: detalles del grupo animación"  
[ImageHoverOverAnimationHighlightViewport]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png "Ilustración 6: Mantenga el mouse sobre la animación para resaltarla en el área de visualización"  
[ImageDiagramAnimationIterations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations-highlight.msft.png "Ilustración 7: Diagrama de las iteraciones de animación"  
[ImageColorCodedAnimations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations.msft.png "Ilustración 8: animaciones con código de color"  
[ImageOriginalAnimationBeforeModification]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations.msft.png "Ilustración 9: animación original antes de la modificación"  
[ImageModifiedDuration]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png "Ilustración 10: duración modificada"  
[ImageModifiedKeyframe]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png "Ilustración 11: fotograma clave modificado"  
[ImageModifiedDelay]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png "Ilustración 12: retraso modificado"  

<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
