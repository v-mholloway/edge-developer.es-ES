---
description: Insertar tecnologías web (HTML, CSS y JavaScript) en las aplicaciones nativas con el control Microsoft Edge WebView2
title: Global
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 37a7d89dbd7d13befe5a07c72fc8baa750775108
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012732"
---
# Global 

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[CompareBrowserVersions](#comparebrowserversions) | Este método es para cualquier persona que desee comparar la versión correctamente para determinar cuál es la versión más reciente, la anterior o la misma.
[CreateCoreWebView2Environment](#createcorewebview2environment) | Crea un entorno de WebView2 de perenne con la versión de Edge instalada.
[CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions) | Exportación de archivos DLL para crear un entorno de WebView2 con una versión personalizada de Edge, directorio de datos de usuario o opciones adicionales.
[GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring) | Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.

## Miembros

#### CompareBrowserVersions 

> público STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR VERSION1, PCWSTR version2, int * result)

Este método es para cualquier persona que desee comparar la versión correctamente para determinar cuál es la versión más reciente, la anterior o la misma.

Puede usarse para determinar si usar webview2 o ciertas características de la base de la versión. Establece el valor de result en-1, 0 o 1 si version1 es menor que, igual o mayor que version2, respectivamente. Devuelve E_INVALIDARG si no se puede analizar ninguna de las cadenas de versión o si cualquier parámetro de entrada es NULL. La entrada puede usar directamente el versionInfo Obtenido de GetAvailableCoreWebView2BrowserVersionString, la información de canal se pasará por alto.

#### CreateCoreWebView2Environment 

> público STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler * environmentCreatedHandler)

Crea un entorno de WebView2 de perenne con la versión de Edge instalada.

Esto es equivalente a llamar a CreateCoreWebView2EnvironmentWithOptions con nullptr para browserExecutableFolder, userDataFolder, additionalBrowserArguments. Para obtener más información, consulta CreateCoreWebView2EnvironmentWithOptions.

#### CreateCoreWebView2EnvironmentWithOptions 

> Public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) * environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) * environmentCreatedHandler)

Exportación de archivos DLL para crear un entorno de WebView2 con una versión personalizada de Edge, directorio de datos de usuario o opciones adicionales.

El entorno WebView2 y todos los demás objetos WebView2 son de subproceso único y tienen dependencias en componentes de Windows que requieren que COM se inicialice para un apartamento de un único subproceso. Se espera que la aplicación llame a CoInitializeEx antes de llamar a CreateCoreWebView2EnvironmentWithOptions.

```
CoInitializeEx(nullptr, COINIT_APARTMENTTHREADED);
```

Si no se llamó a CoInitializeEx o se ha llamado previamente con COINIT_MULTITHREADED, CreateCoreWebView2EnvironmentWithOptions producirá uno de los siguientes errores.

```
CO_E_NOTINITIALIZED (if CoInitializeEx was not called)
RPC_E_CHANGED_MODE  (if CoInitializeEx was previously called with
                     COINIT_MULTITHREADED)
```

`browserExecutableFolder`Se usa para especificar si los controles de WebView2 usan una versión fija o instalada del motor en tiempo de ejecución de WebView2 que existe en un equipo cliente. Para usar una versión fija del motor en tiempo de ejecución de WebView2, pase la ruta de acceso relativa de la carpeta que contiene la versión fija del motor en tiempo de ejecución de WebView2 `browserExecutableFolder` . Para crear controles WebView2 que usen la versión instalada del motor en tiempo de ejecución de WebView2 que existe en los equipos cliente, pase una cadena nula o vacía a `browserExecutableFolder` . En este escenario, la API intenta buscar una versión compatible del tiempo de ejecución de WebView2 que está instalada en el equipo cliente (en primer lugar, en el nivel de equipo y, a continuación, por usuario) con la preferencia de canal seleccionada. La ruta de acceso de la versión fija del tiempo de ejecución de WebView2 no debe contener `\Edge\Application\` . Cuando se usa una ruta de acceso, la API generará un error con ERROR_NOT_SUPPORTED.

El orden de búsqueda de canales predeterminado es el tiempo de ejecución de WebView2, beta, dev y Canarias. Cuando se produce una invalidación WEBVIEW2_RELEASE_CHANNEL_PREFERENCE variable de entorno o el valor de registro releaseChannelPreference aplicable con el valor de 1, se invierte el orden de búsqueda del canal.

userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2. La ruta de acceso puede ser una ruta de acceso de archivo absoluta o una ruta de acceso relativa del archivo que se interprete como relativa al archivo ejecutable del proceso actual. De lo contrario, para las aplicaciones para UWP, la carpeta de datos de usuario predeterminada será la carpeta de datos de la aplicación para el paquete; para las aplicaciones que no son UWP, la carpeta datos de usuario predeterminada se `{Executable File Name}.WebView2` creará en el mismo directorio junto al ejecutable de la aplicación. Se puede producir un error en la creación de WebView2 si el ejecutable se ejecuta en un directorio que el proceso no tiene permiso para crear una carpeta nueva en. La aplicación es responsable de limpiar su carpeta de datos de usuario cuando haya terminado.

Tenga en cuenta que, dado que un proceso de explorador puede compartirse entre las vistas de las web, la creación de WebView no funcionará con HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) si las opciones especificadas no coinciden con las opciones de las vistas previas que se están ejecutando en el proceso del explorador compartido.

environmentCreatedHandler es el resultado de controlador para la operación asincrónica, que contendrá el WebView2Environment que se creó.

Los valores especificados en las variables de entorno o en el registro pueden invalidar browserExecutableFolder, userDataFolder y additionalBrowserArguments de la environmentOptions.

Al crear un WebView2Environment, se comprueban las siguientes variables de entorno:

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

Si se encuentra una variable de entorno override, usamos los valores browserExecutableFolder y userDataFolder como reemplazos de los valores correspondientes en CreateCoreWebView2EnvironmentWithOptions parámetros. Si additionalBrowserArguments se especifica en la variable de entorno o en el registro, se anexará a los valores de correspinding en parámetros de CreateCoreWebView2EnvironmentWithOptions.

Aunque no se invaliden estrictamente, existen variables de entorno adicionales que se pueden establecer:

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

Cuando se encuentra con un valor que no está vacío, indica que WebView se está iniciando bajo un depurador de scripts. En este caso, WebView emitirá un `Page.waitForDebugger` comando CDP que hará que la ejecución de scripts dentro de la vista de WebView se PAUSE al iniciarse, hasta que un depurador emita el `Runtime.runIfWaitingForDebugger` comando CDP correspondiente para reanudar la ejecución. Nota: no hay ninguna clave de registro equivalente a esta variable de entorno.

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

Cuando se encuentra con un valor que no está vacío, indica que WebView se está iniciando bajo un depurador de scripts que también es compatible con aplicaciones host que usan varias vistas previas. El valor se usa como identificador de una canalización con nombre que se abrirá y se escribirá cuando la aplicación host cree un nuevo WebView. La carga coincidirá con la del destino JSON del puerto de depuración remota y el depurador externo puede usarla para adjuntar a una instancia de WebView específica. El formato de la canalización creada por el depurador debe ser: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` Where:

