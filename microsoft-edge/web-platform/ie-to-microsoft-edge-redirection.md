---
description: Mover usuarios a Microsoft Edge desde Internet Explorer
title: Mover usuarios a Microsoft Edge desde Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidad, plataforma web, Internet Explorer
ms.openlocfilehash: 687790a3fcbd912bf4d9896e5bd90c1d2be1159fbcc2db383b24689bd48df5b8
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11798807"
---
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a>Mover usuarios a Microsoft Edge desde Internet Explorer  

Muchos sitios web modernos tienen diseños incompatibles con Internet Explorer \(IE\).  Cuando un usuario de IE visita un sitio web público incompatible, el usuario puede recibir un mensaje.  El mensaje indica que el sitio web es incompatible con el explorador.  Después de mostrar el mensaje, se espera que el usuario cambie manualmente a un explorador moderno.  Para minimizar las interrupciones, a partir de la versión 84, Microsoft Edge admite una nueva funcionalidad que redirige automáticamente a los usuarios.  Cuando un usuario de IE navega a un sitio web incompatible con IE, Windows redirige automáticamente al usuario a Microsoft Edge.  Para revisar los sitios web de la lista, vaya a [Necesita Microsoft Edge lista][MicrosoftEdgeNeededgeV1].

En este artículo se describen los siguientes conceptos.  

*   Por qué se agrega un sitio web a la lista  
*   La experiencia del usuario para el redireccionamiento  
*   Solicitar una actualización a la lista  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a>¿Por qué se agrega un sitio web a la lista de compatibilidad de IE?  

La lista de compatibilidad de IE solo agrega un sitio web cuando se producen las siguientes acciones.  

*   Muestra a un usuario de IE un mensaje que sugiere que el usuario debe usar un explorador diferente por motivos de compatibilidad.  
*   El propietario solicita agregar el sitio web a la lista de compatibilidad de IE.  

## <a name="redirection-experience"></a>Experiencia de redirección

Al volver a Microsoft Edge, se muestra al usuario el cuadro de diálogo de una sola vez en la siguiente captura de pantalla.  El cuadro de diálogo proporciona al usuario la siguiente información.  

*   Explica por qué se redirige el sitio web.  
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
      *   La página principal  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notificación de exploración y aviso para importar datos y preferencias" lightbox="../media/neededge-dialog1.msft.png":::
         Notificación de exploración y aviso para importar datos y preferencias  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Si el usuario no da su consentimiento seleccionando la casilla Traer siempre mis **** datos y preferencias de exploración de **Internet Explorer,** el usuario puede elegir Continuar la exploración para continuar la   sesión de exploración.  

Por último, se muestra un banner de incompatibilidad de sitio web en la barra de direcciones para cada redirección.  En la siguiente figura se muestra un ejemplo de un banner de incompatibilidad de sitios web.

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notificación sobre sitios modernos y solicitud para establecer Microsoft Edge como explorador predeterminado o explorar Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   Notificación sobre sitios modernos y solicitud para establecer Microsoft Edge como explorador predeterminado o explorar Microsoft Edge  
:::image-end:::

El banner de incompatibilidad del sitio web proporciona los siguientes detalles al usuario.  

*   Recomienda al usuario que cambie a Microsoft Edge.  
*   Ofrece establecer Microsoft Edge como explorador predeterminado.  
*   Ofrece al usuario la opción de explorar Microsoft Edge.    
    
Cuando se redirige un sitio web desde Internet Explorer a Microsoft Edge, se produce una de las siguientes acciones.

*   Si la pestaña IE activa no tenía contenido anterior, se cierra.  
*   Si la pestaña IE activa tenía contenido anterior, se desplaza a la página de soporte técnico de Microsoft que explica por qué se redirija el sitio web [a Microsoft Edge.][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]  

> [!NOTE]
> Después de una redirección, los usuarios pueden seguir usando IE para sitios web que no están en la lista de compatibilidad de IE.  

## <a name="request-an-update-to-the-ie-compatibility-list"></a>Solicitar una actualización a la lista de compatibilidad de IE  

La lista de compatibilidad de IE es un archivo XML en [microsoft.com][MicrosoftOfficialHome].  La lista se actualiza periódicamente en respuesta a las solicitudes de los desarrolladores de sitios web y usuarios para agregar o quitar sitios web.  Las actualizaciones de la lista se descargan automáticamente en los equipos de usuario.  

Envíe por correo [electrónico la siguiente ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que su sitio web se agregará o quitará de la lista de compatibilidad de IE.    

*   Nombre del propietario  
*   Título corporativo  
*   Dirección de correo electrónico  
*   Nombre de la empresa  
*   Dirección  
*   Dirección del sitio web  
    
La lista de compatibilidad de IE se actualiza en una semana.

> [!NOTE]
> La lista de compatibilidad de IE está diseñada para funcionar solo con sitios públicos.  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar un correo electrónico a ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Inicio oficial de Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Necesita Microsoft Edge lista v1 xml | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "El sitio web al que intentabas llegar no funciona con Internet Explorer | Microsoft Office Soporte técnico"  
