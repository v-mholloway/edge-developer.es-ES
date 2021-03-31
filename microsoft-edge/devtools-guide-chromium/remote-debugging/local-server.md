---
description: Hospedar un sitio en un servidor web de máquina de desarrollo y, a continuación, acceder al contenido desde un dispositivo Android.
title: Acceso a servidores locales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: 51ef0d951d587d310b6474698924d9f87cf68607
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461265"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="access-local-servers"></a><span data-ttu-id="6eaa2-104">Acceso a servidores locales</span><span class="sxs-lookup"><span data-stu-id="6eaa2-104">Access local servers</span></span>  

<span data-ttu-id="6eaa2-105">Host a site on a development machine web server, then access the content from an Android device.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-105">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="6eaa2-106">Con un cable USB y Microsoft Edge DevTools, ejecute un sitio desde una máquina de desarrollo y, a continuación, vea el sitio en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-106">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <a name="summary"></a><span data-ttu-id="6eaa2-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="6eaa2-107">Summary</span></span>  

*   <span data-ttu-id="6eaa2-108">El reenvío de puertos te permite ver el contenido hospedado por el servidor web que se ejecuta en el equipo de desarrollo en tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-108">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="6eaa2-109">Si el servidor web usa un dominio personalizado, configura el dispositivo Android para tener acceso al contenido de ese dominio con asignación de dominio personalizada.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-109">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <a name="set-up-port-forwarding"></a><span data-ttu-id="6eaa2-110">Configurar el reenvío de puertos</span><span class="sxs-lookup"><span data-stu-id="6eaa2-110">Set up port forwarding</span></span>  

<span data-ttu-id="6eaa2-111">El reenvío de puertos permite que el dispositivo Android obtenga acceso al contenido que se hospeda en el servidor web que se ejecuta en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-111">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="6eaa2-112">El reenvío de puertos funciona creando un puerto TCP de escucha en el dispositivo Android que se asigna a un puerto TCP en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-112">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="6eaa2-113">El tráfico entre los puertos viaja a través de la conexión USB entre el dispositivo Android y el equipo de desarrollo, por lo que la conexión no depende de la configuración de red.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-113">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="6eaa2-114">Para habilitar el reenvío de puertos:</span><span class="sxs-lookup"><span data-stu-id="6eaa2-114">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="6eaa2-115">Configura la [depuración remota entre][RemoteDebuggingGettingStarted] el equipo de desarrollo y el dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-115">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="6eaa2-116">Cuando haya terminado, el dispositivo Android debe mostrarse en  el menú izquierdo del cuadro de diálogo Inspeccionar dispositivos y un **indicador de** estado Conectado.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-116">When you are finished, your Android device should be displayed in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="6eaa2-117">En el **cuadro de diálogo Inspeccionar dispositivos** de DevTools, habilite Reenvío de **puertos**.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-117">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="6eaa2-118">Elija **Agregar regla**.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-118">Choose **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Agregar una regla de reenvío de puertos" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="6eaa2-120">Agregar una regla de reenvío de puertos</span><span class="sxs-lookup"><span data-stu-id="6eaa2-120">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="6eaa2-121">En el **cuadro de texto** Puerto de dispositivo de la izquierda, escribe el número de puerto desde el que quieres tener acceso al sitio en tu dispositivo `localhost` Android.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-121">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="6eaa2-122">Por ejemplo, si desea obtener acceso al sitio desde `localhost:5000` escriba `5000` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-122">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="6eaa2-123">En el **cuadro** de texto Dirección local de la derecha, escriba la dirección IP o el nombre de host en el que se hospeda el sitio en el servidor web que se ejecuta en el equipo de desarrollo, seguido del número de puerto.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-123">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="6eaa2-124">Por ejemplo, si el sitio se está ejecutando al `localhost:7331` escribir `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-124">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="6eaa2-125">Elija **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-125">Choose **Add**.</span></span>  
    
<span data-ttu-id="6eaa2-126">El reenvío de puertos ya está configurado.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-126">Port forwarding is now set up.</span></span>  <span data-ttu-id="6eaa2-127">Revisa el indicador de estado del puerto hacia delante en la pestaña del dispositivo en el cuadro **de diálogo Inspeccionar dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="6eaa2-127">Review the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Estado de reenvío de puertos" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="6eaa2-129">Estado de reenvío de puertos</span><span class="sxs-lookup"><span data-stu-id="6eaa2-129">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="6eaa2-130">Para ver el contenido, abra Microsoft Edge en el dispositivo Android y vaya al puerto que especificó `localhost` en el campo Puerto **de** dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-130">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="6eaa2-131">Por ejemplo, si ha escrito `5000` en el campo, visite `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-131">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <a name="map-to-custom-local-domains"></a><span data-ttu-id="6eaa2-132">Asignar a dominios locales personalizados</span><span class="sxs-lookup"><span data-stu-id="6eaa2-132">Map to custom local domains</span></span>  

