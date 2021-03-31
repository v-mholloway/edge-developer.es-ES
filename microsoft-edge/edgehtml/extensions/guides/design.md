---
description: Obtenga información sobre los diversos aspectos de diseño y comportamiento de la interfaz de usuario que hay que tener en cuenta al crear extensiones de Microsoft Edge.
title: Extensiones-diseño
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, JavaScript, diseño, iconos, desarrollador
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a32223f93baf44d2ca523e92cf9d7584ad9a8333
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236509"
---
# <span data-ttu-id="8f3f9-104">Directrices de diseño para las extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8f3f9-104">Design Guidelines For Microsoft Edge Extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="8f3f9-105">La siguiente página contiene diversos aspectos de diseño y comportamiento de la interfaz de usuario que se debe tener en cuenta al crear extensiones de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-105">The following page contains various design aspects and UI behavior to consider when creating Microsoft Edge extensions.</span></span>  

## <span data-ttu-id="8f3f9-106">Iconos</span><span class="sxs-lookup"><span data-stu-id="8f3f9-106">Icons</span></span>  

<span data-ttu-id="8f3f9-107">Debe crear los iconos de la extensión con un gráfico vectorial.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-107">You should make the icons of your extension using a vector graphic.</span></span>  <span data-ttu-id="8f3f9-108">Debe crear algunos tamaños diferentes de su icono para la extensión y tres tamaños adicionales si desea empaquetar la extensión.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-108">You must create a few different sizes of your icon for your extension, and three additional sizes if you want to package your extension.</span></span>  <span data-ttu-id="8f3f9-109">Las extensiones de Microsoft Edge no admiten iconos SVG.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-109">Microsoft Edge extensions do not support .svg icons.</span></span>  

<span data-ttu-id="8f3f9-110">Antes de crear los iconos de extensión, debe revisar la guía de [accesibilidad][ExtensionsGuidesAccessibility] para asegurarse de que sus iconos tienen el contraste suficiente y están visibles en los temas Light y Dark de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-110">Before you create your extension icons, you should review the [accessibility][ExtensionsGuidesAccessibility] guide to ensure that your icons have high enough contrast and are visible in both the light and dark themes of Microsoft Edge.</span></span>  

<span data-ttu-id="8f3f9-111">Aunque se admite cualquier formato de imagen de WebKit, se recomiendan los iconos. png para la compatibilidad con la transparencia.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-111">While any webkit image format is supported, .png icons are recommended for transparency support.</span></span>  

### <span data-ttu-id="8f3f9-112">Iconos de la extensión</span><span class="sxs-lookup"><span data-stu-id="8f3f9-112">Icons for your extension</span></span>  

<span data-ttu-id="8f3f9-113">Para su extensión, debe crear un tamaño de icono para la acción del explorador o la acción de la página, y un tamaño de icono para el panel **extensiones** .</span><span class="sxs-lookup"><span data-stu-id="8f3f9-113">For your extension, you must create one icon size for the browser action or page action, and one icon size for the **Extensions** pane.</span></span>  <span data-ttu-id="8f3f9-114">Es posible proporcionar más de un tamaño para cada una para admitir pantallas de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-114">More than one size for each may be provided to support high resolution displays.</span></span>  

<span data-ttu-id="8f3f9-115">Una extensión debe tener una acción de explorador o un icono de acción de página.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-115">An extension should have a browser action or page action icon.</span></span>  <span data-ttu-id="8f3f9-116">Los iconos de acción del explorador y de acción de la página se pueden cambiar en tiempo de ejecución con el método [browserAction. setIcon][MSDApiBrowseractionSeticon] o el método [pageAction. setIcon][MDNApiPageactionSeticon] .</span><span class="sxs-lookup"><span data-stu-id="8f3f9-116">The browser action and page action icons may be changed at runtime using the [browserAction.setIcon][MSDApiBrowseractionSeticon] method or [pageAction.setIcon][MDNApiPageactionSeticon] method.</span></span>  

