---
description: Hacer que tu PWA sea más reconocible publicando en Microsoft Store
title: Publicar la aplicación web progresiva en Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 5e78e909187408566219ffe80779bb9221b585fa
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "11527085"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a><span data-ttu-id="0711d-104">Publicar la aplicación web progresiva en Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="0711d-104">Publish your Progressive Web App to the Microsoft Store</span></span>  

<span data-ttu-id="0711d-105">Publicar la aplicación web progresiva \(PWA\) en [Microsoft Store][WindowsUwpPublishIndex] ofrece las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="0711d-105">Publishing your Progressive Web App \(PWA\) to the [Microsoft Store][WindowsUwpPublishIndex] brings the following advantages.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="0711d-106">Detectabilidad</span><span class="sxs-lookup"><span data-stu-id="0711d-106">Discoverability</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="0711d-107">Los usuarios buscan aplicaciones de forma natural en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-107">Users naturally look for apps in the app store.</span></span>  <span data-ttu-id="0711d-108">Cuando publicas en Microsoft Store, millones de usuarios de Windows pueden descubrir tu PWA junto con otras aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="0711d-108">When you publish to the Microsoft Store, millions of Windows users may discover your PWA alongside other Windows apps.</span></span>  <span data-ttu-id="0711d-109">La Tienda muestra aplicaciones a través de categorías, colecciones curadas y mucho más.</span><span class="sxs-lookup"><span data-stu-id="0711d-109">The Store showcases apps through categories, curated collections, and more.</span></span>  <span data-ttu-id="0711d-110">Los portales de detección de aplicaciones proporcionan una experiencia de exploración y compra fácil para los posibles usuarios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0711d-110">The app discovery portals provide an easy browsing and shopping experience for potential users of your app.</span></span>  <span data-ttu-id="0711d-111">Incluso puedes mejorar [la descripción de la Tienda][WindowsUwpPublishAppScreenshotsImages] con capturas de pantalla, una imagen de héroe y tráileres de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0711d-111">You may even [enhance your Store listing][WindowsUwpPublishAppScreenshotsImages] with screenshots, a hero image, and video trailers.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="0711d-112">Fiabilidad</span><span class="sxs-lookup"><span data-stu-id="0711d-112">Trustworthiness</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="0711d-113">Los clientes de Windows saben que pueden confiar en sus compras y descargas de Microsoft Store, ya que se adhieren a los rigurosos estándares de calidad [y seguridad de][LegalWindowsAgreementsStorePolicies]Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0711d-113">Windows customers know they may trust their Microsoft Store purchases and downloads, because they adhere to the rigorous Microsoft [quality and safety standards][LegalWindowsAgreementsStorePolicies].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="0711d-114">Instalación sencilla</span><span class="sxs-lookup"><span data-stu-id="0711d-114">Easy install</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="0711d-115">La Microsoft Store proporciona una experiencia de instalación coherente y fácil de usar en [todas las aplicaciones de Windows 10.][MicrosoftStoreAppsWindows]</span><span class="sxs-lookup"><span data-stu-id="0711d-115">The Microsoft Store provides a consistent and user-friendly install experience across [all Windows 10 apps][MicrosoftStoreAppsWindows].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="0711d-116">Análisis de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="0711d-116">App analytics</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="0711d-117">El [panel del Centro de partners de Windows][WindowsUwpPublishIndex] te proporciona análisis [detallados][WindowsUwpPublishAnalytics] sobre el estado de la aplicación, el uso y mucho más.</span><span class="sxs-lookup"><span data-stu-id="0711d-117">The [Windows Partner Center dashboard][WindowsUwpPublishIndex] provides you with [detailed analytics][WindowsUwpPublishAnalytics] about your app health, usage, and more.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="0711d-118">Para publicar tu PWA en Microsoft Store, no es necesario realizar cambios en el código.</span><span class="sxs-lookup"><span data-stu-id="0711d-118">To publish your PWA to the Microsoft Store, no code changes are required.</span></span>  <span data-ttu-id="0711d-119">En su lugar, creas una reserva de aplicación, empaquetas tu PWA y envías el paquete a la Tienda.</span><span class="sxs-lookup"><span data-stu-id="0711d-119">Instead, you create an app reservation, package your PWA, and submit your package to the Store.</span></span>  <span data-ttu-id="0711d-120">En las secciones siguientes se explican los pasos.</span><span class="sxs-lookup"><span data-stu-id="0711d-120">The following sections explain the steps.</span></span>   

