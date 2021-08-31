---
description: Actualizar o quitar extensiones del sitio Microsoft Edge de complementos.
title: Actualizar una Microsoft Edge extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 11d844327d2d4a652745cb73b311f4a97b6174d7
ms.sourcegitcommit: dc445eae30234af1ad3fa42645aabb940529912b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934315"
---
# <a name="update-a-microsoft-edge-extension"></a>Actualizar una Microsoft Edge extensión  

Puede actualizar una extensión enviada o quitar una descripción de extensión publicada del sitio web Microsoft Edge complementos en cualquier momento.  

> [!NOTE]
> El proceso de certificación de una actualización de una extensión puede tardar entre unas horas y unos días.

## <a name="update-an-existing-extension-in-the-microsoft-edge-add-ons-website"></a>Actualizar una extensión existente en el sitio Microsoft Edge de complementos  

Para actualizar la extensión en la tienda:

1.  Vaya al panel [de desarrolladores][MicrosoftPartnerCenter] y seleccione la extensión que desea actualizar.  

1.  Actualice el paquete de extensión o los metadatos de la extensión.  Si actualiza el paquete de extensión, asegúrese de aumentar la versión en el archivo de manifiesto.  

1.  Después de realizar los cambios, seleccione **Guardar**publicación para actualizar la descripción de la  >  **** extensión e iniciar el proceso de certificación.  

1.  Después de que se muestre la columna, la actualización de extensión está disponible en el Microsoft Edge `Status` `In the store` de complementos.  

<!-- todo: uncomment after the API is available for use.
After your extension has been initially created, you will be able to update it programmatically by [Using the Microsoft Edge Add-ons API][UsingAddonsAPI].
-->


## <a name="update-your-extension-during-the-certification-step"></a>Actualizar la extensión durante el paso de certificación  

Aunque la extensión aún está en la fase de certificación y antes de que se publique en el sitio web Microsoft Edge complementos, puede actualizarla. Si la extensión produce un error en el proceso de certificación, es posible que también necesite actualizar la extensión.    

Para comprobar el estado de la extensión, vaya al panel asociado a su descripción en [el Centro de partners][MicrosoftPartnerCenter].  

Para editar el envío:

1.  Navegue hasta el [panel del desarrollador][MicrosoftPartnerCenter] y seleccione la extensión que desea actualizar.  Se muestra la información que rellenaste durante el envío anterior.  

1.  Para abrir la **sección Información general** de extensión, use la barra de navegación izquierda.  Para cancelar el envío actual, seleccione **Cancelar envío**.  

1.  Muévete a otras secciones y actualiza el paquete de extensión o los metadatos de la extensión.  Si actualiza el paquete de extensión, asegúrese de aumentar la versión del archivo de manifiesto para que coincida con los cambios realizados desde la versión anterior del paquete.  

1.  Después de realizar cambios, **seleccione Guardar**  >  **publicar**.  
    
> [!IMPORTANT]
> El proceso detiene y quita el envío actual de la canalización de certificación de extensiones de Microsoft Edge y una nueva revisión comienza con el envío más reciente.  


## <a name="update-your-extension-after-it-failed-the-certification"></a>Actualizar la extensión después de que falló la certificación  

Después de que la extensión falló el proceso de certificación, debes actualizar la extensión y volver a enviar la extensión que incorpora los comentarios.  

Para editar la extensión:

1.  Navegue hasta el [panel de desarrolladores][MicrosoftPartnerCenter] y seleccione la extensión que ha fallado en el proceso de certificación.  

1.  Actualice el paquete de extensión o los metadatos que incorporan los comentarios recibidos del proceso de certificación.  Si actualiza el paquete de extensión, asegúrese de aumentar la versión en el archivo de manifiesto.  

1.  Después de realizar cambios, **seleccione Guardar**  >  **publicar**.  

    
## <a name="remove-an-extension-from-the-microsoft-edge-add-ons-website"></a>Quitar una extensión del sitio Microsoft Edge de complementos

Para quitar una extensión del sitio Microsoft Edge complementos:

1.  Vaya al panel [de desarrolladores][MicrosoftPartnerCenter].  En la página Panel, seleccione la lista que desea quitar.  

1.  Selecciona **Información general sobre extensiones** en la descripción.  

1.  Seleccione **Anular publicación** para quitar la descripción del sitio Microsoft Edge de complementos.  
    
La extensión se ha quitado del sitio Microsoft Edge de complementos.  Los usuarios que ya instalaron la extensión pueden seguir usarla, pero los nuevos usuarios no la encuentran.  

<!-- links -->
[UsingAddonsAPI]: api/using-addons-api.md "Uso de la API Microsoft Edge complementos | Microsoft Docs"
<!-- external links -->
[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  
