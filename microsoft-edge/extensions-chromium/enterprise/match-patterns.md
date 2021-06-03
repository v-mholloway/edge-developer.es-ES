---
description: Enterprise de directivas para extensiones perimetrales (Chromium).
title: Patrones de coincidencia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: fcb87b62cac063c7663f575fa3d992b187408c28
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461251"
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
# <a name="match-patterns"></a><span data-ttu-id="4c443-104">Patrones de coincidencia</span><span class="sxs-lookup"><span data-stu-id="4c443-104">Match Patterns</span></span>

<span data-ttu-id="4c443-105">Los permisos de host y la coincidencia de scripts de contenido se basan en un conjunto de direcciones URL definidas por patrones de coincidencia.</span><span class="sxs-lookup"><span data-stu-id="4c443-105">Host permissions and content script matching are based on a set of URLs defined by match patterns.</span></span>  <span data-ttu-id="4c443-106">Un patrón de coincidencia es esencialmente una dirección URL que comienza con un esquema permitido ( , , , o , y `http` que puede contener ' ' `https` `file` `ftp` `*` caracteres.</span><span class="sxs-lookup"><span data-stu-id="4c443-106">A match pattern is essentially a URL that begins with a permitted scheme (`http`, `https`, `file`, or `ftp`, and that can contain '`*`' characters.</span></span>  <span data-ttu-id="4c443-107">El patrón especial `<all_urls>` coincide con cualquier dirección URL que comience por un esquema permitido.</span><span class="sxs-lookup"><span data-stu-id="4c443-107">The special pattern `<all_urls>` matches any URL that starts with a permitted scheme.</span></span>  <span data-ttu-id="4c443-108">Cada patrón de coincidencia tiene 3 partes:</span><span class="sxs-lookup"><span data-stu-id="4c443-108">Each match pattern has 3 parts:</span></span>  

*   <span data-ttu-id="4c443-109">_esquema_ , por ejemplo, `http` `file` o</span><span class="sxs-lookup"><span data-stu-id="4c443-109">_scheme_ — for example, `http` or `file` or</span></span> `*`  

> [!NOTE]
> <span data-ttu-id="4c443-110">El acceso `file` a las direcciones URL no es automático.</span><span class="sxs-lookup"><span data-stu-id="4c443-110">Access to `file` URLs is not automatic.</span></span>  <span data-ttu-id="4c443-111">El usuario debe visitar la página de administración de extensiones y participar para obtener `file` acceso a cada extensión que lo solicite.</span><span class="sxs-lookup"><span data-stu-id="4c443-111">The user must visit the Extensions management page and opt in to `file` access for each Extension that requests it.</span></span>  

*   `_host_` <span data-ttu-id="4c443-112">— por ejemplo, `www.google.com` o ; si el esquema es `*.google.com` `*` archivo, no hay ninguna parte host.</span><span class="sxs-lookup"><span data-stu-id="4c443-112">— for example, `www.google.com` or `*.google.com` or `*`; if the scheme is file, there is no host part.</span></span>  
*   `_path_` <span data-ttu-id="4c443-113">— por ejemplo, `/*` , `/foo*` o `/foo/bar` .</span><span class="sxs-lookup"><span data-stu-id="4c443-113">— for example, `/*`, `/foo*`, or `/foo/bar`.</span></span>  <span data-ttu-id="4c443-114">La ruta de acceso debe estar presente en un permiso de host, pero siempre se trata como `/*` .</span><span class="sxs-lookup"><span data-stu-id="4c443-114">The path must be present in a host permission, but is always treated as `/*`.</span></span>  

<span data-ttu-id="4c443-115">Sintaxis básica:</span><span class="sxs-lookup"><span data-stu-id="4c443-115">The basic syntax:</span></span>  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

<span data-ttu-id="4c443-116">El significado de depende de si está en la `*` parte de esquema, host o ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="4c443-116">The meaning of `*` depends on whether it is in the scheme, host, or path part.</span></span>  <span data-ttu-id="4c443-117">Si el esquema es `*` , entonces coincide o , y no , o `http` `https` `file` `ftp` .</span><span class="sxs-lookup"><span data-stu-id="4c443-117">If the scheme is `*`, then it matches either `http` or `https`, and not `file`, or `ftp`.</span></span>  <span data-ttu-id="4c443-118">Si el host es simplemente `*` , entonces coincide con cualquier host.</span><span class="sxs-lookup"><span data-stu-id="4c443-118">If the host is just `*`, then it matches any host.</span></span> <span data-ttu-id="4c443-119">Si el host es `*.hostname` , entonces coincide con el host especificado o cualquiera de los subdominios.</span><span class="sxs-lookup"><span data-stu-id="4c443-119">If the host is `*.hostname`, then it matches the specified host or any of the subdomains.</span></span>  <span data-ttu-id="4c443-120">En la sección ruta de acceso, `*` cada uno coincide con 0 o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="4c443-120">In the path section, each `*` matches 0 or more characters.</span></span>  <span data-ttu-id="4c443-121">En la tabla siguiente se muestran algunos patrones válidos.</span><span class="sxs-lookup"><span data-stu-id="4c443-121">The following table shows some valid patterns.</span></span>  

| <span data-ttu-id="4c443-122">Patrón</span><span class="sxs-lookup"><span data-stu-id="4c443-122">Pattern</span></span> | <span data-ttu-id="4c443-123">Qué hace</span><span class="sxs-lookup"><span data-stu-id="4c443-123">What it does</span></span> | <span data-ttu-id="4c443-124">Ejemplos de direcciones URL que coinciden</span><span class="sxs-lookup"><span data-stu-id="4c443-124">Examples of matching URLs</span></span> |  
|:--- |:--- |:--- |  
| `http://*/*` | <span data-ttu-id="4c443-125">Coincide con cualquier dirección URL que use el esquema http</span><span class="sxs-lookup"><span data-stu-id="4c443-125">Matches any URL that uses the http scheme</span></span> | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | <span data-ttu-id="4c443-126">Coincide con cualquier dirección URL que use el esquema http, en cualquier host, siempre que la ruta comience por</span><span class="sxs-lookup"><span data-stu-id="4c443-126">Matches any URL that uses the http scheme, on any host, as long as the path starts with</span></span> `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | <span data-ttu-id="4c443-127">Coincide con cualquier dirección URL que usa el esquema https, está en un `google.com` host \(como `www.google.com` , o `docs.google.com` `google.com` \), siempre que la ruta comience por `/foo` y termine con</span><span class="sxs-lookup"><span data-stu-id="4c443-127">Matches any URL that uses the https scheme, is on a `google.com` host \(such as `www.google.com`, `docs.google.com`, or `google.com`\), as long as the path starts with `/foo` and ends with</span></span> `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | <span data-ttu-id="4c443-128">Coincide con la dirección URL especificada</span><span class="sxs-lookup"><span data-stu-id="4c443-128">Matches the specified URL</span></span> | `http://example.org/foo/bar.html` |  
|`file:///foo*` | <span data-ttu-id="4c443-129">Coincide con cualquier archivo local cuya ruta de acceso comience por</span><span class="sxs-lookup"><span data-stu-id="4c443-129">Matches any local file whose path starts with</span></span> `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | <span data-ttu-id="4c443-130">Coincide con cualquier dirección URL que usa `http` el esquema y está en el host</span><span class="sxs-lookup"><span data-stu-id="4c443-130">Matches any URL that uses the `http` scheme and is on the host</span></span> `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | <span data-ttu-id="4c443-131">Coincide con cualquier dirección URL que empiece `http://mail.google.com` por o `https://mail.google.com` .</span><span class="sxs-lookup"><span data-stu-id="4c443-131">Matches any URL that starts with `http://mail.google.com` or `https://mail.google.com`.</span></span> | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | <span data-ttu-id="4c443-132">Coincide con cualquier dirección URL que use un esquema permitido.</span><span class="sxs-lookup"><span data-stu-id="4c443-132">Matches any URL that uses a permitted scheme.</span></span> <span data-ttu-id="4c443-133">\(Vea el principio de esta sección para ver la lista de esquemas permitidos.\)</span><span class="sxs-lookup"><span data-stu-id="4c443-133">\(See the beginning of this section for the list of permitted schemes.\)</span></span> | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

<span data-ttu-id="4c443-134">Estos son algunos ejemplos de `_invalid_` coincidencias de patrones:</span><span class="sxs-lookup"><span data-stu-id="4c443-134">Here are some examples of `_invalid_` pattern matches:</span></span>

| <span data-ttu-id="4c443-135">Patrón malo</span><span class="sxs-lookup"><span data-stu-id="4c443-135">Bad pattern</span></span> | <span data-ttu-id="4c443-136">Por qué es malo</span><span class="sxs-lookup"><span data-stu-id="4c443-136">Why it is bad</span></span> |  
|:--- |:--- |  
| `http://www.foo.com` | <span data-ttu-id="4c443-137">No</span><span class="sxs-lookup"><span data-stu-id="4c443-137">No</span></span> `_path_` |  
| `http://*foo/bar` | <span data-ttu-id="4c443-138">' `*` ' en el host puede seguirse solo por un ' ' o ' ' `.` `/` '</span><span class="sxs-lookup"><span data-stu-id="4c443-138">'`*`' in the host can be followed only by a '`.`' or '`/`'</span></span> |  
| `http://foo.*.bar/baz` | <span data-ttu-id="4c443-139">Si ' `*` ' está en , debe ser el primer `_host_` carácter</span><span class="sxs-lookup"><span data-stu-id="4c443-139">If '`*`' is in the `_host_`, it must be the first character</span></span> |  
| `http:/bar` | <span data-ttu-id="4c443-140">Falta `_scheme_` el separador \(' `/` ' debe ser " `//` "\)</span><span class="sxs-lookup"><span data-stu-id="4c443-140">Missing `_scheme_` separator \('`/`' should be "`//`"\)</span></span> |  
| `foo://*` | <span data-ttu-id="4c443-141">No válido</span><span class="sxs-lookup"><span data-stu-id="4c443-141">Invalid</span></span> `_scheme_` |  

<span data-ttu-id="4c443-142">Algunos esquemas no se admiten en todos los contextos.</span><span class="sxs-lookup"><span data-stu-id="4c443-142">Some schemes are not supported in all contexts.</span></span>

> [!NOTE]
> <span data-ttu-id="4c443-143">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4c443-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4c443-144">La página original se encuentra [aquí.](https://developer.chrome.com/extensions/match_patterns)</span><span class="sxs-lookup"><span data-stu-id="4c443-144">The original page is found [here](https://developer.chrome.com/extensions/match_patterns).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="4c443-146">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4c443-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
