---
description: Obtenga información sobre algunas sugerencias y trucos prácticos con respecto a las extensiones de Microsoft Edge
title: Sugerencias y trucos | Extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, extensions
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a5ea19152f5524d86d17d6f978c677c45f8f3a8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399354"
---
# <a name="tips-and-tricks"></a>Sugerencias y trucos  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Tanto si está trabajando actualmente en una extensión de Microsoft Edge como si ya ha publicado una, las siguientes sugerencias y trucos pueden ser útiles.  

## <a name="get-a-direct-link-to-your-extension-in-the-microsoft-store"></a>Obtener un vínculo directo a la extensión en Microsoft Store  

En el panel del Centro de desarrollo de Windows, puedes encontrar un vínculo directo a tu extensión en Microsoft Store.  Este vínculo puede ser útil para la publicidad y el uso compartido de la extensión.  

Después de iniciar sesión en el Centro de desarrollo de Windows y navegar a la extensión a través del panel, en la página Identidad de la aplicación encontrarás el vínculo en la fila vínculo Protocolo de **la** Tienda:  

![vínculo de protocolo de almacenamiento](./media/store-link.png)  
 
## <a name="make-sure-youre-following-the-microsoft-store-policy"></a>Asegúrate de seguir la directiva de Microsoft Store  

Al crear la extensión, asegúrate de tener en cuenta las directrices para enviar a la Microsoft Store resaltadas en la [Directiva de Microsoft Store](/windows/uwp/publish/store-policies).  
 
Las extensiones de Microsoft Edge también tienen un conjunto adicional de directivas que se pueden [seguir](/windows/uwp/publish/store-policies#pol_10_12)aquí.  

## <a name="improve-your-extensions-discoverability-in-the-microsoft-store"></a>Mejorar la capacidad de destisibilidad de la extensión en Microsoft Store  

Puede agregar palabras clave al envío de extensión para mejorar su capacidad de destecciones a través de búsquedas.  Por ejemplo, `Microsoft Edge Extensions` y `name of my extension` .  

Esto se puede hacer en el Centro de desarrollo de Windows en la sección descripción de la extensión.  Estas palabras clave tendrán que agregarse para todos los idiomas que admita la extensión.  

![Usar palabras clave para enviar una respuesta a una revisión](./media/keywords.png)  

## <a name="automate-your-submission-to-the-microsoft-store"></a>Automatizar el envío a Microsoft Store  

Puedes automatizar y simplificar los envíos a Microsoft Store mediante la nueva API de envío de Microsoft Store, que te permite actualizar aplicaciones/juegos, complementos \(compras desde la aplicación\) y paquetes de paquetes a través de una API de REST.  Consulte la documentación [y los ejemplos o](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) use la extensión [VSTS](https://github.com/Microsoft/windows-dev-center-vsts-extension) de la API de envío de código abierto para empezar.  

## <a name="use-the-windows-feedback-hub-to-gather-feedbackreviewsfeature-requests"></a>Usar el Centro de opiniones de Windows para recopilar comentarios, opiniones y solicitudes de características  

Puedes dirigir a los usuarios a la subcategoría Centro de opiniones de Windows para la extensión insertando un vínculo que apunta a ella.  Este vínculo tendrá que crearse con el siguiente formato:  

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

Tendrá que sustituir por `<PFN>` el nombre de familia del paquete de su extensión.  Esto se puede encontrar en la **sección Identidad de** la aplicación para tu extensión en el Centro de desarrollo de Windows.  

## <a name="check-out-your-ratings-and-reviews"></a>Echa un vistazo a tus clasificaciones y opiniones  

Inicie sesión con regularidad para comprobar las opiniones y clasificaciones de los usuarios.  Aunque la aplicación para UWP solo tendrá información sobre el mercado de usuarios actual, al iniciar sesión en el Centro de desarrollo de Windows se mostrará una clasificación promedio en todos los mercados.  

## <a name="respond-to-user-reviews"></a>Responder a las opiniones de los usuarios  

Puedes responder a las opiniones de los usuarios en la Microsoft Store a través del panel del Centro de desarrollo de Windows.  Vaya a la extensión y, en Análisis, seleccione **Revisiones**.  Debajo de cada revisión aparecerá un vínculo que le permitirá responder directamente al cliente.  Este canal de comunicación le permite ofrecer comentarios, resoluciones o enviar un agradecimiento por la revisión.  

![Responder a la revisión del usuario](./media/reviews.png)  
