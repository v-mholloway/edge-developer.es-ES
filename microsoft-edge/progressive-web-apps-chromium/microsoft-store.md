---
description: Haga que su PWA sea más reconocible mediante la publicación en el Microsoft Store
title: Publicar la aplicación web progresiva en el Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 40a6b94412a0788c87f7231025809098c98f18e9
ms.sourcegitcommit: 7cba715ef71cbac4ee0ebe8f07c0c0e4a2c64221
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "11643252"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a><span data-ttu-id="10884-104">Publicar la aplicación web progresiva en el Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="10884-104">Publish your Progressive Web App to the Microsoft Store</span></span>  

<span data-ttu-id="10884-105">Publicar la aplicación web progresiva \(PWA\) en el Microsoft Store [ofrece][WindowsUwpPublishIndex] las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="10884-105">Publishing your Progressive Web App \(PWA\) to the [Microsoft Store][WindowsUwpPublishIndex] brings the following advantages.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="10884-106">Detectabilidad</span><span class="sxs-lookup"><span data-stu-id="10884-106">Discoverability</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="10884-107">Los usuarios buscan aplicaciones de forma natural en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="10884-107">Users naturally look for apps in the app store.</span></span>  <span data-ttu-id="10884-108">Al publicar en el Microsoft Store, millones de Windows usuarios pueden descubrir su PWA junto con otras Windows aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="10884-108">When you publish to the Microsoft Store, millions of Windows users may discover your PWA alongside other Windows apps.</span></span>  <span data-ttu-id="10884-109">La Tienda muestra aplicaciones a través de categorías, colecciones curadas y mucho más.</span><span class="sxs-lookup"><span data-stu-id="10884-109">The Store showcases apps through categories, curated collections, and more.</span></span>  <span data-ttu-id="10884-110">Los portales de detección de aplicaciones proporcionan una experiencia de exploración y compra fácil para los posibles usuarios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10884-110">The app discovery portals provide an easy browsing and shopping experience for potential users of your app.</span></span>  <span data-ttu-id="10884-111">Incluso puedes mejorar [la descripción de la Tienda][WindowsUwpPublishAppScreenshotsImages] con capturas de pantalla, una imagen de héroe y tráileres de vídeo.</span><span class="sxs-lookup"><span data-stu-id="10884-111">You may even [enhance your Store listing][WindowsUwpPublishAppScreenshotsImages] with screenshots, a hero image, and video trailers.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="10884-112">Fiabilidad</span><span class="sxs-lookup"><span data-stu-id="10884-112">Trustworthiness</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="10884-113">Windows clientes saben que pueden confiar en sus Microsoft Store compras y descargas, ya que se adhieren a los rigurosos estándares de calidad [y seguridad de][LegalWindowsAgreementsStorePolicies]Microsoft.</span><span class="sxs-lookup"><span data-stu-id="10884-113">Windows customers know they may trust their Microsoft Store purchases and downloads, because they adhere to the rigorous Microsoft [quality and safety standards][LegalWindowsAgreementsStorePolicies].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="10884-114">Instalación sencilla</span><span class="sxs-lookup"><span data-stu-id="10884-114">Easy install</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="10884-115">El Microsoft Store proporciona una experiencia de instalación coherente y fácil de usar en todas [Windows 10 aplicaciones.][MicrosoftStoreAppsWindows]</span><span class="sxs-lookup"><span data-stu-id="10884-115">The Microsoft Store provides a consistent and user-friendly install experience across [all Windows 10 apps][MicrosoftStoreAppsWindows].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="10884-116">Análisis de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="10884-116">App analytics</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="10884-117">El [Windows centro de partners][WindowsUwpPublishIndex] le [][WindowsUwpPublishAnalytics] proporciona análisis detallados sobre el estado de la aplicación, el uso y mucho más.</span><span class="sxs-lookup"><span data-stu-id="10884-117">The [Windows Partner Center dashboard][WindowsUwpPublishIndex] provides you with [detailed analytics][WindowsUwpPublishAnalytics] about your app health, usage, and more.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="10884-118">Para publicar el PWA en el Microsoft Store, no se requieren cambios de código.</span><span class="sxs-lookup"><span data-stu-id="10884-118">To publish your PWA to the Microsoft Store, no code changes are required.</span></span>  <span data-ttu-id="10884-119">En su lugar, creas una reserva de aplicación, empaquetas tu PWA y envías el paquete a la Tienda.</span><span class="sxs-lookup"><span data-stu-id="10884-119">Instead, you create an app reservation, package your PWA, and submit your package to the Store.</span></span>  <span data-ttu-id="10884-120">En las secciones siguientes se explican los pasos.</span><span class="sxs-lookup"><span data-stu-id="10884-120">The following sections explain the steps.</span></span>   

