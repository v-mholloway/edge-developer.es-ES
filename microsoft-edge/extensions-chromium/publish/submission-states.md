---
description: Obtenga información sobre los diferentes estados al enviar extensiones a la tienda
title: Estados de envío para extensiones en la tienda
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: fee28cf377582e670080f489c442a7c7130aa7448c122d206e47605104219fbb
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11807951"
---
# <a name="submission-states-for-extensions-in-the-microsoft-edge-add-ons-store"></a>Estados de envío para extensiones en el Microsoft Edge complementos  

La página de información general del Centro de partners muestra el estado de la extensión en el flujo de envío general.  En este artículo se describen los diferentes estados en los que puede estar la extensión en cualquier momento durante el proceso de envío y certificación.  

| # |  Estado |  Detalles |  
|:--- |:--- |:--- |  
| 1 |  En borrador |  Creas el envío y guardas un borrador en tu cuenta.  No ha enviado el paquete de extensión ni los detalles del formulario de envío para publicarlos en el Microsoft Edge complementos.  La extensión no está disponible para los usuarios en este estado.  |  
| 2|  En revisión |  Ha enviado la extensión.  Microsoft revisa el paquete de extensión y los detalles del formulario de envío.  La extensión no está disponible para los usuarios en este estado.  |  
| 3|  A la espera de publicar |  El envío se encuentra en este estado una vez completada la revisión de extensión y la extensión se está preparando para su publicación en el Microsoft Store.  Este estado es un estado intermedio entre `In review` y `In the store` .  Es posible que este estado no aparezca para todos los envíos.  |  
| 4|  En la tienda |  La revisión ya está completa y la extensión se publica en el Microsoft Edge complementos.  La extensión está disponible en el Microsoft Store en los mercados que especificó.  |  
| 5 |  En la tienda.  Actualizar en revisión |  La extensión se publica en el almacén Microsoft Edge complementos y ha enviado una actualización que Microsoft está revisando.  |  
| 6 |  Error en la revisión |  El envío está en este estado si la extensión no realiza una revisión.  Puede producirse un error de revisión durante la revisión inicial o durante una actualización.  Debe tomar medidas correctivas y volver a enviar la extensión.  |  
| 7 |  No disponible en la tienda |  Hay tres escenarios posibles cuando la extensión muestra este estado:  **Unpublished from store**, **Removed from store**y **Blocked**.  La descripción de cada uno de los tres estados se especifica en 8, 9 y 10.  |  
| 8 |  Unpublished from store |  Ha deseditado la extensión del almacén Microsoft Edge complementos en el Centro de partners.  En el Centro de partners, eligió **anular la publicación** en la página de envío de extensión.  Después de anular la publicación de la extensión, ya no está disponible en el almacén de complementos de Microsoft Edge para que los nuevos usuarios puedan descargar, pero los usuarios existentes pueden seguir usando sus copias de la extensión.  |  
| 9 |  Eliminado de la tienda |  Si se encuentra que la extensión infringe los términos y condiciones del almacén de complementos de Microsoft Edge, Microsoft puede quitarla del almacén de complementos perimetrales y el estado cambia a este estado.  <br />  Después de eliminar la extensión por parte de Microsoft, la extensión ya no está disponible en la tienda de complementos de Microsoft Edge para que los nuevos usuarios puedan descargar, pero los usuarios existentes pueden seguir usando sus copias de la extensión.  |  
| 10 |  Bloqueado |  Si se encuentra que la extensión es malintencionada y pone en peligro la seguridad y la privacidad de los usuarios, Microsoft tiene derecho a bloquear la extensión del almacén de complementos perimetrales y el estado cambia a este estado.  Si la extensión está bloqueada, se quita del almacén de complementos perimetrales y de todos los dispositivos de usuario.  |  
