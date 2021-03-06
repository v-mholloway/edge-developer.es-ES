---
description: Obtenga información acerca de cómo agregar y quitar extensiones, así como mover el botón de una extensión junto a la barra de direcciones.
title: Agregar y quitar extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, html, css, javascript, desarrollador, extensión
ms.custom: seodec18
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 2ef75e76795d527935a84913528506bfa042e56f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398878"
---
# <a name="adding-moving-and-removing-extensions-for-microsoft-edge"></a>Agregar, mover y eliminar extensiones para Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

El soporte técnico de Microsoft Edge para extensiones se presentó en la **de actualización de aniversario de Windows 10**.  Si está desarrollando una extensión de Microsoft Edge y quiere cargarla, o si ya lo ha hecho y ahora quiere quitarla, consulte los pasos siguientes.  
También se incluyen detalles sobre cómo cambiar la ubicación del icono de extensión en el explorador.  

## <a name="adding-an-extension"></a>Agregar una extensión  

1.  Abra Microsoft Edge y escriba `about:flags` en la barra de direcciones.  
1.  Active la casilla **habilitar las características para desarrolladores de extensión**.  
    
    ![Acerca de: marcas activar las características para desarrolladores](../media/sideload-aboutflags.png)  
    
    > [!NOTE]
    > Si no tiene la actualización de aniversario de Windows 10 o una posterior, esta opción no estará disponible.  
    
1.  Seleccione **más (...)** para abrir el menú.  
    
    ![botón más](../media/morebutton.png)  
    
1.  Seleccione **Extensions** en el menú.  
    
1.  Seleccione el botón **Extensión de carga**.  
    
    ![seleccionar la extensión de carga](../media/sideload-load-extension.png)  
    
1.  Desplácese a la carpeta de su extensión y seleccione el botón **Seleccionar carpeta**.  
    
    ![seleccionar la carpeta de extensión para cargar](../media/sideload-select-extension.png)  
    
    > [!NOTE]
    > Si se produce un mensaje de error al cargar su extensión, consulte la página [solución de problemas de](../troubleshooting.md) para obtener instrucciones.  
    
**Ya está todo listo. Ahora debería ver la extensión que aparece en el panel de extensión de Microsoft Edge.**  

![extensión en el panel de extensión](../media/sideload-extension-installed.png)  

> [!NOTE]
> Las extensiones sin firmar se desactivan automáticamente en los inicios posteriores de Microsoft Edge.  Cuando el explorador escriba un estado de inactividad \(después de aproximadamente 10 segundos de inactividad\) verá la siguiente notificación en la parte inferior de la ventana.  ![notificación arriesgada ](../media/riskynotification.png) Para activar las extensiones sin signo, haga clic en Activar de todos **modos**.  

## <a name="moving-the-extension-button"></a>Mover el botón extensión  

Según la configuración de su extensión, podría aparecer en el menú de **Más (...)**.  

![menú acciones](../media/browseraction.png)  

Si desea quitar el botón de este menú para facilitar el acceso:  

1.  Haga clic con el botón derecho en el botón extensión.  
1.  Seleccione **botón Mostrar situado junto a la barra de direcciones**.  
    
    ![menú contextual en el menú acciones](../media/browseraction_contextmenu.png)  
    
Como alternativa, puede hacerlo desde la página Detalles de extensiones:  

1.  Haga clic en el botón de extensión.  
1.  Alternar **botón Mostrar situado junto a la barra de direcciones** en activado.  
    
    ![Mostrar u ocultar el botón de alternancia encendido](../media/show-button-toggle.png)  
    
> [!NOTE]
> Siempre puede volver a colocar el botón en el menú **Más (...)** si hace clic con el botón secundario en él y anula la selección **Mostrar junto a la barra de direcciones** o yendo a la página Detalles de la extensión y moviendo el botón **Mostrar situado junto a la barra de direcciones** a la posición desactivado.  

## <a name="removing-an-extension"></a>Creación de una extensión  

1.  Abra Microsoft Edge.  
1.  Seleccione **más (...)** para abrir el menú.  
1.  Seleccione **Extensions** en el menú.  
1.  Haga clic con el botón derecho en la extensión que desea quitar y seleccione **quitar**, o bien seleccione la extensión y haga clic en el botón **quitar**.  
    
    ![Menú Quitar en acciones](../media/remove.png)  
    
**La extensión debe desaparecer de la lista de Microsoft Edge.**  
