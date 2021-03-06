---
description: Con F12 Developer Tools, aprenda a depurar el script en segundo plano, los scripts de contenido y las páginas de extensión de una extensión.
title: Depuración | Extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, javascript, developer, debug, debugging
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a23c7558080cca7671cdfc9790705a8d8c9ed705
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399368"
---
# <a name="debugging-extensions"></a>Depuración de extensiones  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Puede depurar las extensiones en Microsoft Edge mediante F12 Developer Tools.  

El siguiente vídeo pasa por una extensión de Microsoft Edge con errores, paseando por cada escenario de depuración y corrigiendo el camino.  Consulta las instrucciones paso a paso que aparecen a continuación para obtener más información.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]  

> [!NOTE]
> Para aprovechar la depuración de extensiones con F12, primero debe activar las características del desarrollador en about:flags.  Consulte [Agregar y quitar extensiones para](./adding-and-removing-extensions.md) obtener más información sobre cómo hacerlo.  

## <a name="background-script-debugging"></a>Depuración de scripts en segundo plano  

Para empezar a depurar el script en segundo plano de la extensión:  

1.  Haga clic **en Más (...)** seguido de **Extensiones** para ir al panel de extensiones.  
    
    ![botón más](../media/morebutton.png)  
    
1.  Haga clic en la extensión que desea depurar.  
1.  Haga clic en **el vínculo Página en** segundo plano para mostrar F12 para el proceso en segundo plano.  
    
    ![vista de extensión seleccionada de las opciones con vínculo inspeccionar](../media/debug-inspect.png)  
    
1.  Seleccione la **pestaña Depurador** en F12.  
1.  Vaya a y seleccione el script en segundo plano de la extensión.  
1.  Coloque puntos de interrupción para la depuración haciendo clic a la izquierda del número de línea de código fuente.  
    
    ![Consola f12 que muestra script en segundo plano con puntos de interrupción](../media/debug-f12-background.png)  
    
1.  Seleccione la **pestaña Consola** y ejecute el `location.reload()` comando.  Esto volverá a ejecutar el script en segundo plano, lo que le permitirá pasar por el código.  
    
    ![consola con location.reload escrito](../media/debug-f12-background-console.png)  
    
## <a name="content-script-debugging"></a>Depuración de scripts de contenido  

Para empezar a depurar el script de contenido de la extensión:  

1.  Inicie F12 navegando al botón **Más (...)** y **seleccionando F12 Developer Tools** o presionando en el `F12` teclado.  
1.  Vaya a y seleccione el script de contenido de la extensión.  Los scripts de contenido de las extensiones que se están ejecutando actualmente se representarán en una carpeta diferente para cada extensión.  
    
    > [!NOTE]
    > Solo aparecerán scripts de contenido en ejecución.  
    
1.  Coloque puntos de interrupción para la depuración haciendo clic a la izquierda del número de línea de código fuente.  
    
    ![f12 con script de contenido que se está depurando](../media/debug-content-f12.png)  
    
1.  Actualice la pestaña del explorador para empezar a pasar por el código.  
    
## <a name="extension-page-debugging"></a>Depuración de páginas de extensión  

Existen dos métodos que se pueden usar para obtener acceso al código fuente de la página de extensión para la depuración.  Un método se aplica a una variedad de páginas mientras que el otro solo funciona para páginas emergentes.  

### <a name="debugging-any-extension-page"></a>Depurar cualquier página de extensión  

El siguiente método funciona para todas las páginas de extensión, como la página de opciones y los elementos emergentes:  

1.  Haga clic con el botón secundario en el fondo de la página.  
1.  Seleccione **Ver origen**.  
    
    ![Abrir depuración emergente con f12](../media/debug-popup-select.png)  
    
1.  Una vez que se abra F12, coloque los puntos de interrupción en el archivo que desea depurar.  
    
    ![depuración emergente con f12](../media/debug-popup-f12.png)  
    
1.  Seleccione la **pestaña Consola** y ejecute el comando `location.reload()` .  Esto volverá a ejecutar el script de página, lo que le permitirá pasar por el código.  
    
    ![consola con location.reload escrito](../media/debug-f12-background-console.png)  
    
### <a name="debugging-a-popup-extension-page"></a>Depurar una página de extensión emergente  

Aunque el método para depurar páginas de extensión también se aplica a las páginas de extensión emergentes, los pasos siguientes describen otra forma de depurar el elemento emergente:  

1.  Haga clic con el botón secundario en el icono de la extensión.  
1.  Seleccione **Inspeccionar elemento emergente**.  
    
    ![inspección de depuración emergente](../media/debug-popup-inspect.png)  
    
1.  Siga los pasos 3 y 4 anteriores para colocar puntos de interrupción y volver a cargar el elemento emergente.  
    