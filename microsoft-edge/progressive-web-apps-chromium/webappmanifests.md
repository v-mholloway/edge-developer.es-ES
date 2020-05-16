---
title: Usar el manifiesto de la aplicación web para integrar la aplicación web progresiva en el sistema operativo
description: Obtenga información sobre cómo usar el manifiesto de la aplicación web para integrar la aplicación web progresiva en el sistema operativo.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f493ae0c3cef3a1950b2207d66fef65055b2d959
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659296"
---
# Usar el manifiesto de la aplicación web para integrar la aplicación web progresiva en el sistema operativo

Un manifiesto de la aplicación Web de un sitio web rige el aspecto y el comportamiento de la aplicación web progresiva \ (PWA \) cuando se instala en un dispositivo.  En el nivel más básico, el manifiesto proporciona detalles sobre el nombre de la aplicación, los iconos que se usan para representar la aplicación en los menús del sistema y los colores del tema que usa el sistema operativo \ (SO \) en la barra de título.  El manifiesto también le permite desbloquear características eficaces que permiten que su aplicación se comporte como cualquier otra aplicación nativa del sistema.  

## Usar métodos abreviados para proporcionar acceso rápido a las características  

La mayoría de los sistemas operativos proporcionan acceso rápido a las características clave de la aplicación mediante accesos directos en el menú contextual conectado al icono de la aplicación.  Para usar los métodos abreviados en el PWA, incluya la `shortcuts` propiedad en el manifiesto de la aplicación Web.  En el siguiente fragmento de código se muestra cómo definir un acceso directo en el manifiesto de la aplicación Web.  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

Cuando se agrega a un manifiesto de aplicación web completo, agregar el fragmento de código anterior permite dos métodos abreviados en el menú contextual en el icono de la aplicación.  El primero es `Play Later` un nombre y tiene un icono personalizado.  El segundo es `Subscriptions` un nombre y no tiene un icono porque la `icons` propiedad es opcional.  La `description` propiedad también es opcional y se puede usar para proporcionar información adicional con fines de accesibilidad.  

## Identificar la aplicación como un destino compartido

Muchos sistemas operativos permiten a los usuarios compartir rápidamente vínculos y archivos con aplicaciones nativas. Las aplicaciones web progresivas también pueden participar en esta característica a través del `share_target` miembro del manifiesto de la aplicación Web. Con share_target, define la página "acción" (similar a un formulario) y los parámetros que espera que se le pasen. El siguiente fragmento de código muestra un ejemplo de uso `share_target` .

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

Cuando se agrega al manifiesto de la aplicación Web, se establece "/share.html" como la página de acciones para un recurso compartido. Además, define tres parámetros que se transferirían a esa página de acción: "title", "Text" y "URL". Estos parámetros se almacenarán en las propiedades "Name", "Descripción" y "link" del objeto [ShareData](https://wicg.github.io/web-share#dom-sharedata) . De forma predeterminada, la página de acción recibe estos parámetros como parte de una solicitud GET, pero puede especificar la solicitud `method` \ (como `enctype` \), tal como lo haría en un formulario Web.

## Consulte también  

Para obtener más información sobre los manifiestos de la aplicación Web, consulte la siguiente lista de temas relacionados.  

* [Manifiestos de la aplicación Web][MDNWebAppManifests]  
* [Destino de recursos compartidos Web][WICGShareTarget]
* [Compartir web][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifiestos de la aplicación Web | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "API de destino de recursos compartidos WICG"
[WICGShare]: https://w3c.github.io/web-share/ "API de uso compartido de Web | WICG"
