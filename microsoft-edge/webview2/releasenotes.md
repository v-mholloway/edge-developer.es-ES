---
description: Notas de la versión para el SDK de Microsoft Edge WebView2
title: Notas de la versión de Microsoft Edge WebView2 para Win32, WPF y WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 3e567373b0faff745e60cd53faddc9af4e370a58
ms.sourcegitcommit: efb12ebe2fe9ef02f04a9ff6e4540c2384c964e2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/19/2020
ms.locfileid: "11120504"
---
# Notas de la versión para el SDK de WebView2  

El equipo de WebView2 está ofreciendo actualizaciones para el [SDK de WebView2][NuGetGallery] en una cadencia de seis semanas.  Revise el siguiente contenido para obtener información actualizada sobre anuncios de productos, adiciones y modificaciones a la superficie de la API y cambios importantes.  

> [!NOTE]
> Vuelve a compilar la aplicación después de actualizar el paquete de NuGet.  

> [!IMPORTANT]
> Aunque WebView2 es una versión preliminar, las API de .NET están en `prerelease package` .  

## 1.0.674-versión preliminar  

Fecha de lanzamiento: 19 de octubre de 2020  

[Paquete NuGet][NuGetGallery1.0.674-prerelease] \ | versión mínima de Microsoft Edge 88.0.674.0.

#### General

*   Se agregó el método [NavigateWithWebResourceRequest][ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674] que permite proporcionar datos de publicación o encabezados de solicitud adicionales durante la navegación.
*   Se ha agregado un evento [DOMContentLoaded][ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674] que se ejecuta cuando se carga y se analiza el documento HTML inicial.
*   Se ha agregado la propiedad [Environment][ReferenceWin32Icorewebview2experimentalGetEnvironment10674] en WebView2. Esta propiedad expone el entorno de WebView2 donde se creó una instancia de WebView2.
*   Se han agregado API de [Administración de cookies][ReferenceWin32Icorewebview2experimentalGetCookiemanager10674] que permiten a los desarrolladores autenticar la sesión de WebView2 o recuperar cookies de WebView para autenticar otras herramientas. Estamos pensando en mejorar las mejoras específicas de idioma y marco. Para obtener más información, vaya a [revisión de API: administración de cookies][GithubMicrosoftedgeWebview2AnnouncementIssue2].
*   Se ha actualizado el evento [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674] y se han agregado [WebResourceResponseView][ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674] inmutables y [WebResourceResponseReceivedEventArgs::P opulateresponsecontent][ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628] para convertirse en [WebResourceResponseView:: GetContent][ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674].
*   Ha desactivado la [protección de aplicaciones de Microsoft defender (WDAG)][WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10] en WebView2.
*   Se ha agregado [SystemCursorId][ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674] para el hospedaje visual.
*   Se ha agregado un error corregido para el método de entrada en hospedaje visual.
*   Los programadores ya no tienen que incluir version. lib al usar la biblioteca estática WebView2.


#### .NET  