## <a name="create-an-app-reservation"></a><span data-ttu-id="0711d-121">Crear una reserva de aplicación</span><span class="sxs-lookup"><span data-stu-id="0711d-121">Create an app reservation</span></span>  

<span data-ttu-id="0711d-122">[El Centro de partners de Windows][MicrosoftPartnerDashboardWindowsOverview] es el centro para que envíes la aplicación a la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="0711d-122">[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] is the hub for you to submit your app to the Microsoft Store.</span></span>  

<span data-ttu-id="0711d-123">Para crear una reserva de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-123">To create an app reservation, complete the following actions.</span></span>  

1.  <span data-ttu-id="0711d-124">Para mostrar los programas inscritos, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-124">To display your enrolled programs, complete the following actions.</span></span>  
    1.  <span data-ttu-id="0711d-125">Inicie sesión en el Centro de partners de Windows con su cuenta microsoft y vaya al [Panel del Centro de partners.][MicrosoftPartnerDashboardHome]</span><span class="sxs-lookup"><span data-stu-id="0711d-125">Sign into Windows Partner Center with your Microsoft account and navigate to the [Partner Center Dashboard][MicrosoftPartnerDashboardHome].</span></span>  
    1.  <span data-ttu-id="0711d-126">Navegar a **Windows & Xbox**</span><span class="sxs-lookup"><span data-stu-id="0711d-126">Navigate to **Windows & Xbox**</span></span>  
        *   <span data-ttu-id="0711d-127">Si se muestra & Xbox de **Windows,** la aplicación ya está registrada.</span><span class="sxs-lookup"><span data-stu-id="0711d-127">If **Windows & Xbox** is displayed, your app is already enrolled.</span></span>  
        *   <span data-ttu-id="0711d-128">Si **Windows & xbox** no se muestra, elige Agregar **programa**.</span><span class="sxs-lookup"><span data-stu-id="0711d-128">If **Windows & Xbox** isn't displayed, choose **Add program**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Agregar un programa en el panel del Centro de partners de Windows" lightbox="./media/windows-partner-center-add-program.msft.png":::
       <span data-ttu-id="0711d-130">Agregar un programa en el panel del Centro de partners de Windows</span><span class="sxs-lookup"><span data-stu-id="0711d-130">Add a program in the Windows Partner Center dashboard</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="0711d-131">Para inscribirse en el programa de desarrolladores, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-131">To enroll in the developer program, complete the following actions.</span></span>  
    1.  <span data-ttu-id="0711d-132">Navega a **Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="0711d-132">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="0711d-133">Elija **Introducción**.</span><span class="sxs-lookup"><span data-stu-id="0711d-133">Choose **Get started**.</span></span>  
    1.  <span data-ttu-id="0711d-134">Sigue las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-134">Follow the prompts.</span></span>  
1.  <span data-ttu-id="0711d-135">Ahora, tu cuenta está inscrita en el programa para desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-135">Now, your account is enrolled in the app developer program.</span></span> <span data-ttu-id="0711d-136">Para crear una reserva de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-136">To create an app reservation, complete the following actions.</span></span>  
    1.  <span data-ttu-id="0711d-137">Navega a **Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="0711d-137">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="0711d-138">Elija **Información general**Crear una nueva  >  **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="0711d-138">Choose **Overview** > **Create a new app**.</span></span>  
    1.  <span data-ttu-id="0711d-139">Escriba el nombre de la aplicación en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="0711d-139">Type the name of your app in the prompt.</span></span>  
    1.  <span data-ttu-id="0711d-140">Elija `Reserve product name` .</span><span class="sxs-lookup"><span data-stu-id="0711d-140">Choose `Reserve product name`.</span></span>  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Crear una reserva de aplicación en el Centro de partners de Windows" lightbox="./media/windows-partner-center-create-app.msft.png":::
       <span data-ttu-id="0711d-142">Crear una reserva de aplicación en el Centro de partners de Windows</span><span class="sxs-lookup"><span data-stu-id="0711d-142">Create an app reservation in Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0711d-143">Para mostrar los detalles del editor para su uso en la sección [Empaquetar su PWA,](#package-your-pwa-for-the-store) elija **Product management**  >  **Product Identity**.</span><span class="sxs-lookup"><span data-stu-id="0711d-143">To display your publisher details for use in the [Package your PWA](#package-your-pwa-for-the-store) section, choose **Product management** > **Product Identity**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copiar la información del editor desde el Centro de partners de Windows" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       <span data-ttu-id="0711d-145">Copiar la información del editor desde el Centro de partners de Windows</span><span class="sxs-lookup"><span data-stu-id="0711d-145">Copy your publisher information from Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0711d-146">Copie y guarde los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="0711d-146">Copy and save the following values.</span></span>  
    *   **<span data-ttu-id="0711d-147">Id. de paquete</span><span class="sxs-lookup"><span data-stu-id="0711d-147">Package ID</span></span>**  
    *   **<span data-ttu-id="0711d-148">Id. de publicador</span><span class="sxs-lookup"><span data-stu-id="0711d-148">Publisher ID</span></span>**  
    *   **<span data-ttu-id="0711d-149">Nombre para mostrar del editor</span><span class="sxs-lookup"><span data-stu-id="0711d-149">Publisher Display Name</span></span>**  
        