#### <span data-ttu-id="8f3f9-117">Acción del explorador</span><span class="sxs-lookup"><span data-stu-id="8f3f9-117">Browser action</span></span>  

<span data-ttu-id="8f3f9-118">Los tamaños preferidos para las acciones del explorador y los iconos de acción de página son `20px` ,, `25px` `30px` y `40px` .</span><span class="sxs-lookup"><span data-stu-id="8f3f9-118">The preferred sizes for browser action and page action icons are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="8f3f9-119">Otros tamaños admitidos son `19px` , `35px` , y `38px` .</span><span class="sxs-lookup"><span data-stu-id="8f3f9-119">Other supported sizes include `19px`, `35px`, and `38px`.</span></span>  

<span data-ttu-id="8f3f9-120">La siguiente [manifest.jsen][ExtensionsApisupportManifestkeys] el fragmento de archivo muestra un icono de acción del explorador estándar y de alta definición que se especifica con la clave [browser_action][MDNManifestjsonBrowserAction] .</span><span class="sxs-lookup"><span data-stu-id="8f3f9-120">The following [manifest.json][ExtensionsApisupportManifestkeys] file snippet shows a standard and high definition browser action icon being specified using the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="8f3f9-121">La misma sintaxis se aplica a la tecla [page_action][MDNManifestjsonPageAction] .</span><span class="sxs-lookup"><span data-stu-id="8f3f9-121">The same syntax applies for the [page_action][MDNManifestjsonPageAction] key.</span></span>  

```json
"browser_action": {
    "default_icon": {
        "20": "images/icon_20.png",
        "40": "images/icon_40.png"
    },
    "default_title": "Fetch page info",
    "default_popup": "popup.html"
}
```  

<span data-ttu-id="8f3f9-122">Si la extensión ha establecido la acción del explorador, aparecerá en el menú acciones después de seleccionar **más (...)** o, a la derecha de la barra de direcciones, si el **botón Mostrar junto a la barra de direcciones** ha sido activado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-122">If the browser action has been set by the extension, it appears either in the Actions menu after selecting **More(...)**,  or to the right of the address bar if **Show button next to the address bar** has been toggled on by the user.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Acción del explorador en el menú Acción":::
         <span data-ttu-id="8f3f9-124">Acción del explorador en el menú Acción</span><span class="sxs-lookup"><span data-stu-id="8f3f9-124">Browser action in action menu</span></span> :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Acción del explorador":::
         <span data-ttu-id="8f3f9-126">Acción del explorador</span><span class="sxs-lookup"><span data-stu-id="8f3f9-126">Browser action</span></span> :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="8f3f9-127">Acción de página</span><span class="sxs-lookup"><span data-stu-id="8f3f9-127">Page action</span></span>  

<span data-ttu-id="8f3f9-128">La clave [page_action][MDNManifestjsonPageAction] tiene la misma sintaxis de manifiesto de JSON que la clave [browser_action][MDNManifestjsonBrowserAction] .</span><span class="sxs-lookup"><span data-stu-id="8f3f9-128">The [page_action][MDNManifestjsonPageAction] key has the same JSON manifest syntax as the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="8f3f9-129">La acción de página también tiene los mismos requisitos de tamaño de icono que la acción del explorador.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-129">Page action also has the same icon size requirements as browser action.</span></span>  

<span data-ttu-id="8f3f9-130">Si se especifica la acción de la página en el [manifest.js][ExtensionsApisupportManifestkeys] archivo, aparece dentro de la barra de direcciones siempre que se usa el método [pageAction. show][MDNApiPageactionShow] .</span><span class="sxs-lookup"><span data-stu-id="8f3f9-130">If page action is specified in the [manifest.json][ExtensionsApisupportManifestkeys] file, it appears within the address bar whenever the [pageAction.show][MDNApiPageactionShow] method is used.</span></span>  

