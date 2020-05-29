---
description: Obtén un resumen de la visión general del camino desde el principio del desarrollo hasta el empaquetado de las extensiones de Microsoft Edge.
title: Extensiones-introducción
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.openlocfilehash: 5d2bf0ea2236e36b9e6205e13291ffee4118d9d7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573651"
---
# Introducción a las extensiones  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Tanto si es un nuevo desarrollador que desea familiarizarse con las extensiones como si es un veterano experto con una extensión Chrome que le gustaría trasladar, esta guía contiene toda la información que necesita para desarrollar, probar, empaquetar y publicar una extensión para Microsoft Edge. 

## Desarrollar una extensión

El primer paso de este viaje es crear una extensión de Microsoft Edge: 
- ¿Es nuevo en las extensiones? Consulta nuestra [Guía sobre cómo crear extensiones](./guides/creating-an-extension.md) para obtener más información sobre cómo crear tu primera extensión de explorador. 
- ¿Ya estás familiarizado con las API de extensión? Consulte nuestra [documentación de soporte de API](./api-support.md) para obtener la información más reciente sobre las API que se admiten/en desarrollo. 
- ¿Tienes una extensión Chrome que deseas trasladar a Microsoft Edge? Prueba el [Kit de herramientas de Microsoft Edge Extension](./guides/porting-chrome-extensions.md).

## Carga y depuración

Una vez que tenga una extensión que funcione en Microsoft Edge, querrá cargarla para verla en acción. El primer paso para hacerlo es asegurarse de tener [habilitadas las características para desarrolladores de extensiones](./guides/adding-and-removing-extensions.md). Esto le permitirá cargar archivos de extensión en Microsoft Edge para poder probar la extensión mientras la desarrolla. Si tiene algún problema, las herramientas de desarrollo F12 le permiten [depurar los distintos contextos de la extensión](./guides/debugging-extensions.md) para determinar exactamente lo que ocurre. ¿Aún está teniendo problemas? Nuestra [Guía de solución de problemas](./troubleshooting.md) tiene soluciones a varias trampas comunes. 

## Notificar errores y obtener ayuda

