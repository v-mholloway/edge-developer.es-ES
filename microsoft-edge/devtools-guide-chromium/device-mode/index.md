---
description: Usa dispositivos virtuales en Microsoft Edge para crear sitios web móviles.
title: Emular dispositivos móviles en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools, emulación, dispositivo, simulación, móvil
ms.openlocfilehash: 1a83dece95acba386385bfea035a9e2c91639240
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398793"
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

# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a>Emular dispositivos móviles en Microsoft Edge DevTools  

Usa **la emulación de dispositivo para** aproximar el aspecto de la página y cómo responde en un dispositivo móvil.  Microsoft Edge DevTools proporciona una colección de características que le ayudarán a emular dispositivos móviles.  La colección incluye las siguientes características.  

*   [Simular una ventanilla móvil](#simulate-a-mobile-viewport)  
*   [Limitar la red](#throttle-the-network-only)  
*   [Limitar la CPU](#throttle-the-cpu-only)  
*   [Simular geolocalización](#override-geolocation)  
*   [Establecer orientación](#set-orientation)  
*   [Establecer la cadena de agente de usuario](#set-user-agent-string)  

## <a name="limitations"></a>Limitaciones  

**La emulación de dispositivo** [es][WikiApproximation] una aproximación de primer orden de la apariencia de la página en un dispositivo móvil.  **La emulación de** dispositivos no ejecuta realmente el código en un dispositivo móvil.  En su lugar, simulas la experiencia del usuario móvil desde tu portátil o escritorio.  

Algunos aspectos de los dispositivos móviles nunca se emulan en DevTools.  Por ejemplo, la arquitectura de las CPU móviles es diferente de la arquitectura de las CPU de equipos portátiles o de escritorio.  Cuando hay dudas, la mejor opción es ejecutar la página en un dispositivo móvil.  Use [Depuración remota][DevToolsRemoteDebugging] para interactuar con el código de una página desde el equipo mientras la página se ejecuta realmente en un dispositivo móvil.  Puede ver, cambiar, depurar, perfil o los cuatro mientras interactúa con el código.  El equipo puede ser un bloc de notas o un equipo de escritorio.  

## <a name="simulate-a-mobile-viewport"></a>Simular una ventanilla móvil  

Elija **Alternar emulación** de dispositivo \( Alternar barra de herramientas del dispositivo \) o elija Personalizar y ![ controlar ][ImageDeviceToolbarIcon] **DevTools** \( `...` \) **** emulación de dispositivo > para abrir la interfaz de usuario que permite simular una ventanilla móvil.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    La barra de herramientas del dispositivo  
:::image-end:::  

De forma predeterminada, la barra de herramientas del dispositivo se abre en modo de ventanilla dinámica.  

### <a name="responsive-viewport-mode"></a>Modo de ventanilla dinámica  

Para probar rápidamente el aspecto de la página en varios tamaños de pantalla, arrastre los controladores para cambiar el tamaño de la ventanilla a las dimensiones necesarias.  También puede especificar valores específicos en los cuadros de ancho y alto.  En la figura siguiente, el ancho se establece en `626` y el alto se establece en `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Los controladores para cambiar las dimensiones de la ventanilla cuando se encuentra en modo de ventanilla dinámica" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    Los controladores para cambiar las dimensiones de la ventanilla cuando se encuentra en modo de ventanilla dinámica  
:::image-end:::  

#### <a name="show-media-queries"></a>Mostrar consultas multimedia  

Si ha definido consultas multimedia en la página, vaya a las dimensiones de ventanilla donde esas consultas multimedia tengan efecto mostrando puntos de interrupción de consulta multimedia encima de la ventanilla.  Elija **Más opciones Mostrar**consultas  >  **multimedia**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas multimedia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Mostrar consultas multimedia**  
:::image-end:::  

Elija un punto de interrupción para cambiar el ancho de la ventanilla para que se desencadene la consulta multimedia.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Elegir un punto de interrupción para cambiar el ancho de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Elegir un punto de interrupción para cambiar el ancho de la ventanilla  
:::image-end:::  

#### <a name="set-the-device-type"></a>Establecer el tipo de dispositivo  

Usa la **lista Tipo de** dispositivo para simular un dispositivo móvil o dispositivo de escritorio.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="La lista Tipo de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   La **lista Tipo de** dispositivo  
:::image-end:::  

En la tabla siguiente se describen las diferencias entre las opciones de tipo de dispositivo disponibles.  La columna Rendering method hace referencia a si Microsoft Edge representa la página como una ventanilla móvil o de escritorio.  La columna de icono cursor hace referencia al tipo de cursor que se muestra al pasar el mouse en la página.  La columna Eventos desencadenados hace referencia a si la página desencadena `touch` o eventos al interactuar con la `click` página.  

| Opción | Método rendering | Icono de cursor | Eventos desencadenados |  
|:--- |:--- |:--- |:--- |  
| Móvil | Móvil | Círculo | Función táctil |  
| Mobile \(no touch\) | Móvil | Normal |  elige  |  
| Escritorio | Escritorio | Normal |  elige  |  
| Escritorio \(touch\) | Escritorio | Círculo | Función táctil |  

> [!NOTE]
> Si no **se muestra la** lista Tipo de dispositivo, elija Más **opciones**Agregar tipo  >  **de dispositivo**.  

### <a name="mobile-device-viewport-mode"></a>Modo de ventanilla de dispositivo móvil  

Para simular las dimensiones de un dispositivo móvil específico, selecciona el dispositivo en la **lista** Dispositivo.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   Lista **de dispositivos**  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a>Girar la ventanilla a orientación horizontal  

Pruebe la página web en orientación horizontal.  

*   Para girar la ventanilla a orientación horizontal, **elija Girar** \( ![ Girar ][ImageRotateIcon] \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Página mostrada en orientación horizontal" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Página mostrada en orientación horizontal  
    :::image-end:::  
    
> [!NOTE]
> El **botón** Girar desaparece si la barra **de herramientas del** dispositivo es estrecha.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   La **barra de herramientas del dispositivo**  
:::image-end:::  

Para obtener más información, vaya a [Establecer orientación](#set-orientation).  

#### <a name="show-device-frame"></a>Mostrar fotograma del dispositivo  

Muestra el marco del dispositivo físico alrededor de la ventanilla cuando simulas las dimensiones de un dispositivo móvil específico, como un iPhone 6.  

1.  Abra **Más opciones**.  
1.  Elija **Mostrar marco de dispositivo**.  

> [!NOTE]
> Si no se muestra un marco de dispositivo para un dispositivo determinado, significa que DevTools no tiene arte para la opción.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar fotograma del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Mostrar fotograma del dispositivo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Marco del dispositivo para el iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Marco del dispositivo para el iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a>Agregar un dispositivo móvil personalizado  

Si la opción de dispositivo móvil que necesitas no está incluida en la lista predeterminada, puedes agregar un dispositivo personalizado.  Para agregar un dispositivo personalizado, siga estos pasos.  

1.  Elija la **lista** Dispositivo > **Editar**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Elegir editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Elegir **editar**  
    :::image-end:::  
    
1.  Elija **Agregar dispositivo personalizado**.  
1.  En **Dispositivos emulados,** escriba un nombre de dispositivo, ancho de pantalla y alto de pantalla para el dispositivo personalizado.  La [relación de píxeles del dispositivo,][MDNWindowDevicePixelRatio] [la cadena de agente de usuario][MDNUserAgent]y los campos de [tipo de](#set-the-device-type) dispositivo son opcionales.  El campo de tipo de dispositivo tiene el valor **predeterminado Mobile**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Crear un dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Crear un dispositivo personalizado  
    :::image-end:::  
    
### <a name="show-rulers"></a>Mostrar reglas  

Si necesita medir las dimensiones de pantalla, puede usar reglas para medir el tamaño de pantalla en píxeles.  Elija **Más opciones**Mostrar reglas para mostrar las reglas arriba y a la izquierda de la  >  **** ventanilla.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Elemento de menú para mostrar reglas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Elemento de menú para mostrar reglas  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Reglas arriba y a la izquierda de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Reglas arriba y a la izquierda de la ventanilla  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a>Acercar la ventanilla  

Para probar la apariencia de la página en varios niveles de zoom, usa la **lista Zoom** para acercar o alejar.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a>Limitar la red y la CPU  

Los dispositivos móviles suelen tener restricciones de red y CPU.  Asegúrate de probar la rapidez con la que se carga la página y cómo responde a diferentes velocidades de Internet y CPU.  

Limita la red y la CPU.  

1.  Elija **Lista de** limitaciones y cambie el valor preestablecido a Móvil de **nivel** intermedio o Móvil de **gama baja.**  
    *   **El móvil de nivel intermedio** simula y limita la `fast 3G` CPU.  Es cuatro veces más lento de lo normal.  
    *   **El móvil de gama baja** simula y limita la `slow 3G` CPU.  Es seis veces más lento de lo normal.  
    
Toda la limitación se basa en la funcionalidad normal de su portátil o escritorio.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="La lista De limitación de la barra de herramientas de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   La **lista De limitación** de la barra de herramientas de dispositivos  
:::image-end:::  

> [!NOTE]
> Si la **lista de limitaciones** está oculta, la **barra de herramientas del** dispositivo es demasiado estrecha.  Para obtener acceso a **la lista de limitaciones,** aumente el ancho de la barra de herramientas **del dispositivo**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   La **barra de herramientas del dispositivo**  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a>Limitar solo la CPU  

Para limitar la CPU solo y no la red, siga estos pasos.

1.  Elija el panel **Rendimiento** y elija **Configuración de captura** \( Configuración de captura ![ ][ImageCaptureIcon] \).
1.  Elija **CPU**  >  **4x slowdown** o **6x slowdown**.
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="La lista de CPU del panel Rendimiento" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       La **lista de CPU** del panel **Rendimiento**  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a>Limitar solo la red  

Para limitar solo la red, siga estos pasos.

1.  Elija la **herramienta Red.**
1.  Elija **Online**  >  **Fast 3G** o Slow **3G**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Lista de limitaciones en el panel Red" lightbox="../media/device-mode-network-throttle.msft.png":::
       Lista **de limitaciones** en el panel Red  
    :::image-end:::  
    
    O seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\) **** `3G` **** **** para abrir el menú comando , escriba y elija Habilitar la limitación rápida de 3G o Habilitar la limitación 3G lenta .  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Menú comando" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       Menú **comando**  
    :::image-end:::  
    
También puede establecer la limitación de red desde **el** panel Rendimiento.  

1.  Elija **Configuración de** captura \( Configuración de captura \) y elija la lista Red y cambie el valor preestablecido ![ a Fast ][ImageCaptureIcon] **3G** o **Slow 3G**. ****  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Establecer limitación de red desde el panel Rendimiento" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Establecer limitación de red desde **el** panel Rendimiento  
    :::image-end:::  
    
## <a name="override-geolocation"></a>Reemplazar geolocalización  

:::row:::
   :::column span="":::
      Si la página depende de la información de geolocalización de un dispositivo móvil para representarse correctamente, proporcione distintas geolocalizaciones mediante la interfaz de usuario de reemplazo de geolocalización.  

      1.  Elija **Personalizar y controlar DevTools** \( `...` \) > Más herramientas ****  >  **Sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores de geolocalización" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores** de geolocalización  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abra el menú comando.  
          *   Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).  
      1. Escriba `Sensors` y elija Mostrar **sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores para geolocalización" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar sensores** para geolocalización  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

En **el** panel Sensores, puede seleccionar una de las **** ubicaciones preestablecidas incluidas en DevTools mediante el menú desplegable Ubicación.  Para especificar una ubicación personalizada, elija **Otros...** e introduzca las coordenadas de la ubicación personalizada.  Para probar la página en un estado de error cuando la información de ubicación no está disponible, elija **Ubicación no disponible.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Panel de sensores con una ubicación preestablecida seleccionada" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    **Panel** de sensores con una ubicación preestablecida seleccionada.  
:::image-end:::

## <a name="set-orientation"></a>Establecer orientación  

:::row:::
   :::column span="":::
      Si la página depende de la información de orientación de un dispositivo móvil para que se represente correctamente, abra la interfaz de usuario de orientación.  

      1.  Elija **Personalizar y controlar DevTools** \( `...` \) > Más herramientas ****  >  **Sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores de orientación" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores** de orientación  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abra el menú comando.  
          *   Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).  
      1. Escriba `Sensors` y elija Mostrar **sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores para orientación" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar sensores** para orientación  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

En **el** panel Sensores, puede seleccionar una orientación preestablecida en **el** menú desplegable Orientación.  Para escribir su propia orientación, elija **Orientación personalizada**e introduzca sus propios [valores alfa,][MDNDeviceOrientaitonAlpha] [beta][MDNDeviceOrientaitonBeta]y [gamma.][MDNDeviceOrientaitonGamma]  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Opciones de orientación en el panel Sensores" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    **Opciones de** orientación en el panel **Sensores**  
:::image-end:::  

## <a name="set-user-agent-string"></a>Establecer cadena de agente de usuario  

:::row:::
   :::column span="":::
      Si la página depende de la cadena de agente de usuario de un dispositivo móvil para representarse correctamente, use el panel **Condiciones** de red para proporcionar distintas cadenas de agente de usuario.  
      
      1.  Elija **Personalizar y controlar DevTools** \( `...` \) > Más herramientas **Condiciones**  >  **de red**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrada condiciones de red en el menú Más herramientas" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         **Entrada condiciones de** red en el **menú Más** herramientas  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abra el menú comando.  
          *   Seleccione `Control` + `Shift` + `P` \(Windows, Linux\) o `Command` + `Shift` + `P` \(macOS\).  
      1. Escriba `Network conditions` y elija Mostrar condiciones de **red**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Mostrar condiciones de red" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Mostrar condiciones de red**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Junto al **agente de usuario,** desactive la **casilla Seleccionar automáticamente.**  A continuación, **elija Personalizado...** para seleccionar de una lista de cadenas de agente de usuario predefinidas.  Para escribir su propia cadena de agente de usuario, escriba la cadena **en Entrar en un agente de usuario personalizado**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Establecer la cadena de agente de usuario en Microsoft Edge en macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Establecer la cadena de agente de usuario en Microsoft Edge en macOS  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Orden de aproximación - Primer orden - Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
