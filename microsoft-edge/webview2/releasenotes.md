---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: Notas de la versión de Microsoft Edge WebView2 para Win32, WPF y WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 1f229474d4de416f9f6516ce62ab88097f2bc1aa
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844421"
---
# Notas de la versión para el SDK de WebView2  

El equipo de WebView2 está ofreciendo actualizaciones para el [SDK de WebView2][NuGetGallery] en una cadencia de 6 semanas.  Revise el siguiente contenido para obtener información actualizada sobre anuncios de productos, adiciones y modificaciones a la superficie de la API y cambios importantes.  

> [!NOTE]
> Vuelve a compilar la aplicación después de actualizar el paquete de NuGet.  

> [!IMPORTANT]
> Aunque WebView2 es una versión preliminar, las API de .NET están en `pre-release package` .  

## 0.9.538  

[Paquete NuGet][NuGetGallery0.9.538] \ | versión mínima de Microsoft Edge 85.0.538.0.  

#### General  

*   Compatibilidad de eliminación de WebView2 SDK versión [0.8.149](#08149).  El equipo de WebView recomienda mantenerse al día con la última versión de WebView2.  
*   Directiva de grupo actualizada que se debe tener en cuenta cuando se modifica la ruta de acceso del perfil del explorador Microsoft Edge ([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]).  

#### C/C++ Win32  

*   Se ha agregado [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures] que `window.open()` se desencadena cuando se llama y se asocia [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin3209538Icorewebview2experimentalwindowfeatures] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Cambio importante**: [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] se ha dejado de usar y se ha reemplazado por [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209538Webview2IdlCreatecorewebview2environmentwithoptions].  
*   > [!IMPORTANT]
    > **Cambio importante**: para asegurarse de que la API de WebView2 se alinee con las convenciones de nomenclatura de la API de Windows, el equipo de WebView actualizará los nombres de los siguientes.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed] es ahora [AreHostObjectsAllowed][ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed].  
*   [AddHostObjectToScript][ReferenceWin3209538Icorewebview2Addhostobjecttoscript] actualizado para garantizar que los marcadores de serializador de objeto de host original se establezcan en los objetos proxy y se serialicen como un objeto de host cuando se pasan como un parámetro en la devolución de llamada de JavaScript \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  

#### .NET (versión preliminar de 0.9.538)  

