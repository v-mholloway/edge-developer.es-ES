---
title: Usar el manifiesto de aplicación web para integrar la aplicación web progresiva en el sistema operativo
description: Aprende a usar el manifiesto de aplicación web para integrar la aplicación web progresiva en el sistema operativo.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: aplicaciones web progresivas, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 0063323b1fde94d84e70df51170726325dd0f2a9
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399102"
---
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a>Usar el manifiesto de aplicación web para integrar la aplicación web progresiva en el sistema operativo

Un manifiesto de aplicación web de un sitio web rige cómo se ve y se comporta la aplicación web progresiva \(PWA\) cuando se instala en un dispositivo.  En el nivel más básico, el manifiesto proporciona detalles sobre el nombre de la aplicación, los iconos que se usarán para representar la aplicación en los menús del sistema y los colores del tema que el sistema operativo \(OS\) usa en la barra de título.  El manifiesto también te permite desbloquear características eficaces que permiten que la aplicación se comporte como otras aplicaciones nativas del sistema.  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a>Usar accesos directos para proporcionar acceso rápido a las características  

La mayoría de los sistemas operativos proporcionan acceso rápido a las características clave de la aplicación mediante accesos directos en el menú contextual conectado al icono de la aplicación.  Para usar accesos directos en el PWA, incluya la `shortcuts` propiedad en el manifiesto de la aplicación web.  El siguiente fragmento de código muestra cómo definir un acceso directo en el manifiesto de la aplicación web.  

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

Cuando se agrega a un manifiesto de aplicación web completo, agregar el fragmento de código anterior habilita dos accesos directos en el menú contextual del icono de la aplicación.  El primero tiene un `Play Later` nombre y un icono personalizado.  El segundo tiene nombre `Subscriptions` y no tiene un icono porque la propiedad es `icons` opcional.  La `description` propiedad también es opcional y puede usarse para proporcionar información adicional con fines de accesibilidad.  

## <a name="identify-your-app-as-a-share-target"></a>Identificar la aplicación como un destino de recurso compartido

Muchos sistemas operativos permiten a los usuarios compartir rápidamente vínculos y archivos con aplicaciones nativas. Las aplicaciones web progresivas también pueden participar en esta característica mediante el `share_target` miembro del manifiesto de la aplicación web.  Con `share_target` , se define la página \(similar a un formulario\) y los parámetros que espera que se `"action"` pasen a ella.  El siguiente fragmento de código muestra un ejemplo de cómo usar `share_target` .

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

Cuando se agrega al manifiesto de aplicación web, se establece `"/share.html"` como la página de acción de un recurso compartido. Además, define tres parámetros que se pasarán a esa página de acción: `"title"` , `"text"` y `"url"` .  Estos parámetros se almacenarán en `"name"` las propiedades , y del objeto `"description"` `"link"` [ShareData.][GitHubWicgWebShareDomSharedata]  De forma predeterminada, la página de acción recibe los parámetros como parte de una solicitud GET, pero puede especificar la solicitud y la codificación \(as \), tal como lo haría en `method` `enctype` un formulario web.

## <a name="see-also"></a>Consulta también  

Para obtener más información sobre los manifiestos de aplicación web, vaya a la siguiente lista de temas relacionados.  

*   [Manifiestos de aplicación web][MDNWebAppManifests]  
*   [Destino de recurso compartido web][GitHubWicgWebShareTarget]
*   [Recurso compartido web][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifiestos de aplicación web | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Api de destino de recurso compartido web | WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "Diccionario de ShareData: API de recurso compartido web | WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "Api de uso compartido web | WICG"
