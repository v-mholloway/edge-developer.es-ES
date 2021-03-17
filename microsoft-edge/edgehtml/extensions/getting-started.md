---
description: Obtenga información general de un extremo a otro del recorrido desde el inicio del desarrollo hasta el empaquetado de extensiones de Microsoft Edge.
title: 'Extensiones: introducción'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, extensions
ms.date: 03/16/2021
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 52d0aa5c1968518194a4e3b90cb0cc876d0c7f86
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439720"
---
# <a name="getting-started-with-extensions"></a>Introducción a las extensiones  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Ya seas un desarrollador nuevo que quiera familiarizarte con las extensiones o un veterano experimentado con una extensión de Chrome que quieras portabilidad, esta guía contiene toda la información que necesitas para desarrollar, probar, empaquetar y publicar una extensión para Microsoft Edge. 

## <a name="developing-an-extension"></a>Desarrollo de una extensión

El primer paso de este recorrido es crear una extensión de Microsoft Edge: 
- ¿Es nuevo en las extensiones? Consulte nuestra [guía sobre cómo crear extensiones para](./guides/creating-an-extension.md) obtener información sobre cómo crear la primera extensión del explorador. 
- ¿Ya está familiarizado con las API de extensión? Consulte nuestra [documentación de soporte técnico de api](./api-support.md) para obtener la información más reciente sobre qué API son compatibles o en desarrollo. 
- ¿Tiene una extensión de Chrome que desea portabilidad a Microsoft Edge? Pruebe el Kit [de herramientas de extensión de Microsoft Edge](./guides/porting-chrome-extensions.md)!

## <a name="loading-and-debugging"></a>Carga y depuración

Una vez que tenga una extensión que funcione en Microsoft Edge, querrá cargarla de forma lateral para verla en acción. El primer paso para hacerlo es asegurarse de que tiene habilitadas las características de [desarrollador de extensión](./guides/adding-and-removing-extensions.md). Esto te permitirá cargar archivos de extensión de lado en Microsoft Edge para que puedas probar la extensión mientras la desarrollas. Si se encuentra con algún problema, las herramientas para desarrolladores de F12 le permiten depurar los [distintos contextos](./guides/debugging-extensions.md) de la extensión para determinar exactamente lo que está sucediendo. ¿Sigues teniendo problemas? Nuestra [guía de solución de problemas](./troubleshooting.md) tiene soluciones para varias gotchas comunes. 

## <a name="reporting-bugs-and-getting-help"></a>Informar de errores y obtener ayuda

¿Crees que has encontrado un error en nuestra plataforma de extensiones? Si el problema es específico de Microsoft Edge, buscalo en nuestro Rastreador de problemas de [Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/issues/) para ver si ya se ha notificado. Si lo ha hecho, ¡genial! Puedes presionar el botón "+ Yo también" para invocar el error y el botón "Ver este problema para actualizaciones" para recibir una alerta sobre cualquier cambio en el problema. Si no encuentra el problema en el que se encuentra, no dude en abrir un nuevo problema y proporcionar tanta información como sea posible para que nuestros desarrolladores puedan buscarlo. 

