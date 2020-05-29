---
description: Proceso escalonado para publicar extensiones de Edge (cromo) en Microsoft Store.
title: Publicar una extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 7b5be511af1e81efd5da4fc4bc0691f317437f94
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607381"
---
# <span data-ttu-id="84de2-104">Publicar una extensión</span><span class="sxs-lookup"><span data-stu-id="84de2-104">Publish An Extension</span></span>  

<span data-ttu-id="84de2-105">Publicar la extensión en el catálogo de complementos de Microsoft Edge \ (complementos de Microsoft Edge \).</span><span class="sxs-lookup"><span data-stu-id="84de2-105">Publish your Extension on Microsoft Edge Addons catalog \(Microsoft Edge Addons\).</span></span>  <span data-ttu-id="84de2-106">Primero debes crear un envío en el [centro de Partners][MicrosoftPartnerCenter] y enviarlo.</span><span class="sxs-lookup"><span data-stu-id="84de2-106">You must first create a submission on [Partner Center][MicrosoftPartnerCenter] and submit it.</span></span>  <span data-ttu-id="84de2-107">En este documento se enumeran todos los detalles que debe proporcionar para crear un envío de extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-107">This document lists all the details that you must provide to create an Extension submission.</span></span>  

## <span data-ttu-id="84de2-108">Antes de empezar</span><span class="sxs-lookup"><span data-stu-id="84de2-108">Before You Begin</span></span>  

*   <span data-ttu-id="84de2-109">Debe tener una cuenta de desarrollador activa en el [centro de Partners][MicrosoftPartnerCenter] para enviar su extensión en los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84de2-109">You must have an active developer account on [Partner Center][MicrosoftPartnerCenter] to submit your Extension in Microsoft Edge Addons.</span></span>  <span data-ttu-id="84de2-110">Si no tiene una, [cree una nueva][MicrosoftPartnerCenter].</span><span class="sxs-lookup"><span data-stu-id="84de2-110">If you do not have one, [create a new developer account][MicrosoftPartnerCenter].</span></span>  
*   <span data-ttu-id="84de2-111">Cree un archivo zip de su paquete de extensión y asegúrese de que contiene estos archivos:</span><span class="sxs-lookup"><span data-stu-id="84de2-111">Create a zip file of your Extension package and ensure that it contains these files:</span></span>  
    *   <span data-ttu-id="84de2-112">El archivo de manifiesto y debe definir el nombre y la versión de la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-112">The manifest file and it must define the name and version of your Extension.</span></span>  
    *   <span data-ttu-id="84de2-113">Las imágenes y otros archivos necesarios para la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-113">The images and other files that are required for your Extension.</span></span>  


<span data-ttu-id="84de2-114">Si no ha empezado a crear una extensión, puede consultar el tutorial de [Introducción][ExtensionsGettingStarted] para crear una extensión de cromo de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84de2-114">If you have not started building an Extension, you may refer to the [Getting Started][ExtensionsGettingStarted] tutorial for building a Microsoft Edge Chromium extension.</span></span>  

<span data-ttu-id="84de2-115">Para crear un envío de extensión en el [centro de Partners][MicrosoftPartnerCenter], siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="84de2-115">To create an Extension submission on [Partner Center][MicrosoftPartnerCenter], follow these steps.</span></span>  

## <span data-ttu-id="84de2-116">Paso 1: iniciar una nueva presentación</span><span class="sxs-lookup"><span data-stu-id="84de2-116">Step 1: Start a New Submission</span></span>  

<span data-ttu-id="84de2-117">Vaya a su [Panel de programadores][MicrosoftPartnerCenter].</span><span class="sxs-lookup"><span data-stu-id="84de2-117">Go to your [developer dashboard][MicrosoftPartnerCenter].</span></span>  <span data-ttu-id="84de2-118">En la página Descripción general, haga clic en **crear nueva extensión**.</span><span class="sxs-lookup"><span data-stu-id="84de2-118">From the Overview page, click **Create new extension**.</span></span>  

## <span data-ttu-id="84de2-119">Paso 2: cargar el archivo zip de extensión</span><span class="sxs-lookup"><span data-stu-id="84de2-119">Step 2: Upload Your Extension Zip File</span></span>  

<span data-ttu-id="84de2-120">La página del **paquete** es el lugar donde se carga el archivo zip para el envío de la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-120">The **Package** page is where you upload the zip file for your Extension submission.</span></span>  <span data-ttu-id="84de2-121">Solo puedes cargar un paquete a la vez, por lo que si la extensión no está completa, puedes cargar un paquete de trabajo en progreso y actualizarlo en cualquier momento antes de publicarlo.</span><span class="sxs-lookup"><span data-stu-id="84de2-121">You may only upload one package at a time, so if your Extension is not complete you may upload a work-in-progress package and update at any time before you publish it.</span></span>  <span data-ttu-id="84de2-122">Asegúrese de que el paquete contiene el `manifest.json` archivo y de que funciona correctamente en Microsoft Edge antes de cargarlo.</span><span class="sxs-lookup"><span data-stu-id="84de2-122">Be sure that your package contains the `manifest.json` file and is working fine on Microsoft Edge prior to uploading.</span></span>  
<span data-ttu-id="84de2-123">Cargue el paquete arrastrándolo al campo cargar o seleccionando **examinar los archivos**.</span><span class="sxs-lookup"><span data-stu-id="84de2-123">Upload the package by dragging it into the upload field or by selecting **Browse your files**.</span></span>  <span data-ttu-id="84de2-124">La página Package valida el archivo zip Extensions y muestra el **Estado de éxito o error de la carga**.</span><span class="sxs-lookup"><span data-stu-id="84de2-124">The Package page validates the Extensions zip file and displays that **success or failure status of your upload**.</span></span>  <span data-ttu-id="84de2-125">Si el paquete supera la validación; se cargó correctamente y verá un mensaje de éxito.</span><span class="sxs-lookup"><span data-stu-id="84de2-125">If the package passes validation; it is uploaded successfully and you see a success message.</span></span>  <span data-ttu-id="84de2-126">Si se produce un error de validación en el paquete; el paquete no se acepta y se muestra un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="84de2-126">If the package fails validation; the package is not accepted and you see an error message.</span></span>  <span data-ttu-id="84de2-127">Si hay errores en el paquete, solucione los problemas e intente cargarlo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="84de2-127">If there are errors in the package, resolve the issues and try uploading it again.</span></span>  

