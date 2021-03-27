---
description: Obtenga información sobre las actualizaciones automáticas de extensiones en Microsoft Edge
title: Extensiones de actualización automática en Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 0f3f140cd3a2a079cd09f4d61e46a420342e15e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461573"
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
# <a name="auto-update-extensions-in-microsoft-edge"></a><span data-ttu-id="32b65-104">Extensiones de actualización automática en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="32b65-104">Auto-update extensions in Microsoft Edge</span></span>  

<span data-ttu-id="32b65-105">La actualización automática de extensiones comparte algunas de las mismas ventajas que la actualización automática de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="32b65-105">Automatically updating extensions share some of the same benefits as automatically updating Microsoft Edge:</span></span>   

*   <span data-ttu-id="32b65-106">Incorporar correcciones de errores y seguridad.</span><span class="sxs-lookup"><span data-stu-id="32b65-106">Incorporate bug and security fixes.</span></span>  
*   <span data-ttu-id="32b65-107">Agregue nuevas características o mejoras de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="32b65-107">Add new features or performance enhancements.</span></span>  
*   <span data-ttu-id="32b65-108">Mejorar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="32b65-108">Improve the user interface.</span></span>  

<span data-ttu-id="32b65-109">Anteriormente, cuando se admiten extensiones no basadas en almacén, era posible actualizar los archivos binarios nativos y la extensión al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="32b65-109">Previously when non-store based extensions were supported, it was possible to update the native binaries and the extension at the same time.</span></span>  <span data-ttu-id="32b65-110">Ahora, esas extensiones se hospedan en el almacén de complementos de Microsoft Edge y las actualizaciones se realizan con el mismo mecanismo que Usa Microsoft Edge, que no se puede controlar.</span><span class="sxs-lookup"><span data-stu-id="32b65-110">Now, those extensions are hosted in the Microsoft Edge Add-ons store and updates are made using the same mechanism that Microsoft Edge uses, which you can't control.</span></span>  <span data-ttu-id="32b65-111">Debe tener cuidado al actualizar las extensiones que tienen una dependencia de los archivos binarios nativos.</span><span class="sxs-lookup"><span data-stu-id="32b65-111">You should be careful when updating extensions that have a dependency on native binaries.</span></span>  

> [!NOTE]
> <span data-ttu-id="32b65-112">Este tema no se aplica a las extensiones publicadas mediante el panel [del Centro de][MicrosoftPartnerCenter] partners.</span><span class="sxs-lookup"><span data-stu-id="32b65-112">This topic does not apply to extensions published using the [Partner Center][MicrosoftPartnerCenter] dashboard.</span></span>  <span data-ttu-id="32b65-113">Puede usar el panel para publicar versiones actualizadas para los usuarios y para el almacén de complementos de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="32b65-113">You may use the dashboard to release updated versions to your users and to the Microsoft Edge Add-ons store.</span></span>

## <a name="overview"></a><span data-ttu-id="32b65-114">Información general</span><span class="sxs-lookup"><span data-stu-id="32b65-114">Overview</span></span>  

<span data-ttu-id="32b65-115">Cada pocas horas, Microsoft Edge comprueba si cada extensión o aplicación instalada tiene una dirección URL de actualización.</span><span class="sxs-lookup"><span data-stu-id="32b65-115">Every few hours, Microsoft Edge checks whether each installed extension or app has an update URL.</span></span>  <span data-ttu-id="32b65-116">Las extensiones pueden especificar una dirección URL de actualización mediante el campo del manifiesto, que apunta `update_url` a una ubicación para realizar una comprobación de actualización.</span><span class="sxs-lookup"><span data-stu-id="32b65-116">Extensions can specify an update URL using the `update_url` field in the manifest, which points to a location to perform an update check.</span></span>  <span data-ttu-id="32b65-117">Para cada `update_url` uno, envía solicitudes de archivos XML de manifiesto actualizados.</span><span class="sxs-lookup"><span data-stu-id="32b65-117">For each `update_url`, it sends requests for updated manifest XML files.</span></span>  <span data-ttu-id="32b65-118">Si el archivo XML del manifiesto de actualización muestra una versión más reciente que la instalada, Microsoft Edge descarga e instala la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="32b65-118">If the update manifest XML file lists a newer version than that installed, Microsoft Edge downloads and installs the newer version.</span></span>  <span data-ttu-id="32b65-119">El mismo proceso funciona para las actualizaciones manuales, donde el nuevo archivo debe firmarse con la misma `.crx` clave privada que la versión instalada actualmente.</span><span class="sxs-lookup"><span data-stu-id="32b65-119">The same process works for manual updates, where the new `.crx` file must be signed with the same private key as the currently installed version.</span></span>  

