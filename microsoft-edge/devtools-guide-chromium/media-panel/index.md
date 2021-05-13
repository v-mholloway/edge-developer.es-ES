---
description: Usa la herramienta Multimedia para ver información y depurar los reproductores multimedia por pestaña del explorador.
title: Ver y depurar información de reproductores multimedia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0d2a60c31d5239a4b47102ae96a713b8bfcf46f3
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564066"
---
<!-- Copyright Jecelyn Yeen

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="view-and-debug-media-players-information"></a>Ver y depurar información de reproductores multimedia  

Use la **herramienta Multimedia** en Microsoft Edge DevTools para ver información y depurar los reproductores multimedia por pestaña del explorador.  

## <a name="open-the-media-tool"></a>Abrir la herramienta Multimedia  

La **herramienta** Multimedia es el lugar principal en DevTools para inspeccionar el reproductor multimedia de una página web.

1.  [Abra DevTools][DevtoolsGuideChromiumOpen].  
1.  Para abrir el panel **Multimedia,** elija **Personalizar y controlar DevTools** `...`  >  **Más herramientas**  >  **Multimedia**.  
    
    :::image type="complex" source="../media/media-panel-empty.msft.png" alt-text="Panel multimedia" lightbox="../media/media-panel-empty.msft.png":::
       **Panel multimedia**  
    :::image-end:::  
    
## <a name="view-media-players-information"></a>Ver información de reproductores multimedia  

1.  Navegue a una página web con un reproductor multimedia, como la siguiente página web.  
    
    [Maximizar la productividad con edge Developer Tools][BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]  
    
1.  En el **menú Reproductores,** se muestra un reproductor multimedia.  
1.  Elige el jugador.  El **panel** Propiedades muestra las propiedades del reproductor multimedia.  
    
    :::image type="complex" source="../media/media-panel-view.msft.png" alt-text="Propiedades multimedia" lightbox="../media/media-panel-view.msft.png":::
       Propiedades multimedia  
    :::image-end:::  
    
1.  Para ver todos los eventos del reproductor multimedia, elija el panel **Eventos.**  
    
    :::image type="complex" source="../media/media-panel-events.msft.png" alt-text="Eventos multimedia" lightbox="../media/media-panel-events.msft.png":::
       Eventos multimedia  
    :::image-end:::  
    
1.  Para ver los registros de mensajes del reproductor multimedia, elija **el** panel Mensajes.  Puede filtrar los mensajes por nivel de registro o cadena.  
    
    :::image type="complex" source="../media/media-panel-messages.msft.png" alt-text="Mensajes multimedia" lightbox="../media/media-panel-messages.msft.png":::
       Mensajes multimedia  
    :::image-end:::  
    
1.  En el panel **Escala de** tiempo, la reproducción multimedia y el estado del búfer se muestran en directo.  
    
    :::image type="complex" source="../media/media-panel-timeline.msft.png" alt-text="Escala de tiempo de medios" lightbox="../media/media-panel-timeline.msft.png":::
       Escala de tiempo de medios  
    :::image-end:::  
    
### <a name="remote-debugging"></a>Depuración remota  

Consulta la información de reproductores multimedia en un dispositivo Android desde tu equipo Windows o macOS.  

1.  Para configurar la depuración remota, vaya a [Introducción a la depuración remota de dispositivos Android.][DevtoolsGuideChromiumRemoteDebuggingIndex]  
1.  Ver la información de reproductores multimedia de forma remota.  
    
    <!-- TODO: recreate image using an Android device -->  
    <!--  
    :::image type="complex" source="../media/media-panel-remote-debug.msft.png" alt-text="Remote debugging" lightbox="../media/media-panel-remote-debug.msft.png":::
       Remote debugging  
    :::image-end:::  
    -->  
    
## <a name="hide-and-show-media-players"></a>Ocultar y mostrar reproductores multimedia  

A veces, ejecutas más de un reproductor multimedia en una página web o usas la misma pestaña del explorador para explorar diferentes páginas web, cada una con reproductores multimedia.

Puede elegir ocultar \(o mostrar\) cada reproductor multimedia para una experiencia de depuración más sencilla.  

1.  Vaya a varias páginas web de vídeo diferentes con la misma pestaña del explorador.  
1.  Para ocultar reproductores multimedia, complete una de las siguientes acciones.  
    *   Para ocultar un reproductor multimedia, mantenga el mouse en un reproductor multimedia, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Ocultar reproductor**.  
    *   Para ocultar todos los demás reproductores multimedia, mantenga el mouse en un reproductor multimedia, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Ocultar todos los demás**.  
    
    :::image type="complex" source="../media/media-panel-hide-show.msft.png" alt-text="Ocultar reproductores multimedia" lightbox="../media/media-panel-hide-show.msft.png":::
       Ocultar reproductores multimedia  
    :::image-end:::  
    
## <a name="export-media-player-information"></a>Exportar información del reproductor multimedia  

1.  Para descargar la información del reproductor multimedia como un archivo JSON, mantenga el mouse en un reproductor multimedia, abra el menú contextual \(clic con el botón secundario\) y elija **Guardar información del reproductor**.  
    
    :::image type="complex" source="../media/media-panel-save.msft.png" alt-text="Exportar información multimedia" lightbox="../media/media-panel-save.msft.png":::
       Exportar información multimedia  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Abra Microsoft Edge (Chromium) DevTools | Microsoft Docs"  

[DevtoolsGuideChromiumRemoteDebuggingIndex]: ../remote-debugging/index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  

[BingVideosSearchViewDetailMidE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8]: https://www.bing.com/videos/search?view=detail&mid=DE0BA14EC0E0D18C06C8DE0BA14EC0E0D18C06C8 "Maximización de la productividad con las herramientas para desarrolladores perimetrales | Bing Vídeo"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/media-panel/index) y está creada por [Jecelyn Yeen][JecelynYeen] \(Promotor de desarrollo, Chrome DevTools\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors#jecelyn-yeen  

