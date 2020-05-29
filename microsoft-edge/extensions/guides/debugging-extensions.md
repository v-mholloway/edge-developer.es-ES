---
description: Con las herramientas de desarrollo F12, aprenda a depurar el script de fondo de una extensión, los scripts de contenido y las páginas de extensión.
title: Extensiones-depuración
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, JavaScript, desarrollador, depuración, depuración
ms.custom: seodec18
ms.openlocfilehash: 34488870cb4e4a92a9d57859509ce7d1176cf284
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573636"
---
# Extensiones de depuración  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Puede depurar las extensiones en Microsoft Edge con las herramientas de desarrollo F12.

El siguiente vídeo pasa por una extensión de Microsoft Edge con errores, caminar a través de cada escenario de depuración y corregirlo a lo largo del camino. Para obtener más información, consulta las instrucciones paso a paso más adelante.

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> Para aprovechar las ventajas de la depuración de la extensión con F12, primero debe activar las características para desarrolladores en about: Flags. Consulte [Agregar y quitar extensiones](./adding-and-removing-extensions.md) para obtener más información sobre cómo hacerlo.


## Depuración de script de fondo
Para empezar a depurar el script de fondo de su extensión:

1. Haga clic en **más (...)** seguido de **extensiones** para ir al panel de extensiones.  
 ![botón más](./../media/morebutton.png)
2. Haga clic en la extensión que desea depurar.
3. Haga clic en el vínculo de la **Página de fondo** para que se muestre F12 para el proceso en segundo plano.  
 ![vista de extensión seleccionada de las opciones con el vínculo de inspección](./../media/debug-inspect.png)
4. Seleccione la pestaña **depurador** en F12.
5. Navegue hasta el script de fondo de la extensión y selecciónelo.
6. Coloque puntos de interrupción para la depuración haciendo clic a la izquierda del número de línea del código de origen.  
 ![consola F12 que muestra el script de fondo con puntos de interrupción](./../media/debug-f12-background.png)
7. Seleccione la ficha **Console (consola** ) y ejecute el comando " `location.reload()` ". Esto volverá a ejecutar el script de fondo, lo que le permitirá recorrer el código.  
 ![consola con ubicación. recarga introducida](./../media/debug-f12-background-console.png)


## Depuración de script de contenido
Para empezar a depurar el script de contenido de la extensión:

1. Para iniciar F12, navegue hasta el botón **más (...)** y seleccione **"herramientas para desarrolladores F12"** o presione F12 en el teclado.
2. Desplácese hasta el script de contenido de la extensión y selecciónelo. Los scripts de contenido para las extensiones que se están ejecutando se representarán mediante una carpeta diferente para cada extensión.

    > [!NOTE]
    > Solo aparecerán los scripts de contenido en ejecución.

3. Coloque puntos de interrupción para la depuración haciendo clic a la izquierda del número de línea del código de origen.  
 ![F12 con secuencia de comandos de contenido en proceso de depuración](./../media/debug-content-f12.png)
4. Actualice la pestaña del explorador para empezar a desplazarse por el código.




## Depuración de la página de extensión

Hay dos métodos que se pueden usar para obtener acceso al código fuente de la página de extensión para la depuración. Un método se aplica a varias páginas, mientras que la otra solo funciona con páginas emergentes.

### Depurar cualquier página de extensión
El siguiente método funciona para todas las páginas de extensión como la página de opciones y los elementos emergentes:


1. Haga clic con el botón derecho en el fondo de la página.
2. Seleccione **"ver origen"**.

   ![depuración de elementos emergentes con F12](./../media/debug-popup-select.png)

3. Una vez que se abra F12, coloque puntos de interrupción dentro del archivo que quiera depurar.

   ![depuración de elementos emergentes con F12](./../media/debug-popup-f12.png)
4. Seleccione la ficha **Console (consola** ) y ejecute el comando `location.reload()` . Esto volverá a ejecutar la secuencia de comandos de la página, lo que le permitirá recorrer el código.  

   ![consola con ubicación. recarga introducida](./../media/debug-f12-background-console.png)

### Depurar una página de extensión emergente
Aunque el método para la depuración de páginas de extensión también se aplica a las páginas de extensión emergentes, los pasos siguientes describen otra manera de depurar el elemento emergente:

1. Haga clic con el botón secundario en el icono de la extensión.
2. Seleccione **"Inspeccionar mensaje emergente"**.

   ![inspección de depuración de popup](./../media/debug-popup-inspect.png)
3. Siga los pasos 3 y 4 anteriores para colocar puntos de interrupción y volver a cargar el elemento emergente.
