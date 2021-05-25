---
description: Insertar de forma dinámica una imagen de la NASA debajo de la etiqueta cuerpo de la página mediante scripts de contenido
title: Crear un tutorial de extensión, parte 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo web, html, css, javascript, desarrollador, extensiones
ms.openlocfilehash: c5a17cbc55c6ccb42e06369474cd274d70742494
ms.sourcegitcommit: 31741a0c331816642ceafd20680bd3206c87c7bf
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "11579732"
---
# <a name="create-an-extension-tutorial-part-2"></a><span data-ttu-id="77a59-104">Crear un tutorial de extensión, parte 2</span><span class="sxs-lookup"><span data-stu-id="77a59-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="77a59-105">Origen del paquete de extensión completado para este elemento</span><span class="sxs-lookup"><span data-stu-id="77a59-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a><span data-ttu-id="77a59-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="77a59-106">Overview</span></span>  

<span data-ttu-id="77a59-107">En este tutorial se tratan las siguientes tecnologías de extensión.</span><span class="sxs-lookup"><span data-stu-id="77a59-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="77a59-108">Insertar bibliotecas de JavaScript en la extensión</span><span class="sxs-lookup"><span data-stu-id="77a59-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="77a59-109">Exponer activos de extensión a pestañas del explorador</span><span class="sxs-lookup"><span data-stu-id="77a59-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="77a59-110">Incluir páginas de contenido en pestañas de explorador existentes</span><span class="sxs-lookup"><span data-stu-id="77a59-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="77a59-111">Hacer que las páginas de contenido escuchen los mensajes de las ventanas emergentes y respondan</span><span class="sxs-lookup"><span data-stu-id="77a59-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="77a59-112">Aprenderás a actualizar el menú emergente para reemplazar la imagen de estrellas estáticas por un título y un botón HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="77a59-112">You'll learn to update your pop-up menu to replace your static stars image with a title and a standard HTML button.</span></span>  <span data-ttu-id="77a59-113">Ese botón, cuando se selecciona, pasa esa imagen de estrellas, que está incrustada en la extensión, a la página de contenido.</span><span class="sxs-lookup"><span data-stu-id="77a59-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="77a59-114">Esa imagen se inserta en la pestaña del explorador activo. Siga los pasos siguientes para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="77a59-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="77a59-115">Quitar la imagen de la ventana emergente y reemplazarla por un botón</span><span class="sxs-lookup"><span data-stu-id="77a59-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="77a59-116">En primer lugar, actualice `popup.html` el archivo con un marcado directo que muestre un título y un botón.</span><span class="sxs-lookup"><span data-stu-id="77a59-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="77a59-117">Programará ese botón en breve, pero por ahora, solo tiene que incluir una referencia a un archivo De JavaScript `popup.js` vacío.</span><span class="sxs-lookup"><span data-stu-id="77a59-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="77a59-118">Este es el código HTML de actualización.</span><span class="sxs-lookup"><span data-stu-id="77a59-118">Here is update HTML.</span></span>  

