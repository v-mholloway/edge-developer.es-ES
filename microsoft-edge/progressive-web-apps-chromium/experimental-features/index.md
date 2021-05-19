---
description: Las últimas características experimentales de Microsoft Edge para aplicaciones web
title: Características experimentales | Aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 4a50b925e002746357b2b770b199d84772b456f5
ms.sourcegitcommit: bbbf722067f1d255f59ab384e66798f8b77ef609
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "11574592"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a><span data-ttu-id="b6a27-104">Características experimentales en aplicaciones web progresivas (PWA)</span><span class="sxs-lookup"><span data-stu-id="b6a27-104">Experimental features in Progressive Web Apps (PWAs)</span></span>  

<span data-ttu-id="b6a27-105">Microsoft Edge proporciona acceso a características experimentales que aún están en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-105">Microsoft Edge provides access to experimental features that are still in development.</span></span>  <span data-ttu-id="b6a27-106">Para determinar si cada característica está lista y cuándo liberar cada una, pruebe y [proporcione comentarios](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="b6a27-106">To determine if each feature is ready and when to release each, test and [provide feedback](#providing-feedback-on-experimental-features).</span></span>  

<span data-ttu-id="b6a27-107">Las características experimentales están disponibles en todos los canales de Microsoft Edge, pero las características experimentales más recientes solo están disponibles en el canal Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="b6a27-107">Experimental features are available in all channels of Microsoft Edge, but the latest experimental features are only available in the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="b6a27-108">Activar características experimentales</span><span class="sxs-lookup"><span data-stu-id="b6a27-108">Turn on experimental features</span></span>  

<span data-ttu-id="b6a27-109">Para activar las características experimentales \(or off\) en Microsoft Edge, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="b6a27-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  
  
1.  <span data-ttu-id="b6a27-110">Abra Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b6a27-110">Open Microsoft Edge.</span></span>   
    
    > [!NOTE]
    > <span data-ttu-id="b6a27-111">Asegúrese de usar una Microsoft Edge que tenga el experimento enumerado en este artículo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-111">Ensure you use a Microsoft Edge version that has the Experiment listed in this article.</span></span>  <span data-ttu-id="b6a27-112">Vaya a [Características experimentales](#features-that-are-available-to-test).</span><span class="sxs-lookup"><span data-stu-id="b6a27-112">Navigate to [Experimental features](#features-that-are-available-to-test).</span></span>  
    
1.  <span data-ttu-id="b6a27-113">Vaya a `edge://flags`.</span><span class="sxs-lookup"><span data-stu-id="b6a27-113">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="b6a27-114">Vaya al experimento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b6a27-114">Navigate to the relevant experiment.</span></span>  
1.  <span data-ttu-id="b6a27-115">Elija el menú desplegable junto a la descripción del experimento y elija `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-115">Choose the dropdown menu next to the experiment description and choose `Enabled`.</span></span>  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Elija Habilitado para activar un experimento" lightbox="../media/turn-on-experimental-flag.png":::
       <span data-ttu-id="b6a27-117">Elija **Habilitado** para activar un experimento</span><span class="sxs-lookup"><span data-stu-id="b6a27-117">Choose **Enabled** to turn on an experiment</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="b6a27-118">Cada experimento suele tener un menú desplegable para elegir los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="b6a27-118">Each experiment usually has a dropdown menu to choose the following values.</span></span>  <span data-ttu-id="b6a27-119">Si una característica experimental no tiene una entrada en **Experimentos,** se proporcionan instrucciones para iniciar Microsoft Edge con esa característica mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b6a27-119">If an experimental feature doesn't have an entry on **Experiments**, instructions are provided to start Microsoft Edge with that feature using the command-line.</span></span>
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  <span data-ttu-id="b6a27-120">Reiniciar Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b6a27-120">Restart Microsoft Edge.</span></span>  
    
### <a name="origin-trials"></a><span data-ttu-id="b6a27-121">Pruebas de origen</span><span class="sxs-lookup"><span data-stu-id="b6a27-121">Origin Trials</span></span>  

<span data-ttu-id="b6a27-122">Microsoft Edge a veces usa pruebas de origen para probar características para dominios o sitios web específicos.</span><span class="sxs-lookup"><span data-stu-id="b6a27-122">Microsoft Edge sometimes uses origin trials to test features for specific domains or websites.</span></span>  <span data-ttu-id="b6a27-123">Es posible que desee usar una versión de prueba de origen para su sitio web para aplicar una característica específica.</span><span class="sxs-lookup"><span data-stu-id="b6a27-123">You may want to use an origin trial for your website to apply a specific feature.</span></span>  <span data-ttu-id="b6a27-124">Si es propietario de un sitio web, puede inscribirse en una prueba de origen.</span><span class="sxs-lookup"><span data-stu-id="b6a27-124">If you're a website owner, you may enroll in an origin trial.</span></span>  <span data-ttu-id="b6a27-125">Una versión de prueba de origen proporciona características a un porcentaje Microsoft Edge usuarios que visitan su sitio web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-125">An origin trial provides features to a percentage of Microsoft Edge users who visit your website.</span></span>

<span data-ttu-id="b6a27-126">Para obtener más información acerca de las pruebas de Origin, [vaya a Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="b6a27-126">For more information about Origin Trials, navigate to [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="b6a27-127">Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6a27-127">Experimental features are constantly updated and may cause performance issues.</span></span>  <span data-ttu-id="b6a27-128">Para desactivar una característica experimental, vaya a [Activar características experimentales,](#turn-on-experimental-features)vaya al experimento y, a continuación, elija `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-128">To turn off an experimental feature, navigate to [Turn on experimental features](#turn-on-experimental-features), navigate to the experiment, and then choose `Disabled`.</span></span>  

## <a name="features-that-are-available-to-test"></a><span data-ttu-id="b6a27-129">Características que están disponibles para probar</span><span class="sxs-lookup"><span data-stu-id="b6a27-129">Features that are available to test</span></span>  

<span data-ttu-id="b6a27-130">En la siguiente lista se describen las nuevas características experimentales de la aplicación web que están disponibles para probar y validar en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b6a27-130">The following list describes the new experimental web app features that are available to test and validate on Microsoft Edge.</span></span>  

