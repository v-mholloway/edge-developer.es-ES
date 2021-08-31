---
description: Obtenga información sobre las actualizaciones automáticas de extensiones en Microsoft Edge
title: Actualizar automáticamente las extensiones en Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: edge-chromium, desarrollo de extensiones, extensiones del explorador, complementos, centro de partners, desarrollador
ms.openlocfilehash: 726414c68dabc15e765d55254e91682f6ced9f1d
ms.sourcegitcommit: dc445eae30234af1ad3fa42645aabb940529912b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2021
ms.locfileid: "11934441"
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
# <a name="automatically-update-extensions-in-microsoft-edge"></a>Actualizar automáticamente las extensiones en Microsoft Edge  

Al establecer la extensión para que se actualice automáticamente, la extensión comparte las siguientes ventajas con Microsoft Edge cuando se establece en actualización automática.  

*   Incorporar correcciones de errores y seguridad.  
*   Agregue nuevas características o mejoras de rendimiento.  
*   Mejorar la interfaz de usuario.  

Anteriormente, se admiten extensiones no basadas en almacén.  Además, actualizó los archivos binarios nativos y la extensión al mismo tiempo.  

Ahora, el Microsoft Edge de complementos hospeda las extensiones y actualiza la extensión con el mismo mecanismo que Microsoft Edge.  No controla el mecanismo de actualización.  Tenga cuidado al actualizar las extensiones que tienen una dependencia de los archivos binarios nativos.  

> [!NOTE]
> Este artículo no se aplica a las extensiones que publique con el panel [del Centro de][MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd] partners.  Puede usar el panel para publicar versiones actualizadas para los usuarios y para el sitio Microsoft Edge de complementos.  Para obtener más información, vaya [a Actualizar una Microsoft Edge extensión][ExtensionsPublishUpdateExtension].  

## <a name="overview"></a>Introducción  

Cada pocas horas, Microsoft Edge comprueba si cada extensión o aplicación instalada tiene una dirección URL de actualización.  Para especificar una dirección URL de actualización para la extensión, use el `update_url` campo del manifiesto.  El `update_url` campo del manifiesto apunta a una ubicación para completar una comprobación de actualización.  Para cada `update_url` uno, envía solicitudes de archivos XML de manifiesto actualizados.  Si el archivo XML del manifiesto de actualización muestra una versión más reciente que la instalada, Microsoft Edge descarga e instala la versión más reciente.  El mismo proceso funciona para las actualizaciones manuales, donde el nuevo archivo debe firmarse con la misma `.crx` clave privada que la versión instalada actualmente.  

> [!NOTE]
> Para mantener la privacidad del usuario, Microsoft Edge no envía ningún encabezado con solicitudes de manifiesto de actualización automática y omite los encabezados de las respuestas a `Cookie` `Set-Cookie` dichas solicitudes.  

## <a name="update-url"></a>Dirección URL de actualización  

Si hospedas tu propia extensión o aplicación, debes agregar el `update_url` campo al `manifest.json` archivo.  Revise el siguiente fragmento de código para ver un ejemplo de `update_url` .  

```json
{
  "name": "My extension",
  ... 
  "update_url": "http://contoso.com/mytestextension/updates.xml",
  ... 
}
```  

## <a name="update-manifest"></a>Manifiesto de actualización  

El manifiesto actualizado devuelto por el servidor debe ser un documento XML.  Revise el siguiente fragmento de código para ver un ejemplo del archivo XML de manifiesto actualizado.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' />
  </app>
</gupdate>
```  

En la tabla siguiente se describen los atributos del archivo XML de manifiesto actualizado.  

| Atributo | Detalles | 
|:--- |:--- |  
| `appid` | El identificador de extensión se genera en función de un hash de la clave pública.  Para buscar el identificador de una extensión, abra Microsoft Edge y vaya a `edge://extensions` . |  
| `codebase` | Dirección URL del `.crx` archivo. |  
| `version` | Este valor de atributo lo usa Microsoft Edge para determinar si debe descargar el `.crx` archivo especificado por `codebase` .  Debe coincidir con el valor del `version` archivo `manifest.json` del `.crx` archivo. |  

El archivo XML del manifiesto de actualización puede contener información sobre varias extensiones al incluir varios elementos.  

## <a name="testing"></a>Pruebas  