> [!NOTE]
> <span data-ttu-id="32b65-120">Para mantener la privacidad del usuario, Microsoft Edge no envía ningún encabezado con solicitudes de manifiesto de actualización automática e omite los encabezados de las respuestas a `Cookie` `Set-Cookie` dichas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="32b65-120">In order to maintain user privacy, Microsoft Edge does not send any `Cookie` headers with auto-update manifest requests, and ignores any `Set-Cookie` headers in the responses to those requests.</span></span>  

## <a name="update-url"></a><span data-ttu-id="32b65-121">Dirección URL de actualización</span><span class="sxs-lookup"><span data-stu-id="32b65-121">Update URL</span></span>  

<span data-ttu-id="32b65-122">Si hospedas tu propia extensión o aplicación, debes agregar el `update_url` campo al `manifest.json` archivo.</span><span class="sxs-lookup"><span data-stu-id="32b65-122">If you host your own extension or app, you must add the `update_url` field to your `manifest.json` file.</span></span>  <span data-ttu-id="32b65-123">Revise el siguiente fragmento de código para ver un ejemplo de `update_url` .</span><span class="sxs-lookup"><span data-stu-id="32b65-123">Review the following code snippet for an example of the `update_url`.</span></span>  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="updated-manifest"></a><span data-ttu-id="32b65-124">Manifiesto actualizado</span><span class="sxs-lookup"><span data-stu-id="32b65-124">Updated manifest</span></span>  

<span data-ttu-id="32b65-125">El manifiesto actualizado devuelto por el servidor debe ser un documento XML.</span><span class="sxs-lookup"><span data-stu-id="32b65-125">The updated manifest returned by the server should be an XML document.</span></span>  <span data-ttu-id="32b65-126">Revise el siguiente fragmento de código para ver un ejemplo del archivo XML de manifiesto actualizado.</span><span class="sxs-lookup"><span data-stu-id="32b65-126">Review the following code snippet for an example of the updated manifest XML file.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.microsoft.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

<span data-ttu-id="32b65-127">En la tabla siguiente se describen los atributos del archivo XML de manifiesto actualizado.</span><span class="sxs-lookup"><span data-stu-id="32b65-127">The following table describes attributes of the updated manifest XML file.</span></span>  

| <span data-ttu-id="32b65-128">Atributo</span><span class="sxs-lookup"><span data-stu-id="32b65-128">Attribute</span></span> | <span data-ttu-id="32b65-129">Detalles</span><span class="sxs-lookup"><span data-stu-id="32b65-129">Details</span></span> | 
|:--- |:--- |  
| `appid` | <span data-ttu-id="32b65-130">El identificador de extensión se genera en función de un hash de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="32b65-130">The extension ID is generated based on a hash of the public key.</span></span>  <span data-ttu-id="32b65-131">Para buscar el identificador de una extensión, abra Microsoft Edge y vaya a `edge://extensions` .</span><span class="sxs-lookup"><span data-stu-id="32b65-131">To find the ID of an extension, open Microsoft Edge and navigate to `edge://extensions`.</span></span> |  
| `codebase` | <span data-ttu-id="32b65-132">Dirección URL del `.crx` archivo.</span><span class="sxs-lookup"><span data-stu-id="32b65-132">A URL to the `.crx` file.</span></span> |  
| `version` | <span data-ttu-id="32b65-133">Microsoft Edge usa este valor de atributo para determinar si debe descargar el `.crx` archivo especificado por `codebase` .</span><span class="sxs-lookup"><span data-stu-id="32b65-133">This attribute value is used by Microsoft Edge to determine whether it should download the `.crx` file specified by `codebase`.</span></span>  <span data-ttu-id="32b65-134">Debe coincidir con el valor del `version` archivo `manifest.json` del `.crx` archivo.</span><span class="sxs-lookup"><span data-stu-id="32b65-134">It should match the value of `version` in the `manifest.json` file of the `.crx` file.</span></span> |  

