---
description: La descripción general de las extensiones de Microsoft Edge (cromo), así como la creación y publicación de extensiones de explorador en general.
title: Extensiones de Microsoft Edge (cromo)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: Edge, desarrollo de extensiones, extensiones de explorador, addons, centro de Partners, desarrollador, extensiones de cromo
ms.openlocfilehash: 2c4c34805e93bf6fbae57f1d0230cc821d1f3f65
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684702"
---
# Extensiones de Microsoft Edge (cromo)  

Una extensión es un pequeño programa que usted (el desarrollador \) puede usar para agregar nuevas características a Microsoft Edge \ (cromo \) o modificar la funcionalidad existente.  Una extensión está pensada para mejorar la experiencia de exploración diaria de un usuario al proporcionar características de nicho que son importantes para las audiencias de destino.  

Puede crear extensiones si su idea o producto depende de la disponibilidad de un explorador Web específico o aumenta la experiencia de exploración en la que la funcionalidad que desea proporcionar extiende los sitios Web existentes.  Entre los ejemplos de experiencias complementarias se incluyen administradores de adblockers y contraseñas.  

Una extensión está estructurada de forma similar a una aplicación web normal.  Como mínimo, incluye un archivo JSON del manifiesto de la aplicación que contiene información básica de la plataforma, un archivo JavaScript para definir la funcionalidad y un archivo HTML y CSS para determinar el aspecto de la interfaz de usuario \ (como se requiere).  Para trabajar directamente con parte del explorador, como una ventana o una pestaña, debe enviar solicitudes de API y, a menudo, hacer referencia al explorador por nombre.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Extensión de Microsoft Edge (cromo)":::
  Una extensión de Microsoft Edge \ (cromo \)  
:::image-end:::  

## Guía básica  

Algunos de los exploradores más populares para compilar para incluyen Safari, Firefox, Chrome, opera, Brave y Microsoft Edge.  Los excelentes lugares para comenzar los tutoriales de desarrollo de extensiones y la investigación de documentación son sitios alojados en las organizaciones del explorador.  La siguiente tabla no es definitiva; úsela como punto de partida útil.  

