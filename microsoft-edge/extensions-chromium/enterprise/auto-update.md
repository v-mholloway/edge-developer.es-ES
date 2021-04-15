---
description: Obtenga información sobre las actualizaciones automáticas de extensiones en Microsoft Edge
title: Actualizar extensiones automáticamente en Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 74d7b61c8eca1155b545b7e81627a652bf336e66
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483075"
---
<!-- Copyright A. W. Fuchs

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="automatically-update-extensions-in-microsoft-edge"></a><span data-ttu-id="97577-104">Actualizar extensiones automáticamente en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="97577-104">Automatically update extensions in Microsoft Edge</span></span>  

<span data-ttu-id="97577-105">Al establecer la extensión para que se actualice automáticamente, la extensión comparte las siguientes ventajas con Microsoft Edge cuando se establece en actualización automática.</span><span class="sxs-lookup"><span data-stu-id="97577-105">When you set your extension to automatically update, your extension shares the following benefits with Microsoft Edge when set to automatically update.</span></span>  

*   <span data-ttu-id="97577-106">Incorporar correcciones de errores y seguridad.</span><span class="sxs-lookup"><span data-stu-id="97577-106">Incorporate bug and security fixes.</span></span>  
*   <span data-ttu-id="97577-107">Agregue nuevas características o mejoras de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="97577-107">Add new features or performance enhancements.</span></span>  
*   <span data-ttu-id="97577-108">Mejorar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="97577-108">Improve the user interface.</span></span>  

<span data-ttu-id="97577-109">Anteriormente, se admiten extensiones no basadas en almacén.</span><span class="sxs-lookup"><span data-stu-id="97577-109">Previously, non-store based extensions were supported.</span></span>  <span data-ttu-id="97577-110">Además, actualizó los archivos binarios nativos y la extensión al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="97577-110">Also, you updated the native binaries and the extension at the same time.</span></span>  

<span data-ttu-id="97577-111">Ahora, el almacén de complementos de Microsoft Edge hospeda las extensiones y actualiza la extensión con el mismo mecanismo que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="97577-111">Now, the Microsoft Edge Add-ons store hosts your extensions and you update your extension using the same mechanism as Microsoft Edge.</span></span>  <span data-ttu-id="97577-112">No controla el mecanismo de actualización.</span><span class="sxs-lookup"><span data-stu-id="97577-112">You don't control the update mechanism.</span></span>  <span data-ttu-id="97577-113">Tenga cuidado al actualizar las extensiones que tienen una dependencia de los archivos binarios nativos.</span><span class="sxs-lookup"><span data-stu-id="97577-113">Be careful when you update extensions that have a dependency on native binaries.</span></span>  

> [!NOTE]
> <span data-ttu-id="97577-114">Este artículo no se aplica a las extensiones que publique con el panel [del Centro de][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] partners.</span><span class="sxs-lookup"><span data-stu-id="97577-114">This article does not apply to extensions that you publish using the [Partner Center][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] dashboard.</span></span>  <span data-ttu-id="97577-115">Puede usar el panel para publicar versiones actualizadas para los usuarios y para el almacén de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="97577-115">You may use the dashboard to release updated versions to your users and to the Microsoft Edge Add-ons store.</span></span>  <span data-ttu-id="97577-116">Para obtener más información, vaya [a Actualizar o quitar la extensión][ExtensionsPublishUpdateExtension].</span><span class="sxs-lookup"><span data-stu-id="97577-116">For more information, navigate to [Update or remove your extension][ExtensionsPublishUpdateExtension].</span></span>  

## <a name="overview"></a><span data-ttu-id="97577-117">Información general</span><span class="sxs-lookup"><span data-stu-id="97577-117">Overview</span></span>  

<span data-ttu-id="97577-118">Cada pocas horas, Microsoft Edge comprueba si cada extensión o aplicación instalada tiene una dirección URL de actualización.</span><span class="sxs-lookup"><span data-stu-id="97577-118">Every few hours, Microsoft Edge checks whether each installed extension or app has an update URL.</span></span>  <span data-ttu-id="97577-119">Para especificar una dirección URL de actualización para la extensión, use el `update_url` campo del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="97577-119">To specify an update URL for your extension, use the `update_url` field in the manifest.</span></span>  <span data-ttu-id="97577-120">El `update_url` campo del manifiesto apunta a una ubicación para completar una comprobación de actualización.</span><span class="sxs-lookup"><span data-stu-id="97577-120">The `update_url` field in the manifest points to a location to complete an update check.</span></span>  <span data-ttu-id="97577-121">Para cada `update_url` uno, envía solicitudes de archivos XML de manifiesto actualizados.</span><span class="sxs-lookup"><span data-stu-id="97577-121">For each `update_url`, it sends requests for updated manifest XML files.</span></span>  <span data-ttu-id="97577-122">Si el archivo XML del manifiesto de actualización muestra una versión más reciente que la instalada, Microsoft Edge descarga e instala la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="97577-122">If the update manifest XML file lists a newer version than that installed, Microsoft Edge downloads and installs the newer version.</span></span>  <span data-ttu-id="97577-123">El mismo proceso funciona para las actualizaciones manuales, donde el nuevo archivo debe firmarse con la misma `.crx` clave privada que la versión instalada actualmente.</span><span class="sxs-lookup"><span data-stu-id="97577-123">The same process works for manual updates, where the new `.crx` file must be signed with the same private key as the currently installed version.</span></span>  