*   Clase [CoreWebView2][DotnetApiMicrosoftWebWebview2CoreCorewebview2] actualizada para exponer la variable CoreWebView2Environment.  
*   Implementaciones modificadas de clases EventArgs personalizadas en `Microsoft.Web.WebView2.Core` espacios de nombres para que sean subclases de [System. EventArgs][DotnetApiSystemEventargs] o [System. ComponentModel. CancelEventArgs][DotnetApiSystemComponentmodelCancelEventargs]. \ ([\ #250][GithubMicrosoftedgeWebviewfeedbackIssue250]\)  
*   Se ha agregado compatibilidad con [CoreWebView2CreationProperties][DotnetApiMicrosoftWebWebview2Winforms] en WinForms. \ ([\ #204][GithubMicrosoftedgeWebviewfeedbackIssue204]\)
*   API de .NET [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested] agregadas.  \ ([\ #219][GithubMicrosoftedgeWebviewfeedbackIssue219]\).  
*   Se actualiza la propiedad [source][DotnetApiMicrosoftWebWebview2WinformsWebview2Source] del diseñador de WinForms como default o reset a NULL. \ ([\ #177][GithubMicrosoftedgeWebviewfeedbackIssue177]\).  
*   Los límites de WebView2 actualizados en WebView2.Init () admiten modos de PPP menores que 100%.  \ ([\ #432][GithubMicrosoftedgeWebviewfeedbackIssue432]\).  
*   [BuildWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore] y [DestroyWindowCore][DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore] actualizados son más sólidos.  \ ([\ #382][GithubMicrosoftedgeWebviewfeedbackIssue382]\).  
*   Base del cargador .NET actualizado para cargarlo en el bit de proceso en lugar de en la arquitectura del sistema operativo. \ ([\ #431][GithubMicrosoftedgeWebviewfeedbackIssue431]\).  
*   Cambió el nombre de EdgeNotFoundExpection a [WebView2RuntimeNotFoundException][WebView2RuntimeNotFoundException].
 
## 1.0.622.22  

Fecha de lanzamiento: 19 de octubre de 2020  

[Paquete NuGet][NuGetGallery1.0.622.22] \ | WebView2 mínimo de versión de tiempo de ejecución 86.0.622.22.  

#### General  

> [!IMPORTANT]
> **Anuncio**: Win32 C/C++ WebView2 está ahora disponible generalmente (GA). A partir de esta versión, los SDK de la versión serán compatibles con el reenvío. Para obtener más información, consulta la [entrada de blog del anuncio GA](https://aka.ms/wv2gablogpost) .

* El [tiempo de ejecución de WebView2 perenne y el instalador][Webview2ConceptsDistributionUnderstandRuntimeInstaller] es GA. El arranque, el vínculo enlace descendente para el programa previo y el instalador independiente para el tiempo de ejecución de hoja de tiempo están disponibles [aquí](https://developer.microsoft.com/microsoft-edge/webview2/). El código de ejemplo para el flujo de trabajo de instalación también está disponible en el [repositorio de WebView2Samples][GithubMicrosoftedgeWebview2samplesMain]. 
* El [modo de versión corregido][Webview2ConceptsDistributionFixedVersionMode] está disponible para Developer Preview.

## 0.9.628-versión preliminar  

Fecha de lanzamiento: 10 de septiembre de 2020  

[Paquete NuGet][NuGetGallery0.9.628-prerelease] \ | versión mínima de Microsoft Edge 87.0.628.0.  

> [!IMPORTANT]
> **Anuncio**: esta versión preliminar continúa la publicación en función de la rama Microsoft Edge 87.  En el futuro, la versión del SDK de la versión preliminar coincide con la compilación Canarias de Microsoft Edge y la versión normal se sincroniza con Microsoft Edge estable.  

#### General  

*   > [!IMPORTANT]
    > **Anuncio**: las API de hospedaje visual ya están en vista previa.  WebView2 usa hospedaje visual para ejecutarse junto con los elementos visuales de WinComp/DComp, en lugar de HWNDs.  Las interfaces están en experimental.  Para obtener más información, vaya a [ICoreWebView2ExperimentalEnvironment][ReferenceWin32Icorewebview2experimentalenvironment09628].  

#### .NET  

*   Los binarios de .NET ahora tienen [un nombre seguro][DotnetStandardAssemblyStrongNamed].  \ ([\ #181][GithubMicrosoftedgeWebviewfeedbackIssue181]\).  
*   Destino de NuGet actualizado que se incluirá `WebViewLoader2.dll` .  \ ([\ #228][GithubMicrosoftedgeWebviewfeedbackIssue228]\) y \ ([\ #183][GithubMicrosoftedgeWebviewfeedbackIssue183]\).  
*   Se ha actualizado `WebResourceRequested` para exponer las API de [HttpRequestHeaders][DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders] y [HttpResponseHeaders][DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders] en .net.  \ ([\ #131][GithubMicrosoftedgeWebviewfeedbackIssue131]\).  

## 0.9.622.11  

Fecha de lanzamiento: 10 de septiembre de 2020  

[Paquete NuGet][NuGetGallery0.9.622.11] \ | WebView2 mínimo de versión de tiempo de ejecución 86.0.622.11.  

#### General  

*   > [!IMPORTANT]
    > **Anuncio**: este SDK es la versión candidata para WebView2 Win32 C/C++ GA.  La versión GA debe usar la misma interfaz y funcionalidad de API.  

*   [Directivas de explorador][DeployedgeMicrosoftEdgePolicies]desconectadas.  
*   Se ha agregado la propiedad [AllowSingleSignOnUsingOSPrimaryAccount][ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622] en las opciones del entorno WebView2 para habilitar el acceso condicional para la vista en WebView.  
*   Se ha actualizado `ICoreWebView2NewWindowRequestedEventArgs` para incluir la propiedad [WindowFeatures][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622] y la [ICoreWebView2WindowFeatures][ReferenceWin32Icorewebview2windowfeatures09622]asociada.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   Actualizado `System.Windows.Rect`  para usar en `System.Drawing.Rectangle` lugar de `System.Windows.Rect` \ ([\ #235][GithubMicrosoftedgeWebviewfeedbackIssue235]\).  
*   Evento NewWindowRequested actualizado para controlar la `window.open()` solicitud sin parámetros.  \ ([\ #293][GithubMicrosoftedgeWebviewfeedbackIssue293]\).  
*   [AdditionalBrowserArguments][ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622] Set using `ICoreWebView2EnvironmentOptions` no se invalida con variables de entorno y valores de registro.  Para obtener más información, vaya a [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622].  

## 0.9.579  

Fecha de publicación: 20 de julio de 2020  

[Paquete NuGet][NuGetGallery0.9.579] \ | versión mínima de Microsoft Edge 86.0.579.0.  

#### General  

*   > [!IMPORTANT]
    > **Anuncio**: el tiempo de ejecución de WebView2 de perennes y el instalador se publica para obtener una vista previa.  Para obtener más información, vaya a [Distribution of WebView2] [Webview2ConceptsDistributionUnderstandRuntimeInstallerPreview].  
*   > [!IMPORTANT]
    > **Anuncio**: las siguientes versiones del SDK de WebView2 ya no se admiten después de la siguiente versión del SDK.  
    > 
    > *   [0.8.190](#08190)  
    > *   [0.8.230](#08230)  
    > *   [0.8.270](#08270)  
    > *   [0.8.314](#08314)  
    > *   [0.8.355](#08355)  
    > 
    > Las versiones del SDK de WebView2 también se marcan como obsoletas en nuget.org.  WebView2 recomienda mantenerse al día con la última versión de WebView2.  

*   Se han agregado mejoras en el subproceso de trabajo de WebView.  \ ([\ #318][GithubMicrosoftedgeWebviewfeedbackIssue318]\).  
*   Bloqueador de elementos emergentes deshabilitado en WebView.  Para obtener más información, vaya a la propiedad [IsUserInitiated][ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538] en el `NewWindowRequested` evento.  
*   Se ha desencadenado el evento de inicio de navegación de WebView asegurado `about:blank` .  Ahora, `NavigationStarting` los eventos se desencadenan para toda la navegación, pero las cancelaciones para `about:blank` o iframe srcdoc no se admiten y no se tienen en cuenta.  
*   `edge:// URI`Esquema bloqueado en WebView.  
*   Se ha agregado la propiedad experimental [IsSingleSignOnUsingOSPrimaryAccountEnabled][ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538] en las opciones del entorno WebView2 para habilitar el acceso condicional para la vista en WebView.  
*   Se ha agregado un evento experimental de [WebResourceResponseReceived][ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538] que se desencadena después de que la vista previa reciba y haya procesado la respuesta de una solicitud de recursos  Los encabezados de autenticación, si los hay, se incluyen en el objeto Response.  

#### .NET  

*   Administración de foco de WPF mejorada.  \ ([\ #185][GithubMicrosoftedgeWebviewfeedbackIssue185]\).  
*   Propiedad agregada `ZoomFactor` en el controlador de Webview2 de WPF.  

## 0.9.538  

[Paquete NuGet][NuGetGallery0.9.538] \ | versión mínima de Microsoft Edge 85.0.538.0.  

#### General  

*   Compatibilidad de eliminación de WebView2 SDK versión [0.8.149](#08149).  WebView2 recomienda mantenerse al día con la última versión de WebView2.  
*   Directiva de grupo actualizada que se debe tener en cuenta cuando se modifica la ruta de acceso del perfil del explorador Microsoft Edge \ ([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]\).  

#### C/C++ Win32  

*   Se ha agregado [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538], que `window.open()` se activa cuando se ejecuta y se asocia con [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin32Icorewebview2experimentalwindowfeatures09538] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Cambio importante**:  [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] se ha dejado de usar y se ha reemplazado por [CreateCoreWebView2EnvironmentWithOptions] [[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538].  
*   > [!IMPORTANT]
    > **Cambio importante**: para asegurarse de que la API de WebView2 se alinee con las convenciones de nomenclatura de la API de Windows, el equipo de WebView actualizará los nombres de los siguientes.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488] es ahora [AreHostObjectsAllowed][ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538].  
*   [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09538] actualizado para garantizar que los marcadores de serializador de objeto de host original se establezcan en los objetos proxy y se serialicen como un objeto de host cuando se pasan como un parámetro en la devolución de llamada de JavaScript \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  

#### .NET (versión preliminar de 0.9.538)  

*   Se han publicado ejemplos de WinForms y WPF WebView2API, que son guías completas del SDK de WebView2.  Para obtener más información, vaya al [repositorio de ejemplos][GithubMicrosoftedgeWebview2samplesMain].  
*   Se ha agregado compatibilidad con las [API experimentales][ConceptsVersioningExperimentalApis]de hospedaje visual y características de la ventana.  
*   > [!IMPORTANT]
    > **Cambio importante**: las siguientes aplazaciones ahora implementan IDisposable:  [ScriptDialogOpening][DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]y [PermissionRequested][DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   Se han agregado [GetAvailableBrowserVersionString][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] y [CompareBrowserVersions][DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] como estáticas de [CoreWebView2Environment][DotnetApiMicrosoftWebWebview2CoreCorewebview2environment] .  

## 0.9.515-versión preliminar  

[Paquete NuGet][NuGetGallery0.9.515-prerelease] \ | versión mínima de Microsoft Edge 84.0.515.0.  

*   > [!IMPORTANT]
    > **Anuncio**: WebView2 ahora es compatible con Windows Forms y WPF en .NET Framework 4.6.2 o versiones posteriores, .net Core 3,0 o posterior en el **paquete preliminar**.  
*   Para obtener más información sobre la creación de aplicaciones WPF y la [referencia de WPF][DotnetApiMicrosoftWebWebview2Wpf] de WebView2 para las API específicas de WPF, vaya a la guía de [Introducción a WPF][GettingstartedWpf].  
*   Para obtener más información sobre la creación de aplicaciones de Windows Forms y la [referencia de Windows Forms][DotnetApiMicrosoftWebWebview2Winforms] WebView2 de las API específicas de Windows Forms, vaya a la guía de introducción a [formularios Windows Forms][GettingstartedWinforms].  
*   Para obtener más información sobre las API de CoreWebView2, vaya a [referencia de .net][DotnetApiMicrosoftWebWebview2Core].  
*   > [!CAUTION]
    > **Problemas conocidos**: el equipo de WebView tiene constancia de algunos problemas en la versión preliminar que se están resolviendo en versiones futuras.  
    > *   **Reconocimiento de PPP**: WEBVIEW2 para WPF actualmente no reconoce los ppp.  Al inicializar WebView2 en monitores con alta resolución de PPP, existe un problema conocido en el que WebView se inicializa en primer lugar como una fracción de la ventana hasta que se cambia el tamaño de la ventana.  
    > *   **WPF Designer**: WPF Designer no es compatible actualmente.  Agrega el control WebView2 en tu aplicación modificando directamente el XAML correspondiente en un editor de texto.  

## 0.9.488  

[Paquete NuGet][NuGetGallery0.9.488] \ | versión mínima de Microsoft Edge 84.0.488.0.  

*   > [!IMPORTANT]
    > **Anuncio**: a partir de la próxima versión 83 de Microsoft Edge, la vista previa de perenne ya no se destina al canal de explorador estable.  En su lugar, se destina a otro conjunto de binarios, [WebView2 tiempo de ejecución][ConceptsDistributionEvergreenMode]de personalización de marca, que se puede encadenar a través de un instalador el equipo de WebView se está desarrollando en este momento.  Para obtener más información, vaya a [la distribución de la aplicación][ConceptsDistribution].  
*   > [!IMPORTANT]
    > **Anuncio**: avanzar, el equipo de WebView publica dos paquetes: un paquete preliminar con las API experimentales \ (para probar \) y un paquete de versión estable con API estables \ (para la confianza \).  Para obtener más información sobre las diferencias, vaya a [Descripción de las versiones del explorador y WebView2][ConceptsVersioning].  
*   > [!IMPORTANT]
    > **Cambio importante**: para garantizar que la API de WebView2 se alinee con las convenciones de nomenclatura de la API de Windows, el equipo de WebView actualizará los nombres de las siguientes interfaces.  
    > *   `CORE_WEBVIEW2_*` el prefijo es ahora `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430] es ahora [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488].  
    > *   [get_BrowserVersionInfo][ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430] está ahora [get_BrowserVersionString][ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488].  
    > *   [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] es ahora [AddHostObjectToScript][ReferenceWin32Icorewebview2Addhostobjecttoscript09488].  
    > *   [RemoveRemoteObject][ReferenceWin32Icorewebview2Removeremoteobject09430] es ahora [RemoveHostObjectFromScript][ReferenceWin32Icorewebview2Removehostobjectfromscript09488].  
    > *   `chrome.webview.remoteObjects` ya está `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Cambio importante**: `AddRemoteObject` también se cambia el nombre a los métodos de proxy de JS.  
    > *   `getLocal` ya está `getLocalProperty` .  
    > *   `setLocal` ya está `setLocalProperty` .  
    > *   `getRemote` ya está `getHostProperty` .  
    > *   `setRemote` ya está `setHostProperty` .  
    > *   `applyRemote` ya está `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Cambio importante**:  [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488] se ha dejado de usar y se ha reemplazado por [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488].  
*   Se agregó el evento [FrameNavigationCompleted][ReferenceWin32Icorewebview2AddFramenavigationcompleted09488] .  Ahora, cuando un iframe completa la navegación, se desencadena un evento y devuelve el éxito de la navegación y el identificador de navegación.  
*   Se agregó la interfaz [ICoreWebView2EnvironmentOptions][ReferenceWin32Icorewebview2environmentoptions09488] , que se puede usar para determinar la versión del motor en tiempo de ejecución de WebView2 de destino de la aplicación.  
*   Se agregó la configuración [IsBuiltInErrorPageEnabled][ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488] .  Ahora, puede habilitar o deshabilitar la página de error integrada para error de navegación y error de proceso de representación.  
*   Se ha actualizado la inyección de objetos remotos para admitir implementaciones de .NET IDispatch \ ([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Evento [NewWindowRequested][ReferenceWin32Icorewebview2AddNewwindowrequested09488] actualizado para administrar solicitudes de menús contextuales \ ([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Publicó el primer paquete de versión preliminar de WebView2 independiente donde puedes tener acceso a las API de hospedaje de visual.  El equipo de WebView actualizó [APISample][GithubMicrosoftedgeWebview2samplesMain] para incluir las nuevas API experimentales.  
    *   Se agregó la interfaz de [ICoreWebView2ExperimentalCompositionController][ReferenceWin32Icorewebview2experimentalcompositioncontroller09488] , para conectar con un árbol de composición y proporcionar la entrada para la vista en WebView.  
    *   Se ha agregado [ICoreWebView2ExperimentalPointerInfo][ReferenceWin32Icorewebview2experimentalpointerinfo09488], que contiene toda la información de un `POINTER_INFO` .  Este objeto se pasa a SendPointerInput para inyectar la entrada de puntero en la vista de vista en WebView.  
    *   Se ha agregado [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488], que indica a la aplicación Cuándo se debe cambiar el cursor del mouse sobre la vista.  Cuando el mouse está sobre un cuadro de texto en la vista de vistas en WebView, el cursor cambia de la flecha al selector.  La `cursor` propiedad en el `CompositionController` indica a la aplicación lo que actualmente debe ser el cursor del ratón para la vista.  

## 0.9.430  

[Paquete NuGet][NuGetGallery0.9.430] \ | versión mínima de Microsoft Edge 82.0.430.0.  

El SDK de WebView2 es la versión oficial de Win32 C++ beta, que incorpora varias solicitudes de características de comentarios.  El equipo de WebView intenta limitar el número de versiones con cambios importantes, pero a medida que se aproxima la disponibilidad general, se usa la versión beta para incorporar varios cambios importantes de una sola vez.  

*   > [!IMPORTANT]
    > **Cambio importante**: a medida que la versión final, el equipo de WebView ha cambiado el nombre del prefijo *IWebView2WebView*   a *ICoreWebView2*   para asegurarse de que la API WebView2 se alinee con la Convención de nomenclatura de la API de Windows.  Además, para poder aprovechar el SDK de WebView2 de marcos de interfaz de usuario, el equipo de WebView se separa `ICoreWebView2` en [ICoreWebView2][ReferenceWin32Icorewebview209430] y [ICoreWebView2Host][ReferenceWin32Icorewebview2host09430].  `ICoreWebView2Host` permite cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.  ICoreWebView2 admite todas las demás funcionalidades de WebView2.  Para obtener más información sobre cómo incorporar los cambios, vaya a la [solicitud de incorporación][GithubMicrosoftedgeWebview2samplesPr17] de WebView2 en el proyecto [APISample][GithubMicrosoftedgeWebview2samplesMain] de WebView2.  
*   > [!IMPORTANT]
    > **Cambio importante**: Divida [DocumentStateChanged][ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190] en tres componentes:  [SourceChanged][ReferenceWin32Icorewebview2AddSourcechanged09430], [ContentLoading][ReferenceWin32Icorewebview2AddContentloading09430]y [HistoryChanged][ReferenceWin32Icorewebview2AddHistorychanged09430].  Ahora, cuando la dirección URL de origen cambia, `SourceChanged` se desencadena el evento.  Cuando se cambia el estado del historial, `HistoryChanged` se activa el evento.  El `ContentLoading` evento se desencadena antes del script inicial cuando se carga un documento nuevo.  
*   Se ha agregado compatibilidad con la arquitectura de ARM64.  
*   Se ha agregado la compatibilidad del panel de entrada de software \ (SIP \) para dispositivos con pantalla táctil.  
*   Se ha agregado compatibilidad con Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 y Windows Server 2016.  
*   Se ha agregado [NotifyParentWindowPositionChanged][ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430] que permite que la barra de estado siga la ventana en el modo de ventana.  El cambio debe implementarse también en el modo sin ventana para que funcionen las características de accesibilidad.  
*   Se ha agregado la configuración [AreRemoteObjectsAllowed][ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430] para controlar globalmente si un objeto remoto puede acceder a una página.  De forma predeterminada, `AreRemoteObjectsAllowed` está habilitado, lo que significa que los objetos remotos agregados por [AddRemoteObject][ReferenceWin32Icorewebview2Addremoteobject09430] son accesibles desde la página.  Cuando `AreRemoteObjectsAllowed` está deshabilitado, no se puede tener acceso a los objetos desde la página.  Los cambios se aplican en el siguiente evento de navegación.  
*   Se ha agregado una configuración de [IsZoomControlEnabled][ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430] para evitar que los usuarios afecten al zoom de la vista en WebView con `ctrl` + `+` y `ctrl` + `-` \ (o `ctrl` + rueda del mouse \).  El zoom se puede establecer con [put_ZoomFactor][ReferenceWin32Icorewebview2hostPutZoomfactor09430] cuando la configuración está deshabilitada.  
*   Se ha cambiado el ZoomFactor para que solo se aplique a la vista en WebView actual.  Los cambios de zoom aplicados a la vista Web actual no afectan a otras vistas de web que haya desplazado hasta el mismo sitio de origen.  Para obtener más información, vaya a [get_ZoomFactor][ReferenceWin32Icorewebview2hostGetZoomfactor09430].  
*   Interfaz de usuario de ZoomView HID para WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Se ha agregado [SetBoundsAndZoomFactor][ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430].  Ahora, puede establecer el factor de zoom y los límites de un WebView al mismo tiempo.  
*   Se agregó el evento [WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] .  Para obtener más información, vaya a [add_WindowCloseRequested][ReferenceWin32Icorewebview2AddWindowcloserequested09430] \ ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]\).  
*   Se ha agregado compatibilidad con el `beforeunload` tipo de cuadro de diálogo para eventos de JavaScript y se ha agregado [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430] entrada enum.  
*   Se ha agregado [GetHeaders][ReferenceWin32Icorewebview2httprequestheadersGetheaders09430] a HttpRequestHeaders, [GetHeader][ReferenceWin32Icorewebview2httpresponseheadersGetheader09430] a HttpResponseHeaders y [get_HasCurrentHeader][ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430] propiedad a HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Cambio importante**: `DevToolsProtocolEventReceived` comportamiento modificado.  Ahora, puedes crear un [DevToolsProtocolEventReceiver][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430] para un determinado evento de protocolo de DevTools y suscribirte o cancelar la suscripción a ese evento con [add_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430] / [remove_DevToolsProtocolEventReceived][ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430].
*   > [!IMPORTANT]
    > **Cambio destacado**: se ha cambiado el WebMessageReceivedEventArgs ' [get_WebMessageAsString][ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190] propiedad a un método [TryGetWebMessageAsString][ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430] .  
*   > [!IMPORTANT]
    > **Cambio destacado**: se ha cambiado `AcceleratorKeyPressedEventArgs` el método [Handle][ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190] a una propiedad [get_Handled][ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430] .  

## 0.8.355

[Paquete NuGet][NuGetGallery0.8.355] \ | versión mínima de Microsoft Edge 80.0.355.0.

*   Se ha publicado el ejemplo WebView2API, una guía completa del SDK de WebView2.  Para obtener más información, vaya a [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Se ha agregado compatibilidad IME para todos los idiomas, además del inglés \ ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Se actualizó la superficie de API del `WebResourceRequested` evento en respuesta a informes de errores.  Especificar simultáneamente un filtro y un evento en la creación ahora está en desuso.  Para crear un evento solicitado de un recurso Web, use [add_WebResourceRequested][ReferenceWin32Iwebview2webview5AddWebresourcerequested08190] para agregar el evento y [AddWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190] para agregar un filtro.  [RemoveWebResourceRequestedFilter][ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190] quita el filtro \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Cambio importante**: comportamiento de pantalla completa modificada.  [IsFullScreenAllowed][ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]desusado.  Ahora, de forma predeterminada, si un elemento de un WebView \ (como un video \) se establece en pantalla completa, rellena los límites de la vista de página.  Usa el evento [ContainsFullScreenElementChanged][ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190] y [get_ContainsFullScreenElement][ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190] para especificar cómo la aplicación debe cambiar el tamaño de WebView si un elemento quiere entrar en modo de pantalla completa.  

## 0.8.314  

[Paquete NuGet][NuGetGallery0.8.314] \ | versión mínima de Microsoft Edge 80.0.314.0.  

*   Se ha agregado compatibilidad con Windows 7, Windows 8 y Windows 8,1.  
*   Se ha agregado compatibilidad de depuración de Visual Studio y Visual Studio para WebView2.  Ahora, depura tu script en el WebView2 directamente desde tu IDE.  Para obtener más información, vaya a [Cómo depurar al desarrollar con controles WebView2][HowtoDebug].  
*   `Native Object Injection`Se agregó, lo que permite que la secuencia de comandos que se ejecuta dentro de WebView2 tenga acceso a un objeto IDispatch desde el componente Win32 de la aplicación y obtenga acceso a las propiedades del objeto IDispatch.  Para obtener más información, vaya a [AddRemoteObject][ReferenceWin32Iwebview2webview4Addremoteobject08190] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   `AcceleratorKeyPressed`Evento agregado.  Para obtener más información, vaya a [add_AcceleratorKeyPressed][ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Deshabilitado `Context Menus` .  Para obtener más información, vaya a [put_AreDefaultContextMenusEnabled][ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Actualizado `DPI Awareness` .  Ahora, el reconocimiento de PPP de WebView es el mismo que el reconocimiento de PPP de la aplicación host.  
    
    > [!NOTE]
    > Si se inicia otra aplicación híbrida con un conocimiento de PPP diferente al de la vista previa original, el nuevo WebView no se inicia si el directorio de datos de usuario es el mismo \ ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]\).  
    
*   Se actualizó `Notification Change Behavior` para que WebView2 rechace automáticamente las solicitudes de permiso de notificaciones que el contenido web hospedado en la vista de Web.  

## 0.8.270  

[Paquete NuGet][NuGetGallery0.8.270] \ | versión mínima de Microsoft Edge 78.0.270.0.  

*   Se ha agregado un `DocumentTitleChanged` evento para indicar que el título del documento debe cambiar \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   API agregada `GetWebView2BrowserVersionInfo` \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   `NewWindowRequested`Evento agregado.  
*   `CreateWebView2EnvironmentWithDetails`Función actualizada para quitar `releaseChannelPreference` .  Para obtener más información sobre la `CreateWebView2EnvironmentWithDetails` función, vaya a [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  El registro y la variable de entorno override aún se admiten.  La preferencia de canal predeterminada se usa a menos que se reemplace.  
    Durante la búsqueda de canales, el equipo de WebView omite cualquier versión de canal anterior que no sea compatible con el SDK de WebView2.  
    El equipo de WebView selecciona el canal más estable para asegurar los comportamientos más coherentes para el usuario final.  Cuando prueba con las últimas compilaciones Canarias, debe crear un script para establecer la `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` variable de entorno en `1` antes de iniciar la aplicación.  
*   Se actualizó la `CreateWebView2EnvironmentWithDetails` función con lógica para seleccionar `userDataFolder` cuando no se especifica.  Para obtener más información sobre la `CreateWebView2EnvironmentWithDetails` función, vaya a [CreateWebView2EnvironmentWithDetails][ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190].  Si previamente usó la ubicación predeterminada `userDataFolder` , al cambiar al nuevo SDK el valor predeterminado `userDataFolder` es RESET \ (establecido en una nueva ubicación en el directorio de códigos de host \) y también se restablece su estado.  
    Si el proceso de hospedaje no tiene permiso de escritura en el directorio especificado, la `CreateWebView2EnvironmentWithDetails` función puede dar error.  Puede copiar los datos del directorio de datos de usuario anterior en el nuevo directorio.  

## 0.8.230  

[Paquete NuGet][NuGetGallery0.8.230] \ | versión mínima de Microsoft Edge 77.0.230.0.  

*   API agregada `Stop` para detener todas las búsquedas de recursos pendientes y navegación \ ([\ #28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   `.tlb`Se agregó el archivo al paquete de NuGet \ ([\ #22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Se han agregado proyectos de .NET a la lista de instalador en el paquete NuGet \ ([\ #32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  

## 0.8.190  

[Paquete NuGet][NuGetGallery0.8.190] \ | versión mínima de Microsoft Edge 77.0.190.0.  

*   Se ha agregado `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` para controlar si los usuarios pueden abrir DevTools \ ([\ #16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` Se agregó al control si se muestra la barra de estado \ ([\ #19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Se ha agregado `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` para volver atrás y reenviarlo mediante el historial de navegación.  
*   Se han agregado los tipos de encabezado HTTP \ ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` \) para ver y modificar los encabezados HTTP en WebView.  
*   Se ha agregado compatibilidad con WebView de 32-bit en máquinas de 64 bits \ ([\ #13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Se ha agregado el IDL de vista previa al SDK \ ([\ #14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Se agregó lib para admitir `IID\_\*` objetos de identificador de interfaz \ ([\ #12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Se agregaron la ruta de inclusión, la vinculación y la copia automática de archivos DLL al `TARGET` archivo NuGet en el SDK.  
*   Se ha habilitado la solicitud `window.open()` de script.  

## 0.8.149  

[Paquete NuGet][NuGetGallery0.8.149] \ | versión mínima de Microsoft Edge 76.0.149.0.  

Versión inicial de Developer Preview.  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Modo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[Webview2ConceptsDistributionFixedVersionMode]: ./concepts/distribution.md#fixed-version-distribution-mode "Modo de distribución de versiones fijas: distribución de aplicaciones con WebView2 | Microsoft docs"  
[Webview2ConceptsDistributionUnderstandRuntimeInstaller]: ./concepts/distribution.md#understanding-the-webview2-runtime "Comprender el motor de tiempo de ejecución y el instalador de WebView2: distribución de aplicaciones con WebView2 | Microsoft docs"  
[ConceptsVersioning]: ./concepts/versioning.md "Descripción de las versiones de explorador y WebView2 | Microsoft docs"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "API experimentales: Descripción de las versiones de explorador y WebView2 | Microsoft docs"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Introducción a WebView2 en las aplicaciones de Windows Forms | Microsoft docs"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Introducción a WebView2 en WPF | Microsoft docs"  
[HowtoDebug]: ./howto/debug.md "Cómo depurar al desarrollar con controles WebView2 | Microsoft docs"  

[ReferenceWin32Iwebview2acceleratorkeypressedeventargsHandle08190]: /microsoft-edge/webview2/reference/win32/iwebview2acceleratorkeypressedeventargs?view=webview2-0.8.355&preserve-view=true#handle "Controlador-interfaz IWebView2AcceleratorKeyPressedEventArgs | Microsoft docs"  
[ReferenceWin32Iwebview2containsfullscreenelementchangedeventhandler08190]: /microsoft-edge/webview2/reference/win32/iwebview2containsfullscreenelementchangedeventhandler?view=webview2-0.8.355&preserve-view=true "interfaz IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft docs"  
[ReferenceWin32Iwebview2settings2PutAredefaultcontextmenusenabled08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings2?view=webview2-0.8.355&preserve-view=true#put_aredefaultcontextmenusenabled "interfaz de put_AreDefaultContextMenusEnabled IWebView2Settings2 | Microsoft docs"  
[ReferenceWin32Iwebview2settingsGetIsfullscreenallowedDeprecated08190]: /microsoft-edge/webview2/reference/win32/iwebview2settings?view=webview2-0.8.355&preserve-view=true#get_isfullscreenallowed_deprecated "interfaz de get_IsFullscreenAllowed_deprecated IWebView2Settings | Microsoft docs"  
[ReferenceWin32Iwebview2webmessagereceivedeventargsGetWebmessageasstring08190]: /microsoft-edge/webview2/reference/win32/iwebview2webmessagereceivedeventargs?view=webview2-0.8.355&preserve-view=true#get_webmessageasstring "interfaz de get_WebMessageAsString IWebView2WebMessageReceivedEventArgs | Microsoft docs"  
[ReferenceWin32Iwebview2webview4AddAcceleratorkeypressed08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#add_acceleratorkeypressed "interfaz de add_AcceleratorKeyPressed IWebView2WebView4 | Microsoft docs"  
[ReferenceWin32Iwebview2webviewAddDocumentstatechanged08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview?view=webview2-0.8.355&preserve-view=true#add_documentstatechanged "interfaz de add_DocumentStateChanged IWebView2WebView | Microsoft docs"  
[ReferenceWin32Iwebview2webview4Addremoteobject08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview4?view=webview2-0.8.355&preserve-view=true#addremoteobject "AddRemoteObject: IWebView2WebView4 | Microsoft docs"  
[ReferenceWin32Iwebview2webview5AddWebresourcerequested08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#add_webresourcerequested "interfaz de add_WebResourceRequested IWebView2WebView5 | Microsoft docs"  
[ReferenceWin32Iwebview2webview5Addwebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#addwebresourcerequestedfilter "AddWebResourceRequestedFilter: IWebView2WebView5 | Microsoft docs"  
[ReferenceWin32Iwebview2webview5GetContainsfullscreenelement08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#get_containsfullscreenelement "interfaz de get_ContainsFullScreenElement IWebView2WebView5 | Microsoft docs"  
[ReferenceWin32Iwebview2webview5Removewebresourcerequestedfilter08190]: /microsoft-edge/webview2/reference/win32/iwebview2webview5?view=webview2-0.8.355&preserve-view=true#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter: IWebView2WebView5 | Microsoft docs"  
[ReferenceWin32WebView2IdlCreatewebview2environmentwithdetails08190]:  /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.8.355&preserve-view=true#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-Globals | Microsoft docs"  

[ReferenceWin32Icorewebview209430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2acceleratorkeypressedeventargsGetHandled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2acceleratorkeypressedeventargs?view=webview2-0.9.430&preserve-view=true#get_handled "interfaz de get_Handled ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft docs"  
[ReferenceWin32Icorewebview2AddContentloading09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_contentloading "interfaz de add_ContentLoading ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2AddHistorychanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_historychanged "interfaz de add_HistoryChanged ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2Addremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#addremoteobject "AddRemoteObject: ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2AddSourcechanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_sourcechanged "interfaz de add_SourceChanged ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2AddWindowcloserequested09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#add_windowcloserequested "interfaz de add_WindowCloseRequested ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2CoreWebview2ScriptDialogKind09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#core_webview2_script_dialog_kind "Interfaz de CORE_WEBVIEW2_SCRIPT_DIALOG_KIND ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiver09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#add_devtoolsprotocoleventreceived "interfaz de add_DevToolsProtocolEventReceived ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived09430]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-0.9.430&preserve-view=true#remove_devtoolsprotocoleventreceived "interfaz de remove_DevToolsProtocolEventReceived ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin32Icorewebview2environmentGetBrowserversioninfo09430]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.430&preserve-view=true#get_browserversioninfo "interfaz de get_BrowserVersionInfo ICoreWebView2Environment | Microsoft docs"  
[ReferenceWin32Icorewebview2host09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true "interfaz ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Webview2IdlGetcorewebview2browserversioninfo09430]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.430&preserve-view=true#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-Globals | Microsoft docs"  
[ReferenceWin32Icorewebview2hostGetZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#get_zoomfactor "interfaz de get_ZoomFactor ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Icorewebview2hostNotifyparentwindowpositionchanged09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged: ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Icorewebview2hostPutZoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#put_zoomfactor "interfaz de put_ZoomFactor ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Icorewebview2hostSetboundsandzoomfactor09430]: /microsoft-edge/webview2/reference/win32/icorewebview2host?view=webview2-0.9.430&preserve-view=true#setboundsandzoomfactor "SetBoundsAndZoomFactor: ICoreWebView2Host | Microsoft docs"  
[ReferenceWin32Icorewebview2httpheaderscollectioniteratorGetHascurrentheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpheaderscollectioniterator?view=webview2-0.9.430&preserve-view=true#get_hascurrentheader "interfaz de get_HasCurrentHeader ICoreWebView2HttpHeadersCollectionIterator | Microsoft docs"  
[ReferenceWin32Icorewebview2httprequestheadersGetheaders09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httprequestheaders?view=webview2-0.9.430&preserve-view=true#getheaders "GetHeaders: ICoreWebView2HttpRequestHeaders | Microsoft docs"  
[ReferenceWin32Icorewebview2httpresponseheadersGetheader09430]: /microsoft-edge/webview2/reference/win32/icorewebview2httpresponseheaders?view=webview2-0.9.430&preserve-view=true#getheader "GetHeader-interfaz ICoreWebView2HttpResponseHeaders | Microsoft docs"  
[ReferenceWin32Icorewebview2Removeremoteobject09430]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.430&preserve-view=true#removeremoteobject "RemoveRemoteObject: ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_areremoteobjectsallowed "interfaz de get_AreRemoteObjectsAllowed ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetIszoomcontrolenabled09430]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.430&preserve-view=true#get_iszoomcontrolenabled "interfaz de get_IsZoomControlEnabled ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin32Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring09430]: /microsoft-edge/webview2/reference/win32/icorewebview2webmessagereceivedeventargs?view=webview2-0.9.430&preserve-view=true#trygetwebmessageasstring "TryGetWebMessageAsString: ICoreWebView2WebMessageReceivedEventArgs | Microsoft docs"  

[ReferenceWin32Icorewebview2AddFramenavigationcompleted09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_framenavigationcompleted "interfaz de add_FrameNavigationCompleted ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2Addhostobjecttoscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#addhostobjecttoscript "AddHostObjectToScript: ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2AddNewwindowrequested09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#add_newwindowrequested "interfaz de add_NewWindowRequested ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2environmentGetBrowserversionstring09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environment?view=webview2-0.9.488&preserve-view=true#get_browserversionstring " | Microsoft docs"  
[ReferenceWin32Icorewebview2environmentoptions09488]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.488&preserve-view=true "interfaz ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCompositionController | Microsoft docs"
[ReferenceWin32Icorewebview2experimentalcompositioncontroller09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCompositionController | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcursorchangedeventhandler09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcursorchangedeventhandler?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalpointerinfo09488]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalpointerinfo?view=webview2-0.9.488-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalPointerInfo | Microsoft docs"  
[ReferenceWin32Icorewebview2Removehostobjectfromscript09488]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-0.9.488&preserve-view=true#removehostobjectfromscript "RemoveHostObjectFromScript: ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetAreremoteobjectsallowed09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_areremoteobjectsallowed "interfaz de get_AreRemoteObjectsAllowed ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetIsbuiltinerrorpageenabled09488]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.488&preserve-view=true#get_isbuiltinerrorpageenabled " | Microsoft docs"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithdetails09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-Globals | Microsoft docs"  
[ReferenceWin32Webview2IdlCreatecorewebview2environmentwithoptions09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  
[ReferenceWin32Webview2IdlGetavailablecorewebview2browserversionstring09488]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.488&preserve-view=true#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Microsoft docs"  


[DotnetApiMicrosoftWebWebview2Core]: /dotnet/api/microsoft.web.webview2.core "Espacio de nombres Microsoft. Web. WebView2. Core | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2Wpf]: /dotnet/api/microsoft.web.webview2.wpf "Espacio de nombres Microsoft. Web. WebView2. WPF | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2Winforms]: /dotnet/api/microsoft.web.webview2.winforms "Espacio de nombres Microsoft. Web. WebView2. WinForms | Microsoft docs"  

[WebView2RuntimeNotFoundException]: /dotnet/api/microsoft.web.webview2.core.webview2runtimenotfoundexception "CoreWebView2. WebView2RuntimeNotFound (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2]: /dotnet/api/microsoft.web.webview2.core.corewebview2 "Clase CoreWebView2 (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environment]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment "Clase CoreWebView2Environment (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.comparebrowserversions "CoreWebView2Environment. CompareBrowserVersions (String, String) (método) (Microsoft. Web. WebView2. Core) | Microsoft docs"
[DotnetApiMicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: /dotnet/api/microsoft.web.webview2.core.corewebview2environment.getavailablebrowserversionstring "CoreWebView2Environment. GetAvailableBrowserVersionString (String) (método) (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.newwindowrequested "Evento CoreWebView2. NewWindowRequested (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Permissionrequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.permissionrequested "Evento CoreWebView2. PermissionRequested (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: /dotnet/api/microsoft.web.webview2.core.corewebview2.scriptdialogopening "Evento CoreWebView2. ScriptDialogOpening (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: /dotnet/api/microsoft.web.webview2.core.corewebview2.webresourcerequested "Evento CoreWebView2. WebResourceRequested (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httprequestheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httprequestheaders "Clase CoreWebView2HttpRequestHeaders (Microsoft. Web. WebView2. Core) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2httpresponseheaders]: /dotnet/api/microsoft.web.webview2.core.corewebview2httpresponseheaders "Clase CoreWebView2HttpResponseHeaders (Microsoft. Web. WebView2. Core) | Microsoft docs"  

[DotnetApiMicrosoftWebWebview2WinformsCorewebview2creationproperties]: /dotnet/api/microsoft.web.webview2.winforms.corewebview2creationproperties "Clase CoreWebView2CreationProperties (Microsoft. Web. WebView2. WinForms) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2WinformsWebview2Source]: /dotnet/api/microsoft.web.webview2.winforms.webview2.source "Webview2. Source (clase) (Microsoft. Web. WebView2. WinForms) | Microsoft docs"  


[DotnetApiMicrosoftWebWebview2WpfWebview2Buildwindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.buildwindowcore "WebView2. BuildWindowCore (HandleRef) (Microsoft. Web. WebView2. WPF) | Microsoft docs"  
[DotnetApiMicrosoftWebWebview2WpfWebview2Destroywindowcore]: /dotnet/api/microsoft.web.webview2.wpf.webview2.destroywindowcore "WebView2. DestroyWindowCore (HandleRef) (Microsoft. Web. WebView2. WPF) | Microsoft docs"  

[ReferenceWin32Icorewebview2Addhostobjecttoscript09538]: /microsoft-edge/webview2/reference/win32/icorewebview2#addhostobjecttoscript?view=webview2-0.9.538&preserve-view=true "AddHostObjectToScript: ICoreWebView2 | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-0.9.538-prerelease&preserve-view=true#add_webresourceresponsereceived "interfaz de add_WebResourceResponseReceived ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentaloptionsGetIssinglesignonusingosprimaryaccountenabled09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironmentoptions?view=webview2-0.9.538-prerelease&preserve-view=true#get_issinglesignonusingosprimaryaccountenabled "interfaz de get_IsSingleSignOnUsingOSPrimaryAccountEnabled ICoreWebView2ExperimentalEnvironmentOptions | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalnewwindowrequestedeventargs?view=webview2-0.9.538-prerelease&preserve-view=true#get_windowfeatures "interfaz de get_WindowFeatures ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalwindowfeatures09538]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwindowfeatures?view=webview2-0.9.538-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalWindowFeatures | Microsoft docs"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetIsuserinitiated09538]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.538&preserve-view=true#get_isuserinitiated "interfaz de get_IsUserInitiated ICoreWebView2NewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin32Icorewebview2settingsGetArehostobjectsallowed09538]: /microsoft-edge/webview2/reference/win32/icorewebview2settings?view=webview2-0.9.538&preserve-view=true#get_arehostobjectsallowed "interfaz de get_AreHostObjectsAllowed ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09538]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.538&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  

[ReferenceWin32Icorewebview2environmentoptionsGetAllowsinglesignonusingosprimaryaccount09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#get_allowsinglesignonusingosprimaryaccount "interfaz de get_AllowSingleSignOnUsingOSPrimaryAccount ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin32Icorewebview2environmentoptionsPutAdditionalbrowserarguments09622]: /microsoft-edge/webview2/reference/win32/icorewebview2environmentoptions?view=webview2-0.9.622&preserve-view=true#put_additionalbrowserarguments "interfaz de put_AdditionalBrowserArguments ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin32Icorewebview2newwindowrequestedeventargsGetWindowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2newwindowrequestedeventargs?view=webview2-0.9.622&preserve-view=true#get_windowfeatures "interfaz de get_WindowFeatures ICoreWebView2NewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin32Icorewebview2windowfeatures09622]: /microsoft-edge/webview2/reference/win32/icorewebview2windowfeatures?view=webview2-0.9.622&preserve-view=true "interfaz ICoreWebView2WindowFeatures | Microsoft docs"  
[ReferenceWin32IdlCreatecorewebview2environmentwithoptions09622]: /microsoft-edge/webview2/reference/win32/webview2-idl?view=webview2-0.9.622&preserve-view=true#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft Edge"  
[ReferenceWin32Icorewebview2experimentalenvironment09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalenvironment?view=webview2-0.9.628-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalEnvironment | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponsereceivedeventargsPopulateresponsecontent09628]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponsereceivedeventargs?view=webview2-0.9.628-prerelease&preserve-view=true#populateresponsecontent "PopulateResponseContent: ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs | Microsoft docs"  

[ReferenceWin32Icorewebview2experimentalAddDomcontentloaded10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_domcontentloaded "interfaz de add_DOMContentLoaded ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalAddWebresourceresponsereceived10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#add_webresourceresponsereceived "interfaz de add_WebResourceResponseReceived ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalGetCookiemanager10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_cookiemanager "interfaz de get_CookieManager ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalGetEnvironment10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#get_environment "interfaz de get_Environment ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalNavigatewithwebresourcerequest10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimental?view=webview2-1.0.674-prerelease&preserve-view=true#navigatewithwebresourcerequest "NavigateWithWebResourceRequest: ICoreWebView2Experimental | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalcompositioncontroller2GetSystemcursorid10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalcompositioncontroller2#get_systemcursorid?view=webview2-1.0.674-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalWebResourceResponseView | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseview10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true "interfaz ICoreWebView2ExperimentalWebResourceResponseView | Microsoft docs"  
[ReferenceWin32Icorewebview2experimentalwebresourceresponseviewGetcontent10674]: /microsoft-edge/webview2/reference/win32/icorewebview2experimentalwebresourceresponseview?view=webview2-1.0.674-prerelease&preserve-view=true#getcontent "GetContent-interface ICoreWebView2ExperimentalWebResourceResponseView | Microsoft docs"  

[DeployedgeMicrosoftEdgePolicies]: /deployedge/microsoft-edge-policies "Microsoft Edge-directivas | Microsoft docs"  
[DeployedgeMicrosoftEdgeWebviewPolicies]: /deployedge/microsoft-edge-webview-policies "Microsoft Edge WebView2-Policies | Microsoft docs"  

[WindowsSecurityThreatProtectionMicrosoftDefenderApplicationGuardWindows10]: /windows/security/threat-protection/microsoft-defender-application-guard/md-app-guard-overview "Protección de aplicaciones de Microsoft defender (Windows 10)-seguridad de Windows | Microsoft docs"

[DotnetApiSystemComponentmodelCancelEventargs]: /dotnet/api/system.componentmodel.canceleventargs "Clase CancelEventArgs (System. ComponentModel) | Microsoft docs"  
[DotnetApiSystemEventargs]: /dotnet/api/system.eventargs "Clase EventArgs (sistema) | Microsoft docs"  
[DotnetStandardAssemblyStrongNamed]: /dotnet/standard/assembly/strong-named "Ensamblados con nombre seguro | Microsoft docs"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 16"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Repositorio de comentarios para el problema 17 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback (problema 18)"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repositorio de comentarios para el problema 27 de MicrosoftEdge/WebViewFeedback"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback (problema 30)"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 108"
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 119"
[GithubMicrosoftedgeWebviewfeedbackIssue131]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/131 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 131"
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue177]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/177 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 177"
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 179"
[GithubMicrosoftedgeWebviewfeedbackIssue181]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/181 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 181"
[GithubMicrosoftedgeWebviewfeedbackIssue183]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/183 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 183"
[GithubMicrosoftedgeWebviewfeedbackIssue185]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/185 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 185"
[GithubMicrosoftedgeWebviewfeedbackIssue204]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/204 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 204"
[GithubMicrosoftedgeWebviewfeedbackIssue219]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/219 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 219"
[GithubMicrosoftedgeWebviewfeedbackIssue228]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/228 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 228"
[GithubMicrosoftedgeWebviewfeedbackIssue235]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/235 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 235"
[GithubMicrosoftedgeWebviewfeedbackIssue250]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/250 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 250"
[GithubMicrosoftedgeWebviewfeedbackIssue293]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/293 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 293"
[GithubMicrosoftedgeWebviewfeedbackIssue318]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/318 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 318"  
[GithubMicrosoftedgeWebviewfeedbackIssue382]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/382 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 382"  
[GithubMicrosoftedgeWebviewfeedbackIssue431]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/431 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 431"  
[GithubMicrosoftedgeWebviewfeedbackIssue432]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/432 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 432"  


[GithubMicrosoftedgeWebview2AnnouncementIssue2]:  https://github.com/MicrosoftEdge/WebView2Announcement/issues/2 "Repositorio de anuncios para MicrosoftEdge/WebViewAnnouncement, problema 2"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Mover Project para usar el SDK más reciente de WebView2 0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/SampleApps/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "Galería de NuGet | Microsoft. Web. WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galería de NuGet | Microsoft. Web. WebView2 v 0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galería de NuGet | Microsoft. Web. WebView2 v 0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galería de NuGet | Versión preliminar de Microsoft. Web. WebView2 v 0.9.515"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Galería de NuGet | Microsoft. Web. WebView2 v 0.9.538"  
[NuGetGallery0.9.579]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.579 "Galería de NuGet | Microsoft. Web. WebView2 v 0.9.579"
[NuGetGallery0.9.622.11]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.622.11 "Galería de NuGet | Microsoft. Web. WebView2 v 0.9.622.11"
[NuGetGallery1.0.622.22]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.622.22 "Galería de NuGet | Microsoft. Web. WebView2 v 1.0.622.22"
[NuGetGallery0.9.628-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.628-prerelease "Galería de NuGet | Versión preliminar de Microsoft. Web. WebView2 v 0.9.628"  
[NuGetGallery1.0.674-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/1.0.674-prerelease "Galería de NuGet | Versión preliminar de Microsoft. Web. WebView2 v 1.0.674"  