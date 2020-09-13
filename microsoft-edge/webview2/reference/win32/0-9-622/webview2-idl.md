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
# <span data-ttu-id="ff224-104">Global</span><span class="sxs-lookup"><span data-stu-id="ff224-104">Globals</span></span> 

## <span data-ttu-id="ff224-105">Resumen</span><span class="sxs-lookup"><span data-stu-id="ff224-105">Summary</span></span>

 <span data-ttu-id="ff224-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff224-106">Members</span></span>                        | <span data-ttu-id="ff224-107">Descripciones</span><span class="sxs-lookup"><span data-stu-id="ff224-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ff224-108">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="ff224-108">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="ff224-109">Este método es para cualquier persona que desee comparar la versión correctamente para determinar cuál es la versión más reciente, la anterior o la misma.</span><span class="sxs-lookup"><span data-stu-id="ff224-109">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="ff224-110">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="ff224-110">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="ff224-111">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="ff224-111">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="ff224-112">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="ff224-112">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="ff224-113">Exportación de archivos DLL para crear un entorno de WebView2 con una versión personalizada de Edge, directorio de datos de usuario o opciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="ff224-113">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="ff224-114">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="ff224-114">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="ff224-115">Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="ff224-115">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="ff224-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff224-116">Members</span></span>

#### <span data-ttu-id="ff224-117">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="ff224-117">CompareBrowserVersions</span></span> 

> <span data-ttu-id="ff224-118">público STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR VERSION1, PCWSTR version2, int \* result)</span><span class="sxs-lookup"><span data-stu-id="ff224-118">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="ff224-119">Este método es para cualquier persona que desee comparar la versión correctamente para determinar cuál es la versión más reciente, la anterior o la misma.</span><span class="sxs-lookup"><span data-stu-id="ff224-119">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="ff224-120">Puede usarse para determinar si usar webview2 o ciertas características de la base de la versión.</span><span class="sxs-lookup"><span data-stu-id="ff224-120">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="ff224-121">Establece el valor de result en-1, 0 o 1 si version1 es menor que, igual o mayor que version2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ff224-121">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="ff224-122">Devuelve E_INVALIDARG si no se puede analizar ninguna de las cadenas de versión o si cualquier parámetro de entrada es NULL.</span><span class="sxs-lookup"><span data-stu-id="ff224-122">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="ff224-123">La entrada puede usar directamente el versionInfo Obtenido de GetAvailableCoreWebView2BrowserVersionString, la información de canal se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="ff224-123">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="ff224-124">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="ff224-124">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="ff224-125">público STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environmentCreatedHandler)</span><span class="sxs-lookup"><span data-stu-id="ff224-125">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)(ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environmentCreatedHandler)</span></span>

<span data-ttu-id="ff224-126">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="ff224-126">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="ff224-127">Esto es equivalente a llamar a CreateCoreWebView2EnvironmentWithOptions con nullptr para browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="ff224-127">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="ff224-128">Para obtener más información, consulta CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="ff224-128">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="ff224-129">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="ff224-129">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="ff224-130">Public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environmentCreatedHandler)</span><span class="sxs-lookup"><span data-stu-id="ff224-130">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environmentCreatedHandler)</span></span>

<span data-ttu-id="ff224-131">Exportación de archivos DLL para crear un entorno de WebView2 con una versión personalizada de Edge, directorio de datos de usuario o opciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="ff224-131">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="ff224-132">El entorno WebView2 y todos los demás objetos WebView2 son de subproceso único y tienen dependencias en componentes de Windows que requieren que COM se inicialice para un apartamento de un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="ff224-132">The WebView2 environment and all other WebView2 objects are single threaded and have dependencies on Windows components that require COM to be initialized for a single-threaded apartment.</span></span> <span data-ttu-id="ff224-133">Se espera que la aplicación llame a CoInitializeEx antes de llamar a CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="ff224-133">The application is expected to call CoInitializeEx before calling CreateCoreWebView2EnvironmentWithOptions.</span></span>

```
CoInitializeEx(nullptr, COINIT_APARTMENTTHREADED);
```

