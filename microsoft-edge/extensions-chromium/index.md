---
description: Información general sobre la creación y publicación de Microsoft Edge (Chromium) extensiones.
title: Introducción a Microsoft Edge (Chromium) extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, extensions development, browser extensions, addons, partner center, developer, chromium extensions
ms.openlocfilehash: 06a8bcac8690229e44e294fbc68e796ec28ce06fdb76bd030509955bcbda2ea1
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11809323"
---
# <a name="overview-of-microsoft-edge-chromium-extensions"></a>Introducción a Microsoft Edge (Chromium) extensiones  

Una extensión es un pequeño programa que \(un desarrollador\) usa para agregar o modificar características para Microsoft Edge \(Chromium\).  Una extensión está diseñada para mejorar la experiencia de exploración diaria de un usuario.  Proporciona funcionalidad de nicho que es importante para una audiencia de destino.  

Puede crear una extensión si tiene una idea o producto basado en cualquiera de las siguientes condiciones.  

*   Un explorador web específico.  
*   Mejoras en las características de páginas web específicas.  
    
Algunos ejemplos de experiencias complementarias incluyen bloqueadores de anuncios y administradores de contraseñas.  

Una extensión está estructurada de forma similar a una aplicación web normal.  Como mínimo, debe incluir las siguientes características.

*   Un archivo JSON de manifiesto de aplicación que contiene información básica de la plataforma.  
*   Un archivo JavaScript que define la funcionalidad.  
*   Archivos HTML y CSS que definen la interfaz de usuario.  

Para trabajar directamente con una parte del explorador, como una ventana o una pestaña, debe enviar solicitudes de API y, a menudo, hacer referencia al explorador por su nombre.  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Una Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  Una Microsoft Edge \(Chromium\)  
:::image-end:::  

## <a name="basic-guidance"></a>Instrucciones básicas  

Algunos de los exploradores más populares para crear extensiones incluyen Safari, Firefox, Chrome, Opera, Brave y Microsoft Edge.  Excelentes lugares para comenzar los tutoriales de desarrollo de extensiones y la investigación de documentación son sitios hospedados por las organizaciones del explorador.  La tabla siguiente no es definitiva y puede usarse como punto de partida.  