¿Crees que has encontrado un error en nuestra plataforma de extensiones? Si el problema es específico de Microsoft Edge, búscalo en nuestro [Microsoft Edge Issue Tracker](https://developer.microsoft.com/microsoft-edge/platform/issues/) para ver si ya se ha notificado. Si es así, ¡ genial! Puedes pulsar el botón "me me gustaría" para votar sobre el error y el botón "ver este problema de actualizaciones" para recibir una alerta de cualquier cambio en el problema. Si no encuentra el problema que está ejecutando, no dude en abrir un nuevo problema y proporcionar la mayor cantidad de información posible para que nuestros programadores puedan encontrarla. 

¿Falta una API que su extensión necesite que funcione correctamente? Si es así, [siempre estamos escuchando en UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/87962-extensions). No dudes en votar en tu API si ya existe, o en crear un nuevo elemento de comentarios para que otros desarrolladores también puedan votar. 

¿Tiene alguna pregunta en la que no encuentre una respuesta en la documentación? Le recomendamos encarecidamente que se una a la [comunidad de las extensiones de Microsoft Edge](https://stackoverflow.com/questions/tagged/microsoft-edge-extension) sobre el desbordamiento de pila.

## Probar la extensión

A partir de la actualización de aniversario de Windows, [Microsoft Webdriver](../dev-guide/tools/webdriver.md) admite la carga automatizada de extensiones en sesiones de Microsoft Edge. Esto le permitirá escribir pruebas sencillas para asegurarse de que todas las extensiones que se destinan a modificar una página lo hagan de la manera esperada. Puede encontrar más información sobre cómo hacerlo en nuestra [Guía de pruebas](./guides/packaging/creating-and-testing-extension-packages.md#automated-testing-with-webdriver). Además, Manténgase atento a las actualizaciones mientras planeamos agregar más características específicas de extensión a Microsoft WebDrive en el futuro.

## Agregar los toques finales

Para que tu extensión funcione en Microsoft Edge. ¿Qué ocurre a continuación? Antes de continuar empaquetando su extensión, le recomendamos encarecidamente que consulte estas guías para asegurarse de que su extensión siga nuestras políticas de mejores prácticas: 
- Asegúrese de que los iconos de extensión sean [correctos](./guides/design.md) y sean [accesibles](./guides/accessibility.md) (es decir, que sean visibles tanto en los temas claros como oscuros de Microsoft Edge, así como en el modo contraste alto). 
- Si tu extensión debe admitir varios idiomas, asegúrate de haber sacado un vistazo a nuestra guía de [internacionalización](./guides/internationalization.md). 

## Empaquetar una extensión

Ahora tu extensión se ha acabado y está lista para ser embalada. Si desea empaquetarlo para prepararse para el envío a Microsoft Store o para que sea más fácil de distribuir dentro de los equipos de desarrollo/pruebas, hay muchos recursos disponibles para ayudarle: 

- Nuestra solución recomendada para crear un paquete de extensión es seguir nuestra [Guía de empaquetado de ManifoldJS](./guides/packaging/using-manifoldjs-to-package-extensions.md) que te guiará a través de los pasos de la herramienta basada en node. js para empaquetar fácilmente tu extensión, independientemente de la plataforma en la que desarrolles. Si desea un aspecto más manual y exhaustivo de nuestro formato de empaquetado de extensiones, consulte nuestra [Guía de creación de paquetes de appx](./guides/packaging/creating-and-testing-extension-packages.md#preparing-the-submission-folder). 
- Si su extensión es compatible con varios idiomas, también tendrá que seguir nuestra guía sobre la [localización de paquetes de extensión](./guides/packaging/localizing-extension-packages.md) para que los idiomas que tiene en su extensión se registren correctamente después del embalaje. 

Si es un cliente empresarial y quiere distribuir sus extensiones empaquetadas a través de canales internos, consulte nuestra [Guía de extensiones para empresas](./extensions-for-enterprise.md) para ver cómo hacerlo.  

## Publicar en Microsoft Store

Debido a que nuestra plataforma de extensiones aún está en sus incaracterísticas, hacemos para administrar los envíos de extensiones a Microsoft Store de modo que podamos centrarnos en ofrecer una experiencia de calidad para nuestros usuarios y programadores. Como se dice, queremos que sea lo más fácil posible para los desarrolladores publicar sus extensiones. Como resultado, recientemente hemos iniciado un nuevo formulario de [envío de extensión](https://aka.ms/extension-request) en el que los desarrolladores pueden solicitar permiso para enviar su appx de extensión a Microsoft Store.
 

El primer paso del proceso de publicación es asegurarse de que la extensión se ajuste a nuestra [Directiva de extensión del explorador](./microsoft-browser-extension-policy.md) , así como a la [sección de las extensiones de Microsoft Edge de las directivas de Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12). 

Una vez que haya confirmado que su extensión sigue las directivas, tendrá que registrarse para obtener una [cuenta de Desarrollador en el centro de Partners y reservar el nombre de la extensión](./guides/packaging/extensions-in-the-windows-dev-center.md). A continuación, deberá enviar una solicitud a través de nuestro [formulario de envío de extensiones](https://aka.ms/extension-request) para solicitar permiso para publicar en Microsoft Store. Si intentas enviar tu AppX de extensión sin obtener primero el permiso, recibirás el siguiente error:

`Package acceptance validation error: com.microsoft.edge.extension is a reserved extension type. Your app does not have permission to use this extension type.`

Una vez que hayas enviado una solicitud, recibiremos una notificación y te intentaremos llegar a tu envío tan pronto como sea posible. Esto puede demorar un poco por el gran volumen de entregas que hemos recibido, pero le enviaremos un mensaje por correo electrónico en el momento en que se le apruebe. Una vez que hayas recibido el mensaje de correo electrónico, podrás enviar tu AppX de extensión a la tienda de Microsoft a través del centro de Partners. Ten en cuenta que no es necesario que firmes tu AppX antes de enviarlo; el proceso de recopilación de Microsoft Store se encargará de hacerlo.
 
> [!NOTE]
> El proceso de publicación de una extensión en Microsoft Store (ya sea una extensión completamente nueva o una actualización a una existente) puede tardar hasta 72 horas en completarse. Para agilizar este proceso, asegúrese de haber verificado estas trampas comunes antes de enviarlas para evitar tener que volver a enviar más tarde: 
> - Las capturas de pantallas tienen el tamaño correcto y se ejecutan en Microsoft Edge 
> - La descripción de la extensión hace referencia a "Microsoft Edge" en lugar de "Edge" (este es un requisito legal). 
> - El icono de 150x150 en el paquete de extensión no [tiene un fondo transparente](./guides/design.md#microsoft-store-icon) (el cliente de Microsoft Store no representa correctamente imágenes con fondos transparentes) 

Además de lo anterior, y si corresponde, asegúrese de que la información de disponibilidad de la plataforma de su sitio web mencione correctamente la disponibilidad de su extensión en Microsoft Edge. Aunque Microsoft Store no permite instalaciones de extensión en línea con un solo clic, puede [vincular en profundidad con su extensión en Microsoft Store](./tips-and-tricks.md#get-a-direct-link-to-your-extension-in-the-microsoft-store) para que los usuarios puedan adquirirla fácilmente. 

Microsoft Store también le permite [controlar la visibilidad de su extensión](https://blogs.windows.com/buildingapps/2015/09/10/managing-hidden-apps-beta-apps-and-visibility-of-in-app-purchases-in-dev-center/) en el catálogo de Microsoft Store. Algunos de nuestros socios han sacado provecho de esta funcionalidad para lograr lo siguiente: 
- Publicar una segunda versión beta de su extensión como oculta en Microsoft Store.
- Inicialmente, publicar su extensión como oculta para supervisar la telemetría inicial antes de cambiar su estado a visible una vez que se alcanza un cierto nivel de confianza.

## Eso es todo.

Si has llegado al final de esta guía, has completado el proceso de desarrollo de una extensión para Microsoft Edge. Asegúrese de consultar nuestra página de [sugerencias y trucos](./tips-and-tricks.md) para obtener ideas sobre cómo promocionar su extensión e interactuar con sus usuarios.