*   Se han publicado ejemplos de WinForms y WPF WebView2API, que son guías completas del SDK de WebView2.  Para obtener más información, consulte [repositorios de ejemplos][GithubMicrosoftedgeWebview2samplesMain].  
*   Se ha agregado compatibilidad con las [API experimentales][ConceptsVersioningExperimentalApis]de hospedaje visual y características de la ventana.  
*   > [!IMPORTANT]
    > **Cambio importante**: las siguientes aplazaciones ahora implementan IDisposable: [ScriptDialogOpening][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Webresourcerequested]y [PermissionRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   Se han agregado [GetAvailableBrowserVersionString][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] y [CompareBrowserVersions][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] como estáticas de [CoreWebView2Environment][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environment] .  

## 0.9.515-versión preliminar  

[Paquete NuGet][NuGetGallery0.9.515-prerelease] \ | versión mínima de Microsoft Edge 84.0.515.0.  

*   > [!IMPORTANT]
    > **Anuncio**: WebView2 ahora es compatible con Windows Forms y WPF en .NET Framework 4.6.2 o versiones posteriores, .net Core 3,0 o posterior en el **paquete preliminar**.  
*   Para obtener más información sobre la creación de aplicaciones WPF y la [referencia de WPF][ReferenceWpf09515Reference] WebView2 en las API específicas de WPF, consulte la guía de [Introducción a WPF][GettingstartedWpf].  
*   Para obtener más información sobre la creación de aplicaciones de Windows Forms y la [referencia de Windows Forms][ReferenceWinforms09515Reference] WebView2 para las API específicas de Windows Forms, vea la guía de introducción a [formularios Windows Forms][GettingstartedWinforms].  
*   Para obtener más información sobre las API de CoreWebView2, consulte [.net Reference][ReferenceDotnet09515Reference].  
*   > [!CAUTION]
    > **Problemas conocidos**: el equipo de WebView tiene constancia de algunos problemas en la versión preliminar que se están resolviendo en versiones futuras.  
    > *   **Reconocimiento de PPP**: WEBVIEW2 para WPF actualmente no reconoce los ppp.  Al inicializar WebView2 en monitores con alta resolución de PPP, existe un problema conocido en el que WebView se inicializa en primer lugar como una fracción de la ventana hasta que se cambia el tamaño de la ventana.  
    > *   **WPF Designer**: WPF Designer no es compatible actualmente.  Agrega el control WebView2 en tu aplicación modificando directamente el XAML correspondiente en un editor de texto.  

## 0.9.488  

[Paquete NuGet][NuGetGallery0.9.488] \ | versión mínima de Microsoft Edge 84.0.488.0.  

*   > [!IMPORTANT]
    > **Anuncio**: a partir de la próxima versión 83 de Microsoft Edge, la vista previa de perenne ya no se destina al canal de explorador estable.  En su lugar, se destina a otro conjunto de binarios, [WebView2 tiempo de ejecución][ConceptsDistributionEvergreenMode]de personalización de marca, que se puede encadenar a través de un instalador el equipo de WebView se está desarrollando en este momento.  Para obtener más información, consulte [aplicación-distribución][ConceptsDistribution].  
*   > [!IMPORTANT]
    > **Anuncio**: avanzar, el equipo de WebView publica dos paquetes: un paquete preliminar con las API experimentales \ (para probar \) y un paquete de versión estable con API estables \ (para la confianza \).  Para obtener más información sobre las diferencias, consulte [comprender las versiones y los exploradores de WebView2][ConceptsVersioning].  
*   > [!IMPORTANT]
    > **Cambio importante**: para garantizar que la API de WebView2 se alinee con las convenciones de nomenclatura de la API de Windows, el equipo de WebView actualizará los nombres de las siguientes interfaces.  
    > *   `CORE_WEBVIEW2_*` el prefijo es ahora `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo] es ahora [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo] está ahora [get_BrowserVersionString][ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring].  
    > *   [AddRemoteObject][ReferenceWin3209430Icorewebview2Addremoteobject] es ahora [AddHostObjectToScript][ReferenceWin3209488Icorewebview2Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][ReferenceWin3209430Icorewebview2Removeremoteobject] es ahora [RemoveHostObjectFromScript][ReferenceWin3209488Icorewebview2Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` ya está `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Cambio importante**: `AddRemoteObject` también se cambia el nombre a los métodos de proxy de JS.  
    > *   `getLocal` ya está `getLocalProperty` .  
    > *   `setLocal` ya está `setLocalProperty` .  
    > *   `getRemote` ya está `getHostProperty` .  
    > *   `setRemote` ya está `setHostProperty` .  
    > *   `applyRemote` ya está `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Cambio importante**: [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] se ha dejado de usar y se ha reemplazado por [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions].  
*   Se agregó el evento [FrameNavigationCompleted][ReferenceWin3209488Icorewebview2AddFramenavigationcompleted] .  Ahora, cuando un iframe completa la navegación, se desencadena un evento y devuelve el éxito de la navegación y el identificador de navegación.  
*   Se agregó la interfaz [ICoreWebView2EnvironmentOptions][ReferenceWin3209488Icorewebview2environmentoptions] , que se puede usar para determinar la versión del motor en tiempo de ejecución de WebView2 de destino de la aplicación.  
*   Se agregó la configuración [IsBuiltInErrorPageEnabled][ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled] .  Ahora, puede habilitar o deshabilitar la página de error integrada para error de navegación y error de proceso de representación.  
*   Se ha actualizado la inyección de objetos remotos para admitir implementaciones de .NET IDispatch \ ([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Evento [NewWindowRequested][ReferenceWin3209488Icorewebview2AddNewwindowrequested] actualizado para administrar solicitudes de menús contextuales \ ([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Publicó el primer paquete de versión preliminar de WebView2 independiente donde puedes tener acceso a las API de hospedaje de visual.  El equipo de WebView actualizó [APISample][GithubMicrosoftedgeWebview2samplesMain] para incluir las nuevas API experimentales.  
    *   Se ha agregado la interfaz de [ICoreWebView2ExperimentalCompositionController][ReferenceWin3209488Icorewebview2experimentalcompositioncontroller] , que se usa para conectarse a un árbol de composición y proporcionar una entrada para la vista.  
    *   Se ha agregado [ICoreWebView2ExperimentalPointerInfo][ReferenceWin3209488Icorewebview2experimentalpointerinfo] que contiene toda la información de un `POINTER_INFO` .  Se pasa a SendPointerInput para inyectar la entrada del puntero en la vista de vista en WebView.  
    *   Se ha agregado un [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler] que indica a la aplicación Cuándo se debe cambiar el cursor del mouse sobre la vista.  Cuando el mouse está sobre un cuadro de texto en la vista de vistas en WebView, el cursor cambia de la flecha al selector.  La propiedad cursor en el `CompositionController` indica a la aplicación lo que debe hacer actualmente el cursor del mouse para la vista en WebView.  

## 0.9.430  

[Paquete NuGet][NuGetGallery0.9.430] \ | versión mínima de Microsoft Edge 82.0.430.0.  

El SDK de WebView2 es la versión oficial de Win32 C++ beta, que incorpora varias solicitudes de características de comentarios.  El equipo de WebView intenta limitar el número de versiones con cambios importantes, pero a medida que se aproxima la disponibilidad general, se usa la versión beta para incorporar varios cambios importantes de una sola vez.  

*   > [!IMPORTANT]
    > **Cambio importante**: a medida que la versión final, el equipo de WebView ha cambiado el nombre del prefijo *IWebView2WebView* a *ICoreWebView2* para asegurarse de que la API WebView2 se alinee con la Convención de nomenclatura de la API de Windows.  Además, para poder aprovechar el SDK de WebView2 de marcos de interfaz de usuario, el equipo de WebView se separa `ICoreWebView2` en [ICoreWebView2][ReferenceWin3209430Icorewebview2] y [ICoreWebView2Host][ReferenceWin3209430Icorewebview2host].  `ICoreWebView2Host` permite cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.  ICoreWebView2 admite todas las demás funcionalidades de WebView2.  Para obtener más información sobre cómo incorporar los cambios, consulte la [solicitud de incorporación][GithubMicrosoftedgeWebview2samplesPr17] de WebView2 en el proyecto de [APISample][GithubMicrosoftedgeWebview2samplesMain] de WebView2.  
*   > [!IMPORTANT]
    > **Cambio importante**: Divida [DocumentStateChanged][ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged] en tres componentes: [SourceChanged][ReferenceWin3209430Icorewebview2AddSourcechanged], [ContentLoading][ReferenceWin3209430Icorewebview2AddContentloading]y [HistoryChanged][ReferenceWin3209430Icorewebview2AddHistorychanged].  Ahora, cuando la dirección URL de origen cambia, `SourceChanged` se desencadena el evento.  Cuando se cambia el estado del historial, se desencadena el evento HistoryChanged.  El `ContentLoading` evento se desencadena antes del script inicial cuando se carga un documento nuevo.  
*   Se ha agregado compatibilidad con la arquitectura de ARM64.  
*   Se ha agregado la compatibilidad del panel de entrada de software \ (SIP \) para dispositivos con pantalla táctil.  
*   Se ha agregado compatibilidad con Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 y Windows Server 2016.  
*   Se ha agregado [NotifyParentWindowPositionChanged][ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged] que permite que la barra de estado siga la ventana en el modo de ventana.  El cambio debe implementarse también en el modo sin ventana para que funcionen las características de accesibilidad.  
*   Se ha agregado la configuración [AreRemoteObjectsAllowed][ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed] para controlar globalmente si un objeto remoto puede acceder a una página.  De forma predeterminada, `AreRemoteObjectsAllowed` está habilitado, lo que significa que los objetos remotos agregados por [AddRemoteObject][ReferenceWin3209430Icorewebview2Addremoteobject] son accesibles desde la página.  Cuando `AreRemoteObjectsAllowed` está deshabilitado, no se puede tener acceso a los objetos desde la página.  Los cambios se aplican en el siguiente evento de navegación.  
*   Se ha agregado una configuración de [IsZoomControlEnabled][ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled] para evitar que los usuarios afecten al zoom de la vista en WebView con `ctrl` + `+` y `ctrl` + `-` \ (o `ctrl` + rueda del mouse \).  El zoom se puede establecer con [put_ZoomFactor][ReferenceWin3209430Icorewebview2hostPutZoomfactor] cuando la configuración está deshabilitada.  
*   Se ha cambiado el ZoomFactor para que solo se aplique a la vista en WebView actual.  Los cambios de zoom aplicados a la vista Web actual no afectan a otras vistas de web que haya desplazado hasta el mismo sitio de origen.  Para obtener más información, consulte [get_ZoomFactor][ReferenceWin3209430Icorewebview2hostGetZoomfactor].  
*   Interfaz de usuario de ZoomView HID para WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Se ha agregado [SetBoundsAndZoomFactor][ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor].  Ahora, puede establecer el factor de zoom y los límites de un WebView al mismo tiempo.  
*   Se agregó el evento [WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] .  Para obtener más información ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]), consulte [add_WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] .  
*   Se ha agregado compatibilidad con el tipo de cuadro de diálogo beforeunload para eventos de cuadros de diálogo de JavaScript y se agrega [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind] entrada de enumeración.  
*   Se ha agregado [GetHeaders][ReferenceWin3209430Icorewebview2httprequestheadersGetheaders] a HttpRequestHeaders, [GetHeader][ReferenceWin3209430Icorewebview2httpresponseheadersGetheader] a HttpResponseHeaders y [get_HasCurrentHeader][ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader] propiedad a HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Cambio importante**: comportamiento de DevToolsProtocolEventReceived modificada.  Ahora, puedes crear un [DevToolsProtocolEventReceiver][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver] para un determinado evento de protocolo de DevTools y suscribirte o cancelar la suscripción a ese evento con [add_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived].
*   > [!IMPORTANT]
    > **Cambio destacado**: se ha cambiado el WebMessageReceivedEventArgs ' [get_WebMessageAsString][ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring] propiedad a un método [TryGetWebMessageAsString][ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring] .  
*   > [!IMPORTANT]
    > **Cambio importante**: se ha cambiado el método [Handle][ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle] de AcceleratorKeyPressedEventArgs ' a una propiedad [get_Handled][ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled] .  

## 0.8.355

[Paquete NuGet][NuGetGallery0.8.355] \ | versión mínima de Microsoft Edge 80.0.355.0.

*   Se ha publicado el ejemplo WebView2API, una guía completa del SDK de WebView2.  Para obtener más información, consulte [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Se ha agregado compatibilidad IME para todos los idiomas, además del inglés \ ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Se actualizó la superficie de API del evento WebResourceRequested en respuesta a informes de errores.  Especificar simultáneamente un filtro y un evento en la creación ahora está en desuso.  Para crear un evento solicitado de un recurso Web, use [add_WebResourceRequested][ReferenceWin3208190Iwebview2webview5AddWebresourcerequested] para agregar el evento y [AddWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter] para agregar un filtro.  [RemoveWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter] quita el filtro \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Cambio importante**: comportamiento de pantalla completa modificada.  [IsFullScreenAllowed][ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated]desusado.  Ahora, de forma predeterminada, si un elemento de un WebView \ (como un video \) se establece en pantalla completa, rellena los límites de la vista de página.  Usa el evento [ContainsFullScreenElementChanged][ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler] y [get_ContainsFullScreenElement][ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement] para especificar cómo la aplicación debe cambiar el tamaño de WebView si un elemento quiere entrar en modo de pantalla completa.  

## 0.8.314  

[Paquete NuGet][NuGetGallery0.8.314] \ | versión mínima de Microsoft Edge 80.0.314.0.  

*   Se ha agregado compatibilidad con Windows 7, Windows 8 y Windows 8,1.  
*   Se ha agregado compatibilidad de depuración de Visual Studio y Visual Studio para WebView2.  Ahora, depura tu script en el WebView2 directamente desde tu IDE.  Para obtener más información, vea [Cómo depurar al desarrollar con controles WebView2][HowtoDebug].  
*   `Native Object Injection`Se agregó, lo que permite que la secuencia de comandos que se ejecuta dentro de WebView2 tenga acceso a un objeto IDispatch desde el componente Win32 de la aplicación y obtenga acceso a las propiedades del objeto IDispatch.  Para obtener más información, consulta [AddRemoteObject][ReferenceWin3208190Iwebview2webview4Addremoteobject] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   `AcceleratorKeyPressed`Evento agregado.  Para obtener más información, consulte [add_AcceleratorKeyPressed][ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Deshabilitado `Context Menus` .  Para obtener más información, consulte [put_AreDefaultContextMenusEnabled][ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Actualizado `DPI Awareness` .  Ahora, el reconocimiento de PPP de WebView es el mismo que el reconocimiento de PPP de la aplicación host.  
    
    > [!NOTE] 
    > Si se inicia otra aplicación híbrida con un conocimiento de PPP diferente al de la vista de vista original, el nuevo WebView no se inicia si el directorio de datos de usuario es el mismo ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]).  
    
*   Se actualizó `Notification Change Behavior` para que WebView2 rechace automáticamente las solicitudes de permiso de notificaciones que el contenido web hospedado en la vista de Web.  

## 0.8.270  

[Paquete NuGet][NuGetGallery0.8.270] \ | versión mínima de Microsoft Edge 78.0.270.0.  

*   Se ha agregado un `DocumentTitleChanged` evento para indicar que el título del documento debe cambiar \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   API agregada `GetWebView2BrowserVersionInfo` \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   `NewWindowRequested`Evento agregado.  
*   `CreateWebView2EnvironmentWithDetails`Función actualizada para quitar `releaseChannelPreference` .  Para obtener más información, consulta la función [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails] .  El registro y la variable de entorno override aún se admiten.  La preferencia de canal predeterminada se usa a menos que se reemplace.  
    Durante la búsqueda de canales, el equipo de WebView omite cualquier versión de canal anterior que no sea compatible con el SDK de WebView2.  
    El equipo de WebView selecciona el canal más estable para asegurar los comportamientos más coherentes para el usuario final.  Cuando prueba con las últimas compilaciones Canarias, debe crear un script para establecer la `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` variable de entorno en `1` antes de iniciar la aplicación.  
*   Se actualizó la `CreateWebView2EnvironmentWithDetails` función con lógica para seleccionar `userDataFolder` cuando no se especifica.  Para obtener más información, consulta la función [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails] .  Si anteriormente usó la ubicación predeterminada `userDataFolder` , al cambiar al nuevo SDK el valor predeterminado `userDataFolder` es restablecer (establecido en una nueva ubicación en el directorio de código de host) y también se restablece su estado.  
    Si el proceso de hospedaje no tiene permiso de escritura en el directorio especificado, la `CreateWebView2EnvironmentWithDetails` función puede dar error.  Puede copiar los datos del directorio de datos de usuario anterior en el nuevo directorio.  

## 0.8.230  

[Paquete NuGet][NuGetGallery0.8.230] \ | versión mínima de Microsoft Edge 77.0.230.0.  

*   API agregada `Stop` para detener todas las búsquedas de recursos pendientes y navegación \ ([\ #28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Se agregó el archivo. tlb al paquete de Nuget \ ([\ #22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Se han agregado proyectos de .NET a la lista de instalador en el paquete NuGet \ ([\ #32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  

## 0.8.190  

[Paquete NuGet][NuGetGallery0.8.190] \ | versión mínima de Microsoft Edge 77.0.190.0.  

*   Se ha agregado `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` para controlar si los usuarios pueden abrir DevTools \ ([\ #16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` Se agregó al control si se muestra la barra de estado \ ([\ #19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Se ha agregado `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` para volver atrás y reenviarlo mediante el historial de navegación.  
*   Se han agregado tipos de encabezado HTTP ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` ) para ver y modificar los encabezados HTTP en WebView.  
*   Se ha agregado compatibilidad con WebView de 32-bit en máquinas de 64 bits \ ([\ #13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Se ha agregado el IDL de vista previa al SDK \ ([\ #14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Se agregó lib para admitir objetos de identificador de interfaz IID\_\ * \ ([\ #12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Se agregaron la ruta de inclusión, la vinculación y la copia automática de archivos DLL al archivo de destino NuGet en el SDK.  
*   Se ha habilitado la solicitud `window.open` de script.  

## 0.8.149  

[Paquete NuGet][NuGetGallery0.8.149] \ | versión mínima de Microsoft Edge 76.0.149.0.  

Versión inicial de Developer Preview.  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Modo de distribución de hoja perenne: distribución de aplicaciones mediante WebView2 | Microsoft docs"  
[ConceptsVersioning]: ./concepts/versioning.md "Descripción de las versiones de explorador y WebView2 | Microsoft docs"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "API experimentales: Descripción de las versiones de explorador y WebView2 | Microsoft docs"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Introducción a WebView2 en las aplicaciones de Windows Forms | Microsoft docs"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Introducción a WebView2 en WPF | Microsoft docs"  
[HowtoDebug]: ./howto/debug.md "Cómo depurar al desarrollar con controles WebView2 | Microsoft docs"  

[ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle]: ./reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle "Controlador-interfaz IWebView2AcceleratorKeyPressedEventArgs | Microsoft docs"  
[ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler]: ./reference/win32/0-8-190/iwebview2containsfullscreenelementchangedeventhandler.md "interfaz IWebView2ContainsFullScreenElementChangedEventHandler | Microsoft docs"  
[ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled]: ./reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled "interfaz de put_AreDefaultContextMenusEnabled IWebView2Settings2 | Microsoft docs"  
[ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated]: ./reference/win32/0-8-190/iwebview2settings.md#get_isfullscreenallowed_deprecated "interfaz de get_IsFullscreenAllowed_deprecated IWebView2Settings | Microsoft docs"  
[ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring]: ./reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring "interfaz de get_WebMessageAsString IWebView2WebMessageReceivedEventArgs | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed]: ./reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed "interfaz de add_AcceleratorKeyPressed IWebView2WebView4 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged]: ./reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged "interfaz de add_DocumentStateChanged IWebView2WebView | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview4Addremoteobject]: ./reference/win32/0-8-190/iwebview2webview4.md#addremoteobject "AddRemoteObject: IWebView2WebView4 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview5AddWebresourcerequested]: ./reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested "interfaz de add_WebResourceRequested IWebView2WebView5 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter]: ./reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter "AddWebResourceRequestedFilter: IWebView2WebView5 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement]: ./reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement "interfaz de get_ContainsFullScreenElement IWebView2WebView5 | Microsoft docs"  
[ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter]: ./reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter: IWebView2WebView5 | Microsoft docs"  
[ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails]:  ./reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-Globals | Microsoft docs"  

[ReferenceWin3209430Icorewebview2]: ./reference/win32/0-9-430/icorewebview2.md "interfaz ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled]: ./reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled "interfaz de get_Handled ICoreWebView2AcceleratorKeyPressedEventArgs | Microsoft docs"  
[ReferenceWin3209430Icorewebview2AddContentloading]: ./reference/win32/0-9-430/icorewebview2.md#add_contentloading "interfaz de add_ContentLoading ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2AddHistorychanged]: ./reference/win32/0-9-430/icorewebview2.md#add_historychanged "interfaz de add_HistoryChanged ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2Addremoteobject]: ./reference/win32/0-9-430/icorewebview2.md#addremoteobject "AddRemoteObject: ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2AddSourcechanged]: ./reference/win32/0-9-430/icorewebview2.md#add_sourcechanged "interfaz de add_SourceChanged ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2AddWindowcloserequested]: ./reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested "interfaz de add_WindowCloseRequested ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind]: ./reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind "Interfaz de CORE_WEBVIEW2_SCRIPT_DIALOG_KIND ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md "interfaz ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived "interfaz de add_DevToolsProtocolEventReceived ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived "interfaz de remove_DevToolsProtocolEventReceived ICoreWebView2DevToolsProtocolEventReceiver | Microsoft docs"  
[ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo]: ./reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo "interfaz de get_BrowserVersionInfo ICoreWebView2Environment | Microsoft docs"  
[ReferenceWin3209430Icorewebview2host]: ./reference/win32/0-9-430/icorewebview2host.md "interfaz ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo]: ./reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-Globals | Microsoft docs"  
[ReferenceWin3209430Icorewebview2hostGetZoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor "interfaz de get_ZoomFactor ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged]: ./reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged: ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Icorewebview2hostPutZoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor "interfaz de put_ZoomFactor ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor "SetBoundsAndZoomFactor: ICoreWebView2Host | Microsoft docs"  
[ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader]: ./reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader "interfaz de get_HasCurrentHeader ICoreWebView2HttpHeadersCollectionIterator | Microsoft docs"  
[ReferenceWin3209430Icorewebview2httprequestheadersGetheaders]: ./reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders "GetHeaders: ICoreWebView2HttpRequestHeaders | Microsoft docs"  
[ReferenceWin3209430Icorewebview2httpresponseheadersGetheader]: ./reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader "GetHeader-interfaz ICoreWebView2HttpResponseHeaders | Microsoft docs"  
[ReferenceWin3209430Icorewebview2Removeremoteobject]: ./reference/win32/0-9-430/icorewebview2.md#removeremoteobject "RemoveRemoteObject: ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed]: ./reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed "interfaz de get_AreRemoteObjectsAllowed ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled]: ./reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled "interfaz de get_IsZoomControlEnabled ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring]: ./reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring "TryGetWebMessageAsString: ICoreWebView2WebMessageReceivedEventArgs | Microsoft docs"  

[ReferenceWin3209488Icorewebview2AddFramenavigationcompleted]: ./reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted "interfaz de add_FrameNavigationCompleted ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209488Icorewebview2Addhostobjecttoscript]: ./reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript "AddHostObjectToScript: ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209488Icorewebview2AddNewwindowrequested]: ./reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested "interfaz de add_NewWindowRequested ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring]: ./reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring "| Microsoft docs"  
[ReferenceWin3209488Icorewebview2environmentoptions]: ./reference/win32/0-9-488/icorewebview2environmentoptions.md "interfaz ICoreWebView2EnvironmentOptions | Microsoft docs"  
[ReferenceWin3209488Icorewebview2experimentalcompositioncontroller]: ./reference/win32/0-9-488/icorewebview2experimentalcompositioncontroller.md "interfaz ICoreWebView2ExperimentalCompositionController | Microsoft docs"  
[ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler]: ./reference/win32/0-9-488/icorewebview2experimentalcursorchangedeventhandler.md "interfaz ICoreWebView2ExperimentalCursorChangedEventHandler | Microsoft docs"  
[ReferenceWin3209488Icorewebview2experimentalpointerinfo]: ./reference/win32/0-9-488/icorewebview2experimentalpointerinfo.md "interfaz ICoreWebView2ExperimentalPointerInfo | Microsoft docs"  
[ReferenceWin3209488Icorewebview2Removehostobjectfromscript]: ./reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript "RemoveHostObjectFromScript: ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed]: ./reference/win32/0-9-488/icorewebview2settings.md#get_areremoteobjectsallowed "interfaz de get_AreRemoteObjectsAllowed ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled]: ./reference/win32/0-9-488/icorewebview2settings.md#get_isbuiltinerrorpageenabled "| Microsoft docs"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails]: ./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-Globals | Microsoft docs"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  
[ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring]: ./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Microsoft docs"  

[ReferenceDotnet09515Reference]: ./reference/dotnet/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWinforms09515Reference]: ./reference/winforms/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  
[ReferenceWpf09515Reference]: ./reference/wpf/0-9-515-reference-webview2.md "Referencia (WebView2) | Microsoft docs"  

[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environment]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md "Clase Microsoft. Web. WebView2. Core. CoreWebView2Environment | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#comparebrowserversions "CompareBrowserVersions-Microsoft. Web. WebView2. Core. CoreWebView2Environment (clase) | Microsoft docs"
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#getavailablebrowserversionstring "GetAvailableBrowserVersionString-Microsoft. Web. WebView2. Core. CoreWebView2Environment (clase) | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#newwindowrequested "NewWindowRequested-Microsoft. Web. WebView2. Core. CoreWebView2 (clase) | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Permissionrequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#permissionrequested "PermissionRequested-Microsoft. Web. WebView2. Core. CoreWebView2 (clase) | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#scriptdialogopening "ScriptDialogOpening-Microsoft. Web. WebView2. Core. CoreWebView2 (clase) | Microsoft docs"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#webresourcerequested "WebResourceRequested-Microsoft. Web. WebView2. Core. CoreWebView2 (clase) | Microsoft docs"  
[ReferenceWin3209538Icorewebview2Addhostobjecttoscript]: ./reference/win32/0-9-538/icorewebview2.md#addhostobjecttoscript "AddHostObjectToScript: ICoreWebView2 | Microsoft docs"  
[ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures]: ./reference/win32/0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md#get_windowfeatures "interfaz de get_WindowFeatures ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Microsoft docs"  
[ReferenceWin3209538Icorewebview2experimentalwindowfeatures]: ./reference/win32/0-9-538/icorewebview2experimentalwindowfeatures.md "interfaz ICoreWebView2ExperimentalWindowFeatures | Microsoft docs"  
[ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed]: ./reference/win32/0-9-538/icorewebview2settings.md#get_arehostobjectsallowed "interfaz de get_AreHostObjectsAllowed ICoreWebView2Settings | Microsoft docs"  
[ReferenceWin3209538Webview2IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-538/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Microsoft docs"  

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
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 179"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "Ejemplos de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Mover Project para usar el SDK más reciente de WebView2 0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample "Ejemplo de API de WebView2: MicrosoftEdge/WebView2Samples | GitHub"  

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
