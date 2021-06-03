---
description: Actualizar al protocolo Microsoft Edge DevTools
title: Microsoft Edge Actualización del protocolo DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/06/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: de7d6c39c09ba321f21b34e6e461ec030f09f6ad
ms.sourcegitcommit: 146072bf606b84e5145a48333abf9c6b892a12d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "11480163"
---
# <a name="microsoft-edge-chromium-devtools-protocol-overview"></a><span data-ttu-id="cd721-103">Microsoft Edge (Chromium) DevTools Protocol overview</span><span class="sxs-lookup"><span data-stu-id="cd721-103">Microsoft Edge (Chromium) DevTools Protocol overview</span></span>  

<span data-ttu-id="cd721-104">Con el cambio en la plataforma web subyacente de Microsoft Edge a Chromium, el protocolo [DevTools de Microsoft Edge (EdgeHTML)](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) no recibirá más actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="cd721-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) will not be receiving any further updates.</span></span>  <span data-ttu-id="cd721-105">El Microsoft Edge \(Chromium\) DevTools Protocol coincidirá con las API del protocolo DevTools de Chrome en el futuro.</span><span class="sxs-lookup"><span data-stu-id="cd721-105">The Microsoft Edge \(Chromium\) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span>  

<span data-ttu-id="cd721-106">Puedes encontrar documentación sobre esos dominios y métodos haciendo referencia al [Visor de protocolos de Chrome DevTools](https://chromedevtools.github.io/devtools-protocol/tot).</span><span class="sxs-lookup"><span data-stu-id="cd721-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot).</span></span>  

> [!NOTE]
> <span data-ttu-id="cd721-107">Los métodos con prefijo en el protocolo `ms` [DevTools de Microsoft Edge (EdgeHTML)](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) ya no se admiten en el protocolo DevTools de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cd721-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](/archive/microsoft-edge/legacy/developer/devtools-protocol/index) are no longer supported in the Microsoft Edge \(Chromium\) DevTools Protocol.</span></span>  

## <a name="using-the-devtools-protocol"></a><span data-ttu-id="cd721-108">Uso del protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="cd721-108">Using the DevTools Protocol</span></span>  

<span data-ttu-id="cd721-109">Este es el modo de adjuntar un cliente de herramientas personalizado al servidor DevTools en Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="cd721-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge \(Chromium\).</span></span>  

1.  <span data-ttu-id="cd721-110">Asegúrese de que todas las instancias Microsoft Edge \(Chromium\) estén cerradas.</span><span class="sxs-lookup"><span data-stu-id="cd721-110">Ensure all instances of Microsoft Edge \(Chromium\) are closed.</span></span>  
1.  <span data-ttu-id="cd721-111">Inicie Microsoft Edge \(Chromium\) con el puerto de depuración remota:.</span><span class="sxs-lookup"><span data-stu-id="cd721-111">Launch Microsoft Edge \(Chromium\) with the remote debugging port:.</span></span> 
    
    ```shell
    msedge.exe --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="cd721-112">Opcionalmente, puede iniciar una instancia independiente de Edge con un perfil de usuario distinto si lo desea.</span><span class="sxs-lookup"><span data-stu-id="cd721-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired.</span></span>  
    
    ```shell
    msedge.exe --user-data-dir=<some directory>
    ```  
    
1.  <span data-ttu-id="cd721-113">A continuación, use el extremo HTTP `list` para obtener una lista de destinos de página adjuntables.</span><span class="sxs-lookup"><span data-stu-id="cd721-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets.</span></span>  
    
    ```http
    http://localhost:9222/json/list
    ```  
    
1.  <span data-ttu-id="cd721-114">Por último, conéctese al destino deseado y emita comandos/suscríbete a los mensajes de evento a través del servidor de `webSocketDebuggerUrl` socket web DevTools.</span><span class="sxs-lookup"><span data-stu-id="cd721-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>  

## <a name="devtools-protocol-http-endpoints"></a><span data-ttu-id="cd721-115">Extremos HTTP del protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="cd721-115">DevTools Protocol HTTP Endpoints</span></span>  

<span data-ttu-id="cd721-116">El Microsoft Edge \(Chromium\) DevTools Protocol admite los siguientes extremos HTTP.</span><span class="sxs-lookup"><span data-stu-id="cd721-116">The Microsoft Edge \(Chromium\) DevTools Protocol supports the following HTTP endpoints.</span></span>  

## <a name="jsonversion"></a><span data-ttu-id="cd721-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="cd721-117">/json/version</span></span>  

<span data-ttu-id="cd721-118">Proporciona información sobre el explorador del equipo host y qué versión del protocolo DevTools admite.</span><span class="sxs-lookup"><span data-stu-id="cd721-118">Provides information on the browser of the host machine and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="cd721-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd721-119">Parameters</span></span>**  

**<span data-ttu-id="cd721-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd721-120">None</span></span>**  

**<span data-ttu-id="cd721-121">Return (objeto)</span><span class="sxs-lookup"><span data-stu-id="cd721-121">Return object</span></span>**  

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
}
```  

