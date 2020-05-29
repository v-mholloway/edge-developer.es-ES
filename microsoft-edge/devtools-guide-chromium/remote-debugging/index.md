---
title: Introducción a la depuración remota dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: a9002ca82e6e0dcaf7f174b336e5c640929a561b
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611822"
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




<!--
<style>
.devtools-inline {
  max-height: 1em;
  vertical-align: middle;
}
</style>
-->  
# Introducción a la depuración remota dispositivos Android   



Depure de forma remota contenido en vivo en un dispositivo Android desde su equipo con Windows o macOS.  Este tutorial le enseña a:  

*   Configure su dispositivo Android para la depuración remota y descárguelo desde el equipo de desarrollo.  
*   Inspeccione y depure contenido en vivo en su dispositivo Android desde su equipo de desarrollo.  
*   Contenido de screencast de su dispositivo Android en una instancia de DevTools en el equipo de desarrollo.  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## Paso 1: descubrir su dispositivo Android   

El flujo de trabajo siguiente funciona para la mayoría de los usuarios.  Consulte [solución de problemas: DevTools no detecta el dispositivo Android](#troubleshooting-devtools-is-not-detecting-the-android-device) para obtener ayuda.  

1.  Abra la pantalla **Opciones del desarrollador** en Android.  Consulte [configurar las opciones de Desarrollador en dispositivos](https://developer.android.com/studio/debug/dev-options.html).  
1.  Seleccione **Habilitar depuración USB**.  
1.  En tu equipo de desarrollo, abre Microsoft Edge.  
1.  [Abra DevTools][DevToolsOpen].  
1.  En DevTools, seleccione el **menú principal** `...` y, a continuación, seleccione **más herramientas**  >  **dispositivos remotos**.  
    
    > ##### Figura 1  
    > Abrir la ficha **dispositivos remotos** a través del **menú principal**  
    > ! [Abriendo la ficha dispositivos remotos a través del menú principal] [ImageOpenRemoteDevices]  

1.  En DevTools, abra la pestaña **configuración** .  

1.  Asegúrese de que la casilla **descubrir dispositivos USB** esté habilitada.  
    
    > ##### Figura 2  
    > La casilla **descubrir dispositivos USB** está habilitada  
    > ! [La casilla descubrir dispositivos USB está habilitada] [ImageDiscoverUSBDevices]  

1.  Conecta el dispositivo Android directamente a tu equipo de desarrollo con un cable USB.  La primera vez que lo haces, verás que DevTools ha detectado un dispositivo desconocido.  Si ve un punto verde y el texto **conectado** debajo del nombre del modelo de su dispositivo Android, DevTools ha establecido correctamente la conexión con el dispositivo.  Continúe con el [paso 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  Si el dispositivo se muestra como **desconocido**, acepte el aviso de permiso de **depuración USB** en tu dispositivo Android.  

### Solución de problemas: DevTools no detecta el dispositivo Android   

Asegúrese de que el hardware esté configurado correctamente:  

*   Si está usando un concentrador USB, intente conectar el dispositivo Android directamente a su equipo de desarrollo.  
*   Intente desconectar el cable USB entre su dispositivo Android y su equipo de desarrollo y, a continuación, conéctelo de nuevo.  Hágalo mientras las pantallas de Android y de equipo de desarrollo estén desbloqueadas.  
*   Asegúrate de que tu cable USB funcione.  Debería poder inspeccionar los archivos de su dispositivo Android desde su equipo de desarrollo.  

Asegúrese de que el software esté configurado correctamente:  

*   Si tu equipo de desarrollo ejecuta Windows, intenta instalar manualmente los drivers USB para tu dispositivo Android.  Consulte [Instalar drivers OEM USB][AndroidUSBDrivers].  
    
*   Algunas combinaciones de dispositivos Windows y Android (especialmente Samsung) requieren una configuración adicional.  Consulte [DevTools dispositivos no detectan el dispositivo cuando está conectado] [StackOverflowDevicesNotDetected].  
    
Si no ve el mensaje **permitir la depuración de USB** en su dispositivo Android, pruebe lo siguiente:  

*   Desconectar y volver a conectar el cable USB mientras DevTools está en el equipo de desarrollo y se muestra el pantalla Android de Android.  En otras palabras, a veces el mensaje no se muestra cuando las pantallas de Android o de equipo de desarrollo están bloqueadas.
*   Actualización de la configuración de pantalla de su dispositivo Android y equipo de desarrollo para que nunca pasen al modo de suspensión.  
*   Configuración del modo USB para Android en PTP.  Consulte [Galaxy S4 no muestra el cuadro de diálogo autorizar depuración USB][StackExchangeGalaxyS4DoesNotShowDialogBox].  
*   Seleccione **revocar las autorizaciones de depuración USB** en la pantalla de **Opciones del desarrollador** de su dispositivo Android para restablecerla a un estado actualizado.  

Si encuentra una solución que no se menciona en esta sección o en [los dispositivos DevTools no detectan el dispositivo cuando está conectado] [StackOverflowDevicesNotDetected] o agrega una respuesta a esa pregunta de desbordamiento de pila<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Paso 2: depure contenido en su dispositivo Android desde su equipo de desarrollo   

1.  Abre Microsoft Edge en tu dispositivo Android.  

1.  En la pestaña **dispositivos remotos** , seleccione la pestaña que coincida con el nombre de su modelo de dispositivo Android.  
    En la parte superior de esta página, verá el nombre del modelo de su dispositivo Android, seguido de su número de serie.  Debajo de eso, debería ver la versión de Microsoft Edge que se ejecuta en el dispositivo, con el número de versión entre paréntesis.  Cada pestaña abierta de Microsoft Edge obtiene su propia sección.  Puede interactuar con esa pestaña de esta sección.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  En el cuadro de texto **nueva pestaña** , escriba una dirección URL y, después, haga clic en **abrir**.  La página se abre en una nueva pestaña en su dispositivo Android.  

1.  Seleccione **inspeccionar** junto a la dirección URL que acaba de abrir.  Se abrirá una nueva instancia de DevTools.  La versión de Microsoft Edge que se ejecuta en su dispositivo Android determina la versión de DevTools que se abre en su equipo de desarrollo.  
    Por lo tanto, si su dispositivo Android está ejecutando una versión muy antigua de Microsoft Edge, la instancia de DevTools puede tener un aspecto muy diferente al que está acostumbrado.  

### Más acciones: volver a cargar, enfocar o cerrar una pestaña   

Seleccione **más opciones** `...` junto a la pestaña que desea volver a cargar, enfocar o cerrar.  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### Inspeccionar elementos   

Vaya al panel **elementos** de la instancia de DevTools y mantenga el mouse sobre un elemento para resaltarlo en el área de visualización de su dispositivo Android.  

También puede seleccionar un elemento de la pantalla de su dispositivo Android para seleccionarlo en el panel **elementos** .  Seleccione el elemento **Seleccionar elemento** ![ ][ImageSelectElementIcon] de la instancia de DevTools y, a continuación, seleccione el elemento en la pantalla de su dispositivo Android.  

> [!NOTE]
> **Seleccionar elemento** está deshabilitado después de la primera selección, por lo que debe volver a habilitarlo cada vez que desee usar esta característica.  

### Screencasts la pantalla de Android a su equipo de desarrollo   

Seleccione **activar o** desactivar ![ la demostración de alternancia ][ImageToggleScreencastIcon] para ver el contenido de su dispositivo Android en la instancia de DevTools.  

Puede interactuar con el screencast de varias maneras:  

*   Los clics se traducen en pulsaciones, lo que desencadena eventos táctiles adecuados en el dispositivo.  
*   Las pulsaciones de tecla de tu equipo se envían al dispositivo.  
*   Para simular un gesto de reducir, espera `Shift` mientras arrastra.  
*   Para desplazarse, use el panel táctil o la rueda del mouse, o Fling con el puntero del mouse.

Algunas notas en los screencasts:  

*   Los screencasts solo muestran el contenido de la página.  Partes transparentes del screencast representan interfaces de dispositivo, como la barra de direcciones de Microsoft Edge, la barra de estado de Android o el teclado Android.  
*   Los screencasts afectan negativamente a las tarifas de fotogramas.  Deshabilite el screencasts y mida los desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.  
*   Si su dispositivo Android bloquea la pantalla, el contenido del screencast desaparecerá.  Desbloquear la pantalla de su dispositivo Android para reanudar automáticamente el screencast.  





<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
[ImageOpenRemoteDevices]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Remote-Debugging-More-Tools-Remote-Devices.msft.png "Ilustración 1: abrir la pestaña dispositivos remotos a través del menú principal"  
[ImageDiscoverUSBDevices]:/Microsoft-Edge/DevTools-Guide-Chromium/Media/Remote-Debugging-Remote-Devices-Tab.msft.png "Ilustración 2: la casilla descubrir dispositivos USB está habilitada"  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--connected-remote-device.msft.png "old Figure 5:  A connected remote device"  -->
<!--[ImageReload]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--reload.msft.png "old Figure 6: The menu for reloading, focusing, or closing a tab"  -->

<!-- links -->  

[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Abrir Microsoft Edge DevTools"  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Instalar controladores USB para OEM | Desarrolladores de Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 "los dispositivos DevTools no detectan el dispositivo cuando el desbordamiento de pila está conectado"  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB-intercambio de pila de entusiastas de Android"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
