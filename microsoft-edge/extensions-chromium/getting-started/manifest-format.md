---
description: Obtenga información sobre el formato del archivo de manifiesto en un paquete de extensión.
title: Formato de archivo de manifiesto
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo web, html, css, javascript, developer, extensions, mv2, mv3, manifest
ms.openlocfilehash: ac2358f8927a762dcef98f9e10cc9f343d8a93f1
ms.sourcegitcommit: afeeeea9fccc3c4c096d7d44c401f4fe87ea2cd7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "11599437"
---
# <a name="manifest-file-format-for-extensions"></a><span data-ttu-id="6b48e-104">Formato de archivo de manifiesto para extensiones</span><span class="sxs-lookup"><span data-stu-id="6b48e-104">Manifest file format for extensions</span></span>

<span data-ttu-id="6b48e-105">Cada extensión para Microsoft Edge (Chromium) tiene un archivo de manifiesto con formato JSON, denominado `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="6b48e-105">Every extension for Microsoft Edge (Chromium) has a JSON-formatted manifest file, named `manifest.json`.</span></span>  <span data-ttu-id="6b48e-106">El archivo de manifiesto es el plano de la extensión.</span><span class="sxs-lookup"><span data-stu-id="6b48e-106">The manifest file is the blueprint of your extension.</span></span>  <span data-ttu-id="6b48e-107">El archivo de manifiesto incluye información como:</span><span class="sxs-lookup"><span data-stu-id="6b48e-107">The manifest file includes information such as:</span></span>

*  <span data-ttu-id="6b48e-108">Número de versión de la extensión.</span><span class="sxs-lookup"><span data-stu-id="6b48e-108">The version number of the extension.</span></span>
*  <span data-ttu-id="6b48e-109">El título de la extensión.</span><span class="sxs-lookup"><span data-stu-id="6b48e-109">The title of the extension.</span></span>
*  <span data-ttu-id="6b48e-110">Los permisos necesarios para que se ejecute la extensión.</span><span class="sxs-lookup"><span data-stu-id="6b48e-110">The permissions that are needed for the extension to run.</span></span>

<span data-ttu-id="6b48e-111">El formato de `manifest.json` las extensiones se mueve de Manifiesto V2 a Manifiesto V3.</span><span class="sxs-lookup"><span data-stu-id="6b48e-111">The format for `manifest.json` for extensions is moving from Manifest V2 to Manifest V3.</span></span>  <span data-ttu-id="6b48e-112">Ambos formatos se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="6b48e-112">Both formats are shown here.</span></span>  <span data-ttu-id="6b48e-113">Para migrar una extensión manifest V2 a Manifest V3, vaya a [Prepare to update your extensions from Manifest v2 to v3][MigrateToMV3].</span><span class="sxs-lookup"><span data-stu-id="6b48e-113">To migrate a Manifest V2 extension to Manifest V3, navigate to [Prepare to update your extensions from Manifest v2 to v3][MigrateToMV3].</span></span>


## <a name="format-of-manifestjson-for-extensions-using-manifest-v3"></a><span data-ttu-id="6b48e-114">Formato de manifest\.jspara extensiones con Manifest V3</span><span class="sxs-lookup"><span data-stu-id="6b48e-114">Format of manifest\.json for extensions using Manifest V3</span></span>

<span data-ttu-id="6b48e-115">El código siguiente muestra los campos compatibles con extensiones `manifest.json` para un paquete manifest V3.</span><span class="sxs-lookup"><span data-stu-id="6b48e-115">The following code shows the fields that are supported in `manifest.json` for extensions, for a Manifest V3 package.</span></span>

<span data-ttu-id="6b48e-116">Para obtener información de referencia sobre cada campo, vaya [a Formato de archivo de manifiesto (V3)][ChromeDeveloperDocsExtensionsMv3Manifest] y, a continuación, seleccione los vínculos de los campos.</span><span class="sxs-lookup"><span data-stu-id="6b48e-116">For reference information about each field, navigate to [Manifest file format (V3)][ChromeDeveloperDocsExtensionsMv3Manifest] and then select the links on the fields.</span></span>

```json
{
  // Required
  "manifest_version": 3,
  "name": "My V3 Extension",
  "version": "versionString",

  // Recommended
  "action": {...},
  "default_locale": "en",
  "description": "A plain-text description",
  "icons": {...},

  // Optional
  "action": ...,
  "author": ...,
  "automation": ...,
  "background": {
    // If `background` is included, `service_ worker` is required
    "service_worker": ...
  },
  "chrome_settings_overrides": {...},
  "chrome_url_overrides": {...},
  "commands": {...},
  "content_capabilities": ...,
  "content_scripts": [{...}],
  "content_security_policy": "policyString",
  "converted_from_user_script": ...,
  "current_locale": ...,
  "declarative_net_request": ...,
  "devtools_page": "devtools.html",
  "differential_fingerprint": ...,
  "event_rules": [{...}],
  "externally_connectable": {
    "matches": ["*://*.contoso.com/*"]
  },
  "file_browser_handlers": [...],
  "file_system_provider_capabilities": {
    "configurable": true,
    "multiple_mounts": true,
    "source": "network"
  },
  "homepage_url": "http://path/to/homepage",
  "host_permissions": [...],
  "import": [{"id": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"}],
  "incognito": "spanning, split, or not_allowed",
  "input_components": ...,
  "key": "publicKey",
  "minimum_chrome_version": "versionString",
  "nacl_modules": [...],
  "natively_connectable": ...,
  "oauth2": ...,
  "offline_enabled": true,
  "omnibox": {
    "keyword": "aString"
  },
  "optional_permissions": ["tabs"],
  "options_page": "options.html",
  "options_ui": {
    "chrome_style": true,
    "page": "options.html"
  },
  "permissions": ["tabs"],
  "platforms": ...,
  "replacement_web_app": ...,
  "requirements": {...},
  "sandbox": [...],
  "short_name": "Short Name",
  "storage": {
    "managed_schema": "schema.json"
  },
  "system_indicator": ...,
  "tts_engine": {...},
  "update_url": "http://path/to/updateInfo.xml",
  "version_name": "aString",
  "web_accessible_resources": [...]
}
```

## <a name="format-of-manifestjson-for-extensions-using-manifest-v2"></a><span data-ttu-id="6b48e-117">Formato de manifest\.jspara extensiones con Manifest V2</span><span class="sxs-lookup"><span data-stu-id="6b48e-117">Format of manifest\.json for extensions using Manifest V2</span></span>

<span data-ttu-id="6b48e-118">El código siguiente muestra los campos compatibles con extensiones `manifest.json` para un paquete manifest V2.</span><span class="sxs-lookup"><span data-stu-id="6b48e-118">The following code shows the fields that are supported in `manifest.json` for extensions, for a Manifest V2 package.</span></span>

<span data-ttu-id="6b48e-119">Para obtener información de referencia sobre cada campo, vaya [a Formato de archivo de manifiesto (V2)][ChromeDeveloperDocsExtensionsMv2Manifest] y, a continuación, seleccione los vínculos de los campos.</span><span class="sxs-lookup"><span data-stu-id="6b48e-119">For reference information about each field, navigate to [Manifest file format (V2)][ChromeDeveloperDocsExtensionsMv2Manifest] and then select the links on the fields.</span></span>

```json
{
  // Required
  "manifest_version": 2,
  "name": "My V2 Extension",
  "version": "versionString",

  // Recommended
  "default_locale": "en",
  "description": "A plain-text description",
  "icons": {...},

  // Pick one or none
  "browser_action": {...},
  "page_action": {...},

  // Optional
  "action": ...,
  "author": ...,
  "automation": ...,
  "background": {
    // If `background` is included, `persistent` is recommended
    "persistent": false,
    // If `background` is included, `service_worker` is optional
    "service_worker": ...
  },
  "chrome_settings_overrides": {...},
  "chrome_url_overrides": {...},
  "commands": {...},
  "content_capabilities": ...,
  "content_scripts": [{...}],
  "content_security_policy": "policyString",
  "converted_from_user_script": ...,
  "current_locale": ...,
  "declarative_net_request": ...,
  "devtools_page": "devtools.html",
  "differential_fingerprint": ...,
  "event_rules": [{...}],
  "externally_connectable": {
    "matches": ["*://*.contoso.com/*"]
  },
  "file_browser_handlers": [...],
  "file_system_provider_capabilities": {
    "configurable": true,
    "multiple_mounts": true,
    "source": "network"
  },
  "homepage_url": "http://path/to/homepage",
  "host_permissions": ...,
  "import": [{"id": "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"}],
  "incognito": "spanning, split, or not_allowed",
  "input_components": ...,
  "key": "publicKey",
  "minimum_chrome_version": "versionString",
  "nacl_modules": [...],
  "natively_connectable": ...,
  "oauth2": ...,
  "offline_enabled": true,
  "omnibox": {
    "keyword": "aString"
  },
  "optional_permissions": ["tabs"],
  "options_page": "options.html",
  "options_ui": {
    "chrome_style": true,
    "page": "options.html"
  },
  "permissions": ["tabs"],
  "platforms": ...,
  "replacement_web_app": ...,
  "requirements": {...},
  "sandbox": [...],
  "short_name": "Short Name",
  "storage": {
    "managed_schema": "schema.json"
  },
  "system_indicator": ...,
  "tts_engine": {...},
  "update_url": "http://path/to/updateInfo.xml",
  "version_name": ...,
  "web_accessible_resources": [...]
}
```

> [!NOTE]
> <span data-ttu-id="6b48e-120">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6b48e-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6b48e-121">La página original se encuentra [aquí.](https://developer.chrome.com/docs/extensions/mv3/manifest/)</span><span class="sxs-lookup"><span data-stu-id="6b48e-121">The original page is found [here](https://developer.chrome.com/docs/extensions/mv3/manifest/).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6b48e-123">Este trabajo dispone de una [Licencia internacional de Atribución de Creative Commons 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6b48e-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies


<!-- links -->
[MigrateToMV3]: ../developer-guide/migrate-your-extension-from-manifest-v2-to-v3.md "Prepararse para actualizar las extensiones de Manifest v2 a v3 | Microsoft Docs"

[ChromeDeveloperDocsExtensionsMv3Manifest]: https://developer.chrome.com/docs/extensions/mv3/manifest "Formato de archivo de manifiesto (V3) | Desarrolladores de Chrome"
[ChromeDeveloperDocsExtensionsMv2Manifest]: https://developer.chrome.com/docs/extensions/mv2/manifest "Formato de archivo de manifiesto (V2) | Desarrolladores de Chrome"
