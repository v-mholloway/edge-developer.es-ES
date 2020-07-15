---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: e9270705ff6c72167185bddfea6f6f310ebc2e3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877668"
---
# 0.9.515: espacio de nombres Microsoft. Web. WebView2. Core 

> [!NOTE]
> Esta referencia puede modificarse o no estar disponible para las versiones posteriores a la versión de SDK 0.9.515. Consulta la referencia de la [API de WebView2](../../../webview2-api-reference.md) para obtener la referencia de API más reciente.

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Formato de imagen usado por el método CoreWebView2CapturePreview.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Motivo de mover el foco.
[CoreWebView2PermissionKind](#corewebview2permissionkind) | El tipo de una solicitud de permiso.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Respuesta a una solicitud de permiso.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Tipo de error de proceso usado en la clase CoreWebView2ProcessFailedEventHandler.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Cuadro de diálogo tipo de JavaScript usado en la clase CoreWebView2ScriptDialogOpeningEventHandler.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Valores de estado de error para navegaciones Web.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Enumeración de contextos de solicitud de recursos Web.
CoreWebView2 | WebView2 le permite hospedar contenido web con la tecnología de explorador Web más reciente.
CoreWebView2AcceleratorKeyPressedEventArgs | Argumentos de evento para el evento AcceleratorKeyPressed.
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
CoreWebView2ProcessFailedEventArgs | Argumentos de evento para el evento ProcessFailed.
CoreWebView2ScriptDialogOpeningEventArgs | Argumentos de evento para el evento ScriptDialogOpening.
CoreWebView2Settings | Define las propiedades que habilitan, deshabilitan o modifican las características de vista de vista.
CoreWebView2SourceChangedEventArgs | Argumentos de evento para el evento SourceChanged.
CoreWebView2WebMessageReceivedEventArgs | Argumentos de evento para el evento WebMessageReceived.
CoreWebView2WebResourceRequestedEventArgs | Argumentos de evento para el evento WebResourceRequested.
EdgeNotFoundException | La excepción que se produce cuando falta la instalación de un extremo.
CoreWebView2PhysicalKeyStatus | Una estructura que representa la información empaquetada en el LPARAM que se proporciona a un evento de tecla Win32.

## Miembros

#### CoreWebView2CapturePreviewImageFormat 

> enumeración [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
PNG            | Formato de imagen PNG.
JPEG            | Formato de imagen JPEG.

Formato de imagen usado por el método CoreWebView2CapturePreview.

#### CoreWebView2KeyEventKind 

> enumeración [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
KeyDown            | Corresponde a WM_KEYDOWN de mensaje de ventana.
KeyUp            | Corresponde a WM_KEYUP de mensaje de ventana.
SystemKeyDown            | Corresponde a WM_SYSKEYDOWN de mensaje de ventana.
SystemKeyUp            | Corresponde a WM_SYSKEYUP de mensaje de ventana.

El tipo de evento de tecla que ha desencadenado un evento AcceleratorKeyPressed.

#### CoreWebView2MoveFocusReason 

> enumeración [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Mediante programación            | El ajuste del foco a WebView.
Siguiente            | Moviendo el foco debido a una resaltado de pestañas hacia adelante.
Anterior            | Moviendo el foco debido a un recorrido de tabulación hacia atrás.

Motivo de mover el foco.

#### CoreWebView2PermissionKind 

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

El tipo de una solicitud de permiso.

#### CoreWebView2PermissionState 

> enumeración [CoreWebView2PermissionState](#corewebview2permissionstate)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Predeterminado            | Use el comportamiento de explorador predeterminado, que suele solicitar a los usuarios la decisión.
Permitir            | Otorgue la solicitud de permiso.
Denegar            | Denegar la solicitud de permiso.

Respuesta a una solicitud de permiso.

#### CoreWebView2ProcessFailedKind 

> enumeración [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
BrowserProcessExited            | Indicó que el proceso del explorador terminó de forma inesperada.
RenderProcessExited            | Indicó que el proceso de representación terminó de forma inesperada.
RenderProcessUnresponsive            | Indica que el proceso de representación no responde.

Tipo de error de proceso usado en la clase CoreWebView2ProcessFailedEventHandler.

#### CoreWebView2ScriptDialogKind 

> enumeración [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Los                         | Descripciones
--------------------------------|---------------------------------------------
Alerta            | Un cuadro de diálogo invocado a través de la función de JavaScript Window. Alert.
Confirmar            | Un cuadro de diálogo invocado a través de la función de la ventana. confirmar JavaScript.
Deba            | Un cuadro de diálogo invocado a través de la función de aviso de JavaScript.
Beforeunload            | Un cuadro de diálogo invocado a través de la función de JavaScript Window. beforeunload.

Cuadro de diálogo tipo de JavaScript usado en la clase CoreWebView2ScriptDialogOpeningEventHandler.

#### CoreWebView2WebErrorStatus 

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

Valores de estado de error para navegaciones Web.

#### CoreWebView2WebResourceContext 

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

Enumeración de contextos de solicitud de recursos Web.

