---
description: Mover usuarios a Microsoft Edge desde Internet Explorer
title: Mover usuarios a Microsoft Edge desde Internet Explorer
author: MSEdgeTeam
ms.date: 11/13/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilidad, plataforma web, Internet Explorer
ms.openlocfilehash: c2106955ed79bd28dc1f847dee220944bb014689
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461139"
---
# <a name="moving-users-to-microsoft-edge-from-internet-explorer"></a><span data-ttu-id="8c792-104">Mover usuarios a Microsoft Edge desde Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="8c792-104">Moving users to Microsoft Edge from Internet Explorer</span></span>  

<span data-ttu-id="8c792-105">Muchos sitios web modernos tienen diseños incompatibles con Internet Explorer \(IE\).</span><span class="sxs-lookup"><span data-stu-id="8c792-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="8c792-106">Cuando un usuario de IE visita un sitio web público incompatible, el usuario puede recibir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="8c792-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="8c792-107">El mensaje indica que el sitio web es incompatible con el explorador.</span><span class="sxs-lookup"><span data-stu-id="8c792-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="8c792-108">Después de mostrar el mensaje, se espera que el usuario cambie manualmente a un explorador moderno.</span><span class="sxs-lookup"><span data-stu-id="8c792-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="8c792-109">Para minimizar las interrupciones, a partir de la versión 84, Microsoft Edge admite una nueva funcionalidad que redirige automáticamente a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="8c792-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="8c792-110">Cuando un usuario de IE navega a un sitio web incompatible con IE, Windows redirige automáticamente al usuario a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8c792-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="8c792-111">Para revisar los sitios web de la lista, vaya a [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="8c792-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="8c792-112">En este artículo se describen los siguientes conceptos.</span><span class="sxs-lookup"><span data-stu-id="8c792-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="8c792-113">Por qué se agrega un sitio web a la lista</span><span class="sxs-lookup"><span data-stu-id="8c792-113">Why a website is added to the list</span></span>  
*   <span data-ttu-id="8c792-114">La experiencia del usuario para el redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="8c792-114">The user experience for redirection</span></span>  
*   <span data-ttu-id="8c792-115">Solicitar una actualización a la lista</span><span class="sxs-lookup"><span data-stu-id="8c792-115">Request an update to the list</span></span>  
    
## <a name="why-is-a-website-added-to-the-ie-compatibility-list"></a><span data-ttu-id="8c792-116">¿Por qué se agrega un sitio web a la lista de compatibilidad de IE?</span><span class="sxs-lookup"><span data-stu-id="8c792-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="8c792-117">La lista de compatibilidad de IE solo agrega un sitio web cuando se producen las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="8c792-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="8c792-118">Muestra a un usuario de IE un mensaje que sugiere que el usuario debe usar un explorador diferente por motivos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="8c792-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="8c792-119">El propietario solicita agregar el sitio web a la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="8c792-119">Owner requests to add the website to the IE compatibility list.</span></span>  

## <a name="redirection-experience"></a><span data-ttu-id="8c792-120">Experiencia de redirección</span><span class="sxs-lookup"><span data-stu-id="8c792-120">Redirection experience</span></span>

<span data-ttu-id="8c792-121">En el redireccionamiento a Microsoft Edge, se muestra al usuario el cuadro de diálogo de una sola vez en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8c792-121">On redirection to Microsoft Edge, the user is shown the one-time dialog in the next screenshot.</span></span>  <span data-ttu-id="8c792-122">El cuadro de diálogo proporciona al usuario la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="8c792-122">The dialog provides the user with the following information.</span></span>  

