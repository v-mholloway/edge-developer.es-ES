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
ms.openlocfilehash: 3473108918ec3cb3945e0999b27873ddea40aa5c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236554"
---
# Agregar, mover y eliminar extensiones para Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

El soporte técnico de Microsoft Edge para extensiones se presentó en la **de actualización de aniversario de Windows 10**. Si está desarrollando una extensión de Microsoft Edge y quiere cargarla, o si ya lo ha hecho y ahora quiere quitarla, consulte los pasos siguientes.
También se incluyen detalles sobre cómo cambiar la ubicación del icono de extensión en el explorador.

## Agregar una extensión

1. Abra Microsoft Edge y escriba "about flags" en la barra de direcciones.

2. Active la casilla **habilitar las características para desarrolladores de extensión**.

   ![Acerca de: marcas activar las características para desarrolladores](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > Si no tiene la actualización de aniversario de Windows 10 o una posterior, esta opción no estará disponible.

3. Seleccione **más (...)** para abrir el menú.

   ![botón más](./../media/morebutton.png)  

4. Seleccione **Extensions** en el menú.

5. Seleccione el botón **Extensión de carga**.

   ![seleccionar la extensión de carga](./../media/sideload-load-extension.png)

6. Desplácese a la carpeta de su extensión y seleccione el botón **Seleccionar carpeta**.
   ![seleccionar la carpeta de extensión para cargar](./../media/sideload-select-extension.png)
   > [!NOTE]
   > Si se produce un mensaje de error al cargar su extensión, consulte la página [solución de problemas de](./../troubleshooting.md) para obtener instrucciones.


**Ya está todo listo. Ahora debería ver la extensión que aparece en el panel de extensión de Microsoft Edge.**

![extensión en el panel de extensión](./../media/sideload-extension-installed.png)

> [!NOTE]
> Las extensiones sin firmar se desactivan automáticamente en los inicios posteriores de Microsoft Edge. Cuando el explorador entre en un estado de inactividad (después de unos 10 segundos de inactividad), verá la siguiente notificación en la parte inferior de la ventana. ![notificación arriesgada](./../media/riskynotification.png) activar las extensiones sin firma, haga clic en "activar de todos modos".



## Mover el botón extensión
Según la configuración de su extensión, podría aparecer en el menú de **Más (...)**.

   ![menú acciones: explorador](./../media/browseraction.png)  


Si desea quitar el botón de este menú para facilitar el acceso:

1. Haga clic con el botón derecho en el botón extensión.

2. Seleccione **botón Mostrar situado junto a la barra de direcciones**.

   ![menú acciones: menú contextual del explorador](./../media/browseraction_contextmenu.png)  

Como alternativa, puede hacerlo desde la página Detalles de extensiones:

1. Haga clic en el botón de extensión.
2. Alternar **botón Mostrar situado junto a la barra de direcciones** en activado.

   ![Mostrar u ocultar el botón de alternancia encendido](./../media/show-button-toggle.png)

> [!NOTE]
> Siempre puede volver a colocar el botón en el menú **Más (...)** si hace clic con el botón secundario en él y anula la selección **Mostrar junto a la barra de direcciones** o yendo a la página Detalles de la extensión y moviendo el botón **Mostrar situado junto a la barra de direcciones** a la posición desactivado.


## Creación de una extensión

1. Abra Microsoft Edge.

2. Seleccione **más (...)** para abrir el menú.

3. Seleccione **Extensions** en el menú.

4. Haga clic con el botón derecho en la extensión que desea quitar y seleccione **quitar**, o bien seleccione la extensión y haga clic en el botón **quitar**.

   ![menú acciones: quitar](./../media/remove.png)  

**La extensión debe desaparecer de la lista de Microsoft Edge.**
