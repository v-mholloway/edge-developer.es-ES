---
description: Conozca las herramientas para desarrolladores de Microsoft Edge (Chromium)
title: Herramientas para desarrolladores de Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/12/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 29ded7376ab1788998acf059c6677916a52d5d15
ms.sourcegitcommit: e29cd1c393fc1f433dba8c3d8f260b425ade63a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "11408279"
---
# <a name="microsoft-edge-chromium-developer-tools-overview"></a>Introducción a Microsoft Edge (Chromium) Developer Tools  

Microsoft Edge ha adoptado el proyecto de código abierto Chromium.  El nuevo explorador de Microsoft Edge crea una mejor compatibilidad web y reduce la fragmentación de diferentes plataformas web.  El cambio debe facilitar la compilación y prueba de las páginas web en Microsoft Edge.  El nuevo Microsoft Edge debe ayudar a que las páginas web funcionen según lo esperado cuando se abran en otros exploradores basados en Chromium.  Los exploradores basados en Chromium incluyen Google Chrome, Vivaldi, Opera, Brave y el nuevo Microsoft Edge.  

La web ha aumentado su uso en una matriz cada vez mayor de tipos de dispositivos.  La complejidad y la sobrecarga implicadas en las páginas web de pruebas han aumentado rápidamente.  Los desarrolladores web como usted deben probar con muchos sistemas diferentes.  Para asegurarte de que las páginas web funcionan bien en todos los tipos de dispositivos y exploradores, es posible que sea casi imposible, especialmente si trabajas en una pequeña empresa.  El nuevo Microsoft Edge ahora se basa en Chromium.  El equipo de Microsoft Edge ha simplificado la matriz alineando la plataforma web de Microsoft Edge con otros exploradores basados en Chromium.  El nuevo Microsoft Edge proporciona la mejor experiencia de desarrollo de su clase.  La experiencia se realiza dentro del explorador y junto con las otras herramientas para desarrolladores que usa todos los días, como Visual Studio código.  

Como desarrollador de explorador basado en Chromium, debes sentirte cómodo con el nuevo explorador de Microsoft Edge.  Microsoft Edge \(Chromium\) DevTools funciona igual que las herramientas para desarrolladores que ya conoces y usas.  Las Herramientas de desarrollo de Microsoft Edge \(Chromium\) a menudo se denominan Microsoft Edge \(Chromium\) DevTools o DevTools.  Para obtener más información, vaya a [Novedades de Microsoft Edge (Chromium) DevTools][DevtoolsGuideChromiumWhatsNewIndex].  

:::image type="complex" source="./media/devtools.png" alt-text="Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools.png":::
   Microsoft Edge (Chromium) DevTools  
:::image-end:::  

Si anteriormente desarrollaste para Microsoft Edge \(EdgeHTML\) y estás evaluando el nuevo Microsoft Edge, ahora proporciona nuevas y excelentes herramientas para crear y probar tus páginas web de forma más fácil y rápida.  

## <a name="open-the-devtools"></a>Abrir devTools  

Microsoft Edge DevTools es un conjunto de herramientas integradas directamente en el explorador Microsoft Edge.  DevTools permite realizar las siguientes tareas directamente en el explorador.  

*   Inspeccionar y realizar cambios en la página web HTML  
*   Editar CSS y ver al instante la vista previa de cómo se representa la página web  
*   Revisar todas las `console.log()` instrucciones del código JavaScript front-end  
*   Depurar el script, establecer puntos de interrupción y pasar por el código línea por línea  
    
Más ejemplos de las características que DevTools proporciona para que sea más fácil y rápido crear y probar su página web en Microsoft Edge.  

Para abrir DevTools  

*   Seleccionar `F12` 
*   Seleccione `Ctrl` + `Shift` + `I` \(Windows/Linux\) o `Command` + `Option` + `I` \(macOS\)  
    
Si desea ver el CÓDIGO HTML o CSS de un elemento en el sitio, haga clic con el botón secundario en el elemento y elija **Inspeccionar** para ir a la **herramienta** Elementos.  Para abrir DevTools en el modo de elemento **Inspect**, seleccione `Ctrl` + `Shift` + `C` \(Windows/Linux\) o `Command` + `Option` + `C` \(macOS\). El **modo de elemento Inspect** le permite elegir un elemento en la página web y mostrar el HTML y CSS en la **herramienta** Elementos.  

