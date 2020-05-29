---
ms.assetid: ef705c70-73f8-445b-84ed-4f83679f1980
description: Obtenga información sobre cómo las comunicaciones en tiempo real (ORTC) de objetos permiten transmitir los medios en tiempo real directamente entre exploradores Web, dispositivos móviles o servidores.
title: 'Guía de desarrollo: API de RTC de objeto'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, desarrollo web, HTML, CSS, JavaScript, desarrollador
ms.openlocfilehash: ac033ea26fa7c1eb435b0164e5dbd2a3a5428474
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572960"
---
# API de RTC de objeto

Las comunicaciones en tiempo real de objetos (ORTC) permiten que los medios (audio y/o video) se transmitan (se envíen y reciban) en tiempo real directamente entre exploradores Web, dispositivos móviles y servidores a través de API de JavaScript nativas.

> [!NOTE]
> Microsoft Edge ahora implementa ORTC para dispositivos Windows 10. Sin embargo, esta implementación difiere de la versión más reciente de la [API de ORTC](https://go.microsoft.com/fwlink/p/?LinkID=690096). ORTC ha continuado evolucionando desde el desarrollo y la publicación de Microsoft Edge, el explorador no implementa cada objeto o método dentro de la API de ORTC, e incluye las extensiones que actualmente no están incorporadas en la especificación. El desarrollo más continuará con el objetivo de permitir a los programadores de todo el mundo crear experiencias que incluyan la capacidad de hablar con usuarios de Skype y otros servicios de comunicación compatibles con WebRTC.



Para obtener una experiencia práctica con ORTC, Pruebe estas demostraciones en la prueba:
-  [SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [Llamada de teléfono ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [Demostración de ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


Para obtener más información sobre ORTC, consulte la [API de ortc ya está disponible en Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) en el blog de dev de Microsoft Edge.


## Diagrama de información general


El diagrama siguiente proporciona un resumen que describe las relaciones entre objetos ORTC. Las flechas horizontales o inclinadas indican el flujo de medios o datos, mientras que las flechas verticales indican las interacciones a través de métodos y eventos.

ORTC usa objetos "*Sender*", "*Receiver*" y "*transporte*", que tienen "*capacidades*" que describen lo que pueden hacer, así como "*parámetros*", que definen lo que están configurados. "*Realiza un seguimiento*" para capturar y codificar transmisiones multimedia por remitentes, viaja a través de transportes y, después, descodificados por receptores que procesan las pistas de la transmisión por secuencias de multimedia a etiquetas de audio o vídeo.

![Diagrama de flujo de Microsoft Edge ORTC ](./../media/ortc_diagram.png) en la ilustración anterior, [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) codifica la pista proporcionada como entrada, que se ha transportando a [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) o a [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) . El envío de tonos de multifrecuencia multitono (DTMF) es compatible a través de [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .

El [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) y [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) usa una [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) para seleccionar una ruta de comunicación para llegar al interlocutor receptor `RTCIceTransport` , que a su vez está asociado con una `RTCDtlsTransport` o la `RTCSrtpSdesTransport` cual se demultiplexa en el medio [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) . `RTCRtpReceiver`Después descodifica los elementos multimedia, lo que genera una pista que se representa mediante una etiqueta de audio o vídeo.

Otros objetos también desempeñan un papel. El [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) reúne los candidatos para hielo local para que los use un solo [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) objeto. Secciones restantes de la API rellene los detalles relacionados con las *capacidades* y *parámetros*de RTP, las *estadísticas operativas* y la compatibilidad con la [API de WebRTC 1,0](https://go.microsoft.com/fwlink/p/?LinkID=627573).

> [!NOTE]
> Puesto que Microsoft Edge no implementa el canal de datos, `RTCDataChannel` los `RTCSctpTransport` objetos y no se admiten.




## Componentes compatibles con la implementación inicial de Microsoft Edge


* **Compatibilidad con la API de ORTC.** Las comunicaciones de audio y vídeo son el principal enfoque, incluidos los siguientes objetos:,,,, [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) , así [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) como las [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces que no se muestran directamente en el diagrama.
* **Compatibilidad con multiplexación de RTP/RTCP.** [`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)es necesario para usar con el [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) . También se admite la multiplexación A/V.
* **Compatibilidad con STUN/TURN/ICE.** STUN [(rfc 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), Turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) y Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621)son compatibles. Dentro del hielo, se admite la nominación normal, con nominación agresiva parcialmente (como receptor). DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) es compatible, basado en DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).
* **Compatibilidad con códecs.** Para los [códecs de audio](https://msdn.microsoft.com/library/Mt599587), admitimos g. 711, g. 722, Opus y seda. También admitimos la comodidad de ruido (CN) y DTMF según los requisitos de audio de RTCWEB. En el caso de video, actualmente admitimos el [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) códec que usan los servicios de Skype y admite características avanzadas como Simulcast, codificación de video escalable y corrección de errores de reenvío. Estamos trabajando para habilitar el video interoperable con H. 264.

> [!NOTE]
> Si está familiarizado con las implementaciones de WebRTC 1,0 y está interesado en la evolución de la compatibilidad de objetos dentro de WebRTC 1,0 y ORTC, recomendamos la siguiente presentación de Google, Microsoft y Hookflash de 2014 IIT RTC Conference: "actualización de la[API de ORTC](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)".




## Flujo de código de nivel de aplicación para comunicaciones de 1:1


Para este escenario, dos equipos con Windows 10 actuarán como dos iguales con un servidor WebServer como canal de señalización para intercambiar información entre los interlocutores de modo que se pueda establecer una conexión entre ellos.

Los pasos siguientes se aplican a las operaciones tomadas por un interlocutor. Ambos participantes deben recorrer pasos similares para configurar las comunicaciones de 1:1. Para obtener más información sobre los fragmentos de código siguientes, consulte la demostración de [Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635).

Este ejemplo usa audio-video y multiplexación RTP/RTCP, por lo que solo verá un único ICE y un transporte DTLS, que se usa para transportar paquetes RTP y RTCP para audio y vídeo.

`Step #1.` Cree un [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) objeto (es decir, la [API de captura y secuencias multimedia](./../multimedia/media-Capture-and-Streams.md)) con una pista de audio y una pista de vídeo.

```js
navigator.MediaDevices.getUserMedia ({
    "audio": true,
    "video": {
        width: 640,
        height: 360,
        facingMode: "user"
    }
}).then(
    gotStream
).catch(
    gotMediaError
);

function gotStream(stream) {
    var mediaStreamLocal = stream;
    …
}
```

`Step #2.` Cree el [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) , y habilite el local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) para que se señalice a un interlocutor remoto.

```js
var iceOptions = new RTCIceGatherOptions;
iceOptions.gatherPolicy = "all";
iceOptions.iceservers = ... ;
var iceGathr = new RTCIceGatherer(iceOptions);
iceGathr.onlocalcandidate = function(evt) {
    mySignaller.signalMessage({
        "candidate": evt.candidate
    });
};
```

Para ayudar a proteger la privacidad del usuario, Microsoft Edge introduce una opción que permite a un usuario controlar si los objetos pueden exponer las direcciones IP de host locales [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) . Se proporcionará una opción de interfaz para activar o desactivar esta configuración.

En la [demostración de Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635), se ha configurado un servidor de torneado. Este servidor de vuelta tiene un rendimiento muy limitado, por lo que solo se puede usar la página de demostración.

`Step #3.` Cree el [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) para audio y vídeo y prepárese para controlar el control remoto [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) en el transporte por hielo.

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

Otra opción es acumular todos los candidatos remotos para hielo en un arreglo de discos `remoteCandidates` y llamar `iceTr.setRemoteCandidates(remoteCandidates)` para agregar todos los candidatos remotos juntos.

`Step #4.` Crear el transporte de DTLS.

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` Cree los objetos Sender y Receiver.

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

Paso #6. Recuperar las capacidades del receptor y el remitente.

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` Se pueden intercambiar parámetros de ICE/DTLS y capacidades de envío y recepción.

```js
mySignaller.signalMessage({
    "ice": iceGathr.getLocalParameters(),
    "dtls": dtlsTr.getLocalParameters(),
    "recvAudioCaps": recvAudioCaps,
    "recvVideoCaps": recvVideoCaps,
    "sendAudioCaps": sendAudioCaps,
    "sendVideoCaps": sendVideoCaps
};
```

`Step #8.` Obtener parámetros remotos, iniciar el [`ICE`](https://msdn.microsoft.com/library/Mt433112) transporte y los [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transportes, y configurar los parámetros de envío y recepción de audio y vídeo.

```js
mySignaller.onRemoteParams = function(params) {
    // The responder answers with its preferences, parameters and capabilities
    // Derive the send and receive parameters.
    var audioSendParams = myCapsToSendParams(sendAudioCaps, params.recvAudioCaps);
    var videoSendParams = myCapsToSendParams(sendVideoCaps, params.recvVideoCaps);
    var audioRecvParams = myCapsToRecvParams(recvAudioCaps, params.sendAudioCaps);
    var videoRecvParams = myCapsToRecvParams(recvVideoCaps, params.sendVideoCaps);
    iceTr.start(iceGathr, params.ice, RTCIceRole.controlling);
    dtlsTr.start(params.dtls);
    audioSender.send(audioSendParams);
    videoSender.send(videoSendParams);
    audioReceiver.receive(audioRecvParams);
    videoReceiver.receive(videoRecvParams);
};
```

A continuación se muestra un esqueleto de las funciones auxiliares. Para obtener más información, vea la [demostración de Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635).

```js
RTCRtpParameters function myCapsToSendParams (RTCRtpCapabilities sendCaps, RTCRtpCapabilities remoteRecvCaps) {
    // Function returning the sender RTCRtpParameters, based on intersection of the local sender and remote receiver capabilities.
    // Steps to be followed:
    // 1. Determine the RTP features that the receiver and sender have in common.
    // 2. Determine the codecs that the sender and receiver have in common.
    // 3. Within each common codec, determine the common formats and rtcpFeedback mechanisms.
    // 4. Determine the payloadType to be used, based on the receiver preferredPayloadType.
    // 5. Set RTCRtcpParameters such as mux to their default values.  
}

RTCRtpParameters function myCapsToRecvParams(RTCRtpCapabilities recvCaps, RTCRtpCapabilities remoteSendCaps) {
    return myCapsToSendParams(remoteSendCaps, recvCaps);
}
```

`Step #9.` Representar y reproducir las pistas de multimedia remotas a través de una etiqueta de vídeo.

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

Una vez que estés familiarizado con la configuración de llamadas de 1:1, aplica los mismos principios para configurar las pequeñas llamadas grupales con una topología de malla, en la que cada interlocutor tendrá una conexión 1:1 con el resto del grupo. Dado que la ramificación paralela no es compatible con la plataforma Microsoft Edge, debe controlarse a través de la señalización de 1:1, de modo que se [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) usarán los objetos independientes y para cada conexión.

## Detalles de la implementación en Microsoft Edge


La especificación de ORTC ha sido relativamente estable, ya que el grupo de la comunidad de ORTC emitió la "llamada para implementaciones" y no se esperan desafíos importantes en el nivel de API de JavaScript. Según esta, se ha publicado la implementación de Microsoft Edge para pruebas de interoperabilidad entre exploradores en el nivel de protocolo.

Debe tener en cuenta algunas limitaciones en la implementación de Microsoft Edge:

* `RTCIceTransportController` no es compatible. La implementación de Microsoft Edge controla la inmovilización/descongelación de hielo en función del transporte, de modo que no sea necesario pedir todo el pedido `IceTransports` . Este enfoque debe interoperar con implementaciones existentes.
* `RtpListener` aún no es compatible. Esto significa que los SSRCs (orígenes de sincronización y flujo) deben especificarse de antemano dentro del [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .
* Las ramificaciones aún no son compatibles con ninguno de los dos `IceTransport` , `IceGatherer` o bien `DtlsTransport` . La solución para la `DtlsTransport` bifurcación está aún en debate en el grupo de la comunidad de ORTC.
* No se admite la compatibilidad con RTP/RTCP que no es MUX con `DtlsTransport` . Cuando use `DtlsTransport` la aplicación, deberá admitir RTP/RTCP Mux.
* En [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) , Microsoft Edge ignora actualmente la mayoría de los controles de calidad de codificación, pero requiere establecer los atributos ' Active ' y ' SSRC '.
* El `icecandidatepairchanged` evento aún no es compatible. Puede extraer la información de los pares de candidatos a través del [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) método.
* Microsoft Edge actualmente no admite ninguna de las `DataChannel` funciones definidas actualmente en la especificación de ORTC.

#### Mirar hacia adelante

La implementación de Microsoft Edge aún es anticipada, espere que el conjunto de características siga creciendo en los próximos meses. El objetivo de la implementación de Microsoft Edge es la interoperabilidad en toda la web, así como con el sector de las comunicaciones en tiempo real a largo plazo.



## Referencia de la API

[ORTC (comunicaciones de objeto en tiempo real)](https://msdn.microsoft.com/library/Mt433097)

## Demos

[SimpleWebRTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[Llamada de teléfono ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[Demostración de ORTC](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## Temas relacionados

[La API de ORTC ahora está disponible en Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[SimpleWebRTC: usa la API de ORTC de Microsoft Edge y las API de WebRTC en Chrome y Firefox para hacer llamadas en conferencia entre navegadores.](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[Habilitación de las experiencias de comunicación perfecta para la web con Skype, Skype empresarial y Microsoft Edge.](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[ORTC (COMUNICACIONES DE OBJETO EN TIEMPO REAL) GRUPO DE LA COMUNIDAD](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## Estadístico

[API de objeto W3C (ORTC) para WebRTC](http://draft.ortc.org/)  
