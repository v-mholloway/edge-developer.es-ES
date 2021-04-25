---
description: La característica Invalidaciones es una característica dentro de la herramienta Orígenes de Microsoft Edge DevTools que permite copiar recursos de página web en el disco duro.  Al actualizar la página web, DevTools no carga el recurso, sino que lo reemplaza por la copia local.
title: Invalidar recursos de página web con copias locales con Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 66c0686c166163f1640384d096288af0b530f135
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519439"
---
# <a name="override-webpage-resources-with-local-copies-using-microsoft-edge-devtools"></a><span data-ttu-id="ee7c0-105">Invalidar recursos de página web con copias locales con Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ee7c0-105">Override webpage resources with local copies using Microsoft Edge DevTools</span></span>  

<span data-ttu-id="ee7c0-106">A veces, necesita probar algunas correcciones posibles para una página web, pero no tiene acceso a los archivos de origen, o cambiar la página requiere un proceso de compilación lento y complejo.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-106">Sometimes you need to try out some possible fixes for a webpage, but you don't have access to the source files, or changing the page requires a slow and complex build process.</span></span>  <span data-ttu-id="ee7c0-107">Puede depurar y corregir todo tipo de problemas en DevTools.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-107">You may debug and fix all kind of problems in DevTools.</span></span>  <span data-ttu-id="ee7c0-108">Pero los cambios no persisten; después de actualizar el archivo local, todo el trabajo ha desaparecido.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-108">But the changes do not persist; after you refresh the local file, all your work is gone.</span></span>  <span data-ttu-id="ee7c0-109">La característica Invalidaciones de la [herramienta Orígenes][DevToolsSourcesTool] le ayuda a resolver este problema.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-109">The Overrides feature in the [Sources][DevToolsSourcesTool] tool helps you solve this problem.</span></span>  

<span data-ttu-id="ee7c0-110">Ahora puede tomar un recurso de la página web actual y almacenarlo localmente.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-110">You may now take a resource of the current webpage and store it locally.</span></span>  <span data-ttu-id="ee7c0-111">Al actualizar la página web, el explorador no carga el recurso desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-111">When you refresh the webpage, the browser does not load the resource from the server.</span></span>  <span data-ttu-id="ee7c0-112">En su lugar, el explorador lo reemplaza por la copia local del recurso.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-112">Instead the browser replaces it with your local copy of the resource.</span></span>  

## <a name="setting-up-your-local-folder-to-store-overrides"></a><span data-ttu-id="ee7c0-113">Configurar la carpeta local para almacenar invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-113">Setting up your local folder to store Overrides</span></span>  

1.  <span data-ttu-id="ee7c0-114">Vaya a la **herramienta Orígenes.**</span><span class="sxs-lookup"><span data-stu-id="ee7c0-114">Navigate to the **Sources** tool.</span></span>  
1.  <span data-ttu-id="ee7c0-115">En el **panel** Navegador (a la izquierda), elija la **pestaña Invalidaciones.**  Si no **se muestra** la pestaña Invalidaciones, elija la opción</span><span class="sxs-lookup"><span data-stu-id="ee7c0-115">In the **Navigator** pane (on the left), choose the **Overrides** tab.  If the **Overrides** tab is not displayed, choose the</span></span> <code>&#x0226B;</code><!--`≫`--> <span data-ttu-id="ee7c0-116">.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-116">icon.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-overflow-menu.msft.png" alt-text="Herramienta Orígenes sin espacio suficiente para mostrar la opción invalidaciones" lightbox="../media/javascript-overrides-overflow-menu.msft.png":::
             <span data-ttu-id="ee7c0-118">**Herramienta Orígenes** sin espacio suficiente para mostrar la opción invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-118">**Sources** tool with not enough space to show the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/javascript-overrides-menu.msft.png" alt-text="Elegir la opción invalidaciones" lightbox="../media/javascript-overrides-menu.msft.png":::
             <span data-ttu-id="ee7c0-120">Elegir la opción invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-120">Choose the overrides option</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  <span data-ttu-id="ee7c0-121">Elija una carpeta en el equipo local para almacenar los archivos de recursos que desea reemplazar.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-121">Choose a folder on your local computer to store the resource files that you want to replace.</span></span>  
     *   <span data-ttu-id="ee7c0-122">Para buscar una carpeta, elija **+ Seleccionar carpeta para invalidaciones.**</span><span class="sxs-lookup"><span data-stu-id="ee7c0-122">To search for a folder, choose **+ Select folder for overrides**.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-select-folder.msft.png" alt-text="Elegir una carpeta que se usará para invalidaciones" lightbox="../media/javascript-overrides-select-folder.msft.png":::
       <span data-ttu-id="ee7c0-124">Elegir una carpeta que se usará para invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-124">Choose a folder to use for overrides</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ee7c0-125">DevTools le advierte que debe tener acceso total a la carpeta y que no debe revelar información confidencial.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-125">DevTools warns you that must have full access to the folder and that you should not reveal any sensitive information.</span></span>  <span data-ttu-id="ee7c0-126">En la barra de advertencias, elija **Permitir** conceder acceso.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-126">On the warning bar, choose **Allow** to grant access.</span></span>  
    
    :::image type="complex" source="../media/javascript-overrides-give-access-to-folder.msft.png" alt-text="conceder acceso de DevTools a la carpeta" lightbox="../media/javascript-overrides-give-access-to-folder.msft.png":::
       <span data-ttu-id="ee7c0-128">Conceder acceso de DevTools a la carpeta</span><span class="sxs-lookup"><span data-stu-id="ee7c0-128">Grant DevTools access to folder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ee7c0-129">En la **pestaña Invalidaciones,** se muestra una casilla junto a **Habilitar invalidaciones locales**.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-129">In the **Overrides** tab, a checkbox is shown next to **Enable Local Overrides**.</span></span>  <span data-ttu-id="ee7c0-130">A la derecha de **Habilitar invalidaciones locales** se encuentra un **icono Borrar** configuración que permite eliminar la configuración de invalidaciones locales.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-130">To the right of **Enable Local Overrides** is a **Clear configuration** icon that allows you to delete your local overrides settings.</span></span>  <span data-ttu-id="ee7c0-131">Ya ha terminado de configurar la carpeta y está listo para reemplazar los recursos en directo por los locales.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-131">You are now done setting up your folder and are ready to replace live resources with local ones.</span></span>
    
    :::image type="complex" source="../media/javascript-overrides-folder-setup-complete.msft.png" alt-text="Instalación correcta de una carpeta de invalidaciones" lightbox="../media/javascript-overrides-folder-setup-complete.msft.png":::
       <span data-ttu-id="ee7c0-133">Instalación correcta de una carpeta de invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-133">Successful setup of an overrides folder</span></span>  
    :::image-end:::  
    
