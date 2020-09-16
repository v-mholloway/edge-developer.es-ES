---
description: El proceso de actualización de la extensión en Microsoft Store.
title: Actualizar una lista de extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 0d4512331b4f9542921d2063c908b5e9d4251074
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015684"
---
# Actualizar una lista de extensiones  

Actualizar un listado existente en el catálogo de complementos de Microsoft Edge \ (Microsoft Edge addons \).  Puede cambiar una extensión Publicada en cualquier momento.  Mientras está actualizando, no tiene que actualizar toda la extensión para realizar algunos cambios como, por ejemplo, la descripción o el logotipo de la actualización.  Pero si actualizas el paquete de extensiones, simplemente recuerda aumentar el número de versión cada vez.  

## Actualizar una extensión ya publicada  

Para actualizar su registro, siga estos pasos:  

1.  Vaya a su [Panel de programadores][MicrosoftPartnerCenter].  En la página Descripción general, haga clic en el listado que desea actualizar.  Esto muestra los detalles del formulario de envío que rellenó durante la publicación.  
1.  Realice los cambios que desee en el paquete, la descripción, los activos gráficos o cualquier otra configuración.  Si actualizas el archivo de paquete, asegúrate de que la versión del manifiesto sea posterior a la de la versión anterior del paquete.
1.  Después de realizar los cambios, haga clic en guardar y, a continuación, en publicar.
1.  Visita el panel del desarrollador del [centro de Partners][MicrosoftPartnerCenter] para ver cómo el estado del anuncio ha cambiado de `In the store` a `In the store.  Certification in progress` .  

> [!NOTE]
> La duración del proceso de publicación de actualizaciones es de unas pocas horas a varios días.  

Una vez que `Status` aparece la columna `In the store` , la actualización de extensión está disponible en los complementos de Microsoft Edge.  

## Actualizar una extensión durante el paso de certificación  

Puede editar y actualizar el envío de la extensión después de enviarlo antes de escribir el paso de publicación.  Puedes verificar el estado de tu extensión en la página de **Descripción general** de la extensión asociada a tu registro en el [centro de Partners][MicrosoftPartnerCenter].  

Para editar su envío, puede seguir estos pasos:  

1.  Vaya a su [Panel de programadores][MicrosoftPartnerCenter].  En la página **Descripción general** , haga clic en el listado que desea actualizar.  Esto muestra los detalles del formulario de envío que rellenó durante la publicación.  
1.  Vaya a la sección **Descripción general** de la extensión con la barra de navegación izquierda, tal como se muestra.  Para cancelar la presentación actual, haga clic en **Cancelar envío** .  
1.  Desplácese a otra sección y realice los cambios que desee en el paquete, la descripción, los activos gráficos u otras opciones.  Si actualizas el archivo de paquete, asegúrate de que la versión del manifiesto sea posterior a la de la versión anterior del paquete.  
1.  Después de realizar los cambios, haga clic en **Guardar** y, a continuación, en **publicar**.  

> [!IMPORTANT]
> Este proceso detiene y elimina el envío actual de nuestra canalización de certificados y comienza una nueva revisión con el último envío.  

> [!NOTE]
> La duración del proceso de publicación de actualizaciones es de unas pocas horas a varios días.  

Una vez que `Status` aparece la columna `In the store` , la actualización de extensión está disponible en los complementos de Microsoft Edge.  

## Quitar la extensión de los complementos de Microsoft Edge  

Para quitar la extensión de los complementos de Microsoft Edge, haga lo siguiente:  

1.  Vaya a su [Panel de programadores][MicrosoftPartnerCenter].  En la página **Descripción general** , haga clic en el listado que quiere quitar.  
1.  Abre la página de **información general de extensión** de tu registro.  
1.  Haga clic en **anular la publicación**.  Esto anula la publicación del listado de los complementos de Microsoft Edge.  

Estos pasos quitan la extensión de los complementos de Microsoft Edge, lo que significa que los nuevos usuarios no pueden encontrar su extensión ni instalarlo, pero los usuarios que ya instalaron la extensión pueden continuar usándolo.  

<!-- image links -->  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de socios"  