<span data-ttu-id="32b65-135">El archivo XML del manifiesto de actualización puede contener información sobre varias extensiones al incluir varios elementos.</span><span class="sxs-lookup"><span data-stu-id="32b65-135">The update manifest XML file may contain information about multiple extensions by including multiple elements.</span></span>  

## <a name="testing"></a><span data-ttu-id="32b65-136">Pruebas</span><span class="sxs-lookup"><span data-stu-id="32b65-136">Testing</span></span>  

<span data-ttu-id="32b65-137">La frecuencia de comprobación de actualización predeterminada es de varias horas.</span><span class="sxs-lookup"><span data-stu-id="32b65-137">The default update check frequency is several hours.</span></span>  <span data-ttu-id="32b65-138">Para forzar una actualización, vaya a `edge://extensions` y elija el botón Actualizar extensiones **ahora.**</span><span class="sxs-lookup"><span data-stu-id="32b65-138">To force an update, navigate to `edge://extensions` and choose the **Update extensions now** button.</span></span>  

## <a name="advanced-usage-request-parameters"></a><span data-ttu-id="32b65-139">Uso avanzado: parámetros de solicitud</span><span class="sxs-lookup"><span data-stu-id="32b65-139">Advanced usage: request parameters</span></span>  

<span data-ttu-id="32b65-140">El mecanismo básico de actualización automática es tan fácil como colocar un archivo XML estático en cualquier servidor web como Apache y actualizar el archivo XML a medida que se lanzan nuevas versiones de las extensiones.</span><span class="sxs-lookup"><span data-stu-id="32b65-140">The basic auto-update mechanism is as easy as dropping a static XML file onto any web server such as Apache, and updating the XML file as you release new versions of your extensions.</span></span>  

<span data-ttu-id="32b65-141">Puede aprovechar el hecho de que los parámetros se agregan a la solicitud de manifiesto de actualización que indican el identificador de extensión y la versión.</span><span class="sxs-lookup"><span data-stu-id="32b65-141">You may take advantage of the fact that parameters are added to the update manifest request that indicate the extension ID and version.</span></span> <span data-ttu-id="32b65-142">Puede usar la misma dirección URL de actualización para todas las extensiones en lugar de un archivo XML estático.</span><span class="sxs-lookup"><span data-stu-id="32b65-142">You can use the same update URL for all your extensions instead of a static XML file.</span></span>  <span data-ttu-id="32b65-143">Para usar la misma dirección URL de actualización para todas las extensiones, señale a una dirección URL que ejecute código dinámico del lado servidor para probar estos parámetros.</span><span class="sxs-lookup"><span data-stu-id="32b65-143">To use the same update URL for all your extensions, point to a URL that runs dynamic server-side code to test these parameters.</span></span>  

<span data-ttu-id="32b65-144">En el siguiente ejemplo se muestra el formato de los parámetros de solicitud de la dirección URL de actualización: `?x={extension_data}` .</span><span class="sxs-lookup"><span data-stu-id="32b65-144">The following example demonstrates the format of the request parameters of update URL: `?x={extension_data}`.</span></span>

<span data-ttu-id="32b65-145">En este ejemplo, `{extension_data}` hay una cadena codificada en url que usa el siguiente formato: `id={id}&v={version}` .</span><span class="sxs-lookup"><span data-stu-id="32b65-145">In this example, `{extension_data}` is a URL-encoded string that uses the following format: `id={id}&v={version}`.</span></span>

<span data-ttu-id="32b65-146">Por ejemplo, las dos extensiones siguientes apuntan a la misma dirección URL de `http://contoso.com/extension_updates.php` actualización.</span><span class="sxs-lookup"><span data-stu-id="32b65-146">For example, the following two extensions both point to the same update URL `http://contoso.com/extension_updates.php`.</span></span>  

*  <span data-ttu-id="32b65-147">Extensión 1 - ID: "aaaaaaaaa" Versión: "1.1"</span><span class="sxs-lookup"><span data-stu-id="32b65-147">Extension 1 - ID: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa" Version: "1.1"</span></span>
*  <span data-ttu-id="32b65-148">Extensión 2 - ID: "bbbbbbbbbbbbbbbbbb" Versión: "0.4"</span><span class="sxs-lookup"><span data-stu-id="32b65-148">Extension 2 - ID: "bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb" Version: "0.4"</span></span>


