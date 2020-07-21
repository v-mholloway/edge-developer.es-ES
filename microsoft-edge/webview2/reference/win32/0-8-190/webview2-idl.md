---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ Globals
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge
ms.openlocfilehash: f413a9ed3afb6360637abead62a3aee20fd23cea
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884641"
---
# 0.8.355-Globals 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

## Resumen

 Miembros                        | Descripciones
--------------------------------|---------------------------------------------
[CreateWebView2EnvironmentWithDetails](#createwebview2environmentwithdetails) | Exportación de archivos DLL para crear un entorno de WebView2 con una versión personalizada de Edge, directorio de datos de usuario o conmutadores de explorador adicionales.
[CreateWebView2Environment](#createwebview2environment) | Crea un entorno de WebView2 de perenne con la versión de Edge instalada.
[GetWebView2BrowserVersionInfo](#getwebview2browserversioninfo) | Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.
[CompareBrowserVersions](#comparebrowserversions) | Este método es para cualquier persona que desee comparar la versión correctamente para determinar cuál es la versión más reciente, la anterior o la misma.

## Miembros

#### CreateWebView2EnvironmentWithDetails 

> Public STDAPI [CreateWebView2EnvironmentWithDetails](#createwebview2environmentwithdetails)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR USERDATAFOLDER, PCWSTR additionalBrowserArguments,[IWebView2CreateWebView2EnvironmentCompletedHandler * environment_created_handler](IWebView2CreateWebView2EnvironmentCompletedHandler.md) )

Exportación de archivos DLL para crear un entorno de WebView2 con una versión personalizada de Edge, directorio de datos de usuario o conmutadores de explorador adicionales.

browserExecutableFolder es la ruta de acceso relativa a la carpeta que contiene el borde incrustado. El borde incrustado se puede obtener copiando la carpeta con el nombre de la versión de un borde instalado, como 73.0.52.0 subcarpeta de un borde de 73.0.52.0 instalado. La carpeta debería tener msedge.exe, msedge.dll, etc. Use null o una cadena vacía para browserExecutableFolder para crear una vista de usuario con Edge instalado en el equipo, en cuyo caso la API intentará buscar una versión compatible de Edge instalada en el equipo según la preferencia de canal intentando buscar primero por instalación de usuario y, después, por instalación de equipo.

El orden de búsqueda de canales predeterminado es estable, beta, dev y Canarias. Cuando se produce una invalidación WEBVIEW2_RELEASE_CHANNEL_PREFERENCE variable de entorno o el valor de registro releaseChannelPreference aplicable con el valor de 1, se invierte el orden de búsqueda del canal.

userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2. La ruta de acceso puede ser una ruta de acceso de archivo absoluta o una ruta de acceso relativa del archivo que se interprete como relativa al archivo ejecutable del proceso actual. De lo contrario, para las aplicaciones para UWP, la carpeta de datos de usuario predeterminada será la carpeta de datos de la aplicación para el paquete; para las aplicaciones que no son UWP, la carpeta datos de usuario predeterminada se `{Executable File Name}.WebView2` creará en el mismo directorio junto al ejecutable de la aplicación. Se puede producir un error en la creación de WebView2 si el ejecutable se ejecuta en un directorio que el proceso no tiene permiso para crear una carpeta nueva en. La aplicación es responsable de limpiar su carpeta de datos de usuario cuando haya terminado.

additionalBrowserArguments se puede especificar para cambiar el comportamiento de la vista en WebView. Se pasarán al proceso de explorador como parte de la línea de comandos. Consulte [Ejecutar cromo con marcas](https://aka.ms/RunChromiumWithFlags) para obtener más información acerca de los modificadores de la línea de comandos para el proceso del explorador. Si la aplicación se inicia con un modificador de línea de comandos, `--edge-webview-switches=xxx` el valor de ese modificador (XXX en el ejemplo anterior) también se anexará a la línea de comandos del proceso del explorador. Algunos conmutadores como los `--user-data-dir` de WebView son internos y importantes. Estos conmutadores se ignorarán incluso si se especifican. Si se especifican los mismos modificadores varias veces, se gana la última. Tenga en cuenta que esto también se aplica a los conmutadores como `--enable-features` . No se intenta combinar los distintos valores del mismo modificador. El valor de la línea de comandos del proceso de la aplicación `--edge-webview-switches` se procesa después de que se procese el parámetro additionalBrowserArguments. Además, tenga en cuenta que, dado que un proceso de explorador puede compartirse entre las vistas Web, no se garantiza la aplicación de los modificadores, excepto para la primera vista Web que inicia el proceso de explorador. Si se produjo un error de análisis en los modificadores especificados, se ignorarán. `nullptr` ejecutará el proceso del explorador sin marcadores.

environment_created_handler es el resultado de controlador para la operación asincrónica, que contendrá la WebView2Environment que se creó.

Los miembros browserExecutableFolder, userDataFolder y additionalBrowserArguments de la environmentParams pueden reemplazarse por valores especificados en variables de entorno o en el registro.

Al crear un WebView2Environment, se comprueban las siguientes variables de entorno:

```cpp
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

Si se encuentra una variable de entorno override, usamos los valores browserExecutableFolder, userDataFolder y additionalBrowserArguments como reemplazos de los valores correspondientes en CreateWebView2EnvironmentWithDetails Parameters.

Aunque no se invaliden estrictamente, existen variables de entorno adicionales que se pueden establecer:

```cpp
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

Cuando se encuentra con un valor que no está vacío, indica que WebView se está iniciando bajo un depurador de scripts. En este caso, WebView emitirá un `Page.waitForDebugger` comando CDP que hará que la ejecución de scripts dentro de la vista de WebView se PAUSE al iniciarse, hasta que un depurador emita el `Runtime.runIfWaitingForDebugger` comando CDP correspondiente para reanudar la ejecución. Nota: no hay ninguna clave de registro equivalente a esta variable de entorno.

```cpp
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

Cuando se encuentra con un valor que no está vacío, indica que WebView se está iniciando bajo un depurador de scripts que también es compatible con aplicaciones host que usan varias vistas previas. El valor se usa como identificador de una canalización con nombre que se abrirá y se escribirá cuando la aplicación host cree un nuevo WebView. La carga coincidirá con la del destino JSON del puerto de depuración remota y el depurador externo puede usarla para adjuntar a una instancia de WebView específica. El formato de la canalización creada por el depurador debe ser: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` Where:

* `{app_name}` es el nombre de archivo exe de la aplicación host, por ejemplo, WebView2Example.exe

* `{pipe_name}` es el valor que se establece para WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.

Para habilitar la depuración de los destinos identificados por el JSON, también tendrá que establecer la variable de entorno WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS para enviar `--remote-debugging-port={port_num}` Dónde:

* `{port_num}` es el puerto al que se enlazará el servidor CDP.

Tenga en cuenta que el establecimiento de las variables de entorno WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER y WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS hará que las vistas previas hospedadas en la aplicación y su contenido se expongan a aplicaciones de terceros, como depuradores.

Nota: no hay ninguna clave de registro equivalente a esta variable de entorno.

Si no existe ninguna de esas variables de entorno, el registro se examinará a continuación. Se comprueban las siguientes claves del registro:

```cpp
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

En el caso improbable, en el que algunas instancias de WebView se abren durante una actualización del explorador, podríamos acabar bloqueando la eliminación de los exploradores antiguos. Para evitar quedarse sin espacio en disco, se producirá un error en la creación de una vista Web nueva con el siguiente error si detecta que hay muchas versiones anteriores.

```cpp
ERROR_DISK_FULL
```

El número máximo predeterminado de versiones de borde permitido es 20.

El número máximo de versiones anteriores de los bordes permitidos puede sobrescribirse con el valor de la siguiente variable de entorno.

```cpp
WEBVIEW2_MAX_INSTANCES
```

Si la vista en WebView depende de un borde instalado y se desinstala, cualquier creación posterior producirá un error con el siguiente error

```cpp
ERROR_PRODUCT_UNINSTALLED
```

En primer lugar, comprobamos la raíz como HKLM y, a continuación, HKCU. AppId se establece primero en el identificador de modelo de usuario de la aplicación del proceso de la llamada, y después, si no hay ninguna clave del registro correspondiente, el AppId se establece en el nombre del archivo ejecutable del proceso de la llamada o si no es una clave del registro y, a continuación, ' * '. Si se encuentra una clave de registro override, usamos los valores de registro browserExecutableFolder, userDataFolder y additionalBrowserArguments como reemplazos de los valores correspondientes en CreateWebView2EnvironmentWithDetails Parameters. Si alguno de esos valores de registro no está presente, el parámetro que se pasa a CreateWebView2Environment se usa.

#### CreateWebView2Environment 

> público STDAPI [CreateWebView2Environment](#createwebview2environment)([IWebView2CreateWebView2EnvironmentCompletedHandler](IWebView2CreateWebView2EnvironmentCompletedHandler.md) * environment_created_handler)

Crea un entorno de WebView2 de perenne con la versión de Edge instalada.

Esto es equivalente a llamar a CreateWebView2EnvironmentWithDetails con nullptr para browserExecutableFolder, userDataFolder, additionalBrowserArguments. Para obtener más información, consulta CreateWebView2EnvironmentWithDetails.

#### GetWebView2BrowserVersionInfo 

> Public STDAPI [GetWebView2BrowserVersionInfo](#getwebview2browserversioninfo)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr * versionInfo)

Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.

Los nombres de canal son beta, dev y Canarias. Si existe una invalidación para el browserExecutableFolder o la preferencia de canal, se usará el reemplazo. Si no hay un reemplazo, se usa el parámetro pasado a GetWebView2BrowserVersionInfo.

#### CompareBrowserVersions 

> público STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR VERSION1, PCWSTR version2, int * result)

Este método es para cualquier persona que desee comparar la versión correctamente para determinar cuál es la versión más reciente, la anterior o la misma.

Puede usarse para determinar si usar webview2 o ciertas características de la base de la versión. Establece el valor de result en-1, 0 o 1 si version1 es menor que, igual o mayor que version2, respectivamente. Devuelve E_INVALIDARG si no se puede analizar ninguna de las cadenas de versión o si cualquier parámetro de entrada es NULL. La entrada puede usar directamente el versionInfo Obtenido de GetWebView2BrowserVersionInfo, la información de canal se pasará por alto.

