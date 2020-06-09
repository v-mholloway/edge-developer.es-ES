---
description: Hospedar contenido web en la aplicación Win32 con el control Microsoft Edge WebView2
title: Microsoft Edge WebView2 para aplicaciones Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, aplicaciones Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, control de explorador, HTML Edge
ms.openlocfilehash: 3af7c02f51a203e434c92bac5219dc4db58f406b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699322"
---
# <span data-ttu-id="bec38-104">Clase Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="bec38-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="bec38-105">Espacio de nombres: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="bec38-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="bec38-106">Ensamblado: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="bec38-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="bec38-107">Esto representa el entorno de WebView2.</span><span class="sxs-lookup"><span data-stu-id="bec38-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="bec38-108">Resumen</span><span class="sxs-lookup"><span data-stu-id="bec38-108">Summary</span></span>

 <span data-ttu-id="bec38-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bec38-109">Members</span></span>                        | <span data-ttu-id="bec38-110">Descripciones</span><span class="sxs-lookup"><span data-stu-id="bec38-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bec38-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="bec38-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="bec38-112">Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="bec38-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="bec38-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="bec38-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="bec38-114">El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="bec38-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="bec38-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="bec38-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="bec38-116">Compare las versiones del explorador correctamente para determinar qué versión es la más reciente, la anterior o la misma.</span><span class="sxs-lookup"><span data-stu-id="bec38-116">Compare browser versions correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="bec38-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="bec38-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="bec38-118">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="bec38-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="bec38-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="bec38-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="bec38-120">Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.</span><span class="sxs-lookup"><span data-stu-id="bec38-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="bec38-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="bec38-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="bec38-122">Cree de forma asincrónica una nueva vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="bec38-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="bec38-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="bec38-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="bec38-124">Cree un CoreWebView2ExperimentalPointerInfo vacío.</span><span class="sxs-lookup"><span data-stu-id="bec38-124">Create an empty CoreWebView2ExperimentalPointerInfo.</span></span>
