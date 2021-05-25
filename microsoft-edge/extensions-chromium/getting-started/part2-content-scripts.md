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
# <a name="create-an-extension-tutorial-part-2"></a>Crear un tutorial de extensión, parte 2  
  
[Origen del paquete de extensión completado para este elemento][ArchiveExtensionGettingStartedPart2]    

## <a name="overview"></a>Introducción  

En este tutorial se tratan las siguientes tecnologías de extensión.
*   Insertar bibliotecas de JavaScript en la extensión  
*   Exponer activos de extensión a pestañas del explorador  
*   Incluir páginas de contenido en pestañas de explorador existentes  
*   Hacer que las páginas de contenido escuchen los mensajes de las ventanas emergentes y respondan  

Aprenderás a actualizar el menú emergente para reemplazar la imagen de estrellas estáticas por un título y un botón HTML estándar.  Ese botón, cuando se selecciona, pasa esa imagen de estrellas, que está incrustada en la extensión, a la página de contenido.  Esa imagen se inserta en la pestaña del explorador activo. Siga los pasos siguientes para obtener más detalles.

1.  Quitar la imagen de la ventana emergente y reemplazarla por un botón  

En primer lugar, actualice `popup.html` el archivo con un marcado directo que muestre un título y un botón.  Programará ese botón en breve, pero por ahora, solo tiene que incluir una referencia a un archivo De JavaScript `popup.js` vacío.  Este es el código HTML de actualización.  

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

Después de actualizar y abrir la extensión, se abre una ventana emergente con un botón para mostrar.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmla pantalla después de seleccionar el icono Extensión":::
   popup.htmla pantalla después de seleccionar el icono Extensión
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

2.  Actualizar estrategia para mostrar la imagen en la parte superior de la pestaña del explorador  

Después de agregar el botón, la siguiente tarea es hacer que se active el archivo de imagen en `images/stars.jpeg` la parte superior de la página de pestaña activa.  

Recuerde que cada página de tabulación se ejecuta en su propio subproceso. Además, la extensión usa un subproceso diferente.  En primer lugar, cree un script de contenido que se inyecte en la página de pestañas.  A continuación, envíe un mensaje desde la ventana emergente a ese script de contenido que se ejecuta en la página de pestaña. El script de contenido recibe el mensaje, que describe qué imagen se debe mostrar.  

3. Crear el JavaScript emergente para enviar un mensaje  

En primer lugar, cree y agregue código para enviar un mensaje al script de contenido aún no creado que debe crear e insertar momentáneamente en la pestaña `popup/popup.js` del explorador.  Para ello, el siguiente código agrega un evento al `onclick` botón de presentación emergente.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

En el `onclick` caso, busque la pestaña del explorador actual.  A continuación, use `chrome.tabs.sendmessage` la API de extensión para enviar un mensaje a esa pestaña.  

En ese mensaje debe incluir la dirección URL de la imagen que desea mostrar. Además, envíe un identificador único para asignar a la imagen insertada.  Puede optar por permitir que la inserción de contenido de JavaScript genere eso, pero por motivos que se hacen evidentes más adelante, genere ese identificador único aquí y pásenlo al script de contenido aún no `popup.js` creado.  

El siguiente fragmento de código describe el código actualizado en `popup/popup.js` .  Además, pase el identificador de pestaña actual, que se usa más adelante en este artículo.  

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

4. Hacer que stars.jpeg esté disponible desde cualquier pestaña del explorador  

Probablemente te estés preguntando por qué, cuando pases el must you use the chrome Extension API en lugar de pasar la dirección URL relativa sin el prefijo adicional como en `images/stars.jpeg` `chrome.extension.getURL` la sección anterior.  Por cierto, ese prefijo adicional devuelto por con la `getUrl` imagen adjunta tiene un aspecto similar al siguiente.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

El motivo es que está insertando la imagen mediante el `src` atributo del elemento en la página de `img` contenido.  La página de contenido se ejecuta en un subproceso único que no es el mismo que el subproceso que ejecuta la extensión.  Debe exponer el archivo de imagen estática como un activo web para que funcione correctamente.  

Agregue otra entrada en el `manifest.json` archivo para declarar que la imagen está disponible para todas las pestañas del explorador.  Esa entrada es la siguiente \(debería verla en el archivo completo siguiente cuando agregue la declaración de script de contenido `manifest.json` próximamente\).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Ahora ha escrito el código en el archivo para enviar un mensaje a la página de contenido que está incrustada en la página de pestaña activa actual, pero no ha creado e insertado esa página `popup.js` de contenido.  Haz eso ahora.  

