---
description: Depure contenido en vivo en un dispositivo Android desde un equipo con Windows o macOS.
title: Introducción a la depuración remota dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: f1ed7c698f588bb4e438d1b85a0cd0d1aba42647
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993502"
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

# Introducción a la depuración remota dispositivos Android  

Depure de forma remota contenido en vivo en un dispositivo Android desde su equipo con Windows o macOS.  La siguiente página del tutorial le enseña a completar las siguientes acciones.  

*   Configure su dispositivo Android para la depuración remota y descárguelo desde el equipo de desarrollo.  
*   Inspeccione y depure contenido en vivo en su dispositivo Android desde su equipo de desarrollo.  
*   Contenido de screencast de su dispositivo Android en una instancia de DevTools en el equipo de desarrollo.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> La depuración remota de la aplicación Microsoft Edge en dispositivos iOS no es compatible actualmente.  La siguiente guía está específicamente centrada en la depuración remota de Microsoft Edge en dispositivos con Android.
> Si tiene un dispositivo macOS, siga la [Guía de depuración Brightcove][BrightcoveSupportDebuggingMobileDevices] para depurar Microsoft Edge de forma remota en un dispositivo iOS con Safari.  Para obtener más información sobre la herramienta Web Inspector de Safari, vea [herramientas de desarrollo web de Safari][AppleDeveloperSafariTools].  

## Paso 1: descubrir su dispositivo Android  