[<span data-ttu-id="bec38-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="bec38-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="bec38-126">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="bec38-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="bec38-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="bec38-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="bec38-128">Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="bec38-128">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>
[<span data-ttu-id="bec38-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="bec38-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="bec38-130">Devuelve el proveedor de automatización de la interfaz de usuario de la CoreWebView2CompositionController que se corresponde con el HWND dado.</span><span class="sxs-lookup"><span data-stu-id="bec38-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="bec38-131">Las vistas web creadas a partir de un entorno se ejecutan en el proceso del explorador especificado con los parámetros de entorno y los objetos creados a partir de un entorno se deben usar en el mismo entorno.</span><span class="sxs-lookup"><span data-stu-id="bec38-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="bec38-132">No se garantiza que su uso en diferentes entornos sea compatible y podría fallar.</span><span class="sxs-lookup"><span data-stu-id="bec38-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="bec38-133">Miembros</span><span class="sxs-lookup"><span data-stu-id="bec38-133">Members</span></span>

#### <span data-ttu-id="bec38-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="bec38-134">BrowserVersionString</span></span> 

<span data-ttu-id="bec38-135">Información de versión del explorador del CoreWebView2Environment actual, incluido el nombre del canal si no es el canal estable.</span><span class="sxs-lookup"><span data-stu-id="bec38-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="bec38-136">cadena pública [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="bec38-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="bec38-137">Coincide con el formato de la API de GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="bec38-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="bec38-138">Los nombres de los canales son ' beta ', ' dev ' y ' Canarias '.</span><span class="sxs-lookup"><span data-stu-id="bec38-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="bec38-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="bec38-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="bec38-140">El evento NewBrowserVersionAvailable se desencadena cuando se instala una versión más reciente del explorador Edge y está disponible para usarla a través de WebView2.</span><span class="sxs-lookup"><span data-stu-id="bec38-140">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="bec38-141">evento público EventHandler< > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="bec38-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="bec38-142">Para usar la versión más reciente del explorador, debe crear un entorno y una vista Web nuevos.</span><span class="sxs-lookup"><span data-stu-id="bec38-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="bec38-143">Este evento solo se activará para la nueva versión desde el mismo canal de borde desde el que se está ejecutando el código.</span><span class="sxs-lookup"><span data-stu-id="bec38-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="bec38-144">Cuando no se esté ejecutando con Edge instalado, no se desencadenará ningún evento.</span><span class="sxs-lookup"><span data-stu-id="bec38-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="bec38-145">Puesto que una carpeta datos de usuario solo puede ser usada por un único proceso del explorador a la vez, si desea usar la misma carpeta datos de usuario en las vistas web con la nueva versión del explorador, debe cerrar primero el entorno y las vistas de web que usan la versión anterior del explorador.</span><span class="sxs-lookup"><span data-stu-id="bec38-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="bec38-146">O simplemente pide al usuario que reinicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bec38-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="bec38-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="bec38-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="bec38-148">Compare las versiones del explorador correctamente para determinar qué versión es la más reciente, la anterior o la misma.</span><span class="sxs-lookup"><span data-stu-id="bec38-148">Compare browser versions correctly to determine which version is newer, older or same.</span></span>

> <span data-ttu-id="bec38-149">public static int [CompareBrowserVersions](#comparebrowserversions)(cadena version1, String version2)</span><span class="sxs-lookup"><span data-stu-id="bec38-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="bec38-150">Devuelve-1, 0 o 1 en función de si version1 es menor, igual o mayor que version2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bec38-150">Returns -1, 0 or 1 depending on whether version1 is less than, equal to or greater than version2, respectively.</span></span>

##### <span data-ttu-id="bec38-151">Parameters</span><span class="sxs-lookup"><span data-stu-id="bec38-151">Parameters</span></span>
* `version1` <span data-ttu-id="bec38-152">Una de las cadenas de versión que se van a comparar.</span><span class="sxs-lookup"><span data-stu-id="bec38-152">One of the version strings to compare.</span></span> 

* `version2` <span data-ttu-id="bec38-153">La otra cadena de versión que se compara.</span><span class="sxs-lookup"><span data-stu-id="bec38-153">The other version string to compare.</span></span>

#### <span data-ttu-id="bec38-154">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="bec38-154">CreateAsync</span></span> 

<span data-ttu-id="bec38-155">Crea un entorno de WebView2 de perenne con la versión de Edge instalada.</span><span class="sxs-lookup"><span data-stu-id="bec38-155">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="bec38-156">tarea pública estática asincrónica< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(String browserExecutableFolder, String userDataFolder, CoreWebView2EnvironmentOptions Options)</span><span class="sxs-lookup"><span data-stu-id="bec38-156">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="bec38-157">Parameters</span><span class="sxs-lookup"><span data-stu-id="bec38-157">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="bec38-158">La ruta de acceso relativa a la carpeta que contiene el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="bec38-158">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="bec38-159">userDataFolder se puede especificar para cambiar la ubicación de la carpeta de datos de usuario predeterminada para WebView2.</span><span class="sxs-lookup"><span data-stu-id="bec38-159">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="bec38-160">Opciones usadas para crear un entorno WebView2.</span><span class="sxs-lookup"><span data-stu-id="bec38-160">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="bec38-161">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="bec38-161">CreateCoreWebView2CompositionControllerAsync</span></span> 

> [!NOTE]
> <span data-ttu-id="bec38-162">Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="bec38-162">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="bec38-163">Cree de forma asincrónica una nueva vista de vista para usarla con el hospedaje visual.</span><span class="sxs-lookup"><span data-stu-id="bec38-163">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="bec38-164">tarea asincrónica pública< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="bec38-164">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="bec38-165">parentWindow es el HWND en el que la aplicación se conectará al árbol visual de la vista de ventana.</span><span class="sxs-lookup"><span data-stu-id="bec38-165">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="bec38-166">Este es el HWND que la aplicación recibirá una entrada de puntero o de mouse para la vista de ventana (y deberá usar SendMouseInput/SendPointerInput para reenviar).</span><span class="sxs-lookup"><span data-stu-id="bec38-166">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="bec38-167">Si la aplicación mueve el árbol visual WebView a una ventana distinta de otra, debe establecer CoreWebView2CompositionController. ParentWindow para actualizar el nuevo HWND primario del árbol visual.</span><span class="sxs-lookup"><span data-stu-id="bec38-167">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="bec38-168">Establezca la propiedad RootVisualTarget en el CoreWebView2CompositionController creado para proporcionar un objeto visual que hospede el árbol visual del explorador.</span><span class="sxs-lookup"><span data-stu-id="bec38-168">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="bec38-169">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bec38-169">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="bec38-170">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="bec38-170">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="bec38-171">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="bec38-171">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="bec38-172">Cree de forma asincrónica una nueva vista de vista previa.</span><span class="sxs-lookup"><span data-stu-id="bec38-172">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="bec38-173">tarea asincrónica pública< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="bec38-173">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="bec38-174">parentWindow es el HWND en el que se debe mostrar la vista en la vista previa y desde la que se recibe la entrada.</span><span class="sxs-lookup"><span data-stu-id="bec38-174">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="bec38-175">La vista en WebView agregará una ventana secundaria a la ventana proporcionada durante la creación de WebView.</span><span class="sxs-lookup"><span data-stu-id="bec38-175">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="bec38-176">El orden Z y otros elementos afectados por el orden de ventanas relacionados se verán afectados según corresponda.</span><span class="sxs-lookup"><span data-stu-id="bec38-176">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="bec38-177">Se recomienda que el identificador de modelo de usuario de la aplicación conjunto de aplicaciones para el proceso o la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bec38-177">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="bec38-178">Si no se establece ninguna, durante la creación de WebView un identificador de modelo de usuario de aplicación generado se establece en la ventana raíz de parentWindow.</span><span class="sxs-lookup"><span data-stu-id="bec38-178">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="bec38-179">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="bec38-179">CreateCoreWebView2PointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="bec38-180">Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="bec38-180">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="bec38-181">Cree un CoreWebView2ExperimentalPointerInfo vacío.</span><span class="sxs-lookup"><span data-stu-id="bec38-181">Create an empty CoreWebView2ExperimentalPointerInfo.</span></span>

> <span data-ttu-id="bec38-182">Public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="bec38-182">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="bec38-183">La CoreWebView2ExperimentalPointerInfo devuelta debe rellenarse con toda la información relevante antes de llamar a SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="bec38-183">The returned CoreWebView2ExperimentalPointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="bec38-184">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="bec38-184">CreateWebResourceResponse</span></span> 

<span data-ttu-id="bec38-185">Crear un nuevo objeto de respuesta de recursos Web.</span><span class="sxs-lookup"><span data-stu-id="bec38-185">Create a new web resource response object.</span></span>

> <span data-ttu-id="bec38-186">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(contenido de Stream, int StatusCode, String ReasonPhrase, encabezados de cadena)</span><span class="sxs-lookup"><span data-stu-id="bec38-186">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="bec38-187">La cabecera es la cadena de encabezado de respuesta sin formato delimitada por newline.</span><span class="sxs-lookup"><span data-stu-id="bec38-187">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="bec38-188">También es posible crear este objeto con una cadena de encabezados vacía y, a continuación, usar el CoreWebView2HttpResponseHeaders para construir los encabezados línea a línea.</span><span class="sxs-lookup"><span data-stu-id="bec38-188">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="bec38-189">Para obtener información sobre otros parámetros, consulte CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="bec38-189">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="bec38-190">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="bec38-190">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="bec38-191">Obtener la información de la versión del explorador incluido el nombre del canal si no es el canal estable o el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="bec38-191">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

> <span data-ttu-id="bec38-192">cadena estática pública [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(cadena browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="bec38-192">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

##### <span data-ttu-id="bec38-193">Parameters</span><span class="sxs-lookup"><span data-stu-id="bec38-193">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="bec38-194">La ruta de acceso relativa a la carpeta que contiene el borde incrustado.</span><span class="sxs-lookup"><span data-stu-id="bec38-194">The relative path to the folder that contains the embedded Edge.</span></span>

#### <span data-ttu-id="bec38-195">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="bec38-195">GetProviderForHwnd</span></span> 

> [!NOTE]
> <span data-ttu-id="bec38-196">Esta es una [API experimental](../../../concepts/versioning.md#experimental-apis) que se incluía con nuestra versión [de SDK 0.9.538-prerelease](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="bec38-196">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="bec38-197">Devuelve el proveedor de automatización de la interfaz de usuario de la CoreWebView2CompositionController que se corresponde con el HWND dado.</span><span class="sxs-lookup"><span data-stu-id="bec38-197">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="bec38-198">[GetProviderForHwnd](#getproviderforhwnd)de objeto público (HWND HWND)</span><span class="sxs-lookup"><span data-stu-id="bec38-198">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