<span data-ttu-id="ff224-134">Si no se llamó a CoInitializeEx o se ha llamado previamente con COINIT_MULTITHREADED, CreateCoreWebView2EnvironmentWithOptions producirá uno de los siguientes errores.</span><span class="sxs-lookup"><span data-stu-id="ff224-134">If CoInitializeEx was not called or has been previously called with COINIT_MULTITHREADED, CreateCoreWebView2EnvironmentWithOptions will fail with one of the following errors.</span></span>

```
CO_E_NOTINITIALIZED (if CoInitializeEx was not called)
RPC_E_CHANGED_MODE  (if CoInitializeEx was previously called with
                     COINIT_MULTITHREADED)
```

<span data-ttu-id="ff224-135">`browserExecutableFolder`Se usa para especificar si los controles de WebView2 usan una versión fija o instalada del motor en tiempo de ejecución de WebView2 que existe en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="ff224-135">Use `browserExecutableFolder` to specify whether WebView2 controls use a fixed or installed version of the WebView2 Runtime that exists on a client machine.</span></span> <span data-ttu-id="ff224-136">Para usar una versión fija del motor en tiempo de ejecución de WebView2, pase la ruta de acceso relativa de la carpeta que contiene la versión fija del motor en tiempo de ejecución de WebView2 `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="ff224-136">To use a fixed version of the WebView2 Runtime, pass the relative path of the folder that contains the fixed version of the WebView2 Runtime to `browserExecutableFolder`.</span></span> <span data-ttu-id="ff224-137">Para crear controles WebView2 que usen la versión instalada del motor en tiempo de ejecución de WebView2 que existe en los equipos cliente, pase una cadena nula o vacía a `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="ff224-137">To create WebView2 controls that use the installed version of the WebView2 Runtime that exists on client machines, pass a null or empty string to `browserExecutableFolder`.</span></span> <span data-ttu-id="ff224-138">En este escenario, la API intenta buscar una versión compatible del tiempo de ejecución de WebView2 que está instalada en el equipo cliente (en primer lugar, en el nivel de equipo y, a continuación, por usuario) con la preferencia de canal seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ff224-138">In this scenario, the API tries to find a compatible version of the WebView2 Runtime that is installed on the client machine (first at the machine level, and then per user) using the selected channel preference.</span></span> <span data-ttu-id="ff224-139">La ruta de acceso de la versión fija del tiempo de ejecución de WebView2 no debe contener `\Edge\Application\` .</span><span class="sxs-lookup"><span data-stu-id="ff224-139">The path of fixed version of the WebView2 Runtime should not contain `\Edge\Application\`.</span></span> <span data-ttu-id="ff224-140">Cuando se usa una ruta de acceso, la API generará un error con ERROR_NOT_SUPPORTED.</span><span class="sxs-lookup"><span data-stu-id="ff224-140">When such a path is used, the API will fail with ERROR_NOT_SUPPORTED.</span></span>