5.  Actualizar el manifest.jspara el contenido y el acceso web  

El actualizado `manifest.json` que incluye el y es el `content-scripts` `web_accessible_resources` siguiente.  

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

La sección que agregó es `content_scripts` .  El atributo se establece en , lo que significa que todos los archivos se insertan en todas las páginas de pestañas del `matches` explorador cuando se carga cada `<all_urls>` `content_scripts` pestaña.  Los tipos de archivos permitidos que se pueden insertar son JavaScript y CSS.  También agregó `libjquery.min.js` .  Puedes incluirlo en la descarga mencionada en la parte superior de la sección.  

6. Agregar jQuery y comprender el subproceso asociado  

En los scripts de contenido que va a insertar, planee el uso de jQuery \( `$` \).  Agregó una versión minificada de jQuery y la puso en el paquete de extensión como `lib\jquery.min.js` .  Estos scripts de contenido se ejecutan en espacios aislados individuales, lo que significa que jQuery inyectado en la `popup.js` página no se comparte con el contenido.  

Tenga en cuenta que incluso si la pestaña del explorador tiene JavaScript ejecutándose en ella en la página web cargada, cualquier contenido inyectado no tiene acceso a eso.  Que JavaScript inyectado solo tiene acceso al DOM real cargado en esa pestaña del explorador.  

7. Agregar el agente de escucha de mensajes de script de contenido  

Este es el `content-scripts\content.js` archivo que se inserta en todas las pestañas del explorador según la `manifest.json` `content-scripts` sección.  

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

Tenga en cuenta que todo lo que hace JavaScript anterior es registrar un `listener` uso del método de la API de `chrome.runtime.onMessage.addListener` extensión.  Este agente de escucha espera mensajes como el que envió desde el `popup.js` descrito anteriormente con el método de la API de `chrome.tabs.sendMessage` extensión.  

El primer parámetro del método es una función cuyo primer parámetro, solicitud, es los detalles `addListener` del mensaje que se pasa.  Recuerde `popup.js` que, a partir de , cuando usó `sendMessage` el método, los atributos del primer parámetro son `url` y `imageDivId` .  

Cuando el agente de escucha procesa un evento, se ejecuta la función que es el primer parámetro.  El primer parámetro de esa función es un objeto que tiene atributos asignados por `sendMessage` .  Esa función simplemente procesa las tres líneas de script de jQuery.  

*   La primera línea de script inserta dinámicamente en el encabezado DOM una sección que debe asignar **\<style\>** como clase al `slide-image` `img` elemento.  
*   La segunda línea de script anexa un elemento justo debajo de la pestaña del explorador que tiene asignada la clase, así como el `img` identificador de ese elemento de `body` `slide-image` `imageDivId` imagen.  
*   La tercera línea de script agrega un evento que cubre toda la imagen, lo que permite al usuario seleccionar cualquier parte de la imagen y esa imagen se quita de la página \(junto con ella es escucha de `click` eventos\).  

8. Agregar funcionalidad para quitar la imagen mostrada cuando se selecciona  

Ahora, cuando vaya a cualquier página y seleccione el icono **Extensión,** el menú emergente se muestra de la siguiente manera.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.htmla pantalla después de seleccionar el icono Extensión":::
   popup.htmla pantalla después de seleccionar el icono Extensión
:::image-end:::

<!--![popup.html display after selecting the Extension icon][ImagePart2Popupdialog]  -->  

Al seleccionar el `Display` botón, obtiene lo que se muestra a continuación.  Si selecciona en cualquier lugar de la imagen, se quita ese elemento de imagen y las páginas de tabulación se contraen con lo `stars.jpeg` que se mostró originalmente.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="La imagen que se muestra en el explorador":::
   La imagen que se muestra en el explorador
:::image-end:::

Ha creado una extensión que envía correctamente un mensaje desde la ventana emergente del icono de extensión y ha insertado dinámicamente JavaScript que se ejecuta como contenido en la pestaña del explorador.  El contenido inyectado establece el elemento image para mostrar el jpeg de estrellas estáticas.  

<!-- image links -->  


<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/extension-getting-started-part2/extension-getting-started-part2 "Origen del paquete de extensión completado | Microsoft Docs"  
