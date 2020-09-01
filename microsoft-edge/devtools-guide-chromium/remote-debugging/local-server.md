---
title: Acceso a servidores locales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: fb8f8aabaf426685417f90e25295f3e8e7b08994
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984916"
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





# <span data-ttu-id="edfa1-103">Servidores locales de Access</span><span class="sxs-lookup"><span data-stu-id="edfa1-103">Access local servers</span></span>   




<span data-ttu-id="edfa1-104">Hospede un sitio en un servidor Web de equipo de desarrollo y, a continuación, obtenga acceso al contenido desde un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="edfa1-104">Host a site on a development machine web server, then access the content from an Android device.</span></span>  

<span data-ttu-id="edfa1-105">Con un cable USB y Microsoft Edge DevTools, ejecute un sitio desde un equipo de desarrollo y, después, vea el sitio en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="edfa1-105">With a USB cable and Microsoft Edge DevTools, run a site from a development machine and then view the site on an Android device.</span></span>  

### <span data-ttu-id="edfa1-106">Resumen</span><span class="sxs-lookup"><span data-stu-id="edfa1-106">Summary</span></span>  

*   <span data-ttu-id="edfa1-107">El reenvío de puertos le permite ver el contenido hospedado en el servidor Web que se está ejecutando en el equipo de desarrollo de su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="edfa1-107">Port forwarding enables you to view content hosted by the web server running in your development machine on your Android device.</span></span>  
*   <span data-ttu-id="edfa1-108">Si su servidor web está usando un dominio personalizado, configure su dispositivo Android para obtener acceso al contenido de ese dominio con asignación de dominio personalizada.</span><span class="sxs-lookup"><span data-stu-id="edfa1-108">If your web server is using a custom domain, set up your Android device to access the content at that domain with custom domain mapping.</span></span>  

## <span data-ttu-id="edfa1-109">Configurar el reenvío de Puerto</span><span class="sxs-lookup"><span data-stu-id="edfa1-109">Set up port forwarding</span></span>   

<span data-ttu-id="edfa1-110">El reenvío de puertos permite que su dispositivo Android obtenga acceso al contenido que se hospeda en el servidor Web que se ejecuta en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="edfa1-110">Port forwarding enables your Android device to access content that is being hosted on the web server running in your development machine.</span></span>  <span data-ttu-id="edfa1-111">El reenvío de puertos funciona creando un puerto TCP de escucha en el dispositivo Android que se asigna a un puerto TCP en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="edfa1-111">Port forwarding works by creating a listening TCP port on your Android device that maps to a TCP port on your development machine.</span></span>  <span data-ttu-id="edfa1-112">El tráfico entre los puertos viaja a través de la conexión USB entre el dispositivo Android y el equipo de desarrollo, de modo que la conexión no depende de la configuración de la red.</span><span class="sxs-lookup"><span data-stu-id="edfa1-112">Traffic between the ports travel through the USB connection between your Android device and development machine, so the connection does not depend on your network configuration.</span></span>  

<span data-ttu-id="edfa1-113">Para habilitar el reenvío de puerto:</span><span class="sxs-lookup"><span data-stu-id="edfa1-113">To enable port forwarding:</span></span>  

1.  <span data-ttu-id="edfa1-114">Configure la [depuración remota][RemoteDebuggingGettingStarted] entre el equipo de desarrollo y el dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="edfa1-114">Set up [remote debugging][RemoteDebuggingGettingStarted] between your development machine and your Android device.</span></span>  <span data-ttu-id="edfa1-115">Cuando haya terminado, debe ver el dispositivo Android en el menú de la izquierda del cuadro de diálogo **inspeccionar dispositivos** y un indicador de estado **conectado** .</span><span class="sxs-lookup"><span data-stu-id="edfa1-115">When you are finished, you should see your Android device in the left-hand menu of the **Inspect Devices** dialog and a **Connected** status indicator.</span></span>  
1.  <span data-ttu-id="edfa1-116">En el cuadro de diálogo **inspeccionar dispositivos** de DevTools, habilite el **reenvío de Puerto**.</span><span class="sxs-lookup"><span data-stu-id="edfa1-116">In the **Inspect Devices** dialog in DevTools, enable **Port forwarding**.</span></span>  
1.  <span data-ttu-id="edfa1-117">Seleccione **Agregar regla**.</span><span class="sxs-lookup"><span data-stu-id="edfa1-117">Select **Add rule**.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png" alt-text="Agregar una regla de reenvío de Puerto" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-add-rule.msft.png":::
       <span data-ttu-id="edfa1-119">Agregar una regla de reenvío de Puerto</span><span class="sxs-lookup"><span data-stu-id="edfa1-119">Adding a port forwarding rule</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="edfa1-120">En el cuadro de texto **Puerto de dispositivo** de la izquierda, escriba el `localhost` número de puerto desde el que desea poder obtener acceso al sitio en su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="edfa1-120">In the **Device port** textbox on the left, enter the `localhost` port number from which you want to be able to access the site on your Android device.</span></span>  <span data-ttu-id="edfa1-121">Por ejemplo, si desea obtener acceso al sitio desde `localhost:5000` entrar `5000` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-121">For example, if you wanted to access the site from `localhost:5000` enter `5000`.</span></span>  
