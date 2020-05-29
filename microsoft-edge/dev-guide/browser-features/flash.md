---
description: Proporciona una experiencia de usuario sin problemas en sitios que requieren Adobe Flash.
title: Guía para desarrolladores de Flash
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, Flash
ms.openlocfilehash: b3e2efe142142b7cdf233acfc4e915cd320b556d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572968"
---
# Flash

Adobe Flash ha sido una parte integral de la web durante décadas, lo que permite realizar animaciones y contenido enriquecido en exploradores antes de que se haya introducido el HTML5. En los exploradores modernos, los estándares web pioneros de Microsoft, Adobe, Google, Apple, Mozilla y muchos otros ahora están permitiendo que los sitios superen esas experiencias sin flash y se ha mejorado el rendimiento y la seguridad. Trabajando en colaboración con otros proveedores de exploradores y con Adobe, recomendamos encarecidamente que los desarrolladores migren a estándares de HTML5, como [extensiones cifradas multimedia](https://developer.microsoft.com/microsoft-edge/platform/status/encryptedmediaextensions), [extensiones de origen multimedia](https://developer.microsoft.com/microsoft-edge/platform/status/mediasourceextensions), [lienzo](https://developer.microsoft.com/microsoft-edge/platform/status/canvas), [audio web](https://developer.microsoft.com/microsoft-edge/platform/status/webaudioapi)y [comunicación en tiempo real](https://developer.microsoft.com/microsoft-edge/platform/status/webrtcobjectrtcapi).

Con la versión de octubre de 2018 de Windows 10, Microsoft Edge continúa el esfuerzo de desuso de Flash que hemos [cubierto](https://blogs.windows.com/msedgedev/2017/07/25/flash-on-windows-timeline/#9mCF959eQEK0poo5.97) como parte del [anuncio de finalización de soporte técnico de Adobe después de](https://theblog.adobe.com/adobe-flash-update/) 2021. En la versión Oct 2018, los usuarios deberán permitir que Flash se ejecute de forma explícita en un sitio durante el período de duración de la ficha. La opción siempre permitir persistentes ya no estará disponible y un usuario no podrá administrar el permiso de Flash por sitio que abarca las sesiones de la pestaña.

A medida que pases por los estándares de HTML5, hay algunas cosas sencillas que puedes hacer para asegurarte de que los usuarios tengan una experiencia positiva en tu sitio web con Microsoft Edge en Windows 10 Creators Update. 

Si se usa Flash en la página, pero el usuario no lo ha habilitado, Microsoft Edge normalmente mostrará un icono de pieza de Puzzle en la barra de direcciones, tal y como se muestra en [este blog](https://blogs.windows.com/msedgedev/2016/12/14/edge-flash-click-run/#41svu6EMwKIAaigx.97). Si va a agregar dinámicamente el control de flash después de cargar la página, es posible que no se muestre este icono de pieza de Puzzle, en este caso es mejor comprobar la presencia de Flash y proporcionar un vínculo como se describe a continuación.

Para asegurarse de que todos los usuarios tengan una buena experiencia, siga probando la presencia de Flash con los mecanismos estándar. Si Microsoft Edge informa que Flash no está disponible, presenta el [vínculo de descarga flash](http://get.adobe.com/flashplayer) y la [imagen de descarga flash](http://www.adobe.com/legal/permissions/icons-web-logos.html#flashplayer) al usuario. Cuando el usuario hace clic en el vínculo, Microsoft Edge (así como otros exploradores) presentará los avisos necesarios para habilitar Flash Player para el sitio. El vínculo debe aparecer en el dominio principal en el que desea habilitar el flash. No funcionará si redirige a los usuarios a las páginas de otros dominios.  [Esta es una demostración](https://microsoftedge.github.io/MicrosoftEdge-Documentation/flashclicktorun/) de la experiencia sugerida y el [código de ejemplo](https://github.com/MicrosoftEdge/MicrosoftEdge-Documentation/tree/master/docs/flashclicktorun)correspondiente.
