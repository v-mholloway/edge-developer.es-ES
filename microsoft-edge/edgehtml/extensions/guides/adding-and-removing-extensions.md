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
# <a name="adding-moving-and-removing-extensions-for-microsoft-edge"></a><span data-ttu-id="53f43-104">Agregar, mover y eliminar extensiones para Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="53f43-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="53f43-105">El soporte técnico de Microsoft Edge para extensiones se presentó en la **de actualización de aniversario de Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="53f43-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span>  <span data-ttu-id="53f43-106">Si está desarrollando una extensión de Microsoft Edge y quiere cargarla, o si ya lo ha hecho y ahora quiere quitarla, consulte los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="53f43-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>  
<span data-ttu-id="53f43-107">También se incluyen detalles sobre cómo cambiar la ubicación del icono de extensión en el explorador.</span><span class="sxs-lookup"><span data-stu-id="53f43-107">Also included are details on how to change your extension icon's location in the browser.</span></span>  

## <a name="adding-an-extension"></a><span data-ttu-id="53f43-108">Agregar una extensión</span><span class="sxs-lookup"><span data-stu-id="53f43-108">Adding an extension</span></span>  

1.  <span data-ttu-id="53f43-109">Abra Microsoft Edge y escriba `about:flags` en la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="53f43-109">Open Microsoft Edge and type `about:flags` into the address bar.</span></span>  
1.  <span data-ttu-id="53f43-110">Active la casilla **habilitar las características para desarrolladores de extensión**.</span><span class="sxs-lookup"><span data-stu-id="53f43-110">Select the **Enable extension developer features** checkbox.</span></span>  
    
    ![Acerca de: marcas activar las características para desarrolladores](../media/sideload-aboutflags.png)  
    
    > [!NOTE]
    > <span data-ttu-id="53f43-112">Si no tiene la actualización de aniversario de Windows 10 o una posterior, esta opción no estará disponible.</span><span class="sxs-lookup"><span data-stu-id="53f43-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>  
    
1.  <span data-ttu-id="53f43-113">Seleccione **más (...)** para abrir el menú.</span><span class="sxs-lookup"><span data-stu-id="53f43-113">Select **More (...)** to open the menu.</span></span>  
    
    ![botón más](../media/morebutton.png)  
    
1.  <span data-ttu-id="53f43-115">Seleccione **Extensions** en el menú.</span><span class="sxs-lookup"><span data-stu-id="53f43-115">Select **Extensions** from the menu.</span></span>  
    
1.  <span data-ttu-id="53f43-116">Seleccione el botón **Extensión de carga**.</span><span class="sxs-lookup"><span data-stu-id="53f43-116">Select the **Load extension** button.</span></span>  
    
    ![seleccionar la extensión de carga](../media/sideload-load-extension.png)  
    
1.  <span data-ttu-id="53f43-118">Desplácese a la carpeta de su extensión y seleccione el botón **Seleccionar carpeta**.</span><span class="sxs-lookup"><span data-stu-id="53f43-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>  
    
    ![seleccionar la carpeta de extensión para cargar](../media/sideload-select-extension.png)  
    
    > [!NOTE]
    > <span data-ttu-id="53f43-120">Si se produce un mensaje de error al cargar su extensión, consulte la página [solución de problemas de](../troubleshooting.md) para obtener instrucciones.</span><span class="sxs-lookup"><span data-stu-id="53f43-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](../troubleshooting.md) page for guidance.</span></span>  
    
**<span data-ttu-id="53f43-121">Ya está todo listo.</span><span class="sxs-lookup"><span data-stu-id="53f43-121">You're all set!</span></span> <span data-ttu-id="53f43-122">Ahora debería ver la extensión que aparece en el panel de extensión de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="53f43-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**  

![extensión en el panel de extensión](../media/sideload-extension-installed.png)  