```html
<html>
    <head>
        <meta charset="utf-8" />
        <style>
            body {
                width: 500px;
            }
            button {
                background-color: #336dab;
                border: none;
                color: white;
                padding: 15px 32px;
                text-align: center;
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <h1>Show the NASA picture of the day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

<span data-ttu-id="77a59-119">Después de actualizar y abrir la extensión, se abre una ventana emergente con un botón para mostrar.</span><span class="sxs-lookup"><span data-stu-id="77a59-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmla pantalla después de seleccionar el icono Extensión":::
   <span data-ttu-id="77a59-121">popup.htmla pantalla después de seleccionar el icono Extensión</span><span class="sxs-lookup"><span data-stu-id="77a59-121">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="77a59-122">Actualizar estrategia para mostrar la imagen en la parte superior de la pestaña del explorador</span><span class="sxs-lookup"><span data-stu-id="77a59-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="77a59-123">Después de agregar el botón, la siguiente tarea es hacer que se active el archivo de imagen en `images/stars.jpeg` la parte superior de la página de pestaña activa.</span><span class="sxs-lookup"><span data-stu-id="77a59-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="77a59-124">Recuerde que cada página de tabulación se ejecuta en su propio subproceso.</span><span class="sxs-lookup"><span data-stu-id="77a59-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="77a59-125">Además, la extensión usa un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="77a59-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="77a59-126">En primer lugar, cree un script de contenido que se inyecte en la página de pestañas.</span><span class="sxs-lookup"><span data-stu-id="77a59-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="77a59-127">A continuación, envíe un mensaje desde la ventana emergente a ese script de contenido que se ejecuta en la página de pestaña.</span><span class="sxs-lookup"><span data-stu-id="77a59-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="77a59-128">El script de contenido recibe el mensaje, que describe qué imagen se debe mostrar.</span><span class="sxs-lookup"><span data-stu-id="77a59-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="77a59-129">Crear el JavaScript emergente para enviar un mensaje</span><span class="sxs-lookup"><span data-stu-id="77a59-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="77a59-130">En primer lugar, cree y agregue código para enviar un mensaje al script de contenido aún no creado que debe crear e insertar momentáneamente en la pestaña `popup/popup.js` del explorador.  Para ello, el siguiente código agrega un evento al `onclick` botón de presentación emergente.</span><span class="sxs-lookup"><span data-stu-id="77a59-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="77a59-131">En el `onclick` caso, busque la pestaña del explorador actual.  A continuación, use `chrome.tabs.sendmessage` la API de extensión para enviar un mensaje a esa pestaña.</span><span class="sxs-lookup"><span data-stu-id="77a59-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="77a59-132">En ese mensaje debe incluir la dirección URL de la imagen que desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="77a59-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="77a59-133">Además, envíe un identificador único para asignar a la imagen insertada.</span><span class="sxs-lookup"><span data-stu-id="77a59-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="77a59-134">Puede optar por permitir que la inserción de contenido de JavaScript genere eso, pero por motivos que se hacen evidentes más adelante, genere ese identificador único aquí y pásenlo al script de contenido aún no `popup.js` creado.</span><span class="sxs-lookup"><span data-stu-id="77a59-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="77a59-135">El siguiente fragmento de código describe el código actualizado en `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="77a59-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="77a59-136">Además, pase el identificador de pestaña actual, que se usa más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="77a59-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
    sendMessageId.onclick = function() {
        chrome.tabs.query({ active: true, currentWindow: true }, function(tabs) {
            chrome.tabs.sendMessage(
                tabs[0].id,
                {
                    url: chrome.extension.getURL("images/stars.jpeg"),
                    imageDivId: `${guidGenerator()}`,
                    tabId: tabs[0].id
                },
                function(response) {
                    window.close();
                }
            );
            function guidGenerator() {
                const S4 = function () {
                    return (((1 + Math.random()) * 0x10000) | 0).toString(16).substring(1);
                };
                return (S4() + S4() + "-" + S4() + "-" + S4() + "-" + S4() + "-" + S4() + S4() + S4());
            }
        });
    };
}
```  

4. <span data-ttu-id="77a59-137">Hacer que stars.jpeg esté disponible desde cualquier pestaña del explorador</span><span class="sxs-lookup"><span data-stu-id="77a59-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="77a59-138">Probablemente te estés preguntando por qué, cuando pases el must you use the chrome Extension API en lugar de pasar la dirección URL relativa sin el prefijo adicional como en `images/stars.jpeg` `chrome.extension.getURL` la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="77a59-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="77a59-139">Por cierto, ese prefijo adicional devuelto por con la `getUrl` imagen adjunta tiene un aspecto similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="77a59-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="77a59-140">El motivo es que está insertando la imagen mediante el `src` atributo del elemento en la página de `img` contenido.</span><span class="sxs-lookup"><span data-stu-id="77a59-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="77a59-141">La página de contenido se ejecuta en un subproceso único que no es el mismo que el subproceso que ejecuta la extensión.</span><span class="sxs-lookup"><span data-stu-id="77a59-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="77a59-142">Debe exponer el archivo de imagen estática como un activo web para que funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="77a59-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="77a59-143">Agregue otra entrada en el `manifest.json` archivo para declarar que la imagen está disponible para todas las pestañas del explorador.</span><span class="sxs-lookup"><span data-stu-id="77a59-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="77a59-144">Esa entrada es la siguiente \(debería verla en el archivo completo siguiente cuando agregue la declaración de script de contenido `manifest.json` próximamente\).</span><span class="sxs-lookup"><span data-stu-id="77a59-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="77a59-145">Ahora ha escrito el código en el archivo para enviar un mensaje a la página de contenido que está incrustada en la página de pestaña activa actual, pero no ha creado e insertado esa página `popup.js` de contenido.</span><span class="sxs-lookup"><span data-stu-id="77a59-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="77a59-146">Haz eso ahora.</span><span class="sxs-lookup"><span data-stu-id="77a59-146">Do that now.</span></span>  

5.  <span data-ttu-id="77a59-147">Actualizar el manifest.jspara el contenido y el acceso web</span><span class="sxs-lookup"><span data-stu-id="77a59-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="77a59-148">El actualizado `manifest.json` que incluye el y es el `content-scripts` `web_accessible_resources` siguiente.</span><span class="sxs-lookup"><span data-stu-id="77a59-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

```json
{
    "name": "NASA picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium extension to show the NASA picture of the day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    },
    "content_scripts": [
        {
            "matches": [
              "<all_urls>"
            ],
            "js": ["lib/jquery.min.js","content-scripts/content.js"]
        }
    ],
    "web_accessible_resources": [
        "images/*.jpeg"
    ]
}
```  

<span data-ttu-id="77a59-149">La sección que agregó es `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="77a59-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="77a59-150">El atributo se establece en , lo que significa que todos los archivos se insertan en todas las páginas de pestañas del `matches` explorador cuando se carga cada `<all_urls>` `content_scripts` pestaña.</span><span class="sxs-lookup"><span data-stu-id="77a59-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="77a59-151">Los tipos de archivos permitidos que se pueden insertar son JavaScript y CSS.</span><span class="sxs-lookup"><span data-stu-id="77a59-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="77a59-152">También agregó `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="77a59-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="77a59-153">Puedes incluirlo en la descarga mencionada en la parte superior de la sección.</span><span class="sxs-lookup"><span data-stu-id="77a59-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="77a59-154">Agregar jQuery y comprender el subproceso asociado</span><span class="sxs-lookup"><span data-stu-id="77a59-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="77a59-155">En los scripts de contenido que va a insertar, planee el uso de jQuery \( `$` \).</span><span class="sxs-lookup"><span data-stu-id="77a59-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="77a59-156">Agregó una versión minificada de jQuery y la puso en el paquete de extensión como `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="77a59-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="77a59-157">Estos scripts de contenido se ejecutan en espacios aislados individuales, lo que significa que jQuery inyectado en la `popup.js` página no se comparte con el contenido.</span><span class="sxs-lookup"><span data-stu-id="77a59-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="77a59-158">Tenga en cuenta que incluso si la pestaña del explorador tiene JavaScript ejecutándose en ella en la página web cargada, cualquier contenido inyectado no tiene acceso a eso.</span><span class="sxs-lookup"><span data-stu-id="77a59-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="77a59-159">Que JavaScript inyectado solo tiene acceso al DOM real cargado en esa pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="77a59-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="77a59-160">Agregar el agente de escucha de mensajes de script de contenido</span><span class="sxs-lookup"><span data-stu-id="77a59-160">Add the content script message listener</span></span>  

