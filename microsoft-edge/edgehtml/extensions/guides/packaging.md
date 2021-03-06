---
description: Obtenga información sobre cómo empaquetar la extensión .
title: 'Extensiones: empaquetado'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
keywords: edge, web development, html, css, javascript, developer
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62c7858c38cf0c06e24c25938a885b10b391fd8f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398500"
---
# <a name="packaging-microsoft-edge-extensions"></a><span data-ttu-id="654fa-104">Empaquetar extensiones de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="654fa-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="654fa-105">Por lo tanto, por fin ha completado la extensión y está listo para empaquetar.</span><span class="sxs-lookup"><span data-stu-id="654fa-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="654fa-106">Es posible que se pregunte cuáles son los pasos siguientes para obtener esto en manos de los usuarios potenciales.</span><span class="sxs-lookup"><span data-stu-id="654fa-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="654fa-107">Esta guía está diseñada para enseñarte a hacerlo.</span><span class="sxs-lookup"><span data-stu-id="654fa-107">This guide is intended to teach you how to do just that.</span></span>  

<span data-ttu-id="654fa-108">La guía de empaquetado de extensiones es completa, ya que cubre todo lo que quieres saber sobre el empaquetado, incluso los detalles más finos y ingeniosos.</span><span class="sxs-lookup"><span data-stu-id="654fa-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="654fa-109">Si no quieres aprender todo lo que hay que saber sobre empaquetar la extensión, tienes suerte.</span><span class="sxs-lookup"><span data-stu-id="654fa-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="654fa-110">Hemos agregado compatibilidad con extensiones a ManifoldJS, una herramienta de código Node.js de código abierto que quita la mayoría de los problemas de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="654fa-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>  

> [!NOTE]
> <span data-ttu-id="654fa-111">Enviar una extensión de Microsoft Edge a la Microsoft Store es actualmente una funcionalidad restringida.</span><span class="sxs-lookup"><span data-stu-id="654fa-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="654fa-112">[Llámenos con](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) sus solicitudes para formar parte de Microsoft Store y le consideraremos para una actualización futura.</span><span class="sxs-lookup"><span data-stu-id="654fa-112">[Reach out to us](https://developer.microsoft.com/en-us/microsoft-edge/extensions/requests) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>  

<span data-ttu-id="654fa-113">Usa el esquema de proceso siguiente para asignar la aventura de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="654fa-113">Use the process outline below to map out your packaging adventure!</span></span>  

## [<a name="extensions-in-the-windows-dev-center"></a><span data-ttu-id="654fa-114">Extensiones en el centro de desarrollo de Windows</span><span class="sxs-lookup"><span data-stu-id="654fa-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)  

<span data-ttu-id="654fa-115">Independientemente de la ruta de creación de paquetes que elijas, manual o ManifoldJS, el primer paso es registrarte para una cuenta de Desarrollador de Windows y reservar los nombres de la extensión.</span><span class="sxs-lookup"><span data-stu-id="654fa-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>  

<span data-ttu-id="654fa-116">Una vez hecho esto, puede pasar [](./packaging/creating-and-testing-extension-packages.md) a Crear y probar paquetes de extensión para obtener información sobre cómo se crean los AppX y empaquetan manualmente la extensión, o bien ir a la ruta más fácil y saltar a [Usar ManifoldJS](./packaging/using-ManifoldJS-to-package-extensions.md)para empaquetar extensiones .</span><span class="sxs-lookup"><span data-stu-id="654fa-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>  

> [!NOTE]
> <span data-ttu-id="654fa-117">Una vez que te hayas puesto en contacto con nosotros y hayas recibido la aprobación para tener la extensión en microsoft Store, consulta la lista de comprobación [de envío de aplicaciones](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span><span class="sxs-lookup"><span data-stu-id="654fa-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>  


## [<a name="creating-and-testing-extension-packages"></a><span data-ttu-id="654fa-118">Crear y probar paquetes de extensión</span><span class="sxs-lookup"><span data-stu-id="654fa-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)  

<span data-ttu-id="654fa-119">En esta sección de la guía se muestra la creación manual de paquetes de extensión una vez que hayas configurado tu cuenta de Desarrollador de Windows y reservados los nombres de [extensión.](./packaging/extensions-in-the-windows-Dev-Center.md)</span><span class="sxs-lookup"><span data-stu-id="654fa-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="654fa-120">Si tienes curiosidad por los detalles más finos de empaquetar una extensión, dale una lectura.</span><span class="sxs-lookup"><span data-stu-id="654fa-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>  

<span data-ttu-id="654fa-121">También se incluye información sobre cómo [probar y desempaquetar una extensión empaquetada.](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package)</span><span class="sxs-lookup"><span data-stu-id="654fa-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="654fa-122">Esta información es relevante incluso si has pasado la ruta de empaquetado manifoldJS.</span><span class="sxs-lookup"><span data-stu-id="654fa-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>  

## [<a name="localizing-extension-packages"></a><span data-ttu-id="654fa-123">Localizar paquetes de extensión</span><span class="sxs-lookup"><span data-stu-id="654fa-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)  

<span data-ttu-id="654fa-124">El paso de localización del paquete se encuentra entre crear el archivo appxmanifest.xml y ejecutar el comando final para empaquetar la extensión.</span><span class="sxs-lookup"><span data-stu-id="654fa-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>  
<span data-ttu-id="654fa-125">Esto te permite indicar qué idiomas admiten tus extensiones en la descripción de Microsoft Store y qué idioma aparece el nombre de la extensión en Windows.</span><span class="sxs-lookup"><span data-stu-id="654fa-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>  

<span data-ttu-id="654fa-126">Puedes ir a [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) en esta sección de la guía si la extensión no admite varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="654fa-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>  

## [<a name="using-manifoldjs-to-package-extensions"></a><span data-ttu-id="654fa-127">Usar ManifoldJS para empaquetar extensiones</span><span class="sxs-lookup"><span data-stu-id="654fa-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)  

<span data-ttu-id="654fa-128">La ruta de herramientas para empaquetar la extensión, ManifoldJS empaquetará la extensión en un instante con el mínimo esfuerzo en el extremo.</span><span class="sxs-lookup"><span data-stu-id="654fa-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="654fa-129">Proporciona algunos activos de Windows/Microsoft Store después de rellenar algunas propiedades de AppXManifest y la extensión se empaquetará en poco tiempo.</span><span class="sxs-lookup"><span data-stu-id="654fa-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>  

<span data-ttu-id="654fa-130">Una vez empaquetada la [](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) extensión, consulta la sección de pruebas de Crear y probar la extensión de Microsoft Edge para obtener información sobre cómo descargarla o desempaquetarla.</span><span class="sxs-lookup"><span data-stu-id="654fa-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>  

## [<a name="running-the-windows-app-certification-kit"></a><span data-ttu-id="654fa-131">Ejecutar el kit para la certificación de aplicaciones en Windows</span><span class="sxs-lookup"><span data-stu-id="654fa-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)  

<span data-ttu-id="654fa-132">Una vez que tenga una extensión empaquetada, puede ejecutarla a través del Kit de certificación de aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="654fa-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="654fa-133">Al hacerlo, se ejecutarán varias pruebas en el paquete de extensión para asegurarse de que está listo para la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="654fa-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>  
