---
description: Inspeccione y modifique las animaciones con Microsoft Edge DevTools Animation Inspector.
title: Inspeccionar animaciones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a695517cb56da057e62293b5ca92b22058602f44
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564220"
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
# <a name="inspect-animations"></a>Inspeccionar animaciones  

Inspeccione y modifique las animaciones con Microsoft Edge DevTools Animation Inspector.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png" alt-text="inspector de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-completed.msft.png":::
   inspector de animación  
:::image-end:::  

### <a name="summary"></a>Resumen  

*   Captura animaciones abriendo el Inspector de animación.  El Inspector de animación detecta y ordena automáticamente las animaciones en grupos.  
*   Inspeccione las animaciones ralentizando cada una, reprobando cada una o viendo el código fuente.  
*   Modifique las animaciones cambiando el tiempo, el retraso, la duración o los desplazamientos de fotograma clave.  

## <a name="overview"></a>Introducción  

El Microsoft Edge DevTools Animation Inspector tiene dos propósitos principales.  

*   Inspeccionar animaciones.  Quieres ralentizar, reproducir o inspeccionar el código fuente de un grupo de animación.  
*   Modificar animaciones.  Desea modificar los desplazamientos de tiempo, retraso, duración o fotograma clave de un grupo de animación.  Actualmente, no se admite la edición de bezier ni la edición de fotogramas clave.  

El Inspector de animación admite animaciones CSS, transiciones CSS y animaciones web.  `requestAnimationFrame` actualmente no se admiten animaciones.  

### <a name="what-is-an-animation-group"></a>¿Qué es un grupo de animación?  

Un grupo de animaciones es un grupo de animaciones que pueden estar relacionadas entre sí.  Actualmente, la web no tiene un concepto real de una animación de grupo, por lo que los diseñadores y desarrolladores de movimiento tienen que componer y dar tiempo a animaciones individuales para que las animaciones se representen como un efecto visual coherente.  El Inspector de animación predice qué animaciones están relacionadas en función de la hora de inicio \(excluyendo retrasos, y así sucesivamente\).  El Inspector de animación también agrupa las animaciones en paralelo.  
En otras palabras, un conjunto de animaciones que se desencadenan en el mismo bloque de script se agrupan.  Si una animación es asincrónica, se coloca en un grupo independiente.  

## <a name="get-started"></a>Comenzar  

Hay dos formas de abrir el Inspector de animación:  

*   Abra el **menú Personalizar y controlar DevTools**  
    1.  Vaya al **submenú Más** herramientas.  
    1.  Elegir **animaciones**:  
        
        :::image type="complex" source="../media/inspect-styles-elements-styles-more-tools-animations.msft.png" alt-text="Animaciones con el menú principal" lightbox="../media/inspect-styles-elements-styles-more-tools-animations.msft.png":::
           **Animaciones con** el menú principal  
        :::image-end:::  
        
*   Abrir el **menú de comandos**  
    1.  Escriba `Drawer: Show Animations`.  
        
El Inspector de animación se abre junto a la **herramienta Consola.**  Dado que el Inspector de animación es una herramienta de cajón, puedes usar el Inspector de animación desde cualquier panel DevTools.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations.msft.png" alt-text="Inspector de animación vacío" lightbox="../media/inspect-styles-elements-styles-drawer-animations.msft.png":::
   Inspector de animación vacío  
:::image-end:::  

El Inspector de animación se agrupa en cuatro secciones principales \(o panes\).  Esta guía hace referencia a cada panel de la siguiente manera:  

| Índice | Panel | Descripción |  
|:--- |:--- |:--- |  
| 1 | **Controles** | Desde aquí, puedes borrar todos los grupos de animación capturados actualmente o cambiar la velocidad del grupo de animación seleccionado actualmente. |  
| 2 | **Introducción** | Elija un grupo de animación aquí para inspeccionarlo y modificarlo en el **panel** Detalles. |  
| 3 | **Línea de tiempo** | Pausa e inicia una animación desde aquí, o salta a un punto específico de la animación. |  
| 4 | **Detalles** | Inspeccione y modifique el grupo de animaciones seleccionado actualmente. |  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png" alt-text="Inspector de animación anotado" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png":::
   Inspector de animación anotado  
