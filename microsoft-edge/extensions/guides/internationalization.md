---
description: Haga que su extensión sea accesible para diferentes idiomas y pruebe las cadenas de idioma con la guía de internacionalización.
title: Extensiones-internacionalización
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: d1f553d0e3e39192e68665fe6720daa811777c0b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573601"
---
# Internacionalización  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Para que la extensión sea accesible para una variedad de personas distintas, es importante que se desarrolle con otros países en mente. Las extensiones de Microsoft Edge le permiten agregar diferentes cadenas de idioma a las extensiones para que su idioma pueda cambiarse fácilmente.

Para obtener más información sobre cómo internacionalizar su extensión, consulte la [Guía de internacionalización](https://developer.mozilla.org/Add-ons/WebExtensions/Internationalization)de MDN.


## Probar idiomas

Para probar las cadenas de idioma, primero debe establecer el idioma de Windows en el idioma que quiera probar.

Siga los pasos que se indican a continuación para cambiar el idioma de Windows:

1. Abra la aplicación configuración.

   ![aplicación de configuración](./../media/loc-settings.png)
2. Selecciona "tiempo & idioma".
3. Selecciona "idioma & región".
4. Seleccione "+ agregar un idioma" para agregar el idioma a la lista de idiomas posibles.
5. Elija el idioma de la lista "idiomas" que desea probar.
6. Selecciona el botón "establecer como predeterminado" (es posible que tengas que reiniciar el equipo).
7. Abra Microsoft Edge y compruebe que las cadenas definidas para la configuración regional aparecen de la forma esperada.

Al usar la propiedad [NavigatorLanguage. Language](https://developer.mozilla.org/docs/Web/API/NavigatorLanguage/language) , puede comprobar que el idioma que Microsoft Edge ha determinado como el idioma de Windows es correcto.

Haz clic en el botón de la CodePen siguiente para ver el idioma de visualización de tu explorador.

<iframe height='300' scrolling='no' title='Obtener configuración regional' src='//codepen.io/MSEdgeDev/embed/VaRWwR/?height=300&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulta la pluma <a href='https://codepen.io/MSEdgeDev/pen/VaRWwR/'> para obtener la configuración regional </a> de MSEdgeDev ( <a href='http://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) en <a href='http://codepen.io'> CodePen </a> .
</iframe>
