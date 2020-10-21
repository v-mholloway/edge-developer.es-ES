---
description: Use dispositivos virtuales en Microsoft Edge para crear sitios web móviles.
title: Emular dispositivos móviles en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools, emulación, dispositivo, simulación, móvil
ms.openlocfilehash: 8b636a20fcb1c55630009031ec8bf300624d03d7
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125107"
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

# Emular dispositivos móviles en Microsoft Edge DevTools  

Use la **emulación de dispositivos** para aproximar el aspecto y la respuesta de la página en un dispositivo móvil.  El DevTools de Microsoft Edge proporciona una colección de características que te ayudan a emular dispositivos móviles.  La colección incluye las siguientes características.  

*   [Simular un área de visualización móvil](#simulate-a-mobile-viewport)  
*   [Limitar la red](#throttle-the-network-only)  
*   [Limitar la CPU](#throttle-the-cpu-only)  
*   [Simular geolocalización](#override-geolocation)  
*   [Establecer orientación](#set-orientation)  
*   [Establecer la cadena de agente de usuario](#set-user-agent-string)  

## Limitaciones  

La **emulación de dispositivos** es una [aproximación de primer orden][WikiApproximation] de la apariencia de la página en un dispositivo móvil.  La **emulación de dispositivos** realmente no ejecuta el código en un dispositivo móvil.  En su lugar, simula la experiencia de usuario móvil desde su equipo portátil o de escritorio.  

Algunos aspectos de los dispositivos móviles nunca se emulan en DevTools.  Por ejemplo, la arquitectura de las CPU móviles es diferente de la arquitectura de las CPU de equipos portátiles o de escritorio.  Cuando tenga dudas, la mejor opción es ejecutar la página en un dispositivo móvil.  Use [depuración remota] [DevToolsRemoteDebugging] para interactuar con el código de una página de su equipo mientras la página se ejecuta en un dispositivo móvil.  Puede ver, cambiar, depurar, perfil o los cuatro mientras interactúa con el código.  Su equipo puede ser un portátil o un equipo de escritorio.  

## Simular un área de visualización móvil  

Elija **alternar emulación de dispositivo**  \ ( ![ Alternar barra de herramientas de dispositivo ][ImageDeviceToolbarIcon] \) o elegir **personalizar y controlar DevTools** \ ( `...` \) > **emulación de dispositivo** para abrir la interfaz de usuario que le permite simular un área de visualización móvil.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    La barra de herramientas del dispositivo  
:::image-end:::  

De forma predeterminada, la barra de herramientas del dispositivo se abre en modo de ventanilla eficaz.  

### Modo de ventanilla receptiva  

Para probar rápidamente la apariencia de la página en varios tamaños de pantalla, arrastre los controladores para cambiar el tamaño de la ventanilla a las dimensiones necesarias.  También puede especificar valores específicos en los cuadros ancho y alto.  En la siguiente ilustración, el ancho se establece en `626` y el alto se establece en `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica  
:::image-end:::  

#### Mostrar consultas multimedia  

Si ha definido consultas multimedia en la página, vaya a las dimensiones de la ventanilla donde las consultas de medios surten efecto mostrando puntos de interrupción de consulta multimedia encima de su ventanilla.  Elija **más opciones**para  >  **Mostrar las consultas de medios**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Mostrar consultas multimedia**  
:::image-end:::  

Elija un punto de interrupción para cambiar el ancho de la ventanilla de modo que se desencadene la consulta multimedia.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Elegir un punto de interrupción para cambiar el ancho de la ventanilla  
:::image-end:::  

#### Establecer el tipo de dispositivo  

Use la lista **tipo de dispositivo** para simular un dispositivo móvil o un dispositivo de escritorio.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Lista **tipo de dispositivo**  
:::image-end:::  

En la siguiente tabla se describen las diferencias entre las opciones de tipo de dispositivo disponibles.  La columna método de representación hace referencia a si Microsoft Edge representa la página como un área de visualización de escritorio o móvil.  La columna icono del cursor hace referencia al tipo de cursor que se ve al pasar el puntero por la página.  La columna eventos desencadenados hace referencia a si la página `touch` se desencadena o `click` se desencadena cuando se interactúa con la página.  

| Opción | Método de representación | Icono cursor | Eventos desencadenados |  
|:--- |:--- |:--- |:--- |  
| Móvil | Móvil | Círculo | Función táctil |  
| Móvil \ (sin contacto \) | Móvil | Normal |  haz clic en  |  
| Escritorio | Escritorio | Normal |  haz clic en  |  
| Escritorio \ (Touch \) | Escritorio | Círculo | Función táctil |  

> [!NOTE]
> Si no se muestra la lista **tipo de dispositivo** , elija **más opciones**  >  **Agregar tipo de dispositivo**.  

### Modo de ventanilla de dispositivos móviles  

Para simular las dimensiones de un dispositivo móvil específico, seleccione el dispositivo en la lista de **dispositivos** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   La lista de **dispositivos**  
:::image-end:::  

#### Girar la ventanilla a la orientación horizontal  

Pruebe la página web con orientación horizontal.  

*   Para girar la ventanilla a orientación horizontal, elija **girar** \ ( ![ girar ][ImageRotateIcon] \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Página mostrada en orientación horizontal  
    :::image-end:::  
    
> [!NOTE]
> El botón **girar** desaparecerá si la **barra de herramientas del dispositivo** es estrecha.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   La **barra de herramientas del dispositivo**  
:::image-end:::  

Para obtener más información, vaya a [establecer orientación](#set-orientation).  

#### Mostrar marco del dispositivo  

Mostrar el marco del dispositivo físico en el área de visualización al simular las dimensiones de un dispositivo móvil específico, como un iPhone 6.  

1.  Abra **más opciones**.  
1.  Elija **Mostrar marco del dispositivo**.  

> [!NOTE]
> Si no ve un marco de dispositivo para un dispositivo en particular, significa que DevTools no tiene arte para esa opción.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Mostrar marco del dispositivo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         El marco del dispositivo para el iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### Agregar un dispositivo móvil personalizado  

Si la opción de dispositivo móvil que necesita no está incluida en la lista predeterminada, puede Agregar un dispositivo personalizado.  Para agregar un dispositivo personalizado, siga los pasos que se indican a continuación.  

1.  Elija la lista de **dispositivos** > **Editar**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Elija **Editar**  
    :::image-end:::  
    
1.  Elija **Agregar dispositivo personalizado**.  
1.  En **dispositivos emulados**, escriba un nombre de dispositivo, un ancho de pantalla y un alto de pantalla para el dispositivo personalizado.  La [relación de píxeles del dispositivo][MDNWindowDevicePixelRatio], la [cadena de agente de usuario][MDNUserAgent]y los campos de tipo de [dispositivo](#set-the-device-type) son opcionales.  El valor predeterminado del campo tipo de dispositivo es **móvil**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Crear un dispositivo personalizado  
    :::image-end:::  
    
### Mostrar reglas  

Si necesita medir las dimensiones de la pantalla, puede usar las reglas para medir el tamaño de la pantalla en píxeles.  Elija **más opciones**  >  para**Mostrar** las reglas para mostrar las reglas por encima y a la izquierda de su ventanilla.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Elemento de menú para mostrar las reglas  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Reglas por encima y a la izquierda de la ventanilla  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Acercar la ventanilla  

Para probar la apariencia de la página en varios niveles de zoom, use la lista de **zoom** para acercar o alejar.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## Limitar la red y la CPU  

Los dispositivos móviles suelen tener restricciones de red y de CPU.  Asegúrese de probar la rapidez con la que se carga la página y cómo responde a diferentes velocidades de Internet y de CPU.  

Limite la red y la CPU.  

1.  Elige la lista de **aceleración** y cambia el ajuste preestablecido a móvil **de nivel intermedio** o **móvil de low-end**.  
    *   El **teléfono móvil de nivel intermedio** simula `fast 3G` y acelera su CPU.  Es cuatro veces más lentas de lo normal.  
    *   La **tecnología móvil de gama baja** simula `slow 3G` y acelera su CPU.  Es seis veces más lento de lo normal.  
    
Todo el límite se basa en la capacidad normal de su equipo portátil o de escritorio.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Lista de **aceleradores** de la barra de herramientas del dispositivo  
:::image-end:::  

> [!NOTE]
> Si la **lista acelerador** está oculta, la **barra de herramientas del dispositivo** es demasiado estrecha.  Para obtener acceso a la **lista aceleradora**, aumente el ancho de la **barra de herramientas del dispositivo**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   La **barra de herramientas del dispositivo**  
:::image-end:::  

### Limitar solo la CPU  

Para limitar solo la CPU y no la red, complete los siguientes pasos.

1.  Elija el panel **rendimiento** y elija **configuración de captura** \ ( ![ configuración de captura ][ImageCaptureIcon] \).
1.  Elija **CPU**  >  **4x lentitud** o **ralentización 6**.
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       Lista de **CPU** en el panel **rendimiento**  
    :::image-end:::  
    
### Limitar la velocidad de la red  

Para limitar solo la red, siga los pasos que se indican a continuación.

1.  Elija el panel **red** .
1.  Elige 3G rápido **en línea**  >  **Fast 3G** o **3G lento**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-network-throttle.msft.png":::
       La lista de **aceleradores** en el panel red  
    :::image-end:::  
    
    O seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**, escriba `3G` y elija **Habilitar la limitación rápida de 3G** o habilitar la limitación de **3G**.  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       El **menú de comandos**  
    :::image-end:::  
    
También puede establecer el límite de red en el panel **rendimiento** .  

1.  Elija **configuración de captura** \ ( ![ configuración de captura ][ImageCaptureIcon] \) y seleccione la lista de **redes** y cambie el ajuste preestablecido a **3G rápido** o **3G lento**.  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Configurar el límite de red en el panel **rendimiento**  
    :::image-end:::  
    
## Reemplazar geolocalización  

:::row:::
   :::column span="":::
      Si su página depende de la información de geolocalización de un dispositivo móvil para representarse correctamente, proporcione geolocalización diferentes mediante la interfaz de usuario de reemplazo de geolocal.  

      1.  Elija **personalizar y controlar DevTools** \ ( `...` \) > **más**  >  **sensores**de herramientas.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores** de geolocalización  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abrir el menú de comandos.  
          *   Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \).  
      1. Escriba `Sensors` y elija **Mostrar sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar sensores** de geolocalización  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

En el panel **sensores** , puede seleccionar una de las ubicaciones preestablecidas incluidas en DevTools con el menú desplegable **Ubicación** .  Para escribir una ubicación personalizada, elija **otro...** e introduzca las coordenadas de la ubicación personalizada.  Para probar la página en estado de error cuando la información de ubicación no está disponible, elija **ubicación no disponible**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    Panel **sensores** con una ubicación preestablecida seleccionada.  
:::image-end:::

## Establecer orientación  

:::row:::
   :::column span="":::
      Si tu página depende de la información de orientación de un dispositivo móvil para representarla correctamente, abre la interfaz de usuario de orientación.  

      1.  Elija **personalizar y controlar DevTools** \ ( `...` \) > **más**  >  **sensores**de herramientas.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores** para orientación  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abrir el menú de comandos.  
          *   Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \).  
      1. Escriba `Sensors` y elija **Mostrar sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar sensores** para la orientación  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

En el panel **sensores** , puede seleccionar una orientación preestablecida en el menú desplegable **orientación** .  Para escribir su propia orientación, elija **orientación personalizada**y escriba sus propios valores de [alfa][MDNDeviceOrientaitonAlpha], [beta][MDNDeviceOrientaitonBeta]y [gamma][MDNDeviceOrientaitonGamma] .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    Opciones de **orientación** en el panel **sensores**  
:::image-end:::  

## Establecer cadena de agente de usuario  

:::row:::
   :::column span="":::
      Si la página depende de la cadena de agente de usuario de un dispositivo móvil para representarla correctamente, use el panel **condiciones de red** para proporcionar diferentes cadenas de agente de usuario.  
      
      1.  Elija **personalizar y controlar DevTools** \ ( `...` \) > **más herramientas**  >  **condiciones de red**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         Entrada de **condiciones de red** en el menú **más herramientas**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Abrir el menú de comandos.  
          *   Seleccione `Control` + `Shift` + `P` \ (Windows, Linux \) o `Command` + `Shift` + `P` \ (MacOS \).  
      1. Escriba `Network conditions` y elija **Mostrar condiciones de red**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Mostrar condiciones de red**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Junto a **agente de usuario**, desactive la casilla **seleccionar automáticamente** .  Después, elija **personalizado...** para seleccionar en una lista de cadenas de agente de usuario predefinidas.  Para introducir su propia cadena de agente de usuario, escriba la cadena en **Escriba un agente de usuario personalizado**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Establecer la cadena de agente de usuario en Microsoft Edge en macOS  
:::image-end:::  

## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "Introducción a la depuración remota de dispositivos Android | Microsoft docs "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. Alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. gamma | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Orden de aproximación-primer orden-Wikipedia"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