<span data-ttu-id="84de2-128">Después de cargar correctamente, revise los detalles de la extensión y haga clic en **siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="84de2-128">After successful upload, review your Extension details and click **Next** to proceed.</span></span>  

## <span data-ttu-id="84de2-129">Paso 3: proporcionar detalles de disponibilidad</span><span class="sxs-lookup"><span data-stu-id="84de2-129">Step 3: Provide Availability details</span></span>  

### <span data-ttu-id="84de2-130">Definir la visibilidad</span><span class="sxs-lookup"><span data-stu-id="84de2-130">Define Visibility</span></span>  

<span data-ttu-id="84de2-131">Seleccione una opción de **visibilidad** para definir la audiencia que puede descubrir y adquirir la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-131">Select a **Visibility** option to define the audience who may discover and acquire your Extension.</span></span>  <span data-ttu-id="84de2-132">Esto le da la opción de especificar si los usuarios deben buscar su extensión en los complementos de Microsoft Edge o ver el listado.</span><span class="sxs-lookup"><span data-stu-id="84de2-132">This gives you the option to specify whether users should find your Extension in Microsoft Edge Addons or see the listing at all.</span></span>  <span data-ttu-id="84de2-133">En este momento, tiene dos opciones en visibilidad:</span><span class="sxs-lookup"><span data-stu-id="84de2-133">Currently, you have two options under visibility:</span></span>  

*   `Public`  
    <span data-ttu-id="84de2-134">Esta es la opción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="84de2-134">This is the default option.</span></span>  
    <span data-ttu-id="84de2-135">Si seleccionas `Public` , tu extensión estará disponible y podrá ser detectada para todos los usuarios de los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84de2-135">If you select `Public`, your Extension is available and discoverable to everyone in Microsoft Edge Addons.</span></span>  <span data-ttu-id="84de2-136">Deje esta opción seleccionada si quiere que la extensión aparezca en complementos de Microsoft Edge para que los usuarios la encuentren a través de la búsqueda, la navegación y el vínculo directo de su extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-136">Leave this option selected if you want your Extension to be listed in Microsoft Edge Addons for users to find via searching, browsing, and the direct link of your Extension.</span></span>  

*   `Hidden`  
    <span data-ttu-id="84de2-137">Si selecciona `Hidden` , la extensión quedará oculta en los complementos de Microsoft Edge de los usuarios que busquen o exploren; debe compartir la dirección URL de su registro para distribuir la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-137">If you select `Hidden`, your Extension is hidden in Microsoft Edge Addons from users searching or browsing; you must share your listing URL to distribute your Extension.</span></span>  <span data-ttu-id="84de2-138">Los usuarios que tienen el vínculo directo al listado pueden descargarlo en Microsoft Edge \ (es posible que encuentres la URL de tu anuncio en la página de **Descripción general** de la extensión del envío de la extensión \).</span><span class="sxs-lookup"><span data-stu-id="84de2-138">Users who have the direct link to the listing may download it on Microsoft Edge \(you may find your listing URL under **Extension Overview** page of Extension submission\).</span></span>  

> [!NOTE]
> <span data-ttu-id="84de2-139">Si envía una extensión como **pública** y la cambia posteriormente a **privada**, los usuarios que instalaron la extensión cuando ésta era pública siguen teniendo acceso y recibirán futuras actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="84de2-139">If you submit an Extension as **Public** and later change it to **Private**, Users who installed the Extension when it was public continue to have access and receive future updates.</span></span>  

### <span data-ttu-id="84de2-140">Definir mercados</span><span class="sxs-lookup"><span data-stu-id="84de2-140">Define markets</span></span>  

<span data-ttu-id="84de2-141">Debe definir los mercados específicos en los que está ofreciendo la extensión, seleccione **Mostrar opciones** en la sección **mercados** de la página **disponibilidad** .</span><span class="sxs-lookup"><span data-stu-id="84de2-141">You must define the specific markets in which you are offering your Extension, select **Show options** in the **Markets** section on the **Availability** page.</span></span>  <span data-ttu-id="84de2-142">Se muestra la ventana emergente de selección de mercado, donde deberías elegir los mercados.</span><span class="sxs-lookup"><span data-stu-id="84de2-142">The Market selection pop-up window is displayed, where you should choose the markets.</span></span>  <span data-ttu-id="84de2-143">De forma predeterminada, se seleccionan todos los mercados, incluidos los **mercados futuros** que se pueden añadir más adelante.</span><span class="sxs-lookup"><span data-stu-id="84de2-143">By default, all markets are selected, including any **future markets** that may be added later.</span></span>  <span data-ttu-id="84de2-144">Puede anular la selección de cada uno de los mercados para excluirlos, o puede hacer clic en **anular selección** y, después, agregar mercados individuales de su elección.</span><span class="sxs-lookup"><span data-stu-id="84de2-144">You may deselect individual markets to exclude them, or you may click **Unselect all** and then add individual markets of your choice.</span></span>  

