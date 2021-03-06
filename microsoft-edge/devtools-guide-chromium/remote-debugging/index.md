---
description: Depuración remota de contenido en directo en un dispositivo Android desde un equipo con Windows o macOS.
title: Introducción a la depuración remota de dispositivos Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 61fad793ca03dbef68a5f769dbfd25e780fd9930
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398262"
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

# <a name="get-started-with-remote-debugging-android-devices"></a>Introducción a la depuración remota de dispositivos Android  

Depuración remota de contenido en directo en un dispositivo Android desde tu equipo Windows o macOS.  La siguiente página de tutorial le enseña a completar las siguientes acciones.  

*   Configura tu dispositivo Android para la depuración remota y descóyralo desde el equipo de desarrollo.  
*   Inspecciona y depura contenido en directo en tu dispositivo Android desde el equipo de desarrollo.  
*   Difusión de contenido desde el dispositivo Android a una instancia de DevTools en el equipo de desarrollo.  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> Actualmente no se admite la depuración remota de la aplicación Microsoft Edge en dispositivos iOS.  La siguiente guía se centra específicamente en la depuración remota de Microsoft Edge en dispositivos Android.
> Si tienes un dispositivo macOS, sigue la guía de depuración de [Brightcove][BrightcoveSupportDebuggingMobileDevices] para depurar de forma remota Microsoft Edge en un dispositivo iOS con Safari.  Para obtener más información acerca de la herramienta Inspector web en Safari, vaya a [Safari Web Development Tools][AppleDeveloperSafariTools].  

## <a name="step-1-discover-your-android-device"></a>Paso 1: Descubrir el dispositivo Android  

