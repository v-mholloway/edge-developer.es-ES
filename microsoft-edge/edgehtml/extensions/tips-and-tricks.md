---
description: Más información sobre algunas sugerencias y trucos prácticos relacionados con las extensiones de Microsoft Edge
title: Sugerencias y trucos | Prórroga
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd512085f13b76c5a8e474301ef296612eeb0414
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236124"
---
# Sugerencias y trucos  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

Si está trabajando en una extensión de Microsoft Edge o ya ha publicado una, es posible que las siguientes sugerencias y trucos sean útiles.

## Obtener un vínculo directo a su extensión en Microsoft Store

En el panel del centro de desarrollo de Windows, puede encontrar un vínculo directo a su extensión en Microsoft Store. Este vínculo puede ser útil para anunciar y compartir tu extensión.

Después de iniciar sesión en el centro de desarrollo de Windows y navegar hasta la extensión a través del panel, en la página identidad de la aplicación encontrará el vínculo en la fila **vínculo de protocolo del almacén** :

![vínculo de protocolo de tienda](./media/store-link.png)
 
## Asegúrese de estar siguiendo la Directiva de Microsoft Store

Al crear la extensión, asegúrese de tener en cuenta las pautas para enviar a Microsoft Store resaltadas en la [Directiva Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx). 
 
Las extensiones de Microsoft Edge también tienen un conjunto adicional de directivas que puede seguir [aquí](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).

## Mejorar la detección de extensiones en Microsoft Store

Puede agregar palabras clave a su envío de extensión para mejorar su descubrimiento a través de las búsquedas. Por ejemplo, "extensiones de Microsoft Edge" y "nombre de mi extensión". 

Esto puede hacerse en el centro de desarrollo de Windows, debajo de la sección de descripción de su extensión. Estas palabras clave deberán agregarse para cada idioma que admita la extensión.

![Enviar una respuesta a una revisión: Palabras clave](./media/keywords.png)

## Automatizar el envío a Microsoft Store

Puede automatizar y simplificar los envíos a Microsoft Store mediante la nueva API de envío de Microsoft Store, que le permite actualizar aplicaciones/juegos, complementos (compras desde la aplicación) y paquetes piloto a través de una API de REST. Consulte la [documentación y las muestras](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) o use la extensión Open Source [Transmission API VSTS](https://github.com/Microsoft/windows-dev-center-vsts-extension) para comenzar.

## Usar el centro de opiniones de Windows para recopilar comentarios/críticas/solicitudes de características

Puede dirigir a los usuarios a la subcategoría concentrador de comentarios de Windows para su extensión incrustando un vínculo que apunte a él. Este vínculo tendrá que crearse con el siguiente formato: 

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

Deberás sustituirlo `<PFN>` por el nombre de familia de paquetes de la extensión. Puedes encontrarla en la sección identidad de la **aplicación** para tu extensión en el centro de desarrollo de Windows.

## Consulta tus calificaciones y opiniones

Inicie sesión regularmente para comprobar las revisiones y las calificaciones de los usuarios. Si bien la aplicación para UWP solo tendrá información sobre el mercado del usuario actual, al iniciar sesión en el centro de desarrollo de Windows se mostrará la calificación promedio en todos los mercados.

## Responder a las opiniones de los usuarios

Puede responder a las opiniones de los usuarios en Microsoft Store a través del panel del centro de desarrollo de Windows. Vaya a la extensión y, en Analytics, seleccione **Recomentarioss**. Debajo de cada opinión, aparecerá un vínculo que le permitirá responder directamente al cliente. Este canal de comunicación le permite ofrecer comentarios, soluciones o enviar una agradecimiento por la revisión.

![Enviar una respuesta a una opinión](./media/reviews.png)
