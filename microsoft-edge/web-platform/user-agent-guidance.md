---
description: En este artículo se describe cómo detectar Microsoft Edge datos con sugerencias de cliente de agente de usuario y la cadena de agente de usuario
title: Detectar Microsoft Edge desde su sitio web
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibility, web platform, user-agent string, ua string, ua overrides, user-agent client hints, user agent client hints, user agent client hints, ua client hints, ua ch, feature detection, browser identification, browser detection, header, https header, verify chromium, detect microsoft edge, detecting microsoft edge
ms.openlocfilehash: 39a01ebc10b48a8214b09096974a3864dcb06e572a119ec6af6b975c1657f6dd
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11798221"
---
# <a name="detecting-microsoft-edge-from-your-website"></a>Detectar Microsoft Edge desde su sitio web

Los exploradores proporcionan mecanismos para que los sitios web detecten información del explorador, como marca, número de versión y sistema operativo host. Las [cadenas de agente de](#user-agent-strings) usuario heredadas están obsoletas y tienen un historial de problemas de compatibilidad de sitios web. Las nuevas [sugerencias de cliente de agente de usuario](#user-agent-client-hints) son un mecanismo mejorado para recuperar información del explorador.

Es posible que desee proporcionar experiencias diferentes a los usuarios en función de su explorador. Por ejemplo, si incluye pasos sobre cómo configurar Microsoft Edge u otro explorador para su uso con el sitio, es posible que desee detectar el explorador y, a continuación, mostrar el contenido adecuado.

Mecanismos para la detección del explorador:

| Mecanismo | Servidor | Lado cliente |  
|:--- |:--- |:--- | 
| **Sugerencias de cliente de** agente de usuario \(recommended\) | `Sec-CH-UA` Encabezado HTTPS | `navigator.userAgentData` Método JavaScript |  
| **Cadena de agente de usuario** \(legacy\) | `User-Agent` Encabezado HTTPS | `navigator.userAgent` Método JavaScript |  

En este artículo se describen los métodos Microsoft Edge para recuperar información del agente de usuario.

## <a name="feature-detection"></a>Detección de características

Microsoft recomienda [detectar si se admite una característica][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] en el explorador siempre que sea posible en lugar de detectar el explorador.

Si debe detectar exploradores, Microsoft recomienda usar sugerencias de cliente de la siguiente manera.

## <a name="user-agent-client-hints"></a>User-Agent sugerencias de cliente

Microsoft Edge admite User-Agent sugerencias de cliente a partir de la versión 90.

User-Agent sugerencias de cliente es una forma más limpia y que preserva la privacidad para obtener acceso a la información del explorador, como el nombre del explorador, el número de versión, la plataforma y mucho más. Pronto, varios exploradores inmovilizarán y desusarán la cadena de User-Agent de datos. Por ejemplo, el sitio Estado de la plataforma Chrome describe el cambio en [Característica: Reducir User-Agent información de cadena .][ReduceUserAgentStringInformation]

Emplee User-Agent sugerencias de cliente cuando desee:
- Determine si la nueva actividad del explorador es del usuario esperado.
- Personalice sugerencias o instrucciones si el usuario es nuevo en este sitio.

No use User-Agent sugerencias de cliente para:
- Bloquear *exploradores no* compatibles.
- Restringir el acceso a las características del sitio.

Para obtener más información, vaya a la especificación en [W3C Community Draft Report | User-Agent Client Hints][W3CCommunityDraftReportUserAgentClientHints].


### <a name="user-agent-client-hints-https-header"></a>User-Agent encabezado HTTPS sugerencias de cliente

Cuando Microsoft Edge una solicitud HTTPS a un servidor, envía un conjunto de encabezados de sugerencias de cliente User-Agent baja entropía. Para obtener más información, vaya [a Tabla de sugerencias de entropía baja][LowEntropyHintTable]. Si el servidor requiere información más detallada sobre el explorador, su respuesta incluye un `Accept-CH` encabezado. El valor de ese encabezado de respuesta es una lista separada por comas de todos los encabezados de solicitud sugerencias de cliente que el servidor desea del explorador, como `Accept-CH: Sec-CH-UA-Full-Version,Sec-CH-UA-Platform-Version` . La siguiente Microsoft Edge solicitud HTTPS al servidor incluirá los encabezados User-Agent sugerencias de cliente especificados.

De forma predeterminada, Microsoft Edge los encabezados `Sec-CH-UA` , y request en el siguiente `Sec-CH-UA-Mobile` `Sec-CH-UA-Platform` formato.  

```https
Sec-CH-UA: "Chromium";v="92", "Microsoft Edge";v="92","Placeholder;Browser Brand";v="99"
Sec-CH-UA-Mobile: ?0
Sec-CH-UA-Platform: "Windows"
```  

En la tabla siguiente se muestran todos los encabezados de solicitud de sugerencias disponibles con valores de ejemplo.

| User-Agent encabezado de solicitud | Ejemplo User-Agent de respuesta |  
|:--- |:--- |  
| `Sec-CH-UA` | `"Chromium";v="91", "Microsoft Edge";v="91","GREASE";v="99"` |  
| `Sec-CH-UA-Mobile` | `?0` |  
| `Sec-CH-UA-Full-Version` | `91.0.866.0` |  
| `Sec-CH-UA-Platform` | `Windows` |  
| `Sec-CH-UA-Platform-Version` | `10.0` |  
| `Sec-CH-UA-Arch` | `x86` | 
| `Sec-CH-UA-Bitness` | `64` |
| `Sec-CH-UA-Model` | `Surface Pro` |  

> [!NOTE]
> User-Agent sugerencias de cliente solo se envían a través de conexiones seguras mediante `HTTPS` .

### <a name="user-agent-client-hints-javascript-api"></a>User-Agent API de JavaScript de sugerencias de cliente  

Puede obtener acceso a User-Agent sugerencias de cliente mediante JavaScript en el lado cliente. Cuando se llama al valor `navigator.userAgentData` predeterminado, devuelve la siguiente respuesta.  

```JSON
{ brands: [ {brand: "Chromium","version":"91"}, {brand: "Microsoft Edge","version":"91"}, {brand: "GREASE","version":"99"}, ]
mobile: false }
```  

Microsoft Edge incluye un valor `GREASE` de marca que cambia con el tiempo. Impide que los sitios coincidan con toda la lista de marcas al intentar detectar una versión de Microsoft Edge.

Para solicitar información más detallada, como `platform` , use el siguiente código.

El siguiente fragmento de código envía una solicitud.

```javascript
navigator.userAgentData.getHighEntropyValues(
   ["architecture", "model", "platform", "platformVersion", "uaFullVersion"])
      .then(ua => { console.log(ua) });
``` 

Para recibir la siguiente respuesta.  

```javascript
{architecture: "x86", 
   model: "", 
   platform: "Windows", 
   platformVersion: "10.0", 
   uaFullVersion: "92.0.866.0"}
```  

Para obtener más información, vaya [a getHighEntropyValues()][GithubWicgUaClientHintsGethighentropyvalues].

### <a name="user-agent-client-hints-suggested-use"></a>User-Agent sugerencias de cliente sugeridas

La combinación User-Agent sugerencias de cliente con la [detección de características][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] es una forma eficaz de ofrecer contenido web compatible. Microsoft recomienda usar este patrón para:
* Mejorar la capacidad de mantenimiento del código.
* Reducir la fragilidad del código.  
* Reduzca la interrupción del código a partir de los cambios realizados en User-Agent string.

Si necesitas buscar un explorador como Chrome, Microsoft recomienda detectar , que es el motor que potencia `Chromium` Microsoft Edge.

Use este método para comprobar la marca y aplicar la detección a todos los `Chromium` exploradores Chromium basados en la marca.

```javascript
function isChromium() {
    for (brand_version_pair in navigator.userAgentData.brands) {
        if (brand_version_pair.brand == "Chromium"){
            return true;
        }
    }
    return false;
}
```

Use el método anterior para evitar comprobaciones de codificación rígida de marcas en índices específicos. Mostrar pedidos de nombres de marca puede cambiar con el tiempo. 

Si no puede usar la [detección de][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]características, no use una lista codificada de exploradores conocidos Chromium basados en características para la comprobación. Algunos ejemplos de nombres de explorador codificados de forma rígida `Microsoft Edge` incluyen y `Google Chrome` . [Es posible que][MdnLearnToolsTestingCrossBrowserTestingFeatureDetection] la detección de características no esté disponible porque se debe evitar una corrección de un error Chromium en versiones posteriores y los exploradores afectados son difíciles de detectar.

## <a name="user-agent-strings"></a>User-Agent cadenas

User-Agent las cadenas están obsoletas y tienen un largo historial de problemas de compatibilidad de sitios web.

Siempre que sea posible, Microsoft recomienda minimizar el uso de Microsoft Edge lógica de detección de explorador basada en la User-Agent string. Si tiene una buena razón para detectar el explorador, el equipo de Microsoft Edge recomienda usar [sugerencias](#user-agent-client-hints) de cliente de agente de usuario como lógica de detección principal. [Las sugerencias de cliente](#user-agent-client-hints) de agente de usuario también reducen la complejidad del código de detección del explorador.

Para la referencia heredada, se usó el siguiente formato para User-Agent cadena.  

En Windows, el `User-Agent` encabezado de solicitud HTTP usa el siguiente formato.

```https
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36 Edg/90.0.818.46
```  

En Android, el `User-Agent` encabezado de solicitud HTTP usa el siguiente formato.

```https
User-Agent: Mozilla/5.0 (Linux; Android 6.0; Nexus 5 Build/MRA58N) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Mobile Safari/537.36 Edg/90.0.818.46
```    

El valor de respuesta del `navigator.userAgent` método usa el siguiente formato.  

```javascript
"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4501.0 Safari/537.36 Edg/91.0.866.0"
```  

Los identificadores de plataforma cambian en función del sistema operativo y los números de versión se incrementan con el tiempo. El formato es el mismo que el Chromium usuario con la adición de un `Edg` nuevo token al final. Microsoft eligió el token para evitar problemas de compatibilidad causados por la cadena, que anteriormente se usaba para el explorador Microsoft Edge basado `Edg` `Edge` en EdgeHTML. El `Edg` token también es coherente con los tokens [existentes][WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper] usados para iOS y Android.

## <a name="map-the-user-agent-string-to-browser-name"></a>Asignar la cadena User-Agent al nombre del explorador  

Asigne los tokens de cadena de agente de usuario a nombres de explorador legibles para usarlos en el código. Esta práctica es común en toda la web. Al asignar el nuevo token a un nombre de explorador, Microsoft recomienda usar un nombre diferente al que se usa para el explorador Microsoft EdgeHTML heredado para evitar aplicar accidentalmente soluciones alternativas heredadas que no se aplican a exploradores basados en `Edg` Chromium.

## <a name="user-agent-overrides"></a>User-Agent invalidaciones  

A veces, un sitio web no reconoce el nuevo Microsoft Edge de usuario. Como resultado, es posible que un conjunto de características del sitio web no funcione correctamente. Cuando se notifica a Microsoft sobre los tipos de problemas, Microsoft se pone en contacto con usted \(propietario de un sitio web\) e informa sobre el agente de usuario actualizado.

Es posible que necesite más tiempo para actualizar y probar la lógica de detección de agentes de usuario de su sitio web para solucionar los problemas notificados por Microsoft. Para maximizar la compatibilidad de los usuarios, los canales Microsoft Edge Beta y Estable usan una lista de invalidaciones de agente de usuario. Use las invalidaciones del agente de usuario mientras actualiza su sitio web. Microsoft proporciona la lista de invalidaciones de agente de usuario.  

Las invalidaciones especifican nuevos valores de agente de usuario que Microsoft Edge en lugar del agente de usuario predeterminado para sitios web específicos. Para mostrar la lista de invalidaciones de agente de usuario que se aplican actualmente, complete las siguientes acciones.  

1. Abra el Microsoft Edge Beta o el canal estable.  
1. Vaya a `edge://compat/useragent`.  

Los Microsoft Edge canary y dev no reciben actualmente invalidaciones de agente de usuario. Los Microsoft Edge Canary y Dev proporcionan entornos que usan el agente Microsoft Edge usuario predeterminado. Use los Microsoft Edge Canary y Dev para reproducir problemas en su sitio web causados por el agente de usuario Microsoft Edge usuario predeterminado. Para desactivar las invalidaciones de agente de usuario en los canales Microsoft Edge Beta o Estable, complete las siguientes acciones.  

1. Abre un símbolo del sistema. Por ejemplo, escriba **cmd en** el Windows de búsqueda y seleccione la aplicación **Símbolo del** sistema.
1. Copie el siguiente fragmento de código.  

    ```shell
    --disable-domain-action-user-agent-override
    ```  

1. Ejecute la Microsoft Edge con el fragmento de código. 

    ```shell
    {path/to/microsoft/edge.ext} --disable-domain-action-user-agent-override
    ```  

<!-- links -->  

[WindowsBlogsMsedgedev20171005MicrosoftEdgeIosAndroidDeveloper]: https://blogs.windows.com/msedgedev/2017/10/05/microsoft-edge-ios-android-developer "Microsoft Edge para iOS y Android: lo que los desarrolladores necesitan saber | Blogs Windows Microsoft"  

[GithubWicgUaClientHintsGethighentropyvalues]: https://wicg.github.io/ua-client-hints#getHighEntropyValues "4.1.5. método getHighEntropyValues: User-Agent sugerencias de cliente | GitHub"  

[MdnLearnToolsTestingCrossBrowserTestingFeatureDetection]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing/Feature_detection "Implementación de la detección de características | MDN" 

[ReduceUserAgentStringInformation]: https://www.chromestatus.com/feature/5704553745874944 "Característica: Reducir la información de cadena del agente de usuario"

[W3CCommunityDraftReportUserAgentClientHints]: https://wicg.github.io/ua-client-hints/ "W3C Community borrador de informe | User-Agent sugerencias de cliente"

[LowEntropyHintTable]: https://wicg.github.io/client-hints-infrastructure/#low-entropy-table "Tabla de sugerencias de entropía baja"