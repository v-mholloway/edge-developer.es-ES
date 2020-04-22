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
# <span data-ttu-id="02c1a-104">Agregar, mover y quitar extensiones para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="02c1a-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="02c1a-105">La compatibilidad de Microsoft Edge para las extensiones se introdujo en la **actualización de aniversario de Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="02c1a-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span> <span data-ttu-id="02c1a-106">Si estás desarrollando una extensión de Microsoft Edge y deseas cargarla, o si ya tienes y deseas quitarla, consulta los pasos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="02c1a-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>
<span data-ttu-id="02c1a-107">También se incluyen detalles sobre cómo cambiar la ubicación del icono de extensión en el explorador.</span><span class="sxs-lookup"><span data-stu-id="02c1a-107">Also included are details on how to change your extension icon's location in the browser.</span></span>

## <span data-ttu-id="02c1a-108">Agregar una extensión</span><span class="sxs-lookup"><span data-stu-id="02c1a-108">Adding an extension</span></span>

1. <span data-ttu-id="02c1a-109">Abra Microsoft Edge y escriba "acerca de: flags" en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="02c1a-109">Open Microsoft Edge and type 'about:flags' into the address bar.</span></span>

2. <span data-ttu-id="02c1a-110">Seleccione la casilla **habilitar las características** para el desarrollador de extensiones.</span><span class="sxs-lookup"><span data-stu-id="02c1a-110">Select the **Enable extension developer features** checkbox.</span></span>

   ![Acerca de: marcas activar las características para desarrolladores](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > <span data-ttu-id="02c1a-112">Si no tiene la actualización de aniversario de Windows 10 o posterior, esta opción no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="02c1a-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>

3. <span data-ttu-id="02c1a-113">Seleccione **más (...)** para abrir el menú.</span><span class="sxs-lookup"><span data-stu-id="02c1a-113">Select **More (...)** to open the menu.</span></span>

   ![botón más](./../media/morebutton.png)  

4. <span data-ttu-id="02c1a-115">Seleccione **extensiones** en el menú.</span><span class="sxs-lookup"><span data-stu-id="02c1a-115">Select **Extensions** from the menu.</span></span>

5. <span data-ttu-id="02c1a-116">Seleccione el botón **cargar extensión** .</span><span class="sxs-lookup"><span data-stu-id="02c1a-116">Select the **Load extension** button.</span></span>

   ![selección de cargar extensión](./../media/sideload-load-extension.png)

6. <span data-ttu-id="02c1a-118">Vaya a la carpeta de la extensión y seleccione el botón **Seleccionar carpeta** .</span><span class="sxs-lookup"><span data-stu-id="02c1a-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>
   ![selección de la carpeta de extensión que se cargará](./../media/sideload-select-extension.png)
   > [!NOTE]
   > <span data-ttu-id="02c1a-120">Si aparece un mensaje de error al cargar la extensión, consulte la página de [solución de problemas](./../troubleshooting.md) para obtener instrucciones.</span><span class="sxs-lookup"><span data-stu-id="02c1a-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](./../troubleshooting.md) page for guidance.</span></span>


**<span data-ttu-id="02c1a-121">Ya está todo listo.</span><span class="sxs-lookup"><span data-stu-id="02c1a-121">You're all set!</span></span> <span data-ttu-id="02c1a-122">Ahora deberías ver la extensión en el panel de extensión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="02c1a-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**

![extensión en el panel de extensión](./../media/sideload-extension-installed.png)

> [!NOTE]
> <span data-ttu-id="02c1a-124">Las extensiones no firmadas se desactivan automáticamente en los siguientes inicios de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="02c1a-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span> <span data-ttu-id="02c1a-125">Cuando el explorador entra en un estado de inactividad (después de unos 10 segundos de inactividad), verá la siguiente notificación en la parte inferior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="02c1a-125">When the browser enters an idle state (after approximately 10 seconds of inactivity) you will see the following notification at the bottom of the window.</span></span> ![<span data-ttu-id="02c1a-126">notificación](./../media/riskynotification.png) arriesgada para activar las extensiones no firmadas, haga clic en "activar de todos modos".</span><span class="sxs-lookup"><span data-stu-id="02c1a-126">risky notification](./../media/riskynotification.png) To turn on the unsigned extensions, click "Turn on anyway".</span></span>



## <span data-ttu-id="02c1a-127">Mover el botón de extensión</span><span class="sxs-lookup"><span data-stu-id="02c1a-127">Moving the extension button</span></span>
<span data-ttu-id="02c1a-128">En función de la configuración de la extensión, podría aparecer en el menú **más (...)** .</span><span class="sxs-lookup"><span data-stu-id="02c1a-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>

   ![menú acciones](./../media/browseraction.png)  


<span data-ttu-id="02c1a-130">Si desea mover el botón fuera de este menú para facilitar el acceso:</span><span class="sxs-lookup"><span data-stu-id="02c1a-130">If you want to move the button out of this menu for easier access:</span></span>

1. <span data-ttu-id="02c1a-131">Haga clic con el botón derecho en el botón de extensión.</span><span class="sxs-lookup"><span data-stu-id="02c1a-131">Right-click the extension button.</span></span>

2. <span data-ttu-id="02c1a-132">Seleccione **Mostrar botón junto a barra de direcciones**.</span><span class="sxs-lookup"><span data-stu-id="02c1a-132">Select **Show button next to address bar**.</span></span>

   ![menú acciones](./../media/browseraction_contextmenu.png)  

<span data-ttu-id="02c1a-134">También puede hacerlo desde la página de detalles de extensiones:</span><span class="sxs-lookup"><span data-stu-id="02c1a-134">Alternatively, you may do this from the extensions details page:</span></span>

1. <span data-ttu-id="02c1a-135">Haz clic en el botón de extensión.</span><span class="sxs-lookup"><span data-stu-id="02c1a-135">Click on the extension button.</span></span>
2. <span data-ttu-id="02c1a-136">Mostrar u ocultar el **botón junto a la barra de direcciones** en activado.</span><span class="sxs-lookup"><span data-stu-id="02c1a-136">Toggle **Show button next to address bar** to on.</span></span>

   ![Mostrar u ocultar el botón](./../media/show-button-toggle.png)

> [!NOTE]
> <span data-ttu-id="02c1a-138">Siempre puede volver a mover el botón al menú **más (...)** haciendo clic con el botón secundario en él y anulando la selección de **Mostrar junto a barra de direcciones** o de ir a la página de detalles de la extensión y desactivar la opción **Mostrar botón junto a barra de direcciones** .</span><span class="sxs-lookup"><span data-stu-id="02c1a-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>


## <span data-ttu-id="02c1a-139">Quitar una extensión</span><span class="sxs-lookup"><span data-stu-id="02c1a-139">Removing an extension</span></span>

1. <span data-ttu-id="02c1a-140">Abra Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="02c1a-140">Open Microsoft Edge.</span></span>

2. <span data-ttu-id="02c1a-141">Seleccione **más (...)** para abrir el menú.</span><span class="sxs-lookup"><span data-stu-id="02c1a-141">Select **More (...)** to open the menu.</span></span>

3. <span data-ttu-id="02c1a-142">Seleccione **extensiones** en el menú.</span><span class="sxs-lookup"><span data-stu-id="02c1a-142">Select **Extensions** from the menu.</span></span>

4. <span data-ttu-id="02c1a-143">Haga clic con el botón secundario en la extensión que desee quitar y seleccione **quitar**, o bien, seleccione la extensión y haga clic en el botón **quitar** .</span><span class="sxs-lookup"><span data-stu-id="02c1a-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>

   ![menú acciones](./../media/remove.png)  

**<span data-ttu-id="02c1a-145">La extensión debería desaparecer de la lista en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="02c1a-145">The extension should disappear from the list in Microsoft Edge.</span></span>**
