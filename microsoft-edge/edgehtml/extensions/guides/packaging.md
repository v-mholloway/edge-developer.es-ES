---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Más información sobre cómo empaquetar tu extensión.
title: 'Extensiones: empaquetado'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.date: 12/15/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0ea4d6a4450d47d116164fd8481fdfb0f79bd30b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "11236496"
---
# <span data-ttu-id="82cbc-104">Empaquetar las extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="82cbc-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="82cbc-105">Por eso, finalizaste la ampliación y estás listo para empaquetarla.</span><span class="sxs-lookup"><span data-stu-id="82cbc-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="82cbc-106">Es posible que se pregunte cuál es el procedimiento siguiente para obtener esta información en manos de posibles usuarios.</span><span class="sxs-lookup"><span data-stu-id="82cbc-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="82cbc-107">La finalidad de esta guía es enseñarle a hacerlo.</span><span class="sxs-lookup"><span data-stu-id="82cbc-107">This guide is intended to teach you how to do just that.</span></span>

<span data-ttu-id="82cbc-108">La guía de empaquetado de la extensión es completa, ya que cubre todo lo que necesita saber sobre el embalaje, incluso los detalles más precisos.</span><span class="sxs-lookup"><span data-stu-id="82cbc-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="82cbc-109">Si no deseas conocer todo lo que hay que saber sobre cómo empaquetar tu extensión, ya estás de suerte.</span><span class="sxs-lookup"><span data-stu-id="82cbc-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="82cbc-110">Hemos agregado compatibilidad con extensiones a ManifoldJS, una herramienta de código abierto Node.js que toma la mayoría de tus woess de embalaje.</span><span class="sxs-lookup"><span data-stu-id="82cbc-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>

> [!NOTE]
> <span data-ttu-id="82cbc-111">El envío de una extensión de Microsoft Edge a Microsoft Store es actualmente una función restringida.</span><span class="sxs-lookup"><span data-stu-id="82cbc-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="82cbc-112">Póngase en [contacto con nosotros](https://aka.ms/extension-request) con sus solicitudes para formar parte de Microsoft Store y le daremos una actualización futura.</span><span class="sxs-lookup"><span data-stu-id="82cbc-112">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>


<span data-ttu-id="82cbc-113">Usa el siguiente Resumen de proceso para diseñar la aventura de empaquetar.</span><span class="sxs-lookup"><span data-stu-id="82cbc-113">Use the process outline below to map out your packaging adventure!</span></span>


## [<span data-ttu-id="82cbc-114">Extensiones en el centro de desarrollo de Windows</span><span class="sxs-lookup"><span data-stu-id="82cbc-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)

<span data-ttu-id="82cbc-115">Independientemente del camino de creación de paquetes que elija, manual o ManifoldJS, el primer paso es registrarse para una cuenta de Windows Developer y reservar el nombre o los nombres de la extensión.</span><span class="sxs-lookup"><span data-stu-id="82cbc-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>

<span data-ttu-id="82cbc-116">Una vez que lo haya hecho, puede continuar con la [creación y la prueba de paquetes de extensión](./packaging/creating-and-testing-extension-packages.md) para obtener información sobre cómo se crean AppXs y empaquetar manualmente la extensión, o ir a la ruta de acceso más sencilla y saltarse a [usar ManifoldJS para empaquetar extensiones](./packaging/using-ManifoldJS-to-package-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="82cbc-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="82cbc-117">Una vez que haya llegado a nosotros y haya sido aprobado para tener su extensión en Microsoft Store, consulte la lista de [comprobación de envío](https://docs.microsoft.com/windows/uwp/publish/app-submissions)de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82cbc-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>


## [<span data-ttu-id="82cbc-118">Crear y probar paquetes de extensión</span><span class="sxs-lookup"><span data-stu-id="82cbc-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)

<span data-ttu-id="82cbc-119">En esta sección de la guía se recorre la creación de paquetes de extensión manual una vez [que haya configurado su cuenta de desarrollador de Windows y reservado los nombres de extensión](./packaging/extensions-in-the-windows-Dev-Center.md).</span><span class="sxs-lookup"><span data-stu-id="82cbc-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="82cbc-120">Si tienes curiosidad sobre los detalles más precisos de empaquetar una extensión, dales una lectura.</span><span class="sxs-lookup"><span data-stu-id="82cbc-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>

<span data-ttu-id="82cbc-121">También se incluye información sobre cómo [probar y desempaquetar una extensión empaquetada](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span><span class="sxs-lookup"><span data-stu-id="82cbc-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="82cbc-122">Esta información es relevante incluso si has salido de la ruta de empaquetado de ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="82cbc-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>

## [<span data-ttu-id="82cbc-123">Localizar paquetes de extensión</span><span class="sxs-lookup"><span data-stu-id="82cbc-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)
<span data-ttu-id="82cbc-124">El paso de localización del paquete se encuentra entre la creación de tu appxmanifest.xml archivo y el comando final para empaquetar tu extensión.</span><span class="sxs-lookup"><span data-stu-id="82cbc-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>
<span data-ttu-id="82cbc-125">Esto le permite indicar qué idiomas son compatibles con las extensiones en la descripción de Microsoft Store y en qué idioma aparece el nombre de la extensión en Windows.</span><span class="sxs-lookup"><span data-stu-id="82cbc-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>

<span data-ttu-id="82cbc-126">Puede saltar a [localizar el nombre y la descripción de Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) en esta sección de la guía si la extensión no es compatible con varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="82cbc-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>

## [<span data-ttu-id="82cbc-127">Usar ManifoldJS para empaquetar extensiones</span><span class="sxs-lookup"><span data-stu-id="82cbc-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)

<span data-ttu-id="82cbc-128">La ruta de la herramienta para embalar tu extensión, ManifoldJS empaquetará tu extensión en un instante con un esfuerzo mínimo para tu fin.</span><span class="sxs-lookup"><span data-stu-id="82cbc-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="82cbc-129">Proporciona algunos activos de Windows/Microsoft Store después de rellenar algunas propiedades de AppXManifest y tu extensión se empaquetará en un momento.</span><span class="sxs-lookup"><span data-stu-id="82cbc-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>

<span data-ttu-id="82cbc-130">Una vez empaquetada la extensión, consulte la sección de [pruebas](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) de creación y prueba de la extensión de Microsoft Edge para obtener información sobre cómo realizar la transferencia o desempaquetar.</span><span class="sxs-lookup"><span data-stu-id="82cbc-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>


## [<span data-ttu-id="82cbc-131">Ejecutar el kit para la certificación de aplicaciones en Windows</span><span class="sxs-lookup"><span data-stu-id="82cbc-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)

<span data-ttu-id="82cbc-132">Una vez que tenga una extensión empaquetada, puede ejecutarla a través del kit para la certificación de aplicaciones en Windows.</span><span class="sxs-lookup"><span data-stu-id="82cbc-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="82cbc-133">Al hacerlo, se ejecutará una serie de pruebas en el paquete de extensión para asegurarse de que esté listo para Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="82cbc-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>
