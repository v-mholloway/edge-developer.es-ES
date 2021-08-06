---
description: Introducción a la depuración remota WebViews en las aplicaciones nativas de Android con Microsoft Edge Developer Tools.
title: Introducción a la depuración remota de Android WebViews
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, desarrollo web, herramientas f12, devtools
ms.openlocfilehash: a30c4c006a8d0bb6a40d54e0821d98af77330004c0260c416e5ab3128ac47a73
ms.sourcegitcommit: 841e41de1a32501ece862399fa56170c022127c5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "11809246"
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
# <a name="get-started-with-remote-debugging-android-webviews"></a>Introducción a la depuración remota de Android WebViews  

Depuración de WebViews de Android en tus aplicaciones nativas de Android con Microsoft Edge Developer Tools.  

En Android 4.4 \(KitKat\) o posterior, usa DevTools para depurar contenido de WebView en aplicaciones nativas de Android.  

### <a name="summary"></a>Resumen  

*   Activa la depuración de Android WebView en tu aplicación nativa de Android; depurar WebViews de Android en Microsoft Edge DevTools.  
*   Para mostrar la lista de Las vistas web de Android con la depuración activada, vaya a `edge://inspect` .  
*   Depurar WebViews de Android de la misma manera que depura una página web a través [de la depuración remota][RemoteDebuggingGettingStarted].  

## <a name="configure-android-webviews-to-debug"></a>Configurar WebViews de Android para depurar  

La depuración de Android WebView debe estar activada dentro de la aplicación.  Para activar la depuración de Android WebView, ejecute el método estático [setWebContentsDebuggingEnabled][AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled] en la `WebView` clase.  

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
    WebView.setWebContentsDebuggingEnabled(true);
}
```  

La configuración se aplica a todos los WebViews de Android de la aplicación.  

> [!TIP]
> La depuración de Android WebView no se ve afectada por el estado de la `debuggable` marca en el manifiesto de la aplicación.  Si desea activar la depuración de Android WebView solo cuando la marca `debuggable` es , pruebe la marca en tiempo de `true` ejecución.  
> 
> ```java
> if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.KITKAT) {
>     if (0 != (getApplicationInfo().flags & ApplicationInfo.FLAG_DEBUGGABLE))
>    { WebView.setWebContentsDebuggingEnabled(true); }
> }
> ```  

## <a name="open-an-android-webview-in-devtools"></a>Abrir un WebView de Android en DevTools  

Para mostrar una lista de los WebView de Android con depuración activada que se ejecutan en el dispositivo, vaya a `edge://inspect` .  

Para iniciar la depuración, en Android WebView que desea depurar, elija **inspeccionar**.  Use DevTools de la misma manera que hace una pestaña del explorador remoto.  

<!--
:::image type="complex" source=".images/webview-debugging.msft.png" alt-text="Inspecting elements in an Android WebView" lightbox=".images/webview-debugging.msft.png":::
   Inspecting elements in an Android WebView  
:::image-end:::  

The gray graphics listed with the Android WebView represent its size and position relative to the screen of the device.  If your Android WebViews have titles set, the titles are listed as well.  
-->  

## <a name="troubleshoot"></a>Solucionar problemas  

¿Los WebView de Android no se muestran en la `edge://inspect` página?  

*   Compruebe que la depuración de Android WebView está activada para la aplicación.  
*   En el dispositivo, abre la aplicación con Android WebView que quieras depurar.  A continuación, actualice `edge://inspect` .  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Ponerse en contacto con el equipo de Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[RemoteDebuggingGettingStarted]: ./index.md "Introducción con dispositivos Android de depuración remota | Microsoft Docs"  

[AndroidDeveloperWebViewsSetWebContentsDebuggingEnabled]: https://developer.android.com/reference/android/webkit/WebView.html#setWebContentsDebuggingEnabled(boolean) "setWebContentsDebuggingEnabled- WebView | Desarrolladores de Android"  

> [!NOTE]
> Algunas partes de esta página son modificaciones basadas en el trabajo creado y [compartido por Google][GoogleSitePolicies] y se usan según los términos descritos en la [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  
> La página original se encuentra [aquí](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/webviews) y es creado por [Meggin Kearney][MegginKearney] \(Tech Writer\).  

[![Licencia de Creative Commons][CCby4Image]][CCA4IL]  
Este trabajo dispone de licencia conforme a [Licencia internacional de Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: http://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