1.  <span data-ttu-id="edfa1-122">En el cuadro de texto **dirección local** de la derecha, escriba la dirección IP o el nombre de host en el que su sitio está hospedado en el servidor Web que se ejecuta en el equipo de desarrollo, seguido del número de puerto.</span><span class="sxs-lookup"><span data-stu-id="edfa1-122">In the **Local address** textbox on the right, enter the IP address or hostname on which your site is hosted on the web server running in your development machine, followed by the port number.</span></span>  <span data-ttu-id="edfa1-123">Por ejemplo, si su sitio se ejecuta en `localhost:7331` entrar `localhost:7331` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-123">For example, if your site is running on `localhost:7331` enter `localhost:7331`.</span></span>  
1.  <span data-ttu-id="edfa1-124">Seleccione **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="edfa1-124">Select **Add**.</span></span>  
    
<span data-ttu-id="edfa1-125">El reenvío de puertos ya está configurado.</span><span class="sxs-lookup"><span data-stu-id="edfa1-125">Port forwarding is now set up.</span></span>  <span data-ttu-id="edfa1-126">En el cuadro de diálogo **inspeccionar dispositivos** , vea el indicador de estado para el puerto hacia adelante en la ficha de su dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edfa1-126">See the status indicator for the port forward on the tab on your device within the **Inspect Devices** dialog.</span></span>  

:::image type="complex" source="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png" alt-text="Estado de reenvío de Puerto" lightbox="../media/remote-debugging-remote-devices-devices-port-forwarding-5000-edge-user-agent.msft.png":::
   <span data-ttu-id="edfa1-128">Estado de reenvío de Puerto</span><span class="sxs-lookup"><span data-stu-id="edfa1-128">Port forwarding status</span></span>  
:::image-end:::  

<span data-ttu-id="edfa1-129">Para ver el contenido, abra Microsoft Edge en su dispositivo Android y vaya al `localhost` Puerto que especificó en el campo **Puerto del dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="edfa1-129">To view the content, open up Microsoft Edge on your Android device and go to the `localhost` port that you specified in the **Device port** field.</span></span>  <span data-ttu-id="edfa1-130">Por ejemplo, si escribió `5000` en el campo, visite `localhost:5000` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-130">For example, if you entered `5000` in the field, visit `localhost:5000`.</span></span>  

## <span data-ttu-id="edfa1-131">Asignar a dominios locales personalizados</span><span class="sxs-lookup"><span data-stu-id="edfa1-131">Map to custom local domains</span></span>   

<span data-ttu-id="edfa1-132">La asignación de dominios personalizada le permite ver el contenido en un dispositivo Android desde un servidor Web en el equipo de desarrollo que usa un dominio personalizado.</span><span class="sxs-lookup"><span data-stu-id="edfa1-132">Custom domain mapping enables you to view content on an Android device from a web server on your development machine that is using a custom domain.</span></span>  

