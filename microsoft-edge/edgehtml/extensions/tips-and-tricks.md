---
description: Obtenga información sobre algunas sugerencias y trucos prácticos con respecto a las extensiones de Microsoft Edge
title: Sugerencias y trucos | Extensiones
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, web development, html, css, javascript, developer, extensions
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 8a5ea19152f5524d86d17d6f978c677c45f8f3a8
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399354"
---
# <a name="tips-and-tricks"></a><span data-ttu-id="5494b-104">Sugerencias y trucos</span><span class="sxs-lookup"><span data-stu-id="5494b-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="5494b-105">Tanto si está trabajando actualmente en una extensión de Microsoft Edge como si ya ha publicado una, las siguientes sugerencias y trucos pueden ser útiles.</span><span class="sxs-lookup"><span data-stu-id="5494b-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>  

## <a name="get-a-direct-link-to-your-extension-in-the-microsoft-store"></a><span data-ttu-id="5494b-106">Obtener un vínculo directo a la extensión en Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="5494b-106">Get a direct link to your extension in the Microsoft Store</span></span>  

<span data-ttu-id="5494b-107">En el panel del Centro de desarrollo de Windows, puedes encontrar un vínculo directo a tu extensión en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="5494b-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span>  <span data-ttu-id="5494b-108">Este vínculo puede ser útil para la publicidad y el uso compartido de la extensión.</span><span class="sxs-lookup"><span data-stu-id="5494b-108">This link can be useful for advertising and sharing out your extension.</span></span>  

<span data-ttu-id="5494b-109">Después de iniciar sesión en el Centro de desarrollo de Windows y navegar a la extensión a través del panel, en la página Identidad de la aplicación encontrarás el vínculo en la fila vínculo Protocolo de **la** Tienda:</span><span class="sxs-lookup"><span data-stu-id="5494b-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>  

![vínculo de protocolo de almacenamiento](./media/store-link.png)  
 
## <a name="make-sure-youre-following-the-microsoft-store-policy"></a><span data-ttu-id="5494b-111">Asegúrate de seguir la directiva de Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="5494b-111">Make sure you’re following the Microsoft Store Policy</span></span>  

<span data-ttu-id="5494b-112">Al crear la extensión, asegúrate de tener en cuenta las directrices para enviar a la Microsoft Store resaltadas en la [Directiva de Microsoft Store](/windows/uwp/publish/store-policies).</span><span class="sxs-lookup"><span data-stu-id="5494b-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](/windows/uwp/publish/store-policies).</span></span>  
 
