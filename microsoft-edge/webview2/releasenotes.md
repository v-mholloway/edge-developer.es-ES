---
description: Notas de la versión del SDK de WebView2 de Microsoft Edge
title: Notas de la versión de Microsoft Edge WebView2 para Win32, WPF y WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/23/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones de win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, html perimetral
ms.openlocfilehash: 913aa7f6a646964aae6aa36665395f64c3b65b36
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519404"
---
# <a name="release-notes-for-webview2-sdk"></a>Notas de la versión del SDK de WebView2  

El equipo de WebView2 actualiza el [SDK de WebView2][NuGetGallery] en una cadencia de seis semanas.  Revise el siguiente contenido para obtener información actualizada sobre anuncios de productos, adiciones, modificaciones y cambios importantes en las API.  

> [!NOTE]
> Asegúrate de volver a compilar la aplicación después de actualizar el paquete NuGet.  El equipo de WebView recomienda usar el canal Canary al desarrollar con los paquetes de versión preliminar y Evergreen WebView2 Runtime al usar los paquetes de lanzamiento.  Para obtener más información, vaya [a Coincidencia de versiones de WebView2 Runtime][Webview2ConceptsVersioningMatchingWebview2RuntimeVersions].  

> [!NOTE]
> Las correcciones de errores de WebView2 son específicas de Runtime o SDK.  
<!-- 
## 1.0.865-prerelease  

Release Date: April 19, 2021  

[NuGet package][NuGetGallery1.0.865-prerelease] \| Minimum Microsoft Edge version to load: 86.0.616.0 or newer \| Full API Compatibility: 91.0.865.0 or newer  

### General  

#### Experimental Features  

*   Added [IsPinchZoomEnabled][Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled] setting. It allows you to turn on or off page scale zoom control in a setting.  
*   Added Custom [add_DownloadStarting][Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting] API.  It allows you to block downloads, save to a different path, and access the required metadata to build custom download UI.  
*   Added `iframe` element support from [AddHostObjectToScriptWithOrigins][Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins].  
*   Added sample code for [WPF sample app][GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser] to use the API to turn off browser function keys.  
*   Added the [UpdateRuntime][Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime] API, to easily update the WebView2 Runtime.  
    
#### Bug fixes  

