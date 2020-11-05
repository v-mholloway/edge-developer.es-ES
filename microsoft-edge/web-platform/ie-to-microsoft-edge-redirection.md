---
description: Mover usuarios a Microsoft Edge desde Internet Explorer
title: Mover usuarios a Microsoft Edge desde Internet Explorer
author: MSEdgeTeam
ms.date: 11/04/2020
ms.author: msedgedevrel
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilidad, plataforma web, Internet Explorer
ms.openlocfilehash: 48f0f4121fb444d80603dcbb408397679c64753d
ms.sourcegitcommit: 7b4441b7656c8317139650f904b70cc87797d37e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "11154338"
---
# <span data-ttu-id="586cf-104">Mover usuarios a Microsoft Edge desde Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="586cf-104">Moving users to Microsoft Edge from Internet Explorer</span></span> 

<span data-ttu-id="586cf-105">Muchos sitios web modernos tienen diseños incompatibles con Internet Explorer \ (IE \).</span><span class="sxs-lookup"><span data-stu-id="586cf-105">Many modern websites have designs that are incompatible with Internet Explorer \(IE\).</span></span>  <span data-ttu-id="586cf-106">Cuando un usuario de IE visita un sitio web público incompatible, es posible que reciba un mensaje.</span><span class="sxs-lookup"><span data-stu-id="586cf-106">When an IE user visits an incompatible public website, the user may get a message.</span></span>  <span data-ttu-id="586cf-107">El mensaje indica que el sitio web es incompatible con el explorador.</span><span class="sxs-lookup"><span data-stu-id="586cf-107">The message states that the website is incompatible with the browser.</span></span>  <span data-ttu-id="586cf-108">Después de que se muestre el mensaje, se espera que el usuario cambie manualmente a un explorador moderno.</span><span class="sxs-lookup"><span data-stu-id="586cf-108">After the message is displayed, the user is expected to manually switch to a modern browser.</span></span>  <span data-ttu-id="586cf-109">Para minimizar las interrupciones, a partir de la versión 84, Microsoft Edge admite una nueva capacidad que redirige a los usuarios de forma automática.</span><span class="sxs-lookup"><span data-stu-id="586cf-109">To minimize disruptions, starting with version 84, Microsoft Edge supports a new capability that automatically redirects users.</span></span>  <span data-ttu-id="586cf-110">Cuando un usuario de IE navega a un sitio web que es incompatible con IE, Windows redirige automáticamente al usuario a Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="586cf-110">When an IE user navigates to a website that is incompatible with IE, Windows automatically redirects the user to Microsoft Edge.</span></span>  <span data-ttu-id="586cf-111">Para revisar los sitios web de la lista, vaya a [necesita una lista de Microsoft Edge][MicrosoftEdgeNeededgeV1].</span><span class="sxs-lookup"><span data-stu-id="586cf-111">To review the websites on the list, navigate to [Need Microsoft Edge list][MicrosoftEdgeNeededgeV1].</span></span>

<span data-ttu-id="586cf-112">En este artículo se describen los siguientes conceptos:</span><span class="sxs-lookup"><span data-stu-id="586cf-112">This article describes the following concepts.</span></span>  

*   <span data-ttu-id="586cf-113">La experiencia de usuario para el redireccionamiento</span><span class="sxs-lookup"><span data-stu-id="586cf-113">The user experience for redirection</span></span>  
*   <span data-ttu-id="586cf-114">Cómo agregar su sitio web a la lista de compatibilidad de IE</span><span class="sxs-lookup"><span data-stu-id="586cf-114">How to add your website to the IE compatibility list</span></span>  
*   <span data-ttu-id="586cf-115">Cómo quitar su sitio web de la lista de compatibilidad de IE</span><span class="sxs-lookup"><span data-stu-id="586cf-115">How to remove your website from the IE compatibility list</span></span>  
    
## <span data-ttu-id="586cf-116">¿Por qué se agrega un sitio web a la lista de compatibilidad de IE?</span><span class="sxs-lookup"><span data-stu-id="586cf-116">Why is a website added to the IE compatibility list?</span></span>  

<span data-ttu-id="586cf-117">La lista de compatibilidad de IE solo agrega un sitio web cuando se producen las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="586cf-117">The IE compatibility List only adds a website when the following actions occur.</span></span>  

*   <span data-ttu-id="586cf-118">Muestra un usuario de IE un mensaje que sugiere que el usuario debe usar un explorador diferente por razones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="586cf-118">Shows an IE user a message suggesting the user should use a different browser for compatibility reasons.</span></span>  
*   <span data-ttu-id="586cf-119">Solicitudes de propietario para agregar el sitio web a la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="586cf-119">Owner requests to add the website to the IE compatibility list.</span></span>  
    
## <span data-ttu-id="586cf-120">Actualizar la lista de compatibilidad de IE</span><span class="sxs-lookup"><span data-stu-id="586cf-120">Update the IE compatibility list</span></span>  

<span data-ttu-id="586cf-121">La lista de compatibilidad de IE es un archivo XML en [Microsoft.com][MicrosoftOfficialHome].</span><span class="sxs-lookup"><span data-stu-id="586cf-121">The IE compatibility list is an XML file on [microsoft.com][MicrosoftOfficialHome].</span></span>  <span data-ttu-id="586cf-122">La lista se actualiza regularmente en respuesta a las solicitudes de los programadores de los usuarios y sitios web para agregar o quitar sitios Web.</span><span class="sxs-lookup"><span data-stu-id="586cf-122">The list is regularly updated in response to user's and website developers requests to have websites added or removed.</span></span>  <span data-ttu-id="586cf-123">Las actualizaciones de la lista se descargan automáticamente en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="586cf-123">Updates to the list are automatically downloaded to user machines.</span></span>  

<span data-ttu-id="586cf-124">Envíe por correo electrónico la siguiente información a [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] para que su sitio web se agregue o se quite de la lista de compatibilidad de IE.</span><span class="sxs-lookup"><span data-stu-id="586cf-124">Email the following information to [ietoedge@microsoft.com][MailtoMicrosoftIetoedge] for your website to be added or removed from the IE compatibility list.</span></span>    

*   <span data-ttu-id="586cf-125">Nombre del propietario</span><span class="sxs-lookup"><span data-stu-id="586cf-125">Owner name</span></span>  
*   <span data-ttu-id="586cf-126">Título de la empresa</span><span class="sxs-lookup"><span data-stu-id="586cf-126">Corporate title</span></span>  
*   <span data-ttu-id="586cf-127">Dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="586cf-127">Email address</span></span>  
*   <span data-ttu-id="586cf-128">Nombre de la empresa</span><span class="sxs-lookup"><span data-stu-id="586cf-128">Company name</span></span>  
*   <span data-ttu-id="586cf-129">Dirección</span><span class="sxs-lookup"><span data-stu-id="586cf-129">Street address</span></span>  
*   <span data-ttu-id="586cf-130">Dirección del sitio web</span><span class="sxs-lookup"><span data-stu-id="586cf-130">Website address</span></span>  
<!--  *   Telephone number  -->  
<!--  *   Target platform \(desktop, phone, Xbox\)  -->  
    
<!-- links -->  

[MailtoMicrosoftIetoedge]: mailto:ietoedge@microsoft.com "Enviar un correo electrónico a ietoedge@microsoft.com"  

[MicrosoftOfficialHome]: https://www.microsoft.com "Página de inicio oficial de Microsoft"  

[MicrosoftEdgeNeededgeV1]:  https://edge.microsoft.com/neededge/v1 "Se necesita la lista de Microsoft Edge v1 XML Microsoft Edge"  
