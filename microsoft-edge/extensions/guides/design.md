---
description: Obtenga información sobre los diversos aspectos de diseño y comportamiento de la interfaz de usuario que hay que tener en cuenta al crear extensiones de Microsoft Edge.
title: Extensiones-diseño
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, JavaScript, diseño, iconos, desarrollador
ms.openlocfilehash: 622d72453ea3ecd2897efcf8f67e1b2aa7a0937c
ms.sourcegitcommit: da768193c7ae7b611f4fbb1746f16d9818e42bac
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684067"
---
# Directrices de diseño para las extensiones de Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

La siguiente página contiene diversos aspectos de diseño y comportamiento de la interfaz de usuario que se debe tener en cuenta al crear extensiones de Microsoft Edge.  

## Iconos  

Debe crear los iconos de la extensión con un gráfico vectorial.  Debe crear algunos tamaños diferentes de su icono para la extensión y tres tamaños adicionales si desea empaquetar la extensión.  Las extensiones de Microsoft Edge no admiten iconos SVG.  

Antes de crear los iconos de extensión, debe revisar la guía de [accesibilidad][ExtensionsGuidesAccessibility] para asegurarse de que sus iconos tienen el contraste suficiente y están visibles en los temas Light y Dark de Microsoft Edge.  

Aunque se admite cualquier formato de imagen de WebKit, se recomiendan los iconos. png para la compatibilidad con la transparencia.  

### Iconos de la extensión  

Para su extensión, debe crear un tamaño de icono para la acción del explorador o la acción de la página, y un tamaño de icono para el panel **extensiones** .  Es posible proporcionar más de un tamaño para cada una para admitir pantallas de alta resolución.  

Una extensión debe tener una acción de explorador o un icono de acción de página.  Los iconos de acción del explorador y de acción de la página se pueden cambiar en tiempo de ejecución con el método [browserAction. setIcon][MSDApiBrowseractionSeticon] o el método [pageAction. setIcon][MDNApiPageactionSeticon] .  

#### Acción del explorador  

Los tamaños preferidos para las acciones del explorador y los iconos de acción de página son `20px` ,, `25px` `30px` y `40px` .  Otros tamaños admitidos son `19px` , `35px` , y `38px` .  

El siguiente fragmento de archivo [manifest. JSON][ExtensionsApisupportManifestkeys] muestra un icono de acción del explorador estándar y de alta definición que se está especificando con la tecla [browser_action][MDNManifestjsonBrowserAction] .  La misma sintaxis se aplica a la tecla [page_action][MDNManifestjsonPageAction] .  

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

Si la extensión ha establecido la acción del explorador, aparecerá en el menú acciones después de seleccionar **más (...)** o, a la derecha de la barra de direcciones, si el **botón Mostrar junto a la barra de direcciones** ha sido activado por el usuario.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Acción del explorador en el menú Acción":::
         Acción del explorador en el menú Acción :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Acción del explorador":::
         Acción del explorador :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### Acción de página  

La clave [page_action][MDNManifestjsonPageAction] tiene la misma sintaxis de manifiesto de JSON que la clave [browser_action][MDNManifestjsonBrowserAction] .  La acción de página también tiene los mismos requisitos de tamaño de icono que la acción del explorador.  

Si se especifica la acción de la página en el archivo [manifest. JSON][ExtensionsApisupportManifestkeys] , aparece dentro de la barra de direcciones siempre que se usa el método [pageAction. show][MDNApiPageactionShow] .  

:::image type="complex" source="../media/pageaction.png" alt-text="Acción de página":::
   Acción de página
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### Interfaz de usuario de administración  

Cuando los usuarios se desplazan al panel de extensiones yendo al menú **más (.** ..) y seleccionando **extensiones**, aparece un icono junto al nombre de la extensión.  

Debe especificar los siguientes tamaños de icono.  

| Key | Detalles |  
|:--- |:--- |  
| `48px` | Icono para la resolución estándar. |  
| `128px` | Icono para pantallas de alta resolución. |  
| `176px` | Icono para pantallas de mayor resolución. |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Interfaz de usuario de administración":::
   Interfaz de usuario de administración
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### Iconos para empaquetar  

Una vez que la extensión está lista para empaquetar, debe tener preparados tres tamaños de icono adicionales.  

| Tamaño | Detalles |  
|:--- |:--- |  
| 44px | Se usa en la interfaz de usuario de Windows \ (**lista**de aplicaciones, **Settings**  \>  aplicaciones**del sistema**de configuración  \>  **& características**\). |  
| aplica un fundido | Requisito de empaquetado \ (no visible en ninguna parte \). |  
| 150px | Se usa como el icono de Microsoft Store. |  


Consulte la [Guía de empaquetado manual][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] o la [Guía de formato de ManifoldJS][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] para determinar dónde se colocan estos iconos.  Depende del método de empaquetado que elijas.  

#### Icono de Microsoft Store  

Si el icono de 150px de Microsoft Store tiene un fondo transparente, el color de énfasis del dispositivo del usuario aparece como el color de fondo del icono.  

Por ejemplo, si un usuario ha seleccionado rosa como color de énfasis, el fondo transparente del icono de su tienda se muestra como rosa.  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Color de Windows acentuado":::
          Color de Windows acentuado :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Color de fondo seleccionado automáticamente":::
         Color de fondo seleccionado automáticamente :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

Si desea elegir su propio color de fondo para su Microsoft Store, debe hacer que el fondo sea opaco.  

> [!NOTE]
> El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.  [Póngase en contacto con nosotros][AkaExtensionRequest] con sus solicitudes de Microsoft Store y se considerará su solicitud para una actualización futura.  

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
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action-manifest. JSON | MDN"  
