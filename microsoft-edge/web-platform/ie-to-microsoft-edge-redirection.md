---
description: Mover usuarios a Microsoft Edge desde Internet Explorer
title: Mover usuarios a Microsoft Edge desde Internet Explorer
author: MSEdgeTeam
ms.date: 11/06/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidad, plataforma web, Internet Explorer
ms.openlocfilehash: 2e1488359e405247e290ad8f6300c480a7e20af6
ms.sourcegitcommit: 6ef48c8cda392c6bf8217cff5f696ac620d10739
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/10/2020
ms.locfileid: "11163211"
---
# <span data-ttu-id="a47a6-104">Mover usuarios a Microsoft Edge desde Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="a47a6-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="a47a6-105">Muchos sitios web modernos tienen diseños incompatibles con Internet Explorer \ (IE \).</span><span class="sxs-lookup"><span data-stu-id="a47a6-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="a47a6-106">Cuando un usuario de IE visita un sitio web público incompatible, es posible que reciba un mensaje.</span><span class="sxs-lookup"><span data-stu-id="a47a6-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="a47a6-107">El mensaje indica que el sitio web es incompatible con el explorador.</span><span class="sxs-lookup"><span data-stu-id="a47a6-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="a47a6-108">Después de que se muestre el mensaje, se espera que el usuario cambie manualmente a un explorador moderno.</span><span class="sxs-lookup"><span data-stu-id="a47a6-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="a47a6-109">Para minimizar las interrupciones, a partir de la versión 84, Microsoft Edge admite una nueva capacidad que redirige a los usuarios de forma automática.</span><span class="sxs-lookup"><span data-stu-id="a47a6-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="a47a6-110">Cuando un usuario de IE navega a un sitio web que es incompatible con IE, Windows redirige automáticamente al usuario a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a47a6-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="a47a6-111">Para revisar los sitios web de la lista, vaya a [necesita una lista de Microsoft Edge][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="a47a6-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="a47a6-112">En este artículo se describen los siguientes conceptos:</span><span class="sxs-lookup"><span data-stu-id="a47a6-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="a47a6-113">La experiencia de usuario para el redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="a47a6-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="a47a6-114">Cómo solicitar una actualización a la lista</span><span class="sxs-lookup"><span data-stu-id="a47a6-114">How to request an update to the list</span></span>  
    
## <span data-ttu-id="a47a6-115">¿Por qué se agrega un sitio web a la lista de compatibilidad de IE?</span><span class="sxs-lookup"><span data-stu-id="a47a6-115">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="a47a6-116">La lista de compatibilidad de IE solo agrega un sitio web cuando se producen las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="a47a6-116">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="a47a6-117">Muestra un usuario de IE un mensaje que sugiere que el usuario debe usar un explorador diferente por razones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="a47a6-117">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="a47a6-118">Solicitudes de propietario para agregar el sitio web a la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="a47a6-118">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="a47a6-119">Actualizar la lista de compatibilidad de IE</span><span class="sxs-lookup"><span data-stu-id="a47a6-119">Update the IE compatibility list</span></span>  

<span data-ttu-id="a47a6-120">La lista de compatibilidad de IE es un archivo XML en [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="a47a6-120">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="a47a6-121">La lista se actualiza regularmente en respuesta a las solicitudes de los programadores de usuarios y sitios web para agregar o quitar sitios Web.</span><span class="sxs-lookup"><span data-stu-id="a47a6-121">The list is regularly updated in response to user and website developer requests to have websites added or removed.</span></span>  <span data-ttu-id="a47a6-122">Las actualizaciones de la lista se descargan automáticamente en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a47a6-122">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="a47a6-123">Envíe por correo electrónico la siguiente información a [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que su sitio web se agregue o se quite de la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="a47a6-123">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="a47a6-124">Nombre del propietario</span><span class="sxs-lookup"><span data-stu-id="a47a6-124">Owner name</span></span>  
*   <span data-ttu-id="a47a6-125">Título de la empresa</span><span class="sxs-lookup"><span data-stu-id="a47a6-125">Corporate title</span></span>  
*   <span data-ttu-id="a47a6-126">Dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="a47a6-126">Email address</span></span>  
*   <span data-ttu-id="a47a6-127">Nombre de la empresa</span><span class="sxs-lookup"><span data-stu-id="a47a6-127">Company name</span></span>  
*   <span data-ttu-id="a47a6-128">Dirección</span><span class="sxs-lookup"><span data-stu-id="a47a6-128">Street address</span></span>  
*   <span data-ttu-id="a47a6-129">Dirección del sitio web</span><span class="sxs-lookup"><span data-stu-id="a47a6-129">Website address</span></span>  
    
> [!NOTE]
> <span data-ttu-id="a47a6-130">La lista de compatibilidad de IE está diseñada para trabajar solo con sitios públicos.</span><span class="sxs-lookup"><span data-stu-id="a47a6-130">The IE compatibility list is designed to work with public sites only.</span></span>  

<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar un correo electrónico a ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Página de inicio oficial de Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Se necesita la lista de Microsoft Edge v1 XML Microsoft Edge"  