Si desea revisar los registros de su código JavaScript front-end o ejecutar rápidamente algún script, abra la **consola**.   Para iniciar la **herramienta consola** en DevTools, seleccione `Ctrl` + `Shift` + `J` \(Windows/Linux\) o `Command` + `Option` + `J` \(macOS\).  

## <a name="core-tools"></a>Herramientas básicas  

:::image type="complex" source="./media/devtools-core-tools.png" alt-text="Herramientas principales de Microsoft Edge (Chromium) DevTools" lightbox="./media/devtools-core-tools.png":::
   Herramientas principales de Microsoft Edge (Chromium) DevTools  
:::image-end::: 

Microsoft Edge \(Chromium\) DevTools incluye las siguientes herramientas.  

*   Una **herramienta Elements** para editar HTML y CSS, inspeccionar las propiedades de accesibilidad, ver escuchas de eventos y establecer puntos de interrupción de mutación dom  
*   Una **consola para** revisar y filtrar mensajes de registro, inspeccionar objetos JavaScript y nodos DOM y ejecutar JavaScript en el contexto de la ventana o marco seleccionados  
*   Herramienta **Orígenes** para abrir y editar el código, establecer puntos de interrupción, pasar por el código y mostrar el estado de la página web
*   Una **herramienta de** red para supervisar e inspeccionar solicitudes y respuestas de la red y la memoria caché del explorador   
*   Una **herramienta de** rendimiento para perfiles de la hora y los recursos del sistema necesarios para el sitio  
*   Una **herramienta de** memoria para medir el uso de recursos de memoria y comparar instantáneas de montón en distintos estados de tiempo de ejecución de código  
*   Una **herramienta de** aplicación para inspeccionar, modificar y depurar manifiestos de aplicaciones web, trabajadores de servicio y cachés de trabajadores de servicio.  También puede inspeccionar y administrar el almacenamiento, las bases de datos y las memorias caché desde la **herramienta Aplicación.**  
*   Una **herramienta de** seguridad para depurar problemas de seguridad y asegurarse de que ha implementado HTTPS correctamente en su página web.  HTTPS proporciona seguridad crítica e integridad de datos tanto para el sitio como para los usuarios que proporcionan información personal en el sitio.  
*   Una **herramienta Auditorías** \(ahora se ha cambiado el nombre **de Faro**\) para ejecutar una auditoría de la página web.  Los resultados de la auditoría le ayudan a mejorar la calidad del sitio de las siguientes maneras.  
    *   Detecta errores comunes relacionados con hacer que tu página web sea accesible, segura, con rendimiento, entre otros.  
    *   Corrección de cada error.  
    *   Cree un PWA.  
        
[!INCLUDE [audits-panel-note](./includes/audits-panel-note.md)]  

