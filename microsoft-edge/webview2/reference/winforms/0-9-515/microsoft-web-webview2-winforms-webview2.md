---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 532c898845125564ad5af6460dc8d1ff6464abfb
ms.sourcegitcommit: 83efa259be89cc773a82751242495a0a919d54cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2020
ms.locfileid: "10687807"
---
# Clase Microsoft. Web. WebView2. WinForms. WebView2 

Espacio de nombres: Microsoft. Web. WebView2. WinForms \
Ensamblado: Microsoft. Web. WebView2. WinForms. dll

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

Control para incrustar WebView2 en WinForms.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | ContentLoading las distribuciones después de la navegación comienzan a un nuevo URI y el contenido de ese URI comienza a representarse.
[CoreWebView2Ready](#corewebview2ready) | Este evento se desencadena cuando se ha terminado de inicializar el [CoreWebView2](#corewebview2) del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.
[NavigationCompleted](#navigationcompleted) | NavigationCompleted se envía después de navegar por el documento de nivel superior para representarlo correctamente o no.
[NavigationStarting](#navigationstarting) | NavigationStarting se envía antes de que se inicie una nueva navegación en el documento de nivel superior de la WebView2.
[SourceChanged](#sourcechanged) | SourceChanged se distribuye después de que cambie la propiedad de origen.
[WebMessageReceived](#webmessagereceived) | WebMessageReceived se distribuye después de que el contenido web envíe un mensaje al host de la aplicación a través de `chrome.webview.postMessage` .
[CoreWebView2](#corewebview2) | El CoreWebView2 subyacente.
[Source](#source) | La propiedad Source es el identificador URI del documento de nivel superior del WebView2.
[ZoomFactor](#zoomfactor) | El factor de zoom para la vista de WebView.
[CanGoBack](#cangoback) | Devuelve true si la vista Web puede navegar a una página anterior en el historial de navegación a través del método GoBack.
[CanGoForward](#cangoforward) | Devuelve true si la vista Web puede navegar a una página siguiente del historial de navegación a través del método GoForward.
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Desencadenar de forma explícita la inicialización de la [CoreWebView2](#corewebview2)del control.
[ExecuteScriptAsync](#executescriptasync) | Ejecuta el script proporcionado en el documento de nivel superior del WebView2.
[GoBack](#goback) | Ir a la página anterior del historial de navegación.
[GoForward](#goforward) | Ir a la página siguiente del historial de navegación.
[NavigateToString](#navigatetostring) | Representar el código HTML proporcionado como documento de nivel superior del WebView2.
[Volver a cargar](#reload) | Vuelva a cargar el documento de nivel superior del WebView2.
[Detener](#stop) | Detenga cualquier navegación en curso en el WebView2.
[WebView2](#webview2) | Cree un nuevo control WebView2 WinForms.

## Miembros

#### ContentLoading 

ContentLoading las distribuciones después de la navegación comienzan a un nuevo URI y el contenido de ese URI comienza a representarse.

> evento público EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

Esto es equivalente al evento ContentLoading en CoreWebView2. Para obtener más información, consulta la documentación de CoreWebView2. ContentLoading.

#### CoreWebView2Ready 

Este evento se desencadena cuando se ha terminado de inicializar el [CoreWebView2](#corewebview2) del control (independientemente de cómo se haya desencadenado la inicialización), pero antes de que se use para nada.

> evento público EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Debe controlar este evento si necesita realizar operaciones de configuración una vez en el CoreWebView2 el que desea afectar a todos sus usos (por ejemplo, agregar controladores de eventos, configurar valores, instalar scripts de creación de documentos, agregar objetos host).

Este evento no proporciona ningún argumento, y el remitente será el control WebView2, cuya propiedad CoreWebView2 será válida (es decir, no NULL) por primera vez.

#### NavigationCompleted 

NavigationCompleted se envía después de navegar por el documento de nivel superior para representarlo correctamente o no.

> evento público EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

Esto es equivalente al evento NavigationCompleted en CoreWebView2. Para obtener más información, consulta la documentación de CoreWebView2. NavigationCompleted.

#### NavigationStarting 

NavigationStarting se envía antes de que se inicie una nueva navegación en el documento de nivel superior de la WebView2.

> evento público EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

Esto es equivalente al evento NavigationStarting en CoreWebView2. Para obtener más información, consulta la documentación de CoreWebView2. NavigationStarting.

#### SourceChanged 

SourceChanged se distribuye después de que cambie la propiedad de origen.

> evento público EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)

Esto puede ocurrir durante una navegación o si, de lo contrario, el script de la página cambia el URI del documento. Esto es equivalente al evento SourceChanged en CoreWebView2. Para obtener más información, consulta la documentación de CoreWebView2. SourceChanged.

#### WebMessageReceived 

WebMessageReceived se distribuye después de que el contenido web envíe un mensaje al host de la aplicación a través de `chrome.webview.postMessage` .

> evento público EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

Esto es equivalente al evento WebMessageReceived en CoreWebView2. Para obtener más información, consulta la documentación de CoreWebView2. WebMessageReceived.

#### CoreWebView2 

El CoreWebView2 subyacente.

> CoreWebView2 pública [CoreWebView2](#corewebview2)

Use esta propiedad para realizar más operaciones en el contenido de WebView2 de las que se exponen en el WebView2. Este valor es null hasta que se inicializa. Puedes forzar que el CoreWebView2 subyacente se inicialice mediante el método InitializeAsync.

#### Source 

La propiedad Source es el identificador URI del documento de nivel superior del WebView2.

> [origen](#source) de URI público

Establecer el origen es equivalente a llamar a CoreWebView2. Navigate. Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es "About: Blank". Si la propiedad se establece en un URI no absoluto o en null, la propiedad permanece sin modificar. Para obtener más información, consulta la documentación de CoreWebView2.

#### ZoomFactor 

El factor de zoom para la vista de WebView.

> [ZoomFactor](#zoomfactor) doble público

#### CanGoBack 

Devuelve true si la vista Web puede navegar a una página anterior en el historial de navegación a través del método GoBack.

> Public bool [CanGoBack](#cangoback)

Esto es equivalente a la propiedad CanGoBack de CoreWebView2. Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es falsa. Para obtener más información, consulta la documentación de CoreWebView2. CanGoBack.

#### CanGoForward 

Devuelve true si la vista Web puede navegar a una página siguiente del historial de navegación a través del método GoForward.

> Public bool [CanGoForward](#cangoforward)

Esto es equivalente a la propiedad CanGoForward de CoreWebView2. Si el CoreWebView2 subyacente aún no se ha inicializado, esta propiedad es falsa. Para obtener más información, consulta la documentación de CoreWebView2. CanGoForward.

#### EnsureCoreWebView2Async 

Desencadenar de forma explícita la inicialización de la [CoreWebView2](#corewebview2)del control.

> [EnsureCoreWebView2Async](#ensurecorewebview2async)de tareas públicas (entorno de CoreWebView2Environment)

##### Parameters
* `environment` Un CoreWebView2Environment creado previamente que se debe usar para crear el CoreWebView2. Crear su propio entorno le proporciona control sobre varias opciones que afectan a la forma en que se inicializa CoreWebView2. Si pasa null (el valor predeterminado), se creará un entorno predeterminado y se usará automáticamente. 

##### Devuelve
Una tarea que representa el proceso de inicialización en segundo plano. Cuando la tarea se complete, la propiedad CoreWebView2 estará disponible para su uso (es decir, no NULL). Observe que el evento [CoreWebView2Ready](#corewebview2ready) del control se invocará antes de que se complete la tarea. 

Llamar a este método los tiempos adicionales no tendrán efecto (se ignora cualquier entorno especificado) y devolverán la misma tarea que la primera llamada. La llamada a este método después de la inicialización se ha desencadenado de forma implícita mediante la configuración de la propiedad [source](#source) no tendrá ningún efecto (se ignora cualquier entorno especificado) y simplemente devuelva una tarea que represente la inicialización que ya está en curso. 

##### Excepciones
* `System.InvalidOperationException` Se produce cuando se invoca desde un subproceso que no es de interfaz de usuario.

#### ExecuteScriptAsync 

Ejecuta el script proporcionado en el documento de nivel superior del WebView2.

> Tarea asincrónica pública< cadena > [ExecuteScriptAsync](#executescriptasync)(secuencia de comandos de cadena)

Es equivalente al método ExecuteScriptAsync en CoreWebView2. Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException. Para obtener más información, consulta la documentación de CoreWebView2. ExecuteScriptAsync.

#### GoBack 

Ir a la página anterior del historial de navegación.

> public void [GoBack](#goback)()

Esto es equivalente al método GoBack de la CoreWebView2. Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada. Para obtener más información, vea la documentación de CoreWebView2. GoBack.

#### GoForward 

Ir a la página siguiente del historial de navegación.

> public void [GoForward](#goforward)()

Es equivalente al método GoForward de la CoreWebView2. Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada. Para obtener más información, consulte la documentación de CoreWebView2. GoForward.

#### NavigateToString 

Representar el código HTML proporcionado como documento de nivel superior del WebView2.

> public void [NavigateToString](#navigatetostring)(String htmlContent)

Es equivalente al método NavigateToString en CoreWebView2. Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException. Para obtener más información, consulta la documentación de CoreWebView2. NavigateToString.

#### Volver a cargar 

Vuelva a cargar el documento de nivel superior del WebView2.

> public void [Reload](#reload)()

Es equivalente al método Reload de la CoreWebView2. Si el CoreWebView2 subyacente aún no se ha inicializado, este método inicia una InvalidOperationException. Consulte CoreWebView2. Vuelva a cargar la documentación para obtener más información.

#### Detener 

Detenga cualquier navegación en curso en el WebView2.

> public void [Stop](#stop)()

Es equivalente al método Stop de la CoreWebView2. Si el CoreWebView2 subyacente aún no se ha inicializado, este método no hace nada. Consulte CoreWebView2. detenga la documentación para obtener más información.

#### WebView2 

Cree un nuevo control WebView2 WinForms.

> [WebView2](#webview2)pública ()

Después de la construcción, la propiedad CoreWebView2 es NULL. Llama a [EnsureCoreWebView2Async](#ensurecorewebview2async) para inicializar el CoreWebView2 subyacente.

