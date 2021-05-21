---
description: Información general sobre la creación y publicación de extensiones de Microsoft Edge (Chromium).
title: Información general sobre las extensiones de Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador, extensiones de chromium
ms.openlocfilehash: 3ed0871883acfb7c3cf08c2da9f47d18ae3465f0
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327529"
---
# <span data-ttu-id="69da2-104">Información general sobre las extensiones de Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="69da2-104">Overview of Microsoft Edge (Chromium) Extensions</span></span>  

<span data-ttu-id="69da2-105">Una extensión es un pequeño programa que \(un desarrollador\) usa para agregar o modificar características de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="69da2-105">An extension is a small program that you \(a developer\) use to add or modify features for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="69da2-106">Una extensión está pensada para mejorar la experiencia de exploración diaria de un usuario.</span><span class="sxs-lookup"><span data-stu-id="69da2-106">An extension is intended to improve a user's day-to-day browsing experience.</span></span>  <span data-ttu-id="69da2-107">Proporciona funcionalidad de nicho que es importante para un público objetivo.</span><span class="sxs-lookup"><span data-stu-id="69da2-107">It provides niche functionality that is important to a target audience.</span></span>  

<span data-ttu-id="69da2-108">Puedes crear una extensión si tienes una idea o un producto basado en cualquiera de las siguientes condiciones.</span><span class="sxs-lookup"><span data-stu-id="69da2-108">You may create an extension if you have an idea or product that is based upon either of the following conditions.</span></span>  

*   <span data-ttu-id="69da2-109">Un explorador web específico.</span><span class="sxs-lookup"><span data-stu-id="69da2-109">A specific web browser.</span></span>  
*   <span data-ttu-id="69da2-110">Mejoras en las características de páginas web específicas.</span><span class="sxs-lookup"><span data-stu-id="69da2-110">Improvements to features of specific webpages.</span></span>  
    
<span data-ttu-id="69da2-111">Algunos ejemplos de experiencias complementarias son los bloqueadores de anuncios y los administradores de contraseñas.</span><span class="sxs-lookup"><span data-stu-id="69da2-111">Examples of companion experiences include ad blockers and password managers.</span></span>  

<span data-ttu-id="69da2-112">Una extensión está estructurada de forma similar a una aplicación web normal.</span><span class="sxs-lookup"><span data-stu-id="69da2-112">An extension is structured similar to a regular web app.</span></span>  <span data-ttu-id="69da2-113">Como mínimo, debe incluir las siguientes características.</span><span class="sxs-lookup"><span data-stu-id="69da2-113">At a minimum, it should include the following features.</span></span>

*   <span data-ttu-id="69da2-114">Un archivo JSON de manifiesto de aplicación que contiene información básica de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="69da2-114">An app manifest JSON file that contains basic platform information.</span></span>  
*   <span data-ttu-id="69da2-115">Un archivo JavaScript que define la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="69da2-115">A JavaScript file that define functionality.</span></span>  
*   <span data-ttu-id="69da2-116">Archivos HTML y CSS que definen la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="69da2-116">HTML and CSS files that define the user interface.</span></span>  

<span data-ttu-id="69da2-117">Para trabajar directamente con parte del explorador, como una ventana o una pestaña, debe enviar solicitudes API y, a menudo, hacer referencia al explorador por su nombre.</span><span class="sxs-lookup"><span data-stu-id="69da2-117">To work directly with part of the browser, such as a window or tab, you must send API requests and often reference the browser by name.</span></span>  

:::image type="complex" source="./media/example-extension-screenshot.png" alt-text="Una extensión de Microsoft Edge (Chromium)" lightbox="./media/example-extension-screenshot.png":::
  <span data-ttu-id="69da2-119">Una extensión de Microsoft Edge \(Chromium\)</span><span class="sxs-lookup"><span data-stu-id="69da2-119">A Microsoft Edge \(Chromium\) extension</span></span>  
:::image-end:::  

## <span data-ttu-id="69da2-120">Instrucciones básicas</span><span class="sxs-lookup"><span data-stu-id="69da2-120">Basic guidance</span></span>  

