---
description: Más información sobre cómo crear una extensión de Microsoft Edge
title: Crear una extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: a08fc6bd604ce810895e7103f7f6384dbedc9f78
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683654"
---
# Creación de una extensión de Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

En esta guía, aprenderá a crear una extensión para Microsoft Edge.  Esta extensión de ejemplo le permite manipular CSS específicas para páginas de [docs.Microsoft.com][MicrosoftDocs] , como repasarle por la creación de un archivo de manifiesto, la interfaz de usuario y los scripts de contenido y de fondo.  

:::image type="complex" source="../media/color-changer_header.png" alt-text="El cuerpo de Docs.microsoft.com cambió a azul":::
   El cuerpo de Docs.microsoft.com cambió a azul
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

En este tutorial se supone que tiene conocimientos básicos sobre qué es una extensión de explorador y cómo funciona.  Para obtener más información sobre los bloques de creación de las extensiones, vea [anatomía de una extensión][MDNAnatomyExtension].  

Descarga el código de la [muestra completa en github][GithubMicrosoftEdgeExtensionsDemosColorChanger].  

## Crear el archivo de manifiesto  

Para empezar, cree un directorio para la extensión y asígnele un nombre `color-changer` .  

En la `color-changer` carpeta, cree un archivo denominado `manifest.json` .  El `manifest.json` archivo es necesario para todas las extensiones y proporciona información importante para la extensión, desde el nombre de la extensión a los permisos.  

> [!NOTE] 
> Esta guía le guiará por todas las claves del manifiesto que debe usar en esta guía, pero para obtener una lista de todas las claves de manifiesto compatibles y recomendadas, consulte [claves de manifiesto admitidas][ExtensionsApisupportManifestKeys].  

En `manifest.json` el interior, agregue el siguiente código.  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### Definiciones de clave de manifiesto  

| Key | Detalles |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | El nombre de la extensión.  |  
| [autorización][MDNManifestjsonAuthor] | El autor de la extensión.  |  
| [version][MDNManifestjsonVersion] | Número de versión de la extensión.  |  
| [description][MDNManifestjsonDescription] | La descripción de la extensión mostrada en la sección acerca del menú extensión en Microsoft Edge.  |  
| [permisos][MDNManifestjsonPermissions] | Matriz de cadenas que solicitan permisos para la extensión.  Para tu extensión, Estás solicitando permisos para ver los sitios web visitados \ ("pestañas" \) y para actualizar el contenido de las direcciones URL que coincidan con " `*://docs.microsoft.com/*` ".  |  
| [browser_action][MDNManifestjsonBrowserAction] | Contiene la información de un icono. El icono se coloca en la barra de herramientas de Microsoft Edge, a la derecha de la barra de direcciones.  |  

#### browser_action definiciones de clave  

| Key | Detalles |  
|:--- |:--- |  
| `default_icon` | El icono que se usa en la barra de herramientas.  |  
| `default_title` | El texto que se muestra cuando un usuario mantiene el puntero sobre el icono de la barra de herramientas.  |  
| `default_popup` | La ruta de acceso al archivo HTML de la ventana emergente.  |  

Ahora que ha creado el archivo de manifiesto, necesita una interfaz de usuario para la extensión.  

## Crear la ventana emergente  

Para su extensión, cree un elemento emergente para la interfaz de usuario, como se muestra a continuación.  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="La interfaz emergente de la extensión":::
   La interfaz emergente de la extensión
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

Cree un archivo con `popup.html` el nombre en la raíz de la `color-changer` carpeta.  Pegue el código siguiente en `popup.html` .  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

En `popup.html` , puedes crear un título, un párrafo y tres botones \ (AliceBlue, Cornsilk y restablecer \).  

Ahora cree una carpeta con el nombre `css` y dentro de crear un archivo denominado `styles.css` .  Agregue los siguientes estilos.  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

