---
description: Obtenga información sobre cómo declarar permisos para API en el manifiesto
title: Declarar permisos de API en manifiestos de extensión
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 987279a8072388d3fd47ee8b7cbf5f9bb3c483e0
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461577"
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
# <a name="declare-api-permissions-in-extension-manifests"></a><span data-ttu-id="d082a-104">Declarar permisos de API en manifiestos de extensión</span><span class="sxs-lookup"><span data-stu-id="d082a-104">Declare API permissions in extension manifests</span></span>  

<span data-ttu-id="d082a-105">Para usar la mayoría de `chrome.*` las API, la extensión debe declarar la `permissions` en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="d082a-105">To use most of the `chrome.*` APIs, your extension must declare the `permissions` in the manifest.</span></span>  <span data-ttu-id="d082a-106">Puede declarar permisos mediante una cadena de permisos de la tabla siguiente o usar un patrón para coincidir con cadenas similares.</span><span class="sxs-lookup"><span data-stu-id="d082a-106">You may declare permissions using a permission string from the table that follows, or use a pattern to match similar strings.</span></span>  <span data-ttu-id="d082a-107">Los permisos ayudan a restringir la extensión si se ve comprometida por malware.</span><span class="sxs-lookup"><span data-stu-id="d082a-107">Permissions help to constrain your extension if it gets compromised by malware.</span></span>  <span data-ttu-id="d082a-108">Algunos permisos pueden mostrarse a los usuarios antes de la instalación de la extensión mediante advertencias de permisos.</span><span class="sxs-lookup"><span data-stu-id="d082a-108">Some permissions may display to users before installation of the extension using Permission Warnings.</span></span>  

<span data-ttu-id="d082a-109">Si una API requiere que declare permisos en el manifiesto, revise la documentación de esa API para comprender los permisos necesarios.</span><span class="sxs-lookup"><span data-stu-id="d082a-109">If an API requires you to declare permissions in the manifest, review the documentation for that API to understand the needed permissions.</span></span>  <span data-ttu-id="d082a-110">Por ejemplo, la página API de almacenamiento describe cómo declarar el `storage` permiso.</span><span class="sxs-lookup"><span data-stu-id="d082a-110">For example, the Storage API page describes how to declare the `storage` permission.</span></span>  

<span data-ttu-id="d082a-111">En el siguiente fragmento de código se describe cómo declarar permisos en el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="d082a-111">The following code snippet outlines how to declare permissions in the manifest file.</span></span>  

```json
"permissions": [
  "tabs",
  "bookmarks",
  "http://www.blogger.com/",
  "http://*.google.com/",
  "unlimitedStorage"
]
```  

<span data-ttu-id="d082a-112">En la tabla siguiente se enumeran las cadenas de permisos disponibles actualmente para usar en el manifiesto y las descripciones.</span><span class="sxs-lookup"><span data-stu-id="d082a-112">The following table lists the currently available permission strings to use in your manifest, and the descriptions.</span></span>  