*   <span data-ttu-id="8c792-123">Explica por qué se redirige el sitio web.</span><span class="sxs-lookup"><span data-stu-id="8c792-123">It explains why the website is being redirected.</span></span>  
*   <span data-ttu-id="8c792-124">Solicita al usuario su consentimiento para copiar los datos de exploración y las preferencias de IE a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8c792-124">It prompts the user for consent to copy browsing data and preferences from IE to Microsoft Edge.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="8c792-125">Se importan los siguientes datos de exploración.</span><span class="sxs-lookup"><span data-stu-id="8c792-125">The following browsing data is imported.</span></span>  
      
      *   <span data-ttu-id="8c792-126">Favoritos</span><span class="sxs-lookup"><span data-stu-id="8c792-126">Favorites</span></span>  
      *   <span data-ttu-id="8c792-127">Contraseñas</span><span class="sxs-lookup"><span data-stu-id="8c792-127">Passwords</span></span>  
      *   <span data-ttu-id="8c792-128">Motores de búsqueda</span><span class="sxs-lookup"><span data-stu-id="8c792-128">Search engines</span></span>  
      *   <span data-ttu-id="8c792-129">Abrir pestañas</span><span class="sxs-lookup"><span data-stu-id="8c792-129">Open tabs</span></span>  
      *   <span data-ttu-id="8c792-130">Historial</span><span class="sxs-lookup"><span data-stu-id="8c792-130">History</span></span>  
      *   <span data-ttu-id="8c792-131">Configuración</span><span class="sxs-lookup"><span data-stu-id="8c792-131">Settings</span></span>  
      *   <span data-ttu-id="8c792-132">Cookies</span><span class="sxs-lookup"><span data-stu-id="8c792-132">Cookies</span></span>  
      *   <span data-ttu-id="8c792-133">La página principal</span><span class="sxs-lookup"><span data-stu-id="8c792-133">The Home Page</span></span>  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/neededge-dialog1.msft.png" alt-text="Notificación de exploración y aviso para importar datos y preferencias" lightbox="../media/neededge-dialog1.msft.png":::
         <span data-ttu-id="8c792-135">Notificación de exploración y aviso para importar datos y preferencias</span><span class="sxs-lookup"><span data-stu-id="8c792-135">Browsing notification and prompt to import data and preferences</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="8c792-136">Si el usuario no da su consentimiento seleccionando la casilla Traer siempre mis  datos y preferencias de exploración de **Internet Explorer,** el usuario puede elegir Continuar la exploración para continuar la   sesión de exploración.</span><span class="sxs-lookup"><span data-stu-id="8c792-136">If the user does not consent by choosing the **Always bring over my browsing data and preferences from Internet Explorer** checkbox, the user may choose **Continue browsing** to continue the browsing session.</span></span>  

<span data-ttu-id="8c792-137">Por último, se muestra un banner de incompatibilidad de sitio web en la barra de direcciones para cada redirección.</span><span class="sxs-lookup"><span data-stu-id="8c792-137">Finally, a website incompatibility banner is displayed under the address bar for each redirection.</span></span>  <span data-ttu-id="8c792-138">En la siguiente figura se muestra un ejemplo de un banner de incompatibilidad de sitios web.</span><span class="sxs-lookup"><span data-stu-id="8c792-138">An example of a website incompatibility banner is displayed in following figure.</span></span>

:::image type="complex" source="../media/neededge-banner.msft.png" alt-text="Notificación sobre sitios modernos y solicitud para establecer Microsoft Edge como explorador predeterminado o explorar Microsoft Edge" lightbox="../media/neededge-banner.msft.png":::
   <span data-ttu-id="8c792-140">Notificación sobre sitios modernos y solicitud para establecer Microsoft Edge como explorador predeterminado o explorar Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="8c792-140">Notification about modern sites and prompt to set Microsoft Edge as default browser or explore Microsoft Edge</span></span>  
:::image-end:::

<span data-ttu-id="8c792-141">El banner de incompatibilidad del sitio web proporciona los siguientes detalles al usuario.</span><span class="sxs-lookup"><span data-stu-id="8c792-141">The website incompatibility banner provides the following details to the user.</span></span>  

*   <span data-ttu-id="8c792-142">Recomienda al usuario que cambie a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8c792-142">Recommends that the user to switch to Microsoft Edge.</span></span>  
*   <span data-ttu-id="8c792-143">Ofrece establecer Microsoft Edge como explorador predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8c792-143">Offers to set Microsoft Edge as the default browser.</span></span>  
*   <span data-ttu-id="8c792-144">Ofrece al usuario la opción de explorar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="8c792-144">Gives the user the option to explore Microsoft Edge.</span></span>    
    