:::image type="complex" source="../media/pageaction.png" alt-text="Acción de página":::
   <span data-ttu-id="8f3f9-132">Acción de página</span><span class="sxs-lookup"><span data-stu-id="8f3f9-132">Page action</span></span>
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### <span data-ttu-id="8f3f9-133">Interfaz de usuario de administración</span><span class="sxs-lookup"><span data-stu-id="8f3f9-133">Management UI</span></span>  

<span data-ttu-id="8f3f9-134">Cuando los usuarios se desplazan al panel de extensiones yendo al menú **más (.** ..) y seleccionando **extensiones**, aparece un icono junto al nombre de la extensión.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-134">When users navigate to the extensions pane by going to the **More(...)** menu and selecting **Extensions**, an icon is displayed next to the name of the extension.</span></span>  

<span data-ttu-id="8f3f9-135">Debe especificar los siguientes tamaños de icono.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-135">You should specify the following icon sizes.</span></span>  

| <span data-ttu-id="8f3f9-136">Key</span><span class="sxs-lookup"><span data-stu-id="8f3f9-136">Key</span></span> | <span data-ttu-id="8f3f9-137">Detalles</span><span class="sxs-lookup"><span data-stu-id="8f3f9-137">Details</span></span> |  
|:--- |:--- |  
| `48px` | <span data-ttu-id="8f3f9-138">Icono para la resolución estándar.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-138">Icon for standard resolution displays.</span></span> |  
| `128px` | <span data-ttu-id="8f3f9-139">Icono para pantallas de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-139">Icon for high resolution displays.</span></span> |  
| `176px` | <span data-ttu-id="8f3f9-140">Icono para pantallas de mayor resolución.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-140">Icon for even higher resolution displays.</span></span> |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Interfaz de usuario de administración":::
   <span data-ttu-id="8f3f9-142">Interfaz de usuario de administración</span><span class="sxs-lookup"><span data-stu-id="8f3f9-142">Management UI</span></span>
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### <span data-ttu-id="8f3f9-143">Iconos para empaquetar</span><span class="sxs-lookup"><span data-stu-id="8f3f9-143">Icons for packaging</span></span>  

<span data-ttu-id="8f3f9-144">Una vez que la extensión está lista para empaquetar, debe tener preparados tres tamaños de icono adicionales.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-144">Once your extension is ready for packaging, you must have three additional icon sizes ready.</span></span>  

| <span data-ttu-id="8f3f9-145">Tamaño</span><span class="sxs-lookup"><span data-stu-id="8f3f9-145">Size</span></span> | <span data-ttu-id="8f3f9-146">Detalles</span><span class="sxs-lookup"><span data-stu-id="8f3f9-146">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="8f3f9-147">44px</span><span class="sxs-lookup"><span data-stu-id="8f3f9-147">44px</span></span> | <span data-ttu-id="8f3f9-148">Se usa en la interfaz de usuario de Windows \(**lista**de aplicaciones,   \>  aplicaciones**del sistema**de configuración  \>  **& características**\).</span><span class="sxs-lookup"><span data-stu-id="8f3f9-148">Used in the Windows UI \(**App List**, **Settings** \> **System** \> **Apps & features**\).</span></span> |  
| <span data-ttu-id="8f3f9-149">aplica un fundido</span><span class="sxs-lookup"><span data-stu-id="8f3f9-149">50px</span></span> | <span data-ttu-id="8f3f9-150">Requisito de empaquetado \(no visible en ninguna parte \).</span><span class="sxs-lookup"><span data-stu-id="8f3f9-150">Packaging requirement \(not visible anywhere\).</span></span> |  
| <span data-ttu-id="8f3f9-151">150px</span><span class="sxs-lookup"><span data-stu-id="8f3f9-151">150px</span></span> | <span data-ttu-id="8f3f9-152">Se usa como el icono de Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-152">Used as the icon for the Microsoft Store.</span></span> |  


