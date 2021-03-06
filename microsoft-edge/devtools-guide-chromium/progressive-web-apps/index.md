---
description: Use el panel Aplicación para inspeccionar, modificar y depurar manifiestos de aplicaciones web, trabajadores de servicio y cachés de trabajadores de servicio.
title: Depurar aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: aea01d25474a030e78ac0eaeaef3954ab7f4539f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398542"
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

# <a name="debug-progressive-web-apps"></a>Depurar aplicaciones web progresivas  

Use el panel **Aplicación** para inspeccionar, modificar y depurar manifiestos de aplicaciones web, trabajadores de servicio y cachés de trabajadores de servicio.  

<!--Related Guides:  

*   [Progressive Web Apps](/web/progressive-web-apps)  -->

<!--TODO:  Link web "Progressive Web Apps" section when available. -->

Esta guía solo analiza las características de La aplicación web progresiva **del** panel Aplicación.  <!--If you're looking for help on the other panes, check out the last section of this guide, [Other Application panel guides](#other-application-panel-guides).  -->

<!--TODO:  Link to sections when available. -->

### <a name="summary"></a>Resumen  

*   Usa el **panel Manifiesto** para inspeccionar el manifiesto de la aplicación web y desencadenar los eventos Agregar a pantalla principal.  
*   Use el panel **Trabajadores** de servicio para toda una gama de tareas relacionadas con el trabajo de servicio, como anular el registro o actualizar un servicio, emular eventos de inserción, desconectarse o detener a un trabajador de servicio.  
*   Vea la memoria caché del trabajador de servicio desde el **panel Almacenamiento de caché.**  
*   Anula el registro de un trabajador de servicio y borra todo el almacenamiento y las memorias caché con un solo botón elige en el **panel Borrar** almacenamiento.  
    
## <a name="web-app-manifest"></a>Manifiesto de aplicación web  

Si quieres que los usuarios puedan agregar la aplicación a sus pantallas de inicio móviles, necesitas un manifiesto de aplicación web.  El manifiesto define cómo aparece la aplicación en la pantalla principal, dónde dirigir al usuario al iniciarse desde la pantalla principal y cómo es la aplicación al iniciarla.  

<!--Related Guides:  

*   [Improve user experiences with a Web App Manifest](/web/fundamentals/web-app-manifest)  
*   [Using App Install Banners](/web/fundamentals/app-install-banners)  -->

<!--TODO:  Link to sections when available. -->

Después de configurar el manifiesto, puede usar el **panel Manifiesto** del panel **Aplicación** para inspeccionarlo.  

:::image type="complex" source="../media/manifest-pane.msft.png" alt-text="Panel de manifiesto" lightbox="../media/manifest-pane.msft.png":::
   Panel **de** manifiesto  
:::image-end:::  

*   Para ver el origen del manifiesto, elija el vínculo debajo de la etiqueta **manifiesto** de la aplicación \( `https://airhorner.com/manifest.json` en la figura anterior\).  
<!-- *   Choose the **Add to homescreen** button to simulate an Add to Homescreen event.  Check out the next section for more information.  -->  
*   Las **secciones Identity** y **Presentation** solo muestran campos del origen del manifiesto en una presentación más fácil de usar.  
*   La **sección** Iconos muestra todos los iconos especificados.  
    
<!--### Simulate Add to Homescreen events  -->

<!--A web app may only be added to a homescreen when the site is visited at least twice, with at least five minutes between visits.  While developing or debugging your Add to Homescreen workflow, the criteria is potentially inconvenient.  
The **Add to homescreen** button on the **App Manifest** pane lets you simulate Add to Homescreen events whenever you want.  -->

