---
description: Extensiones Introducción a la parte 2
title: Insertar dinámicamente la imagen de la NASA debajo de la etiqueta cuerpo de página con scripts de contenido
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-cromo, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.openlocfilehash: fd2276c069116a7f69f06ae50f201e284b60f3ea
ms.sourcegitcommit: 744e2ecf42bcc427ae33e5dadbf6cd48ee0ab6a5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/17/2020
ms.locfileid: "11016732"
---
# Insertar dinámicamente la imagen de la NASA debajo de la etiqueta cuerpo de página con scripts de contenido  

<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart2]  
-->  

## Introducción  

En la parte 2, aprenderá a actualizar el menú emergente para no mostrar la imagen de los estrellas estáticos que tenía antes, pero para reemplazar la imagen con un título y un botón HTML estándar.  Este botón, cuando está seleccionado, pasa a la página de contenido la imagen de las estrellas, que está insertada en la extensión.  Esta imagen se inserta en la ficha del explorador activo.  

*   Tecnologías de extensión descritas en esta guía  
    *   Inyectar bibliotecas de JavaScript en la extensión  
    *   Exponer los recursos de extensión a las pestañas del explorador  
    *   Incluir páginas de contenido en pestañas del explorador existentes  
    *   Hacer que las páginas de contenido escuchen los mensajes de las ventanas emergentes y respondan  

## Quitar la imagen de la ventana emergente y reemplazarla por un botón  

En primer lugar, actualice el `popup.html` archivo con una marca hacia adelante recta que muestre un título y un botón.  Podrás programar ese botón muy pronto, pero por ahora, solo debes incluir una referencia a un archivo de JavaScript vacío `popup.js` .  Aquí es Update HTML.  

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
        <h1>Show the NASA Picture of the Day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

Después de actualizar la extensión y seleccionar el icono de inicio de la extensión, el tiene la siguiente ventana emergente incluye un botón Mostrar.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html Mostrar después de pulsar el icono de extensión":::
   popup.html Mostrar después de pulsar el icono de extensión
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

## Estrategia actualizada para mostrar la imagen en la parte superior de la pestaña del explorador  

Después de agregar el botón, la siguiente tarea es hacer que muestre el `images/stars.jpeg` archivo de imagen en la parte superior de la página de la pestaña activa.  

Recuerde que cada página de pestaña tiene un subproceso único y la extensión tiene un subproceso independiente.  Por lo tanto, primero debe crear un script de contenido y inyectar ese script de contenido en la página de pestañas.  Una vez que lo haya hecho, debe enviar un mensaje desde el elemento emergente a la secuencia de comandos de contenido que se ejecuta en la página de la ficha que indica el contenido, la imagen que se muestra y cómo mostrarlo.  

## Crear el JavaScript emergente para enviar un mensaje  

En primer lugar, cree `popup/popup.js` y agregue código para enviar un mensaje a su script de contenido que no haya creado, que debe crear momentáneamente e inyectar en la pestaña del explorador.  Para ello, el siguiente código agrega un `onclick` evento al botón Mostrar emergente.  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

En el `onclick` evento, lo que debe hacer es encontrar la pestaña del explorador actual \ (si solo hay una abierta, se trata de un \).  Después, una vez que encuentre esa pestaña, use la `chrome.tabs.sendmessage` API de extensión para enviar un mensaje a esa pestaña.  

En ese mensaje, debe incluir la dirección URL de la imagen que desea mostrar y desea enviar un identificador único que se debe asignar a la imagen insertada.  Puede optar por permitir que el JavaScript de inserción de contenido genere eso, pero por razones que se hacen evidentes más adelante, genera ese identificador único aquí `popup.js` y lo pasa al script de contenido que aún no se ha creado.  

Este es tu `popup/popup.js` archivo actualizado.  Además, pase el identificador de pestaña actual que necesita en una sección posterior, pero por ahora, no se usa.  

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

## Cómo conseguir que las cintas. JPEG estén disponibles desde cualquier pestaña del explorador  

Probablemente se pregunte por qué, cuando pase el, `images/stars.jpeg` debe usar la `chrome.extension.getURL` API de extensión Chrome en lugar de simplemente pasar la dirección URL relativa sin el prefijo adicional como en la sección anterior.  Por cierto, ese prefijo adicional, devuelto por `getUrl` la imagen adjunta, tiene un aspecto similar al siguiente.  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

El motivo es que se inserta la imagen con el `src` atributo del `img` elemento en la página de contenido.  La página de contenido se está ejecutando en un subproceso único que no es el mismo que el subproceso que ejecuta la extensión.  Debe exponer el archivo de imagen estática como un recurso Web para que funcione correctamente.  

