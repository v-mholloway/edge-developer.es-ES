---
ms.assetid: ''
description: Experimentos con seguridad durante un período de tiempo fijo y proporciona comentarios sobre las nuevas características de las plataformas.
title: Pruebas de Origen
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, pruebas de origen, desarrollador
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846531"
---
# <span data-ttu-id="0860d-104">Usar pruebas de origen en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0860d-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="0860d-105">Los programadores pueden usar pruebas de origen para probar las API experimentales en sitios activos durante un período de tiempo limitado.</span><span class="sxs-lookup"><span data-stu-id="0860d-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="0860d-106">Al usar las pruebas de origen, los usuarios de Microsoft Edge que visitan su sitio pueden ejecutar código que usa las API experimentales.</span><span class="sxs-lookup"><span data-stu-id="0860d-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="0860d-107">Para obtener acceso a las API experimentales de cada equipo de usuario, no es necesario ir a `edge://flags` y activar las marcas de características.</span><span class="sxs-lookup"><span data-stu-id="0860d-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="0860d-108">Para obtener más información, consulte [API experimentales][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="0860d-108">For more information, see [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="0860d-109">Además, puede proporcionar comentarios sobre el diseño de la API, sus casos de uso o su experiencia con las API para ingenieros del explorador y la comunidad estándar Web.</span><span class="sxs-lookup"><span data-stu-id="0860d-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <span data-ttu-id="0860d-110">Empezar a usar las pruebas de origen</span><span class="sxs-lookup"><span data-stu-id="0860d-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="0860d-111">Para obtener más información sobre las API experimentales disponibles en Microsoft Edge, consulta la [consola de desarrollo de pruebas de origen de Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="0860d-111">For more information about the experimental APIs available in Microsoft Edge, see [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="0860d-112">Asegúrese de revisar los requisitos de versión mínima de Microsoft Edge y la fecha de finalización de la prueba para evaluar la idoneidad del uso de las API experimentales en su sitio Web.</span><span class="sxs-lookup"><span data-stu-id="0860d-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="0860d-113">Un experimento puede finalizar antes de lo planeado si se produce alguna de las situaciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="0860d-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="0860d-114">Un incidente de seguridad importante.</span><span class="sxs-lookup"><span data-stu-id="0860d-114">A major security incident.</span></span>  
> *   <span data-ttu-id="0860d-115">Si se recopilan los comentarios suficientes que indican que es necesario un rediseño importante para satisfacer las necesidades de los programadores de Internet.</span><span class="sxs-lookup"><span data-stu-id="0860d-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="0860d-116">En cualquiera de los casos, se envía una notificación por correo electrónico a todos los desarrolladores actualmente inscritos en el experimento.</span><span class="sxs-lookup"><span data-stu-id="0860d-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <span data-ttu-id="0860d-117">Registrarse para una prueba de una API experimental</span><span class="sxs-lookup"><span data-stu-id="0860d-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="0860d-118">Siga estos pasos para registrar una prueba de una API experimental.</span><span class="sxs-lookup"><span data-stu-id="0860d-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="0860d-119">Visite la página de la [consola de desarrollo de versiones de prueba de Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .</span><span class="sxs-lookup"><span data-stu-id="0860d-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="0860d-120">Elija el botón registrar en cualquiera de los experimentos disponibles.</span><span class="sxs-lookup"><span data-stu-id="0860d-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="0860d-121">Inicia sesión en la consola del desarrollador con tu nombre de usuario y contraseña de GitHub.</span><span class="sxs-lookup"><span data-stu-id="0860d-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="0860d-122">Elija **autorizar MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="0860d-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="0860d-123">Complete el formulario.</span><span class="sxs-lookup"><span data-stu-id="0860d-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="0860d-124">Para inscribir uno o todos los subdominios, elija establecer la `Do you need to match all subdomains for the provided origin?` configuración en `Yes` .</span><span class="sxs-lookup"><span data-stu-id="0860d-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="0860d-125">Por ejemplo, `https://dev.contoso.com` es un solo dominio y `https://*.contoso.com` usa un carácter comodín para representar todos los subdominios.</span><span class="sxs-lookup"><span data-stu-id="0860d-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="0860d-126">No se permiten los siguientes formatos de origen.</span><span class="sxs-lookup"><span data-stu-id="0860d-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="0860d-127">Especificar una subcarpeta en el origen.</span><span class="sxs-lookup"><span data-stu-id="0860d-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="0860d-128">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0860d-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="0860d-129">Usar un origen con parámetros de cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="0860d-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="0860d-130">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0860d-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="0860d-131">Elija **Aceptar y registrar**.</span><span class="sxs-lookup"><span data-stu-id="0860d-131">Choose **ACCEPT and REGISTER**.</span></span>  

### <span data-ttu-id="0860d-132">Aplicar tu token</span><span class="sxs-lookup"><span data-stu-id="0860d-132">Apply your token</span></span>  

<span data-ttu-id="0860d-133">Se genera un token de forma instantánea y se muestra en la página de la [consola de desarrollador de Microsoft Edge de origen][DeveloperMicrsoftEdgeOriginTrials] .</span><span class="sxs-lookup"><span data-stu-id="0860d-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="0860d-134">Para empezar a usar la versión de prueba en su sitio web, use uno de los métodos siguientes para aplicar el token a la página.</span><span class="sxs-lookup"><span data-stu-id="0860d-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="0860d-135">Agregue el `origin-trial` valor de atributo y el token a la `meta` etiqueta en todas las páginas que usen la API experimental.</span><span class="sxs-lookup"><span data-stu-id="0860d-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="0860d-136">Agregar `Origin-Trial` al encabezado de respuesta HTTP del servidor.</span><span class="sxs-lookup"><span data-stu-id="0860d-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="0860d-137">Tu token es válido durante 6 semanas.</span><span class="sxs-lookup"><span data-stu-id="0860d-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="0860d-138">Antes de que finalice el período de prueba, te enviaremos recordatorio por correo electrónico que te pidan tus comentarios y te pidan que consideres la posibilidad de renovar la prueba antes de que venza el token.</span><span class="sxs-lookup"><span data-stu-id="0860d-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <span data-ttu-id="0860d-139">No participar en un experimento</span><span class="sxs-lookup"><span data-stu-id="0860d-139">Opt out of an experiment</span></span>  

<span data-ttu-id="0860d-140">Para no participar en un experimento, usa uno de los siguientes métodos para quitar tu token.</span><span class="sxs-lookup"><span data-stu-id="0860d-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="0860d-141">Quite la `meta` etiqueta de todas las páginas que usaron la API experimental.</span><span class="sxs-lookup"><span data-stu-id="0860d-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="0860d-142">Quitar `Origin-Trial` del encabezado de respuesta HTTP del servidor.</span><span class="sxs-lookup"><span data-stu-id="0860d-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <span data-ttu-id="0860d-143">Detectar características experimentales y proporcionar un respaldo</span><span class="sxs-lookup"><span data-stu-id="0860d-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="0860d-144">Cuando uses las API experimentales, asegúrate de proporcionar una experiencia laboral a todos los visitantes de tu sitio Web.</span><span class="sxs-lookup"><span data-stu-id="0860d-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="0860d-145">Los visitantes pueden usar exploradores que no sean compatibles con las API experimentales que agregó al código.</span><span class="sxs-lookup"><span data-stu-id="0860d-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="0860d-146">Además, si tu token vence antes de renovarlo, la API experimental ya no está disponible, lo que puede provocar errores.</span><span class="sxs-lookup"><span data-stu-id="0860d-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="0860d-147">Para evitar esta situación, asegúrese de que detecta las características disponibles en el explorador.</span><span class="sxs-lookup"><span data-stu-id="0860d-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="0860d-148">Para obtener más información, consulte implementación de la [detección de características][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="0860d-148">For more information, see [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <span data-ttu-id="0860d-149">Guía básica para orígenes permitidos</span><span class="sxs-lookup"><span data-stu-id="0860d-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="0860d-150">El portal de versiones de prueba de Microsoft Edge solo admite orígenes habilitados para SSL, lo que significa que los sitios web deben tener HTTPS correctamente implementados para registrarse en un experimento.</span><span class="sxs-lookup"><span data-stu-id="0860d-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="0860d-151">En el futuro, se planean los siguientes orígenes seguros.</span><span class="sxs-lookup"><span data-stu-id="0860d-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="0860d-152">Regístrate `http://localhost` como el origen de tus experimentos.</span><span class="sxs-lookup"><span data-stu-id="0860d-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="0860d-153">Para usar `http://localhost` hoy, vaya a `edge://flags` y establezca el experimento en **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="0860d-153">To use `http://localhost` today, go to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="0860d-154">Use extensiones con `extensions://` orígenes con prefijo para inscribirse en experimentos.</span><span class="sxs-lookup"><span data-stu-id="0860d-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Prueba de Microsoft Edge origen consola de desarrollador | Microsoft docs"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Implementación de la detección de características | MDN"  
