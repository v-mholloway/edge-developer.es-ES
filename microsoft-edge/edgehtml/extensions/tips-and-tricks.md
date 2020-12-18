---
description: Más información sobre algunas sugerencias y trucos prácticos relacionados con las extensiones de Microsoft Edge
title: Sugerencias y trucos | Prórroga
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador, extensiones
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd512085f13b76c5a8e474301ef296612eeb0414
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236124"
---
# <span data-ttu-id="9e5d5-104">Sugerencias y trucos</span><span class="sxs-lookup"><span data-stu-id="9e5d5-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="9e5d5-105">Si está trabajando en una extensión de Microsoft Edge o ya ha publicado una, es posible que las siguientes sugerencias y trucos sean útiles.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>

## <span data-ttu-id="9e5d5-106">Obtener un vínculo directo a su extensión en Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="9e5d5-106">Get a direct link to your extension in the Microsoft Store</span></span>

<span data-ttu-id="9e5d5-107">En el panel del centro de desarrollo de Windows, puede encontrar un vínculo directo a su extensión en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span> <span data-ttu-id="9e5d5-108">Este vínculo puede ser útil para anunciar y compartir tu extensión.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-108">This link can be useful for advertising and sharing out your extension.</span></span>

<span data-ttu-id="9e5d5-109">Después de iniciar sesión en el centro de desarrollo de Windows y navegar hasta la extensión a través del panel, en la página identidad de la aplicación encontrará el vínculo en la fila **vínculo de protocolo del almacén** :</span><span class="sxs-lookup"><span data-stu-id="9e5d5-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>

![vínculo de protocolo de tienda](./media/store-link.png)
 
## <span data-ttu-id="9e5d5-111">Asegúrese de estar siguiendo la Directiva de Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="9e5d5-111">Make sure you’re following the Microsoft Store Policy</span></span>

<span data-ttu-id="9e5d5-112">Al crear la extensión, asegúrese de tener en cuenta las pautas para enviar a Microsoft Store resaltadas en la [Directiva Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e5d5-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span></span> 
 
<span data-ttu-id="9e5d5-113">Las extensiones de Microsoft Edge también tienen un conjunto adicional de directivas que puede seguir [aquí](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span><span class="sxs-lookup"><span data-stu-id="9e5d5-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span></span>

## <span data-ttu-id="9e5d5-114">Mejorar la detección de extensiones en Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="9e5d5-114">Improve your extension’s discoverability in the Microsoft Store</span></span>

<span data-ttu-id="9e5d5-115">Puede agregar palabras clave a su envío de extensión para mejorar su descubrimiento a través de las búsquedas.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-115">You can add keywords to your extension submission to improve its discoverability through searches.</span></span> <span data-ttu-id="9e5d5-116">Por ejemplo, "extensiones de Microsoft Edge" y "nombre de mi extensión".</span><span class="sxs-lookup"><span data-stu-id="9e5d5-116">For example, "Microsoft Edge Extensions" and "name of my extension".</span></span> 

<span data-ttu-id="9e5d5-117">Esto puede hacerse en el centro de desarrollo de Windows, debajo de la sección de descripción de su extensión.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span> <span data-ttu-id="9e5d5-118">Estas palabras clave deberán agregarse para cada idioma que admita la extensión.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-118">These keywords will need to be added for every language your extension supports.</span></span>

![Enviar una respuesta a una revisión: Palabras clave](./media/keywords.png)

## <span data-ttu-id="9e5d5-120">Automatizar el envío a Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="9e5d5-120">Automate your submission to the Microsoft Store</span></span>

<span data-ttu-id="9e5d5-121">Puede automatizar y simplificar los envíos a Microsoft Store mediante la nueva API de envío de Microsoft Store, que le permite actualizar aplicaciones/juegos, complementos (compras desde la aplicación) y paquetes piloto a través de una API de REST.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons (in-app purchases), and package flights through a REST API.</span></span> <span data-ttu-id="9e5d5-122">Consulte la [documentación y las muestras](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) o use la extensión Open Source [Transmission API VSTS](https://github.com/Microsoft/windows-dev-center-vsts-extension) para comenzar.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-122">Check out the [documentation and samples](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>

## <span data-ttu-id="9e5d5-123">Usar el centro de opiniones de Windows para recopilar comentarios/críticas/solicitudes de características</span><span class="sxs-lookup"><span data-stu-id="9e5d5-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>

<span data-ttu-id="9e5d5-124">Puede dirigir a los usuarios a la subcategoría concentrador de comentarios de Windows para su extensión incrustando un vínculo que apunte a él.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span> <span data-ttu-id="9e5d5-125">Este vínculo tendrá que crearse con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="9e5d5-125">This link will need to be created using the following format:</span></span> 

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

<span data-ttu-id="9e5d5-126">Deberás sustituirlo `<PFN>` por el nombre de familia de paquetes de la extensión.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span> <span data-ttu-id="9e5d5-127">Puedes encontrarla en la sección identidad de la **aplicación** para tu extensión en el centro de desarrollo de Windows.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>

## <span data-ttu-id="9e5d5-128">Consulta tus calificaciones y opiniones</span><span class="sxs-lookup"><span data-stu-id="9e5d5-128">Check out your ratings and reviews</span></span>

<span data-ttu-id="9e5d5-129">Inicie sesión regularmente para comprobar las revisiones y las calificaciones de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-129">Log in regularly to check your user reviews and ratings.</span></span> <span data-ttu-id="9e5d5-130">Si bien la aplicación para UWP solo tendrá información sobre el mercado del usuario actual, al iniciar sesión en el centro de desarrollo de Windows se mostrará la calificación promedio en todos los mercados.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>

## <span data-ttu-id="9e5d5-131">Responder a las opiniones de los usuarios</span><span class="sxs-lookup"><span data-stu-id="9e5d5-131">Respond to user reviews</span></span>

<span data-ttu-id="9e5d5-132">Puede responder a las opiniones de los usuarios en Microsoft Store a través del panel del centro de desarrollo de Windows.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span> <span data-ttu-id="9e5d5-133">Vaya a la extensión y, en Analytics, seleccione **Recomentarioss**.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-133">Navigate to your extension and under Analytics select **Reviews**.</span></span> <span data-ttu-id="9e5d5-134">Debajo de cada opinión, aparecerá un vínculo que le permitirá responder directamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span> <span data-ttu-id="9e5d5-135">Este canal de comunicación le permite ofrecer comentarios, soluciones o enviar una agradecimiento por la revisión.</span><span class="sxs-lookup"><span data-stu-id="9e5d5-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>

![Enviar una respuesta a una opinión](./media/reviews.png)
