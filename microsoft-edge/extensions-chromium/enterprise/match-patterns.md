---
description: Documentación de la Directiva de empresa para extensiones de la periferia (cromo).
title: Patrones de coincidencia
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: 'Edge: cromo, desarrollo de extensiones, extensiones de explorador, complementos, centro de Partners, desarrollador'
ms.openlocfilehash: 59427769a010ca774833a809d3025e7594634202
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015663"
---
# Patrones de coincidencia

Los permisos de host y la coincidencia de script de contenido se basan en un conjunto de direcciones URL definidas por patrones de coincidencia.  Un modelo de coincidencia es esencialmente una dirección URL que comienza con un esquema permitido ( `http` ,, `https` `file` , o `ftp` , y que puede contener `*` caracteres ' ').  El patrón especial `<all_urls>` coincide con cualquier dirección URL que comience con un esquema permitido.  Cada patrón de coincidencia tiene 3 partes:  

*   _esquema_ : por ejemplo, `http` o `file` bien `*`  

> [!NOTE]
> El acceso a las `file` direcciones URL no es automático.  El usuario debe visitar la página de administración de extensiones y participar para `file` acceder a cada extensión que la solicita.  

*   `_host_` , por ejemplo, `www.google.com` o `*.google.com` o `*` ; si el esquema es archivo, no hay elemento del host.  
*   `_path_` , por ejemplo, `/*` , `/foo*` o `/foo/bar` .  La ruta de acceso debe estar presente en un permiso de hospedaje, pero siempre se tratará como `/*` .  

La sintaxis básica:  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

El significado de `*` depende de si está en la parte de esquema, de host o de la ruta de acceso.  Si el esquema es `*` , entonces coincide con `http` o `https` , y no con `file` o `ftp` .  Si el host es solo `*` , entonces coincide con cualquier host. Si el host es `*.hostname` , entonces coincide con el host especificado o cualquiera de los subdominios.  En la sección Path, cada uno `*` coincide con 0 o más caracteres.  En la tabla siguiente se muestran algunos patrones válidos.  

| Periodic | Qué hace | Ejemplos de coincidencia de direcciones URL |  
|:--- |:--- |:--- |  
| `http://*/*` | Coincide con cualquier dirección URL que use el esquema http | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Coincide con cualquier dirección URL que use el esquema http en cualquier host, siempre y cuando la ruta empiece por `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Coincide con cualquier dirección URL que use el esquema https, está en un `google.com` host \ (como `www.google.com` , `docs.google.com` , o `google.com` \), siempre y cuando la ruta empiece por `/foo` y termine por `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Coincide con la dirección URL especificada | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Coincide con cualquier archivo local cuya ruta empiece por `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Coincide con cualquier dirección URL que use el `http` esquema y se encuentra en el host. `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Coincide con cualquier dirección URL que comience con `http://mail.google.com` o `https://mail.google.com` . | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Coincide con cualquier dirección URL que use un esquema permitido. \ (Vea el principio de esta sección para obtener la lista de esquemas permitidos. \) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

A continuación se muestran algunos ejemplos de `_invalid_` coincidencia de patrones:

| Patrón incorrecto | Por qué es malo |  
|:--- |:--- |  
| `http://www.foo.com` | No `_path_` |  
| `http://*foo/bar` | ' `*` ' en el host solo puede ir seguido de un ' `.` ' o ' `/` ' |  
| `http://foo.*.bar/baz` | Si ' `*` ' está en el `_host_` , debe ser el primer carácter |  
| `http:/bar` | Falta el `_scheme_` separador \ (' `/` ' debe ser " `//` " \) |  
| `foo://*` | No válido `_scheme_` |  

Algunos esquemas no se admiten en todos los contextos.

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].  
> La página original se encuentra [aquí](https://developer.chrome.com/extensions/match_patterns/).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
