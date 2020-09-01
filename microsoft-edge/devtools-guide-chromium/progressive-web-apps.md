---
title: Depurar aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 6733d7823348bc02dd6f29ec218a33ab4073dbfc
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984972"
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





# Depurar aplicaciones web progresivas   



Use el panel de **aplicaciones** para inspeccionar, modificar y depurar manifiestos de aplicaciones Web, trabajos de servicios y cachés de trabajos de servicios.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

Esta guía solo trata las características de la aplicación web progresiva del panel de la **aplicación** .  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### Resumen  

*   Use el panel **manifiesto** para inspeccionar el manifiesto de la aplicación web y desencadenar agregar a eventos de pantalla Android.  
*   Use el panel de **trabajos de servicio** para toda la gama de tareas relacionadas con los trabajos de los trabajadores, como la anulación del registro o la actualización de un servicio, la emulación de eventos de inserción, la desconexión o la detención de un trabajador de servicio.  
*   Vea la caché de trabajos del servicio en el panel **almacenamiento en caché** .  
*   Anula el registro de un trabajador del servicio y borra todo el almacenamiento y las memorias caché con un solo clic del botón en el panel **Borrar almacenamiento** .  
    
## Manifiesto de la aplicación Web   

Si quiere que los usuarios puedan agregar la aplicación a su homescreens móvil, necesita un manifiesto de la aplicación Web.  El manifiesto define cómo aparece la aplicación en la pantalla Android, dónde dirigir al usuario cuando se inicia desde pantalla Android y qué aspecto tiene la aplicación al iniciar.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

Una vez que tenga configurado el manifiesto, puede usar el panel de **manifiesto** del panel de **aplicaciones** para inspeccionarlo.  

:::image type="complex" source="./media/manifest-pane.msft.png" alt-text="El panel manifiesto" lightbox="./media/manifest-pane.msft.png":::
   El panel **manifiesto**  
:::image-end:::  

*   Para ver el origen del manifiesto, haga clic en el vínculo debajo de la etiqueta de manifiesto de la **aplicación** \ ( `https://airhorner.com/manifest.json` en la figura anterior \).  
<!-- *   Press the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   Las secciones **identidad** y **presentación** solo muestran campos del origen del manifiesto en una pantalla más fácil de usar.  
*   En la sección **iconos** se muestran todos los iconos que especificó.  
    
<!--### Simulate Add to Homescreen events   -->

<!--A web app can only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, this criteria can be inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You can test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Clicking on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="./media/io.msft.png" alt-text="Add to desktop shelf" lightbox="./media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature cannot yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you can successfully add your app to your desktop shelf, then it'll work for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you can connect a real mobile device to DevTools via **remote debugging**, and then click the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## Trabajadores de servicio   

Los trabajadores de servicios son una tecnología fundamental en la plataforma web futura.  Son scripts que el explorador ejecuta en segundo plano, independientes de una página web.  Estas secuencias de comandos le permiten acceder a las características que no necesitan una página web o interacción del usuario, como las notificaciones de inserción, la sincronización en segundo plano y las experiencias sin conexión.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

El panel de **trabajos de servicios** del panel de **aplicaciones** es el lugar principal en el DevTools para inspeccionar y depurar trabajos de servicio.  

:::image type="complex" source="./media/service-workers-pane.msft.png" alt-text="El panel de trabajos de servicios" lightbox="./media/service-workers-pane.msft.png":::
   El panel de **trabajos de servicios**  
:::image-end:::  