<span data-ttu-id="32b65-149">Las siguientes son las solicitudes para actualizar cada extensión.</span><span class="sxs-lookup"><span data-stu-id="32b65-149">The following are the requests to update each extension.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="32b65-150">También puede enumerar varias extensiones en una sola solicitud para cada dirección URL de actualización única.</span><span class="sxs-lookup"><span data-stu-id="32b65-150">You may also list multiple extensions in a single request for each unique update URL.</span></span>  <span data-ttu-id="32b65-151">En el ejemplo siguiente se combinan las solicitudes anteriores en una sola solicitud.</span><span class="sxs-lookup"><span data-stu-id="32b65-151">The following example merges the previous requests into a single request.</span></span>  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

<span data-ttu-id="32b65-152">Si envía una sola solicitud y el número de extensiones instaladas que usan la misma dirección URL de actualización es demasiado largo, la comprobación de actualización emite más `GET` solicitudes.</span><span class="sxs-lookup"><span data-stu-id="32b65-152">If you send a single request and the number of installed extensions that use the same update URL is too long, the update check issues more `GET` requests.</span></span>  <span data-ttu-id="32b65-153">Una `GET` dirección URL de solicitud es demasiado larga si tiene aproximadamente 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="32b65-153">A `GET` request URL is too long if it is approximately 2000 characters.</span></span>  

> [!NOTE]
> <span data-ttu-id="32b65-154">En el futuro, una sola `POST` solicitud puede reemplazar varias `GET` solicitudes.</span><span class="sxs-lookup"><span data-stu-id="32b65-154">In the future, a single `POST` request may replace multiple `GET` requests.</span></span>  <span data-ttu-id="32b65-155">La `POST` solicitud puede contener los parámetros de solicitud en el `POST` cuerpo.</span><span class="sxs-lookup"><span data-stu-id="32b65-155">The `POST` request may contain the request parameters in the `POST` body.</span></span>  

## <a name="advanced-usage-minimum-browser-version"></a><span data-ttu-id="32b65-156">Uso avanzado: versión mínima del explorador</span><span class="sxs-lookup"><span data-stu-id="32b65-156">Advanced usage: minimum browser version</span></span>  

<span data-ttu-id="32b65-157">Como nueva versión de las API para el sistema de extensiones de Microsoft Edge, puedes publicar una versión actualizada de la extensión o aplicación que solo funciona con versiones más recientes de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="32b65-157">As new APIs release for the Microsoft Edge extensions system, you may release an updated version of your extension or app that only works with newer Microsoft Edge versions.</span></span>  <span data-ttu-id="32b65-158">Cuando Microsoft Edge se actualiza automáticamente, puede tardar unos días antes de que la mayoría de los usuarios se actualicen a esa nueva versión.</span><span class="sxs-lookup"><span data-stu-id="32b65-158">When Microsoft Edge is auto-updated, it may take a few days before most of your users update to that new release.</span></span>  <span data-ttu-id="32b65-159">Para asegurarse de que una actualización específica solo se aplica a las versiones de Microsoft Edge actuales o más recientes que una versión específica, agregue el `prodversionmin` atributo en el manifiesto de actualización.</span><span class="sxs-lookup"><span data-stu-id="32b65-159">To ensure that a specific update applies only to Microsoft Edge versions that are current or newer than a specific version, add the `prodversionmin` attribute in your update manifest.</span></span>  <span data-ttu-id="32b65-160">En el siguiente fragmento de código, el valor de atributo de especifica que la aplicación actualiza automáticamente a la versión solo cuando el usuario ejecuta Microsoft Edge o una versión `prodversionmin` `3.0.193.0` más `2.0` `3.0.193.0` reciente.</span><span class="sxs-lookup"><span data-stu-id="32b65-160">In the following code snippet, the `prodversionmin` attribute value of `3.0.193.0` specifies that your app auto-updates to version `2.0` only when the user is running Microsoft Edge `3.0.193.0` or newer.</span></span>  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  

> [!NOTE]
> <span data-ttu-id="32b65-162">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="32b65-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="32b65-163">La página original se encuentra [aquí.](https://developer.chrome.com/docs/apps/autoupdate/)</span><span class="sxs-lookup"><span data-stu-id="32b65-163">The original page is found [here](https://developer.chrome.com/docs/apps/autoupdate/).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="32b65-165">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="32b65-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
