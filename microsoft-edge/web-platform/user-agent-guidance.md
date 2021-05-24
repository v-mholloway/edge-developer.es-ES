---
description: En este artículo se proporciona documentación sobre las sugerencias Microsoft Edge cliente del agente de usuario y la cadena de agente de usuario
title: Cómo detectar Microsoft Edge en su sitio web
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
# <a name="how-to-detect-microsoft-edge-in-your-website"></a>Cómo detectar Microsoft Edge en su sitio web  

Los exploradores proporcionan mecanismos para que los sitios web detecten información del explorador, como la marca y el número de versión.  Los mecanismos también detectan otras características del dispositivo, como el sistema operativo host.  Dos de estos mecanismos admitidos en Microsoft Edge [son sugerencias](#user-agent-client-hints) de cliente de agente de usuario y [cadenas de agente de usuario.](#user-agent-string)  Después de décadas de uso, User-Agent cadenas de caracteres están obsoletas y tienen un largo historial como causa de problemas de compatibilidad de sitios web.  En su lugar, el Microsoft Edge recomienda usar un mecanismo mejorado para recuperar información del explorador denominada [Sugerencias](#user-agent-client-hints)de cliente de agente de usuario .  En este artículo se describen los dos mecanismos Microsoft Edge para recuperar la información del agente de usuario.  

|  | Servidor | Lado cliente |  
|:--- |:--- |:--- | 
| **Sugerencias de cliente de** agente de usuario \(recommended\) | `Sec-CH-UA` Encabezado HTTPS | `navigator.userAgentData` Método JavaScript |  
| **Cadena de agente de usuario** \(legacy\) | `User-Agent` Encabezado HTTPS | `navigator.userAgent` Método JavaScript |  

Microsoft recomienda usar la detección [de características][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] siempre que sea posible por los siguientes motivos.  

*   Mejorar la capacidad de mantenimiento del código.  
*   Reducir la fragilidad del código.  
*   Reduzca la interrupción del código de los cambios realizados en la User-Agent cadena.  
    
Cuando [la detección][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] de características no es aplicable y debe usar la detección de agentes de usuario, use el siguiente formato para detectar Microsoft Edge de usuario en Windows y Android.  

## <a name="user-agent-client-hints"></a>User-Agent sugerencias de cliente  

A partir Microsoft Edge versión 90, accede a la información del explorador de una forma más limpia y que preserve la privacidad.  

### <a name="user-agent-client-hints-https-header"></a>User-Agent encabezado HTTPS sugerencias de cliente  

De forma predeterminada, Chromium exploradores incluidos Microsoft Edge el encabezado `Accept-CH-UA` de respuesta en el siguiente formato.  

```https
Sec-CH-UA: "Chromium";v="91", "Microsoft Edge";v="91","Dummy;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
```  

> [!NOTE]
> Las sugerencias de cliente solo se envían a través de conexiones seguras mediante `HTTPS` .  

Las siguientes sugerencias de entropía baja se envían de forma predeterminada.  Si necesita obtener más información, envíe uno de los siguientes encabezados de solicitud.  

#### <a name="user-agent-request-and-response-headers"></a>User-Agent de solicitud y respuesta  

| Encabezado de la solicitud | Valor de respuesta de ejemplo |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `false` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` |  
| `Sec-CH-UA-Model` |  |  

### <a name="user-agent-client-hints-javascript-api"></a>User-Agent API de JavaScript de sugerencias de cliente  

El valor de respuesta predeterminado de `navigator.userAgentData` usa el siguiente formato.  

```javascript
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

Si necesita obtener acceso a información más detallada, use el [método getHighEntropyValues().][GithubWicgUaClientHintsGethighentropyvalues]  

:::row:::
   :::column span="":::
      El siguiente fragmento de código envía una solicitud.  
   :::column-end:::
   :::column span="":::
      Para recibir la siguiente respuesta.  
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

## <a name="recommended-uses-of-user-agent-client-hints"></a>Usos recomendados de User-Agent sugerencias de cliente  

El conjunto de marcas y el orden de presentación asociado cambian con el tiempo, por lo que nunca debes codificar los índices en la matriz de marcas devueltas.  Para garantizar que detecte problemas similares en su sitio web antes de tiempo, el explorador incluye un valor de marca que cambia con el tiempo y tiene formato para interrumpirse debido a problemas comunes de análisis de `GREASE` cadenas.  

Si no puedes usar la detección de [características,][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]no uses una lista codificada de exploradores Chromium para la comprobación.  Algunos ejemplos de nombres de explorador codificados de forma rígida `Microsoft Edge` incluyen y `Google Chrome` .  Las razones [por las que la][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] detección de características no es aplicable pueden incluir la siguiente situación.  

*   Se debe evitar una corrección de un error Chromium en una versión posterior y los exploradores afectados son difíciles de detectar fuera de una comprobación de la marca y la versión.  
    
En su lugar, debe comprobar la marca, lo que garantiza que la detección se aplique a todos los `Chromium` exploradores Chromium basados en la marca.  


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

## <a name="user-agent-string"></a>Cadena de agente de usuario  

Siempre que sea posible, Microsoft recomienda minimizar el uso de Microsoft Edge lógica de detección de explorador basada en la cadena de agente de usuario.  Si tiene una buena razón para detectar el agente de usuario, el equipo de Microsoft Edge recomienda usar [sugerencias](#user-agent-client-hints) de cliente de agente de usuario como lógica de detección principal.  [Las sugerencias de cliente de](#user-agent-client-hints) agente de usuario también reducen el número necesario de cadenas analizadas.  Sin embargo, para la referencia heredada, se usa el siguiente formato para la cadena User-Agent.  

:::row:::
   :::column span="":::
      En Windows, el `User-Agent` encabezado de solicitud HTTP usa el siguiente formato.  
   :::column-end:::
   :::column span="":::
      En Android, el `User-Agent` encabezado de solicitud HTTP usa el siguiente formato.  
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

El valor de respuesta del `navigator.userAgent` método usa el siguiente formato.  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

Los identificadores de plataforma cambian en función del sistema operativo usado y los números de versión también aumentan a medida que pasa el tiempo.  El formato es el mismo que el Chromium usuario con la adición de un `Edg` nuevo token al final.  Microsoft eligió el token para evitar problemas de compatibilidad causados por la cadena, que se usó Microsoft Edge explorador basado `Edg` `Edge` en EdgeHTML.  El `Edg` token también es coherente con los tokens [existentes][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] usados en iOS y Android.

## <a name="map-the-user-agent-string-to-browser-name"></a>Asignar la cadena de agente de usuario al nombre del explorador  

Asigne los tokens de cadena de agente de usuario a un nombre de explorador más legible para usar en el código.  Es un patrón común en la web hoy en día.  Al asignar el nuevo token a un nombre de explorador, Microsoft recomienda usar un nombre diferente al que se usa para el explorador de Microsoft Edge heredado para evitar aplicar accidentalmente cualquier solución alternativa heredada que no sea aplicable a los exploradores basados en `Edg` Chromium.

## <a name="user-agent-overrides"></a>Invalidaciones del agente de usuario  

A veces, un sitio web no reconoce el nuevo Microsoft Edge de usuario.  Como resultado, es posible que un conjunto de características del sitio web no funcione correctamente.  Cuando se notifica a Microsoft sobre los tipos de problemas, Microsoft se pone en contacto con usted \(propietario de un sitio web\) e informa sobre el agente de usuario actualizado.  

Es posible que necesite más tiempo para actualizar y probar la lógica de detección de agentes de usuario de su sitio web para solucionar los problemas notificados por Microsoft.  Para maximizar la compatibilidad de los usuarios, los canales Microsoft Edge Beta y Estable usan una lista de invalidaciones de agente de usuario.  Use las invalidaciones del agente de usuario mientras actualiza su sitio web.  La lista de invalidaciones de agente de usuario proporcionada por Microsoft.  

Las invalidaciones especifican nuevos valores de agente de usuario que Microsoft Edge en lugar del agente de usuario predeterminado para sitios web específicos.  Para mostrar la lista de invalidaciones de agente de usuario que se aplican actualmente, complete las siguientes acciones.  

1.  Abra el Microsoft Edge Beta o el canal estable.  
1.  Vaya a `edge://compat/useragent`.  
    
Los Microsoft Edge canary y dev no reciben actualmente invalidaciones de agente de usuario.  Los Microsoft Edge Canary y Dev proporcionan entornos que usan el agente Microsoft Edge usuario predeterminado.  Use los Microsoft Edge Canary y Dev para reproducir fácilmente problemas en su sitio web causados por el agente Microsoft Edge usuario predeterminado.  Para desactivar las invalidaciones de agente de usuario en los canales Microsoft Edge Beta o Estable, complete las siguientes acciones.  

1.  Abre la aplicación de línea de comandos.  
1.  Copie y pegue el siguiente fragmento de código.  
    
    ```shell
    --disable-domain-action-user-agent-override
    ```  
    
1.  Ejecute la Microsoft Edge con el fragmento de código.  
    
    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  
    
<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge para iOS y Android: lo que los desarrolladores necesitan saber | Blogs Windows Microsoft"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. método getHighEntropyValues: User-Agent sugerencias de cliente | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Implementación de la detección de características | MDN"  