Envíe sus [comentarios y solicitudes de características](#getting-in-touch-with-the-microsoft-edge-devtools-team).  

## <a name="extensions"></a>Extensions  

Es posible que haya accedido a DevTools con extensiones al diagnosticar y depurar problemas mientras creó las páginas web \(o aplicaciones\). Las extensiones de Microsoft Edge se adquieren [a partir de complementos de Microsoft Edge][MicrosoftEdgeAddonsExtensions].  En [Complementos de Microsoft Edge,][MicrosoftEdgeAddonsExtensions]busque extensiones DevTools desde la categoría **Herramientas** para desarrolladores o busque una extensión específica.  

También puede agregar extensiones de [Chrome Web Store][GoogleChromeWebstoreExtensions].  

:::image type="complex" source="./media/allow-extensions-from-stores.png" alt-text="Chrome Web Store en Microsoft Edge" lightbox="./media/allow-extensions-from-stores.png":::
   Chrome Web Store en Microsoft Edge  
:::image-end:::  

En la parte superior, elija **Permitir extensiones de otros** almacenes y, a continuación, elija **Permitir** en el cuadro de diálogo que aparece.  

> [!NOTE]
> Las extensiones instaladas desde orígenes distintos de Microsoft Store no se han confirmado y pueden afectar al rendimiento del explorador.  

Elija **Agregar a Chrome** para agregar la extensión DevTools a Microsoft Edge.  

:::image type="complex" source="./media/install-extension-from-chrome-store.png" alt-text="Agregar extensión de Chrome Web Store a Microsoft Edge" lightbox="./media/install-extension-from-chrome-store.png":::
   Agregar extensión de Chrome Web Store a Microsoft Edge  
:::image-end:::  

## <a name="shortcuts"></a>Accesos directos  

Los siguientes métodos abreviados controlan la ventana principal de DevTools, funcionan en todas las herramientas o en ambas.  

| Acción | Windows/Linux | macOS |  
|:--- |:--- | :--- |  
| Mostrar/Ocultar DevTools \(se abre a la última herramienta vista\) | `F12` o `Ctrl`+`Shift`+`I` | `Command`+`Option`+`I` |  
| Mostrar la consola | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| Mostrar devTools en **modo de** elemento de inspección que le permite elegir un elemento y mostrar el HTML y CSS en la **herramienta** Elementos | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| Mostrar configuración | `?` o `Fn`+`F1` | `?` o `Fn`+`F1` |  
| Mostrar el panel siguiente | `Ctrl`+`]` | `Command`+`]` |  
| Mostrar el panel anterior | `Ctrl`+`[` | `Command`+`[` |  
| Acopla las DevTools en la última posición usada.  Si DevTools permanece en la posición predeterminada para toda la sesión, el acceso directo desacopla las DevTools en una ventana independiente | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| Alternar **modo de dispositivo** | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| Alternar **inspeccionar el modo de** elemento que le permite elegir un elemento y mostrar el HTML y CSS en la **herramienta** Elementos | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| Mostrar el menú de comandos | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| Mostrar/ocultar el cajón | `Esc` | `Esc` |  
| Actualizar  Actualiza la página web mediante la memoria caché.  | `F5` o `Ctrl`+`R` | `Command`+`R` |  
| Actualización dura.  Fuerza a Microsoft Edge a volver a descargar recursos y volver a cargarlos.  Los recursos que se usan pueden provienen de una versión almacenada en caché | `Ctrl`+`F5` o `Ctrl`+`Shift`+`R` | `Command`+`Shift`+`R` |  
| Busque texto en el panel actual.  No se admite en las herramientas auditorías, aplicaciones y seguridad | `Ctrl`+`F` | `Command`+`F` |  
| Mostrar la herramienta de búsqueda en el cajón, que le permite buscar texto en todos los recursos cargados | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| Abrir un archivo en el panel Orígenes | `Ctrl`+`O` o `Ctrl`+`P` | `Command`+`O` o `Command`+`P` |  
| Acercar | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| Alejar | `Ctrl`+`-` | `Command`+`-` |  
| Restaurar el nivel de zoom predeterminado | `Ctrl`+`0` | `Command`+`0` |  
| Ejecutar fragmento de código | `Ctrl`+`O`o `Ctrl` + `P` , escriba `!` seguido del nombre del script y, a continuación, seleccione `Enter` | Seleccione `Command` + `O` o , escriba seguido del nombre del script y, a `Command` + `P` `!` continuación, seleccione `Enter` |  
| Mostrar código fuente HTML no editable en una nueva pestaña | `Ctrl`+`U` | N/D |  

> [!NOTE]
> Si está depurando y pausado en un punto de interrupción, el método abreviado **Actualizar** reanuda primero el tiempo de ejecución.  

## <a name="see-also"></a>Consulte también  

*   [DevTools para principiantes: Introducción a HTML y DOM][DevtoolsGuideChromiumBeginnersHtml]  
*   [Protocolo DevTools de Microsoft Edge (Chromium)][DevtoolsProtocolChromiumIndex]  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contactar al equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

Si quieres obtener una vista previa de las características más recientes que llegan a [DevTools,][DevtoolsGuideChromiumWhatsNewIndex]descarga [Microsoft Edge Canary,][MicrosoftedgeinsiderDownload]que se compila por la noche.  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools para principiantes: Introducción a HTML y dom | Microsoft Docs"  
[DevtoolsGuideChromiumWhatsNewIndex]: /microsoft-edge/devtools-guide-chromium/whats-new/2021/02/devtools "Novedades de Microsoft Edge (Chromium) DevTools | Microsoft Docs"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Protocolo DevTools de Microsoft Edge (Chromium) | Microsoft Docs"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Complementos de Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Extensiones | Chrome Web Store"  
