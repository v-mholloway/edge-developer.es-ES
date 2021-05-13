---
description: Introducción a la depuración remota WebViews en las aplicaciones nativas de Android con Microsoft Edge Developer Tools.
title: Introducción a la depuración remota de Android WebViews
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, desarrollo web, herramientas F12, DevTools
ms.openlocfilehash: 75d948465c62c63c9ccbe0fcd46616819a04e79d
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565081"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="get-started-with-remote-debugging-android-webviews"></a><span data-ttu-id="d8c70-104">Introducción a la depuración remota de Android WebViews</span><span class="sxs-lookup"><span data-stu-id="d8c70-104">Get started with remote debugging Android WebViews</span></span>  

<span data-ttu-id="d8c70-105">Depuración de WebViews de Android en tus aplicaciones nativas de Android con Microsoft Edge Developer Tools.</span><span class="sxs-lookup"><span data-stu-id="d8c70-105">Debug Android WebViews in your native Android apps using Microsoft Edge Developer Tools.</span></span>  

<span data-ttu-id="d8c70-106">En Android 4.4 \(KitKat\) o posterior, usa DevTools para depurar contenido de WebView en aplicaciones nativas de Android.</span><span class="sxs-lookup"><span data-stu-id="d8c70-106">On Android 4.4 \(KitKat\) or later, use DevTools to debug WebView content in native Android apps.</span></span>  

### <a name="summary"></a><span data-ttu-id="d8c70-107">Resumen</span><span class="sxs-lookup"><span data-stu-id="d8c70-107">Summary</span></span>  

*   <span data-ttu-id="d8c70-108">Activa la depuración de Android WebView en tu aplicación nativa de Android; depurar WebViews de Android en Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="d8c70-108">Turn on Android WebView debugging in your native Android app; debug Android WebViews in Microsoft Edge DevTools.</span></span>  
*   <span data-ttu-id="d8c70-109">Para mostrar la lista de Las vistas web de Android con la depuración activada, vaya a `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="d8c70-109">To display the list of the Android WebViews with debugging turned on, navigate to `edge://inspect`.</span></span>  
*   <span data-ttu-id="d8c70-110">Depurar WebViews de Android de la misma manera que depura una página web a través [de la depuración remota][RemoteDebuggingGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="d8c70-110">Debug Android WebViews in the same way you debug a webpage through [remote debugging][RemoteDebuggingGettingStarted].</span></span>  

## <a name="configure-android-webviews-to-debug"></a><span data-ttu-id="d8c70-111">Configurar WebViews de Android para depurar</span><span class="sxs-lookup"><span data-stu-id="d8c70-111">Configure Android WebViews to debug</span></span>  

<span data-ttu-id="d8c70-112">La depuración de Android WebView debe estar activada dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8c70-112">Android WebView debugging must be turned on within your app.</span></span>  <span data-ttu-id="d8c70-113">Para activar la depuración de Android WebView, ejecute el método estático [setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] en la `WebView` clase.</span><span class="sxs-lookup"><span data-stu-id="d8c70-113">To turn on Android WebView debugging, run the [setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] static method on the `WebView` class.</span></span>  

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```  

<span data-ttu-id="d8c70-114">La configuración se aplica a todos los WebViews de Android de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8c70-114">The setting applies to all of the Android WebViews of the app.</span></span>  

> [!TIP]
> <span data-ttu-id="d8c70-115">La depuración de Android WebView no se ve afectada por el estado de la `debuggable` marca en el manifiesto de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8c70-115">Android WebView debugging is not affected by the state of the `debuggable` flag in the manifest of the app.</span></span>  <span data-ttu-id="d8c70-116">Si desea activar la depuración de Android WebView solo cuando la marca `debuggable` es , pruebe la marca en tiempo de `true` ejecución.</span><span class="sxs-lookup"><span data-stu-id="d8c70-116">If you want to turn on Android WebView debugging only when the `debuggable` flag is `true`, test the flag at runtime.</span></span>  
> 
> ```java
> if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
>     if (0 != (getApplicationInfo().flags & ApplicationInfo.FLAG_DEBUGGABLE))
>    { WebView.setWebContentsDebuggingEnabled(true); }
> }
> ```  

## <a name="open-an-android-webview-in-devtools"></a><span data-ttu-id="d8c70-117">Abrir un WebView de Android en DevTools</span><span class="sxs-lookup"><span data-stu-id="d8c70-117">Open an Android WebView in DevTools</span></span>  

<span data-ttu-id="d8c70-118">Para mostrar una lista de los WebView de Android con depuración activada que se ejecutan en el dispositivo, vaya a `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="d8c70-118">To display a list of the Android WebViews with debugging turned on that run on your device, navigate to `edge://inspect`.</span></span>  

<span data-ttu-id="d8c70-119">Para iniciar la depuración, en Android WebView que desea depurar, elija **inspeccionar**.</span><span class="sxs-lookup"><span data-stu-id="d8c70-119">To start debugging, under the Android WebView you want to debug, choose **inspect**.</span></span>  <span data-ttu-id="d8c70-120">Use DevTools de la misma manera que hace una pestaña del explorador remoto.</span><span class="sxs-lookup"><span data-stu-id="d8c70-120">Use DevTools in the same way that you do a remote browser tab.</span></span>  

<!--
:::image type="complex" source=".images/webview-debugging.msft.png" alt-text="Inspecting elements in an Android WebView" lightbox=".images/webview-debugging.msft.png":::
   Inspecting elements in an Android WebView  
:::image-end:::  

The gray graphics listed with the Android WebView represent its size and position relative to the screen of the device.  If your Android WebViews have titles set, the titles are listed as well.  
-->  

## <a name="troubleshoot"></a><span data-ttu-id="d8c70-121">Solucionar problemas</span><span class="sxs-lookup"><span data-stu-id="d8c70-121">Troubleshoot</span></span>  

<span data-ttu-id="d8c70-122">¿Los WebView de Android no se muestran en la `edge://inspect` página?</span><span class="sxs-lookup"><span data-stu-id="d8c70-122">Your Android WebViews aren't displayed on the `edge://inspect` page?</span></span>  

*   <span data-ttu-id="d8c70-123">Compruebe que la depuración de Android WebView está activada para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8c70-123">Verify that Android WebView debugging is turned on for your app.</span></span>  
*   <span data-ttu-id="d8c70-124">En el dispositivo, abre la aplicación con Android WebView que quieras depurar.</span><span class="sxs-lookup"><span data-stu-id="d8c70-124">On your device, open the app with the Android WebView you want to debug.</span></span>  <span data-ttu-id="d8c70-125">A continuación, actualice `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="d8c70-125">Then, refresh `edge://inspect`.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="d8c70-126">Contactar al equipo de Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d8c70-126">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introducción con dispositivos Android de depuración remota | Microsoft Docs"  

[AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled]: https://developer.android.com/reference/android/webkit/WebView.html#setWebContentsDebuggingEnabled(boolean) "setWebContentsDebuggingEnabled- WebView | Desarrolladores de Android"  

> [!NOTE]
> <span data-ttu-id="d8c70-129">Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d8c70-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d8c70-130">La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) y es creado por [Meggin Kearney][MegginKearney] \(Tech Writer\).</span><span class="sxs-lookup"><span data-stu-id="d8c70-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d8c70-132">Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d8c70-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: http://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