## <a name="adding-files-to-your-overrides-folder"></a><span data-ttu-id="ee7c0-134">Agregar archivos a la carpeta Invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-134">Adding files to your Overrides folder</span></span>  
  
<span data-ttu-id="ee7c0-135">Para agregar archivos a la carpeta invalidaciones, abra la **herramienta Elementos** e inspeccione la página web.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-135">To add files to your overrides folder, open the **Elements** tool and inspect the webpage.</span></span>  <span data-ttu-id="ee7c0-136">Para editar, elija el nombre del archivo CSS en el inspector **de estilos.**</span><span class="sxs-lookup"><span data-stu-id="ee7c0-136">To edit, choose the name of the CSS file in the **Styles** inspector.</span></span>  

:::image type="complex" source="../media/javascript-overrides-select-css-file.msft.png" alt-text="Elegir un archivo en el inspector de estilos" lightbox="../media/javascript-overrides-select-css-file.msft.png":::
   <span data-ttu-id="ee7c0-138">Elegir un archivo en el inspector **de estilos**</span><span class="sxs-lookup"><span data-stu-id="ee7c0-138">Choose a file in the **Styles** inspector</span></span>  
:::image-end:::  

<span data-ttu-id="ee7c0-139">En el editor **de** orígenes, mantenga el mouse sobre el nombre del archivo elegido, abra el menú contextual \(hacer clic con el botón secundario\) y elija **Guardar para reemplazos**.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-139">On the **Sources** editor, hover on the file name of your chosen file, open the contextual menu \(right-click\), and choose **Save for overrides**.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-name.msft.png" alt-text="En el editor de orígenes, agregue el nombre del archivo a invalidaciones" lightbox="../media/javascript-overrides-file-name.msft.png":::
   <span data-ttu-id="ee7c0-141">En el editor **de** orígenes, agregue el nombre del archivo a invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-141">In the **Sources** editor, add the name of the file to overrides</span></span>  
:::image-end:::  

:::image type="complex" source="../media/javascript-overrides-save-for-overrides.msft.png" alt-text="En el menú contextual, elija Guardar para invalidaciones" lightbox="../media/javascript-overrides-save-for-overrides.msft.png":::
   <span data-ttu-id="ee7c0-143">En el menú contextual, elija **Guardar para invalidaciones**</span><span class="sxs-lookup"><span data-stu-id="ee7c0-143">On the context menu, choose **Save for overrides**</span></span>  
:::image-end:::  

<span data-ttu-id="ee7c0-144">El archivo se almacena en la carpeta invalidaciones.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-144">The file is stored in your overrides folder.</span></span>  <span data-ttu-id="ee7c0-145">Compruebe que DevTools cree una carpeta que se denomina mediante la dirección URL del archivo con la estructura de directorio correcta.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-145">Verify that DevTools create a folder that is named using the URL of the file with the correct directory structure.</span></span>  <span data-ttu-id="ee7c0-146">El archivo se almacena dentro.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-146">The file is stored inside.</span></span>  <span data-ttu-id="ee7c0-147">El nombre de archivo del editor ahora también muestra un punto púrpura que indica que el archivo es local y no uno vivo.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-147">The file name in the editor now also shows a purple dot that indicates that the file is local and not a live one.</span></span>  

