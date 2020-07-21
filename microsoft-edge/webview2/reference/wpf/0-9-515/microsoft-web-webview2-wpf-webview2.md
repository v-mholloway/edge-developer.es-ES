---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WPF. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/17/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, App, Edge, CoreWebView2, CoreWebView2Controller, control de explorador, Edge HTML, Microsoft. Web. WebView2. WPF. WebView2
ms.openlocfilehash: e7f5d11b540d1d7ad9630aa674ef5bc0073195c2
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885299"
---
# Clase Microsoft. Web. WebView2. WPF. WebView2 

Espacio de nombres: Microsoft. Web. WebView2. WPF \
Ensamblado: Microsoft.Web.WebView2.Wpf.dll

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

Un control para incrustar contenido web en una aplicación de WPF.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | Un contenedor para el evento CoreWebView2. ContentLoading de CoreWebView2.
[CoreWebView2Ready](#corewebview2ready) | Este evento se desencadena cuando se ha terminado de inicializar el CoreWebView2 del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.
[NavigationCompleted](#navigationcompleted) | Un contenedor para el evento CoreWebView2. NavigationCompleted de CoreWebView2.
[NavigationStarting](#navigationstarting) | Un contenedor para el evento CoreWebView2. NavigationStarting de CoreWebView2.
[SourceChanged](#sourcechanged) | Un contenedor para el evento CoreWebView2. SourceChanged de CoreWebView2.
[WebMessageReceived](#webmessagereceived) | Un contenedor para el evento CoreWebView2. WebMessageReceived de CoreWebView2.
[ZoomFactorChanged](#zoomfactorchanged) | El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa.
[CanGoBack](#cangoback) | Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.
[CanGoForward](#cangoforward) | Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.
[CoreWebView2](#corewebview2) | Accede a la funcionalidad completa de la API básica. CoreWebView2 COM.
[CreationProperties](#creationproperties) | Obtiene o establece una bolsa de opciones que se usan durante la inicialización de la CoreWebView2 del control.
[Source](#source) | Identificador URI de nivel superior que la vista en pantalla está mostrando (o se muestra cuando finaliza la inicialización de su CoreWebView2).
[ZoomFactor](#zoomfactor) | El factor de zoom para la vista de WebView.
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Desencadenar de forma explícita la inicialización de la CoreWebView2 del control.
[ExecuteScriptAsync](#executescriptasync) | Ejecuta el código de JavaScript desde el parámetro de javaScript en el documento de nivel superior actual representado en la vista de gráfico.
[GoBack](#goback) | Navega por la vista Web a la página anterior del historial de navegación.
[GoForward](#goforward) | Navega por la vista Web a la página siguiente del historial de navegación.
[NavigateToString](#navigatetostring) | Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.
[Volver a cargar](#reload) | Vuelve a cargar la página actual.
[Detener](#stop) | Detiene todas las navegaciones y las búsquedas de recursos pendientes.
[WebView2](#webview2) | Crea una nueva instancia de un control WebView2.

Este control es realmente un contenedor de la API COM de WebView2, en el que puede encontrar documentación aquí: [https://aka.ms/webview2](https://aka.ms/webview2) puede acceder directamente a la interfaz de ICoreWebView2 subyacente y a toda su funcionalidad mediante el acceso a la propiedad CoreWebView2. Algunas de las funciones COM más comunes también son accesibles directamente a través de métodos de contenedor/propiedades o eventos del control.

Una vez creada, la propiedad CoreWebView2 del control será null. Esto se debe a que la creación de CoreWebView2 es una operación costosa que implica cosas como iniciar procesos de explorador Edge. Hay dos maneras de crear el CoreWebView2:1) llama al método EnsureCoreWebView2Async. Esto se conoce como inicialización explícita. 2) establezca la propiedad Source (que puede realizarse desde el marcado, por ejemplo). Esto se conoce como inicialización implícita. Ambas opciones iniciarán la inicialización en segundo plano y regresarán a la persona que llama sin esperar a que finalice. Para especificar las opciones relacionadas con el proceso de inicialización, pase su propio CoreWebView2Environment a EnsureCoreWebView2Async o establezca la propiedad CreationProperties del control antes de la inicialización.

Cuando la inicialización ha finalizado (independientemente de cómo se haya activado), se iniciarán las siguientes acciones, en este orden: 1) se invocará el evento CoreWebView2Ready del control. Si necesita realizar operaciones de configuración una vez en el CoreWebView2 antes de su uso, debe hacerlo en un controlador para ese evento. 2) si un URI se ha establecido en la propiedad de origen, el control comenzará a navegar en él en segundo plano (es decir, los pasos continuarán sin esperar a que finalice la navegación). 3) la tarea devuelta de EnsureCoreWebView2Async se completará.

Para obtener más información sobre cualquiera de los métodos, propiedades o eventos implicados en el proceso de inicialización, consulte su documentación específica.

Debido a que el CoreWebView2 del control es un objeto muy pesado (posiblemente responsable de varios procesos en ejecución y megabytes de espacio en disco), el control implementa IDisposable para proporcionar un medio explícito para liberarlo. Al llamar a Dispose, se liberará el CoreWebView2 y sus recursos subyacentes (excepto los que también usan otras webviews), y se restablecerá CoreWebView2 a NULL. Una vez que se haya llamado a Dispose, CoreWebView2 no se podrá reinicializar y cualquier intento de usar la funcionalidad que lo requiera iniciará una ObjectDisposedException.

Tenga en cuenta que este control extiende HwndHost para insertar Windows que reside fuera del ecosistema de WPF. Esto tiene algunas implicaciones en relación con el comportamiento de entrada y salida del control, así como con la funcionalidad que "hereda" de UIElement y FrameworkElement. Para obtener más información, consulta la documentación de interoperabilidad de HwndHost y WPF/Win32:

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## Miembros

#### ContentLoading 

Un contenedor para el evento CoreWebView2. ContentLoading de CoreWebView2.

> evento público EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

La única diferencia entre este evento y CoreWebView2. ContentLoading es el primer parámetro que se pasa a los controladores. Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. ContentLoading recibirán la instancia de CoreWebView2.

#### CoreWebView2Ready 

Este evento se desencadena cuando se ha terminado de inicializar el CoreWebView2 del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.

> evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Debe controlar este evento si necesita realizar operaciones de configuración una vez en el CoreWebView2 el que desea afectar a todos sus usos (por ejemplo, agregar controladores de eventos, configurar valores, instalar scripts de creación de documentos, agregar objetos host). Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.

Este evento no proporciona ningún argumento, y el remitente será el control WebView2, cuya propiedad CoreWebView2 será válida (es decir, no NULL) por primera vez.

#### NavigationCompleted 

Un contenedor para el evento CoreWebView2. NavigationCompleted de CoreWebView2.

> evento público EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

La única diferencia entre este evento y CoreWebView2. NavigationCompleted es el primer parámetro que se pasa a los controladores. Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. NavigationCompleted recibirán la instancia de CoreWebView2.

#### NavigationStarting 

Un contenedor para el evento CoreWebView2. NavigationStarting de CoreWebView2.

> evento público EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

La única diferencia entre este evento y CoreWebView2. NavigationStarting es el primer parámetro que se pasa a los controladores. Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. NavigationStarting recibirán la instancia de CoreWebView2.

#### SourceChanged 

Un contenedor para el evento CoreWebView2. SourceChanged de CoreWebView2.

> evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)

La única diferencia entre este evento y CoreWebView2. SourceChanged es el primer parámetro que se pasa a los controladores. Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. SourceChanged recibirán la instancia de CoreWebView2.

#### WebMessageReceived 

Un contenedor para el evento CoreWebView2. WebMessageReceived de CoreWebView2.

> evento público EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

La única diferencia entre este evento y CoreWebView2. WebMessageReceived es el primer parámetro que se pasa a los controladores. Los controladores de este evento recibirán el control WebView2, mientras que los controladores de CoreWebView2. WebMessageReceived recibirán la instancia de CoreWebView2.

#### ZoomFactorChanged 

El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa.

> evento público EventHandler< EventArgs > [ZoomFactorChanged](#zoomfactorchanged)

Este evento expone directamente CoreWebView2Controller. ZoomFactorChanged, consulta su documentación para obtener más información.

#### CanGoBack 

Devuelve verdadero si la vista en web puede navegar a una página anterior en el historial de navegación.

> Public bool [CanGoBack](#cangoback)

Contenedor de la propiedad CoreWebView2. CanGoBack de CoreWebView2. Si CoreWebView2 aún no se ha inicializado, devolverá FALSE.

#### CanGoForward 

Devuelve true si la vista Web puede navegar a la página siguiente del historial de navegación.

> Public bool [CanGoForward](#cangoforward)

Contenedor de la propiedad CoreWebView2. CanGoForward de CoreWebView2. Si CoreWebView2 aún no se ha inicializado, devolverá FALSE.

#### CoreWebView2 

Accede a la funcionalidad completa de la API básica. CoreWebView2 COM.

> CoreWebView2 pública [CoreWebView2](#corewebview2)

Devuelve null hasta que se haya completado la inicialización. Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.

##### Excepciones
* `InvalidOperationException` Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario). Para obtener más información, consulta DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Se produce si ya se ha llamado a Dispose en el control.

#### CreationProperties 

Obtiene o establece una bolsa de opciones que se usan durante la inicialización de la CoreWebView2 del control.

> CoreWebView2CreationProperties pública [CreationProperties](#creationproperties)

El establecimiento de esta propiedad no funcionará después de que se haya iniciado la inicialización de la CoreWebView2 del control (se conservará el valor anterior). Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.

#### Source 

Identificador URI de nivel superior que la vista en pantalla está mostrando (o se muestra cuando finaliza la inicialización de su CoreWebView2).

> [origen](#source) de URI público

En general, la obtención de esta propiedad es equivalente a obtener la propiedad CoreWebView2. Source de CoreWebView2 y establecer esta propiedad (a un valor diferente) es equivalente a llamar al método CoreWebView2. Navigate en CoreWebView2. Un valor de NULL tiene el mismo significado que "About: Blank" (vea la sección Comentarios para obtener más información). Si se obtiene esta propiedad antes de que se haya inicializado CoreWebView2, se recuperará el último URI establecido en él o null (el valor predeterminado) si no se ha realizado ninguno. Si se establece esta propiedad antes de que se haya inicializado CoreWebView2, la inicialización se iniciará en el fondo (si aún no está en curso), después de la cual el WebView2 se desplazará al identificador URI especificado. Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.

Si esta propiedad es null, el CoreWebView2 mostrará "About: Blank" (o si se establece en NULL y el CoreWebView2 se desplazará a "About: Blank"). También es posible que esta propiedad se tenga (o se establezca en) el valor explícito "About: Blank", que tiene el mismo efecto en el CoreWebView2. En otras palabras, si el CoreWebView2 muestra "About: Blank", el valor de esta propiedad puede ser null o "About: Blank". Sin embargo, NULL y "About: Blank" son valores distintos de esta propiedad y no se tratan como iguales entre sí. Esto es importante para la inicialización de controles porque significa que cambiar el valor de null (predeterminado) por "About: Blank" sigue siendo un cambio y seguirá desencadenando la inicialización implícita. 

##### Excepciones
* `ObjectDisposedException` Se produce si ya se ha llamado a Dispose en el control.

#### ZoomFactor 

El factor de zoom para la vista de WebView.

> [ZoomFactor](#zoomfactor) doble público

Esta propiedad expone directamente CoreWebView2Controller. ZoomFactor, consulta su documentación para obtener más información. Si se obtiene esta propiedad antes de que se haya inicializado CoreWebView2, se recuperará el último valor que se estableció en él, o 1,0 (valor predeterminado) si no se ha realizado ninguno. El valor más reciente establecido en esta propiedad antes de que se haya inicializado el CoreWebView2 se establecerá en él después de la inicialización.

#### EnsureCoreWebView2Async 

Desencadenar de forma explícita la inicialización de la CoreWebView2 del control.

> [EnsureCoreWebView2Async](#ensurecorewebview2async)de tareas públicas (entorno de CoreWebView2Environment)

Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.

##### Parameters
* `environment` Un CoreWebView2Environment creado previamente que se debe usar para crear el CoreWebView2. Crear su propio entorno le proporciona control sobre varias opciones que afectan a la forma en que se inicializa CoreWebView2. Si pasas un entorno a este método, se invalidarán los valores especificados en la propiedad CreationProperties. Si pasa null (el valor predeterminado) y no se ha establecido ningún valor en CreationProperties, se creará un entorno predeterminado y se usará automáticamente. 

##### Devuelve
Una tarea que representa el proceso de inicialización en segundo plano. Cuando la tarea se complete, la propiedad CoreWebView2 estará disponible para su uso (es decir, no NULL). Observe que el evento CoreWebView2Ready del control se invocará antes de que se complete la tarea. 

Llamar a este método los tiempos adicionales no tendrán efecto (se ignora cualquier entorno especificado) y devolverán la misma tarea que la primera llamada. La llamada a este método después de la inicialización se ha desencadenado de forma implícita mediante la configuración de la propiedad Source no tendrá ningún efecto (se ignora cualquier entorno especificado) y simplemente devuelva una tarea que represente la inicialización que ya está en curso. Ten en cuenta que aunque este método es asincrónico y devuelve una tarea, aún debe llamarse en el subproceso de la interfaz de usuario, como la mayoría de las funciones públicas de la mayoría de los controles de la interfaz de usuario. 

##### Excepciones
* `InvalidOperationException` Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario). Para obtener más información, consulta DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Se produce si ya se ha llamado a Dispose en el control.

#### ExecuteScriptAsync 

Ejecuta el código de JavaScript desde el parámetro de javaScript en el documento de nivel superior actual representado en la vista de gráfico.

> Tarea asincrónica pública< cadena > [ExecuteScriptAsync](#executescriptasync)(cadena JavaScript)

Equivale a llamar a CoreWebView2.ExecuteScriptAsync en CoreWebView2

##### Excepciones
* `InvalidOperationException` Se produce si CoreWebView2 todavía no se ha inicializado.

* `InvalidOperationException` Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario). Para obtener más información, consulta DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Se produce si ya se ha llamado a Dispose en el control.

#### GoBack 

Navega por la vista Web a la página anterior del historial de navegación.

> public void [GoBack](#goback)()

Equivale a llamar a CoreWebView2. GoBack en CoreWebView2 si CoreWebView2 no se ha inicializado todavía no hace nada.

##### Excepciones
* `InvalidOperationException` Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario). Para obtener más información, consulta DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Se produce si ya se ha llamado a Dispose en el control.

#### GoForward 

Navega por la vista Web a la página siguiente del historial de navegación.

> public void [GoForward](#goforward)()

Equivale a llamar a CoreWebView2. GoForward en CoreWebView2 si CoreWebView2 no se ha inicializado aún no hace nada.

##### Excepciones
* `InvalidOperationException` Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (normalmente, el subproceso de la interfaz de usuario). Para obtener más información, consulta DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Se produce si ya se ha llamado a Dispose en el control.

#### NavigateToString 

Inicia una navegación para htmlContent como HTML de origen de un documento nuevo.

> public void [NavigateToString](#navigatetostring)(String htmlContent)

Equivale a llamar a CoreWebView2. NavigateToString en CoreWebView2

##### Excepciones
* `InvalidOperationException` Se produce si CoreWebView2 todavía no se ha inicializado.

" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).  Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.

#### Volver a cargar 

Vuelve a cargar la página actual.

> public void [Reload](#reload)()

Equivale a llamar a CoreWebView2. Reload en CoreWebView2

##### Excepciones
* `InvalidOperationException` Se produce si CoreWebView2 todavía no se ha inicializado.

" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).  Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.

#### Detener 

Detiene todas las navegaciones y las búsquedas de recursos pendientes.

> public void [Stop](#stop)()

Equivale a llamar a CoreWebView2. STOP en CoreWebView2

##### Excepciones
* `InvalidOperationException` Se produce si CoreWebView2 todavía no se ha inicializado.

" <exception cref="InvalidOperationException"> Se produce si el subproceso de la llamada no es el subproceso que creó este objeto (generalmente, el subproceso de la interfaz de usuario).  Para obtener más información, consulta DispatcherObject. VerifyAccess. </exception>
<exception cref="ObjectDisposedException"> Se produce si ya se ha llamado a Dispose en el control.

#### WebView2 

Crea una nueva instancia de un control WebView2.

> [WebView2](#webview2)pública ()

Ten en cuenta que la CoreWebView2 del control será null hasta que se inicialice. Consulta la documentación de la clase WebView2 para obtener información general sobre la inicialización.