> [!NOTE]
> <span data-ttu-id="53f43-124">Las extensiones sin firmar se desactivan automáticamente en los inicios posteriores de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="53f43-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span>  <span data-ttu-id="53f43-125">Cuando el explorador escriba un estado de inactividad \(después de aproximadamente 10 segundos de inactividad\) verá la siguiente notificación en la parte inferior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="53f43-125">When the browser enters an idle state \(after approximately 10 seconds of inactivity\) you will see the following notification at the bottom of the window.</span></span>  ![<span data-ttu-id="53f43-126">notificación arriesgada ](../media/riskynotification.png) Para activar las extensiones sin signo, haga clic en Activar de todos **modos**.</span><span class="sxs-lookup"><span data-stu-id="53f43-126">risky notification](../media/riskynotification.png) To turn on the unsigned extensions, click **Turn on anyway**.</span></span>  

## <a name="moving-the-extension-button"></a><span data-ttu-id="53f43-127">Mover el botón extensión</span><span class="sxs-lookup"><span data-stu-id="53f43-127">Moving the extension button</span></span>  

<span data-ttu-id="53f43-128">Según la configuración de su extensión, podría aparecer en el menú de **Más (...)**.</span><span class="sxs-lookup"><span data-stu-id="53f43-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>  

![menú acciones](../media/browseraction.png)  

<span data-ttu-id="53f43-130">Si desea quitar el botón de este menú para facilitar el acceso:</span><span class="sxs-lookup"><span data-stu-id="53f43-130">If you want to move the button out of this menu for easier access:</span></span>  

1.  <span data-ttu-id="53f43-131">Haga clic con el botón derecho en el botón extensión.</span><span class="sxs-lookup"><span data-stu-id="53f43-131">Right-click the extension button.</span></span>  
1.  <span data-ttu-id="53f43-132">Seleccione **botón Mostrar situado junto a la barra de direcciones**.</span><span class="sxs-lookup"><span data-stu-id="53f43-132">Select **Show button next to address bar**.</span></span>  
    
    ![menú contextual en el menú acciones](../media/browseraction_contextmenu.png)  
    
<span data-ttu-id="53f43-134">Como alternativa, puede hacerlo desde la página Detalles de extensiones:</span><span class="sxs-lookup"><span data-stu-id="53f43-134">Alternatively, you may do this from the extensions details page:</span></span>  

1.  <span data-ttu-id="53f43-135">Haga clic en el botón de extensión.</span><span class="sxs-lookup"><span data-stu-id="53f43-135">Click on the extension button.</span></span>  
1.  <span data-ttu-id="53f43-136">Alternar **botón Mostrar situado junto a la barra de direcciones** en activado.</span><span class="sxs-lookup"><span data-stu-id="53f43-136">Toggle **Show button next to address bar** to on.</span></span>  
    
    ![Mostrar u ocultar el botón de alternancia encendido](../media/show-button-toggle.png)  
    
> [!NOTE]
> <span data-ttu-id="53f43-138">Siempre puede volver a colocar el botón en el menú **Más (...)** si hace clic con el botón secundario en él y anula la selección **Mostrar junto a la barra de direcciones** o yendo a la página Detalles de la extensión y moviendo el botón **Mostrar situado junto a la barra de direcciones** a la posición desactivado.</span><span class="sxs-lookup"><span data-stu-id="53f43-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>  

## <a name="removing-an-extension"></a><span data-ttu-id="53f43-139">Creación de una extensión</span><span class="sxs-lookup"><span data-stu-id="53f43-139">Removing an extension</span></span>  

1.  <span data-ttu-id="53f43-140">Abra Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="53f43-140">Open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="53f43-141">Seleccione **más (...)** para abrir el menú.</span><span class="sxs-lookup"><span data-stu-id="53f43-141">Select **More (...)** to open the menu.</span></span>  
1.  <span data-ttu-id="53f43-142">Seleccione **Extensions** en el menú.</span><span class="sxs-lookup"><span data-stu-id="53f43-142">Select **Extensions** from the menu.</span></span>  
1.  <span data-ttu-id="53f43-143">Haga clic con el botón derecho en la extensión que desea quitar y seleccione **quitar**, o bien seleccione la extensión y haga clic en el botón **quitar**.</span><span class="sxs-lookup"><span data-stu-id="53f43-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>  
    
    ![Menú Quitar en acciones](../media/remove.png)  
    
**<span data-ttu-id="53f43-145">La extensión debe desaparecer de la lista de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="53f43-145">The extension should disappear from the list in Microsoft Edge.</span></span>**  
