---
description: Hacer que tu PWA sea más reconocible publicando en Microsoft Store
title: Publicar la aplicación web progresiva en Microsoft Store
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: aplicaciones web progresivas, PWA, Edge, Windows, Microsoft Store
ms.openlocfilehash: 68471535446a2270a23b32205717da225fd9e4bf
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461566"
---
# <a name="publish-your-progressive-web-app-to-the-microsoft-store"></a><span data-ttu-id="39078-104">Publicar la aplicación web progresiva en Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="39078-104">Publish your Progressive Web App to the Microsoft Store</span></span>  

<span data-ttu-id="39078-105">Publicar la aplicación web progresiva \(PWA\) en [Microsoft Store][WindowsUwpPublishIndex] ofrece las siguientes ventajas.</span><span class="sxs-lookup"><span data-stu-id="39078-105">Publishing your Progressive Web App \(PWA\) to the [Microsoft Store][WindowsUwpPublishIndex] brings the following advantages.</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="39078-106">Detectabilidad</span><span class="sxs-lookup"><span data-stu-id="39078-106">Discoverability</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="39078-107">Los usuarios buscan aplicaciones de forma natural en la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="39078-107">Users naturally look for apps in the app store.</span></span>  <span data-ttu-id="39078-108">Al publicar en la Microsoft Store, millones de usuarios de Windows pueden descubrir su PWA junto con otras aplicaciones de Windows.</span><span class="sxs-lookup"><span data-stu-id="39078-108">By publishing to the Microsoft Store, millions of Windows users may discover your PWA alongside other Windows apps.</span></span>  <span data-ttu-id="39078-109">La Tienda muestra aplicaciones a través de categorías, colecciones curadas y mucho más.</span><span class="sxs-lookup"><span data-stu-id="39078-109">The Store showcases apps through categories, curated collections, and more.</span></span>  <span data-ttu-id="39078-110">Los portales de detección de aplicaciones proporcionan una experiencia de exploración y compra fácil para los posibles usuarios de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39078-110">The app discovery portals provide an easy browsing and shopping experience for potential users of your app.</span></span>  <span data-ttu-id="39078-111">Incluso puedes mejorar [la descripción de la Tienda][WindowsUwpPublishAppScreenshotsImages] con capturas de pantalla, una imagen de héroe y tráileres de vídeo.</span><span class="sxs-lookup"><span data-stu-id="39078-111">You may even [enhance your Store listing][WindowsUwpPublishAppScreenshotsImages] with screenshots, a hero image, and video trailers.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="39078-112">Fiabilidad</span><span class="sxs-lookup"><span data-stu-id="39078-112">Trustworthiness</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="39078-113">Los clientes de Windows saben que pueden confiar en sus compras y descargas de Microsoft Store, ya que se adhieren a los rigurosos estándares de calidad [y seguridad de][LegalWindowsAgreementsStorePolicies]Microsoft.</span><span class="sxs-lookup"><span data-stu-id="39078-113">Windows customers know they may trust their Microsoft Store purchases and downloads, because they adhere to the rigorous Microsoft [quality and safety standards][LegalWindowsAgreementsStorePolicies].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="39078-114">Instalación sencilla</span><span class="sxs-lookup"><span data-stu-id="39078-114">Easy install</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="39078-115">La Microsoft Store proporciona una experiencia de instalación coherente y fácil de usar en [todas las aplicaciones de Windows 10.][MicrosoftStoreAppsWindows]</span><span class="sxs-lookup"><span data-stu-id="39078-115">The Microsoft Store provides a consistent and user-friendly install experience across [all Windows 10 apps][MicrosoftStoreAppsWindows].</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **<span data-ttu-id="39078-116">Análisis de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="39078-116">App analytics</span></span>**  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="39078-117">El [panel del Centro de partners de Windows][WindowsUwpPublishIndex] te proporciona análisis [detallados][WindowsUwpPublishAnalytics] sobre el estado de la aplicación, el uso y mucho más.</span><span class="sxs-lookup"><span data-stu-id="39078-117">The [Windows Partner Center dashboard][WindowsUwpPublishIndex] provides you with [detailed analytics][WindowsUwpPublishAnalytics] about your app health, usage, and more.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="39078-118">Para publicar tu PWA en Microsoft Store, no es necesario realizar cambios en el código.</span><span class="sxs-lookup"><span data-stu-id="39078-118">To publish your PWA to the Microsoft Store, no code changes are required.</span></span>  <span data-ttu-id="39078-119">En su lugar, creas una reserva de aplicación, empaquetas tu PWA y envías el paquete a la Tienda.</span><span class="sxs-lookup"><span data-stu-id="39078-119">Instead, you create an app reservation, package your PWA, and submit your package to the Store.</span></span>  <span data-ttu-id="39078-120">En las secciones siguientes se explican los pasos.</span><span class="sxs-lookup"><span data-stu-id="39078-120">The following sections explain the steps.</span></span>   