## <a name="package-your-pwa-for-the-store"></a><span data-ttu-id="0711d-150">Empaquetar tu PWA para la Tienda</span><span class="sxs-lookup"><span data-stu-id="0711d-150">Package your PWA for the Store</span></span> 

<span data-ttu-id="0711d-151">Ahora que ya tienes la información de publicación de aplicaciones, genera un paquete de aplicación de Windows para tu PWA.</span><span class="sxs-lookup"><span data-stu-id="0711d-151">Now that you have your app publishing information, generate a Windows app package for your PWA.</span></span>

<span data-ttu-id="0711d-152">Para generar un paquete de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-152">To generate an app package, complete the following actions.</span></span>  

1.  <span data-ttu-id="0711d-153">Vaya al [Generador de PWA][PwabuilderMain].</span><span class="sxs-lookup"><span data-stu-id="0711d-153">Navigate to [PWA Builder][PwabuilderMain].</span></span>  
1.  <span data-ttu-id="0711d-154">Escriba la dirección URL de su PWA.</span><span class="sxs-lookup"><span data-stu-id="0711d-154">Type the URL of your PWA.</span></span>  
1.  <span data-ttu-id="0711d-155">Elija **Start**  >  **Build My PWA**  >  **Windows**  >  **Options**.</span><span class="sxs-lookup"><span data-stu-id="0711d-155">Choose **Start** > **Build My PWA** > **Windows** > **Options**.</span></span>  
1.  <span data-ttu-id="0711d-156">Pegue los siguientes valores que guardó en la [sección Crear una reserva de](#create-an-app-reservation) aplicación.</span><span class="sxs-lookup"><span data-stu-id="0711d-156">Paste the following values that you saved in the [Create an app reservation](#create-an-app-reservation) section.</span></span>  
    *   **<span data-ttu-id="0711d-157">Id. de paquete</span><span class="sxs-lookup"><span data-stu-id="0711d-157">Package ID</span></span>**  
    *   **<span data-ttu-id="0711d-158">Id. de publicador</span><span class="sxs-lookup"><span data-stu-id="0711d-158">Publisher ID</span></span>**  
    *   **<span data-ttu-id="0711d-159">Nombre para mostrar del editor</span><span class="sxs-lookup"><span data-stu-id="0711d-159">Publisher Display Name</span></span>**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Pegar información del editor en PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       <span data-ttu-id="0711d-161">Pegar información del editor en PWABuilder</span><span class="sxs-lookup"><span data-stu-id="0711d-161">Paste publisher information into PWABuilder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0711d-162">Elija **Listo**.</span><span class="sxs-lookup"><span data-stu-id="0711d-162">Choose **Done**.</span></span>  
1.  <span data-ttu-id="0711d-163">Para descargar el paquete de la aplicación de Windows, elija **Descargar**.</span><span class="sxs-lookup"><span data-stu-id="0711d-163">To download your Windows app package, choose **Download**.</span></span>

<span data-ttu-id="0711d-164">La descarga es un `.zip` archivo que contiene un archivo y un `.msixbundle` `.classic.appxbundle` archivo.</span><span class="sxs-lookup"><span data-stu-id="0711d-164">Your download is a `.zip` archive that contains an `.msixbundle` file and a `.classic.appxbundle` file.</span></span>  <span data-ttu-id="0711d-165">Los dos paquetes de aplicaciones permiten que tu PWA se ejecute en una amplia variedad de versiones de Windows.</span><span class="sxs-lookup"><span data-stu-id="0711d-165">The two app packages allow your PWA to run on a wide variety of Windows versions.</span></span>  <span data-ttu-id="0711d-166">Para obtener más información, vaya [a ¿Qué es un paquete clásico?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].</span><span class="sxs-lookup"><span data-stu-id="0711d-166">For more information, navigate to [What is a classic package?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].</span></span>  

### <a name="submit-your-app-package-to-the-store"></a><span data-ttu-id="0711d-167">Enviar el paquete de la aplicación a la Tienda</span><span class="sxs-lookup"><span data-stu-id="0711d-167">Submit your app package to the Store</span></span>  

<span data-ttu-id="0711d-168">Para enviar la aplicación a la Tienda, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="0711d-168">To submit your app to the Store, complete the following actions.</span></span>  

1.  <span data-ttu-id="0711d-169">Navegar al [Centro de partners de Windows][MicrosoftPartnerDashboardWindowsOverview]</span><span class="sxs-lookup"><span data-stu-id="0711d-169">Navigate to [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span></span> 
1.  <span data-ttu-id="0711d-170">Elige tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="0711d-170">Choose your app.</span></span>  
1.  <span data-ttu-id="0711d-171">Elija **Iniciar el envío**.</span><span class="sxs-lookup"><span data-stu-id="0711d-171">Choose **Start your Submission**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Iniciar un nuevo envío de aplicación en el Centro de partners de Windows" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       <span data-ttu-id="0711d-173">Iniciar un nuevo envío de aplicación en el Centro de partners de Windows</span><span class="sxs-lookup"><span data-stu-id="0711d-173">Start a new app submission on Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="0711d-174">Complete los siguientes mensajes para obtener información sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0711d-174">Complete the following prompts for information about your app.</span></span>
    *   <span data-ttu-id="0711d-175">pricing</span><span class="sxs-lookup"><span data-stu-id="0711d-175">pricing</span></span>  
    *   <span data-ttu-id="0711d-176">clasificación por edades</span><span class="sxs-lookup"><span data-stu-id="0711d-176">age rating</span></span>  
    *   <span data-ttu-id="0711d-177">y mucho más</span><span class="sxs-lookup"><span data-stu-id="0711d-177">and more</span></span>  
        
1.  <span data-ttu-id="0711d-178">En el **símbolo del** sistema Paquetes, elija el archivo y los `.msixbundle` que `.classic.appxbundle` generó en la sección [Empaquetar su PWA.](#package-your-pwa-for-the-store)</span><span class="sxs-lookup"><span data-stu-id="0711d-178">On the **Packages** prompt, choose the `.msixbundle` and the `.classic.appxbundle` files you generated in the [Package your PWA](#package-your-pwa-for-the-store) section.</span></span>  
    
<span data-ttu-id="0711d-179">Después de completar el envío, se revisa la aplicación, normalmente en un plazo de entre 24 y 48 horas.</span><span class="sxs-lookup"><span data-stu-id="0711d-179">After you complete your submission, your app is reviewed, typically within between 24 and 48 hours.</span></span>  <span data-ttu-id="0711d-180">Después de recibir la aprobación, tu PWA está disponible en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="0711d-180">After you receive approval, your PWA is available in the Microsoft Store.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0711d-181">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0711d-181">See also</span></span>  

<span data-ttu-id="0711d-182">PWABuilder proporciona más documentación que le ayudará a obtener su PWA en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="0711d-182">PWABuilder provides more documentation to help you get your PWA in the Microsoft Store.</span></span>  

*   [<span data-ttu-id="0711d-183">Probar y enviar el paquete de la aplicación de PWA</span><span class="sxs-lookup"><span data-stu-id="0711d-183">Test and submit your PWA app package</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [<span data-ttu-id="0711d-184">Publicar un nuevo PWA en la Tienda</span><span class="sxs-lookup"><span data-stu-id="0711d-184">Publish a new PWA to the Store</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [<span data-ttu-id="0711d-185">Actualizar una aplicación de la Tienda existente a un PWA</span><span class="sxs-lookup"><span data-stu-id="0711d-185">Update an existing Store app to a PWA</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [<span data-ttu-id="0711d-186">Recomendaciones de imagen para las PWA en la Tienda</span><span class="sxs-lookup"><span data-stu-id="0711d-186">Image recommendations for PWAs in the Store</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [<span data-ttu-id="0711d-187">Explicador de empaquetado de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="0711d-187">App packaging explainer</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Directivas de Microsoft Store | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analizar el rendimiento de la aplicación | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Capturas de pantalla, imágenes y tráileres de la aplicación | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publicar aplicaciones y juegos de Windows | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Inicio | Centro de partners de Microsoft"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Recursos para partners | Centro de partners de Microsoft"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Hosted App Model | Blog para desarrolladores de Windows"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "¿Qué es un paquete clásico? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Recomendaciones de imagen para paquetes de PWA de Windows | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Pasos siguientes para obtener tu PWA en microsoft store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Publicar una nueva aplicación en la tienda | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Actualizar una aplicación existente en la tienda | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
