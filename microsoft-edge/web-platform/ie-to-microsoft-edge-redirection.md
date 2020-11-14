---
description: Mover usuarios a Microsoft Edge desde Internet Explorer
title: Mover usuarios a Microsoft Edge desde Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidad, plataforma web, Internet Explorer
ms.openlocfilehash: 872bd5ec52f471e4958ef7354c046ec30f1ba72e
ms.sourcegitcommit: 62258ce0ef469948ca8af42141d02aa9719243f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/13/2020
ms.locfileid: "11168374"
---
# Mover usuarios a Microsoft Edge desde Internet Explorer  

Muchos sitios web modernos tienen diseños incompatibles con Internet Explorer \ (IE \).  Cuando un usuario de IE visita un sitio web público incompatible, es posible que reciba un mensaje.  El mensaje indica que el sitio web es incompatible con el explorador.  Después de que se muestre el mensaje, se espera que el usuario cambie manualmente a un explorador moderno.  Para minimizar las interrupciones, a partir de la versión 84, Microsoft Edge admite una nueva capacidad que redirige a los usuarios de forma automática.  Cuando un usuario de IE navega a un sitio web que es incompatible con IE, Windows redirige automáticamente al usuario a Microsoft Edge.  Para revisar los sitios web de la lista, vaya a [necesita una lista de Microsoft Edge][MicrosoftEdgeNeededgeV1].

En este artículo se describen los siguientes conceptos:  

*   Por qué se agrega un sitio web a la lista  
*   La experiencia de usuario para el redireccionamiento  
*   Solicitar una actualización de la lista  
    
## ¿Por qué se agrega un sitio web a la lista de compatibilidad de IE?  

La lista de compatibilidad de IE solo agrega un sitio web cuando se producen las siguientes acciones.  

*   Muestra un usuario de IE un mensaje que sugiere que el usuario debe usar un explorador diferente por razones de compatibilidad.  
*   Solicitudes de propietario para agregar el sitio web a la lista de compatibilidad de IE.  

## Experiencia de redirección

En el redireccionamiento a Microsoft Edge, se muestra al usuario el cuadro de diálogo de una sola vez en la siguiente captura de pantalla.  El cuadro de diálogo proporciona al usuario la siguiente información.  

*   Explica por qué se redirige el sitio Web.  
*   Solicita al usuario su consentimiento para copiar los datos de exploración y las preferencias de IE a Microsoft Edge.  

:::row:::
   :::column span="":::
      Se importan los siguientes datos de exploración.  
      
      *   Favoritos  
      *   Contraseñas  
      *   Motores de búsqueda  
      *   Abrir pestañas  
      *   Historial  
      *   Configuración  
      *   Cookies  
      *   La Página principal  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Examen de la notificación y solicitud para importar datos y preferencias" lightbox="../media/neededge-dialog1.msft.png":::
         Examen de la notificación y solicitud para importar datos y preferencias  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Si el usuario no acepta el consentimiento seleccionando la casilla **de verificación presentar siempre los datos y preferencias de búsqueda de Internet Explorer** , el usuario puede elegir continuar con la **exploración**   para continuar con la sesión de exploración.  

Por último, se muestra un banner de incompatibilidad de sitios web debajo de la barra de direcciones para cada redireccionamiento.  En la siguiente ilustración se muestra un ejemplo de un banner de incompatibilidad de sitios Web.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notificaciones sobre sitios modernos y preguntar para establecer Microsoft Edge como explorador predeterminado o explorar Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Notificaciones sobre sitios modernos y preguntar para establecer Microsoft Edge como explorador predeterminado o explorar Microsoft Edge  
:::image-end:::

El banner de incompatibilidad del sitio web proporciona los siguientes detalles al usuario.  

*   Recomienda que el usuario cambie a Microsoft Edge.  
*   Ofrece establecer Microsoft Edge como explorador predeterminado.  
*   Ofrece al usuario la opción de explorar Microsoft Edge.    
    
Cuando se redirige un sitio web de Internet Explorer a Microsoft Edge, se produce una de las siguientes acciones.

*   Si la pestaña activa de IE no tenía contenido anterior, se cerrará.  
*   Si la pestaña activa de IE tenía contenido anterior, se desplaza a la [Página de soporte técnico de Microsoft que explica por qué el sitio web se redirigió a Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].  

> [!NOTE]
> Después de una redirección, los usuarios pueden seguir usando IE en sitios web que no se encuentran en la lista de compatibilidad de IE.  

## Solicitar una actualización de la lista de compatibilidad de IE  

La lista de compatibilidad de IE es un archivo XML en [Microsoft.com][MicrosoftOfficialHome].  La lista se actualiza regularmente en respuesta a las solicitudes de los programadores de usuarios y sitios web para agregar o quitar sitios Web.  Las actualizaciones de la lista se descargan automáticamente en los equipos de los usuarios.  

Envíe por correo electrónico la siguiente información a [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que su sitio web se agregue o se quite de la lista de compatibilidad de IE.    

*   Nombre del propietario  
*   Título de la empresa  
*   Dirección de correo electrónico  
*   Nombre de la empresa  
*   Dirección  
*   Dirección del sitio web  
    
> [!NOTE]
> La lista de compatibilidad de IE está diseñada para trabajar solo con sitios públicos.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar un correo electrónico a ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Página de inicio oficial de Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Se necesita la lista de Microsoft Edge v1 XML Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "El sitio web al que intentaba llamar no funciona con Internet Explorer | Soporte técnico de Microsoft Office"  
