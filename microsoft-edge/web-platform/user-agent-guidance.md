---
description: En este artículo se proporciona documentación sobre las sugerencias Microsoft Edge cliente del agente de usuario y la cadena de agente de usuario
title: Cómo detectar Microsoft Edge en el sitio web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, user agent string, ua string, ua overrides, user-agent client hints, user agent client hints, ua client hints, ua ch
ms.openlocfilehash: 1957bb5bd33d9d921d8a12e16a4a52a23836027b
ms.sourcegitcommit: e90bbc210b5d510004bbc2145d49e14fe72ed54b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/20/2021
ms.locfileid: "11578785"
---
# <a name="how-to-detect-microsoft-edge-in-your-website"></a><span data-ttu-id="51ccd-104">Cómo detectar Microsoft Edge en el sitio web</span><span class="sxs-lookup"><span data-stu-id="51ccd-104">How to detect Microsoft Edge in your website</span></span>  

<span data-ttu-id="51ccd-105">Los exploradores proporcionan mecanismos para que los sitios web detecten información del explorador, como la marca y el número de versión.</span><span class="sxs-lookup"><span data-stu-id="51ccd-105">Browsers provide mechanisms for websites to detect browser information such as brand and version number.</span></span>  <span data-ttu-id="51ccd-106">Los mecanismos también detectan otras características del dispositivo, como el sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="51ccd-106">The mechanisms also detect other device characteristics like the host operating system.</span></span>  <span data-ttu-id="51ccd-107">Dos de estos mecanismos admitidos en Microsoft Edge [son sugerencias](#user-agent-client-hints) de cliente de agente de usuario y [cadenas de agente de usuario.](#user-agent-string)</span><span class="sxs-lookup"><span data-stu-id="51ccd-107">Two such mechanisms supported on Microsoft Edge are [User-Agent Client Hints](#user-agent-client-hints) and [User-Agent strings](#user-agent-string).</span></span>  <span data-ttu-id="51ccd-108">Después de décadas de uso, User-Agent cadenas de caracteres están obsoletas y tienen un largo historial como causa de problemas de compatibilidad de sitios web.</span><span class="sxs-lookup"><span data-stu-id="51ccd-108">After decades of use, User-Agent strings are outdated and have a long history as the cause of website compatibility issues.</span></span>  <span data-ttu-id="51ccd-109">En su lugar, el Microsoft Edge recomienda usar un mecanismo mejorado para recuperar información del explorador denominada [Sugerencias](#user-agent-client-hints)de cliente de agente de usuario .</span><span class="sxs-lookup"><span data-stu-id="51ccd-109">Instead, the Microsoft Edge team recommends you use an improved mechanism to retrieve browser information named [User-Agent Client Hints](#user-agent-client-hints).</span></span>  <span data-ttu-id="51ccd-110">En este artículo se describen los dos mecanismos Microsoft Edge para recuperar la información del agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="51ccd-110">This article outlines the two mechanisms Microsoft Edge supports for retrieving user agent information.</span></span>  

|  | <span data-ttu-id="51ccd-111">Servidor</span><span class="sxs-lookup"><span data-stu-id="51ccd-111">Server-side</span></span> | <span data-ttu-id="51ccd-112">Lado cliente</span><span class="sxs-lookup"><span data-stu-id="51ccd-112">Client-side</span></span> |  
|:--- |:--- |:--- | 
| <span data-ttu-id="51ccd-113">**Sugerencias de cliente de** agente de usuario \(recommended\)</span><span class="sxs-lookup"><span data-stu-id="51ccd-113">**User-Agent Client Hints** \(recommended\)</span></span> | `Sec-CH-UA` <span data-ttu-id="51ccd-114">Encabezado HTTPS</span><span class="sxs-lookup"><span data-stu-id="51ccd-114">HTTPS header</span></span> | `navigator.userAgentData` <span data-ttu-id="51ccd-115">Método JavaScript</span><span class="sxs-lookup"><span data-stu-id="51ccd-115">JavaScript method</span></span> |  
| <span data-ttu-id="51ccd-116">**Cadena de agente de usuario** \(legacy\)</span><span class="sxs-lookup"><span data-stu-id="51ccd-116">**User-Agent string** \(legacy\)</span></span> | `User-Agent` <span data-ttu-id="51ccd-117">Encabezado HTTPS</span><span class="sxs-lookup"><span data-stu-id="51ccd-117">HTTPS header</span></span> | `navigator.userAgent` <span data-ttu-id="51ccd-118">Método JavaScript</span><span class="sxs-lookup"><span data-stu-id="51ccd-118">JavaScript method</span></span> |  

<span data-ttu-id="51ccd-119">Microsoft recomienda usar la detección [de características][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] siempre que sea posible por los siguientes motivos.</span><span class="sxs-lookup"><span data-stu-id="51ccd-119">Microsoft recommends that you use [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] whenever possible for the following reasons.</span></span>  

*   <span data-ttu-id="51ccd-120">Mejorar la capacidad de mantenimiento del código.</span><span class="sxs-lookup"><span data-stu-id="51ccd-120">Improve code maintainability.</span></span>  
*   <span data-ttu-id="51ccd-121">Reducir la fragilidad del código.</span><span class="sxs-lookup"><span data-stu-id="51ccd-121">Reduce code fragility.</span></span>  
*   <span data-ttu-id="51ccd-122">Reduzca la interrupción del código de los cambios realizados en la User-Agent cadena.</span><span class="sxs-lookup"><span data-stu-id="51ccd-122">Reduce code breakage from changes to the User-Agent string.</span></span>  
    
<span data-ttu-id="51ccd-123">Cuando [la detección][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] de características no es aplicable y debe usar la detección de agentes de usuario, use el siguiente formato para detectar Microsoft Edge de usuario en Windows y Android.</span><span class="sxs-lookup"><span data-stu-id="51ccd-123">When [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] isn't applicable and you must use user agent detection, use the following format to detect Microsoft Edge user agent on Windows and Android.</span></span>  

## <a name="user-agent-client-hints"></a><span data-ttu-id="51ccd-124">User-Agent sugerencias de cliente</span><span class="sxs-lookup"><span data-stu-id="51ccd-124">User-Agent Client Hints</span></span>  

<span data-ttu-id="51ccd-125">A partir Microsoft Edge versión 90, accede a la información del explorador de una forma más limpia y que preserve la privacidad.</span><span class="sxs-lookup"><span data-stu-id="51ccd-125">Starting in Microsoft Edge version 90, access browser information in a cleaner, more privacy-preserving way.</span></span>  

### <a name="user-agent-client-hints-https-header"></a><span data-ttu-id="51ccd-126">User-Agent encabezado HTTPS sugerencias de cliente</span><span class="sxs-lookup"><span data-stu-id="51ccd-126">User-Agent Client Hints HTTPS Header</span></span>  

<span data-ttu-id="51ccd-127">De forma predeterminada, Chromium exploradores incluidos Microsoft Edge el encabezado `Accept-CH-UA` de respuesta en el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="51ccd-127">By default, Chromium browsers including Microsoft Edge send the `Accept-CH-UA` response header in the following format.</span></span>  

```https
Sec-CH-UA: "Chromium";v="91", "Microsoft Edge";v="91","Dummy;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
```  

> [!NOTE]
> <span data-ttu-id="51ccd-128">Las sugerencias de cliente solo se envían a través de conexiones seguras mediante `HTTPS` .</span><span class="sxs-lookup"><span data-stu-id="51ccd-128">Client Hints are only sent over secure connections using `HTTPS`.</span></span>  

<span data-ttu-id="51ccd-129">Las siguientes sugerencias de entropía baja se envían de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="51ccd-129">The following low entropy hints are sent by default.</span></span>  <span data-ttu-id="51ccd-130">Si necesita obtener más información, envíe uno de los siguientes encabezados de solicitud.</span><span class="sxs-lookup"><span data-stu-id="51ccd-130">If you need to access more information, send one of the following request headers.</span></span>  

#### <a name="user-agent-request-and-response-headers"></a><span data-ttu-id="51ccd-131">User-Agent de solicitud y respuesta</span><span class="sxs-lookup"><span data-stu-id="51ccd-131">User-Agent request and response headers</span></span>  

| <span data-ttu-id="51ccd-132">Encabezado de la solicitud</span><span class="sxs-lookup"><span data-stu-id="51ccd-132">Request header</span></span> | <span data-ttu-id="51ccd-133">Valor de respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="51ccd-133">Example response value</span></span> |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `false` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` |  
| `Sec-CH-UA-Model` |  |  

### <a name="user-agent-client-hints-javascript-api"></a><span data-ttu-id="51ccd-134">User-Agent API de JavaScript de sugerencias de cliente</span><span class="sxs-lookup"><span data-stu-id="51ccd-134">User-Agent Client Hints JavaScript API</span></span>  

<span data-ttu-id="51ccd-135">El valor de respuesta predeterminado de `navigator.userAgentData` usa el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="51ccd-135">The default response value from `navigator.userAgentData` uses the following format.</span></span>  

```javascript
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

<span data-ttu-id="51ccd-136">Si necesita obtener acceso a información más detallada, use el [método getHighEntropyValues().][GithubWicgUaClientHintsGethighentropyvalues]</span><span class="sxs-lookup"><span data-stu-id="51ccd-136">If you need to access more detailed information, use the [getHighEntropyValues()][GithubWicgUaClientHintsGethighentropyvalues] method.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="51ccd-137">El siguiente fragmento de código envía una solicitud.</span><span class="sxs-lookup"><span data-stu-id="51ccd-137">The following code snippet sends a request.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="51ccd-138">Para recibir la siguiente respuesta.</span><span class="sxs-lookup"><span data-stu-id="51ccd-138">To receive the following response.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```javascript
         navigator.userAgentData.getHighEntropyValues(
             ["architecture", "model", "platform", "platformVersion", "uaFullVersion"])
             .then(ua => { console.log(ua) });
      ```  
   :::column-end:::
   :::column span="":::
      ```javascript
      {architecture: "x86", 
      model: "", 
      platform: "Windows", 
      platformVersion: "10.0", 
      uaFullVersion: "92.0.866.0"}
      ```  
   :::column-end:::
:::row-end:::  

## <a name="recommended-uses-of-user-agent-client-hints"></a><span data-ttu-id="51ccd-139">Usos recomendados de User-Agent sugerencias de cliente</span><span class="sxs-lookup"><span data-stu-id="51ccd-139">Recommended uses of User-Agent Client Hints</span></span>  

<span data-ttu-id="51ccd-140">El conjunto de marcas y el orden de presentación asociado cambian con el tiempo, por lo que nunca debes codificar los índices en la matriz de marcas devueltas.</span><span class="sxs-lookup"><span data-stu-id="51ccd-140">The set of brands and the associated display order change over time, so you should never hard-code indices into the array of returned brands.</span></span>  <span data-ttu-id="51ccd-141">Para garantizar que detecte problemas similares en su sitio web antes de tiempo, el explorador incluye un valor de marca que cambia con el tiempo y tiene formato para interrumpirse debido a problemas comunes de análisis de `GREASE` cadenas.</span><span class="sxs-lookup"><span data-stu-id="51ccd-141">To help ensure you spot similar issues in your website early, the browser includes a `GREASE` brand value that changes over time and is formatted to break because of common string parsing issues.</span></span>  

<span data-ttu-id="51ccd-142">Si no puedes usar la detección de [características,][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]no uses una lista codificada de exploradores Chromium para la comprobación.</span><span class="sxs-lookup"><span data-stu-id="51ccd-142">If you're prevented from using [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection], don't use a hardcoded list of known Chromium-based browsers for verification.</span></span>  <span data-ttu-id="51ccd-143">Algunos ejemplos de nombres de explorador codificados de forma rígida `Microsoft Edge` incluyen y `Google Chrome` .</span><span class="sxs-lookup"><span data-stu-id="51ccd-143">Examples of hardcoded browser names include `Microsoft Edge` and `Google Chrome`.</span></span>  <span data-ttu-id="51ccd-144">Las razones [por las que la][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] detección de características no es aplicable pueden incluir la siguiente situación.</span><span class="sxs-lookup"><span data-stu-id="51ccd-144">Reasons why [feature detection][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] isn't applicable may include the following situation.</span></span>  

*   <span data-ttu-id="51ccd-145">Se debe evitar una corrección de un error Chromium en una versión posterior y los exploradores afectados son difíciles de detectar fuera de una comprobación de la marca y la versión.</span><span class="sxs-lookup"><span data-stu-id="51ccd-145">A fix for a Chromium bug in a later version must be avoided and the affected browsers are difficult to detect outside of a verification of the brand and version.</span></span>  
    
<span data-ttu-id="51ccd-146">En su lugar, debe comprobar la marca, lo que garantiza que la detección se aplique a todos los `Chromium` exploradores Chromium basados en la marca.</span><span class="sxs-lookup"><span data-stu-id="51ccd-146">Instead, you should verify the `Chromium` brand, which ensures your detection applies to all affected Chromium-based browsers.</span></span>  


```javascript
function isChromium() {
    for (brand_version_pair in navigator.userAgentData.brands) {
        if (brand_version_pair.brand == "Chromium") {
            return true;
        }
    }
    return false;
}
```  

## <a name="user-agent-string"></a><span data-ttu-id="51ccd-147">Cadena de agente de usuario</span><span class="sxs-lookup"><span data-stu-id="51ccd-147">User agent string</span></span>  

<span data-ttu-id="51ccd-148">Siempre que sea posible, Microsoft recomienda minimizar el uso de Microsoft Edge lógica de detección de explorador basada en la cadena de agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="51ccd-148">Wherever possible, Microsoft recommends you minimize your use of Microsoft Edge browser detection logic based on the user agent string.</span></span>  <span data-ttu-id="51ccd-149">Si tiene una buena razón para detectar el agente de usuario, el equipo de Microsoft Edge recomienda usar [sugerencias](#user-agent-client-hints) de cliente de agente de usuario como lógica de detección principal.</span><span class="sxs-lookup"><span data-stu-id="51ccd-149">If you have a good reason to detect the user agent, the Microsoft Edge team recommends you use [User-Agent Client Hints](#user-agent-client-hints) as the primary detection logic.</span></span>  <span data-ttu-id="51ccd-150">[Las sugerencias de cliente de](#user-agent-client-hints) agente de usuario también reducen el número necesario de cadenas analizadas.</span><span class="sxs-lookup"><span data-stu-id="51ccd-150">[User-Agent Client Hints](#user-agent-client-hints) also reduces the required number of parsed strings.</span></span>  <span data-ttu-id="51ccd-151">Sin embargo, para la referencia heredada, se usa el siguiente formato para la cadena User-Agent.</span><span class="sxs-lookup"><span data-stu-id="51ccd-151">However, for legacy reference, the following format is used for the User-Agent string.</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="51ccd-152">En Windows, el `User-Agent` encabezado de solicitud HTTP usa el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="51ccd-152">On Windows, the `User-Agent` HTTP request header uses the following format.</span></span>  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="51ccd-153">En Android, el `User-Agent` encabezado de solicitud HTTP usa el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="51ccd-153">On Android, the `User-Agent` HTTP request header uses the following format.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
   :::column span="":::
      ```https
      User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Mobile Safari/537.36 Edg/90.0.818.46
      ```  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="51ccd-154">El valor de respuesta del `navigator.userAgent` método usa el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="51ccd-154">The response value from `navigator.userAgent` method uses the following format.</span></span>  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

<span data-ttu-id="51ccd-155">Los identificadores de plataforma cambian en función del sistema operativo usado y los números de versión también aumentan a medida que pasa el tiempo.</span><span class="sxs-lookup"><span data-stu-id="51ccd-155">Platform identifiers change based on the operating system used, and the version numbers also increment as time passes.</span></span>  <span data-ttu-id="51ccd-156">El formato es el mismo que el Chromium usuario con la adición de un `Edg` nuevo token al final.</span><span class="sxs-lookup"><span data-stu-id="51ccd-156">The format is the same as the Chromium user agent with the addition of a new `Edg` token at the end.</span></span>  <span data-ttu-id="51ccd-157">Microsoft eligió el token para evitar problemas de compatibilidad causados por la cadena, que se usó Microsoft Edge explorador basado `Edg` `Edge` en EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="51ccd-157">Microsoft chose the `Edg` token to avoid compatibility issues caused by `Edge` string, which was used legacy Microsoft Edge browser based on EdgeHTML.</span></span>  <span data-ttu-id="51ccd-158">El `Edg` token también es coherente con los tokens [existentes][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] usados en iOS y Android.</span><span class="sxs-lookup"><span data-stu-id="51ccd-158">The `Edg` token is also consistent with [existing tokens][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] used on iOS and Android.</span></span>

## <a name="map-the-user-agent-string-to-browser-name"></a><span data-ttu-id="51ccd-159">Asignar la cadena de agente de usuario al nombre del explorador</span><span class="sxs-lookup"><span data-stu-id="51ccd-159">Map the user agent string to browser name</span></span>  

<span data-ttu-id="51ccd-160">Asigne los tokens de cadena de agente de usuario a un nombre de explorador más legible para usar en el código.</span><span class="sxs-lookup"><span data-stu-id="51ccd-160">Map the user agent string tokens to a more human-readable browser name to use in code.</span></span>  <span data-ttu-id="51ccd-161">Es un patrón común en la web hoy en día.</span><span class="sxs-lookup"><span data-stu-id="51ccd-161">It's a common pattern on the web today.</span></span>  <span data-ttu-id="51ccd-162">Al asignar el nuevo token a un nombre de explorador, Microsoft recomienda usar un nombre diferente al que se usa para el explorador de Microsoft Edge heredado para evitar aplicar accidentalmente cualquier solución alternativa heredada que no sea aplicable a los exploradores basados en `Edg` Chromium.</span><span class="sxs-lookup"><span data-stu-id="51ccd-162">When you map the new `Edg` token to a browser name, Microsoft recommends that you use a different name than the one used for the legacy Microsoft Edge browser to avoid accidentally applying any legacy workarounds that aren't applicable to Chromium-based browsers.</span></span>

## <a name="user-agent-overrides"></a><span data-ttu-id="51ccd-163">Invalidaciones del agente de usuario</span><span class="sxs-lookup"><span data-stu-id="51ccd-163">User Agent overrides</span></span>  

<span data-ttu-id="51ccd-164">A veces, un sitio web no reconoce el nuevo Microsoft Edge de usuario.</span><span class="sxs-lookup"><span data-stu-id="51ccd-164">Sometimes, a website doesn't recognize the new Microsoft Edge user agent.</span></span>  <span data-ttu-id="51ccd-165">Como resultado, es posible que un conjunto de características del sitio web no funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="51ccd-165">As a result, a set of the features of the website may not work correctly.</span></span>  <span data-ttu-id="51ccd-166">Cuando se notifica a Microsoft sobre los tipos de problemas, Microsoft se pone en contacto con usted \(propietario de un sitio web\) e informa sobre el agente de usuario actualizado.</span><span class="sxs-lookup"><span data-stu-id="51ccd-166">When Microsoft is notified about the types of issues, Microsoft contacts you \(a website owner\) and informs you about the updated user agent.</span></span>  

<span data-ttu-id="51ccd-167">Es posible que necesite más tiempo para actualizar y probar la lógica de detección de agentes de usuario de su sitio web para solucionar los problemas notificados por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="51ccd-167">You may need more time to update and test the user agent detection logic for your website to address the issues reported by Microsoft.</span></span>  <span data-ttu-id="51ccd-168">Para maximizar la compatibilidad de los usuarios, los canales Microsoft Edge Beta y Estable usan una lista de invalidaciones de agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="51ccd-168">To maximize compatibility for your users, the Microsoft Edge Beta and Stable channels use a list of user agent overrides.</span></span>  <span data-ttu-id="51ccd-169">Use las invalidaciones del agente de usuario mientras actualiza su sitio web.</span><span class="sxs-lookup"><span data-stu-id="51ccd-169">Use the user agent overrides while you update your website.</span></span>  <span data-ttu-id="51ccd-170">La lista de invalidaciones de agente de usuario proporcionada por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="51ccd-170">The list of user agent overrides provided by Microsoft.</span></span>  

<span data-ttu-id="51ccd-171">Las invalidaciones especifican nuevos valores de agente de usuario que Microsoft Edge en lugar del agente de usuario predeterminado para sitios web específicos.</span><span class="sxs-lookup"><span data-stu-id="51ccd-171">The overrides specify new user agent values that Microsoft Edge sends instead of the default user agent for specific websites.</span></span>  <span data-ttu-id="51ccd-172">Para mostrar la lista de invalidaciones de agente de usuario que se aplican actualmente, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="51ccd-172">To display the list of user agent overrides that are currently applied, complete the following actions.</span></span>  

1.  <span data-ttu-id="51ccd-173">Abra el Microsoft Edge Beta o el canal estable.</span><span class="sxs-lookup"><span data-stu-id="51ccd-173">Open the Microsoft Edge Beta or Stable channel.</span></span>  
1.  <span data-ttu-id="51ccd-174">Vaya a `edge://compat/useragent`.</span><span class="sxs-lookup"><span data-stu-id="51ccd-174">Navigate to `edge://compat/useragent`.</span></span>  
    
<span data-ttu-id="51ccd-175">Los Microsoft Edge canary y dev no reciben actualmente invalidaciones de agente de usuario.</span><span class="sxs-lookup"><span data-stu-id="51ccd-175">The Microsoft Edge Canary and Dev channels don't currently receive user agent overrides.</span></span>  <span data-ttu-id="51ccd-176">Los Microsoft Edge Canary y Dev proporcionan entornos que usan el agente Microsoft Edge usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="51ccd-176">The Microsoft Edge Canary and Dev channels provide environments that use the default Microsoft Edge user agent.</span></span>  <span data-ttu-id="51ccd-177">Use los Microsoft Edge Canary y Dev para reproducir fácilmente problemas en su sitio web causados por el agente Microsoft Edge usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="51ccd-177">Use the Microsoft Edge Canary and Dev channels to easily reproduce issues on your website caused by the default Microsoft Edge user agent.</span></span>  <span data-ttu-id="51ccd-178">Para desactivar las invalidaciones de agente de usuario en los canales Microsoft Edge Beta o Estable, complete las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="51ccd-178">To turn off user agent overrides in the Microsoft Edge Beta or Stable channels, complete the following actions.</span></span>  

1.  <span data-ttu-id="51ccd-179">Abre la aplicación de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="51ccd-179">Open your command-line app.</span></span>  
1.  <span data-ttu-id="51ccd-180">Copie y pegue el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="51ccd-180">Copy and paste the following code snippet.</span></span>  
    
    ```shell
    --disable-domain-action-user-agent-override
    ```  
    
1.  <span data-ttu-id="51ccd-181">Ejecute la Microsoft Edge con el fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="51ccd-181">Run the Microsoft Edge app using the code snippet.</span></span>  
    
    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  
    
<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge para iOS y Android: lo que los desarrolladores necesitan saber | Blogs Windows Microsoft"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. método getHighEntropyValues: User-Agent sugerencias de cliente | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Implementación de la detección de características | MDN"  
