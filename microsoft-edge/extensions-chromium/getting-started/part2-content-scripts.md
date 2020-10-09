---
description: Insertar dinámicamente la imagen de la NASA debajo de la etiqueta cuerpo de página con scripts de contenido
title: Crear un tutorial de extensiones, parte 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-cromo, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.openlocfilehash: 755b70635c93d7331ef3ac985625ba7ac5689679
ms.sourcegitcommit: 845a0d53a86bee3678f421adee26b3372cefce57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/08/2020
ms.locfileid: "11104717"
---
# <span data-ttu-id="fd92a-104">Crear un tutorial de extensiones, parte 2</span><span class="sxs-lookup"><span data-stu-id="fd92a-104">Create an extension tutorial Part 2</span></span>  
  
[<span data-ttu-id="fd92a-105">Origen del paquete de extensión completado para este elemento</span><span class="sxs-lookup"><span data-stu-id="fd92a-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]    

## <span data-ttu-id="fd92a-106">Introducción</span><span class="sxs-lookup"><span data-stu-id="fd92a-106">Overview</span></span>  

<span data-ttu-id="fd92a-107">En este tutorial se tratan las siguientes tecnologías de extensión.</span><span class="sxs-lookup"><span data-stu-id="fd92a-107">This tutorial covers the following extension technologies.</span></span>
*   <span data-ttu-id="fd92a-108">Inyectar bibliotecas de JavaScript en la extensión</span><span class="sxs-lookup"><span data-stu-id="fd92a-108">Injecting JavaScript libraries into extension</span></span>  
*   <span data-ttu-id="fd92a-109">Exponer los recursos de extensión a las pestañas del explorador</span><span class="sxs-lookup"><span data-stu-id="fd92a-109">Exposing extension assets to browser tabs</span></span>  
*   <span data-ttu-id="fd92a-110">Incluir páginas de contenido en pestañas del explorador existentes</span><span class="sxs-lookup"><span data-stu-id="fd92a-110">Including content pages in existing browser tabs</span></span>  
*   <span data-ttu-id="fd92a-111">Hacer que las páginas de contenido escuchen los mensajes de las ventanas emergentes y respondan</span><span class="sxs-lookup"><span data-stu-id="fd92a-111">Having content pages listen for messages from pop-ups and respond</span></span>  

<span data-ttu-id="fd92a-112">Aprenderá a actualizar el menú emergente para reemplazar la imagen de inicios estáticos con un título y un botón estándar de HTML.</span><span class="sxs-lookup"><span data-stu-id="fd92a-112">You'll learn to update your pop-up menu to replace your static starts image with a title and a standard HTML button.</span></span>  <span data-ttu-id="fd92a-113">Este botón, cuando está seleccionado, pasa a la página de contenido la imagen de las estrellas, que está insertada en la extensión.</span><span class="sxs-lookup"><span data-stu-id="fd92a-113">That button, when selected, passes that stars image, which is embedded in the extension, to the content page.</span></span>  <span data-ttu-id="fd92a-114">Esta imagen se inserta en la ficha del explorador activo. Siga los pasos a continuación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fd92a-114">That image, is inserted into the active browser tab. Follow the below steps for further details.</span></span>

1.  <span data-ttu-id="fd92a-115">Quitar la imagen de la ventana emergente y reemplazarla por un botón</span><span class="sxs-lookup"><span data-stu-id="fd92a-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="fd92a-116">En primer lugar, actualice el `popup.html` archivo con una marca hacia adelante recta que muestre un título y un botón.</span><span class="sxs-lookup"><span data-stu-id="fd92a-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="fd92a-117">Programará ese botón muy pronto, pero por ahora, solo tienes que incluir una referencia a un archivo de JavaScript vacío `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="fd92a-117">You'll program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="fd92a-118">Aquí es Update HTML.</span><span class="sxs-lookup"><span data-stu-id="fd92a-118">Here is update HTML.</span></span>  

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

<span data-ttu-id="fd92a-119">Después de actualizar y abrir la extensión, se abre un elemento emergente con un botón Mostrar.</span><span class="sxs-lookup"><span data-stu-id="fd92a-119">After updating and opening the extension, a pop-up opens with a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html Mostrar después de pulsar el icono de extensión":::
   <span data-ttu-id="fd92a-121">popup.html Mostrar después de pulsar el icono de extensión</span><span class="sxs-lookup"><span data-stu-id="fd92a-121">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

2.  <span data-ttu-id="fd92a-122">Estrategia de actualización para mostrar la imagen en la parte superior de la pestaña del explorador</span><span class="sxs-lookup"><span data-stu-id="fd92a-122">Update strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="fd92a-123">Después de agregar el botón, la siguiente tarea es hacer que muestre el `images/stars.jpeg` archivo de imagen en la parte superior de la página de la pestaña activa.</span><span class="sxs-lookup"><span data-stu-id="fd92a-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="fd92a-124">Recuerde que cada página de pestaña se ejecuta en su propio subproceso.</span><span class="sxs-lookup"><span data-stu-id="fd92a-124">Remember, each tab page runs in its own thread.</span></span> <span data-ttu-id="fd92a-125">Además, la extensión usa un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="fd92a-125">Also, the extension uses a different thread.</span></span>  <span data-ttu-id="fd92a-126">En primer lugar, cree un script de contenido que se inserte en la página de pestañas.</span><span class="sxs-lookup"><span data-stu-id="fd92a-126">First, create a content script that is injected into the tab page.</span></span>  <span data-ttu-id="fd92a-127">Después, envíe un mensaje desde el elemento emergente a la secuencia de comandos de contenido que se ejecuta en la página de pestañas.</span><span class="sxs-lookup"><span data-stu-id="fd92a-127">Then, send a message from your pop-up to that content script running on the tab page.</span></span> <span data-ttu-id="fd92a-128">El script de contenido recibe el mensaje, que describe qué imagen se debe mostrar.</span><span class="sxs-lookup"><span data-stu-id="fd92a-128">The content script receives the message, which describes which image should be displayed.</span></span>  

3. <span data-ttu-id="fd92a-129">Crear el JavaScript emergente para enviar un mensaje</span><span class="sxs-lookup"><span data-stu-id="fd92a-129">Create the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="fd92a-130">En primer lugar, cree `popup/popup.js` y agregue código para enviar un mensaje a su script de contenido que no haya creado, que debe crear momentáneamente e inyectar en la pestaña del explorador.  Para ello, el siguiente código agrega un `onclick` evento al botón Mostrar emergente.</span><span class="sxs-lookup"><span data-stu-id="fd92a-130">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="fd92a-131">En el `onclick` evento, busque la pestaña actual del explorador.  Después, usa la `chrome.tabs.sendmessage` API de extensión para enviar un mensaje a esa pestaña.</span><span class="sxs-lookup"><span data-stu-id="fd92a-131">In the `onclick` event, find the current browser tab.  Then, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="fd92a-132">En ese mensaje, debe incluir la dirección URL de la imagen que desea mostrar.</span><span class="sxs-lookup"><span data-stu-id="fd92a-132">In that message you must include the URL to the image you want to display.</span></span> <span data-ttu-id="fd92a-133">Además, envía un identificador único para asignar a la imagen insertada.</span><span class="sxs-lookup"><span data-stu-id="fd92a-133">Also, send a unique ID to assign to the inserted image.</span></span>  <span data-ttu-id="fd92a-134">Puede optar por permitir que el JavaScript de inserción de contenido genere eso, pero por razones que se hacen evidentes más adelante, genera ese identificador único aquí `popup.js` y lo pasa al script de contenido que aún no se ha creado.</span><span class="sxs-lookup"><span data-stu-id="fd92a-134">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="fd92a-135">En el siguiente fragmento de código se describe el código actualizado en `popup/popup.js` .</span><span class="sxs-lookup"><span data-stu-id="fd92a-135">The following code snippet outlines the updated code in `popup/popup.js`.</span></span>  <span data-ttu-id="fd92a-136">Además, pasa el identificador de pestaña actual, que se usa más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="fd92a-136">Also, pass in the current tab ID, which is used later in this article.</span></span>  

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

4. <span data-ttu-id="fd92a-137">Hacer que las estrellas. JPEG estén disponibles desde cualquier pestaña del explorador</span><span class="sxs-lookup"><span data-stu-id="fd92a-137">Make your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="fd92a-138">Probablemente se pregunte por qué, cuando pase el, `images/stars.jpeg` debe usar la `chrome.extension.getURL` API de extensión Chrome en lugar de simplemente pasar la dirección URL relativa sin el prefijo adicional como en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="fd92a-138">You're probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="fd92a-139">Por cierto, ese prefijo adicional, devuelto por `getUrl` la imagen adjunta, tiene un aspecto similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="fd92a-139">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="fd92a-140">El motivo es que se inserta la imagen con el `src` atributo del `img` elemento en la página de contenido.</span><span class="sxs-lookup"><span data-stu-id="fd92a-140">The reason is that you're injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="fd92a-141">La página de contenido se está ejecutando en un subproceso único que no es el mismo que el subproceso que ejecuta la extensión.</span><span class="sxs-lookup"><span data-stu-id="fd92a-141">The content page is running on a unique thread that isn't the same as the thread running the Extension.</span></span>  <span data-ttu-id="fd92a-142">Debe exponer el archivo de imagen estática como un recurso Web para que funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="fd92a-142">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="fd92a-143">Agregue otra entrada en el `manifest.json` archivo para declarar que la imagen está disponible para todas las pestañas del explorador.</span><span class="sxs-lookup"><span data-stu-id="fd92a-143">Add another entry in the `manifest.json` file to declare that the image is available to all browser tabs.</span></span>  <span data-ttu-id="fd92a-144">Esa entrada es la siguiente \ (debería verla en el `manifest.json` archivo completo a continuación al agregar la declaración de script de contenido).</span><span class="sxs-lookup"><span data-stu-id="fd92a-144">That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="fd92a-145">Ya ha escrito el código en el `popup.js` archivo para enviar un mensaje a la página de contenido que está insertada en la página de la pestaña activa actual, pero no ha creado e insertado esa página de contenido.</span><span class="sxs-lookup"><span data-stu-id="fd92a-145">You've now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you haven't created and injected that content page.</span></span>  <span data-ttu-id="fd92a-146">Hágalo ahora.</span><span class="sxs-lookup"><span data-stu-id="fd92a-146">Do that now.</span></span>  

5.  <span data-ttu-id="fd92a-147">Actualizar su manifest.jspara contenido y acceso web</span><span class="sxs-lookup"><span data-stu-id="fd92a-147">Update your manifest.json for content and web access</span></span>  

<span data-ttu-id="fd92a-148">La actualización `manifest.json` que incluye el `content-scripts` y `web_accessible_resources` es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="fd92a-148">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

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

<span data-ttu-id="fd92a-149">La sección que has agregado es `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="fd92a-149">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="fd92a-150">El `matches` atributo se establece en `<all_urls>` , lo que significa que todos los archivos de `content_scripts` se insertan en todas las páginas de la pestaña del explorador cuando se carga cada pestaña.</span><span class="sxs-lookup"><span data-stu-id="fd92a-150">The `matches` attribute is set to `<all_urls>`, which means that all files in `content_scripts` are injected into all browser tab pages when each tab is loaded.</span></span>  <span data-ttu-id="fd92a-151">Los tipos de archivos permitidos que se pueden insertar son JavaScript y CSS.</span><span class="sxs-lookup"><span data-stu-id="fd92a-151">The allowed files types that can be injected are JavaScript and CSS.</span></span>  <span data-ttu-id="fd92a-152">También has añadido `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="fd92a-152">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="fd92a-153">Podrás incluirlo en la descarga mencionada en la parte superior de la sección.</span><span class="sxs-lookup"><span data-stu-id="fd92a-153">You're able to include that from the download mentioned at the top of the section.</span></span>  

6. <span data-ttu-id="fd92a-154">Agregar jQuery y comprender el subproceso asociado</span><span class="sxs-lookup"><span data-stu-id="fd92a-154">Add jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="fd92a-155">En los scripts de contenido que está inyectando, planee el uso de jQuery \ ( `$` \).</span><span class="sxs-lookup"><span data-stu-id="fd92a-155">In the content scripts that you're injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="fd92a-156">Agregó una versión de minified de jQuery y la puso en el paquete de extensión como `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="fd92a-156">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="fd92a-157">Estos scripts de contenido se ejecutan en entornos limitados individuales, lo que significa que jQuery inyectado en la `popup.js` Página no se comparte con el contenido.</span><span class="sxs-lookup"><span data-stu-id="fd92a-157">These content scripts run in individual sandboxes, which means that the jQuery injected into the `popup.js` page isn't shared with the content.</span></span>  

<span data-ttu-id="fd92a-158">Tenga en cuenta que incluso si la pestaña del explorador tiene JavaScript ejecutándose en la página web cargada, el contenido insertado no tiene acceso a él.</span><span class="sxs-lookup"><span data-stu-id="fd92a-158">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected doesn't have access to that.</span></span>  <span data-ttu-id="fd92a-159">Los JavaScript insertados solo tienen acceso al DOM real cargado en la pestaña del explorador.</span><span class="sxs-lookup"><span data-stu-id="fd92a-159">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

7. <span data-ttu-id="fd92a-160">Agregar el agente de escucha de mensajes de script de contenido</span><span class="sxs-lookup"><span data-stu-id="fd92a-160">Add the content script message listener</span></span>  

<span data-ttu-id="fd92a-161">Este es `content-scripts\content.js` el archivo que se inyecta en todas las páginas de la pestaña del explorador en función de la `manifest.json` `content-scripts` sección.</span><span class="sxs-lookup"><span data-stu-id="fd92a-161">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

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

<span data-ttu-id="fd92a-162">Ten en cuenta que todo lo mencionado anteriormente es registrar un `listener` con el `chrome.runtime.onMessage.addListener` método API de extensión.</span><span class="sxs-lookup"><span data-stu-id="fd92a-162">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="fd92a-163">Este agente de escucha espera mensajes como el que envió desde la `popup.js` Descripción anterior con el `chrome.tabs.sendMessage` método API de extensión.</span><span class="sxs-lookup"><span data-stu-id="fd92a-163">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="fd92a-164">El primer parámetro del `addListener` método es una función cuyo primer parámetro, Request, son los detalles del mensaje que se pasa.</span><span class="sxs-lookup"><span data-stu-id="fd92a-164">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="fd92a-165">Recuerde, de `popup.js` , cuando usó el `sendMessage` método, los atributos del primer parámetro son `url` y `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="fd92a-165">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="fd92a-166">Cuando el agente de escucha procesa un evento, se ejecuta la función que es el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="fd92a-166">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="fd92a-167">El primer parámetro de esa función es un objeto que tiene atributos asignados por `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="fd92a-167">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="fd92a-168">Esa función simplemente procesa las tres líneas de script jQuery.</span><span class="sxs-lookup"><span data-stu-id="fd92a-168">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="fd92a-169">La primera línea de la secuencia de comandos inserta dinámicamente en el encabezado DOM una **\<style\>** sección que debe asignar como `slide-image` clase al `img` elemento.</span><span class="sxs-lookup"><span data-stu-id="fd92a-169">The first script line dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="fd92a-170">La segunda línea del script anexa un `img` elemento a la parte inferior `body` de la pestaña del explorador que tiene la `slide-image` clase asignada, así como el `imageDivId` identificador del elemento de imagen.</span><span class="sxs-lookup"><span data-stu-id="fd92a-170">The second script line appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="fd92a-171">La tercera línea de la secuencia de comandos agrega un `click` evento que cubre toda la imagen, lo que permite al usuario seleccionar en cualquier lugar de la imagen y esa imagen se elimina de la página \ (junto con la escucha de eventos \).</span><span class="sxs-lookup"><span data-stu-id="fd92a-171">The third script line adds a `click` event that covers the entire image allowing the user to select anywhere on the image and that image is removed from the page \(along with it is event listener\).</span></span>  

8. <span data-ttu-id="fd92a-172">Agregar funcionalidad para quitar la imagen mostrada al seleccionarla</span><span class="sxs-lookup"><span data-stu-id="fd92a-172">Add functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="fd92a-173">Ahora, cuando vaya a cualquier página y seleccione el icono de **extensión** , el menú emergente aparecerá de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="fd92a-173">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html Mostrar después de pulsar el icono de extensión":::
   <span data-ttu-id="fd92a-175">popup.html Mostrar después de pulsar el icono de extensión</span><span class="sxs-lookup"><span data-stu-id="fd92a-175">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="fd92a-176">Al seleccionar el `Display` botón, obtienes lo que aparece a continuación.</span><span class="sxs-lookup"><span data-stu-id="fd92a-176">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="fd92a-177">Si selecciona cualquier lugar de la `stars.jpeg` imagen, este elemento de imagen se quita y las páginas de pestañas se vuelven a las que se mostraban originalmente.</span><span class="sxs-lookup"><span data-stu-id="fd92a-177">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="popup.html Mostrar después de pulsar el icono de extensión":::
   <span data-ttu-id="fd92a-179">Imagen que se muestra en el explorador</span><span class="sxs-lookup"><span data-stu-id="fd92a-179">The image showing in browser</span></span>
:::image-end:::

<span data-ttu-id="fd92a-180">Ha creado una extensión que envía correctamente un mensaje desde el icono emergente de la extensión e insertado dinámicamente en JavaScript que se ejecuta como contenido en la pestaña del explorador.  El contenido insertado establece el elemento de imagen para que muestre sus estrellas estáticas JPEG.</span><span class="sxs-lookup"><span data-stu-id="fd92a-180">You've created an Extension that successfully sends a message from the extension icon pop-up, and dynamically inserted JavaScript running as content on the browser tab.  The injected content sets the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Origen del paquete de extensión completado | Microsoft docs"  