<span data-ttu-id="8f3f9-153">Consulte la [Guía de empaquetado manual][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] o la [Guía de formato de ManifoldJS][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] para determinar dónde se colocan estos iconos.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-153">See either the [manual packaging guide][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] or the [ManifoldJS packaging guide][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] to determine where these icons is placed.</span></span>  <span data-ttu-id="8f3f9-154">Depende del método de empaquetado que elijas.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-154">This depends upon which packaging method you choose.</span></span>  

#### <span data-ttu-id="8f3f9-155">Icono de Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="8f3f9-155">Microsoft Store icon</span></span>  

<span data-ttu-id="8f3f9-156">Si el icono de 150px de Microsoft Store tiene un fondo transparente, el color de énfasis del dispositivo del usuario aparece como el color de fondo del icono.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-156">If the 150px icon for the Microsoft Store has a transparent background, the accent color of the user's device appears as the background color of the icon.</span></span>  

<span data-ttu-id="8f3f9-157">Por ejemplo, si un usuario ha seleccionado rosa como color de énfasis, el fondo transparente del icono de su tienda se muestra como rosa.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-157">For example, if a user has selected pink as the accent color, the transparent background of your store icon is displayed as pink.</span></span>  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Color de Windows acentuado":::
          <span data-ttu-id="8f3f9-159">Color de Windows acentuado</span><span class="sxs-lookup"><span data-stu-id="8f3f9-159">Windows accent color</span></span> :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Color de fondo seleccionado automáticamente":::
         <span data-ttu-id="8f3f9-161">Color de fondo seleccionado automáticamente</span><span class="sxs-lookup"><span data-stu-id="8f3f9-161">Background color auto selected</span></span> :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

<span data-ttu-id="8f3f9-162">Si desea elegir su propio color de fondo para su Microsoft Store, debe hacer que el fondo sea opaco.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-162">If you want to pick your own background color for your Microsoft Store, you must make the background opaque.</span></span>  

> [!NOTE]
> <span data-ttu-id="8f3f9-163">El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-163">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="8f3f9-164">[Póngase en contacto con nosotros][AkaExtensionRequest] con sus solicitudes de Microsoft Store y se considerará su solicitud para una actualización futura.</span><span class="sxs-lookup"><span data-stu-id="8f3f9-164">[Contact us][AkaExtensionRequest] with your requests for the Microsoft Store, and your request is considered for a future update.</span></span>  

<!-- image links -->  

<!--[ImageActionmenuBrowseraction]: ../media/actionmenu-browseraction.png "browser action in action menu"  -->  
<!--[ImageBrowserActionIcon]: ../media/browseractionicon.png "browser action"  -->  
<!--[ImagePageaction]: ../media/pageaction.png "page action"  -->  
<!--[ImageManagementUi]: ../media/management-ui.png "management UI"  -->  
<!--[ImageWindowsAccentColor]: ../media/windows-accent-color.png "Windows accent color"  -->  
<!--[ImageStoreIconTransparencyBackground]: ../media/store-icon-with-transparent-background.png "Background color auto selected"  -->  

<!-- links -->  

[ExtensionsGuidesAccessibility]: ./accessibility.md "Accesibilidad | Microsoft docs"  
[ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder]: ./packaging/creating-and-testing-extension-packages.md#assets-folder "Carpeta activos: crear y probar un paquete AppX de extensión de Microsoft Edge | Microsoft docs"  
[ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]: ./packaging/using-manifoldjs-to-package-extensions.md#packaging-with-manifoldjs "Empaquetado con ManifoldJS: uso de ManifoldJS para crear paquetes AppX de extensión | Microsoft docs"  

[ExtensionsApisupportManifestkeys]: ../API-support/supported-manifest-keys.md "Claves de manifiesto admitidas | Microsoft docs"  

[AkaExtensionRequest]: https://aka.ms/extension-request "Comunicarse con nosotros"  

[MSDApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction. setIcon ()-API | MDN"  
[MDNApiPageactionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/setIcon "pageAction. setIcon ()-API | MDN"  
[MDNApiPageactionShow]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/show "pageAction. Show ()-API | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action manifest.jsen | MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action manifest.jsen | MDN"  
