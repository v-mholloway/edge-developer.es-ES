---
description: Directiva de seguridad de contenido para extensiones perimetrales (Chromium).
title: Directiva de seguridad de contenido (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 8307482e780b4d631edffd976cca7ba724e2ad40
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397520"
---
# <a name="content-security-policy-csp"></a><span data-ttu-id="2243e-104">Directiva de seguridad de contenido \(CSP\)</span><span class="sxs-lookup"><span data-stu-id="2243e-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="2243e-105">Para mitigar una gran clase de posibles problemas de scripting entre sitios, el sistema de extensión perimetral de Microsoft ha incorporado el concepto general de directiva de seguridad de contenido [\(CSP\)][W3CContentSecurityPolicy].</span><span class="sxs-lookup"><span data-stu-id="2243e-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="2243e-106">Esto presenta algunas directivas bastante estrictas que hacen que las extensiones sean más seguras de forma predeterminada y le proporciona la capacidad de crear y aplicar reglas que rigen los tipos de contenido que pueden cargarse y ejecutarse por las extensiones y las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2243e-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="2243e-107">En general, CSP funciona como un mecanismo de bloqueo/lista de permitidos para los recursos cargados o ejecutados por las extensiones.</span><span class="sxs-lookup"><span data-stu-id="2243e-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="2243e-108">La definición de una directiva razonable para su extensión le permite tener en cuenta cuidadosamente los recursos que necesita la extensión y solicitar al explorador que se asegure de que esos son los únicos recursos a los que tiene acceso la Extensión.</span><span class="sxs-lookup"><span data-stu-id="2243e-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="2243e-109">Las directivas proporcionan seguridad por encima de los permisos de host que solicita la extensión; son una capa adicional de protección, no un reemplazo.</span><span class="sxs-lookup"><span data-stu-id="2243e-109">The policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="2243e-110">En la web, dicha directiva se define a través de un elemento o encabezado `meta` HTTP.</span><span class="sxs-lookup"><span data-stu-id="2243e-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="2243e-111">Dentro del sistema de extensión de Microsoft Edge, ninguno de los dos es un mecanismo adecuado.</span><span class="sxs-lookup"><span data-stu-id="2243e-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="2243e-112">En su lugar, se define una directiva de extensión con `manifest.json` el archivo de la extensión de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2243e-112">Instead, an Extension policy is defined using the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="2243e-113">Para obtener información completa acerca de la [][W3CContentSecurityPolicy] sintaxis de CSP, consulte la especificación de directiva de seguridad de contenido y el artículo "Introducción a la directiva de seguridad de [contenido"][HTML5RocksIntroductionContentSecurityPolicy] en HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="2243e-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <a name="default-policy-restrictions"></a><span data-ttu-id="2243e-114">Restricciones de directiva predeterminadas</span><span class="sxs-lookup"><span data-stu-id="2243e-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="2243e-115">Los paquetes que no definen una `manifest_version` no tienen una directiva de seguridad de contenido predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2243e-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="2243e-116">Los paquetes que `manifest_version` elijan 2 tienen la siguiente directiva de seguridad de contenido predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2243e-116">Packages that choose `manifest_version` 2, have a the follwoing default content security policy.</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="2243e-117">La directiva agrega seguridad limitando las extensiones y las aplicaciones de tres maneras:</span><span class="sxs-lookup"><span data-stu-id="2243e-117">The policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="2243e-118">Las funciones Eval y relacionadas están deshabilitadas</span><span class="sxs-lookup"><span data-stu-id="2243e-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="2243e-119">El código como el siguiente no funciona:</span><span class="sxs-lookup"><span data-stu-id="2243e-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="2243e-120">Evaluar cadenas de JavaScript como esta es un vector de ataque XSS común.</span><span class="sxs-lookup"><span data-stu-id="2243e-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="2243e-121">En su lugar, debe escribir código como:</span><span class="sxs-lookup"><span data-stu-id="2243e-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="2243e-122">JavaScript en línea no se ejecuta</span><span class="sxs-lookup"><span data-stu-id="2243e-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="2243e-123">JavaScript en línea no se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="2243e-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="2243e-124">Esta restricción prohíbe tanto los bloques en línea como los controladores de eventos en `<script>` línea, como `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="2243e-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="2243e-125">La primera restricción elimina una gran clase de ataques de scripting entre sitios al hacer que sea imposible ejecutar accidentalmente el script proporcionado por un tercero malintencionado.</span><span class="sxs-lookup"><span data-stu-id="2243e-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="2243e-126">Sin embargo, requiere que escriba el código con una separación limpia entre el contenido y el comportamiento \(que, por supuesto, debe hacer de todos modos, ¿no?\).</span><span class="sxs-lookup"><span data-stu-id="2243e-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="2243e-127">Un ejemplo puede hacerlo más claro.</span><span class="sxs-lookup"><span data-stu-id="2243e-127">An example may make this clearer.</span></span>  <span data-ttu-id="2243e-128">Puede intentar escribir una ventana emergente Acción del explorador como una sola `pop-up.html` que contenga:</span><span class="sxs-lookup"><span data-stu-id="2243e-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

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

<span data-ttu-id="2243e-129">Tres cosas deben cambiar para que esto funcione de la manera que espera:</span><span class="sxs-lookup"><span data-stu-id="2243e-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="2243e-130">La `clickHandler` definición debe moverse a un archivo JavaScript externo \( `popup.js` puede ser un buen destino).</span><span class="sxs-lookup"><span data-stu-id="2243e-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="2243e-131">Las definiciones del controlador de eventos en línea deben reescribirse en términos de y `addEventListener` extraerse en `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="2243e-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="2243e-132">Si está iniciando el programa con código como , considere la posibilidad de reemplazarlo conectando al evento del documento o al evento de la ventana, según `<body onload="main();">` `DOMContentLoaded` sus `load` requisitos.</span><span class="sxs-lookup"><span data-stu-id="2243e-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="2243e-133">Use el primero, ya que generalmente se desencadena más rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2243e-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="2243e-134">La `setTimeout` llamada debe reescribirse para evitar convertir la cadena `"awesome(); totallyAwesome()"` en JavaScript para que se ejecute.</span><span class="sxs-lookup"><span data-stu-id="2243e-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="2243e-135">Estos cambios pueden tener un aspecto parecido al siguiente:</span><span class="sxs-lookup"><span data-stu-id="2243e-135">Those changes may look something like the following:</span></span>  

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

**<span data-ttu-id="2243e-136">Solo se cargan los recursos de script y objeto locales</span><span class="sxs-lookup"><span data-stu-id="2243e-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="2243e-137">Los recursos de script y objeto solo se pueden cargar desde el paquete de extensión, no desde la web en general.</span><span class="sxs-lookup"><span data-stu-id="2243e-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="2243e-138">Esto garantiza que la extensión solo ejecute el código que aprobó específicamente, lo que impide que un atacante de red activo redirija malintencionadamente la solicitud de un recurso.</span><span class="sxs-lookup"><span data-stu-id="2243e-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="2243e-139">En lugar de escribir código que dependa de la carga de jQuery \(o cualquier otra biblioteca\) desde una red CDN externa, considere la posibilidad de incluir la versión específica de jQuery en el paquete de extensión.</span><span class="sxs-lookup"><span data-stu-id="2243e-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="2243e-140">Es decir, en lugar de:</span><span class="sxs-lookup"><span data-stu-id="2243e-140">That is, instead of:</span></span>  

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

<span data-ttu-id="2243e-141">Descargue el archivo, inscríbalo en el paquete y escriba:</span><span class="sxs-lookup"><span data-stu-id="2243e-141">Download the file, include it in your package, and write:</span></span>  

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

## <a name="relaxing-the-default-policy"></a><span data-ttu-id="2243e-142">Relajación de la directiva predeterminada</span><span class="sxs-lookup"><span data-stu-id="2243e-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="2243e-143">Script en línea</span><span class="sxs-lookup"><span data-stu-id="2243e-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="2243e-144">Los scripts en línea pueden permitirse especificando el hash codificado en base64 del código fuente en la directiva.</span><span class="sxs-lookup"><span data-stu-id="2243e-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="2243e-145">Este hash debe ir precedido por el algoritmo hash usado \(sha256, sha384 o sha512\).</span><span class="sxs-lookup"><span data-stu-id="2243e-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="2243e-146">Para obtener un ejemplo, vaya a [Uso hash de los \<script\> elementos][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span><span class="sxs-lookup"><span data-stu-id="2243e-146">For an example, navigate to [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span></span>  

**<span data-ttu-id="2243e-147">Script remoto</span><span class="sxs-lookup"><span data-stu-id="2243e-147">Remote Script</span></span>**  

<span data-ttu-id="2243e-148">Si necesita algunos recursos de objeto u JavaScript externos, puede que relaje la directiva en una medida limitada al permitir la lista de orígenes seguros desde los que se deben aceptar scripts.</span><span class="sxs-lookup"><span data-stu-id="2243e-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="2243e-149">Compruebe que los recursos en tiempo de ejecución cargados con permisos elevados de una extensión son exactamente los recursos que espera y que no se reemplazan por un atacante de red activo.</span><span class="sxs-lookup"><span data-stu-id="2243e-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="2243e-150">Como los ataques de tipo [man-in-the-middle][WikiManMiddleAttacks] son triviales e indetectables a través de HTTP, esos orígenes no se aceptan.</span><span class="sxs-lookup"><span data-stu-id="2243e-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="2243e-151">Actualmente, los desarrolladores pueden permitir orígenes de lista con los siguientes esquemas: `blob` , `filesystem` , y `https` `extension` .</span><span class="sxs-lookup"><span data-stu-id="2243e-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="2243e-152">La parte host del origen debe especificarse explícitamente para los `https` esquemas `extension` y.</span><span class="sxs-lookup"><span data-stu-id="2243e-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="2243e-153">Caracteres comodín genéricos como https:, y no están permitidos; se permiten caracteres `https://*` `https://*.com` comodín de subdominio `https://*.example.com` como.</span><span class="sxs-lookup"><span data-stu-id="2243e-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="2243e-154">Los dominios de la [lista Sufijo público][PublicSuffixList] también se ven como dominios genéricos de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="2243e-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="2243e-155">Para cargar un recurso desde estos dominios, el subdominio debe aparecer explícitamente.</span><span class="sxs-lookup"><span data-stu-id="2243e-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="2243e-156">Por ejemplo, `https://*.cloudfront.net` no es válido, pero `https://XXXX.cloudfront.net` puede `https://*.XXXX.cloudfront.net` ser `allowlisted` .</span><span class="sxs-lookup"><span data-stu-id="2243e-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be `allowlisted`.</span></span>  

<span data-ttu-id="2243e-157">Para facilitar el desarrollo, los recursos cargados a través de HTTP desde los servidores de la máquina local pueden ser `allowlisted` .</span><span class="sxs-lookup"><span data-stu-id="2243e-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be `allowlisted`.</span></span>  <span data-ttu-id="2243e-158">Puede permitir el script de lista y los orígenes de objetos en cualquier puerto de cualquiera `http://127.0.0.1` o `http://localhost` .</span><span class="sxs-lookup"><span data-stu-id="2243e-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="2243e-159">La restricción de los recursos cargados a través de HTTP solo se aplica a los recursos que se ejecutan directamente.</span><span class="sxs-lookup"><span data-stu-id="2243e-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="2243e-160">Sigue siendo libre, por ejemplo, para realizar conexiones a cualquier origen que quiera; la directiva predeterminada no restringe ni ninguna de las otras directivas `XMLHTTPRequest` CSP de ninguna `connect-src` manera.</span><span class="sxs-lookup"><span data-stu-id="2243e-160">You are still free, for example, to make `XMLHTTPRequest` connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="2243e-161">Una definición de directiva relajada que permite cargar recursos de script desde `example.com` https puede tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="2243e-161">A relaxed policy definition which allows script resources to be loaded from `example.com` over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="2243e-162">Ambos `script-src` y `object-src` están definidos por la directiva.</span><span class="sxs-lookup"><span data-stu-id="2243e-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="2243e-163">Microsoft Edge no acepta una directiva que no limite cada uno de estos valores a \(al menos\) ' `self` '.</span><span class="sxs-lookup"><span data-stu-id="2243e-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="2243e-164">JavaScript evaluado</span><span class="sxs-lookup"><span data-stu-id="2243e-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="2243e-165">La directiva y las funciones relacionadas como , y pueden ser `eval()` `setTimeout(String)` `setInterval(String)` `new Function(String)` relajadas agregando `unsafe-eval` a la directiva:</span><span class="sxs-lookup"><span data-stu-id="2243e-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="2243e-166">Sin embargo, debe evitar las directivas de relajación.</span><span class="sxs-lookup"><span data-stu-id="2243e-166">However, you should avoid relaxing policies.</span></span>  <span data-ttu-id="2243e-167">Las funciones son vectores de ataque XSS notorios.</span><span class="sxs-lookup"><span data-stu-id="2243e-167">The functions are notorious XSS attack vectors.</span></span>  

## <a name="tightening-the-default-policy"></a><span data-ttu-id="2243e-168">Ajustar la directiva predeterminada</span><span class="sxs-lookup"><span data-stu-id="2243e-168">Tightening the default policy</span></span>  

<span data-ttu-id="2243e-169">Por supuesto, puede ajustar esta directiva en la medida en que la extensión lo permita para aumentar la seguridad a expensas de la comodidad.</span><span class="sxs-lookup"><span data-stu-id="2243e-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="2243e-170">Para especificar que la extensión solo puede cargar recursos de cualquier tipo \(imágenes, y así sucesivamente\) del paquete de extensión asociado, por ejemplo, una directiva de puede `default-src 'self'` ser adecuada.</span><span class="sxs-lookup"><span data-stu-id="2243e-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a><span data-ttu-id="2243e-171">Scripts de contenido</span><span class="sxs-lookup"><span data-stu-id="2243e-171">Content Scripts</span></span>  

<span data-ttu-id="2243e-172">La directiva que se está analizando se aplica a las páginas en segundo plano y a las páginas de eventos de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2243e-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="2243e-173">El modo en que los scripts de contenido se aplican a los scripts de contenido de la extensión es más complicado.</span><span class="sxs-lookup"><span data-stu-id="2243e-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="2243e-174">Por lo general, los scripts de contenido no están sujetos al CSP de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2243e-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="2243e-175">Dado que los scripts de contenido no son HTML, el impacto principal de esto es que pueden usar incluso si el CSP de la extensión no especifica , aunque esto `eval` `unsafe-eval` no se recomienda.</span><span class="sxs-lookup"><span data-stu-id="2243e-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="2243e-176">Además, el CSP de la página no se aplica a los scripts de contenido.</span><span class="sxs-lookup"><span data-stu-id="2243e-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="2243e-177">Más complicadas son las etiquetas que los scripts de contenido crean `<script>` y ponen en el DOM de la página en la que se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="2243e-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="2243e-178">A estos se les hace referencia como scripts inyectados por DOM en el futuro.</span><span class="sxs-lookup"><span data-stu-id="2243e-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="2243e-179">Los scripts inyectados por DOM que se ejecutan inmediatamente después de la inyección en la página se ejecutan como puede esperar.</span><span class="sxs-lookup"><span data-stu-id="2243e-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="2243e-180">Imagine un script de contenido con el siguiente código como un ejemplo sencillo:</span><span class="sxs-lookup"><span data-stu-id="2243e-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="2243e-181">Este script de contenido provoca `alert` una inmediatamente después de `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="2243e-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="2243e-182">Tenga en cuenta que esto se ejecuta independientemente de la directiva que pueda especificar una página.</span><span class="sxs-lookup"><span data-stu-id="2243e-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="2243e-183">Sin embargo, el comportamiento se vuelve más complicado tanto dentro de ese script inyectado por DOM como para cualquier script que no se ejecute inmediatamente después de la inyección.</span><span class="sxs-lookup"><span data-stu-id="2243e-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="2243e-184">Imagine que la extensión se ejecuta en una página que proporciona un CSP asociado que especifica `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="2243e-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="2243e-185">Ahora imagine que el script de contenido ejecuta el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="2243e-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="2243e-186">Si un usuario elige ese botón, el `onclick` script no se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="2243e-186">If a user chooses that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="2243e-187">Esto se debe a que el script no se ha ejecutado inmediatamente y el código no se interpreta hasta que el evento se produce no se considera parte del script de contenido, por lo que el CSP de la página \(no de extension\) restringe el `click` comportamiento.</span><span class="sxs-lookup"><span data-stu-id="2243e-187">This is because the script did not immediately run and code is not interpreted until the `click` event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="2243e-188">Y como ese CSP no especifica , se bloquea el controlador de `unsafe-inline` eventos en línea.</span><span class="sxs-lookup"><span data-stu-id="2243e-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="2243e-189">La forma correcta de implementar el comportamiento deseado en este caso puede ser agregar el controlador como una función del script de contenido de la `onclick` siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2243e-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="2243e-190">Se produce otro problema similar si el script de contenido ejecuta lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2243e-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="2243e-191">En este caso, se ejecuta el script y se muestra la alerta.</span><span class="sxs-lookup"><span data-stu-id="2243e-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="2243e-192">Sin embargo, tome este caso:</span><span class="sxs-lookup"><span data-stu-id="2243e-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="2243e-193">Mientras se ejecuta el script inicial, se bloquea `eval` la llamada a.</span><span class="sxs-lookup"><span data-stu-id="2243e-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="2243e-194">Es decir, mientras se permite el tiempo de ejecución del script inicial, el comportamiento dentro del script está regulado por el CSP de la página.</span><span class="sxs-lookup"><span data-stu-id="2243e-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="2243e-195">Por lo tanto, en función de cómo escriba los scripts inyectados de DOM en la extensión, los cambios en el CSP de la página pueden afectar al comportamiento de la extensión.</span><span class="sxs-lookup"><span data-stu-id="2243e-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="2243e-196">Dado que los scripts de contenido no se ven afectados por el CSP de la página, este es un gran motivo para colocar el mayor comportamiento posible de la extensión en el script de contenido en lugar de scripts inyectados por DOM.</span><span class="sxs-lookup"><span data-stu-id="2243e-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Una introducción a la directiva de seguridad de contenido | Rocas de HTML5"  
[PublicSuffixList]: https://publicsuffix.org/list "VER LA LISTA DE SUFIJOS PÚBLICOS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Uso de hash para elementos \<script\>: nivel 2 de directiva de seguridad de contenido | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Directiva de seguridad de contenido nivel 3 | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Ataque man-in-the-middle | Wikipedia"  

> [!NOTE]
> <span data-ttu-id="2243e-202">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2243e-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2243e-203">La página original se encuentra [aquí.](https://developer.chrome.com/extensions/contentSecurityPolicy)</span><span class="sxs-lookup"><span data-stu-id="2243e-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2243e-205">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2243e-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
