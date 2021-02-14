---
description: Notas de la versión del SDK de Microsoft Edge WebView2
title: Notas de la versión de Microsoft Edge WebView2 para Win32, WPF y WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, aplicaciones win32, win32, edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, edge html
ms.openlocfilehash: 43df4c6155350881059fc6ca7f6fe3a047ba0f12
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327641"
---
# Notas de la versión del SDK de WebView2  

El equipo de WebView2 actualiza el [SDK de WebView2][NuGetGallery] con una cadencia de seis semanas.  Revise el siguiente contenido para obtener información actualizada sobre los anuncios de productos, las adiciones, las modificaciones y los cambios importantes en las API.  

> [!NOTE]
> Asegúrate de volver a compilar la aplicación después de actualizar el paquete de NuGet.  El equipo recomienda usar el canal Canary al desarrollar con los paquetes de versión preliminar y el tiempo de ejecución de hoja de vida al usar paquetes publicados.  Para obtener más información, vaya [a Control de versiones.][VersioningDoc]  
 
## 1.0.790-prerelease  

Fecha de lanzamiento: 10 de febrero de 2021  

[Paquete NuGet][NuGetGallery1.0.790-prerelease] \| Microsoft Edge versión 86.0.616.0 o posterior  

### General  

> [!IMPORTANT]
> **Cambio importante:** el paquete de versión previa a WebView2 1.0.781 está en desuso.  Suspenda el desarrollo con este paquete.  

> [!IMPORTANT]
> El paquete de versión previa a WebView2 0.9.430 está en desuso y se está quitando de la próxima versión.  Si la aplicación WebView usa el paquete, te recomendamos actualizar a un paquete más reciente.  

##### Características  