| <span data-ttu-id="b6a27-131">Característica</span><span class="sxs-lookup"><span data-stu-id="b6a27-131">Feature</span></span> | <span data-ttu-id="b6a27-132">Microsoft Edge versión</span><span class="sxs-lookup"><span data-stu-id="b6a27-132">Microsoft Edge version</span></span> | <span data-ttu-id="b6a27-133">Plataforma</span><span class="sxs-lookup"><span data-stu-id="b6a27-133">Platform</span></span> |  
|:--- |:--- |:--- |  
| [<span data-ttu-id="b6a27-134">Administración del protocolo URI</span><span class="sxs-lookup"><span data-stu-id="b6a27-134">URI Protocol Handling</span></span>](#uri-protocol-handling) | <span data-ttu-id="b6a27-135">91 o posterior</span><span class="sxs-lookup"><span data-stu-id="b6a27-135">91 or later</span></span> | <span data-ttu-id="b6a27-136">Windows y Linux</span><span class="sxs-lookup"><span data-stu-id="b6a27-136">Windows and Linux</span></span> |    
| [<span data-ttu-id="b6a27-137">Administración de vínculos URL</span><span class="sxs-lookup"><span data-stu-id="b6a27-137">URL Link Handling</span></span>](#url-link-handling) | <span data-ttu-id="b6a27-138">91 o posterior</span><span class="sxs-lookup"><span data-stu-id="b6a27-138">91 or later</span></span> | <span data-ttu-id="b6a27-139">Windows</span><span class="sxs-lookup"><span data-stu-id="b6a27-139">Windows</span></span>|
| [<span data-ttu-id="b6a27-140">Superposición de controles de ventana para aplicaciones de escritorio</span><span class="sxs-lookup"><span data-stu-id="b6a27-140">Window Controls Overlay for Desktop Apps</span></span>](#window-controls-overlay-for-installed-desktop-web-apps) | <span data-ttu-id="b6a27-141">91 o posterior</span><span class="sxs-lookup"><span data-stu-id="b6a27-141">91 or later</span></span> | <span data-ttu-id="b6a27-142">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b6a27-142">Windows 10</span></span>|   
| [<span data-ttu-id="b6a27-143">Ejecutar en inicio de sesión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b6a27-143">Run on OS Login</span></span>](#run-on-os-login) | <span data-ttu-id="b6a27-144">88 o posterior</span><span class="sxs-lookup"><span data-stu-id="b6a27-144">88 or later</span></span> | <span data-ttu-id="b6a27-145">Todos</span><span class="sxs-lookup"><span data-stu-id="b6a27-145">All</span></span> |  
| [<span data-ttu-id="b6a27-146">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="b6a27-146">Shortcuts</span></span>](#shortcuts) | <span data-ttu-id="b6a27-147">87 o posterior</span><span class="sxs-lookup"><span data-stu-id="b6a27-147">87 or later</span></span> | <span data-ttu-id="b6a27-148">Todos</span><span class="sxs-lookup"><span data-stu-id="b6a27-148">All</span></span> |  
| [<span data-ttu-id="b6a27-149">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="b6a27-149">File Handling</span></span>](#file-handling) | <span data-ttu-id="b6a27-150">83 o posterior</span><span class="sxs-lookup"><span data-stu-id="b6a27-150">83 or later</span></span> | <span data-ttu-id="b6a27-151">Todo el escritorio</span><span class="sxs-lookup"><span data-stu-id="b6a27-151">All Desktop</span></span> |  

## <a name="uri-protocol-handling"></a><span data-ttu-id="b6a27-152">Administración del protocolo URI</span><span class="sxs-lookup"><span data-stu-id="b6a27-152">URI Protocol Handling</span></span>  

<span data-ttu-id="b6a27-153">Se puede usar un identificador uniforme de recursos \(URI\) para definir algo más que vínculos a páginas web y contenido web mediante el protocolo HTTP o FTP.</span><span class="sxs-lookup"><span data-stu-id="b6a27-153">A uniform resource identifier \(URI\) may be used to define more than just links to webpages and web content using the HTTP or FTP protocol.</span></span>  <span data-ttu-id="b6a27-154">Los URI pueden usarse para describir vínculos a todo lo que codifique en un esquema.</span><span class="sxs-lookup"><span data-stu-id="b6a27-154">URIs may be used to describe links to anything that you codify into a schema.</span></span>  <span data-ttu-id="b6a27-155">Por ejemplo, el protocolo se usa para describir un vínculo de correo electrónico y el sistema operativo \(OS\) o el explorador decide qué página web o aplicación debe controlar `mailto://` ese protocolo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-155">For example, the `mailto://` protocol is used to describe an email link and the operating system \(OS\) or browser decides which webpage or app should handle that protocol.</span></span>  

<span data-ttu-id="b6a27-156">Para obtener más información acerca de la compatibilidad basada en explorador existente, vaya a [Controladores de protocolo basados][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]en web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-156">For more information about existing browser-based support, navigate to [Web-based protocol handlers][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span></span>  

<span data-ttu-id="b6a27-157">Esta característica le permite completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b6a27-157">This feature allows you to complete the following actions.</span></span>  

*   <span data-ttu-id="b6a27-158">Registrar el PWA con el sistema operativo host mediante el manifiesto de la aplicación web</span><span class="sxs-lookup"><span data-stu-id="b6a27-158">Register your PWA with the host OS using the manifest of your web app</span></span>
*   <span data-ttu-id="b6a27-159">Declarar que una PWA controla un protocolo URI específico</span><span class="sxs-lookup"><span data-stu-id="b6a27-159">Declare that a PWA handles a specific URI protocol</span></span>  
    
<span data-ttu-id="b6a27-160">Después de registrar un PWA como controlador de protocolo, cuando un usuario elige un hipervínculo con un esquema específico, como un explorador o una aplicación nativa, el sistema operativo activa el PWA registrado y recibe el `mailto://` `web+music://` URI.</span><span class="sxs-lookup"><span data-stu-id="b6a27-160">After you register a PWA as a protocol handler, when a user chooses a hyperlink with a specific scheme such as `mailto://` or `web+music://` from a browser or a native app, the registered PWA is activated by the OS and receives the URI.</span></span>  

<span data-ttu-id="b6a27-161">Esta característica requiere que actualices el manifiesto de la aplicación web para incluir una matriz, en la `protocol_handlers` matriz debes especificar dos campos:</span><span class="sxs-lookup"><span data-stu-id="b6a27-161">This feature requires you to update the web app manifest to include a `protocol_handlers` array, in the array you need to specify two fields:</span></span>  

*   `protocol`<span data-ttu-id="b6a27-162">: el protocolo para controlar la solicitud, por ejemplo `mailto` o `web+jngl` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-162">:  The protocol to handle the request, for example `mailto` or `web+jngl`.</span></span>  
*   `url`<span data-ttu-id="b6a27-163">: URI HTTPS en el ámbito de la aplicación que controla el protocolo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-163">: The HTTPS URI in the app scope that handles the protocol.</span></span>  <span data-ttu-id="b6a27-164">En el futuro, el URI a partir del esquema de controladores de protocolo está planeado para reemplazar el `%s` token.</span><span class="sxs-lookup"><span data-stu-id="b6a27-164">In the future, the URI starting with the protocol handlers scheme is planned to replace the `%s` token.</span></span>  
    
<span data-ttu-id="b6a27-165">Actualice el manifiesto para admitir el protocolo que desea registrar.</span><span class="sxs-lookup"><span data-stu-id="b6a27-165">Update your manifest to support the protocol that you want to register.</span></span>  <span data-ttu-id="b6a27-166">Después de activar esta característica, Microsoft Edge completa las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b6a27-166">After you turn on this feature, Microsoft Edge completes the following actions.</span></span>  

1.  <span data-ttu-id="b6a27-167">Detecta cambios en el manifiesto</span><span class="sxs-lookup"><span data-stu-id="b6a27-167">Detects changes in the manifest</span></span>  
1.  <span data-ttu-id="b6a27-168">Registra la aplicación para el protocolo</span><span class="sxs-lookup"><span data-stu-id="b6a27-168">Registers the app for the protocol</span></span>  
    
<span data-ttu-id="b6a27-169">Si más de una aplicación registra un protocolo, se muestra al usuario un mensaje.</span><span class="sxs-lookup"><span data-stu-id="b6a27-169">If more than one app registers a protocol, the user is presented with a prompt.</span></span>  <span data-ttu-id="b6a27-170">El usuario elige la aplicación adecuada de la lista presentada por el sistema operativo o el explorador.</span><span class="sxs-lookup"><span data-stu-id="b6a27-170">The user chooses the appropriate app from the list presented by the OS or browser.</span></span>  

<span data-ttu-id="b6a27-171">Para obtener una vista previa del Microsoft Edge en Windows, vaya a Activar características [experimentales](#turn-on-experimental-features) y active Control de protocolo **de PWA escritorio.**</span><span class="sxs-lookup"><span data-stu-id="b6a27-171">To preview protocol handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA Protocol handling**.</span></span>  

<span data-ttu-id="b6a27-172">Para obtener más información acerca de la versión de prueba de origen que se está ejecutando para los controladores de protocolo, vaya a Registrar para el registro del controlador de [protocolo de aplicación web.][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]</span><span class="sxs-lookup"><span data-stu-id="b6a27-172">For more information about origin trial is running for protocol handlers, navigate to [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span></span>  

### <a name="example-manifest"></a><span data-ttu-id="b6a27-173">Manifiesto de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6a27-173">Example Manifest</span></span>

<span data-ttu-id="b6a27-174">En este ejemplo, un manifiesto de aplicación web declara que la aplicación debe registrarse para controlar los protocolos `web+jngl` y `web+jnglstore` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-174">In this example, a web app manifest declares that the app should be registered to handle the protocols `web+jngl` and `web+jnglstore`.</span></span>

```json
{
  "name": "Jungle",
  "description": "A plant encyclopedia",
  "protocol_handlers": [
    {
      "protocol": "web+jngl",
      "url": "/lookup?type=%s"
    },
    {
      "protocol": "web+jnglstore",
      "url": "/shop?for=%s"
    }
  ],
  "icons": [
    {
      "src": "images/icons-192.png",
      "type": "image/png",
      "sizes": "192x192"
    },
  ],
  "background_color": "#007f87",

  "display": "standalone",
  "start_url": "/",
}
```  
 
## <a name="url-link-handling"></a><span data-ttu-id="b6a27-175">Administración de vínculos URL</span><span class="sxs-lookup"><span data-stu-id="b6a27-175">URL Link Handling</span></span>  

<span data-ttu-id="b6a27-176">Un localizador uniforme de recursos \(URL\) es un tipo de URI.</span><span class="sxs-lookup"><span data-stu-id="b6a27-176">A uniform resource locator \(URL\) is a type of URI.</span></span>  <span data-ttu-id="b6a27-177">Crea una experiencia más atractiva cuando las aplicaciones web progresivas \(PWAs\) se registren como controladores para URI https.</span><span class="sxs-lookup"><span data-stu-id="b6a27-177">Create a more engaging experience when Progressive Web Apps \(PWAs\) register as handlers for https URIs.</span></span>  <span data-ttu-id="b6a27-178">Las PWA pueden solicitar que se inicien cuando se activen los URI asociados.</span><span class="sxs-lookup"><span data-stu-id="b6a27-178">PWAs may request to launch when associated URIs are activated.</span></span>  <span data-ttu-id="b6a27-179">Por ejemplo, si un usuario elige un vínculo a un artículo de noticias de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b6a27-179">For example, if a user chooses a link to a news story from an email message.</span></span>  <span data-ttu-id="b6a27-180">Se inicia automáticamente PWA asociado para mostrar artículos de noticias para controlar la activación del vínculo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-180">An associated PWA to display news stories is automatically launched to handle the activation of the link.</span></span>  

<span data-ttu-id="b6a27-181">Esta característica te permite registrar una PWA con el explorador mediante el manifiesto de la aplicación web y declarar que el explorador controla vínculos específicos.</span><span class="sxs-lookup"><span data-stu-id="b6a27-181">This feature allows you to register a PWA with the browser using the web app manifest and declare that the browser handles specific links.</span></span>  <span data-ttu-id="b6a27-182">Para registrar una PWA con el explorador, agregue el miembro `url_handlers` opcional al archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b6a27-182">To register a PWA with the browser, add the optional `url_handlers` member to the manifest file.</span></span>  <span data-ttu-id="b6a27-183">El `url_handlers` miembro es un que agrupa los orígenes de los URI que la aplicación desea `object[]` controlar.</span><span class="sxs-lookup"><span data-stu-id="b6a27-183">The `url_handlers` member is an `object[]` that groups the origins of URIs that the app wishes to handle.</span></span>  

<span data-ttu-id="b6a27-184">El explorador valida el control de vínculos mediante un `web-app-origin-association` archivo JSON que se encuentra en el origen.</span><span class="sxs-lookup"><span data-stu-id="b6a27-184">Link handling is validated by the browser using a `web-app-origin-association` JSON file that is located on the origin.</span></span>  <span data-ttu-id="b6a27-185">El archivo de origen afina aún más las rutas de acceso incluidas o excluidas en el origen.</span><span class="sxs-lookup"><span data-stu-id="b6a27-185">The origin file further fine-tunes the included or excluded paths at the origin.</span></span>  <span data-ttu-id="b6a27-186">Para obtener instrucciones detalladas sobre cómo probar el controlador de direcciones URL, vaya a [PWA como controladores de dirección URL][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span><span class="sxs-lookup"><span data-stu-id="b6a27-186">For detailed instructions about testing the URL handler, navigate to [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span></span>  

<span data-ttu-id="b6a27-187">Para obtener una vista previa del control de vínculos url en Microsoft Edge en Windows, vaya a Activar características [experimentales](#turn-on-experimental-features) y active Control de direcciones **URL PWA escritorio.**</span><span class="sxs-lookup"><span data-stu-id="b6a27-187">To preview URL link handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA URL Handling**.</span></span>  

### <a name="example-of-the-url_handlers-in-the-manifest"></a><span data-ttu-id="b6a27-188">Ejemplo de la url_handlers en el manifiesto</span><span class="sxs-lookup"><span data-stu-id="b6a27-188">Example of the url_handlers in the manifest</span></span>  

<span data-ttu-id="b6a27-189">El siguiente fragmento de código es un manifiesto de aplicación web de ejemplo con el `url_handlers` miembro.</span><span class="sxs-lookup"><span data-stu-id="b6a27-189">The following code snippet is an example web app manifest with the `url_handlers` member.</span></span>  

```json 
{
    "name": "Contoso Business App",
    "display": "standalone",
    "icons": [
        {
            "src": "images/icons-144.png",
            "type": "image/png",
            "sizes": "144x144"
        }
    ],
    "capture_links": "existing_client_event",
    "url_handlers" : [
        {
            "origin": "https://contoso.com"
        },
        {
            "origin": "https://conto.so"
        },
        {
            "origin": "https://*.contoso.com"
        }
    ]
}
```  

<span data-ttu-id="b6a27-190">Un PWA coincide con un URI para el control de direcciones URL si el URI coincide con una de las cadenas de origen y el explorador valida que el origen acepta permitir que esta aplicación controle `url_handlers` dicho URI.</span><span class="sxs-lookup"><span data-stu-id="b6a27-190">A PWA matches a URI for URL handling if the URI matches one of the origin strings in `url_handlers` and the browser validates that the origin agrees to allow this app handle such a URI.</span></span>  

<span data-ttu-id="b6a27-191">El miembro contiene un origen que abarca el ámbito y otros orígenes no relacionados de la `url_handlers` PWA.</span><span class="sxs-lookup"><span data-stu-id="b6a27-191">The `url_handlers` member contains an origin that encompasses the scope and other unrelated origins of the requesting PWA.</span></span>  <span data-ttu-id="b6a27-192">No restringir los URI al mismo ámbito o dominio que el PWA de solicitud permite usar nombres de dominio diferentes para el mismo contenido, pero controlarlos con el mismo PWA.</span><span class="sxs-lookup"><span data-stu-id="b6a27-192">Not restricting URIs to the same scope or domain as the requesting PWA allows you to use different domain names for the same content but handle them with the same PWA.</span></span>  

#### <a name="wildcard-matching"></a><span data-ttu-id="b6a27-193">Coincidencia de caracteres comodín</span><span class="sxs-lookup"><span data-stu-id="b6a27-193">Wildcard matching</span></span>  

<span data-ttu-id="b6a27-194">Use el carácter comodín \( `*` \) para que coincida con uno o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6a27-194">Use the wildcard character \(`*`\) to match one or more characters.</span></span>  

<span data-ttu-id="b6a27-195">Se usa un prefijo comodín en las cadenas de origen del `url_handlers` miembro para que coincidan con los subdominios diferentes.</span><span class="sxs-lookup"><span data-stu-id="b6a27-195">A wildcard prefix is used in origin strings of the `url_handlers` member to match for different subdomains.</span></span>  <span data-ttu-id="b6a27-196">El prefijo debe ser `*.` para este uso.</span><span class="sxs-lookup"><span data-stu-id="b6a27-196">The prefix must be `*.` for this usage.</span></span>  <span data-ttu-id="b6a27-197">El `https` esquema se asume cuando se usa un prefijo comodín.</span><span class="sxs-lookup"><span data-stu-id="b6a27-197">The `https` scheme is assumed when you use a wildcard prefix.</span></span>  

<span data-ttu-id="b6a27-198">Por ejemplo, el `url_handlers` valor de miembro se establece en `*.contoso.com` coincidencias y , pero no `tenant.contoso.com` coincide con `www.tenant.contoso.com` `contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-198">For example, the `url_handlers` member value is set to `*.contoso.com` matches `tenant.contoso.com` and `www.tenant.contoso.com`, but doesn't match `contoso.com`.</span></span>  

## <a name="window-controls-overlay-for-installed-desktop-web-apps"></a><span data-ttu-id="b6a27-199">Superposición de controles de ventana para aplicaciones web de escritorio instaladas</span><span class="sxs-lookup"><span data-stu-id="b6a27-199">Window Controls Overlay for installed desktop web apps</span></span>  

<span data-ttu-id="b6a27-200">Para crear una barra de título envolvente como una aplicación \*\*\*\* nativa para la aplicación web instalada en el escritorio, la característica Superposición de controles de ventana completa las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="b6a27-200">To create an immersive title bar like a native app for your desktop installed web app, the **Window Controls Overlay** feature completes the following actions.</span></span>  
    
1.  <span data-ttu-id="b6a27-201">Quita la barra de título reservada del sistema.</span><span class="sxs-lookup"><span data-stu-id="b6a27-201">Removes the system reserved title bar.</span></span>  <span data-ttu-id="b6a27-202">Normalmente abarca el ancho del marco de cliente.</span><span class="sxs-lookup"><span data-stu-id="b6a27-202">It usually spans the width of the client frame.</span></span>  
1.  <span data-ttu-id="b6a27-203">Lo reemplaza por una superposición.</span><span class="sxs-lookup"><span data-stu-id="b6a27-203">Replaces it with an overlay.</span></span>  <span data-ttu-id="b6a27-204">Contiene solo los controles de ventana necesarios para que un usuario controle la propia ventana.</span><span class="sxs-lookup"><span data-stu-id="b6a27-204">It contains just the critical system required window controls necessary for a user to control the window itself.</span></span>  
    
<span data-ttu-id="b6a27-205">Después de proporcionar una superposición, todo el área de cliente web está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="b6a27-205">After it provides an overlay, the entire web client area is available for you to use.</span></span>  <span data-ttu-id="b6a27-206">Esta característica incluye una actualización de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b6a27-206">This feature includes a manifest update.</span></span>  <span data-ttu-id="b6a27-207">Proporciona formas de determinar el tamaño y la posición de la superposición para ayudarle a organizar el contenido.</span><span class="sxs-lookup"><span data-stu-id="b6a27-207">It provides ways for you to determine the size and position of the overlay to help you arrange content.</span></span>  

<span data-ttu-id="b6a27-208">Para obtener una vista previa de las superposiciones de controles de ventana en Microsoft Edge para Windows 10, vaya a Activar características [experimentales](#turn-on-experimental-features) y vaya a Escritorio PWA superposición **de controles de ventana**.</span><span class="sxs-lookup"><span data-stu-id="b6a27-208">To preview the Window Controls Overlays in Microsoft Edge for Windows 10, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.</span></span>   

### <a name="examples-of-title-bar-area-customization"></a><span data-ttu-id="b6a27-209">Ejemplos de personalización del área de la barra de título</span><span class="sxs-lookup"><span data-stu-id="b6a27-209">Examples of title bar area customization</span></span>  

<span data-ttu-id="b6a27-210">Esta característica se basa en la capacidad de las aplicaciones nativas para personalizar la barra de título.</span><span class="sxs-lookup"><span data-stu-id="b6a27-210">This feature is based on the ability in native apps to customize the title bar.</span></span>  <span data-ttu-id="b6a27-211">Puedes personalizar una barra de título para las notificaciones o acciones importantes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6a27-211">You may customize a title bar for important app actions or notifications.</span></span>  <span data-ttu-id="b6a27-212">Revise los siguientes ejemplos para obtener Microsoft Visual Studio código y Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="b6a27-212">Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.</span></span>  

#### <a name="visual-studio-code"></a><span data-ttu-id="b6a27-213">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b6a27-213">Visual Studio Code</span></span>  

<span data-ttu-id="b6a27-214">Microsoft Visual Studio Code es un editor popular basado en Electron que se incluye en varias plataformas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="b6a27-214">Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.</span></span>  

<span data-ttu-id="b6a27-215">En el ejemplo siguiente se muestra cómo Visual Studio Code la barra de título para maximizar la propiedad de pantalla disponible para incluir el nombre de archivo actual y la estructura de menús de nivel superior en la barra de título.</span><span class="sxs-lookup"><span data-stu-id="b6a27-215">The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.</span></span>  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="Un ejemplo de la barra de título de Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   <span data-ttu-id="b6a27-217">Un ejemplo de la barra de título de Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b6a27-217">An example of the title bar in Visual Studio Code</span></span>  
:::image-end:::  

#### <a name="microsoft-teams"></a><span data-ttu-id="b6a27-218">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b6a27-218">Microsoft Teams</span></span>  

<span data-ttu-id="b6a27-219">Las herramientas de comunicación y colaboración Microsoft Teams workplace también se han creado con Electron y están disponibles en varias plataformas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="b6a27-219">Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.</span></span>  <span data-ttu-id="b6a27-220">En el siguiente ejemplo, Microsoft Teams y botones de navegación, un cuadro `back` de búsqueda y controles de perfil de `forward` usuario.</span><span class="sxs-lookup"><span data-stu-id="b6a27-220">In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.</span></span>  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="Un ejemplo de la barra de título de Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   <span data-ttu-id="b6a27-222">Un ejemplo de la barra de título de Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b6a27-222">An example of the title bar in Microsoft Teams</span></span>  
:::image-end:::  

### <a name="overlay-window-controls-on-a-frameless-window"></a><span data-ttu-id="b6a27-223">Superponer controles de ventana en una ventana sin marco</span><span class="sxs-lookup"><span data-stu-id="b6a27-223">Overlay Window Controls on a Frameless Window</span></span>  

<span data-ttu-id="b6a27-224">Para maximizar el área direccionable para el contenido web, el explorador crea una ventana sin marco.</span><span class="sxs-lookup"><span data-stu-id="b6a27-224">To maximize the addressable area for web content, the browser creates a frameless window.</span></span>  <span data-ttu-id="b6a27-225">Una ventana sin marco quita toda la interfaz de usuario del explorador, excepto los controles de ventana proporcionados como una superposición.</span><span class="sxs-lookup"><span data-stu-id="b6a27-225">A frameless window removes all browser UI, except for the window controls provided as an overlay.</span></span>  <span data-ttu-id="b6a27-226">La superposición de controles de ventana permite a los usuarios minimizar, maximizar, restaurar y cerrar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6a27-226">The window controls overlay allows users to still minimize, maximize, restore, and close the app.</span></span>  <span data-ttu-id="b6a27-227">También proporciona acceso a controles de explorador relevantes mediante el menú de la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-227">It also provides access to relevant browser controls using the web app menu.</span></span>  <span data-ttu-id="b6a27-228">Para Chromium exploradores basados en el usuario, la superposición incluye los siguientes controles.</span><span class="sxs-lookup"><span data-stu-id="b6a27-228">For Chromium-based browsers, the overlay includes the following controls.</span></span>  

*   <span data-ttu-id="b6a27-229">Una región arrastrable con el mismo ancho y alto de cada uno de los botones de control de ventana</span><span class="sxs-lookup"><span data-stu-id="b6a27-229">A draggable region the same width and height of each of the window control buttons</span></span>  
*   <span data-ttu-id="b6a27-230">El **Configuración y más** \(...\) botón</span><span class="sxs-lookup"><span data-stu-id="b6a27-230">The **Settings and more** \(...\) button</span></span>  
*   <span data-ttu-id="b6a27-231">Los botones de control de ventana minimizan, maximizan, restauran y cierran</span><span class="sxs-lookup"><span data-stu-id="b6a27-231">The window control buttons minimize, maximize, restore, and close</span></span>  
    
<span data-ttu-id="b6a27-232">Además de los controles enumerados anteriormente, la interfaz de usuario mostrada en la superposición cambia de tamaño dinámicamente en los siguientes escenarios.</span><span class="sxs-lookup"><span data-stu-id="b6a27-232">Besides the previously listed controls, the UI displayed in the overlay is dynamically resized in the following scenarios.</span></span>  

*   <span data-ttu-id="b6a27-233">Cuando se inicia una aplicación web instalada, el origen de la página web se muestra a la izquierda del menú **Configuración** y más \(...\) durante unos segundos y, a continuación, desaparece.</span><span class="sxs-lookup"><span data-stu-id="b6a27-233">When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.</span></span>  
*   <span data-ttu-id="b6a27-234">Si un usuario interactúa con una extensión mediante el menú **Configuración y** más \(...\), el icono de la extensión se muestra en la superposición a la izquierda del menú de tres puntos.</span><span class="sxs-lookup"><span data-stu-id="b6a27-234">If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.</span></span>  <span data-ttu-id="b6a27-235">Después de salir de cualquier cuadro de diálogo de extensión, el icono se quita de la superposición.</span><span class="sxs-lookup"><span data-stu-id="b6a27-235">After you exit any extension dialog, the icon is removed from the overlay.</span></span>  
    
| <span data-ttu-id="b6a27-236">Dirección del idioma</span><span class="sxs-lookup"><span data-stu-id="b6a27-236">Language direction</span></span> | <span data-ttu-id="b6a27-237">Ubicación de superposición</span><span class="sxs-lookup"><span data-stu-id="b6a27-237">Overlay location</span></span> | <span data-ttu-id="b6a27-238">Detalles</span><span class="sxs-lookup"><span data-stu-id="b6a27-238">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="b6a27-239">De izquierda a derecha \(LTR\)</span><span class="sxs-lookup"><span data-stu-id="b6a27-239">Left-to-right \(LTR\)</span></span> | <span data-ttu-id="b6a27-240">Superior izquierda del área de cliente</span><span class="sxs-lookup"><span data-stu-id="b6a27-240">Upper left of the client area</span></span> | <span data-ttu-id="b6a27-241">Los controles se voltearán</span><span class="sxs-lookup"><span data-stu-id="b6a27-241">The controls are flipped</span></span> |  
| <span data-ttu-id="b6a27-242">De derecha a izquierda \(RTL\)</span><span class="sxs-lookup"><span data-stu-id="b6a27-242">Right-to-left \(RTL\)</span></span> | <span data-ttu-id="b6a27-243">Esquina superior derecha del área de cliente</span><span class="sxs-lookup"><span data-stu-id="b6a27-243">Upper right corner of the client area</span></span> |  |  

> [!IMPORTANT]
> <span data-ttu-id="b6a27-244">La superposición siempre está en la parte superior del índice Z del contenido web y acepta todas las entradas del usuario sin pasarla al contenido web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-244">The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.</span></span>  

### <a name="working-around-the-window-controls-overlay"></a><span data-ttu-id="b6a27-245">Trabajar alrededor de la superposición de controles de ventana</span><span class="sxs-lookup"><span data-stu-id="b6a27-245">Working around the Window Controls Overlay</span></span>  

<span data-ttu-id="b6a27-246">El contenido web debe tener en cuenta el área reservada para la superposición de controles.</span><span class="sxs-lookup"><span data-stu-id="b6a27-246">Your web content must be aware of the reserved area for the controls overlay.</span></span>  <span data-ttu-id="b6a27-247">Asegúrese de que el área reservada no espera la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="b6a27-247">Ensure the reserved area doesn't expect user interaction.</span></span>  <span data-ttu-id="b6a27-248">Consulta al explorador el rectángulo de límite y la visibilidad de la superposición de controles.</span><span class="sxs-lookup"><span data-stu-id="b6a27-248">Query the browser for the bounding rectangle and visibility of the controls overlay.</span></span>  <span data-ttu-id="b6a27-249">La información se proporciona a través de las API de JavaScript y las variables de entorno CSS.</span><span class="sxs-lookup"><span data-stu-id="b6a27-249">The information is provided to you through JavaScript APIs and CSS environment variables.</span></span>  

#### <a name="javascript-apis"></a><span data-ttu-id="b6a27-250">API de JavaScript</span><span class="sxs-lookup"><span data-stu-id="b6a27-250">JavaScript APIs</span></span>  

<span data-ttu-id="b6a27-251">Un nuevo objeto de la propiedad permite consultar el `windowControlsOverlay` rectángulo delimitador de la `window.navigator` superposición de controles.</span><span class="sxs-lookup"><span data-stu-id="b6a27-251">A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.</span></span>  

<span data-ttu-id="b6a27-252">El `windowControlsOverlay` objeto tiene los dos objetos siguientes.</span><span class="sxs-lookup"><span data-stu-id="b6a27-252">The `windowControlsOverlay` object has the following two objects.</span></span>  

*   `getBoundingClientRect()` <span data-ttu-id="b6a27-253">devuelve un `DOMRect` objeto.</span><span class="sxs-lookup"><span data-stu-id="b6a27-253">returns a `DOMRect` object.</span></span>  <span data-ttu-id="b6a27-254">El `DOMRect` objeto representa el área debajo de la superposición de controles de ventana.</span><span class="sxs-lookup"><span data-stu-id="b6a27-254">The `DOMRect` object represents the area under the window controls overlay.</span></span>  
*   `visible` <span data-ttu-id="b6a27-255">es un valor booleano que indica que la superposición de controles se representa y se muestra.</span><span class="sxs-lookup"><span data-stu-id="b6a27-255">is a boolean that indicates that the controls overlay is rendered and displayed.</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="b6a27-256">Por motivos de privacidad, los elementos del `windowControlsOverlay` contenido web no son `iframe` accesibles.</span><span class="sxs-lookup"><span data-stu-id="b6a27-256">For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.</span></span>  

<span data-ttu-id="b6a27-257">Cada vez que se cambia el tamaño de la superposición, se ejecuta un evento en el objeto para notificar al `geometrychange` cliente que recalcula el diseño de `navigator.windowControlsOverlay` contenido.</span><span class="sxs-lookup"><span data-stu-id="b6a27-257">Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.</span></span>  <span data-ttu-id="b6a27-258">El diseño de contenido recalculado se basa en el nuevo rectángulo delimitador de la superposición.</span><span class="sxs-lookup"><span data-stu-id="b6a27-258">The recalculated content layout is based on the new bounding rectangle of the overlay.</span></span>  

#### <a name="css-environment-variables"></a><span data-ttu-id="b6a27-259">Variables de entorno CSS</span><span class="sxs-lookup"><span data-stu-id="b6a27-259">CSS Environment Variables</span></span>  

<span data-ttu-id="b6a27-260">Además de la API de JavaScript, puede usar CSS para consultar el rectángulo delimitador de la superposición de controles.</span><span class="sxs-lookup"><span data-stu-id="b6a27-260">Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.</span></span>  <span data-ttu-id="b6a27-261">Use las siguientes cuatro nuevas variables de entorno CSS para realizar la consulta.</span><span class="sxs-lookup"><span data-stu-id="b6a27-261">Use the following four new CSS environment variables to accomplish to query.</span></span>  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### <a name="define-draggable-regions-in-web-content"></a><span data-ttu-id="b6a27-262">Definir regiones arrastrables en contenido web</span><span class="sxs-lookup"><span data-stu-id="b6a27-262">Define Draggable Regions in Web Content</span></span>  

<span data-ttu-id="b6a27-263">Los usuarios esperan agarrar y arrastrar la región superior de una ventana.</span><span class="sxs-lookup"><span data-stu-id="b6a27-263">Users expect to grab and drag the upper region of a window.</span></span>  <span data-ttu-id="b6a27-264">Para dar cabida a la expectativa, declare elementos específicos del contenido web como arrastrables.</span><span class="sxs-lookup"><span data-stu-id="b6a27-264">To accommodate the expectation, declare specific parts of the web content as draggable.</span></span>  
<span data-ttu-id="b6a27-265">Para especificar que un elemento se puede arrastrar, use la propiedad CSS propietaria de `-webkit-app-region` WebKit.</span><span class="sxs-lookup"><span data-stu-id="b6a27-265">To specify an element is draggable, use the WebKit-proprietary `-webkit-app-region` CSS property.</span></span>  <span data-ttu-id="b6a27-266">El grupo de trabajo css continúa los esfuerzos para estandarizar la `app-region` propiedad.</span><span class="sxs-lookup"><span data-stu-id="b6a27-266">The CSS working group continues efforts to standardize the `app-region` property.</span></span>  

### <a name="custom-title-bar-example"></a><span data-ttu-id="b6a27-267">Ejemplo de barra de título personalizada</span><span class="sxs-lookup"><span data-stu-id="b6a27-267">Custom title bar example</span></span>  

<span data-ttu-id="b6a27-268">En el ejemplo siguiente se muestra cómo las nuevas características crean una aplicación web con una barra de título personalizada.</span><span class="sxs-lookup"><span data-stu-id="b6a27-268">The following example displays how the new features create a web app with a custom title bar.</span></span>  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Ejemplo de una barra de título personalizada en Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   <span data-ttu-id="b6a27-270">Ejemplo de una barra de título personalizada en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="b6a27-270">Example of a custom title bar in Microsoft Teams</span></span>  
:::image-end:::  

#### <a name="manifestwebmanifest"></a><span data-ttu-id="b6a27-271">manifest.webmanifest</span><span class="sxs-lookup"><span data-stu-id="b6a27-271">manifest.webmanifest</span></span>  

<span data-ttu-id="b6a27-272">En el manifiesto, establezca `display_override` la matriz en  `window-controls-overlay` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-272">In the manifest, set `display_override` array to  `window-controls-overlay`.</span></span>  <span data-ttu-id="b6a27-273">Establece el `theme_color` color que elijas para la barra de título.</span><span class="sxs-lookup"><span data-stu-id="b6a27-273">Set the `theme_color` to your choice of color for the title bar.</span></span>  <span data-ttu-id="b6a27-274">Establezca el modo de presentación en una reserva adecuada para cuando se `display_override` admite o `window-controls-overlay` no.</span><span class="sxs-lookup"><span data-stu-id="b6a27-274">Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.</span></span>  

<span data-ttu-id="b6a27-275">El siguiente fragmento de código incluye las actualizaciones de manifiesto recomendadas.</span><span class="sxs-lookup"><span data-stu-id="b6a27-275">The following code snippet includes the recommended manifest updates.</span></span>  

```json
{
  "name": "Example PWA",
  "display": "standalone",
  "display_override": [ 
    "window-controls-overlay" 
  ],
  "theme_color": "#254B85"
}
```  

### <a name="indexhtml"></a><span data-ttu-id="b6a27-276">index.html</span><span class="sxs-lookup"><span data-stu-id="b6a27-276">index.html</span></span>  

<span data-ttu-id="b6a27-277">Los siguientes IDs representan las dos regiones principales de la página web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-277">The following IDs represent the two main regions of the webpage.</span></span>  

*   `titleBarContainer`  
*   `mainContent`  
    
<span data-ttu-id="b6a27-278">El elemento con el identificador se establece en y el elemento secundario del cuadro de `div` búsqueda se establece en `titleBar` `draggable` `input` `nonDraggable` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-278">The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.</span></span>  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

<span data-ttu-id="b6a27-279">En el `div` elemento con el `titleBarContainer` identificador, el con el identificador representa `div` la parte visible del área de la barra de `titleBar` título.</span><span class="sxs-lookup"><span data-stu-id="b6a27-279">In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.</span></span>  

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Example PWA</title>
    <link rel="stylesheet" href="style.css">
    <link rel="manifest" href="./manifest.webmanifest">
  </head>
  <body>
    <div id="titleBarContainer">
      <div id="titleBar" class=" draggable">
        <span class="draggable">Example PWA</span>
        <input class="nonDraggable" type="text" placeholder="Search"></input>
      </div>
    </div>
    <div id="mainContent"><!-- The rest of the webpage --></div>
  </body>
</html>
```  

### <a name="stylecss"></a><span data-ttu-id="b6a27-280">style.css</span><span class="sxs-lookup"><span data-stu-id="b6a27-280">style.css</span></span>  

<span data-ttu-id="b6a27-281">Las regiones arrastrables y no arrastrables se establecen mediante `-webkit-app-region: drag` y `-webkit-app-region: no-drag` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-281">The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.</span></span>  

```css
.draggable {
    app-region: drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: drag;
}

.nonDraggable {
    app-region: no-drag;
    /* Pre-fix app-region during standardization process */
    -webkit-app-region: no-drag;
}
```  

<span data-ttu-id="b6a27-282">Para el elemento, los márgenes se establecen para garantizar que la barra `body` de título llegue a los bordes de la `0` ventana.</span><span class="sxs-lookup"><span data-stu-id="b6a27-282">For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.</span></span>  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

<span data-ttu-id="b6a27-283">El `titleBarContainer` identificador usa y establece el valor en , que adjunta el contenedor a la parte superior `position: absolute` de la página `top` `titlebar-area-inset-top` web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-283">The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.</span></span>  <span data-ttu-id="b6a27-284">Se establece en y vuelve a si la superposición de controles de ventana `bottom` `titlebar-area-inset-bottom` no está `100% - var(--fallback-title-bar-height)` visible.</span><span class="sxs-lookup"><span data-stu-id="b6a27-284">The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.</span></span>  <span data-ttu-id="b6a27-285">El color de fondo del `titleBarContainer` identificador es el mismo que el `theme_color` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-285">The background color of the `titleBarContainer` ID is the same as the `theme_color`.</span></span>  <span data-ttu-id="b6a27-286">El ancho se establece en , de modo que el elemento rellena el ancho de la página web y fluye debajo de la superposición cuando está visible para una `100%` `div` apariencia contigua.</span><span class="sxs-lookup"><span data-stu-id="b6a27-286">The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.</span></span>  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

<span data-ttu-id="b6a27-287">El `titleBar` identificador también usa y para `position: absolute` `top: titlebar-area-inset-top` adjuntarlo a la parte superior de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b6a27-287">The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.</span></span>  <span data-ttu-id="b6a27-288">De forma predeterminada, consume el ancho completo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="b6a27-288">By default, it consumes the full width of the window.</span></span>  <span data-ttu-id="b6a27-289">Los `left` bordes y se establecen en y `right` respectivamente, ambos se `titlebar-area-inset-left` `titlebar-area-inset-right` resonarán `0` cuando no se establecen los valores.</span><span class="sxs-lookup"><span data-stu-id="b6a27-289">The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.</span></span>  <span data-ttu-id="b6a27-290">También se establece para evitar cualquier intento de arrastrar la ventana consumida en su lugar `user-select: none` resalta el texto del `div` elemento.</span><span class="sxs-lookup"><span data-stu-id="b6a27-290">It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.</span></span>  

```css
#titleBar {
    position: absolute;
    top: 0;
    display: flex;
    user-select: none;
    height: 100%;
    left: env(titlebar-area-x, 0);
    right: env(titlebar-area-width, 0);
    color: #FFFFFF;
    font-weight: bold;
    text-align: center;
}

#titleBar > span {
    margin: auto;
    padding: 0px 16px 0px 16px;
}

#titleBar > input {
    flex: 1;
    margin: 8px;
    border-radius: 5px;
    border: none;
    padding: 8px;
}
```

<span data-ttu-id="b6a27-291">El contenedor del identificador también se fija en su lugar `mainContent` y se adjunta a la parte inferior de la página `position: absolute` web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-291">The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.</span></span>  <span data-ttu-id="b6a27-292">The `height` is set to and falls back to to fill the remaining space below the title `titlebar-area-inset-bottom` `100% - var(--fallback-titlebar-height)` bar.</span><span class="sxs-lookup"><span data-stu-id="b6a27-292">The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.</span></span>  <span data-ttu-id="b6a27-293">Se establece `overflow-y: scroll` para permitir que el contenido se desplace verticalmente en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="b6a27-293">It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.</span></span>  

```css
#mainContent {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    overflow-y: scroll;
}
```

<span data-ttu-id="b6a27-294">En los casos en los que el explorador no admite la superposición de controles de ventana, se agrega una variable CSS para establecer un alto predeterminado para la barra de título.</span><span class="sxs-lookup"><span data-stu-id="b6a27-294">For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.</span></span>  <span data-ttu-id="b6a27-295">Los límites de los e IDs se establecen inicialmente para rellenar todo el área de cliente y no es necesario cambiarlo si no se admite `titleBarContainer` `mainContent` la superposición.</span><span class="sxs-lookup"><span data-stu-id="b6a27-295">The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.</span></span>  

<span data-ttu-id="b6a27-296">El siguiente fragmento de código incluye todas las actualizaciones CSS recomendadas.</span><span class="sxs-lookup"><span data-stu-id="b6a27-296">The following code snippet includes all the recommended CSS updates.</span></span>

```css
:root {
  --fallback-title-bar-height: 40px;
}

.draggable {
  app-region: drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: drag;
}

.nonDraggable {
  app-region: no-drag;
  /* Pre-fix app-region during standardization process */
  -webkit-app-region: no-drag;
}

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  margin: 0;
}

#titleBarContainer {
  position: absolute;
  top: env(titlebar-area-y, 0);
  bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  width: 100%;
  background-color:#254B85;
}

#titleBar {
  position: absolute;
  top: 0;
  display: flex;
  user-select: none;
  height: 100%;
  left: env(titlebar-area-x, 0);
  right: env(titlebar-area-width, 0);
  color: #FFFFFF;
  font-weight: bold;
  text-align: center;
}

#titleBar > span {
  margin: auto;
  padding: 0px 16px 0px 16px;
}

#titleBar > input {
  flex: 1;
  margin: 8px;
  border-radius: 5px;
  border: none;
  padding: 8px;
}

#mainContent {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
  overflow-y: scroll;
}
```  

<span data-ttu-id="b6a27-297">Chromium exploradores basados en aplicaciones están probando y dando forma a esta característica.</span><span class="sxs-lookup"><span data-stu-id="b6a27-297">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="b6a27-298">Para obtener más información, incluidos los ejemplos de código, vaya a Personalizar la superposición de controles de ventana de la barra de título de [PWA de la ventana.][WebDevWindowControlsOverlay]</span><span class="sxs-lookup"><span data-stu-id="b6a27-298">For more information including code examples, navigate to [Customize the window controls overlay of your PWA's title bar][WebDevWindowControlsOverlay].</span></span>  

## <a name="run-on-os-login"></a><span data-ttu-id="b6a27-299">Ejecutar en inicio de sesión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b6a27-299">Run On OS Login</span></span>  

<span data-ttu-id="b6a27-300">Esta característica te permite configurar la aplicación para que se inicie automáticamente cuando el usuario inicie sesión en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b6a27-300">This feature allows you to configure your app to automatically launch when the user logs into Microsoft Windows.</span></span>  <span data-ttu-id="b6a27-301">Varias clases de aplicaciones aprovechan la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="b6a27-301">Several classes of apps take advantage of the capability.</span></span>  <span data-ttu-id="b6a27-302">Las clases de aplicaciones incluyen correo electrónico, chat, panel de supervisión y aplicaciones para mostrar datos en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="b6a27-302">The classes of apps include email, chat, monitoring dashboard, and real-time data display apps.</span></span>  <span data-ttu-id="b6a27-303">La funcionalidad permite a un usuario interactuar con las aplicaciones tan pronto como el usuario inicia sesión en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-303">The capability allows a user to engage with the apps as soon as the user logs into the OS.</span></span>  <span data-ttu-id="b6a27-304">Esta característica inicia automáticamente el PWA de la misma forma que se inicia manualmente.</span><span class="sxs-lookup"><span data-stu-id="b6a27-304">This feature automatically starts the PWA the same way it's launched manually.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b6a27-305">**Ejecutar en inicio de sesión del sistema** operativo es una característica [eficaz.][GithubW3cPermissionsPowerfulFeature]</span><span class="sxs-lookup"><span data-stu-id="b6a27-305">**Run on OS Login** is a [powerful feature][GithubW3cPermissionsPowerfulFeature].</span></span>  <span data-ttu-id="b6a27-306">Los usuarios deben decidir si se activa la funcionalidad de la aplicación web instalada.</span><span class="sxs-lookup"><span data-stu-id="b6a27-306">Users should decide whether to turn on the capability for the installed web app.</span></span>  

### <a name="turn-on-run-on-os-login"></a><span data-ttu-id="b6a27-307">Activar Ejecutar inicio de sesión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="b6a27-307">Turn on Run On OS Login</span></span>  

<span data-ttu-id="b6a27-308">Para obtener una **vista** previa de las capacidades ejecutar en el sistema operativo para su PWA, vaya a Activar características [experimentales](#turn-on-experimental-features) y active Las PWA de escritorio se ejecutan en el inicio de sesión **del sistema operativo.**</span><span class="sxs-lookup"><span data-stu-id="b6a27-308">To preview the **Run On OS Login** capabilities for your PWA, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWAs run on OS login**.</span></span>  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Activar las PWA de escritorio que se ejecutan en el experimento inicio de sesión del sistema operativo" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   <span data-ttu-id="b6a27-310">Activar las **PWA de escritorio que se ejecutan en el experimento de inicio de sesión del sistema** operativo</span><span class="sxs-lookup"><span data-stu-id="b6a27-310">Turn on the **Desktop PWAs run on OS login** experiment</span></span>  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a><span data-ttu-id="b6a27-311">Activar la característica de la aplicación web instalada</span><span class="sxs-lookup"><span data-stu-id="b6a27-311">Turn on the feature for the installed web app</span></span>  

<span data-ttu-id="b6a27-312">Para activar la característica `Start app when you sign in` de un servidor PWA,</span><span class="sxs-lookup"><span data-stu-id="b6a27-312">To turn on the `Start app when you sign in` feature for an installed PWA,</span></span> 

1.  <span data-ttu-id="b6a27-313">Abra Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b6a27-313">Open Microsoft Edge.</span></span>   
1.  <span data-ttu-id="b6a27-314">Vaya a `edge://apps`.</span><span class="sxs-lookup"><span data-stu-id="b6a27-314">Navigate to `edge://apps`.</span></span>  
1.  <span data-ttu-id="b6a27-315">Mantenga el mouse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b6a27-315">Hover on your app.</span></span>  
1.  <span data-ttu-id="b6a27-316">Abra el menú contextual \(right-click\) y, a continuación, elija **Iniciar aplicación al iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="b6a27-316">Open the contextual menu \(right-click\) and then choose **Start app when you sign in**.</span></span>  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Usa el menú contextual para activar la aplicación Inicio cuando inicies sesión en la Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       <span data-ttu-id="b6a27-318">Usa el menú contextual para activar la **aplicación Inicio cuando inicies sesión** en la Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b6a27-318">Use the contextual menu to turn on the **Start app when you sign in** feature in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="shortcuts"></a><span data-ttu-id="b6a27-319">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="b6a27-319">Shortcuts</span></span>  

`Shortcuts` <span data-ttu-id="b6a27-320">es un nuevo miembro del archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b6a27-320">is a new member of the manifest file.</span></span>  <span data-ttu-id="b6a27-321">Te permite definir vínculos a elementos, páginas web clave o acciones en la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-321">It allows you to define links to parts, key webpages, or actions in your web app.</span></span>  <span data-ttu-id="b6a27-322">Microsoft Windows integra como **listas de saltos**.</span><span class="sxs-lookup"><span data-stu-id="b6a27-322">Microsoft Windows integrates it as **Jumplists**.</span></span>  <span data-ttu-id="b6a27-323">**Las listas de accesos** emergentes definen menús emergentes que aparecen cuando se encuentra en uno de los siguientes elementos de la interfaz de usuario y se abre un menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="b6a27-323">**Jumplists** define popup menus that appear when you on one of the following UI elements and open a contextual menu \(right-click\).</span></span>  

*   <span data-ttu-id="b6a27-324">Un icono en el menú Inicio</span><span class="sxs-lookup"><span data-stu-id="b6a27-324">A tile on the Start Menu</span></span>  
*   <span data-ttu-id="b6a27-325">Un icono en la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="b6a27-325">An icon on the Taskbar</span></span>  
    
<span data-ttu-id="b6a27-326">Cuando un usuario invoca un acceso directo, el usuario navega a la dirección especificada por el `url` miembro del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-326">When a user invokes a shortcut, the user navigates to the address specified by the `url` member of the shortcut.</span></span>  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Un ejemplo de listas de saltos en Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   <span data-ttu-id="b6a27-328">Un ejemplo de **listas de saltos** en Windows 10</span><span class="sxs-lookup"><span data-stu-id="b6a27-328">An example of **Jumplists** on Windows 10</span></span>  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a><span data-ttu-id="b6a27-329">Accesos directos en el archivo de manifiesto</span><span class="sxs-lookup"><span data-stu-id="b6a27-329">Shortcuts in the Manifest file</span></span>  

```json
"shortcuts" : [
  {
    "name": "Today's agenda",
    "url": "/today",
    "description": "List of events planned for today"
  },
  {
    "name": "New event",
    "url": "/create/event"
  },
  {
    "name": "New reminder",
    "url": "/create/reminder"
  }
]
```  

#### <a name="properties-of-shortcuts"></a><span data-ttu-id="b6a27-330">Propiedades de accesos directos</span><span class="sxs-lookup"><span data-stu-id="b6a27-330">Properties of shortcuts</span></span>  

<span data-ttu-id="b6a27-331">Las siguientes propiedades definen cada acceso directo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-331">The following properties define each shortcut.</span></span>  

| <span data-ttu-id="b6a27-332">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6a27-332">Property</span></span> | <span data-ttu-id="b6a27-333">Detalles</span><span class="sxs-lookup"><span data-stu-id="b6a27-333">Details</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="b6a27-334">Cadena que se muestra al usuario en **listas de saltos** o en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b6a27-334">A string that is displayed to the user on **Jumplists** or the contextual menu.</span></span> |  
| `short_name` | <span data-ttu-id="b6a27-335">Cadena que se muestra cuando hay espacio insuficiente para mostrar el nombre completo del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-335">A string that is displayed when insufficient space exists to display the full name of the shortcut.</span></span> |  
| `description` | <span data-ttu-id="b6a27-336">Cadena que describe el propósito del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-336">A string that describes the purpose of the shortcut.</span></span>  <span data-ttu-id="b6a27-337">Es posible que se pueda acceder a ella mediante tecnología de asistencia.</span><span class="sxs-lookup"><span data-stu-id="b6a27-337">It may be accessed by assistive technology.</span></span> |  
| `url` | <span data-ttu-id="b6a27-338">Uri de la aplicación web que se abre cuando se activa el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-338">The URI in the web app that opens when the shortcut is activated.</span></span> |  
| `icons` | <span data-ttu-id="b6a27-339">Un conjunto de iconos que representa el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-339">A set of icons that represents the shortcut.</span></span> |  

## <a name="file-handling"></a><span data-ttu-id="b6a27-340">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="b6a27-340">File Handling</span></span>  

<span data-ttu-id="b6a27-341">La capacidad de registrarse como un controlador de tipos de archivo está en la fase de experimentación.</span><span class="sxs-lookup"><span data-stu-id="b6a27-341">The ability to register as a file type handler is in the experimentation phase.</span></span>  <span data-ttu-id="b6a27-342">Puedes especificar los tipos de archivo que controla la aplicación en una entrada de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b6a27-342">You may specify the file types that your app handles in a manifest entry.</span></span>  <span data-ttu-id="b6a27-343">Durante la instalación, el sistema operativo host del usuario registra la aplicación como un controlador de archivos para los tipos de archivo enumerados.</span><span class="sxs-lookup"><span data-stu-id="b6a27-343">During installation, the user's host OS registers your app as a file handler for the listed file types.</span></span>  <span data-ttu-id="b6a27-344">Asegúrese de la existencia de la característica en el código de inicio de las `launchQueue` aplicaciones y de que controla el archivo.</span><span class="sxs-lookup"><span data-stu-id="b6a27-344">Ensure the existence of the feature `launchQueue` in your apps startup code and that it handles the file.</span></span>  

<span data-ttu-id="b6a27-345">Chromium exploradores basados en aplicaciones están probando y dando forma a esta característica.</span><span class="sxs-lookup"><span data-stu-id="b6a27-345">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="b6a27-346">Para obtener más información, incluidos los ejemplos de código, vaya a [Permitir que las aplicaciones web sean controladores de archivos][WebDevFileHandling].</span><span class="sxs-lookup"><span data-stu-id="b6a27-346">For more information including code examples, navigate to [Let web applications be file handlers][WebDevFileHandling].</span></span>  

<span data-ttu-id="b6a27-347">Para obtener una vista previa del control de archivos Microsoft Edge para Windows 10, vaya a Activar características [experimentales](#turn-on-experimental-features) y active la **API de administración de archivos**.</span><span class="sxs-lookup"><span data-stu-id="b6a27-347">To preview file handling in Microsoft Edge for Windows 10, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **File Handling API**.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="b6a27-348">Proporcionar comentarios sobre características experimentales</span><span class="sxs-lookup"><span data-stu-id="b6a27-348">Providing feedback on experimental features</span></span>  

<span data-ttu-id="b6a27-349">Para proporcionar comentarios sobre Microsoft Edge de aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="b6a27-349">To provide feedback on Microsoft Edge web app experiments.</span></span>  

*   <span data-ttu-id="b6a27-350">Envíe sus comentarios con **Configuración y Más** \( `...` \) > Enviar comentarios a **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="b6a27-350">Send your feedback using **Settings and More** \(`...`\) > **Send Feedback to Microsoft**.</span></span>  
*   <span data-ttu-id="b6a27-351">Seleccione `Alt` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="b6a27-351">Select `Alt`+`Shift`+`I`.</span></span>  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Enviar comentarios desde su PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   <span data-ttu-id="b6a27-353">Enviar comentarios desde su PWA</span><span class="sxs-lookup"><span data-stu-id="b6a27-353">Send Feedback from your PWA</span></span>  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Pruebas de origen | Microsoft Edge Programador"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registrar para el registro del controlador de protocolo de aplicación web | Microsoft Developer"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Controladores de protocolo basados en web | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Característica eficaz: permisos | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PwAs como controladores de dirección URL | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Permitir que las aplicaciones web sean controladores de archivos | web.dev"  
[WebDevWindowControlsOverlay]: https://web.dev/window-controls-overlay "Personalizar la superposición de controles de ventana de la barra de PWA la barra de título | web.dev"  
