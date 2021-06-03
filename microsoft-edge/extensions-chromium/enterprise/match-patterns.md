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
# <a name="match-patterns"></a>Patrones de coincidencia

Los permisos de host y la coincidencia de scripts de contenido se basan en un conjunto de direcciones URL definidas por patrones de coincidencia.  Un patrón de coincidencia es esencialmente una dirección URL que comienza con un esquema permitido ( , , , o , y `http` que puede contener ' ' `https` `file` `ftp` `*` caracteres.  El patrón especial `<all_urls>` coincide con cualquier dirección URL que comience por un esquema permitido.  Cada patrón de coincidencia tiene 3 partes:  

*   _esquema_ , por ejemplo, `http` `file` o `*`  

> [!NOTE]
> El acceso `file` a las direcciones URL no es automático.  El usuario debe visitar la página de administración de extensiones y participar para obtener `file` acceso a cada extensión que lo solicite.  

*   `_host_` — por ejemplo, `www.google.com` o ; si el esquema es `*.google.com` `*` archivo, no hay ninguna parte host.  
*   `_path_` — por ejemplo, `/*` , `/foo*` o `/foo/bar` .  La ruta de acceso debe estar presente en un permiso de host, pero siempre se trata como `/*` .  

Sintaxis básica:  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

El significado de depende de si está en la `*` parte de esquema, host o ruta de acceso.  Si el esquema es `*` , entonces coincide o , y no , o `http` `https` `file` `ftp` .  Si el host es simplemente `*` , entonces coincide con cualquier host. Si el host es `*.hostname` , entonces coincide con el host especificado o cualquiera de los subdominios.  En la sección ruta de acceso, `*` cada uno coincide con 0 o más caracteres.  En la tabla siguiente se muestran algunos patrones válidos.  

| Patrón | Qué hace | Ejemplos de direcciones URL que coinciden |  
|:--- |:--- |:--- |  
| `http://*/*` | Coincide con cualquier dirección URL que use el esquema http | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Coincide con cualquier dirección URL que use el esquema http, en cualquier host, siempre que la ruta comience por `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Coincide con cualquier dirección URL que usa el esquema https, está en un `google.com` host \(como `www.google.com` , o `docs.google.com` `google.com` \), siempre que la ruta comience por `/foo` y termine con `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Coincide con la dirección URL especificada | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Coincide con cualquier archivo local cuya ruta de acceso comience por `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Coincide con cualquier dirección URL que usa `http` el esquema y está en el host `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Coincide con cualquier dirección URL que empiece `http://mail.google.com` por o `https://mail.google.com` . | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Coincide con cualquier dirección URL que use un esquema permitido. \(Vea el principio de esta sección para ver la lista de esquemas permitidos.\) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

Estos son algunos ejemplos de `_invalid_` coincidencias de patrones:

| Patrón malo | Por qué es malo |  
|:--- |:--- |  
| `http://www.foo.com` | No `_path_` |  
| `http://*foo/bar` | ' `*` ' en el host puede seguirse solo por un ' ' o ' ' `.` `/` ' |  
| `http://foo.*.bar/baz` | Si ' `*` ' está en , debe ser el primer `_host_` carácter |  
| `http:/bar` | Falta `_scheme_` el separador \(' `/` ' debe ser " `//` "\) |  
| `foo://*` | No válido `_scheme_` |  

Algunos esquemas no se admiten en todos los contextos.

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí.](https://developer.chrome.com/extensions/match_patterns)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
