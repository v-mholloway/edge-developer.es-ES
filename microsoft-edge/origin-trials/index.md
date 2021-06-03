---
ms.assetid: ''
description: Experimente de forma segura durante un período de tiempo fijo y proporcione comentarios sobre las nuevas características de la plataforma.
title: Pruebas de origen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge, desarrollo web, html, css, pruebas de origen, desarrollador
ms.openlocfilehash: cc03ec556d4b32ca37cebcd4ee7ba155bfe4404b
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397548"
---
# <a name="use-origin-trials-in-microsoft-edge"></a><span data-ttu-id="1816b-104">Usar pruebas de origen en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1816b-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="1816b-105">Los desarrolladores pueden usar las pruebas de Origin para probar api experimentales en sitios en directo durante un período de tiempo limitado.</span><span class="sxs-lookup"><span data-stu-id="1816b-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="1816b-106">Al usar las pruebas de origen, los usuarios de Microsoft Edge que visiten el sitio pueden ejecutar código que use API experimentales.</span><span class="sxs-lookup"><span data-stu-id="1816b-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="1816b-107">Para obtener acceso a las API experimentales en cada equipo de usuario, no es necesario ir a y activar `edge://flags` las marcas de características.</span><span class="sxs-lookup"><span data-stu-id="1816b-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="1816b-108">Para obtener más información, vaya a [API experimentales][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="1816b-108">For more information, navigate to [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="1816b-109">Además, puede proporcionar comentarios sobre el diseño de la API, los casos de uso o la experiencia con las API para ingenieros de exploradores y la comunidad estándar web.</span><span class="sxs-lookup"><span data-stu-id="1816b-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <a name="get-started-using-origin-trials"></a><span data-ttu-id="1816b-110">Introducción al uso de pruebas de Origin</span><span class="sxs-lookup"><span data-stu-id="1816b-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="1816b-111">Para obtener más información acerca de las API experimentales disponibles en Microsoft Edge, vaya [a Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="1816b-111">For more information about the experimental APIs available in Microsoft Edge, navigate to [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="1816b-112">Asegúrese de revisar los requisitos mínimos de versión Microsoft Edge y la fecha de finalización de la prueba para evaluar la idoneidad del uso de las API experimentales en su sitio web.</span><span class="sxs-lookup"><span data-stu-id="1816b-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="1816b-113">Un experimento puede finalizar antes de lo planeado si se produce alguna de las siguientes situaciones.</span><span class="sxs-lookup"><span data-stu-id="1816b-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="1816b-114">Un incidente de seguridad importante.</span><span class="sxs-lookup"><span data-stu-id="1816b-114">A major security incident.</span></span>  
> *   <span data-ttu-id="1816b-115">Si se recopilan suficientes comentarios que indican que se necesita un rediseño importante para satisfacer las necesidades de los desarrolladores web.</span><span class="sxs-lookup"><span data-stu-id="1816b-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="1816b-116">En cualquier caso, se envía un correo electrónico de notificación a todos los desarrolladores inscritos actualmente en el experimento.</span><span class="sxs-lookup"><span data-stu-id="1816b-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <a name="register-for-a-trial-of-an-experimental-api"></a><span data-ttu-id="1816b-117">Registrarse para una prueba de una API experimental</span><span class="sxs-lookup"><span data-stu-id="1816b-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="1816b-118">Siga estos pasos para registrarse para una prueba de una API experimental.</span><span class="sxs-lookup"><span data-stu-id="1816b-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="1816b-119">Visite la página Microsoft Edge Consola para [desarrolladores de pruebas de][DeveloperMicrsoftEdgeOriginTrials] origin.</span><span class="sxs-lookup"><span data-stu-id="1816b-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="1816b-120">Elija el botón Registrar en cualquiera de los experimentos disponibles.</span><span class="sxs-lookup"><span data-stu-id="1816b-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="1816b-121">Inicie sesión en la Consola de desarrollador con GitHub nombre de usuario y contraseña.</span><span class="sxs-lookup"><span data-stu-id="1816b-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="1816b-122">Elija **Autorizar MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="1816b-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="1816b-123">Complete el formulario.</span><span class="sxs-lookup"><span data-stu-id="1816b-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="1816b-124">Para inscribir un único o todos los subdominios, elija establecer la `Do you need to match all subdomains for the provided origin?` configuración en `Yes` .</span><span class="sxs-lookup"><span data-stu-id="1816b-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="1816b-125">Por ejemplo, `https://dev.contoso.com` es un dominio único y usa un `https://*.contoso.com` comodín para representar todos los subdominios.</span><span class="sxs-lookup"><span data-stu-id="1816b-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="1816b-126">No se permiten los siguientes formatos de origen.</span><span class="sxs-lookup"><span data-stu-id="1816b-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="1816b-127">Especificación de una subcarpeta en el origen.</span><span class="sxs-lookup"><span data-stu-id="1816b-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="1816b-128">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1816b-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="1816b-129">Uso de un origen con parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="1816b-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="1816b-130">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1816b-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="1816b-131">Elija **ACEPTAR y REGISTRAR**.</span><span class="sxs-lookup"><span data-stu-id="1816b-131">Choose **ACCEPT and REGISTER**.</span></span>  
    