<span data-ttu-id="6eaa2-133">La asignación de dominio personalizada permite ver contenido en un dispositivo Android desde un servidor web en el equipo de desarrollo que usa un dominio personalizado.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-133">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="6eaa2-134">Por ejemplo, supongamos que el sitio usa una biblioteca de JavaScript de terceros que solo funciona en el dominio `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-134">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="6eaa2-135">Por lo tanto, cree una entrada en el archivo en el equipo de desarrollo para asignar este dominio `hosts` a `localhost` \(por ejemplo, `127.0.0.1 microsoft-edge.devtools` \).</span><span class="sxs-lookup"><span data-stu-id="6eaa2-135">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="6eaa2-136">Después de configurar la asignación de dominio personalizada y el reenvío de puertos, vea el sitio en el dispositivo Android en la dirección URL `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-136">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <a name="set-up-port-forwarding-to-proxy-server"></a><span data-ttu-id="6eaa2-137">Configurar el reenvío de puertos al servidor proxy</span><span class="sxs-lookup"><span data-stu-id="6eaa2-137">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="6eaa2-138">Para asignar un dominio personalizado, debe ejecutar un servidor proxy en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-138">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="6eaa2-139">Ejemplos de servidores proxy [son Charles,][CharlesWebDebuggingProxy] [Squid][SquidOptimisingWebDelivery]y [Fiddler.][FiddlerWebDebuggingProxy]</span><span class="sxs-lookup"><span data-stu-id="6eaa2-139">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="6eaa2-140">Para configurar el reenvío de puertos a un proxy:</span><span class="sxs-lookup"><span data-stu-id="6eaa2-140">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="6eaa2-141">Ejecute el servidor proxy y registre el puerto que está usando.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-141">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6eaa2-142">El servidor proxy y el servidor web deben ejecutarse en puertos diferentes.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-142">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="6eaa2-143">Configura el [reenvío de puertos](#set-up-port-forwarding) a tu dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-143">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="6eaa2-144">Para el **campo de dirección local,** escriba seguido del puerto en el que se `localhost:` está ejecutando el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-144">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="6eaa2-145">Por ejemplo, si se está ejecutando en el puerto `8000` , vaya a `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-145">For example, if it is running on port `8000`, navigate to `localhost:8000`.</span></span>  <span data-ttu-id="6eaa2-146">En el **campo puerto del** dispositivo, escriba el número en el que desea que su dispositivo Android escuche, como `3333` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-146">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <a name="configure-proxy-settings-on-your-device"></a><span data-ttu-id="6eaa2-147">Configurar la configuración de proxy en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="6eaa2-147">Configure proxy settings on your device</span></span>  

<span data-ttu-id="6eaa2-148">A continuación, debes configurar el dispositivo Android para que se comunique con el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-148">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="6eaa2-149">En el dispositivo Android, vaya **a Configuración**  >  **Wi-Fi**.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-149">On your Android device, navigate to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="6eaa2-150">Presione durante mucho tiempo el nombre de la red a la que está conectado actualmente.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-150">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="6eaa2-151">La configuración de proxy se aplica por red.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-151">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="6eaa2-152">Elija **Modificar red**.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-152">Choose **Modify network**.</span></span>  
1.  <span data-ttu-id="6eaa2-153">Elija **Opciones avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-153">Choose **Advanced options**.</span></span>  <span data-ttu-id="6eaa2-154">Se muestra la configuración de proxy.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-154">The proxy settings display.</span></span>  
1.  <span data-ttu-id="6eaa2-155">Elija el **menú Proxy** y **elija Manual**.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-155">Choose the **Proxy** menu and choose **Manual**.</span></span>  
1.  <span data-ttu-id="6eaa2-156">Para el **campo Nombre de host** proxy, escriba `localhost` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-156">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="6eaa2-157">Para el **campo Puerto proxy,** escriba el número de puerto que escribió para el **puerto del dispositivo** en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-157">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="6eaa2-158">Elija **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-158">Choose **Save**.</span></span>  
    
<span data-ttu-id="6eaa2-159">Con esta configuración, el dispositivo reenvía todas sus solicitudes al proxy en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-159">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="6eaa2-160">El proxy realiza solicitudes en nombre de su dispositivo, por lo que las solicitudes a su dominio local personalizado se resuelven correctamente.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-160">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="6eaa2-161">Ahora, accede a dominios personalizados en tu dispositivo Android al igual que en la máquina de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-161">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="6eaa2-162">Si el servidor web se está ejecutando fuera de un puerto no estándar, recuerde especificar el puerto al solicitar el contenido desde el dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-162">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="6eaa2-163">Por ejemplo, si el servidor web usa el dominio personalizado en el puerto , cuando vea el sitio desde su dispositivo Android, debe usar `microsoft-edge.devtools` `7331` la dirección URL `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="6eaa2-163">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="6eaa2-164">Para reanudar la exploración normal, recuerda revertir la configuración de proxy en el dispositivo Android después de desconectarte del equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="6eaa2-164">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="6eaa2-165">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6eaa2-165">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introducción a la depuración remota de dispositivos Android | Microsoft Docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de depuración web de Carlos"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "squid : Optimización de la entrega web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler: proxy de depuración web gratuito"  

> [!NOTE]
> <span data-ttu-id="6eaa2-170">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6eaa2-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6eaa2-171">La página original [](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) se encuentra aquí y está redactada por [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) y [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="6eaa2-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="6eaa2-173">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6eaa2-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
