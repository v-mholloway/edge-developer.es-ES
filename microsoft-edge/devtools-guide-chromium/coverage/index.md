---
title: Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: ebb8ae15a6888ce2227ec1dc18f307b03ddf9319
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601722"
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





# Buscar código JavaScript y CSS sin usar con la pestaña cobertura en Microsoft Edge DevTools   



La pestaña cobertura de Microsoft Edge DevTools ayuda a buscar código de JavaScript y CSS no usado.  Quitar el código no usado puede acelerar la carga de la página y guardar los datos celulares de los usuarios móviles.  

> ##### Figura 1  
> Analizar la cobertura de código  
> ![Analizar la cobertura de código][ImageExample]  

> [!WARNING]
> Encontrar un código no usado es relativamente fácil.  Pero refactorizar un código base para que cada página solo envíe el código JavaScript y CSS que necesita puede ser difícil.  En esta guía no se trata cómo refactorizar un código base para evitar el código no usado, ya que estos Refactores dependen enormemente de la pila tecnológica.  

## Introducción   

El envío de código JavaScript o CSS sin usar es un problema común en el desarrollo web.  Por ejemplo, supongamos que desea usar el [componente del botón bootstrap][BootstrapButtons] en la página.  Para usar el componente Button, necesita agregar un vínculo a la hoja de estilos bootstrap en el código HTML, como este:  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Esta hoja de estilos no incluye simplemente el código del componente de botón.  Contiene la CSS de **todos** los componentes de bootstrap.  Pero no usa ninguno de los otros componentes de bootstrap.  Por lo tanto, la página está descargando un montón de CSS que no necesita.  Esta CSS adicional es un problema por los siguientes motivos:  

*   El código adicional ralentiza la carga de la página.  <!--See [Render-Blocking CSS][render].  -->  
*   Si un usuario accede a la página en un dispositivo móvil, el código adicional usa sus datos móviles.  

<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## Abrir la pestaña cobertura   

1.  [Abrir el menú de comandos][DevToolsCommandMenu].  
1.  Comience `coverage` a escribir, seleccione el comando **Mostrar cobertura** y, a continuación, presione `Enter` para ejecutar el comando.  La pestaña **cobertura** se abre en el **cajón**.  

    > ##### Figura 2  
    > La ficha **cobertura**  
    > ![La ficha cobertura][ImageCoverage]  

## Registrar la cobertura de código   

1.  Haga clic en uno de los siguientes botones de la pestaña **cobertura** :  
    *   Haga clic en **empezar a instrumentar cobertura y volver a cargar página** ![ iniciar la cobertura de instrumentación y recargar página ][ImageReloadIcon] si desea ver qué código se necesita para cargar la página.  
    *   Haga clic en cobertura del instrumento de **cobertura del instrumento** ![ ][ImageRecordIcon] si desea ver qué código se usa después de interactuar con la página.  
1.  Haga clic en **detener la cobertura de la instrumentación y mostrar resultados** ![ detener la instrumentación de la cobertura y mostrar resultados ][ImageStopIcon] cuando desee detener la grabación de la cobertura de código.  

## Analizar la cobertura de código   

La tabla de la pestaña **cobertura** le muestra los recursos que se han analizado y la cantidad de código que se usa dentro de cada recurso. Haga clic en una fila para abrir ese recurso en el panel **orígenes** y ver un desglose línea por línea de código usado y código no usado.  

> ##### Imagen 3  
> Un informe de cobertura de código  
> ![Un informe de cobertura de código][ImageExample]  

*   La columna **URL** es la dirección URL del recurso que se analizó.  
*   En la columna **tipo** se indica si el recurso contiene CSS, JavaScript o ambos.  
*   La columna **total bytes** es el tamaño total del recurso en bytes.  
*   La columna **bytes no usados** es el número de bytes que no se han usado.  
*   La última columna sin nombre es una visualización de las columnas bytes **totales** y **bytes no usados** .  La sección roja de la barra es bytes no usados.  La sección verde es bytes usados.  

 



<!-- image links -->  

[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  
[ImageStopIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-icon.msft.png  

[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage.msft.png "Ilustración 1: analizar la cobertura de código"  
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/coverage-console-drawer-coverage-empty.msft.png "Ilustración 2: la pestaña cobertura"  
[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage-selected.msft.png "Ilustración 3: un informe de cobertura de código"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Ejecutar comandos con el menú de comandos de Microsoft Edge DevTools"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Botones: bootstrap"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/coverage/index) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