:::image type="complex" source="../media/javascript-overrides-file-stored.msft.png" alt-text="Almacenado correctamente el archivo en la carpeta invalidaciones" lightbox="../media/javascript-overrides-file-stored.msft.png":::
   <span data-ttu-id="ee7c0-149">Almacenado correctamente el archivo en la carpeta invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-149">Successfully stored the file in your overrides folder</span></span>  
:::image-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="ee7c0-150">En el siguiente ejemplo, ahora puede cambiar los estilos de la página web.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-150">In the following example, you may now change the styles of the webpage.</span></span>  <span data-ttu-id="ee7c0-151">Para agregar un borde rojo alrededor del archivo, en el editor **de estilos,** copie el siguiente estilo y agrégálo al elemento body.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-151">To add a red border around the file, on the **Styles** editor, copy the following style, and add it to the body element.</span></span>  
      
      ```css
      border: 10px solid firebrick
      ```  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ee7c0-152">El archivo se guarda automáticamente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-152">The file is automatically saved on your computer.</span></span>  <span data-ttu-id="ee7c0-153">Si actualiza el archivo, se muestra el borde y no se pierde nada de su trabajo.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-153">If you refresh the file, the border is displayed and none of your work is lost.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-changing-styles.msft.png" alt-text="Cambiar los estilos de página web de forma persistente mediante la edición de un archivo en la carpeta invalidaciones" lightbox="../media/javascript-overrides-changing-styles.msft.png":::
         <span data-ttu-id="ee7c0-155">Cambiar los estilos de página web de forma persistente mediante la edición de un archivo en la carpeta invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-155">Change webpage styles persistently by editing a file in your overrides folder</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

:::row:::
   :::column span="":::
      <span data-ttu-id="ee7c0-156">En la **herramienta Orígenes,** en la sección Página, mantenga el mouse en cualquier archivo, abra el menú contextual \(haga clic con el botón secundario\) y agrégálo a invalidaciones. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="ee7c0-156">On the **Sources** tool, in the **Page** section, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="ee7c0-157">De nuevo, los archivos que ya están en la carpeta invalidaciones tienen un punto púrpura en el icono.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-157">Again, files that are already in your overrides folder have a purple dot on the icon.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-safe-from-sources.msft.png" alt-text="Elegir un archivo de la herramienta Orígenes para invalidaciones" lightbox="../media/javascript-overrides-safe-from-sources.msft.png":::
         <span data-ttu-id="ee7c0-159">Elegir un archivo de la **herramienta Orígenes** para invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-159">Choose a file from the **Sources** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="ee7c0-160">Como alternativa, en la **herramienta Red,** mantenga el mouse en cualquier archivo, abra el menú contextual \(haga clic con el botón secundario\) y agrégálo a invalidaciones.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-160">Alternatively, on the **Network** tool, hover on any file, open the contextual menu \(right-click\), and add it to overrides.</span></span>  <span data-ttu-id="ee7c0-161">Cuando las invalidaciones están en vigor, los archivos que se encuentran en el equipo y no desde la página web en directo.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-161">When overrides are in effect, files that are located on your computer and not from the live webpage.</span></span>  <span data-ttu-id="ee7c0-162">Cuando las invalidaciones estén en vigor, en la **herramienta Red,** busque un icono de advertencia junto al nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-162">When overrides are in effect, on the **Network** tool, locate a warning icon next to the file name.</span></span>  
      
      :::image type="complex" source="../media/javascript-overrides-network.msft.png" alt-text="Elegir un archivo de la herramienta Red para invalidaciones" lightbox="../media/javascript-overrides-network.msft.png":::
         <span data-ttu-id="ee7c0-164">Elegir un archivo de la **herramienta Red** para invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-164">Choose a file from the **Network** tool for overrides</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <a name="two-way-interaction-of-overrides"></a><span data-ttu-id="ee7c0-165">Interacción en dos sentidos de invalidaciones</span><span class="sxs-lookup"><span data-stu-id="ee7c0-165">Two-way interaction of overrides</span></span>  

<span data-ttu-id="ee7c0-166">Use el editor proporcionado con la **herramienta Orígenes** de DevTools o cualquier editor que desee cambiar los archivos.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-166">Use the editor provided with the **Sources** tool of DevTools or any editor you want to change the files.</span></span>  <span data-ttu-id="ee7c0-167">Los cambios se sincronizan en todos los productos que tienen acceso a los archivos de la carpeta invalidaciones.</span><span class="sxs-lookup"><span data-stu-id="ee7c0-167">Changes are synced across all the products that access the files in the overrides folder.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="ee7c0-168">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ee7c0-168">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsSourcesTool]: ../sources/index.md "Información general sobre la herramienta sources | Microsoft Docs"  
