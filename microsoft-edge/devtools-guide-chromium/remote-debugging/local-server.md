---
description: Hospede un sitio en un servidor Web de equipo de desarrollo y, a continuación, obtenga acceso al contenido desde un dispositivo Android.
title: Acceso a servidores locales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f994092460f090743119d7304bfe12aa28556b19
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125415"
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

# Acceso a servidores locales  

Hospede un sitio en un servidor Web de equipo de desarrollo y, a continuación, obtenga acceso al contenido desde un dispositivo Android.  

Con un cable USB y Microsoft Edge DevTools, ejecute un sitio desde un equipo de desarrollo y, después, vea el sitio en un dispositivo Android.  

### Resumen  

*   El reenvío de puertos le permite ver el contenido hospedado en el servidor Web que se está ejecutando en el equipo de desarrollo de su dispositivo Android.  
*   Si su servidor web está usando un dominio personalizado, configure su dispositivo Android para obtener acceso al contenido de ese dominio con asignación de dominio personalizada.  

## Configurar el reenvío de Puerto  

El reenvío de puertos permite que su dispositivo Android obtenga acceso al contenido que se hospeda en el servidor Web que se ejecuta en el equipo de desarrollo.  El reenvío de puertos funciona creando un puerto TCP de escucha en el dispositivo Android que se asigna a un puerto TCP en el equipo de desarrollo.  El tráfico entre los puertos viaja a través de la conexión USB entre el dispositivo Android y el equipo de desarrollo, de modo que la conexión no depende de la configuración de la red.  

Para habilitar el reenvío de puerto:  

1.  Configure la [depuración remota][RemoteDebuggingGettingStarted] entre el equipo de desarrollo y el dispositivo Android.  Cuando haya terminado, debe ver el dispositivo Android en el menú de la izquierda del cuadro de diálogo **inspeccionar dispositivos** y un indicador de estado **conectado** .  
1.  En el cuadro de diálogo **inspeccionar dispositivos** de DevTools, habilite el **reenvío de Puerto**.  
1.  Elija **Agregar regla**.  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Agregar una regla de reenvío de Puerto" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       Agregar una regla de reenvío de Puerto  
    :::image-end:::  
    
1.  En el cuadro de texto **Puerto de dispositivo** de la izquierda, escriba el `localhost` número de puerto desde el que desea poder obtener acceso al sitio en su dispositivo Android.  Por ejemplo, si desea obtener acceso al sitio desde `localhost:5000` entrar `5000` .  
1.  En el cuadro de texto **dirección local** de la derecha, escriba la dirección IP o el nombre de host en el que su sitio está hospedado en el servidor Web que se ejecuta en el equipo de desarrollo, seguido del número de puerto.  Por ejemplo, si su sitio se ejecuta en `localhost:7331` entrar `localhost:7331` .  
1.  Elija **Agregar**.  
    
El reenvío de puertos ya está configurado.  En el cuadro de diálogo **inspeccionar dispositivos** , vea el indicador de estado para el puerto hacia adelante en la ficha de su dispositivo.  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Agregar una regla de reenvío de Puerto" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   Estado de reenvío de Puerto  
:::image-end:::  

Para ver el contenido, abra Microsoft Edge en su dispositivo Android y vaya al `localhost` Puerto que especificó en el campo **Puerto del dispositivo** .  Por ejemplo, si escribió `5000` en el campo, visite `localhost:5000` .  

## Asignar a dominios locales personalizados  

La asignación de dominios personalizada le permite ver el contenido en un dispositivo Android desde un servidor Web en el equipo de desarrollo que usa un dominio personalizado.  

Por ejemplo, supongamos que su sitio usa una biblioteca de JavaScript de terceros que solo funciona en el dominio `microsoft-edge.devtools` .  Por lo tanto, puede crear una entrada en el `hosts` archivo en el equipo de desarrollo para asignar este dominio a `localhost` \ (por ejemplo, `127.0.0.1 microsoft-edge.devtools` \).  Después de configurar la asignación de dominios y el reenvío de puertos personalizados, vea el sitio en su dispositivo Android en la dirección URL `microsoft-edge.devtools` .  

### Configurar el desvío de puertos para el servidor proxy  

Para asignar un dominio personalizado, debe ejecutar un servidor proxy en el equipo de desarrollo.  Ejemplos de servidores proxy son [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]y [Fiddler][FiddlerWebDebuggingProxy].  

Para configurar el reenvío de puertos a un proxy:  

1.  Ejecute el servidor proxy y grabe el puerto que está usando.  
    
    > [!NOTE]
    > El servidor proxy y el servidor Web deben ejecutarse en puertos diferentes.  
    
1.  Configure el [reenvío de Puerto](#set-up-port-forwarding) a su dispositivo Android.  En el campo **dirección local** , escriba `localhost:` seguido del puerto en el que se está ejecutando el servidor proxy.  Por ejemplo, si se está ejecutando en el puerto `8000` , vaya a `localhost:8000` .  En el campo **Puerto del dispositivo** , escriba el número en el que desea que escuche el dispositivo Android, como `3333` .  
    
### Establecer la configuración de proxy en el dispositivo  

A continuación, debe configurar su dispositivo Android para comunicarse con el servidor proxy.  

1.  En su dispositivo Android, vaya a **configuración**  >  **WiFi**.  
1.  Pulse el nombre de la red a la que está conectado en ese momento.  
    
    > [!NOTE]
    > Se aplica la configuración de proxy por red.  
    
1.  Elija **modificar red**.  
1.  Elija **Opciones avanzadas**.  Se muestra la configuración de proxy.  
1.  Seleccione el menú **proxy** y elija **manual**.  
1.  En el campo **nombre de host del proxy** , escriba `localhost` .  
1.  En el campo **Puerto proxy** , escriba el número de puerto que escribió para **Puerto de dispositivo** en la sección anterior.  
1.  Elija **Guardar**.  
    
Con esta configuración, el dispositivo reenvía todas sus solicitudes al proxy en el equipo de desarrollo.  El proxy realiza solicitudes en nombre de su dispositivo, de modo que las solicitudes a su dominio local personalizado se resuelvan correctamente.  

Ahora, obtenga acceso a los dominios personalizados de su dispositivo Android como en el equipo de desarrollo.  

Si su servidor Web se está ejecutando fuera de un puerto no estándar, recuerde especificar el puerto al solicitar el contenido de su dispositivo Android.  Por ejemplo, si su servidor web está usando el dominio personalizado `microsoft-edge.devtools` en el puerto `7331` , al ver el sitio desde su dispositivo Android debe usar la dirección URL `microsoft-edge.devtools:7331` .  

> [!TIP]
> Para reanudar la exploración normal, recuerde revertir la configuración del proxy en su dispositivo Android después de desconectarse de la máquina de desarrollo.  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introducción a la depuración remota dispositivos Android | Microsoft docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de depuración web de Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: optimizar la entrega en la web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler: proxy de depuración web gratuito"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