El flujo de trabajo siguiente funciona para la mayoría de los usuarios.  Para obtener más ayuda, vaya [a Solución de problemas: DevTools no detecta la sección dispositivo Android.](#troubleshooting-devtools-is-not-detecting-the-android-device)  

1.  Abre la **pantalla Opciones de** desarrollador en tu Android.  Para obtener más información, vaya a [Configurar opciones de desarrollador en el dispositivo][AndroidDeveloperStudioDevOptions].  
1.  Elija **Habilitar depuración USB**.  
1.  En el equipo de desarrollo, abra Microsoft Edge.  
1.  Vaya a la `edge://inspect` página de Microsoft Edge.  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="La edge://inspect en Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       Figura 1.  La `edge://inspect` página de Microsoft Edge  
    :::image-end:::  
    
1.  Conecta el dispositivo Android directamente a la máquina de desarrollo mediante un cable USB.  La primera vez que intentes conectarte, debería mostrarse un mensaje sobre DevTools que detecta un dispositivo desconocido.  Acepta el **símbolo del permiso Permitir depuración USB** en tu dispositivo Android.  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="El símbolo del sistema de permiso Permitir depuración USB en un dispositivo Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       Figura 2.  El **símbolo del sistema de permiso Permitir depuración USB** en un dispositivo Android  
    :::image-end:::  
    
1.  Si se muestra el nombre del modelo del dispositivo Android, Microsoft Edge ha establecido correctamente la conexión con el dispositivo.  Continúe con la [sección Paso 2.](#step-2-debug-content-on-your-android-device-from-your-development-machine)  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <a name="troubleshooting-devtools-is-not-detecting-the-android-device"></a>Solución de problemas: DevTools no detecta el dispositivo Android  

Use las siguientes sugerencias para ayudarle a solucionar problemas con la configuración correcta del hardware.  

*   Si usas un concentrador USB, prueba a conectar el dispositivo Android directamente a la máquina de desarrollo.  
*   Prueba a desconectar el cable USB entre el dispositivo Android y la máquina de desarrollo y, a continuación, vuelve a conectar el cable USB.  Completa la tarea mientras se desbloquean las pantallas de la máquina de desarrollo y Android.  
*   Asegúrese de que el cable USB funciona.  Debes poder inspeccionar los archivos del dispositivo Android desde el equipo de desarrollo.  

Use las siguientes sugerencias para comprobar que el software está configurado correctamente.  

*   Si el equipo de desarrollo ejecuta Windows, intenta instalar manualmente los controladores USB para tu dispositivo Android.  Para obtener más información, vaya a [Instalar controladores USB OEM.][AndroidDeveloperToolsOemUsb]  
*   Algunas combinaciones de dispositivos Windows y Android \(especialmente Samsung\) requieren configuraciones adicionales.  Para obtener más información, vaya [a DevTools Devices no detecta el dispositivo cuando está conectado][Stackoverflow21925992].  

Usa las siguientes sugerencias para ayudarte a solucionar problemas si el mensaje Permitir **depuración USB** no se muestra en tu dispositivo Android.  

*   Desconectar y volver a conectar el cable USB mientras DevTools se centra en la máquina de desarrollo y se muestra la pantalla principal de Android.  
    
    > [!NOTE]
    > El mensaje se muestra si las pantallas de la máquina de desarrollo o Android están bloqueadas.  

*   Actualizar la configuración de pantalla para el dispositivo Android y la máquina de desarrollo para que cada uno nunca entre en suspensión.  
*   Establecer el modo USB para Android en PTP.  Para obtener más información, vaya [a Galaxy S4 no muestra el cuadro de diálogo Autorizar depuración USB][StackexchangeAndroid101933].  
*   Elige **Revocar autorizaciones de depuración USB** en la pantalla Opciones de desarrollador del dispositivo Android para restablecerla a un estado nuevo. ****  

Si encuentras una solución que no se menciona en esta página o en [DevTools Devices][Stackoverflow21925992] no detecta el dispositivo cuando está conectado a Stack Overflow, agrega la solución a la pregunta Stack Overflow<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->.  

## <a name="step-2-debug-content-on-your-android-device-from-your-development-machine"></a>Paso 2: Depurar contenido en el dispositivo Android desde el equipo de desarrollo  

1.  Abre Microsoft Edge en tu dispositivo Android.  
1.  Navegue hasta , se muestra el nombre del modelo del dispositivo `edge://inspect` Android, seguido del número de serie del dispositivo.  A continuación, se debe mostrar la versión de Microsoft Edge que se ejecuta en el dispositivo, con el número de versión entre paréntesis.  Cada pestaña de Microsoft Edge abierta obtiene una sección única.  Puede interactuar con esa pestaña desde una sección.  <!--If there are any apps using WebView, a section for each of those apps should be displayed, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Un dispositivo remoto conectado" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       Figura 3.  Un dispositivo remoto conectado  
    :::image-end:::  
    
1.  En el **cuadro de texto Abrir pestaña con dirección URL,** escriba una dirección URL y, a continuación, elija **Abrir**.  La página se abre en una nueva pestaña en el dispositivo Android.  
1.  Elija **inspeccionar** junto a la dirección URL que acaba de abrir.  Se abre una nueva instancia de DevTools.  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <a name="more-actions-focus-refresh-or-close-a-tab"></a>Más acciones: enfocar, actualizar o cerrar una pestaña  

Elija **la pestaña foco,** **volver**a cargar o **cerrar** junto a la pestaña que desea enfocar, actualizar o cerrar.  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Botones para enfocar, actualizar o cerrar una pestaña" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   Figura 4.  Botones para enfocar, actualizar o cerrar una pestaña  
:::image-end:::  

### <a name="inspect-elements"></a>Inspeccionar elementos  

Vaya a la **herramienta Elementos** de la instancia de DevTools y mantenga el mouse sobre un elemento para resaltarlo en la ventanilla del dispositivo Android.  

También puedes seleccionar un elemento en la pantalla del dispositivo Android para seleccionarlo en la **herramienta** Elementos.  Elija **Seleccionar elemento** \( Seleccionar elemento \) icono en la instancia de ![ DevTools y, a continuación, seleccione ][ImageSelectElementIcon] el elemento en la pantalla del dispositivo Android.  

> [!NOTE]
> **Select Element** está deshabilitado después de la primera selección, por lo que debes volver a habilitarlo cada vez que quieras usar la característica.  

### <a name="screencast-your-android-screen-to-your-development-machine"></a>Difusión en pantalla de la pantalla de Android a la máquina de desarrollo  

Elija **Alternar difusión** de pantalla \( Alternar difusión por pantalla \) icono para ver el contenido de su dispositivo ![ Android en la instancia de ][ImageToggleScreencastIcon] DevTools.  

Puede interactuar con la difusión en pantalla de las siguientes maneras.  

*   Las opciones se traducen en pulsaciones, lo que dispara los eventos táctiles adecuados en el dispositivo.  
*   Las pulsaciones de teclas del equipo se envían al dispositivo.  
*   Para simular un gesto de pellizco, mantén `Shift` presionado mientras arrastras.  
*   Para desplazarse, use el trackpad o la rueda del mouse o fling con el puntero del mouse.

> [!NOTE]
> Usa las siguientes sugerencias para ayudarte a la difusión en pantalla.  
> 
> *   Los difusión en pantalla solo muestran el contenido de la página.  Las partes transparentes de la difusión por pantalla representan interfaces de dispositivo, como la barra de direcciones de Microsoft Edge, la barra de estado de Android o el teclado androide.  
> *   Las difusión en pantalla afectan negativamente a las tasas de fotogramas.  Deshabilite la difusión por pantalla al medir desplazamientos o animaciones para obtener una imagen más precisa del rendimiento de la página.  
> *   Si la pantalla del dispositivo Android se bloquea, el contenido de la difusión en pantalla desaparece.  Desbloquea la pantalla del dispositivo Android para reanudar automáticamente la difusión por pantalla.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Configurar opciones de desarrollador en el dispositivo | Desarrollador de Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Instalar controladores USB OEM | Desarrolladores de Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Herramientas de desarrollo web de Safari | Desarrollador de Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Depuración en dispositivos móviles | Compatibilidad con Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "adb: Exchange de pila de entusiastas de Android"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Dispositivos DevTools no detecta el dispositivo cuando está conectado: desbordamiento de pila"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
