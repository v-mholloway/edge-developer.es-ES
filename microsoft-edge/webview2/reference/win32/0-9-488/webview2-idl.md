---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ Globals
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 1134aa10717dfc5be8ef1a4de5805a3fc319aeb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883801"
---
# <span data-ttu-id="c7e9e-104">0.9.515-Globals</span><span class="sxs-lookup"><span data-stu-id="c7e9e-104">0.9.515 - Globals</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

## <span data-ttu-id="c7e9e-105">Resumen</span><span class="sxs-lookup"><span data-stu-id="c7e9e-105">Summary</span></span>

 <span data-ttu-id="c7e9e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c7e9e-106">Members</span></span>                        | <span data-ttu-id="c7e9e-107">Descripciones</span><span class="sxs-lookup"><span data-stu-id="c7e9e-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c7e9e-108">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="c7e9e-108">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="c7e9e-109">Este método es para cualquier persona que desee comparar la versión correctamente para determinar cuál es la versión más reciente, la anterior o la misma.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-109">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="c7e9e-110">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="c7e9e-110">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="c7e9e-111">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-111">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="c7e9e-112">CreateCoreWebView2EnvironmentWithDetails</span><span class="sxs-lookup"><span data-stu-id="c7e9e-112">CreateCoreWebView2EnvironmentWithDetails</span></span>](#createcorewebview2environmentwithdetails) | <span data-ttu-id="c7e9e-113">Esta API se eliminará en la próxima versión del SDK.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-113">This API is going to be removed in next SDK release.</span></span>
[<span data-ttu-id="c7e9e-114">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="c7e9e-114">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="c7e9e-115">Exportación de archivos DLL para crear un entorno de WebView2 con una versión personalizada de Edge, directorio de datos de usuario o opciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-115">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="c7e9e-116">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="c7e9e-116">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="c7e9e-117">Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-117">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="c7e9e-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="c7e9e-118">Members</span></span>

#### <span data-ttu-id="c7e9e-119">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="c7e9e-119">CompareBrowserVersions</span></span> 

> <span data-ttu-id="c7e9e-120">público STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR VERSION1, PCWSTR version2, int \* result)</span><span class="sxs-lookup"><span data-stu-id="c7e9e-120">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="c7e9e-121">Este método es para cualquier persona que desee comparar la versión correctamente para determinar cuál es la versión más reciente, la anterior o la misma.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-121">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="c7e9e-122">Puede usarse para determinar si usar webview2 o ciertas características de la base de la versión.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-122">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="c7e9e-123">Establece el valor de result en-1, 0 o 1 si version1 es menor que, igual o mayor que version2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-123">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="c7e9e-124">Devuelve E_INVALIDARG si no se puede analizar ninguna de las cadenas de versión o si cualquier parámetro de entrada es NULL.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-124">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="c7e9e-125">La entrada puede usar directamente el versionInfo Obtenido de GetAvailableCoreWebView2BrowserVersionString, la información de canal se pasará por alto.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-125">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="c7e9e-126">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="c7e9e-126">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="c7e9e-127">público STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="c7e9e-127">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="c7e9e-128">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-128">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="c7e9e-129">Esto es equivalente a llamar a CreateCoreWebView2EnvironmentWithOptions con nullptr para browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-129">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="c7e9e-130">Para obtener más información, consulta CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-130">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="c7e9e-131">CreateCoreWebView2EnvironmentWithDetails</span><span class="sxs-lookup"><span data-stu-id="c7e9e-131">CreateCoreWebView2EnvironmentWithDetails</span></span> 

> <span data-ttu-id="c7e9e-132">Public STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR USERDATAFOLDER, PCWSTR additionalBrowserArguments, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environment_created_handler](icorewebview2createcorewebview2environmentcompletedhandler.md) )</span><span class="sxs-lookup"><span data-stu-id="c7e9e-132">public STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, PCWSTR additionalBrowserArguments, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="c7e9e-133">Esta API se eliminará en la próxima versión del SDK.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-133">This API is going to be removed in next SDK release.</span></span>

<span data-ttu-id="c7e9e-134">Usa CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-134">Please use CreateCoreWebView2EnvironmentWithOptions.</span></span>