> [!NOTE]
> <span data-ttu-id="84de2-145">Si los usuarios ya tienen su extensión en un mercado determinado y después lo quita, los usuarios que ya tienen la extensión en ese mercado pueden continuar utilizándolo, pero no obtienen las actualizaciones posteriores que envíe.</span><span class="sxs-lookup"><span data-stu-id="84de2-145">If users already have your Extension in a certain market, and you later remove that market, users who already has the Extension in that market may continue to use it, but they do not get the later updates you submit.</span></span>  

<span data-ttu-id="84de2-146">Haga clic en **Guardar** para ir a la sección de **propiedades** .</span><span class="sxs-lookup"><span data-stu-id="84de2-146">Click **Save** to proceed to **Properties** section.</span></span>  

## <span data-ttu-id="84de2-147">Paso 4: seleccionar las propiedades de la extensión</span><span class="sxs-lookup"><span data-stu-id="84de2-147">Step 4: Select Properties for Your Extension</span></span>  

### <span data-ttu-id="84de2-148">Propiedades de extensión</span><span class="sxs-lookup"><span data-stu-id="84de2-148">Extension properties</span></span>  

*   [<span data-ttu-id="84de2-149">Categoría</span><span class="sxs-lookup"><span data-stu-id="84de2-149">Category</span></span>](#category)  
*   [<span data-ttu-id="84de2-150">Requisitos de la política de privacidad</span><span class="sxs-lookup"><span data-stu-id="84de2-150">Privacy policy requirements</span></span>](#privacy-policy-requirements)  
*   [<span data-ttu-id="84de2-151">Dirección URL de la directiva de privacidad</span><span class="sxs-lookup"><span data-stu-id="84de2-151">Privacy policy URL</span></span>](#privacy-policy-url)  
*   [<span data-ttu-id="84de2-152">Dirección URL del sitio web</span><span class="sxs-lookup"><span data-stu-id="84de2-152">Website URL</span></span>](#website-url)  
*   [<span data-ttu-id="84de2-153">Dirección URL de soporte/dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="84de2-153">Support URL/email address</span></span>](#support-urlemail-address)  
*   [<span data-ttu-id="84de2-154">Clasificación de extensión</span><span class="sxs-lookup"><span data-stu-id="84de2-154">Extension Rating</span></span>](#extension-rating)  

#### <span data-ttu-id="84de2-155">Categoría</span><span class="sxs-lookup"><span data-stu-id="84de2-155">Category</span></span>  

<span data-ttu-id="84de2-156">El listado de tu extensión en la categoría adecuada ayuda a los usuarios a encontrar tu extensión fácilmente y a entender más acerca de ella.</span><span class="sxs-lookup"><span data-stu-id="84de2-156">Listing your Extension in the right category helps users find your Extension easily and understand more about it.</span></span>  <span data-ttu-id="84de2-157">Seleccione la categoría que mejor describa la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-157">Select a Category that best describes your Extension.</span></span>  

<span data-ttu-id="84de2-158">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-158">**Possible Values**:</span></span>  

*   `Accessibility`  
*   `Blogging`  
*   `Developer Tools`  
*   `Fun`  
*   `News & Weather`  
*   `Photos`  
*   `Productivity`  
*   `Search Tools`  
*   `Shopping`  
*   `Social & Communication`  
*   `Sports`  

#### <span data-ttu-id="84de2-159">Requisitos de la política de privacidad</span><span class="sxs-lookup"><span data-stu-id="84de2-159">Privacy policy requirements</span></span>  

<span data-ttu-id="84de2-160">Indique si su extensión accede, recopila o transmite cualquier tipo de información personal.</span><span class="sxs-lookup"><span data-stu-id="84de2-160">Indicate whether your Extension accesses, collects, or transmits any personal information.</span></span>  

> [!NOTE]
> <span data-ttu-id="84de2-161">Si tu extensión requiere una política de privacidad y no proporcionaste ninguna, tu envío puede dar error de certificación.</span><span class="sxs-lookup"><span data-stu-id="84de2-161">If your Extension requires a privacy policy and you have not provided one, your submission may fail certification.</span></span>  

<span data-ttu-id="84de2-162">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-162">**Possible Values**:</span></span>  

*   `No`<span data-ttu-id="84de2-163">: Una dirección URL de política de privacidad es opcional.</span><span class="sxs-lookup"><span data-stu-id="84de2-163">:  A privacy policy URL is optional.</span></span>  
*   `Yes`<span data-ttu-id="84de2-164">: Es necesaria una dirección URL de política de privacidad.</span><span class="sxs-lookup"><span data-stu-id="84de2-164">:  A privacy policy URL is required.</span></span>  

#### <span data-ttu-id="84de2-165">Dirección URL de la directiva de privacidad</span><span class="sxs-lookup"><span data-stu-id="84de2-165">Privacy policy URL</span></span>  

<span data-ttu-id="84de2-166">Usted es responsable de asegurar que su extensión cumpla con las leyes y regulaciones de privacidad, y para proporcionar una URL de política de privacidad válida, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="84de2-166">You are responsible for ensuring your Extension complies with privacy laws and regulations, and for providing a valid privacy policy URL, if required.</span></span>  <span data-ttu-id="84de2-167">Debe proporcionar una URL de política de privacidad Si su extensión accede, transmite o recopila toda la información personal.</span><span class="sxs-lookup"><span data-stu-id="84de2-167">You must provide a privacy policy URL if any personal information is being accessed, transmitted, or collected by your Extension.</span></span>  
<span data-ttu-id="84de2-168">Para determinar si su extensión requiere una política de privacidad, revise el [contrato para desarrolladores de Microsoft Edge][MicrosoftAppDeveloperAgreement] y el [documento directivas para desarrolladores de catálogos de Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="84de2-168">To determine if your Extension requires a privacy policy, review the [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement] and the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="84de2-169">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-169">**Possible Values**:</span></span>  

*   `{url}`  

#### <span data-ttu-id="84de2-170">Dirección URL del sitio web</span><span class="sxs-lookup"><span data-stu-id="84de2-170">Website URL</span></span>  

<span data-ttu-id="84de2-171">Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="84de2-171">This property is Optional.</span></span>  
<span data-ttu-id="84de2-172">Dirección URL de la Página Web de la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-172">The URL of the web page for your Extension.</span></span>  <span data-ttu-id="84de2-173">Esta dirección URL debe apuntar a una página de su propio sitio web, no a la lista de sitios web para su extensión en los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84de2-173">This URL must point to a page on your own website, not the web listing for your Extension in Microsoft Edge Addons.</span></span>  

<span data-ttu-id="84de2-174">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-174">**Possible Values**:</span></span>  

*   `{url}`  

#### <span data-ttu-id="84de2-175">Dirección URL de soporte/dirección de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="84de2-175">Support URL/email address</span></span>  

<span data-ttu-id="84de2-176">Esta propiedad es opcional.</span><span class="sxs-lookup"><span data-stu-id="84de2-176">This property is Optional.</span></span>  
<span data-ttu-id="84de2-177">La dirección URL de la página web en la que los usuarios van por soporte técnico con la extensión o una dirección de correo electrónico para ponerse en contacto con usted para obtener asistencia.</span><span class="sxs-lookup"><span data-stu-id="84de2-177">The URL of the web page where users go for support with your Extension, or an email address to contact you for support.</span></span>  <span data-ttu-id="84de2-178">Incluye información de soporte técnico para todos los recibos, de modo que los usuarios sepan cómo obtener asistencia de usted.</span><span class="sxs-lookup"><span data-stu-id="84de2-178">You include support information for all submissions, so that your users know how to get support from you.</span></span>  

<span data-ttu-id="84de2-179">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-179">**Possible Values**:</span></span>  

*   `{email_address}`  
*   `{url}`  

#### <span data-ttu-id="84de2-180">Clasificación de extensión</span><span class="sxs-lookup"><span data-stu-id="84de2-180">Extension Rating</span></span>  

<span data-ttu-id="84de2-181">La clasificación de extensión nos ayuda a determinar la edad del público objetivo de tu extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-181">Extension rating helps us determine the age of the target audience of your Extension.</span></span>  
<span data-ttu-id="84de2-182">Para ayudarle a determinar si las extensiones tienen un contenido adulto, revise el [documento Microsoft Edge addons Catalog Policies][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="84de2-182">To help you determine if your Extensions has a mature content, review the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="84de2-183">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-183">**Possible Values**:</span></span>  

*   <span data-ttu-id="84de2-184">Adultos \ (casilla de verificación \): Active esta casilla si su extensión contiene algún contenido maduro.</span><span class="sxs-lookup"><span data-stu-id="84de2-184">Mature \(checkbox\): Check this box if your Extension contains any mature content.</span></span>  <span data-ttu-id="84de2-185">Si seleccionas adultos para tu extensión, tu registro estará disponible con una etiqueta independiente para indicar que la extensión contiene contenido para adultos.</span><span class="sxs-lookup"><span data-stu-id="84de2-185">If you select mature for your Extension, your listing is available with a separate tag to indicate that the Extension contains mature content.</span></span>  

<span data-ttu-id="84de2-186">Haz clic en **Guardar** para ir a la sección de inscripción.</span><span class="sxs-lookup"><span data-stu-id="84de2-186">Click **Save** to proceed to listing section.</span></span>  

## <span data-ttu-id="84de2-187">Paso 5: agregar información de registros para la extensión</span><span class="sxs-lookup"><span data-stu-id="84de2-187">Step 5: Add Listings Information for Your Extension</span></span>  

<span data-ttu-id="84de2-188">Esta es la información que los usuarios ven al ver el listado en los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84de2-188">This is the information that users see when viewing your listing in Microsoft Edge Addons.</span></span>  <span data-ttu-id="84de2-189">Muchos de los campos de un registro son opcionales, pero sugerimos proporcionar la mayor cantidad de información posible para hacer que su registro destaque.  El mínimo requerido para que tu registro en los complementos de Microsoft Edge se considere completo es la [Descripción de texto](#description), el [logotipo de extensión](#store-logo)y el [pequeño mosaico promocional](#small-promotional-tile) en cada idioma mencionado en el paquete de extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-189">Many of the fields in a listing are optional, but we suggest providing as much information as possible to make your listing stand out.  The minimum required for your listing in Microsoft Edge Addons to be considered complete is the [text description](#description), [Extension logo](#store-logo), and [small promotional tile](#small-promotional-tile) in each language mentioned in your Extension package.</span></span>  

### <span data-ttu-id="84de2-190">Campos de descripción de la tienda</span><span class="sxs-lookup"><span data-stu-id="84de2-190">Store Listing fields</span></span>  

*   [<span data-ttu-id="84de2-191">Idiomas de la descripción de la Store</span><span class="sxs-lookup"><span data-stu-id="84de2-191">Store listing languages</span></span>](#store-listing-languages)  
*   [<span data-ttu-id="84de2-192">Nombre para mostrar de la tienda</span><span class="sxs-lookup"><span data-stu-id="84de2-192">Store display name</span></span>](#store-display-name)  
*   [<span data-ttu-id="84de2-193">Descripción</span><span class="sxs-lookup"><span data-stu-id="84de2-193">Description</span></span>](#description)  
*   [<span data-ttu-id="84de2-194">Logotipo de la tienda</span><span class="sxs-lookup"><span data-stu-id="84de2-194">Store logo</span></span>](#store-logo)  
*   [<span data-ttu-id="84de2-195">Pequeño mosaico promocional</span><span class="sxs-lookup"><span data-stu-id="84de2-195">Small promotional tile</span></span>](#small-promotional-tile)  
*   [<span data-ttu-id="84de2-196">Multimedia</span><span class="sxs-lookup"><span data-stu-id="84de2-196">Media</span></span>](#media)  
*   [<span data-ttu-id="84de2-197">Descripción corta</span><span class="sxs-lookup"><span data-stu-id="84de2-197">Short description</span></span>](#short-description)  
*   [<span data-ttu-id="84de2-198">Términos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="84de2-198">Search terms</span></span>](#search-terms)  

#### <span data-ttu-id="84de2-199">Idiomas de la descripción de la Store</span><span class="sxs-lookup"><span data-stu-id="84de2-199">Store listing languages</span></span>  

<span data-ttu-id="84de2-200">Si tu paquete de extensión admite varios idiomas, tu extensión debe tener una página de registro para cada uno.</span><span class="sxs-lookup"><span data-stu-id="84de2-200">If your Extension package supports multiple languages, your Extension must have a listing page for each one.</span></span>  
<span data-ttu-id="84de2-201">Debe completar los detalles de la lista \ (Descripción de texto, imágenes, etc.) para cada idioma por separado, incluso si usa el mismo contenido para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="84de2-201">You must complete listing details \(text description, images, and so on\) for each language separately even if you are using the same content for each language.</span></span>  <span data-ttu-id="84de2-202">Si tu extensión está localizada en más de un idioma, esos idiomas se mostrarán en la página de la parte superior de la lista.</span><span class="sxs-lookup"><span data-stu-id="84de2-202">If your Extension is localized in more than one language, those languages are displayed at the top of listing page.</span></span>  

1.  <span data-ttu-id="84de2-203">Seleccione cualquier nombre de idioma en la lista desplegable **idiomas** .</span><span class="sxs-lookup"><span data-stu-id="84de2-203">Select any one language name from **Languages** drop-down list.</span></span>  
1.  <span data-ttu-id="84de2-204">Rellene los detalles del registro.</span><span class="sxs-lookup"><span data-stu-id="84de2-204">Fill the listing details.</span></span>  
1.  <span data-ttu-id="84de2-205">Haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="84de2-205">Click **Save**.</span></span>  
1.  <span data-ttu-id="84de2-206">Repita el procedimiento para todos los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="84de2-206">Repeat for all of your supported languages.</span></span>  

> [!NOTE]
> <span data-ttu-id="84de2-207">Para agregar o quitar idiomas para su registro en los complementos de Microsoft Edge, debe modificar la lista de idiomas admitidos por el paquete de extensión y volver a cargarlo.</span><span class="sxs-lookup"><span data-stu-id="84de2-207">To add or remove languages for your listing in Microsoft Edge Addons, you must modify the list of languages supported by your Extension package and re-upload it.</span></span>  

<span data-ttu-id="84de2-208">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-208">**Possible Values**:</span></span>  

*   `English (United States)`<span data-ttu-id="84de2-209">: Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="84de2-209">:  This is the default value.</span></span>  <span data-ttu-id="84de2-210">Si no menciona ningún idioma en su paquete, establecemos el idioma predeterminado en inglés \ (Estados Unidos \) y debe proporcionar un registro en inglés \ (Estados Unidos \).</span><span class="sxs-lookup"><span data-stu-id="84de2-210">If you do not mention any language in your package, we set your default language to English \(United States\) and you must provide a listing in English \(United States\).</span></span>  
*   `{language}` <span data-ttu-id="84de2-211">\(`{Country}`\)</span><span class="sxs-lookup"><span data-stu-id="84de2-211">\(`{Country}`\)</span></span>  

#### <span data-ttu-id="84de2-212">Nombre para mostrar de la tienda</span><span class="sxs-lookup"><span data-stu-id="84de2-212">Store display name</span></span>  

<span data-ttu-id="84de2-213">El nombre de la extensión según se indica en el manifiesto del paquete de extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-213">The name of Extension as mentioned in your Extension package manifest.</span></span>  

> [!NOTE]
> <span data-ttu-id="84de2-214">Para editar el nombre, debe actualizar el manifiesto en el paquete de extensión y volver a cargarlo.</span><span class="sxs-lookup"><span data-stu-id="84de2-214">To edit the name, you must update the manifest in your Extension package and re-upload it.</span></span>  

#### <span data-ttu-id="84de2-215">Descripción</span><span class="sxs-lookup"><span data-stu-id="84de2-215">Description</span></span>  

<span data-ttu-id="84de2-216">Este campo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="84de2-216">This field is required.</span></span>  
<span data-ttu-id="84de2-217">La descripción de los usuarios de lo que hace la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-217">The description for your users of what your Extension does.</span></span>  

<span data-ttu-id="84de2-218">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-218">**Possible Values**:</span></span>  

*   <span data-ttu-id="84de2-219">{plain_text}: menos de 10.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="84de2-219">{plain_text}: Less than 10,000 characters.</span></span>  

#### <span data-ttu-id="84de2-220">Logotipo de la tienda</span><span class="sxs-lookup"><span data-stu-id="84de2-220">Store logo</span></span>  

<span data-ttu-id="84de2-221">Este campo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="84de2-221">This field is required.</span></span>  
<span data-ttu-id="84de2-222">Una imagen de 1:1 para tu logotipo de extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-222">A 1:1 image for your Extension logo.</span></span>  

<span data-ttu-id="84de2-223">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-223">**Possible Values**:</span></span>  

*   <span data-ttu-id="84de2-224">128px x 128px, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="84de2-224">128px x 128px, PNG \(.png\)</span></span>  
*   <span data-ttu-id="84de2-225">150px x 140px, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="84de2-225">150px x 140px, PNG \(.png\)</span></span>  
*   <span data-ttu-id="84de2-226">300px x 300px, PNG \ (. png \): el tamaño recomendado.</span><span class="sxs-lookup"><span data-stu-id="84de2-226">300px x 300px, PNG \(.png\):  The recommended size.</span></span>  

#### <span data-ttu-id="84de2-227">Pequeño mosaico promocional</span><span class="sxs-lookup"><span data-stu-id="84de2-227">Small promotional tile</span></span>  

<span data-ttu-id="84de2-228">Este campo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="84de2-228">This field is required.</span></span>  
<span data-ttu-id="84de2-229">Un mosaico promocional de tamaño pequeño.</span><span class="sxs-lookup"><span data-stu-id="84de2-229">A small size promotional tile.</span></span>  <span data-ttu-id="84de2-230">Tu registro se muestra en este icono.</span><span class="sxs-lookup"><span data-stu-id="84de2-230">Your listing is displayed on this tile.</span></span>  

<span data-ttu-id="84de2-231">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-231">**Possible Values**:</span></span>  

*   <span data-ttu-id="84de2-232">440px x 280x, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="84de2-232">440px x 280x, PNG \(.png\)</span></span>  

#### <span data-ttu-id="84de2-233">Multimedia</span><span class="sxs-lookup"><span data-stu-id="84de2-233">Media</span></span>  

<span data-ttu-id="84de2-234">Este campo es opcional.</span><span class="sxs-lookup"><span data-stu-id="84de2-234">This field is optional.</span></span>  
<span data-ttu-id="84de2-235">Debes proporcionar estos activos para ayudar a mostrar tu producto de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="84de2-235">You should provide these assets to help display your product more effectively.</span></span>  

*   <span data-ttu-id="84de2-236">Capturas de pantalla</span><span class="sxs-lookup"><span data-stu-id="84de2-236">Screenshots</span></span>  
    <span data-ttu-id="84de2-237">Las imágenes de la extensión que describen lo que hace la extensión.</span><span class="sxs-lookup"><span data-stu-id="84de2-237">The images of your Extension that describe what your Extension does.</span></span>  
    
*   <span data-ttu-id="84de2-238">Iconos de promoción grandes</span><span class="sxs-lookup"><span data-stu-id="84de2-238">Large promotion tiles</span></span>  
    <span data-ttu-id="84de2-239">Un gran mosaico promocional para que sea más destacado en los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84de2-239">A large promotional tile to be feature your Extension more prominently in Microsoft Edge Addons.</span></span>  
    
*   <span data-ttu-id="84de2-240">Dirección URL de vídeo de YouTube</span><span class="sxs-lookup"><span data-stu-id="84de2-240">YouTube video URL</span></span>  
    <span data-ttu-id="84de2-241">Una [dirección URL de vídeo de YouTube válida para la extensión][MicrosoftEdgeAddonsUploadYouTubeVideo].</span><span class="sxs-lookup"><span data-stu-id="84de2-241">A valid [YouTube video URL for your Extension][MicrosoftEdgeAddonsUploadYouTubeVideo].</span></span>  <span data-ttu-id="84de2-242">El video debe ser de buena calidad y longitud mínima.</span><span class="sxs-lookup"><span data-stu-id="84de2-242">Your video should be good quality and minimal length.</span></span>  <span data-ttu-id="84de2-243">El vídeo de YouTube debe superar la certificación antes de publicar su extensión en los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84de2-243">Your YouTube video must pass certification before publishing your Extension in Microsoft Edge Addons.</span></span>  <span data-ttu-id="84de2-244">Compruebe que el vídeo de YouTube cumple con el [documento de directivas para desarrolladores de catálogos de Microsoft Edge addons][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="84de2-244">Verify that your YouTube video complies with the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="84de2-245">**Valores posibles**:</span><span class="sxs-lookup"><span data-stu-id="84de2-245">**Possible Values**:</span></span>  

*   <span data-ttu-id="84de2-246">10 capturas de pantallas como máximo.</span><span class="sxs-lookup"><span data-stu-id="84de2-246">10 Screenshots maximum.</span></span>  
    *   <span data-ttu-id="84de2-247">640px x 480px, PNG \ (. png \): capturas de pantallas.</span><span class="sxs-lookup"><span data-stu-id="84de2-247">640px x 480px, PNG \(.png\):  Screenshots.</span></span>  
    *   <span data-ttu-id="84de2-248">1280px x 800px, PNG \ (. png \): capturas de pantallas.</span><span class="sxs-lookup"><span data-stu-id="84de2-248">1280px x 800px, PNG \(.png\):  Screenshots.</span></span>  
*   <span data-ttu-id="84de2-249">1400px x 560px, PNG \ (. png \): mosaicos de promoción grandes.</span><span class="sxs-lookup"><span data-stu-id="84de2-249">1400px x 560px, PNG \(.png\):  Large promotion tiles.</span></span>  
*   <span data-ttu-id="84de2-250">60 segundos o más corto y 2GB o menos, dirección URL de vídeo de YouTube.</span><span class="sxs-lookup"><span data-stu-id="84de2-250">60 seconds or shorter and 2GB or smaller, YouTube video URL.</span></span>  

#### <span data-ttu-id="84de2-251">Descripción corta</span><span class="sxs-lookup"><span data-stu-id="84de2-251">Short description</span></span>  

<span data-ttu-id="84de2-252">Una descripción breve y breve que se puede usar en la parte superior de la lista de productos.</span><span class="sxs-lookup"><span data-stu-id="84de2-252">A short, catchy description that may be used at the top of the listing for your product.</span></span>  <span data-ttu-id="84de2-253">Si no se proporciona, se usan las primeras líneas de la descripción más larga.</span><span class="sxs-lookup"><span data-stu-id="84de2-253">If not provided, the first few lines from your longer description are used instead.</span></span>  <span data-ttu-id="84de2-254">Debido a que tu descripción también aparece debajo de este texto, debes proporcionar una breve descripción con distintos textos para que el registro sea menos repetitivo.</span><span class="sxs-lookup"><span data-stu-id="84de2-254">Because your description also appears below this text, you should provide a short description with different text so that your listing is less repetitive.</span></span>  <span data-ttu-id="84de2-255">La descripción breve de tu extensión se selecciona directamente desde el archivo de manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="84de2-255">The Short description of your Extension is picked directly from the manifest file of your package.</span></span>  

> [!NOTE]
> <span data-ttu-id="84de2-256">Para modificar la descripción breve, debe actualizar el manifiesto en el paquete de extensión y volver a cargarla.</span><span class="sxs-lookup"><span data-stu-id="84de2-256">To edit the short description, you must update the manifest in your Extension package and re-upload it.</span></span>  

#### <span data-ttu-id="84de2-257">Términos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="84de2-257">Search terms</span></span>  

<span data-ttu-id="84de2-258">Los términos de búsqueda son palabras individuales o frases cortas que no se muestran a los usuarios, pero ayudan a que la extensión se pueda detectar en los complementos de Microsoft Edge cuando los usuarios buscan las condiciones.</span><span class="sxs-lookup"><span data-stu-id="84de2-258">Search terms are single words or short phrases that are not displayed to users but help make your Extension discoverable in Microsoft Edge Addons when users search using those terms.</span></span>  

<span data-ttu-id="84de2-259">**Requisitos**:</span><span class="sxs-lookup"><span data-stu-id="84de2-259">**Requirements**:</span></span>  

*   <span data-ttu-id="84de2-260">7 o menos términos de búsqueda</span><span class="sxs-lookup"><span data-stu-id="84de2-260">7 or fewer search terms</span></span>  
*   <span data-ttu-id="84de2-261">30 o menos caracteres por término de búsqueda</span><span class="sxs-lookup"><span data-stu-id="84de2-261">30 or fewer characters per search term</span></span>  
*   <span data-ttu-id="84de2-262">21 o menos palabras para los términos de búsqueda combinados</span><span class="sxs-lookup"><span data-stu-id="84de2-262">21 or fewer words for combined search terms</span></span>  

<span data-ttu-id="84de2-263">Haz clic en **Guardar** para continuar con la sección guardar la lista.</span><span class="sxs-lookup"><span data-stu-id="84de2-263">Click **Save** to proceed to save your listing section.</span></span>  <span data-ttu-id="84de2-264">Haga clic en **publicar** para proporcionar detalles de presentación.</span><span class="sxs-lookup"><span data-stu-id="84de2-264">Click **Publish** to provide submission details.</span></span>  

## <span data-ttu-id="84de2-265">Paso 6: completar el envío y hacer clic en publicar</span><span class="sxs-lookup"><span data-stu-id="84de2-265">Step 6: Complete your submission and click Publish</span></span>  

<span data-ttu-id="84de2-266">En la página de opciones de envío del proceso de envío de extensión se proporciona más información para ayudarnos a probar el producto correctamente.</span><span class="sxs-lookup"><span data-stu-id="84de2-266">The Submission options page of the Extension submission process is where you provide more information to help us test your product properly.</span></span>  <span data-ttu-id="84de2-267">Este paso es opcional, pero se recomienda para muchos supuestos.</span><span class="sxs-lookup"><span data-stu-id="84de2-267">This is an optional step, but it is recommended for many submissions.</span></span>  

### <span data-ttu-id="84de2-268">Opciones de suspensión de publicación</span><span class="sxs-lookup"><span data-stu-id="84de2-268">Publishing hold options</span></span>  

<span data-ttu-id="84de2-269">De forma predeterminada, tu envío se publicará tan pronto como pase la certificación.</span><span class="sxs-lookup"><span data-stu-id="84de2-269">By default, your submission is published as soon as it passes certification.</span></span>  <span data-ttu-id="84de2-270">Puede optar por suspender la presentación hasta una fecha específica.</span><span class="sxs-lookup"><span data-stu-id="84de2-270">You may choose to place a hold on publishing your submission until a specific date.</span></span>  <span data-ttu-id="84de2-271">A continuación se describen las opciones de esta sección.</span><span class="sxs-lookup"><span data-stu-id="84de2-271">The options in this section are described below.</span></span>  

*   **<span data-ttu-id="84de2-272">Publicar el envío tan pronto como pase la certificación</span><span class="sxs-lookup"><span data-stu-id="84de2-272">Publish your submission as soon as it passes certification</span></span>**  

    <span data-ttu-id="84de2-273">Esta es la selección predeterminada.</span><span class="sxs-lookup"><span data-stu-id="84de2-273">This is the default selection.</span></span>  <span data-ttu-id="84de2-274">Significa que su envío comienza el proceso de publicación tan pronto como pase la certificación</span><span class="sxs-lookup"><span data-stu-id="84de2-274">It means that your submission begins the publishing process as soon as it passes certification</span></span>  

*   **<span data-ttu-id="84de2-275">Empezar a publicar el envío en una fecha determinada</span><span class="sxs-lookup"><span data-stu-id="84de2-275">Start publishing your submission on a certain date</span></span>**  

    <span data-ttu-id="84de2-276">Elija **empezar a publicar su presentación en una fecha determinada** para asegurarse de que el envío no se publique hasta una fecha específica.</span><span class="sxs-lookup"><span data-stu-id="84de2-276">Choose **Start publishing your submission on a certain date** to ensure that the submission is not published until a specific date.</span></span>  <span data-ttu-id="84de2-277">Con esta opción, tu envío se lanzará tan pronto como sea posible en la fecha que especifiques o después de ella.</span><span class="sxs-lookup"><span data-stu-id="84de2-277">With this option, your submission is released as soon as possible on or after the date you specify.</span></span>  <span data-ttu-id="84de2-278">La fecha debe ser al menos 24 horas después del momento actual.</span><span class="sxs-lookup"><span data-stu-id="84de2-278">The date must be at least 24 hours in the future.</span></span>  <span data-ttu-id="84de2-279">Además de la fecha, puedes especificar la hora a la que debe comenzar a publicarse el envío.</span><span class="sxs-lookup"><span data-stu-id="84de2-279">Along with the date, you may specify the time at which the submission should begin to be published.</span></span>  

### <span data-ttu-id="84de2-280">Notas para la certificación</span><span class="sxs-lookup"><span data-stu-id="84de2-280">Notes for certification</span></span>  

<span data-ttu-id="84de2-281">A medida que envíe la extensión, tendrá la opción de usar la página notas para el certificado para proporcionar información adicional a los evaluadores de certificación.</span><span class="sxs-lookup"><span data-stu-id="84de2-281">As you submit your Extension, you have the option to use the Notes for certification page to provide additional information to the certification testers.</span></span>  <span data-ttu-id="84de2-282">Esta información ayuda a garantizar que tu extensión se pruebe correctamente.</span><span class="sxs-lookup"><span data-stu-id="84de2-282">This information helps ensure that your Extension is tested correctly.</span></span>  <span data-ttu-id="84de2-283">Si no podemos probar completamente su envío, es posible que se produzca un error de certificación.</span><span class="sxs-lookup"><span data-stu-id="84de2-283">If we are not able to fully test your submission, it may fail certification.</span></span>  

<span data-ttu-id="84de2-284">Asegúrese de incluir el siguiente \ (si corresponde a la extensión \):</span><span class="sxs-lookup"><span data-stu-id="84de2-284">Make sure to include the following \(if applicable for your Extension\):</span></span>  

*   <span data-ttu-id="84de2-285">Nombres de usuario y contraseñas para cuentas de prueba.</span><span class="sxs-lookup"><span data-stu-id="84de2-285">User names and passwords for test accounts.</span></span>  
*   <span data-ttu-id="84de2-286">Pasos para tener acceso a las características ocultas o bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="84de2-286">Steps to access hidden or locked features.</span></span>  
*   <span data-ttu-id="84de2-287">Se esperaban diferencias en el comportamiento según la configuración regional o de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="84de2-287">Expected differences in behavior based on region or other user settings.</span></span>  
*   <span data-ttu-id="84de2-288">Información sobre lo que ha cambiado en una actualización de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="84de2-288">Information about what changed in an app update.</span></span>  
*   <span data-ttu-id="84de2-289">Todo lo que cree que los evaluadores debe conocer sobre su envío.</span><span class="sxs-lookup"><span data-stu-id="84de2-289">Anything else you think testers must understand about your submission.</span></span>  

<span data-ttu-id="84de2-290">Después de completar los detalles anteriores, haga clic en **publicar** para enviar la extensión en los complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="84de2-290">After completing the above details, click **Publish** to submit your Extension in Microsoft Edge Addons.</span></span>  

<span data-ttu-id="84de2-291">Cuando haya terminado de crear el envío para su extensión y haga clic en **publicar**, el envío entra en el paso de certificación.</span><span class="sxs-lookup"><span data-stu-id="84de2-291">When you finish creating the submission for your Extension and click **Publish**, the submission enters the certification step.</span></span>  <span data-ttu-id="84de2-292">Este proceso generalmente se completa dentro de un par de días, aunque en algunos casos puede demorar hasta 7 días hábiles.</span><span class="sxs-lookup"><span data-stu-id="84de2-292">This process usually is completed within a couple of days, though in some cases it may take up to 7 business days.</span></span>  <span data-ttu-id="84de2-293">Una vez que el envío pase la certificación, su extensión se publicará en los complementos de Microsoft Edge, a menos que haya seleccionado las opciones de conservación de publicaciones para especificar que no se debe liberar hasta una fecha determinada.</span><span class="sxs-lookup"><span data-stu-id="84de2-293">After your submission passes certification, your Extension is published in Microsoft Edge Addons unless you selected the Publishing hold options to specify that it should not be released until a certain date.</span></span>  <span data-ttu-id="84de2-294">Recibirá una notificación cuando se publique el envío y el estado de la extensión en el panel cambiará a `In the Store` .</span><span class="sxs-lookup"><span data-stu-id="84de2-294">You are notified when your submission is published, and the status of your Extension in the dashboard changes to `In the Store`.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Introducción a las extensiones de Microsoft Edge \ (cromo \) | Microsoft docs"  

[MicrosoftEdgeAddonsUploadYouTubeVideo]: ./upload-video.md "Cargar un vídeo de YouTube | Microsoft docs"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Directivas para desarrolladores de catálogos de Microsoft Edge addons | Microsoft docs"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Acuerdo de desarrollador de aplicaciones | Microsoft docs"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de socios"  
