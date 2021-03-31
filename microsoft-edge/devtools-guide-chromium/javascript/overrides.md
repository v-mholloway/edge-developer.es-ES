---
description: La característica de invalidaciones es una característica de la herramienta de orígenes de Microsoft Edge DevTools que le permite copiar recursos de páginas web en su disco duro.  Cuando actualice la página web, DevTools no cargue el recurso, pero reemplácelo con su copia local en su lugar.
title: Invalidar los recursos de páginas web con copias locales con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 7f273f89708e0948e68cd2c7ba79cefb6d7e167c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230967"
---
# <span data-ttu-id="5e71f-105">Invalidar los recursos de páginas web con copias locales con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5e71f-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="5e71f-106">En ocasiones, es necesario solucionar un problema en una página web a la que no tiene acceso o las correcciones implican un proceso de compilación lento y complejo.</span><span class="sxs-lookup"><span data-stu-id="5e71f-106">Sometimes you need to fix a problem on a webpage that you do not have access to or fixes involve a slow and complex build process.</span></span>  <span data-ttu-id="5e71f-107">Puede depurar y corregir todo tipo de problemas en DevTools.</span><span class="sxs-lookup"><span data-stu-id="5e71f-107">You may debug and fix all kind of problems in DevTools.</span></span> <span data-ttu-id="5e71f-108">Pero el problema es que los cambios no se conservan.</span><span class="sxs-lookup"><span data-stu-id="5e71f-108">But the problem is the changes do not persist.</span></span>  <span data-ttu-id="5e71f-109">Después de actualizar el archivo, desaparecerá todo el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5e71f-109">After you refresh the file, all your work is gone.</span></span>  

