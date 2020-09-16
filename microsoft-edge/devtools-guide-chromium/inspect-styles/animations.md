---
description: Inspeccione y modifique las animaciones con el inspector de animación de Microsoft Edge DevTools.
title: Inspeccionar animaciones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e867cc373286666f73bee3b8fb886f60fa1b94f6
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015775"
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

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="Inspector de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   Inspector de animación  
:::image-end:::  

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
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animaciones con el menú principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Animaciones** con el menú principal  
    :::image-end:::  
        
*   Abrir el **menú de comandos**  
    1.  Escribe `Drawer: Show Animations`.  

El inspector de animación se abre como una pestaña junto al cajón de consola.  Como el inspector de animación es una pestaña de cajón, puede usar el inspector de animación desde cualquier panel de DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspector de animación vacío" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Inspector de animación vacío  
:::image-end:::  

El inspector de animación se agrupa en cuatro secciones principales \ (o paneles \).  En esta guía se hace referencia a cada panel de la siguiente manera:  

| Índice | Panel | Descripción |  
|:--- |:--- |:--- |  
| uno | **Controles** | Desde aquí puede borrar todos los grupos de animación capturados actualmente o cambiar la velocidad del grupo de animación seleccionado actualmente. |  
| 1 | **Introducción** | Seleccione un grupo de animación aquí para inspeccionarlo y modificarlo en el panel de **detalles** . |  
| 2 | **Línea de tiempo** | PAUSE e inicie una animación desde aquí, o vaya a un punto específico de la animación. |  
| cuatro | **Detalles** | Inspeccionar y modificar el grupo de animación seleccionado actualmente. |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspector de animación con anotaciones" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Inspector de animación con anotaciones  
:::image-end:::  

Para capturar una animación, solo tiene que realizar la interacción que desencadena la animación mientras el inspector de animación está abierto.  Si se desencadena una animación durante la carga de la página, vuelva a cargar la página con el inspector de animación abierto para detectar la animación.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## Inspeccionar animaciones  

Una vez capturada una animación, hay varias maneras de reproducirla:  

*   Mantenga el mouse sobre la miniatura en el panel de **información general** para ver una vista previa de ella.  
*   Seleccione el grupo animación en el panel de **Descripción general** \ (para que se muestre en el panel de **detalles** \) y pulse el icono **reproducir** \ ( ![ icono de reproducción ][ImageReplayButtonIcon] \).  La animación se reproduce en la ventanilla.  Haga clic en los iconos **velocidad de animación** \ ( ![ iconos de velocidad ][ImageAnimationSpeedButtonsIcon] de animación \) para cambiar la velocidad de vista previa del grupo de animación seleccionado actualmente.  Puede usar la barra vertical roja para cambiar la posición actual.  
*   Haga clic y arrastre la barra vertical roja para borrar la animación de la ventanilla.  
    
### Ver detalles de la animación  

Después de capturar un grupo de animaciones, haga clic en él en el panel de **información general** para ver los detalles.  En el panel **detalles** , se asigna una fila a cada animación.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Detalles del grupo animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Detalles del grupo animación  
:::image-end:::  

Mantenga el mouse sobre una animación para resaltarla en el área de visualización.  Haga clic en la animación para seleccionarla en el panel **elementos** .  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Desplace el puntero sobre la animación para resaltarla en el área de visualización" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Desplace el puntero sobre la animación para resaltarla en el área de visualización  
:::image-end:::  

La definición más a la izquierda es la más oscura de una animación.  La sección derecha, más atenuada representa las iteraciones.  Por ejemplo, en la siguiente ilustración, las secciones dos y tres representan iteraciones de la sección uno.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagrama de iteraciones de animación" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Diagrama de iteraciones de animación  
:::image-end:::  

Si se aplica la misma animación a dos elementos, el inspector de animación asigna el mismo color a los elementos.  El color es aleatorio y no tiene importancia.  Por ejemplo, en la siguiente ilustración, los dos elementos `div.cwccw.earlier` y `div.cwccw.later` tienen la misma animación \ ( `spinrightleft` \) aplicada, como los `div.ccwcw.earlier` elementos y `div.ccwcw.later` .  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animaciones con códigos de color" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Animaciones con códigos de color  
:::image-end:::  

## Modificar animaciones  

Hay tres maneras en las que puede modificar una animación con el inspector de animación.  

*   Duración de la animación.  
*   Intervalos de fotogramas clave.  
*   Retardo de inicio.  
    
En la siguiente ilustración, se representa la animación original.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animación original antes de la modificación" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Animación original antes de la modificación  
:::image-end:::  

Para cambiar la duración de una animación, haga clic y arrastre el primer o el último círculo.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Duración modificada" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Duración modificada  
:::image-end:::  

Si la animación define reglas de fotograma clave, se representan como círculos interiores blancos.  Haga clic y arrastre uno de estos para cambiar los intervalos del fotograma clave.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Fotograma clave modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Fotograma clave modificado  
:::image-end:::  

Para agregar un retraso a una animación, haga clic en él y arrástrelo a cualquier lugar excepto los círculos.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Retraso modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Retraso modificado  
:::image-end:::  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: ../media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: ../media/replay-button-icon.msft.png  

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
