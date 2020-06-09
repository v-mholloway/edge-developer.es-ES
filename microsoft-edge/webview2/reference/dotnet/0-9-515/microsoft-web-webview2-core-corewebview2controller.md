---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 2b9ad09fd347a6719523213e5ebc13d9000d536b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697710"
---
# Clase Microsoft. Web. WebView2. Core. CoreWebView2Controller 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

Espacio de nombres: Microsoft. Web. WebView2. Core \
Ensamblado: Microsoft. Web. WebView2. Core. dll

Esta clase es el propietario del objeto CoreWebView2 y proporciona compatibilidad para cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[AcceleratorKeyPressed](#acceleratorkeypressed) | AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa.
[Límites](#bounds) | Los límites de la vista previa.
[CoreWebView2](#corewebview2) | Obtiene el CoreWebView2 asociado a este CoreWebView2Controller.
[GotFocus](#gotfocus) | GotFocus se desencadena cuando WebView tiene el foco.
[IsVisible](#isvisible) | La propiedad IsVisible determina si se muestra u oculta la vista en WebView.
[LostFocus](#lostfocus) | LostFocus se desencadena cuando WebView pierde el foco.
[MoveFocusRequested](#movefocusrequested) | MoveFocusRequested se activa cuando el usuario intenta usar la tecla TAB fuera de la vista.
[ParentWindow](#parentwindow) | La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.
[ZoomFactor](#zoomfactor) | El factor de zoom para la vista de WebView.
[ZoomFactorChanged](#zoomfactorchanged) | El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa.
[Cerrar](#close) | Cierra WebView y limpia la instancia de explorador subyacente.
[MoveFocus](#movefocus) | Mover el foco a WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Esta es una notificación independiente de los límites que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.

El CoreWebView2Controller es propietario de la CoreWebView2 y, si todas las referencias a CoreWebView2Controller desaparecen, se cerrará la WebView.

## Miembros

#### AcceleratorKeyPressed 

AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa.

> evento público EventHandler< [CoreWebView2AcceleratorKeyPressedEventArgs](microsoft-web-webview2-core-corewebview2acceleratorkeypressedeventargs.md)  >  [AcceleratorKeyPressed](#acceleratorkeypressed)

AcceleratorKeyPressed se desencadena cuando se presiona o se suelta una tecla de aceleración o un combinado de teclas mientras la vista de la vista en WebView está activa. Una clave se considera un acelerador si:

1. La tecla Ctrl o Alt se está retenida actualmente, o bien

1. la tecla presionada no se asigna a un carácter. Algunas teclas específicas nunca se consideran aceleradores, como Mayús. La tecla de escape se considera siempre un acelerador.

Los eventos de teclas autorepetidos que se provocan al mantener presionada la tecla también desencadenan este evento. Puedes filtrarlos comprobando los argumentos del evento ' KeyEventLParam o PhysicalKeyStatus.

En el modo de ventana, se llama a este controlador de eventos de forma sincrónica. Hasta que llames al controlador () en los argumentos del evento o se devuelva el controlador de eventos, el proceso del explorador se bloqueará y las llamadas COM salientes entre procesos generarán un error con RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Sin embargo, todos los métodos de la API de CoreWebView2 funcionarán.

En el modo sin ventana, se llama al controlador de eventos de forma asincrónica. La entrada de datos adicionales no llegará al explorador hasta que el controlador de eventos devuelva o se llame a (), pero el proceso del explorador en sí no se bloqueará y las llamadas COM salientes funcionarán normalmente.

Se recomienda que llame al controlador (TRUE) tan pronto como sepa que desea controlar la tecla de aceleración.

#### Límites 

Los límites de la vista previa.

> [límites](#bounds) del rectángulo público

Los límites son relativos al identificador HWND primario. La aplicación tiene dos formas en las que puede ubicar una vista en WebView:

1. Cree un HWND secundario que sea el objeto HWND de la vista < View. Coloque esta ventana donde debería estar la vista en la vista. En este caso, use (0,0) para la Bound's esquina superior izquierda de la vista de vista previa (el desplazamiento).

1. Use la última ventana de la aplicación como el HWND primario de WebView. Establezca la Bound's esquina superior izquierda de la vista previa para que la vista de la vista en la aplicación se coloque correctamente en la aplicación. Los valores de la entrada enlazada están en el espacio de coordenadas del host.

#### CoreWebView2 

Obtiene el CoreWebView2 asociado a este CoreWebView2Controller.

> [CoreWebView2](microsoft-web-webview2-core-corewebview2.md) pública [CoreWebView2](#corewebview2)

#### GotFocus 

GotFocus se desencadena cuando WebView tiene el foco.

> objeto public EventHandler< > [GotFocus](#gotfocus)

#### IsVisible 

La propiedad IsVisible determina si se muestra u oculta la vista en WebView.

> Public bool [IsVisible](#isvisible)

Si IsVisible se establece en false, WebView será transparente y no se representará. Sin embargo, esto no afectará a la ventana que contenga la vista de contenido (el parámetro HWND pasado a CreateCoreWebView2Controller). Si desea que esta ventana desaparezca también, llame a ShowWindow directamente, además de modificar la propiedad IsVisible. Si la ventana superior está minimizada o restaurada, WebView no recibirá mensajes de ventana. Por motivos de rendimiento, desarrollador debe establecer el valor de la propiedad IsVisible de la WebView en falso cuando la ventana de la aplicación está minimizada y volver a ser true cuando se restaura la ventana de la aplicación. La ventana de la aplicación puede hacerlo controlando SC_MINIMIZE y SC_RESTORE comando al recibir WM_SYSCOMMAND mensaje.

#### LostFocus 

LostFocus se desencadena cuando WebView pierde el foco.

> objeto public evento EventHandler< > [LostFocus](#lostfocus)

En caso de que se inicie el evento MoveFocusRequested, el foco seguirá en la vista previa cuando se desencadene el evento MoveFocusRequested. Perder el foco solo se activa cuando el código de la aplicación o la acción predeterminada del evento MoveFocusRequested está lejos de WebView.

#### MoveFocusRequested 

MoveFocusRequested se activa cuando el usuario intenta usar la tecla TAB fuera de la vista.

> evento público EventHandler< [CoreWebView2MoveFocusRequestedEventArgs](microsoft-web-webview2-core-corewebview2movefocusrequestedeventargs.md)  >  [MoveFocusRequested](#movefocusrequested)

El foco de la vista de WebView no ha cambiado cuando se desencadena este evento.

#### ParentWindow 

La ventana principal proporcionada por la aplicación que esta vista previa usa para representar contenido.

> [IntPtr Public](#parentwindow)

La configuración de la propiedad hará que la vista de la vista de ventana reorigen su ventana a la ventana recién suministrada.

#### ZoomFactor 

El factor de zoom para la vista de WebView.

> [ZoomFactor](#zoomfactor) doble público

Ten en cuenta que cambiar el factor de zoom podría provocar un `window.innerWidth/innerHeight` cambio en el diseño de página. Un factor de zoom aplicado por el host mediante una llamada a ZoomFactor se convierte en el nuevo zoom predeterminado para la vista de la vista en WebView. Este factor de zoom se aplica en la navegación y se vuelve al factor de zoom en la vista previa cuando el usuario presiona Ctrl + 0. Cuando el usuario cambia el factor de zoom (es decir, la aplicación que recibe la ZoomFactorChanged), ese zoom solo se aplica a la página actual. Cualquier zoom aplicado a un usuario solo es para la página actual y se restablece en una navegación. No se permite especificar un zoomFactor menor o igual que 0. WebView también tiene un intervalo de factor de zoom compatible interno. Cuando un factor de zoom especificado está fuera de ese rango, se normalizará para que esté dentro del rango y se desencadenará un evento ZoomFactorChanged para el factor de zoom aplicado real. Cuando se produzca esta normalización de rango, la propiedad ZoomFactor informará sobre el factor de zoom especificado durante la modificación anterior de la propiedad ZoomFactor hasta que se reciba el evento ZoomFactorChanged después de que la vista previa aplique el factor de zoom normalizado.

#### ZoomFactorChanged 

El evento se desencadena cuando cambia la propiedad ZoomFactor de la vista de vista previa.

> evento público EventHandler< > [ZoomFactorChanged](#zoomfactorchanged)

El evento se podría activar porque el autor de la llamada modificó la propiedad ZoomFactor o debido a que el usuario modificaba manualmente el zoom. Cuando el autor de la llamada lo modifica a través de la propiedad ZoomFactor, el factor de zoom interno se actualiza inmediatamente y no se producirá ningún evento ZoomFactorChanged. La vista Web asocia el último factor de zoom usado para cada sitio. Por lo tanto, es posible que el factor de zoom cambie al navegar a una página diferente. Cuando el factor de zoom cambia debido a esto, el evento ZoomFactorChanged se activa justo después del evento ContentLoading.

#### Cerrar 

Cierra WebView y limpia la instancia de explorador subyacente.

> public void [Close](#close)()

La limpieza de la instancia del explorador liberará los recursos que se encienden en la vista Web. La instancia del explorador se cerrará si no hay ninguna otra vista previa con ella.

Después de llamar a Close, todas las llamadas a métodos producirán errores y los controladores de eventos dejarán de activarse. Específicamente, la WebView liberará sus referencias a los controladores de eventos cuando se llama a Close.

Close se llama de forma implícita cuando CoreWebView2Controller pierde su referencia final y se destruye. Sin embargo, se recomienda llamar de forma explícita a Close para evitar cualquier ciclo de referencias entre la vista de WebView y el código de la aplicación. En concreto, si capturas una referencia a la vista de la vista en un controlador de eventos, crearás un ciclo de referencia entre la vista en WebView y el controlador de eventos. Al llamar a Close se interrumpirá este ciclo liberando todos los controladores de eventos. Pero para evitar esta situación, lo mejor es llamar explícitamente a Close en WebView y no capturar una referencia a WebView para asegurarte de que la WebView pueda limpiarse correctamente.

#### MoveFocus 

Mover el foco a WebView.

> public void [MoveFocus](#movefocus)([CoreWebView2MoveFocusReason](./namespace-microsoft-web-webview2-core.md) Reason)

La vista web obtendrá el foco y el foco se establecerá en el elemento de corresponsal de la página hospedada en la vista Web. Por motivos de programación, el foco se establece en elemento con enfoque anterior o en el elemento predeterminado si no hay ningún elemento con el foco anterior. Por el siguiente motivo, el foco se establece en el primer elemento. Por el motivo anterior, el foco se establece en el último elemento. WebView también puede obtener el foco a través de la interacción del usuario, como hacer clic en la vista previa o en la pestaña en la misma. Para la tabulación, la aplicación puede llamar a MoveFocus con la función siguiente o anterior para alinear con la tabulación y Mayús + Tab, respectivamente al decidir la vista previa del elemento tabulador. O bien, la aplicación puede llamar a IsDialogMessage como parte de su bucle de mensajes para permitir que la plataforma maneje automáticamente la tabulación. La plataforma girará en todas las ventanas con WS_TABSTOP. Cuando la vista de la vista de la vista de IsDialogMessage, coloca internamente el foco en el primer o el último elemento de Tab y Mayús + Tab, respectivamente.

#### NotifyParentWindowPositionChanged 

Esta es una notificación independiente de los límites que informa a WebView de que se ha movido su HWND primario (o cualquier antecesor).

> public void [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Esto es necesario para que la accesibilidad y determinados cuadros de diálogo de WebView funcionen correctamente.

#### SetBoundsAndZoomFactor 

Actualice las propiedades Bounds y ZoomFactor al mismo tiempo.

> public void [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(límites Rect, Double ZoomFactor)

Esta operación es atómica desde la perspectiva del anfitrión. Después de volver de esta función, las propiedades Bounds y ZoomFactor se actualizarán si la función se realiza correctamente, o no se actualizará si se produce un error en la función. Si los límites y ZoomFactor se actualizan con la misma escala (es decir, los límites y ZoomFactor están duplicados), la página no verá un cambio en la ventana. innerWidth/innerHeight y la WebView representará el contenido en el nuevo tamaño y zoom sin representaciones intermedias. Esta función también se puede usar para actualizar solo una de ZoomFactor o límites pasando el nuevo valor para uno y el valor actual para el otro.