> [!NOTE]
> <span data-ttu-id="97577-124">Para mantener la privacidad del usuario, Microsoft Edge no envía ningún encabezado con solicitudes de manifiesto de actualización automática e omite los encabezados de las respuestas a `Cookie` `Set-Cookie` dichas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="97577-124">In order to maintain user privacy, Microsoft Edge does not send any `Cookie` headers with auto-update manifest requests, and ignores any `Set-Cookie` headers in the responses to those requests.</span></span>  

## <a name="update-url"></a><span data-ttu-id="97577-125">Dirección URL de actualización</span><span class="sxs-lookup"><span data-stu-id="97577-125">Update URL</span></span>  

<span data-ttu-id="97577-126">Si hospedas tu propia extensión o aplicación, debes agregar el `update_url` campo al `manifest.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="97577-126">If you host your own extension or app, you must add the `update_url` field to your `manifest.json` file.</span></span>  <span data-ttu-id="97577-127">Revise el siguiente fragmento de código para ver un ejemplo de `update_url` .</span><span class="sxs-lookup"><span data-stu-id="97577-127">Review the following code snippet for an example of the `update_url`.</span></span>  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a><span data-ttu-id="97577-128">Manifiesto actualizado</span><span class="sxs-lookup"><span data-stu-id="97577-128">Updated manifest</span></span>  

<span data-ttu-id="97577-129">El manifiesto actualizado devuelto por el servidor debe ser un documento XML.</span><span class="sxs-lookup"><span data-stu-id="97577-129">The updated manifest returned by the server should be an XML document.</span></span>  <span data-ttu-id="97577-130">Revise el siguiente fragmento de código para ver un ejemplo del archivo XML de manifiesto actualizado.</span><span class="sxs-lookup"><span data-stu-id="97577-130">Review the following code snippet for an example of the updated manifest XML file.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

<span data-ttu-id="97577-131">En la tabla siguiente se describen los atributos del archivo XML de manifiesto actualizado.</span><span class="sxs-lookup"><span data-stu-id="97577-131">The following table describes attributes of the updated manifest XML file.</span></span>  

| <span data-ttu-id="97577-132">Atributo</span><span class="sxs-lookup"><span data-stu-id="97577-132">Attribute</span></span> | <span data-ttu-id="97577-133">Detalles</span><span class="sxs-lookup"><span data-stu-id="97577-133">Details</span></span> | 
|:--- |:--- |  
| `appid` | <span data-ttu-id="97577-134">El identificador de extensión se genera en función de un hash de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="97577-134">The extension ID is generated based on a hash of the public key.</span></span>  <span data-ttu-id="97577-135">Para buscar el identificador de una extensión, abra Microsoft Edge y vaya a `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="97577-135">To find the ID of an extension, open Microsoft Edge and navigate to `edge://extensions`.</span></span> |  
| `codebase` | <span data-ttu-id="97577-136">Dirección URL del `.crx` archivo.</span><span class="sxs-lookup"><span data-stu-id="97577-136">A URL to the `.crx` file.</span></span> |  
| `version` | <span data-ttu-id="97577-137">Microsoft Edge usa este valor de atributo para determinar si debe descargar el `.crx` archivo especificado por `codebase` .</span><span class="sxs-lookup"><span data-stu-id="97577-137">This attribute value is used by Microsoft Edge to determine whether it should download the `.crx` file specified by `codebase`.</span></span>  <span data-ttu-id="97577-138">Debe coincidir con el valor del `version` archivo `manifest.json` del `.crx` archivo.</span><span class="sxs-lookup"><span data-stu-id="97577-138">It should match the value of `version` in the `manifest.json` file of the `.crx` file.</span></span> |  

<span data-ttu-id="97577-139">El archivo XML del manifiesto de actualización puede contener información sobre varias extensiones al incluir varios elementos.</span><span class="sxs-lookup"><span data-stu-id="97577-139">The update manifest XML file may contain information about multiple extensions by including multiple elements.</span></span>  

