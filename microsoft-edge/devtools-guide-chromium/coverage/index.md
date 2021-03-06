---
description: Cómo buscar y analizar código JavaScript y CSS sin usar en Microsoft Edge DevTools.
title: Buscar código JavaScript y CSS sin usar con el panel Cobertura en Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 092788606347352876483b1a8282fbb75b2bff66
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398766"
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

# <a name="find-unused-javascript-and-css-code-with-the-coverage-panel-in-microsoft-edge-devtools"></a>Buscar código JavaScript y CSS sin usar con el panel Cobertura en Microsoft Edge DevTools  

El panel **Cobertura** de Microsoft Edge DevTools le ayuda a encontrar código JavaScript y CSS sin usar.  La eliminación de código no usado puede acelerar la carga de la página y guardar los datos móviles de los usuarios móviles.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Análisis de la cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   Análisis de la cobertura de código  
:::image-end:::  

> [!WARNING]
> Encontrar código sin usar es relativamente fácil.  Pero refactorizar una base de código para que cada página solo incluye el JavaScript y CSS que necesita puede resultar difícil.  En esta guía no se explica cómo refactorizar una base de código para evitar el código no usado, ya que estos refactores dependen en gran medida de la pila de tecnología.  

## <a name="overview"></a>Introducción  

El envío de JavaScript o CSS sin usar es un problema común en el desarrollo web.  Por ejemplo, supongamos que desea usar el componente [de botón Bootstrap][BootstrapButtons] en la página.  Para usar el componente de botón, debe agregar un vínculo a la hoja de estilos de Bootstrap en su HTML, de esta forma:  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

Esta hoja de estilos no solo incluye el código del componente de botón.  Contiene el CSS para **todos los** componentes de Bootstrap.  Pero no está usando ninguno de los demás componentes de Bootstrap.  Por lo tanto, la página está descargando un montón de CSS que no necesita.  Este CSS adicional es un problema por los siguientes motivos.  

*   El código adicional ralentiza la carga de la página.  <!--Navigate to [Render-Blocking CSS][render].  -->  
*   Si un usuario accede a la página en un dispositivo móvil, el código adicional usa sus datos móviles.  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <a name="open-the-coverage-panel"></a>Abrir el panel Cobertura  

1.  [Abra el menú de comandos][DevToolsCommandMenu].  
1.  Empiece a `coverage` escribir , seleccione el comando Mostrar **cobertura** y, a continuación, seleccione para ejecutar `Enter` el comando.  El panel **Cobertura** se abre en el **cajón**.  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="El panel Cobertura" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       El panel **Cobertura**  
    :::image-end:::  
    
## <a name="record-code-coverage"></a>Cobertura de código de registro  

1.  Elija uno de los botones siguientes en **el** panel Cobertura.  
    *   Elija **Start Instrumenting Coverage and Reload Page** \( Start Instrumenting Coverage and Reload Page \) si desea revisar qué código es necesario ![ para cargar la ][ImageReloadIcon] página.  
    *   Elija **Cobertura de instrumento** \( Cobertura de instrumento \) si desea revisar qué código se usa después de interactuar con la ![ ][ImageRecordIcon] página.  
1.  Elija **Detener la cobertura de instrumentación y Mostrar** resultados \( Detener la cobertura de instrumentación y Mostrar ![ resultados \) cuando desee detener la grabación de la cobertura de ][ImageStopIcon] código.  
    
## <a name="analyze-code-coverage"></a>Analizar la cobertura de código  

La tabla del panel **Cobertura** muestra los recursos analizados y la cantidad de código que se usa en cada recurso.  Elija una fila para abrir ese recurso en el panel **Orígenes** y revise un desglose línea por línea del código usado y el código no usado.  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Un informe de cobertura de código" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   Un informe de cobertura de código  
:::image-end:::  

*   La **columna URL** es la dirección URL del recurso analizado.  
*   La **columna Tipo** indica si el recurso contiene CSS, JavaScript o ambos.  
*   La **columna Bytes totales** es el tamaño total del recurso en bytes.  
*   La **columna Bytes sin** usar es el número de bytes que no se usaron.  
*   La última columna sin nombre es una visualización de las columnas **Bytes totales** y **Bytes no** usados.  La sección roja de la barra es bytes no usados.  La sección verde se usa bytes.  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Ejecute comandos con el menú Comando de Microsoft Edge DevTools | Microsoft Docs"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Botones - Bootstrap"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/coverage/index) y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
