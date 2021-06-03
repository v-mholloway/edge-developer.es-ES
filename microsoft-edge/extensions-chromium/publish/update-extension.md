---
description: Proceso de actualización o eliminación de extensiones del almacén de Microsoft Edge complementos
title: Actualizar una descripción de extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 692c534ac0586d53002e4a032197e22ae24e2863
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343178"
---
# Actualizar o quitar la extensión  

Puede actualizar una extensión enviada o quitar una descripción de extensión publicada del Microsoft Edge complementos en cualquier momento.  

## Actualizar la extensión en el almacén Microsoft Edge complementos  

> [!NOTE]
> La duración del proceso de certificación para una actualización de una extensión puede tardar entre unas horas y unos días.  

### Actualizar una extensión existente en el Microsoft Edge complementos  

Para actualizar la extensión en la tienda, siga estos pasos.  

1.  Vaya al panel [de desarrolladores][MicrosoftPartnerCenter] y elija la extensión que desea actualizar.  
1.  Actualice el paquete de extensión o los metadatos de la extensión.  Si actualiza el paquete de extensión, asegúrese de aumentar la versión en el archivo de manifiesto.  
1.  Después de realizar los cambios, elija **Guardar**publicación para actualizar la descripción de la  >  **** extensión e iniciar el proceso de certificación.  
1.  Después de que se muestre la columna, la actualización de extensión está `Status` disponible en el Microsoft Edge de `In the store` complementos.  
    
### Actualizar la extensión durante el paso de certificación  

Aunque la extensión todavía está en la fase de certificación y antes de que se publique en el almacén de complementos Microsoft Edge, puede actualizarla. Si la extensión produce un error en el proceso de certificación, es posible que también deba actualizar la extensión.    

Para comprobar el estado de la extensión, vaya al panel asociado a su descripción en [el Centro de partners][MicrosoftPartnerCenter].  

Para editar el envío, siga estos pasos.  

1.  Vaya al panel [de desarrolladores][MicrosoftPartnerCenter] y elija la extensión que desea actualizar.  Se muestra la información que rellenaste durante el envío anterior.  
1.  Para abrir la **sección Información general** de extensión, use la barra de navegación izquierda.  Para cancelar el envío actual, elija **Cancelar envío**.  
1.  Muévete a otras secciones y actualiza el paquete de extensión o los metadatos de la extensión.  Si actualiza el paquete de extensión, asegúrese de aumentar la versión del archivo de manifiesto para que coincida con los cambios realizados desde la versión anterior del paquete.  
1.  Después de realizar cambios, elija **Guardar**  >  **publicación**.  
    
> [!IMPORTANT]
> El proceso detiene y quita el envío actual de la canalización de certificación de extensiones de Microsoft Edge y una nueva revisión comienza con el envío más reciente.  

### Actualizar la extensión después de que falló la certificación  

Después de que la extensión falló el proceso de certificación, debes actualizar la extensión y volver a enviar la extensión que incorpora los comentarios.  

Para editar la extensión, siga estos pasos.  

1.  Vaya al panel [de desarrolladores][MicrosoftPartnerCenter] y elija la extensión que falló en el proceso de certificación.  
1.  Actualice el paquete de extensión o los metadatos que incorporan los comentarios recibidos del proceso de certificación.  Si actualiza el paquete de extensión, asegúrese de aumentar la versión en el archivo de manifiesto.  
1.  Después de realizar cambios, elija **Guardar**  >  **publicación**.  
    
## Quitar extensiones del almacén Microsoft Edge complementos  

Para quitar la extensión del Microsoft Edge complementos, siga estos pasos.  

1.  Vaya al panel [de desarrolladores][MicrosoftPartnerCenter].  En la página Panel, elija la lista que desea quitar.  
1.  Elija **Información general sobre la** extensión en la descripción.  
1.  Elija **Unpublish** para quitar la descripción del Microsoft Edge de complementos.  
    
La extensión se ha quitado del Microsoft Edge complementos.  Es posible que los usuarios que ya instalaron la extensión la sigan usando, pero los nuevos usuarios no la encuentran.  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  