<span data-ttu-id="ff224-141">El orden de búsqueda de canales predeterminado es el tiempo de ejecución de WebView2, beta, dev y Canarias.</span><span class="sxs-lookup"><span data-stu-id="ff224-141">The default channel search order is the WebView2 Runtime, Beta, Dev, and Canary.</span></span> <span data-ttu-id="ff224-142">Cuando se produce una invalidación WEBVIEW2_RELEASE_CHANNEL_PREFERENCE variable de entorno o el valor de registro releaseChannelPreference aplicable con el valor de 1, se invierte el orden de búsqueda del canal.</span><span class="sxs-lookup"><span data-stu-id="ff224-142">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="ff224-143">userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2.</span><span class="sxs-lookup"><span data-stu-id="ff224-143">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="ff224-144">La ruta de acceso puede ser una ruta de acceso de archivo absoluta o una ruta de acceso relativa del archivo que se interprete como relativa al archivo ejecutable del proceso actual.</span><span class="sxs-lookup"><span data-stu-id="ff224-144">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="ff224-145">De lo contrario, para las aplicaciones para UWP, la carpeta de datos de usuario predeterminada será la carpeta de datos de la aplicación para el paquete; para las aplicaciones que no son UWP, la carpeta datos de usuario predeterminada se `{Executable File Name}.WebView2` creará en el mismo directorio junto al ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ff224-145">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="ff224-146">Se puede producir un error en la creación de WebView2 si el ejecutable se ejecuta en un directorio que el proceso no tiene permiso para crear una carpeta nueva en.</span><span class="sxs-lookup"><span data-stu-id="ff224-146">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="ff224-147">La aplicación es responsable de limpiar su carpeta de datos de usuario cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="ff224-147">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="ff224-148">Tenga en cuenta que, dado que un proceso de explorador puede compartirse entre las vistas de las web, la creación de WebView no funcionará con HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) si las opciones especificadas no coinciden con las opciones de las vistas previas que se están ejecutando en el proceso del explorador compartido.</span><span class="sxs-lookup"><span data-stu-id="ff224-148">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="ff224-149">environmentCreatedHandler es el resultado de controlador para la operación asincrónica, que contendrá el WebView2Environment que se creó.</span><span class="sxs-lookup"><span data-stu-id="ff224-149">environmentCreatedHandler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="ff224-150">Los valores especificados en las variables de entorno o en el registro pueden invalidar browserExecutableFolder, userDataFolder y additionalBrowserArguments de la environmentOptions.</span><span class="sxs-lookup"><span data-stu-id="ff224-150">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="ff224-151">Al crear un WebView2Environment, se comprueban las siguientes variables de entorno:</span><span class="sxs-lookup"><span data-stu-id="ff224-151">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="ff224-152">Si se encuentra una variable de entorno override, usamos los valores browserExecutableFolder y userDataFolder como reemplazos de los valores correspondientes en CreateCoreWebView2EnvironmentWithOptions parámetros.</span><span class="sxs-lookup"><span data-stu-id="ff224-152">If an override environment variable is found then we use the browserExecutableFolder and userDataFolder values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span> <span data-ttu-id="ff224-153">Si additionalBrowserArguments se especifica en la variable de entorno o en el registro, se anexará a los valores de correspinding en parámetros de CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="ff224-153">If additionalBrowserArguments specified in environment variable or in the registry, it will be appended to the correspinding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="ff224-154">Aunque no se invaliden estrictamente, existen variables de entorno adicionales que se pueden establecer:</span><span class="sxs-lookup"><span data-stu-id="ff224-154">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="ff224-155">Cuando se encuentra con un valor que no está vacío, indica que WebView se está iniciando bajo un depurador de scripts.</span><span class="sxs-lookup"><span data-stu-id="ff224-155">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="ff224-156">En este caso, WebView emitirá un `Page.waitForDebugger` comando CDP que hará que la ejecución de scripts dentro de la vista de WebView se PAUSE al iniciarse, hasta que un depurador emita el `Runtime.runIfWaitingForDebugger` comando CDP correspondiente para reanudar la ejecución.</span><span class="sxs-lookup"><span data-stu-id="ff224-156">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="ff224-157">Nota: no hay ninguna clave de registro equivalente a esta variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="ff224-157">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="ff224-158">Cuando se encuentra con un valor que no está vacío, indica que WebView se está iniciando bajo un depurador de scripts que también es compatible con aplicaciones host que usan varias vistas previas.</span><span class="sxs-lookup"><span data-stu-id="ff224-158">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="ff224-159">El valor se usa como identificador de una canalización con nombre que se abrirá y se escribirá cuando la aplicación host cree un nuevo WebView.</span><span class="sxs-lookup"><span data-stu-id="ff224-159">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="ff224-160">La carga coincidirá con la del destino JSON del puerto de depuración remota y el depurador externo puede usarla para adjuntar a una instancia de WebView específica.</span><span class="sxs-lookup"><span data-stu-id="ff224-160">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="ff224-161">El formato de la canalización creada por el depurador debe ser: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` Where:</span><span class="sxs-lookup"><span data-stu-id="ff224-161">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="ff224-162">es el nombre de archivo exe de la aplicación host, por ejemplo, WebView2Example.exe</span><span class="sxs-lookup"><span data-stu-id="ff224-162">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="ff224-163">es el valor que se establece para WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span><span class="sxs-lookup"><span data-stu-id="ff224-163">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="ff224-164">Para habilitar la depuración de los destinos identificados por el JSON, también tendrá que establecer la variable de entorno WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS para enviar `--remote-debugging-port={port_num}` Dónde:</span><span class="sxs-lookup"><span data-stu-id="ff224-164">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="ff224-165">es el puerto al que se enlazará el servidor CDP.</span><span class="sxs-lookup"><span data-stu-id="ff224-165">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="ff224-166">Tenga en cuenta que el establecimiento de las variables de entorno WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER y WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS hará que las vistas previas hospedadas en la aplicación y su contenido se expongan a aplicaciones de terceros, como depuradores.</span><span class="sxs-lookup"><span data-stu-id="ff224-166">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="ff224-167">Nota: no hay ninguna clave de registro equivalente a esta variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="ff224-167">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="ff224-168">Si no existe ninguna de esas variables de entorno, el registro se examinará a continuación.</span><span class="sxs-lookup"><span data-stu-id="ff224-168">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="ff224-169">Se comprueban los siguientes valores de registro:</span><span class="sxs-lookup"><span data-stu-id="ff224-169">The following registry values are checked:</span></span>

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