| Navegador web | Chromium basado en Chromium? | Página web de desarrollo de extensiones |  
|:--- |:--- |:--- |  
| Safari | No | [developer.apple.com/documentation/safariservices/safari_app_extensions][AppleDeveloperSafariservicesAppExtensions] |  
| Firefox | No | [developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions][MDNWebextensions] |  
| Chrome | Sí | [developer.chrome.com/extensions][ChromeDeveloperExtensions] |  
| Opera | Sí | [dev.opera.com/extensions][OperaDevExtensions] |  
| Valiente | Sí | Usa [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions] |  
| nueva Microsoft Edge | Sí | [developer.microsoft.com/microsoft-edge/extensions][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> Muchos de los tutoriales de los sitios usan API específicas del explorador que pueden no coincidir con el explorador para el que desarrolla.  En la mayoría de los casos, una extensión Chromium funciona tal como está en diferentes exploradores Chromium y las API funcionan según lo esperado.  Solo algunas API menos comunes pueden ser estrictamente específicas del explorador.  Para obtener vínculos a los tutoriales, vaya [a Ver también](#see-also).  

## <a name="why-chromium"></a>¿Por Chromium?  

Si el objetivo es publicar la extensión en el almacén de extensiones de cada explorador, debe modificarse para que cada versión tenga como destino y se ejecute en cada entorno de explorador distinto.  Por ejemplo, [las extensiones de Safari][AppleDeveloperSafariservicesAppExtensions] pueden usar código web y nativo para comunicarse con aplicaciones nativas equivalentes.  Los últimos cuatro exploradores de la tabla anterior usan el mismo paquete de código y minimizan el requisito de mantener versiones en paralelo.  Estos exploradores se basan en el [Chromium de código abierto][|::ref1::|Home].  

Cree una extensión Chromium para escribir la menor cantidad de código.  También se dirige al número máximo de almacenes de extensiones y, en última instancia, al número máximo de usuarios que encuentran y adquieren la extensión.  

El siguiente contenido se centra principalmente en Chromium extensiones.  

## <a name="browser-compatibility-and-extension-testing"></a>Pruebas de compatibilidad y extensión del explorador  

En ocasiones, la paridad de api no existe entre Chromium exploradores.  Por ejemplo, hay diferencias en las API de identidad y pago.  Para asegurarse de que la extensión cumple las expectativas del cliente, revise el estado de la API a través de los siguientes documentos oficiales del explorador.  

*   [API de Chrome][ChromeDeveloperExtensionsApiIndex]  
*   [API de extensión admitidas en Opera][OperaDevExtensionsApis]  
*   [Extensión de Puerto Chrome a Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome]  
    
Las API que necesita definir los cambios que debe realizar para solucionar las diferencias entre cada explorador.  Puede significar que debes crear paquetes de código ligeramente diferentes con pequeñas diferencias para cada almacén.  

Para probar la extensión en diferentes entornos antes de enviarla a un almacén de exploradores, trascárguela localmente en el explorador mientras la desarrolla.  

## <a name="publish-your-extension-to-browser-stores"></a>Publicar la extensión en almacenes de exploradores  

Puede enviar y buscar extensiones de explorador en los siguientes almacenes de exploradores.  

*   [Complementos del explorador Firefox][MozillaAddonsFirefoxExtensions]  
*   [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]  
*   [Complementos de Opera][OperaAddonsExtensions]  
*   [Complementos de Microsoft Edge][MicrosoftEdgeAddonsCategoryExtensions]  

Algunos almacenes permiten descargar extensiones enumeradas de otros exploradores.  Sin embargo, los almacenes de exploradores no garantizan el acceso entre exploradores.  Para garantizar que los usuarios encuentren la extensión en diferentes exploradores, debe mantener una descripción en cada almacén de extensiones de explorador.  

Es posible que los usuarios necesiten instalar la extensión en diferentes exploradores. En este escenario, puede migrar las extensiones de Chromium existentes de un explorador a otro.  

### <a name="migrate-an-existing-extension-to-microsoft-edge"></a>Migrar una extensión existente a Microsoft Edge  

Si ya ha desarrollado una extensión para otro explorador Chromium, puede enviarla al Microsoft Edge complementos. No es necesario volver a escribir la extensión y comprobar que funciona en Microsoft Edge.  Al migrar una extensión de Chromium existente a otros exploradores Chromium, asegúrese de que las mismas API o alternativas estén disponibles para el explorador de destino.  

Para obtener más información sobre cómo Microsoft Edge la extensión de Chrome a Microsoft Edge, vaya a Extensiones de [Port Chrome Microsoft Edge (Chromium).][ExtensionsChromiumDeveloperGuidePortChrome] Después de portabilidad de la extensión al explorador de destino, el siguiente paso es publicarla.  

### <a name="publish-to-the-microsoft-edge-add-ons-website"></a>Publicar en el sitio Complementos para Microsoft Edge web  

Para empezar a publicar la extensión en Microsoft Edge, debes registrarte para una cuenta de desarrollador con una cuenta de correo electrónico de MSA para enviar la descripción de extensión [a][MicrosoftDeveloperRegistration] la tienda.  Una cuenta de correo electrónico de MSA incluye `@outlook.com` , , y así `@live.com` sucesivamente.  Cuando elija una dirección de correo electrónico para registrarse, considere si debe transferir o compartir la propiedad de la extensión con otros usuarios de su organización.  Una vez completado el registro, puede crear un nuevo envío de extensión a la tienda.  

Para enviar la extensión a la tienda, asegúrese de proporcionar los siguientes elementos.  

*   Un archivo \( `.zip` \) que contiene los archivos de código.  
*   Todos los activos visuales necesarios, que incluyen un logotipo y un pequeño icono promocional.  
*   Medios promocionales opcionales, como capturas de pantalla, iconos promocionales y una dirección URL de vídeo.  
*   Información que describe la extensión, como el nombre, la descripción breve y un vínculo de directiva de privacidad.  

> [!NOTE]
> Los distintos almacenes pueden tener requisitos de envío diferentes.  En la lista anterior se resumen [los requisitos][ExtensionsChromiumPublish] para publicar una extensión para Microsoft Edge.  

Después de enviar correctamente la extensión, la extensión se somete a un proceso de revisión y pasa o falla el proceso de certificación.  A los propietarios se les notifica el resultado y se les dan los pasos siguientes según sea necesario.  Si envía una actualización de extensión al almacén, se inicia un nuevo proceso de revisión.  

## <a name="see-also"></a>Consulte también  

*   [Portabilidad de una extensión de Google Chrome][ExtensionworkshopPorting]  
*   [Crear una extensión de aplicación safari][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [La primera extensión (Firefox)][MDNWebextensionsYourFirst]  
*   [Tutorial de introducción (Chrome)][ChromeDeveloperExtensionsGetstarted]  
*   [Introducción (Opera)][OperaDevExtensionsGettingStarted]  
*   [Introducción a las Microsoft Edge (Chromium)][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Extensión de Chrome de puerto Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Introducción a Microsoft Edge (Chromium) extensiones | Microsoft Docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publicar una extensión | Microsoft Docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Desarrollar extensiones para Microsoft Edge | Microsoft Developer"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Centro de partners | Microsoft Developer"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensiones para Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensiones de aplicación safari | Desarrollador de Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Creación de una extensión de aplicación de Safari | Desarrollador de Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "¿Qué son las extensiones? | Desarrollador de Chrome"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "Api de Chrome | Desarrollador de Chrome"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Introducción al tutorial | Desarrollador de Chrome"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Porte de una extensión de Google Chrome | Taller de extensión"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensiones | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensiones de explorador | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "La primera extensión | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensiones | Complementos para Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensiones | Opera Addons"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentación de extensiones | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API de extensión admitidas en Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Introducción | Dev. Opera"  