<span data-ttu-id="5e71f-110">La característica de invalidaciones de la herramienta [orígenes][DevToolsSourcesTool] le ayuda a resolver este problema.</span><span class="sxs-lookup"><span data-stu-id="5e71f-110">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="5e71f-111">Ahora puede tomar un recurso de la página web actual y almacenarlo de forma local.</span><span class="sxs-lookup"><span data-stu-id="5e71f-111">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="5e71f-112">Al actualizar la página web, el explorador no carga el recurso desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="5e71f-112">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="5e71f-113">En su lugar, el explorador lo reemplaza por la copia local del recurso.</span><span class="sxs-lookup"><span data-stu-id="5e71f-113">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <span data-ttu-id="5e71f-114">Configurar la carpeta local para almacenar invalidaciones</span><span class="sxs-lookup"><span data-stu-id="5e71f-114">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="5e71f-115">En la herramienta **orígenes** , busque varias secciones en la parte izquierda.</span><span class="sxs-lookup"><span data-stu-id="5e71f-115">In the **Sources** tool, find several sections on the left-hand side.</span></span>  <span data-ttu-id="5e71f-116">Si no se muestra la opción **sobrescrituras** , elija la</span><span class="sxs-lookup"><span data-stu-id="5e71f-116">If the **Overrides** option is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="5e71f-117">icono para ir allí.</span><span class="sxs-lookup"><span data-stu-id="5e71f-117">icon to get there.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Herramienta de orígenes con un espacio insuficiente para mostrar la opción sobrescrituras" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="5e71f-119">Herramienta de **orígenes** con un espacio insuficiente para mostrar la opción sobrescrituras</span><span class="sxs-lookup"><span data-stu-id="5e71f-119">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Elegir la opción de sobrescrituras" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="5e71f-121">Elegir la opción de sobrescrituras</span><span class="sxs-lookup"><span data-stu-id="5e71f-121">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="5e71f-122">Después de elegir la opción **invalidaciones** , debe elegir una carpeta en el equipo local para almacenar los archivos de recursos que desea reemplazar.</span><span class="sxs-lookup"><span data-stu-id="5e71f-122">After you choose the **Overrides** option, you must choose a folder on your local computer to store the resource files that you want to replace.</span></span>  <span data-ttu-id="5e71f-123">Elija la opción **+ Seleccionar carpeta para reemplazos** para buscar una carpeta.</span><span class="sxs-lookup"><span data-stu-id="5e71f-123">Choose the **+ Select folder for overrides** to search for a folder.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Elegir una carpeta para reemplazarla" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="5e71f-125">Elegir una carpeta para reemplazarla</span><span class="sxs-lookup"><span data-stu-id="5e71f-125">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5e71f-126">DevTools le advierte que debe tener acceso total a la carpeta y que no debe revelar información confidencial.</span><span class="sxs-lookup"><span data-stu-id="5e71f-126">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="5e71f-127">En la barra de advertencia, elija **permitir** para conceder acceso.</span><span class="sxs-lookup"><span data-stu-id="5e71f-127">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="conceder acceso DevTools a la carpeta" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="5e71f-129">Conceder acceso DevTools a la carpeta</span><span class="sxs-lookup"><span data-stu-id="5e71f-129">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5e71f-130">En el panel **sobrescrituras** , debe aparecer una casilla junto a `Enable Local Overrides` la carpeta invalidaciones.</span><span class="sxs-lookup"><span data-stu-id="5e71f-130">In the **Overrides** pane, a checkbox should be displayed next to `Enable Local Overrides` and your overrides folder.</span></span>  <span data-ttu-id="5e71f-131">Aparece un icono junto a ella que le permite eliminar la configuración local de reemplazos.</span><span class="sxs-lookup"><span data-stu-id="5e71f-131">An icon is displayed next to it that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="5e71f-132">Ya ha terminado de configurar la carpeta y está listo para reemplazar los recursos en vivo por otros locales.</span><span class="sxs-lookup"><span data-stu-id="5e71f-132">You are now done setting up your folder and ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Configuración correcta de una carpeta de invalidaciones" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="5e71f-134">Configuración correcta de una carpeta de invalidaciones</span><span class="sxs-lookup"><span data-stu-id="5e71f-134">Successful set up of an overrides folder</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="5e71f-135">Agregar archivos a la carpeta Overrides</span><span class="sxs-lookup"><span data-stu-id="5e71f-135">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="5e71f-136">Para agregar archivos a la carpeta Overrides, abra la herramienta **elementos** e inspeccione la Página Web.</span><span class="sxs-lookup"><span data-stu-id="5e71f-136">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="5e71f-137">Para editar, elija el nombre del archivo CSS en el inspector de **estilos** .</span><span class="sxs-lookup"><span data-stu-id="5e71f-137">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Elegir un archivo en el inspector de estilos" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="5e71f-139">Elegir un archivo en el inspector de **estilos**</span><span class="sxs-lookup"><span data-stu-id="5e71f-139">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="5e71f-140">En el editor de **orígenes** , desplace el puntero sobre el nombre de archivo del archivo que ha elegido, abra el menú contextual \(haga clic con el botón derecho \) y elija **Guardar para reemplazos**.</span><span class="sxs-lookup"><span data-stu-id="5e71f-140">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="En el editor de orígenes, agregue el nombre del archivo a Overrides" lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="5e71f-142">En el editor de **orígenes** , agregue el nombre del archivo a Overrides</span><span class="sxs-lookup"><span data-stu-id="5e71f-142">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="En el menú contextual, elija Guardar para reemplazos" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="5e71f-144">En el menú contextual, elija **Guardar para reemplazos**</span><span class="sxs-lookup"><span data-stu-id="5e71f-144">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="5e71f-145">El archivo se almacena en la carpeta Overrides.</span><span class="sxs-lookup"><span data-stu-id="5e71f-145">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="5e71f-146">Compruebe que DevTools crear una carpeta cuyo nombre contenga la dirección URL del archivo con la estructura de directorios correcta.</span><span class="sxs-lookup"><span data-stu-id="5e71f-146">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="5e71f-147">El archivo se almacena en el interior.</span><span class="sxs-lookup"><span data-stu-id="5e71f-147">The file is stored inside.</span></span>  <span data-ttu-id="5e71f-148">El nombre de archivo en el editor ahora también muestra un punto púrpura que indica que el archivo es local y no es dinámico.</span><span class="sxs-lookup"><span data-stu-id="5e71f-148">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="El archivo se ha guardado correctamente en la carpeta Overrides" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="5e71f-150">El archivo se ha guardado correctamente en la carpeta Overrides</span><span class="sxs-lookup"><span data-stu-id="5e71f-150">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="5e71f-151">En el ejemplo siguiente, puede cambiar ahora los estilos de la Página Web.</span><span class="sxs-lookup"><span data-stu-id="5e71f-151">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="5e71f-152">Para agregar un borde rojo sobre el archivo, en el editor de **estilos** , copie el estilo siguiente y agréguelo al elemento de cuerpo.</span><span class="sxs-lookup"><span data-stu-id="5e71f-152">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5e71f-153">El archivo se guardará automáticamente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5e71f-153">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="5e71f-154">Si actualiza el archivo, se mostrará el borde y no se perderá nada de su trabajo.</span><span class="sxs-lookup"><span data-stu-id="5e71f-154">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Cambiar los estilos de una página web de forma permanente mediante la edición de un archivo en la carpeta sobrescrituras" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="5e71f-156">Cambiar los estilos de una página web de forma permanente mediante la edición de un archivo en la carpeta sobrescrituras</span><span class="sxs-lookup"><span data-stu-id="5e71f-156">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="5e71f-157">En la herramienta **orígenes** , en la sección **Página** , mantenga el puntero sobre cualquier archivo, abra el menú contextual \(haga clic con el botón derecho \) y agréguelo a reemplazos.</span><span class="sxs-lookup"><span data-stu-id="5e71f-157">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="5e71f-158">De nuevo, los archivos que ya están en la carpeta sobrescrituras tienen un punto púrpura en el icono.</span><span class="sxs-lookup"><span data-stu-id="5e71f-158">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Elegir un archivo de la herramienta orígenes para invalidaciones" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="5e71f-160">Elegir un archivo de la herramienta **orígenes** para invalidaciones</span><span class="sxs-lookup"><span data-stu-id="5e71f-160">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="5e71f-161">Como alternativa, en la herramienta **red** , desplace el puntero sobre cualquier archivo, abra el menú contextual \(haga clic con el botón derecho \) y agréguelo a reemplazos.</span><span class="sxs-lookup"><span data-stu-id="5e71f-161">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="5e71f-162">Cuando las invalidaciones son efectivas, los archivos que se encuentran en el equipo y no desde la página web en vivo.</span><span class="sxs-lookup"><span data-stu-id="5e71f-162">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="5e71f-163">Cuando las invalidaciones estén en vigor, en la herramienta **red** , busque un icono de advertencia junto al nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="5e71f-163">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Elegir un archivo de la herramienta red para invalidaciones" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="5e71f-165">Elegir un archivo de la herramienta **red** para invalidaciones</span><span class="sxs-lookup"><span data-stu-id="5e71f-165">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="5e71f-166">Interacción bidireccional de invalidaciones</span><span class="sxs-lookup"><span data-stu-id="5e71f-166">Two-way interaction of overrides</span></span>  

<span data-ttu-id="5e71f-167">Use el editor que se proporciona con la herramienta **orígenes** de DevTools o cualquier editor al que desee cambiar los archivos.</span><span class="sxs-lookup"><span data-stu-id="5e71f-167">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="5e71f-168">Los cambios se sincronizan en todos los productos que tienen acceso a los archivos de la carpeta Overrides.</span><span class="sxs-lookup"><span data-stu-id="5e71f-168">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <span data-ttu-id="5e71f-169">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5e71f-169">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Información general de la herramienta orígenes | Microsoft docs"  