#### <span data-ttu-id="c7e9e-135">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="c7e9e-135">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="c7e9e-136">Public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="c7e9e-136">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="c7e9e-137">Exportación de archivos DLL para crear un entorno de WebView2 con una versión personalizada de Edge, directorio de datos de usuario o opciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-137">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="c7e9e-138">browserExecutableFolder es la ruta de acceso relativa a la carpeta que contiene el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-138">browserExecutableFolder is the relative path to the folder that contains the embedded Edge.</span></span> <span data-ttu-id="c7e9e-139">El borde incrustado se puede obtener copiando la carpeta con el nombre de la versión de un borde instalado, como 73.0.52.0 subcarpeta de un borde de 73.0.52.0 instalado.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-139">The embedded Edge can be obtained by copying the version named folder of an installed Edge, like 73.0.52.0 sub folder of an installed 73.0.52.0 Edge.</span></span> <span data-ttu-id="c7e9e-140">La carpeta debería tener msedge.exe, msedge.dll y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-140">The folder should have msedge.exe, msedge.dll, and so on.</span></span> <span data-ttu-id="c7e9e-141">Use null o una cadena vacía para browserExecutableFolder para crear una vista de usuario con Edge instalado en el equipo, en cuyo caso la API intentará buscar una versión compatible de Edge instalada en el equipo según la preferencia de canal intentando buscar primero por instalación de usuario y, después, por instalación de equipo.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-141">Use null or empty string for browserExecutableFolder to create WebView using Edge installed on the machine, in which case the API will try to find a compatible version of Edge installed on the machine according to the channel preference trying to find first per user install and then per machine install.</span></span>

