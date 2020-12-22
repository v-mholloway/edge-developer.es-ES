---
description: Familiarizarse con las herramientas para desarrolladores de Microsoft Edge (cromo)
title: Herramientas para desarrolladores de Microsoft Edge (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fcae8f0974244e87ba781b94221cb5d8a1bb3dce
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11235932"
---
# Información general de las herramientas de desarrollo de Microsoft Edge (cromo)  

Microsoft Edge ha adoptado el proyecto de código abierto de cromo para mejorar la compatibilidad web y la fragmentación de las distintas plataformas web subyacentes.  Este cambio debe facilitar la creación y la prueba de tus sitios web en Microsoft Edge y asegurarte de que cada uno funcione según lo esperado, aunque se vea en otro explorador basado en cromo \ (como Google Chrome, Vivaldi, opera o Brave \).  

A medida que la web ha crecido de uso en una amplia variedad de tipos de dispositivos, la complejidad y la carga de trabajo de los sitios web se han expandido. Como los programadores web \ (especialmente aquellos de pequeñas empresas \) deben probar muchos sistemas diferentes, puede que sea casi imposible garantizar que los sitios funcionen bien en todos los tipos de dispositivos y en todos los exploradores.  Ahora que Microsoft Edge está basado en cromo, el equipo de Microsoft Edge ha simplificado la matriz alineando la plataforma Microsoft Edge web con otros exploradores de cromo y proporcionó una experiencia de herramientas para programadores de la mejor calidad, tanto dentro del explorador como con las otras herramientas de desarrollador que usa todos los días \ (como Visual Studio Code \).  

Si va a retirar Microsoft Edge y principalmente desarrolla en un explorador basado en cromo, debe sentirse bien en casa.  Las herramientas para desarrolladores de Microsoft Edge \ (cromo \) funcionan de la misma manera que las herramientas para desarrolladores que ya conoces y usas.  Para obtener más información, vaya a [novedades de la DevTools Microsoft Edge (cromo)][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (cromo) DevTools" lightbox="./media/devtools.png":::
   Microsoft Edge (cromo) DevTools  
:::image-end:::  

Si desproteges el nuevo Microsoft Edge y ya desarrollaste en Microsoft Edge \ (EdgeHTML \), ahora tienes algunas fantásticas herramientas nuevas que hacen que sea más fácil y rápido crear y probar tus sitios web en Microsoft Edge.  

## Abrir la DevTools  

Si nunca antes usaste el DevTools, las herramientas para desarrolladores de Microsoft Edge son un conjunto de herramientas creadas directamente en el explorador Microsoft Edge.  Con el DevTools, podrás hacer lo siguiente.  

*   Inspeccionar y realizar cambios en el sitio web HTML  
*   Editar CSS y ver al instante cómo se representa el sitio web  
*   Consulta todas las `console.log()` instrucciones de tu código de JavaScript front-end  
*   Depure su script mediante la configuración de puntos de interrupción y su paso por línea  
    
Todo directamente en el explorador.  Estos son solo ejemplos de algunas de las características que DevTools proporcionar para que sea más fácil y rápida crear y probar sus sitios web en Microsoft Edge.  

Para abrir la DevTools  

*   Seleccionar `F12` 
*   Seleccione `Ctrl` + `Shift` + `I` on Windows/Linux \ ( `Command` + `Option` + `I` en MacOS \)  
    
Si desea ver el código HTML o CSS de un elemento de su sitio, haga clic con el botón derecho en el elemento y seleccione **inspeccionar** para ir al panel elementos.  También puede pulsar `Ctrl` + `Shift` + `C` en Windows/Linux \ ( `Command` + `Option` + `C` en MacOS \) para abrir la DevTools en el **modo de elemento de inspección** que le permite seleccionar un elemento del sitio y ver el código HTML y CSS en el panel **elementos** .  

Si desea ver los registros del código de JavaScript de front-end o ejecutar rápidamente algún script, seleccione `Ctrl` + `Shift` + `J` en Windows/Linux o `Command` + `Option` + `J` en MacOS para iniciar el panel de **consola** en el DevTools.  

## Herramientas básicas  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Herramientas de Microsoft Edge (cromo) DevTools Core" lightbox="./media/devtools-core-tools.png":::
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
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Envía tus [comentarios y solicitudes de características](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## Extensiones  

Es posible que hayas usado las extensiones de la DevTools para ayudarte a diagnosticar y depurar problemas al crear sitios web o aplicaciones.  Puede adquirir las extensiones para Microsoft Edge desde la página de [Complementos de Microsoft Edge][MicrosoftEdgeAddonsExtensions] .  Desde la página de [Complementos de Microsoft Edge][MicrosoftEdgeAddonsExtensions] , puede examinar las extensiones de DevTools desde la categoría **herramientas de desarrollo** o buscar una extensión específica.  

También puede Agregar extensiones desde la [tienda web de Chrome][GoogleChromeWebstoreExtensions].  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Tienda web de Chrome en Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Tienda web de Chrome en Microsoft Edge  
:::image-end:::  

En la parte superior, elija **permitir extensiones de otras tiendas** y, a continuación, elija **permitir** en el cuadro de diálogo que aparece.  

> [!NOTE]
> Las extensiones instaladas desde orígenes distintos de Microsoft Store no se han verificado y pueden afectar al rendimiento del explorador.  

Elija **Agregar a Chrome** para agregar la extensión de DevTools a Microsoft Edge.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Agregar extensión de la tienda web de Chrome a Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Agregar extensión de la tienda web de Chrome a Microsoft Edge  
:::image-end:::  

## Accesos directos  

Estos métodos abreviados controlan la ventana principal de DevTools, funcionan en todas las herramientas, o ambas.  

| Acción | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Mostrar u ocultar DevTools \(se abre en el último panel visualizado\) | `F12` ni `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Mostrar el panel de consola | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Mostrar la DevTools en el **modo de elemento de inspección** que le permite elegir un elemento del sitio y ver el código HTML y CSS en el panel **elementos** | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Mostrar configuración | `?` ni `Fn`+`F1` | `?` ni `Fn`+`F1` |  
| Mostrar el panel siguiente | `Ctrl`+`]` | `Command`+`]` |  
| Mostrar el panel anterior | `Ctrl`+`[` | `Command`+`[` |  
| Acople el DevTools en la última posición utilizada.  Si el DevTools permanece en la posición predeterminada para toda la sesión, el acceso directo desacopla la DevTools en una ventana independiente. | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Activar o desactivar el **modo de dispositivo** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Activar o desactivar **inspeccionar el modo de elemento** que le permite seleccionar un elemento del sitio y ver el código HTML y CSS en el panel **elementos** | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Mostrar el menú de comandos | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Mostrar u ocultar el cajón | `Esc` | `Esc` |  
| Actualizar  Fefreshes la página con la memoria caché.  | `F5` ni `Ctrl`+`R` | `Command`+`R` |  
| Actualización de hardware.  Fuerza a que Microsoft Edge Descargue los recursos de nuevo y vuelve a cargarlos.  Es posible que los recursos usados puedan proceder de una versión almacenada en caché | `Ctrl`+`F5` ni `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Buscar texto en el panel actual.  No es compatible con los paneles auditoría, aplicación y seguridad | `Ctrl`+`F` | `Command`+`F` |  
| Mostrar el panel de búsqueda en el cajón, que le permite buscar texto en todos los recursos cargados | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Abrir un archivo en el panel orígenes | `Ctrl`+`O` ni `Ctrl`+`P` | `Command`+`O` ni `Command`+`P` |  
| Acercar | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Alejar | `Ctrl`+`-` | `Command`+`-` |  
| Restaurar el nivel de zoom predeterminado | `Ctrl`+`0` | `Command`+`0` |  
| Ejecutar fragmento de código | `Ctrl`+`O`o bien `Ctrl` + `P` , escriba `!` seguido del nombre del script y, a continuación, pulse `Enter` | Presione `Command` + `O` o `Command` + `P` , escriba `!` seguido del nombre del script y, a continuación, pulse `Enter` |  
| Mostrar código fuente HTML no editable en una pestaña nueva | `Ctrl`+`U` | N/D |  

> [!NOTE]
> Si está depurando un punto de interrupción o pausado, el método abreviado de **actualización** reanuda primero el tiempo de ejecución.  

## Consulte también  

*   [DevTools para principiantes: Introducción a HTML y el DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Protocolo de DevTools Microsoft Edge (cromo)][DevtoolsProtocolChromiumIndex]  
    
## Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Si deseas obtener una vista previa de las [características más recientes que DevTools][DevtoolsGuideChromiumWhatsNewIndex], descarga [Microsoft Edge Canarias][MicrosoftedgeinsiderDownload], que se construye por la noche.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools para principiantes: Introducción a HTML y DOM | Microsoft docs"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/11/devtools "Novedades de Microsoft Edge (cromo) DevTools | Microsoft docs"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Protocolo de DevTools Microsoft Edge (cromo) | Microsoft docs"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Complementos de Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensiones | Tienda web de Chrome"  