* `{app_name}` es el nombre de archivo exe de la aplicación host, por ejemplo, WebView2Example.exe

* `{pipe_name}` es el valor que se establece para WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.

Para habilitar la depuración de los destinos identificados por el JSON, también tendrá que establecer la variable de entorno WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS para enviar `--remote-debugging-port={port_num}` Dónde:

* `{port_num}` es el puerto al que se enlazará el servidor CDP.

Tenga en cuenta que el establecimiento de las variables de entorno WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER y WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS hará que las vistas previas hospedadas en la aplicación y su contenido se expongan a aplicaciones de terceros, como depuradores.

Nota: no hay ninguna clave de registro equivalente a esta variable de entorno.

Si no existe ninguna de esas variables de entorno, el registro se examinará a continuación. Se comprueban los siguientes valores de registro:

```
[{Root}]\Software\Policies\Microsoft\Edge\WebView2\browserExecutableFolder
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\releaseChannelPreference
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\additionalBrowserArguments
"{AppId}"=""

[{Root}]\Software\Policies\Microsoft\Edge\WebView2\userDataFolder
"{AppId}"=""
```

browserExecutableFolder y releaseChannelPreference se pueden configurar mediante la Directiva de grupo en plantillas administrativas > Microsoft Edge WebView2. La ubicación del registro anterior estará obsoleta pronto:

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

En el caso improbable, en el que algunas instancias de WebView se abren durante una actualización del explorador, podríamos acabar bloqueando la eliminación de los exploradores antiguos. Para evitar quedarse sin espacio en disco, se producirá un error en la creación de una vista Web nueva con el siguiente error si detecta que hay muchas versiones anteriores.

```
ERROR_DISK_FULL
```

El número máximo predeterminado de versiones de borde permitido es 20.

El número máximo de versiones anteriores de los bordes permitidos puede sobrescribirse con el valor de la siguiente variable de entorno.

```
WEBVIEW2_MAX_INSTANCES
```

Si la vista en WebView depende de un borde instalado y se desinstala, cualquier creación posterior producirá un error con el siguiente error

```
ERROR_PRODUCT_UNINSTALLED
```

En primer lugar, comprobamos la raíz como HKLM y, a continuación, HKCU. AppId se establece primero en el identificador de modelo de usuario de la aplicación del proceso de la llamada, y después, si no hay ninguna clave del registro correspondiente, el AppId se establece en el nombre del archivo ejecutable del proceso de la llamada o si no es una clave del registro y, a continuación, ' * '. Si se encuentra una clave del registro override, usamos los valores del registro browserExecutableFolder y userDataFolder como reemplazos y adjuntamos additionalBrowserArguments valores de registro para los valores correspondientes en CreateCoreWebView2EnvironmentWithOptions parámetros.

#### GetAvailableCoreWebView2BrowserVersionString 

> Public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr * versionInfo)

Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.

Los nombres de canal son beta, dev y Canarias. Si existe una invalidación para el browserExecutableFolder o la preferencia de canal, se usará el reemplazo. Si no hay un reemplazo, se usa el parámetro pasado a GetAvailableCoreWebView2BrowserVersionString.