<span data-ttu-id="c7e9e-142">El orden de búsqueda de canales predeterminado es estable, beta, dev y Canarias.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-142">The default channel search order is stable, beta, dev, and canary.</span></span> <span data-ttu-id="c7e9e-143">Cuando se produce una invalidación WEBVIEW2_RELEASE_CHANNEL_PREFERENCE variable de entorno o el valor de registro releaseChannelPreference aplicable con el valor de 1, se invierte el orden de búsqueda del canal.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-143">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="c7e9e-144">userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-144">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="c7e9e-145">La ruta de acceso puede ser una ruta de acceso de archivo absoluta o una ruta de acceso relativa del archivo que se interprete como relativa al archivo ejecutable del proceso actual.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-145">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="c7e9e-146">De lo contrario, para las aplicaciones para UWP, la carpeta de datos de usuario predeterminada será la carpeta de datos de la aplicación para el paquete; para las aplicaciones que no son UWP, la carpeta datos de usuario predeterminada se `{Executable File Name}.WebView2` creará en el mismo directorio junto al ejecutable de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-146">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="c7e9e-147">Se puede producir un error en la creación de WebView2 si el ejecutable se ejecuta en un directorio que el proceso no tiene permiso para crear una carpeta nueva en.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-147">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="c7e9e-148">La aplicación es responsable de limpiar su carpeta de datos de usuario cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-148">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="c7e9e-149">Tenga en cuenta que, dado que un proceso de explorador puede compartirse entre las vistas de las web, la creación de WebView no funcionará con HRESULT_FROM_WIN32 (ERROR_INVALID_STATE) si las opciones especificadas no coinciden con las opciones de las vistas previas que se están ejecutando en el proceso del explorador compartido.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-149">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="c7e9e-150">environment_created_handler es el resultado de controlador para la operación asincrónica, que contendrá la WebView2Environment que se creó.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-150">environment_created_handler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="c7e9e-151">Los valores especificados en las variables de entorno o en el registro pueden invalidar browserExecutableFolder, userDataFolder y additionalBrowserArguments de la environmentOptions.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-151">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="c7e9e-152">Al crear un WebView2Environment, se comprueban las siguientes variables de entorno:</span><span class="sxs-lookup"><span data-stu-id="c7e9e-152">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="c7e9e-153">Si se encuentra una variable de entorno override, usamos los valores browserExecutableFolder, userDataFolder y additionalBrowserArguments como reemplazos de los valores correspondientes en CreateCoreWebView2EnvironmentWithOptions Parameters.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-153">If an override environment variable is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="c7e9e-154">Aunque no se invaliden estrictamente, existen variables de entorno adicionales que se pueden establecer:</span><span class="sxs-lookup"><span data-stu-id="c7e9e-154">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="c7e9e-155">Cuando se encuentra con un valor que no está vacío, indica que WebView se está iniciando bajo un depurador de scripts.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-155">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="c7e9e-156">En este caso, WebView emitirá un `Page.waitForDebugger` comando CDP que hará que la ejecución de scripts dentro de la vista de WebView se PAUSE al iniciarse, hasta que un depurador emita el `Runtime.runIfWaitingForDebugger` comando CDP correspondiente para reanudar la ejecución.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-156">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="c7e9e-157">Nota: no hay ninguna clave de registro equivalente a esta variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-157">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="c7e9e-158">Cuando se encuentra con un valor que no está vacío, indica que WebView se está iniciando bajo un depurador de scripts que también es compatible con aplicaciones host que usan varias vistas previas.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-158">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="c7e9e-159">El valor se usa como identificador de una canalización con nombre que se abrirá y se escribirá cuando la aplicación host cree un nuevo WebView.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-159">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="c7e9e-160">La carga coincidirá con la del destino JSON del puerto de depuración remota y el depurador externo puede usarla para adjuntar a una instancia de WebView específica.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-160">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="c7e9e-161">El formato de la canalización creada por el depurador debe ser: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` Where:</span><span class="sxs-lookup"><span data-stu-id="c7e9e-161">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="c7e9e-162">es el nombre de archivo exe de la aplicación host, por ejemplo, WebView2Example.exe</span><span class="sxs-lookup"><span data-stu-id="c7e9e-162">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="c7e9e-163">es el valor que se establece para WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-163">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="c7e9e-164">Para habilitar la depuración de los destinos identificados por el JSON, también tendrá que establecer la variable de entorno WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS para enviar `--remote-debugging-port={port_num}` Dónde:</span><span class="sxs-lookup"><span data-stu-id="c7e9e-164">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="c7e9e-165">es el puerto al que se enlazará el servidor CDP.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-165">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="c7e9e-166">Tenga en cuenta que el establecimiento de las variables de entorno WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER y WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS hará que las vistas previas hospedadas en la aplicación y su contenido se expongan a aplicaciones de terceros, como depuradores.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-166">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="c7e9e-167">Nota: no hay ninguna clave de registro equivalente a esta variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-167">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="c7e9e-168">Si no existe ninguna de esas variables de entorno, el registro se examinará a continuación.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-168">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="c7e9e-169">Se comprueban las siguientes claves del registro:</span><span class="sxs-lookup"><span data-stu-id="c7e9e-169">The following registry keys are checked:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="c7e9e-170">En el caso improbable, en el que algunas instancias de WebView se abren durante una actualización del explorador, podríamos acabar bloqueando la eliminación de los exploradores antiguos.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-170">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="c7e9e-171">Para evitar quedarse sin espacio en disco, se producirá un error en la creación de una vista Web nueva con el siguiente error si detecta que hay muchas versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-171">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="c7e9e-172">El número máximo predeterminado de versiones de borde permitido es 20.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-172">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="c7e9e-173">El número máximo de versiones anteriores de los bordes permitidos puede sobrescribirse con el valor de la siguiente variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-173">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="c7e9e-174">Si la vista en WebView depende de un borde instalado y se desinstala, cualquier creación posterior producirá un error con el siguiente error</span><span class="sxs-lookup"><span data-stu-id="c7e9e-174">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="c7e9e-175">En primer lugar, comprobamos la raíz como HKLM y, a continuación, HKCU.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-175">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="c7e9e-176">AppId se establece primero en el identificador de modelo de usuario de la aplicación del proceso de la llamada, y después, si no hay ninguna clave del registro correspondiente, el AppId se establece en el nombre del archivo ejecutable del proceso de la llamada o si no es una clave del registro y, a continuación, ' \* '.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-176">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="c7e9e-177">Si se encuentra una clave de registro override, usamos los valores de registro browserExecutableFolder, userDataFolder y additionalBrowserArguments como reemplazos de los valores correspondientes en CreateCoreWebView2EnvironmentWithOptions Parameters.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-177">If an override registry key is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments registry values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="c7e9e-178">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="c7e9e-178">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="c7e9e-179">Public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="c7e9e-179">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="c7e9e-180">Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-180">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="c7e9e-181">Los nombres de canal son beta, dev y Canarias.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-181">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="c7e9e-182">Si existe una invalidación para el browserExecutableFolder o la preferencia de canal, se usará el reemplazo.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-182">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="c7e9e-183">Si no hay un reemplazo, se usa el parámetro pasado a GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="c7e9e-183">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>

