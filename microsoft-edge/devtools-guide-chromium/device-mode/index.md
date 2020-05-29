---
title: Simular dispositivos móviles con el modo de dispositivo en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607429"
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

Haga clic en **activar o** desactivar la barra de herramientas dispositivo ![ ][ImageDeviceToolbarIcon] para abrir la interfaz de usuario que le permite simular un área de visualización móvil.  

> ##### Figura 1  
> La barra de herramientas del dispositivo  
> ![La barra de herramientas del dispositivo][ImageDeviceToolbar]  

De forma predeterminada, la barra de herramientas del dispositivo se abre en modo de ventanilla eficaz.  

### Modo de ventanilla receptiva   

Arrastre los controladores para cambiar el tamaño de la ventanilla a cualquier dimensión que necesite.  O bien, escriba valores específicos en los cuadros ancho y alto.  En la [ilustración 2](#figure-2), el ancho se establece en `626` y el alto se establece en `516` .  

> ##### Figura 2  
> Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica  
> ![Los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla dinámica][ImageResponsiveHandles]  

#### Mostrar consultas multimedia   

Para mostrar los puntos de interrupción de la consulta multimedia encima de su ventanilla, haga clic en **más opciones** y seleccione **Mostrar consultas multimedia**.  

> ##### Imagen 3  
> Mostrar consultas multimedia  
> ![Mostrar consultas multimedia][ImageShowMediaQueries]  

Haga clic en un punto de interrupción para cambiar el ancho de la ventanilla de modo que se desencadene el punto de interrupción.  

> ##### Imagen 4  
> Hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla  
> ![Hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla][ImageBreakpoint]  

#### Establecer el tipo de dispositivo   

Use la lista **tipo de dispositivo** para simular un dispositivo móvil o un dispositivo de escritorio.  

> ##### Imagen 5  
> Lista **tipo de dispositivo**  
> ![Lista tipo de dispositivo][ImageDeviceType]  

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

> ##### Imagen 6  
> La lista de dispositivos  
> ![La lista de dispositivos][ImageDeviceList]  

#### Girar la ventanilla a la orientación horizontal   

Haga clic en **girar** ![ girar ][ImageRotateIcon] para girar la ventanilla a orientación horizontal.  

> ##### Imagen 7  
> Orientación horizontal  
> ![Orientación horizontal][ImageLandscape]  

> [!NOTE]
> El botón **girar** desaparecerá si la **barra de herramientas del dispositivo** es estrecha.  

> ##### Imagen 8  
> La barra de herramientas del dispositivo  
> ![La barra de herramientas del dispositivo][ImageDeviceToolbar2]  

Consulte también [establecer orientación](#set-orientation).  

#### Mostrar marco del dispositivo   

Al simular las dimensiones de un dispositivo móvil específico, como un iPhone 6, Abra **más opciones** y, a continuación, seleccione **Mostrar marco del dispositivo** para mostrar el marco del dispositivo físico en la ventanilla.  

> [!NOTE]
> Si no ve un marco de dispositivo para un dispositivo en particular, significa que es probable que DevTools simplemente no tenga imágenes para esa opción específica.  

> ##### Imagen 9  
> Mostrar marco del dispositivo  
> ![Mostrar marco del dispositivo][ImageShowDeviceFrame]  

> ##### Imagen 10  
> El marco del dispositivo para el iPhone 6  
> ![El marco del dispositivo para el iPhone 6][ImageIphoneFrame]  

#### Agregar un dispositivo móvil personalizado   

Para agregar un dispositivo personalizado:  

1.  Haga clic en la lista de **dispositivos** y seleccione **Editar**.  

> ##### Imagen 11  
> Selección de **Editar**, 
> ![ selección de edición][ImageEdit]  

1.  Haga clic en **Agregar dispositivo personalizado**.  

1.  Escriba un nombre, una anchura y un alto para el dispositivo.  La [relación de píxeles del dispositivo][MDNWindowDevicePixelRatio], la [cadena de agente de usuario][MDNUserAgent]y los campos de tipo de [dispositivo](#set-the-device-type) son opcionales.  El campo tipo de dispositivo es la lista que se establece en **móvil** de forma predeterminada.  

> ##### Imagen 12  
> Crear un dispositivo personalizado  
> ![Crear un dispositivo personalizado][ImageAddCustomDevice]  

### Mostrar reglas   

Haga clic en **más opciones** y, a continuación, seleccione **Mostrar reglas** para ver las reglas por encima y a la izquierda de su ventanilla.  La unidad de tamaño de las reglas es píxeles.  

> ##### Imagen 13  
> Mostrar reglas  
> ![Mostrar reglas][ImageShowRulers]  

> ##### Imagen 14  
> Reglas por encima y a la izquierda de la ventanilla  
> ![Reglas por encima y a la izquierda de la ventanilla][ImageRulers]  

### Acercar la ventanilla   

Use la lista de **zoom** para acercar o alejar.  

> ##### Imagen 15  
> Zoom  
> ![Zoom][ImageZoomViewport]  

## Limitar la red y la CPU   

Para limitar la red y la CPU, seleccione teléfono móvil de **nivel intermedio** o **móvil de gama baja** de la lista **acelerador** .  

> ##### Imagen 16  
> La lista de aceleración  
> ![La lista de aceleración][ImageThrottling]  

El **teléfono móvil de nivel intermedio** simula una 3G rápida y acelera tu CPU para que sea 4 veces más lenta de lo normal.  Los **teléfonos móviles de low-end** simulan una 3G lenta y aceleran la CPU 6 veces más despacio de lo normal.  Tenga en cuenta que el límite es relativo a la capacidad normal de su equipo portátil o de escritorio.  

> [!NOTE]
> La lista de **aceleradores** se ocultará si la **barra de herramientas del dispositivo** es estrecha.  

> ##### Imagen 17  
> La barra de herramientas del dispositivo  
> ![La barra de herramientas del dispositivo][ImageDeviceToolbar3]  

### Limitar solo la CPU   

Para limitar solo la CPU y no la red, vaya al panel **rendimiento** , haga clic en **capturar** ajustes de ![ captura configuración ][ImageCaptureIcon] y, a continuación, seleccione velocidad **lenta** o velocidad **6. disminución** de la lista de **CPU** .  

> ##### Ilustración 18  
> Lista de CPU  
> ![Lista de CPU][ImageCPU]  

### Limitar la velocidad de la red   

Para limitar solo la red y no la CPU, vaya al panel **red** y seleccione **3G rápido** o **3G lento** de la lista **acelerador** .  

> ##### Ilustración 19  
> La lista de aceleración  
> ![La lista de aceleración][ImageNetwork]  

O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `3G` y seleccione **Habilitar aceleración 3G rápida** o **Habilitar limitación 3G lento**.  

> ##### Ilustración 20  
> El menú de comandos  
> ![El menú de comandos][ImageCommandMenu]  

También puede establecer el límite de red en el panel **rendimiento** .  Haga clic en **capturar** ![ configuración ][ImageCaptureIcon] de captura y, a continuación, seleccione **3G rápido** o **3G lento** de la lista de **redes** .  

> ##### Ilustración 21  
> Configurar el límite de red en el panel rendimiento  
> ![Configurar el límite de red en el panel rendimiento][ImageNetwork2]  

## Invalidar geolocalización   

Para abrir la interfaz de usuario de reemplazo de ubicaciones, haga clic en **personalizar y controle DevTools** `...` y, a continuación, seleccione **más**  >  **sensores**de herramientas.  

> ##### Ilustración 22  
> Sensores  
> ![Sensores][ImageSensors]  

O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `Sensors` y, a continuación, seleccione **Mostrar sensores**.  

> ##### Ilustración 23  
> Mostrar sensores  
> ![Mostrar sensores][ImageShowSensors]  

Seleccione uno de los valores preestablecidos de la lista **ubicación geográfica** o seleccione **ubicación personalizada** para escribir sus propias coordenadas o seleccione **ubicación no disponible** para probar cómo se comporta la página cuando la geolocalización está en un estado de error.  

> ##### Ilustración 24  
> Geolocalización  
> ![Geolocalización][ImageGeolocation]  

## Establecer orientación   

Para abrir la interfaz de usuario de orientación, haga clic en **personalizar y controle DevTools** `...` y, a continuación, seleccione **más**  >  **sensores**de herramientas.  

> ##### Ilustración 25  
> Sensores  
> ![Sensores][ImageSensors2]  

O pulse `Control` + `Shift` + `P` \ (Windows \) o `Command` + `Shift` + `P` \ (MacOS \) para abrir el menú de comandos, escriba `Sensors` y, a continuación, seleccione **Mostrar sensores**.  

> ##### Ilustración 26  
> Mostrar sensores  
> ![Mostrar sensores][ImageShowSensors2]  

Seleccione uno de los valores preestablecidos de la lista **orientación** o seleccione **orientación personalizada** para establecer sus propios valores alfa, beta y gamma.  

> ##### Ilustración 27  
> Orientación  
> ![Orientación][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Ilustración 1: la barra de herramientas del dispositivo"  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Ilustración 2: los controladores para cambiar las dimensiones del área de visualización en el modo de ventanilla con capacidad de respuesta"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Ilustración 3: mostrar las consultas multimedia"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Ilustración 4: hacer clic en un punto de interrupción para cambiar el ancho de la ventanilla"  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Ilustración 5: lista tipo de dispositivo"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Ilustración 6: la lista de dispositivos"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Ilustración 7: orientación horizontal"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Ilustración 8: la barra de herramientas del dispositivo"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Ilustración 9: Mostrar marco del dispositivo"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Ilustración 10: el marco del dispositivo para iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Ilustración 11: selección de edición"  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Ilustración 12: crear un dispositivo personalizado"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Ilustración 13: mostrar las reglas"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Ilustración 14: reglas por encima y a la izquierda de la ventanilla"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Ilustración 15: zoom"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Ilustración 16: la lista de aceleración"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Ilustración 17: la barra de herramientas del dispositivo"  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Ilustración 18: la lista de CPU"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "Ilustración 19: la lista de aceleración"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Ilustración 20: el menú de comandos"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Ilustración 21: configuración del límite de red en el panel rendimiento"  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Ilustración 22: sensores"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Ilustración 23: Mostrar sensores"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Ilustración 24: geolocalización"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Ilustración 25: sensores"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Ilustración 26: Mostrar sensores"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Ilustración 27: orientación"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/DevTools-Guide-Chromium/Remote-Debugging/index "Introducción a la depuración remota de dispositivos Android"  

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