Esta CSS proporciona a nuestra extensión algunos estilos básicos.  Puede agregar más estilos para personalizar la extensión.  

A continuación, debe crear el archivo JavaScript que interactúa con el elemento emergente.  Cree una `js` carpeta y un archivo con el nombre `popup.js` Inside.  Actualice `popup.js` con el código siguiente.  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

En `popup.js` , la API de [Tabs][MDNApiTabs] le permite interactuar con las pestañas del explorador e insertar secuencias de comandos y estilos en el contenido de la página.  Con el método [Tabs. insertCSS ()][MDNApiTabsInsertcss] , inyecta el CSS especificado en la página, lo que cambia el encabezado de [docs.Microsoft.com][MicrosoftDocs] a un color diferente cuando se hace clic en el botón especificado.  

Ahora que ya tiene la funcionalidad emergente básica, agregue iconos a la extensión.  

## Agregar iconos  

Los iconos se usan para representar la extensión en la barra de herramientas del explorador, en el menú extensiones y en otros lugares.  Descarga los [iconos de tu extensión en github][GithubMicrosoftEdgeExtensionsDemosColorChangerImages]. Para obtener más información sobre los iconos de extensión en Microsoft Edge, consulte [Guía de diseño][ExtensionsGuidesDesignIcons].  

Después de descargar los iconos de extensión, guarde los iconos en una `images` carpeta dentro de `color-changer` .  

El icono que aparece en la barra de herramientas se establece mediante `default_icon` la tecla [browser_action][MDNManifestjsonBrowserAction] , que ya agregó al archivo de manifiesto en una sección anterior.  

La `icons` clave define los iconos que se deben usar en los menús de configuración de extensiones.  A continuación, está especificando varios iconos con diferentes tamaños para tener en cuenta diferentes resoluciones de pantalla.  El nombre de los iconos `25` y `48` el alto en píxeles de los iconos.  

En el archivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] , incluye una clave de nivel superior para `icons` .  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### Definiciones de clave de manifiesto  

| Key | Detalles |  
|:--- |:--- |  
| [iconos][MDNManifestjsonIcons] | Los iconos de la extensión con pares clave-valor en el tamaño de la imagen `px` y la ruta de la imagen en relación con el directorio raíz de la extensión. |  

> [!NOTE]
> Use los iconos denominados `inactive##.png` que se encuentran en la carpeta imágenes, más adelante en esta guía.  

## Probar la extensión  

Ahora que ha agregado la interfaz de usuario y ha creado iconos, pruebe la extensión.  Siga los pasos para [Agregar una extensión][ExtensionsGuidesAddingRemovingExtensionsAdding] a Microsoft Edge.  Después, vuelva a esta guía.  

Después de agregar la extensión, vaya a cualquier página de [docs.Microsoft.com][MicrosoftDocs] .  Verá la siguiente ventana emergente después de hacer clic en la acción del explorador.  El color del cuerpo del [docs.Microsoft.com][MicrosoftDocs] también debe cambiar de color.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="El encabezado de Docs.microsoft.com cambió a AliceBlue":::
         El encabezado de Docs.microsoft.com cambió a AliceBlue :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="El encabezado de Docs.microsoft.com cambió a Cornsilk":::
         El encabezado de Docs.microsoft.com cambió a Cornsilk :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

Si encuentra algún error o funcionalidad que no funcione, consulte la guía de las [extensiones de depuración][ExtensionsGuidesDebuggingExtensions] o descargue el [ejemplo completo en github][GithubMicrosoftEdgeExtensionsDemosColorChanger].  

## Agregar contenido y secuencias de comandos de fondo  

Ir un paso más allá y agregar lógica para deshabilitar la extensión para que no funcione en páginas fuera del dominio [docs.Microsoft.com][MicrosoftDocs] .  

