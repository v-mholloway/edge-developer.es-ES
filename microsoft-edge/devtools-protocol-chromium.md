---
description: Actualizar al protocolo Microsoft Edge DevTools
title: Actualización del protocolo Microsoft Edge DevTools
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: f1936a83f948dd17cc76139b7fd67fc73cd692d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/09/2020
ms.locfileid: "10573768"
---
# <span data-ttu-id="b2bb7-103">Protocolo de DevTools Microsoft Edge (cromo)</span><span class="sxs-lookup"><span data-stu-id="b2bb7-103">Microsoft Edge (Chromium) DevTools Protocol</span></span>

<span data-ttu-id="b2bb7-104">Con el turno de la plataforma web subyacente de Microsoft Edge a cromo, el [Protocolo DevTools de Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) no recibirá más actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) will not be receiving any further updates.</span></span> <span data-ttu-id="b2bb7-105">El protocolo de DevTools Microsoft Edge (cromo) coincidirá con las API del Protocolo de DevTools de Chrome hacia adelante.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-105">The Microsoft Edge (Chromium) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span> 

<span data-ttu-id="b2bb7-106">Puede encontrar documentación sobre esos dominios y métodos en el [visor de protocolos de Chrome DevTools](https://chromedevtools.github.io/devtools-protocol/tot/).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot/).</span></span>

> [!NOTE]
> <span data-ttu-id="b2bb7-107">Los métodos con el prefijo `ms` en el [Protocolo DevTools de Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) ya no se admiten en el protocolo de DevTools Microsoft Edge (cromo).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) are no longer supported in the Microsoft Edge (Chromium) DevTools Protocol.</span></span>

## <span data-ttu-id="b2bb7-108">Usar el protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="b2bb7-108">Using the DevTools Protocol</span></span>

<span data-ttu-id="b2bb7-109">A continuación se explica cómo adjuntar un cliente de herramientas personalizado al servidor de DevTools en Microsoft Edge (cromo).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge (Chromium).</span></span>

1. <span data-ttu-id="b2bb7-110">Asegúrate de que todas las instancias de Microsoft Edge (cromo) estén cerradas.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-110">Ensure all instances of Microsoft Edge (Chromium) are closed.</span></span>

2. <span data-ttu-id="b2bb7-111">Inicia Microsoft Edge (cromo) con el puerto de depuración remota:</span><span class="sxs-lookup"><span data-stu-id="b2bb7-111">Launch Microsoft Edge (Chromium) with the remote debugging port:</span></span>

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. <span data-ttu-id="b2bb7-112">De manera opcional, puede iniciar una instancia independiente de Edge con un perfil de usuario distinto si lo desea:</span><span class="sxs-lookup"><span data-stu-id="b2bb7-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired:</span></span>

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. <span data-ttu-id="b2bb7-113">A continuación, use el `list` punto de conexión http para obtener una lista de destinos de página que se puede adjuntar:</span><span class="sxs-lookup"><span data-stu-id="b2bb7-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets:</span></span>

    ```
    http://localhost:9222/json/list
    ```

5. <span data-ttu-id="b2bb7-114">Por último, conéctese a los `webSocketDebuggerUrl` comandos de destino y de salida deseados/suscribirse a los mensajes de eventos a través del servidor de socket web DevTools.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>

## <span data-ttu-id="b2bb7-115">Puntos de conexión HTTP del protocolo DevTools</span><span class="sxs-lookup"><span data-stu-id="b2bb7-115">DevTools Protocol HTTP Endpoints</span></span>

<span data-ttu-id="b2bb7-116">El protocolo de DevTools Microsoft Edge (cromo) admite los siguientes puntos de conexión HTTP.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-116">The Microsoft Edge (Chromium) DevTools Protocol supports the following HTTP endpoints.</span></span>

## <span data-ttu-id="b2bb7-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="b2bb7-117">/json/version</span></span>
<span data-ttu-id="b2bb7-118">Proporciona información sobre el explorador del equipo host y la versión del protocolo DevTools que admite.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-118">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="b2bb7-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2bb7-119">Parameters</span></span>**

*<span data-ttu-id="b2bb7-120">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2bb7-120">None</span></span>*

**<span data-ttu-id="b2bb7-121">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bb7-121">Return object</span></span>**

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

## <span data-ttu-id="b2bb7-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="b2bb7-122">/json/protocol</span></span>

<span data-ttu-id="b2bb7-123">Proporciona toda la superficie de la API de protocolo serializada como JSON.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-123">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="b2bb7-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2bb7-124">Parameters</span></span>**

*<span data-ttu-id="b2bb7-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2bb7-125">None</span></span>*

**<span data-ttu-id="b2bb7-126">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bb7-126">Return object</span></span>**

<span data-ttu-id="b2bb7-127">Objeto JSON que representa la superficie de API disponible para la versión actual del protocolo.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-127">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="b2bb7-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="b2bb7-128">/json/list</span></span>

<span data-ttu-id="b2bb7-129">Proporciona una lista de candidatos de los destinos de página para la depuración.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-129">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="b2bb7-130">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2bb7-130">Parameters</span></span>**

*<span data-ttu-id="b2bb7-131">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2bb7-131">None</span></span>*

