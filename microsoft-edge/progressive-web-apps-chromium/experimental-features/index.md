---
description: Las últimas características experimentales de Microsoft Edge para aplicaciones web
title: Características experimentales | Aplicaciones web progresivas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, experiment, progressive web apps, web apps, PWAs, PWA
ms.openlocfilehash: 587797bc8577f1c1aaca42394eecb997d21e9955
ms.sourcegitcommit: f605e4e27fed88aca286f2ae236e27f9a396b517
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "11474989"
---
# <a name="experimental-features-in-progressive-web-apps-pwas"></a><span data-ttu-id="0dd06-104">Características experimentales en aplicaciones web progresivas (PWA)</span><span class="sxs-lookup"><span data-stu-id="0dd06-104">Experimental features in Progressive Web Apps (PWAs)</span></span>  

<span data-ttu-id="0dd06-105">Microsoft Edge proporciona acceso a características experimentales que aún están en desarrollo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-105">Microsoft Edge provides access to experimental features that are still in development.</span></span>  <span data-ttu-id="0dd06-106">Para determinar si cada característica está lista y cuándo liberar cada una, pruebe y [proporcione comentarios](#providing-feedback-on-experimental-features).</span><span class="sxs-lookup"><span data-stu-id="0dd06-106">To determine if each feature is ready and when to release each, test and [provide feedback](#providing-feedback-on-experimental-features).</span></span>  

<span data-ttu-id="0dd06-107">Las características experimentales están disponibles en todos los canales de Microsoft Edge, pero las últimas características experimentales solo están disponibles en el canal de Microsoft Edge Canary.</span><span class="sxs-lookup"><span data-stu-id="0dd06-107">Experimental features are available in all channels of Microsoft Edge, but the latest experimental features are only available in the Microsoft Edge Canary channel.</span></span>  

## <a name="turn-on-experimental-features"></a><span data-ttu-id="0dd06-108">Activar características experimentales</span><span class="sxs-lookup"><span data-stu-id="0dd06-108">Turn on experimental features</span></span>  

<span data-ttu-id="0dd06-109">Para activar las características experimentales \(or off\) en Microsoft Edge, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="0dd06-109">To turn on \(or off\) experimental features in Microsoft Edge, complete the following steps.</span></span>  
  
1.  <span data-ttu-id="0dd06-110">Abra Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0dd06-110">Open Microsoft Edge.</span></span>   
    
    > [!NOTE]
    > <span data-ttu-id="0dd06-111">Asegúrese de usar una versión de Microsoft Edge que tenga el experimento enumerado en este artículo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-111">Ensure you use a Microsoft Edge version that has the Experiment listed in this article.</span></span>  <span data-ttu-id="0dd06-112">Vaya a [Características experimentales](#features-that-are-available-to-test).</span><span class="sxs-lookup"><span data-stu-id="0dd06-112">Navigate to [Experimental features](#features-that-are-available-to-test).</span></span>  
    
1.  <span data-ttu-id="0dd06-113">Vaya a `edge://flags` .</span><span class="sxs-lookup"><span data-stu-id="0dd06-113">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="0dd06-114">Vaya al experimento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="0dd06-114">Navigate to the relevant experiment.</span></span>  
1.  <span data-ttu-id="0dd06-115">Elija el menú desplegable junto a la descripción del experimento y elija `Enabled` .</span><span class="sxs-lookup"><span data-stu-id="0dd06-115">Choose the dropdown menu next to the experiment description and choose `Enabled`.</span></span>  
    
    :::image type="complex" source="../media/turn-on-experimental-flag.png" alt-text="Elija Habilitado para activar un experimento" lightbox="../media/turn-on-experimental-flag.png":::
       <span data-ttu-id="0dd06-117">Elija **Habilitado** para activar un experimento</span><span class="sxs-lookup"><span data-stu-id="0dd06-117">Choose **Enabled** to turn on an experiment</span></span>  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="0dd06-118">Cada experimento suele tener un menú desplegable para elegir los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="0dd06-118">Each experiment usually has a dropdown menu to choose the following values.</span></span>  <span data-ttu-id="0dd06-119">Si una característica experimental no tiene una entrada en **Experimentos,** se proporcionan instrucciones para iniciar Microsoft Edge con esa característica mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0dd06-119">If an experimental feature doesn't have an entry on **Experiments**, instructions are provided to start Microsoft Edge with that feature using the command-line.</span></span>
    > 
    > *   `Default`  
    > *   `Disabled`  
    > *   `Enabled`  
    
1.  <span data-ttu-id="0dd06-120">Reiniciar MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="0dd06-120">Restart Microsoft Edge.</span></span>  
    
### <a name="origin-trials"></a><span data-ttu-id="0dd06-121">Pruebas de origen</span><span class="sxs-lookup"><span data-stu-id="0dd06-121">Origin Trials</span></span>  

<span data-ttu-id="0dd06-122">Microsoft Edge a veces usa pruebas de origen para probar características para dominios o sitios web específicos.</span><span class="sxs-lookup"><span data-stu-id="0dd06-122">Microsoft Edge sometimes uses origin trials to test features for specific domains or websites.</span></span>  <span data-ttu-id="0dd06-123">Es posible que desee usar una versión de prueba de origen para su sitio web para aplicar una característica específica.</span><span class="sxs-lookup"><span data-stu-id="0dd06-123">You may want to use an origin trial for your website to apply a specific feature.</span></span>  <span data-ttu-id="0dd06-124">Si es propietario de un sitio web, puede inscribirse en una prueba de origen.</span><span class="sxs-lookup"><span data-stu-id="0dd06-124">If you're a website owner, you may enroll in an origin trial.</span></span>  <span data-ttu-id="0dd06-125">Una versión de prueba de origen proporciona características a un porcentaje de usuarios de Microsoft Edge que visitan su sitio web.</span><span class="sxs-lookup"><span data-stu-id="0dd06-125">An origin trial provides features to a percentage of Microsoft Edge users who visit your website.</span></span>

