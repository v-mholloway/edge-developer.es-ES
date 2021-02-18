---
description: Proceso de actualización o eliminación de extensiones del almacén de complementos de Microsoft Edge
title: Actualizar una lista de extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones de explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 692c534ac0586d53002e4a032197e22ae24e2863
ms.sourcegitcommit: 916b4daa26c2c78611f7d837bd6ecf009f0082df
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/17/2021
ms.locfileid: "11343178"
---
# Actualizar o quitar la extensión  

Puedes actualizar una extensión enviada o quitar una descripción de extensión publicada de la tienda de complementos de Microsoft Edge en cualquier momento.  

## Actualizar la extensión en el almacén de complementos de Microsoft Edge  

> [!NOTE]
> La duración del proceso de certificación para una actualización de una extensión puede tardar entre unas horas y unos días.  

### Actualizar una extensión existente en el almacén de complementos de Microsoft Edge  

Para actualizar la extensión en la tienda, siga estos pasos.  

1.  Ve al panel [del desarrollador][MicrosoftPartnerCenter] y elige la extensión que quieras actualizar.  
1.  Actualiza el paquete de extensión o los metadatos de la extensión.  Si actualiza el paquete de extensión, asegúrese de aumentar la versión en el archivo de manifiesto.  
1.  Después de realizar los cambios, elija **Guardar**publicación para actualizar la lista de extensiones  >  **** e inicie el proceso de certificación.  
1.  Una vez `Status` que se muestra la columna, la actualización de extensión está disponible en el almacén de complementos de Microsoft `In the store` Edge.  
    
### Actualizar la extensión durante el paso de certificación  

Mientras la extensión aún esté en la fase de certificación y antes de que se publique en la tienda de complementos de Microsoft Edge, puedes actualizarla. Si la extensión no cumple el proceso de certificación, es posible que también deba actualizar la extensión.    

Para comprobar el estado de la extensión, ve al panel asociado a tu descripción en el [Centro de partners.][MicrosoftPartnerCenter]  

Para editar el envío, sigue estos pasos.  

1.  Ve al panel [del desarrollador][MicrosoftPartnerCenter] y elige la extensión que quieras actualizar.  Se muestra la información que rellenaste durante el envío anterior.  
1.  Para abrir la **sección Información general de** extensión, use la barra de navegación izquierda.  Para cancelar el envío actual, elija **Cancelar envío.**  
1.  Pase a otras secciones y actualice el paquete de extensión o los metadatos de la extensión.  Si actualizas el paquete de extensión, asegúrate de aumentar la versión en el archivo de manifiesto para que coincida con los cambios desde la versión anterior del paquete.  
1.  Después de realizar cambios, elija **Guardar**  >  **publicación.**  
    
> [!IMPORTANT]
> El proceso se detiene y quita el envío actual de la canalización de certificación de extensiones de Microsoft Edge y se inicia una nueva revisión con el envío más reciente.  

### Actualizar la extensión después de que no se haya podido realizar la certificación  

Después de que la extensión no haya podido realizar el proceso de certificación, debe actualizar la extensión y volver a enviar la extensión que incorpora los comentarios.  

Para editar la extensión, siga estos pasos.  

1.  Vaya al panel [del desarrollador][MicrosoftPartnerCenter] y elija la extensión que no ha podido obtener la certificación.  
1.  Actualiza el paquete de extensión o los metadatos que incorporan los comentarios recibidos del proceso de certificación.  Si actualiza el paquete de extensión, asegúrese de aumentar la versión en el archivo de manifiesto.  
1.  Después de realizar cambios, elija **Guardar**  >  **publicación.**  
    
## Quitar extensiones del almacén de complementos de Microsoft Edge  

Para quitar la extensión del almacén de complementos de Microsoft Edge, siga estos pasos.  

1.  Vaya al panel [del desarrollador.][MicrosoftPartnerCenter]  En la página Panel, elija la descripción que desea quitar.  
1.  Elija **Información general sobre la** extensión en la descripción.  
1.  Elija **Anular publicación** para quitar la descripción del almacén de complementos de Microsoft Edge.  
    
La extensión ahora se ha quitado del almacén de complementos de Microsoft Edge.  Es posible que los usuarios que ya han instalado la extensión la sigan usando, pero los nuevos usuarios no la encuentran.  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  
