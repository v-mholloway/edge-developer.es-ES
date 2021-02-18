---
description: Obtenga información sobre los diferentes estados al enviar extensiones a la tienda
title: Estados de envío para extensiones en la tienda
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 881166471ec5fabb66367ead650cb86b883cf01d
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343147"
---
# Estados de envío de extensiones en el almacén de complementos de Microsoft Edge  

La página de información general del Centro de partners muestra el estado de la extensión en el flujo de envío general.  En este artículo se describen los diferentes estados en los que puede encontrarse la extensión en cualquier momento durante el proceso de envío y certificación.  

| # |  Estado |  Detalles |  
|:--- |:--- |:--- |  
| 1 |  En borrador |  Creas el envío y guardas un borrador en tu cuenta.  No has enviado el paquete de extensión ni los detalles del formulario de envío para publicarlos en la tienda de complementos de Microsoft Edge.  La extensión no está disponible para los usuarios en este estado.  |  
| 2|  En revisión |  Ha enviado la extensión.  Microsoft revisa el paquete de extensión y los detalles del formulario de envío.  La extensión no está disponible para los usuarios en este estado.  |  
| 3|  En espera de publicar |  El envío se encuentra en este estado una vez completada la revisión de la extensión y la extensión se prepara para su publicación en Microsoft Store.  Este estado es un estado intermedio entre `In review` y `In the store` .  Es posible que este estado no aparezca para todos los envíos.  |  
| 4|  En la tienda |  La revisión ya está completa y la extensión se publica en la Tienda de complementos de Microsoft Edge.  La extensión está disponible en Microsoft Store en los mercados que especificaste.  |  
| 5 |  En la tienda.  Actualizar en revisión |  La extensión se publica en la tienda de complementos de Microsoft Edge y has enviado una actualización que Microsoft está revisando.  |  
| 6 |  Error de revisión |  El envío está en este estado si la extensión no puede revisarse.  Puede producirse un error de revisión durante la revisión inicial o durante una actualización.  Debe tomar medidas correctivas y volver a enviar la extensión.  |  
| 7 |  No disponible en la tienda |  Existen tres escenarios posibles cuando la extensión muestra este estado:  **Unpublished from store**, **Removed from store**y **Blocked**.  La descripción de cada uno de los tres estados se especifica en 8, 9 y 10.  |  
| 8 |  Unpublished from store |  Has publicado la extensión de la tienda de complementos de Microsoft Edge en el Centro de partners.  En el Centro de partners, has **elegido anular la publicación** en la página de envío de extensión.  Después de anular la publicación de la extensión, ya no está disponible en la tienda de complementos de Microsoft Edge para que los usuarios nuevos puedan descargar, pero los usuarios existentes pueden seguir usando sus copias de la extensión.  |  
| 9 |  Se quitó del almacén |  Si se encuentra que la extensión infringe los términos y condiciones del almacén de complementos de Microsoft Edge, Microsoft puede quitarla del almacén de complementos perimetrales y los cambios de estado en este estado.  <br />  Después de quitar la extensión por parte de Microsoft, la extensión ya no está disponible en la tienda de complementos de Microsoft Edge para que los usuarios nuevos puedan descargar, pero los usuarios existentes pueden seguir usando sus copias de la extensión.  |  
| 10 |  Bloqueado |  Si se encuentra que la extensión es malintencionada y pone en peligro la seguridad y privacidad de los usuarios, Microsoft tiene derecho a bloquear la extensión del almacén de complementos perimetrales y el estado cambia a este estado.  Si la extensión está bloqueada, se quita del almacén de complementos perimetrales y de todos los dispositivos de usuario.  |  