<span data-ttu-id="77a59-161">Este es el `content-scripts\content.js` archivo que se inserta en todas las pestañas del explorador según la `manifest.json` `content-scripts` sección.</span><span class="sxs-lookup"><span data-stu-id="77a59-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

```javascript
chrome.runtime.onMessage.addListener(function(request, sender, sendResponse) {
    $("body").prepend(
        `<img  src="${request.url}" id="${request.imageDivId}"
               class="slide-image" /> `
    );
    $("head").prepend(
        `<style>
          .slide-image {
              height: auto;
              width: 100vw;
          }
        </style>`
    );
    $(`#${request.imageDivId}`).click(function() {
        $(`#${request.imageDivId}`).remove(`#${request.imageDivId}`);
    });
    sendResponse({ fromcontent: "This message is from content.js" });
});
```  

<span data-ttu-id="77a59-162">Tenga en cuenta que todo lo que hace JavaScript anterior es registrar un `listener` uso del método de la API de `chrome.runtime.onMessage.addListener` extensión.</span><span class="sxs-lookup"><span data-stu-id="77a59-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="77a59-163">Este agente de escucha espera mensajes como el que envió desde el `popup.js` descrito anteriormente con el método de la API de `chrome.tabs.sendMessage` extensión.</span><span class="sxs-lookup"><span data-stu-id="77a59-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="77a59-164">El primer parámetro del método es una función cuyo primer parámetro, solicitud, es los detalles `addListener` del mensaje que se pasa.</span><span class="sxs-lookup"><span data-stu-id="77a59-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="77a59-165">Recuerde `popup.js` que, a partir de , cuando usó `sendMessage` el método, los atributos del primer parámetro son `url` y `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="77a59-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="77a59-166">Cuando el agente de escucha procesa un evento, se ejecuta la función que es el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="77a59-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="77a59-167">El primer parámetro de esa función es un objeto que tiene atributos asignados por `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="77a59-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="77a59-168">Esa función simplemente procesa las tres líneas de script de jQuery.</span><span class="sxs-lookup"><span data-stu-id="77a59-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="77a59-169">La primera línea de script inserta dinámicamente en el encabezado DOM una sección que debe asignar **\<style\>** como clase al `slide-image` `img` elemento.</span><span class="sxs-lookup"><span data-stu-id="77a59-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="77a59-170">La segunda línea de script anexa un elemento justo debajo de la pestaña del explorador que tiene asignada la clase, así como el `img` identificador de ese elemento de `body` `slide-image` `imageDivId` imagen.</span><span class="sxs-lookup"><span data-stu-id="77a59-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="77a59-171">La tercera línea de script agrega un evento que cubre toda la imagen, lo que permite al usuario seleccionar cualquier parte de la imagen y esa imagen se quita de la página \(junto con ella es escucha de `click` eventos\).</span><span class="sxs-lookup"><span data-stu-id="77a59-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="77a59-172">Agregar funcionalidad para quitar la imagen mostrada cuando se selecciona</span><span class="sxs-lookup"><span data-stu-id="77a59-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="77a59-173">Ahora, cuando vaya a cualquier página y seleccione el icono **Extensión,** el menú emergente se muestra de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="77a59-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmla pantalla después de seleccionar el icono Extensión":::
   <span data-ttu-id="77a59-175">popup.htmla pantalla después de seleccionar el icono Extensión</span><span class="sxs-lookup"><span data-stu-id="77a59-175">popup.html display after selecting the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="77a59-176">Al seleccionar el `Display` botón, obtiene lo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="77a59-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="77a59-177">Si selecciona en cualquier lugar de la imagen, se quita ese elemento de imagen y las páginas de tabulación se contraen con lo `stars.jpeg` que se mostró originalmente.</span><span class="sxs-lookup"><span data-stu-id="77a59-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="La imagen que se muestra en el explorador":::
   <span data-ttu-id="77a59-179">La imagen que se muestra en el explorador</span><span class="sxs-lookup"><span data-stu-id="77a59-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="77a59-180">Ha creado una extensión que envía correctamente un mensaje desde la ventana emergente del icono de extensión y ha insertado dinámicamente JavaScript que se ejecuta como contenido en la pestaña del explorador.  El contenido inyectado establece el elemento image para mostrar el jpeg de estrellas estáticas.</span><span class="sxs-lookup"><span data-stu-id="77a59-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Origen del paquete de extensión completado | Microsoft Docs"  