*   Se [agregaron los métodos TrySuspend y Resume][ReferenceWin32Icorewebview210790PreReleaseTrySuspendResume] para suspender y reanudar WebViews.  
*   Se [agregó el método SetVirtualHostNameToFolderMapping][ReferenceWin32Icorewebview210790PreReleaseSetVirtualHostNameToFolderMapping] que asigna un nombre de host virtual a una ruta de directorio.  \([\#37][GithubMicrosoftedgeWebviewfeedbackIssue37], [\#161][GithubMicrosoftedgeWebviewfeedbackIssue161]y [\#212][GithubMicrosoftedgeWebviewfeedbackIssue212]\).  
*   Se agregó [la propiedad DefaultBackgroundColor][ReferenceWin32Icorewebview2controllerViewWebview210790PreReleaseDefaultBackgroundColor] para establecer el color y el canal alfa del fondo.  \([\#414][GithubMicrosoftedgeWebviewfeedbackIssue414]\).  
*   Se agregó [la propiedad UserAgent][ReferenceWin32Icorewebview2experimentalsettings10790PreReleaseGetUserAgent] para obtener o establecer el agente de usuario.  \([\#122][GithubMicrosoftedgeWebviewfeedbackIssue122]\).
*   Se `CreateCookieWithCookie` reemplazó el método por `CopyCookie` el método.  
*   Se ha agregado compatibilidad de hospedaje visual con la interfaz [ICoreWebView2CompositionController,][ReferenceWin32Icorewebview2controllerViewWebview210790CompositionController] que se crea con el nuevo `CreateCoreWebView2CompositionController` método de `ICoreWebView2Environment3` .  

    
##### Correcciones de errores  

*   Se ha desactivado la característica De compras de Microsoft Edge en WebView2.  
*   Desactivado el menú contextual en el visor de PDF cuando `AreDefaultContextMenusEnabled` está `false` .  \([\#605][GithubMicrosoftedgeWebviewfeedbackIssue605]\).  
*   Se ha corregido un error que `E_NOINTERFACE` se devolvió al `ICoreWebView2` consultar `ICoreWebView2Experimental` .  \([\#691][GithubMicrosoftedgeWebviewfeedbackIssue691]\).  
*   Se ha corregido un error que permitía la navegación con URI con formato de error `CoreWebView2NavigationStartingEventArgs.Cancel` cuando se estableció en `false` .  \([\#400][GithubMicrosoftedgeWebviewfeedbackIssue400]\).  
*   Se ha corregido un error que `window.print()` bloqueaba las ventanas emergentes con controladores de eventos adjuntos a `NewWindowRequested` eventos.  \([\#409][GithubMicrosoftedgeWebviewfeedbackIssue409]\).  
*   Se ha corregido un problema de PPP dinámico al mover aplicaciones entre diferentes monitores.  \([\#58][GithubMicrosoftedgeWebviewfeedbackIssue58]\)  
*   Se han mejorado `HRESULT` los s pasados por [ICoreWebView2WebResourceResponseViewGetContentCompletedHandler::Invoke][ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerInvoke10790].  
*   Botón De administración de autorrellenar deshabilitado.  \([\#585][GithubMicrosoftedgeWebviewfeedbackIssue585]\). 
*   Se Visual Studio bloqueos de llamadas `WebView2.Dispose` cuando se hospedan en varias ventanas.  \([\#816][GithubMicrosoftedgeWebviewfeedbackIssue816]\ y [\#442][GithubMicrosoftedgeWebviewfeedbackIssue442]\).  
*   Se ha corregido un error para mostrar el control WebView2 en Visual Studio cuadro de herramientas.  \([\#210][GithubMicrosoftedgeWebviewfeedbackIssue210]\). 
*   Se han reducido los problemas de uso elevado de CPU.  \([\#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
*   Se han corregido problemas con el paquete de versión preliminar 1.0.781 en desuso. [\#875][GithubMicrosoftedgeWebviewfeedbackIssue875] [y \#878][GithubMicrosoftedgeWebviewfeedbackIssue878]\).  
    
##### Promociones  

*   Las siguientes API experimentales ahora se promueven a Estable.  
    *   API de hospedaje visual.  
    *   [SetVirtualHostNameToFolderMapping][ReferenceWin32Icorewebview210790PreReleaseSetVirtualHostNameToFolderMapping]  
    *   [TrySuspend y Resume][ReferenceWin32Icorewebview210790PreReleaseTrySuspendResume]  
    *   [DefaultBackgroundColor][ReferenceWin32Icorewebview2controllerViewWebview210790PreReleaseDefaultBackgroundColor]  
    
#### .NET  

##### Correcciones de errores  

*   Se ha corregido un error que bloqueaba las aplicaciones WebView que usan el SDK de WPF.  El bloqueo se produjo cuando las ventanas se cerraron con la tecla F4.  \([\#399][GithubMicrosoftedgeWebviewfeedbackIssue399]\).  
*   La pantalla de inicialización de WebView2 es ahora transparente, en lugar de gris.  \([\#196][GithubMicrosoftedgeWebviewfeedbackIssue196]\).  
    
## 1.0.705.50  

Fecha de lanzamiento: 25 de enero de 2021  

[Paquete NuGet][NuGetGallery1.0.705.50] \| WebView2 Runtime versión 86.0.616.0 o posterior  

##### Promociones  

*   Las siguientes API experimentales ahora se promueven a Estable.  
    *   [WebResourceResponseReceived API][WebResourceResponseReceivedAPI]  
    *   [NavigateWithWebResourceRequest API][NavigateWithWebResourceRequestAPI]  
    *   [API de administración de cookies][CookiemanagementAPI]  
    *   [DOMContentLoaded API][DOMContentLoadedAPI]  
    *   [WebView Environment (propiedad)][WebViewEnvironmentproperty]  

## 1.0.721-prerelease  

Fecha de lanzamiento: 8 de diciembre de 2020  

[Paquete NuGet][NuGetGallery1.0.721-prerelease] \| Microsoft Edge versión 86.0.616.0 o posterior  

#### General  

> [!IMPORTANT]
> **Cambio importante:** los paquetes de versión previa a WebView2 1.0.707 y 0.9.628 están en desuso.  Suspenda el desarrollo con estos paquetes.  

###### Características  

*   Se agregaron [directivas de grupo de WebView2][DeployedgeMicrosoftEdgeWebviewPolicies].  Para obtener más información sobre las prácticas recomendadas, vaya a [las directivas de grupo de WebView2][Webview2ConceptsEnterpriseGroupPoliciesForWebview2].  
*   > [!IMPORTANT]
    > **Cambio importante:** en desuso la antigua ubicación del Registro.  
    > 
    > ```text
    > {Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}
    > ```  
    
*   Se ha agregado compatibilidad con [Arrastrar y colocar][ReferenceWin32Icorewebview2experimentalcompositioncontroller3] en WebView2.  
*   Se agregaron API para controlar la compatibilidad con PPP.  
    *   Se agregó [la propiedad RasterizationScale][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale] para cambiar la escala de PPP para el contenido webView y los elementos emergentes de la interfaz de usuario, y el [evento RasterizationScaleChanged][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged] asociado.  
    *   Se [agregó la propiedad ShouldDetectMonitorScaleChanges][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShouldDetectMonitorScaleChanges] para actualizar automáticamente `RasterizationScale` la propiedad si es necesario.  
    *   Se agregó la propiedad [BoundsMode][ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsMode] para especificar que los límites son píxeles lógicos y permiten que WebView use para la visualización de píxeles webView2, y WebView usa el con el para obtener el `RasterizationScale` `RasterizationScale` tamaño `Bounds` físico.  
*   Evento `NewWindowRequested` actualizado para controlar y `Ctrl` + `click` `Shift` + `click` .  \([\#168][GithubMicrosoftedgeWebviewfeedbackIssue168] [\#371][GithubMicrosoftedgeWebviewfeedbackIssue371]\).  
*   Las siguientes API experimentales ahora se promueven a Estable.  
    *   [WebResourceResponseReceived API][WebResourceResponseReceivedAPI]  
    *   [NavigateWithWebResourceRequest API][NavigateWithWebResourceRequestAPI]  
    *   [API de administración de cookies][CookiemanagementAPI]  
    *   [DOMContentLoaded API][DOMContentLoadedAPI]  
    *   [WebView Environment (propiedad)][WebViewEnvironmentproperty]  
        
#### .NET  

###### Características  

*   Activado el diseñador de WinForms en .NET Core 3.1+ y .NET 5.  
*   Administración mejorada de cookies de .NET.  \([\#611][GithubMicrosoftedgeWebviewfeedbackIssue611]\).  
*   Reemplazado `CoreWebView2Ready` por [CoreWebView2InitializationCompleted][DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs].  

###### Correcciones de errores

*   Se agregó [el evento AcceleratorKeyPressed][DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed] para admitir la presión AcceleratorKey en WebView2.  \([\#288][GithubMicrosoftedgeWebviewfeedbackIssue288]\).  
*   Se quitaron los archivos innecesarios de salida a las carpetas WebView2.  \([\#461][GithubMicrosoftedgeWebviewfeedbackIssue461]\).  
*   API de objeto de host mejorada.  \([\#335][GithubMicrosoftedgeWebviewfeedbackIssue335] [\#525][GithubMicrosoftedgeWebviewfeedbackIssue525]\).  
    
## 1.0.664.37  

Fecha de lanzamiento: 20 de noviembre de 2020  

[Paquete NuGet][NuGetGallery1.0.664.37] \| WebView2 Runtime versión 86.0.616.0 o posterior.  

#### General  

> [!IMPORTANT]
> **Anuncio:** los SDK de .NET WPF/WinForms WebView2 ahora están generalmente disponibles \(GA\).  A partir de esta versión, los SDK de la versión son compatibles con el reenvío.  Para obtener más información, vaya a la [entrada de blog del anuncio de GA.][MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]  

###### Características  

*   .NET WPF/WinForms WebView2 ahora está disponible generalmente \(GA\).  
*   El modo de distribución fija \(Bring-your-own\) alcanzó ga.  
    
#### .NET  

###### Correcciones de errores  

*   `CoreWebView2NewWindowRequestedEventArgs.Handled` impide que se abra una nueva ventana.  \([\#549][GithubMicrosoftedgeWebviewfeedbackIssue549] [\#560][GithubMicrosoftedgeWebviewfeedbackIssue560]\).  
    
## 1.0.674-prerelease  

Fecha de lanzamiento: 19 de octubre de 2020  

[Paquete NuGet][NuGetGallery1.0.674-prerelease] \| WebView2 Runtime versión 86.0.616.0 o posterior.  

#### General  

*   Se agregó [el método NavigateWithWebResourceRequest para][ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674] proporcionar datos de publicación u otros encabezados de solicitud durante la navegación.  
*   Se [agregó el evento DOMContentLoaded][ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674] que se ejecuta cuando se carga y analiza el documento HTML inicial.  
*   Se agregó [la propiedad Environment][ReferenceWin32Icorewebview2experimentalGetEnvironment10674] en WebView2.  Esta propiedad expone el entorno webView2 donde se creó una instancia de WebView2.  
*   Se [agregaron API de administración][ReferenceWin32Icorewebview2experimentalGetCookiemanager10674] de cookies que permiten a los desarrolladores autenticar la sesión de WebView2 o recuperar cookies de WebView para autenticar otras herramientas.  El equipo de Webview planea realizar mejoras específicas del lenguaje o del marco de trabajo.  Para obtener más información, vaya a [Revisión de API: Administración de cookies.][GithubMicrosoftedgeWebview2AnnouncementIssue2]  
*   Se actualizó el evento [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674] y se agregaron [WebResourceResponseView][ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674] y [WebResourceResponseReceivedEventArgs::P opulateResponseContent][ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628] a [WebResourceResponseView::GetContent][ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674].  
*   Desactivado la [Protección de aplicaciones de Microsoft Defender (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] en WebView2.  
*   Se [agregó SystemCursorId][ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674] para el hospedaje visual.  
*   Se ha agregado un error corregido para el método de entrada en el hospedaje visual.  
*   Se ha quitado el requisito `version.lib` de incluir al usar la biblioteca estática WebView2.  
    
#### .NET  

*   Se actualizó la clase [CoreWebView2][DotnetApiMicrosoftWebWebview2CoreCorewebview2] para exponer la `CoreWebView2Environment` variable.  
*   Se han cambiado las implementaciones de clases EventArgs personalizadas en el espacio de nombres a `Microsoft.Web.WebView2.Core` subclases [de System.EventArgs][DotnetApiSystemEventargs] o [System.ComponentModel.CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs].  \([\#250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Se ha agregado compatibilidad [con CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] en WinForms.  \([\#204][GithubMicrosoftedgeWebviewfeedbackIssue204]\)
*   Se [agregaron API webResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] .NET.  \([\#219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Se actualizó la propiedad De origen del diseñador [de][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] WinForms de forma predeterminada o se restablece a null.  \([\#177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Se actualizaron los límites de WebView2 WebView2.Init() para admitir modos de PPP inferiores al 100 %.  \([\#432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   Se [actualizaron BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] [y DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] para aumentar la solidez.  \([\#382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Se actualizó la base del cargador de .NET para cargar en el bit de proceso en lugar de en la arquitectura del sistema operativo.  \([\#431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Se cambió `EdgeNotFoundExpection` el [nombre a WebView2RuntimeNotFoundException][DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception].  
    
## 1.0.622.22  

Fecha de lanzamiento: 19 de octubre de 2020  

[Paquete NuGet][NuGetGallery1.0.622.22] \| WebView2 Runtime versión 86.0.616.0 o posterior.  

#### General  

> [!IMPORTANT]
> **Anuncio:** Win32 C/C++ WebView2 ahora está disponible generalmente \(GA\).  A partir de esta versión, los SDK de la versión son compatibles con el reenvío.  Para obtener más información, vaya a la entrada [de blog del anuncio de GA.][WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]  

*   [El runtime y el instalador de WebView2 de Evergreen][Webview2ConceptsDistributionUnderstandRuntimeInstaller] son GA.  Bootstrapper, downlink link for the Bootstrapper, and Standalone Installer for the Evergreen WebView2 Runtime are available on [Microsoft Edge WebView2][MicrosoftDeveloperMicrosoftEdgeWebView2].  El código de ejemplo para el flujo de trabajo de instalación también está disponible en el repositorio [WebView2Samples][GithubMicrosoftedgeWebview2samplesMain].  
*   [El modo de versión fija][Webview2ConceptsDistributionFixedVersionMode] está disponible para la versión preliminar del desarrollador.  
    
## 0.9.622.11  

Fecha de lanzamiento: 10 de septiembre de 2020  

[Paquete NuGet][NuGetGallery0.9.622.11] \| WebView2 Runtime versión 86.0.616.0 o posterior.  

#### General  

*   > [!IMPORTANT]
    > **Anuncio:** este SDK es el candidato de lanzamiento para WebView2 Win32 C/C++ GA.  La versión ga debe usar la misma interfaz y funcionalidad de la API.  
    
*   Directivas de [explorador desconectadas.][DeployedgeMicrosoftEdgePolicies]  
*   Se [agregó la propiedad AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622] en las opciones del entorno WebView2 para activar el acceso condicional para WebView.  
*   Se `ICoreWebView2NewWindowRequestedEventArgs` actualizó [para incluir la propiedad WindowFeatures][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622] y el [objeto ICoreWebView2WindowFeatures asociado.][ReferenceWin32Icorewebview2windowfeatures09622]  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Actualizado `System.Windows.Rect`  para su uso en lugar de `System.Drawing.Rectangle` `System.Windows.Rect` \([\#235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Se actualizó el evento NewWindowRequested para controlar `window.open()` la solicitud sin parámetros.  \([\#293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [Los valores adicionales deBrowserArguments especificados][ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622] con no se reemplazan con `ICoreWebView2EnvironmentOptions` variables de entorno o valores del Registro.  Para obtener más información, vaya [a CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622].  
    
## 0.9.579  

Fecha de lanzamiento: 20 de julio de 2020  

[Paquete NuGet][NuGetGallery0.9.579] \| Microsoft Edge versión 86.0.579.0.  

#### General  

*   > [!IMPORTANT]
    > **Anuncio:** Runtime de Evergreen WebView2 y el instalador se lanzan para la versión preliminar.  Para obtener más información, vaya [a Distribución de WebView2][Webview2ConceptsDistributionUnderstandRuntimeInstaller].  
    
*   > [!IMPORTANT]
    > **Anuncio:** las siguientes versiones del SDK de WebView2 ya no se admiten después de la próxima versión del SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Las versiones del SDK de WebView2 también están marcadas como en desuso en nuget.org.  WebView2 recomienda mantenerse al día con la versión más reciente de WebView2.  
    
*   Se agregaron mejoras en los subprocesos de trabajo de WebView.  \([\#318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Desactivado el bloqueador de elementos emergentes en WebView.  Para obtener más información, vaya a la [propiedad IsUserInitiated][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538] del `NewWindowRequested` evento.  
*   Se ha asegurado de que se ejecuta el evento de inicio de navegación WebView para `about:blank` .  Ahora, los eventos se ejecutan para toda la navegación, pero las cancelaciones para `NavigationStarting` `about:blank` o iframe no se `srcdoc` admiten ni se omiten.  
*   Se bloquearon `edge://` algunos esquemas de URI en WebView.  
*   Se agregó la propiedad experimental [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538] en las opciones del entorno WebView2 para activar el acceso condicional para WebView.  
*   Se agregó [el evento experimental WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538] que se ejecuta después de que WebView recibe y procesa la respuesta de una solicitud WebResource.  Los encabezados de autenticación, si los hay, se incluyen en el objeto de respuesta.  
    
#### .NET  

*   Se ha mejorado el control de foco de WPF.  \([\#185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Se `ZoomFactor` agregó la propiedad en el controlador Webview2 wpf.  
    
## 0.9.538  

[Paquete NuGet][NuGetGallery0.9.538] \| Microsoft Edge versión 85.0.538.0.  

#### General  

*   Dejar de admitir la versión [0.8.149](#08149)del SDK de WebView2.  WebView2 recomienda mantenerse al día con la versión más reciente de WebView2.  
*   Directiva de grupo actualizada para tener en cuenta cuándo se modifica la ruta de acceso de perfil del explorador Microsoft Edge \([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  
    
#### Win32 C/C++  

*   Se agregó [ICoreWebView2ExperimentalNewWindowRequestedEventArgs::get_WindowFeatures][ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538], que se activa cuando se ejecuta y se asocia con `window.open()` [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin32Icorewebview2experimentalwindowfeatures09538] \([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Cambio importante:** [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] en desuso y reemplazado por [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538].  
    
*   > [!IMPORTANT]
    > **Cambio importante:** para garantizar que la API de WebView2 se alinee con las convenciones de nomenclatura de la API de Windows, el equipo de WebView actualizó los nombres de lo siguiente.  
    > 
    > *   [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488] es [ahora AreHostObjectsAllowed][ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538].  
    
*   [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09538]actualizado.  Los marcadores del serializador de objetos host originales ahora se establecen en los objetos proxy.  A continuación, los marcadores del serializador de objetos host se serializan como un objeto host cuando se pasan como un parámetro en la devolución de llamada de JavaScript \([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  
    
#### .NET (versión previa 0.9.538)  

*   Se han publicado los ejemplos WinForms y WPF WebView2API, que son guías completas del SDK de WebView2.  Para obtener más información, vaya a [Repositorio de muestras.][GithubMicrosoftedgeWebview2samplesMain]  
*   Se ha agregado compatibilidad con las API experimentales de hospedaje visual y características [de ventana.][ConceptsVersioningExperimentalApis]  
*   > [!IMPORTANT]
    > **Cambio importante:** los siguientes aplazamientos ahora implementan IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]y [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
    
*   Se [agregaron GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] y [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] como [estáticos CoreWebView2Environment.][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]  
    
## 0.9.515-prerelease  

[Paquete NuGet][NuGetGallery0.9.515-prerelease] \| Microsoft Edge versión 84.0.515.0.  

*   > [!IMPORTANT]
    > **Anuncio:** WebView2 ahora admite Windows Forms y WPF en .NET Framework 4.6.2 o posterior y .NET Core 3.0 o posterior en el paquete **de**versión previa.  
    
*   Para obtener más información acerca de la creación de aplicaciones WPF, vaya a la Guía de introducción a [WPF][GettingstartedWpf] y a la referencia de [WPF][DotnetApiMicrosoftWebWebview2Wpf] WebView2 para LAS API específicas de WPF.  
*   Para obtener más información acerca de la creación de aplicaciones de Windows Forms, vaya a la Guía de introducción de [Windows Forms][GettingstartedWinforms] y a la Referencia de [Windows Forms][DotnetApiMicrosoftWebWebview2Winforms] WebView2 para API específicas de Windows Forms.  
*   Para obtener más información acerca de las API de CoreWebView2, vaya a [.NET Reference][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Problemas conocidos:** el equipo de WebView es consciente de algunos problemas de la versión previa que se están resolviendo en versiones futuras.  
    > 
    > *   **Reconocimiento de PPP:** WebView2 para WPF actualmente no es compatible con PPP.  Al inicializar WebView2 en monitores con valores altos de PPP, existe un problema conocido por el que WebView se inicializa al principio como una fracción de la ventana hasta que se cambia el tamaño de la ventana.  
    > *   **Diseñador WPF:** el diseñador WPF no se admite actualmente.  Agrega el control WebView2 en tu aplicación modificando directamente el XAML adecuado en un editor de texto.  
    
## 0.9.488  

[Paquete NuGet][NuGetGallery0.9.488] \| Microsoft Edge versión 84.0.488.0.  

*   > [!IMPORTANT]
    > **Anuncio:** a partir de la próxima versión 83 de Microsoft Edge, Evergreen WebView ya no tiene como destino el canal de explorador estable.  En su lugar, está dirigido a otro conjunto de archivos binarios, branded [Evergreen WebView2 Runtime,][ConceptsDistributionEvergreenMode]que puede encadenar la instalación a través de un instalador que el equipo de WebView está desarrollando actualmente.  Para obtener más información, vaya [a Distribución de aplicaciones.][ConceptsDistribution]  
    
*   > [!IMPORTANT]
    > **Anuncio:** más adelante, el equipo de WebView lanza dos paquetes: un paquete de versión previa con API experimentales \(para que lo pruebes\) y un paquete de versión estable con API estables \(para tu confianza\).  Para obtener información sobre las diferencias, vaya a [Descripción de las versiones del explorador y WebView2][ConceptsVersioning].  
    
*   > [!IMPORTANT]
    > **Cambio importante:** para garantizar que la API de WebView2 se alinee con las convenciones de nomenclatura de la API de Windows, el equipo de WebView actualizó los nombres de las siguientes interfaces.  
    > 
    > *   `CORE_WEBVIEW2_*` prefix es ahora `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430] es [ahora GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488].  
    > *   [get_BrowserVersionInfo][ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430] [está][ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]get_BrowserVersionString .  
    > *   [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] es [ahora AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09488].  
    > *   [RemoveRemoteObject][ReferenceWin32Icorewebview2Removeremoteobject09430] es [ahora RemoveHostObjectFromScript][ReferenceWin32Icorewebview2Removehostobjectfromscript09488].  
    > *   `chrome.webview.remoteObjects` es ahora `chrome.webview.hostObjects` .  
    
*   > [!IMPORTANT]
    > **Cambio importante:** también se cambia el nombre de los métodos `AddRemoteObject` de proxy js.  
    > 
    > *   `getLocal` es ahora `getLocalProperty` .  
    > *   `setLocal` es ahora `setLocalProperty` .  
    > *   `getRemote` es ahora `getHostProperty` .  
    > *   `setRemote` es ahora `setHostProperty` .  
    > *   `applyRemote` es ahora `applyHostFunction` .  
    
*   > [!IMPORTANT]
    > **Cambio importante:** [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] en desuso y reemplazado por [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488].  
    
*   Se [agregó el evento FrameNavigationCompleted.][ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]  Ahora, cuando un iframe completa la navegación, se ejecuta un evento y devuelve el éxito de la navegación y el identificador de navegación.  
*   Se [agregó la interfaz ICoreWebView2EnvironmentOptions,][ReferenceWin32Icorewebview2environmentoptions09488] que puede usarse para determinar la versión de WebView2 Runtime de destino de la aplicación.  
*   Se agregó [la configuración IsBuiltInErrorPageEnabled.][ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]  Ahora, puede elegir activar o desactivar la página web de error integrada para el error de navegación y representar el error del proceso.  
*   Se actualizó la inserción remota de objetos para admitir implementaciones de .NET `IDispatch` \([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Evento [NewWindowRequested actualizado][ReferenceWin32Icorewebview2AddNewwindowrequested09488] para controlar las solicitudes de los menús contextuales \([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Se publicó el primer paquete de versión previa a WebView2 independiente en el que puedes acceder a las API de hospedaje visual.  El equipo de WebView actualizó [APISample][GithubMicrosoftedgeWebview2samplesMain] para incluir las nuevas API experimentales.  
    
    *   Se [agregó la interfaz ICoreWebView2ExperimentalCompositionController,][ReferenceWin32Icorewebview2experimentalcompositioncontroller09488] para conectarse a un árbol de composición y proporcionar entrada para WebView.  
    *   Se [agregó ICoreWebView2ExperimentalPointerInfo][ReferenceWin32Icorewebview2experimentalpointerinfo09488], que contiene toda la información de un `POINTER_INFO` archivo .  Este objeto se pasa a SendPointerInput para insertar una entrada de puntero en la vista web.  
    *   Se [agregó ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488], que indica a la aplicación cuándo debe cambiarse el cursor del mouse sobre webView.  Cuando el mouse está sobre un cuadro de texto en webView, el cursor cambia de la flecha al selector.  La propiedad de la aplicación indica a la aplicación cuál debe ser actualmente el cursor del `cursor` `CompositionController` mouse para WebView.  
    
## 0.9.430  

[Paquete NuGet][NuGetGallery0.9.430] \| Microsoft Edge versión 82.0.430.0.  

El SDK de WebView2 es la versión beta oficial de Win32 C++, que incorpora varias solicitudes de características de los comentarios.  El equipo de WebView intenta limitar el número de versiones con cambios importantes.  A medida que se aproxima la disponibilidad general, se incorporan varios cambios importantes en la versión beta.  

*   > [!IMPORTANT]
    > Cambio **importante:** a medida que se acerca la versión final, el equipo de WebView cambió el nombre del prefijo *IWebView2WebView* a *ICoreWebView2* para asegurarse de que la API de WebView2 se alinea con la convención de nomenclatura de la API de Windows.  Además, para aprovechar el SDK de WebView2 de los marcos de interfaz de usuario, el equipo de WebView se separó en `ICoreWebView2` [ICoreWebView2][ReferenceWin32Icorewebview209430] e [ICoreWebView2Host.][ReferenceWin32Icorewebview2host09430]  `ICoreWebView2Host` admite cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.  ICoreWebView2 admite todas las demás funciones de WebView2.  Para obtener más información sobre cómo incorporar los cambios, ve a la solicitud de incorporación de [cambios][GithubMicrosoftedgeWebview2samplesPr17] de WebView2 en el proyecto [APISample][GithubMicrosoftedgeWebview2samplesMain] de WebView2.  
    
*   > [!IMPORTANT]
    > **Cambio importante:** Dividir [DocumentStateChanged][ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190] en tres componentes:  [SourceChanged][ReferenceWin32Icorewebview2AddSourcechanged09430], [ContentLoading][ReferenceWin32Icorewebview2AddContentloading09430]e [HistoryChanged][ReferenceWin32Icorewebview2AddHistorychanged09430].  Ahora, cuando la dirección URL de origen cambia, `SourceChanged` se ejecuta el evento.  Cuando se cambia el estado del historial, `HistoryChanged` se ejecuta el evento.  El `ContentLoading` evento se ejecuta antes del script inicial cuando se carga un nuevo documento.  
    
*   Se ha agregado compatibilidad con la arquitectura arm64.  
*   Se ha agregado compatibilidad con panel de entrada suave \(SIP\) para dispositivos de pantalla táctil.  
*   Se ha agregado compatibilidad con Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 y Windows Server 2016.  
*   Se [agregó NotifyParentWindowPositionChanged para][ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430] que la barra de estado siga la ventana en modo de ventana.  Además, implementa el cambio en modo sin ventanas para que funcionen las características de accesibilidad.  
*   Se [agregó la configuración AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430] para controlar globalmente si algún objeto remoto puede tener acceso a una página web.  De forma predeterminada, está activado, por lo que los objetos remotos agregados por `AreRemoteObjectsAllowed` [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] son accesibles desde la página web.  Cuando `AreRemoteObjectsAllowed` está desactivada, los objetos no son accesibles desde la página web.  Los cambios se aplican en el siguiente evento de navegación.  
*   Se [agregó la configuración IsZoomControlEnabled][ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430] para evitar que los usuarios repercutan en el zoom de WebView con `ctrl` + `+` `ctrl` + `-` \(o `ctrl` + rueda del mouse\).  Es posible que aún se establezca el [zoom put_ZoomFactor][ReferenceWin32Icorewebview2hostPutZoomfactor09430] cuando la configuración esté desactivada.  
*   Se cambió ZoomFactor para que solo se aplique a la vista web actual.  Los cambios de zoom en la vista web actual no afectan a otras vistas web a las que navegaste con el mismo sitio de origen.  Para obtener más información, vaya [a get_ZoomFactor][ReferenceWin32Icorewebview2hostGetZoomfactor09430].  
*   Hid ZoomView UI for WebView \([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Se [agregó SetBoundsAndZoomFactor][ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430].  Ahora, puedes establecer el factor de zoom y los límites de una vista web al mismo tiempo.  
*   Se agregó [el evento WindowCloseRequested.][ReferenceWin32Icorewebview2AddWindowcloserequested09430]  Para obtener más información, vaya [a add_WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] \([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Se agregó compatibilidad con el tipo `beforeunload` de [][ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430] diálogo para eventos de diálogo de JavaScript y se CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD entrada de enumeración.  
*   Se [agregó GetHeaders][ReferenceWin32Icorewebview2httprequestheadersGetheaders09430] a HttpRequestHeaders, [GetHeader][ReferenceWin32Icorewebview2httpresponseheadersGetheader09430] a HttpResponseHeaders y get_HasCurrentHeader [propiedad][ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430] a HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Cambio importante:** comportamiento `DevToolsProtocolEventReceived` modificado.  Ahora, puede crear un [DevToolsProtocolEventReceiver][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430] para un evento concreto del Protocolo DevTools y suscribirse o cancelar la suscripción a dicho evento mediante [add_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430] / [remove_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430].  
    
*   > [!IMPORTANT]
    > **Cambio importante:** se `WebMessageReceivedEventArgs` [get_WebMessageAsString][ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190] propiedad a [un método TryGetWebMessageAsString.][ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]  
    
*   > [!IMPORTANT]
    > **Cambio de separación:** se `AcceleratorKeyPressedEventArgs` [cambió][ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190] el método Handle a [get_Handled][ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430] propiedad.  
    
## 0.8.355  

[Paquete NuGet][NuGetGallery0.8.355] \| Microsoft Edge versión 80.0.355.0.  

*   Ejemplo webView2API publicado, una guía completa del SDK de WebView2.  Para obtener más información, vaya a [ejemplo de API.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Se agregó compatibilidad con IME para todos los idiomas además del inglés \([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Se actualizó la superficie de LA API `WebResourceRequested` del evento en respuesta a los informes de errores.  La especificación simultánea de un filtro y un evento al crearse ahora está en desuso.  Para crear un evento solicitado de recurso web, use [add_WebResourceRequested][ReferenceWin32Iwebview2webview5AddWebresourcerequested08190] para agregar el evento y [AddWebResourceRequestedFilter para][ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190] agregar un filtro.  [RemoveWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190] quita el filtro \([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Cambio de separación:** se modificó el comportamiento de pantalla completa.  En [desuso IsFullScreenAllowed][ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190].  Ahora, de forma predeterminada, si un elemento de una vista web \(como un vídeo\) se establece en pantalla completa, rellena los límites de WebView.  Usa el [evento ContainsFullScreenElementChanged][ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190] [y get_ContainsFullScreenElement][ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190] para especificar cómo debe cambiar el tamaño de la aplicación webView si un elemento desea entrar en modo de pantalla completa.  
    
## 0.8.314  

[Paquete NuGet][NuGetGallery0.8.314] \| Microsoft Edge versión 80.0.314.0.  

*   Se ha agregado compatibilidad con Windows 7, Windows 8 y Windows 8.1.  
*   Se agregó Visual Studio y Visual Studio de depuración de código para WebView2.  Ahora, depure el script en webView2 directamente desde su IDE.  Para obtener más información, vaya [a Cómo depurar al desarrollar con controles WebView2][HowtoDebug].  
*   Se ha agregado para que el script en ejecución en WebView2 acceda a un objeto IDispatch desde el componente Win32 de la aplicación y obtenga acceso a las propiedades del objeto `Native Object Injection` IDispatch.  Para obtener más información, vaya [a AddRemoteObject][ReferenceWin32Iwebview2webview4Addremoteobject08190] \([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Evento `AcceleratorKeyPressed` agregado.  Para obtener más información, vaya [a add_AcceleratorKeyPressed][ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Desactivado el `Context Menus` archivo .  Para obtener más información, vaya [a put_AreDefaultContextMenusEnabled][ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190] \([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Actualizado `DPI Awareness` .  Ahora, el reconocimiento de PPP de WebView es el mismo que el reconocimiento de PPP de la aplicación host.  
    
    > [!NOTE]
    > Si se inicia otra aplicación híbrida con un reconocimiento de PPP diferente al webview original, la nueva vista web no se inicia si es el mismo `user data folder` \([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Se `Notification Change Behavior` actualizó para que WebView2 rechace automáticamente las solicitudes de permisos de notificación que solicita el contenido web hospedado en WebView.  
    
## 0.8.270  

[Paquete NuGet][NuGetGallery0.8.270] \| Microsoft Edge versión 78.0.270.0.  

*   Evento agregado `DocumentTitleChanged` para indicar el cambio de título del documento \([\#27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   Se `GetWebView2BrowserVersionInfo` agregó la API \([\#18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Evento `NewWindowRequested` agregado.  
*   Función `CreateWebView2EnvironmentWithDetails` actualizada para quitar `releaseChannelPreference` .  Para obtener más información acerca `CreateWebView2EnvironmentWithDetails` de la función, vaya a [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  La invalidación de variable de registro y entorno sigue siendo compatible.  La preferencia de canal predeterminada se usa a menos que se invalide.  
    Durante la búsqueda de canal, el equipo de WebView omite cualquier versión anterior del canal que no sea compatible con el SDK de WebView2.  
    El equipo de WebView selecciona el canal más estable para garantizar los comportamientos más coherentes para el usuario final.  Cuando pruebes con las compilaciones más recientes de Canary, debes crear un script para establecer la variable de entorno antes `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` `1` de iniciar la aplicación.  
*   Se `CreateWebView2EnvironmentWithDetails` actualizó la función con lógica para seleccionar `userDataFolder` cuando no se especifica.  Para obtener más información acerca `CreateWebView2EnvironmentWithDetails` de la función, vaya a [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Si usó anteriormente la ubicación predeterminada, al cambiar al nuevo SDK, el valor predeterminado es restablecer \(establecido en una nueva ubicación en el directorio de código host\) y su estado también se `userDataFolder` `userDataFolder` restablece.  Si el proceso de host no tiene permiso para escribir en el directorio especificado, puede producirse `CreateWebView2EnvironmentWithDetails` un error en la función.  Puede copiar los datos del directorio antiguo `user data folder` al nuevo.  
    
## 0.8.230  

[Paquete NuGet][NuGetGallery0.8.230] \| Microsoft Edge versión 77.0.230.0.  

*   Se agregó una API para detener todas las búsquedas de recursos pendientes y de navegación `Stop` \([\#28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Se `.tlb` agregó un archivo al paquete NuGet \([\#22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Se agregaron proyectos de .NET a la lista de instaladores en el paquete NuGet \([\#32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  
    
## 0.8.190  

[Paquete NuGet][NuGetGallery0.8.190] \| Microsoft Edge versión 77.0.190.0.  

*   Se `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` agregó para controlar si los usuarios pueden abrir DevTools \([\#16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Se agrega al control si se muestra `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` la barra de estado \([\#19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Se ha `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` agregado para volver atrás y avanzar a través del historial de navegación.  
*   Se agregaron tipos de encabezado HTTP \( \) para ver y modificar `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` encabezados HTTP en WebView.  
*   Se agregó compatibilidad con WebView de 32 bits en máquinas de 64 bits \([\#13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Se agregó WebView IDL al SDK \([\#14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Se agregó lib para admitir `IID\_\*` objetos de identificador de interfaz \([\#12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Se agregó la ruta de acceso, la vinculación y la copia automática de archivos DLL en el archivo NuGet `TARGET` del SDK.  
*   Activada la solicitud en `window.open()` el script.  
    
## 0.8.149  

[Paquete NuGet][NuGetGallery0.8.149] \| Microsoft Edge versión 76.0.149.0.  

Versión preliminar del desarrollador inicial.  

<!-- Links -->  

[VersioningDoc]: ./concepts/versioning.md#matching-webview2-runtime-versions
[ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones mediante webView2 | Microsoft Docs"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Modo de distribución permanente: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionFixedVersionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Modo de distribución de versiones fijas: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Comprender el tiempo de ejecución y el instalador de WebView2: distribución de aplicaciones con WebView2 | Microsoft Docs"  
[Webview2ConceptsEnterpriseGroupPoliciesForWebview2]: ./concepts/enterprise.md#group-policies-for-webview2 "Directivas de grupo para WebView2: administración de aplicaciones webView2 | Microsoft Docs"  
[ConceptsVersioning]: ./concepts/versioning.md "Descripción de las versiones del explorador y las versiones de WebView2 | Microsoft Docs"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "API experimentales: descripción de las versiones del explorador y las versiones de WebView2 | Microsoft Docs"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Introducción a WebView2 en aplicaciones de Windows Forms | Microsoft Docs"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Introducción a WebView2 en WPF | Microsoft Docs"  
[HowtoDebug]: ./howto/debug.md "Cómo depurar al desarrollar con controles WebView2 | Microsoft Docs"  

[ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Identificador: interfaz IWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs"  
[ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interfaz IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft Docs"  
[ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled: interfaz IWebView2Settings2 | Microsoft Docs"  
[ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated: interfaz IWebView2Settings | Microsoft Docs"  
[ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "get_WebMessageAsString: interfaz IWebView2WebMessageReceivedEventArgs | Microsoft Docs"  
[ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "add_AcceleratorKeyPressed: interfaz IWebView2WebView4 | Microsoft Docs"  
[ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "add_DocumentStateChanged: interfaz IWebView2WebView | Microsoft Docs"  
[ReferenceWin32Iwebview2webview4Addremoteobject08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject: interfaz IWebView2WebView4 | Microsoft Docs"  
[ReferenceWin32Iwebview2webview5AddWebresourcerequested08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "add_WebResourceRequested: interfaz IWebView2WebView5 | Microsoft Docs"  
[ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter: interfaz IWebView2WebView5 | Microsoft Docs"  
[ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "get_ContainsFullScreenElement: interfaz IWebView2WebView5 | Microsoft Docs"  
[ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter: interfaz IWebView2WebView5 | Microsoft Docs"  
[ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]:  /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails- Globals | Microsoft Docs"  

[ReferenceWin32Icorewebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "get_Handled: interfaz ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddContentloading09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "add_ContentLoading: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddHistorychanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "add_HistoryChanged: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2Addremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddSourcechanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "add_SourceChanged: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddWindowcloserequested09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "add_WindowCloseRequested: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived: interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived: interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft Docs"  
[ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "get_BrowserVersionInfo: interfaz ICoreWebView2Environment | Microsoft Docs"  
[ReferenceWin32Icorewebview2host09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo- Globals | Microsoft Docs"  
[ReferenceWin32Icorewebview2hostGetZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "get_ZoomFactor: interfaz ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged: interfaz ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Icorewebview2hostPutZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "put_ZoomFactor: interfaz ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor: interfaz ICoreWebView2Host | Microsoft Docs"  
[ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "get_HasCurrentHeader: interfaz ICoreWebView2HttpHeadersCollectionIterator | Microsoft Docs"  
[ReferenceWin32Icorewebview2httprequestheadersGetheaders09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders: interfaz ICoreWebView2HttpRequestHeaders | Microsoft Docs"  
[ReferenceWin32Icorewebview2httpresponseheadersGetheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader: interfaz ICoreWebView2HttpResponseHeaders | Microsoft Docs"  
[ReferenceWin32Icorewebview2Removeremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed: interfaz ICoreWebView2Settings | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "get_IsZoomControlEnabled: interfaz ICoreWebView2Settings | Microsoft Docs"  
[ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString: interfaz ICoreWebView2WebMessageReceivedEventArgs | Microsoft Docs"  

[ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "add_FrameNavigationCompleted: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2Addhostobjecttoscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2AddNewwindowrequested09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "add_NewWindowRequested: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring " | Microsoft Docs"  
[ReferenceWin32Icorewebview2environmentoptions09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interfaz ICoreWebView2EnvironmentOptions | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCompositionController | Microsoft Docs"
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCompositionController | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalpointerinfo09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalPointerInfo | Microsoft Docs"  
[ReferenceWin32Icorewebview2Removehostobjectfromscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed: interfaz ICoreWebView2Settings | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Microsoft Docs"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails- Globals | Microsoft Docs"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions- Globals | Microsoft Docs"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString- Globals | Microsoft Docs"  

[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseAddRasterizationscalechanged]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#add_rasterizationscalechanged "add_RasterizationScaleChanged: interfaz ICoreWebView2ExperimentalController | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetBoundsMode]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_boundsmode "get_BoundsMode: interfaz ICoreWebView2ExperimentalController | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetRasterizationscale]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_rasterizationscale "get_RasterizationScale: interfaz ICoreWebView2ExperimentalController | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcontrollerViewWebview210721PrereleaseGetShouldDetectMonitorScaleChanges]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcontroller?view=webview2-1.0.721-prerelease&preserve-view=true#get_shoulddetectmonitorscalechanges "get_ShouldDetectMonitorScaleChanges: interfaz ICoreWebView2ExperimentalController | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Espacio de nombres Microsoft.Web.WebView2.Core | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft.Web.WebView2.Wpf | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft.Web.WebView2.WinForms | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2CoreWebview2runtimenotfoundexception]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2.WebView2RuntimeNotFound (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Clase CoreWebView2 (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Clase CoreWebView2Environment (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "Método CoreWebView2Environment.CompareBrowserVersions(String, String) (Microsoft.Web.WebView2.Core) | Microsoft Docs"
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "Método CoreWebView2Environment.GetAvailableBrowserVersionString(String) (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Evento CoreWebView2.NewWindowRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Evento CoreWebView2.PermissionRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Evento CoreWebView2.ScriptDialogOpening (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Evento CoreWebView2.WebResourceRequested (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Clase CoreWebView2HttpRequestHeaders (Microsoft.Web.WebView2.Core) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Clase CoreWebView2HttpResponseHeaders (Microsoft.Web.WebView2.Core) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Clase CoreWebView2CreationProperties (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Clase Webview2.Source (Microsoft.Web.WebView2.Winforms) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "Método WebView2.BuildWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "Método WebView2.DestroyWindowCore(HandleRef) (Microsoft.Web.WebView2.Wpf) | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2WpfWebview2Acceleratorkeypressed]: /dotnet/api/microsoft.web.webview2.wpf.webview2.acceleratorkeypressed "microsoft.web.webview2.wpf.webview2.acceleratorkeypressed | Microsoft Docs"  

[DotnetApiMicrosoftWebWebview2Corewebview2initializationcompletedeventargs]: /dotnet/api/microsoft.web.webview2.core.corewebview2initializationcompletedeventargs "Clase CoreWebView2InitializationCompletedEventArgs | Microsoft Docs"  

[ReferenceWin32Icorewebview2Addhostobjecttoscript09538]: /microsoft-edge/webview2/reference/win32/icorewebview2#addhostobjecttoscript?view=webview2-0.9.538&preserve-view=true "AddHostObjectToScript: interfaz ICoreWebView2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived: interfaz ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "get_IsSingleSignOnUsingOSPrimaryAccountEnabled- interfaz ICoreWebView2ExperimentalEnvironmentOptions | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "get_WindowFeatures: interfaz ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalwindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalWindowFeatures | Microsoft Docs"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "get_IsUserInitiated interfaz ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs"  
[ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "get_AreHostObjectsAllowed: interfaz ICoreWebView2Settings | Microsoft Docs"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions- Globals | Microsoft Docs"  

[ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "get_AllowSingleSignOnUsingOSPrimaryAccount: interfaz ICoreWebView2EnvironmentOptions | Microsoft Docs"  
[ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "put_AdditionalBrowserArguments: interfaz ICoreWebView2EnvironmentOptions | Microsoft Docs"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "get_WindowFeatures: interfaz ICoreWebView2NewWindowRequestedEventArgs | Microsoft Docs"  
[ReferenceWin32Icorewebview2windowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interfaz ICoreWebView2WindowFeatures | Microsoft Docs"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions- Globals | Microsoft Edge"  
[ReferenceWin32Icorewebview2experimentalenvironment09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment?view=webview2-0.9.628-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalEnvironment | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent: interfaz ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft Docs"  

[ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "add_DOMContentLoaded: interfaz ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "add_WebResourceResponseReceived: interfaz ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalGetCookiemanager10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "get_CookieManager: interfaz ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalGetEnvironment10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "get_Environment: interfaz ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest: interfaz ICoreWebView2Experimental | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2#get_systemcursorid?view=webview2-1.0.674-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent: interfaz ICoreWebView2ExperimentalWebResourceResponseView | Microsoft Docs"  

[ReferenceWin32Icorewebview2experimentalcompositioncontroller3]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller3?view=webview2-1.0.721-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCompositionController3 | Microsoft Docs"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge: directivas | Microsoft Docs"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2: directivas | Microsoft Docs"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Protección de aplicaciones de Microsoft Defender (Windows 10): protección de seguridad de Windows | Microsoft Docs"

[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Clase CancelEventArgs (System.ComponentModel) | Microsoft Docs"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Clase EventArgs (System) | Microsoft Docs"  
[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Ensamblados con nombre fuerte | Microsoft Docs"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Repositorio de comentarios del problema 1 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repositorio de comentarios del problema 13 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repositorio de comentarios del problema 14 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repositorio de comentarios del problema 16 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Repositorio de comentarios del problema 17 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repositorio de comentarios del problema 18 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repositorio de comentarios del problema 19 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repositorio de comentarios del problema 27 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Repositorio de comentarios del problema 30 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Repositorio de comentarios del problema 36 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Repositorio de comentarios del problema 57 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Repositorio de comentarios del problema 70 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Repositorio de comentarios del problema 74 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Repositorio de comentarios del problema 95 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Repositorio de comentarios del problema 108 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Repositorio de comentarios del problema 113 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Repositorio de comentarios del problema 119 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue131]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Repositorio de comentarios del problema 131 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repositorio de comentarios del problema 148 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue168]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/168 "Repositorio de comentarios del problema 168 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Repositorio de comentarios del problema 177 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repositorio de comentarios del problema 179 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Repositorio de comentarios del problema 181 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Repositorio de comentarios del problema 183 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Repositorio de comentarios del problema 185 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue204]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 204"
[GithubMicrosoftedgeWebviewfeedbackIssue219]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Repositorio de comentarios del problema 219 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Repositorio de comentarios del problema 228 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Repositorio de comentarios del problema 235 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue250]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Repositorio de comentarios del problema 250 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue288]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/288 "Repositorio de comentarios del problema 288 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Repositorio de comentarios del problema 293 de MicrosoftEdge/WebViewFeedback"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Repositorio de comentarios del problema 318 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue335]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/335 "Repositorio de comentarios del problema 335 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue371]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/371 "Repositorio de comentarios del problema 371 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Repositorio de comentarios del problema 382 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Repositorio de comentarios del problema 431 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Repositorio de comentarios del problema 432 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue461]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/461 "Repositorio de comentarios del problema 461 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue525]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/525 "Repositorio de comentarios del problema 525 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue549]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/549 "Repositorio de comentarios del problema 549 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue560]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/560 "Repositorio de comentarios del problema 560 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue611]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/611 "Repositorio de comentarios del problema 611 de MicrosoftEdge/WebViewFeedback"  

[GithubMicrosoftedgeWebview2AnnouncementIssue2]:  https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Repositorio de anuncios para MicrosoftEdge/WebViewAnnouncement Issue 2"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Mover el proyecto para usar la versión más reciente del SDK de WebView2 0.9.430: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[MicrosoftDevblogDotnetAnnouncingGeneralAvailabilityForMicrosoftEdgeWebview2ForNetFixedDistributionMethod]: https://devblogs.microsoft.com/dotnet/announcing-general-availability-for-microsoft-edge-webview2-for-net-and-fixed-distribution-method "Anuncio de disponibilidad general para Microsoft Edge WebView2 para .NET y método de distribución fija | blog de .NET"  

[MicrosoftDeveloperMicrosoftEdgeWebView2]: https://developer.microsoft.com/microsoft-edge/webview2/ "Microsoft Edge WebView2 | Desarrollador de Microsoft Edge"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "Galería nuGet | Microsoft.Web.WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galería nuGet | Microsoft.Web.WebView2 v0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galería nuGet | Microsoft.Web.WebView2 v0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galería nuGet | Microsoft.Web.WebView2 v0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galería nuGet | Microsoft.Web.WebView2 v0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galería nuGet | Microsoft.Web.WebView2 v0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galería nuGet | Microsoft.Web.WebView2 v0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galería nuGet | Microsoft.Web.WebView2 v0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galería nuGet | Microsoft.Web.WebView2 v0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v0.9.515"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Galería nuGet | Microsoft.Web.WebView2 v0.9.538"  
[NuGetGallery0.9.579]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Galería nuGet | Microsoft.Web.WebView2 v0.9.579"
[NuGetGallery0.9.622.11]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Galería nuGet | Microsoft.Web.WebView2 v0.9.622.11"
[NuGetGallery1.0.622.22]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Galería nuGet | Microsoft.Web.WebView2 v1.0.622.22"
[NuGetGallery1.0.664.34]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.34 "Galería nuGet | Microsoft.Web.WebView2 v1.0.664.34"
[NuGetGallery1.0.664.37]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.664.37 "Galería nuGet | Microsoft.Web.WebView2 v1.0.664.37"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v0.9.628"  
[NuGetGallery1.0.674-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v1.0.674"  
[NuGetGallery1.0.721-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.721-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v1.0.721"  
[WindowsBlogsMsedgedevEdgeWebview2GeneralAvailability]: https://blogs.windows.com/msedgedev/edge-webview2-general-availability "Anuncio de la disponibilidad general de Microsoft Edge WebView2 | Microsoft Edge Blog"  

[WebResourceResponseReceivedAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#add_webresourceresponsereceived&preserve-view=true "add_WebResourceResponseReceived: interfaz ICoreWebView2 | Microsoft Docs"
[NavigateWithWebResourceRequestAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2environment2?view=webview2-1.0.721-prerelease#createwebresourcerequest&preserve-view=true "CreateWebResourceRequest: interfaz ICoreWebView2Environment | Microsoft Docs"
[CookiemanagementAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2cookiemanager?view=webview2-1.0.721-prerelease&preserve-view=true "ICoreWebView2CookieManager | Microsoft Docs"
[DOMContentLoadedAPI]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#add_domcontentloaded&preserve-view=true "add_DOMContentLoaded: interfaz ICoreWebView2_2 | Microsoft Docs"
[WebViewEnvironmentproperty]: /microsoft-edge/webview2/reference/win32/icorewebview2_2?view=webview2-1.0.721-prerelease#get_environment&preserve-view=true "ICoreWebView2CookieManager | Microsoft Docs"

[GithubMicrosoftedgeWebviewfeedbackIssue585]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/585 "Repositorio de comentarios del problema 585 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue275]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/275 "Repositorio de comentarios del problema 275 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue816]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/816 "Repositorio de comentarios del problema 816 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue210]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/210 "Repositorio de comentarios del problema 210 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue442]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/442 "Repositorio de comentarios del problema 442 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue878]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/878 "Repositorio de comentarios del problema 878 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue875]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/875 "Repositorio de comentarios del problema 875 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue37]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/37 "Repositorio de comentarios del problema 37 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue58]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/58 "Repositorio de comentarios del problema 58 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue122]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/122 "Repositorio de comentarios del problema 122 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue161]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/161 "Repositorio de comentarios del problema 161 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue196]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/196 "Repositorio de comentarios del problema 196 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue205]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/205 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback Issue 205" 
[GithubMicrosoftedgeWebviewfeedbackIssue212]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/212 "Repositorio de comentarios del problema 212 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue399]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/399 "Repositorio de comentarios del problema 399 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue400]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/400 "Repositorio de comentarios del problema 400 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue409]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/409 "Repositorio de comentarios para el problema 409 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue605]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/605 "Repositorio de comentarios del problema 605 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue691]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/691 "Repositorio de comentarios del problema 691 de MicrosoftEdge/WebViewFeedback" 
[GithubMicrosoftedgeWebviewfeedbackIssue414]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/414 "Repositorio de comentarios del problema 414 de MicrosoftEdge/WebViewFeedback" 
[NuGetGallery1.0.705.50]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.705.50 "Galería nuGet | Microsoft.Web.WebView2 v1.0.705.50"
[NuGetGallery1.0.790-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.790-prerelease "Galería nuGet | Versión preliminar de Microsoft.Web.WebView2 v1.0.790"  
[ReferenceWin32Icorewebview210790PreReleaseTrySuspendResume]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#trysuspend "TrySuspend: interfaz ICoreWebview2_3 | Microsoft Docs"  
[ReferenceWin32Icorewebview2experimentalsettings10790PreReleaseGetUserAgent]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalsettings?view=webview2-1.0.790-prerelease&preserve-view=true#get_useragent "get_UserAgent: interfaz ICoreWebView2ExperimentalSettings | Microsoft Docs"  
[ReferenceWin32Icorewebview210790PreReleaseSetVirtualHostNameToFolderMapping]: /microsoft-edge/webview2/reference/win32/icorewebview2_3?view=webview2-1.0.790-prerelease&preserve-view=true#setvirtualhostnametofoldermapping "SetVirtualHostNameToFolderMapping: interfaz ICoreWebView2_3 | Microsoft Docs"   
[ReferenceWin32Icorewebview2controllerViewWebview210790PreReleaseDefaultBackgroundColor]: /microsoft-edge/webview2/reference/win32/icorewebview2controller2?view=webview2-1.0.790-prerelease&preserve-view=true#get_defaultbackgroundcolor "get_DefaultBackgroundColor: interfaz ICoreWebView2Controller2 | Microsoft Docs"  
[ReferenceWin32Icorewebview2controllerViewWebview210790CompositionController]:  /microsoft-edge/webview2/reference/win32/icorewebview2compositioncontroller?view=webview2-1.0.790-prerelease&preserve-view=true "interfaz ICoreWebView2CompositionController | Microsoft Docs"  
[ReferenceWin32Icorewebview2webresourceresponseviewgetcontentcompletedhandlerInvoke10790]: /microsoft-edge/webview2/reference/win32/icorewebview2webresourceresponseviewgetcontentcompletedhandler?view=webview2-1.0.790-prerelease&preserve-view=true#invoke "Invoke: interfaz ICoreWebView2WebResourceResponseViewGetContentCompletedHandler | Microsoft Docs"  