## <a name="create-an-app-reservation"></a><span data-ttu-id="10884-121">Crear una reserva de aplicación</span><span class="sxs-lookup"><span data-stu-id="10884-121">Create an app reservation</span></span>  

<span data-ttu-id="10884-122">[Windows centro de partners][MicrosoftPartnerDashboardWindowsOverview] es el centro para que envíes la aplicación al Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="10884-122">[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] is the hub for you to submit your app to the Microsoft Store.</span></span>  

<span data-ttu-id="10884-123">Para crear una reserva de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="10884-123">To create an app reservation, complete the following actions.</span></span>  

1.  <span data-ttu-id="10884-124">Para mostrar los programas inscritos, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="10884-124">To display your enrolled programs, complete the following actions.</span></span>  
    1.  <span data-ttu-id="10884-125">Inicie sesión Windows centro de partners con su cuenta de Microsoft y vaya al [Panel del Centro de partners.][MicrosoftPartnerDashboardHome]</span><span class="sxs-lookup"><span data-stu-id="10884-125">Sign into Windows Partner Center with your Microsoft account and navigate to the [Partner Center Dashboard][MicrosoftPartnerDashboardHome].</span></span>  
    1.  <span data-ttu-id="10884-126">Navegar a **Windows & Xbox**</span><span class="sxs-lookup"><span data-stu-id="10884-126">Navigate to **Windows & Xbox**</span></span>  
        *   <span data-ttu-id="10884-127">Si Windows & se muestra **Xbox,** la aplicación ya está registrada.</span><span class="sxs-lookup"><span data-stu-id="10884-127">If **Windows & Xbox** is displayed, your app is already enrolled.</span></span>  
        *   <span data-ttu-id="10884-128">Si **Windows & xbox** no se muestra, elige Agregar **programa**.</span><span class="sxs-lookup"><span data-stu-id="10884-128">If **Windows & Xbox** isn't displayed, choose **Add program**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Agregar un programa en el panel Windows centro de partners" lightbox="./media/windows-partner-center-add-program.msft.png":::
       <span data-ttu-id="10884-130">Agregar un programa en el panel Windows centro de partners</span><span class="sxs-lookup"><span data-stu-id="10884-130">Add a program in the Windows Partner Center dashboard</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="10884-131">Para inscribirse en el programa de desarrolladores, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="10884-131">To enroll in the developer program, complete the following actions.</span></span>  
    1.  <span data-ttu-id="10884-132">Vaya a **Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="10884-132">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="10884-133">Elija **Introducción**.</span><span class="sxs-lookup"><span data-stu-id="10884-133">Choose **Get started**.</span></span>  
    1.  <span data-ttu-id="10884-134">Sigue las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="10884-134">Follow the prompts.</span></span>  