<span data-ttu-id="69da2-121">Algunos de los exploradores más populares para crear extensiones incluyen Safari, Firefox, Chrome, Opera, Andy Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69da2-121">Some of the most popular browsers to build extensions for include Safari, Firefox, Chrome, Opera, Brave, and Microsoft Edge.</span></span>  <span data-ttu-id="69da2-122">Excelentes lugares para comenzar los tutoriales de desarrollo de extensiones y la investigación de documentación son los sitios hospedados por las organizaciones del explorador.</span><span class="sxs-lookup"><span data-stu-id="69da2-122">Great places to begin your extension development tutorials and documentation research are sites hosted by the browser organizations.</span></span>  <span data-ttu-id="69da2-123">La tabla siguiente no es definitiva y puede usarse como punto de partida.</span><span class="sxs-lookup"><span data-stu-id="69da2-123">The following table isn't definitive, and may be used as a starting point.</span></span>  

| <span data-ttu-id="69da2-124">Navegador web</span><span class="sxs-lookup"><span data-stu-id="69da2-124">Web browser</span></span> | <span data-ttu-id="69da2-125">¿Basado en Chromium?</span><span class="sxs-lookup"><span data-stu-id="69da2-125">Chromium-based?</span></span> | <span data-ttu-id="69da2-126">Página web de desarrollo de extensiones</span><span class="sxs-lookup"><span data-stu-id="69da2-126">Extension development webpage</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="69da2-127">Safari</span><span class="sxs-lookup"><span data-stu-id="69da2-127">Safari</span></span> | <span data-ttu-id="69da2-128">No</span><span class="sxs-lookup"><span data-stu-id="69da2-128">No</span></span> | [<span data-ttu-id="69da2-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span><span class="sxs-lookup"><span data-stu-id="69da2-129">developer.apple.com/documentation/safariservices/safari_app_extensions</span></span>][AppleDeveloperSafariservicesAppExtensions] |  
| <span data-ttu-id="69da2-130">Firefox</span><span class="sxs-lookup"><span data-stu-id="69da2-130">Firefox</span></span> | <span data-ttu-id="69da2-131">No</span><span class="sxs-lookup"><span data-stu-id="69da2-131">No</span></span> | [<span data-ttu-id="69da2-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span><span class="sxs-lookup"><span data-stu-id="69da2-132">developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions</span></span>][MDNWebextensions] |  
| <span data-ttu-id="69da2-133">Chrome</span><span class="sxs-lookup"><span data-stu-id="69da2-133">Chrome</span></span> | <span data-ttu-id="69da2-134">Sí</span><span class="sxs-lookup"><span data-stu-id="69da2-134">Yes</span></span> | [<span data-ttu-id="69da2-135">developer.chrome.com/extensions</span><span class="sxs-lookup"><span data-stu-id="69da2-135">developer.chrome.com/extensions</span></span>][ChromeDeveloperExtensions] |  
| <span data-ttu-id="69da2-136">Opera</span><span class="sxs-lookup"><span data-stu-id="69da2-136">Opera</span></span> | <span data-ttu-id="69da2-137">Sí</span><span class="sxs-lookup"><span data-stu-id="69da2-137">Yes</span></span> | [<span data-ttu-id="69da2-138">dev.opera.com/extensions</span><span class="sxs-lookup"><span data-stu-id="69da2-138">dev.opera.com/extensions</span></span>][OperaDevExtensions] |  
| <span data-ttu-id="69da2-139">Resalte</span><span class="sxs-lookup"><span data-stu-id="69da2-139">Brave</span></span> | <span data-ttu-id="69da2-140">Sí</span><span class="sxs-lookup"><span data-stu-id="69da2-140">Yes</span></span> | <span data-ttu-id="69da2-141">Usa [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span><span class="sxs-lookup"><span data-stu-id="69da2-141">Uses [Chrome Web Store][GoogleChromeWebstoreCategoryExtensions]</span></span> |  
| <span data-ttu-id="69da2-142">nuevo Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="69da2-142">new Microsoft Edge</span></span> | <span data-ttu-id="69da2-143">Sí</span><span class="sxs-lookup"><span data-stu-id="69da2-143">Yes</span></span> | [<span data-ttu-id="69da2-144">developer.microsoft.com/microsoft-edge/extensions</span><span class="sxs-lookup"><span data-stu-id="69da2-144">developer.microsoft.com/microsoft-edge/extensions</span></span>][MicrosoftDeveloperEdgeExtensions] |  

> [!IMPORTANT]
> <span data-ttu-id="69da2-145">Muchos de los tutoriales de los sitios usan API específicas del explorador que pueden no coincidir con el explorador para el que desarrolla.</span><span class="sxs-lookup"><span data-stu-id="69da2-145">Many of the tutorials of the sites use browser-specific APIs that may not match the browser for which you develop.</span></span>  <span data-ttu-id="69da2-146">En la mayoría de los casos, una extensión chromium funciona tal como está en diferentes exploradores de Chromium y las API funcionan según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="69da2-146">In most cases, a Chromium extension works as-is in different Chromium browsers and the APIs work as expected.</span></span>  <span data-ttu-id="69da2-147">Solo algunas API menos comunes pueden ser estrictamente específicas del explorador.</span><span class="sxs-lookup"><span data-stu-id="69da2-147">Only some less common APIs may be strictly browser-specific.</span></span>  <span data-ttu-id="69da2-148">Para obtener vínculos a los tutoriales, vaya [a Ver también.](#see-also)</span><span class="sxs-lookup"><span data-stu-id="69da2-148">For links to the tutorials, navigate to [See also](#see-also).</span></span>  

## <span data-ttu-id="69da2-149">¿Por qué Chromium?</span><span class="sxs-lookup"><span data-stu-id="69da2-149">Why Chromium?</span></span>  

<span data-ttu-id="69da2-150">Si el objetivo es publicar la extensión en el almacén de extensiones de cada explorador, debe modificarse para que cada versión tenga como destino y se ejecute en cada entorno de explorador distinto.</span><span class="sxs-lookup"><span data-stu-id="69da2-150">If your goal is to publish your extension in the extensions store for each browser, it must be modified for each version to target and run in each distinct browser environment.</span></span>  <span data-ttu-id="69da2-151">Por ejemplo, [las extensiones Safari pueden][AppleDeveloperSafariservicesAppExtensions] usar código web y nativo para comunicarse con aplicaciones nativas equivalentes.</span><span class="sxs-lookup"><span data-stu-id="69da2-151">For example, [Safari extensions][AppleDeveloperSafariservicesAppExtensions] may use both web and native code to communicate with counterpart native applications.</span></span>  <span data-ttu-id="69da2-152">Los últimos cuatro exploradores de la tabla anterior usan el mismo paquete de código y minimizan el requisito de mantener versiones paralelas.</span><span class="sxs-lookup"><span data-stu-id="69da2-152">The last four browsers in the previous table use the same code package, and minimizes the requirement to maintain parallel versions.</span></span>  <span data-ttu-id="69da2-153">Estos exploradores se basan en [el proyecto de código abierto chromium.][|::ref1::|Home]</span><span class="sxs-lookup"><span data-stu-id="69da2-153">These browsers are based on the [Chromium open-source project][|::ref1::|Home].</span></span>  

<span data-ttu-id="69da2-154">Crea una extensión chromium para escribir la menor cantidad de código.</span><span class="sxs-lookup"><span data-stu-id="69da2-154">Create a Chromium extension to write the least amount of code.</span></span>  <span data-ttu-id="69da2-155">También se dirige al número máximo de almacenes de extensiones y, en última instancia, al número máximo de usuarios que encuentran y adquieren la extensión.</span><span class="sxs-lookup"><span data-stu-id="69da2-155">It also targets the maximum number of extension stores and ultimately the maximum number of users who find and acquire your extension.</span></span>  

<span data-ttu-id="69da2-156">El siguiente contenido se centra principalmente en las extensiones de Chromium.</span><span class="sxs-lookup"><span data-stu-id="69da2-156">The following content focuses mostly on Chromium extensions.</span></span>  

## <span data-ttu-id="69da2-157">Pruebas de compatibilidad y extensión del explorador</span><span class="sxs-lookup"><span data-stu-id="69da2-157">Browser compatibility and extension testing</span></span>  

<span data-ttu-id="69da2-158">En ocasiones, la paridad de api no existe entre los exploradores chromium.</span><span class="sxs-lookup"><span data-stu-id="69da2-158">Occasionally, API parity doesn't exist between Chromium browsers.</span></span>  <span data-ttu-id="69da2-159">Por ejemplo, existen diferencias en las API de identidad y pago.</span><span class="sxs-lookup"><span data-stu-id="69da2-159">For example, there are differences in the identity and payment APIs.</span></span>  <span data-ttu-id="69da2-160">Para asegurarse de que la extensión cumple las expectativas del cliente, revise el estado de la API a través de los siguientes documentos oficiales del explorador.</span><span class="sxs-lookup"><span data-stu-id="69da2-160">To ensure your extension meets customer expectations, review API status through the following official browser docs.</span></span>  

*   [<span data-ttu-id="69da2-161">API de Chrome</span><span class="sxs-lookup"><span data-stu-id="69da2-161">Chrome APIs</span></span>][ChromeDeveloperExtensionsApiIndex]  
*   [<span data-ttu-id="69da2-162">API de extensión admitidas en Opera</span><span class="sxs-lookup"><span data-stu-id="69da2-162">Extension APIs supported in Opera</span></span>][OperaDevExtensionsApis]  
*   [<span data-ttu-id="69da2-163">Extensión port Chrome a Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="69da2-163">Port Chrome extension to Microsoft Edge (Chromium)</span></span>][ExtensionsChromiumDeveloperGuidePortChrome]  
    
<span data-ttu-id="69da2-164">Las API que necesita definir los cambios que debe realizar para abordar las diferencias entre cada explorador.</span><span class="sxs-lookup"><span data-stu-id="69da2-164">The APIs you require define the changes you must make to address the differences between each browser.</span></span>  <span data-ttu-id="69da2-165">Esto puede significar que debes crear paquetes de código ligeramente diferentes con pequeñas diferencias para cada tienda.</span><span class="sxs-lookup"><span data-stu-id="69da2-165">It may mean that you must create slightly different code packages with small differences for each store.</span></span>  

<span data-ttu-id="69da2-166">Para probar la extensión en diferentes entornos antes de enviarla a un almacén de explorador, cándala localmente en el explorador mientras la desarrolla.</span><span class="sxs-lookup"><span data-stu-id="69da2-166">To test your extension in different environments before you submit it to a browser store, sideload it into your browser while you develop it.</span></span>  

## <span data-ttu-id="69da2-167">Publicar la extensión en almacenes de exploradores</span><span class="sxs-lookup"><span data-stu-id="69da2-167">Publish your extension to browser stores</span></span>  

<span data-ttu-id="69da2-168">Puede enviar y buscar extensiones de explorador en los siguientes almacenes de explorador.</span><span class="sxs-lookup"><span data-stu-id="69da2-168">You may submit and seek browser extensions in the following browser stores.</span></span>  

*   [<span data-ttu-id="69da2-169">Complementos del explorador Firefox</span><span class="sxs-lookup"><span data-stu-id="69da2-169">Firefox Browser Add-ons</span></span>][MozillaAddonsFirefoxExtensions]  
*   [<span data-ttu-id="69da2-170">Chrome Web Store</span><span class="sxs-lookup"><span data-stu-id="69da2-170">Chrome Web Store</span></span>][GoogleChromeWebstoreCategoryExtensions]  
*   [<span data-ttu-id="69da2-171">Complementos de Opera</span><span class="sxs-lookup"><span data-stu-id="69da2-171">Opera addons</span></span>][OperaAddonsExtensions]  
*   [<span data-ttu-id="69da2-172">Complementos de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="69da2-172">Microsoft Edge Add-ons</span></span>][MicrosoftEdgeAddonsCategoryExtensions]  

<span data-ttu-id="69da2-173">Algunos almacenes le permiten descargar extensiones enumeradas de otros exploradores.</span><span class="sxs-lookup"><span data-stu-id="69da2-173">Some stores allow you to download listed extensions from other browsers.</span></span>  <span data-ttu-id="69da2-174">Sin embargo, los almacenes de explorador no garantizan el acceso entre exploradores.</span><span class="sxs-lookup"><span data-stu-id="69da2-174">However, cross-browser access is not guaranteed by browser stores.</span></span>  <span data-ttu-id="69da2-175">Para asegurarse de que los usuarios encuentran la extensión en diferentes exploradores, debe mantener una lista en cada almacén de extensiones de explorador.</span><span class="sxs-lookup"><span data-stu-id="69da2-175">To ensure your users find your extension in different browsers, you should maintain a listing on each browser extension store.</span></span>  

<span data-ttu-id="69da2-176">Es posible que los usuarios deba instalar la extensión en diferentes exploradores.</span><span class="sxs-lookup"><span data-stu-id="69da2-176">Users may need to install your extension in different browsers.</span></span> <span data-ttu-id="69da2-177">En este escenario, puedes migrar las extensiones de Chromium existentes de un explorador a otro.</span><span class="sxs-lookup"><span data-stu-id="69da2-177">In this scenario, you may migrate existing Chromium extensions from one browser to another.</span></span>  

### <span data-ttu-id="69da2-178">Migrar una extensión existente a Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="69da2-178">Migrate an existing extension to Microsoft Edge</span></span>  

<span data-ttu-id="69da2-179">Si ya has desarrollado una extensión para otro explorador Chromium, puedes enviarla a la tienda de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69da2-179">If you've already developed an extension for another Chromium browser, you may submit it to the Microsoft Edge Add-ons store.</span></span> <span data-ttu-id="69da2-180">No es necesario reescribir la extensión y comprobar que funciona en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69da2-180">You don't need to rewrite your extension, and must verify it works in Microsoft Edge.</span></span>  <span data-ttu-id="69da2-181">Al migrar una extensión de Chromium existente a otros exploradores de Chromium, asegúrate de que las mismas API o alternativas estén disponibles para el explorador de destino.</span><span class="sxs-lookup"><span data-stu-id="69da2-181">When you migrate an existing Chromium extension to other Chromium browsers, ensure the same APIs or alternatives are available for your target browser.</span></span>  

<span data-ttu-id="69da2-182">Para obtener más información sobre cómo portabilidad de la extensión de Chrome a Microsoft Edge, vaya a Extensiones de Port Chrome a [Microsoft Edge (Chromium).][ExtensionsChromiumDeveloperGuidePortChrome]</span><span class="sxs-lookup"><span data-stu-id="69da2-182">For more information on porting your Chrome extension to Microsoft Edge, navigate to [Port Chrome extensions to Microsoft Edge (Chromium)][ExtensionsChromiumDeveloperGuidePortChrome].</span></span> <span data-ttu-id="69da2-183">Después de portabilidad de la extensión al explorador de destino, el siguiente paso es publicarla.</span><span class="sxs-lookup"><span data-stu-id="69da2-183">After you port your extension to the target browser, the next step is to publish it.</span></span>  

### <span data-ttu-id="69da2-184">Publicar en el sitio web de complementos de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="69da2-184">Publish to the Microsoft Edge add-ons website</span></span>  

<span data-ttu-id="69da2-185">Para empezar a publicar la extensión en Microsoft Edge, debes registrarte para obtener una cuenta de desarrollador con una cuenta de correo electrónico de MSA para enviar la descripción de la extensión [a][MicrosoftDeveloperRegistration] la tienda.</span><span class="sxs-lookup"><span data-stu-id="69da2-185">To start publishing your extension to Microsoft Edge, you must [register for a developer account][MicrosoftDeveloperRegistration] with an MSA email account to submit your extension listing to the store.</span></span>  <span data-ttu-id="69da2-186">Una cuenta de correo electrónico de MSA `@outlook.com` `@live.com` incluye, y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="69da2-186">An MSA email account includes `@outlook.com`, `@live.com`, and so on.</span></span>  <span data-ttu-id="69da2-187">Cuando elija una dirección de correo electrónico para registrarse, considere si debe transferir o compartir la propiedad de la extensión con otras personas de su organización.</span><span class="sxs-lookup"><span data-stu-id="69da2-187">When you choose an email address to register, consider if you must transfer or share ownership of the extension with others in your organization.</span></span>  <span data-ttu-id="69da2-188">Una vez completado el registro, puedes crear un nuevo envío de extensión a la tienda.</span><span class="sxs-lookup"><span data-stu-id="69da2-188">After registration is complete, you may create a new extension submission to the store.</span></span>  

<span data-ttu-id="69da2-189">Para enviar la extensión a la tienda, asegúrate de proporcionar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="69da2-189">To submit your extension to the store, ensure you provide the following items.</span></span>  

*   <span data-ttu-id="69da2-190">Un archivo \( `.zip` \) que contiene los archivos de código.</span><span class="sxs-lookup"><span data-stu-id="69da2-190">An archive \(`.zip`\) file that contains your code files.</span></span>  
*   <span data-ttu-id="69da2-191">Todos los activos visuales necesarios, que incluyen un logotipo y un icono promocional pequeño.</span><span class="sxs-lookup"><span data-stu-id="69da2-191">All required visual assets, which include a logo and small promotional tile.</span></span>  
*   <span data-ttu-id="69da2-192">Medios promocionales opcionales, como capturas de pantalla, iconos promocionales y una dirección URL de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69da2-192">Optional promotional media, such as screenshots, promotional tiles, and a video URL.</span></span>  
*   <span data-ttu-id="69da2-193">Información que describe la extensión, como el nombre, la descripción breve y un vínculo de directiva de privacidad.</span><span class="sxs-lookup"><span data-stu-id="69da2-193">Information that describes your extension such as the name, short description, and a privacy policy link.</span></span>  

> [!NOTE]
> <span data-ttu-id="69da2-194">Es posible que diferentes almacenes tengan requisitos de envío diferentes.</span><span class="sxs-lookup"><span data-stu-id="69da2-194">Different stores may have different submission requirements.</span></span>  <span data-ttu-id="69da2-195">En la lista anterior se resumen los [requisitos][ExtensionsChromiumPublish] para publicar una extensión para Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="69da2-195">The above list summarizes the [requirements][ExtensionsChromiumPublish] to publish an extension for Microsoft Edge.</span></span>  

<span data-ttu-id="69da2-196">Después de enviar correctamente la extensión, la extensión se somete a un proceso de revisión y pasa o no el proceso de certificación.</span><span class="sxs-lookup"><span data-stu-id="69da2-196">After you've successfully submitted your extension, your extension undergoes a review process and either passes or fails the certification process.</span></span>  <span data-ttu-id="69da2-197">A los propietarios se les notifica el resultado y se les indican los pasos siguientes según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="69da2-197">Owners are notified of the outcome and given next steps as required.</span></span>  <span data-ttu-id="69da2-198">Si envías una actualización de extensión a la tienda, se inicia un nuevo proceso de revisión.</span><span class="sxs-lookup"><span data-stu-id="69da2-198">If you submit an extension update to the store, a new review process is started.</span></span>  

## <a name="see-also"></a><span data-ttu-id="69da2-199">Consulte también</span><span class="sxs-lookup"><span data-stu-id="69da2-199">See also</span></span>  

*   [<span data-ttu-id="69da2-200">Portabilidad de una extensión de Google Chrome</span><span class="sxs-lookup"><span data-stu-id="69da2-200">Port a Google Chrome extension</span></span>][ExtensionworkshopPorting]  
*   [<span data-ttu-id="69da2-201">Crear una extensión de aplicación Safari</span><span class="sxs-lookup"><span data-stu-id="69da2-201">Build a Safari App extension</span></span>][AppleDeveloperSafariservicesAppExtensionsBuilding]  
*   [<span data-ttu-id="69da2-202">Su primera extensión (Firefox)</span><span class="sxs-lookup"><span data-stu-id="69da2-202">Your first extension (Firefox)</span></span>][MDNWebextensionsYourFirst]  
*   [<span data-ttu-id="69da2-203">Tutorial de introducción (Chrome)</span><span class="sxs-lookup"><span data-stu-id="69da2-203">Get started tutorial (Chrome)</span></span>][ChromeDeveloperExtensionsGetstarted]  
*   [<span data-ttu-id="69da2-204">Introducción (Opera)</span><span class="sxs-lookup"><span data-stu-id="69da2-204">Get started (Opera)</span></span>][OperaDevExtensionsGettingStarted]  
*   [<span data-ttu-id="69da2-205">Introducción a las extensiones de Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="69da2-205">Get started with Microsoft Edge (Chromium) extensions</span></span>][ExtensionsChromiumGettingStartedIndex]  

<!-- links -->  

[ExtensionsChromiumDeveloperGuidePortChrome]: ./developer-guide/port-chrome-extension.md "Port Chrome Extension to Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumGettingStartedIndex]: ./getting-started/index.md "Introducción a las extensiones de Microsoft Edge (Chromium) | Microsoft Docs"  
[ExtensionsChromiumPublish]: ./publish/publish-extension.md "Publicar una extensión | Microsoft Docs"  

[MicrosoftDeveloperEdgeExtensions]: https://developer.microsoft.com/microsoft-edge/extensions "Desarrollar extensiones para Microsoft Edge | Microsoft Developer"  
[MicrosoftDeveloperRegistration]: https://developer.microsoft.com/registration "Centro de partners | Microsoft Developer"  

[MicrosoftEdgeAddonsCategoryExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Extensiones para Microsoft Edge | Microsoft Edge"  

[AppleDeveloperSafariservicesAppExtensions]: https://developer.apple.com/documentation/safariservices/safari_app_extensions "Extensiones de la aplicación Safari | Desarrollador de Apple"  
[AppleDeveloperSafariservicesAppExtensionsBuilding]: https://developer.apple.com/documentation/safariservices/safari_app_extensions/building_a_safari_app_extension "Creación de una extensión de aplicación de Safari | Desarrollador de Apple"  

[ChromeDeveloperExtensions]: https://developer.chrome.com/extensions "¿Qué son las extensiones? | Chrome Developer"  
[ChromeDeveloperExtensionsApiIndex]: https://developer.chrome.com/extensions/api_index "Api de Chrome | Chrome Developer"  
[ChromeDeveloperExtensionsGetstarted]: https://developer.chrome.com/extensions/getstarted "Tutorial de introducción | Chrome Developer"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium"  

[ExtensionworkshopPorting]: https://extensionworkshop.com/documentation/develop/porting-a-google-chrome-extension "Porting a Google Chrome extension | Taller de extensión"  

[GoogleChromeWebstoreCategoryExtensions]: https://chrome.google.com/webstore/category/extensions "Extensiones | Chrome Web Store"  

[MDNWebextensions]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions "Extensiones del explorador | MDN"  
[MDNWebextensionsYourFirst]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/Your_first_WebExtension "La primera extensión | MDN"  

[MozillaAddonsFirefoxExtensions]: https://addons.mozilla.org/firefox/extensions "Extensiones | Complementos para Firefox"  

[OperaAddonsExtensions]: https://addons.opera.com/extensions "Extensiones | Complementos de Opera"  

[OperaDevExtensions]: https://dev.opera.com/extensions "Documentación de extensiones | Dev. Opera"  
[OperaDevExtensionsApis]: https://dev.opera.com/extensions/apis "API de extensión admitidas en Opera | Dev. Opera"  
[OperaDevExtensionsGettingStarted]: https://dev.opera.com/extensions/getting-started "Introducción a | Dev. Opera"  