## <a name="testing"></a><span data-ttu-id="97577-140">Pruebas</span><span class="sxs-lookup"><span data-stu-id="97577-140">Testing</span></span>  

<span data-ttu-id="97577-141">La frecuencia de comprobación de actualización predeterminada es de varias horas.</span><span class="sxs-lookup"><span data-stu-id="97577-141">The default update check frequency is several hours.</span></span>  <span data-ttu-id="97577-142">Para forzar una actualización, vaya a `edge://extensions` y elija el botón Actualizar extensiones **ahora.**</span><span class="sxs-lookup"><span data-stu-id="97577-142">To force an update, navigate to `edge://extensions` and choose the **Update extensions now** button.</span></span>  

## <a name="advanced-usage-request-parameters"></a><span data-ttu-id="97577-143">Uso avanzado: parámetros de solicitud</span><span class="sxs-lookup"><span data-stu-id="97577-143">Advanced usage: request parameters</span></span>  

<span data-ttu-id="97577-144">El mecanismo básico es simple.</span><span class="sxs-lookup"><span data-stu-id="97577-144">The basic mechanism is simple.</span></span>  <span data-ttu-id="97577-145">Para actualizar automáticamente la extensión, realice las siguientes acciones.</span><span class="sxs-lookup"><span data-stu-id="97577-145">To automatically update your extension, complete the following actions.</span></span>  

1.  <span data-ttu-id="97577-146">Cargue el archivo XML estático en el servidor web, como Apache.</span><span class="sxs-lookup"><span data-stu-id="97577-146">Upload your static XML file on your web server, such as Apache.</span></span>  
1.  <span data-ttu-id="97577-147">Actualice el archivo XML a medida que libere nuevas versiones de las extensiones.</span><span class="sxs-lookup"><span data-stu-id="97577-147">Update the XML file as you release new versions of your extensions.</span></span>  
    
<span data-ttu-id="97577-148">Aproveche el hecho de que algunos parámetros agregados a la solicitud de manifiesto de actualización indican la extensión `ID` y `version` .</span><span class="sxs-lookup"><span data-stu-id="97577-148">Take advantage of the fact that some parameters added to the update manifest request indicate the extension `ID` and `version`.</span></span>  <span data-ttu-id="97577-149">Puede usar lo mismo `update URL` para todas las extensiones en lugar de un archivo XML estático.</span><span class="sxs-lookup"><span data-stu-id="97577-149">You may use the same `update URL` for all your extensions instead of a static XML file.</span></span>  <span data-ttu-id="97577-150">Para usar lo mismo para todas las extensiones, señale a una dirección URL que ejecute código dinámico del lado servidor `update URL` para probar los parámetros.</span><span class="sxs-lookup"><span data-stu-id="97577-150">To use the same `update URL` for all your extensions, point to a URL that runs dynamic server-side code to test the parameters.</span></span>  

<span data-ttu-id="97577-151">En el ejemplo siguiente se muestra el formato de los parámetros de solicitud de la dirección URL de actualización.</span><span class="sxs-lookup"><span data-stu-id="97577-151">The following example demonstrates the format of the request parameters of update URL.</span></span>  

```url
?x={extension_data}
```  

<span data-ttu-id="97577-152">En este ejemplo, `{extension_data}` es una cadena codificada en dirección URL que usa el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="97577-152">In this example, `{extension_data}` is a URL-encoded string that uses the following format.</span></span>  

```url
id={id}&v={version}
```  

<span data-ttu-id="97577-153">Por ejemplo, las dos extensiones siguientes apuntan a la misma dirección URL de `http://contoso.com/extension_updates.php` actualización.</span><span class="sxs-lookup"><span data-stu-id="97577-153">For example, the following two extensions both point to the same update URL `http://contoso.com/extension_updates.php`.</span></span>  

*   <span data-ttu-id="97577-154">Extensión 1</span><span class="sxs-lookup"><span data-stu-id="97577-154">Extension 1</span></span>  
    *   <span data-ttu-id="97577-155">Identificador:</span><span class="sxs-lookup"><span data-stu-id="97577-155">ID:</span></span> `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`  
    *   <span data-ttu-id="97577-156">dirección URL de actualización:</span><span class="sxs-lookup"><span data-stu-id="97577-156">update URL:</span></span> `http://contoso.com/extension_updates.php`
    *   <span data-ttu-id="97577-157">Versión:</span><span class="sxs-lookup"><span data-stu-id="97577-157">Version:</span></span> `1.1`  