1.  <span data-ttu-id="10884-135">Ahora, tu cuenta está inscrita en el programa para desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="10884-135">Now, your account is enrolled in the app developer program.</span></span> <span data-ttu-id="10884-136">Para crear una reserva de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="10884-136">To create an app reservation, complete the following actions.</span></span>  
    1.  <span data-ttu-id="10884-137">Vaya a **Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="10884-137">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="10884-138">Elija **Información general**Crear una nueva  >  **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="10884-138">Choose **Overview** > **Create a new app**.</span></span>  
    1.  <span data-ttu-id="10884-139">Escriba el nombre de la aplicación en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="10884-139">Type the name of your app in the prompt.</span></span>  
    1.  <span data-ttu-id="10884-140">Elija `Reserve product name` .</span><span class="sxs-lookup"><span data-stu-id="10884-140">Choose `Reserve product name`.</span></span>  
        
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Crear una reserva de aplicación en Windows Partner Center" lightbox="./media/windows-partner-center-create-app.msft.png":::
       <span data-ttu-id="10884-142">Crear una reserva de aplicación en Windows Partner Center</span><span class="sxs-lookup"><span data-stu-id="10884-142">Create an app reservation in Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10884-143">Para mostrar los detalles del editor para su uso en la sección [Empaquetar PWA,](#package-your-pwa-for-the-store) elija **Product management**  >  **Product Identity**.</span><span class="sxs-lookup"><span data-stu-id="10884-143">To display your publisher details for use in the [Package your PWA](#package-your-pwa-for-the-store) section, choose **Product management** > **Product Identity**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copiar la información del editor desde Windows de partners" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       <span data-ttu-id="10884-145">Copiar la información del editor desde Windows de partners</span><span class="sxs-lookup"><span data-stu-id="10884-145">Copy your publisher information from Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10884-146">Copie y guarde los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="10884-146">Copy and save the following values.</span></span>  
    *   **<span data-ttu-id="10884-147">Id. de paquete</span><span class="sxs-lookup"><span data-stu-id="10884-147">Package ID</span></span>**  
    *   **<span data-ttu-id="10884-148">Publisher Id.</span><span class="sxs-lookup"><span data-stu-id="10884-148">Publisher ID</span></span>**  
    *   **<span data-ttu-id="10884-149">Publisher Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="10884-149">Publisher Display Name</span></span>**  
        
## <a name="package-your-pwa-for-the-store"></a><span data-ttu-id="10884-150">Empaquetar el PWA para la Tienda</span><span class="sxs-lookup"><span data-stu-id="10884-150">Package your PWA for the Store</span></span> 

<span data-ttu-id="10884-151">Ahora que ya tienes la información de publicación de la aplicación, genera un Windows de la aplicación para tu PWA.</span><span class="sxs-lookup"><span data-stu-id="10884-151">Now that you have your app publishing information, generate a Windows app package for your PWA.</span></span>

<span data-ttu-id="10884-152">Para generar un paquete de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="10884-152">To generate an app package, complete the following actions.</span></span>  