| Navegador web | ¿Estás basado en cromo? | Página principal de desarrollo de extensiones |  
|:--- |:--- |:--- |  
| Safari | No | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | No | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrome | Sí | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Sí | [dev.opera.com/extensions][OperaDevExtensions] |  
| Brave | Sí | Usa el [almacén Web de Chrome][GoogleChromeWebstoreCategoryExtensions] |  
| nuevo Microsoft Edge | Sí | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Muchos de los tutoriales de los sitios usan las API específicas del explorador que pueden no coincidir con el explorador para el que está desarrollando.  En la mayoría de los casos, una extensión de cromo funciona tal cual en diferentes exploradores de cromo y las API funcionan de la forma esperada.  Solo algunas API menos comunes pueden ser estrictamente específicas del explorador.  Para obtener vínculos a los tutoriales, vea [Ver también](#see-also).  

## Por qué cromo  

Si su objetivo es publicar su extensión en el mayor número posible de almacenamientos de extensiones del explorador, debe modificarla para varias versiones a fin de que se pueda usar en cada entorno de explorador diferente.  [Las extensiones Safari][AppleDeveloperSafariservicesAppExtensions], a diferencia de otros tipos de extensión, pueden aprovechar el código nativo y web para comunicarse con aplicaciones nativas de homólogo.  [Las extensiones de Firefox][MDNWebextensions] comparten más en común con los otros tipos de extensiones, pero también hay algunas [diferencias][ExtensionworkshopPorting] que se deben tener en cuenta.  Sin embargo, hay buenas noticias; los últimos cuatro exploradores del gráfico anterior pueden aprovechar el mismo paquete de código y minimizar el requisito de alterar y mantener las versiones paralelas.  Esto se debe a que los exploradores se basan en el [proyecto de origen abierto cromo][|::ref1::|Home].  

La creación de una extensión de cromo te permite escribir la cantidad mínima de código para maximizar el número de almacenes de extensiones a los que se destina y, en última instancia, la cantidad de usuarios que pueden encontrar y adquirir la extensión.  

El siguiente contenido se centra principalmente en las extensiones de cromo.  

## Comprobación de extensiones y compatibilidad de exploradores  

Ocasionalmente, la paridad de API no existe entre los exploradores de cromo.  Por ejemplo, existen diferencias en las API de identidad y de pago.  Para asegurarse de que su extensión cumpla con las expectativas del cliente, revise el estado de la API mediante la documentación oficial del explorador, como las [API de Chrome][ChromeDeveloperExtensionsApiIndex], las [API de extensión compatibles con opera][OperaDevExtensionsApis], y la extensión de cromo del [Puerto a Microsoft (cromo)][ExtensionsChromiumDeveloperGuidePortChrome].  

En función de las API que necesite, estas diferencias pueden significar que debe crear paquetes de código ligeramente diferentes con pequeñas diferencias en el código de cada tienda.  

Al desarrollar la extensión, puede transferirla en el explorador para probarla en diferentes entornos antes de enviar su extensión a los almacenes del explorador.  

## Publicar la extensión en tiendas del explorador  

Puede enviar y buscar extensiones del explorador en los siguientes almacenes del explorador.  

*   [Complementos del explorador Firefox][MozillaAddonsFirefoxExtensions]  
*   [Tienda web de Chrome][GoogleChromeWebstoreCategoryExtensions]  
*   [Complementos de ópera][OperaAddonsExtensions]  
*   [Complementos de Microsoft Edge][MicrosoftEdgeAddonsCategoryExtensions]  

Algunas tiendas te permiten descargar las extensiones de la lista de otros navegadores.  La descarga desde desde otro explorador puede guardarte \ (el desarrollador \) está al frente y quitar el requisito de enviarlo a tiendas adicionales si los usuarios pueden navegar a la lista de la tienda existente a través de diferentes exploradores.  Sin embargo, los almacenes del explorador no garantizan el acceso entre navegadores.  Para garantizar que los usuarios puedan encontrar su extensión en exploradores diferentes, debe mantener una lista en cada almacén de extensiones del explorador.  

Una extensión puede tener audiencias superpuestas que usan a menudo varios exploradores, o puede que descubriera que debe dirigirse a una audiencia que no haya antes.  Para que esto suceda, las extensiones de cromo existentes pueden migrarse de un explorador a otro.  

### Migrar una extensión existente a Microsoft Edge  

Si ya ha desarrollado una extensión para otro explorador de cromo y quiere ofrecerla y asegurarse de que funciona a través de Microsoft Edge, no es necesario que vuelva a escribir la extensión.  Migrar las extensiones de cromo existentes a otros exploradores de cromo es muy sencillo, siempre y cuando las API que uses estén disponibles en exploradores diferentes o existen otras API que proporcionan la funcionalidad necesaria.  

Para obtener más información sobre cómo migrar su extensión de cromo, consulte [las extensiones de Chrome para puertos para el borde de Microsoft (cromo)][ExtensionsChromiumDeveloperGuidePortChrome].  Una vez que haya trasladado la extensión al explorador de destino, el siguiente paso es publicarlo.  

### Publicar en el sitio web de complementos de Microsoft Edge  

Para empezar a publicar su extensión a Microsoft Edge, debe [registrarse para obtener una cuenta de desarrollador][MicrosoftDeveloperRegistration] con una cuenta de correo de MSA \ (@outlook. com, @live. com, etc. \) para enviar la lista de extensiones en la tienda.  Cuando elija una dirección de correo electrónico para registrarse, tenga en cuenta si debe transferir o compartir la propiedad de la extensión con otros usuarios de su organización.  Una vez completado el registro, puedes crear un nuevo envío de extensión a la tienda.  

Para enviar su extensión a la tienda, debe cumplir los siguientes requisitos:  

*   Un archivo \ (. zip \) que contiene los archivos de código.  
*   Todos los activos visuales necesarios, que incluyen un logotipo y un pequeño mosaico promocional.  
*   Medios de promoción opcionales, como capturas de pantallas, iconos de promoción más grandes, una dirección URL o cualquier combinación de vídeos de la extensión.  
*   Información que describe su extensión, como el nombre, la descripción breve, la descripción larga y un vínculo a su política de privacidad.  

> [!NOTE]
> Diferentes almacenes pueden tener requisitos de presentación diferentes.  En la lista anterior se resumen los [requisitos][ExtensionsChromiumPublish] para publicar una extensión en Microsoft Edge.  

Después de completar el proceso de envío, se revisa la extensión y se supera o no el proceso de certificación.  A los propietarios se les notifica el resultado y se les proporcionan los siguientes pasos.  Si envía una extensión actualizada a la tienda, incluidas las actualizaciones de los detalles de la lista de extensiones, se iniciará un nuevo proceso de revisión.  

## Consulte también  

*   [Migración de una extensión de Google Chrome][ExtensionworkshopPorting]  
*   [Creación de una extensión de la aplicación Safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [Su primera extensión (Firefox)][MDNWebextensionsYourFirst]  
*   [Tutorial de introducción (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Introducción (Opera)][OperaDevExtensionsGettingStarted]  
*   [Introducción a Microsoft Edge (cromo)][ExtensionsChromiumGettingStartedIndex]  

<!-- image links -->  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Extensión de cromo de puerto para Edge de Microsoft (cromo) | Microsoft docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Introducción a Microsoft Edge (cromo) | Microsoft docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publicar una extensión | Microsoft docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Desarrollar extensiones para Microsoft Edge | Microsoft Developer"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Centro de Partners | Microsoft Developer"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensiones para Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensiones para aplicaciones Safari | Desarrollador de Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Crear una extensión de la aplicación Safari | Desarrollador de Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "¿Qué son las extensiones? | Desarrollador de Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "API de Chrome | Desarrollador de Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Tutorial de introducción | Desarrollador de Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Cromo"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Migración de una extensión Google Chrome | Taller de ampliación"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensiones | Tienda web de Chrome"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensiones de explorador | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "Su primera extensión | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensiones | Complementos para Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensiones | Complementos de ópera"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentación de extensiones | Dev. opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API de extensión compatibles en opera | Dev. opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Introducción | Dev. opera"  