El flujo de trabajo siguiente funciona para la mayoría de los usuarios.  Para obtener más ayuda, consulte la [solución de problemas: DevTools no detecta la sección del dispositivo Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .  

1.  Abra la pantalla **Opciones del desarrollador** en Android.  Para obtener más información, vea [configurar las opciones de Desarrollador en dispositivos][AndroidDeveloperStudioDevOptions].  
1.  Seleccione **Habilitar depuración USB**.  
1.  En tu equipo de desarrollo, abre Microsoft Edge.  
1.  Vaya a la `edge://inspect` Página de Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="La página edge://inspect en Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Figura 1.  La `edge://inspect` página en Microsoft Edge  
    :::image-end:::  
    
1.  Conecta el dispositivo Android directamente a tu equipo de desarrollo con un cable USB.  La primera vez que intentes conectarte, normalmente verás pregunta sobre DevTools detectando un dispositivo desconocido.  Acepte la solicitud de permiso de **depuración USB** en su dispositivo Android.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="La solicitud de permiso de depuración USB en un dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Figura 2.  La solicitud de permiso de **depuración USB** en un dispositivo Android  
    :::image-end:::  
    
1.  Si ve el nombre del modelo de su dispositivo Android, Microsoft Edge ha establecido correctamente la conexión con el dispositivo.  Continúe con la sección [paso 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### Solución de problemas: DevTools no detecta el dispositivo Android  

Use las siguientes sugerencias para solucionar problemas relacionados con la configuración correcta de su hardware.  

*   Si está usando un concentrador USB, intente conectar el dispositivo Android directamente a su equipo de desarrollo.  
*   Intenta desconectar el cable USB entre el dispositivo Android y el equipo de desarrollo y, a continuación, vuelve a conectar tu cable USB.  Complete la tarea mientras las pantallas de Android y de equipo de desarrollo estén desbloqueadas.  
*   Asegúrate de que tu cable USB funcione.  Debería poder inspeccionar los archivos de su dispositivo Android desde su equipo de desarrollo.  

Use las siguientes sugerencias para comprobar que el software está configurado correctamente.  

*   Si tu equipo de desarrollo ejecuta Windows, intenta instalar manualmente los drivers USB para tu dispositivo Android.  Para obtener más información, consulte [instalar controladores de OEM USB][AndroidDeveloperToolsOemUsb].  
*   Algunas combinaciones de Windows y dispositivos Android \ (especialmente Samsung \) requieren configuración adicional.  Para obtener más información, consulte los [dispositivos de DevTools no detectan el dispositivo cuando está conectado][Stackoverflow21925992].  

Use las siguientes sugerencias para evitar que se vea el aviso de **depuración USB** en su dispositivo Android.  

*   Desconectar y volver a conectar el cable USB mientras DevTools está en el equipo de desarrollo y se muestra el pantalla Android de Android.  
    
    > [!NOTE]
    > Es posible que no vea el mensaje si su pantalla de Android o de equipo de desarrollo está bloqueada.  

*   Actualización de la configuración de pantalla de su dispositivo Android y de la máquina de desarrollo para que cada uno nunca vaya al modo de suspensión.  
*   Configuración del modo USB para Android en PTP.  Para obtener más información, consulte [Galaxy S4 no muestra el cuadro de diálogo autorizar depuración USB][StackexchangeAndroid101933].  
*   Seleccione **revocar las autorizaciones de depuración USB** en la pantalla de **Opciones del desarrollador** de su dispositivo Android para restablecerla a un estado actualizado.  

Si encuentra una solución que no está mencionada en esta página o en [DevTools dispositivos no detecta el dispositivo cuando está conectado][Stackoverflow21925992] al desbordamiento de la pila, agregue la solución a la pregunta de desbordamiento de pila.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Paso 2: depure contenido en su dispositivo Android desde su equipo de desarrollo  

1.  Abre Microsoft Edge en tu dispositivo Android.  
1.  En la `edge://inspect` página, verá el nombre del modelo de su dispositivo Android, seguido del número de serie del dispositivo.  Debajo de eso, debería ver la versión de Microsoft Edge que se ejecuta en el dispositivo, con el número de versión entre paréntesis.  Cada pestaña abierta de Microsoft Edge obtiene una sección única.  Puede interactuar con esa pestaña en una sección.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Figura 3.  Un dispositivo remoto conectado  
    :::image-end:::  
    
1.  En el cuadro de texto **pestaña abrir con dirección URL** , escriba una dirección URL y, a continuación, seleccione **abrir**.  La página se abre en una nueva pestaña en su dispositivo Android.  
1.  Seleccione **inspeccionar** junto a la dirección URL que acaba de abrir.  Se abrirá una nueva instancia de DevTools.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### Más acciones: foco, volver a cargar o cerrar una pestaña  

Seleccione la **pestaña foco**, **volver a cargar**o **cerca** de la pestaña que desea centrar, volver a cargar o cerrar.  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Botones para centrar, volver a cargar o cerrar una pestaña" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Figura 4.  Botones para centrar, volver a cargar o cerrar una pestaña  
:::image-end:::  

### Inspeccionar elementos  

Vaya al panel **elementos** de la instancia de DevTools y mantenga el mouse sobre un elemento para resaltarlo en el área de visualización de su dispositivo Android.  

También puede seleccionar un elemento de la pantalla de su dispositivo Android para seleccionarlo en el panel **elementos** .  Seleccione **Select Element** ![ ][ImageSelectElementIcon] el icono de elemento seleccionar elemento en la instancia de DevTools y, a continuación, seleccione el elemento en la pantalla de su dispositivo Android.  

> [!NOTE]
> **Seleccionar elemento** está deshabilitado después de la primera selección, por lo que debe volver a habilitarlo cada vez que desee usar la característica.  

### Screencasts la pantalla de Android a su equipo de desarrollo  

Seleccione **activar o desactivar** ![ ][ImageToggleScreencastIcon] el icono del screencast para ver el contenido de su dispositivo Android en la instancia de DevTools.  

Puede interactuar con el screencast de las siguientes maneras.  

*   Los clics se traducen en pulsaciones, lo que desencadena eventos táctiles adecuados en el dispositivo.  
*   Las pulsaciones de tecla de tu equipo se envían al dispositivo.  
*   Para simular un gesto de reducir, espera `Shift` mientras arrastra.  
*   Para desplazarse, use el panel táctil o la rueda del mouse, o Fling con el puntero del mouse.

> [!NOTE]
> Use las siguientes sugerencias para ayudarle con el screencast.  
> 
> *   Los screencasts solo muestran el contenido de la página.  Partes transparentes del screencast representan interfaces de dispositivo, como la barra de direcciones de Microsoft Edge, la barra de estado de Android o el teclado Android.  
> *   Los screencasts afectan negativamente a las tarifas de fotogramas.  Deshabilite el screencasts y mida los desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.  
> *   Si su dispositivo Android bloquea la pantalla, el contenido del screencast desaparecerá.  Desbloquear la pantalla de su dispositivo Android para reanudar automáticamente el screencast.  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurar opciones de Desarrollador en el dispositivo | Desarrollador de Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Instalar controladores USB para OEM | Desarrolladores de Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Herramientas de desarrollo web de Safari | Desarrollador de Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Depurar en dispositivos móviles | Soporte técnico de Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "ADB-intercambio de pila de entusiastas de Android"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Los dispositivos DevTools no detectan el dispositivo cuando está conectado el desbordamiento de pila"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