*   Si un trabajador de servicio está instalado en la página abierta actualmente, aparecerá en este panel.  Por ejemplo, en la ilustración anterior, hay un trabajo de servicio instalado para el ámbito de `https://weather-pwa-sample.firebaseapp.com` .  
*   La casilla de verificación **sin conexión** pone DevTools al modo sin conexión.  Es equivalente al modo sin conexión disponible en el panel **red** o a la `Go offline` opción en el [menú de comandos][DevtoolsCommandMenuIndex].  
*   La casilla **actualizar al volver a cargar** fuerza al trabajador del servicio a actualizar en todas las cargas de páginas.  
*   La casilla **omitir para red** evita el trabajo de servicio y obliga al explorador a ir a la red para obtener los recursos solicitados.  
*   El botón **Actualizar** realiza una actualización única del trabajo de servicio especificado.  
*   El botón de **comando** emula una notificación de inserción sin una carga \ (también conocida como **Tickle**\).  
*   El botón de **sincronización** emula un evento de sincronización en segundo plano.  
*   El botón **anular registro** anula el registro del trabajo de servicio especificado.  Consulte [Borrar almacenamiento](#clear-storage) para una forma de anular el registro de un trabajador de servicio y de borrar almacenamiento y memorias caché con un solo clic de botón.  
*   La línea de **origen** le indica cuándo se instaló el trabajo de servicio actualmente en ejecución.  El vínculo es el nombre del archivo de origen del trabajador del servicio.  Al hacer clic en el vínculo, se le envía a la fuente del trabajador del servicio.  
*   La línea de **Estado** indica el estado del trabajador de servicio.  El número de identificación situado junto al indicador de estado verde \ ( `#36` en la figura anterior \) es para el trabajador de servicios actualmente activo.  Junto al estado verás un botón **iniciar** \ (si el trabajo de servicio está detenido \) o un botón **detener** \ (si el trabajo de servicio se está ejecutando \).  Los trabajadores de servicios están diseñados para que el navegador los detenga y los inicie en cualquier momento.  Detener explícitamente el trabajo del servicio con el botón **detener** puede simularlo.  Detener el trabajo del servicio es una excelente forma de comprobar cómo se comporta el código cuando vuelve a iniciarse el trabajo del servicio.  Con frecuencia, revela errores a causa de suposiciones defectuosas sobre el estado global persistente.  
*   La línea **clientes** le indica el origen al que el trabajador de servicio está en el ámbito.  El botón **foco** es principalmente útil cuando se ha habilitado la casilla **Mostrar todo** .  Cuando esta casilla esté habilitada, todos los trabajos de servicio registrados aparecerán en la lista.  Si hace clic en el botón **foco** junto a un trabajador de servicio que se está ejecutando en una pestaña diferente, Microsoft Edge se centra en esa pestaña.  
    
Si el trabajo de servicio provoca errores, aparece una nueva etiqueta denominada **errores** .  

<!--  
:::image type="complex" source="./media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="./media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## Cachés de trabajos del servicio 

El panel **almacenamiento en caché** proporciona una lista de solo lectura de los recursos que se han almacenado en caché con la [API de caché][MDNWebCacheAPI]\ (trabajo de servicio \).  

:::image type="complex" source="./media/cache-pane-cache-storage-resources.msft.png" alt-text="Panel almacenamiento en caché" lightbox="./media/cache-pane-cache-storage-resources.msft.png":::
   Panel **almacenamiento en caché**  
:::image-end:::  

> [!NOTE]
> La primera vez que abre una caché y le agrega un recurso, es posible que DevTools no detecte el cambio.  Vuelva a cargar la página y verá la memoria caché.  

Si tiene dos o más memorias caché abiertas, las verá debajo de la lista desplegable **almacenamiento en caché** .  

:::image type="complex" source="./media/cache-pane-cache-storage.msft.png" alt-text="Lista desplegable de almacenamiento en caché" lightbox="./media/cache-pane-cache-storage.msft.png":::
   Lista desplegable de **almacenamiento en caché**  
:::image-end:::  

## Uso de cuotas 

Es posible que algunas respuestas dentro del panel **almacenamiento en caché** se marquen como "opacas".  Se refiere a una respuesta recuperada de un origen diferente, como en una **CDN** o una API remota, cuando [CORS][FetchHttpCorsProtocol] no está habilitado.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Para evitar la pérdida de información entre dominios, se agrega un relleno significativo al tamaño de una respuesta opaca que se usa para calcular los límites de la cuota de almacenamiento \ (por ejemplo, si `QuotaExceeded` se inicia una excepción \) y la API informa de ello `navigator.storage` .  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Los detalles de este relleno varían según el explorador y el explorador, pero en Microsoft Edge, esto significa que el **tamaño mínimo** de una sola respuesta opaca en caché contribuye al uso general de almacenamiento es de [aproximadamente 7 megabytes][ChromiumIssues796060#c17].  Debe tener esto en cuenta al determinar cuántas respuestas opacas desea almacenar en caché, ya que es posible que pueda haber superado fácilmente las limitaciones de la cuota de almacenamiento, muy pronto como cabría esperar, en función del tamaño real de los recursos opacos.  

Guías relacionadas:  

*   [Desbordamiento de la pila: ¿Qué limitaciones se aplican a las respuestas opacas?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## Borrar almacenamiento 

El panel **Borrar almacenamiento** es una característica muy útil al desarrollar aplicaciones web progresivas.  Este panel le permite anular el registro de los trabajadores de los servicios y borrar todas las cachés y almacenamiento con un solo clic de botón.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides 

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
<!--TODO  -->

<!--  
 


-->  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ./command-menu/index.md "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools | Microsoft docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Cromo problema 796060: el valor de almacenamiento en caché aumenta en cada actualización cuando el código de análisis está en HTML"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Caché-API Web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Desbordamiento de la pila: ¿Qué limitaciones se aplican a las respuestas opacas?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
