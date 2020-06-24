---
description: Hospedar contenido web en la aplicación Win32 con el control de WebView 2 de Microsoft Edge
title: Notas de la versión de Microsoft Edge WebView2 para Win32, WPF y WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 68a32b8e7175f2e52960e7c3a7fe16b66e5a043d
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757616"
---
# Notas de la versión para el SDK de WebView2  

El equipo de WebView2 enviará actualizaciones para el [SDK de WebView2][WebView2NuGetGallery] en una cadencia de 6 semanas. Esta página le mantendrá al día con: anuncios de productos, adiciones y modificaciones a la superficie de la API y cambios importantes.

> [!NOTE]
> Vuelve a compilar la aplicación después de actualizar el paquete de NuGet.

> [!IMPORTANT]
> Mientras WebView2 está en versión preliminar, las API de .NET estarán en el **paquete anterior al lanzamiento**.

## 0.9.538

[Paquete NuGet][WebView2NuGetGallery0.9.538] | versión mínima de Microsoft Edge 85.0.538.0.

#### General

* Compatibilidad con la versión de SDK [0.8.149](#08149). Te recomendamos estar al día con la última versión de WebView2.
* Directiva de grupo actualizada que se debe tener en cuenta cuando se modifica la ruta de acceso del perfil del explorador Microsoft Edge ([#179](https://github.com/MicrosoftEdge/WebViewFeedback/issues/179))

#### C/C++ Win32

* Se ha agregado [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures](reference/win32/0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md#get_windowfeatures) que se desencadena cuando se llama a Window. Open () y se asocia [ICoreWebView2ExperimentalWindowFeatures](reference/win32/0-9-538/icorewebview2experimentalwindowfeatures.md). ([#70](https://github.com/MicrosoftEdge/WebViewFeedback/issues/70))
* **Cambio importante:** [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) se ha dejado de usar y se ha reemplazado por [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-538/webview2-idl.md#createcorewebview2environmentwithoptions)
* **Cambio importante:** Para asegurarnos de que nuestra API se alinee con las convenciones de nomenclatura de la API de Windows, hemos actualizado los nombres de los siguientes:
  * [AreRemoteObjectsAllowed](reference/win32/0-9-488/icorewebview2settings.md#get_areremoteobjectsallowed) es ahora [AreHostObjectsAllowed](reference/win32/0-9-538/icorewebview2settings.md#get_arehostobjectsallowed)
* [AddHostObjectToScript](reference/win32/0-9-538/icorewebview2.md#addhostobjecttoscript) actualizado para garantizar que los marcadores de serializador de objeto de host original se establezcan en los objetos proxy y se serialicen como un objeto de host cuando se pasan como un parámetro en la devolución de llamada de JavaScript. ([#148](https://github.com/MicrosoftEdge/WebViewFeedback/issues/148))

#### .NET (versión preliminar de 0.9.538)

* Se han publicado ejemplos de WinForms y WPF WebView2API, que son guías completas de nuestro SDK. Consulta el [repositorio de ejemplos de WebView2](https://github.com/MicrosoftEdge/WebView2Samples).
* Se ha agregado compatibilidad con las [API experimentales](./concepts/versioning.md#experimental-apis) de hospedaje visual y características de la ventana
* **Cambio importante:** Las siguientes aplazaciones ahora implementan IDisposable: [ScriptDialogOpening](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#scriptdialogopening), [NewWindowRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#newwindowrequested), [WebResourceRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#webresourcerequested)y [PermissionRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#permissionrequested).
* Se han agregado [GetAvailableBrowserVersionString](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#getavailablebrowserversionstring) y [CompareBrowserVersions](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#comparebrowserversions) como estáticas de [CoreWebView2Environment](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md) .

## 0.9.515-versión preliminar

[Paquete NuGet][WebView2NuGetGallery0.9.515-prerelease] | versión mínima de Microsoft Edge 84.0.515.0.

* **Anuncio:** WebView2 ahora es compatible con Windows Forms y WPF en .NET Framework 4.6.2 o versiones posteriores, .NET Core 3,0 o una versión posterior en el **paquete preliminar**
* Desproteja la [Guía de introducción a WPF](./gettingstarted/wpf.md) para empezar a crear aplicaciones WPF y nuestra referencia de [WPF](./reference/wpf/0-9-515-reference-webview2.md) para API específicas de WPF
* Desproteja la [Guía de introducción a Windows Forms](./gettingstarted/winforms.md) para empezar a crear aplicaciones de Windows Forms y la [referencia de Windows Forms](./reference/winforms/0-9-515-reference-webview2.md) para las API específicas de Windows Forms
* Desproteger la [referencia de .net](./reference/dotnet/0-9-515-reference-webview2.md) para las API de CoreWebView2
* **Problemas conocidos:** Sabemos que algunos problemas de esta versión preliminar se resolverán en versiones futuras.
  * **Reconocimiento de PPP:** WebView2 para WPF actualmente no reconoce los ppp. Al inicializar WebView2 en monitores con alta resolución de PPP, existe un problema conocido en el que WebView se inicializa en primer lugar como una fracción de la ventana hasta que se cambia el tamaño de la ventana.
  * **Diseñador de WPF:** Esta versión no es compatible actualmente con el diseñador de WPF. Coloca el control WebView2 en tu aplicación modificando directamente el XAML correspondiente en un editor de texto

## 0.9.488

[Paquete NuGet][WebView2NuGetGallery0.9.488] | versión mínima de Microsoft Edge 84.0.488.0.

* **Anuncio:** A partir de la próxima versión 83 de Microsoft Edge, la vista previa de perenne ya no se destina al canal de explorador estable. En su lugar, se dirige a otro conjunto de binarios, con marca [Microsoft Edge WebView2 Runtime](./concepts/distribution.md#microsoft-edge-webview2-runtime), que se puede instalar en cadena mediante un instalador que estamos desarrollando actualmente. Más información en [la distribución de la aplicación](./concepts/distribution.md).
* **Anuncio:** En el futuro, publicaremos dos paquetes: un paquete preliminar con las API experimentales (para que lo pruebes) y un paquete de versión estable con API estables (puede depender). Desproteja [Microsoft Edge WEBVIEW2 SDK](./concepts/versioning.md) para obtener más información sobre las diferencias.
* **Cambio importante:** Para asegurarnos de que nuestra API se alinee con las convenciones de nomenclatura de la API de Windows, hemos actualizado los nombres de las siguientes interfaces:
  * El prefijo CORE_WEBVIEW2_ * ahora está COREWEBVIEW2_ *.
  * [GetCoreWebView2BrowserVersionInfo](reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo) es ahora [GetAvailableCoreWebView2BrowserVersionString](reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring)
  * [get_BrowserVersionInfo](reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo) está ahora [get_BrowserVersionString](reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring)
  * [AddRemoteObject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) es ahora [AddHostObjectToScript](reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript)
  * [RemoveRemoteObject](reference/win32/0-9-430/icorewebview2.md#removeremoteobject) es ahora [RemoveHostObjectFromScript](reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript)
  * Chrome. Webview. remoteObjects es ahora Chrome. Webview. hostObjects
* **Cambio importante:** También se cambió el nombre de los métodos de proxy de AddRemoteObject JS.
  * getLocal es ahora getLocalProperty
  * setLocal es ahora setLocalProperty
  * getRemote es ahora getHostProperty
  * setRemote es ahora setHostProperty
  * applyRemote es ahora applyHostFunction
* **Cambio importante:** [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) está obsoleto y ha sido reemplazado por [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).  
* Se agregó el evento [FrameNavigationCompleted](reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted) . Ahora, cuando un iframe completa la navegación, se desencadena un evento y devuelve el éxito de la navegación y el identificador de navegación.
* Se agregó la interfaz de [ICoreWebView2EnvironmentOptions](reference/win32/0-9-488/ICoreWebView2EnvironmentOptions.md) , que se puede usar para determinar la versión del tiempo de ejecución de WebView2 de destino de la aplicación.
* Se agregó la configuración [IsBuiltInErrorPageEnabled](reference/win32/0-9-488/ICoreWebView2Settings.md#get_isbuiltinerrorpageenabled) . Ahora, puede habilitar o deshabilitar la página de error integrada para error de navegación y error de proceso de representación.
* Se ha actualizado la inyección de objetos remotos para admitir implementaciones de .NET IDispatch. ([#113](https://github.com/MicrosoftEdge/WebViewFeedback/issues/113))
* Evento [NewWindowRequested](reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested) actualizado para administrar solicitudes de menús contextuales. ([#108](https://github.com/MicrosoftEdge/WebViewFeedback/issues/108))
* Publicó nuestro primer paquete de versión preliminar en el que puedes acceder a las API de hospedaje de visual. Hemos actualizado [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) para incluir estas nuevas API experimentales.
  * Se ha agregado la interfaz de [ICoreWebView2ExperimentalCompositionController](reference/win32/0-9-488/ICoreWebView2ExperimentalCompositionController.md) , que se usa para conectarse a un árbol de composición y proporcionar una entrada para la vista.
  * Se ha agregado [ICoreWebView2ExperimentalPointerInfo](reference/win32/0-9-488/ICoreWebView2ExperimentalPointerInfo.md) que contiene toda la información de un POINTER_INFO. Se pasa a SendPointerInput para inyectar la entrada del puntero en la vista de vista en WebView.
  * Se ha agregado un [ICoreWebView2ExperimentalCursorChangedEventHandler](reference/win32/0-9-488/ICoreWebView2ExperimentalCursorChangedEventHandler.md) que indica a la aplicación Cuándo se debe cambiar el cursor del mouse sobre la vista. Cuando el mouse está sobre un cuadro de texto en la vista de vistas en WebView, el cursor cambia de la flecha al selector. La propiedad cursor en el CompositionController indica a la aplicación lo que debe hacer actualmente el cursor del mouse para la vista en WebView.

## 0.9.430

[Paquete NuGet][WebView2NuGetGallery0.9.430] | versión mínima de Microsoft Edge 82.0.430.0.

Este SDK es nuestra versión oficial de Win32 C++ beta, que incorpora varias solicitudes de características que hemos recibido. Hemos intentado limitar el número de versiones con cambios importantes, pero a medida que nos encontramos en la disponibilidad general, estamos usando nuestra versión beta para incorporar varios cambios importantes de una sola vez.

* **Cambio importante:**  A medida que nos acercamos a la versión final, hemos cambiado el nombre de la *IWebView2WebView* de prefijo a *ICoreWebView2* para asegurarnos de que nuestra API se alinee con la Convención de nomenclatura de la API de Windows. Además, para que nuestro SDK pueda ser usado por los marcos de la interfaz de usuario, hemos separado ICoreWebView2 a [ICoreWebView2](reference/win32/0-9-430/icorewebview2.md) y [ICoreWebView2Host](reference/win32/0-9-430/icorewebview2host.md). ICoreWebView2Host admite cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición. ICoreWebView2 admite todas las demás funcionalidades de WebView2. Para obtener más información sobre cómo incorporar estos cambios, desproteja nuestra [solicitud de incorporación](https://github.com/MicrosoftEdge/WebView2Samples/pull/17) de cambios en nuestro proyecto [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) .
* **Cambio importante:** Divida [DocumentStateChanged](reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged) en tres componentes: [SourceChanged](reference/win32/0-9-430/icorewebview2.md#add_sourcechanged), [ContentLoading](reference/win32/0-9-430/icorewebview2.md#add_contentloading)y [HistoryChanged](reference/win32/0-9-430/icorewebview2.md#add_historychanged). Ahora, cuando se cambia la dirección URL de origen, se desencadena el evento SourceChanged. Cuando se cambia el estado del historial, se desencadena el evento HistoryChanged. El evento ContentLoading se desencadena antes del script inicial cuando se carga un documento nuevo.
* Se ha agregado compatibilidad con la arquitectura de ARM64
* Se ha agregado compatibilidad con el panel de entrada de software (SIP) para dispositivos con pantalla táctil
* Se ha agregado soporte técnico para `Windows Server 2008 R2` , `Windows Server 2012/2012 R2` y `Windows Server 2016`
* Se ha agregado [NotifyParentWindowPositionChanged](reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged) que permite que la barra de estado siga la ventana en el modo de ventana. También será necesario implementarlo en el modo sin ventana para que funcionen las características de accesibilidad.
* Se ha agregado la configuración [AreRemoteObjectsAllowed](reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed) para controlar globalmente si un objeto remoto puede acceder a una página. De forma predeterminada, AreRemoteObjectsAllowed está habilitado, lo que significa que los objetos remotos agregados por [AddRemoteObject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) son accesibles desde la página. Cuando AreRemoteObjectsAllowed está deshabilitado, no se podrá acceder a los objetos desde la página. Los cambios se aplicarán en el siguiente evento de navegación.
* Se ha agregado una configuración de [IsZoomControlEnabled](reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled) para evitar que los usuarios afecten al zoom de la vista en WebView con `ctrl`  +  `+` / `-` o `ctrl` + del mouse. El zoom aún puede establecerse a través de [put_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor) cuando esta configuración está deshabilitada.  
* Se ha cambiado el ZoomFactor para que solo se aplique a la vista en WebView actual. Los cambios de zoom en la vista Web actual no afectan a otras vistas de web que se encuentren en el mismo sitio de origen. Para obtener más información, consulta [get_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor) .
* Interfaz de usuario de ZoomView HID para WebView. ([#95](https://github.com/MicrosoftEdge/WebViewFeedback/issues/95))
* Se ha agregado [SetBoundsAndZoomFactor](reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor). Ahora, puede establecer el factor de zoom y los límites de un WebView al mismo tiempo.
* Se agregó el evento [WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) . Para obtener más información, consulta [add_WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) . ([#119](https://github.com/MicrosoftEdge/WebViewFeedback/issues/119))
* Se ha agregado compatibilidad con el tipo de cuadro de diálogo beforeunload para eventos de cuadros de diálogo de JavaScript y se agrega [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD](reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind) entrada de enumeración.
* Se ha agregado [GetHeaders](reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders) a HttpRequestHeaders, [GetHeader](reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader) a HttpResponseHeaders y [get_HasCurrentHeader](reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader) propiedad a HttpHeadersCollectionIterator.
* **Cambio importante:** Comportamiento de DevToolsProtocolEventReceived modificada. Ahora, puede crear un [DevToolsProtocolEventReceiver](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md) para un evento de protocolo de DevTools determinado y suscribirse o cancelar la suscripción a dicho evento mediante [add_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived) / [remove_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived).
* **Cambio importante:** Se ha cambiado la propiedad ' [get_WebMessageAsString](reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring) ' de WebMessageReceivedEventArgs a un método [TryGetWebMessageAsString](reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring) .
* **Cambio importante:** Se ha cambiado el método [Handle](reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle) de AcceleratorKeyPressedEventArgs ' a una propiedad [get_Handled](reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled) .

## 0.8.355

[Paquete NuGet][WebView2NuGetGallery0.8.355] | versión mínima de Microsoft Edge 80.0.355.0.

* Ejemplo WebView2API: una guía completa de nuestro SDK. ¡ Consultarlo [aquí](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample)!
* Se ha agregado compatibilidad IME para todos los idiomas, además del inglés. ([#30](https://github.com/MicrosoftEdge/WebViewFeedback/issues/30))
* Se actualizó la superficie de API del evento WebResourceRequested en respuesta a informes de errores.  Especificar simultáneamente un filtro y un evento en la creación ahora está en desuso.  Para crear un evento solicitado de un recurso Web, use [add_WebResourceRequested](reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested) para agregar el evento y [AddWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter) para agregar un filtro.  [RemoveWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter) elimina el filtro.  ([#36](https://github.com/MicrosoftEdge/WebViewFeedback/issues/36)) ([#74](https://github.com/MicrosoftEdge/WebViewFeedback/issues/74))  
* **Cambio importante:**  Comportamiento de pantalla completa modificada. [IsFullScreenAllowed](reference/win32/0-8-190/IWebView2Settings.md#get_isfullscreenallowed_deprecated)desusado.  Ahora, de forma predeterminada, si un elemento de un WebView (como un vídeo) se establece en pantalla completa, rellenará los límites de la vista de página.  Usa el evento [ContainsFullScreenElementChanged](reference/win32/0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md#interface-iwebview2containsfullscreenelementchangedeventhandler) y [get_ContainsFullScreenElement](reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement) para especificar cómo la aplicación debe cambiar el tamaño de WebView si un elemento quiere entrar en modo de pantalla completa.  

## 0.8.314

[Paquete NuGet][WebView2NuGetGallery0.8.314] | versión mínima de Microsoft Edge 80.0.314.0.

* Se ha agregado compatibilidad con Windows 7, Windows 8/8.1.
* Se ha agregado compatibilidad de depuración de Visual Studio y Visual Studio para WebView2. Ahora, puedes depurar tu script en el WebView2 directamente desde tu IDE. Haz clic [aquí](/microsoft-edge/hosting/webview2#debugging-webview2) para obtener más información.  
* Se ha agregado `Native Object Injection` , lo que permite que el script que se ejecuta dentro de WebView2 se pase un objeto IDispatch desde el componente Win32 de la aplicación y obtenga acceso a las propiedades del objeto IDispatch.  Para obtener más información, consulta [AddRemoteObject](reference/win32/0-8-190/iwebview2webview4.md#addremoteobject) .  ([#17](https://github.com/MicrosoftEdge/WebViewFeedback/issues/17)).  
* `AcceleratorKeyPressed`Evento agregado.  Para obtener más información, consulta [add_AcceleratorKeyPressed](reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed) .  ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)).  
* Deshabilitado `Context Menus` .  Para obtener más información ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)), consulte [put_AreDefaultContextMenusEnabled](reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled) .  
* Actualizado `DPI Awareness` . Ahora, el reconocimiento de PPP de la vista de la WebView será el mismo que el reconocimiento de PPP de la aplicación host. Nota: si se inicia otra aplicación híbrida con un conocimiento de PPP diferente al de la vista de vista original, la nueva vista de WebView no se iniciará si el directorio de datos del usuario es el mismo ([#1](https://github.com/MicrosoftEdge/WebViewFeedback/issues/1)).
* Se actualizó `Notification Change Behavior` para que WebView2 rechace automáticamente las solicitudes de permiso de notificaciones que el contenido web hospedado en la vista de Web.

## 0.8.270  

[Paquete NuGet][WebView2NuGetGallery0.8.270] | versión mínima de Microsoft Edge 78.0.270.0.  

* Se ha agregado un `DocumentTitleChanged` evento para indicar que el título del documento debe cambiar \ ([\ #27][MicrosoftEdgeWebViewFeedbackIssue27]\).  
* API agregada `GetWebView2BrowserVersionInfo` \ ([\ #18][MicrosoftEdgeWebViewFeedbackIssue18]\).  
* `NewWindowRequested`Evento agregado.  
* `CreateWebView2EnvironmentWithDetails`Función actualizada para quitar `releaseChannelPreference` .  Para obtener más información, consulta la función [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] .  El registro y la variable de entorno override aún se admiten.  La preferencia de canal predeterminada se usa a menos que se reemplace.  
    Durante la búsqueda de canales, omitiremos cualquier versión de canal anterior que no sea compatible con el SDK de WebView2.  
    Seleccionamos el canal más estable para asegurar los comportamientos más uniformes para el usuario final.  Cuando prueba con las últimas compilaciones Canarias, debe crear un script para establecer `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` la variable de entorno en antes de `1` iniciar la aplicación.  
* Función updateed `CreateWebView2EnvironmentWithDetails` con lógica para seleccionar `userDataFolder` cuando no se especifica.  Para obtener más información, consulta la función [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] .  Si anteriormente usó la ubicación predeterminada `userDataFolder` , al cambiar al nuevo SDK el valor predeterminado `userDataFolder` es restablecer (establecido en una nueva ubicación en el directorio de código de host) y también se restablece su estado.  
    Si el proceso de hospedaje no tiene permiso para escribir en el directorio especificado, `CreateWebView2EnvironmentWithDetails` puede dar error.  Puede copiar los datos del directorio de datos de usuario anterior en el nuevo directorio.  

## 0.8.230  

[Paquete NuGet][WebView2NuGetGallery0.8.230] | versión mínima de Microsoft Edge 77.0.230.0.  

* API agregada `Stop` para detener todas las búsquedas de recursos pendientes y navegación \ ([\ #28][MicrosoftEdgeWebViewFeedbackIssue28]\).  
* Se agregó el archivo. tlb al paquete de Nuget \ ([\ #22][MicrosoftEdgeWebViewFeedbackIssue22]\).  
* Se han agregado proyectos de .NET a la lista de instalador en el paquete NuGet \ ([\ #32][MicrosoftEdgeWebViewFeedbackIssue32]\).  

## 0.8.190  

[Paquete NuGet][WebView2NuGetGallery0.8.190] | versión mínima de Microsoft Edge 77.0.190.0.  

* Se ha agregado `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` para controlar si los usuarios pueden abrir DevTools \ ([\ #16][MicrosoftEdgeWebViewFeedbackIssue16]\).  
* `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` Se agregó al control si se muestra la barra de estado \ ([\ #19][MicrosoftEdgeWebViewFeedbackIssue19]\).  
* Se ha agregado `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` para volver atrás y reenviarlo mediante el historial de navegación.  
* Se han agregado tipos de encabezado HTTP ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` ) para ver y modificar los encabezados HTTP en WebView.  
* Se ha agregado compatibilidad con WebView de 32-bit en máquinas de 64 bits \ ([\ #13][MicrosoftEdgeWebViewFeedbackIssue13]\).  
* Se ha agregado el IDL de vista previa al SDK \ ([\ #14][MicrosoftEdgeWebViewFeedbackIssue14]\).  
* Se agregó lib para admitir objetos de identificador de interfaz IID\_\ * \ ([\ #12][MicrosoftEdgeWebViewFeedbackIssue12]\).  
* Se agregaron la ruta de inclusión, la vinculación y la copia automática de archivos DLL al archivo de destino NuGet en el SDK.  
* Se ha habilitado la solicitud `window.open` de script.  

## 0.8.149  

[Paquete NuGet][WebView2NuGetGallery0.8.149] | versión mínima de Microsoft Edge 76.0.149.0.  

Versión inicial de Developer Preview.  

<!-- image links -->

<!-- Links -->
[MicrosoftEdgeWebViewFeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 12"  
[MicrosoftEdgeWebViewFeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 13"  
[MicrosoftEdgeWebViewFeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 14"  
[MicrosoftEdgeWebViewFeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 16"  
[MicrosoftEdgeWebViewFeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback (problema 18)"  
[MicrosoftEdgeWebViewFeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 19"  
[MicrosoftEdgeWebViewFeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 22"  
[MicrosoftEdgeWebViewFeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Repositorio de comentarios para el problema 27 de MicrosoftEdge/WebViewFeedback"  
[MicrosoftEdgeWebViewFeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "Repositorio de comentarios para MicrosoftEdge/WebViewFeedback, problema 28"  
[MicrosoftEdgeWebViewFeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Repositorio de comentarios para el problema de MicrosoftEdge/WebViewFeedback 32"  

[WebView2NuGetGallery]: https://aka.ms/webviewnuget "Galería de NuGet | Microsoft. Web. WebView2"  
[WebView2NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[WebView2NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[WebView2NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[WebView2NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[WebView2NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[WebView2NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Galería de NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[WebView2NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Galería de NuGet | Microsoft. Web. WebView2 v 0.9.430"
[WebView2NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Galería de NuGet | Microsoft. Web. WebView2 v 0.9.488"
[WebView2NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Galería de NuGet | Versión preliminar de Microsoft. Web. WebView2 v 0.9.515"
[WebView2NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Galería de NuGet | Microsoft. Web. WebView2 v 0.9.538"

[WebViewsGlobalsCreateWebView2EnvironmentWithDetails]: reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "GLOBALS de vista global: función CreateWebView2EnvironmentWithDetails"  