## <a name="create-an-app-reservation"></a><span data-ttu-id="39078-121">Crear una reserva de aplicación</span><span class="sxs-lookup"><span data-stu-id="39078-121">Create an app reservation</span></span>  

<span data-ttu-id="39078-122">[El Centro de partners de Windows][MicrosoftPartnerDashboardWindowsOverview] es el centro para que envíes la aplicación a la Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="39078-122">[Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview] is the hub for you to submit your app to the Microsoft Store.</span></span>  

<span data-ttu-id="39078-123">Para crear una reserva de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="39078-123">To create an app reservation, complete the following actions.</span></span>  

1.  <span data-ttu-id="39078-124">Para mostrar los programas inscritos, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="39078-124">To display your enrolled programs, complete the following actions.</span></span>  
    1.  <span data-ttu-id="39078-125">Inicie sesión en el Centro de partners de Windows con su cuenta microsoft y vaya al [Panel del Centro de partners.][MicrosoftPartnerDashboardHome]</span><span class="sxs-lookup"><span data-stu-id="39078-125">Sign into Windows Partner Center with your Microsoft account and navigate to the [Partner Center Dashboard][MicrosoftPartnerDashboardHome].</span></span>  
    1.  <span data-ttu-id="39078-126">Navegar a **Windows & Xbox**</span><span class="sxs-lookup"><span data-stu-id="39078-126">Navigate to **Windows & Xbox**</span></span>  
        *   <span data-ttu-id="39078-127">Si se muestra & Xbox de **Windows,** la aplicación ya está registrada.</span><span class="sxs-lookup"><span data-stu-id="39078-127">If **Windows & Xbox** is displayed, your app is already enrolled.</span></span>  
        *   <span data-ttu-id="39078-128">Si **Windows & xbox** no se muestra, elige Agregar **programa**.</span><span class="sxs-lookup"><span data-stu-id="39078-128">If **Windows & Xbox** isn't displayed, choose **Add program**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-add-program.msft.png" alt-text="Agregar un programa en el panel del Centro de partners de Windows" lightbox="./media/windows-partner-center-add-program.msft.png":::
       <span data-ttu-id="39078-130">Agregar un programa en el panel del Centro de partners de Windows</span><span class="sxs-lookup"><span data-stu-id="39078-130">Add a program in the Windows Partner Center dashboard</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="39078-131">Para inscribirse en el programa de desarrolladores, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="39078-131">To enroll in the developer program, complete the following actions.</span></span>  
    1.  <span data-ttu-id="39078-132">Navega a **Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="39078-132">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="39078-133">Elija **Introducción**.</span><span class="sxs-lookup"><span data-stu-id="39078-133">Choose **Get started**.</span></span>  
    1.  <span data-ttu-id="39078-134">Sigue las instrucciones.</span><span class="sxs-lookup"><span data-stu-id="39078-134">Follow the prompts.</span></span>  
