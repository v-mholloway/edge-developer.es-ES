---
description: Obtenga información sobre cómo agregar y quitar extensiones, así como mover el botón de una extensión junto a la barra de direcciones.
title: Agregar y quitar extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensión
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: fdc6950962e7ce7e0a720d0bafa7e2c63ebd7098
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573632"
---
# Agregar, mover y quitar extensiones para Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

La compatibilidad de Microsoft Edge para las extensiones se introdujo en la **actualización de aniversario de Windows 10**. Si estás desarrollando una extensión de Microsoft Edge y deseas cargarla, o si ya tienes y deseas quitarla, consulta los pasos que se indican a continuación.
También se incluyen detalles sobre cómo cambiar la ubicación del icono de extensión en el explorador.

## Agregar una extensión

1. Abra Microsoft Edge y escriba "acerca de: flags" en la barra de direcciones.

2. Seleccione la casilla **habilitar las características** para el desarrollador de extensiones.

   ![Acerca de: marcas activar las características para desarrolladores](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > Si no tiene la actualización de aniversario de Windows 10 o posterior, esta opción no estará disponible.

3. Seleccione **más (...)** para abrir el menú.

   ![botón más](./../media/morebutton.png)  

4. Seleccione **extensiones** en el menú.

5. Seleccione el botón **cargar extensión** .

   ![selección de cargar extensión](./../media/sideload-load-extension.png)

6. Vaya a la carpeta de la extensión y seleccione el botón **Seleccionar carpeta** .
   ![selección de la carpeta de extensión que se cargará](./../media/sideload-select-extension.png)
   > [!NOTE]
   > Si aparece un mensaje de error al cargar la extensión, consulte la página de [solución de problemas](./../troubleshooting.md) para obtener instrucciones.


**Ya está todo listo. Ahora deberías ver la extensión en el panel de extensión de Microsoft Edge.**

![extensión en el panel de extensión](./../media/sideload-extension-installed.png)

> [!NOTE]
> Las extensiones no firmadas se desactivan automáticamente en los siguientes inicios de Microsoft Edge. Cuando el explorador entra en un estado de inactividad (después de unos 10 segundos de inactividad), verá la siguiente notificación en la parte inferior de la ventana. ![notificación arriesgada ](./../media/riskynotification.png) para activar las extensiones no firmadas, haga clic en "activar de todos modos".



## Mover el botón de extensión
En función de la configuración de la extensión, podría aparecer en el menú **más (...)** .

   ![menú acciones](./../media/browseraction.png)  


Si desea mover el botón fuera de este menú para facilitar el acceso:

1. Haga clic con el botón derecho en el botón de extensión.

2. Seleccione **Mostrar botón junto a barra de direcciones**.

   ![menú acciones](./../media/browseraction_contextmenu.png)  

También puede hacerlo desde la página de detalles de extensiones:

1. Haz clic en el botón de extensión.
2. Mostrar u ocultar el **botón junto a la barra de direcciones** en activado.

   ![Mostrar u ocultar el botón](./../media/show-button-toggle.png)

> [!NOTE]
> Siempre puede volver a mover el botón al menú **más (...)** haciendo clic con el botón secundario en él y anulando la selección de **Mostrar junto a barra de direcciones** o de ir a la página de detalles de la extensión y desactivar la opción **Mostrar botón junto a barra de direcciones** .


## Quitar una extensión

1. Abra Microsoft Edge.

2. Seleccione **más (...)** para abrir el menú.

3. Seleccione **extensiones** en el menú.

4. Haga clic con el botón secundario en la extensión que desee quitar y seleccione **quitar**, o bien, seleccione la extensión y haga clic en el botón **quitar** .

   ![menú acciones](./../media/remove.png)  

**La extensión debería desaparecer de la lista en Microsoft Edge.**