*   Fixed handler for a `Chromium DevTools Protocol` message with `POST` binary data in WebView2.  
*   Turned off the `OpenSaveAsAwareness` download UI, because it included links to `edge://settings`.  \([\#1120][GithubMicrosoftedgeWebviewfeedbackIssue1120]\).  
*   Removed branding from screen share dialog.  \([\#940][GithubMicrosoftedgeWebviewfeedbackIssue940]\).  
*   Fixed bug where the [SetWindowDisplayAffinity][WindowsWin32ApiWinuserSetWindowDisplayAffinity] function broke WebView2 when it stopped screen capture in an WebView2 app.  \([\#841][GithubMicrosoftedgeWebviewfeedbackIssue841]\).
*   Fixed bug for composition hosting where mouse input stopped working if any pen input was sent to WebView2.  
*   Fixed bug that broke mouse input after any pen input.  This change is Runtime-specific.  
    
### .NET  

#### Experimental Features  

*   Added WebView2 designer tool to WPF Toolbox.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Added WebView2 UI element in .NET Designer Mode.  
    
#### Bug fixes  

*   Improved COM Exception descriptions by wrapping each in a more detailed .NET exception.  \([\#338][GithubMicrosoftedgeWebviewfeedbackIssue338]\).  This change is Runtime-specific.  
*   Fixed bug caused when you select `tab` to shift focus caused WebView2 control to crash in Microsoft Visual Studio Tools for Office.  \([\#589][GithubMicrosoftedgeWebviewfeedbackIssue589] and [\#933][GithubMicrosoftedgeWebviewfeedbackIssue933]\).  This change is Runtime-specific.  
*   Improved .NET framework loader down level to be more robust.  \([\#946][GithubMicrosoftedgeWebviewfeedbackIssue946]\).
*   Fixed bug that caused crash when you try to refresh before first navigation completed.  \([\#1011][GithubMicrosoftedgeWebviewfeedbackIssue1011]\).
*   Fixed initialization so navigation occurs during `CoreWebView2InitializationCompleted`.  \([\#1050][GithubMicrosoftedgeWebviewfeedbackIssue1050]\).
*   Improved .NET browser process crash error handling.  You may now recreate controls after you handle a `ProcessFailed` event without a crash.  \([\#996][GithubMicrosoftedgeWebviewfeedbackIssue996]\).  
     -->
## <a name="1081841"></a>1.0.818.41  

Fecha de lanzamiento: 21 de abril de 2021  

[Paquete NuGet][NuGetGallery1.0.818.41] \| Versión mínima en tiempo de ejecución para cargar: 86.0.616.0 o posterior \| Compatibilidad completa de API: 90.0.818.41 o posterior  

### <a name="general"></a>General  

#### <a name="features"></a>Características  

*   Código WebView2 mejorado para que sea más resistente a los archivos `.exe` de aplicación con información de versión malformatada.  \([\#850][GithubMicrosoftedgeWebviewfeedbackIssue850]\).  
*   Se quitó de la línea de comandos del proceso del explorador WebView y se desactivaron otras opciones de línea de comandos `--winhttp-proxy-resolver` de proxy para WebView2.  
  
## <a name="10824-prerelease"></a>1.0.824-prerelease  

Fecha de lanzamiento: 8 de marzo de 2021  

[Paquete NuGet][NuGetGallery1.0.824-prerelease] \| Versión mínima de Microsoft Edge para cargar: 86.0.616.0 o posterior \| Compatibilidad completa de API: 91.0.824.0 o posterior  

### <a name="general"></a>General  

#### <a name="features"></a>Características  

*   Extendió el `ProcessFailed` evento.  Ahora se genera para los procesos secundarios que no representan el representador y los representadores de fotogramas.  
*   Se agregó [la configuración experimental AreBrowserAcceleratorKeysEnabled.][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled]  Puede impedir que el explorador responda a los métodos abreviados de teclado relacionados con la navegación, la impresión, el almacenamiento y otras funciones específicas del explorador.  
*   Se agregó `iframe` compatibilidad con elementos para `AddScriptToExecuteOnDocumentCreated` .  
    
#### <a name="promotion"></a>Promoción  

*   [UserAgent][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] Ahora, la API se promueve a Estable.  
*   Las API de escala de rasterización \([RasterizationScale][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] property,  [RasterizationScaleChanged][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] event, [BoundsMode property][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]y [ShouldDetectMonitorScaleChanges][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] property\) ahora se promueven a Stable.  
    
#### <a name="bug-fixes"></a>Correcciones de errores  

*   Tipos de proyecto C++ y .NET expandido compatibles, como MFC y ATL.  \([\#506][GithubMicrosoftedgeWebviewfeedbackIssue506], [\#669][GithubMicrosoftedgeWebviewfeedbackIssue669]y [\#851][GithubMicrosoftedgeWebviewfeedbackIssue851]\).  
*   Se ha corregido un error que generaba que Evergreen WebView2 Runtime filtrara la entrada de firewall entrante.  
*   Configuración fija Respuesta durante el `WebResourceRequested` evento.  \([\#568][GithubMicrosoftedgeWebviewfeedbackIssue568]\).  
*   Se ha corregido un error que provocaba la salida del `edge://` proceso del explorador.  \([\#604][GithubMicrosoftedgeWebviewfeedbackIssue604]\).  
*   Se ha corregido un error que limitaba los límites de WebView2 al tamaño de pantalla en el modo de hospedaje visual.  

## <a name="1077444"></a>1.0.774.44  

Fecha de lanzamiento: 8 de marzo de 2021  

[Paquete NuGet][NuGetGallery1.0.774.44] \| Versión mínima en tiempo de ejecución para cargar: 86.0.616.0 o posterior \| Compatibilidad completa de api: 89.0.774.44 o posterior  

### <a name="general"></a>General  

#### <a name="features"></a>Características  

*   Desactivados varios servicios de explorador de Microsoft Edge en WebView2.  
*   Las API de hospedaje visual ahora están disponibles en general.  

#### <a name="promotions"></a>Promociones  

*   Las siguientes API experimentales ahora se promueven a Estable.  
    *   [API relacionadas con][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived] la compatibilidad con PPP  
    *   API de hospedaje visual  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
    *   [TrySuspend y Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]  
    *   [DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]  
        
#### <a name="bug-fixes"></a>Correcciones de errores  

*   Se ha corregido un error que limitaba los límites de WebView2 al tamaño de pantalla en el modo de hospedaje visual.  
    
## <a name="10790-prerelease"></a>1.0.790-prerelease  

Fecha de lanzamiento: 10 de febrero de 2021  

[Paquete NuGet][NuGetGallery1.0.790-prerelease] \| Versión de Microsoft Edge 86.0.616.0 o posterior  

### <a name="general"></a>General  

> [!IMPORTANT]
> **Breaking Change**: El paquete de versión previa a WebView2 1.0.781 está en desuso.  Discontinue el desarrollo con el paquete 1.0.781.  

> [!IMPORTANT]
> El paquete de versión previa a webView2 0.9.430 está en desuso y se quita con la siguiente versión.  Si la aplicación WebView usa el paquete, el equipo de WebView recomienda pasar a un paquete más reciente.  

#### <a name="features"></a>Características  

*   Se [agregó el método TrySuspend y Resume][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend] para suspender y reanudar WebViews.  
*   Se [agregó el método SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping] que asigna un nombre de host virtual a una ruta de acceso de directorio.  \([\#37][GithubMicrosoftedgeWebviewfeedbackIssue37], [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]y [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Se agregó [la propiedad DefaultBackgroundColor][Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor] para establecer el color y el canal alfa del fondo.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Se agregó [la propiedad UserAgent][Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent] para obtener o establecer el agente de usuario.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).  
*   Se `CreateCookieWithCookie` reemplazó el método por el `CopyCookie` método.  
*   Se agregó compatibilidad de hospedaje visual con la [interfaz ICoreWebView2CompositionController,][Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease] que se crea con el nuevo `CreateCoreWebView2CompositionController` método de `ICoreWebView2Environment3` .  
    
#### <a name="bug-fixes"></a>Correcciones de errores  

*   Desactivada la característica Microsoft Edge Shopping en WebView2.  
*   Desactivado el menú contextual en el visor de PDF cuando `AreDefaultContextMenusEnabled` es `false` .  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Se ha corregido un error que `E_NOINTERFACE` se devolvía al `ICoreWebView2` consultar `ICoreWebView2Experimental` .  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Se ha corregido un error que permitía la navegación con URI malformados cuando `CoreWebView2NavigationStartingEventArgs.Cancel` se establece en `false` .  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Se ha corregido un error que bloqueaba las ventanas `window.print()` emergentes con controladores de eventos adjuntos a `NewWindowRequested` eventos.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Se ha corregido un problema de PPP dinámico al mover aplicaciones entre distintos monitores.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Se han mejorado `HRESULT` las instancias pasadas por [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke][Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke].  
*   Desactivado el botón de administración de autocompletar.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\).  
*   Se Visual Studio bloqueos mientras se ejecuta `WebView2.Dispose` cuando se hospeda en varias ventanas.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\) [y \#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Se ha corregido un error para mostrar el control WebView2 en Visual Studio cuadro de herramientas.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\).  
*   Se han reducido los problemas de uso elevado de LA CPU.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Se han corregido problemas con el paquete de versión preliminar 1.0.781 en desuso.  \([\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] [y \#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
#### <a name="promotions"></a>Promociones  

*   Las siguientes API experimentales ahora se promueven a Estable.  
    *   API de hospedaje visual  
    *   [SetVirtualHostNameToFolderMapping][Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]  
        
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Correcciones de errores  

*   Se ha corregido un error que bloqueaba las aplicaciones webView que usaban el SDK de WPF.  El bloqueo se produjo cuando `F4` seleccionaste cerrar una ventana.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   La pantalla de inicialización de WebView2 ahora es transparente, en lugar de gris.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## <a name="1070550"></a>1.0.705.50  

Fecha de lanzamiento: 25 de enero de 2021  

[Paquete NuGet][NuGetGallery1.0.705.50] \| WebView2 Runtime versión 86.0.616.0 o posterior  

### <a name="general"></a>General  

#### <a name="promotions"></a>Promociones  

*   Las siguientes API experimentales ahora se promueven a Estable.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API de administración de cookies][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Propiedad WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  

## <a name="10721-prerelease"></a>1.0.721-prerelease  

Fecha de lanzamiento: 8 de diciembre de 2020  

[Paquete NuGet][NuGetGallery1.0.721-prerelease] \| Versión de Microsoft Edge 86.0.616.0 o posterior  

### <a name="general"></a>General  

> [!IMPORTANT]
> **Cambio de**última hora: el paquete de versión previa a WebView2 1.0.707 y el paquete 0.9.628 están en desuso.  Suspenda el desarrollo con el paquete 1.0.707 y package0.9.628.  

#### <a name="features"></a>Características  

*   Se [agregaron directivas de grupo de WebView2][DeployedgeMicrosoftEdgeWebviewPolicies].  Para obtener más información sobre los procedimientos recomendados, vaya a [directivas de grupo para WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Breaking Change:** Desusado la antigua ubicación del Registro.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Se agregó compatibilidad con [Arrastrar y colocar][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease] en WebView2.  
*   Se agregaron API para controlar la compatibilidad con PPP.  
    *   Se agregó [la propiedad RasterizationScale][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] para cambiar la escala de PPP del contenido webView y los elementos emergentes de la interfaz de usuario, y el [evento RasterizationScaleChanged][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] asociado.  
    *   Se [agregó la propiedad ShouldDetectMonitorScaleChanges][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges] para actualizar automáticamente la `RasterizationScale` propiedad si es necesario.  
    *   Se agregó la propiedad [BoundsMode][Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode] para especificar que los límites son píxeles lógicos y permitir que WebView use para la presentación de píxeles de WebView2 y WebView use el con el para obtener el `RasterizationScale` `RasterizationScale` tamaño `Bounds` físico.  
*   Evento `NewWindowRequested` actualizado para controlar y `Ctrl` + `click` `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] y [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Las siguientes API experimentales ahora se promueven a Estable.  
    *   [WebResourceResponseReceived API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]  
    *   [NavigateWithWebResourceRequest API][Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]  
    *   [API de administración de cookies][Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]  
    *   [DOMContentLoaded API][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]  
    *   [Propiedad WebView Environment][Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]  
        
### <a name="net"></a>.NET  

#### <a name="features"></a>Características  

*   Activado el diseñador de WinForms en .NET Core 3.1+ y .NET 5.  
*   Administración de cookies .NET mejorada.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Se `CoreWebView2Ready` reemplaza [por CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  

#### <a name="bug-fixes"></a>Correcciones de errores

*   Se agregó [el evento AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] para admitir `AcceleratorKey` seleccionar en WebView2.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Se quitaron los archivos innecesarios de salida a las carpetas WebView2.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   API de objetos host mejorada.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] y [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## <a name="1066437"></a>1.0.664.37  

Fecha de lanzamiento: 20 de noviembre de 2020  

[Paquete NuGet][NuGetGallery1.0.664.37] \| WebView2 Runtime versión 86.0.616.0 o posterior  

### <a name="general"></a>General  

> [!IMPORTANT]
> **Anuncio:** los SDK de WebView2 de .NET WPF/WinForms ahora están disponibles en general \(GA\).  A partir de esta versión, los SDK de versión son compatibles con el avance.  Para obtener más información, vaya a [la entrada de blog del anuncio de GA][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod].  

#### <a name="features"></a>Características  

*   .NET WPF/WinForms WebView2 ahora está disponible generalmente \(GA\).  
*   Modo de distribución fijo \(Bring-your-own\) alcanzado ga.  
    
### <a name="net"></a>.NET  

#### <a name="bug-fixes"></a>Correcciones de errores  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` impide que se abra una nueva ventana.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] y [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## <a name="10674-prerelease"></a>1.0.674-prerelease  

Fecha de lanzamiento: 19 de octubre de 2020  

[Paquete NuGet][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime versión 86.0.616.0 o posterior  

### <a name="general"></a>General  

*   Se agregó [el método NavigateWithWebResourceRequest para][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest] proporcionar datos de publicación u otros encabezados de solicitud durante la navegación.  
*   Se agregó [el evento DOMContentLoaded][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded] que se ejecuta cuando se carga y analiza el documento HTML inicial.  
*   Se agregó [la propiedad Environment][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment] en WebView2.  Esta propiedad expone el entorno WebView2 donde se creó una instancia de WebView2.  
*   Se [agregaron API de administración][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager] de cookies que permiten a los desarrolladores autenticar la sesión de WebView2 o recuperar cookies de WebView para autenticar otras herramientas.  El equipo de Webview planea realizar mejoras de lenguaje o específicas del marco.  Para obtener más información, vaya a [Api Review: Cookie Management][GithubMicrosoftedgeWebview2AnnouncementIssue2].  
*   Se actualizó el evento [WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived] y se agregaron [WebResourceResponseView][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease] y [WebResourceResponseReceivedEventArgs::P opulateResponseContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent] a [WebResourceResponseView::GetContent][Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent].  
*   Desactivado Microsoft [Defender Application Guard (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] en WebView2.  
*   Se agregó [SystemCursorId][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid] para el hospedaje visual.  
*   Se agregó un error corregido para el método Input en el hospedaje visual.  
*   Se ha quitado el requisito `version.lib` de uso de la biblioteca estática de WebView2.  
    
### <a name="net"></a>.NET  

*   Se actualizó la clase [CoreWebView2][DotnetApiMicrosoftWebWebview2CoreCorewebview2] para exponer la `CoreWebView2Environment` variable.  
*   Se han cambiado las implementaciones de clases EventArgs personalizadas en el espacio de nombres a `Microsoft.Web.WebView2.Core` subclases [de System.EventArgs][DotnetApiSystemEventargs] o [System.ComponentModel.CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs].  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Se agregó compatibilidad [con CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] en WinForms.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\).  
*   Se [agregaron API de WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Se actualizó la propiedad Source del Diseñador [de][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] WinForms para que se restablezca de forma predeterminada o se restablezca a null.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Se han actualizado los límites de WebView2 WebView2.Init() para admitir modos de PPP inferiores al 100 %.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   Se [han actualizado BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] [y DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] para aumentar la robustez.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Se actualizó la base del cargador de .NET para cargar el bit de proceso en lugar de la arquitectura del sistema operativo.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Se `EdgeNotFoundException` cambió el nombre [a WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## <a name="1062222"></a>1.0.622.22  

Fecha de lanzamiento: 19 de octubre de 2020  

[Paquete NuGet][NuGetGallery1.0.622.22] \| WebView2 Runtime versión 86.0.616.0 o posterior  

### <a name="general"></a>General  

> [!IMPORTANT]
> **Anuncio:** Win32 C/C++ WebView2 ahora está disponible generalmente \(GA\).  A partir de esta versión, los SDK de versión son compatibles con el avance.  Para obtener más información, vaya a [la entrada de blog de anuncios de GA][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability].  

*   [Evergreen WebView2 Runtime y el instalador son][Webview2ConceptsDistributionUnderstandRuntimeInstaller] GA.  Bootstrapper, downlink link for the Bootstrapper, and Standalone Installer for the Evergreen WebView2 Runtime are available on [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  El código de ejemplo para el flujo de trabajo de instalación también está disponible en el repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   [El modo versión fija][Webview2ConceptsDistributionFixedVersionDistributionMode] está disponible para la vista previa del desarrollador.  
    
## <a name="0962211"></a>0.9.622.11  

Fecha de lanzamiento: 10 de septiembre de 2020  

[Paquete NuGet][NuGetGallery0.9.622.11] \| WebView2 Runtime versión 86.0.616.0 o posterior  

### <a name="general"></a>General  

*   > [!IMPORTANT]
    > **Anuncio:** este SDK es el candidato de versión de WebView2 Win32 C/C++ GA.  La versión de GA debe usar la misma interfaz y funcionalidad de la API.  
    
*   Directivas de [explorador desconectado][DeployedgeMicrosoftEdgePolicies].  
*   Se agregó [la propiedad AllowSingleSignOnUsingOSPrimaryAccount][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount] en las opciones del entorno WebView2 para activar el acceso condicional para WebView.  
*   Se actualizó para incluir la propiedad `ICoreWebView2NewWindowRequestedEventArgs` [WindowFeatures][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures] y la [propiedad ICoreWebView2WindowFeatures asociada.][Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Se `System.Windows.Rect`  actualizó `System.Drawing.Rectangle` para su uso en lugar de `System.Windows.Rect` [\( \#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Evento NewWindowRequested actualizado para controlar `window.open()` la solicitud sin parámetros.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments especificados][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments] con `ICoreWebView2EnvironmentOptions` no se invalidan con variables de entorno o valores del Registro.  Para obtener más información, ve a [ CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions].  
    
## <a name="09579"></a>0.9.579  

Fecha de lanzamiento: 20 de julio de 2020  

[Paquete NuGet][NuGetGallery0.9.579] \| Versión 86.0.579.0 de Microsoft Edge.  

### <a name="general"></a>General  

*   > [!IMPORTANT]
    > **Anuncio:** Evergreen WebView2 Runtime y el instalador se liberan para obtener una vista previa.  Para obtener más información, vaya [a Distribución de WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstaller].  
    
*   > [!IMPORTANT]
    > **Anuncio:** las siguientes versiones del SDK de WebView2 ya no se admiten después de la próxima versión del SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Las versiones del SDK de WebView2 también se marcan en desuso en nuget.org.  WebView2 recomienda mantenerse al día con la versión más reciente de WebView2.  
    
*   Se agregaron mejoras en los subprocesos de trabajo de WebView.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Desactivado el bloqueador de elementos emergentes en WebView.  Para obtener más información, vaya a la [propiedad IsUserInitiated][Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated] en el `NewWindowRequested` evento.  
*   Se ha asegurado de que se ejecute el evento de inicio de navegación WebView para `about:blank` .  Ahora, los eventos se ejecutan para toda la navegación, pero las cancelaciones para `NavigationStarting` o del elemento no se `about:blank` `srcdoc` `iframe` admiten ni se omiten.  
*   Se bloquearon `edge://` algunos esquemas uri en WebView.  
*   Se agregó la propiedad [experimental IsSingleSignOnUsingOSPrimaryAccountEnabled][Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled] en las opciones del entorno WebView2 para activar el acceso condicional para WebView.  
*   Se agregó [el evento experimental WebResourceResponseReceived][Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived] que se ejecuta después de que WebView recibe y procesa la respuesta de una solicitud WebResource.  Los encabezados de autenticación, si los hay, se incluyen en el objeto de respuesta.  
    
### <a name="net"></a>.NET  

*   Se ha mejorado el control de foco de WPF.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Se `ZoomFactor` agregó la propiedad en wpf Webview2 Controller.  
    
## <a name="09538"></a>0.9.538  

[Paquete NuGet][NuGetGallery0.9.538] \| Versión 85.0.538.0 de Microsoft Edge.  

### <a name="general"></a>General  

*   Quitar compatibilidad con WebView2 SDK Versión [0.8.149](#08149).  WebView2 recomienda mantenerse al día con la versión más reciente de WebView2.  
*   Directiva de grupo actualizada para tener en cuenta cuándo se modifica la ruta de acceso de perfil del explorador Microsoft Edge \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
### <a name="win32-cc"></a>Win32 C/C++  

*   Se agregó [ICoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures], que se activa cuando se ejecuta y se asocia con `window.open()` [ICoreWebView2ExperimentalWindowFeatures][Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Cambio de**ruptura: [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] en desuso y reemplazado por [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions].  
    
*   > [!IMPORTANT]
    > **Breaking Change:** Para garantizar que la API de WebView2 se alinee con las convenciones de nomenclatura de la API de Windows, el equipo de WebView actualizó los nombres de los siguientes.  
    > 
    > *   [AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed] ahora [es AreHostObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed].  
    
*   [AddHostObjectToScript actualizado][Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript].  Los marcadores del serializador de objetos host originales ahora se establecen en los objetos proxy.  A continuación, los marcadores del serializador de objetos host se serializan de nuevo como un objeto host cuando se pasan como parámetro en la devolución de llamada de JavaScript \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  
    
### <a name="net-09538-pre-release"></a>.NET (versión previa 0.9.538)  

*   WinForms y WPF WebView2API Samples publicados, que son guías completas del SDK de WebView2.  Para obtener más información, vaya a [Samples Repo][GithubMicrosoftedgeWebview2samplesMain].  
*   Se agregó compatibilidad con las API experimentales de características de ventana y hospedaje [visual.][Webview2ConceptsVersioningExperimentalApis]  
*   > [!IMPORTANT]
    > **Breaking Change:** los siguientes aplazamientos ahora implementan IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]y [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   Se [agregaron GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] y [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] como [estáticas de CoreWebView2Environment.][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]  
    
## <a name="09515-prerelease"></a>0.9.515-prerelease  

[Paquete NuGet][NuGetGallery0.9.515-prerelease] \| Versión 84.0.515.0 de Microsoft Edge.  

*   > [!IMPORTANT]
    > **Anuncio:** WebView2 ahora admite Windows Forms y WPF en .NET Framework 4.6.2 o posterior y .NET Core 3.0 o posterior en el paquete **de**versión previa.  
    
*   Para obtener más información acerca de la creación de aplicaciones WPF, vaya a la Guía de introducción de [WPF][Webview2GettingstartedWpf] y la Referencia [de WPF][DotnetApiMicrosoftWebWebview2Wpf] de WebView2 para LAS API específicas de WPF.  
*   Para obtener más información acerca de la creación de aplicaciones de Windows Forms, vaya a la Guía de introducción de [Windows Forms][Webview2GettingstartedWinforms] y a la Referencia de [Windows Forms][DotnetApiMicrosoftWebWebview2Winforms] de WebView2 para API específicas de Windows Forms.  
*   Para obtener más información acerca de las API de CoreWebView2, vaya a [.NET Reference][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Problemas conocidos:** el equipo de WebView es consciente de algunos problemas de la versión previa que se están resolviendo en versiones futuras.  
    > 
    > *   **Reconocimiento de PPP:** WebView2 para WPF actualmente no es compatible con PPP.  Al inicializar WebView2 en monitores de PPP altos, existe un problema conocido en el que WebView se inicializa al principio como una fracción de la ventana hasta que se cambia el tamaño de la ventana.  
    > *   **Diseñador WPF:** el diseñador WPF no es compatible actualmente.  Agrega el control WebView2 en la aplicación modificando directamente el XAML adecuado en un editor de texto.  
    
## <a name="09488"></a>0.9.488  

[Paquete NuGet][NuGetGallery0.9.488] \| Versión 84.0.488.0 de Microsoft Edge.  

*   > [!IMPORTANT]
    > **Anuncio:** a partir de la próxima versión 83 de Microsoft Edge, Evergreen WebView ya no está dirigido al canal del explorador Estable.  En su lugar, está dirigido a otro conjunto de archivos binarios, con la marca [Evergreen WebView2 Runtime,][Webview2ConceptsDistributionEvergreenDistributionMode]que puede instalar en cadena a través de un instalador que el equipo de WebView está desarrollando actualmente.  Para obtener más información, vaya a [Distribución de aplicaciones][Webview2ConceptsDistribution].  
    
*   > [!IMPORTANT]
    > **Anuncio:** avanzando, el equipo de WebView publica dos paquetes: un paquete de versión previa con API experimentales \(para que lo pruebe\) y un paquete de versión estable con API estables \(para su confianza\).  Para obtener información sobre las diferencias, vaya a [Understanding browser versions y WebView2][Webview2ConceptsVersioning].  
    
*   > [!IMPORTANT]
    > **Breaking Change:** Para garantizar que la API de WebView2 se alinee con las convenciones de nomenclatura de la API de Windows, el equipo de WebView actualizó los nombres de las interfaces siguientes.  
    > 
    > *   `CORE_WEBVIEW2_*` prefix es ahora `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo] es [ahora GetAvailableCoreWebView2BrowserVersionString][Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo] está [get_BrowserVersionString][Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring].  
    > *   [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] es [ahora AddHostObjectToScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject] es [ahora RemoveHostObjectFromScript][Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` es ahora `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Cambio de separación:** también se cambia el nombre de `AddRemoteObject` los métodos de proxy JS.  
    > 
    > *   `getLocal` es ahora `getLocalProperty` .  
    > *   `setLocal` es ahora `setLocalProperty` .  
    > *   `getRemote` es ahora `getHostProperty` .  
    > *   `setRemote` es ahora `setHostProperty` .  
    > *   `applyRemote` es ahora `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Cambio de**ruptura: [CreateCoreWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails] en desuso y reemplazado por [CreateCoreWebView2EnvironmentWithOptions][Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions].  
    
*   Se agregó [el evento FrameNavigationCompleted.][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]  Ahora, cuando un elemento completa la navegación, se ejecuta un evento y devuelve el éxito de la navegación `iframe` y el identificador de navegación.  
*   Se agregó la interfaz [ICoreWebView2EnvironmentOptions,][Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488] que puede usarse para determinar la versión de Evergreen WebView2 Runtime dirigida por la aplicación.  
*   Se agregó [la configuración IsBuiltInErrorPageEnabled.][Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]  Ahora, puede elegir activar o desactivar la página web de error integrada para el error de navegación y representar el error del proceso.  
*   Inyección de objetos remota actualizada para admitir implementaciones de .NET `IDispatch` \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Evento [NewWindowRequested actualizado][Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested] para controlar solicitudes de menús contextuales \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Se publicó el primer paquete de versión previa a WebView2 independiente en el que puede tener acceso a las API de hospedaje visual.  El equipo de WebView actualizó [APISample][GithubMicrosoftedgeWebview2samplesMain] para incluir las nuevas API experimentales.  
    *   Se [agregó la interfaz ICoreWebView2ExperimentalCompositionController,][Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease] para conectarse a un árbol de composición y proporcionar entradas para WebView.  
    *   Se [agregó ICoreWebView2ExperimentalPointerInfo][Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease], que contiene toda la información de un `POINTER_INFO` archivo .  Este objeto se pasa a SendPointerInput para insertar entrada de puntero en webView.  
    *   Se [agregó ICoreWebView2ExperimentalCursorChangedEventHandler][Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease], que indica a la aplicación cuándo debe cambiarse el cursor del mouse sobre WebView.  Cuando el mouse está sobre un cuadro de texto en WebView, el cursor cambia de la flecha al selector.  La propiedad de la aplicación indica a la aplicación cuál debe ser el cursor del `cursor` `CompositionController` mouse actualmente para WebView.  
        
## <a name="09430"></a>0.9.430  

[Paquete NuGet][NuGetGallery0.9.430] \| Versión 82.0.430.0 de Microsoft Edge.  

El SDK de WebView2 es la versión beta oficial de Win32 C++, que incorpora varias solicitudes de características de comentarios.  El equipo de WebView intenta limitar el número de versiones con cambios importantes.  A medida que se acerca la disponibilidad general, se incorporan varios cambios importantes en la versión beta.  

*   > [!IMPORTANT]
    > **Cambio de**separación: a medida que se acerca la versión final, el equipo de WebView cambió el nombre del prefijo para asegurarse de que la `IWebView2WebView` API de WebView2 se alinea con la convención de nomenclatura `ICoreWebView2` de la API de Windows.  Además, para aprovechar el SDK de WebView2 de los marcos de interfaz de usuario, el equipo de WebView se separó de `ICoreWebView2` [ICoreWebView2][Webview2ReferenceWin32Icorewebview2ViewWebview209430] e [ICoreWebView2Host][Webview2ReferenceWin32Icorewebview2hostViewWebview209430].  `ICoreWebView2Host` admite cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con las ventanas y la composición.  ICoreWebView2 admite todas las demás funciones de WebView2.  Para obtener más información sobre cómo incorporar [][GithubMicrosoftedgeWebview2samplesPr17] los cambios, vaya a la solicitud de extracción de WebView2 en el proyecto [APISample][GithubMicrosoftedgeWebview2samplesMain] de WebView2.  
    
*   > [!IMPORTANT]
    > **Breaking Change**: Split [DocumentStateChanged][Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged] en tres componentes:  [SourceChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged], [ContentLoading][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]e [HistoryChanged][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged].  Ahora, cuando la dirección URL de origen cambia, `SourceChanged` se ejecuta el evento.  Cuando se cambia el estado del historial, `HistoryChanged` se ejecuta el evento.  El `ContentLoading` evento se ejecuta antes del script inicial cuando se carga un nuevo documento.  
    
*   Se agregó compatibilidad con la arquitectura ARM64.  
*   Se agregó compatibilidad con panel de entrada suave \(SIP\) para dispositivos de pantalla táctil.  
*   Se agregó compatibilidad con Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 y Windows Server 2016.  
*   Se [agregó NotifyParentWindowPositionChanged para][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged] que la barra de estado siga la ventana en modo de ventana.  Además, implemente el cambio en modo sin ventanas para que funcionen las características de accesibilidad.  
*   Se [agregó la configuración AreRemoteObjectsAllowed][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed] para controlar globalmente si los objetos remotos pueden tener acceso a una página web.  De forma predeterminada, está activada, por lo que los objetos remotos agregados `AreRemoteObjectsAllowed` por [AddRemoteObject][Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject] son accesibles desde la página web.  Cuando `AreRemoteObjectsAllowed` está desactivado, los objetos no son accesibles desde la página web.  Los cambios se aplican en el siguiente evento de navegación.  
*   Se agregó [la configuración IsZoomControlEnabled][Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled] para evitar que los usuarios afectaran al zoom de WebView usando `ctrl` + `+` y `ctrl` + `-` \(o `ctrl` + rueda del mouse\).  Es posible que el zoom aún [se establezca put_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor] cuando la configuración esté desactivada.  
*   Se ha cambiado ZoomFactor para que solo se aplique al WebView actual.  Los cambios de zoom en el WebView actual no afectan a otros WebView a los que ha navegado con el mismo sitio de origen.  Para obtener más información, vaya [a get_ZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor].  
*   Hid ZoomView UI for WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Se agregó [SetBoundsAndZoomFactor][Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor].  Ahora, puede establecer el factor de zoom y los límites de un WebView al mismo tiempo.  
*   Se agregó [el evento WindowCloseRequested.][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]  Para obtener más información, vaya [a add_WindowCloseRequested][Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Se agregó compatibilidad con el tipo de cuadro de diálogo para eventos de diálogo `beforeunload` de JavaScript y se CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD entrada de enumeración. [][Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]  
*   Se [agregó GetHeaders][Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders] [a][Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader] HttpRequestHeaders, [GetHeader][Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader] a HttpResponseHeaders y get_HasCurrentHeader propiedad a HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Breaking Change**: Comportamiento `DevToolsProtocolEventReceived` modificado.  Ahora, puede crear [un DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430] para un evento de Protocolo DevTools en particular y suscribirse o cancelar la suscripción a dicho evento mediante [add_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived].  
    
*   > [!IMPORTANT]
    > **Breaking Change:** se `WebMessageReceivedEventArgs` [get_WebMessageAsString][Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring] propiedad a [un método TryGetWebMessageAsString.][Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]  
    
*   > [!IMPORTANT]
    > **Breaking Change:** se cambió `AcceleratorKeyPressedEventArgs` [el método Handle][Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle] a [get_Handled][Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled] propiedad.  
    
## <a name="08355"></a>0.8.355  

[Paquete NuGet][NuGetGallery0.8.355] \| Versión 80.0.355.0 de Microsoft Edge.  

*   Ejemplo webView2API publicado, una guía completa del SDK de WebView2.  Para obtener más información, vaya a [Ejemplo de API][GithubMicrosoftedgeWebview2samplesApisample].  
*   Se agregó compatibilidad con IME para todos los idiomas además del inglés \([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Se actualizó la superficie api del `WebResourceRequested` evento en respuesta a los informes de errores.  Ahora, la especificación simultánea de un filtro y un evento en la creación está en desuso.  Para crear un evento solicitado de recurso web, use [add_WebResourceRequested][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested] para agregar el evento y [AddWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter] para agregar un filtro.  [RemoveWebResourceRequestedFilter][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter] quita el filtro \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Breaking Change:** Comportamiento de pantalla completa modificado.  [IsFullScreenAllowed en desuso][Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated].  Ahora, de forma predeterminada, si un elemento de webView \(such as a video\) está establecido en pantalla completa, rellena los límites de WebView.  Usa el [evento ContainsFullScreenElementChanged][Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355] y get_ContainsFullScreenElement para especificar cómo debe cambiar el [tamaño][Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement] de la aplicación WebView si un elemento quiere entrar en modo de pantalla completa.  
    
## <a name="08314"></a>0.8.314  

[Paquete NuGet][NuGetGallery0.8.314] \| Versión 80.0.314.0 de Microsoft Edge.  

*   Se agregó compatibilidad con Windows 7, Windows 8 y Windows 8.1.  
*   Se agregó Visual Studio y Visual Studio de depuración de código para WebView2.  Ahora, depure el script en webView2 directamente desde el IDE.  Para obtener más información, vaya [a How to debug when developing with WebView2 controls][Webview2HowtoDebug].  
*   Se agregó para que el script en ejecución en WebView2 obtenga acceso a un objeto IDispatch desde el componente Win32 de la aplicación y obtenga acceso a las propiedades del `Native Object Injection` objeto IDispatch.  Para obtener más información, vaya a [AddRemoteObject][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Evento `AcceleratorKeyPressed` agregado.  Para obtener más información, vaya [a add_AcceleratorKeyPressed][Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Desactivado el `Context Menus` .  Para obtener más información, vaya [a put_AreDefaultContextMenusEnabled][Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Actualizado `DPI Awareness` .  Ahora, el reconocimiento de PPP de WebView es el mismo que el reconocimiento de PPP de la aplicación host.  
    
    > [!NOTE]
    > Si se inicia otra aplicación híbrida con un reconocimiento de PPP diferente al WebView original, el nuevo WebView no se inicia si es el mismo `user data folder` \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Se actualizó para que WebView2 rechazara automáticamente las solicitudes de permisos de notificación que solicita el contenido `Notification Change Behavior` web hospedado en WebView.  
    
## <a name="08270"></a>0.8.270  

[Paquete NuGet][NuGetGallery0.8.270] \| Versión 78.0.270.0 de Microsoft Edge.  

*   Evento agregado `DocumentTitleChanged` para indicar el cambio de título del documento \([\#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   API `GetWebView2BrowserVersionInfo` agregada \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Evento `NewWindowRequested` agregado.  
*   Función `CreateWebView2EnvironmentWithDetails` actualizada para quitar `releaseChannelPreference` .  Para obtener más información acerca `CreateWebView2EnvironmentWithDetails` de la función, vaya a [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  La invalidación de la variable del registro y del entorno sigue siendo compatible.  La preferencia de canal predeterminada se usa a menos que se invalide.  
    Durante la búsqueda de canal, el equipo de WebView omite cualquier versión del canal anterior que no sea compatible con el SDK de WebView2.  
    El equipo de WebView selecciona el canal más estable para garantizar los comportamientos más coherentes para el usuario final.  Cuando pruebes con las compilaciones más recientes de Canary, debes crear un script para establecer la variable de entorno en antes `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` de iniciar la aplicación.  
*   Se `CreateWebView2EnvironmentWithDetails` actualizó la función con lógica para seleccionar `userDataFolder` cuando no se especificó.  Para obtener más información acerca `CreateWebView2EnvironmentWithDetails` de la función, vaya a [CreateWebView2EnvironmentWithDetails][Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails].  Si usó anteriormente la ubicación predeterminada, al cambiar al nuevo SDK, el valor predeterminado se restablece \(establecido en una nueva ubicación en el directorio de código host\) y el estado también se `userDataFolder` `userDataFolder` restablece.  Si el proceso de host no tiene permiso para escribir en el directorio especificado, es posible que la `CreateWebView2EnvironmentWithDetails` función falle.  Puede copiar los datos del antiguo `user data folder` al nuevo directorio.  
    
## <a name="08230"></a>0.8.230  

[Paquete NuGet][NuGetGallery0.8.230] \| Versión 77.0.230.0 de Microsoft Edge.  

*   Se agregó la API para detener todas las búsquedas de recursos pendientes y de navegación `Stop` \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Se `.tlb` agregó el archivo al paquete NuGet \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Se agregaron proyectos .NET a la lista de instaladores en el paquete NuGet \([\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  
    
## <a name="08190"></a>0.8.190  

[Paquete NuGet][NuGetGallery0.8.190] \| Versión 77.0.190.0 de Microsoft Edge.  

*   Se `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` agregó al control si los usuarios pueden abrir DevTools \([\#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Se agrega al control si se muestra la barra de `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` estado \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Se ha `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` agregado para volver y avanzar a través del historial de navegación.  
*   Se agregaron tipos de encabezado HTTP \( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` \) para ver y modificar encabezados HTTP en WebView.  
*   Se agregó compatibilidad con WebView de 32 bits en máquinas de 64 bits \([\#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Se agregó WebView IDL al SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Se agregó lib para admitir `IID\_\*` objetos de identificador de interfaz[\( \#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Se agregó la ruta de acceso, la vinculación y la autocopia de archivos DLL al archivo NuGet `TARGET` en sdk.  
*   Activada la solicitud `window.open()` en el script.  
    
## <a name="08149"></a>0.8.149  

[Paquete NuGet][NuGetGallery0.8.149] \| Versión 76.0.149.0 de Microsoft Edge.  

Versión preliminar del desarrollador inicial.  

<!-- Links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones mediante WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionEvergreenDistributionMode]: ./concepts/distribution.md#evergreen-distribution-mode "Modo de distribución Evergreen: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionDistributionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Modo de distribución de versiones fijas: distribución de aplicaciones mediante WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Comprender el tiempo de ejecución y el instalador de WebView2: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Directivas de grupo para WebView2: administración de aplicaciones webView2 | Microsoft Docs"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Descripción de las versiones de explorador y WebView2 | Microsoft Docs"  
[Webview2ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "API experimentales: descripción de las versiones de explorador y webView2 | Microsoft Docs"  
[Webview2ConceptsVersioningMatchingWebview2RuntimeVersions]: ./concepts/versioning.md#matching-webview2-runtime-versions "Coincidencia de versiones de WebView2 Runtime: comprender las versiones del SDK de WebView2 | Microsoft Docs"  
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Introducción a WebView2 en aplicaciones de Windows Forms | Microsoft Docs"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Introducción a WebView2 en WPF | Microsoft Docs"  
[Webview2HowtoDebug]: ./howto/debug.md "Cómo depurar al desarrollar con controles WebView2 | Microsoft Docs"  

[Webview2ReferenceWin32Icorewebview2experimental2ViewWebview210865PrereleaseAddDownloadstarting]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental2?view=webview2-1.0.865-prerelease&preserve-view=true#add_downloadstarting  "add_DownloadStarting: interfaz ICoreWebView2Experimental2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironment3ViewWebview210865PrereleaseUpdateruntime]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment3?view=webview2-1.0.865-prerelease&preserve-view=true#updateruntime  "UpdateRuntime: interfaz ICoreWebView2ExperimentalEnvironment3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalframeViewWebview210865PrereleaseAddhostobjecttoscriptwithorigins]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalframe?view=webview2-1.0.865-prerelease&preserve-view=true#addhostobjecttoscriptwithorigins  "AddHostObjectToScriptWithOrigins: interfaz ICoreWebView2ExperimentalFrame | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalsettings4ViewWebview210865PrereleaseIspinchzoomenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings4?view=webview2-1.0.865-prerelease&preserve-view=true#ispinchzoomenabled  "IsPinchZoomEnabled: interfaz ICoreWebView2ExperimentalSettings4 | Microsoft Docs" 

[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210824GetArebrowseracceleratorkeysenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings2?view=webview2-1.0.824&preserve-view=true#get_arebrowseracceleratorkeysenabled "get_AreBrowserAcceleratorKeyPressed: interfaz ICoreWebView2ExperimentalSettings | Microsoft Docs" 

[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded: interfaz ICoreWebView2_2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview22ViewWebview210721PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease&preserve-view=true#get_environment "ICoreWebView2CookieManager | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseSetvirtualhostnametofoldermapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping: interfaz ICoreWebView2_3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview23ViewWebview210790PrereleaseTrysuspend]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend: interfaz ICoreWebview2_3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2acceleratorkeypressedeventargsViewWebview209430GetHandled]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled interfaz ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2compositioncontrollerViewWebview210790Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "interfaz ICoreWebView2CompositionController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2controller2ViewWebview210790PrereleaseGetDefaultbackgroundcolor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor: interfaz ICoreWebView2Controller2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2cookiemanagerViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430AddDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview209430RemoveDevtoolsprotocoleventreceived]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environment2ViewWebview210721PrereleaseCreatewebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease&preserve-view=true#createwebresourcerequest "CreateWebResourceRequest: interfaz ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interfaz ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622GetAllowsinglesignonusingosprimaryaccount]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount: interfaz ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentoptionsViewWebview209622PutAdditionalbrowserarguments]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments: interfaz ICoreWebView2EnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209430GetBrowserversioninfo]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo: interfaz ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2environmentViewWebview209488GetBrowserversionstring]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring "get_BrowserVersionString: interfaz ICoreWebView2Environment | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller2ViewWebview210674PrereleaseGetSystemcursorid]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2?view=webview2-1.0.674-prerelease&preserve-view=true#get_systemcursorid "interfaz ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontroller3ViewWebview210721Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCompositionController3 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcompositioncontrollerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCompositionController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged: interfaz ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsmode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode- interfaz ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale: interfaz ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShoulddetectmonitorscalechanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges: interfaz ICoreWebView2ExperimentalController | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalcursorchangedeventhandlerViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalenvironmentoptionsViewWebview209538PrereleaseGetIssinglesignonusingosprimaryaccountenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled- interfaz ICoreWebView2ExperimentalEnvironmentOptions | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsViewWebview209538PrereleaseGetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures- interfaz ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalpointerinfoViewWebview209488Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalPointerInfo | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalsettingsViewWebview210790PrereleaseGetUseragent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent: interfaz ICoreWebView2ExperimentalSettings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview209538PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived: interfaz ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddDomcontentloaded]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded: interfaz ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseAddWebresourceresponsereceived]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived: interfaz ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetCookiemanager]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager: interfaz ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseGetEnvironment]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment: interfaz ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalViewWebview210674PrereleaseNavigatewithwebresourcerequest]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest: interfaz ICoreWebView2Experimental | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsViewWebview209628PrereleasePopulateresponsecontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent: interfaz ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwebresourceresponseviewViewWebview210674PrereleaseGetcontent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent: interfaz ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2experimentalwindowfeaturesViewWebview209538Prerelease]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalWindowFeatures | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430GetZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor: interfaz ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Notifyparentwindowpositionchanged]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged: interfaz ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430PutZoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor: interfaz ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2hostViewWebview209430Setboundsandzoomfactor]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor: interfaz ICoreWebView2Host | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httpheaderscollectioniteratorViewWebview209430GetHascurrentheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader: interfaz ICoreWebView2HttpHeadersCollectionIterator | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httprequestheadersViewWebview209430Getheaders]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders: interfaz ICoreWebView2HttpRequestHeaders | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2httpresponseheadersViewWebview209430Getheader]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader: interfaz ICoreWebView2HttpResponseHeaders | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209538GetIsuserinitiated]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated interfaz ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2newwindowrequestedeventargsViewWebview209622GetWindowfeatures]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures- interfaz ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed: interfaz ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209430GetIszoomcontrolenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled: interfaz ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetAreremoteobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed: interfaz ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209488GetIsbuiltinerrorpageenabled]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled "get_IsBuiltInErrorPageEnabled: interfaz ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2settingsViewWebview209538GetArehostobjectsallowed]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed: interfaz ICoreWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddContentloading]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddHistorychanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Addremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddSourcechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430AddWindowcloserequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430CoreWebview2ScriptDialogKind]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209430Removeremoteobject]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddFramenavigationcompleted]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Addhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488AddNewwindowrequested]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209488Removehostobjectfromscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2ViewWebview209538ddhostobjecttoscript]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.538&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript: interfaz ICoreWebView2 | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2webmessagereceivedeventargsViewWebview209430Trygetwebmessageasstring]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString: interfaz ICoreWebView2WebMessageReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerViewWebview210790PrereleaseInvoke]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invoke: interfaz ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Microsoft Docs" 
[Webview2ReferenceWin32Icorewebview2windowfeaturesViewWebview209622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interfaz ICoreWebView2WindowFeatures | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2acceleratorkeypressedeventargsViewWebview208355Handle]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Handle: interfaz IWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandlerViewWebview208355]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interfaz IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2settings2ViewWebview208355PutAredefaultcontextmenusenabled]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled: interfaz IWebView2Settings2 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2settingsViewWebview208355GetIsfullscreenallowedDeprecated]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated: interfaz IWebView2Settings | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webmessagereceivedeventargsViewWebview208355GetWebmessageasstring]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString: interfaz IWebView2WebMessageReceivedEventArgs | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355AddAcceleratorkeypressed]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed: interfaz IWebView2WebView4 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview4ViewWebview208355Addremoteobject]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject: interfaz IWebView2WebView4 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355AddWebresourcerequested]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested: interfaz IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Addwebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter: interfaz IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355GetContainsfullscreenelement]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement: interfaz IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webview5ViewWebview208355Removewebresourcerequestedfilter]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter: interfaz IWebView2WebView5 | Microsoft Docs" 
[Webview2ReferenceWin32Iwebview2webviewViewWebview208355AddDocumentstatechanged]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged: interfaz IWebView2WebView | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview208355Createwebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails- Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209430Getcorewebview2browserversioninfo]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo: global | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithdetails]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails- Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209488Getavailablecorewebview2browserversionstring]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString: global | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209538Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions - Globals | Microsoft Docs" 
[Webview2ReferenceWin32Webview2IdlViewWebview209622Createcorewebview2environmentwithoptions]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions- Globals | Microsoft Edge" 

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge: directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2: directivas | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Espacio de nombres Microsoft.Web.WebView2.Core | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Clase CoreWebView2 (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Clase CoreWebView2Environment (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "Método CoreWebView2Environment.CompareBrowserVersions(String, String) (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Método CoreWebView2Environment.GetAvailableBrowserVersionString(String) (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Clase CoreWebView2HttpRequestHeaders (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Clase CoreWebView2HttpResponseHeaders (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Evento CoreWebView2.NewWindowRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Evento CoreWebView2.PermissionRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Evento CoreWebView2.ScriptDialogOpening (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Evento CoreWebView2.WebResourceRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Clase CoreWebView2InitializationCompletedEventArgs | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft.Web.WebView2.WinForms | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Clase CoreWebView2CreationProperties (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Clase Webview2.Source (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "Método WebView2.BuildWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Método WebView2.DestroyWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Clase CancelEventArgs (System.ComponentModel) | Microsoft Docs"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Clase EventArgs (System) | Microsoft Docs"  

[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Ensamblados con nombre | Microsoft Docs"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Protección de aplicaciones de Microsoft Defender (Windows 10): seguridad de Windows | Microsoft Docs"  
[WindowsWin32ApiWinuserSetWindowDisplayAffinity]: /windows/win32/api/winuser/nf-winuser-setwindowdisplayaffinity "Función SetWindowDisplayAffinity (winuser.h): aplicaciones de Win32 | Microsoft Docs"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]: https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Repositorio de anuncios para MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesWebview2wpfbrowser]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2WpfBrowser "WebView2WpfBrowser: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Move project to use latest WebView2 SDK 0.9.430 - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue37]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 37"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue58]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 58"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 119"  
[GithubMicrosoftedgeWebviewfeedbackIssue122]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 122"  
[GithubMicrosoftedgeWebviewfeedbackIssue131]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 131"  
[GithubMicrosoftedgeWebviewfeedbackIssue148]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue161]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 161"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 168"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 177"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 179"  
[GithubMicrosoftedgeWebviewfeedbackIssue181]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 181"  
[GithubMicrosoftedgeWebviewfeedbackIssue183]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 183"  
[GithubMicrosoftedgeWebviewfeedbackIssue185]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 185"  
[GithubMicrosoftedgeWebviewfeedbackIssue196]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 196"  
[GithubMicrosoftedgeWebviewfeedbackIssue204]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 204"  
[GithubMicrosoftedgeWebviewfeedbackIssue205]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 205"  
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 210"  
[GithubMicrosoftedgeWebviewfeedbackIssue212]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 212"  
[GithubMicrosoftedgeWebviewfeedbackIssue219]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 219"  
[GithubMicrosoftedgeWebviewfeedbackIssue228]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 228"  
[GithubMicrosoftedgeWebviewfeedbackIssue235]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 235"  
[GithubMicrosoftedgeWebviewfeedbackIssue250]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 250"  
[GithubMicrosoftedgeWebviewfeedbackIssue275]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 275"  
[GithubMicrosoftedgeWebviewfeedbackIssue288]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 288"  
[GithubMicrosoftedgeWebviewfeedbackIssue293]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 293"  
[GithubMicrosoftedgeWebviewfeedbackIssue318]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 335"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 371"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue399]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 399"  
[GithubMicrosoftedgeWebviewfeedbackIssue400]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 400"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 409"  
[GithubMicrosoftedgeWebviewfeedbackIssue414]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 414"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 432"  
[GithubMicrosoftedgeWebviewfeedbackIssue442]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 442"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 461"  
[GithubMicrosoftedgeWebviewfeedbackIssue506]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/506 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 506"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 525"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 549"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Problema 560"  
[GithubMicrosoftedgeWebviewfeedbackIssue568]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/568 "Repositorio de comentarios de MicrosoftEdge/WebViewFeedback Issue 568"  
[GithubMicrosoftedgeWebviewfeedbackIssue585]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 585"  
[GithubMicrosoftedgeWebviewfeedbackIssue604]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/604 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 604"  
[GithubMicrosoftedgeWebviewfeedbackIssue605]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 605"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 611"  
[GithubMicrosoftedgeWebviewfeedbackIssue669]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/669 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 669"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 691"  
[GithubMicrosoftedgeWebviewfeedbackIssue816]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 816"  
[GithubMicrosoftedgeWebviewfeedbackIssue851]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/851 "Repositorio de comentarios de MicrosoftEdge/WebViewFeedback Issue 851"  
[GithubMicrosoftedgeWebviewfeedbackIssue875]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 875"  
[GithubMicrosoftedgeWebviewfeedbackIssue878]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 878"  
[GithubMicrosoftedgeWebviewfeedbackIssue1120]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1120 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 1120"
[GithubMicrosoftedgeWebviewfeedbackIssue940]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/940 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 940"
[GithubMicrosoftedgeWebviewfeedbackIssue841]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/841 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 841"
[GithubMicrosoftedgeWebviewfeedbackIssue210]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 210"
[GithubMicrosoftedgeWebviewfeedbackIssue338]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/338 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 338"
[GithubMicrosoftedgeWebviewfeedbackIssue589]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/589 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 589"
[GithubMicrosoftedgeWebviewfeedbackIssue933]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/933 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 933"
[GithubMicrosoftedgeWebviewfeedbackIssue946]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/946 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 946"
[GithubMicrosoftedgeWebviewfeedbackIssue1011]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1011 "Repositorio de comentarios de MicrosoftEdge/WebViewFeedback Issue 1011"
[GithubMicrosoftedgeWebviewfeedbackIssue1050]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/1050 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 1050"
[GithubMicrosoftedgeWebviewfeedbackIssue996]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/996 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 996"
[GithubMicrosoftedgeWebviewfeedbackIssue850]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/850 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 850"

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Anuncio de disponibilidad general para Microsoft Edge WebView2 para .NET y método de distribución fija | blog de .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Desarrollador de Microsoft Edge"  

[NuGetGallery]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Galería nuGet | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galería nuGet | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galería nuGet | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galería nuGet | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galería nuGet | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galería nuGet | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galería nuGet | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galería nuGet | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galería nuGet | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v0.9.515"  
[NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Galería nuGet | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Galería nuGet | Microsoft.Web.WebView2 v0.9.579"  
[NuGetGallery0.9.622.11]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Galería nuGet | Microsoft.Web.WebView2 v0.9.622.11"  
[NuGetGallery0.9.628-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v0.9.628"  
[NuGetGallery1.0.622.22]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Galería nuGet | Microsoft.Web.WebView2 v1.0.622.22"  
[NuGetGallery1.0.664.34]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "Galería nuGet | Microsoft.Web.WebView2 v1.0.664.34"  
[NuGetGallery1.0.664.37]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "Galería nuGet | Microsoft.Web.WebView2 v1.0.664.37"  
[NuGetGallery1.0.674-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v1.0.674"  
[NuGetGallery1.0.705.50]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "Galería nuGet | Microsoft.Web.WebView2 v1.0.705.50"  
[NuGetGallery1.0.721-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v1.0.721"  
[NuGetGallery1.0.774.44]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.774.44 "Galería nuGet | Microsoft.Web.WebView2 v1.0.774.44"  
[NuGetGallery1.0.790-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v1.0.790"  
[NuGetGallery1.0.818.41]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.818.41 "Galería nuGet | Microsoft.Web.WebView2 v1.0.818.41"  
[NuGetGallery1.0.824-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.824-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v1.0.824"  
[NuGetGallery1.0.865-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.865-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v1.0.865"  

[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Anuncio de disponibilidad general de Microsoft Edge WebView2 | Microsoft Edge Blog"  
