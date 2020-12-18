---
description: Use el panel multimedia para ver información y depurar los reproductores multimedia por pestaña del explorador.
title: Ver y depurar información de los reproductores multimedia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: e6259cf573b76df7e281527ad30360b8f473a165
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230953"
---
# Ver y depurar información de los reproductores multimedia  

Use el panel **multimedia** en Microsoft Edge DevTools para ver información y depurar los reproductores multimedia por pestaña del explorador.  

## Abrir el panel multimedia  

El panel **multimedia** es el lugar principal en DevTools para inspeccionar el reproductor multimedia de una página web.

1.  [Abra DevTools][DevtoolsGuideChromiumOpen].  
1.  Para abrir el panel **multimedia** , elija **personalizar y controle DevTools** `...`  >  **más herramientas**  >  **multimedia**.  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Panel multimedia" lightbox="../media/media-panel-empty.msft.png":::
       Panel **multimedia**  
    :::image-end:::  
    
## Ver información de los reproductores multimedia  

1.  Vaya a una página web con un reproductor multimedia, como la siguiente página web.  
    
    [Maximizar la productividad con las herramientas para desarrolladores perimetrales][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  En el menú **Players** , se muestra un reproductor de medios.  
1.  Seleccione el reproductor.  La pestaña **propiedades** muestra las propiedades del reproductor multimedia.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propiedades de elementos multimedia" lightbox="../media/media-panel-view.msft.png":::
       Propiedades de elementos multimedia  
    :::image-end:::  
    
1.  Para ver todos los eventos del reproductor multimedia, elija la pestaña **eventos** .  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Eventos multimedia" lightbox="../media/media-panel-events.msft.png":::
       Eventos multimedia  
    :::image-end:::  
    
1.  Para ver los registros de mensajes del reproductor multimedia, elija la pestaña **mensajes** .  Puede filtrar los mensajes por nivel de registro o cadena.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Mensajes multimedia" lightbox="../media/media-panel-messages.msft.png":::
       Mensajes multimedia  
    :::image-end:::  
    
1.  En la pestaña **escala de tiempo** , la reproducción multimedia y el estado del búfer se muestran en vivo.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Escala de tiempo multimedia" lightbox="../media/media-panel-timeline.msft.png":::
       Escala de tiempo multimedia  
    :::image-end:::  
    
### Depuración remota  

Ver la información de los reproductores multimedia en un dispositivo Android desde un equipo Windows o macOS.  

1.  Para configurar la depuración remota, vaya a introducción a la [depuración remota de dispositivos Android][DevtoolsGuideChromiumRemoteDebuggingIndex].  
1.  Ver la información de los reproductores multimedia de forma remota.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## Ocultar y mostrar reproductores multimedia  

A veces ejecuta más de un reproductor multimedia en una página web o usa la misma pestaña de explorador para examinar diferentes páginas web, cada una con reproductores multimedia.

Puede ocultar \ (o mostrar \) cada reproductor multimedia para una experiencia de depuración más sencilla.  

1.  Vaya a varias páginas web de vídeo diferentes usando la misma pestaña del explorador.  
1.  Para ocultar reproductores multimedia, lleve a cabo una de las siguientes acciones.  
    *   Para ocultar un reproductor multimedia, desplace el puntero sobre un reproductor multimedia, abra el menú contextual \ (haga clic con el botón derecho \) y elija **ocultar reproductor**.  
    *   Para ocultar todos los demás reproductores multimedia, desplace el puntero sobre un reproductor multimedia y abra el menú contextual \ (haga clic con el botón derecho \) y elija **ocultar todos los demás**.  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ocultar reproductores multimedia" lightbox="../media/media-panel-hide-show.msft.png":::
       Ocultar reproductores multimedia  
    :::image-end:::  
    
## Exportar información de reproductor multimedia  

1.  Para descargar la información del reproductor multimedia como un archivo JSON, desplace el puntero sobre un reproductor multimedia y abra el menú contextual \ (haga clic con el botón derecho \) y elija **Guardar información del reproductor**.  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportar información multimedia" lightbox="../media/media-panel-save.msft.png":::
       Exportar información multimedia  
    :::image-end:::  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abrir Microsoft Edge (cromo) DevTools | Microsoft docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Introducción a la depuración remota dispositivos Android | Microsoft docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximizar la productividad con las herramientas para desarrolladores de Edge | Vídeo de Bing"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  