### <a name="apply-your-token"></a><span data-ttu-id="1816b-132">Aplicar el token</span><span class="sxs-lookup"><span data-stu-id="1816b-132">Apply your token</span></span>  

<span data-ttu-id="1816b-133">Un token se genera de forma instantánea y se muestra en la Microsoft Edge Consola para desarrolladores de [pruebas de][DeveloperMicrsoftEdgeOriginTrials] Origin.</span><span class="sxs-lookup"><span data-stu-id="1816b-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="1816b-134">Para empezar a usar la prueba en su sitio web, use cualquiera de los siguientes métodos para aplicar el token a la página.</span><span class="sxs-lookup"><span data-stu-id="1816b-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="1816b-135">Agregue el `origin-trial` valor de atributo y el token a la etiqueta en cada página que use la API `meta` experimental.</span><span class="sxs-lookup"><span data-stu-id="1816b-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="1816b-136">Agregue `Origin-Trial` al encabezado de respuesta HTTP del servidor.</span><span class="sxs-lookup"><span data-stu-id="1816b-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="1816b-137">El token es válido durante 6 semanas.</span><span class="sxs-lookup"><span data-stu-id="1816b-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="1816b-138">Antes de que finalice la prueba, se le enviarán correos electrónicos de aviso que le pedirán sus comentarios y le pedirán que considere la posibilidad de renovar la prueba antes de que expire el token.</span><span class="sxs-lookup"><span data-stu-id="1816b-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <a name="opt-out-of-an-experiment"></a><span data-ttu-id="1816b-139">No participar en un experimento</span><span class="sxs-lookup"><span data-stu-id="1816b-139">Opt out of an experiment</span></span>  

<span data-ttu-id="1816b-140">Para no participar en un experimento, use uno de los siguientes métodos para quitar el token.</span><span class="sxs-lookup"><span data-stu-id="1816b-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="1816b-141">Quite la `meta` etiqueta de todas las páginas que usaron la API experimental.</span><span class="sxs-lookup"><span data-stu-id="1816b-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="1816b-142">Quite `Origin-Trial` del encabezado de respuesta HTTP del servidor.</span><span class="sxs-lookup"><span data-stu-id="1816b-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <a name="detect-experimental-features-and-provide-a-fallback"></a><span data-ttu-id="1816b-143">Detectar características experimentales y proporcionar una reserva</span><span class="sxs-lookup"><span data-stu-id="1816b-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="1816b-144">Al usar API experimentales, asegúrese de proporcionar una experiencia de trabajo a todos los visitantes de su sitio web.</span><span class="sxs-lookup"><span data-stu-id="1816b-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="1816b-145">Los visitantes pueden usar exploradores que no admiten las API experimentales que agregó al código.</span><span class="sxs-lookup"><span data-stu-id="1816b-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="1816b-146">Además, si el token expira antes de renovarlo, la API experimental ya no está disponible, lo que puede provocar errores.</span><span class="sxs-lookup"><span data-stu-id="1816b-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="1816b-147">Para evitar esta situación, asegúrese de detectar las características disponibles en el explorador.</span><span class="sxs-lookup"><span data-stu-id="1816b-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="1816b-148">Para obtener más información, vaya [a Implementar la detección de características][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="1816b-148">For more information, navigate to [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <a name="roadmap-for-allowed-origins"></a><span data-ttu-id="1816b-149">Guía básica para orígenes permitidos</span><span class="sxs-lookup"><span data-stu-id="1816b-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="1816b-150">El portal Microsoft Edge pruebas de origen actual solo admite orígenes habilitados para SSL, lo que significa que los sitios web deben tener HTTPS correctamente implementado para registrarse en un experimento.</span><span class="sxs-lookup"><span data-stu-id="1816b-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="1816b-151">En el futuro, se planean los siguientes orígenes seguros.</span><span class="sxs-lookup"><span data-stu-id="1816b-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="1816b-152">Registrarse `http://localhost` como origen de los experimentos.</span><span class="sxs-lookup"><span data-stu-id="1816b-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="1816b-153">Para usarlo `http://localhost` hoy, vaya a `edge://flags` y establezca el experimento en **Habilitado**.</span><span class="sxs-lookup"><span data-stu-id="1816b-153">To use `http://localhost` today, navigate to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="1816b-154">Use extensiones con `extensions://` orígenes con prefijo para inscribirse en experimentos.</span><span class="sxs-lookup"><span data-stu-id="1816b-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Microsoft Edge Origin Trials Developer Console | Microsoft Docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementación de la detección de características | MDN"  