Primero debe crear un [script de contenido][MDNContentScripts].  A continuación, debe crear scripts de contenido que se ejecuten en el contexto de una página web determinada, puedan tener acceso al contenido de una página web y podrán comunicarse con scripts en segundo plano.  En el `js` directorio, cree un archivo con `content.js` el nombre y agregue el código siguiente.  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

Este script obtiene la dirección URL de la página actual a través de `document.location.href` y comprueba si la página actual se encuentra en el dominio [docs.Microsoft.com][MicrosoftDocs] .  Si la página no está en el dominio [docs.Microsoft.com][MicrosoftDocs] \ (por ejemplo [https://www.bing.com/][|::ref1::|] \), las rutas de los iconos inactivos \ (iconos gris \) se envían al script de fondo con [Runtime. SendMessage ()][MDNApiRuntimeSendmessage].  

Debe actualizar el archivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] para incluir la siguiente `content_scripts` clave.  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### Definiciones de clave de manifiesto  

| Key | Detalles |  
|:--- |:---- |  
| [content_scripts][MDNManifestjsonContentScripts] | Contiene la información sobre qué scripts de contenido debe cargar el explorador. |  

#### content_scripts definiciones de clave  

| Key | Detalles |  
|:--- |:---- |  
| `matches` \ (requerido \) | El modelo de dirección URL que debe coincidir antes de cargar el script de contenido. |  
| `js` | El script que debe cargarse en las direcciones URL coincidentes. |  
| `run_at` | Especifica dónde se insertan los archivos JavaScript de la `js` clave. |  

A continuación, debe crear un [script de fondo][MDNAnatomyExtensionBackgroundScripts].  Los scripts de fondo se ejecutan en el fondo del explorador, se ejecutan independientemente de la duración de una página web o ventana del explorador, y pueden comunicarse con scripts de contenido.  

En la `js` carpeta, cree un archivo con `background.js` el nombre y agregue el código siguiente.  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

El método [Runtime.][MDNApiRuntimeOnmessage] método de mensaje escucha en [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] de la secuencia de comandos de contenido.  Si el dominio de la página no es [docs.Microsoft.com][MicrosoftDocs], el método [browserAction. setIcon ()][MDNApiBrowseractionSeticon] establece las rutas de los iconos en las imágenes inactivas.  

La secuencia de comandos también deshabilita la acción del explorador \ ([browserAction. Disable][MDApiBrowseractionDisable]\), de modo que los usuarios no puedan hacer clic en la acción del explorador fuera de una página [docs.Microsoft.com][MicrosoftDocs] .  

Debe agregar el script de fondo al archivo [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] .  Agregue la siguiente `background` clave al manifiesto.  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### Definiciones de clave de manifiesto  

| Key | Detalles|  
|:--- |:--- |  
| [fondo][MDNManifestjsonBackground] | Contiene los scripts de fondo. |  

#### definiciones de teclas de fondo  

| Key | Detalles |  
|:--- |:--- |  
| `scripts` | La ruta de acceso a un archivo JavaScript. |  
| `persistent` (obligatorio) | Debe establecerse en `true` o `false` .  Si se establece en `true` , el script de fondo se carga y se conserva para toda la sección de exploración.  Si se establece en `false` , el script de fondo se carga con un retraso y se conserva para la sesión de exploración. |  

Vuelva a cargar la extensión y vuelva a probar.  Para volver a cargar la extensión: haga clic en **...** para ver la configuración y más en Microsoft Edge, haga clic en **extensiones**, haga clic en la extensión \ (**cambiador de color**\) y haga clic en **volver a cargar extensión**.  

Ahora, abra una nueva pestaña o actualice una pestaña existente que no sea una página de [docs.Microsoft.com][MicrosoftDocs] .  Debe ver el icono inactivo y no podrá hacer clic en la acción del explorador.  

¡Enhorabuena!  Has creado una extensión para Microsoft Edge.  Ver el [ejemplo completo en github][GithubMicrosoftEdgeExtensionsDemosColorChanger].  Continúe leyendo para obtener más información sobre las extensiones.  

## Escribir una extensión más compleja  

¿Desea escribir una extensión más compleja?  Eche un vistazo a la extensión Beastify de MDN en el artículo, [su segunda extensión][MDNYourSecondWebextension].  El modelo de extensión de Microsoft Edge difiere ligeramente del modelo de extensión para Firefox, la extensión Beastify creada en [tu segunda extensión][MDNYourSecondWebextension] se adaptaba a la función en Microsoft Edge.  Compruébalo en [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].  

Mientras recorres el artículo de MDN, [tu segunda extensión][MDNYourSecondWebextension], ten en cuenta las siguientes secciones.  

### API  

Consulta la página [API compatibles][ExtensionsAPIsupportApis] para obtener una lista de las API de extensiones admitidas en Microsoft Edge.  

### Tamaños de icono  

Los tamaños de icono de extensión preferidos para Microsoft Edge son `20px` ,, `25px` `30px` y `40px` .  Otros tamaños admitidos son `19px` , `35px` y `38px` .  Para obtener más información sobre los tamaños de los iconos y procedimientos recomendados, consulte la guía de [diseño][ExtensionsGuidesDesign] .  

### JavaScript  

El modelo de extensión de Microsoft Edge no admite promesas de JavaScript.  En su lugar, use devoluciones de llamada.  Para obtener más ejemplos de cómo usar las devoluciones de llamada en una extensión, eche un vistazo a las demostraciones de [impresión rápida][GithubMicrosoftEdgeExtensionsDemosQuickPrint] y de [intercambio de texto][GithubMicrosoftEdgeExtensionsDemosTextSwap] .  

Recorra el ejemplo de [impresión rápida][GithubMicrosoftEdgeExtensionsDemosQuickPrint] en el siguiente vídeo.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### Manifest. JSON  

*   La `author` clave es necesaria en Microsoft Edge  
*   La `activeTab` clave no es compatible con Microsoft Edge  

Para obtener más información sobre [las extensiones del explorador][MDNBrowserExtensions], consulte los [documentos web de MDN][MDNWebDocs].  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Agregar una extensión: agregar, mover y quitar extensiones para Microsoft Edge | Microsoft docs"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Extensiones de depuración | Microsoft docs"  
[ExtensionsGuidesDesign]: ./design.md "Directrices de diseño para Microsoft Edge Extensions | Microsoft docs"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Iconos: pautas de diseño para las extensiones de Microsoft Edge | Microsoft docs"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md "API admitidas | Microsoft docs"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Claves de manifiesto admitidas | Microsoft docs"  

[MicrosoftDocs]: https://docs.microsoft.com "Microsoft docs"  

[MDNWebDocs]: https://developer.mozilla.org "Documentos web de MDN"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Extensiones de explorador | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Anatomía de una extensión | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Scripts en segundo plano: Anatomía de una extensión | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "browserAction. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction. setIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. el mensaje-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. sendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "fichas-API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Tabs. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Scripts de contenido | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "autor-manifest. JSON | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "Background-manifest. JSON | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest. JSON | MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Descripción: manifest. JSON | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "iconos-manifest. JSON | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "Name-manifest. JSON | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "Permissions-manifest. JSON | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "version-manifest. JSON | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Tu segunda extensión | MDN"  

[Bing]: https://www.bing.com "Bing"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Cambiador de color-MicrosoftEdge/MicrosoftEdge-Extensions-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Imágenes: cambio de color-MicrosoftEdge/MicrosoftEdge-dedemos-demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest. JSON-color Changer-MicrosoftEdge/MicrosoftEdge-dedemos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Impresión rápida: MicrosoftEdge/MicrosoftEdge: demos | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Intercambio de texto: MicrosoftEdge MicrosoftEdge-Extensions-demos | GitHub"  