<span data-ttu-id="ff224-170">browserExecutableFolder y releaseChannelPreference se pueden configurar mediante la Directiva de grupo en plantillas administrativas > Microsoft Edge WebView2.</span><span class="sxs-lookup"><span data-stu-id="ff224-170">browserExecutableFolder and releaseChannelPreference can be configured using group policy under Administrative Templates > Microsoft Edge WebView2.</span></span> <span data-ttu-id="ff224-171">La ubicación del registro anterior estará obsoleta pronto:</span><span class="sxs-lookup"><span data-stu-id="ff224-171">The old registry location will be deprecated soon:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="ff224-172">En el caso improbable, en el que algunas instancias de WebView se abren durante una actualización del explorador, podríamos acabar bloqueando la eliminación de los exploradores antiguos.</span><span class="sxs-lookup"><span data-stu-id="ff224-172">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="ff224-173">Para evitar quedarse sin espacio en disco, se producirá un error en la creación de una vista Web nueva con el siguiente error si detecta que hay muchas versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="ff224-173">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="ff224-174">El número máximo predeterminado de versiones de borde permitido es 20.</span><span class="sxs-lookup"><span data-stu-id="ff224-174">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="ff224-175">El número máximo de versiones anteriores de los bordes permitidos puede sobrescribirse con el valor de la siguiente variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="ff224-175">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="ff224-176">Si la vista en WebView depende de un borde instalado y se desinstala, cualquier creación posterior producirá un error con el siguiente error</span><span class="sxs-lookup"><span data-stu-id="ff224-176">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="ff224-177">En primer lugar, comprobamos la raíz como HKLM y, a continuación, HKCU.</span><span class="sxs-lookup"><span data-stu-id="ff224-177">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="ff224-178">AppId se establece primero en el identificador de modelo de usuario de la aplicación del proceso de la llamada, y después, si no hay ninguna clave del registro correspondiente, el AppId se establece en el nombre del archivo ejecutable del proceso de la llamada o si no es una clave del registro y, a continuación, ' \* '.</span><span class="sxs-lookup"><span data-stu-id="ff224-178">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="ff224-179">Si se encuentra una clave del registro override, usamos los valores del registro browserExecutableFolder y userDataFolder como reemplazos y adjuntamos additionalBrowserArguments valores de registro para los valores correspondientes en CreateCoreWebView2EnvironmentWithOptions parámetros.</span><span class="sxs-lookup"><span data-stu-id="ff224-179">If an override registry key is found, then we use the browserExecutableFolder and userDataFolder registry values as replacements and append additionalBrowserArguments registry values for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="ff224-180">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="ff224-180">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="ff224-181">Public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="ff224-181">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="ff224-182">Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="ff224-182">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="ff224-183">Los nombres de canal son beta, dev y Canarias.</span><span class="sxs-lookup"><span data-stu-id="ff224-183">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="ff224-184">Si existe una invalidación para el browserExecutableFolder o la preferencia de canal, se usará el reemplazo.</span><span class="sxs-lookup"><span data-stu-id="ff224-184">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="ff224-185">Si no hay un reemplazo, se usa el parámetro pasado a GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="ff224-185">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>
