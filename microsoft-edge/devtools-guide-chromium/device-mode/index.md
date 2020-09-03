---
description: Usa dispositivos virtuales en modo de dispositivo para que Microsoft Edge compile sitios web móviles.
title: Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: eababe8112b5d888671a8955e16f0fe1c89564fb
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993019"
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





# Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools   

  

Use el modo de dispositivo para aproximar el aspecto y el rendimiento de la página en un dispositivo móvil.  

El modo de dispositivo es el nombre de la colección floja de características de Microsoft Edge DevTools que le ayudan a simular dispositivos móviles.  Entre estas funciones se incluyen:  

*   [Simular un área de visualización móvil](#simulate-a-mobile-viewport)  
*   [Limitación de la red](#throttle-the-network-only)  
*   [Limitación de la CPU](#throttle-the-cpu-only)  
*   [Simulando geolocalización](#override-geolocation)  
*   [Establecer la orientación](#set-orientation)  

## Limitaciones   

Considere el modo de dispositivo como una [aproximación de primer orden][WikiApproximation] de la apariencia y el aspecto de su página en un dispositivo móvil.  Con el modo de dispositivo, no ejecutas el código en un dispositivo móvil.  Simula la experiencia de usuario móvil desde su equipo portátil o de escritorio.  

Hay algunos aspectos de los dispositivos móviles que DevTools nunca podrá simular.  Por ejemplo, la arquitectura de las CPU móviles es muy diferente de la arquitectura de las CPU de equipos portátiles o de escritorio.  Cuando tenga dudas, la mejor opción es ejecutar la página en un dispositivo móvil.  Use [depuración remota] [DevToolsRemoteDebugging] para ver, cambiar, depurar y perfilar el código de una página desde su equipo portátil o de escritorio mientras se ejecuta en un dispositivo móvil.  

## Simular un área de visualización móvil   

Haga clic en **Alternar barra de herramientas dispositivo** \ ( ![ Alternar barra de herramientas dispositivo ][ImageDeviceToolbarIcon] \) para abrir la interfaz de usuario que le permite simular un área de visualización móvil.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   La barra de herramientas del dispositivo  
:::image-end:::  

De forma predeterminada, la barra de herramientas del dispositivo se abre en modo de ventanilla eficaz.  

### Modo de ventanilla receptiva   

Arrastre los controladores para cambiar el tamaño de la ventanilla a cualquier dimensión que necesite.  O bien, escriba valores específicos en los cuadros ancho y alto.  En la siguiente ilustración, el ancho se establece en `626` y el alto se establece en `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica  
:::image-end:::  

#### Mostrar consultas multimedia   

Para mostrar los puntos de interrupción de la consulta multimedia encima de su ventanilla, haga clic en **más opciones** y seleccione **Mostrar consultas multimedia**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Mostrar consultas multimedia" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Mostrar consultas multimedia**  
:::image-end:::  

Haga clic en un punto de interrupción para cambiar el ancho de la ventanilla de modo que se desencadene el punto de interrupción.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla  
:::image-end:::  

#### Establecer el tipo de dispositivo   

Use la lista **tipo de dispositivo** para simular un dispositivo móvil o un dispositivo de escritorio.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Lista tipo de dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Lista **tipo de dispositivo**  
:::image-end:::  

En la tabla siguiente se describen las diferencias entre las opciones.  **Método de representación** hace referencia a si Microsoft Edge representa la página como un área de visualización de escritorio o móvil.  El **icono cursor** hace referencia al tipo de cursor que se ve al pasar el puntero por la página.  **Eventos desencadenados** hace referencia a si la página `touch` se desencadena o se produce un `click` evento al interactuar con la página.  

| Opción | Método de representación | Icono cursor | Eventos desencadenados |  
|:--- |:--- |:--- |:--- |  
| Móvil | Móvil | Círculo | Función táctil |  
| Móvil \ (sin contacto \) | Móvil | Normal |  haz clic en  |  
| Escritorio | Escritorio | Normal |  haz clic en  |  
| Escritorio \ (Touch \) | Escritorio | Círculo | Función táctil |  

> [!NOTE]
> Si no ve la lista **tipo de dispositivo** , haga clic en **más opciones** y seleccione **Agregar tipo de dispositivo**.  

### Modo de ventanilla de dispositivos móviles   

Para simular las dimensiones de un dispositivo móvil específico, seleccione el dispositivo en la lista de **dispositivos** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="La lista de dispositivos" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   La lista de **dispositivos**  
:::image-end:::  

#### Girar la ventanilla a la orientación horizontal   

Haga clic en **girar** \ ( ![ girar ][ImageRotateIcon] \) para girar la ventanilla a orientación horizontal.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Orientación horizontal" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   Orientación horizontal  
:::image-end:::  

> [!NOTE]
> El botón **girar** desaparecerá si la **barra de herramientas del dispositivo** es estrecha.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   La **barra de herramientas del dispositivo**  
:::image-end:::  

Consulte también [establecer orientación](#set-orientation).  

#### Mostrar marco del dispositivo   

Al simular las dimensiones de un dispositivo móvil específico, como un iPhone 6, Abra **más opciones** y, a continuación, seleccione **Mostrar marco del dispositivo** para mostrar el marco del dispositivo físico en la ventanilla.  

> [!NOTE]
> Si no ve un marco de dispositivo para un dispositivo en particular, significa que es probable que DevTools simplemente no tenga imágenes para esa opción específica.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Mostrar marco del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Mostrar marco del dispositivo  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="El marco del dispositivo para el iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         El marco del dispositivo para el iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Agregar un dispositivo móvil personalizado   

Para agregar un dispositivo personalizado:  

1.  Haga clic en la lista de **dispositivos** y seleccione **Editar**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Seleccione Editar" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Seleccione **Editar**  
    :::image-end:::  
    
1.  Haga clic en **Agregar dispositivo personalizado**.  
1.  Escriba un nombre, una anchura y un alto para el dispositivo.  La [relación de píxeles del dispositivo][MDNWindowDevicePixelRatio], la [cadena de agente de usuario][MDNUserAgent]y los campos de tipo de [dispositivo](#set-the-device-type) son opcionales.  El campo tipo de dispositivo es la lista que se establece en **móvil** de forma predeterminada.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Crear un dispositivo personalizado" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Crear un dispositivo personalizado  
    :::image-end:::  

### Mostrar reglas   

Haga clic en **más opciones** y, a continuación, seleccione **Mostrar reglas** para ver las reglas por encima y a la izquierda de su ventanilla.  La unidad de tamaño de las reglas es píxeles.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Mostrar reglas" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **Mostrar reglas**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Reglas por encima y a la izquierda de la ventanilla" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Reglas por encima y a la izquierda de la ventanilla  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Acercar la ventanilla   

Use la lista de **zoom** para acercar o alejar.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## Limitar la red y la CPU   

Para limitar la red y la CPU, seleccione teléfono móvil de **nivel intermedio** o **móvil de gama baja** de la lista **acelerador** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="La lista de aceleración" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   La lista de **aceleración**  
:::image-end:::  

El **teléfono móvil de nivel intermedio** simula una 3G rápida y acelera tu CPU para que sea 4 veces más lenta de lo normal.  Los **teléfonos móviles de low-end** simulan una 3G lenta y aceleran la CPU 6 veces más despacio de lo normal.  Tenga en cuenta que el límite es relativo a la capacidad normal de su equipo portátil o de escritorio.  

> [!NOTE]
> La lista de **aceleradores** se oculta si la **barra de herramientas del dispositivo** es estrecha.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="La barra de herramientas del dispositivo" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   La **barra de herramientas del dispositivo**  
:::image-end:::  

### Limitar solo la CPU   

Para limitar solo la CPU y no la red, vaya al panel **rendimiento** , haga clic en **configuración de captura** \ ![ (capturar configuración ][ImageCaptureIcon] \) y, a continuación, seleccione velocidad **lenta** o velocidad **6X** en la lista de **CPU** .  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Lista de CPU" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   Lista de **CPU**  
:::image-end:::  

### Limitar la velocidad de la red   

Para limitar solo la red y no la CPU, vaya al panel **red** y seleccione **3G rápido** o **3G lento** de la lista **acelerador** .  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="La lista de aceleración" lightbox="../media/device-mode-network-throttle.msft.png":::
   La lista de **aceleración**  
:::image-end:::  

O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el **menú de comandos**, escriba `3G` y seleccione **Habilitar aceleración 3G rápida** o **Habilitar limitación 3G lento**.  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="El menú de comandos" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   El **menú de comandos**  
:::image-end:::  

También puede establecer el límite de red en el panel **rendimiento** .  Haga clic en **configuración de captura** \ ( ![ capturar configuración ][ImageCaptureIcon] \) y, a continuación, seleccione **3G rápido** o **3G lento** de la lista de **redes** .  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Configurar el límite de red en el panel rendimiento" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   Configurar el límite de red en el panel **rendimiento**  
:::image-end:::  

## Invalidar geolocalización   

Para abrir la interfaz de usuario de reemplazo de ubicaciones, haga clic en **personalizar y control DevTools** \ ( `...` \) y, a continuación, seleccione **más**  >  **sensores**de herramientas.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **Sensores**  
:::image-end:::  

O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `Sensors` y, a continuación, seleccione **Mostrar sensores**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **Mostrar sensores**  
:::image-end:::  

Seleccione uno de los valores preestablecidos de la lista **ubicación geográfica** o seleccione **ubicación personalizada** para escribir sus propias coordenadas o seleccione **ubicación no disponible** para probar cómo se comporta la página cuando la geolocalización está en un estado de error.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Geolocalización" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **Geolocalización**  
:::image-end:::  

## Establecer orientación   

:::row:::
   :::column span="":::
      Para abrir la interfaz de usuario de orientación, haga clic en **personalizar y controle DevTools** `...` y, a continuación, seleccione **más**  >  **sensores**de herramientas.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Sensores" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Sensores**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `Sensors` y, a continuación, seleccione **Mostrar sensores**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Mostrar sensores" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Mostrar sensores**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Seleccione uno de los valores preestablecidos de la lista **orientación** o seleccione **orientación personalizada** para establecer sus propios valores alfa, beta y gamma.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Orientación" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **Orientación**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "Introducción a la depuración remota de dispositivos Android | Microsoft docs "  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agente de usuario | MDN"  

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