La frecuencia de comprobación de actualización predeterminada es de varias horas.  Para forzar una actualización, vaya a `edge://extensions` y elija el botón Actualizar extensiones **ahora.**  

## <a name="advanced-usage-request-parameters"></a>Uso avanzado: parámetros de solicitud  

El mecanismo básico es simple.  Para actualizar automáticamente la extensión:

1.  Upload el archivo XML estático en el servidor web, como Apache.  
1.  Actualice el archivo XML a medida que libere nuevas versiones de las extensiones.  
    
Aproveche el hecho de que algunos parámetros agregados a la solicitud de manifiesto de actualización indican la extensión `ID` y `version` .  Puede usar lo mismo `update URL` para todas las extensiones en lugar de un archivo XML estático.  Para usar lo mismo para todas las extensiones, señale a una dirección URL que ejecute código dinámico del lado servidor `update URL` para probar los parámetros.  

En el ejemplo siguiente se muestra el formato de los parámetros de solicitud de la dirección URL de actualización.  

```url
?x={extension_data}
```  

En este ejemplo, `{extension_data}` es una cadena codificada en dirección URL que usa el siguiente formato.  

```url
id={id}&v={version}
```  

Por ejemplo, las dos extensiones siguientes apuntan a la misma dirección URL de `http://contoso.com/extension_updates.php` actualización.  

*   Extensión 1  
    *   Identificador: `aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa`  
    *   dirección URL de actualización: `http://contoso.com/extension_updates.php`
    *   Versión: `1.1`  
*   Extensión 2  
    *   Identificador: `bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb`  
    *   dirección URL de actualización: `http://contoso.com/extension_updates.php`
    *   Versión: `0.4`  


Las siguientes son las solicitudes para actualizar cada extensión.  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1
```  

```https
http://contoso.com/extension_updates.php?x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

También puede enumerar varias extensiones en una sola solicitud para cada dirección URL de actualización única.  En el ejemplo siguiente se combinan las solicitudes anteriores en una sola solicitud.  

```https
http://contoso.com/extension_updates.php?x=id%3Daaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa%26v%3D1.1&x=id%3Dbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb%26v%3D0.4
```  

Si envía una sola solicitud y el número de extensiones instaladas que usan la misma dirección URL de actualización es demasiado largo, la comprobación de actualización emite más `GET` solicitudes.  Una `GET` dirección URL de solicitud es demasiado larga si tiene aproximadamente 2000 caracteres.  

> [!NOTE]
> En el futuro, una sola `POST` solicitud puede reemplazar varias `GET` solicitudes.  La `POST` solicitud puede contener los parámetros de solicitud en el `POST` cuerpo.  

## <a name="advanced-usage-minimum-browser-version"></a>Uso avanzado: versión mínima del explorador  

Como nueva versión de las API para el sistema de extensiones de Microsoft Edge, puedes liberar una versión actualizada de la extensión o aplicación que solo funciona con versiones Microsoft Edge más recientes.  Cuando Microsoft Edge se actualiza automáticamente, puede tardar unos días antes de que la mayoría de los usuarios se actualicen a esa nueva versión.  

Para asegurarse de que una actualización específica solo se aplica a Microsoft Edge versiones actuales o más recientes que una versión específica, agregue el atributo en `prodversionmin` el manifiesto de actualización.  En el siguiente fragmento de código, el valor de atributo de especifica que la aplicación se actualizó automáticamente a la versión solo cuando el usuario ejecuta Microsoft Edge `prodversionmin` `3.0.193.0` o `2.0` `3.0.193.0` posterior.  

```xml
<?xml version='1.0' encoding='UTF-8'?>
<gupdate xmlns='http://www.google.com/update2/response' protocol='2.0'>
  <app appid='aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa'>
    <updatecheck codebase='http://contoso.com/mytestextension/mte_v2.crx' version='2.0' prodversionmin='3.0.193.0' />
  </app>
</gupdate>
```  

<!-- links -->  
[ExtensionsPublishUpdateExtension]: ../publish/update-extension.md "Actualizar una Microsoft Edge de | Microsoft Docs"  

[MicrosoftPartnerDashboardMicrosoftedgePublicLoginRefDd]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Centro de partners"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí.](https://developer.chrome.com/docs/apps/autoupdate)  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
