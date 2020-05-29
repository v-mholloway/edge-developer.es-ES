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
# <span data-ttu-id="03f0c-104">API de RTC de objeto</span><span class="sxs-lookup"><span data-stu-id="03f0c-104">Object RTC API</span></span>

<span data-ttu-id="03f0c-105">Las comunicaciones en tiempo real de objetos (ORTC) permiten que los medios (audio y/o video) se transmitan (se envíen y reciban) en tiempo real directamente entre exploradores Web, dispositivos móviles y servidores a través de API de JavaScript nativas.</span><span class="sxs-lookup"><span data-stu-id="03f0c-105">Object Real-Time Communications (ORTC) enables media (audio and/or video) to be streamed (sent and received) in real-time directly between web browsers, mobile devices, and servers via native Javascript APIs.</span></span>

> [!NOTE]
> <span data-ttu-id="03f0c-106">Microsoft Edge ahora implementa ORTC para dispositivos Windows 10.</span><span class="sxs-lookup"><span data-stu-id="03f0c-106">Microsoft Edge now implements ORTC for Windows 10 devices.</span></span> <span data-ttu-id="03f0c-107">Sin embargo, esta implementación difiere de la versión más reciente de la [API de ORTC](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span><span class="sxs-lookup"><span data-stu-id="03f0c-107">However, this implementation differs from the most recent version of the [ORTC API](https://go.microsoft.com/fwlink/p/?LinkID=690096).</span></span> <span data-ttu-id="03f0c-108">ORTC ha continuado evolucionando desde el desarrollo y la publicación de Microsoft Edge, el explorador no implementa cada objeto o método dentro de la API de ORTC, e incluye las extensiones que actualmente no están incorporadas en la especificación.</span><span class="sxs-lookup"><span data-stu-id="03f0c-108">ORTC has continued to evolve since the development and release of Microsoft Edge -- the browser does not implement every object or method within the ORTC API, and includes extensions not currently incorporated within the specification.</span></span> <span data-ttu-id="03f0c-109">El desarrollo más continuará con el objetivo de permitir a los programadores de todo el mundo crear experiencias que incluyan la capacidad de hablar con usuarios de Skype y otros servicios de comunicación compatibles con WebRTC.</span><span class="sxs-lookup"><span data-stu-id="03f0c-109">Further development will continue with the goal to enable developers around the world to build experiences that include the ability to talk to Skype users and other WebRTC compatible communication services.</span></span>



<span data-ttu-id="03f0c-110">Para obtener una experiencia práctica con ORTC, Pruebe estas demostraciones en la prueba:</span><span class="sxs-lookup"><span data-stu-id="03f0c-110">To get a hands-on experience with ORTC, try out these demos on Test Drive:</span></span>
-  [<span data-ttu-id="03f0c-111">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="03f0c-111">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)
-  [<span data-ttu-id="03f0c-112">Llamada de teléfono ORTC</span><span class="sxs-lookup"><span data-stu-id="03f0c-112">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)
-  [<span data-ttu-id="03f0c-113">Demostración de ORTC</span><span class="sxs-lookup"><span data-stu-id="03f0c-113">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)


<span data-ttu-id="03f0c-114">Para obtener más información sobre ORTC, consulte la [API de ortc ya está disponible en Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) en el blog de dev de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="03f0c-114">For more information about ORTC, check out [ORTC API is now available in Microsoft Edge](https://go.microsoft.com/fwlink/p/?LinkID=627564) on the Microsoft Edge dev blog.</span></span>


## <span data-ttu-id="03f0c-115">Diagrama de información general</span><span class="sxs-lookup"><span data-stu-id="03f0c-115">Overview Diagram</span></span>


<span data-ttu-id="03f0c-116">El diagrama siguiente proporciona un resumen que describe las relaciones entre objetos ORTC.</span><span class="sxs-lookup"><span data-stu-id="03f0c-116">The diagram below provides a summary describing relationships between ORTC objects.</span></span> <span data-ttu-id="03f0c-117">Las flechas horizontales o inclinadas indican el flujo de medios o datos, mientras que las flechas verticales indican las interacciones a través de métodos y eventos.</span><span class="sxs-lookup"><span data-stu-id="03f0c-117">Horizontal or slanted arrows denote the flow of media or data, whereas vertical arrows denote interactions via methods and events.</span></span>

<span data-ttu-id="03f0c-118">ORTC usa objetos "*Sender*", "*Receiver*" y "*transporte*", que tienen "*capacidades*" que describen lo que pueden hacer, así como "*parámetros*", que definen lo que están configurados.</span><span class="sxs-lookup"><span data-stu-id="03f0c-118">ORTC uses "*sender*", "*receiver*" and "*transport*" objects, which have "*capabilities*" describing what they are capable of doing, as well as "*parameters*" which define what they are configured to do.</span></span> <span data-ttu-id="03f0c-119">"*Realiza un seguimiento*" para capturar y codificar transmisiones multimedia por remitentes, viaja a través de transportes y, después, descodificados por receptores que procesan las pistas de la transmisión por secuencias de multimedia a etiquetas de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-119">"*Tracks*" capture and encode media streams by senders, traveling over transports, then decoded by receivers that render the media stream tracks to video/audio tags.</span></span>

![<span data-ttu-id="03f0c-120">Diagrama de flujo de Microsoft Edge ORTC ](./../media/ortc_diagram.png) en la ilustración anterior, [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) codifica la pista proporcionada como entrada, que se ha transportando a [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) o a [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) .</span><span class="sxs-lookup"><span data-stu-id="03f0c-120">Microsoft Edge ORTC Flow Diagram](./../media/ortc_diagram.png) In the figure above, the [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) encodes the track provided as input, which is transported over a [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) or an [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527).</span></span> <span data-ttu-id="03f0c-121">El envío de tonos de multifrecuencia multitono (DTMF) es compatible a través de [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496) .</span><span class="sxs-lookup"><span data-stu-id="03f0c-121">Sending of Dual Tone Multi Frequency (DTMF) tones is supported via the [`RTCDtmfSender`](https://msdn.microsoft.com/library/Mt502496).</span></span>

<span data-ttu-id="03f0c-122">El [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) y [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) usa una [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) para seleccionar una ruta de comunicación para llegar al interlocutor receptor `RTCIceTransport` , que a su vez está asociado con una `RTCDtlsTransport` o la `RTCSrtpSdesTransport` cual se demultiplexa en el medio [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="03f0c-122">The [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) and [`RTCSrtpSdesTransport`](https://msdn.microsoft.com/library/Mt502527) utilize an [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) to select a communication path to reach the receiving peer's `RTCIceTransport`, which is in turn associated with an `RTCDtlsTransport` or `RTCSrtpSdesTransport` which de-multiplexes media to the [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span> <span data-ttu-id="03f0c-123">`RTCRtpReceiver`Después descodifica los elementos multimedia, lo que genera una pista que se representa mediante una etiqueta de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-123">The `RTCRtpReceiver` then decodes media, producing a track which is rendered by an audio or video tag.</span></span>

<span data-ttu-id="03f0c-124">Otros objetos también desempeñan un papel.</span><span class="sxs-lookup"><span data-stu-id="03f0c-124">Several other objects also play a role.</span></span> <span data-ttu-id="03f0c-125">El [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) reúne los candidatos para hielo local para que los use un solo [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) objeto.</span><span class="sxs-lookup"><span data-stu-id="03f0c-125">The [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) gathers local ICE candidates for use by a single [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) object.</span></span> <span data-ttu-id="03f0c-126">Secciones restantes de la API rellene los detalles relacionados con las *capacidades* y *parámetros*de RTP, las *estadísticas operativas* y la compatibilidad con la [API de WebRTC 1,0](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span><span class="sxs-lookup"><span data-stu-id="03f0c-126">Remaining sections of the API fill in details relating to RTP *capabilities* and *parameters*, *operational statistics* and compatibility with the [WebRTC 1.0 API](https://go.microsoft.com/fwlink/p/?LinkID=627573).</span></span>

> [!NOTE]
> <span data-ttu-id="03f0c-127">Puesto que Microsoft Edge no implementa el canal de datos, `RTCDataChannel` los `RTCSctpTransport` objetos y no se admiten.</span><span class="sxs-lookup"><span data-stu-id="03f0c-127">Since Microsoft Edge does not implement the data channel, the `RTCDataChannel` and `RTCSctpTransport` objects are not supported.</span></span>




## <span data-ttu-id="03f0c-128">Componentes compatibles con la implementación inicial de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="03f0c-128">Components supported in the initial Microsoft Edge implementation</span></span>


* **<span data-ttu-id="03f0c-129">Compatibilidad con la API de ORTC.</span><span class="sxs-lookup"><span data-stu-id="03f0c-129">ORTC API support.</span></span>** <span data-ttu-id="03f0c-130">Las comunicaciones de audio y vídeo son el principal enfoque, incluidos los siguientes objetos:,,,, [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112) , así [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495) [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516) [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508) como las [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces que no se muestran directamente en el diagrama.</span><span class="sxs-lookup"><span data-stu-id="03f0c-130">Audio/video communications is the primary focus, including the following objects: [`RTCIceGatherer`](https://msdn.microsoft.com/library/Mt433107), [`RTCIceTransport`](https://msdn.microsoft.com/library/Mt433112), [`RTCDtlsTransport`](https://msdn.microsoft.com/library/Mt502495), [`RTCRtpSender`](https://msdn.microsoft.com/library/Mt502516), [`RTCRtpReceiver`](https://msdn.microsoft.com/library/Mt502508), as well as the [`RTCStats`](https://msdn.microsoft.com/library/Mt589726) interfaces that are not shown directly in the diagram.</span></span>
* **<span data-ttu-id="03f0c-131">Compatibilidad con multiplexación de RTP/RTCP.</span><span class="sxs-lookup"><span data-stu-id="03f0c-131">RTP/RTCP multiplexing support.</span></span>** <span data-ttu-id="03f0c-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503)es necesario para usar con el [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) .</span><span class="sxs-lookup"><span data-stu-id="03f0c-132">[`RTP/RTCP multiplexing`](https://msdn.microsoft.com/library/Mt502503) is required for use with the [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495).</span></span> <span data-ttu-id="03f0c-133">También se admite la multiplexación A/V.</span><span class="sxs-lookup"><span data-stu-id="03f0c-133">A/V multiplexing is also supported.</span></span>
* **<span data-ttu-id="03f0c-134">Compatibilidad con STUN/TURN/ICE.</span><span class="sxs-lookup"><span data-stu-id="03f0c-134">STUN/TURN/ICE support.</span></span>** <span data-ttu-id="03f0c-135">STUN [(rfc 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), Turn [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) y Ice [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621)son compatibles.</span><span class="sxs-lookup"><span data-stu-id="03f0c-135">STUN [(RFC 5389)](https://go.microsoft.com/fwlink/p/?LinkID=627619), TURN [(RFC 5766)](https://go.microsoft.com/fwlink/p/?LinkID=627620) as well as ICE [(RFC 5245)](https://go.microsoft.com/fwlink/p/?LinkID=627621), are supported.</span></span> <span data-ttu-id="03f0c-136">Dentro del hielo, se admite la nominación normal, con nominación agresiva parcialmente (como receptor).</span><span class="sxs-lookup"><span data-stu-id="03f0c-136">Within ICE, regular nomination is supported, with aggressive nomination partially supported (as a receiver).</span></span> <span data-ttu-id="03f0c-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) es compatible, basado en DTLS 1,0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span><span class="sxs-lookup"><span data-stu-id="03f0c-137">DTLS-SRTP [(RFC 5764)](https://go.microsoft.com/fwlink/p/?LinkID=627622) is supported, based on DTLS 1.0 [(RFC4347)](https://go.microsoft.com/fwlink/p/?LinkID=627629).</span></span>
* **<span data-ttu-id="03f0c-138">Compatibilidad con códecs.</span><span class="sxs-lookup"><span data-stu-id="03f0c-138">Codec support.</span></span>** <span data-ttu-id="03f0c-139">Para los [códecs de audio](https://msdn.microsoft.com/library/Mt599587), admitimos g. 711, g. 722, Opus y seda.</span><span class="sxs-lookup"><span data-stu-id="03f0c-139">For [audio codecs](https://msdn.microsoft.com/library/Mt599587), we support G.711, G.722, Opus and SILK.</span></span> <span data-ttu-id="03f0c-140">También admitimos la comodidad de ruido (CN) y DTMF según los requisitos de audio de RTCWEB.</span><span class="sxs-lookup"><span data-stu-id="03f0c-140">We also support Comfort Noise (CN) and DTMF according to the RTCWEB audio requirements.</span></span> <span data-ttu-id="03f0c-141">En el caso de video, actualmente admitimos el [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) códec que usan los servicios de Skype y admite características avanzadas como Simulcast, codificación de video escalable y corrección de errores de reenvío.</span><span class="sxs-lookup"><span data-stu-id="03f0c-141">For video we currently support the [`H.264UC`](https://msdn.microsoft.com/library/Mt589706) codec used by Skype services, supporting advanced features such as simulcast, scalable video coding and forward error correction.</span></span> <span data-ttu-id="03f0c-142">Estamos trabajando para habilitar el video interoperable con H. 264.</span><span class="sxs-lookup"><span data-stu-id="03f0c-142">We're working toward to enabling interoperable video with H.264.</span></span>

> [!NOTE]
> <span data-ttu-id="03f0c-143">Si está familiarizado con las implementaciones de WebRTC 1,0 y está interesado en la evolución de la compatibilidad de objetos dentro de WebRTC 1,0 y ORTC, recomendamos la siguiente presentación de Google, Microsoft y Hookflash de 2014 IIT RTC Conference: "actualización de la[API de ORTC](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)".</span><span class="sxs-lookup"><span data-stu-id="03f0c-143">If you are familiar with WebRTC 1.0 implementations, and are interested in the evolution of object support within WebRTC 1.0 and ORTC, we recommend the following presentation by Google, Microsoft, and Hookflash from the 2014 IIT RTC Conference: "[ORTC API Update](http://www.rtc-conference.com/2016/wp-content/uploads/gravity_forms/2-2f7a537445fa703985ab4d2372ac42ca/2014/10/ORTC_API_Update.pdf)."</span></span>




## <span data-ttu-id="03f0c-144">Flujo de código de nivel de aplicación para comunicaciones de 1:1</span><span class="sxs-lookup"><span data-stu-id="03f0c-144">App level code flow for 1:1 communications</span></span>


<span data-ttu-id="03f0c-145">Para este escenario, dos equipos con Windows 10 actuarán como dos iguales con un servidor WebServer como canal de señalización para intercambiar información entre los interlocutores de modo que se pueda establecer una conexión entre ellos.</span><span class="sxs-lookup"><span data-stu-id="03f0c-145">For this scenario, two Windows 10 machines will act as two peers with a webserver as the signaling channel to exchange information between the peers so that a connection may be established between them.</span></span>

<span data-ttu-id="03f0c-146">Los pasos siguientes se aplican a las operaciones tomadas por un interlocutor.</span><span class="sxs-lookup"><span data-stu-id="03f0c-146">The steps below are scoped to operations taken by one peer.</span></span> <span data-ttu-id="03f0c-147">Ambos participantes deben recorrer pasos similares para configurar las comunicaciones de 1:1.</span><span class="sxs-lookup"><span data-stu-id="03f0c-147">Both peers must go through similar steps in order to set up the 1:1 communications.</span></span> <span data-ttu-id="03f0c-148">Para obtener más información sobre los fragmentos de código siguientes, consulte la demostración de [Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="03f0c-148">To make better sense out of the code snippets below, refer to the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

<span data-ttu-id="03f0c-149">Este ejemplo usa audio-video y multiplexación RTP/RTCP, por lo que solo verá un único ICE y un transporte DTLS, que se usa para transportar paquetes RTP y RTCP para audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-149">This example uses audio-video and RTP/RTCP multiplexing, so you will see only a single ICE and DTLS transport, used to transport RTP and RTCP packets for both audio and video.</span></span>

`Step #1.` <span data-ttu-id="03f0c-150">Cree un [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) objeto (es decir, la [API de captura y secuencias multimedia](./../multimedia/media-Capture-and-Streams.md)) con una pista de audio y una pista de vídeo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-150">Create [`MediaStream`](https://msdn.microsoft.com/library/Mt131875) object (i.e. [Media Capture and Streams API](./../multimedia/media-Capture-and-Streams.md)) with one audio track and one video track.</span></span>

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

`Step #2.` <span data-ttu-id="03f0c-151">Cree el [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx) , y habilite el local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) para que se señalice a un interlocutor remoto.</span><span class="sxs-lookup"><span data-stu-id="03f0c-151">Create the [`ICE gatherer`](https://msdn.microsoft.com/library/mt433107(v=vs.85).aspx), and enable local [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) to be signaled to remote peer.</span></span>

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

<span data-ttu-id="03f0c-152">Para ayudar a proteger la privacidad del usuario, Microsoft Edge introduce una opción que permite a un usuario controlar si los objetos pueden exponer las direcciones IP de host locales [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) .</span><span class="sxs-lookup"><span data-stu-id="03f0c-152">To help protect user privacy, Microsoft Edge introduces an option that allows a user to control whether local host IP addresses can be exposed by the [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) objects.</span></span> <span data-ttu-id="03f0c-153">Se proporcionará una opción de interfaz para activar o desactivar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="03f0c-153">An interface option will be provided to toggle this setting.</span></span>

<span data-ttu-id="03f0c-154">En la [demostración de Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635), se ha configurado un servidor de torneado.</span><span class="sxs-lookup"><span data-stu-id="03f0c-154">In the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635), a TURN server has been set up.</span></span> <span data-ttu-id="03f0c-155">Este servidor de vuelta tiene un rendimiento muy limitado, por lo que solo se puede usar la página de demostración.</span><span class="sxs-lookup"><span data-stu-id="03f0c-155">This TURN server has a very limited throughput, so is limited to only demo page use.</span></span>

`Step #3.` <span data-ttu-id="03f0c-156">Cree el [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) para audio y vídeo y prepárese para controlar el control remoto [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) en el transporte por hielo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-156">Create the [`ICE transport`](https://msdn.microsoft.com/library/Mt433112) for audio and video, and prepare to handle remote [`ICE candidates`](https://msdn.microsoft.com/library/Mt502499) on the ICE transport.</span></span>

```js
var iceTr = new RTCIceTransport();
mySignaller.onRemoteCandidate = function(remote) {
    iceTr.addRemoteCandidate(remote.candidate);
}
```

<span data-ttu-id="03f0c-157">Otra opción es acumular todos los candidatos remotos para hielo en un arreglo de discos `remoteCandidates` y llamar `iceTr.setRemoteCandidates(remoteCandidates)` para agregar todos los candidatos remotos juntos.</span><span class="sxs-lookup"><span data-stu-id="03f0c-157">Another option here is to accumulate all the remote ICE candidates into an array `remoteCandidates` and call `iceTr.setRemoteCandidates(remoteCandidates)` to add all the remote candidates together.</span></span>

`Step #4.` <span data-ttu-id="03f0c-158">Crear el transporte de DTLS.</span><span class="sxs-lookup"><span data-stu-id="03f0c-158">Create the DTLS transport.</span></span>

```js
var dtlsTr = new RTCDtlsTransport(iceTr);
```

`Step #5.` <span data-ttu-id="03f0c-159">Cree los objetos Sender y Receiver.</span><span class="sxs-lookup"><span data-stu-id="03f0c-159">Create the sender and receiver objects.</span></span>

```js
var audioTrack = mediaStreamLocal.getAudioTracks()[0];
var videoTrack = mediaStreamLocal.getVideoTracks()[0];
var audioSender = new RtpSender(audioTrack, dtlsTr);
var videoSender = new RtpSender(videoTrack, dtlsTr);
var audioReceiver = new RtpReceiver(dtlsTr, "audio");
var videoReceiver = new RtpReceiver(dtlsTr, "video");
```

<span data-ttu-id="03f0c-160">Paso #6.</span><span class="sxs-lookup"><span data-stu-id="03f0c-160">Step #6.</span></span> <span data-ttu-id="03f0c-161">Recuperar las capacidades del receptor y el remitente.</span><span class="sxs-lookup"><span data-stu-id="03f0c-161">Retrieve the receiver and sender capabilities.</span></span>

```js
var recvAudioCaps = RTCRtpReceiver.getCapabilities("audio");
var recvVideoCaps = RTCRtpReceiver.getCapabilities("video");
var sendAudioCaps = RTCRtpSender.getCapabilities("audio");
var sendVideoCaps = RTCRtpSender.getCapabilities("video");
```

`Step #7.` <span data-ttu-id="03f0c-162">Se pueden intercambiar parámetros de ICE/DTLS y capacidades de envío y recepción.</span><span class="sxs-lookup"><span data-stu-id="03f0c-162">ICE/DTLS parameters and Send/Receive capabilities can be exchanged.</span></span>

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

`Step #8.` <span data-ttu-id="03f0c-163">Obtener parámetros remotos, iniciar el [`ICE`](https://msdn.microsoft.com/library/Mt433112) transporte y los [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transportes, y configurar los parámetros de envío y recepción de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-163">Get remote params, start the [`ICE`](https://msdn.microsoft.com/library/Mt433112) and [`DTLS`](https://msdn.microsoft.com/library/Mt502495) transports, and set the audio and video send and receive parameters.</span></span>

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

<span data-ttu-id="03f0c-164">A continuación se muestra un esqueleto de las funciones auxiliares.</span><span class="sxs-lookup"><span data-stu-id="03f0c-164">Below is a skeleton of the helper functions.</span></span> <span data-ttu-id="03f0c-165">Para obtener más información, vea la [demostración de Microsoft Edge Test Drive](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span><span class="sxs-lookup"><span data-stu-id="03f0c-165">Find more details in the [Microsoft Edge Test Drive Demo](https://go.microsoft.com/fwlink/p/?LinkID=627635).</span></span>

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

`Step #9.` <span data-ttu-id="03f0c-166">Representar y reproducir las pistas de multimedia remotas a través de una etiqueta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-166">Render and play the remote media stream tracks through a video tag.</span></span>

```js
var videoRenderer = document.getElementById("myRtcVideoTag");
var mediaStreamRemote = new MediaStream();
mediaStreamRemote.addTrack(audioReceiver.track);
mediaStreamRemote.addTrack(videoReceiver.track);
videoRenderer.srcObject = mediaStreamRemote;
videoRenderer.play();
```

<span data-ttu-id="03f0c-167">Una vez que estés familiarizado con la configuración de llamadas de 1:1, aplica los mismos principios para configurar las pequeñas llamadas grupales con una topología de malla, en la que cada interlocutor tendrá una conexión 1:1 con el resto del grupo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-167">Once familiar with setting up 1:1 calls, apply the same principles to set up small group calls using a mesh topology, where each peer will have a 1:1 connection with the rest of the group.</span></span> <span data-ttu-id="03f0c-168">Dado que la ramificación paralela no es compatible con la plataforma Microsoft Edge, debe controlarse a través de la señalización de 1:1, de modo que se [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) usarán los objetos independientes y para cada conexión.</span><span class="sxs-lookup"><span data-stu-id="03f0c-168">Since parallel forking is not supported on the Microsoft Edge platform, this should be handled via 1:1 signaling, so that independent [`IceGatherer`](https://msdn.microsoft.com/library/Mt433107) and [`DtlsTransport`](https://msdn.microsoft.com/library/Mt502495) objects will be used for each connection.</span></span>

## <span data-ttu-id="03f0c-169">Detalles de la implementación en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="03f0c-169">Implementation details in Microsoft Edge</span></span>


<span data-ttu-id="03f0c-170">La especificación de ORTC ha sido relativamente estable, ya que el grupo de la comunidad de ORTC emitió la "llamada para implementaciones" y no se esperan desafíos importantes en el nivel de API de JavaScript.</span><span class="sxs-lookup"><span data-stu-id="03f0c-170">The ORTC spec has been relatively stable since the ORTC Community Group issued the "Call for Implementations," and significant challenges at the JavaScript API level are not expected.</span></span> <span data-ttu-id="03f0c-171">Según esta, se ha publicado la implementación de Microsoft Edge para pruebas de interoperabilidad entre exploradores en el nivel de protocolo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-171">Based on this, Microsoft Edge implementation has been released for cross-browser interoperability testing at the protocol level.</span></span>

<span data-ttu-id="03f0c-172">Debe tener en cuenta algunas limitaciones en la implementación de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="03f0c-172">A few limitations in the Microsoft Edge implementation should be noted:</span></span>

* `RTCIceTransportController` <span data-ttu-id="03f0c-173">no es compatible.</span><span class="sxs-lookup"><span data-stu-id="03f0c-173">is not supported.</span></span> <span data-ttu-id="03f0c-174">La implementación de Microsoft Edge controla la inmovilización/descongelación de hielo en función del transporte, de modo que no sea necesario pedir todo el pedido `IceTransports` .</span><span class="sxs-lookup"><span data-stu-id="03f0c-174">Microsoft Edge implementation handles ICE freezing/unfreezing on a per-transport basis, so that ordering all the `IceTransports` is not necessary.</span></span> <span data-ttu-id="03f0c-175">Este enfoque debe interoperar con implementaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="03f0c-175">This approach should interoperate with existing implementations.</span></span>
* `RtpListener` <span data-ttu-id="03f0c-176">aún no es compatible.</span><span class="sxs-lookup"><span data-stu-id="03f0c-176">is not yet supported.</span></span> <span data-ttu-id="03f0c-177">Esto significa que los SSRCs (orígenes de sincronización y flujo) deben especificarse de antemano dentro del [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508) .</span><span class="sxs-lookup"><span data-stu-id="03f0c-177">This means that SSRCs (stream and synchronization sources) need to be specified in advance within the [`RtpReceiver`](https://msdn.microsoft.com/library/Mt502508).</span></span>
* <span data-ttu-id="03f0c-178">Las ramificaciones aún no son compatibles con ninguno de los dos `IceTransport` , `IceGatherer` o bien `DtlsTransport` .</span><span class="sxs-lookup"><span data-stu-id="03f0c-178">Forking is not yet supported in either `IceTransport`, `IceGatherer`, or `DtlsTransport`.</span></span> <span data-ttu-id="03f0c-179">La solución para la `DtlsTransport` bifurcación está aún en debate en el grupo de la comunidad de ORTC.</span><span class="sxs-lookup"><span data-stu-id="03f0c-179">The solution to `DtlsTransport` forking is still under discussion in the ORTC Community Group.</span></span>
* <span data-ttu-id="03f0c-180">No se admite la compatibilidad con RTP/RTCP que no es MUX con `DtlsTransport` .</span><span class="sxs-lookup"><span data-stu-id="03f0c-180">RTP/RTCP non-mux with `DtlsTransport` is not yet supported.</span></span> <span data-ttu-id="03f0c-181">Cuando use `DtlsTransport` la aplicación, deberá admitir RTP/RTCP Mux.</span><span class="sxs-lookup"><span data-stu-id="03f0c-181">When using `DtlsTransport` your application will need to support RTP/RTCP mux.</span></span>
* <span data-ttu-id="03f0c-182">En [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx) , Microsoft Edge ignora actualmente la mayoría de los controles de calidad de codificación, pero requiere establecer los atributos ' Active ' y ' SSRC '.</span><span class="sxs-lookup"><span data-stu-id="03f0c-182">In [`RTCRtpEncodingParameters Dictionary`](https://msdn.microsoft.com/library/mt502505(v=vs.85).aspx), Microsoft Edge currently ignores most of the encoding quality controls, but does require setting the 'active' and 'ssrc' attributes.</span></span>
* <span data-ttu-id="03f0c-183">El `icecandidatepairchanged` evento aún no es compatible.</span><span class="sxs-lookup"><span data-stu-id="03f0c-183">The `icecandidatepairchanged` event is not yet supported.</span></span> <span data-ttu-id="03f0c-184">Puede extraer la información de los pares de candidatos a través del [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) método.</span><span class="sxs-lookup"><span data-stu-id="03f0c-184">You can extract the candidate pair information through the [`getNominatedCandidatePair`](https://msdn.microsoft.com/library/Mt433087) method.</span></span>
* <span data-ttu-id="03f0c-185">Microsoft Edge actualmente no admite ninguna de las `DataChannel` funciones definidas actualmente en la especificación de ORTC.</span><span class="sxs-lookup"><span data-stu-id="03f0c-185">Microsoft Edge currently does not support any of the `DataChannel` functionality currently defined in the ORTC spec.</span></span>

#### <span data-ttu-id="03f0c-186">Mirar hacia adelante</span><span class="sxs-lookup"><span data-stu-id="03f0c-186">Looking forward</span></span>

<span data-ttu-id="03f0c-187">La implementación de Microsoft Edge aún es anticipada, espere que el conjunto de características siga creciendo en los próximos meses.</span><span class="sxs-lookup"><span data-stu-id="03f0c-187">Microsoft Edge implementation is still early, expect the feature set to continue to grow in the coming months.</span></span> <span data-ttu-id="03f0c-188">El objetivo de la implementación de Microsoft Edge es la interoperabilidad en toda la web, así como con el sector de las comunicaciones en tiempo real a largo plazo.</span><span class="sxs-lookup"><span data-stu-id="03f0c-188">The goal for Microsoft Edge implementation is interoperability across the web today as well as with the real-time communications industry in the long term.</span></span>



## <span data-ttu-id="03f0c-189">Referencia de la API</span><span class="sxs-lookup"><span data-stu-id="03f0c-189">API reference</span></span>

[<span data-ttu-id="03f0c-190">ORTC (comunicaciones de objeto en tiempo real)</span><span class="sxs-lookup"><span data-stu-id="03f0c-190">ORTC (Object Real-Time Communications)</span></span>](https://msdn.microsoft.com/library/Mt433097)

## <span data-ttu-id="03f0c-191">Demos</span><span class="sxs-lookup"><span data-stu-id="03f0c-191">Demos</span></span>

[<span data-ttu-id="03f0c-192">SimpleWebRTC</span><span class="sxs-lookup"><span data-stu-id="03f0c-192">SimpleWebRTC</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/simplewebrtc/)

[<span data-ttu-id="03f0c-193">Llamada de teléfono ORTC</span><span class="sxs-lookup"><span data-stu-id="03f0c-193">ORTC phone call</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/twilioortc/)

[<span data-ttu-id="03f0c-194">Demostración de ORTC</span><span class="sxs-lookup"><span data-stu-id="03f0c-194">ORTC demo</span></span>](https://developer.microsoft.com/microsoft-edge/testdrive/demos/ortcdemo/)

## <span data-ttu-id="03f0c-195">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="03f0c-195">Related topics</span></span>

[<span data-ttu-id="03f0c-196">La API de ORTC ahora está disponible en Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="03f0c-196">ORTC API is now available in Microsoft Edge</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=627564)

[<span data-ttu-id="03f0c-197">SimpleWebRTC: usa la API de ORTC de Microsoft Edge y las API de WebRTC en Chrome y Firefox para hacer llamadas en conferencia entre navegadores.</span><span class="sxs-lookup"><span data-stu-id="03f0c-197">SimpleWebRTC: Use Microsoft Edge's ORTC API and the WebRTC APIs in Chrome and Firefox to make cross-browser conference calls.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=629636)

[<span data-ttu-id="03f0c-198">Habilitación de las experiencias de comunicación perfecta para la web con Skype, Skype empresarial y Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="03f0c-198">Enabling Seamless Communication Experiences for the Web with Skype, Skype for Business, and Microsoft Edge.</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671722)

[<span data-ttu-id="03f0c-199">ORTC (COMUNICACIONES DE OBJETO EN TIEMPO REAL) GRUPO DE LA COMUNIDAD</span><span class="sxs-lookup"><span data-stu-id="03f0c-199">ORTC (OBJECT REAL-TIME COMMUNICATIONS) COMMUNITY GROUP</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=671724)

## <span data-ttu-id="03f0c-200">Estadístico</span><span class="sxs-lookup"><span data-stu-id="03f0c-200">Specification</span></span>

[<span data-ttu-id="03f0c-201">API de objeto W3C (ORTC) para WebRTC</span><span class="sxs-lookup"><span data-stu-id="03f0c-201">W3C Object RTC (ORTC) API for WebRTC</span></span>](http://draft.ortc.org/)  
