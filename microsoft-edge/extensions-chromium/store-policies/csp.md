---
description: Directiva de seguridad de contenido para las extensiones de Edge (cromo).
title: Directiva de seguridad de contenido (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: f3769639465d048c42ad0705f74598fbd1db8a20
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015719"
---
# <span data-ttu-id="b279a-104">Directiva de seguridad de contenido \ (CSP \)</span><span class="sxs-lookup"><span data-stu-id="b279a-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="b279a-105">Para mitigar una gran clase de posibles problemas de scripting entre sitios, el sistema de extensiones Microsoft Edge ha incorporado el concepto general de [Directiva de seguridad de contenido \ (CSP \)][W3CContentSecurityPolicy].</span><span class="sxs-lookup"><span data-stu-id="b279a-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="b279a-106">Esto presenta directivas muy estrictas que hacen que las extensiones sean más seguras de forma predeterminada y le proporcionan la capacidad de crear y aplicar reglas que rijan los tipos de contenido que las extensiones y aplicaciones pueden cargar y ejecutar.</span><span class="sxs-lookup"><span data-stu-id="b279a-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="b279a-107">En general, CSP funciona como un mecanismo de bloqueo/allowlisting para los recursos cargados o ejecutados por las extensiones.</span><span class="sxs-lookup"><span data-stu-id="b279a-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="b279a-108">La definición de una directiva razonable para su extensión le permite considerar cuidadosamente los recursos que la extensión necesita y pedir al explorador que asegúrese de que son los únicos recursos a los que tiene acceso la extensión.</span><span class="sxs-lookup"><span data-stu-id="b279a-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="b279a-109">Estas directivas proporcionan seguridad y una mayor parte de los permisos de host y las solicitudes de extensión; son una capa adicional de protección, no un sustituto.</span><span class="sxs-lookup"><span data-stu-id="b279a-109">These policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="b279a-110">En la web, tal directiva se define a través de un elemento o encabezado HTTP `meta` .</span><span class="sxs-lookup"><span data-stu-id="b279a-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="b279a-111">En el sistema de extensión Microsoft Edge, ninguno de los mecanismos es adecuado.</span><span class="sxs-lookup"><span data-stu-id="b279a-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="b279a-112">En su lugar, se define una política de extensión a través del `manifest.json` archivo para la extensión de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b279a-112">Instead, an Extension policy is defined via the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="b279a-113">Para obtener información completa sobre la sintaxis de CSP, eche un vistazo a la especificación de la [política de seguridad de contenido][W3CContentSecurityPolicy] y el artículo ["una introducción a la Directiva de seguridad de contenido"][HTML5RocksIntroductionContentSecurityPolicy] en HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="b279a-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <span data-ttu-id="b279a-114">Restricciones de directiva predeterminadas</span><span class="sxs-lookup"><span data-stu-id="b279a-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="b279a-115">Los paquetes que no definen una no `manifest_version` tienen una directiva de seguridad de contenido predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b279a-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="b279a-116">Los que seleccionan `manifest_version` 2, tienen una directiva de seguridad de contenido predeterminada de:</span><span class="sxs-lookup"><span data-stu-id="b279a-116">Those that select `manifest_version` 2, have a default content security policy of:</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="b279a-117">Esta directiva agrega seguridad limitando las extensiones y aplicaciones de tres maneras:</span><span class="sxs-lookup"><span data-stu-id="b279a-117">This policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="b279a-118">Eval y las funciones relacionadas están deshabilitadas</span><span class="sxs-lookup"><span data-stu-id="b279a-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="b279a-119">El código como el siguiente no funciona:</span><span class="sxs-lookup"><span data-stu-id="b279a-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="b279a-120">La evaluación de cadenas de JavaScript como esta es un vector de ataques XSS común.</span><span class="sxs-lookup"><span data-stu-id="b279a-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="b279a-121">En su lugar, debe escribir código como el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b279a-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="b279a-122">No se ejecutan JavaScript en línea</span><span class="sxs-lookup"><span data-stu-id="b279a-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="b279a-123">No se ejecutan los JavaScripts en línea.</span><span class="sxs-lookup"><span data-stu-id="b279a-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="b279a-124">Esta restricción prohíbe tanto los bloques alineados como los `<script>` controladores de eventos alineados, como `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="b279a-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="b279a-125">La primera restricción elimina una enorme clase de ataques de scripting entre sitios, lo que le impide ejecutar accidentalmente la secuencia de comandos proporcionada por un tercero malintencionado.</span><span class="sxs-lookup"><span data-stu-id="b279a-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="b279a-126">Sin embargo, le pedirá que escriba su código con una separación clara entre el contenido y el comportamiento \ (¿qué debe hacer? de todos modos, ¿bien? \).</span><span class="sxs-lookup"><span data-stu-id="b279a-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="b279a-127">Un ejemplo puede hacer que sea más claro.</span><span class="sxs-lookup"><span data-stu-id="b279a-127">An example may make this clearer.</span></span>  <span data-ttu-id="b279a-128">Puede intentar escribir un elemento emergente de acción del explorador como un único `pop-up.html` contenedor:</span><span class="sxs-lookup"><span data-stu-id="b279a-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script>
            function awesome() {
                // do something awesome!
            }
            
            function totallyAwesome() {
                // do something TOTALLY awesome!
            }
            
            function clickHandler(element) {
                setTimeout("awesome(); totallyAwesome()", 1000);
            }
            
            function main() {
                // Initialization work goes here.
            }
        </script>
    </head>
    <body onload="main();">
        <button onclick="clickHandler(this)">
            Click for awesomeness!
        </button>
    </body>
</html>
```  

<span data-ttu-id="b279a-129">Deben cambiarse tres cosas para que este funcione de la manera esperada:</span><span class="sxs-lookup"><span data-stu-id="b279a-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="b279a-130">La `clickHandler` definición se debe mover a un archivo JavaScript externo \ ( `popup.js` puede ser un buen objetivo).</span><span class="sxs-lookup"><span data-stu-id="b279a-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="b279a-131">Las definiciones de los controladores de eventos en línea se deben volver a escribir en términos de `addEventListener` y extraer en `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="b279a-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="b279a-132">Si actualmente inicia su programa con un código como `<body onload="main();">` , considere la posibilidad de reemplazarlo enlazando el `DOMContentLoaded` evento del documento o el `load` evento de la ventana, en función de sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="b279a-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="b279a-133">Use el antiguo, ya que generalmente se desencadena más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="b279a-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="b279a-134">La `setTimeout` llamada se debe volver a escribir para evitar convertir la cadena `"awesome(); totallyAwesome()"` en JavaScript para ejecutarla.</span><span class="sxs-lookup"><span data-stu-id="b279a-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="b279a-135">Esos cambios pueden tener un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="b279a-135">Those changes may look something like the following:</span></span>  

```javascript
function awesome() {
    // Do something awesome!
}

function totallyAwesome() {
    // do something TOTALLY awesome!
}

function awesomeTask() {
    awesome();
    totallyAwesome();
}

function clickHandler(e) {
    setTimeout(awesomeTask, 1000);
}

function main() {
    // Initialization work goes here.
}

// Add event listeners once the DOM has fully loaded by listening for the
// `DOMContentLoaded` event on the document, and adding your listeners to
// specific elements when it triggers.
document.addEventListener('DOMContentLoaded', function () {
    document.querySelector('button').addEventListener('click', clickHandler);
    main();
});
```  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="popup.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

**<span data-ttu-id="b279a-136">Solo se cargan los recursos de objetos y scripts locales</span><span class="sxs-lookup"><span data-stu-id="b279a-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="b279a-137">Los recursos de scripts y objetos solo se pueden cargar desde el paquete de extensión, no desde la web en general.</span><span class="sxs-lookup"><span data-stu-id="b279a-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="b279a-138">Esto garantiza que su extensión solo ejecutará el código que haya aprobado específicamente, evitando que un atacante de red activa redirija su solicitud de un recurso por error.</span><span class="sxs-lookup"><span data-stu-id="b279a-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="b279a-139">En lugar de escribir código que depende de jQuery \ (o cualquier otra biblioteca \) que se cargue desde una red CDN externa, considere la posibilidad de incluir la versión específica de jQuery en el paquete de extensión.</span><span class="sxs-lookup"><span data-stu-id="b279a-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="b279a-140">Es decir, en lugar de:</span><span class="sxs-lookup"><span data-stu-id="b279a-140">That is, instead of:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

<span data-ttu-id="b279a-141">Descargar el archivo, incluirlo en el paquete y escribir:</span><span class="sxs-lookup"><span data-stu-id="b279a-141">Download the file, include it in your package, and write:</span></span>  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

## <span data-ttu-id="b279a-142">Cómo relajar la directiva predeterminada</span><span class="sxs-lookup"><span data-stu-id="b279a-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="b279a-143">Script en línea</span><span class="sxs-lookup"><span data-stu-id="b279a-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="b279a-144">Los scripts en línea pueden permitirse especificando el hash codificado en base64 del código fuente de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="b279a-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="b279a-145">Este hash debe ir precedido por el algoritmo hash usado \ (SHA256, SHA384 o SHA512 \).</span><span class="sxs-lookup"><span data-stu-id="b279a-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="b279a-146">Consulta el [uso de hash de \<script\> los elementos][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] para obtener un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b279a-146">See [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] for an example.</span></span>  

**<span data-ttu-id="b279a-147">Script remoto</span><span class="sxs-lookup"><span data-stu-id="b279a-147">Remote Script</span></span>**  

<span data-ttu-id="b279a-148">Si necesita algunos recursos de JavaScript o de objeto externo, puede relajar la Directiva en una medida limitada por allowlisting los orígenes seguros de los que se deben aceptar las secuencias de comandos.</span><span class="sxs-lookup"><span data-stu-id="b279a-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="b279a-149">Compruebe que los recursos en tiempo de ejecución cargados con permisos elevados de una extensión son exactamente los recursos que espera y no son reemplazados por un atacante de red activo.</span><span class="sxs-lookup"><span data-stu-id="b279a-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="b279a-150">Dado que los [ataques de intermediario][WikiManMiddleAttacks] son sencillos y no detectables a través de http, no se aceptan esos orígenes.</span><span class="sxs-lookup"><span data-stu-id="b279a-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="b279a-151">En la actualidad, los desarrolladores pueden lista denegados origen con los siguientes esquemas: `blob` ,, `filesystem` `https` , y `extension` .</span><span class="sxs-lookup"><span data-stu-id="b279a-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="b279a-152">La parte del host del origen debe especificarse explícitamente para `https` los `extension` esquemas y.</span><span class="sxs-lookup"><span data-stu-id="b279a-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="b279a-153">Los caracteres comodín genéricos, como https:, `https://*` y `https://*.com` no están permitidos; se permiten los caracteres comodín de subdominio, como por ejemplo `https://*.example.com` .</span><span class="sxs-lookup"><span data-stu-id="b279a-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="b279a-154">Los dominios de la [lista de sufijos públicos][PublicSuffixList] también se visualizan como dominios genéricos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b279a-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="b279a-155">Para cargar un recurso desde estos dominios, el subdominio debe mostrarse explícitamente.</span><span class="sxs-lookup"><span data-stu-id="b279a-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="b279a-156">Por ejemplo, `https://*.cloudfront.net` no es válido, pero `https://XXXX.cloudfront.net` y `https://*.XXXX.cloudfront.net` puede ser allowlisted.</span><span class="sxs-lookup"><span data-stu-id="b279a-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be allowlisted.</span></span>  

<span data-ttu-id="b279a-157">Por facilidad de desarrollo, los recursos cargados por HTTP desde los servidores en el equipo local pueden allowlisted.</span><span class="sxs-lookup"><span data-stu-id="b279a-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be allowlisted.</span></span>  <span data-ttu-id="b279a-158">Puede lista denegados los orígenes de scripts y objetos en cualquier puerto de `http://127.0.0.1` o `http://localhost` .</span><span class="sxs-lookup"><span data-stu-id="b279a-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="b279a-159">La restricción de los recursos cargados por HTTP solo se aplica a los recursos que se ejecutan directamente.</span><span class="sxs-lookup"><span data-stu-id="b279a-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="b279a-160">Sigue siendo gratis, por ejemplo, hacer conexiones de XMLHTTPRequest a cualquier origen que desee; la directiva predeterminada no se restringe `connect-src` de ninguna manera a las demás directivas de CSP ni ninguna de ellas.</span><span class="sxs-lookup"><span data-stu-id="b279a-160">You are still free, for example, to make XMLHTTPRequest connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="b279a-161">Una definición de directiva relajada que permite que los recursos de script se carguen desde example.com a través de HTTPS puede tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="b279a-161">A relaxed policy definition which allows script resources to be loaded from example.com over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="b279a-162">Ambos `script-src` y `object-src` los define la Directiva.</span><span class="sxs-lookup"><span data-stu-id="b279a-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="b279a-163">Microsoft Edge no acepta una directiva que no limite cada uno de estos valores a \ (por lo menos \) ' `self` '.</span><span class="sxs-lookup"><span data-stu-id="b279a-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="b279a-164">JavaScript evaluado</span><span class="sxs-lookup"><span data-stu-id="b279a-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="b279a-165">La Directiva en relación con las `eval()` funciones relacionadas como `setTimeout(String)` , `setInterval(String)` y que se pueden `new Function(String)` relajar agregando `unsafe-eval` a la Directiva:</span><span class="sxs-lookup"><span data-stu-id="b279a-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="b279a-166">Sin embargo, le recomendamos especialmente que lo haga.</span><span class="sxs-lookup"><span data-stu-id="b279a-166">However, we strongly recommend against doing this.</span></span>  <span data-ttu-id="b279a-167">Estas funciones son vectores de ataque XSS.</span><span class="sxs-lookup"><span data-stu-id="b279a-167">These functions are notorious XSS attack vectors.</span></span>  

## <span data-ttu-id="b279a-168">Ajustar la directiva predeterminada</span><span class="sxs-lookup"><span data-stu-id="b279a-168">Tightening the default policy</span></span>  

<span data-ttu-id="b279a-169">Por supuesto, puede ajustar esta directiva a cualquier medida que su extensión permita para aumentar la seguridad a costa de comodidad.</span><span class="sxs-lookup"><span data-stu-id="b279a-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="b279a-170">Para especificar que la extensión solo puede cargar recursos de cualquier tipo \ (imágenes, etc.) del paquete de extensión asociado, por ejemplo, una directiva de `default-src 'self'` puede ser adecuada.</span><span class="sxs-lookup"><span data-stu-id="b279a-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <span data-ttu-id="b279a-171">Scripts de contenido</span><span class="sxs-lookup"><span data-stu-id="b279a-171">Content Scripts</span></span>  

<span data-ttu-id="b279a-172">La Directiva que se está discutiendo se aplica a las páginas de fondo y a las páginas de evento de la extensión.</span><span class="sxs-lookup"><span data-stu-id="b279a-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="b279a-173">La forma en que los scripts de contenido se aplican a los scripts de contenido es más complicado.</span><span class="sxs-lookup"><span data-stu-id="b279a-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="b279a-174">Los scripts de contenido generalmente no están sujetos al CSP de la extensión.</span><span class="sxs-lookup"><span data-stu-id="b279a-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="b279a-175">Dado que los scripts de contenido no son HTML, la principal repercusión de esto es que pueden usarse `eval` incluso si el CSP de la extensión no especifica `unsafe-eval` , aunque no se recomienda.</span><span class="sxs-lookup"><span data-stu-id="b279a-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="b279a-176">Además, el CSP de la página no se aplica a los scripts de contenido.</span><span class="sxs-lookup"><span data-stu-id="b279a-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="b279a-177">Más complicadas son las `<script>` etiquetas que los scripts de contenido crean y se colocan en el Dom de la página en la que se están ejecutando.</span><span class="sxs-lookup"><span data-stu-id="b279a-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="b279a-178">Se hace referencia a estos como scripts inyectados en DOM hacia adelante.</span><span class="sxs-lookup"><span data-stu-id="b279a-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="b279a-179">DOM inyectado los scripts que se ejecutan inmediatamente después de la inserción en la página se ejecuta como cabría esperar.</span><span class="sxs-lookup"><span data-stu-id="b279a-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="b279a-180">Imagínese un script de contenido con el código siguiente como un ejemplo simple:</span><span class="sxs-lookup"><span data-stu-id="b279a-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="b279a-181">Esta secuencia de comandos de contenido provoca una `alert` inmediata `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="b279a-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="b279a-182">Ten en cuenta que esto se ejecuta independientemente de la Directiva que una página puede especificar.</span><span class="sxs-lookup"><span data-stu-id="b279a-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="b279a-183">Sin embargo, el comportamiento es más complicado tanto dentro de la secuencia de comandos inyectada de DOM como en cualquier secuencia de comandos que no se ejecuta inmediatamente después de la inserción.</span><span class="sxs-lookup"><span data-stu-id="b279a-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="b279a-184">Suponga que su extensión se está ejecutando en una página que proporciona un CSP asociado que especifica `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="b279a-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="b279a-185">Ahora Imagine que el script de contenido ejecuta el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="b279a-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="b279a-186">Si un usuario hace clic en el botón, el `onclick` script no se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="b279a-186">If a user clicks on that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="b279a-187">Esto se debe a que el script no se ejecutó inmediatamente y el código no se interpreta hasta que el evento click no se considera parte del script de contenido, por lo que el CSP de la página \ (no la extensión \) restringe el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="b279a-187">This is because the script did not immediately run and code is not interpreted until the click event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="b279a-188">Y como ese CSP no lo especifica `unsafe-inline` , el controlador de eventos inline se bloquea.</span><span class="sxs-lookup"><span data-stu-id="b279a-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="b279a-189">La manera correcta de implementar el comportamiento deseado en este caso puede ser agregar el `onclick` controlador como una función de la secuencia de comandos de contenido de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b279a-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="b279a-190">Otro problema similar se produce si el script de contenido ejecuta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b279a-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="b279a-191">En este caso, se ejecutará la secuencia de comandos y aparecerá la alerta.</span><span class="sxs-lookup"><span data-stu-id="b279a-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="b279a-192">Sin embargo, tomemos este caso:</span><span class="sxs-lookup"><span data-stu-id="b279a-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="b279a-193">Mientras se ejecuta el script inicial, la llamada a `eval` está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="b279a-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="b279a-194">Es decir, mientras se permite el tiempo de ejecución de los scripts iniciales, el comportamiento dentro del script se regula por el CSP de la página.</span><span class="sxs-lookup"><span data-stu-id="b279a-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="b279a-195">Por lo tanto, según el modo en que se escriben las secuencias de comandos inyectadas de DOM en la extensión, los cambios en el CSP de la página pueden afectar al comportamiento de la extensión.</span><span class="sxs-lookup"><span data-stu-id="b279a-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="b279a-196">Dado que los scripts de contenido no se ven afectados por el CSP de la página, esta es una excelente razón para poner el mayor comportamiento posible de la extensión en el script de contenido en lugar de las secuencias de comandos inyectadas en DOM.</span><span class="sxs-lookup"><span data-stu-id="b279a-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Introducción a la Directiva de seguridad de contenido: Rock HTML5"  
[PublicSuffixList]: https://publicsuffix.org/list "VER LA LISTA DE SUFIJOS PÚBLICOS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Uso de hash para \ <scripts \ > elementos-nivel 2 de directiva de seguridad de contenido"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Nivel 3 de directiva de seguridad de contenido"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Ataque de hombre en el medio: Wikipedia"  

> [!NOTE]
> <span data-ttu-id="b279a-202">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b279a-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b279a-203">La página original se encuentra [aquí](https://developer.chrome.com/extensions/contentSecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="b279a-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b279a-205">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b279a-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
