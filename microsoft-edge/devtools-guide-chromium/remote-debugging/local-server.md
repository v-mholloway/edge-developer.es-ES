---
description: Hospedar un sitio en un servidor web de máquina de desarrollo y, a continuación, acceder al contenido desde un dispositivo Android.
title: Acceso a servidores locales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 2d721a0ccd27befc7a59726f4c5ef9227042b30b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565095"
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
# <a name="access-local-servers"></a>Acceso a servidores locales  

Host a site on a development machine web server, then access the content from an Android device.  

Con un cable USB y Microsoft Edge DevTools, ejecute un sitio desde una máquina de desarrollo y, a continuación, vea el sitio en un dispositivo Android.  

### <a name="summary"></a>Resumen  

*   El reenvío de puertos te permite ver el contenido hospedado por el servidor web que se ejecuta en el equipo de desarrollo en tu dispositivo Android.  
*   Si el servidor web usa un dominio personalizado, configura el dispositivo Android para tener acceso al contenido de ese dominio con asignación de dominio personalizada.  

## <a name="set-up-port-forwarding"></a>Configurar el reenvío de puertos  

El reenvío de puertos permite que el dispositivo Android obtenga acceso al contenido que se hospeda en el servidor web que se ejecuta en el equipo de desarrollo.  El reenvío de puertos funciona creando un puerto TCP de escucha en el dispositivo Android que se asigna a un puerto TCP en el equipo de desarrollo.  El tráfico entre los puertos viaja a través de la conexión USB entre el dispositivo Android y el equipo de desarrollo, por lo que la conexión no depende de la configuración de red.  

Para habilitar el reenvío de puertos:  

1.  Configura la [depuración remota entre][RemoteDebuggingGettingStarted] el equipo de desarrollo y el dispositivo Android.  Cuando haya terminado, el dispositivo Android debe mostrarse en **** el menú izquierdo del cuadro de diálogo Inspeccionar dispositivos y un **indicador de** estado Conectado.  
1.  En el **cuadro de diálogo Inspeccionar dispositivos** de DevTools, habilite Reenvío de **puertos**.  
1.  Elija **Agregar regla**.  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Agregar una regla de reenvío de puertos" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       Agregar una regla de reenvío de puertos  
    :::image-end:::  
    
1.  En el **cuadro de texto** Puerto de dispositivo de la izquierda, escribe el número de puerto desde el que quieres tener acceso al sitio en tu dispositivo `localhost` Android.  Por ejemplo, si desea obtener acceso al sitio desde `localhost:5000` escriba `5000` .  
1.  En el **cuadro** de texto Dirección local de la derecha, escriba la dirección IP o el nombre de host en el que se hospeda el sitio en el servidor web que se ejecuta en el equipo de desarrollo, seguido del número de puerto.  Por ejemplo, si el sitio se está ejecutando al `localhost:7331` escribir `localhost:7331` .  
1.  Elija **Agregar**.  
    
El reenvío de puertos ya está configurado.  Revisa el indicador de estado del puerto hacia delante en la pestaña del dispositivo en el cuadro **de diálogo Inspeccionar dispositivos.**  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Estado de reenvío de puertos" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   Estado de reenvío de puertos  
:::image-end:::  

Para ver el contenido, abra Microsoft Edge en el dispositivo Android y vaya al puerto que especificó `localhost` en el campo Puerto **de** dispositivo.  Por ejemplo, si ha escrito `5000` en el campo, visite `localhost:5000` .  

## <a name="map-to-custom-local-domains"></a>Asignar a dominios locales personalizados  

La asignación de dominio personalizada permite ver contenido en un dispositivo Android desde un servidor web en el equipo de desarrollo que usa un dominio personalizado.  

Por ejemplo, supongamos que el sitio usa una biblioteca de JavaScript de terceros que solo funciona en el dominio `microsoft-edge.devtools` .  Por lo tanto, cree una entrada en el archivo en el equipo de desarrollo para asignar este dominio `hosts` a `localhost` \(por ejemplo, `127.0.0.1 microsoft-edge.devtools` \).  Después de configurar la asignación de dominio personalizada y el reenvío de puertos, vea el sitio en el dispositivo Android en la dirección URL `microsoft-edge.devtools` .  

### <a name="set-up-port-forwarding-to-proxy-server"></a>Configurar el reenvío de puertos al servidor proxy  

Para asignar un dominio personalizado, debe ejecutar un servidor proxy en el equipo de desarrollo.  Ejemplos de servidores proxy [son Charles,][CharlesWebDebuggingProxy] [Squid][SquidCacheWiki]y [Fiddler.][TelerikFiddler]  

Para configurar el reenvío de puertos a un proxy:  

1.  Ejecute el servidor proxy y registre el puerto que está usando.  
    
    > [!NOTE]
    > El servidor proxy y el servidor web deben ejecutarse en puertos diferentes.  
    
1.  Configura el [reenvío de puertos](#set-up-port-forwarding) a tu dispositivo Android.  Para el **campo de dirección local,** escriba seguido del puerto en el que se `localhost:` está ejecutando el servidor proxy.  Por ejemplo, si se está ejecutando en el puerto `8000` , vaya a `localhost:8000` .  En el **campo puerto del** dispositivo, escriba el número en el que desea que su dispositivo Android escuche, como `3333` .  
    
### <a name="configure-proxy-settings-on-your-device"></a>Configurar la configuración de proxy en el dispositivo  

A continuación, debes configurar el dispositivo Android para que se comunique con el servidor proxy.  

1.  En el dispositivo Android, vaya **a Configuración**  >  **Wi-Fi**.  
1.  Presione durante mucho tiempo el nombre de la red a la que está conectado actualmente.  
    
    > [!NOTE]
    > La configuración de proxy se aplica por red.  
    
1.  Elija **Modificar red**.  
1.  Elija **Opciones avanzadas**.  Se muestra la configuración de proxy.  
1.  Elija el **menú Proxy** y **elija Manual**.  
1.  Para el **campo Nombre de host** proxy, escriba `localhost` .  
1.  Para el **campo Puerto proxy,** escriba el número de puerto que escribió para el **puerto del dispositivo** en la sección anterior.  
1.  Elija **Guardar**.  
    
Con esta configuración, el dispositivo reenvía todas sus solicitudes al proxy en el equipo de desarrollo.  El proxy realiza solicitudes en nombre de su dispositivo, por lo que las solicitudes a su dominio local personalizado se resuelven correctamente.  

Ahora, accede a dominios personalizados en tu dispositivo Android al igual que en la máquina de desarrollo.  

Si el servidor web se está ejecutando fuera de un puerto no estándar, recuerde especificar el puerto al solicitar el contenido desde el dispositivo Android.  Por ejemplo, si el servidor web usa el dominio personalizado en el puerto , cuando vea el sitio desde su dispositivo Android, debe usar `microsoft-edge.devtools` `7331` la dirección URL `microsoft-edge.devtools:7331` .  

> [!TIP]
> Para reanudar la exploración normal, recuerda revertir la configuración de proxy en el dispositivo Android después de desconectarte del equipo de desarrollo.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de depuración web de Carlos"  

[SquidCacheWiki]: https://wiki.squid-cache.org "Wiki proxy de wiki de calamar"  

[TelerikFiddler]: https://www.telerik.com/fiddler "Fiddler: proxy de depuración web gratuito"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) se encuentra aquí y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) y [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