<span data-ttu-id="edfa1-133">Por ejemplo, supongamos que su sitio usa una biblioteca de JavaScript de terceros que solo funciona en el dominio `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-133">For example, suppose that your site uses a third-party JavaScript library that only works on the domain `microsoft-edge.devtools`.</span></span>  <span data-ttu-id="edfa1-134">Por lo tanto, puede crear una entrada en el `hosts` archivo en el equipo de desarrollo para asignar este dominio a `localhost` \ (por ejemplo, `127.0.0.1 microsoft-edge.devtools` \).</span><span class="sxs-lookup"><span data-stu-id="edfa1-134">So, you create an entry in your `hosts` file on your development machine to map this domain to `localhost` \(for example, `127.0.0.1 microsoft-edge.devtools`\).</span></span>  <span data-ttu-id="edfa1-135">Después de configurar la asignación de dominios y el reenvío de puertos personalizados, vea el sitio en su dispositivo Android en la dirección URL `microsoft-edge.devtools` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-135">After setting up custom domain mapping and port forwarding, view the site on your Android device at the URL `microsoft-edge.devtools`.</span></span>  

### <span data-ttu-id="edfa1-136">Configurar el desvío de puertos para el servidor proxy</span><span class="sxs-lookup"><span data-stu-id="edfa1-136">Set up port forwarding to proxy server</span></span>  

<span data-ttu-id="edfa1-137">Para asignar un dominio personalizado, debe ejecutar un servidor proxy en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="edfa1-137">To map a custom domain you must run a proxy server on your development machine.</span></span>  <span data-ttu-id="edfa1-138">Ejemplos de servidores proxy son [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery]y [Fiddler][FiddlerWebDebuggingProxy].</span><span class="sxs-lookup"><span data-stu-id="edfa1-138">Examples of proxy servers are [Charles][CharlesWebDebuggingProxy], [Squid][SquidOptimisingWebDelivery], and [Fiddler][FiddlerWebDebuggingProxy].</span></span>  

<span data-ttu-id="edfa1-139">Para configurar el reenvío de puertos a un proxy:</span><span class="sxs-lookup"><span data-stu-id="edfa1-139">To set up port forwarding to a proxy:</span></span>  

1.  <span data-ttu-id="edfa1-140">Ejecute el servidor proxy y grabe el puerto que está usando.</span><span class="sxs-lookup"><span data-stu-id="edfa1-140">Run the proxy server and record the port that it is using.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="edfa1-141">El servidor proxy y el servidor Web deben ejecutarse en puertos diferentes.</span><span class="sxs-lookup"><span data-stu-id="edfa1-141">The proxy server and your web server must run on different ports.</span></span>  
    
1.  <span data-ttu-id="edfa1-142">Configure el [reenvío de Puerto](#set-up-port-forwarding) a su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="edfa1-142">Set up [port forwarding](#set-up-port-forwarding) to your Android device.</span></span>  <span data-ttu-id="edfa1-143">En el campo **dirección local** , escriba `localhost:` seguido del puerto en el que se está ejecutando el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="edfa1-143">For the **local address** field, enter `localhost:` followed by the port that your proxy server is running on.</span></span>  <span data-ttu-id="edfa1-144">Por ejemplo, si se está ejecutando en el puerto `8000` , visite `localhost:8000` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-144">For example, if it is running on port `8000`, visit `localhost:8000`.</span></span>  <span data-ttu-id="edfa1-145">En el campo **Puerto del dispositivo** , escriba el número en el que desea que escuche el dispositivo Android, como `3333` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-145">In the **device port** field enter the number that you want your Android device to listen on, such as `3333`.</span></span>  
    
### <span data-ttu-id="edfa1-146">Establecer la configuración de proxy en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="edfa1-146">Configure proxy settings on your device</span></span>  

<span data-ttu-id="edfa1-147">A continuación, debe configurar su dispositivo Android para comunicarse con el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="edfa1-147">Next, you need to configure your Android device to communicate with the proxy server.</span></span>  

1.  <span data-ttu-id="edfa1-148">En su dispositivo Android, vaya a **configuración**  >  **WiFi**.</span><span class="sxs-lookup"><span data-stu-id="edfa1-148">On your Android device go to **Settings** > **Wi-Fi**.</span></span>  
1.  <span data-ttu-id="edfa1-149">Pulse el nombre de la red a la que está conectado en ese momento.</span><span class="sxs-lookup"><span data-stu-id="edfa1-149">Long-press the name of the network to which you are currently connected.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="edfa1-150">Se aplica la configuración de proxy por red.</span><span class="sxs-lookup"><span data-stu-id="edfa1-150">Proxy settings apply per network.</span></span>  
    
1.  <span data-ttu-id="edfa1-151">Seleccione **modificar red**.</span><span class="sxs-lookup"><span data-stu-id="edfa1-151">Select **Modify network**.</span></span>  
1.  <span data-ttu-id="edfa1-152">Seleccione **Opciones avanzadas**.</span><span class="sxs-lookup"><span data-stu-id="edfa1-152">Select **Advanced options**.</span></span>  <span data-ttu-id="edfa1-153">Se muestra la configuración de proxy.</span><span class="sxs-lookup"><span data-stu-id="edfa1-153">The proxy settings display.</span></span>  
1.  <span data-ttu-id="edfa1-154">Seleccione el menú **proxy** y seleccione **manual**.</span><span class="sxs-lookup"><span data-stu-id="edfa1-154">Select the **Proxy** menu and select **Manual**.</span></span>  
1.  <span data-ttu-id="edfa1-155">En el campo **nombre de host del proxy** , escriba `localhost` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-155">For the **Proxy hostname** field, enter `localhost`.</span></span>  
1.  <span data-ttu-id="edfa1-156">En el campo **Puerto proxy** , escriba el número de puerto que escribió para **Puerto de dispositivo** en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="edfa1-156">For the **Proxy port** field, enter the port number that you entered for **device port** in the previous section.</span></span>  
1.  <span data-ttu-id="edfa1-157">Selecciona **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="edfa1-157">Select **Save**.</span></span>  
    
<span data-ttu-id="edfa1-158">Con esta configuración, el dispositivo reenvía todas sus solicitudes al proxy en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="edfa1-158">With these settings, your device forwards all of its requests to the proxy on your development machine.</span></span>  <span data-ttu-id="edfa1-159">El proxy realiza solicitudes en nombre de su dispositivo, de modo que las solicitudes a su dominio local personalizado se resuelvan correctamente.</span><span class="sxs-lookup"><span data-stu-id="edfa1-159">The proxy makes requests on behalf of your device, so requests to your customized local domain are properly resolved.</span></span>  

<span data-ttu-id="edfa1-160">Ahora, obtenga acceso a los dominios personalizados de su dispositivo Android como en el equipo de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="edfa1-160">Now access custom domains on your Android device just like on the development machine.</span></span>  

<span data-ttu-id="edfa1-161">Si su servidor Web se está ejecutando fuera de un puerto no estándar, recuerde especificar el puerto al solicitar el contenido de su dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="edfa1-161">If your web server is running off of a non-standard port, remember to specify the port when requesting the content from your Android device.</span></span>  <span data-ttu-id="edfa1-162">Por ejemplo, si su servidor web está usando el dominio personalizado `microsoft-edge.devtools` en el puerto `7331` , al ver el sitio desde su dispositivo Android debe usar la dirección URL `microsoft-edge.devtools:7331` .</span><span class="sxs-lookup"><span data-stu-id="edfa1-162">For example, if your web server is using the custom domain `microsoft-edge.devtools` on port `7331`, when you view the site from your Android device you should be using the URL `microsoft-edge.devtools:7331`.</span></span>  

> [!TIP]
> <span data-ttu-id="edfa1-163">Para reanudar la exploración normal, recuerde revertir la configuración del proxy en su dispositivo Android después de desconectarse de la máquina de desarrollo.</span><span class="sxs-lookup"><span data-stu-id="edfa1-163">To resume normal browsing, remember to revert the proxy settings on your Android device after you disconnect from the development machine.</span></span>  

<!--  
  


-->  
<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introducción a la depuración remota dispositivos Android | Microsoft docs"  

[CharlesWebDebuggingProxy]: https://www.charlesproxy.com "Proxy de depuración web de Charles"  

[SquidOptimisingWebDelivery]: https://www.squid-cache.org "Squid: optimizar la entrega en la web"  

[FiddlerWebDebuggingProxy]: https://www.telerik.com/fiddler "Fiddler: proxy de depuración web gratuito"  

> [!NOTE]
> <span data-ttu-id="edfa1-168">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según las condiciones descritas en la [licencia internacional de Creative Commons Atribution 4,0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="edfa1-168">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="edfa1-169">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) y está modificada por [Kayce vascos][KayceBasques] \ (redactor técnico, Chrome DevTools \ & Lighthouse \) y [Meggin Kearney][MegginKearney] \ (Tech Writer \).</span><span class="sxs-lookup"><span data-stu-id="edfa1-169">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/local-server) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="edfa1-171">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="edfa1-171">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