## <a name="jsonprotocol"></a><span data-ttu-id="cd721-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="cd721-122">/json/protocol</span></span>  

<span data-ttu-id="cd721-123">Proporciona toda la superficie de API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="cd721-123">Provides the entire protocol API surface serialized as JSON.</span></span>  

**<span data-ttu-id="cd721-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd721-124">Parameters</span></span>**  

**<span data-ttu-id="cd721-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd721-125">None</span></span>**  

**<span data-ttu-id="cd721-126">Return (objeto)</span><span class="sxs-lookup"><span data-stu-id="cd721-126">Return object</span></span>**  

<span data-ttu-id="cd721-127">Objeto JSON que representa la superficie de API disponible para la versión actual del protocolo.</span><span class="sxs-lookup"><span data-stu-id="cd721-127">JSON object which represents the available API surface for current version of the protocol.</span></span>  

## <a name="jsonlist"></a><span data-ttu-id="cd721-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="cd721-128">/json/list</span></span>  

<span data-ttu-id="cd721-129">Proporciona una lista de candidatos de destinos de página para la depuración.</span><span class="sxs-lookup"><span data-stu-id="cd721-129">Provides a candidate list of page targets for debugging.</span></span>  

**<span data-ttu-id="cd721-130">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd721-130">Parameters</span></span>**  

**<span data-ttu-id="cd721-131">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd721-131">None</span></span>**  

**<span data-ttu-id="cd721-132">Return (objeto)</span><span class="sxs-lookup"><span data-stu-id="cd721-132">Return object</span></span>**  

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, ...  ]
```  

## <a name="jsonclose"></a><span data-ttu-id="cd721-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="cd721-133">/json/close</span></span>  

<span data-ttu-id="cd721-134">Cierra el proceso de destino \(por ejemplo, en Microsoft Edge \(Chromium\), cierra la pestaña de página\).</span><span class="sxs-lookup"><span data-stu-id="cd721-134">Closes down the target process \(for example, in Microsoft Edge \(Chromium\), closes the page tab\).</span></span>  

**<span data-ttu-id="cd721-135">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd721-135">Parameters</span></span>**  

<span data-ttu-id="cd721-136">Id. de destino</span><span class="sxs-lookup"><span data-stu-id="cd721-136">Target ID</span></span>  

**<span data-ttu-id="cd721-137">Return (objeto)</span><span class="sxs-lookup"><span data-stu-id="cd721-137">Return object</span></span>**  

```
String(“Target is closing”)
```  

## <a name="remote-tools-for-microsoft-edge-beta"></a><span data-ttu-id="cd721-138">Herramientas remotas para Microsoft Edge (Beta)</span><span class="sxs-lookup"><span data-stu-id="cd721-138">Remote Tools for Microsoft Edge (Beta)</span></span>  

<span data-ttu-id="cd721-139">Ahora puede instalar las Herramientas remotas [para Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) desde el [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span><span class="sxs-lookup"><span data-stu-id="cd721-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span>  <span data-ttu-id="cd721-140">Esta aplicación te permite depurar de forma remota Microsoft Edge (Chromium) que se ejecuten en un Windows 10 desde el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="cd721-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>  

<span data-ttu-id="cd721-141">Para obtener información sobre cómo configurar el dispositivo Windows 10 y conectarse a él desde el equipo de desarrollo, vaya a Introducción con depuración [remota Windows 10 dispositivos](../devtools-guide-chromium/remote-debugging/windows.md).</span><span class="sxs-lookup"><span data-stu-id="cd721-141">To learn how to set up your Windows 10 device and connect to it from your development machine, navigate to [Get Started with Remote Debugging Windows 10 Devices](../devtools-guide-chromium/remote-debugging/windows.md).</span></span>  

<span data-ttu-id="cd721-142">Remote [Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usa el mismo protocolo de devTools de Microsoft Edge (Chromium) que de [devTools](../devtools-guide-chromium/index.md) para comunicarse con Microsoft Edge que se ejecuta en el dispositivo Windows 10 que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="cd721-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](../devtools-guide-chromium/index.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span>  <span data-ttu-id="cd721-143">Esta aplicación solo antepone y `/msedge/` un identificador de proceso ( ) antes de cada llamada al `pid` protocolo.</span><span class="sxs-lookup"><span data-stu-id="cd721-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span>  <span data-ttu-id="cd721-144">Admite los siguientes puntos de conexión HTTP.</span><span class="sxs-lookup"><span data-stu-id="cd721-144">It supports the following HTTP endpoints.</span></span>  

### <a name="msedgejsonlist"></a><span data-ttu-id="cd721-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="cd721-145">/msedge/json/list</span></span>  

<span data-ttu-id="cd721-146">Proporciona una lista de candidatos de todos los procesos `msedge.exe` \(incluidos [los PWA](../progressive-web-apps-chromium/index.md) y todas las pestañas en todas las instancias de Microsoft Edge\) en el dispositivo Windows 10 para la depuración.</span><span class="sxs-lookup"><span data-stu-id="cd721-146">Provides a candidate list of all `msedge.exe` processes \(including [PWAs](../progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge\) on the Windows 10 device for debugging.</span></span>  

**<span data-ttu-id="cd721-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd721-147">Parameters</span></span>**  

**<span data-ttu-id="cd721-148">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd721-148">None</span></span>**  

**<span data-ttu-id="cd721-149">Return (objeto)</span><span class="sxs-lookup"><span data-stu-id="cd721-149">Return object</span></span>**  

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, ...  ]
```  

