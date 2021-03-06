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
# <a name="use-the-web-app-manifest-to-integrate-your-progressive-web-app-into-the-operating-system"></a><span data-ttu-id="c5dfc-104">Usar el manifiesto de aplicación web para integrar la aplicación web progresiva en el sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c5dfc-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="c5dfc-105">Un manifiesto de aplicación web de un sitio web rige el aspecto y el comportamiento de la aplicación web progresiva \(PWA\) cuando se instala en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="c5dfc-106">En el nivel más básico, el manifiesto proporciona detalles sobre el nombre de la aplicación, los iconos que se usarán para representar la aplicación en los menús del sistema y los colores del tema que el sistema operativo \(OS\) usa en la barra de título.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="c5dfc-107">El manifiesto también te permite desbloquear características eficaces que permiten que la aplicación se comporte como otras aplicaciones nativas del sistema.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <a name="use-shortcuts-to-provide-quick-access-to-features"></a><span data-ttu-id="c5dfc-108">Usar accesos directos para proporcionar acceso rápido a las características</span><span class="sxs-lookup"><span data-stu-id="c5dfc-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="c5dfc-109">La mayoría de los sistemas operativos proporcionan acceso rápido a las características clave de la aplicación mediante accesos directos en el menú contextual conectado al icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="c5dfc-110">Para usar accesos directos en tu PWA, incluye la `shortcuts` propiedad en el manifiesto de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="c5dfc-111">El siguiente fragmento de código muestra cómo definir un acceso directo en el manifiesto de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-111">The following code snippet displays how to define a shortcut in your web app manifest.</span></span>  

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

<span data-ttu-id="c5dfc-112">Cuando se agrega a un manifiesto de aplicación web completo, agregar el fragmento de código anterior habilita dos accesos directos en el menú contextual del icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="c5dfc-113">El primero tiene un `Play Later` nombre y un icono personalizado.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="c5dfc-114">El segundo tiene nombre `Subscriptions` y no tiene un icono porque la propiedad es `icons` opcional.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="c5dfc-115">La `description` propiedad también es opcional y puede usarse para proporcionar información adicional con fines de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <a name="identify-your-app-as-a-share-target"></a><span data-ttu-id="c5dfc-116">Identificar la aplicación como un destino de recurso compartido</span><span class="sxs-lookup"><span data-stu-id="c5dfc-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="c5dfc-117">Muchos sistemas operativos permiten a los usuarios compartir rápidamente vínculos y archivos con aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="c5dfc-118">Las aplicaciones web progresivas también pueden participar en esta característica mediante el `share_target` miembro del manifiesto de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-118">Progressive Web Apps can participate in this feature as well, using the `share_target` member of the Web App Manifest.</span></span>  <span data-ttu-id="c5dfc-119">Con `share_target` , se define la página \(similar a un formulario\) y los parámetros que espera que se `"action"` pasen a ella.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-119">Using `share_target`, you define the `"action"` page \(similar to a form\) and the parameters you expect to be passed into it.</span></span>  <span data-ttu-id="c5dfc-120">El siguiente fragmento de código muestra un ejemplo de cómo usar `share_target` .</span><span class="sxs-lookup"><span data-stu-id="c5dfc-120">The following code snippet displays an example of how to use `share_target`.</span></span>

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

<span data-ttu-id="c5dfc-121">Cuando se agrega al manifiesto de aplicación web, se establece `"/share.html"` como la página de acción de un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-121">When added to the Web App Manifest, this establishes `"/share.html"` as the action page for a share.</span></span> <span data-ttu-id="c5dfc-122">Además, define tres parámetros que se pasarán a esa página de acción: `"title"` , `"text"` y `"url"` .</span><span class="sxs-lookup"><span data-stu-id="c5dfc-122">Additionally, it defines three parameters that would be passed to that action page:`"title"`, `"text"`, and `"url"`.</span></span>  <span data-ttu-id="c5dfc-123">Estos parámetros se almacenarán en `"name"` las propiedades , y del objeto `"description"` `"link"` [ShareData.][GitHubWicgWebShareDomSharedata]</span><span class="sxs-lookup"><span data-stu-id="c5dfc-123">These parameters will be stored in the `"name"`, `"description"`, and `"link"` properties of the [ShareData][GitHubWicgWebShareDomSharedata] object.</span></span>  <span data-ttu-id="c5dfc-124">De forma predeterminada, la página de acción recibe los parámetros como parte de una solicitud GET, pero puede especificar la solicitud y la codificación \(as \), tal como lo haría en `method` `enctype` un formulario web.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-124">By default, the action page receives the parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5dfc-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c5dfc-125">See also</span></span>  

<span data-ttu-id="c5dfc-126">Para obtener más información sobre los manifiestos de aplicación web, vaya a la siguiente lista de temas relacionados.</span><span class="sxs-lookup"><span data-stu-id="c5dfc-126">To learn more about Web App Manifests, navigate to the following list of related topics.</span></span>  

*   [<span data-ttu-id="c5dfc-127">Manifiestos de aplicación web</span><span class="sxs-lookup"><span data-stu-id="c5dfc-127">Web App Manifests</span></span>][MDNWebAppManifests]  
*   [<span data-ttu-id="c5dfc-128">Destino de recurso compartido web</span><span class="sxs-lookup"><span data-stu-id="c5dfc-128">Web Share Target</span></span>][GitHubWicgWebShareTarget]
*   [<span data-ttu-id="c5dfc-129">Recurso compartido web</span><span class="sxs-lookup"><span data-stu-id="c5dfc-129">Web Share</span></span>][GithubW3cWebShare]
    
<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifiestos de aplicación web | MDN"  

[GitHubWicgWebShareTarget]: https://wicg.github.io/web-share-target "Api de destino de recurso compartido web | WICG"
[GitHubWicgWebShareDomSharedata]: https://wicg.github.io/web-share#dom-sharedata "Diccionario de ShareData: API de recurso compartido web | WICG"  

[GithubW3cWebShare]: https://w3c.github.io/web-share/ "Api de uso compartido web | WICG"