<span data-ttu-id="8c792-145">Cuando se redirige un sitio web desde Internet Explorer a Microsoft Edge, se produce una de las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="8c792-145">When a website is redirected from Internet Explorer to Microsoft Edge, one of the following actions occurs.</span></span>

*   <span data-ttu-id="8c792-146">Si la pestaña IE activa no tenía contenido anterior, se cierra.</span><span class="sxs-lookup"><span data-stu-id="8c792-146">If the active IE tab had no prior content, it is closed.</span></span>  
*   <span data-ttu-id="8c792-147">Si la pestaña IE activa tenía contenido anterior, se desplaza a la página de soporte técnico de Microsoft que explica por qué se redirija el sitio web [a Microsoft Edge.][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]</span><span class="sxs-lookup"><span data-stu-id="8c792-147">If the active IE tab had prior content, it navigates to the [Microsoft support page that explains why the website was redirected to Microsoft Edge][MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer].</span></span>  

> [!NOTE]
> <span data-ttu-id="8c792-148">Después de una redirección, los usuarios pueden seguir usando IE para sitios web que no están en la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="8c792-148">After a redirection, users may continue to use IE for websites that are not on the IE compatibility list.</span></span>  

## <a name="request-an-update-to-the-ie-compatibility-list"></a><span data-ttu-id="8c792-149">Solicitar una actualización a la lista de compatibilidad de IE</span><span class="sxs-lookup"><span data-stu-id="8c792-149">Request an update to the IE compatibility list</span></span>  

<span data-ttu-id="8c792-150">La lista de compatibilidad de IE es un archivo XML en [microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="8c792-150">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="8c792-151">La lista se actualiza periódicamente en respuesta a las solicitudes de los desarrolladores de sitios web y usuarios para agregar o quitar sitios web.</span><span class="sxs-lookup"><span data-stu-id="8c792-151">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="8c792-152">Las actualizaciones de la lista se descargan automáticamente en los equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="8c792-152">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="8c792-153">Envíe por correo [electrónico la siguiente ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que su sitio web se agregará o quitará de la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="8c792-153">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="8c792-154">Nombre del propietario</span><span class="sxs-lookup"><span data-stu-id="8c792-154">Owner name</span></span>  
*   <span data-ttu-id="8c792-155">Título corporativo</span><span class="sxs-lookup"><span data-stu-id="8c792-155">Corporate title</span></span>  
*   <span data-ttu-id="8c792-156">Dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="8c792-156">Email address</span></span>  
*   <span data-ttu-id="8c792-157">Nombre de la empresa</span><span class="sxs-lookup"><span data-stu-id="8c792-157">Company name</span></span>  
*   <span data-ttu-id="8c792-158">Dirección</span><span class="sxs-lookup"><span data-stu-id="8c792-158">Street address</span></span>  
*   <span data-ttu-id="8c792-159">Dirección del sitio web</span><span class="sxs-lookup"><span data-stu-id="8c792-159">Website address</span></span>  
    
<span data-ttu-id="8c792-160">La lista de compatibilidad de IE se actualiza en una semana.</span><span class="sxs-lookup"><span data-stu-id="8c792-160">The IE compatibility list is updated within a week.</span></span>

> [!NOTE]
> <span data-ttu-id="8c792-161">La lista de compatibilidad de IE está diseñada para funcionar solo con sitios públicos.</span><span class="sxs-lookup"><span data-stu-id="8c792-161">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar un correo electrónico a ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Inicio oficial de Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Necesita microsoft edge list v1 xml | Microsoft Edge"  

[MicrosoftSupportOfficeTheWebsiteYouWereTryingToReachDoesntWorkWithInternetExplorer]: https://support.microsoft.com/office/the-website-you-were-trying-to-reach-doesn-t-work-with-internet-explorer-8f5fc675-cd47-414c-9535-12821ddfc554 "El sitio web al que intentabas llegar no funciona con Internet Explorer | Microsoft Office soporte técnico"  
