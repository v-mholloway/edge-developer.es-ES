---
description: Modelos de versión usados para Microsoft Edge WebView2
title: Comprender las versiones de SDK de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/03/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, controlador de explorador, edge html
ms.openlocfilehash: 5461d752164b2af49c7104e3008166ce8abbbaea
ms.sourcegitcommit: 01ed086305c06b4e3a0436586524986700276148
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "11893572"
---
# <a name="understand-webview2-sdk-versions"></a>Comprender las versiones de SDK de WebView2

El NuGet para el SDK de WebView2 contiene una versión y un paquete de versión preliminar.  Use un SDK de versión preliminar con un canal de vista previa de Microsoft Edge o use un SDK de versión con WebView2 Runtime.

_Versión preliminar_ Los paquetes de SDK se usan durante el desarrollo si quieres probar las API webView2 más recientes, incluidas las API experimentales, antes de agregar compatibilidad con esas API al tiempo de ejecución.  Se recomienda el canal canary, ya que tiene las implementaciones de las API más recientes.  Cuando desee probar y usar API experimentales de WebView2, use la siguiente combinación:
*   Una _versión preliminar del_ SDK de WebView2.
*   Un _canal de vista_ previa de Microsoft Edge en el cliente de desarrollo.

_Versión_ Los paquetes de SDK solo contienen API estables, no API experimentales.  Cuando estés trabajando en una versión de producción de la aplicación WebView2, usa la siguiente combinación:
*   Una _versión_ de lanzamiento del SDK de WebView2.
*   Tiempo de __ ejecución de WebView2 en el cliente de desarrollo.

A continuación se proporciona más información sobre los paquetes de SDK de versión preliminar y versión.


## <a name="use-a-prerelease-version-of-the-sdk-along-with-a-preview-channel-of-microsoft-edge"></a>Use una versión preliminar del SDK junto con un canal de vista previa de Microsoft Edge

Al desarrollar una aplicación Evergreen WebView2, pruebe regularmente la aplicación con el canal de vista previa Microsoft Edge versión preliminar más reciente, además de realizar pruebas con El tiempo de ejecución de WebView2.  Dado que la plataforma web está en constante evolución, las pruebas periódicas son la mejor manera de garantizar que la aplicación siga funcionando según lo previsto.

Cuando use un paquete de _versión_ preliminar del SDK de WebView2, use un canal Microsoft Edge vista previa en el cliente de desarrollo.  Los canales de vista previa también se _denominan canales Insiders._  El canal de vista previa de Canary se recomienda en lugar de Beta o Dev, ya que Canary es el más reciente y tiene implementaciones de las API experimentales más recientes.