| <span data-ttu-id="d082a-113">Cadena de permisos</span><span class="sxs-lookup"><span data-stu-id="d082a-113">Permission string</span></span> | <span data-ttu-id="d082a-114">Detalles</span><span class="sxs-lookup"><span data-stu-id="d082a-114">Details</span></span> |  
|:--- |:--- |  
| `activeTab` | <span data-ttu-id="d082a-115">Solicita que se concedan permisos a la extensión de acuerdo con la `activeTab` especificación.</span><span class="sxs-lookup"><span data-stu-id="d082a-115">Requests that the extension is granted permissions according to the `activeTab` specification.</span></span> |  
| `alarms` | <span data-ttu-id="d082a-116">Proporciona a la extensión acceso a la `chrome.alarms` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-116">Gives your extension access to the `chrome.alarms` API.</span></span> |  
| `background` | <span data-ttu-id="d082a-117">Hace que Microsoft Edge se inicie antes y se cierre tarde, de modo que las extensiones puedan tener una vida más larga.</span><span class="sxs-lookup"><span data-stu-id="d082a-117">Makes Microsoft Edge start up early and shut down late, so that extensions may have a longer life.</span></span>  <span data-ttu-id="d082a-118">Cuando cualquier extensión instalada tiene permiso, Microsoft Edge se ejecuta invisiblemente tan pronto como el usuario inicia sesión en el equipo del usuario y antes de que el usuario inicie `background` Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d082a-118">When any installed extension has `background` permission, Microsoft Edge runs invisibly as soon as the user logs into the user's computer, and before the user launches Microsoft Edge.</span></span>  <span data-ttu-id="d082a-119">El permiso también hace que Microsoft Edge continúe ejecutándose, incluso después de cerrar su última ventana, hasta que el usuario `background` salga explícitamente de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d082a-119">The `background` permission also makes Microsoft Edge continue running, even after its last window is closed, until the user explicitly quits Microsoft Edge.</span></span>  <span data-ttu-id="d082a-120">Este permiso no afecta a las extensiones que están desactivadas en el explorador.</span><span class="sxs-lookup"><span data-stu-id="d082a-120">This permission does not affect extensions that are turned off in the browser.</span></span>  <span data-ttu-id="d082a-121">El `background` permiso se usa normalmente en una página en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d082a-121">The `background` permission is normally used on a background page.</span></span> |  
| `bookmarks` | <span data-ttu-id="d082a-122">Proporciona a la extensión acceso a la `chrome.bookmarks` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-122">Gives your extension access to the `chrome.bookmarks` API.</span></span> |  
| `browsingData` | <span data-ttu-id="d082a-123">Proporciona a la extensión acceso a la `chrome.browsingData` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-123">Gives your extension access to the `chrome.browsingData` API.</span></span> |  
| `certificateProvider` | <span data-ttu-id="d082a-124">Proporciona a la extensión acceso a la `chrome.certificateProvider` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-124">Gives your extension access to the `chrome.certificateProvider` API.</span></span> |  
| `clipboardRead` | <span data-ttu-id="d082a-125">Obligatorio si la extensión usa `document.execCommand('paste')` .</span><span class="sxs-lookup"><span data-stu-id="d082a-125">Required if the extension uses `document.execCommand('paste')`.</span></span> |  
| `clipboardWrite` | <span data-ttu-id="d082a-126">Indica que la extensión usa `document.execCommand('copy')` o `document.execCommand('cut')` .</span><span class="sxs-lookup"><span data-stu-id="d082a-126">Indicates the extension uses `document.execCommand('copy')` or `document.execCommand('cut')`.</span></span> |  
| `contentSettings` | <span data-ttu-id="d082a-127">Proporciona a la extensión acceso a la `chrome.contentSettings` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-127">Gives your extension access to the `chrome.contentSettings` API.</span></span> |  
| `contextMenus` | <span data-ttu-id="d082a-128">Proporciona a la extensión acceso a la `chrome.contextMenus` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-128">Gives your extension access to the `chrome.contextMenus` API.</span></span> |  
| `cookies` | <span data-ttu-id="d082a-129">Proporciona a la extensión acceso a la `chrome.cookies` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-129">Gives your extension access to the `chrome.cookies` API.</span></span> |  
| `debugger` | <span data-ttu-id="d082a-130">Proporciona a la extensión acceso a la `chrome.debugger` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-130">Gives your extension access to the `chrome.debugger` API.</span></span> |  
| `declarativeContent` | <span data-ttu-id="d082a-131">Proporciona a la extensión acceso a la `chrome.declarativeContent` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-131">Gives your extension access to the `chrome.declarativeContent` API.</span></span> |  
| `declarativeNetRequest` | <span data-ttu-id="d082a-132">Proporciona a la extensión acceso a la `chrome.declarativeNetRequest` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-132">Gives your extension access to the `chrome.declarativeNetRequest` API.</span></span> |  
| `declarativeNetRequestFeedback` | <span data-ttu-id="d082a-133">Concede a la extensión acceso a eventos y métodos dentro de la `chrome.declarativeNetRequest` API, que devuelve información sobre las reglas declarativas coincidentes.</span><span class="sxs-lookup"><span data-stu-id="d082a-133">Grants the extension access to events and methods within the `chrome.declarativeNetRequest` API, which returns information on declarative rules matched.</span></span> |  
| `declarativeWebRequest` | <span data-ttu-id="d082a-134">Proporciona a la extensión acceso a la `chrome.declarativeWebRequest` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-134">Gives your extension access to the `chrome.declarativeWebRequest` API.</span></span> |  
| `desktopCapture` | <span data-ttu-id="d082a-135">Proporciona a la extensión acceso a la `chrome.desktopCapture` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-135">Gives your extension access to the `chrome.desktopCapture` API.</span></span> |  
| `documentScan` | <span data-ttu-id="d082a-136">Proporciona a la extensión acceso a la `chrome.documentScan` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-136">Gives your extension access to the `chrome.documentScan` API.</span></span> |  
| `downloads` | <span data-ttu-id="d082a-137">Proporciona a la extensión acceso a la `chrome.downloads` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-137">Gives your extension access to the `chrome.downloads` API.</span></span> |  
| `enterprise.deviceAttributes` | <span data-ttu-id="d082a-138">Proporciona a la extensión acceso a la `chrome.enterprise.deviceAttributes` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-138">Gives your extension access to the `chrome.enterprise.deviceAttributes` API.</span></span> |  
| `enterprise.hardwarePlatform` | <span data-ttu-id="d082a-139">Proporciona a la extensión acceso a la `chrome.enterprise.hardwarePlatform` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-139">Gives your extension access to the `chrome.enterprise.hardwarePlatform` API.</span></span> |  
| `enterprise.networkingAttributes` | <span data-ttu-id="d082a-140">Proporciona a la extensión acceso a la `chrome.enterprise.networkingAttributes` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-140">Gives your extension access to the `chrome.enterprise.networkingAttributes` API.</span></span> |  
| `enterprise.platformKeys` | <span data-ttu-id="d082a-141">Proporciona a la extensión acceso a la `chrome.enterprise.platformKeys` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-141">Gives your extension access to the `chrome.enterprise.platformKeys` API.</span></span> |  
| `experimental` | <span data-ttu-id="d082a-142">Obligatorio si la extensión usa alguna `chrome.experimental.*` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-142">Required if the extension uses any `chrome.experimental.*` API.</span></span> |  
| `fileBrowserHandler` | <span data-ttu-id="d082a-143">Proporciona a la extensión acceso a la `chrome.fileBrowserHandler` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-143">Gives your extension access to the `chrome.fileBrowserHandler` API.</span></span> |  
| `fileSystemProvider` | <span data-ttu-id="d082a-144">Proporciona a la extensión acceso a la `chrome.fileSystemProvider` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-144">Gives your extension access to the `chrome.fileSystemProvider` API.</span></span> |  
| `fontSettings` | <span data-ttu-id="d082a-145">Proporciona a la extensión acceso a la `chrome.fontSettings` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-145">Gives your extension access to the `chrome.fontSettings` API.</span></span> |  
| `geolocation` | <span data-ttu-id="d082a-146">Permite que la extensión use la API de geolocalización sin pedir permiso al usuario.</span><span class="sxs-lookup"><span data-stu-id="d082a-146">Allows the extension to use the geolocation API without prompting the user for permission.</span></span> |  
| `history` | <span data-ttu-id="d082a-147">Proporciona a la extensión acceso a la `chrome.history` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-147">Gives your extension access to the `chrome.history` API.</span></span> |  
| `identity` | <span data-ttu-id="d082a-148">Proporciona a la extensión acceso a la `chrome.identity` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-148">Gives your extension access to the `chrome.identity` API.</span></span> |  
| `idle` | <span data-ttu-id="d082a-149">Proporciona a la extensión acceso a la `chrome.idle` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-149">Gives your extension access to the `chrome.idle` API.</span></span> |  
| `loginState` | <span data-ttu-id="d082a-150">Proporciona a la extensión acceso a la `chrome.loginState` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-150">Gives your extension access to the `chrome.loginState` API.</span></span> |  
| `management` | <span data-ttu-id="d082a-151">Proporciona a la extensión acceso a la `chrome.management` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-151">Gives your extension access to the `chrome.management` API.</span></span> |  
| `nativeMessaging` | <span data-ttu-id="d082a-152">Proporciona a la extensión acceso a la API de mensajería nativa.</span><span class="sxs-lookup"><span data-stu-id="d082a-152">Gives your extension access to the native messaging API.</span></span> |  
| `notifications` | <span data-ttu-id="d082a-153">Proporciona a la extensión acceso a la `chrome.notifications` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-153">Gives your extension access to the `chrome.notifications` API.</span></span> |  
| `pageCapture` | <span data-ttu-id="d082a-154">Proporciona a la extensión acceso a la `chrome.pageCapture` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-154">Gives your extension access to the `chrome.pageCapture` API.</span></span> |  
| `platformKeys` | <span data-ttu-id="d082a-155">Proporciona a la extensión acceso a la `chrome.platformKeys` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-155">Gives your extension access to the `chrome.platformKeys` API.</span></span> |  
| `power` | <span data-ttu-id="d082a-156">Proporciona a la extensión acceso a la `chrome.power` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-156">Gives your extension access to the `chrome.power` API.</span></span> |  
| `printerProvider` | <span data-ttu-id="d082a-157">Proporciona a la extensión acceso a la `chrome.printerProvider` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-157">Gives your extension access to the `chrome.printerProvider` API.</span></span> |  
| `printing` | <span data-ttu-id="d082a-158">Proporciona a la extensión acceso a la `chrome.printing` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-158">Gives your extension access to the `chrome.printing` API.</span></span> |  
| `printingMetrics` | <span data-ttu-id="d082a-159">Proporciona a la extensión acceso a la `chrome.printingMetrics` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-159">Gives your extension access to the `chrome.printingMetrics` API.</span></span> |  
| `privacy` | <span data-ttu-id="d082a-160">Proporciona a la extensión acceso a la `chrome.privacy` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-160">Gives your extension access to the `chrome.privacy` API.</span></span> |  
| `processes` | <span data-ttu-id="d082a-161">Proporciona a la extensión acceso a la `chrome.processes` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-161">Gives your extension access to the `chrome.processes` API.</span></span> |  
| `proxy` | <span data-ttu-id="d082a-162">Proporciona a la extensión acceso a la `chrome.proxy` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-162">Gives your extension access to the `chrome.proxy` API.</span></span> |  
| `scripting` | <span data-ttu-id="d082a-163">Proporciona a la extensión acceso a la `chrome.scripting` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-163">Gives your extension access to the `chrome.scripting` API.</span></span> |  
| `search` | <span data-ttu-id="d082a-164">Proporciona a la extensión acceso a la `chrome.search` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-164">Gives your extension access to the `chrome.search` API.</span></span> |  
| `sessions` | <span data-ttu-id="d082a-165">Proporciona a la extensión acceso a la `chrome.sessions` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-165">Gives your extension access to the `chrome.sessions` API.</span></span> |  
| `signedInDevices` | <span data-ttu-id="d082a-166">Proporciona a la extensión acceso a la `chrome.signedInDevices` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-166">Gives your extension access to the `chrome.signedInDevices` API.</span></span> |  
| `storage` | <span data-ttu-id="d082a-167">Proporciona a la extensión acceso a la `chrome.storage` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-167">Gives your extension access to the `chrome.storage` API.</span></span> |  
| `system.cpu` | <span data-ttu-id="d082a-168">Proporciona a la extensión acceso a la `chrome.system.cpu` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-168">Gives your extension access to the `chrome.system.cpu` API.</span></span> |  
| `system.display` | <span data-ttu-id="d082a-169">Proporciona a la extensión acceso a la `chrome.system.display` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-169">Gives your extension access to the `chrome.system.display` API.</span></span> |  
| `system.memory` | <span data-ttu-id="d082a-170">Proporciona a la extensión acceso a la `chrome.system.memory` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-170">Gives your extension access to the `chrome.system.memory` API.</span></span> |  
| `system.storage` | <span data-ttu-id="d082a-171">Proporciona a la extensión acceso a la `chrome.system.storage` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-171">Gives your extension access to the `chrome.system.storage` API.</span></span> |  
| `tabCapture` | <span data-ttu-id="d082a-172">Proporciona a la extensión acceso a la `chrome.tabCapture` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-172">Gives your extension access to the `chrome.tabCapture` API.</span></span> |  
| `tabGroups` | <span data-ttu-id="d082a-173">Proporciona a la extensión acceso a la `chrome.tabGroups` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-173">Gives your extension access to the `chrome.tabGroups` API.</span></span> |  
| `tabs` | <span data-ttu-id="d082a-174">Proporciona a la extensión acceso a campos con privilegios de los objetos que pueden usar varias `Tab` API, `chrome.tabs` incluidas y `chrome.windows` .</span><span class="sxs-lookup"><span data-stu-id="d082a-174">Gives your extension access to privileged fields of the `Tab` objects that may be used by several APIs including `chrome.tabs` and `chrome.windows`.</span></span>  <span data-ttu-id="d082a-175">En muchas circunstancias, la extensión no necesita declarar el permiso para hacer `tabs` uso de estas API.</span><span class="sxs-lookup"><span data-stu-id="d082a-175">In many circumstances, your extension does not need to declare the `tabs` permission to make use of these APIs.</span></span> |  
| `topSites` | <span data-ttu-id="d082a-176">Proporciona a la extensión acceso a la `chrome.topSites` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-176">Gives your extension access to the `chrome.topSites` API.</span></span> |  
| `tts` | <span data-ttu-id="d082a-177">Proporciona a la extensión acceso a la `chrome.tts` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-177">Gives your extension access to the `chrome.tts` API.</span></span> |  
| `ttsEngine` | <span data-ttu-id="d082a-178">Proporciona a la extensión acceso a la `chrome.ttsEngine` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-178">Gives your extension access to the `chrome.ttsEngine` API.</span></span> |  
| `unlimitedStorage` | <span data-ttu-id="d082a-179">Proporciona una cuota ilimitada para almacenar datos del lado cliente, como bases de datos y archivos de almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="d082a-179">Provides an unlimited quota for storing client-side data, such as databases and local storage files.</span></span>  <span data-ttu-id="d082a-180">Sin este permiso, la extensión está limitada a 5 MB de almacenamiento local.</span><span class="sxs-lookup"><span data-stu-id="d082a-180">Without this permission, the extension is limited to 5 MB of local storage.</span></span> |  
| `vpnProvider` | <span data-ttu-id="d082a-181">Proporciona a la extensión acceso a la `chrome.vpnProvider` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-181">Gives your extension access to the `chrome.vpnProvider` API.</span></span> |  
| `wallpaper` | <span data-ttu-id="d082a-182">Proporciona a la extensión acceso a la `chrome.wallpaper` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-182">Gives your extension access to the `chrome.wallpaper` API.</span></span> |  
| `webNavigation` | <span data-ttu-id="d082a-183">Proporciona a la extensión acceso a la `chrome.webNavigation` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-183">Gives your extension access to the `chrome.webNavigation` API.</span></span> |  
| `webRequest` | <span data-ttu-id="d082a-184">Proporciona a la extensión acceso a la `chrome.webRequest` API.</span><span class="sxs-lookup"><span data-stu-id="d082a-184">Gives your extension access to the `chrome.webRequest` API.</span></span> |  
| `webRequestBlocking` | <span data-ttu-id="d082a-185">Obligatorio si la extensión usa la `chrome.webRequest` API para bloquear solicitudes.</span><span class="sxs-lookup"><span data-stu-id="d082a-185">Required if the extension uses the `chrome.webRequest` API to block requests.</span></span> |  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="d082a-186">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d082a-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d082a-187">La página original se encuentra [aquí.](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/)</span><span class="sxs-lookup"><span data-stu-id="d082a-187">The original page is found [here](https://developer.chrome.com/docs/extensions/mv3/declare_permissions/).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d082a-189">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d082a-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