1.  <span data-ttu-id="39078-135">Ahora, la aplicación está inscrita en el programa para desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="39078-135">Now, your app is enrolled in the app developer program.</span></span> <span data-ttu-id="39078-136">Para crear una reserva de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="39078-136">To create an app reservation, complete the following actions.</span></span>  
    1.  <span data-ttu-id="39078-137">Navega a **Windows & Xbox**.</span><span class="sxs-lookup"><span data-stu-id="39078-137">Navigate to **Windows & Xbox**.</span></span>  
    1.  <span data-ttu-id="39078-138">Elija **Información general**Crear una nueva  >  **aplicación**.</span><span class="sxs-lookup"><span data-stu-id="39078-138">Choose **Overview** > **Create a new app**.</span></span>  
    1.  <span data-ttu-id="39078-139">Escriba el nombre de PWA en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="39078-139">Type your PWA name in the prompt.</span></span>  
    1.  <span data-ttu-id="39078-140">Elija `Reserve product name` .</span><span class="sxs-lookup"><span data-stu-id="39078-140">Choose `Reserve product name`.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-create-app.msft.png" alt-text="Crear una reserva de aplicación en el Centro de partners de Windows" lightbox="./media/windows-partner-center-create-app.msft.png":::
       <span data-ttu-id="39078-142">Crear una reserva de aplicación en el Centro de partners de Windows</span><span class="sxs-lookup"><span data-stu-id="39078-142">Create an app reservation in Windows Partner Center</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="39078-143">Para mostrar los detalles del editor para su uso en la sección [Empaquetar su PWA,](#package-your-pwa) elija **Product management**  >  **Product Identity**.</span><span class="sxs-lookup"><span data-stu-id="39078-143">To display your publisher details for use in the [Package your PWA](#package-your-pwa) section, choose **Product management** > **Product Identity**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-publisher-info.msft.png" alt-text="Copiar la información del editor desde el Centro de partners de Windows" lightbox="./media/windows-partner-center-publisher-info.msft.png":::
       <span data-ttu-id="39078-145">Copiar la información del editor desde el Centro de partners de Windows</span><span class="sxs-lookup"><span data-stu-id="39078-145">Copy your publisher information from Windows Partner Center</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="39078-146">Copie y guarde los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="39078-146">Copy and save the following values.</span></span>  
    *   **<span data-ttu-id="39078-147">Id. de paquete</span><span class="sxs-lookup"><span data-stu-id="39078-147">Package ID</span></span>**  
    *   **<span data-ttu-id="39078-148">Id. de publicador</span><span class="sxs-lookup"><span data-stu-id="39078-148">Publisher ID</span></span>**  
    *   **<span data-ttu-id="39078-149">Nombre para mostrar del editor</span><span class="sxs-lookup"><span data-stu-id="39078-149">Publisher Display Name</span></span>**  
        
## <a name="package-your-pwa"></a><span data-ttu-id="39078-150">Empaquetar su PWA</span><span class="sxs-lookup"><span data-stu-id="39078-150">Package your PWA</span></span>  

<span data-ttu-id="39078-151">Genera un paquete de aplicación de Windows para tu PWA.</span><span class="sxs-lookup"><span data-stu-id="39078-151">Generate a Windows app package for your PWA.</span></span>  

<span data-ttu-id="39078-152">El paquete de la aplicación es un archivo que contiene los metadatos de la aplicación, incluidos el `.msixbundle` nombre, la descripción, los iconos, entre otros.</span><span class="sxs-lookup"><span data-stu-id="39078-152">Your app package is an `.msixbundle` file that contains the metadata of your app including the name, description, icons, and so on.</span></span>  <span data-ttu-id="39078-153">Usa el [modelo de aplicaciones hospedadas,][WindowsBlogWindowsdeveloperHostedAppModel]con Microsoft Edge potenciando tu PWA.</span><span class="sxs-lookup"><span data-stu-id="39078-153">It uses the [Hosted App Model][WindowsBlogWindowsdeveloperHostedAppModel], with Microsoft Edge powering your PWA.</span></span>  <span data-ttu-id="39078-154">En este modelo, tu PWA usa funcionalidades web modernas mientras funciona como una aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="39078-154">In this model, your PWA uses modern web capabilities while functioning as a Windows app.</span></span>  <span data-ttu-id="39078-155">Entre las funcionalidades web modernas se incluyen el trabajador del servicio, sin conexión, las notificaciones de inserción, la mala administración y mucho más.</span><span class="sxs-lookup"><span data-stu-id="39078-155">Modern web capabilities include service worker, offline, push notifications, badging, and more.</span></span>  

<span data-ttu-id="39078-156">Para generar un paquete de aplicación, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="39078-156">To generate an app package, complete the following actions.</span></span>  

1.  <span data-ttu-id="39078-157">Vaya al [Generador de PWA][PwabuilderMain].</span><span class="sxs-lookup"><span data-stu-id="39078-157">Navigate to [PWA Builder][PwabuilderMain].</span></span>  
1.  <span data-ttu-id="39078-158">Escriba la dirección URL de su PWA.</span><span class="sxs-lookup"><span data-stu-id="39078-158">Type the URL of your PWA.</span></span>  
1.  <span data-ttu-id="39078-159">Elija **Start**  >  **Build My PWA**  >  **Windows**  >  **Options**.</span><span class="sxs-lookup"><span data-stu-id="39078-159">Choose **Start** > **Build My PWA** > **Windows** > **Options**.</span></span>  
1.  <span data-ttu-id="39078-160">Pegue los siguientes valores que guardó en la [sección Crear una reserva de](#create-an-app-reservation) aplicación.</span><span class="sxs-lookup"><span data-stu-id="39078-160">Paste the following values that you saved in the [Create an app reservation](#create-an-app-reservation) section.</span></span>  
    *   **<span data-ttu-id="39078-161">Id. de paquete</span><span class="sxs-lookup"><span data-stu-id="39078-161">Package ID</span></span>**  
    *   **<span data-ttu-id="39078-162">Id. de publicador</span><span class="sxs-lookup"><span data-stu-id="39078-162">Publisher ID</span></span>**  
    *   **<span data-ttu-id="39078-163">Nombre para mostrar del editor</span><span class="sxs-lookup"><span data-stu-id="39078-163">Publisher Display Name</span></span>**  
        
    :::image type="complex" source="./media/pwabuilder-publisher-info.msft.png" alt-text="Pegar información del editor en PWABuilder" lightbox="./media/pwabuilder-publisher-info.msft.png":::
       <span data-ttu-id="39078-165">Pegar información del editor en PWABuilder</span><span class="sxs-lookup"><span data-stu-id="39078-165">Paste publisher information into PWABuilder</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="39078-166">Elija **Listo**.</span><span class="sxs-lookup"><span data-stu-id="39078-166">Choose **Done**.</span></span>  
1.  <span data-ttu-id="39078-167">Para descargar el paquete de la aplicación de Windows, elija **Descargar**.</span><span class="sxs-lookup"><span data-stu-id="39078-167">To download your Windows app package, choose **Download**.</span></span>  <span data-ttu-id="39078-168">La descarga es un `.zip` archivo que contiene un `.msixbundle` archivo.</span><span class="sxs-lookup"><span data-stu-id="39078-168">Your download is a `.zip` archive containing an `.msixbundle` file.</span></span>  <span data-ttu-id="39078-169">Usa el `.msixbundle` archivo en la sección Enviar el paquete de la aplicación a la [Tienda.](#submit-your-app-package-to-the-store)</span><span class="sxs-lookup"><span data-stu-id="39078-169">Use the `.msixbundle` file in the [Submit your app package to the Store](#submit-your-app-package-to-the-store) section.</span></span>  

### <a name="submit-your-app-package-to-the-store"></a><span data-ttu-id="39078-170">Enviar el paquete de la aplicación a la Tienda</span><span class="sxs-lookup"><span data-stu-id="39078-170">Submit your app package to the Store</span></span>  

<span data-ttu-id="39078-171">Ahora, tienes el paquete `.msixbundle` de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39078-171">Now, you have your `.msixbundle` app package.</span></span>  <span data-ttu-id="39078-172">Para enviar el paquete de la aplicación a la Tienda, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="39078-172">To submit your app package to the Store, complete the following actions.</span></span>  

1.  <span data-ttu-id="39078-173">Navegar al [Centro de partners de Windows][MicrosoftPartnerDashboardWindowsOverview]</span><span class="sxs-lookup"><span data-stu-id="39078-173">Navigate to [Windows Partner Center][MicrosoftPartnerDashboardWindowsOverview]</span></span> 
1.  <span data-ttu-id="39078-174">Elige tu aplicación.</span><span class="sxs-lookup"><span data-stu-id="39078-174">Choose your app.</span></span>  
1.  <span data-ttu-id="39078-175">Elija **Iniciar el envío**.</span><span class="sxs-lookup"><span data-stu-id="39078-175">Choose **Start your Submission**.</span></span>  
    
    :::image type="complex" source="./media/windows-partner-center-start-submission.msft.png" alt-text="Iniciar un nuevo envío de aplicación en el Centro de partners de Windows" lightbox="./media/windows-partner-center-start-submission.msft.png":::
       <span data-ttu-id="39078-177">Iniciar un nuevo envío de aplicación en el Centro de partners de Windows</span><span class="sxs-lookup"><span data-stu-id="39078-177">Start a new app submission on Windows Partner Center</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="39078-178">Complete los siguientes mensajes para obtener información sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="39078-178">Complete the following prompts for information about your app.</span></span>
    *   <span data-ttu-id="39078-179">pricing</span><span class="sxs-lookup"><span data-stu-id="39078-179">pricing</span></span>  
    *   <span data-ttu-id="39078-180">clasificación por edades</span><span class="sxs-lookup"><span data-stu-id="39078-180">age rating</span></span>  
    *   <span data-ttu-id="39078-181">y mucho más</span><span class="sxs-lookup"><span data-stu-id="39078-181">and more</span></span>  
        
1.  <span data-ttu-id="39078-182">En el **símbolo del** sistema Paquetes, elija el archivo generado en la `.msixbundle` sección [Empaquetar su PWA.](#package-your-pwa)</span><span class="sxs-lookup"><span data-stu-id="39078-182">On the **Packages** prompt, choose the `.msixbundle` file your generated in the [Package your PWA](#package-your-pwa) section.</span></span>  

<span data-ttu-id="39078-183">Después de completar el envío, se revisa la aplicación, normalmente en un plazo de entre 24 y 48 horas.</span><span class="sxs-lookup"><span data-stu-id="39078-183">After you complete your submission, your app is reviewed, typically within between 24 and 48 hours.</span></span>  <span data-ttu-id="39078-184">Después de recibir la aprobación, tu PWA está disponible en Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="39078-184">After you receive approval, your PWA is available in the Microsoft Store.</span></span>  

<!-- links -->  

[LegalWindowsAgreementsStorePolicies]: /legal/windows/agreements/store-policies "Directivas de Microsoft Store | Microsoft Docs"  

[WindowsUwpPublishAnalytics]: /windows/uwp/publish/analytics "Analizar el rendimiento de la aplicación | Microsoft Docs"  
[WindowsUwpPublishAppScreenshotsImages]: /windows/uwp/publish/app-screenshots-and-images "Capturas de pantalla, imágenes y tráileres de la aplicación | Microsoft Docs"  
[WindowsUwpPublishIndex]: /windows/uwp/publish/index "Publicar aplicaciones y juegos de Windows | Microsoft Docs"  

[MicrosoftPartnerDashboardHome]: https://partner.microsoft.com/dashboard/home "Inicio | Centro de partners de Microsoft"  
[MicrosoftPartnerDashboardWindowsOverview]: https://partner.microsoft.com/dashboard/windows/overview "Recursos para partners | Centro de partners de Microsoft"  

[MicrosoftStoreAppsWindows]: https://www.microsoft.com/store/apps/windows "Windows Apps | Microsoft Store"  

[WindowsBlogWindowsdeveloperHostedAppModel]: https://blogs.windows.com/windowsdeveloper/hosted-app-model "Hosted App Model | Blog para desarrolladores de Windows"  

[PwabuilderMain]: https://www.pwabuilder.com "PWABuilder"  