El paquete _de versión_ preliminar del SDK es un superconjunto del paquete de versión del SDK, con firmas de método para más, [API experimentales.](#experimental-apis)  Los canales de vista previa proporcionan las implementaciones de las API experimentales de WebView2.  Las API experimentales están sujetas a cambios en función de sus comentarios.  Evite usar el paquete de versión preliminar del SDK para crear aplicaciones de producción.

Para obtener información sobre cómo apuntar temporalmente la aplicación a un canal de vista previa en lugar de pasar al tiempo de ejecución de WebView2, vaya [a Cambiar a][SetPreviewChannel]un canal de vista previa para probar las próximas API y características .


## <a name="use-a-release-version-of-the-sdk-along-with-the-runtime"></a>Usar una versión de lanzamiento del SDK junto con el tiempo de ejecución

Cuando use un paquete de versión del _SDK_ de WebView2, use El tiempo de ejecución de WebView2 _Evergreen_ en el cliente de desarrollo, en lugar de un Microsoft Edge versión preliminar.  De forma predeterminada, una aplicación WebView2 está dirigida al runtime en lugar de Microsoft Edge.  Por diseño, el Microsoft Edge stable no admite WebView2.

El paquete _de versión del_ SDK contiene todas las API estables de Win32 C/C++ y .NET, y no incluye firmas de método para API experimentales.  Todas las API que están en un paquete de versión de SDK son totalmente compatibles, en un número de compilación igual o superior del tiempo de ejecución de WebView2.

El paquete de versión del SDK contiene los siguientes componentes:
*  [API de Win32 C/C++.][ReferenceWin32]
*  API de .NET:  [WPF,][DotnetMicrosoftWebWebview2WpfNamespace] [WinForms][DotnetMicrosoftWebWebview2WinformsNamespace]y [Core][DotnetMicrosoftWebWebview2CoreNamespace].

Para obtener más información acerca de la actualización automática de Evergreen Runtime, vaya a Distribuir una aplicación [WebView2 y WebView2 Runtime][Webview2ConceptsDistribution].


## <a name="release-cadence"></a>Cadencia de lanzamientos

Las nuevas versiones del SDK de WebView2 se envían con la misma cadencia general que el explorador Microsoft Edge \(Chromium\), que ha sido aproximadamente cada seis semanas.  Esta cadencia está planeada para cambiar a cada cuatro semanas a partir Microsoft Edge versión 94.


## <a name="minimum-version-and-build-number-to-instantiate-webview2"></a>Versión mínima y número de compilación para crear una instancia de WebView2

Para que el cliente pueda crear una instancia webView2 y usar el conjunto de API de la versión de disponibilidad general de WebView2 (compilación 616 del SDK), el cliente debe tener WebView2 Runtime versión 86.0.616.0 o posterior.  Runtime 86.0.616.0 es una versión especial, ya que es la versión de disponibilidad general.

En un equipo de desarrollo, el cliente debe tener la versión 86.0.616.0 o posterior del canal de vista previa de Microsoft Edge o la versión 86.0.616.0 o posterior de WebView2 Runtime.


## <a name="forward-compatibility-of-apis"></a>Compatibilidad de reenvío de API

El SDK de versión _de_ WebView2 ha sido compatible con el reenvío desde la versión 1 (es decir, la versión [1.0.622.22 del](../release-notes.md#1062222)SDK).
Puedes actualizar la aplicación WebView2 para usar las API más recientes de la versión de lanzamiento más reciente del SDK.  La aplicación seguirá funcionando en clientes porque los clientes tienen automáticamente la versión más reciente de WebView2 Evergreen Runtime.

Las API de WebView2 en un _paquete_ de versión de SDK son estables y compatibles con el reenvío.  Una API de WebView2 funciona cuando se usa un tiempo de ejecución de WebView2 que tiene un número de compilación igual o mayor que el número de compilación del SDK en el que se introdujo la API.  El número de compilación es la tercera parte del número de versión de cuatro partes del SDK de Webview2 y del número de versión de cuatro partes para Microsoft Edge y el tiempo de ejecución de WebView2.

*  Cuando usa un SDK de WebView2 __ que tiene un número de compilación igual o menor que WebView2 Runtime, cada API a la que tenga acceso en ese SDK funciona con esa versión del tiempo de ejecución.
*  Cuando se usa un SDK de WebView2 que tiene un número de compilación mayor que El tiempo de ejecución de WebView2, las implementaciones de las API más recientes no están disponibles en tiempo de ejecución. __

<!-- create diagram showing 3 SDK releases on a timeline, which ones would work w/ a given runtime -->
Por ejemplo, si se introduce una API en SDK 1.0. **900**.0, esa API funcionaría con Runtime 94.0. **900+**.0, pero no con Runtime 90.0. **700**.0.

<!-- dup statements, delete? -->
Debe coordinar la versión del SDK de WebView2 que usa para el desarrollo y la versión de Tiempo de ejecución de WebView2 que está instalada en máquinas cliente.
El cliente debe tener una versión del tiempo de ejecución que admita todas las API más recientes que estén en la versión del SDK que use para desarrollar la aplicación.
Para obtener compatibilidad completa con las API más recientes de una versión de lanzamiento del SDK, el tiempo de ejecución en el cliente debe tener un número de compilación mayor o igual que el número de compilación del SDK.


## <a name="experimental-apis"></a>API experimentales

No se garantiza que las API experimentales de un paquete de versión preliminar del _SDK_ de WebView2 sean compatibles con el reenvío y podrían quitarse en futuras actualizaciones en tiempo de ejecución.
Cuando _inicialmente está disponible_ una versión preliminar del SDK de WebView2, ese SDK solo funciona con Microsoft Edge Canary.  Poco después, el SDK de versión preliminar también funciona con los canales Beta y Dev.
Usa un SDK de versión preliminar para probar las nuevas API de forma anticipada y proporcionar comentarios antes de que las nuevas API se conviertan en API estables y compatibles con el avance.

Para obtener compatibilidad completa con las API experimentales, use un canal Microsoft Edge vista previa, no webView2 Evergreen Runtime.
No se garantiza que las API experimentales que están en un SDK de versión preliminar sean compatibles con el avance.
Las API que están en una versión _de lanzamiento del_ SDK son compatibles con el reenvío.  Para obtener más información, vea [Compatibilidad de reenvío de API anteriores.](#forward-compatibility-of-apis)

El equipo de WebView2 está buscando comentarios sobre las API experimentales de WebView2 que podrían promoverse a Stable en futuras versiones.
Las API experimentales se indican como "experimentales" en la documentación de referencia del SDK de WebView2.
Para ayudarle a evaluar las API experimentales y compartir sus comentarios, vaya al repositorio de comentarios [de WebView][GithubMicrosoftedgeWebviewfeedback].

Evita usar las API experimentales en aplicaciones de producción.  En versiones posteriores del SDK, las API experimentales pueden modificarse, quitarse o agregarse.  Después de la versión de una API como estable y pública, la versión experimental de esa API se admite para dos versiones en un estado en desuso.


## <a name="matching-the-runtime-version-with-the-sdk-version"></a>Coincidencia de la versión en tiempo de ejecución con la versión del SDK

En el enfoque de distribución Evergreen, El tiempo de ejecución de WebView2 del cliente se actualiza automáticamente a la versión más reciente disponible.
Sin embargo, un usuario o administrador de TI puede optar por impedir la actualización automática de WebView2 Runtime.
El tiempo de ejecución obsoleto resultante en el cliente puede provocar problemas de compatibilidad con la aplicación webView2 actualizada que usa nuevas API de un SDK reciente.

En caso de que no se pueda actualizar El tiempo de ejecución de WebView2 en el cliente, asegúrese de conocer el número de compilación mínimo del tiempo de ejecución de [WebView2][MicrosoftDeveloperEdgeWebview2] que requiere la aplicación.
La versión mínima necesaria en tiempo de ejecución para admitir la versión de disponibilidad general del SDK (compilación 616) es anterior a la del runtime más reciente.
El tiempo de ejecución más reciente admite todas las API que se encuentran en la última compilación de la versión del SDK.

Para comprobar la compatibilidad entre números de compilación específicos del SDK y el canal de vista previa en tiempo de ejecución o Microsoft Edge, vaya a Notas de la versión [del SDK de WebView2][Webview2ReleaseNotes].


## <a name="feature-detecting-to-test-whether-the-installed-runtime-supports-recently-added-apis"></a>Detección de características para probar si el tiempo de ejecución instalado admite API agregadas recientemente

<!-- this is the main section about QI; other articles should have a couple paragraphs only, and link to here -->

Si la aplicación usa evergreen runtime en lugar de la versión fija, debes ajustar las llamadas a las API relativamente nuevas de WebView2 mediante `QueryInterface` o `try-catch` .  Hay casos perimetrales en los que evergreen runtime de un cliente no es la compilación más reciente y, por lo tanto, se encuentra detrás del número de compilación del SDK, ya que el administrador puede haber desactivado la actualización de WebView2 Runtime o el cliente podría estar sin conexión.

Al desarrollar una aplicación WebView2 con una versión reciente del SDK de WebView2, si usa una API agregada recientemente, debe probar o "detectar características" si esa API está presente en el tiempo de ejecución de WebView2 instalado del cliente.  La forma en que la aplicación prueba mediante programación la compatibilidad con la API depende de la plataforma de codificación.

*   **Win32 C/C++**.  Al solicitar la exportación de DLL `CreateCoreWebView2Environment` y al `QueryInterface` ejecutarse en cualquier `CoreWebView2` objeto, pruebe un valor devuelto de `E_NOINTERFACE` .  Ese valor devuelto probablemente indica que webView2 Runtime del cliente es una versión anterior que no admite esa interfaz.  Para ver un ejemplo de comprobación de la existencia de API de WebView2 específicas en tiempo de ejecución, busque `try_query` [en AppWindow.cpp][GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCpp].  Este archivo ajusta las llamadas a la API de WebView2 en la `CHECK_FAILURE` función de macro, definida en `CheckFailure.h` .

*   **.NET y WinUI**.  Use y compruebe si hay una excepción al usar métodos, propiedades y eventos que se agregaron a versiones más recientes `try/catch` `No such interface supported` del SDK de WebView2.  Esta excepción probablemente indica que webView2 Runtime del cliente es una versión anterior que no admite esa API.

Si el código determina que una API no está disponible en el WebView2 Runtime instalado del cliente, debe proporcionar una reserva correcta para la característica asociada o informar al usuario de que debe actualizar WebView2 Runtime para usar la característica.

Esta técnica se muestra como un procedimiento recomendado de desarrollo de WebView2, en Probar si las API son compatibles [con webView2 Runtime instalado.][Webview2ConceptsDevguideTestAPIs]


<!--links -->
[Webview2ConceptsDistribution]: ./distribution.md "Distribuir una aplicación WebView2 y el motor de ejecución de WebView2 | Microsoft Docs"
[Webview2ReleaseNotes]: ../release-notes.md "Notas de la versión de SDK de WebView2 | Microsoft Docs"
[Webview2ReleaseNotes1062222]: ../release-notes.md#1062222 "1.0.622.22: notas de la versión de WebView2 SDK | Microsoft Docs"
[Webview2ConceptsDevguideTestAPIs]: developer-guide.md#test-whether-newer-apis-are-supported-by-the-installed-webview2-runtime "Compruebe si las API son compatibles con el sitio web instalado de WebView2 Runtime | Microsoft Docs"
[SetPreviewChannel]: ../how-to/set-preview-channel.md "Cambiar a un canal de vista previa para probar las próximas API y características | Microsoft Docs"
<!-- external links -->
[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Información general sobre los canales de Microsoft Edge | Microsoft Docs"

[DotnetMicrosoftWebWebview2CoreNamespace]: /dotnet/api/microsoft.web.webview2.core "Espacio de nombres Microsoft.Web.WebView2.Core | Microsoft Docs"
[DotnetMicrosoftWebWebview2WpfNamespace]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft.Web.WebView2.Wpf | Microsoft Docs"
[DotnetMicrosoftWebWebview2WinformsNamespace]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft.Web.WebView2.WinForms | Microsoft Docs"
[DotnetApiWebview2WinformsWebview2Appliesto]: /dotnet/api/microsoft.web.webview2.winforms.webview2#applies-to "Clase WebView2 | Microsoft Docs"
[ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "WebView2 Win32 C++ Reference | Microsoft Docs"

[MicrosoftDeveloperEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Microsoft Developer"

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Comentarios de WebView: MicrosoftEdge/WebViewFeedback | GitHub"
[GithubMicrosoftedgeWebview2samplesSampleappsWebview2apisampleAppwindowCpp]: https://github.com/MicrosoftEdge/WebView2Samples/blob/8ec7de9d3e80a942bc7025cffad98eee75e11e64/SampleApps/WebView2APISample/AppWindow.cpp#L622 "AppWindow.cpp: MicrosoftEdge/WebView2Samples | GitHub"

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Descargar Microsoft Edge Insider Channels"
