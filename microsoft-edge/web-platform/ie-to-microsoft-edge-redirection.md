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
# <span data-ttu-id="7e1fe-104">Mover usuarios a Microsoft Edge desde Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="7e1fe-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="7e1fe-105">Muchos sitios web modernos tienen diseños incompatibles con Internet Explorer \ (IE \).</span><span class="sxs-lookup"><span data-stu-id="7e1fe-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="7e1fe-106">Cuando un usuario de IE visita un sitio web público incompatible, es posible que reciba un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="7e1fe-107">El mensaje indica que el sitio web es incompatible con el explorador.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="7e1fe-108">Después de que se muestre el mensaje, se espera que el usuario cambie manualmente a un explorador moderno.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="7e1fe-109">Para minimizar las interrupciones, a partir de la versión 84, Microsoft Edge admite una nueva capacidad que redirige a los usuarios de forma automática.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="7e1fe-110">Cuando un usuario de IE navega a un sitio web que es incompatible con IE, Windows redirige automáticamente al usuario a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="7e1fe-111">Para revisar los sitios web de la lista, vaya a [necesita una lista de Microsoft Edge][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="7e1fe-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="7e1fe-112">En este artículo se describen los siguientes conceptos:</span><span class="sxs-lookup"><span data-stu-id="7e1fe-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="7e1fe-113">Por qué se agrega un sitio web a la lista</span><span class="sxs-lookup"><span data-stu-id="7e1fe-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="7e1fe-114">La experiencia de usuario para el redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="7e1fe-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="7e1fe-115">Solicitar una actualización de la lista</span><span class="sxs-lookup"><span data-stu-id="7e1fe-115">Request an update to the list</span></span>  
    
## <span data-ttu-id="7e1fe-116">¿Por qué se agrega un sitio web a la lista de compatibilidad de IE?</span><span class="sxs-lookup"><span data-stu-id="7e1fe-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="7e1fe-117">La lista de compatibilidad de IE solo agrega un sitio web cuando se producen las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="7e1fe-118">Muestra un usuario de IE un mensaje que sugiere que el usuario debe usar un explorador diferente por razones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="7e1fe-119">Solicitudes de propietario para agregar el sitio web a la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <span data-ttu-id="7e1fe-120">Experiencia de redirección</span><span class="sxs-lookup"><span data-stu-id="7e1fe-120">Redirection experience</span></span>

