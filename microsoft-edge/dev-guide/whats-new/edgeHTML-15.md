---
description: Esta guía proporciona una descripción general de las características y los estándares para desarrolladores incluidos en EdgeHTML 15.
title: Novedades de EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.custom: seodec18
ms.openlocfilehash: e750a9272bb8bcdb51662839a31cc303c4064ef9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572986"
---
# Novedades de EdgeHTML 15
Estos son los cambios que se incluyen en la versión actual de la plataforma Microsoft Edge, a partir de [Windows 10 Creators Update](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (04/2017, compilación 15063). Para obtener información general sobre los cambios en el explorador general de Microsoft Edge, consulte [novedades de Microsoft Edge en Windows 10 Creators Update](https://blogs.windows.com/msedgedev/2017/04/11/introducing-edgehtml-15/#DrVEvmPU6TPq3tMK.97)

Para obtener información sobre los cambios en versiones posteriores de Windows Insider Preview, vea [novedades de EdgeHTML](../whats-new.md).

Este es el vínculo permanente de la siguiente lista de cambios: **[https://aka.ms/devguide_edgehtml_15](https://aka.ms/devguide_edgehtml_15)** .

## Nuevas características

### Propiedades personalizadas de CSS
Microsoft Edge ahora es compatible con [las propiedades personalizadas CSS](https://drafts.csswg.org/css-variables/), a. k. a variables de CSS. Las variables CSS permiten crear propiedades CSS personalizadas que se pueden volver a usar en las hojas de estilo para ayudar a reducir la cantidad de datos duplicados, como los colores repetidos. El uso de variables CSS es simple:

```css
/* define a custom property by using two dashes and assign it a value */
body {   
   --default-color: #3390b1
}

/* reference it in your stylesheet with the "var()" function */
h1 {
   color: var(--default-color);
}
```  

### Observador de intersección
EdgeHTML 15 presenta la especificación de la [API de intersección de Observer](https://w3c.github.io/IntersectionObserver/) . La API de Intersection Observer le permite consultar de forma asincrónica la posición y visibilidad de los elementos DOM en relación con otros elementos o la ventanilla global. Esta API elimina la necesidad de códigos caros personalizados creando un método para notificar a los elementos de forma eficaz cuando están en vista.

### JavaScript

Las optimizaciones de rendimiento llevan la fase central con el EdgeHTML 15 Rev del motor de JavaScript de Chakra. Con Windows 10 Creators Update, Chakra ahorra memoria reduciendo las funciones y optimizando los argumentos del montón y mejora el rendimiento del código minified.

Además, EdgeHTML 15 presenta las siguientes vistas previas de características:

#### Características experimentales de JavaScript (habilitado con *About: flags*)

* [Webassembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) ([demostración](https://webassembly.org/demo/))
* [Memoria compartida y atómicas](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

Para obtener más información, consulta el [*rendimiento, el ensamblado Webassembly y la memoria compartida de JavaScript mejorados en Microsoft Edge*](https://blogs.windows.com/msedgedev/2017/04/20/improved-javascript-performance-webassembly-shared-memory/#t4gwUKjjtdmstMbs.97) .

### API de solicitud de pago
Ahora se admite la [API de solicitud de pago](https://w3.org/TR/payment-request/) , lo que permite una desprotección y pagos más sencillos en la web en equipos y teléfonos con Windows 10. Esta API permite que Microsoft Edge actúe como intermediario entre comerciantes, consumidores y las formas de pago (por ejemplo, tarjetas de crédito) que los consumidores han almacenado en la nube. Para obtener más información sobre la API de solicitud de pago, consulta [pagos Web más sencillos: Presentamos la API de solicitud](https://blogs.windows.com/msedgedev/2016/12/15/payment-request-api-edge/) de pago y la guía para desarrolladores de la [API de solicitud de pago](/microsoft-edge/dev-guide/device/payment-request-api) .

### TCP Fast Open (TFO)
TCP Fast Open es una característica que reduce el número de viajes de ida y vuelta necesarios para abrir una conexión TCP, lo que mejora el rendimiento de la red del explorador. Para obtener más información, consulte [creación de una web más rápida y segura con TCP Fast Open](https://blogs.windows.com/msedgedev/2016/06/15/building-a-faster-and-more-secure-web-with-tcp-fast-open-tls-false-start-and-tls-1-3/#eQMauReErmIRXYqh.97). Debido a diferencias de interoperabilidad en varias topologías de red, esta característica no está habilitada de forma predeterminada en Microsoft Edge. Para habilitarlo, escriba `about:flags` la barra de direcciones y seleccione la casilla **Habilitar TCP Fast Open** en la sección *redes* . 

### WebRTC e interoperabilidad compatible con códecs de vídeo de RTC

EdgeHTML 15 es compatible con un subconjunto de la API de WebRTC 1,0 para la interoperabilidad con aplicaciones creadas con versiones anteriores de la API W3C WebRTC-PC, que incluye 2015. Para obtener más información, consulta la referencia de la [API de WebRTC](https://msdn.microsoft.com/library/mt806139(v=vs.85).aspx) .

Para aprovechar las características más avanzadas de la comunicación de audio y vídeo de punto a punto, recomendamos usar la [API de comunicación en tiempo real](../realtime-communication/object-rtc-api.md). La API de ORTC es más adecuada para situaciones en las que desees configurar llamadas de audio y videollamadas grupales, o para controlar directamente los objetos de transporte, remitente y receptor individual.

Microsoft Edge admite el vídeo H. 264/AVC y VP8 con ORTC y WebRTC 1,0, y ofrece las siguientes características en apoyo de ambos tipos de códec: [ABS-Send-Time](https://webrtc.org/experiments/rtp-hdrext/abs-send-time/), [GOOG-Remb](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03), [indicación de pérdida de imagen y comentarios genéricos de Nack](https://tools.ietf.org/html/rfc4585), [retransmisión de RTP](https://tools.ietf.org/html/rfc4588).

Para obtener más información, consulta [Introducción a WebRTC 1,0 y comunicaciones interoperables en tiempo real en Microsoft Edge](https://blogs.windows.com/msedgedev/2017/01/31/introducing-webrtc-microsoft-edge/#k8XMeWKyZDQDPYR4.97).

### WebVR

Microsoft Edge ahora tiene compatibilidad con [WebVR](https://immersive-web.github.io/webxr/), una API experimental que conecta las pantallas montadas de Windows Mixed Reality y Microsoft Edge. Esta conexión permite que el contenido de VR se pueda experimentar en un sitio web, lo que significa que las experiencias de VR envolventes ya no se limitan a las aplicaciones de escritorio.  

La realidad virtual de Microsoft Edge es powered by WebGL, una API de JavaScript para representar gráficos 3D y 2D. Las aplicaciones de WebGL y las aplicaciones creadas con bibliotecas de WebGL como BabylonJS son compatibles. Una vez conectado, WebVR envía objetos visuales que corresponden a la posición y la información del sensor en los auriculares con micrófono. La API de WebVR también admite controladores espaciales gracias a una extensión de la [API del controlador para juegos](../dom/gamepad-api.md). Esta API está activada de forma predeterminada, por lo que no es necesario activar una marca.

Consulta la referencia de la [API de WebVR](https://msdn.microsoft.com/library/mt806281(v=vs.85).aspx) y la referencia de la [API de controlador](https://msdn.microsoft.com/library/dn743630(v=vs.85).aspx) para obtener más información.

 > [!NOTE] 
 > Puesto que la especificación de WebVR aún está en desarrollo, la implementación de Microsoft Edge puede cambiar más adelante en la línea.



## Características actualizadas

### Directiva de seguridad de contenido (nivel 2)
Los sitios que ya usan CSP 1 deberían seguir funcionando con el soporte técnico de Microsoft Edge para CSP 2, pero es mejor cambiar cualquier directiva `frame-src` que cargue scripts de trabajo a la nueva `child-src` Directiva para mejorar el sitio en el futuro. (En el CSP 3, ya `frame-src` no se aplicará a los trabajadores). CSP 2 también agrega lo siguiente:

1. Nuevas directivas: `base-uri` , `child-src` , `form-action` , `frame-ancestors` y `plugin-types` . Para obtener más información, consulta las [directivas de CSP compatibles con Microsoft Edge](../security/content-security-policy.md) .

2. Soporte técnico para trabajadores: los scripts de trabajo en segundo plano se rigen por su propia Directiva, aparte de la Directiva del documento que los carga. Al igual que con los documentos host, puede establecer el CSP para un trabajador en el encabezado de respuesta. Otra novedad en el CSP 2 es `allow-scripts` que `allow-same-origin` los indicadores de la `sandbox` Directiva afectan ahora a la creación de subprocesos de trabajo.

3. Secuencias de comandos y estilos en línea: CSP 2 permite la ejecución de scripts y bloques de estilos en línea proporcionando nonces y hash como mecanismo de lista blanca. Nonces son valores base aleatorios de 64 que se generan en cada carga de página que aparece en la Directiva de CSP y en las etiquetas de script de la página. Cuando la página se genera dinámicamente durante la carga, el servidor genera un valor nonce, la inserta en la NonceToken de la página y también la declara en el encabezado HTTP de la Directiva de seguridad de contenido. Los valores hash son valores estáticos generados (a través de algoritmos *SHA256*, *SHA384* o *SHA512* ) del contenido de un `<script>` `<style>` elemento o que se especifican (mediante `script-src` `style-src` directivas) en la Directiva CSP.

4. Informe de infracción de CSP: un nuevo evento, SecurityPolicyViolationEvent se desencadena ahora A través de infracciones de CSP. El mecanismo anterior para los informes de CSP, `report-uri` sigue siendo compatible. Se han agregado varios campos nuevos a los informes de violación comunes a ambos, incluyendo `effectiveDirective` (la Directiva que se ha infringido), `statusCode` (el código de respuesta HTTP), `sourceFile` (la dirección URL del recurso infractor), `lineNumber` y `columnNumber` .

### Autenticación Web
La compatibilidad de Microsoft Edge para la [API de autenticación Web](../device/web-authentication.md) emergente con [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometría se ha actualizado con los siguientes cambios:
- La implementación inicial de la API experimental de autenticación Web introducida en [EdgeHTML 14](https://blogs.windows.com/msedgedev/2016/08/04/introducing-edgehtml-14/#TVSCzKDkG4jCI5mt.97) (actualización de aniversario de Windows 10, compilación 10240, 7/2016) se expuso a través de las API prefijadas por MS (la interfaz de [MSCredentials](https://msdn.microsoft.com/library/mt697639) ). Aunque estas API siguen estando disponibles en el EdgeHTML 15, ahora se han dejado de utilizar en favor de las API y comportamientos no prefijos y basados en estándares definidos en una [instantánea más reciente](https://w3.org/TR/2016/WD-webauthn-20160928) de la especificación, y es probable que sigan cambiando a medida que la especificación madura de la estandarización.

- La implementación más reciente de Microsoft Edge está desactivada de forma predeterminada y se envía detrás de una bandera (escriba la `about:flags` barra de direcciones para activar la característica).

- Microsoft Edge aún no admite credenciales externas como SerialKeys o dispositivos Bluetooth. La API actual está limitada a las credenciales incrustadas almacenadas en el TPM. Se usa una reserva de software si el TPM no está disponible en el dispositivo.

- La cuenta de usuario de Windows actualmente conectada debe estar configurada para admitir al menos un PIN y, preferiblemente, una cara o una biometría de huellas digitales. Esto garantiza que Windows pueda autenticar el acceso al TPM.

- De las [extensiones predefinidas](https://w3.org/TR/webauthn/#extension-predef) que se describen en las especificaciones, Microsoft Edge solo admite [Fido AppID](https://w3.org/TR/webauthn/#extension-appid) ( `webauthn_txAuthSimple` ) en este momento.

- La `timeoutSeconds` opción no se evalúa actualmente

### WebDriver

EdgeHTML 15 trae una serie de actualizaciones de Webdriver, entre las que se incluyen compatibilidad con la marca de la línea de comandos silenciosa y nuevos puntos de conexión:

Método | Plantilla URI | Comando
:----- | :----------  | :--------
POST | /Session/{Session ID}/Alert/Accept | [Aceptar alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert)
POST | /Session/{Session ID}/Alert/Dismiss | [Descartar alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert)
GET | /Session/{Session ID}/Alert/Text | [Obtener texto de alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text)
POST | /Session/{Session ID}/Alert/Text | [Enviar mensaje de alerta](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text)
POST | /Session/{Session ID}/Execute/Async | [Ejecutar script asincrónico](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script)
POST | /Session/{Session ID}/Execute/Sync | [Ejecutar script](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script)
GET | /Session/{Session ID}/window | [Controlador de la ventana obtener](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle)
GET | /Session/{Session ID}/window/handles | [Obtener identificadores de ventana](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles)

Para obtener más información y el estado de otras características de Webdriver, consulte [Webdriver](../../webdriver.md).

## Nuevas API en EdgeHTML 15

Esta es la lista completa de las API nuevas de EdgeHTML 15. Se muestran en el formato **[nombre de la interfaz]. [ nombre de la API]**.

<iframe height='582' scrolling='no' title='Nuevas API de EdgeHTML15' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>Consulta las <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> nuevas API de EdgeHTML15 </a> en Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) en <a href='http://codepen.io'> CodePen </a> .</iframe>  

## Versiones anteriores de EdgeHTML
[EdgeHTML 12/Windows compilación 10240 (7/2015)](https://aka.ms/devguide_edgehtml_12)

[EdgeHTML 13/Windows compilación 10586 (11/2015)](https://aka.ms/devguide_edgehtml_13)

[EdgeHTML 14/Windows compilación 14393 (8/2016)](https://aka.ms/devguide_edgehtml_14)