Para ello, debe agregar otra entrada en el `manifest.json` archivo.  Debe declarar la imagen para que sea accesible desde cualquier pestaña del explorador.  Esa entrada es la siguiente \ (debería verla en el `manifest.json` archivo completo a continuación al agregar la declaración de script de contenido).  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

Ya ha escrito el código en el `popup.js` archivo para enviar un mensaje a la página de contenido que está insertada en la página de la pestaña activa actual, pero no ha creado e insertado esa página de contenido.  Hágalo ahora.  

## Actualizar su manifest.jspara contenido y acceso web  

La actualización `manifest.json` que incluye el `content-scripts` y `web_accessible_resources` es la siguiente.  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day.",
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

La sección que has agregado es `content_scripts` .  El atributo `matches` establecido `<all_urls>` significa que todos los archivos que se mencionan en la sección **content_scripts** se insertan en todas las páginas de la pestaña del explorador cuando se cargan.  Los tipos permitidos de archivos que se pueden insertar aquí son JavaScript y CSS.  También has añadido `libjquery.min.js` .  Podrás incluirlo en la descarga mencionada en la parte superior de la sección.  

## Agregar jQuery y comprender el subproceso asociado  

En los scripts de contenido que está inyectando, planee el uso de jQuery \ ( `$` \).  Agregó una versión de minified de jQuery y la puso en el paquete de extensión como `lib\jquery.min.js` .  Estos scripts de contenido se ejecutan en un espacio aislado individual de ordenaciones, lo que significa que jQuery inyectado en la `popup.js` Página no se comparte con el contenido.  

Tenga en cuenta que incluso si la pestaña del explorador tiene JavaScript ejecutándose en la página web cargada, el contenido insertado no tendrá acceso a él.  Los JavaScript insertados solo tienen acceso al DOM real cargado en la pestaña del explorador.  

## Agregar el agente de escucha de mensajes de script de contenido  

Este es `content-scripts\content.js` el archivo que se inyecta en todas las páginas de la pestaña del explorador en función de la `manifest.json` `content-scripts` sección.  

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

Ten en cuenta que todo lo mencionado anteriormente es registrar un `listener` con el `chrome.runtime.onMessage.addListener` método API de extensión.  Este agente de escucha espera mensajes como el que envió desde la `popup.js` Descripción anterior con el `chrome.tabs.sendMessage` método API de extensión.  

El primer parámetro del `addListener` método es una función cuyo primer parámetro, Request, son los detalles del mensaje que se pasa.  Recuerde, de `popup.js` , cuando usó el `sendMessage` método, los atributos del primer parámetro son `url` y `imageDivId` .  

Cuando el agente de escucha procesa un evento, se ejecuta la función que es el primer parámetro.  El primer parámetro de esa función es un objeto que tiene atributos asignados por `sendMessage` .  Esa función simplemente procesa las tres líneas de script jQuery.  

*   El primero inserta dinámicamente en el encabezado DOM una **\<style\>** sección que debes asignar como una `slide-image` clase al `img` elemento.  
*   La segunda anexa un `img` elemento a la parte inferior `body` de la pestaña del explorador que tiene la `slide-image` clase asignada, así como el `imageDivId` identificador del elemento de imagen.  
*   El tercero agrega un `click` evento que cubre toda la imagen, lo que permite al usuario seleccionar cualquier lugar de la imagen y esa imagen se elimina de la página \ (junto con la escucha de eventos \).  

## Agregar funcionalidad para quitar la imagen mostrada al seleccionarla  

Ahora, cuando vaya a cualquier página y seleccione el icono de **extensión** , el menú emergente aparecerá de la siguiente manera.  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="popup.html Mostrar después de pulsar el icono de extensión":::
   popup.html Mostrar después de pulsar el icono de extensión
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

Al seleccionar el `Display` botón, obtienes lo que aparece a continuación.  Si selecciona cualquier lugar de la `stars.jpeg` imagen, este elemento de imagen se quita y las páginas de pestañas se vuelven a las que se mostraban originalmente.  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Imagen que se muestra en el explorador":::
   Imagen que se muestra en el explorador
:::image-end:::

<!--![The image showing in browser][ImagePart2Showingimage]  -->  

Ya ha creado una extensión que ha enviado correctamente un mensaje desde el icono emergente de extensión, al contenido de JavaScript que se ha insertado dinámicamente en la pestaña del explorador.  Ese contenido insertado estableció el elemento de imagen para mostrar tus estrellas estáticas JPEG.  

<!-- image links -->  

<!--[ImagePart2Popupdialog]: ./media/part2-popupdialog.png "popup.html display after pressing the Extension icon"  -->  
<!--[ImagePart2Showingimage]: ./media/part2-showingimage.png "The image showing in browser"  -->

<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: ./extension-source/extension-getting-started-part2.zip "Origen del paquete de extensión completado para esta parte | Microsoft docs"  
