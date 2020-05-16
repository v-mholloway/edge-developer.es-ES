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
# <span data-ttu-id="27fd1-104">Usar el manifiesto de la aplicación web para integrar la aplicación web progresiva en el sistema operativo</span><span class="sxs-lookup"><span data-stu-id="27fd1-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="27fd1-105">Un manifiesto de la aplicación Web de un sitio web rige el aspecto y el comportamiento de la aplicación web progresiva \ (PWA \) cuando se instala en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="27fd1-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="27fd1-106">En el nivel más básico, el manifiesto proporciona detalles sobre el nombre de la aplicación, los iconos que se usan para representar la aplicación en los menús del sistema y los colores del tema que usa el sistema operativo \ (SO \) en la barra de título.</span><span class="sxs-lookup"><span data-stu-id="27fd1-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="27fd1-107">El manifiesto también le permite desbloquear características eficaces que permiten que su aplicación se comporte como cualquier otra aplicación nativa del sistema.</span><span class="sxs-lookup"><span data-stu-id="27fd1-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <span data-ttu-id="27fd1-108">Usar métodos abreviados para proporcionar acceso rápido a las características</span><span class="sxs-lookup"><span data-stu-id="27fd1-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="27fd1-109">La mayoría de los sistemas operativos proporcionan acceso rápido a las características clave de la aplicación mediante accesos directos en el menú contextual conectado al icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27fd1-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="27fd1-110">Para usar los métodos abreviados en el PWA, incluya la `shortcuts` propiedad en el manifiesto de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="27fd1-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="27fd1-111">En el siguiente fragmento de código se muestra cómo definir un acceso directo en el manifiesto de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="27fd1-111">The following code snippet shows how to define a shortcut in your web app manifest.</span></span>  

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

<span data-ttu-id="27fd1-112">Cuando se agrega a un manifiesto de aplicación web completo, agregar el fragmento de código anterior permite dos métodos abreviados en el menú contextual en el icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="27fd1-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="27fd1-113">El primero es `Play Later` un nombre y tiene un icono personalizado.</span><span class="sxs-lookup"><span data-stu-id="27fd1-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="27fd1-114">El segundo es `Subscriptions` un nombre y no tiene un icono porque la `icons` propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="27fd1-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="27fd1-115">La `description` propiedad también es opcional y se puede usar para proporcionar información adicional con fines de accesibilidad.</span><span class="sxs-lookup"><span data-stu-id="27fd1-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <span data-ttu-id="27fd1-116">Identificar la aplicación como un destino compartido</span><span class="sxs-lookup"><span data-stu-id="27fd1-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="27fd1-117">Muchos sistemas operativos permiten a los usuarios compartir rápidamente vínculos y archivos con aplicaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="27fd1-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="27fd1-118">Las aplicaciones web progresivas también pueden participar en esta característica a través del `share_target` miembro del manifiesto de la aplicación Web.</span><span class="sxs-lookup"><span data-stu-id="27fd1-118">Progressive Web Apps can participate in this feature as well, via the `share_target` member of the Web App Manifest.</span></span> <span data-ttu-id="27fd1-119">Con share_target, define la página "acción" (similar a un formulario) y los parámetros que espera que se le pasen.</span><span class="sxs-lookup"><span data-stu-id="27fd1-119">Using share_target, you define the "action" page (similar to a form) and the parameters you expect to be passed into it.</span></span> <span data-ttu-id="27fd1-120">El siguiente fragmento de código muestra un ejemplo de uso `share_target` .</span><span class="sxs-lookup"><span data-stu-id="27fd1-120">The following code snippet shows an example of how to use `share_target`.</span></span>

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

<span data-ttu-id="27fd1-121">Cuando se agrega al manifiesto de la aplicación Web, se establece "/share.html" como la página de acciones para un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="27fd1-121">When added to the Web App Manifest, this establishes "/share.html" as the action page for a share.</span></span> <span data-ttu-id="27fd1-122">Además, define tres parámetros que se transferirían a esa página de acción: "title", "Text" y "URL".</span><span class="sxs-lookup"><span data-stu-id="27fd1-122">Additionally, it defines three parameters that would be passed to that action page: "title", "text", and "url".</span></span> <span data-ttu-id="27fd1-123">Estos parámetros se almacenarán en las propiedades "Name", "Descripción" y "link" del objeto [ShareData](https://wicg.github.io/web-share#dom-sharedata) .</span><span class="sxs-lookup"><span data-stu-id="27fd1-123">These parameters will be stored in the [ShareData](https://wicg.github.io/web-share#dom-sharedata) object’s "name", "description", and "link" properties.</span></span> <span data-ttu-id="27fd1-124">De forma predeterminada, la página de acción recibe estos parámetros como parte de una solicitud GET, pero puede especificar la solicitud `method` \ (como `enctype` \), tal como lo haría en un formulario Web.</span><span class="sxs-lookup"><span data-stu-id="27fd1-124">By default, the action page receives these parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <span data-ttu-id="27fd1-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="27fd1-125">See also</span></span>  

<span data-ttu-id="27fd1-126">Para obtener más información sobre los manifiestos de la aplicación Web, consulte la siguiente lista de temas relacionados.</span><span class="sxs-lookup"><span data-stu-id="27fd1-126">To learn more about Web App Manifests, see the following list of related topics.</span></span>  

* [<span data-ttu-id="27fd1-127">Manifiestos de la aplicación Web</span><span class="sxs-lookup"><span data-stu-id="27fd1-127">Web App Manifests</span></span>][MDNWebAppManifests]  
* [<span data-ttu-id="27fd1-128">Destino de recursos compartidos Web</span><span class="sxs-lookup"><span data-stu-id="27fd1-128">Web Share Target</span></span>][WICGShareTarget]
* [<span data-ttu-id="27fd1-129">Compartir web</span><span class="sxs-lookup"><span data-stu-id="27fd1-129">Web Share</span></span>][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Manifiestos de la aplicación Web | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "API de destino de recursos compartidos WICG"
[WICGShare]: https://w3c.github.io/web-share/ "API de uso compartido de Web | WICG"