<!--Are we missing an API that your extension needs to work properly? If so, [we're always listening on UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions). Feel free to upvote your API if it already exists, or to create a new feedback item so that other developers can upvote it too! -->  

¿Tiene una pregunta a la que no puede encontrar una respuesta en la documentación? Te recomendamos encarecidamente que te unas a la comunidad de extensiones de [Microsoft Edge](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) en Stack Overflow y pregúntele allí.

## <a name="testing-your-extension"></a>Probar la extensión

Desde Windows Anniversary Update, [Microsoft WebDriver](../webdriver/index.md) admite la carga lateral automatizada de extensiones en sesiones de Microsoft Edge. Esto le permitirá escribir pruebas sencillas para asegurarse de que cualquier extensión destinada a modificar una página lo haga de la manera esperada. Puedes encontrar más información sobre cómo hacerlo en nuestra guía [de pruebas.](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver) Además, mantente atento a las actualizaciones mientras planeamos agregar más características específicas de extensión a Microsoft WebDriver en el futuro.

## <a name="adding-the-final-touches"></a>Agregar los toques finales

Por lo tanto, la extensión funciona en Microsoft Edge. ¿Qué sucede a continuación? Antes de continuar empaquetando la extensión, le recomendamos encarecidamente que consulte estas guías para asegurarse de que la extensión siga nuestras directivas de procedimiento recomendado: 
- Asegúrate de que [](./guides/design.md) los iconos de extensión tienen el tamaño y el acceso [correctos](./guides/accessibility.md) (lo que significa que están visibles en los temas claros y oscuros de Microsoft Edge, así como en el modo de contraste alto). 
- Si la extensión necesita admitir varios idiomas, asegúrese de que ha hecho un vistazo a nuestra guía [de internacionalización](./guides/internationalization.md). 

## <a name="packaging-an-extension"></a>Empaquetar una extensión

Ahora, la extensión finalmente se pule y está lista para empaquetarse. Tanto si quieres empaquetar para preparar el envío a Microsoft Store como para facilitar la distribución en los equipos de desarrollo y pruebas, hay muchos recursos disponibles para ayudarte: 

- Nuestra solución recomendada para crear un paquete de extensión es seguir nuestra guía de empaquetado [manifoldJS](./guides/packaging/using-manifoldjs-to-package-extensions.md) que le guiará a través de los pasos del uso de una herramienta basada en Node.js para empaquetar fácilmente la extensión independientemente de la plataforma en la que desarrolle. Si desea obtener una mirada más detallada y manual a nuestro formato de empaquetado de extensiones, consulte nuestra guía de creación [de paquetes AppX](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder). 
- Si la extensión admite varios idiomas, también tendrás [](./guides/packaging/localizing-extension-packages.md) que seguir nuestra guía sobre la localización de paquetes de extensión para que los idiomas que tienes en la extensión se registren correctamente después del empaquetado. 

Si es un cliente de empresa que busca distribuir las extensiones [](./extensions-for-enterprise.md) empaquetadas a través de canales internos, consulte nuestra guía de extensiones para empresas para ver cómo hacerlo.  

## <a name="publishing-to-the-microsoft-store"></a>Publicación en Microsoft Store

Dado que nuestra plataforma de extensiones aún está en sus inicios, estamos administrando específicamente envíos de extensiones a Microsoft Store para que podamos centrarnos en ofrecer una experiencia de calidad para nuestros usuarios y desarrolladores. Dicho esto, queremos que sea lo más fácil posible que los desarrolladores publiquen sus extensiones. Como resultado, hemos iniciado recientemente [](https://aka.ms/extension-request) un nuevo formulario de envío de extensión donde los desarrolladores pueden solicitar permiso para enviar su extensión AppX a Microsoft Store.
 
El primer paso del proceso de publicación es asegurarse **** de que la extensión se ajusta a nuestra directiva de extensión del explorador, así como a la sección extensiones de Microsoft Edge de las directivas [de Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).  

<!--  The first step of the publishing process is to make sure your extension conforms to our [browser extension policy](./microsoft-browser-extension-policy.md) as well as the [Microsoft Edge extensions section of the Microsoft Store Policies](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).  -->  

Una vez que hayas confirmado que la extensión sigue las directivas, deberás registrarte para una cuenta de desarrollador en el Centro de partners y reservar el nombre [de la extensión](./guides/packaging/extensions-in-the-windows-dev-center.md). A continuación, tendrás que enviar [](https://aka.ms/extension-request) una solicitud a través de nuestro formulario de envío de extensión para solicitar permiso para publicar en Microsoft Store. Si intenta enviar la extensión AppX sin obtener primero permiso, recibirá el siguiente error:

```text
Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.
```  

Una vez que haya enviado una solicitud, recibiremos una notificación e intentaremos llegar a su envío tan pronto como sea posible. Esto puede tardar un poco debido al gran volumen de envíos que hemos recibido, pero le notificaremos por correo electrónico en el momento en que se apruebe. Una vez que hayas recibido el correo, podrás enviar la extensión AppX a Microsoft Store a través del Centro de partners. Ten en cuenta que no tienes que firmar tu AppX antes de enviarlo; el proceso de ingesta de Microsoft Store se ocupará de eso por ti.
 
> [!NOTE]
> El proceso para publicar una extensión en Microsoft Store (ya sea una extensión nueva o una actualización de una existente) puede tardar hasta 72 horas en completarse. Para acelerar este proceso, asegúrese de que ha comprobado estos gotchas comunes antes de enviarlos para evitar tener que volver a enviar más tarde: 
> - Las capturas de pantalla tienen el tamaño correcto y son de la extensión que se ejecuta en Microsoft Edge 
> - La descripción de la extensión hace referencia a "Microsoft Edge" en lugar de "Edge" (este es un requisito legal) 
> - El icono de 150 x 150 del paquete de extensión no tiene un fondo transparente [(el](./guides/design.md#microsoft-store-icon) cliente de Microsoft Store no representa correctamente imágenes con fondos transparentes) 

Además de lo anterior y, si procede, asegúrese de que cualquier información de disponibilidad de la plataforma en su sitio web mencione correctamente la disponibilidad de la extensión en Microsoft Edge. Aunque la Microsoft Store no permite instalar extensiones en línea con un solo clic, puedes vincularla profundamente a la extensión en [la Microsoft Store](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) para facilitar que los usuarios puedan adquirirla. 

La Microsoft Store también te permite [controlar la visibilidad de tu extensión en](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) el catálogo de Microsoft Store. Algunos de nuestros partners han aprovechado esta funcionalidad para lograr lo siguiente: 
- Publicar una segunda versión beta de su extensión como oculta en Microsoft Store.
- Inicialmente publicar su extensión como oculta para supervisar la telemetría inicial antes de cambiar finalmente su estado a visible una vez que se alcanza un cierto nivel de confianza.

## <a name="thats-it"></a>Eso es todo.

Si has llegado a la parte inferior de esta guía, has completado el proceso de desarrollo de una extensión para Microsoft Edge. Asegúrate de consultar nuestra página de [sugerencias y](./tips-and-tricks.md) trucos para obtener ideas sobre cómo comercializar tu extensión e interactuar con los usuarios.