*   <span data-ttu-id="97577-158">Extensión 2</span><span class="sxs-lookup"><span data-stu-id="97577-158">Extension 2</span></span>  
    *   <span data-ttu-id="97577-159">Identificador:</span><span class="sxs-lookup"><span data-stu-id="97577-159">ID:</span></span> `bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb`  
    *   <span data-ttu-id="97577-160">dirección URL de actualización:</span><span class="sxs-lookup"><span data-stu-id="97577-160">update URL:</span></span> `http://contoso.com/extension_updates.php`
    *   <span data-ttu-id="97577-161">Versión:</span><span class="sxs-lookup"><span data-stu-id="97577-161">Version:</span></span> `0.4`  


<span data-ttu-id="97577-162">Las siguientes son las solicitudes para actualizar cada extensión.</span><span class="sxs-lookup"><span data-stu-id="97577-162">The following are the requests to update each extension.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="97577-163">También puede enumerar varias extensiones en una sola solicitud para cada dirección URL de actualización única.</span><span class="sxs-lookup"><span data-stu-id="97577-163">You may also list multiple extensions in a single request for each unique update URL.</span></span>  <span data-ttu-id="97577-164">En el ejemplo siguiente se combinan las solicitudes anteriores en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="97577-164">The following example merges the previous requests into a single request.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="97577-165">Si envía una sola solicitud y el número de extensiones instaladas que usan la misma dirección URL de actualización es demasiado largo, la comprobación de actualización emite más `GET` solicitudes.</span><span class="sxs-lookup"><span data-stu-id="97577-165">If you send a single request and the number of installed extensions that use the same update URL is too long, the update check issues more `GET` requests.</span></span>  <span data-ttu-id="97577-166">Una `GET` dirección URL de solicitud es demasiado larga si tiene aproximadamente 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="97577-166">A `GET` request URL is too long if it's approximately 2000 characters.</span></span>  

> [!NOTE]
> <span data-ttu-id="97577-167">En el futuro, una sola `POST` solicitud puede reemplazar varias `GET` solicitudes.</span><span class="sxs-lookup"><span data-stu-id="97577-167">In the future, a single `POST` request may replace multiple `GET` requests.</span></span>  <span data-ttu-id="97577-168">La `POST` solicitud puede contener los parámetros de solicitud en el `POST` cuerpo.</span><span class="sxs-lookup"><span data-stu-id="97577-168">The `POST` request may contain the request parameters in the `POST` body.</span></span>  

## <a name="advanced-usage-minimum-browser-version"></a><span data-ttu-id="97577-169">Uso avanzado: versión mínima del explorador</span><span class="sxs-lookup"><span data-stu-id="97577-169">Advanced usage: minimum browser version</span></span>  

<span data-ttu-id="97577-170">Como nueva versión de las API para el sistema de extensiones de Microsoft Edge, puedes publicar una versión actualizada de la extensión o aplicación que solo funciona con versiones más recientes de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="97577-170">As new APIs release for the Microsoft Edge extensions system, you may release an updated version of your extension or app that only works with newer Microsoft Edge versions.</span></span>  <span data-ttu-id="97577-171">Cuando Microsoft Edge se actualiza automáticamente, puede tardar unos días antes de que la mayoría de los usuarios se actualicen a esa nueva versión.</span><span class="sxs-lookup"><span data-stu-id="97577-171">When Microsoft Edge is automatically updated, it may take a few days before most of your users update to that new release.</span></span>  <span data-ttu-id="97577-172">Para asegurarse de que una actualización específica solo se aplica a las versiones de Microsoft Edge actuales o más recientes que una versión específica, agregue el `prodversionmin` atributo en el manifiesto de actualización.</span><span class="sxs-lookup"><span data-stu-id="97577-172">To ensure that a specific update applies only to Microsoft Edge versions that are current or newer than a specific version, add the `prodversionmin` attribute in your update manifest.</span></span>  <span data-ttu-id="97577-173">En el siguiente fragmento de código, el valor de atributo de especifica que la aplicación se actualizó automáticamente a la versión solo cuando el usuario ejecuta Microsoft Edge o una versión `prodversionmin` `3.0.193.0` más `2.0` `3.0.193.0` reciente.</span><span class="sxs-lookup"><span data-stu-id="97577-173">In the following code snippet, the `prodversionmin` attribute value of `3.0.193.0` specifies that your app automatically updated to version `2.0` only when the user is running Microsoft Edge `3.0.193.0` or newer.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[ExtensionsPublishUpdateExtension]: ../publish/update-extension.md "Actualizar o quitar la extensión | Microsoft Docs"  

[MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  

> [!NOTE]
> <span data-ttu-id="97577-176">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="97577-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="97577-177">La página original se encuentra [aquí.](https://developer.chrome.com/docs/apps/autoupdate)</span><span class="sxs-lookup"><span data-stu-id="97577-177">The original page is found [here](https://developer.chrome.com/docs/apps/autoupdate).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="97577-179">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="97577-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