:::image-end:::  

Para capturar una animación, simplemente realiza la interacción que desencadena la animación mientras el Inspector de animación está abierto.  Si se desencadena una animación al cargar la página, actualice la página con el Inspector de animación abierto para detectar la animación.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## <a name="inspect-animations"></a>Inspeccionar animaciones  

Después de capturar una animación, hay varias maneras de reproducirla:  

*   Mantenga el mouse en la miniatura del panel **Información** general para ver una vista previa de ella.  
*   Elija el grupo de animación en el **panel** Información **** general \(para que se muestre en el panel Detalles\) y elija el icono **de** reproducción \( icono de reproducción ![ ](../media/replay-button-icon.msft.png) \).  La animación se reproduce en la ventanilla.  Elige los **iconos de velocidad de** animación \( iconos de velocidad de animación \) para cambiar la velocidad de vista previa del grupo de ![ ](../media/animation-speed-buttons-icon.msft.png) animaciones seleccionado actualmente.  Puede usar la barra vertical roja para cambiar la posición actual.  
*   Elija y arrastre la barra vertical roja para limpiar la animación de la ventanilla.  
    
### <a name="view-animation-details"></a>Ver detalles de animación  

Después de capturar un grupo de animación, elige en él en el **panel** Información general para ver los detalles.  En el **panel Detalles,** se asigna una fila a cada animación individual.  

:::image type="complex" source="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Detalles del grupo de animación" lightbox="../media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png":::
   Detalles del grupo de animación  
:::image-end:::  

Mantenga el mouse sobre una animación para resaltarla en la ventanilla.  Elija la animación para seleccionarla en la **herramienta** Elementos.  

:::image type="complex" source="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png" alt-text="Mantenga el mouse sobre la animación para resaltarla en la ventanilla" lightbox="../media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png":::
   Mantenga el mouse sobre la animación para resaltarla en la ventanilla  
:::image-end:::  

La sección más izquierda y más oscura de una animación es la definición.  La sección derecha más atenuada representa iteraciones.  Por ejemplo, en la siguiente figura, las secciones dos y tres representan iteraciones de la sección uno.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations-highlight.msft.png" alt-text="Diagrama de iteraciones de animación" lightbox="../media/inspect-styles-glitch-display-animations-highlight.msft.png":::
   Diagrama de iteraciones de animación  
:::image-end:::  

Si se aplica la misma animación a dos elementos, el Inspector de animación asigna el mismo color a los elementos.  El color es aleatorio y no tiene importancia.  Por ejemplo, en la siguiente figura, los dos elementos y tienen la misma animación `div.cwccw.earlier` `div.cwccw.later` \( `spinrightleft` \) aplicada, al igual que los elementos `div.ccwcw.earlier` `div.ccwcw.later` and.  

:::image type="complex" source="../media/inspect-styles-glitch-display-animations.msft.png" alt-text="Animaciones codificadas por colores" lightbox="../media/inspect-styles-glitch-display-animations.msft.png":::
   Animaciones codificadas por colores  
:::image-end:::  

## <a name="modify-animations"></a>Modificar animaciones  

Hay tres formas de modificar una animación con el Inspector de animación.  

*   Duración de animación.  
*   Intervalos de fotogramas clave.  
*   Retraso de tiempo de inicio.  
    
En la siguiente figura, se representa la animación original.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png" alt-text="Animación original antes de la modificación" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations.msft.png":::
   Animación original antes de la modificación  
:::image-end:::  

Para cambiar la duración de una animación, elija y arrastre el primer o último círculo.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png" alt-text="Duración modificada" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png":::
   Duración modificada  
:::image-end:::  

Si la animación define alguna regla de fotograma clave, estas se representan como círculos interiores blancos.  Elija y arrastre uno de estos para cambiar el tiempo del fotograma clave.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png" alt-text="Fotograma clave modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png":::
   Fotograma clave modificado  
:::image-end:::  

Para agregar un retraso a una animación, elige y arrástrala en cualquier lugar excepto en los círculos.  

:::image type="complex" source="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png" alt-text="Retraso modificado" lightbox="../media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png":::
   Retraso modificado  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