<span data-ttu-id="5494b-113">Las extensiones de Microsoft Edge también tienen un conjunto adicional de directivas que se pueden [seguir](/windows/uwp/publish/store-policies#pol_10_12)aquí.</span><span class="sxs-lookup"><span data-stu-id="5494b-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](/windows/uwp/publish/store-policies#pol_10_12).</span></span>  

## <a name="improve-your-extensions-discoverability-in-the-microsoft-store"></a><span data-ttu-id="5494b-114">Mejorar la capacidad de destisibilidad de la extensión en Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="5494b-114">Improve your extension’s discoverability in the Microsoft Store</span></span>  

<span data-ttu-id="5494b-115">Puede agregar palabras clave al envío de extensión para mejorar su capacidad de destecciones a través de búsquedas.</span><span class="sxs-lookup"><span data-stu-id="5494b-115">You can add keywords to your extension submission to improve its discoverability through searches.</span></span>  <span data-ttu-id="5494b-116">Por ejemplo, `Microsoft Edge Extensions` y `name of my extension` .</span><span class="sxs-lookup"><span data-stu-id="5494b-116">For example, `Microsoft Edge Extensions` and `name of my extension`.</span></span>  

<span data-ttu-id="5494b-117">Esto se puede hacer en el Centro de desarrollo de Windows en la sección descripción de la extensión.</span><span class="sxs-lookup"><span data-stu-id="5494b-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span>  <span data-ttu-id="5494b-118">Estas palabras clave tendrán que agregarse para todos los idiomas que admita la extensión.</span><span class="sxs-lookup"><span data-stu-id="5494b-118">These keywords will need to be added for every language your extension supports.</span></span>  

![Usar palabras clave para enviar una respuesta a una revisión](./media/keywords.png)  

## <a name="automate-your-submission-to-the-microsoft-store"></a><span data-ttu-id="5494b-120">Automatizar el envío a Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="5494b-120">Automate your submission to the Microsoft Store</span></span>  

<span data-ttu-id="5494b-121">Puedes automatizar y simplificar los envíos a Microsoft Store mediante la nueva API de envío de Microsoft Store, que te permite actualizar aplicaciones/juegos, complementos \(compras desde la aplicación\) y paquetes de paquetes a través de una API de REST.</span><span class="sxs-lookup"><span data-stu-id="5494b-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons \(in-app purchases\), and package flights through a REST API.</span></span>  <span data-ttu-id="5494b-122">Consulte la documentación [y los ejemplos o](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) use la extensión [VSTS](https://github.com/Microsoft/windows-dev-center-vsts-extension) de la API de envío de código abierto para empezar.</span><span class="sxs-lookup"><span data-stu-id="5494b-122">Check out the [documentation and samples](/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>  

## <a name="use-the-windows-feedback-hub-to-gather-feedbackreviewsfeature-requests"></a><span data-ttu-id="5494b-123">Usar el Centro de opiniones de Windows para recopilar comentarios, opiniones y solicitudes de características</span><span class="sxs-lookup"><span data-stu-id="5494b-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>  

<span data-ttu-id="5494b-124">Puedes dirigir a los usuarios a la subcategoría Centro de opiniones de Windows para la extensión insertando un vínculo que apunta a ella.</span><span class="sxs-lookup"><span data-stu-id="5494b-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span>  <span data-ttu-id="5494b-125">Este vínculo tendrá que crearse con el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="5494b-125">This link will need to be created using the following format:</span></span>  

```text
feedback-hub://?tabid=2&appid=<PFN>!App
```  

<span data-ttu-id="5494b-126">Tendrá que sustituir por `<PFN>` el nombre de familia del paquete de su extensión.</span><span class="sxs-lookup"><span data-stu-id="5494b-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span>  <span data-ttu-id="5494b-127">Esto se puede encontrar en la **sección Identidad de** la aplicación para tu extensión en el Centro de desarrollo de Windows.</span><span class="sxs-lookup"><span data-stu-id="5494b-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>  

## <a name="check-out-your-ratings-and-reviews"></a><span data-ttu-id="5494b-128">Echa un vistazo a tus clasificaciones y opiniones</span><span class="sxs-lookup"><span data-stu-id="5494b-128">Check out your ratings and reviews</span></span>  

<span data-ttu-id="5494b-129">Inicie sesión con regularidad para comprobar las opiniones y clasificaciones de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="5494b-129">Log in regularly to check your user reviews and ratings.</span></span>  <span data-ttu-id="5494b-130">Aunque la aplicación para UWP solo tendrá información sobre el mercado de usuarios actual, al iniciar sesión en el Centro de desarrollo de Windows se mostrará una clasificación promedio en todos los mercados.</span><span class="sxs-lookup"><span data-stu-id="5494b-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>  

## <a name="respond-to-user-reviews"></a><span data-ttu-id="5494b-131">Responder a las opiniones de los usuarios</span><span class="sxs-lookup"><span data-stu-id="5494b-131">Respond to user reviews</span></span>  

<span data-ttu-id="5494b-132">Puedes responder a las opiniones de los usuarios en la Microsoft Store a través del panel del Centro de desarrollo de Windows.</span><span class="sxs-lookup"><span data-stu-id="5494b-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span>  <span data-ttu-id="5494b-133">Vaya a la extensión y, en Análisis, seleccione **Revisiones**.</span><span class="sxs-lookup"><span data-stu-id="5494b-133">Navigate to your extension and under Analytics select **Reviews**.</span></span>  <span data-ttu-id="5494b-134">Debajo de cada revisión aparecerá un vínculo que le permitirá responder directamente al cliente.</span><span class="sxs-lookup"><span data-stu-id="5494b-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span>  <span data-ttu-id="5494b-135">Este canal de comunicación le permite ofrecer comentarios, resoluciones o enviar un agradecimiento por la revisión.</span><span class="sxs-lookup"><span data-stu-id="5494b-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>  

![Responder a la revisión del usuario](./media/reviews.png)  