**<span data-ttu-id="b2bb7-132">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bb7-132">Return object</span></span>**

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, … ]
```

## <span data-ttu-id="b2bb7-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="b2bb7-133">/json/close</span></span>

<span data-ttu-id="b2bb7-134">Cierra el proceso de destino (por ejemplo, en Microsoft Edge (cromo), cierra la pestaña de la página).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-134">Closes down the target process (e.g., in Microsoft Edge (Chromium), closes the page tab.)</span></span>

**<span data-ttu-id="b2bb7-135">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2bb7-135">Parameters</span></span>**

<span data-ttu-id="b2bb7-136">IDENTIFICADOR de destino</span><span class="sxs-lookup"><span data-stu-id="b2bb7-136">Target ID</span></span> 

**<span data-ttu-id="b2bb7-137">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bb7-137">Return object</span></span>**

```
String(“Target is closing”)
```

## <span data-ttu-id="b2bb7-138">Herramientas remotas para Microsoft Edge (beta)</span><span class="sxs-lookup"><span data-stu-id="b2bb7-138">Remote Tools for Microsoft Edge (Beta)</span></span>

<span data-ttu-id="b2bb7-139">Ahora puede instalar las [herramientas remotas de Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) desde [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span> <span data-ttu-id="b2bb7-140">Esta aplicación te permite depurar de forma remota Microsoft Edge (cromo) en un dispositivo con Windows 10 de tu equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>

<span data-ttu-id="b2bb7-141">Para obtener información sobre cómo configurar su dispositivo Windows 10 y conectarse a él desde su equipo de desarrollo, consulte [este tutorial](./devtools-guide-chromium/remote-debugging/windows.md).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-141">To learn how to set up your Windows 10 device and connect to it from your development machine, check out [this tutorial](./devtools-guide-chromium/remote-debugging/windows.md).</span></span>

<span data-ttu-id="b2bb7-142">Las [herramientas remotas para Microsoft Edge (beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) usan el mismo protocolo de DevTools de Microsoft Edge (cromo) que el [DevTools](./devtools-guide-chromium.md) para comunicarse con Microsoft Edge que se ejecuta en el dispositivo de Windows 10 que desea depurar.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](./devtools-guide-chromium.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span> <span data-ttu-id="b2bb7-143">Esta aplicación simplemente antepone `/msedge/` un identificador de proceso ( `pid` ) antes de cada llamada al Protocolo.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span> <span data-ttu-id="b2bb7-144">Es compatible con los siguientes puntos de conexión HTTP.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-144">It supports the following HTTP endpoints.</span></span>

### <span data-ttu-id="b2bb7-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="b2bb7-145">/msedge/json/list</span></span>

<span data-ttu-id="b2bb7-146">Proporciona una lista de candidatos de todos los `msedge.exe` procesos (incluidos [PWAs](./progressive-web-apps-chromium/index.md) y todas las pestañas de todas las instancias de Microsoft Edge) en el dispositivo Windows 10 para la depuración.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-146">Provides a candidate list of all `msedge.exe` processes (including [PWAs](./progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge) on the Windows 10 device for debugging.</span></span>

**<span data-ttu-id="b2bb7-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2bb7-147">Parameters</span></span>**

*<span data-ttu-id="b2bb7-148">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2bb7-148">None</span></span>*

**<span data-ttu-id="b2bb7-149">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bb7-149">Return object</span></span>**

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
}, … ]
```

### <span data-ttu-id="b2bb7-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="b2bb7-150">/msedge/</span></span>

<span data-ttu-id="b2bb7-151">Funcionalmente equivalente a [/msedge/JSON/List](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="b2bb7-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span> 

### <span data-ttu-id="b2bb7-152">/msedge/[PID]/JSON/List</span><span class="sxs-lookup"><span data-stu-id="b2bb7-152">/msedge/[pid]/json/list</span></span>

<span data-ttu-id="b2bb7-153">Proporciona una lista de candidatos de destinos de página para la instancia de Microsoft Edge que coincide con la proporcionada `[pid]` para la depuración.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>

**<span data-ttu-id="b2bb7-154">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2bb7-154">Parameters</span></span>**

*<span data-ttu-id="b2bb7-155">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2bb7-155">None</span></span>*

**<span data-ttu-id="b2bb7-156">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bb7-156">Return object</span></span>**

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
}, … ]
```

### <span data-ttu-id="b2bb7-157">/msedge/[PID]/JSON/version</span><span class="sxs-lookup"><span data-stu-id="b2bb7-157">/msedge/[pid]/json/version</span></span>

<span data-ttu-id="b2bb7-158">Proporciona información sobre la instancia de Microsoft Edge que coincide con el proporcionado `[pid]` y la versión del protocolo DevTools que admite.</span><span class="sxs-lookup"><span data-stu-id="b2bb7-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="b2bb7-159">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2bb7-159">Parameters</span></span>**

*<span data-ttu-id="b2bb7-160">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2bb7-160">None</span></span>*

**<span data-ttu-id="b2bb7-161">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bb7-161">Return object</span></span>**

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

### <span data-ttu-id="b2bb7-162">/msedge/[PID]/JSON/Protocol/</span><span class="sxs-lookup"><span data-stu-id="b2bb7-162">/msedge/[pid]/json/protocol/</span></span>

<span data-ttu-id="b2bb7-163">Proporciona toda la superficie de la API de protocolo serializada como JSON para la instancia de Microsoft Edge que coincide con el proporcionado `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="b2bb7-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>

**<span data-ttu-id="b2bb7-164">Parameters</span><span class="sxs-lookup"><span data-stu-id="b2bb7-164">Parameters</span></span>**

*<span data-ttu-id="b2bb7-165">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b2bb7-165">None</span></span>*

**<span data-ttu-id="b2bb7-166">Objeto devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bb7-166">Return object</span></span>**

<span data-ttu-id="b2bb7-167">Objeto JSON que representa la superficie de API disponible para la versión del protocolo que usa la instancia de Microsoft Edge que coincide con el proporcionado `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="b2bb7-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>
