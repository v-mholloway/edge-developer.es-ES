---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: c4dae1a20d728a92e7a3abb3c8602eeff76da44c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699340"
---
# Espacio de nombres Microsoft.Web.WebView2.Core 

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Formato de imagen usado por el método CoreWebView2CapturePreview.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.
[CoreWebView2MouseEventKind](#corewebview2mouseeventkind) | Tipo de evento del mouse usado por SendMouseInput para transmitir el tipo de evento del mouse que se envía a WebView.
[CoreWebView2MouseEventVirtualKeys](#corewebview2mouseeventvirtualkeys) | Teclas virtuales de eventos del mouse asociadas a una CoreWebView2MouseEventKind para SendMouseInput.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Motivo de mover el foco.
[CoreWebView2PermissionKind](#corewebview2permissionkind) | El tipo de una solicitud de permiso.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Respuesta a una solicitud de permiso.
[CoreWebView2PointerEventKind](#corewebview2pointereventkind) | Tipo de evento de puntero usado por SendPointerInput para transmitir el tipo de evento de puntero que se envía a WebView.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Tipo de error de proceso usado en la clase CoreWebView2ProcessFailedEventHandler.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Cuadro de diálogo tipo de JavaScript usado en la clase CoreWebView2ScriptDialogOpeningEventHandler.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Valores de estado de error para navegaciones Web.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Enumeración de contextos de solicitud de recursos Web.
CoreWebView2 | WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.
CoreWebView2AcceleratorKeyPressedEventArgs | Argumentos de evento para el evento AcceleratorKeyPressed.
CoreWebView2CompositionController | Esta clase es una extensión de la clase CoreWebView2Controller para admitir el hospedaje visual.
CoreWebView2ContentLoadingEventArgs | Argumentos de evento para el evento ContentLoading.
CoreWebView2Controller | Esta clase es el propietario del objeto CoreWebView2 y proporciona compatibilidad para cambiar el tamaño, mostrar y ocultar, enfocar y otras funciones relacionadas con la ventana y la composición.
CoreWebView2Deferral | Esta clase se usa para completar aplazamientos en argumentos de evento que admiten la obtención de aplazamientos a través de su método GetDeferral.
CoreWebView2DevToolsProtocolEventReceivedEventArgs | Argumentos de evento para el evento DevToolsProtocolEventReceived.
CoreWebView2DevToolsProtocolEventReceiver | Se crea un receptor para un evento de protocolo DevTools en particular y le permite suscribirse y anular la suscripción de ese evento.
CoreWebView2Environment | Esto representa el entorno de WebView2.
CoreWebView2EnvironmentOptions | Opciones usadas para crear un entorno WebView2.
CoreWebView2MoveFocusRequestedEventArgs | Argumentos de evento para el evento MoveFocusRequested.
CoreWebView2NavigationCompletedEventArgs | Argumentos de evento para el evento NavigationCompleted.
CoreWebView2NavigationStartingEventArgs | Argumentos de evento para el evento NavigationStarting.
CoreWebView2NewWindowRequestedEventArgs | Argumentos de evento para el evento NewWindowRequested.
CoreWebView2PermissionRequestedEventArgs | Argumentos de evento para el evento PermissionRequested.
CoreWebView2PointerInfo | Esto representa principalmente un objeto Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.
CoreWebView2ProcessFailedEventArgs | Argumentos de evento para el evento ProcessFailed.
CoreWebView2ScriptDialogOpeningEventArgs | Argumentos de evento para el evento ScriptDialogOpening.
CoreWebView2Settings | Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.
CoreWebView2SourceChangedEventArgs | Argumentos de evento para el evento SourceChanged.
CoreWebView2WebMessageReceivedEventArgs | Argumentos de evento para el evento WebMessageReceived.
CoreWebView2WebResourceRequestedEventArgs | Argumentos de evento para el evento WebResourceRequested.
CoreWebView2WindowFeatures | Características de la ventana de una ventana emergente de vista previa.
EdgeNotFoundException | La excepción que se produce cuando falta la instalación de un extremo.
CoreWebView2Matrix4x4 | Esta transformación se usa para calcular las coordenadas correctas al llamar a CreateCoreWebView2PointerInfoFromPointerId.
CoreWebView2PhysicalKeyStatus | Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.

## Miembros

#### CoreWebView2CapturePreviewImageFormat 

Formato de imagen usado por el método CoreWebView2CapturePreview.

> enumeración [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
PNG            | Formato de imagen PNG.
JPEG            | Formato de imagen JPEG.

#### CoreWebView2KeyEventKind 

El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.

> enumeración [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
KeyDown            | Corresponde a WM_KEYDOWN de mensaje de ventana.
KeyUp            | Corresponde a WM_KEYUP de mensaje de ventana.
SystemKeyDown            | Corresponde a WM_SYSKEYDOWN de mensaje de ventana.
SystemKeyUp            | Corresponde a WM_SYSKEYUP de mensaje de ventana.

#### CoreWebView2MouseEventKind 

> [!NOTE]
> Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).

Tipo de evento del mouse usado por SendMouseInput para transmitir el tipo de evento del mouse que se envía a WebView.

> enumeración [CoreWebView2MouseEventKind](#corewebview2mouseeventkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
HorizontalWheel            | Evento de desplazamiento horizontal de la rueda del mouse, WM_MOUSEHWHEEL.
LeftButtonDoubleClick            | Botón izquierdo doble clic en evento de mouse, WM_LBUTTONDBLCLK.
LeftButtonDown            | Botón izquierdo de un evento de mouse, WM_LBUTTONDOWN.
LeftButtonUp            | Evento de botón arriba del botón izquierdo, WM_LBUTTONUP.
Dejen            | Evento Leave de mouse, WM_MOUSELEAVE.
MiddleButtonDoubleClick            | Botón central doble clic en evento de mouse, WM_MBUTTONDBLCLK.
MiddleButtonDown            | Botón central de mouse, WM_MBUTTONDOWN.
MiddleButtonUp            | Evento de botón arriba del botón central, WM_MBUTTONUP.
Move            | Evento de movimiento del mouse, WM_MOUSEMOVE.
RightButtonDoubleClick            | Botón secundario doble clic en el evento del mouse WM_RBUTTONDBLCLK.
RightButtonDown            | Botón secundario del mouse, WM_RBUTTONDOWN.
RightButtonUp            | Evento de botón arriba del botón secundario, WM_RBUTTONUP.
Rueda            | Evento scroll de la rueda del mouse, WM_MOUSEWHEEL.
XButtonDoubleClick            | Primer o segundo botón X haga doble clic en evento del mouse, WM_XBUTTONDBLCLK.
XButtonDown            | Primer o segundo evento de mouse en el botón X presionado, WM_XBUTTONDOWN.
XButtonUp            | Primer o segundo evento del botón X del botón arriba, WM_XBUTTONUP.

#### CoreWebView2MouseEventVirtualKeys 

> [!NOTE]
> Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).

Teclas virtuales de eventos del mouse asociadas a una CoreWebView2MouseEventKind para SendMouseInput.

> enumeración [CoreWebView2MouseEventVirtualKeys](#corewebview2mouseeventvirtualkeys)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Ninguno            | No se han presionado teclas adicionales.
LeftButton            | El botón primario del mouse está presionado, MK_LBUTTON.
RightButton            | El botón secundario del mouse está presionado, MK_RBUTTON.
Mayús            | La tecla Mayús está presionada, MK_SHIFT.
Control            | La tecla CTRL está presionada, MK_CONTROL.
MiddleButton            | El botón central del mouse está presionado, MK_MBUTTON.
XButton1            | El primer botón X está presionado, MK_XBUTTON1.
XButton2            | El segundo botón X está presionado, MK_XBUTTON2.

#### CoreWebView2MoveFocusReason 

Motivo de mover el foco.

> enumeración [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Mediante programación            | El ajuste del foco a WebView.
Siguiente            | Moviendo el foco debido a una resaltado de pestañas hacia adelante.
Anterior            | Moviendo el foco debido a un recorrido de tabulación hacia atrás.

#### CoreWebView2PermissionKind 

El tipo de una solicitud de permiso.

> enumeración [CoreWebView2PermissionKind](#corewebview2permissionkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
UnknownPermission            | Permiso desconocido.
Micrófono            | Permiso para capturar audio.
Cámara            | Permiso para capturar video.
Geolocalización            | Permiso para acceder a la ubicación geográfica.
Notificaciones            | Permiso para enviar notificaciones Web.
OtherSensors            | Permiso para acceder al sensor genérico.
ClipboardRead            | Permiso para leer el Portapapeles del sistema sin un gesto de usuario.

#### CoreWebView2PermissionState 

Respuesta a una solicitud de permiso.

> enumeración [CoreWebView2PermissionState](#corewebview2permissionstate)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Predeterminado            | Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.
Permitir            | Otorgue la solicitud de permiso.
Denegar            | Denegar la solicitud de permiso.

#### CoreWebView2PointerEventKind 

> [!NOTE]
> Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).

Tipo de evento de puntero usado por SendPointerInput para transmitir el tipo de evento de puntero que se envía a WebView.

> enumeración [CoreWebView2PointerEventKind](#corewebview2pointereventkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Activar            | Corresponde a WM_POINTERACTIVATE.
Abajo            | Corresponde a WM_POINTERDOWN.
Entrar            | Corresponde a WM_POINTERENTER.
Dejen            | Corresponde a WM_POINTERLEAVE.
Arriba            | Corresponde a WM_POINTERUP.
Actualizar            | Corresponde a WM_POINTERUPDATE.

#### CoreWebView2ProcessFailedKind 

Tipo de error de proceso usado en la clase CoreWebView2ProcessFailedEventHandler.

> enumeración [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
BrowserProcessExited            | Indicó que el proceso del explorador terminó de forma inesperada.
RenderProcessExited            | Indicó que el proceso de representación terminó de forma inesperada.
RenderProcessUnresponsive            | Indica que el proceso de representación no responde.

#### CoreWebView2ScriptDialogKind 

Cuadro de diálogo tipo de JavaScript usado en la clase CoreWebView2ScriptDialogOpeningEventHandler.

> enumeración [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Alerta            | Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.
Confirmar            | Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.
Deba            | Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.
Beforeunload            | Un cuadro de diálogo invocado a través de la función de JavaScript Window. beforeunload.

#### CoreWebView2WebErrorStatus 

Valores de estado de error para navegaciones Web.

> enumeración [CoreWebView2WebErrorStatus](#corewebview2weberrorstatus)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Unknown            | Se ha producido un error desconocido.
CertificateCommonNameIsIncorrect            | El nombre común del certificado SSL no coincide con la dirección Web.
CertificateExpired            | El certificado SSL ha expirado.
ClientCertificateContainsErrors            | El certificado de cliente SSL contiene errores.
CertificateRevoked            | El certificado SSL ha sido revocado.
CertificateIsInvalid            | El certificado SSL no es válido &ndash; esto puede significar que el certificado no coincide con los pin de clave pública del nombre de host, que el certificado está firmado por una autoridad que no es de confianza o con un algoritmo de signo débil. el certificado alegó que los nombres DNS han infringido las restricciones de nombres, el certificado contiene una clave débil, el período de validez del certificado es demasiado largo, falta de información de revocación o de mecanismo de revocación, nombre de host no único, falta de información de transparencia del certificado o el certificado está encadenado a una [raíz de Symantec heredado](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).
ServerUnreachable            | No se puede comunicar con el host.
Tiempo de espera agotado            | Se agotó el tiempo de espera de la conexión.
ErrorHttpInvalidServerResponse            | El servidor ha devuelto una respuesta no válida o no reconocida.
ConnectionAborted            | La conexión ha sido cancelada.
ConnectionReset            | Se restableció la conexión.
Desconectado            | Se perdió la conexión a Internet.
CannotConnect            | No se puede conectar al destino.
HostNameNotResolved            | No se pudo resolver el nombre de host proporcionado.
OperationCanceled            | Se canceló la operación.
RedirectFailed            | Error en la redirección de la solicitud.
UnexpectedError            | Se ha producido un error inesperado.

#### CoreWebView2WebResourceContext 

Enumeración de contextos de solicitud de recursos Web.

> enumeración [CoreWebView2WebResourceContext](#corewebview2webresourcecontext)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Todos            | Todos los recursos.
Documento            | Recursos de documentos.
Extensible            | Recursos de CSS.
Imagen            | Recursos de imagen.
Multimedia            | Otros recursos multimedia, como los vídeos.
Fuente            | Recursos de fuentes.
Script            | Recursos de script.
XmlHttpRequest            | Solicitudes XML HTTP.
Desempeño            | Capture la comunicación de la API.
TextTrack            | Recursos de TextTrack.
EventSource            | Comunicación de la API de EventSource.
Websocket            | Comunicación de API WebSocket.
Manifiesta            | Manifiestos de la aplicación Web.
SignedExchange            | Intercambio de HTTP firmado.
Ejecutar            | Solicitudes de ping.
CspViolationReport            | Informes de violación de CSP.
Otros            | Otros recursos.