<span data-ttu-id="0dd06-126">Para obtener más información acerca de las pruebas de Origen, vaya a [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="0dd06-126">For more information about Origin Trials, navigate to [Microsoft Edge Origin Trials Developer Console][MicrosoftDeveloperMicrosoftEdgeOriginTrials].</span></span>  
    
> [!NOTE]
> <span data-ttu-id="0dd06-127">Las características experimentales se actualizan constantemente y pueden causar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0dd06-127">Experimental features are constantly updated and may cause performance issues.</span></span>  <span data-ttu-id="0dd06-128">Para desactivar una característica experimental, vaya a [Activar características experimentales,](#turn-on-experimental-features)vaya al experimento y, a continuación, elija `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="0dd06-128">To turn off an experimental feature, navigate to [Turn on experimental features](#turn-on-experimental-features), navigate to the experiment, and then choose `Disabled`.</span></span>  

## <a name="features-that-are-available-to-test"></a><span data-ttu-id="0dd06-129">Características que están disponibles para probar</span><span class="sxs-lookup"><span data-stu-id="0dd06-129">Features that are available to test</span></span>  

<span data-ttu-id="0dd06-130">En la siguiente lista se describen las nuevas características experimentales de la aplicación web que están disponibles para probar y validar en Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0dd06-130">The following list describes the new experimental web app features that are available to test and validate on Microsoft Edge.</span></span>  

| <span data-ttu-id="0dd06-131">Característica</span><span class="sxs-lookup"><span data-stu-id="0dd06-131">Feature</span></span> | <span data-ttu-id="0dd06-132">Versión de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0dd06-132">Microsoft Edge version</span></span> | <span data-ttu-id="0dd06-133">Plataforma</span><span class="sxs-lookup"><span data-stu-id="0dd06-133">Platform</span></span> |  
|:--- |:--- |:--- |  
| [<span data-ttu-id="0dd06-134">Administración del protocolo URI</span><span class="sxs-lookup"><span data-stu-id="0dd06-134">URI Protocol Handling</span></span>](#uri-protocol-handling) | <span data-ttu-id="0dd06-135">91 o posterior</span><span class="sxs-lookup"><span data-stu-id="0dd06-135">91 or later</span></span> | <span data-ttu-id="0dd06-136">Windows</span><span class="sxs-lookup"><span data-stu-id="0dd06-136">Windows</span></span> |    
| [<span data-ttu-id="0dd06-137">Administración de vínculos URL</span><span class="sxs-lookup"><span data-stu-id="0dd06-137">URL Link Handling</span></span>](#url-link-handling) | <span data-ttu-id="0dd06-138">91 o posterior</span><span class="sxs-lookup"><span data-stu-id="0dd06-138">91 or later</span></span> | <span data-ttu-id="0dd06-139">Windows</span><span class="sxs-lookup"><span data-stu-id="0dd06-139">Windows</span></span>|  
| [<span data-ttu-id="0dd06-140">Ejecutar en inicio de sesión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0dd06-140">Run on OS Login</span></span>](#run-on-os-login) | <span data-ttu-id="0dd06-141">88 o posterior</span><span class="sxs-lookup"><span data-stu-id="0dd06-141">88 or later</span></span> | <span data-ttu-id="0dd06-142">Todos</span><span class="sxs-lookup"><span data-stu-id="0dd06-142">All</span></span> |  
| [<span data-ttu-id="0dd06-143">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="0dd06-143">Shortcuts</span></span>](#shortcuts) | <span data-ttu-id="0dd06-144">87 o posterior</span><span class="sxs-lookup"><span data-stu-id="0dd06-144">87 or later</span></span> | <span data-ttu-id="0dd06-145">Todos</span><span class="sxs-lookup"><span data-stu-id="0dd06-145">All</span></span> |  
| [<span data-ttu-id="0dd06-146">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="0dd06-146">File Handling</span></span>](#file-handling) | <span data-ttu-id="0dd06-147">83 o posterior</span><span class="sxs-lookup"><span data-stu-id="0dd06-147">83 or later</span></span> | <span data-ttu-id="0dd06-148">Todo el escritorio</span><span class="sxs-lookup"><span data-stu-id="0dd06-148">All Desktop</span></span> |  


## <a name="uri-protocol-handling"></a><span data-ttu-id="0dd06-149">Administración del protocolo URI</span><span class="sxs-lookup"><span data-stu-id="0dd06-149">URI Protocol Handling</span></span>  

<span data-ttu-id="0dd06-150">Se puede usar un identificador uniforme de recursos \(URI\) para definir algo más que vínculos a páginas web y contenido web mediante el protocolo HTTP o FTP.</span><span class="sxs-lookup"><span data-stu-id="0dd06-150">A uniform resource identifier \(URI\) may be used to define more than just links to webpages and web content using the HTTP or FTP protocol.</span></span>  <span data-ttu-id="0dd06-151">Los URI pueden usarse para describir vínculos a todo lo que codifique en un esquema.</span><span class="sxs-lookup"><span data-stu-id="0dd06-151">URIs may be used to describe links to anything that you codify into a schema.</span></span>  <span data-ttu-id="0dd06-152">Por ejemplo, el protocolo se usa para describir un vínculo de correo electrónico y el sistema operativo \(OS\) o el explorador decide qué página web o aplicación debe controlar `mailto://` ese protocolo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-152">For example, the `mailto://` protocol is used to describe an email link and the operating system \(OS\) or browser decides which webpage or app should handle that protocol.</span></span>  

<span data-ttu-id="0dd06-153">Para obtener más información acerca de la compatibilidad basada en explorador existente, vaya a [Controladores de protocolo basados][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]en web.</span><span class="sxs-lookup"><span data-stu-id="0dd06-153">For more information about existing browser-based support, navigate to [Web-based protocol handlers][MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers].</span></span>  

<span data-ttu-id="0dd06-154">Esta característica le permite completar las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="0dd06-154">This feature allows you to complete the following actions.</span></span>  

*   <span data-ttu-id="0dd06-155">Registrar tu PWA con el sistema operativo host mediante el manifiesto de la aplicación web</span><span class="sxs-lookup"><span data-stu-id="0dd06-155">Register your PWA with the host OS using the manifest of your web app</span></span>
*   <span data-ttu-id="0dd06-156">Declarar que una PWA controla un protocolo URI específico</span><span class="sxs-lookup"><span data-stu-id="0dd06-156">Declare that a PWA handles a specific URI protocol</span></span>  
     
<span data-ttu-id="0dd06-157">Después de registrar un PWA como controlador de protocolo, cuando un usuario elige un hipervínculo con un esquema específico, como un explorador o una aplicación nativa, el sistema operativo activa la PWA registrada y recibe el `mailto://` `web+music://` URI.</span><span class="sxs-lookup"><span data-stu-id="0dd06-157">After you register a PWA as a protocol handler, when a user chooses a hyperlink with a specific scheme such as `mailto://` or `web+music://` from a browser or a native app, the registered PWA is activated by the OS and receives the URI.</span></span>  

<span data-ttu-id="0dd06-158">Esta característica requiere que actualices el manifiesto de la aplicación web para incluir una matriz, en la `protocol_handlers` matriz debes especificar dos campos:</span><span class="sxs-lookup"><span data-stu-id="0dd06-158">This feature requires you to update the web app manifest to include a `protocol_handlers` array, in the array you need to specify two fields:</span></span>  

*   `protocol`<span data-ttu-id="0dd06-159">: el protocolo para controlar la solicitud, por ejemplo `mailto` o `web+jngl` .</span><span class="sxs-lookup"><span data-stu-id="0dd06-159">:  The protocol to handle the request, for example `mailto` or `web+jngl`.</span></span>  
*   `url`<span data-ttu-id="0dd06-160">: URI HTTPS en el ámbito de la aplicación que controla el protocolo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-160">: The HTTPS URI in the app scope that handles the protocol.</span></span>  <span data-ttu-id="0dd06-161">En el futuro, el URI a partir del esquema de controladores de protocolo está planeado para reemplazar el `%s` token.</span><span class="sxs-lookup"><span data-stu-id="0dd06-161">In the future, the URI starting with the protocol handlers scheme is planned to replace the `%s` token.</span></span>  
    
<span data-ttu-id="0dd06-162">Actualice el manifiesto para admitir el protocolo que desea registrar.</span><span class="sxs-lookup"><span data-stu-id="0dd06-162">Update your manifest to support the protocol that you want to register.</span></span>  <span data-ttu-id="0dd06-163">Después de activar esta característica, Microsoft Edge completa las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="0dd06-163">After you turn on this feature, Microsoft Edge completes the following actions.</span></span>  

1.  <span data-ttu-id="0dd06-164">Detecta cambios en el manifiesto</span><span class="sxs-lookup"><span data-stu-id="0dd06-164">Detects changes in the manifest</span></span>  
1.  <span data-ttu-id="0dd06-165">Registra la aplicación para el protocolo</span><span class="sxs-lookup"><span data-stu-id="0dd06-165">Registers the app for the protocol</span></span>  
    
<span data-ttu-id="0dd06-166">Si más de una aplicación registra un protocolo, se muestra al usuario un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0dd06-166">If more than one app registers a protocol, the user is presented with a prompt.</span></span>  <span data-ttu-id="0dd06-167">El usuario elige la aplicación adecuada de la lista presentada por el sistema operativo o el explorador.</span><span class="sxs-lookup"><span data-stu-id="0dd06-167">The user chooses the appropriate app from the list presented by the OS or browser.</span></span>  

<span data-ttu-id="0dd06-168">Para obtener una vista previa del control de protocolos en Microsoft Edge en Windows, vaya a Activar características [experimentales](#turn-on-experimental-features) y active **Desktop Web Apps support Protocol Handlers**.</span><span class="sxs-lookup"><span data-stu-id="0dd06-168">To preview protocol handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop Web Apps support Protocol Handlers**.</span></span>  

<span data-ttu-id="0dd06-169">Para obtener más información acerca de la versión de prueba de origen que se está ejecutando para los controladores de protocolo, vaya a Registrar para el registro del controlador de [protocolo de aplicación web.][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]</span><span class="sxs-lookup"><span data-stu-id="0dd06-169">For more information about origin trial is running for protocol handlers, navigate to [Register for Web App Protocol Handler Registration][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].</span></span>  

### <a name="example-manifest"></a><span data-ttu-id="0dd06-170">Manifiesto de ejemplo</span><span class="sxs-lookup"><span data-stu-id="0dd06-170">Example Manifest</span></span>

<span data-ttu-id="0dd06-171">En este ejemplo, un manifiesto de aplicación web declara que la aplicación debe registrarse para controlar los protocolos `web+jngl` y `web+jnglstore` .</span><span class="sxs-lookup"><span data-stu-id="0dd06-171">In this example, a web app manifest declares that the app should be registered to handle the protocols `web+jngl` and `web+jnglstore`.</span></span>

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
 
## <a name="url-link-handling"></a><span data-ttu-id="0dd06-172">Administración de vínculos URL</span><span class="sxs-lookup"><span data-stu-id="0dd06-172">URL Link Handling</span></span>  

<span data-ttu-id="0dd06-173">Un localizador uniforme de recursos \(URL\) es un tipo de URI.</span><span class="sxs-lookup"><span data-stu-id="0dd06-173">A uniform resource locator \(URL\) is a type of URI.</span></span>  <span data-ttu-id="0dd06-174">Crea una experiencia más atractiva cuando las aplicaciones web progresivas \(PWAs\) se registren como controladores para URI https.</span><span class="sxs-lookup"><span data-stu-id="0dd06-174">Create a more engaging experience when Progressive Web Apps \(PWAs\) register as handlers for https URIs.</span></span>  <span data-ttu-id="0dd06-175">Las PWA pueden solicitar que se inicien cuando se activen los URI asociados.</span><span class="sxs-lookup"><span data-stu-id="0dd06-175">PWAs may request to launch when associated URIs are activated.</span></span>  <span data-ttu-id="0dd06-176">Por ejemplo, si un usuario elige un vínculo a un artículo de noticias de un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="0dd06-176">For example, if a user chooses a link to a news story from an email message.</span></span>  <span data-ttu-id="0dd06-177">Se inicia automáticamente un PWA asociado para mostrar artículos de noticias para controlar la activación del vínculo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-177">An associated PWA to display news stories is automatically launched to handle the activation of the link.</span></span>  

<span data-ttu-id="0dd06-178">Esta característica te permite registrar un PWA con el explorador mediante el manifiesto de la aplicación web y declarar que el explorador controla vínculos específicos.</span><span class="sxs-lookup"><span data-stu-id="0dd06-178">This feature allows you to register a PWA with the browser using the web app manifest and declare that the browser handles specific links.</span></span>  <span data-ttu-id="0dd06-179">Para registrar un PWA con el explorador, agregue el miembro `url_handlers` opcional al archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="0dd06-179">To register a PWA with the browser, add the optional `url_handlers` member to the manifest file.</span></span>  <span data-ttu-id="0dd06-180">El `url_handlers` miembro es un que agrupa los orígenes de los URI que la aplicación desea `object[]` controlar.</span><span class="sxs-lookup"><span data-stu-id="0dd06-180">The `url_handlers` member is an `object[]` that groups the origins of URIs that the app wishes to handle.</span></span>  

<span data-ttu-id="0dd06-181">El explorador valida el control de vínculos mediante un `web-app-origin-association` archivo JSON que se encuentra en el origen.</span><span class="sxs-lookup"><span data-stu-id="0dd06-181">Link handling is validated by the browser using a `web-app-origin-association` JSON file that is located on the origin.</span></span>  <span data-ttu-id="0dd06-182">El archivo de origen afina aún más las rutas de acceso incluidas o excluidas en el origen.</span><span class="sxs-lookup"><span data-stu-id="0dd06-182">The origin file further fine-tunes the included or excluded paths at the origin.</span></span>  <span data-ttu-id="0dd06-183">Para obtener instrucciones detalladas sobre cómo probar el controlador de direcciones URL, vaya a [PWA como controladores de dirección URL][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span><span class="sxs-lookup"><span data-stu-id="0dd06-183">For detailed instructions about testing the URL handler, navigate to [PWAs as URL Handlers][GithubWicgPwaUrlHandlerBlobMainExplainerMd].</span></span>  

<span data-ttu-id="0dd06-184">Para obtener una vista previa del control de vínculos url en Microsoft Edge en Windows, vaya a Activar características [experimentales](#turn-on-experimental-features) y active Control de **direcciones URL de PWA de escritorio.**</span><span class="sxs-lookup"><span data-stu-id="0dd06-184">To preview URL link handling in Microsoft Edge on Windows, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWA URL  Handling**.</span></span>  

### <a name="example-of-the-url_handlers-in-the-manifest"></a><span data-ttu-id="0dd06-185">Ejemplo de la url_handlers en el manifiesto</span><span class="sxs-lookup"><span data-stu-id="0dd06-185">Example of the url_handlers in the manifest</span></span>  

<span data-ttu-id="0dd06-186">El siguiente fragmento de código es un manifiesto de aplicación web de ejemplo con el `url_handlers` miembro.</span><span class="sxs-lookup"><span data-stu-id="0dd06-186">The following code snippet is an example web app manifest with the `url_handlers` member.</span></span>  

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

<span data-ttu-id="0dd06-187">Un PWA coincide con un URI para el control de direcciones URL si el URI coincide con una de las cadenas de origen y el explorador valida que el origen acepta permitir que esta aplicación controle `url_handlers` dicho URI.</span><span class="sxs-lookup"><span data-stu-id="0dd06-187">A PWA matches a URI for URL handling if the URI matches one of the origin strings in `url_handlers` and the browser validates that the origin agrees to allow this app handle such a URI.</span></span>  

<span data-ttu-id="0dd06-188">El miembro contiene un origen que abarca el ámbito y otros orígenes no relacionados `url_handlers` de la PWA solicitante.</span><span class="sxs-lookup"><span data-stu-id="0dd06-188">The `url_handlers` member contains an origin that encompasses the scope and also other unrelated origins of the requesting PWA.</span></span>  <span data-ttu-id="0dd06-189">No restringir los URI al mismo ámbito o dominio que el PWA solicitante permite usar nombres de dominio diferentes para el mismo contenido, pero controlarlos con el mismo PWA.</span><span class="sxs-lookup"><span data-stu-id="0dd06-189">Not restricting URIs to the same scope or domain as the requesting PWA allows you to use different domain names for the same content but handle them with the same PWA.</span></span>  

#### <a name="wildcard-matching"></a><span data-ttu-id="0dd06-190">Coincidencia de caracteres comodín</span><span class="sxs-lookup"><span data-stu-id="0dd06-190">Wildcard matching</span></span>  

<span data-ttu-id="0dd06-191">Use el carácter comodín \( `*` \) para que coincida con uno o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="0dd06-191">Use the wildcard character \(`*`\) to match one or more characters.</span></span>  

<span data-ttu-id="0dd06-192">Se usa un prefijo comodín en las cadenas de origen del `url_handlers` miembro para que coincidan con los subdominios diferentes.</span><span class="sxs-lookup"><span data-stu-id="0dd06-192">A wildcard prefix is used in origin strings of the `url_handlers` member to match for different subdomains.</span></span>  <span data-ttu-id="0dd06-193">El prefijo debe ser `*.` para este uso.</span><span class="sxs-lookup"><span data-stu-id="0dd06-193">The prefix must be `*.` for this usage.</span></span>  <span data-ttu-id="0dd06-194">El `https` esquema se asume cuando se usa un prefijo comodín.</span><span class="sxs-lookup"><span data-stu-id="0dd06-194">The `https` scheme is assumed when you use a wildcard prefix.</span></span>  

<span data-ttu-id="0dd06-195">Por ejemplo, el `url_handlers` valor de miembro se establece en `*.contoso.com` coincidencias y , pero no `tenant.contoso.com` coincide con `www.tenant.contoso.com` `contoso.com` .</span><span class="sxs-lookup"><span data-stu-id="0dd06-195">For example, the `url_handlers` member value is set to `*.contoso.com` matches `tenant.contoso.com` and `www.tenant.contoso.com`, but doesn't match `contoso.com`.</span></span>  

<!-- Hold for future release -->  
<!--  ## Window Controls Overlay for installed desktop web apps  

To create an immersive title bar similar to a native app for your desktop installed web app.  The **Window Controls Overlay** feature  completes the following actions.  
    
1.  Removes the system reserved title bar.  It usually spans the width of the client frame.  
1.  Replaces it with an overlay.  It contains just the critical system required window controls necessary for a user to control the window itself.  
    
After it provides an overlay, the entire web client area is available for you to use.  This feature includes a manifest update.  It provides ways for you to determine the size and position of the overlay to help you arrange content.  
    
### Examples of title bar area customization  

This feature is based on the ability in native apps to customize the title bar.  You may customize a title bar for important app actions or notifications.  Review the following examples for Microsoft Visual Studio Code and Microsoft Teams.  

#### Visual Studio Code  

Microsoft Visual Studio Code is a popular editor built on Electron that ships on multiple desktop platforms.  

The following example displays how Visual Studio Code uses the title bar to maximize available screen real estate to include the current file name and top-level menu structure in the title bar.  

:::image type="complex" source="../media/visual-studio-code-title-customization.png" alt-text="An example of the title bar in Visual Studio Code" lightbox="../media/visual-studio-code-title-customization.png":::
   An example of the title bar in Visual Studio Code  
:::image-end:::  

#### Microsoft Teams  

Workplace collaboration and communication tool Microsoft Teams is also built with Electron and available on multiple desktop platforms.  In the following example, Microsoft Teams displays `back` and `forward` navigation buttons, a search box, and user profile controls.  

:::image type="complex" source="../media/teams-title-customization.png" alt-text="An example of the title bar in Microsoft Teams" lightbox="../media/teams-title-customization.png":::
   An example of the title bar in Microsoft Teams  
:::image-end:::  

### Overlay Window Controls on a Frameless Window  

To provide the maximum addressable area for web content, the browser creates a frameless window, removing all browser UI except for the window controls provided as an overlay.  
The window controls overlay ensures users still minimize, maximize, restore, and close the app.  It also provides access to relevant browser controls using the web app menu.  For Chromium-based browsers, the controls in the overlay.

*   A draggable region the same width and height of each of the window control buttons  
*   The **Settings and more** \(...\) button  
*   The window control buttons minimize, maximize, restore, and close  
    
The following scenarios include when browser displays other content in the controls overlay.  

*   When an installed web app is launched, the origin of the webpage displays to the left of the **Settings and more** \(...\) menu for a few seconds and then disappears.  
*   If a user interacts with an extension using the **Settings and more** \(...\) menu, the icon of the extension displays in the overlay to the left of the three-dot menu.  After you exit any extension dialog, the icon is removed from the overlay.  
    
| Language direction | Overlay location | Details |  
|:--- |:--- |:--- |  
| Left-to-right \(LTR\) | Upper left of the client area | The controls are flipped |  
| Right-to-left \(RTL\) | Upper right corner of the client area |  |  

>[!IMPORTANT]
> The overlay is always on top of the Z-index of the web content and accepts all user input without flowing it through to the web content.  

### Working around the Window Controls Overlay  

Your web content must be aware of the reserved area for the controls overlay.  Ensure the reserved area doesn't expect user interaction.  Query the browser for the bounding rectangle and visibility of the controls overlay.  The information is provided to you through JavaScript APIs and CSS environment variables.  

#### JavaScript APIs  

A new `windowControlsOverlay` object on the `window.navigator` property allows you to query the bounding rectangle of the controls overlay.  

The `windowControlsOverlay` object has the following two objects.  

*   `getBoundingClientRect()` returns a `DOMRect` object.  The `DOMRect` object represents the area under the window controls overlay.  
*   `visible` is a boolean that indicates that the controls overlay is rendered and displayed.  
    
> [!IMPORTANT]
> For privacy reasons, the `windowControlsOverlay` isn't accessible to `iframe` elements in the web content.  

Whenever the overlay is resized, a `geometrychange` event runs on the `navigator.windowControlsOverlay` object to notify the client to recalculate the content layout.  The recalculated content layout is based on the new bounding rectangle of the overlay.  

#### CSS Environment Variables  

Besides the JavaScript API, you may use CSS to query the bounding rectangle of the controls overlay.  Use the following four new CSS environment variables to accomplish to query.  

*   `titlebar-area-x`  
*   `titlebar-area-y`  
*   `titlebar-area-width`  
*   `titlebar-area-height`  
    
### Define Draggable Regions in Web Content  

Users expect to grab and drag the upper region of a window.  To accommodate the expectation, declare specific parts of the web content as draggable.  
To specify an element is draggable, use the webkit proprietary `-webkit-app-region` CSS property.  The CSS working group continues efforts to standardize the `app-region` property.  

To preview this feature in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and navigate to **Desktop PWA Window Controls Overlay**.   

### Custom title bar example  

The following example displays how the new features create a web app with a custom title bar.  

:::image type="complex" source="../media/teams-title-customization-example.png" alt-text="Example of a custom title bar in Microsoft Teams" lightbox="../media/teams-title-customization-example.png":::
   Example of a custom title bar in Microsoft Teams  
:::image-end:::  

#### manifest.webmanifest  

In the manifest, set `display_override` array to  `window-controls-overlay`.  Set the `theme_color` to your choice of color for the title bar.  Set the display mode to an appropriate fallback for when either `display_override` or `window-controls-overlay` isn't supported.  

The following code snippet includes the recommended manifest updates.  

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

### index.html  

The following IDs represent the two main regions of the webpage.  

*   `titleBarContainer`  
*   `mainContent`  
    
The `div` element with the `titleBar` ID is set to `draggable` and the search box `input` child element is set to `nonDraggable`.  

```html
<div id="titleBar" class=" draggable">
    <span class="draggable">Example PWA</span>
    <input class="nonDraggable" type="text" placeholder="Search"></input>
</div>
```

In the `div` element with the `titleBarContainer` ID, the `div` with the `titleBar` ID represents the visible portion of the title bar area.  

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
    <div id="mainContent">The rest of the webpage</div>
  </body>
</html>
```  

### style.css  

The draggable and non-draggable regions are set using `-webkit-app-region: drag` and `-webkit-app-region: no-drag`.  

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

For the `body` element, margins are set to `0` to ensure the title bar reaches to the edges of the window.  

```css
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
}
```  

The `titleBarContainer` ID uses `position: absolute` and sets the `top` to `titlebar-area-inset-top`, which attaches the container to the top of the webpage.  The `bottom` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-title-bar-height)` if the window controls overlay isn't visible.  The background color of the `titleBarContainer` ID is the same as the `theme_color`.  The width is set to `100%`, so that the `div` element fills the width of the webpage and flows under the overlay when it's visible for a contiguous appearance.  

```css
#titleBarContainer {
    position: absolute;
    top: env(titlebar-area-y, 0);
    bottom: env(titlebar-area-height, calc(100% - var(--fallback-title-bar-height)));
    width: 100%;
    background-color:#254B85;
}
```  

The `titleBar` ID also uses `position: absolute` and `top: titlebar-area-inset-top` to attaches it to the top of the window.  By default, it consumes the full width of the window.  The `left` and `right` edges are set to `titlebar-area-inset-left` and `titlebar-area-inset-right` respectively, both fall back to `0` when the values aren't set.  It also sets `user-select: none` to prevent any attempts to drag the window consumed instead it highlights text in the `div` element.  

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

The container for the `mainContent` ID is also fixed in place with `position: absolute` and is attached to the bottom of the webpage.  The `height` is set to `titlebar-area-inset-bottom` and falls back to `100% - var(--fallback-titlebar-height)` to fill the remaining space below the title bar.  It sets `overflow-y: scroll` to allow the contents to scroll vertically in the container.  

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

For cases where the browser doesn't support the window controls overlay, a CSS variable is added to set a default height for the title bar.  The bounds of the `titleBarContainer` and `mainContent` IDs are initially set to fill the entire client area, and you don't need to change it if the overlay isn't supported.  

The following code snippet includes all of the recommended css updates.

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
-->  

## <a name="run-on-os-login"></a><span data-ttu-id="0dd06-196">Ejecutar en inicio de sesión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0dd06-196">Run On OS Login</span></span>  

<span data-ttu-id="0dd06-197">Esta característica te permite configurar la aplicación para que se inicie automáticamente cuando el usuario inicie sesión en Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="0dd06-197">This feature allows you to configure your app to automatically launch when the user logs into Microsoft Windows.</span></span>  <span data-ttu-id="0dd06-198">Varias clases de aplicaciones aprovechan la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="0dd06-198">Several classes of apps take advantage of the capability.</span></span>  <span data-ttu-id="0dd06-199">Las clases de aplicaciones incluyen correo electrónico, chat, panel de supervisión y aplicaciones para mostrar datos en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="0dd06-199">The classes of apps include email, chat, monitoring dashboard, and real-time data display apps.</span></span>  <span data-ttu-id="0dd06-200">La funcionalidad permite a un usuario interactuar con las aplicaciones tan pronto como el usuario inicia sesión en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-200">The capability allows a user to engage with the apps as soon as the user logs into the OS.</span></span>  <span data-ttu-id="0dd06-201">Esta característica inicia automáticamente el PWA de la misma manera que se inicia manualmente.</span><span class="sxs-lookup"><span data-stu-id="0dd06-201">This feature automatically starts the PWA the same way it's launched manually.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="0dd06-202">**Ejecutar en inicio de sesión del sistema** operativo es una característica [eficaz.][GithubW3cPermissionsPowerfulFeature]</span><span class="sxs-lookup"><span data-stu-id="0dd06-202">**Run on OS Login** is a [powerful feature][GithubW3cPermissionsPowerfulFeature].</span></span>  <span data-ttu-id="0dd06-203">Los usuarios deben decidir si se activa la funcionalidad de la aplicación web instalada.</span><span class="sxs-lookup"><span data-stu-id="0dd06-203">Users should decide whether to turn on the capability for the installed web app.</span></span>  

### <a name="turn-on-run-on-os-login"></a><span data-ttu-id="0dd06-204">Activar Ejecutar inicio de sesión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0dd06-204">Turn on Run On OS Login</span></span>  

<span data-ttu-id="0dd06-205">Para activar ejecutar las **capacidades** de inicio de sesión del sistema operativo para su PWA, vaya a Activar características [experimentales](#turn-on-experimental-features) y active Las PWA de escritorio se ejecutan en el inicio **de sesión del sistema operativo.**</span><span class="sxs-lookup"><span data-stu-id="0dd06-205">To turn on **Run On OS Login** capabilities for your PWA, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **Desktop PWAs run on OS login**.</span></span>  

:::image type="complex" source="../media/desktop-pwas-run-on-os-login-flag.png" alt-text="Activar las PWA de escritorio que se ejecutan en el experimento inicio de sesión del sistema operativo" lightbox="../media/desktop-pwas-run-on-os-login-flag.png":::
   <span data-ttu-id="0dd06-207">Activar las **PWA de escritorio que se ejecutan en el experimento de inicio de sesión del sistema** operativo</span><span class="sxs-lookup"><span data-stu-id="0dd06-207">Turn on the **Desktop PWAs run on OS login** experiment</span></span>  
:::image-end:::  

### <a name="turn-on-the-feature-for-the-installed-web-app"></a><span data-ttu-id="0dd06-208">Activar la característica de la aplicación web instalada</span><span class="sxs-lookup"><span data-stu-id="0dd06-208">Turn on the feature for the installed web app</span></span>  

<span data-ttu-id="0dd06-209">Para activar la `Start app when you sign in` característica de un PWA instalado,</span><span class="sxs-lookup"><span data-stu-id="0dd06-209">To turn on the `Start app when you sign in` feature for an installed PWA,</span></span> 

1.  <span data-ttu-id="0dd06-210">Abra Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0dd06-210">Open Microsoft Edge.</span></span>   
1.  <span data-ttu-id="0dd06-211">Vaya a `edge://apps` .</span><span class="sxs-lookup"><span data-stu-id="0dd06-211">Navigate to `edge://apps`.</span></span>  
1.  <span data-ttu-id="0dd06-212">Mantenga el mouse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0dd06-212">Hover on your app.</span></span>  
1.  <span data-ttu-id="0dd06-213">Abra el menú contextual \(right-click\) y, a continuación, elija **Iniciar aplicación al iniciar sesión**.</span><span class="sxs-lookup"><span data-stu-id="0dd06-213">Open the contextual menu \(right-click\) and then choose **Start app when you sign in**.</span></span>  
    
    :::image type="complex" source="../media/turn-on-run-on-os-login-flag.png" alt-text="Usa el menú contextual para activar la aplicación Inicio al iniciar sesión en la característica de Microsoft Edge" lightbox="../media/turn-on-run-on-os-login-flag.png":::
       <span data-ttu-id="0dd06-215">Usa el menú contextual para activar la **aplicación Inicio al iniciar sesión en** la característica de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="0dd06-215">Use the contextual menu to turn on the **Start app when you sign in** feature in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="shortcuts"></a><span data-ttu-id="0dd06-216">Accesos directos</span><span class="sxs-lookup"><span data-stu-id="0dd06-216">Shortcuts</span></span>  

`Shortcuts` <span data-ttu-id="0dd06-217">es un nuevo miembro del archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="0dd06-217">is a new member of the manifest file.</span></span>  <span data-ttu-id="0dd06-218">Te permite definir vínculos a elementos, páginas web clave o acciones en la aplicación web.</span><span class="sxs-lookup"><span data-stu-id="0dd06-218">It allows you to define links to parts, key webpages, or actions in your web app.</span></span>  <span data-ttu-id="0dd06-219">Microsoft Windows lo integra como **jumplists**.</span><span class="sxs-lookup"><span data-stu-id="0dd06-219">Microsoft Windows integrates it as **Jumplists**.</span></span>  <span data-ttu-id="0dd06-220">**Las listas de accesos** emergentes definen menús emergentes que aparecen cuando se encuentra en uno de los siguientes elementos de la interfaz de usuario y se abre un menú contextual \(hacer clic con el botón secundario\).</span><span class="sxs-lookup"><span data-stu-id="0dd06-220">**Jumplists** define popup menus that appear when you on one of the following UI elements and open a contextual menu \(right-click\).</span></span>  

*   <span data-ttu-id="0dd06-221">Un icono en el menú Inicio</span><span class="sxs-lookup"><span data-stu-id="0dd06-221">A tile on the Start Menu</span></span>  
*   <span data-ttu-id="0dd06-222">Un icono en la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="0dd06-222">An icon on the Taskbar</span></span>  
    
<span data-ttu-id="0dd06-223">Cuando un usuario invoca un acceso directo, el usuario navega a la dirección especificada por el `url` miembro del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-223">When a user invokes a shortcut, the user navigates to the address specified by the `url` member of the shortcut.</span></span>  
  
:::image type="complex" source="../media/jumplists-on-windows-10.png" alt-text="Un ejemplo de listas de saltos en Windows 10" lightbox="../media/jumplists-on-windows-10.png":::
   <span data-ttu-id="0dd06-225">Un ejemplo de **listas de saltos** en Windows 10</span><span class="sxs-lookup"><span data-stu-id="0dd06-225">An example of **Jumplists** on Windows 10</span></span>  
:::image-end:::  

### <a name="shortcuts-in-the-manifest-file"></a><span data-ttu-id="0dd06-226">Accesos directos en el archivo de manifiesto</span><span class="sxs-lookup"><span data-stu-id="0dd06-226">Shortcuts in the Manifest file</span></span>  

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

#### <a name="properties-of-shortcuts"></a><span data-ttu-id="0dd06-227">Propiedades de accesos directos</span><span class="sxs-lookup"><span data-stu-id="0dd06-227">Properties of shortcuts</span></span>  

<span data-ttu-id="0dd06-228">Las siguientes propiedades definen cada acceso directo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-228">The following properties define each shortcut.</span></span>  

| <span data-ttu-id="0dd06-229">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0dd06-229">Property</span></span> | <span data-ttu-id="0dd06-230">Detalles</span><span class="sxs-lookup"><span data-stu-id="0dd06-230">Details</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="0dd06-231">Cadena que se muestra al usuario en **listas de saltos** o en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="0dd06-231">A string that is displayed to the user on **Jumplists** or the contextual menu.</span></span> |  
| `short_name` | <span data-ttu-id="0dd06-232">Cadena que se muestra cuando hay espacio insuficiente para mostrar el nombre completo del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-232">A string that is displayed when insufficient space exists to display the full name of the shortcut.</span></span> |  
| `description` | <span data-ttu-id="0dd06-233">Cadena que describe el propósito del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-233">A string that describes the purpose of the shortcut.</span></span>  <span data-ttu-id="0dd06-234">Es posible que se pueda acceder a ella mediante tecnología de asistencia.</span><span class="sxs-lookup"><span data-stu-id="0dd06-234">It may be accessed by assistive technology.</span></span> |  
| `url` | <span data-ttu-id="0dd06-235">Uri de la aplicación web que se abre cuando se activa el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-235">The URI in the web app that opens when the shortcut is activated.</span></span> |  
| `icons` | <span data-ttu-id="0dd06-236">Un conjunto de iconos que representa el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-236">A set of icons that represents the shortcut.</span></span> |  

## <a name="file-handling"></a><span data-ttu-id="0dd06-237">Administración de archivos</span><span class="sxs-lookup"><span data-stu-id="0dd06-237">File Handling</span></span>  

<span data-ttu-id="0dd06-238">La capacidad de registrarse como un controlador de tipos de archivo está en la fase de experimentación.</span><span class="sxs-lookup"><span data-stu-id="0dd06-238">The ability to register as a file type handler is in the experimentation phase.</span></span>  <span data-ttu-id="0dd06-239">Puedes especificar los tipos de archivo que controla la aplicación en una entrada de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="0dd06-239">You may specify the file types that your app handles in a manifest entry.</span></span>  <span data-ttu-id="0dd06-240">Durante la instalación, el sistema operativo host del usuario registra la aplicación como un controlador de archivos para los tipos de archivo enumerados.</span><span class="sxs-lookup"><span data-stu-id="0dd06-240">During installation, the user's host OS registers your app as a file handler for the listed file types.</span></span>  <span data-ttu-id="0dd06-241">Asegúrese de la existencia de la característica en el código de inicio de las `launchQueue` aplicaciones y de que controla el archivo.</span><span class="sxs-lookup"><span data-stu-id="0dd06-241">Ensure the existence of the feature `launchQueue` in your apps startup code and that it handles the file.</span></span>  

<span data-ttu-id="0dd06-242">Los exploradores basados en Chromium están probando y dando forma a esta característica.</span><span class="sxs-lookup"><span data-stu-id="0dd06-242">Chromium-based browsers are testing and shaping this feature.</span></span>  <span data-ttu-id="0dd06-243">Para obtener más información, incluidos los ejemplos de código, vaya a [Permitir que las aplicaciones web sean controladores de archivos][WebDevFileHandling].</span><span class="sxs-lookup"><span data-stu-id="0dd06-243">For more information including code examples, navigate to [Let web applications be file handlers][WebDevFileHandling].</span></span>  

<span data-ttu-id="0dd06-244">Para obtener una vista previa del control de archivos en Microsoft Edge para sistemas operativo de escritorio, vaya a Activar características [experimentales](#turn-on-experimental-features) y active api **de administración de archivos.**</span><span class="sxs-lookup"><span data-stu-id="0dd06-244">To preview file handling in Microsoft Edge for desktop OSs, navigate to [Turn on experimental features](#turn-on-experimental-features) and turn on **File Handling API**.</span></span>  
    
## <a name="providing-feedback-on-experimental-features"></a><span data-ttu-id="0dd06-245">Proporcionar comentarios sobre características experimentales</span><span class="sxs-lookup"><span data-stu-id="0dd06-245">Providing feedback on experimental features</span></span>  

<span data-ttu-id="0dd06-246">Para proporcionar comentarios sobre los experimentos de la aplicación web de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0dd06-246">To provide feedback on Microsoft Edge web app experiments.</span></span>  

*   <span data-ttu-id="0dd06-247">Envíe sus comentarios con **Configuración y Más** \( `...` \) > Enviar comentarios a **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="0dd06-247">Send your feedback using **Settings and More** \(`...`\) > **Send Feedback to Microsoft**.</span></span>  
*   <span data-ttu-id="0dd06-248">Seleccione `Alt` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="0dd06-248">Select `Alt`+`Shift`+`I`.</span></span>  
    
:::image type="complex" source="../media/send-feedback-from-progressive-web-app.png" alt-text="Enviar comentarios desde su PWA" lightbox="../media/send-feedback-from-progressive-web-app.png":::
   <span data-ttu-id="0dd06-250">Enviar comentarios desde su PWA</span><span class="sxs-lookup"><span data-stu-id="0dd06-250">Send Feedback from your PWA</span></span>  
:::image-end:::  

<!-- links -->  

[MicrosoftEdgeMain]: https://www.microsoft.com/edge "Microsoft Edge"  

[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Pruebas de origen | Desarrollador de Microsoft Edge"  
[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Registrar para el registro del controlador de protocolo de aplicación web | Microsoft Developer"  

[MdnDocsWebApiNavigatorRegisterprotocolhandlerWebBasedProtocolHandlers]: https://developer.mozilla.org/docs/Web/API/Navigator/registerProtocolHandler/Web-based_protocol_handlers "Controladores de protocolo basados en web | MDN"  

[GithubW3cPermissionsPowerfulFeature]: https://w3c.github.io/permissions#powerful-feature "Característica eficaz: permisos | GitHub"  

[GithubWicgPwaUrlHandlerBlobMainExplainerMd]: https://github.com/WICG/pwa-url-handler/blob/main/explainer.md "PwAs como controladores de dirección URL | GitHub"  

[WebDevFileHandling]: https://web.dev/file-handling "Permitir que las aplicaciones web sean controladores de archivos | web.dev"  