### <a name="msedge"></a><span data-ttu-id="cd721-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="cd721-150">/msedge/</span></span>  

<span data-ttu-id="cd721-151">Funcionalmente equivalente a [/msedge/json/list](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="cd721-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span>  

### <a name="msedgepidjsonlist"></a><span data-ttu-id="cd721-152">/msedge/[pid]/json/list</span><span class="sxs-lookup"><span data-stu-id="cd721-152">/msedge/[pid]/json/list</span></span>  

<span data-ttu-id="cd721-153">Proporciona una lista candidata de destinos de página para la Microsoft Edge que coincide con la proporcionada `[pid]` para la depuración.</span><span class="sxs-lookup"><span data-stu-id="cd721-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>  

**<span data-ttu-id="cd721-154">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd721-154">Parameters</span></span>**  

**<span data-ttu-id="cd721-155">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd721-155">None</span></span>**  

**<span data-ttu-id="cd721-156">Return (objeto)</span><span class="sxs-lookup"><span data-stu-id="cd721-156">Return object</span></span>**  

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, ...  ]
```  

### <a name="msedgepidjsonversion"></a><span data-ttu-id="cd721-157">/msedge/[pid]/json/version</span><span class="sxs-lookup"><span data-stu-id="cd721-157">/msedge/[pid]/json/version</span></span>  

<span data-ttu-id="cd721-158">Proporciona información sobre la Microsoft Edge que coincide con la proporcionada y qué versión del `[pid]` protocolo DevTools admite.</span><span class="sxs-lookup"><span data-stu-id="cd721-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>  

**<span data-ttu-id="cd721-159">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd721-159">Parameters</span></span>**  

**<span data-ttu-id="cd721-160">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd721-160">None</span></span>**  

**<span data-ttu-id="cd721-161">Return (objeto)</span><span class="sxs-lookup"><span data-stu-id="cd721-161">Return object</span></span>**  

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```  

### <a name="msedgepidjsonprotocol"></a><span data-ttu-id="cd721-162">/msedge/[pid]/json/protocol/</span><span class="sxs-lookup"><span data-stu-id="cd721-162">/msedge/[pid]/json/protocol/</span></span>  

<span data-ttu-id="cd721-163">Proporciona toda la superficie de api de protocolo serializada como JSON para la Microsoft Edge que coincide con el `[pid]` proporcionado .</span><span class="sxs-lookup"><span data-stu-id="cd721-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>  

**<span data-ttu-id="cd721-164">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd721-164">Parameters</span></span>**  

**<span data-ttu-id="cd721-165">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd721-165">None</span></span>**  

**<span data-ttu-id="cd721-166">Return (objeto)</span><span class="sxs-lookup"><span data-stu-id="cd721-166">Return object</span></span>**  

<span data-ttu-id="cd721-167">Objeto JSON que representa la superficie de API disponible para la versión del protocolo que usa la instancia Microsoft Edge que coincide con la `[pid]` proporcionada.</span><span class="sxs-lookup"><span data-stu-id="cd721-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>  
