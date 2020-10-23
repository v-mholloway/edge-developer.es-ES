---
description: Familiarizarse con las herramientas para desarrolladores de Microsoft Edge (cromo)
title: Herramientas para desarrolladores de Microsoft Edge (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 9f035df5bc80aa6a1df0464eb326e4185e2205d2
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/23/2020
ms.locfileid: "11133907"
---
# Herramientas para desarrolladores de Microsoft Edge (cromo)  

Microsoft Edge ha adoptado el proyecto de código abierto de cromo para mejorar la compatibilidad web y la fragmentación de las distintas plataformas web subyacentes.  Este cambio debe facilitar la creación y la prueba de tus sitios web en Microsoft Edge y asegurarte de que cada uno funcione según lo esperado, aunque se vea en otro explorador basado en cromo \ (como Google Chrome, Vivaldi, opera o Brave \).  

A medida que la web ha crecido de uso en una amplia variedad de tipos de dispositivos, la complejidad y la carga de trabajo de los sitios web se han expandido. Como los programadores web \ (especialmente aquellos de pequeñas empresas \) deben probar muchos sistemas diferentes, puede que sea casi imposible garantizar que los sitios funcionen bien en todos los tipos de dispositivos y en todos los exploradores.  Ahora que Microsoft Edge está basado en cromo, el equipo de Microsoft Edge ha simplificado la matriz alineando la plataforma Microsoft Edge web con otros exploradores de cromo y proporcionó una experiencia de herramientas para programadores de la mejor calidad, tanto dentro del explorador como con las otras herramientas de desarrollador que usa todos los días \ (como Visual Studio Code \).  

Si va a retirar Microsoft Edge y principalmente desarrolla en un explorador basado en cromo, debe sentirse bien en casa.  Las herramientas para desarrolladores de Microsoft Edge \ (cromo \) funcionan de la misma manera que las herramientas para desarrolladores que ya conoces y usas.  Para obtener más información, vea [novedades de la DevTools de Microsoft Edge (cromo)][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./devtools-guide-chromium/media/devtools.png" alt-text="Microsoft Edge (cromo) DevTools":::
   Microsoft Edge (cromo) DevTools  
:::image-end:::  

Si estás desprotegiendo la siguiente versión de Microsoft Edge y ya desarrollaste en Microsoft Edge \ (EdgeHTML \), ahora tienes algunas fantásticas herramientas nuevas que hacen que sea más fácil y más rápido crear y probar tus sitios web en Microsoft Edge.  

## Abrir la DevTools  

Si nunca antes usaste el DevTools, las herramientas para desarrolladores de Microsoft Edge son un conjunto de herramientas creadas directamente en el explorador Microsoft Edge.  Con estas DevTools, podrás hacer lo siguiente.  

*   Inspeccionar y realizar cambios en el sitio web HTML  
*   Editar CSS y ver al instante cómo se representa el sitio web  
*   Consulta todas las `console.log()` instrucciones de tu código de JavaScript front-end  
*   Depure su script mediante la configuración de puntos de interrupción y su paso por línea  

todo directamente en el explorador.  Estos son solo ejemplos de algunas de las características que DevTools proporcionar para que sea más fácil y rápida crear y probar sus sitios web en Microsoft Edge.  

Para abrir la DevTools  

*   Mantenga `F12` 
*   Pulse `Ctrl` + `Shift` + `I` en Windows/Linux \ ( `Command` + `Option` + `I` en MacOS \)  

Si desea ver el código HTML o CSS de un elemento de su sitio, haga clic con el botón derecho en el elemento y seleccione **inspeccionar** para ir al panel elementos.  También puede pulsar `Ctrl` + `Shift` + `C` en Windows/Linux \ ( `Command` + `Option` + `C` en MacOS \) para abrir la DevTools en el **modo de elemento de inspección** que le permite seleccionar un elemento del sitio y ver el código HTML y CSS en el panel **elementos** .  

Si desea ver los registros del código de JavaScript de front-end o ejecutar rápidamente algún script, pulse `Ctrl` + `Shift` + `J` en Windows/Linux o `Command` + `Option` + `J` en MacOS para iniciar el panel de consola en el DevTools.  

## Herramientas básicas  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-core-tools.png" alt-text="Microsoft Edge (cromo) DevTools":::
   Herramientas de Microsoft Edge (cromo) DevTools Core  
:::image-end::: 

La DevTools Microsoft Edge \ (cromo \) incluye los siguientes paneles.  

*   Un **panel de elementos** para editar HTML y CSS, inspeccionar propiedades de accesibilidad, visualizar escuchas de eventos y definir puntos de interrupción de mutación de DOM  
*   Una **consola** para ver y filtrar los mensajes de registro, inspeccionar objetos de JavaScript y nodos de DOM y ejecutar JavaScript en el contexto de la ventana o marco seleccionados  
*   Panel **orígenes** para abrir y editar en vivo el código, establecer puntos de interrupción, recorrer el código y ver el estado de su sitio web una línea de JavaScript a la vez  
*   Un panel de **red** para supervisar e inspeccionar las solicitudes y respuestas de la red y de la memoria caché del explorador   
*   Un panel de **rendimiento** para generar perfiles de tiempo y de los recursos del sistema necesarios para su sitio  
*   Un panel de **memoria** para medir su uso de los recursos de memoria y comparar instantáneas de pila en diferentes estados del tiempo de ejecución de código.  
*   Un panel de **aplicación** para inspeccionar, modificar y depurar manifiestos de aplicaciones Web, trabajos de servicios y cachés de trabajos de servicios.  También puede inspeccionar y administrar almacenamiento, bases de datos y memorias caché desde el panel **aplicación** .  
*   Un panel de **seguridad** para depurar problemas de seguridad y asegurarse de que ha implementado correctamente HTTPS en su sitio Web.  HTTPS proporciona seguridad crítica e integridad de datos tanto para el sitio como para los usuarios que proporcionen información personal en su sitio.  
*   Un panel de **Auditoría** \ (ahora con el nombre **Lighthouse**\) para ejecutar una auditoría de tu sitio Web.  Los resultados de la auditoría le ayudan a mejorar la calidad de su sitio de la siguiente manera.  
    *   Detecta errores comunes relacionados con hacer que tu sitio web sea accesible, seguro, de rendimiento, etc.  
    *   Corrija cada error.  
    *   Crear un PWA.  

[!INCLUDE [audits-panel-note](./devtools-guide-chromium/includes/audits-panel-note.md)]  

Envía tus [comentarios y solicitudes de características](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Extensions  

Es posible que hayas usado las extensiones de la DevTools para ayudarte a diagnosticar y depurar problemas al crear sitios web o aplicaciones.  Puede adquirir las extensiones para Microsoft Edge desde la página de [Complementos de Microsoft Edge][MicrosoftEdgeAddonsExtensions] .  Desde la página de [Complementos de Microsoft Edge][MicrosoftEdgeAddonsExtensions] , puede examinar las extensiones de DevTools desde la categoría **herramientas de desarrollo** o buscar una extensión específica.  

También puede Agregar extensiones desde la [tienda web de Chrome][GoogleChromeWebstoreExtensions].  

:::image type="complex" source="./devtools-guide-chromium/media/allow-extensions-from-stores.png" alt-text="Microsoft Edge (cromo) DevTools":::
   Tienda web de Chrome en Microsoft Edge  
:::image-end:::  

En la parte superior, seleccione **permitir extensiones de otras tiendas** y, a continuación, seleccione **permitir** en el cuadro de diálogo que aparece.  

> [!NOTE]
> Las extensiones instaladas desde orígenes distintos de Microsoft Store no se han verificado y pueden afectar al rendimiento del explorador.  

Seleccione **Agregar a Chrome** para agregar la extensión de DevTools a Microsoft Edge.  

:::image type="complex" source="./devtools-guide-chromium/media/install-extension-from-chrome-store.png" alt-text="Microsoft Edge (cromo) DevTools"  