<!--You may test out this feature with the [Microsoft I/O 2016 progressive web app](https://events.alpahabet.com/io2016/), which has proper support for Add to Homescreen.  Choosing on **Add to Homescreen** while the app is open prompts Microsoft Edge to display the "add this site to your shelf" banner, which is the desktop equivalent of the "add to homescreen" banner for mobile devices.  -->

<!--  
:::image type="complex" source="../media/io.msft.png" alt-text="Add to desktop shelf" lightbox="../media/io.msft.png":::
   Add to desktop shelf  
:::image-end:::
-->  

<!--
> [!Tip]
> Keep the **Console** drawer open while simulating Add to Homescreen events.  The Console tells you if your manifest has any issues and logs other information about the Add to Homescreen lifecycle.  -->

<!--The **Add to Homescreen** feature may not yet simulate the workflow for mobile devices.  Notice how the "add to shelf" prompt was triggered in the screenshot above, even though DevTools is in Device Mode.  However, if you may successfully add your app to your desktop shelf, then it works for mobile, too.  -->

<!-- TODO: Rework content after sample app is created. -->

<!--If you want to test out the genuine mobile experience, you may connect a real mobile device to DevTools via **remote debugging**, and then choose the **Add to Homescreen** button \(on DevTools\) to trigger the "add to homescreen" prompt on the connected mobile device.  -->

<!--TODO:  Link Debug "remote debugging" sections when available. -->

## <a name="service-workers"></a>Trabajadores de servicios  

Los trabajadores de servicio son una tecnología fundamental en la futura plataforma web.  Son scripts que el explorador ejecuta en segundo plano, separados de una página web.  Los scripts permiten tener acceso a características que sin necesidad de una página web o interacción del usuario, como notificaciones de inserción, sincronización en segundo plano y experiencias sin conexión.  

<!--Related Guides:  

*   [Intro to Service Workers](/web/fundamentals/primers/service-worker)  
*   [Push Notifications: Timely, Relevant, and Precise](/web/fundamentals/push-notifications)  -->  
    
<!--TODO:  Link to sections when available. -->  

El **panel Trabajadores de** servicio del panel **Aplicación** es el lugar principal de DevTools para inspeccionar y depurar trabajadores de servicio.  

:::image type="complex" source="../media/service-workers-pane.msft.png" alt-text="Panel Trabajadores de servicio" lightbox="../media/service-workers-pane.msft.png":::
   Panel **Trabajadores de** servicio  
:::image-end:::  

*   Si un trabajador de servicio está instalado en la página abierta actualmente, aparece en este panel.  Por ejemplo, en la figura anterior, hay un trabajador de servicio instalado para el ámbito de `https://weather-pwa-sample.firebaseapp.com` .  
*   La **casilla Sin** conexión pone DevTools en modo sin conexión.  Esto equivale al modo sin conexión disponible en la **herramienta Red** o a la opción del `Go offline` menú [comando][DevtoolsCommandMenuIndex].  
*   La **casilla Actualizar al volver a cargar** fuerza al trabajador del servicio a actualizarse en cada carga de página.  
*   La **casilla Omitir para red** omite al trabajador del servicio y fuerza al explorador a ir a la red en busca de recursos solicitados.  
*   El **botón** Actualizar realiza una actualización única del trabajador de servicio especificado.  
*   El **botón Push** emula una notificación de inserción sin una carga \(también conocida como **tickle**\).  
*   El **botón Sincronizar** emula un evento de sincronización en segundo plano.  
*   El **botón Anular registro** anula el registro del trabajador de servicio especificado.  Consulte [Borrar almacenamiento para](#clear-storage) obtener una forma de anular el registro de un trabajador de servicio y borrar el almacenamiento y las memorias caché con un solo botón.  
*   La **línea Origen** indica cuándo se instaló el trabajador de servicio que se está ejecutando actualmente.  El vínculo es el nombre del archivo de origen del trabajador de servicio.  Al elegir en el vínculo, se envía al origen del trabajador de servicio.  
*   La **línea** Estado indica el estado del trabajador del servicio.  El número de identificador junto al indicador de estado verde \( en la `#36` figura anterior\) es para el trabajador de servicio activo actualmente.  Junto al estado, **** se muestra un botón inicio \(si **** el trabajador de servicio está detenido\) o un botón de detenerse \(si el trabajador de servicio se está ejecutando\).  Los trabajadores de servicio están diseñados para ser detenidos e iniciados por el explorador en cualquier momento.  Detener explícitamente al trabajador del servicio mediante el **botón de** detención puede simularlo.  Detener al trabajador de servicio es una excelente manera de probar cómo se comporta el código cuando el trabajador de servicio vuelve a iniciar la copia de seguridad.  Con frecuencia, se revelan errores debido a suposiciones erróneas sobre el estado global persistente.  
*   La **línea Clientes** indica el origen al que está ámbito el trabajador de servicio.  El **botón** de foco es principalmente útil cuando se ha habilitado la casilla **mostrar todo.**  Cuando esta casilla está habilitada, se enumeran todos los trabajadores de servicio registrados.  Si elige en el botón **de enfoque** junto a un trabajador de servicio que se ejecuta en una pestaña diferente, Microsoft Edge se centra en esa pestaña.  
    
Si el trabajador del servicio provoca algún error, aparece una nueva etiqueta denominada **Errores.**  

<!--  
:::image type="complex" source="../media/sw-error.msft.png" alt-text="Service worker with errors" lightbox="../media/sw-error.msft.png":::
   Service worker with errors  
:::image-end:::
-->  

<!--TODO:  Capture Service Worker Errors sample when available. -->
<!--TODO:  Link Web "How tickle works" sections when available. -->

## <a name="service-worker-caches"></a>Cachés de trabajadores de servicio  

El **panel Almacenamiento de** caché proporciona una lista de solo lectura de los recursos que se han almacenado en caché mediante la [API][MDNWebCacheAPI]de caché \(service worker\) .  

:::image type="complex" source="../media/cache-pane-cache-storage-resources.msft.png" alt-text="Panel de almacenamiento en caché" lightbox="../media/cache-pane-cache-storage-resources.msft.png":::
   Panel **de almacenamiento en caché**  
:::image-end:::  

> [!NOTE]
> La primera vez que abra una memoria caché y le agregue un recurso, Es posible que DevTools no detecte el cambio.  Actualice la página y muestre la memoria caché.  

Si tiene dos o más cachés abiertas, las cachés se muestran en el siguiente desplegable **Almacenamiento de caché.**  

:::image type="complex" source="../media/cache-pane-cache-storage.msft.png" alt-text="Desplegable Almacenamiento en caché" lightbox="../media/cache-pane-cache-storage.msft.png":::
   Desplegable **Almacenamiento en caché**  
:::image-end:::  

## <a name="quota-usage"></a>Uso de cuota  

Algunas respuestas dentro del panel **Almacenamiento de** caché pueden estar marcadas como "opacas".  Esto hace referencia a una respuesta recuperada de un origen diferente, como de una **RED CDN** o API remota, cuando [CORS][FetchHttpCorsProtocol] no está habilitado.  

<!--TODO:  Link Web "CDN" section when available. -->  
<!--TODO:  Link Web "opaque" section when available. -->

Para evitar la pérdida de información entre dominios, se agrega un relleno significativo al tamaño de una respuesta opaca usada para calcular los límites de cuota de almacenamiento \(por ejemplo, si se produce una excepción\) y se notifica mediante la `QuotaExceeded` `navigator.storage` API.  

<!--TODO:  Link Estimating "`navigator.storage` API" sections when available. -->

Los detalles de este relleno varían de un explorador a **** otro, pero para Microsoft Edge, esto significa que el tamaño mínimo que cualquier respuesta opaca almacenada en caché contribuye al uso general de almacenamiento es de aproximadamente [7 megabytes][ChromiumIssues796060#c17].  Recuerde el relleno al determinar cuántas respuestas opacas desea almacenar en caché, ya que puede superar fácilmente las limitaciones de cuota de almacenamiento mucho antes de lo que espera en función del tamaño real de los recursos opacos.  

Guías relacionadas:  

*   [Desbordamiento de pila: ¿qué limitaciones se aplican a las respuestas opacas?][StackOverflowLimitationsForOpaqueResponses]  
<!--*   [Alphabet work container: Understanding Storage Quota](/web/tools/Alphabet-work-container/guides/storage-quota#beware_of_opaque_responses)  -->
    
<!--TODO:  Link Work container storage quota for opaque responses section when available. -->

## <a name="clear-storage"></a>Borrar almacenamiento  

El **panel Borrar almacenamiento** es una característica muy útil al desarrollar aplicaciones web progresivas.  Este panel permite anular el registro de los trabajadores del servicio y borrar todas las cachés y el almacenamiento con un solo botón.  <!--Check out the section below to learn more.  -->

<!--Related Guides:  

*   [Clear Storage](/iterate/manage-data/local-storage#clear-storage)  -->
    
<!--TODO:  Link to sections when available. -->

<!--## Other Application panel guides   

Check out the guides below for more help on the other panes of the **Application** panel.  

Related Guides:  

*   [Inspect page resources](/iterate/manage-data/page-resources)  
*   [Inspect and manage local storage and caches](/iterate/manage-data/local-storage)  -->
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsCommandMenuIndex]: ../command-menu/index.md "Ejecutar comandos con el menú de comandos DevTools de Microsoft Edge | Microsoft Docs"  

[ChromiumIssues796060#c17]: https://bugs.chromium.org/p/chromium/issues/detail?id=796060#c17 "Chromium Issue 796060: El valor de almacenamiento en caché aumenta en cada actualización cuando el código de Analytics está en el html"  

[FetchHttpCorsProtocol]: https://fetch.spec.whatwg.org/#http-cors-protocol  

[MDNWebCacheAPI]: https://developer.mozilla.org/docs/Web/API/Cache "Caché: API web | MDN"  

[StackOverflowLimitationsForOpaqueResponses]: https://stackoverflow.com/q/39109789/385997 "Desbordamiento de pila: ¿qué limitaciones se aplican a las respuestas opacas?"  

<!--[WebEstimatingAvailableStorageSpace]: whats-new/2017/08/estimating-available-storage-space  -->
<!--[RemoteDebugging]: /debug/remote-debugging/remote-debugging  -->

<!--[WebHowPushWorks]: /web/fundamentals/push-notifications/how-push-works  -->  
<!--[WebGlossaryCDN]: /web/fundamentals/glossary#CDN  -->
<!--[WebGlossaryOpaque]: /web/fundamentals/glossary#opaque-response  -->

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/progressive-web-apps) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
