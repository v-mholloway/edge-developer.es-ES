---
title: Ver recursos de página con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611920"
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





# Ver recursos de página con Microsoft Edge DevTools   

  

Esta guía le enseña cómo usar Microsoft Edge DevTools para ver los recursos de una página web.  Los recursos son los archivos que necesita una página para que se muestren correctamente.  Algunos ejemplos de recursos son los archivos CSS, JavaScript y HTML, así como las imágenes.  

En esta guía se presupone que está familiarizado con los conceptos básicos de [desarrollo web][MDNLearnWebDevelopment] y [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Abrir recursos   

Cuando conoce el nombre del recurso que quiere inspeccionar, el **menú de comandos** proporciona una forma rápida de abrir el recurso.  

1.  Pulse `Control` + `P` \ (Windows \) o `Command` + `P` \ (MacOS \).  Se abrirá el cuadro de diálogo **Abrir archivo** .  
    
    > ##### Figura 1  
    > Cuadro de diálogo **Abrir archivo**  
    > ![Cuadro de diálogo Abrir archivo][ImageOpenFile]  
    
1.  Seleccione el archivo de la lista desplegable o empiece a escribir el nombre de archivo y presione `Enter` una vez que el archivo correcto esté resaltado en el cuadro Autocompletar.  
    
    > ##### Figura 2  
    > Escribir un nombre de archivo en el cuadro de diálogo **Abrir archivo**  
    > ![Escribir un nombre de archivo en el cuadro de diálogo Abrir archivo][ImageFileSearch]  
    
### Abrir recursos en el panel red   

Consulte [inspeccionar los detalles de un recurso][DevtoolsNetworkInspectDetailsResource].  

> ##### Imagen 3  
> Inspeccionar un recurso en el panel red  
> ![Inspeccionar un recurso en el panel red][ImageNetworkResponse]  

### Mostrar recursos en el panel de red de otros paneles   

En la sección [examinar recursos](#browse-resources) que se muestra a continuación se muestra cómo ver los recursos de varias partes de la interfaz de usuario de DevTools.  Si alguna vez desea inspeccionar un recurso en el panel **red** , haga clic con el botón derecho en el recurso y seleccione **Mostrar en el panel de red**.  

> ##### Imagen 4  
> Opción **Mostrar en el panel red**  
> ![Mostrar en el panel red][ImageRevealNetwork]  

## Examinar recursos   

### Examinar recursos en el panel red   

Consulte [Registrar actividad de red][DevtoolsNetworkLogActivity].  

> ##### Imagen 5  
> Recursos de página en el registro de red  
> ![Recursos de página en el registro de red][ImageNetworkLog]  

### Examinar por directorio   

Para ver los recursos de una página organizada por directorio:  

1.  Haga clic en la pestaña **orígenes** para abrir el panel **fuentes** .  
1.  Haga clic en la pestaña de la **Página** para mostrar los recursos de la página.  Se abre el panel de **páginas** .  
    
    > ##### Imagen 6  
    > El panel de **páginas**  
    > ![El panel de páginas][ImagePage]  
    
    A continuación se muestra un desglose de los elementos no obvios de la [Ilustración 6](#figure-6):  
    
    | Elemento de página | Descripción |  
    |:--- |:--- |  
    | `top` | [Contexto de examen][MDNInlineFrame]de documento principal. |  
    | `airhorner.com` | El dominio.  Todos los recursos anidados en él provienen de ese dominio.  Por ejemplo, la dirección URL completa del `comlink.global.j` archivo es probablemente `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Un directorio. |  
    | `(index)` | Documento HTML principal. |  
    | `sw.js` | Contexto en tiempo de ejecución de un trabajo de servicio. |  
    
1.  Haga clic en un recurso para verlo en el **Editor**.  
    
    > ##### Imagen 7  
    > Ver un archivo en el **Editor**  
    > ![Ver un archivo en el editor][ImageSourcesView]  
    
### Examinar por nombre de archivo   

De forma predeterminada, el panel de **páginas** agrupa los recursos por directorio.  Para deshabilitar esta agrupación y ver los recursos de cada dominio como una lista plana:  

1.  Abra el panel de **páginas** .  Consulte [examinar por directorio](#browse-by-directory).  
1.  Haga clic en **más opciones** `...` y deshabilite **Agrupar por carpeta**.  
    
    > ##### Imagen 8  
    > La opción **Agrupar por carpeta**  
    > ![La opción agrupar por carpeta][ImageGroupByFolder]  
    
    Los recursos están organizados por tipo de archivo.  Dentro de cada tipo de archivo, los recursos están organizados alfabéticamente.  
    
    > ##### Imagen 9  
    > El panel de **páginas** después de deshabilitar **Agrupar por carpeta**  
    > ![El panel de páginas después de deshabilitar agrupar por carpeta][ImageFileNames]  
    
### Examinar por tipo de archivo   

Para agrupar recursos en función de su tipo de archivo:  

1.  Haga clic en la pestaña **aplicación** .  Se abre el panel de la **aplicación** .  De forma predeterminada, el panel **manifiesto** generalmente se abre en primer lugar.  
    
    > ##### Imagen 10  
    > El panel de **aplicaciones**  
    > ![El panel de aplicaciones][ImageApplication]  
    
1.  Desplácese hacia abajo hasta el panel **Marcos** .  
    
    > ##### Imagen 11  
    > El panel **Marcos**  
    > ![El panel marcos][ImageFrames]  
    
1.  Expanda las secciones en las que esté interesado.  
1.  Haga clic en un recurso para verlo.  
    
    > ##### Imagen 12  
    > Ver un recurso en el panel de la **aplicación**  
    > ![Ver un recurso en el panel de la aplicación][ImageApplicationView]  

#### Examinar archivos por tipo en el panel red   

Consulte [filtrar por tipo de recurso][DevtoolsNetworkFilterByResourceType].  

> ##### Imagen 13  
> Filtrar por CSS en el registro de red  
> ![Filtrar por CSS en el registro de red][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Ilustración 1: el cuadro de diálogo Abrir archivo"  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Ilustración 2: escribir un nombre de archivo en el cuadro de diálogo Abrir archivo"  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Ilustración 3: inspección de un recurso en el panel * * red * *"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Ilustración 4: Mostrar en el panel red"  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Ilustración 5: recursos de página en el registro de red"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Ilustración 6: el panel de páginas"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Ilustración 7: visualización de un archivo en el editor"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Ilustración 8: opción Group by Folder"  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Ilustración 9: el panel de páginas después de deshabilitar agrupar por carpeta"  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Ilustración 10: el panel de la aplicación"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Ilustración 11: el panel marcos"  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Ilustración 12: visualización de un recurso en el panel de aplicaciones"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Ilustración 13: filtrar por CSS en el registro de red"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Herramientas para desarrolladores de Microsoft Edge (cromo)"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Filtrar por tipo de recurso-comprobar actividad de red en Microsoft Edge DevTools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Comprobar los detalles de la actividad de red inspeccionar recursos en Microsoft Edge DevTools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Registrar actividad de red: inspeccionar actividad de red en Microsoft Edge DevTools"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> iframe: el elemento marco alineado | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Aprenda el desarrollo web | MDN"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/resources/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