1.  <span data-ttu-id="10884-153">Vaya a [PWA Builder][PwabuilderMain].</span><span class="sxs-lookup"><span data-stu-id="10884-153">Navigate to [PWA Builder][PwabuilderMain].</span></span>  
1.  <span data-ttu-id="10884-154">Escriba la dirección URL de su PWA.</span><span class="sxs-lookup"><span data-stu-id="10884-154">Type the URL of your PWA.</span></span>  
1.  <span data-ttu-id="10884-155">Elija **Start**  >  **Build My PWA**  >  **Windows**  >  **Options**.</span><span class="sxs-lookup"><span data-stu-id="10884-155">Choose **Start** > **Build My PWA** > **Windows** > **Options**.</span></span>  
1.  <span data-ttu-id="10884-156">Pegue los siguientes valores que guardó en la [sección Crear una reserva de](#create-an-app-reservation) aplicación.</span><span class="sxs-lookup"><span data-stu-id="10884-156">Paste the following values that you saved in the [Create an app reservation](#create-an-app-reservation) section.</span></span>  
    *   **<span data-ttu-id="10884-157">Id. de paquete</span><span class="sxs-lookup"><span data-stu-id="10884-157">Package ID</span></span>**  
    *   **<span data-ttu-id="10884-158">Publisher Id.</span><span class="sxs-lookup"><span data-stu-id="10884-158">Publisher ID</span></span>**  
    *   **<span data-ttu-id="10884-159">Publisher Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="10884-159">Publisher Display Name</span></span>**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Pegar información del editor en PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       <span data-ttu-id="10884-161">Pegar información del editor en PWABuilder</span><span class="sxs-lookup"><span data-stu-id="10884-161">Paste publisher information into PWABuilder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10884-162">Elija **Listo**.</span><span class="sxs-lookup"><span data-stu-id="10884-162">Choose **Done**.</span></span>  
1.  <span data-ttu-id="10884-163">Para descargar el paquete Windows aplicación, elija **Descargar**.</span><span class="sxs-lookup"><span data-stu-id="10884-163">To download your Windows app package, choose **Download**.</span></span>

<span data-ttu-id="10884-164">La descarga es un `.zip` archivo que contiene un archivo y un `.msixbundle` `.classic.appxbundle` archivo.</span><span class="sxs-lookup"><span data-stu-id="10884-164">Your download is a `.zip` archive that contains an `.msixbundle` file and a `.classic.appxbundle` file.</span></span>  <span data-ttu-id="10884-165">Los dos paquetes de aplicaciones permiten que PWA se ejecuten en una amplia variedad de Windows versiones.</span><span class="sxs-lookup"><span data-stu-id="10884-165">The two app packages allow your PWA to run on a wide variety of Windows versions.</span></span>  <span data-ttu-id="10884-166">Para obtener más información, vaya [a ¿Qué es un paquete clásico?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].</span><span class="sxs-lookup"><span data-stu-id="10884-166">For more information, navigate to [What is a classic package?][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd].</span></span>  

### <a name="submit-your-app-package-to-the-store"></a><span data-ttu-id="10884-167">Enviar el paquete de la aplicación a la Tienda</span><span class="sxs-lookup"><span data-stu-id="10884-167">Submit your app package to the Store</span></span>  

<span data-ttu-id="10884-168">Para enviar la aplicación a la Tienda, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="10884-168">To submit your app to the Store, complete the following actions.</span></span>  

1.  <span data-ttu-id="10884-169">Vaya al [Centro Windows partners][MicrosoftPartnerDashboardWindowsOverview]</span><span class="sxs-lookup"><span data-stu-id="10884-169">Navigate to [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span></span> 
1.  <span data-ttu-id="10884-170">Elige tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="10884-170">Choose your app.</span></span>  
1.  <span data-ttu-id="10884-171">Elija **Iniciar el envío**.</span><span class="sxs-lookup"><span data-stu-id="10884-171">Choose **Start your Submission**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Iniciar un nuevo envío de aplicación en Windows de partners" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       <span data-ttu-id="10884-173">Iniciar un nuevo envío de aplicación en Windows de partners</span><span class="sxs-lookup"><span data-stu-id="10884-173">Start a new app submission on Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="10884-174">Complete los siguientes mensajes para obtener información sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="10884-174">Complete the following prompts for information about your app.</span></span>
    *   <span data-ttu-id="10884-175">pricing</span><span class="sxs-lookup"><span data-stu-id="10884-175">pricing</span></span>  
    *   <span data-ttu-id="10884-176">clasificación por edades</span><span class="sxs-lookup"><span data-stu-id="10884-176">age rating</span></span>  
    *   <span data-ttu-id="10884-177">y mucho más</span><span class="sxs-lookup"><span data-stu-id="10884-177">and more</span></span>  
        
1.  <span data-ttu-id="10884-178">En el **símbolo del** sistema Paquetes, elija el archivo y los `.msixbundle` que `.classic.appxbundle` generó en la sección [Empaquetar PWA.](#package-your-pwa-for-the-store)</span><span class="sxs-lookup"><span data-stu-id="10884-178">On the **Packages** prompt, choose the `.msixbundle` and the `.classic.appxbundle` files you generated in the [Package your PWA](#package-your-pwa-for-the-store) section.</span></span>  
    
<span data-ttu-id="10884-179">Después de completar el envío, se revisa la aplicación, normalmente en un plazo de entre 24 y 48 horas.</span><span class="sxs-lookup"><span data-stu-id="10884-179">After you complete your submission, your app is reviewed, typically within between 24 and 48 hours.</span></span>  <span data-ttu-id="10884-180">Después de recibir la aprobación, el PWA está disponible en el Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="10884-180">After you receive approval, your PWA is available in the Microsoft Store.</span></span>  

### <a name="measure-usage-of-your-store-installed-pwa"></a><span data-ttu-id="10884-181">Medir el uso de las aplicaciones instaladas en la Tienda PWA</span><span class="sxs-lookup"><span data-stu-id="10884-181">Measure usage of your Store-installed PWA</span></span>

<span data-ttu-id="10884-182">Cuando el PWA se inicia inicialmente, si el PWA se instaló desde el Microsoft Store, Microsoft Edge incluye el siguiente encabezado con la solicitud para la primera navegación de la aplicación `Referer` web.</span><span class="sxs-lookup"><span data-stu-id="10884-182">When your PWA is initially launched, if the PWA was installed from the Microsoft Store, Microsoft Edge includes the following `Referer` header with the request for the first navigation of your web app.</span></span>

```
Referer: app-info://platform/microsoft-store
```

<span data-ttu-id="10884-183">Usa esta característica para medir el tráfico distinto del tráfico instalado en la Tienda PWA.</span><span class="sxs-lookup"><span data-stu-id="10884-183">Use this feature to measure distinct traffic from your Store-installed PWA.</span></span>  <span data-ttu-id="10884-184">En función del tráfico, puedes ajustar el contenido de la aplicación para mejorar la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="10884-184">Based on the traffic, you can adjust your app’s content to improve the user experience.</span></span>  <span data-ttu-id="10884-185">Esta característica es accesible tanto para el código de cliente como para el código del servidor.</span><span class="sxs-lookup"><span data-stu-id="10884-185">This feature is accessible to both client and server code.</span></span>

<span data-ttu-id="10884-186">Esta característica se introdujo en Microsoft Edge versión 91.</span><span class="sxs-lookup"><span data-stu-id="10884-186">This feature was introduced in Microsoft Edge version 91.</span></span>

## <a name="see-also"></a><span data-ttu-id="10884-187">Consulte también</span><span class="sxs-lookup"><span data-stu-id="10884-187">See also</span></span>  

<span data-ttu-id="10884-188">PWABuilder proporciona más documentación para ayudarle a obtener sus PWA en el Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="10884-188">PWABuilder provides more documentation to help you get your PWA in the Microsoft Store.</span></span>  

*   [<span data-ttu-id="10884-189">Probar y enviar el paquete PWA aplicación</span><span class="sxs-lookup"><span data-stu-id="10884-189">Test and submit your PWA app package</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]  
*   [<span data-ttu-id="10884-190">Publicar una nueva PWA en la Tienda</span><span class="sxs-lookup"><span data-stu-id="10884-190">Publish a new PWA to the Store</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]  
*   [<span data-ttu-id="10884-191">Actualizar una aplicación de la Tienda existente a un PWA</span><span class="sxs-lookup"><span data-stu-id="10884-191">Update an existing Store app to a PWA</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]  
*   [<span data-ttu-id="10884-192">Recomendaciones de imagen para las PWA en la Tienda</span><span class="sxs-lookup"><span data-stu-id="10884-192">Image recommendations for PWAs in the Store</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]  
*   [<span data-ttu-id="10884-193">Explicador de empaquetado de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="10884-193">App packaging explainer</span></span>][GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Microsoft Store Directivas | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analizar el rendimiento de la aplicación | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Capturas de pantalla, imágenes y tráileres de la aplicación | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publicar Windows aplicaciones y juegos | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Inicio | Centro de partners de Microsoft"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Recursos para partners | Centro de partners de Microsoft"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Aplicaciones | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Hosted App Model | Windows Blog para desarrolladores"  

[GithubPwaBuilderPwabuilderWindowsChromiumDocsClassicPackageMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/classic-package.md "¿Qué es un paquete clásico? | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsImageRecommendationsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/image-recommendations.md "Recomendaciones de imagen para Windows PWA paquetes | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsNextStepsMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/next-steps.md "Pasos siguientes para obtener el PWA en el Microsoft Store | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsPublishNewAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/publish-new-app.md "Publicar una nueva aplicación en la tienda | GitHub"  
[GithubPwaBuilderPwabuilderWindowsChromiumDocsUpdateExistingAppMd]: https://github.com/pwa-builder/pwabuilder-windows-chromium-docs/blob/master/update-existing-app.md "Actualizar una aplicación existente en la tienda | GitHub"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  