<span data-ttu-id="7e1fe-121">En el redireccionamiento a Microsoft Edge, se muestra al usuario el cuadro de diálogo de una sola vez en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="7e1fe-122">El cuadro de diálogo proporciona al usuario la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="7e1fe-123">Explica por qué se redirige el sitio Web.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="7e1fe-124">Solicita al usuario su consentimiento para copiar los datos de exploración y las preferencias de IE a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="7e1fe-125">Se importan los siguientes datos de exploración.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="7e1fe-126">Favoritos</span><span class="sxs-lookup"><span data-stu-id="7e1fe-126">Favorites</span></span>  
      *   <span data-ttu-id="7e1fe-127">Contraseñas</span><span class="sxs-lookup"><span data-stu-id="7e1fe-127">Passwords</span></span>  
      *   <span data-ttu-id="7e1fe-128">Motores de búsqueda</span><span class="sxs-lookup"><span data-stu-id="7e1fe-128">Search engines</span></span>  
      *   <span data-ttu-id="7e1fe-129">Abrir pestañas</span><span class="sxs-lookup"><span data-stu-id="7e1fe-129">Open tabs</span></span>  
      *   <span data-ttu-id="7e1fe-130">Historial</span><span class="sxs-lookup"><span data-stu-id="7e1fe-130">History</span></span>  
      *   <span data-ttu-id="7e1fe-131">Configuración</span><span class="sxs-lookup"><span data-stu-id="7e1fe-131">Settings</span></span>  
      *   <span data-ttu-id="7e1fe-132">Cookies</span><span class="sxs-lookup"><span data-stu-id="7e1fe-132">Cookies</span></span>  
      *   <span data-ttu-id="7e1fe-133">La Página principal</span><span class="sxs-lookup"><span data-stu-id="7e1fe-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Examen de la notificación y solicitud para importar datos y preferencias" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="7e1fe-135">Examen de la notificación y solicitud para importar datos y preferencias</span><span class="sxs-lookup"><span data-stu-id="7e1fe-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="7e1fe-136">Si el usuario no acepta el consentimiento seleccionando la casilla **de verificación presentar siempre los datos y preferencias de búsqueda de Internet Explorer** , el usuario puede elegir continuar con la **exploración**   para continuar con la sesión de exploración.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="7e1fe-137">Por último, se muestra un banner de incompatibilidad de sitios web debajo de la barra de direcciones para cada redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="7e1fe-138">En la siguiente ilustración se muestra un ejemplo de un banner de incompatibilidad de sitios Web.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notificaciones sobre sitios modernos y preguntar para establecer Microsoft Edge como explorador predeterminado o explorar Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="7e1fe-140">Notificaciones sobre sitios modernos y preguntar para establecer Microsoft Edge como explorador predeterminado o explorar Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7e1fe-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="7e1fe-141">El banner de incompatibilidad del sitio web proporciona los siguientes detalles al usuario.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="7e1fe-142">Recomienda que el usuario cambie a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="7e1fe-143">Ofrece establecer Microsoft Edge como explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="7e1fe-144">Ofrece al usuario la opción de explorar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="7e1fe-145">Cuando se redirige un sitio web de Internet Explorer a Microsoft Edge, se produce una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="7e1fe-146">Si la pestaña activa de IE no tenía contenido anterior, se cerrará.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="7e1fe-147">Si la pestaña activa de IE tenía contenido anterior, se desplaza a la [Página de soporte técnico de Microsoft que explica por qué el sitio web se redirigió a Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span><span class="sxs-lookup"><span data-stu-id="7e1fe-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="7e1fe-148">Después de una redirección, los usuarios pueden seguir usando IE en sitios web que no se encuentran en la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <span data-ttu-id="7e1fe-149">Solicitar una actualización de la lista de compatibilidad de IE</span><span class="sxs-lookup"><span data-stu-id="7e1fe-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="7e1fe-150">La lista de compatibilidad de IE es un archivo XML en [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="7e1fe-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="7e1fe-151">La lista se actualiza regularmente en respuesta a las solicitudes de los programadores de usuarios y sitios web para agregar o quitar sitios Web.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="7e1fe-152">Las actualizaciones de la lista se descargan automáticamente en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="7e1fe-153">Envíe por correo electrónico la siguiente información a [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que su sitio web se agregue o se quite de la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="7e1fe-154">Nombre del propietario</span><span class="sxs-lookup"><span data-stu-id="7e1fe-154">Owner name</span></span>  
*   <span data-ttu-id="7e1fe-155">Título de la empresa</span><span class="sxs-lookup"><span data-stu-id="7e1fe-155">Corporate title</span></span>  
*   <span data-ttu-id="7e1fe-156">Dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="7e1fe-156">Email address</span></span>  
*   <span data-ttu-id="7e1fe-157">Nombre de la empresa</span><span class="sxs-lookup"><span data-stu-id="7e1fe-157">Company name</span></span>  
*   <span data-ttu-id="7e1fe-158">Dirección</span><span class="sxs-lookup"><span data-stu-id="7e1fe-158">Street address</span></span>  
*   <span data-ttu-id="7e1fe-159">Dirección del sitio web</span><span class="sxs-lookup"><span data-stu-id="7e1fe-159">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="7e1fe-160">La lista de compatibilidad de IE está diseñada para trabajar solo con sitios públicos.</span><span class="sxs-lookup"><span data-stu-id="7e1fe-160">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar un correo electrónico a ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Página de inicio oficial de Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Se necesita la lista de Microsoft Edge v1 XML Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "El sitio web al que intentaba llamar no funciona con Internet Explorer | Soporte técnico de Microsoft Office"  
